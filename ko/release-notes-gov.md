## Network > 릴리스 노트

### 2025. 06. 05

#### 기능 추가

##### NAT Gateway
* Public API에 NAT Gateway 관련 API가 추가되었습니다. [NAT Gateway API 가이드](/Network/NAT%20Gateway/ko/public-api-gov/)를 참고하세요.

##### Security Groups
* Public API에 Security Groups 연결 정보 조회 API가 추가되었습니다. [Security Groups API 가이드](/Network/Security%20Groups/ko/public-api-gov/)를 참고하세요.
* 보안 규칙 대량 생성, 보안 규칙 목록 다운로드 기능이 추가되었습니다.

##### Internet Gateway
* Public API에 Internet Gateway 관련 API가 추가되었습니다. [Internet Gateway API 가이드](/Network/Internet%20Gateway/ko/public-api-gov/)를 참고하세요.

##### Colocation Gateway
* Public API에 Colocation Gateway 관련 API가 추가되었습니다. [Colocation Gateway API 가이드](/Network/Colocation%20Gateway/ko/public-api-gov/)를 참고하세요.

##### Private DNS
* Public API에 Private DNS 관련 API가 추가되었습니다. [Private DNS API 가이드](/Network/Private%20DNS/ko/public-api-gov/)를 참고하세요.

##### Floating IP
* 플로팅 IP에 레이블 설정 기능이 추가되었습니다. [Floating IP 콘솔 사용 가이드](/Network/Floating%20IP/ko/console-guide/)를 참고하세요.

### 2025. 04. 29.

#### 기능 변경

##### DNS Plus
* 레코드 세트 TTL의 최솟값을 1에서 10으로 변경하였습니다.


### 2025. 03. 11.

#### 기능 개선

##### Service Gateway
* Service Gateway 생성 시 사용자가 IP 주소를 지정하여 생성할 수 있도록 개선하였습니다.

##### Load Balancer
* L7 정책에서 L7 Redirect URL을 사용자가 더 세분화하여 설정할 수 있도록 개선하였습니다.
* 멤버 그룹별로 고정된 포트 번호가 아닌 각 멤버별로 지정된 포트 번호에 대하여 상태 확인을 할 수 있도록 개선되었습니다.

##### Routing
* 라우트에 설명 항목이 추가되었습니다. 라우트 생성 또는 변경 시 값을 입력할 수 있으며, 라우트 정보에 표시됩니다.
* 라우트의 CIDR, 게이트웨이 항목을 변경하는 기능이 추가되었습니다.


### 2024. 12. 03.

#### 기능 개선

##### Peering Gateway
* 피어링에 설명 항목이 추가되었습니다. 피어링 생성 또는 변경 시 해당 피어링에 대한 설명을 입력할 수 있으며, 피어링 기본 정보에 표시됩니다.

### 2024. 09. 05.

#### 기능 추가

##### Routing
* Public API에 라우팅 테이블과 연관된 게이트웨이 정보 조회 API가 추가되었습니다. [VPC API 가이드](/Network/VPC/ko/public-api-gov/)를 참고하세요.


#### 기능 개선

##### Load Balancer
* 멤버별로 포트 번호를 지정할 수 있습니다.

##### Region Peering
* 다른 프로젝트에서 생성된 VPC에 연결할 수 있도록 기능이 추가되었습니다.

##### Transit Hub
* 멀티캐스트 도메인을 다른 프로젝트에 공유할 수 있도록 기능이 추가되었습니다. 다른 프로젝트에서 생성된 VPC 간에 멀티캐스트 통신을 할 수 있습니다.


### 2024. 06. 04.

#### 기능 추가

##### Network ACL, NAT Instance, Transit Hub, Colocation Gateway, NAT Gateway, Service Gateway, Traffic Mirroring, Private DNS
* 한국(판교) 리전에 기능이 추가되었습니다.

#### Load Balancer
* L7 로드 밸런싱 기능이 추가되었습니다. [로드 밸런서 사용자 가이드](/Network/Load%20Balancer/ko/console-guide-gov/)를 참고해 주세요.

### 2024. 05. 28.

#### 기능 추가 

##### DNS Plus
* GSLB 헬스 체크에서 헬스 체크 요청의 헤더, 헬스 체크 주기, 최대 응답 대기 시간, 최대 재시도 횟수 설정 기능이 추가되었습니다.

### 2024. 03. 12.

#### 기능 개선

##### DNS Plus
* SPF 레코드 세트 타입 지원이 중단되었습니다. TXT 레코드 세트 타입으로 대신 사용할 수 있습니다.
    * 상세 내용은 [[RFC 7208#section-14.1]](https://datatracker.ietf.org/doc/html/rfc7208#section-14.1)에서 확인할 수 있습니다.

### 2024. 02. 29.

#### 기능 추가

##### Floating IP
* 플로팅 IP 삭제 보호 기능이 추가되었습니다.

##### Load Balancer
* 로드 밸런서 삭제 보호 기능이 추가되었습니다.
* Public API에 L7 로드 밸런싱 관련 API가 추가되었습니다. [로드 밸런서 API 가이드](https://docs.gov-nhncloud.com/ko/Network/Load%20Balancer/ko/public-api-gov/)를 참고해 주세요.

#### 기능 개선

##### Transit Hub
* 라우팅 룰 패킷 처리 방식에 패킷을 소멸시키는 BLACKHOLE이 추가되었습니다. 

### 2023. 11. 30.

#### 기능 추가

##### Load Balancer

* 로드 밸런서에 서브넷 정적 라우트 적용 기능이 추가되었습니다. 로드 밸런서가 속한 서브넷에 설정된 정적 라우트를 인스턴스뿐만 아니라 로드 밸런서에도 적용할 수 있습니다.

### 2023. 09. 05.

#### 기능 추가

##### VPC

* Public API에 Routing API가 추가되었습니다. [VPC API 가이드](https://docs.gov-nhncloud.com/ko/Network/VPC/ko/public-api-gov/)를 참고해 주세요.


### 2023. 06. 08.

#### 기능 개선

##### Network Interface

* Network Interface UI 개선
    * 검색 기능이 추가되었습니다.
    * 장치 이름을 표시하도록 개선했습니다.

### 2023. 04. 04.

#### 기능 개선 

##### VPC

* Public API에 VPC 및 VPC Subnet API가 추가되었습니다. 자세한 사항은 [VPC API 가이드](https://docs.gov-nhncloud.com/ko/Network/VPC/ko/public-api-gov/)를 참고해 주세요.   

#### 기능 변경

##### VPC, Floating IP, Security Groups, Load Balancer

* API 엔드포인트 주소가 변경되었습니다.

### 2022. 08. 02.

#### 기능 추가

##### Load Balancer

* 상태 확인 시 호스트 헤더의 필드값을 변경할 수 있는 기능이 추가되었습니다.

### 2022. 05. 31.

#### 기능 추가

##### VPC

* 프로젝트 피어링 기능이 추가되었습니다. 같은 리전, 다른 프로젝트에 생성된 두 개의 VPC를 연결할 수 있습니다.

### 2022. 04. 05.

#### 기능 추가

##### VPC

* 서브넷에 정적 라우트 설정 기능이 추가되었습니다. 서브넷 내의 인스턴스들에게 DHCP를 통해 전달할 정적 라우트를 설정할 수 있습니다.
* "중앙 집중형 라우팅 테이블" 생성 및 변경 기능이 추가되었습니다. 

##### Network Interface

* 이중화를 위한 가상 IP 생성 기능이 추가되었습니다. 가상 IP로 사용할 IP를 선점하고, 라우팅 테이블에서 해당 IP로의 라우트를 추가할 수 있습니다.
* 인스턴스를 게이트웨이/방화벽 등의 용도로 사용할 수 있도록 네트워크 인터페이스의 보안 설정을 해제하는 기능이 추가되었습니다. 

#### 기능 개선

##### Load Balancer

* TERMINATED_HTTPS 프로토콜을 사용하는 로드 밸런서에서 TLS 1.3 버전을 사용할 수 있도록 개선되었습니다.

### 2021. 12. 07.

#### 기능 추가

##### DNS Plus

* 레코드 세트 대량 생성 기능이 추가되었습니다.


### 2021. 07. 02.

#### 기능 변경

##### VPC

* 라우팅 테이블의 기본 라우트(VPC 주소 영역 전체로의 로컬 라우트)가 적용되지 않는 문제를 수정했습니다. 기존에는 VPC 내의 서브넷이라도 같은 라우팅 테이블에 연결되어 있는 서브넷 간에만 통신이 가능했지만, 서로 다른 라우팅 테이블에 연결되어 있는 서브넷 간에도 통신이 가능합니다.


#### 기능 추가

##### Network Interface

* Network Interface 기능이 추가되었습니다.


### 2020. 11. 03.

#### 기능 변경

##### VPC
* 라우팅 테이블의 라우트 생성 창에서 게이트웨이 항목에 IP를 직접 입력하는 방식을 IP를 소유한 장치를 선택하는 방식으로 변경했습니다. 라우팅 테이블에 명시적으로 연결하지 않은 서브넷의 장치도 선택할 수 있습니다.
* 인터넷 게이트웨이 목록에서 IP 정보 대신 연결된 라우팅 테이블의 정보를 표시하도록 변경했습니다. 라우팅 테이블의 라우트 탭에서도 연결된 인터넷 게이트웨이의 이름이 표시됩니다.


#### 기능 개선

##### DNS Plus

* 레코드 세트 수정 시 레코드 세트 타입 수정이 가능하도록 개선되었습니다.

#### 기능 추가

##### Load Balancer

* Public API v2가 IP 접근 제어 기능을 지원합니다. 자세한 사항은 [로드밸런서API가이드](https://gov-docs.toast.com/ko/Network/Load%20Balancer/ko/public-api-gov/#ip-acl)를 참고해 주세요.


### 2020. 08. 25.

#### 기능 개선

##### Load Balancer

* 전용 로드밸런서 서비스가 추가되었습니다.
* 전용 로드밸런서는 하드웨어 자원을 선점하여 생성되기에 1Gbps의 대역폭과 48만 동시세션을 지원합니다.

### 2020. 06. 16.

#### 기능 개선

##### VPC

* Public API v2가 출시됩니다. Public API v2는 Openstack API와 호환됩니다.

##### Load Balancer

* 로드 밸런서와 동일한 VPC에 속한 다른 서브넷의 인스턴스를 로드 밸런서의 멤버로 등록할 수 있습니다. 로드 밸런서가 속한 서브넷과 인스턴스의 서브넷이 라우팅 테이블에 연결되어야 합니다.
* 로드 밸런서가 속한 VPC가 피어링(peering) 연결되어 있다면, 피어 VPC에 속한 인스턴스를 로드 밸런서의 멤버로 등록할 수 있습니다. 피어 VPC의 기본 라우팅 테이블에 연결된 서브넷의 인스턴스만 연결할 수 있습니다.
* 로드 밸런서에 여러 리스너를 운용하는 경우 모든 리스너에 동일한 멤버 인스턴스를 구성해야 했었는데, 이제는 리스너별 멤버 인스턴스를 서로 다르게 설정할 수 있습니다.
* Public API v2가 출시됩니다. Public API v2는 Openstack API와 호환됩니다.

### 2020. 04. 07.

#### 신규 상품 출시

##### DNS Plus

* DNS Plus는 도메인 관리 기능과 서버의 트래픽을 안정적으로 로드벨런싱하는 기능을 제공합니다.
* DNS(Domain Name System)로 도메인을 간편하게 설정하고 관리할 수 있습니다.
* GSLB(Global Server Load Balancing)로 라우팅 규칙에 따라 엔드포인트 서버를 DR(Disaster Recovery), 랜덤 로드밸런싱, 전 세계적인 로드밸런싱으로 구성할 수 있습니다.

### 2020. 03. 10.

#### 기능 개선
##### 플로팅 IP
* 인스턴스에 연결된 모든 네트워크 인터페이스에 각각 플로팅 IP를 연결할 수 있습니다.

##### Load Balancer
* TERMINATED_HTTPS 로드밸런서에 클라이언트와 통신할 TLS 버전을 지정할 수 있습니다.
  * 로드밸런서 TLS 버전 설정 기능에 대한 자세한 사항은 [사용자가이드](https://gov-docs.toast.com/ko/Network/Load%20Balancer/ko/overview/#ssltls)를 참고해 주세요.
* 체인 인증서를 등록할 때 인증서 파일에 포함된 개별 인증서의 형식이 잘못된 경우, 웹콘솔을 통해 알리는 기능이 추가되었습니다.

##### Security Groups

* 보안 그룹 규칙에 "설명" 항목이 추가되었습니다. 보안 그룹 규칙별로 설명을 추가할 수 있습니다.

### 2019. 08. 13.

#### 기능 개선

##### Load Balancer
* IP 접근제어 기능을 사용할 수 있습니다.
    * IP를 기반으로 한 접근제어 기능을 로드밸런서에서 사용할 수 있습니다.
    * IP 접근제어 기능에 대한 자세한 사항은 사용자가이드 문서를 참고해주세요.
    * 유선으로 설정 요청하신 제어 대상 IP 목록은 Default 라는 이름의 IP 접근제어 그룹에 자동 반영되었습니다.

#### 기능 변경

##### VPC

* 피어링 생성 기능을 다시 사용할 수 있습니다.

### 2018. 12. 27.

#### 기능 변경

##### VPC

* 피어링 된 두 VPC 사이의 통신 시 패킷 플러딩이 발생할 가능성이 있어, 당분간 새로운 피어링 생성 기능을 제공하지 않습니다.
	기존에 만들어진 피어링의 통신에는 문제가 없으며 피어링 생성을 제외한 나머지 기능은 그대로 제공됩니다.

### 2018. 11. 27.

#### 버그 수정

##### Load Balancer

* 로드 밸런서에 리스너를 추가 생성하는 경우, 비활성화된 인스턴스에 추가된 인스턴스 멤버가 활성화된채 생성되는 버그를 수정하였습니다.

#### 기능 개선

##### Load Balancer

* 로드밸런싱 통계 기능이 추가되어 다음 통계량이 차트 형식으로 제공됩니다.
    * 세션수, 클라이언트 초당 세션증가량, 인스턴스 초당 세션 증가량, In 트래픽량, Out 트래픽량, 로드밸런싱 제외 개수
    * 삭제된 로드밸런서, 리스너, 멤버에 대한 통계량은 제공되지 않습니다.
    * 트래픽량에는 L2, L3, L4 헤더가 포함되지 않습니다.
    * 자세한 사항은 사용자가이드 문서를 참고해주세요.


### 2018. 09. 20.

#### 버그 수정

##### Load Balancer

* Load Balancer에 Member로 등록된 Instance를 삭제할 때 일부 Listener의 Member가 남아있는 문제를 수정했습니다.

#### 기능 개선

##### Load Balancer

* 전용 로드밸런서 서비스가 추가되었습니다. 
* 전용 로드밸런서는 하드웨어 자원을 선점하여 생성되기에 1Gbps의 대역폭과 48만 동시세션을 지원합니다.

### 2018. 08. 28.

#### 버그 수정

##### VPC

* 라우트가 존재하는 서브넷을 가진 VPC에 대해 삭제를 시도할 수 있는 문제를 수정했습니다.

#### 기능 변경

##### VPC

* 서브넷, 라우팅 테이블, 라우트에 대해 최대 생성 가능 개수를 조정했습니다.
* VPC의 리소스 별 최대 생성 가능 개수는 각 리소스 생성 창의 우측 설명 부분에서 확인하실 수 있습니다.
    * 서브넷: VPC당 10개까지 생성이 가능합니다.
    * 라우팅 테이블: VPC당 10개까지 생성이 가능합니다.
    * 라우트: 라우팅 테이블당 10개까지 생성이 가능합니다.

##### Load Balancer

* TCP, HTTPS 프로토콜을 사용하는 경우 클라이언트의 IP를 알기 위해 Proxy Protocol을 활성화할 수 있습니다.
* Load Balancer의 Keepalive timeout 값을 설정할 수 있습니다.


### 2018. 04. 24.

#### 버그 수정

##### VPC

* 피어링 시 로컬 VPC의 인스턴스에서 피어 VPC의 로드밸런서로 접속이 원활하지 않은 문제를 수정했습니다.

#### 기능 개선

##### VPC

* VPC, 서브넷, 라우팅테이블, 인터넷게이트웨이의 개요 페이지에서 연결된 리소스 정보를 확인할 수 있습니다.

##### Floating IP

* Floating IP 목록에 페이지네이션 기능을 적용했습니다.

##### Security Group

* Rule 편집 기능이 추가되었습니다.

##### Load Balancer

* Keepalive Timeout을 5분으로 변경하였습니다.
* Listener의 세션 제한값을 최대 60,000 까지 설정할 수 있습니다.

### 2018. 03. 22.

#### 버그 수정

##### VPC

* 새로 추가한 서브넷에 인스턴스를 연결하면 DHCP를 통해 IP를 받아오지 못하는 문제를 수정했습니다.
* 라우팅 정책을 추가할 때 기존 라우팅 정책의 타겟과 동일한 타겟을 입력할 수 있는 문제를 수정했습니다.
* Floating IP가 연결된 인스턴스에서 간헐적으로 다른 서브넷에 위치한 인스턴스와 통신이 되지 않는 문제를 수정했습니다.

### 2018. 02. 22.

#### 버그 수정

##### VPC

* Floating IP가 연결된 인스턴스에서 로컬 네트워크로 트래픽이 전달되지 않는 문제를 수정했습니다.

#### 기능 개선

##### Network 기본 모델로 VPC를 도입했습니다.

* 서브넷을 여러개 사용할 수 있습니다.
* 서브넷 단위로 포트를 생성하여 인스턴스에 연결할 수 있습니다.
* 라우팅 정책을 추가할 수 있습니다.
* VPC간 통신을 위해 피어링 기능이 추가되었습니다.
* 인스턴스에 여러 VPC 포트를 추가하거나 삭제할 수 있습니다.
* 자세한 내용은 VPC Overview와 사용자 가이드를 참고해주시기 바랍니다.


### 2017. 11. 23.

#### 버그 수정

##### Load Balancer
* Load Balancer 생성시 리스너의 연결 제한값이 잘못 표기되는 현상을 수정하였습니다.

### 2017. 10. 26.

#### 버그 수정

##### Load Balancer
* Load Balancer 생성시 인증서가 등록되지 않는 버그가 수정되었습니다.

### 2017. 09. 21.

#### 기능 추가

##### Public API 추가

* Object Storage에 이어 Compute&Network 상품을 API를 이용해 관리할 수 있습니다.
* 현재 제한적인 기능만 이용할 수 있으며, 추후 API 추가를 통해 기능이 확장되었습니다.

#### 버그 수정

* Project에 Admin 권한이 없는 사용자가 security group을 수정할 수 없도록 수정되었습니다.
* Project에 Admin 권한이 없는 사용자에게는 Network 메뉴가 노출되지 않도록 수정되었습니다.

### 2017. 08. 24.

#### 버그 수정

##### Load Balancer
* Load Balancer 서비스의 세션 지속성 항목이 제대로 표시되지 않던 버그가 수정되었습니다.

### 2017. 04. 20.

#### 버그 수정
##### Load Balancer
* Listener에 인증서 파일 업로드시 간헐적으로 인증서 등록창이 사라지는 버그가 수정되었습니다.


### 2017. 03. 23.

#### 버그 수정
##### Floating IP
* Floating IP 연결 팝업에서 "생성" 버튼이 노출되지 않는 문제가 수정되었습니다.


### 2017. 02. 23.

#### 기능 개선/변경

##### Load Balancer

* 로드밸런서에 등록된 리스너가 1개일 경우 삭제할 수 없다는 것을 알리도록 변경합니다.
	  * 기존에도 삭제가 되지 않았으나 사용자에게 별다른 알림이 없어 혼동을 주었습니다.
	  * 이제 사용자에게 명시적으로 삭제할 수 없다고 메시지를 공지하도록 변경합니다.

##### Floating IP

* Floating IP 삭제 시 인스턴스 혹은 로드밸런서가 연결되어 있을 경우 삭제 할 수 없도록 변경합니다.
	  * 기존에는 인스턴스나 로드밸런서가 연결되어 있는 Floating IP를 삭제할 수 있어 서비스에 장애를 일으킬 수 있었습니다.
	  * 이런 실수를 미연에 방지할 수 있도록 연결이 있는 Floating IP는 삭제할 수 없도록 변경합니다.
* 명칭변경 : '포트' -> '네트워크 인터페이스'
	  * 인스턴스에 Floating IP를 붙일 때 대상이 되는 명칭을 기존 “포트”에서 “네트워크 인터페이스”로 변경합니다.


### 2017. 01. 19.

#### 버그 수정
##### Load Balancer
* Load Balancer 생성시 연결 제한 설정이 적용되지 않는 문제를 수정하였습니다.



### 2016. 12. 22.

#### 버그 수정

##### Load Balancer
* Health Check Protocol이 TCP인 경우 Listener 내용 수정이 안되는 문제를 수정하였습니다.

##### Floating IP
* Floating IP에 연결된 Load Balancer의 이름이 노출되지 않는 문제를 수정하였습니다.

##### Security Group
* 중복된 Rule 추가 시 Security Group 목록이 사라지는 문제를 수정하였습니다.






### 2016. 12. 08.

#### 버그 수정

##### Load Balancer
* Load Balancer의 Heath check url이 미노출되는 문제를 수정하였습니다.
* Listener 수정 버튼 클릭시 기등록한 Health Check URL이 아닌 "/"로 노출되는 문제를 수정하였습니다.








### 2016. 11. 29.

#### 버그 수정
##### Load Balancer
* TERMINATED_HTTPS type의 Load Balancer 생성이 실패하던 문제를 수정하였습니다.



### 2016. 11. 24.

#### 기능 개선/변경
##### Load Balancer
* Load Balancer의 Listener별 세션 제한 값을 노출하도록 변경하였습니다.

#### 버그 수정
##### Load Balancer
* 특정 Project에서 Load Balancer 생성 실패하던 문제를 수정하였습니다.



### 2016. 08. 04.

#### 기능 개선/변경
##### Load Balancer
* Load Balancer의 SSL offloading 기능을 추가하였습니다.

#### 버그 수정
##### Load Balancer
* Load Balancer 제거 시 간헐적으로 정상 종료되지 않던 문제를 수정하였습니다.
