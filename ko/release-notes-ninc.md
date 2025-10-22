## Network > 릴리스 노트

### 2025.11.29

#### Load Balancer
* Public API에 Load Balancer 관련 API가 추가되었습니다. [Load Balancer API 가이드](/Network/Load%20Balancer/ko/public-api-ninc)를 참고하세요.

#### Private DNS
* Public API에 Private DNS 관련 API가 추가되었습니다. [Private DNS API 가이드](/Network/Private%20DNS/ko/public-api-ninc)를 참고하세요.

#### Flow Log 
* Public API에 Flow Log DNS 관련 API가 추가되었습니다. [Flow Log API 가이드](/Network/Flow%20Log/ko/public-api-ninc/)를 참고하세요.

### 2025. 03. 13.

#### 기능 개선

##### Service Gateway
* Service Gateway 생성 시 사용자가 IP 주소를 지정하여 생성할 수 있도록 개선하였습니다.
  
##### Load Balancer
* L7 정책에서 L7 Redirect URL을 사용자가 더 세분화하여 설정할 수 있도록 개선하였습니다.
* 멤버 그룹별로 고정된 포트 번호가 아닌 각 멤버별로 지정된 포트 번호에 대하여 상태 확인을 할 수 있도록 개선되었습니다.

##### Flow Log
* Transit Hub의 연결을 대상으로 Flow Log를 생성할 수 있도록 기능이 추가되었습니다.
* Flow Log 수집 대상에 VPC 및 Subnet이 추가되었습니다.

##### Routing
* 라우트에 설명 항목이 추가되었습니다. 라우트 생성 또는 변경 시 값을 입력할 수 있으며, 라우트 정보에 표시됩니다.
* 라우트의 CIDR, 게이트웨이 항목을 변경하는 기능이 추가되었습니다.


### 2025. 01. 24.

* 신규 서비스 출시
