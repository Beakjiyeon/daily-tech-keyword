## GraphQL
### 세줄 요약
* 페이스북에서 만든 쿼리 언어
* 웹 클라이언트가 데이터를 서버로부터 효율적으로 가져오기 위해 사용한다.


### 특징
* 서버사이드 그래프큐엘 어플리케이션은 쿼리를 입력 받아 처리한 결과를 다시 클라이언트로 응답한다.
* 특정 데이터베이스나 플랫폼에 종속적이지 않다.
* 일반적으로 L7 계층의 http post 메소드와 웹소켓 프로토콜을 활용한다. 
* 여러 번 네트워크 호출을 할 필요 없이 한번의 네트워크 호출로 처리할 수 있다.


### REST API 와 차이
* REST API 는 url, method를 조합하기 떄문에 다양한 엔드포인트가 존재한다.
* GraphQL은 단 하나의 엔드포인트가 존재하고, 쿼리의 조합을 통해 응답 데이터의 종류를 결정한다.
* REST API 는 각 엔드포인트마다 sql 쿼리가 달라지는 반면, GraphQL은 gql 스키마의 타입마다 sql 쿼리가 달라진다.
![image](https://user-images.githubusercontent.com/35768650/231185400-8a63ee47-c80e-4bcd-879f-a90abbdcf38b.png)


### 구조
* 요청 쿼리 구조와 응답 내용 구조가 거의 일치한다.
* TBD


### 참고 레퍼런스
* https://tech.kakao.com/2019/08/01/graphql-basic/