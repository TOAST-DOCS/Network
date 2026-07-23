## Network > 릴리스 노트

<a id="july-24-2026"></a>
### 2026. 07. 24. { #july-24-2026 }

<a id="july-24-2026-added-features"></a>
#### 기능 추가

##### Network Interface
* "소스/대상 확인" 기능의 이름을 "스푸핑 방지"로 변경하고 네트워크 인터페이스 생성, 변경 화면에서 설정하도록 위치를 이동하였습니다.
* 스푸핑 방지 사용 중 특정 주소만 스푸핑을 허용하는 "추가 허용 주소" 설정 기능이 추가되었습니다. 
* [Network Interface 콘솔 사용 가이드](/Network/Network%20Interface/ko/console-guide/)를 참고하세요.

<a id="july-24-2026-feature-updates"></a>
#### 기능 개선

##### Load Balancer
* 재암호화 기능이 추가되었습니다. 멤버 그룹의 프로토콜로 HTTP_REENCRYPT를 선택하면 멤버로 전송 시 SSL 암호화 통신을 사용합니다.
* HTTP Keepalive 비활성화 기능이 추가되었습니다. Keepalive 타임아웃 설정 시 '사용 안 함'을 선택하면 Keepalive가 비활성화됩니다.
* SSL/TLS 암호화 정책 설정 기능이 추가되었습니다. SSL/TLS 암호화 스위트(Cipher Suite)를 사용자가 커스터마이징하여 사용할 수 있습니다.

##### Flow Log
* 트래픽 경로(`traffic_path`) 필드가 추가되었습니다.
    * 패킷이 통과한 네트워크 경로(VPC Local, Internet Gateway, VPN Gateway, VPC Peering, Region Peering, Project Peering, Service Gateway)를 정수 값으로 확인할 수 있습니다.
    * [Flow Log 개요](/Network/Flow%20Log/ko/overview/)를 참고하세요.

<a id="july-24-2026-july-24-2026-feature-updates"></a>
#### 기능 변경

##### VPC
* 네트워크 서비스 연동 지원을 위해 VPC의 내부 트래픽 처리 방식이 일부 변경되었습니다. 신규 생성되는 VPC부터 적용됩니다.

### 2025. 11. 29.

#### 기능 추가

##### Service Gateway
* Service Gateway 생성 시 사용자가 NAT IP를 고정하여 생성할 수 있도록 개선되었습니다.

##### Load Balancer

- Public API에 Load Balancer 관련 API가 추가되었습니다. [Load Balancer API 가이드](/Network/Load%20Balancer/ko/public-api-ngovc)를 참고하세요.

##### Private DNS

- Public API에 Private DNS 관련 API가 추가되었습니다. [Private DNS API 가이드](/Network/Private%20DNS/ko/public-api-ngovc)를 참고하세요.

##### Flow Log

- Public API에 Flow Log DNS 관련 API가 추가되었습니다. [Flow Log API 가이드](/Network/Flow%20Log/ko/public-api-ngovc/)를 참고하세요.

### 2025. 09. 01.

- 신규 서비스 출시
