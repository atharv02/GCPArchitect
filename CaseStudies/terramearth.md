# **Terram Earth**

---

## **Overview**

Manufactures heavy equipment with 500 dealers and service centres in ***100 countries***. 

---

## **Solution Concept**

 - 2 Million vehicles in operation, 20% growth
 - Vehicles collect ***telemetry data from sensors***
 - ***Subset*** of critical data transmitted ***in real time*** to facilitate fleet management
 - ***Rest*** is collected, ***compresssed and uploaded daily***. 
 - Each vehicle usually ***generates 200 to 500 MB of data*** every day. *Hint: Daily data in petabytes*

---

## **Existing Technical environment**

 - Vehicle data aggregation and analysis infra in GCP. Serves clients ***across the world***
 - Data from two main plants sent to ***private DCs that contains legacy inventory and logistics management systems***
 - Private DCs have ***multiple interconnects*** to GCP
 - Web frontend running in GCP allows access to stock management and analytics

---

## **Business Requirement**

 - Predict/ Detect vehicle malfunction, ship parts to dealership for JIT repair
 - Decrease ***cloud operational costs and adapt to seasonality***. *Hint: Autoscaling*
 - Allow remote developers, keeping security. *Hint: Cloud IAP/ code validation in pipeline*
 - Flexible/Scalable platform for developers to create custom API services

---

## **Technical Requirement**

 - Create abstraction layer for ***HTTP API access to legacy system***. *Hint: Cloud LB*
 - Modernize ***CI/CD pipelines*** to deploy ***container workloads***
 - Developers to run experiments without compromising security and governance
 - Self-service portal to create new projects, request resources for ***data analytics jobs*** and centrally manage access to API endpoints
 - Cloud native solutions for ***keys and secrets management***. *Hint: Cloud KMS with Secret manager*
 - Improve/ Standardize tools for ***application and network monitoring***


---

## **Executive Statement**

5 Year Plan to include
 - Partner eco-system by eanbling access to data
 - Increasing autonomous operation capabilities
 - Move remaining legacy systems to the cloud