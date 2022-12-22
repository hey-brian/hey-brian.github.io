---
title: pandas(판다스) 쿼리(query) 조회
feed: show
date : 2022-12-20
tags : [📝️/🌞️, 🐍/pandas]
comments: true
---

---

pandas query를 사용한 조회 방법을 정리한다.
> 비교, in, not in, 논리, index, 변수 참조, 함수 참조, 문자열 관련 쿼리

![](/attachments/Pasted_image_20221221073033.png)

# 1. 비교연산자
## 1.1 비교연산자(\=\=)
``` python
query1 = 'number1 == 10'
result1 = df.query(query1)
```
![](/attachments/Pasted_image_20221221073055.png)

## 1.2 비교연산자(\!\=)
``` python
query2 = 'number1 != 10'
result2 = df.query(query2)
```
![](/attachments/Pasted_image_20221221073218.png)

## 1.3 in 연산자(in, \=\=과 동일)
#### \=\=
``` python
query3 = 'number1 == [10,12]'
result3 = df.query(query3)
```
![](/attachments/Pasted_image_20221221073300.png)

#### in
``` python
query4 = 'number1 in [10,12]'
result4 = df.query(query4)
```
![](/attachments/Pasted_image_20221221073402.png)


## 1.4 not in 연산자(not in, \!\=과 동일)
#### \!\=
``` python
query5 = 'number1 != [10,12]'
result5 = df.query(query5)
```
![](/attachments/Pasted_image_20221221073550.png)

#### not in
``` python
query6 = 'number1 not in [10,12]'
result6 = df.query(query6)
```
![](/attachments/Pasted_image_20221221073626.png)

# 2 논리 연산자(and, or, not)
## 2.1 AND
``` python
query7 = '(number1 in [10,12]) and (number2 in [200, 300]) '
result7 = df.query(query7)
print('원본 DataFrame vs. number1이 10과 12범위 포함되면서 number2가 200과 300범위 포함되는 데이터')
```
![](/attachments/Pasted_image_20221221073936.png)

## 2.2 OR
``` python
query8 = '(number1 in [10,12]) or (number2 in [200, 300]) '
result8 = df.query(query8)
print('원본 DataFrame vs. number1이 10과 12범위 포함되거나 number2가 200과 300범위 포함되는 데이터')
```
![](/attachments/Pasted_image_20221221074042.png)

## 2.3 NOT
``` python
query8 = '(number1 in [10,12]) and not (number2 in [200, 300]) '
result8 = df.query(query8)
print('원본 DataFrame vs. number1이 10과 12범위 포함되지만 number2가 200과 300범위 포함 안 되는 데이터')
```
![](/attachments/Pasted_image_20221221074131.png)

# 3. index 사용
``` python
condi1 = 11
result13 = df.query('index > 2')
```
![](/attachments/Pasted_image_20221221074231.png)

# 4. 변수 참조 쿼리
## 4.1 \@
``` python
condi1 = 11
query9 = 'number1 == @condi1'
result9 = df.query(query9)
```
![](/attachments/Pasted_image_20221221074321.png)

## 4.2 f-string
``` python
condi1 = 11
query10 = f'number1 == {condi1}'
result10 = df.query(query10)
```
![](/attachments/Pasted_image_20221221074408.png)

# 5. 함수 참조 쿼리
## 5.1 외부 함수 참조
``` python
def cust_min(data):
    return min(data)
```
``` python
condi1 = 11
query11 = f'number1 == @cust_min([10, 11, 12, 13])'
result11 = df.query(query11)
```
![](/attachments/Pasted_image_20221221074554.png)

## 5.2 외부 함수, 외부 변수 참조
``` python
condi1 = 11
query12 = f'number1 == @cust_min(@df.number1)'
result12 = df.query(query12)
```
![](/attachments/Pasted_image_20221221074726.png)

# 6. 문자열 관련 쿼리
## 6.1 특정 문자 포함 여부 (대문자 소문자 구분)
``` python
result14 = df.query('name.str.contains("a")')
print('원본 DataFrame vs. name에 \'a\'가 포함된 데이터 (case의 default는 True 확인)')
```
![](/attachments/Pasted_image_20221221074844.png)

## 6.2 특정 문자 포함 여부 (대문자 소문자 구분 안 함)
``` python
result15 = df.query('name.str.contains("a", case=False)')
print('원본 DataFrame vs. name에 \'a\'가 포함된 데이터 (case 구분 안 함)')
```
![](/attachments/Pasted_image_20221221075002.png)

## 6.3 특정 문자로 시작
``` python
result16 = df.query('name.str.startswith("a")')
```
![](/attachments/Pasted_image_20221221075040.png)

## 6.4 특정 문자로 종료
``` python
result17 = df.query('name.str.endswith("c")')
```
![](/attachments/Pasted_image_20221221075115.png)


_끝_
