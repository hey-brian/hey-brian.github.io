---
title: Scikit-Mobility(skmob) tutorial
feed: show
date : 2023-03-09
time : 22:48:21
tags : []
format: list
comments: true
---

# 📝Scikit-Mobility ([official github](https://github.com/scikit-mobility/scikit-mobility))
- GPS 좌표/이동경로 분석용 파이썬 패키지 
- 설치방법

``` shell
# pip 설치
pip install scikit-mobility
# conda 설치
conda install -c conda-forge scikit-mobility
```
``` python
# google colab 사용
!apt-get install -qq curl g++ make
```
``` python
!curl -L http://download.osgeo.org/libspatialindex/spatialindex-src-1.8.5.tar.gz | tar xz
```
``` python
import os
os.chdir('spatialindex-src-1.8.5')
!./configure
!make
!make install
!pip install rtree
!ldconfig
!pip install scikit-mobility
```

# Trajectories, Flows, and Tessellations

## TrajDataFrame
#### Format
- 입력인자: lat, lng, datetime
- optional: uid(user id), tid(trajectory id)
- 

![](/attachments/Pasted_image_20230306084333.png)

(\=\-\= image by author)


#### Created from
- skmob.TrajDataFrame.from_file()
- list, numpy array, dataframe, text file
- Attributes
	- crs(coordinate reference system)
		- default epsg:4326 (lat, lng)
	- optional
		- customized parameters를 dictionary type으로 자유롭게 추가 가능
- Writing
	- timezone 정보는 저장할 때 휘발하기 때문에, parameters로 미리 등록해놓는게 좋음
``` python
skmob.write(tdf, './tdf.json')
```

- Reading
``` python
skmob.read('./tdf.json')
```
	
#### Plotting
``` python
tdf.plot_trajectory()
```
![](/attachments/Pasted_image_20230306084521.jpeg)

(\=\-\= image by author)

## Tessellation
#### Format
![](/attachments/Pasted_image_20230306084716.jpeg)

(\=\-\= image by author)

- Tessellation: tile_id, geometry 등 (geopandas)
``` python
tessellation = \
	gpd.GeoDataFrame\
	.from_file('~.geojson')
```
- tile_id
	- tessellation column 이름

#### from dataframe
> - TrajDataFrame -> GeoDataFrame -> GeoDataFrame을 기반으로 tilers를 만든다. = tessellation
> - TrajDataFrame의 이동경로를 모두 포함하는 (직사각형) 영역의 tiles를 생성한다.

tdf 샘플
``` python
a_tdf = tdf[tdf['uid']==1]
``` 
![](/attachments/Pasted_image_20230306091231.png)

(\=\-\= image by author)

``` python
a_tdf.plot_trajectory(
	zoom=12, 
	weight=3, 
	opacity=0.9,
	tiles='Stamen Toner', 
	start_end_markers=True)
``` 
![](/attachments/Pasted_image_20230306091323.jpeg)

(\=\-\= image by author)

``` python
# tdf contains trajectories from GeoLife
a_gdf = a_tdf.to_geodataframe()
a_gdf.head()
```
![](/attachments/Pasted_image_20230306091411.jpeg)

(\=\-\= image by author)

NOTE: It accepts also geodataframe with list of polygons
``` python
a_tessellation = tilers.tiler.get(
	"squared", 
	base_shape=a_gdf, 
	meters=100000)
``` 
![](/attachments/Pasted_image_20230306091518.jpeg)

(\=\-\= image by author)

``` python
map_f = plot.plot_gdf(
	a_tessellation, zoom=11,
	popup_features=['tile_ID'], 
	style_func_args=tess_style)
a_tdf.plot_trajectory(
	map_f=map_f, 
	start_end_markers=False, 
	hex_color='red')
```
![](/attachments/Pasted_image_20230306091614.jpeg)

(\=\-\= image by author)

#### TrajDataFrame을 Tessellation에 매핑
a_tdf가 있는데 이걸 a_tessellation 어느 tile에 매핑되는지?
``` python
mapped_a_tdf = a_tdf.mapping(a_tessellation)
```
![](/attachments/Pasted_image_20230306091810.jpeg)

(\=\-\= image by author)

#### Select points within a tessellation
``` python
haidian_tess = tilers.tiler.get(
	"squared", 
	base_shape='Haidian, China', 
	meters=1000)
map_f = plot.plot_gdf(
	haidian_tess, 
	zoom=11, 
	popup_features=['tile_ID'], 
	style_func_args=tess_style)

#$% map_f에 tdf를 올린다.
tdf.plot_trajectory(
	map_f=map_f, 
	hex_color='blue')
```
![](/attachments/Pasted_image_20230306100742.jpeg)

(\=\-\= image by author)

#$% tdf를 tessellation에 매핑하여 결과 tdf(mapped_tdf)를 만든다.
``` python
mapped_tdf = tdf.mapping(
	haidian_tess, remove_na=True) 
# 매핑 안 되는 trajectories는 제외
map_f = plot.plot_gdf(
	haidian_tess, zoom=11, 
	popup_features=['tile_ID'], 
	style_func_args=tess_style)

#$% map_f에 mapped_tdf를 올린다.
mapped_tdf.plot_trajectory(
	map_f=map_f, 
	start_end_markers=False)
```
![](/attachments/Pasted_image_20230306101836.jpeg)

(\=\-\= image by author)

```python
fdf = tdf.to_flowdataframe(
	tessellation=haidian_tess, 
	self_loops=True)
```
![](/attachments/Pasted_image_20230306113431.png)

(\=\-\= image by author)

``` python
fdf.plot_flows(flow_exp=0., zoom=11)
```
![](/attachments/Pasted_image_20230306113448.jpeg)

(\=\-\= image by author)

``` python
map_f = plot.plot_gdf(
	haidian_tess, 
	zoom=11, 
	popup_features=['tile_ID'], 
	style_func_args=tess_style)
mapped_tdf.plot_trajectory(
	map_f=map_f, 
	start_end_markers=False)
fdf.plot_flows(
	map_f=map_f, 
	flow_exp=0., 
	zoom=11)
```
![](/attachments/Pasted_image_20230306113704.jpeg)

(\=\-\= image by author)

## FlowDataFrame
#### Format
- 입력인자: origin, destination, flow(# of data)
- optional: datetime
- 

![](/attachments/Pasted_image_20230306084611.png)

(\=\-\= image by author)	

#### Created from
- skmob.TrajDataFrame.from_file()
	- tdf = skmob.FlowDataFrame.from_file()
	- 입력인자: 파일path, tessellation = tessellation, tile_id = 'tile_id', sep

#### Plotting
``` python
fdf.plot_tessellation(
	popup_features = [
		'tile_id', 
		'population'])
```
![](/attachments/Pasted_image_20230306085124.jpeg)

(\=\-\= image by author)

``` python
fdf.plot_flows(flow_color='green')
```
![](/attachments/Pasted_image_20230306085201.png)

(\=\-\= image by author)

``` python
tess_style = {
	'color':'gray', 
	'fillColor':'gray', 
	'opacity':0.2}

# plotting tessellation
map_f = fdf.plot_tessellation(
	style_func_args=tess_style) 

# plotting flow
fdf[fdf['origin'] == '36061'].plot_flows(
	map_f=map_f, 
	flow_exp=0., 
	flow_popup=True) 
```
![](/attachments/Pasted_image_20230306085314.jpeg)

(\=\-\= image by author)

# Processing mobility data
## Mobility data processing
#### 1) filtering
``` python
from skmob.preprocessing import filtering
max_speed_kmh = 500.
user1_f_tdf = filtering.filter(
	user1_tdf, 
	max_speed_kmh=max_speed_kmh)
```
- tdf: "lat, lng, datetime"
- 적용 후 parameter (dictionary)에 filter 내역 기록됨. 
- 
![](/attachments/Pasted_image_20230306154126.png)

(\=\-\= image by author)

``` python
# indicator adds column _merge
merged = user1_tdf.merge(
	user1_f_tdf, 
	indicator=True, 
	how='outer') 
# user1_tdf에 user1_f_tdf가 
# 속하기 때문에 실행

diff_df = merged[
	merged['_merge'] == 'left_only']
diff_df
```

``` python
map_f = unfiltered_tdf.plot_trajectory(
	zoom=14, 
	weight=10, 
	opacity=0.5, 
	hex_color='black') 
	#, tiles='Stamen Toner')

filtered_tdf.plot_trajectory(
	map_f=map_f, 
	hex_color='red')
```
![](/attachments/Pasted_image_20230306155528.jpeg)

(\=\-\= image by author)

#### 2) compress
``` python
from skmob.preprocessing import compression
```
#$% spatial_radius_km=0.1 kilometers 안에 있는 gps 좌표들을 모두 merging!
``` python
skmob.preprocessing.compression(
	tdf, 
	spatial_radius_km=0.1)
```
- 적용 후 parameter (dictionary)에 filter 내역 기록됨. (\=\-\= image by author)
- 
![](/attachments/Pasted_image_20230306160404.png)

- 압축률을 확인해보면, 비슷한 좌표에서 측정된 GPS 좌표가 많았다는 것을 확인할 수 있다. (\=\-\= image by author)
- 
![](/attachments/Pasted_image_20230306160537.jpeg)

- 원본 데이터와 다르게 gps 좌표들이 제거되어 경로가 일부 변경된 것을 확인할 수 있다. (\=\-\= image by author)
- 
![](/attachments/Pasted_image_20230306160948.jpeg)

#### stop detection
``` python
user1_scf_tdf = detection\
	.stay_locations(
		user1_cf_tdf, 
		minutes_for_a_stop=20.0,
		patial_radius_km=0.2, 
		leaving_time=True)
user1_scf_tdf.head()
```
- 최소 minutes for a stop 이상, spatial radius km * stop radius factor 내 머물러 있을 경우 stop이라고 인식 (\=\-\= image by author)
- 
![](/attachments/Pasted_image_20230306161610.jpeg)
 - 적용 후 parameter (dictionary)에 filter 내역 기록됨. (\=\-\= image by author)
 - 
![](/attachments/Pasted_image_20230306161843.png)

#### Visualise the compressed trajectory and the stops
- stops를 시각화하면 기본적으로 아래의 attributes를 확인할 수 있다.
	- User ID
	- Coordinates of the stop (click to see the location on Google maps)
	- Arrival time
	- Departure time
``` python
map_f = user1_scf_tdf.plot_trajectory(
	max_points=1000, 
	hex_color='blue', 
	start_end_markers=False)
user1_scf_tdf.plot_stops(
	map_f=map_f, 
	hex_color='red')
``` 
![](/attachments/Pasted_image_20230306163454.jpeg)

(\=\-\= image by author)

#### Stops define trips
``` python
dt1 = user1_scf_tdf.iloc[0].leaving_datetime
dt2 = user1_scf_tdf.iloc[1].leaving_datetime

# select all points between the first two stops
user1_tid1_tdf = user1_tdf[
	(user1_tdf.datetime >= dt1) & \
	(user1_tdf.datetime <= dt2)]
user1_tid1_tdf.head()

user1_tid1_map = user1_tid1_tdf\
	.plot_trajectory(
		zoom=12, 
		weight=5, 
		opacity=0.9,
		hex_color='red', 
		tiles='Stamen Toner', )
```
![](/attachments/Pasted_image_20230306163746.jpeg)

(\=\-\= image by author)

``` python
from skmob.utils.gislib import getDistanceByHaversine
from skmob.measures.individual import distance_straight_line
```
``` python
# take origin and destination of the trip
start_loc = user1_tid1_tdf.iloc[0]\
	\[\['lat', 'lng'\]\]
end_loc = user1_tid1_tdf.iloc[-1]\
	\[\['lat', 'lng'\]\]

# compute distance between 
# origin and destination
print(
	"distance:", 
	getDistanceByHaversine(end_loc, start_loc))

### distance: 5.568109302866517

# 전체 이동거리의 합
distance_straight_line(user1_tid1_tdf)
### 8.60392
```

#### Find clusters of stops
- 비슷한 stops 위치를 DBSCAN clustering을 하고, cluster ID의 숫자가 낮을수록 더 자주 방문한 곳(stops)이다.
- user1_scf_tdf으로 계산된 stops에 대해 clustering을 적용하는 것이기 때문에, user1_clscf_tdf 데이터의 개수는 user1_scf_tdf와 동일하다.
``` python
from skmob.preprocessing import clustering
user1_clscf_tdf = clustering.cluster(
	user1_scf_tdf, 
	cluster_radius_km=0.1, 
	min_samples=1)
user1_clscf_tdf.head()
```
- user1_clscf_tdf (\=\-\= image by author)

![](/attachments/Pasted_image_20230306161610.jpeg)

- user1_clscf_tdf (\=\-\= image by author)

![](/attachments/Pasted_image_20230307134757.jpeg)

- parameters (\=\-\= image by author)

![](/attachments/Pasted_image_20230307135259.png)

#### Visualise clustered stops  
``` python
map_f = user1_cf_tdf.plot_trajectory(
	max_points=1000, 
	hex_color='blue', 
	start_end_markers=False)
user1_clscf_tdf.sort_values('cluster')\
	.query("cluster < 5")\
	.plot_stops(map_f=map_f)
```
![](/attachments/Pasted_image_20230307135740.jpeg)

(\=\-\= image by author)

## examples
``` python
sm_tess = tilers.tiler.get(
	'squared', 
	base_shape='San Mateo, USA', 
	meters=5000)
map_filtered_tdf = filtered_tdf.mapping(
	sm_tess, 
	remove_na=True)
map_compressed_tdf = compressed_tdf.mapping(
	sm_tess, 
	remove_na=True)
```
tessellation부터 시각화할 때는 plot 패키지 자체에서 plot_gdf를 실행
``` python
map_f = plot.plot_gdf(
	sm_tess, 
	zoom=9, 
	style_func_args={
		'color':'gray',
		'fillColor':'gray', 
		'opacity':0.2})
map_f = map_filtered_tdf.plot_trajectory(
	map_f=map_f, 
	max_points=None, 
	weight=5,
	hex_color='black', 
	opacity=0.5)
map_compressed_tdf.plot_trajectory(
	map_f=map_f, 
	max_points=None, 
	hex_color='red')
```
![](/attachments/Pasted_image_20230307144702.jpeg)

(\=\-\= image by author)

_끝_
