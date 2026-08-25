<!-- pre-align:aligned sig=3251e04c861f -->

<a id="network-release-notes"></a>
## Network > Release Notes { #network-release-notes }

<a id="august-25-2026"></a>
### 2026. 08. 25. { #august-25-2026 }

#### Added Features

##### Service Gateway
* Added the custom endpoint feature. If the user publishes his own load balancer on the endpoint, he can access it via Service Gateway from another project without an internet connection.
	* Custom endpoint is only available in the Korea (Pyeongchon) region and Korea (Pangyo) region.

##### Load Balancer
* Added the feature for HTTP/2 support. It is available when the listener protocol is TERMINATED_HTTPS and the member group protocol is HTTP or HTTP_REENCRYPT.
	* You can select the protocol version on the screen for listener and member group settings. HTTP/1 is the default.
* Added the feature to select the load balancer engine version (`v1`/`v2`). A new load balancer is created with the latest version (`v2`), and the engine version can be changed by load balancer type.                                             
    * Since some actions, including HTTP traffic handling, can be different by engine version, you must apply the version to the operating environment after verifying it.
* See [Load Balancer Console User Guide](/Network/Load%20Balancer/zh/console-guide/).

#### Feature Updates

##### Flow Log
* The timezone template variable (`#{timezone}`) can be added as an option in customizing the Flow Log file name.
    * When customizing a file name, timezone is displayed on the file name if `#{timezone}` variable is included and is not displayed if the variable is not included.
    * The default file name includes the timezone as the existing file name. The timezone value is chosen by region (KST for the Korea region).
    * See [Flow Log Console User Guide](/Network/Flow%20Log/zh/console-guide/).


<a id="may-27-2026"></a>
### May 27, 2026 { #may-27-2026 }

<a id="may-27-2026-added-features"></a>
#### Added Features

##### Network Interface
* Renamed the "Source/Destination Check" feature to "Anti-Spoofing" and moved its configuration to the network interface creation and modification screens.
* Added the "Additional Allowed Addresses" configuration feature, which allows spoofing for specific addresses while Anti-Spoofing is enabled.
* For more information, see the [Network Interface Console User Guide](/Network/Network%20Interface/zh/console-guide/).

##### Load Balancer (DSR)
* Added the Load Balancer (DSR) service. It provides a load balancer that operates in Direct Server Return (DSR) mode.
	* Load Balancer (DSR) is available only in the Korea (Pyeongchon) and Korea (Pangyo) regions.
* For more information, see the [Load Balancer (DSR) Console User Guide](/Network/Load%20Balancer(DSR)/zh/console-guide/).

<a id="may-27-2026-feature-updates"></a>
#### Feature Updates

##### Load Balancer
* Added a re-encryption feature. Selecting `HTTP_REENCRYPT` as the protocol for a member group enables SSL encrypted communication when forwarding to members.
* Added the HTTP Keepalive disable feature. Selecting "Disabled" when configuring the Keepalive timeout disables Keepalive.
* Added the SSL/TLS encryption policy configuration feature. Users can customize the SSL/TLS cipher suite.

##### Flow Log
* Added the `traffic_path` field.
    * The network path that a packet traversed (VPC Local, Internet Gateway, VPN Gateway, VPC Peering, Region Peering, Project Peering, Service Gateway) can be viewed as an integer value.
    * For more information, see [Flow Log Overview](/Network/Flow%20Log/zh/overview/).

<a id="may-27-2026-may-27-2026-feature-updates"></a>
#### Feature Updates

##### VPC
* The internal traffic handling method for VPCs has been partially changed to support network service integration. This applies to newly created VPCs.

<a id="april-14-2026"></a>
### April 14, 2026 { #april-14-2026 }

<a id="april-14-2026-added-features"></a>
#### Added Features

##### DNS Plus
* Added API v2.0
    * Supports User Access Key tokens.

<a id="november-25-2025"></a>
### November 25, 2025 { #november-25-2025 }

<a id="november-25-2025-added-features"></a>
#### Added Features

##### VPN Gateway
* When you connect a Transit Hub to a VPC with a VPN connection, VPN communication with on-premises networks is also supported from VPCs of other projects connected via the Transit Hub. (An additional VPN Connection must be created for the connected bandwidth.)

##### Service Gateway
* Improved so that you can create a Service Gateway with a fixed NAT IP.

##### Traffic Mirroring
* Added Traffic Mirroring-related APIs to the Public API. See the [Traffic Mirroring API Guide](/Network/Traffic%20Mirroring/zh/public-api/).

##### Load Balancer
* Added the custom response configuration feature per listener.
* Added the feature to enable/disable X-Forwarded-* headers.

<a id="november-25-2025-feature-updates"></a>
#### Feature Updates

##### Load Balancer
* Multiple SSL certificate registration/management is now supported in the console.

<a id="november-25-2025-november-25-2025-feature-updates"></a>
#### Feature Updates

##### DNS Plus
* Changed the maximum length of record values for TXT record set types from 255 bytes to 4,096 bytes.

<a id="august-26-2025"></a>
### August 26, 2025 { #august-26-2025 }

<a id="august-26-2025-added-features"></a>
#### Added Features

##### VPN Gateway
* Released v2.
* When creating a VPN gateway, a local gateway address is assigned and can be viewed in the console.
* You can configure multiple peer gateway connections in a single VPC.
* In the same project, you can configure connections from multiple VPCs to a single peer gateway.
* IKE v2 connections are supported.
* VPN connections between regions where the VPN gateway service is available are supported (devices must be configured as Fortinet - Fortigate Series).
* With the release of v2, creation of new v1 VPN gateways is restricted.

##### Load Balancer
* Added load balancer metrics — including CPU usage, listener-level statistics, and socket connection status — which can now be monitored through the Cloud Monitoring service.

<a id="may-27-2025"></a>
### May 27, 2025 { #may-27-2025 }

<a id="may-27-2025-added-features"></a>
#### Added Features

##### NAT Gateway
* Added APIs related to NAT Gateway to the Public API. See the [NAT Gateway API Guide](/Network/NAT%20Gateway/zh/public-api/).

##### Security Groups
* Added an API to retrieve Security Groups connection information to the Public API. See the [Security Groups API Guide](/Network/Security%20Groups/zh/public-api/).
* Added bulk creation of security rules and security rule list download features.

##### Internet Gateway
* Added APIs related to Internet Gateway to the Public API. See the [Internet Gateway API Guide](/Network/Internet%20Gateway/zh/public-api/).

##### Colocation Gateway
* Added APIs related to Colocation Gateway to the Public API. See the [Colocation Gateway API Guide](/Network/Colocation%20Gateway/zh/public-api/).

##### Private DNS
* Added APIs related to Private DNS to the Public API. See the [Private DNS API Guide](/Network/Private%20DNS/zh/public-api/).

##### Floating IP
* Added a label configuration feature to Floating IP. See the [Floating IP Console User Guide](/Network/Floating%20IP/zh/console-guide/).

##### Flow Log
* Added support for creating Flow Logs targeting the network interfaces of Region peering gateway, Project peering gateway, Colocation gateway, and load balancers.

<a id="may-27-2025-feature-updates"></a>
#### Feature Updates
##### Flow Log
* Improved so that you can freely edit folder and file names when saving Flow Log files to OBS.

<a id="april-29-2025"></a>
### April 29, 2025 { #april-29-2025 }

<a id="april-29-2025-feature-updates"></a>
#### Feature Updates

##### DNS Plus
* Changed the minimum value of the record set TTL from 1 to 10.

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
* Added support for creating Flow Logs targeting Transit Hub connections.
* Added VPC and Subnet to Flow Log Collection Target.

##### Routing
* Added a description field to Route. You can enter a value when creating or changing a route, and it will appear in the route information.
* Added the ability to change the CIDR and gateway fields of a route.

<a id="november-26-2024"></a>
### November 26, 2024 { #november-26-2024 }

<a id="november-26-2024-feature-updates"></a>
#### Feature Updates

##### Peering Gateway
* Added a description field to peering. You can enter a description for the peering when creating or changing it, and it will appear in the peering basic information.

##### Flow Log
* Added Gzip compression support.
* Improved so that you can select only the statistical information items that you want to record from the items supported by Flow Log. For supported statistical items, see [Flow Log Overview](/Network/Flow%20Log/zh/overview/).

<a id="august-27-2024"></a>
### August 27, 2024 { #august-27-2024 }

<a id="august-27-2024-added-features"></a>
#### Added Features

##### Flow Log
* Added the Flow Log service. Flow Log allows you to collect and store information about IP traffic sent to and received from a network interface.
    * Flow Log is only available in the Korea (Pyeongchon) region and Korea (Pangyo) region.

##### Routing
* Added API to get gateway information associated with routing tables to the Public API. See the [VPC API Guide](/Network/VPC/zh/public-api/).

##### VPN Gateway
* Added support for Diffie-Hellman groups 14, 15, 16, 17, 18, 19, 20, 21, 27, and 28.


<a id="august-27-2024-feature-updates"></a>
#### Feature Updates

##### Load Balancer
* You can specify a port number per member.

##### Region Peering
* Added the feature to attach to VPCs created in other projects.

##### Transit Hub
* Added the feature to share multicast domains to other projects. You can have multicast communication between VPCs created in different projects.

<a id="may-28-2024"></a>
### May 28, 2024 { #may-28-2024 }

<a id="may-28-2024-added-features"></a>
#### Added Features

##### Load Balancer
* Added L7 load balancing. See the [Load Balancer User Guide](/Network/Load%20Balancer/zh/console-guide/).

##### VPN Gateway
* Added the Cisco - Firepower 1000 Series to the list of supported peer gateway devices.

##### Network ACL
* Added the Network ACL feature in the Korea (Pangyo) region.
* Integrated Network ACL with CloudTrail.

##### Service Gateway
* Added Service Gateway-related APIs to the Public API. See the [Service Gateway API Guide](/Network/Service%20Gateway/zh/public-api/).

##### DNS Plus
* Added the feature to set the header for health check requests, health check cycle, maximum response latency, and maximum number of retries in GSLB health checks.

<a id="may-28-2024-feature-updates"></a>
#### Feature Updates

##### Service Gateway
* Added the API endpoint domain field to the Basic Information tab.

<a id="march-26-2024"></a>
### March 26, 2024 { #march-26-2024 }

<a id="march-26-2024-added-features"></a>
#### Added Features

##### Transit Hub
* Added Transit Hub-related APIs to the Public API. See the [Transit Hub API Guide](/Network/Transit%20Hub/zh/public-api/).

<a id="march-12-2024"></a>
### March 12, 2024 { #march-12-2024 }

<a id="march-12-2024-feature-updates"></a>
#### Feature Updates

##### DNS Plus
* Stopped support for the SPF record set type. You can use the TXT record set type instead.
    * For more information, see [[RFC 7208#section-14.1]](https://datatracker.ietf.org/doc/html/rfc7208#section-14.1).

<a id="february-27-2024"></a>
### February 27, 2024 { #february-27-2024 }

<a id="february-27-2024-added-features"></a>
#### Added Features

##### Floating IP
* Added deletion protection for Floating IP.

##### Load Balancer
* Added deletion protection for load balancers.
* Added L7 load balancing-related APIs to the Public API. See the [Load Balancer API Guide](https://docs.nhncloud.com/ko/Network/Load%20Balancer/ko/public-api/).

<a id="february-27-2024-feature-updates"></a>
#### Feature Updates

##### Private DNS

- Added the description field to record sets.

##### Transit Hub
* Added BLACKHOLE to the routing rule packet processing method. BLACKHOLE drops packets.

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

* Added the Transit Hub service. It manages VPCs through centralized connectivity and provides routing and multicast communication between connected resources.
    * Transit Hub is available only in the Korea (Pyeongchon) and Korea (Pangyo) regions.

##### VPN Gateway

* Added VPN Gateway to the Korea (Pangyo) region.

##### NAT Instance

* Added the NAT instance feature to the Korea (Pangyo) region.

##### VPC

* Added Routing API to the Public API. For more information, see the [VPC API Guide](https://docs.nhncloud.com/ko/Network/VPC/ko/public-api/).

##### Network ACL

* Released the Public API for Korea (Pyeongchon). For more information, see the [Network ACL API Guide](https://docs.nhncloud.com/ko/Network/Network%20ACL/ko/public-api/).

<a id="may-30-2023"></a>
### May 30, 2023 { #may-30-2023 }

<a id="may-30-2023-feature-updates"></a>
#### Feature Updates

##### Network Interface

* Improved the Network Interface UI.
    * Added a search feature.
    * Improved the interface to display device names.

<a id="march-28-2023"></a>
### March 28, 2023 { #march-28-2023 }

<a id="march-28-2023-added-features"></a>
#### Added Features

##### Traffic Mirroring

* Added the Traffic Mirroring feature. You can capture packets and route them to detection tools for purposes such as content security, threat analysis, and troubleshooting.
    * Traffic Mirroring is available only in the Korea (Pyeongchon) and Korea (Pangyo) regions.

<a id="march-28-2023-feature-updates"></a>
#### Feature Updates

##### VPC

* Added VPC and VPC Subnet APIs to the Public API. For more information, see the [VPC API User Guide](https://docs.nhncloud.com/ko/Network/VPC/ko/public-api/).

<a id="march-28-2023-march-28-2023-feature-updates"></a>
#### Feature Updates

##### VPC, Floating IP, Security Groups, Load Balancer

* Changed the API endpoint address.

<a id="january-31-2023"></a>
### January 31, 2023 { #january-31-2023 }

<a id="january-31-2023-feature-updates"></a>
#### Feature Updates

##### Colocation Gateway

* [Korea Pyeongchon/Pangyo regions] Added the ability to configure routes on the colocation gateway.

##### Service Gateway

* Removed the restriction that limited communication to service gateways within the same VPC.
* You can now use a service gateway in another VPC by routing through a peering gateway or colocation gateway.

<a id="november-29-2022"></a>
### November 29, 2022 { #november-29-2022 }

<a id="november-29-2022-added-features"></a>
#### Added Features

##### Peering Gateway

* [Korea Pyeongchon/Pangyo regions] Added the ability to configure routes for peering, project peering, and region peering.

<a id="october-4-2022"></a>
### October 4, 2022 { #october-4-2022 }

<a id="october-4-2022-feature-updates"></a>
#### Feature Updates

##### Service Gateway

* Added supported services:
    * NCR

<a id="july-26-2022"></a>
### July 26, 2022 { #july-26-2022 }

<a id="july-26-2022-added-features"></a>
#### Added Features

##### Load Balancer

* Added the ability to change the host header field value during health checks.

<a id="june-30-2022"></a>
### June 30, 2022 { #june-30-2022 }

<a id="june-30-2022-feature-updates"></a>
#### Feature Updates

##### Service Gateway

* Added supported services:
    * CloudTrail

<a id="may-24-2022"></a>
### May 24, 2022 { #may-24-2022 }

<a id="may-24-2022-added-features"></a>
#### Added Features

##### Peering Gateway

* Added the project peering feature. You can connect two VPCs created in the same region but in different projects.
    * Project peering is available only in the Korea (Pyeongchon) and Korea (Pangyo) regions.

##### VPN Gateway

* [Korea Pyeongchon region] Added VPN Gateway.

##### NAT Gateway

* [Korea Pangyo region] Added the NAT Gateway feature.

<a id="march-29-2022"></a>
### March 29, 2022 { #march-29-2022 }

<a id="march-29-2022-added-features"></a>
#### Added Features

##### VPC

* Added the service gateway feature. You can use a service gateway IP to connect the service selected when creating the service gateway.
    * Service Gateway is available only in the Korea (Pyeongchon) and Korea (Pangyo) regions.
* Added the region peering feature. You can connect two VPCs created in different regions.
    * Region peering is available only in the Korea (Pyeongchon) and Korea (Pangyo) regions.

<a id="january-18-2022"></a>
### January 18, 2022 { #january-18-2022 }

<a id="january-18-2022-added-features"></a>
#### Added Features

##### VPC

* Added the static route configuration feature for subnets. You can configure static routes to be delivered to instances in the subnet via DHCP.
* Added the ability to create and modify a "Centralized routing table".

##### Network Interface

* Added the ability to create a virtual IP for redundancy. You can reserve an IP for use as a virtual IP and add a route to that IP in the routing table.
* Added the ability to disable security settings on a network interface so that instances can be used as gateways or firewalls.

<a id="january-18-2022-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Improved load balancers using the TERMINATED_HTTPS protocol to support TLS 1.3.

<a id="august-24-2021"></a>
### August 24, 2021 { #august-24-2021 }

<a id="august-24-2021-added-features"></a>
#### Added Features

##### DNS Plus

* Added the ability to create record sets in bulk.

<a id="april-27-2021"></a>
### April 27, 2021 { #april-27-2021 }

<a id="april-27-2021-added-features"></a>
#### Added Features

##### NAT Instance

* [Korea Pyeongchon region] Added the NAT instance feature.

##### Load Balancer

* [Korea Pyeongchon region] Added the ability to create a physical load balancer online. For changes compared to the existing load balancer, see the [Load Balancer Guide](https://docs.toast.com/ko/Network/Load%20Balancer/ko/console-guide/#_19).

<a id="march-23-2021"></a>
### March 23, 2021 { #march-23-2021 }

<a id="march-23-2021-added-features"></a>
#### Added Features

##### NAT Gateway

* [Korea Pyeongchon region] Added the NAT Gateway feature.

##### Load Balancer

* [Korea/Japan/US regions] Added the ability to block invalid requests.
* [Korea/Japan/US regions] Changed the default connection limit for newly created load balancers from 2,000 to 60,000.

<a id="february-6-2021"></a>
### February 6, 2021 { #february-6-2021 }

<a id="february-6-2021-feature-updates"></a>
#### Feature Updates

##### VPC

* [Korea Pangyo region] Fixed an issue where the default route of the routing table (local route covering the entire VPC address range) was not applied. Previously, communication was only possible between subnets connected to the same routing table, even if they were within the same VPC. Now, communication is also possible between subnets connected to different routing tables.

<a id="november-24-2020"></a>
### November 24, 2020 { #november-24-2020 }

<a id="november-24-2020-added-features"></a>
#### Added Features

##### Network Interface

* Added the Network Interface feature.

<a id="september-22-2020"></a>
### September 22, 2020 { #september-22-2020 }

<a id="september-22-2020-feature-updates"></a>
#### Feature Updates

##### DNS Plus

* Improved the record set editing feature to allow modification of the record set type.

<a id="august-25-2020"></a>
### August 25, 2020 { #august-25-2020 }

<a id="august-25-2020-added-features"></a>
#### Added Features

##### Network ACL

* [Korea Pyeongchon region] Added the Network ACL feature. You can use the ACL feature to control access by protocol, IP, and port.

##### Load Balancer

* Added IP access control support to Public API v2. For more information, see the [Load Balancer API Guide](https://docs.toast.com/ko/Network/Load%20Balancer/ko/public-api/#ip-acl).

<a id="june-23-2020"></a>
### June 23, 2020 { #june-23-2020 }

<a id="june-23-2020-feature-updates"></a>
#### Feature Updates

##### VPC

* [Korea/Japan/US regions] Changed the gateway field in the route creation window of the routing table from manually entering an IP address to selecting the device that owns the IP. You can also select devices from subnets that are not explicitly associated with the routing table.
* [Korea/Japan/US regions] Changed the internet gateway list to display information about the associated routing table instead of IP information. The name of the associated internet gateway is also displayed on the Routes tab of the routing table.

<a id="may-26-2020"></a>
### May 26, 2020 { #may-26-2020 }

<a id="may-26-2020-feature-updates"></a>
#### Feature Updates

##### VPC

* Public API v2 is now available. Public API v2 is compatible with the OpenStack API.

##### Load Balancer

* You can now register instances from other subnets within the same VPC as the load balancer as members of the load balancer. The subnet of the load balancer and the subnet of the instance must be connected to a routing table.
* If the VPC that the load balancer belongs to has a peering connection, you can register instances from the peer VPC as members of the load balancer. Only instances in subnets connected to the default routing table of the peer VPC can be added.
* Previously, when running multiple listeners on a load balancer, the same member instances had to be configured for all listeners. Now, you can configure different member instances per listener.
* Public API v2 is now available. Public API v2 is compatible with the OpenStack API.

<a id="march-24-2020"></a>
### March 24, 2020 { #march-24-2020 }

<a id="march-24-2020-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Added certificate management via the Cert Manager service.
* You can register a certificate in the Cert Manager service and associate it with a listener to receive email alerts for certificate expiration.

<a id="february-25-2020"></a>
### February 25, 2020 { #february-25-2020 }

<a id="february-25-2020-feature-updates"></a>
#### Feature Updates

##### Security Group

* Added a "Description" field to security group rules. You can now add a description to each security group rule.

<a id="december-24-2019"></a>
### December 24, 2019 { #december-24-2019 }

<a id="december-24-2019-added-features"></a>
#### Added Features

##### DNS Plus

* Added the GSLB (global server load balancing) feature that allows reliable load balancing of traffic of an endpoint server.
* The created GSLB domain can be configured with DR (disaster recovery), random load balancing, or global load balancing according to the routing rule.
* A pool is the smallest unit to which routing rules can be applied, and it groups endpoint servers together.
* Supports reliable services by periodically performing health checks on the endpoint servers included in the pool. Health check supports HTTP, HTTPS, and TCP.

<a id="december-24-2019-feature-updates"></a>
#### Feature Updates

##### DNS Plus

* Made improvements so that, when creating or modifying record sets, users can enter the CNAME record set type by selecting from their own GSLB domains.

<a id="december-17-2019"></a>
### December 17, 2019 { #december-17-2019 }

<a id="december-17-2019-feature-updates"></a>
#### Feature Updates

* [Korea/Japan/US region] You can now associate a floating IP with each network interface connected to an instance.

<a id="october-29-2019"></a>
### October 29, 2019 { #october-29-2019 }

<a id="october-29-2019-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* [Korea/Japan region] Added a notification feature that alerts you through the web console when an individual certificate in the certificate file has an invalid format while registering a chain certificate.

<a id="august-27-2019"></a>
### August 27, 2019 { #august-27-2019 }

<a id="august-27-2019-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* [Korea/Japan region] You can now specify the TLS version for communication with clients on a TERMINATED_HTTPS load balancer.
    * For more information about the load balancer TLS version setting feature, see the [User Guide](https://docs.toast.com/ko/Network/Load%20Balancer/ko/overview/#ssltls).

##### DNS Plus

* Added the maximum number of record sets that can be created. You can create up to 5,000 record sets per DNS Zone.
* Made a modification so that, when querying record set statistics, query for the CNAME record set type retrieves the A record set type and the AAAA record set type as well.

<a id="june-25-2019"></a>
### June 25, 2019 { #june-25-2019 }

<a id="june-25-2019-new-service-launch"></a>
#### New Service Launch

##### DNS Plus

* DNS Plus is a service that provides domain management features.
* You can configure DNS servers.

<a id="may-30-2019"></a>
### May 30, 2019 { #may-30-2019 }

<a id="may-30-2019-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* [Japan region] IP access control is now available.
    * IP-based access control is now available for the load balancer.
    * For more information about IP access control, see the user guide.

<a id="may-28-2019"></a>
### May 28, 2019 { #may-28-2019 }

<a id="may-28-2019-feature-updates"></a>
#### Feature Updates

##### VPC

* [Korea region] The peering creation feature is available again.

<a id="april-25-2019"></a>
### April 25, 2019 { #april-25-2019 }

<a id="april-25-2019-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* IP access control is now available.
    * IP-based access control is now available for the load balancer.
    * For more information about IP access control, see the user guide.
    * The list of IP addresses requested for access control via wired communication has been automatically added to the IP access control group named "Default".

<a id="december-27-2018"></a>
### December 27, 2018 { #december-27-2018 }

<a id="december-27-2018-feature-updates"></a>
#### Feature Updates

##### VPC

* Due to the possibility of packet flooding during communication between two peered VPCs, the peering creation feature will not be available for the time being.
	Communication for existing peerings is not affected, and all other features except peering creation remain available.

<a id="november-27-2018"></a>
### November 27, 2018 { #november-27-2018 }

<a id="november-27-2018-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer

* Fixed an issue where, when adding a new listener to a load balancer, instance members added to disabled instances were created in an active state.

<a id="november-27-2018-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Added a load balancing statistics feature that provides the following metrics in chart format:
    * Number of sessions, client sessions per second, instance sessions per second, inbound traffic, outbound traffic, and number of instances excluded from load balancing
    * Statistics for deleted load balancers, listeners, and members are not provided.
    * Traffic volume does not include L2, L3, or L4 headers.
    * For more information, see the user guide.

<a id="september-20-2018"></a>
### September 20, 2018 { #september-20-2018 }

<a id="september-20-2018-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer

* Fixed an issue where, when deleting an instance registered as a member of a load balancer, the member remained in some listeners.

<a id="september-20-2018-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Added the dedicated load balancer service.
* The dedicated load balancer is created by reserving hardware resources and supports 1 Gbps of bandwidth and 480,000 concurrent sessions.

<a id="august-28-2018"></a>
### August 28, 2018 { #august-28-2018 }

<a id="august-28-2018-bug-fixes"></a>
#### Bug Fixes

##### VPC

* Fixed an issue where it was possible to attempt deletion of a VPC that had subnets with routes.

<a id="august-28-2018-feature-updates"></a>
#### Feature Updates

##### VPC

* Adjusted the maximum number of subnets, routing tables, and routes that can be created.
* You can check the maximum number of resources that can be created for each VPC resource in the description area on the right side of the resource creation window.
    * Subnets: Up to 10 per VPC.
    * Routing tables: Up to 10 per VPC.
    * Routes: Up to 10 per routing table.

##### Load Balancer

* When using TCP or HTTPS protocols, you can enable the Proxy Protocol to identify the client's IP address.
* You can configure the keepalive timeout value for the load balancer.

<a id="april-24-2018"></a>
### April 24, 2018 { #april-24-2018 }

<a id="april-24-2018-bug-fixes"></a>
#### Bug Fixes

##### VPC

* Fixed an issue where instances in the local VPC could not connect smoothly to the load balancer in the peer VPC during peering.

<a id="april-24-2018-feature-updates"></a>
#### Feature Updates

##### VPC

* You can now view connected resource information on the overview pages for VPC, subnets, routing tables, and internet gateways.

##### Floating IP

* Added pagination to the floating IP list.

##### Security Group

* Added the rule editing feature.

##### Load Balancer

* Changed the Keepalive Timeout to 5 minutes.
* You can now set the session limit for a listener to up to 60,000.

<a id="march-22-2018"></a>
### March 22, 2018 { #march-22-2018 }

<a id="march-22-2018-bug-fixes"></a>
#### Bug Fixes

##### VPC

* Fixed an issue where instances connected to a newly added subnet could not obtain an IP address via DHCP.
* Fixed an issue where a routing policy with the same target as an existing routing policy could be added.
* Fixed an issue where instances with a floating IP could intermittently not communicate with instances in other subnets.

<a id="february-22-2018"></a>
### February 22, 2018 { #february-22-2018 }

<a id="february-22-2018-bug-fixes"></a>
#### Bug Fixes

##### VPC

* Fixed an issue where traffic from instances with a floating IP was not forwarded to the local network.

<a id="february-22-2018-feature-updates"></a>
#### Feature Updates

##### Introduced VPC as the Default Network Model

* You can use multiple subnets.
* You can create ports per subnet and connect them to instances.
* You can add routing policies.
* Added the peering feature for communication between VPCs.
* You can add or remove multiple VPC ports from an instance.
* For more information, see the VPC Overview and the user guide.

<a id="november-23-2017"></a>
### November 23, 2017 { #november-23-2017 }

<a id="november-23-2017-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed an issue where the connection limit value for a listener was displayed incorrectly when creating a load balancer.

<a id="october-26-2017"></a>
### October 26, 2017 { #october-26-2017 }

<a id="october-26-2017-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed an issue where certificates were not registered when creating a load balancer.

<a id="september-21-2017"></a>
### September 21, 2017 { #september-21-2017 }

<a id="september-21-2017-added-features"></a>
#### Added Features

##### Public API

* Following Object Storage, you can now manage the Compute & Network service via API.
* Currently, only limited features are available, and features will be expanded through additional API updates.

<a id="september-21-2017-bug-fixes"></a>
#### Bug Fixes

* Fixed an issue where users without Admin permissions in a project could modify security groups.
* Fixed an issue where the Network menu was visible to users without Admin permissions in a project.

<a id="august-24-2017"></a>
### August 24, 2017 { #august-24-2017 }

<a id="august-24-2017-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed an issue where the session persistence setting for the load balancer service was not displayed correctly.

<a id="april-20-2017"></a>
### April 20, 2017 { #april-20-2017 }

<a id="april-20-2017-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed an issue where the certificate registration window intermittently disappeared when uploading a certificate file to a listener.

<a id="march-23-2017"></a>
### March 23, 2017 { #march-23-2017 }

<a id="march-23-2017-bug-fixes"></a>
#### Bug Fixes
##### Floating IP
* Fixed an issue where the "Create" button was not displayed in the floating IP association popup.

<a id="february-23-2017"></a>
### February 23, 2017 { #february-23-2017 }

<a id="february-23-2017-feature-updates"></a>
#### Feature Updates

##### Load Balancer

* Changed to notify users that a listener cannot be deleted when there is only one listener registered to the load balancer.
	  * Previously, the deletion was already blocked, but users were not notified, which caused confusion.
	  * Users are now explicitly notified with a message that the listener cannot be deleted.

##### Floating IP

* Changed to prevent deleting a floating IP when an instance or load balancer is associated with it.
	  * Previously, a floating IP associated with an instance or load balancer could be deleted, which could cause a service failure.
	  * To prevent such mistakes, a floating IP that is associated with a resource can no longer be deleted.
* Renamed: 'Port' → 'Network Interface'
	  * The name of the target used when associating a floating IP with an instance has been changed from "Port" to "Network Interface."

<a id="january-19-2017"></a>
### January 19, 2017 { #january-19-2017 }

<a id="january-19-2017-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed an issue where the connection limit setting was not applied when creating a load balancer.

<a id="december-22-2016"></a>
### December 22, 2016 { #december-22-2016 }

<a id="december-22-2016-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed an issue where a listener could not be modified when the health check protocol was TCP.

##### Floating IP
* Fixed an issue where the name of the load balancer associated with a floating IP was not displayed.

##### Security Group
* Fixed an issue where the security group list disappeared when a duplicate rule was added.

<a id="december-8-2016"></a>
### December 8, 2016 { #december-8-2016 }

<a id="december-8-2016-bug-fixes"></a>
#### Bug Fixes

##### Load Balancer
* Fixed an issue where the health check URL of a load balancer was not displayed.
* Fixed an issue where "/" was displayed instead of the previously registered health check URL when clicking the Edit Listener button.

<a id="november-29-2016"></a>
### November 29, 2016 { #november-29-2016 }

<a id="november-29-2016-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed an issue where creating a TERMINATED_HTTPS type load balancer failed.

<a id="november-24-2016"></a>
### November 24, 2016 { #november-24-2016 }

<a id="november-24-2016-feature-updates"></a>
#### Feature Updates
##### Load Balancer
* Updated to display the session limit value per listener of a load balancer.

<a id="november-24-2016-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed an issue where creating a load balancer failed in certain projects.

<a id="august-4-2016"></a>
### August 4, 2016 { #august-4-2016 }

<a id="august-4-2016-feature-updates"></a>
#### Feature Updates
##### Load Balancer
* Added SSL offloading support for load balancers.

<a id="august-4-2016-bug-fixes"></a>
#### Bug Fixes
##### Load Balancer
* Fixed an issue where removing a load balancer intermittently failed to terminate properly.
