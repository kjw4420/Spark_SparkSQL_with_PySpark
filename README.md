# Spark_SparkSQL_with_PySpark
# 실습파일 목록
### 1. PySpark_UDF: UDF(User Defined Function)실습
- DataFrame 또는 SQL에서 적용할 수 있는 사용자 정의 함수
- 하나의 레코드로부터 다수의 레코드 생성하기
  * Order 데이터의 items 필드에서 다수의 Order Item 레코드 만들기
<img width="702" alt="스크린샷 2024-07-04 오전 12 52 17" src="https://github.com/kjw4420/Spark_SparkSQL_with_PySpark/assets/97749184/d26dc3f0-e3fa-491e-b594-6d7629295aed">

---
### 2. PySpark_SQL_JOIN: JOIN 실습
- JOIN by DataFrame
  * INNER JOIN
  * LEFT JOIN
  * RIGHT JOIN
  * FULL OUTER JOIN
  * CROSS JOIN
  * SELF JOIN
- JOIN by SparkSQL
  * INNER JOIN
  * LEFT JOIN
  * RIGHT JOIN
  * OUTER JOIN
  * CROSS JOIN
  * SELF JOIN
---
### 3. PySpark_SQL_총_매출이_가장_많은_사용자_10명_찾기
- user_session_channel, session_timestamp, session_transaction 테이블 사용
- Redshift 상에서 테이블 가져와 월별 채널별 매출과 방문자 정보 계산
- 총 매출이 가장 많은 사용자 10명 찾기
  * 3개의 테이블을 각각 데이터프레임으로 로딩
  * 데이터프레임 별로 테이블 이름 지정
  * SparkSQL로 처리
    * 조인 방식 결정(조인키, 조인방식(INNER, LEFT, RIGHT, FULL)
  * 간단한 지표부터 계산
- 다음 형태의 결과 도출
  * 매출은 refund 포함
  <img width="465" alt="스크린샷 2024-07-04 오전 12 58 32" src="https://github.com/kjw4420/Spark_SparkSQL_with_PySpark/assets/97749184/b665e47f-2a62-49c6-aa91-ec1510b3de53">

---
### 4. PySpark_SQL_월별_채널별_매출과_방문자_정보
- user_session_channel, session_timestamp, session_transaction 테이블 사용
- Redshift 상에서 테이블 가져와 월별 채널별 매출과 방문자 정보 계산
- 월별 채널별 매출과 방문자 정보 계산
  * 3개의 테이블을 각각 데이터프레임으로 로딩
  * 데이터프레임 별로 테이블 이름 지정
  * Spark SQL로 처리
    * 조인 방식 결정(조인키, 조인방식(INNER, LEFT, RIGHT, FULL)
- 다음 형태의 결과 도출
   <img width="461" alt="스크린샷 2024-07-04 오전 1 04 12" src="https://github.com/kjw4420/Spark_SparkSQL_with_PySpark/assets/97749184/3c70bf31-80a2-4f8b-81e3-f3d4aba96f78">
  * 월별 채널별 총 방문자 계산
  * 월별 채널별 총 방문자와 구매 방문자 계산
  * 월별 채널별 총 매출액 (리펀드 포함), 총 방문자, 매출 발생 방문자, 전환률 계산
---
### 5.PySpark_SQL_사용자별로_처음_채널과_마지막_채널_알아내기
- user_session_channel, session_timestamp, session_transaction 테이블 사용
- Redshift 상의 각각의 테이블을 데이터프레임으로 로딩
- 사용자별로 처음 채널과 마지막 채널 알아내기
  * ROW_NUMBER 이용
- 다음 형태의 결과 도출
<img width="461" alt="스크린샷 2024-07-04 오전 1 12 19" src="https://github.com/kjw4420/Spark_SparkSQL_with_PySpark/assets/97749184/751e77e2-ce6e-44e7-9790-f70a7546d320">
---   
### 6. PySpark_Hive_테이블
- DataFrame을 Managed Table로 저장
- 'default'말고 새로운 데이터베이스 사용하기
- Spark SQL로 Managed Table 사용하기(CTAS)

---
### 7. PySpark 유닛 테스트
- 유닛 테스트: 코드 상의 특정 기능을 테스트하기 위해 작성된 코드
- unittest 사용
- 코드와 SQL 검증을 위한 유닛 테스트
