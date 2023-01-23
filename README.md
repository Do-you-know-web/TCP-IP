# TCP-IP

## intro - 인터넷
= 전 세계에 걸쳐 파일 전송 등의 데이터 통신 서비스를 받을 수 있는 컴퓨터 네트워크 시스템 

- 바다 밑에 있는 광속 케이블을 타고 구글까지 찾아가야 함
- 데이터 → 디지털 신호 → 데이터로 변환되면서 네트워크 통신이 일어남
- 이런 통신을 위해 미리 정해놓은 매뉴얼 = ‘프로토콜’

## 웹브라우저에서 특정 주소를 입력하면 

1. 웹브라우저 주소창에 www.google.com을 입력
= 구글 웹서버 80포트에 HTTP로 작성된 request을 처리해달라고 메시지를 보내는 것 

<aside>
💡 요청 헤더 : 메시지의 콘텐츠와는 관련이 없는 HTTP 요청에 사용되는 헤더
</aside>

2. 패킷을 만듦 → 각 계층에 필요한 정보를 담음


## TCP/IP
= 인터넷에서 컴퓨터들이 서로 정보를 주고 받는 데 쓰이는 프로토콜의 집합

### TCP/IP의 4개의 계층
1. Application Layer
- 브라우저와 웹서버 간 **HTTP request & response**
- HTTP, DNS, FTP, SSH, Telnet, SMTP

2. Transport Layer	
- 송신된 데이터를 수신하는 애플리케이션에 확실히 전달하기 위해 사용 
- 네트워크 통신하는 애플리케이션은 포트번호 사용 
 → 포트번호를 이용하여 애플리케이션을 찾아줌 
- TCP, UDP, RTP, RTCP

3. Internet Layer
- 수신 측까지 데이터를 전달하기 위해 사용 
- 송신 측, 수신 측 모두 IP 주소를 가지고 있음 
  → IP 주소 바탕으로 올바른 목적지까지 찾아갈 수 있도록 도와줌 
- IP, ARP, ICMP, PARP, OSPF

4. Network Access Layer
- 네트워크에 직접 연결된 기기 간 전송을 도와줌 
- 물리적 주소인 MAC 주소 사용
- Eternet, PPP, Token Ring


### 신뢰할 수 있는 TCP

- 하나의 패킷에 담을 수 없는 큰 데이터를 주고 받는 경우가 많아짐 
  → 패킷으로 데이터를 잘게 쪼개서 많이 보냄
- 이런 많은 패킷/데이터를 엄청나게 복잡한 인터넷을 통하여 목적지로 갈 때 유실되지 않고 순서대로 도착할 수 있도록 보장
