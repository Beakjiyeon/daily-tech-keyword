## SSH

### 세줄 요약
* 네트워크 상에서 다른 컴퓨터에 로그인하거나 
* 원격 시스템에서 명령을 실행하고 다른 시스템으로 파일을 복사하기 위해 사용되는 프로토콜이다.
* SSH는 암호화된 통신(공개키, 개인키)을 통해 안전하게 데이터를 전송할 수 있습니다.

<br/>
<br/>

### 정리
* Secure SHell = 보안 셸
* 네트워크 프로토콜
* **데이터 전송, 원격 제어에 사용하는 기술**
* FTP, Telnet 보다 보안적으로 훨씬 안전한 채널을 구성한 뒤 정보를 교환한다.
* **비밀번호 입력이 아닌** **공개키, 비밀키를 통해 접속하려는 컴퓨터와 인증** 과정을 거친다.
* 클라이언트가 SSH 접속을 시도하면 서버에서 상대방이 개인키를 가졌는지 테스트하고 연결 여부를 결정한다. (비대칭키 방식)

### 공개키
* 공개되어도 안전한 내용
* 통신하려는 컴퓨터에 저장한다. ex. Github setting, ~/.ssh/authorized_keys

### 개인키
* 외부에 노출되면 안되는 키
* 컴퓨터 내부에 저장되어 있다.


<br/>
<br/>
<hr/>



### 참고 레퍼런스
* https://hanamon.kr/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-ssh%EB%9E%80/
* https://danthetech.netlify.app/Backend/configure-ssh-key-based-authentication-on-a-linux-server
* https://library.gabia.com/contents/infrahosting/9002/
* https://library.gabia.com/contents/9008/
