# Database_Design
컴퓨터공학과 데이터베이스설계 정리입니다. 

2022-03-02
![image](https://user-images.githubusercontent.com/58906858/222395361-293a98dd-31d7-42a0-a78b-9eff5a937ac2.png)      
![image](https://user-images.githubusercontent.com/58906858/222395653-839f49ac-ef08-478a-857c-ea48680ed09b.png)      
![image](https://user-images.githubusercontent.com/58906858/222396023-8f125511-29c6-4999-86f6-3d944e34b8e4.png)      
![image](https://user-images.githubusercontent.com/58906858/222396175-5d94319f-8f45-47f8-9c2a-81637d61118e.png)


## 데이터베이스
```
조직에 필요한 정보를 얻기 위해 논리적으로 연관된 데이터를 모아 구조적으로 통합해 놓은 것이다.
```

## 데이터베이스의 개념
```
데이터에 대한 통합된 데이터, 저장된 데이터, 운영 데이터, 공용 데이터를 말한다.
```

## 데이터베이스의 특징
```
실시간 접근성, 계속적인 변화, 동시 공유, 내용에 따른 참조 등이 있다.
```

## 데이터베이스 시스템의 구성
```
데이터베이스 관리 시스템(DBMS), 데이터베이스, 데이터 모델의 세 가지로 구성되어 있다.
```

## 정보 시스템의 발전
```
1. 파일 시스템 : DBMS가 없는 시스템으로, 데이터는 파일 단위로 저장되며 파일을 다루는 파일 서버가 있다.
2. 데이터베이스 시스템 : DBMS를 도입하여 데이터를 통합 관리하는 시스템이다.
3. 웹 데이터베이스 시스템 : 데이터베이스를 웹 브라우저에서 사용하도록 제공하는 시스템이다. 웹 서버와, JSP, PHP, 웹 데이터베이스
연동 언어들을 사용한다.
4. 분산 데이터베이스 시스템 : 여러 곳에 분산된 DBMS 서버를 연결하여 운영하는 시스템으로 대규모 응용 시스템에 이용된다.
```

## DBMS의 장점
```
데이터를 공유하여 중복 가능성을 최소화하고 이를 통해 데이터의 일관성을 유지한다. 또 데이터 구조가 변경되더라도 프로그램을
수정할 필요가 없어 데이터 독립성을 유지할 수 있다.
```

## SQL
```
데이터베이스 시스템에 사용하는 전용 언어로 데이터 정의어(DDL : Data Definition Language), 데이터 조작어(Data Manipulation language), 
데이터 제어어(Data Control Language)로 구성된다.

1. 데이터 정의어 : CREATE, ALTER, DROP 문과 같이 DBMS에 저장된 테이블의 구조를 정의한다.
2. 데이터 조작어 : SELECT, INSERT, DELETE, UPDATE 문과 같이 데이터를 검색, 삽입, 삭제, 수정하는 데 사용한다.
3. 데이터 제어어 : GRANT, REVOKE 문과 같이 데이터의 사용 권한을 관리한다.
```

## 데이터베이스 관리자(DBA)
```
데이터베이스 관리에 대한 모든 권한을 갖고 운영을 총괄하는 사람이다.
```

## 데이터 모델
```
데이터베이스 시스템에서 데이터를 저장하는 이론적인 방법에 관한 것으로, 데이터베이스에 데이터가 어떻게 구조화되어 저장되는 지를 
결정한다.
```

## 3단계 데이터베이스 구조
```
외부 단계, 개념 단계, 내부 단계로 나누어지며 각 단계는 외부 스키마, 개념 스키마, 내부 스키마로 구성된다.
스키마는 그리스어에서 유래된 단어로 데이터베이스의 조직이나 구조를 의미한다.

외부 스키마 : 서브 스키마라고도 부르며, 뷰의 개념이다. 개념 스키마 중 사용자에게 필요한 부분 스키마를 의미한다.
개념 스키마 : 전체 데이터베이스의 정의를 말하는 것으로 통합 조직별로 하나만 존재한다. 저장장치에 독립적으로 기술되며,
데이터와 관계, 제약사항, 무결성에 대한 내용이 포함된다.
내부 스키마 : 물리적 저장장치에서 데이터베이스가 실제로 저장되는 방법의 표현이다. 인덱스, 데이터 레코드의 배치 방법,
데이터 압축 등에 관한 사항이 포함된다.
```

## 데이터 독립성
```
3단계 데이터베이스 구조에서 하위 단계의 내용을 추상화하여 상위 단계에 그 세부 사항을 숨김으로써 한 단계 내의 변경에 대해서
다른 관계와 상호 간섭이 없도록 하는 것이다.

1. 논리적 데이터 독립성 : 외부 단계와 개념 단계 사이의 독립성으로, 개념 스키마가 변경되더라도 외부 스키마에는 영향을 미치지 않도록 지원한다.
2. 물리적 데이터 독립성 : 내부 단계와 개념 단계 사이의 도긻성으로, 저장장치 구조 변경과 같이 내부 스키마가 변경되어도 개념 스키마에는 영향을
미치지 않도록 지원한다.

논리적 -> 개념적 -> 물리적  ( 화살표 오른쪽에 영향을 미치지 아니하게 함 독립성!!)
```

## 데이터 모델링 중요성
```
데이터베이스 설계 - 건축의 지반 설계와 같다. 
```

## 데이터의 세계
```
현실 세계(개체) : 개체 - 특성 - 값
개념 세계(개념) : 개체 - 속성 - 값
컴퓨터세계(데이터) : 레코드타입 - 필드 - 값
```
