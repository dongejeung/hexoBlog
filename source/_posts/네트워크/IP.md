---
title: 
date: 2020-01-17 16:57:10
categories:
    - 네트워크
---

<pre>
필요한 일이 있어서 ip 우회를 해야한다.
하는 김에 ip에 대한 개념과 
우회 방법 등을 살펴보기로 하자.

/*
    아주 간단하게 추상화시켜서
    딱 까놓고 말하면
    통신이란 것은
    데이터를 전송, 응답하는 행위가 아닐까 싶다.
    (Request, Response)
    주소라는 것은 발신지와 수신지를 나타낼 수 있는 가상의 지리적 위치라고 생각해도 될 것이다.
*/

개념을 보자.
(나무위키 등을 참조.)

IP : Internet Protocol 의 약자.
인터넷은 인터넷이고 프로토콜은 규약을 뜻한다.
인터넷을 사용할 때 각 장치의 주소값을 표준화시킨 것이라고 보면 된다.

통신을 위해서 ISO위원회에서 표준화된 모델을 발표한 이후 이어져온 것 같다.
여기서 TCP/IP 가 표준이 되었다. 라고 나온다.
그리고 OSI 7계층이라는 개념이 나온다.
(물리, 데이터, 네트워크, 전송, 세션, 표현, 응용)
이런 것들은 나중에 필요할 경우 심화하도록 하고..

예전에는 IP를 할당할 때 클래스를 나누어서 할당하였는데
처음에는 주로 Class-B의 영역에서 할당했지만 => CIDR란 방식으로 변화.
(CIDR(사이더)는 연속된 IP 주소의 범위를 표기하는 방법 중 하나.)
IP주소는 IPv4, IPv6 두 가지 체계가 있다.

IPv4
-32비트의 값.
- 각 자리수는 0~255의 10진수 숫자.
- 8비트씩 끊어서 . 으로 구분.

 // 그러니까 주소나 전화번호는 편의상 수나 문자의 조합이 되고,
 그 가지수는 장치와 주소별 1대일 매칭을 소화하여 아이덴티티를 구분해줄 편의성이 있나인 것 같다.
 숫자의 경우 자리수를 무한정 늘릴수도 있는 듯.
 
IPv6
- 
-16진수로 표기.
-중간에 0이 있는필드 생략가능.
// 예컨데 0000 => 생략 가능, 0010 => 10으로 표기


뭔 소린지 잘 모르겠다.
속도를 높이거나 IP노출을 피하고자 할 때,
프록시 서버나 가상 사설망을 쓰게 된다는데
이것이 지금 당장 내가 필요한 것이다.

// 후이즈 사이트에서 IP주소를 확인할 수 있다. 다른 사이트도 있겠지.

* 주소 할당.
지역별로 쓸 수 있는 IP주소의 범위가 있으며,
관리 기관에 할당받아야 사용할 수 있다.

* 사설 IP.
IP주소 할당에는 비용을 지불해야 해서,
내부의 사설 네트워크를 구축하는 식으로 많이 쓰는데,
공유기를 생각하면 편하다.
//공유기를 써도 표시되는 IP주소는 동일하다는 소리.
사설 IP를 쓰면,
실제 사람이 사용하는 IP주소는 사설IP 주소인데,
외부에서 쓰는 것은 공인 IP 주소이기 때문에 불편한 점이 발생한다.

그냥 다음, 네이버에서 ip주소라고 치면 사용중인 공인 IP주소가 나온다.
/* 
    테스트로 공유기를 통해 인터넷을 연결한 노트북과 데스크탑의 IP주소를 비교해보니
    끝자리만 차이가 있었다.
    카스퍼스키 시큐어 커넥션을 사용하니 IP주소가 완전히 변경되었다.
    시큐어 커넥션은 데이터량의 제한과 속도 저하가 있다.
*/


*IP우회 방법으로 프록시 서버라는 것이 등장한다.
// 유동 IP 라는 것도 나옴. 패킷이라는 개념도 나오고..


* 프록시 서버
클라이언트가 자신을 통해서 다른 네트워크 서비스에 간접적으로 접속할 수 있게 해 주는
컴퓨터 시스템이나 응용 프로개름을 가리킨다.

* VPN
가상 사설망.
보안을 통해 통신 내용을 암호화 하는데 주로 쓰이는 것 같다.
개인정보 보호 등.
공개된 Wi-Fi 등은 보안에 굉장히 취약하다고 들었다.


그럼 이제 본론으로 들어가서,
IP우회에 대해 알아보겠다.
등장하는 것들이
VPN, 프록시 서버 이용 등이 있다.

원격 서버를 통해서 통신을 한다는 것은 공통점인 것 같다.
나는 일단 무료여야 되고,
안전해야 하고,
속도가 빨라야 한다.
그롬 익스텐션으로도 제공하고 있네..
VM웨어에다 익스텐션을 설치해 봐야겠다.

된다. uVPN이 다운로드수가 압도적으로 많고 
무료로 쓸 수 있는 것 같아서 그것으로 설치했다.
Vmware 내에서 메인 OS와 다른 주소로 표기되었다.

나중에 궁금하거나 필요하면 관련 학습을 더
진행하도록 하겠다.

</pre>
## Reference
#나무위키 #위키백과
