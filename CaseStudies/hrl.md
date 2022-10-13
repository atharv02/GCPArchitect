# **Helicopter Racing League**

---

## **Overview**

Competitive helicopter racing sports league. HRL offers a paid service to steam the races ***all over the world*** with live ***telemetry*** and ***predictions***

---

## **Solution Concept**

 - Migrate existing service to expand use of managed AI and ML services
 - Move serving of content ***realtime and recorded*** closer to users in emerging regions
  

---

## **Existing Technical Environment**
 - Core of mission critical apps run on current cloud provider
 - Video recording and editing perform at race track. ***Encoding and transcoding*** in the cloud on ***VMs created for each job***
 - Connectivity and local compute provided by truck mounted mobile DCs
 - Content stored in ***Object Storage Service***
 - Race predictions using ***Tensorflow on VMs***

---

## **Business Requirements**
 - Expose predictive models to partners. *Hint: through secured API*
 - Increase predictive capabilities before and during races. *Race results, mechanical failures and crowd sentiment*
 - Telemetry and additional insights *Hint: Data Ingestion pub/sub and dataflow/BigQuery with DataStudio*
 - Measure fan engagement with new predictions
 - Enhance global availability, quality and concurrent viewers *Hint: Multi-regional capability/ Global LB, CDN*
 - Minimize operational complexity and compliance with regulations
 - Create merchandisiing revenue stream. *Hint: New hosting option*

---

## **Technical Requirements**
 - Increase prediction throughput and accuracy. *Hint: Better ingestion/ data processing*
 - Reduce viewer latency *Hint: Multi-regional services with cloud CDN*
 - Increase transcoding performance. *Hint: Managed Instance Groups/ Autoscaling. Use transcoder API*
 - Data mart to enable processing of large volumes of race data. *Hint: BigQuery*

---

## **Executive Statement**

 - Bring racing to fans ***all over the world***
 - Enhanced video streams that include prediction of events. *Hint: Realtime ML*
 - Current platform lacks realtime-predictions during races and capacity to process season long results