# ARP 프로토콜
- 같은 네트워크 대역에서 통신을 위해 필요한 **MAC주소를 IP주소를 이용해서** 알아오는 프로토콜

- 같은 네트워크 대역에서 통신을 한다고 하더라도 데이터를 보내기 위해서는 7계층부터 캡슐화를 통해 데이터를 보내기 때문에 IP주소와 MAC주소가 모두 필요하다. 이 때 IP주소는 알고 MAC주소는 모르더라도 ARP를 통해 통신이 가능하다.

## ARP 프로토콜의 구조(28Byte)

 - **Hardware type(2byte)** - 2계층 타입(Ethernet(0001))
 - **Protocl type(2byte)** - 프로토콜 타입(IPv4(0800))
 - **Hardware Address Length(1byte)** - MAC주소의 길이(06)
 - **Protocol Address Length(1byte)** - IPv4주소의 길이(04)
 - **Opcode(2byte)** - operation code(어떻게 동작하는지 알려주는 코드) 물어볼 때 1, 응답할 때 2
 - **Source Hardware Address(6byte)** - 출발지 MAC주소\
 - **Source Protocol Address(4byte)** - 출발지 IP주소\
 - **Destination Hardware Address(6byte)** - 목적지 MAC주소\
 - **Destination Protocol Address(4byte)** - 목적지 IP주소

 # ARP 통신과정
 1. Ethernet + ARP요청 패킷으로 ARP가 원하는 IP주소의 같은 네트워크 대역을 쓰는 장비들에게 ARP의 MAC정보는 0으로, Ethernet의 MAC 정보는 F로 채워(다 1111~~~~이면 브로드캐스트) 보낸다.

2. 스위치(2계층)는 그 패킷을 받아 Ethernet을 디캡슐화를 한 다음 브로드캐스트를 한다. 

3. 각 네트워크 장비들은 ARP까지 디캡슐화 해 보고 그 IP주소에 해당하는 장비를 제외한 나머지는 그 패킷을 무시한다. 

4. IP에 해당한 장비는 0orF로 채워진 MAC주소의 값을 채워준 후 Ethernet + ARP응답 패킷을 만들어 다시 전송(Opcode : 2)한다.

5. 받으면 ARP 캐시 테이블(통신 했던 컴퓨터들의 주소가 남는다.)에 IP주소와 MAC주소의 값을 저장해놓는다.