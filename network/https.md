## HTTPS
### 세줄 요약
* HTTP 에 데이터 암호화가 추가된 프로토콜이다.
* 443 포트를 사용한다.
* 대칭키, 비대칭키 암호화 방식을 모두 사용하고 있다.

<br/>

### 동작 과정
1. 브라우저가 서버로 최초 연결 시도
2. 서버는 공개키(인증서)를 브라우저에게 응답한다.
3. 브라우저는 인증서의 유효성을 검사하고 세션 키를 발급한다.
4. 브라우저는 세션 키를 보관하며 추가로 서버의 공개키로 세션 키를 암호화하여 서버로 전송한다.
5. 서버는 개인 키로 암호화된 세션 키를 복호화하여 세션 키를 얻는다.
6. 클라이언트와 서버는 동일한 세션 키를 공유하므로 데이터를 전달할 때 세션 키로 암호화/복호화를 진행한다.

<br/>
<br/>
<hr/>

## 참고 레퍼런스
* https://mangkyu.tistory.com/98