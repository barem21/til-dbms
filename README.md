# 데이터베이스 모델링 및 ERD, MySQL 활용하기

- MySQL (DBMS) : RDBMS를 다룬다. (Relation:관계)

## 1. 요구사항 분석

- 회의 참석(회의록)
- 회의록 검토 후 각 사항을 요구사항 분석(요구사항 정의서, 업무 지시서)

## 2. 요구사항 분석을 하는 이유

- 각 내용의 속성을 찾고, 분류
- 분류된 내용을 모아서 Entity를 생성한다.
- Entity와 Entity 간의 관계를 찾는다.
- 요구사항 정의서 작성

### 2.1. 요구사항 분석 예

- 고객은 고객코드, 고객명, 전화번호, 이메일, 주소(기본주소, 상세주소), 지역, 가입일로 되어있다.
- 고객은 지역별로 관리되도록 한다.
- 지역은 지역코드와 지역명으로 되어 있고 지역명은 대한민국의 지역코드(02:서울특별시)를 이용한다.
- 한 지역에는 여려 고객이 있을 수 있다.
- 제품은 제품코드, 제품명, 제품색상, 가격으로 되어있다.
- 하나의 제품은 여러 색상을 가질 수가 있다.
- 고객은 등록된 제품을 구매할 수 있다.
- 한 명의 고객은 여러 제품을 구매 할 수 있고, 하나의 제품은 여러 고객이 구매할 수 있다.
- 고객이 제품을 구매 시 구매수량과 구매일자를 기록한다.

### 2.2. 요구사항 정의서, 또는 업무 기술서(회사마다 포멧이 다름)

![Image](https://github.com/user-attachments/assets/876cbcc1-50c2-49ba-937c-663a70c747af)

### 2.3. 속성(Attribute)을 찾기 후 Entity 정의하기

- 데이터베이스 설계 전문가는 Entity를 정의 후 속성을 선별해 나간다.
- 신입 데이터 설계자는 속성을 선별 후 Entity를 정의해 나간다.

## 2.3.1. 먼저 Entity 항목 정리 : 명사 소문자 추천

![Image](https://github.com/user-attachments/assets/b51d8ff7-495c-49b9-8eb8-65d27ce99a15)

## 2.3.2. Entity와 Entity의 관계 정리 : 동사 소문자 추천

![Image](https://github.com/user-attachments/assets/53747688-e144-4edf-9c48-c6ce20fe0d12)

## 3. ERD 그리기

### 3.1. 개념적 모델링

- E-R 다이어그램 : Entity Relationship Diagram
- https://app.diagrams.net
  ![Image](https://github.com/user-attachments/assets/b862d97b-c4d1-4d98-82a9-074b6a775e81)

- 고객
  ![Image](https://github.com/user-attachments/assets/6f566bca-beb9-4277-851d-15e9ac0520b2)

- 고객 PK 후보
  ![Image](https://github.com/user-attachments/assets/efa54857-fe82-4674-bb5c-d5da9c464de1)

- 지역
  ![Image](https://github.com/user-attachments/assets/62ab89a6-47a6-49da-85f6-69285a522518)

- 제품
  ![Image](https://github.com/user-attachments/assets/2147cff0-ed15-4264-b1f8-97d9e8bcc6c8)

### 3.2. Relaltion 표현하기

- 개체와 개체가 맺고 있는 연관성을 표현
  ![Image](https://github.com/user-attachments/assets/53747688-e144-4edf-9c48-c6ce20fe0d12)

#### 고객은 제품을 구매한다.

![Image](https://github.com/user-attachments/assets/b89f0b1a-a090-4e2e-aaa4-21f89abaef41)

## 4. Logical Data Modeling (논리적 모델링)

- 개념적 스키마를 표현식 또는 테이블 형식으로 표현함
- Entity 의 속성 데이터 타입, 길이, null 허용여부, 기본값, 제약 조건등을 세부적으로 작성후 문서화
- 즉 `테이블정의서` 를 생성함. (도구는 다양합니다.)

![Image](https://github.com/user-attachments/assets/bb3d3b7a-e10a-4c15-9bb1-82a98bfd06a5)
