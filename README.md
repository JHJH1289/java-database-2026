# java-database-2026
자바개발자 과정 데이터베이스 리포지토리

---
## Day 01
### 데이터 / 정보
데이터는 단순한 컴퓨터환경의 특정 값을 의미한다. 정보는 이러한 데이터에 의미를 부여한 것.

### 데이터베이스 (Database : DB)
데이터를 기반으로 하는 관리 시스템을 의미. 데이터를 모아둔 장소를 의미하기도 함.
- DataBase Management System -> DBMS 라고 부른다. 줄여서 DB라고도 함.
- 대부분 기업의 `도메인 정보`를 저장하고 있음

![alt text](image-1.png)

### 데이터 베이스 종류
- 관계형 데이터베이스 (RDBMS)
    - Oracle - 학습할 DB
    - SQLServer - Microsoft사 제품, Oracle보다 성능이 낮음
    - MySQL - 오픈소스지녕ㅇ에서 Oracle로 합병
    - MariaDB - MySQL 개발자들이 다시 만든 오픈소스 DB
    - PostgreSQL

- NoSQL 데이터베이스(빅데이터...)
    - Redis
    - MongoDB
    
- In-Memory 데이터베이스
    - SAP HANA (겁나 빠름)

### 오라클 설치 방법
 1. 로컬 설치

 2. 도커 설치(클라우드 동일)

 ### 오라클 설치 이전
 1. 도커 설치 - DevOps의 필수품
    - https://www.doker.com/
    - Download Docker Desktop 버튼 클릭
    - Download for Windows - AMD64 선택
2. Docker command 사용



    - 컨테이너 실행
    ```
    docker run -d --name oracle-xe -p 1521:1521 -e ORACLE_PASSWORD=P12345s! gvenzl/oracle-xe:21-slim
    ```

### DBeaver 사용법

- Database Navigator 에서 DB연결 시작

    ![alt text](image-5.png)

    - 마우스 오른쪽버튼 > Create > Connection

        ![alt text](image-6.png)

- 연결정보 입력 Test Connection
- 입력 시 주의사항 : port번호 확인, Database 이름변경 Oracle -> XE로, Username, Password 일치

    ![alt text](image-7.png)


### 기본 사용법

- DBeaver
    - 연결된 XE - java > Schema(Database와 같은의미) 확장 > JAVA 선택
    - 마우스 오른쪽 버튼 > SQL 편집기
    - 글자 크기 변경 > 메뉴 윈도우 > 환경 설정
        - User Interface > 모양 > 색상 및 글꼴 > DBeaver Fonts > Monospace font를 편집

    ![alt text](image-9.png)

- 샘플 데이터베이스 생성

    1. 테이블 생성 : [쿼리](./day01/1.sample_schemas.sql)
    2. 시퀀스 생성 : [쿼리](./day01/2.sequences.sql)
    3. 부서데이터 추가 : [쿼리](./day01/3.department_datas.sql)
    4. 직원데이터 추가 : [쿼리](./day01/4.employee_datas.sql)
    5. 고객데이터 추가 : [쿼리](./day01/5.customer_datas.sql)
    6. 상품데이터 추가 : [쿼리](./day01/6.product_datas.sql)
    7. 주문과 주문상세데이터 추가 : [쿼리](./day01/7.order_order_item_datas.sql)

- 간단 연습 : [쿼리]
    - DB파일은 확장자를 `.sql` 로 한다
    - 하나의 며령으로 ; 으로 끝나는 문장을 쿼리(query) 로 지칭
    - 쿼리문은 대소문자 구분 없음
    - DBeaver에서 쿼리 한줄 실행은  ctrl + ENTER
    - 여러줄 동시실행은 `Alt+x`

- SQL(Structured Query Language)
    - 구조화된 질의 언어
    - 관계형 데이터 베이스