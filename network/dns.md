## DNS

* Domain Name System

<br/>
<br/>

### 세줄 요약

* 

<br/>
<br/>


### 사용자가 도메인 주소로 접속하는 과정
1. 로컬 컴퓨터가 특정 도메인 주소에 접속한다.
2. 호스트 파일에서 도메인 네임을 찾고 없으면 DNS 서버로 도메인 네임의 ip 를 요청한다.
3. DNS 서버는 해당 ip 를 응답한다.
4. 사용자는 해당 ip를 가지고 도메인주소로 통신하게 된다.


<br/>
<br/>

### Domain 이름의 구조
* 도메인 네임 맨 뒤에는 사실 '.' 이 존재한다. 

  예시 : blog.example.com.
  * 마지막에 있는 점 : 최상위 단위 root
  * blog.example.com. : root 도메인
  * com : top-level 도메인 (.net, .co.kr)
  * example : second-level 도메인
  * blog : sub 도메인
* 각 레벨을 담당하는 DNS 서버가 각각 존재하며 상위 DNS 서버가 직속 하위 정보를 알고 있어야 한다.
  * root 담당 DNS 서버는 top-level 담당 DNS 서버 목록을 알고 있어야 한다.
  * top-level 담당 DNS 서버는 second-level 담당 DNS 서버 목록을 알고 있어야 한다.
  * second-level 담당 DNS 서버는 sub 담당 DNS 서버 목록을 알고 있어야 한다.
* blog.example.com 의 ip 주소를 찾는 과정
  (로컬 컴퓨터는 root 네임 서버의 ip 주소는 알고 있다.)
  1. root 도메인 전담 서버에게 blog.example.com. 을 요청한다.
  2. root 도메인 전담 서버는 com 전담 서버들의 ip 를 알려준다.
  3. top-level 도메인 전담 서버에게 blog.example.com. 을 요청한다.
  4. top-level 도메인 전담 서버는 example.com 전담 서버들의 ip 를 알려준다.
  5. sub 도메인 전담 서버에게 blog.example.com. 을 요청한다.
  6. sub 도메인 전담 서버는 blog.example.com. 의 ip 를 응답한다.
* 전 세계에 퍼져있는 수 많은 DNS 서버들이 위와 같은 과정을 통해 ip 주소를 응답한다. 

<br/>
<br/>


### Domain 이름 등록 과정과 원리


<br/>
<br/>
<hr/>

### 참고 레퍼런스
* https://opentutorials.org/course/3276/20299
* https://opentutorials.org/course/3276/20303
