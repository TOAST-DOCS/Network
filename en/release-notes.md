<a id="network-release-notes"></a>
## Network > Release Notes { #network-release-notes }

<a id="may-27-2026"></a>
### May 27, 2026 { #may-27-2026 }

<a id="may-27-2026-added-features"></a>
#### Added Features

##### Network Interface
* Renamed the "Source/Destination Check" feature to "Anti-Spoofing" and moved its configuration to the network interface creation and modification screens.
* Added the "Additional Allowed Addresses" configuration feature, which allows spoofing for specific addresses while Anti-Spoofing is enabled.
* See [Network Interface Console User Guide](/Network/Network%20Interface/en/console-guide/).

##### Load Balancer (DSR)
* Added Load Balancer (DSR) as a new service. Provides a load balancer service that operates using the Direct Server Return (DSR) method.
	* Load Balancer (DSR) is available only in the Korea (Pyeongchon) and Korea (Pangyo) regions.
* See [Load Balancer (DSR) Console User Guide](/Network/Load%20Balancer(DSR)/en/console-guide/).

<a id="may-27-2026-feature-updates"></a>
#### Feature Updates

##### Load Balancer
* Added a re-encryption feature. Selecting `HTTP_REENCRYPT` as the protocol for a member group enables SSL encrypted communication when forwarding to members.
* Added an HTTP Keepalive disable feature. Selecting "Disabled" when configuring the Keepalive timeout disables Keepalive.
* Added an SSL/TLS encryption policy configuration feature. Users can customize the SSL/TLS cipher suite.

##### Flow Log
* Added the traffic path (`traffic_path`) field.
    * The network path that a packet traversed (VPC Local, Internet Gateway, VPN Gateway, VPC Peering, Region Peering, Project Peering, Service Gateway) can be viewed as an integer value.
    * See [Flow Log Overview](/Network/Flow%20Log/en/overview/).

<a id="may-27-2026-may-27-2026-feature-updates"></a>
#### Feature Updates

##### VPC
* The internal traffic handling method for VPCs has been partially changed to support network service integration. This change applies to newly created VPCs.

<a id="april-14-2026"></a>
### April 14, 2026 { #april-14-2026 }

<a id="april-14-2026-added-features"></a>
#### Added Features

##### DNS Plus
* Added API v2.0
    * Added support for User Access Key tokens.

<a id="november-25-2025"></a>
### November 25, 2025 { #november-25-2025 }

<a id="november-25-2025-added-features"></a>
#### Added Features

##### VPN Gateway
* When you connect a Transit Hub to a VPC with a VPN connection, VPCs in other projects connected to the Transit Hub also support VPN communication with your on-premises network. (VPN Connection with connected range requires additional creation)

##### Service Gateway
* Made improvements to allow users to create a fixed NAT IP when creating a Service Gateway.

##### Traffic Mirroring
* Added Traffic Mirroring related API to Public API. Refer to [Traffic Mirroring API Guide](/Network/Traffic%20Mirroring/en/public-api/).

##### Load Balancer
* Added the feature to configure custom response per listener.
* Added the feature to enable/disable X-Forwarded-* header.

<a id="november-25-2025-feature-updates"></a>
#### Feature Updates

##### Load Balancer 
* Added the feature to register/manage multiple SSL certificates in the console.

<a id="november-25-2025-1"></a>
#### Feature Changes

<!-- TODO: translate body -->

##### DNS Plus

<!-- TODO: translate body -->

<a id="august-26-2025"></a>
### August 26, 2025 { #august-26-2025 }

<a id="august-26-2025-added-features"></a>
#### Added Features

##### VPN Gateway
* v2 has been released.
* The Local gateway address is assigned and can be checked in the console when creating a VPN gateway.
* You can set multiple peer gateway connections in one VPC.
* You can set one peer gateway connection in multiple VPCs from the same project.
* Supported IKE v2 connection.
* VPN connections are available between regions where VPN gateway services are provided (The device is set to Fortinet - FortiGate Series).
* New creation of v1 VPN gateway is restricted as v2 has been released.

##### Load Balancer
* Added support for checking metrics such as the Load Balancer's CPU usage, listener-level statistics, and socket connection status with the Cloud Monitoring service.

<a id="may-27-2025"></a>
### May 27, 2025 { #may-27-2025 }

<a id="may-27-2025-added-features"></a>
#### Added Features

##### NAT Gateway
* Added NAT Gateway-related API to the Public API. Refer to [NAT Gateway API Guide](/Network/NAT%20Gateway/en/public-api/).

##### Security Groups
* Added API for querying Security Groups connection information to the Public API. Refer to [Security Groups API Guide](/Network/Security%20Groups/en/public-api/).
* Added the features to bulk create security rules and download a list of security rules.

##### Internet Gateway
* Added Internet Gateway-related API to the Public API. Refer to [Internet Gateway API Guide](/Network/Internet%20Gateway/en/public-api/).

##### Colocation Gateway
* Added Colocation Gateway-related API to the Public API. Refer to [Colocation Gateway API Guide](/Network/Colocation%20Gateway/en/public-api/).

##### Private DNS
* Added Private DNS-related API to the Public API. Refer to [Private DNS API Guide](/Network/Private%20DNS/en/public-api/).

##### Floating IP
* Added label setting feature to floating IP. Refer to [Floating IP Console User Guide](/Network/Floating%20IP/en/console-guide/).

##### Flow Log
* Added the feature to create Flow Logs for network interfaces of Region peering gateway, Project peering gateway, and Colocation gateway.

<a id="may-27-2025-feature-updates"></a>
#### Feature Updates
##### Flow Log
* Improved that you can freely edit the folder and file names when saving Flow Log files to OBS.


<a id="april-29-2025"></a>
### April 29, 2025 { #april-29-2025 }

<a id="april-29-2025-feature-updates"></a>
#### Feature Updates

##### DNS Plus
* Changed the minimum value of the recordset TTL from 1 to 10.


<a id="march-4-2025"></a>
### March 4, 2025 { #march-4-2025 }

<a id="march-4-2025-feature-updates"></a>
#### Feature Updates

##### Service Gateway
* Improved so that you can create Service Gateway by specifying an IP address.

##### Load Balancer
* Improved so that you can refine settings for L7 Redirect URL in L7 policies.
* Improved so that you can check for status for a port number specified for each member, rather than a fixed port number per member group.

##### Flow Log
* Added the feature to create Flow Log for attachments in Transit Hub.
* Added VPC and Subnet to Flow Log Collection Target.

##### Routing
* Added a description field  to Route. You can enter a value when creating or changing a route, and it will appear in the route information.
* Added the feature to change the CIDR, gateway entry for a route.


<a id="november-26-2024"></a>
### November 26, 2024 { #november-26-2024 }

<a id="november-26-2024-feature-updates"></a>
#### Feature Updates

##### Peering Gateway
* Added the description field to peering. When you create or change a peering, you can enter a description for that peering, which appears in the peering basic information.

##### Flow Log
* Added Gzip compression feature.
* Improved to allow users to select only the statistical information items that they want to record from the ones supported by Flow Log. For the supported statistical items, see [Flowlog Overview](/Network/Flow%20Log/en/overview/).


<a id="network-release-notes-1"></a>
### August 27, 2024 { #network-release-notes-1 }

<!-- TODO: translate body -->

<a id="network-release-notes-1-1"></a>
#### Added Features

<!-- TODO: translate body -->

##### Flow Log

<!-- TODO: translate body -->

##### Routing

<!-- TODO: translate body -->

##### VPN Gateway

<!-- TODO: translate body -->

<a id="network-release-notes-1-2"></a>
#### Feature Updates

<!-- TODO: translate body -->

##### Load Balancer

<!-- TODO: translate body -->

##### Region Peering

<!-- TODO: translate body -->

##### Transit Hub

<!-- TODO: translate body -->

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 (Duplicate 'Flow Log' under t47; no corresponding ko heading (k51 already matched to t49); belongs to missing 2024.08.27 section) -->
##### Flow Log
* Added the Flow Log service. Flow Log allows you to collect and store information about IP traffic sent to and received from a network interface.
    * Flow Log is only available in the Korea (Pyeongchon) region and Korea (Pangyo) region.

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('Routing' under t47 Feature Updates has no ko counterpart under k48/k49; belongs to missing 2024.08.27 Added Features section (k55)) -->
##### Routing
* Added API to get gateway information associated with routing tables to the Public API. See the [VPC API Guide](/Network/VPC/en/public-api/).

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('VPN Gateway' under t47 Feature Updates has no ko counterpart under k48/k49; belongs to missing 2024.08.27 Added Features section (k56)) -->
##### VPN Gateway
* Added support for Diffie-Hellman groups 14,15,16,17,18,19,20,21,27,28.


<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 (Second 'Feature Updates' L4 under November 26, 2024 has no ko counterpart; belongs to missing 2024.08.27 Feature Updates section (k57)) -->
#### Feature Updates

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('Load Balancer' under t53 has no ko counterpart under k48; belongs to missing 2024.08.27 k58) -->
##### Load Balancer
* You can specify a port number per member.

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('Region Peering' under t53 has no ko counterpart under k48; belongs to missing 2024.08.27 k59) -->
##### Region Peering
* Added the feature to attach to VPCs created in other projects.

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('Transit Hub' under t53 has no ko counterpart under k48; belongs to missing 2024.08.27 k60) -->
##### Transit Hub
* Added the feature to share multicast domains to other projects. You can have multicast communication between VPCs created in different projects.

<a id="may-28-2024"></a>
### May 28, 2024 { #may-28-2024 }

<a id="may-28-2024-added-features"></a>
#### Added Features

##### Load Balancer

<!-- TODO: translate body -->

##### VPN Gateway

<!-- TODO: translate body -->

##### Network ACL

<!-- TODO: translate body -->

##### Service Gateway

<!-- TODO: translate body -->

##### DNS Plus

<!-- TODO: translate body -->

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('Load Balancer' L4 under May 28, 2024 has no ko L4 counterpart; ko k63 is L5 under k62) -->
#### Load Balancer
* Added the L7 load balancing feature. See [Load Balancer User Guide](/Network/Load%20Balancer/en/console-guide/).

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('VPN Gateway' L4 under May 28, 2024 has no ko L4 counterpart; ko k64 is L5 under k62) -->
#### VPN Gateway
* Added Cisco - Firepower 1000 Series to the peer gateway equipment.

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('Network ACL' L5 under t60 VPN Gateway has no ko counterpart at this nesting; ko k65 is L5 under k62) -->
##### Network ACL
* Added the Network ACL feature to the Korea (Pangyo) region.
* Integrated Network ACL with CloudTrail.

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('Service Gateway' L5 under t60 VPN Gateway has no ko counterpart at this nesting; ko k66 is L5 under k62) -->
##### Service Gateway
* Added Service Gateway-related APIs to the Public APIs. See [Service Gateway API Guide](/Network/Service%20Gateway/en/public-api/).

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('DNS Plus' L5 under t60 VPN Gateway has no ko counterpart at this nesting; ko k67 is L5 under k62) -->
##### DNS Plus
* Added the feature to set the header for health check requests, health check interval, maximum response latency (timeout), and maximum number of retries in GSLB health checks.

<a id="may-28-2024-feature-updates"></a>
#### Feature Updates

##### Service Gateway
* Added the domain field for API endpoints on the basic information tab.

<a id="march-26-2024"></a>
### March 26, 2024 { #march-26-2024 }

<a id="march-26-2024-added-features"></a>
#### Added Features

##### Transit Hub
* Added Transit Hub-related APIs to Public APIs. See [Transit Hub API Guide](/Network/Transit%20Hub/en/public-api/).

<a id="march-12-2024"></a>
### March 12, 2024 { #march-12-2024 }

<a id="march-12-2024-feature-updates"></a>
#### Feature Updates

##### DNS Plus
* Stopped support for the SPF record set type. You can use the TXT record set type instead.
    * For more information, see [RFC 7208#section-14.1](https://datatracker.ietf.org/doc/html/rfc7208#section-14.1).

<a id="february-27-2024"></a>
### February 27, 2024 { #february-27-2024 }

<a id="february-27-2024-added-features"></a>
#### Added Features

##### Floating IP
* Added the feature to protect floating IPs from deletion.

##### Load Balancer
* Added the feature to protect load balancer from deletion.
* Added L7 Load Balancing-related API to Public API. See [Load Balancer API Guide](https://docs.nhncloud.com/en/Network/Load%20Balancer/en/public-api/).

<a id="february-27-2024-feature-updates"></a>
#### Feature Updates

##### Private DNS

- Added the description field to the record set.

##### Transit Hub
* Added BLACKHOLE, which destroys packets, to the routing rule packet processing method.

<a id="november-28-2023"></a>
### November 28, 2023 { #november-28-2023 }

<a id="november-28-2023-added-features"></a>
#### Added Features

##### Load Balancer

* Added the feature to apply subnet static routes to load balancers. You can apply static routes set on the subnet to which the load balancer belongs to load balancers as well as to instances.

##### Private DNS

* Added the Private DNS service. You can configure independent DNS for each VPC. 
  * Private DNS is only available in the Korea (Pyeongchon) region and Korea (Pangyo) region.

<a id="august-29-2023"></a>
### August 29, 2023 { #august-29-2023 }

<a id="august-29-2023-added-features"></a>
#### Added Features

##### Transit Hub

* Added the Transit Hub service. The service manages VPCs through a centralized connectivity and provides routing and multicast communication between connected resources.
    * Transit Hub is only available in the Korea (Pyeongchon) and Korea (Pangyo) regions.

##### VPN Gateway

* Added the VPN Gateway feature to the Korea (Pangyo) region.

##### NAT Instance

* Added the NAT Instance feature to the Korea (Pangyo) region.

##### VPC

* Added the Routing API to Public API. See [VPC API Guide](https://docs.nhncloud.com/en/Network/VPC/en/public-api/).

##### Network ACL

* [Pyeongchon region, Korea]  Released Public API. See [Network ACL API Guide](https://docs.nhncloud.com/en/Network/Network%20ACL/en/public-api/).

<a id="may-30-2023"></a>
### May 30, 2023 { #may-30-2023 }

<a id="may-30-2023-feature-updates"></a>
#### Feature Updates

##### Network Interface

* Improved the Network Interface UI
    * Added the search feature.
    * Improved to display device names.

<a id="march-28-2023"></a>
### March 28, 2023 { #march-28-2023 }

<a id="march-28-2023-added-features"></a>
#### Added Features

##### Traffic Mirroring

* Added the Traffic Mirroring feature. Packets can be captured and routed to detection tools for purposes such as content security, threat analysis, and troubleshooting.
    * Traffic Mirroring is only available in Korea (Pyeongchon) and Korea (Pangyo) regions.

<a id="march-28-2023-feature-updates"></a>
#### Feature Updates

##### VPC

* Added the VPC and VPC Subnet API to Public API. For more information, see [VPC API Guide](https://docs.nhncloud.com/en/Network/VPC/en/public-api/). 

<a id="march-28-2023-1"></a>
#### Feature Changes

<!-- TODO: translate body -->

##### VPC, Floating IP, Security Groups, Load Balancer

<!-- TODO: translate body -->

<!-- pre-align: ko에 대응 섹션 없음 — 검토 필요 ('VPC, Floating IP, Security Groups, Load Balancer' placed as L5 under t96 Feature Updates; ko k103 is L5 under k102 (Feature Changes), which is a missing heading in target) -->
##### VPC, Floating IP, Security Groups, Load Balancer

* Changed API endpoint addresses.

<a id="january-31-2023"></a>
### January 31, 2023 { #january-31-2023 }

<a id="january-31-2023-feature-updates"></a>
#### Feature Updates

##### Colocation Gateway

* [Pyeongchon/Pangyo region, Korea] Added the feature to set a route to colocation gateway.

##### Service Gateway

* Removed the constraint where communication is only possible for service gateway within the same VPC. 
* You can use the service gateway of other VPCs via peering gateway and colocation gateway.

<a id="november-29-2022"></a>
### November, 29, 2022 { #november-29-2022 }

<a id="november-29-2022-added-features"></a>
#### Added Features

##### Peering Gateway

* [Pyeongchon/Pangyo region, Korea] Added the feature to configure a route for Peering, Project peering, and Region peering.

<a id="october-26-2022"></a>
### October 26, 2022 { #october-26-2022 }

<a id="october-26-2022-feature-updates"></a>
#### Feature Updates

##### Service Gateway

* Added a supported service
    * NCR

<a id="july-26-2022"></a>
### July 26, 2022 { #july-26-2022 }

<a id="july-26-2022-added-features"></a>
#### Added Features

##### Load Balancer

* Added the feature to change host header field values for health checks.

<a id="june-30-2022"></a>
### June 30, 2022 { #june-30-2022 }

<a id="june-30-2022-feature-updates"></a>
#### Feature Updates

##### Service Gateway

* Added a supported service
    * CloudTrail

<a id="may-24-2022"></a>
### May 24, 2022 { #may-24-2022 }

<a id="may-24-2022-added-features"></a>
#### Added Features

##### Peering Gateway

* Added the project peering feature, which allows you to connect two VPCs created in the same region but in different projects.
    * Project peering is only available in the Korea (Pyeongchon) region and the Korea (Pangyo) region.

##### VPN Gateway

* [Pyeongchon region, Korea] Added the VPN Gateway feature.

##### NAT Gateway

* [Pangyo region, Korea] Added the NAT Gateway feature.


<a id="march-29-2022"></a>
### March 29, 2022 { #march-29-2022 }

<a id="march-29-2022-added-features"></a>
#### Added Features

##### VPC

* Added the service gateway feature. You can use the service gateway IP to connect to the service selected when creating the service gateway.
    * The service gateway feature is only available in the Korea (Pyeongchon) region and the Korea (Pangyo) region.
* Added the inter-region peering feature, which allows you to connect two VPCs created in different regions.
    * Inter-region peering is only available in the Korea (Pyeongchon) region and the Korea (Pangyo) region.

<a id="january-18-2022"></a>
### January 18, 2022 { #january-18-2022 }

<a id="january-18-2022-added-features"></a>
#### Added Features

##### VPC

* Added the static route configuration feature to subnets. You can configure static routes to forward via DHCP to instances within a subnet.
* Added the feature to create and change a "centralized virtual routing table".

##### Network Interface

* Added the feature to create virtual IP for redundancy. You can preempt an IP to use as a virtual IP, and add a route to the IP in the routing table.
* Added the feature to disable network interface security settings so that the instance can be used as a gateway, firewall, etc.

<a id="january-18-2022-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Enhanced to use TLS version 1.3 with load balancers that use the TERMINATED_HTTPS protocol.

<a id="august-24-2021"></a>
### August 24, 2021 { #august-24-2021 }

<a id="august-24-2021-added-features"></a>
#### Added Features

##### DNS Plus

* Added the Create multiple record sets feature.


<a id="april-27-2021"></a>
### April 27, 2021 { #april-27-2021 }

<a id="april-27-2021-added-features"></a>
#### Added Features

##### NAT instance

* [Pyeongchon region, Korea] Added the NAT Instance feature.

##### Load Balancer

* [Pyeongchon region, Korea] Physical load balancers can be created online. To learn more about the changes from the previous load balancers, see [Load Balancer Guide](https://docs.toast.com/en/Network/Load%20Balancer/en/console-guide/#difference-between-physical-load-balancers-and-regular-load-balancer).

<a id="march-23-2021"></a>
### March 23, 2021 { #march-23-2021 }

<a id="march-23-2021-added-features"></a>
#### Added Features

##### NAT Gateway

* [Pyeongchon region, Korea] Added the NAT Gateway feature.

##### Load Balancer

* [Korea/Japan/United States] Added the Block Invalid Request feature.
* [Korea/Japan/United States regions] The default connection limit of newly created load balancers is changed from 2,000 to 60,000.

<a id="february-6-2021"></a>
### February 6, 2021 { #february-6-2021 }

<a id="february-6-2021-feature-updates"></a>
#### Feature Updates

##### VPC

* [Pangyo region, Korea] Fixed the issue where the default route (local route to the whole VPC address area) of routing table is not properly applied. Previously, even subnets within the VPC same could communicate with one another only if they are all connected to the same routing table. Now, communication is possible between subnets connected to different routing tables.


<a id="november-24-2020"></a>
### November 24, 2020 { #november-24-2020 }

<a id="november-24-2020-feature-updates"></a>
#### Feature Updates

##### Network Interface
* Added Network Interface service.

<a id="september-22-2020"></a>
### September 22, 2020 { #september-22-2020 }

<a id="september-22-2020-feature-updates"></a>
#### Feature Updates

##### DNS Plus

* Improved the application to enable the editing of the record set type when editing a record set.

<a id="august-25-2020"></a>
### August 25, 2020 { #august-25-2020 }

<a id="august-25-2020-added-features"></a>
#### Added Features

##### Network ACL

* [Pyeongchon region, Korea] Network ACL function added. Using the ACL function, you can control the access per protocol, IP, and port.

##### Load Balancer

* Public API v2 supports IP access control function. For details, refer to [Load Balancer API Guide](https://docs.toast.com/en/Network/Load%20Balancer/en/public-api/#ip-acl).

<a id="june-23-2020"></a>
### June 23, 2020 { #june-23-2020 }

<a id="june-23-2020-features-updates"></a>
#### Features Updates

##### VPC
* [Korea/Japan/United States] Changed the way to enter the IP of a gateway from manually typing in the address to selecting the device owning the IP from the Create Route window of a routing table. The devices that are not explicitly associated with a routing table in the subnet can also be selected.
* [Korea/Japan/United States] Changed the Internet gateway list to display the information of the associated routing table instead of the IP information. The name of the associated Internet gateway is also displayed in the Route tab of a routing table.

<a id="may-26-2020"></a>
### May 26, 2020 { #may-26-2020 }
<a id="may-26-2020-feature-updates"></a>
#### Feature Updates

##### VPC

* Released Public API v2, which is compatible with OpenStack API.

##### Load Balancer

* The instance of a different subnet that belongs to the same VPC as Load Balancer can be registered as a member of Load Balancer. The subnet to which Load Balancer belongs and the subnet of the instance need to be connected to the routing table.
* The instance that belongs to a peer VPC can be registered as a member of Load Balancer if the VPC to which Load Balancer belongs has a peering connection. Only the instances of the subnet connected to the default routing table of the peer VPC can be connected.
* Now, the member instance of each listener can be configured differently. Previously, all the listeners needed to have the same member instance when running multiple listeners in Load Balancer.
* Released Public API v2, which is compatible with OpenStack API.

<a id="march-24-2020"></a>
### March 24, 2020 { #march-24-2020 }

<a id="march-24-2020-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Added Certificate management through the Cert Manager service.
* By registering a certificate at Cert Manager and connecting it to the listener, you can receive an email on certificate expiration date.

<a id="february-25-2020"></a>
### February 25, 2020 { #february-25-2020 }

<a id="february-25-2020-feature-updates"></a>
#### Feature Updates

##### Security Group

* Added "Description" entry to security group rules. You can add description for each security group rule.

<a id="december-24-2019"></a>
### December 24, 2019 { #december-24-2019 }

<a id="december-24-2019-added-features"></a>
#### Added Features

##### DNS Plus

* Added GSLB (Global Server Load Balancing) to allow stable load balancing of traffic at an endpoint server.
* The GSLB domain can be configured either, according to routing rules, Disaster Recovery (DR), Random, or Global Load Balancing.
* The pool serves as a grouping element for endpoint servers at the minimum unit so as to apply the routing rule.
* Health check is conducted on a regular basis for endpoint servers included to a pool so as to support stable services. Health check is supported for HTTP/HTTPS/TCP.

<a id="december-24-2019-feature-updates"></a>
#### Feature Updates

##### DNS Plus

* Updated to select user's GSLB domain for CNAME record set type, for creating/updating the record set.

<a id="december-17-2019"></a>
### December 17. 2019 { #december-17-2019 }

<a id="december-17-2019-feature-updates"></a>
#### Feature Updates
* [Korea/Japan/US Region] Every network interface connected with an instance can be assosicated with each floating IP.

<a id="october-29-2019"></a>
### October 29, 2019 { #october-29-2019 }

<a id="october-29-2019-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Added the feature of notification via web console, for chain certificate registration, when an individual certificate which is included in the certificate file has an invalid format.

<a id="august-27-2019"></a>
### August 27, 2019 { #august-27-2019 }

<a id="august-27-2019-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* It is available to specify TLS version to communicate with clients via TERMINATED_HTTPS load balancer.
    * For more details on the setting of load balancer in TLS version, see [user guide](https://docs.toast.com/en/Network/Load%20Balancer/en/overview/#ssltls-version-for-load-balancer).

##### DNS Plus

* Exceeded the maximum available number of record sets to be created. For each DNS zone, up to 5,000 record sets can be created.
* Modified, in the query of record set statistics for CNAME, to query A record set type along with AAAA record set type.

<a id="june-25-2019"></a>
### June 25, 2019 { #june-25-2019 }

<a id="june-25-2019-release-of-new-products"></a>
#### Release of New Products

##### DNS Plus

* DNS Plus provides features for domain management.
* It is easy to configure a DNS server.

<a id="may-30-2019"></a>
### May 30, 2019 { #may-30-2019 }

<a id="may-30-2019-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* [Japan Region] IP access control is available.
    * IP-based access control is available for load balancer.
    * For more details on IP access control, see user guides.

<a id="may-28-2019"></a>
### May 28, 2019 { #may-28-2019 }

<a id="may-28-2019-feature-updates"></a>
#### Feature Updates

##### VPC

* [Korea Region] Creating a peering can be made available again.

<a id="april-25-2019"></a>
### April 25, 2019 { #april-25-2019 }

<a id="april-25-2019-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* IP access control is available.
    * IP-based access control is available at load balancer.
    * For more details on IP access control features, see User Guide.
    * List of IPs for control has been auto-applied to the IP access control group named Default.

<a id="december-27-2018"></a>
### December 27, 2018 { #december-27-2018 }

<a id="december-27-2018-feature-updates"></a>
#### Feature Updates

##### VPC

* Creating a new peering is not going to be provided for the time being, due to concerns for packet flooding between peered VPCs.
	Such concerns, however, are not related to communication between previously created peering, and features are provided as usual, except peering creation.

<a id="november-27-2018"></a>
### November 27, 2018 { #november-27-2018 }

<a id="november-27-2018-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer

* Fixed a bug occurring when a listener is added to load balancer, in which, an instance member that is newly added to a deactivate instance is created while activated.

<a id="november-27-2018-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Added the statistics feature for load balancing, with the following statistical volume provided on a chart.
    * Session count, Session increase volume of client per second, Session increase volume of instance per second, In/Out traffic volume, Number of exceptions to load balancing
    * Statistics on deleted load balancers, listeners, or members are not provided.
    * Traffic volume does not include L2, L3, and L4 headers.
    * For more details, see User Guide.


<a id="september-20-2018"></a>
### September 20, 2018 { #september-20-2018 }

<a id="september-20-2018-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer

* Fixed an issue in which some listener members still remain after an instance which is registered as member of load balancer is deleted.

<a id="september-20-2018-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Added dedicated load balancer services.
* Since dedicated load balancer services are created by occupying hardware resources, 1Gbps bandwidth for 48 thousand concurrent sessions are supported.

<a id="august-28-2018"></a>
### August 28, 2018 { #august-28-2018 }

<a id="august-28-2018-bug-fixes"></a>
#### Bug Fixes

##### VPC

* Fixed an issue in which deleting may be tried to VPC with subnets that have routes

<a id="august-28-2018-feature-updates"></a>
#### Feature Updates

##### VPC

* Updated the maximum available numbers to create subnet, routing table, and route.
* Check the maximum available numbers to create each resource of VPC from description on the right of the popup.
    * Subnet: Available up to 10 for each VPC.
    * Routing Table: Available up to 10 for each VPC.
    * Route: Available up to 10 for each routing table.

##### Load Balancer

* For TCP or HTTPS protocol, a proxy protocol can be activated to check client IP.
* Keepalive timeout can be configured for load balancer.


<a id="april-24-2018"></a>
### April 24, 2018 { #april-24-2018 }

<a id="april-24-2018-bug-fixes"></a>
#### Bug Fixes

##### VPC

* Fixed failed access to load balancer of a peer VPC from instance of a local VPC.

<a id="april-24-2018-feature-updates"></a>
#### Feature Updates

##### VPC

* You can find information of attached resources on Overview of VPC, Subnet, Routing Table, and Internet Gateway.

##### Floating IP

* Applied pagination to Floating IP list.

##### Security Group

* Added rule editing.

##### Load Balancer

* Changed the Keeaplive Timeout to 5 minutes.
* Up to 60,000 session limit can be configured for listener.

<a id="march-22-2018"></a>
### March 22, 2018 { #march-22-2018 }

<a id="march-22-2018-bug-fixes"></a>
#### Bug Fixes

##### VPC

* Fixed failure in getting an IP via DHCP when an instance is attached to a newly added subnet.
* Fixed an issue in which the same target of a previous routing policy may be entered to add a routing policy.
* Fixed infrequently failed communication of an instance associated to a floating IP with an instance located at a different subnet.

<a id="february-22-2018"></a>
### February 22, 2018 { #february-22-2018 }

<a id="february-22-2018-bug-fixes"></a>
#### Bug Fixes

##### VPC

* Fixed failed traffic from an instance associated with floating IP to a local network.

<a id="february-22-2018-feature-updates"></a>
#### Feature Updates

##### Adopted VPC as Basic Model for Network

* You can use many subnets.
* A port can be created by the subnet and attached to an instance.
* More routing policies can be added.
* Added the peering feature for communication between VPCs.
* Many VPC ports may be added to or deleted from an instance.
* For more details, Overview and User Guide of VPC.


<a id="november-23-2017"></a>
### November 23, 2017 { #november-23-2017 }

<a id="november-23-2017-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed the display of invalid connection limit for listener, when a load balancer is created.

<a id="october-26-2017"></a>
### October 26, 2017 { #october-26-2017 }

<a id="october-26-2017-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed failure in certificate registration when a load balancer is created.

<a id="september-21-2017"></a>
### September 21, 2017 { #september-21-2017 }

<a id="september-21-2017-added-features"></a>
#### Added Features

##### Added Public API

* Like Object Storage, you can also manage Compute & Network by using APIs.
* The feature is limited at the moment, but will be extended by adding more APIs.

<a id="september-21-2017-bug-fixes"></a>
#### Bug Fixes

* Fixed to disallow users without project admin authority to modify security group.
* Updated not to show the Network menu to users, except authorized admin users of a project.

<a id="august-24-2017"></a>
### August 24, 2017 { #august-24-2017 }

<a id="august-24-2017-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed a bug in which the session persistence of load balancer did not show properly.

<a id="april-20-2017"></a>
### April 20, 2017 { #april-20-2017 }

<a id="april-20-2017-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed a bug in which the popup for certificate registration is frequently missing while uploading certificate files to listener.


<a id="march-23-2017"></a>
### March 23, 2017 { #march-23-2017 }

<a id="march-23-2017-bug-fixes"></a>
#### Bug Fixes
##### Floating IP
* Fixed failed display of the "Create" button on the popup for associating with floating IP.


<a id="february-23-2017"></a>
### February 23, 2017 { #february-23-2017 }

<a id="february-23-2017-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Updated to notify that deleting a listener is unavailable, if there is only one registered listener to a load balancer.
	  * There's no defacto change in the process: sending no notification may have been confusing to some users.
	  * The updated version now allows the user to be notified clearly that it is unavailable to delete.

##### Floating IP

* Updated to prevent a floating IP from being deleted, if it is associated with an instance or a load balancer.
	  * Previously, deleting a floating IP which is associated with an instance or a load balancer might have caused a failure to service.
	  * To prevent any potential error, the updated version disallows an associated floating IP to be deleted.
* Name Changes: 'Port' -> 'Network Interface'
	  * Name for the target of floating IP to be associated with is changed from "Port" to "Network Interface".


<a id="january-19-2017"></a>
### January 19, 2017 { #january-19-2017 }

<a id="january-19-2017-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed the issue in which the restricted connection setting was not applied when creating a load balancer.



<a id="december-22-2016"></a>
### December 22, 2016 { #december-22-2016 }

<a id="december-22-2016-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed failed editing of listener when the Health Check Protocol is TCP.

##### Floating IP
* Fixed failed display of the name of load balancer associated with floating IP.

##### Security Group
* Fixed an issue in which security group list disappears when a duplicate rule is added.






<a id="december-8-2016"></a>
### December 8, 2016 { #december-8-2016 }

<a id="december-8-2016-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed failed display of Health Check URL of load balancer.
* Fixed the show of "/", instead of a registered Health Check URL, at the click of Edit Listener,








<a id="november-29-2016"></a>
### November 29, 2016 { #november-29-2016 }

<a id="november-29-2016-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed failure in creating TERMINATED_HTTPS-type load balancers.



<a id="november-24-2016"></a>
### November 24, 2016 { #november-24-2016 }

<a id="november-24-2016-feature-updates"></a>
#### Feature Updates
##### Load Balancer
* Updated to show the value of session limit per listener of load balancer.

<a id="november-24-2016-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed failure in creating load balancers at a particular project.

<a id="august-4-2016"></a>
### August 4, 2016 { #august-4-2016 }

<a id="august-4-2016-feature-updates"></a>
#### Feature Updates
##### Load Balancer
* Added SSL offloading of load balancer.

<a id="august-4-2016-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed infrequent failure in closing when load balancer is removed.
