# Networking

## VPC 

---

## Shared VPC

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