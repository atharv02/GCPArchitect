# **Mountkirk Games**

---

## **Overview**

Makes online, session-based, multiplayer games for mobile platforms. Recent endeavor to create games that allows ***hundreds of players in a geo-specific arena***. A ***real-time*** digital banner will display a ***global leaderboard*** of top players across all arenas

---

## **Solution Concept**
 - New multiplayer game on ***GKE*** to scale rapidly 
 - Google ***Global Loadbalancer*** to route players to ***closest regional game arena***
 - ***Multi-Region CloudSpanner*** to keep global leaderboard in sync

---

## **Existing Technical Environment**
 - Existing env recently migrated. 5 Games moved using ***lift and shift VM migrations***
 - Each new game in isolate Project nested below a folder on which permissions are set
 - Legacy games consolidated into one project, separate envs for development and testing

---

## **Business Requirement**

 - Support multiple gaming platforms. *Dont think too relevant*
 - Support multiple regions
 - Support rapid iteration of game features. *Hint: CICD using Jenkins/CloudBuild*
 - Minimize latency *Hint: Route to nearest region*
 - Optimize for dynamic scaling. *Hint: GKE horizontal pod autoscaler, node autoscaler*
 - Use managed services and pooled resources.
 - Minimize costs

## **Technical Requirements**

 - Dynamically scale based on game activity
 - Publish scoring data on a ***near real-time global leaderboard***
 - Store ***game activity logs in structured files*** for future analysis. *Hint: GCS with nearline/coldline*
 - Use GPU processing to render graphics. *Hint: GKE GPU Node pools with standard pools*
 - Support eventual migration of legacy games to new platform. 

## **Executive Statement**

 - Start building games ***using cloud-native design principles***
 - ***Latency*** is top priority, ***cost management*** second priority
 - Advanced ***analytics*** capabilities
 - Rapidly iterate on deployments of bug fixes and new functionality. *Hint: CI/CD*
