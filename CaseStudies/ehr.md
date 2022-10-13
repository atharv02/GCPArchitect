# **EHR Healthcare Case Study**

---

## **Overview**

EHR Healthcare is a leading provider of electronic health record software to the ***medical*** industry. It provides software as a service to ***multi-national*** medical offices, hospitals and insurance providers

---

## **Solution Concept**

 - Scale Environment
 - Adopt DR Plan
 - Add CI/CD Capabilities
 - GCP to replace co-location facilities

---

## **Current Landscape**
 - Many *containerized* workloads on *Kubernetes Clusters*
 - Data resides in *MySQL, MS-SQL, Redis and Mongo DB*
 - Legacy file & API based integrations on-prem. No plan to migrate currently
 - Users managed via *Microsoft Active Directory*
 - Monitoring via various opensource tools. Alerts via email often ignored

---

## **Business Requirements**

  - Onboard new customers as quickly as possible
  - Provide a minimum 99.9% Availability for customer facing systems
  - Centralized visibility and proactive action on system performance and usage. *Hint: Integrate GCP monitoring*
  - Increase ability to provide insights into healthcare trends
  - Reduce latency *Hint: Multi-region deployments/ Integrate CDN*
  - Maintain regulatory compliance. *Hint: Verify services for HIPAA/ BA agreement for HIPAA*
  - Decrease infrastructure administration costs. 
  - Make predictions and generate reports on industry trends on provider data

---

## **Technical Requirements**
 - Maintain legarcy interfaces with connectivity to on-prem and cloud providers. *Hint: Dedicated Interconnect*
 - Consistent way to maange customer-facing applications that are container based. *Hint: GKE or integrated CloudRun*
 - Secure and high-performance connection between on-prem and GCP
 - Provide consistent logging, log retention, monitoring and alerting capabilities *Hint: Cloud operations. Consider sinks for retention*
 - Maintain and manae multiple container-based environments. *Hint: GKE/ Anthos*
 - Dynamically scale and provision new environments. 
 - Create interfaces to ingest and process data from new providers. *Hint Pub/Sub with Dataflow*

---

## **Executive Statement**

 - On-prem strategy required major investment of time and money
 - Team trained on different systems managing similar but separate environments *Hint: Considering unifying to a single tech stack*
 - Outages caused by 
   - Misconfigured systems
   - Inadequate capacity to manage spikes in traffic. *Scaling issues*
   - Inconsistent monitoring practices