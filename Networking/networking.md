# Networking

## VPC 
 GCP VPC is a scalable private network within the Google Cloud

Key Features: 
 - VPC is a global resource, while subnets are regional
 - Creation in two modes
   - Auto Mode creates VPC with subnets in all regions in the predefined 10.x range
   - Custom Mode VPC lets users pick subnet ranges and regions. ***Hint: Use custom mode to prevent overlapping IP address***
 - Cloud NAT can be configured to provide external outbound connectivity from instances with no public IP
 - Firewall rules can be configured and applied based on ***service accounts and network tags***
 - Flowlogs can be manually enabled (disabled by default) to capture traffic
 - VPCs can be peered to each other to provide internal connectivity between VPCs with ***no overlapping subnets***
   - ***Note: VPC peering is non-transitive. A <-> B <-> C , cannot provide connectivity from A to C***
 - Cloud VPN with Cloud Router can be used to provide connectivity between two VPCs with some overlapping subnets
---

## Shared VPC

Shared VPC can be configured to allow resources from multiple projects to connect using a common VPC network


***GCP best practice to create a shared VPC in a host project, to centrally manage all network resources***

 - Project in which the VPC is created is called *host project*
 - Projects where the VPC/subnets are shared is called the *service project*

---

## Hybrid Connectivity

Two important types to establish connectivity - Cloud Interconnect and VPN

### Cloud Interconnect

Best practice to deploy redundantly for high availability

**Offered in two flavours**
 - Dedicated Interconnect: Use cases
    - 10/100 G connections over private network
    - ***Hint: Useful for replicating databases/ DR scenarios***
 - Partner Interconnect: Use cases
    - ***Dedicated facilities are unavailable***
    - Entire 10Gb connectivity not required

### Cloud VPN

 - Classic VPN partially deprecated. Best practice to use HA VPN. 
 - HA VPN provides redundant connectivity to one region. 
 - ***3Gbps connectivity per VPN tunnel***, use interconnect for high-bandwidth requirements

---

## Additional
 - Private Google Access
    - provides connectivity from VPC to GCP services over private network
    - can be used in conjunction with VPN/Interconnect to provide GCP service access to on-prem systems

 - VPC service perimeter
    - Can be configured to ***mitigate the risk of data exfiltration***
    - Service perimiters can be configured at Organization, folder or project level. 
 - Serverless VPC access
    - Can be used to provide serverless applications (cloudrun/App engine) access to resources inside a VPC