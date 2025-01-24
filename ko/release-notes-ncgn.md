## Network > 릴리스 노트

### 2025. 03. 06.

#### 기능 개선

##### Service Gateway
* Service Gateway 생성시 사용자가 IP주소를 지정하여 생성할 수 있도록 개선되었습니다.

##### Load Balancer
* L7 정책에서 L7 redirect url을 사용자가 더 세분화하여 설정할 수 있도록 개선되었습니다.

##### Flow Log
* Transit Hub의 연결을 대상으로 Flow Log를 생성할 수 있도록 기능이 추가되었습니다.
* Flowlog 수집 대상에 VPC 및 Subnet이 추가되었습니다.

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
* Public API에 라우팅 테이블과 연관된 게이트웨이 정보 조회 API가 추가되었습니다. [VPC API 가이드](/Network/VPC/ko/public-api-ngsc/)를 참고하세요.

#### 기능 개선

##### Load Balancer
* 멤버별로 포트 번호를 지정할 수 있습니다.

 
### 2024. 06. 04.

#### 기능 추가

#### Load Balancer
* L7 로드 밸런싱 기능이 추가되었습니다. [로드 밸런서 사용자 가이드](/Network/Load%20Balancer/ko/console-guide-ngsc/)를 참고해 주세요.

##### Service Gateway
* Public API에 Service Gateway 관련 API가 추가되었습니다. [Service Gateway API 가이드](/Network/Service%20Gateway/ko/public-api-ngsc/)를 참고해 주세요.

#### 기능 개선

##### Service Gateway
* 기본 정보 탭에 API 엔드포인트 도메인 항목이 추가되었습니다.

### 2024. 03. 05.

#### 기능 추가

##### Floating IP
* 플로팅 IP 삭제 보호 기능이 추가되었습니다.

##### Load Balancer
* 로드 밸런서 삭제 보호 기능이 추가되었습니다.

#### 기능 개선

##### Transit Hub
* 라우팅 룰 패킷 처리 방식에 패킷을 소멸시키는 BLACKHOLE이 추가되었습니다. 

### 2023. 12. 05.

#### 기능 추가

##### Load Balancer

* 로드 밸런서에 서브넷 정적 라우트 적용 기능이 추가되었습니다. 로드 밸런서가 속한 서브넷에 설정된 정적 라우트를 인스턴스뿐만 아니라 로드 밸런서에도 적용할 수 있습니다.


### 2023. 09. 12.

#### 기능 추가

##### VPC

* Public API에 Routing API가 추가되었습니다. [VPC API 사용자 가이드](https://docs.gncloud.go.kr/ko/Network/VPC/ko/public-api-ngsc/)를 참고해 주세요.

