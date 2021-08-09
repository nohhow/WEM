# ETC. 개발관련 용어 정리
> 현장실습 과정동안에 듣게 된 용어와 내용들을 순서 없이 나열한 자료입니다.  

### OLTP
온라인 트랜잭션 처리

### Batch Processing
일괄 처리 라고도 하는 과정으로서 실시간으로 요청에 의해서 처리되는 방식이 아닌 일괄적으로 한꺼번에 대량의 프로세스를 처리하는 방식이다.

### Master Detail 구조(1:N)
* list in list (SUB list)
* 1:N (REFERRENCE variable 사용)

### N:N의 관계
N:N 관계에서는 중복이 발생할 가능성이 다분하기 때문에 N:N관계를 갖는 테이블 사이에 중간 테이블을 두어 1:N 관계로 풀어내줘야한다.
-> WEM에서는 Reference Field(Variable 사용)

### REFERRENCE FIELD
가 갖는 값 : ROW ID
* RDB에서도 rowID는 있음. 그러나 안보여줌 (접근은 가능)

WEM에서 rowID 는 고유의 ROW ID 와 기본 ID를 포함하여 생성되는 것으로 추정 됨.

### Modal 
팝업화면 -> WEM에서는 Overlay라고 함.
[Building no code enterprise applications | WEM APAC](https://wemapac.com/)

### Elastic Search
연관검색어 서치

### csv 
구분자를 통해서 정리된 데이터

### xml 
확장형 mark up language

### json 
심플하게 데이터 표현 xml의 오버헤드를 줄이기 위해 출현  
JavaScriptObjectNotation

### DB 에 isdeleted를 넣는 이유
- 실제 db에서 삭제하는 것이 아닌 보여지는 값에서 만 제외함
- 이 데이터들은 분석에 사용 -> 빅데이터

#현장실습#
