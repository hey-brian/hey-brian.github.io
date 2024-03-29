---
title: Oracle SQL procedure에서 random characters(무작위 문자) 사용
feed: show
date: 2024-03-22
time: 08:30:16
tags: 
permalink: 
format: 
comments: true
imageNameKey: oracle_sql_proc
---
# 테스트용 테이블 생성하기 
### Create a table
- 아래와 같이 하나의 컬럼을 가지는 test용 table을 생성한다.
``` sql
CREATE TABLE random_strings_table (
  random_string VARCHAR2(15)
);
```

# Random characters 생성하기
### Random characters 컨셉
- 15자리수로 영어 대소문자, 숫자 조합으로 경우의 수를 크게 잡고 이를 unique key로 사용하고자 한다.
- DBMS_RANDOM.STRING 함수는 랜덤 문자열을 생성한다. 
	- 첫 번째 인자는 문자열의 형태를 지정하고, 두 번째 인자는 문자열의 길이를 지정한다.
- 1) 문자열의 형태를 지정하는 첫 번째 인자는 다음과 같은 옵션을 사용할 수 있으며, 여기에서는 X 옵션을 사용한다.
	- 'U' - 대문자 알파벳 문자
	- 'L' - 소문자 알파벳 문자
	- 'A' - 대소문자 알파벳 문자
	- 'X' - 대소문자 알파벳 및 숫자 문자
- 2) 문자열의 길이는 두 번째 인자로 지정할 수 있으며, 길이는 고정된 값이 아닌 랜덤한 값을 사용할 수도 있다.
``` sql
SELECT DBMS_RANDOM.STRING('X', 15) FROM DUAL; 
-- 15자리 대소문자 알파벳 및 숫자를 조합한 랜덤 문자열 생성 

SELECT DBMS_RANDOM.STRING('X', DBMS_RANDOM.VALUE(10, 20)) FROM DUAL; 
-- 10~20자리 대소문자 알파벳 및 숫자를 조합한 랜덤 문자열 생성 
```

### 앞에서 생성한 테이블에 Random characters를 삽입
``` sql
CREATE OR REPLACE PROCEDURE insert_random_string IS
	-- 변수를 선언
	randomnum VARCHAR2(15); 
BEGIN     
	-- 선언된 변수에 15글자의 Random characters
	randomnum := DBMS_RANDOM.STRING('X', 15);      
	
	EXECUTE IMMEDIATE 'INSERT INTO random_strings_table (random_string) VALUES (:1)'   
	USING randomnum;
	COMMIT; 
END;
```


_끝_