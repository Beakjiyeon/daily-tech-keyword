## GraphQL
### 세줄 요약
* rest api 방식을 사용했을 때보다 클라이언트 입장에서 호출 횟수가 감소하고, 응답 데이터를 조합하여 사용하는 수고를 덜 수 있다.
  * 프론트 입장에서 페이지가 복잡해질 수록 많은 호출을 해야 하고 데이터 조합을 위해 순차적인 처리가 들어가야 한다.
* grapql은 클라이언트가 필요한 데이터만을 쿼리할 수 있다. 
  * 이런 데이터 sql 처리를 위해 graphql이라는 서비스 브로커 레이어가 필요하다.
* 클라이언트에서는 통신이 편해지지만, 그만큼 서버에서는 요청이 가중 될 수도 있다.


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
* 쿼리 : 데이터 조회용
  * 오퍼레이션 네임 쿼리 : 변수를 주는 쿼리 
* 뮤테이션 : 데이터 변조용
* 리졸버 : gql에서 데이터를 가져오는 부분이다. 
  * 데이터 특성(db, 일반 파일, http, soap)에 상관없이 구현할 수 있다.
  * 레거시 시스템을 gql 기반으로 바꾸는데 활용할 수 있다.


### 참고 레퍼런스
* https://tech.kakao.com/2019/08/01/graphql-basic/
* https://kotlinworld.com/330
