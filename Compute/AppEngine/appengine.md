# App Engine

This section refers to both the App Engine Standard and Flexible Environment.

App Engine is highly managed compute option from GCP that *let's the developers focus on code*

---

## Important Concepts

 - Only one App Engine environment per project/region
 - Multiple services deployed within the same environment
 - New code deployed as ***versions***
 - Supports ***traffic splitting*** e.g 90% to ver 2 and 10% to ver 1
 - Easy to rollback by setting 100% traffic to previous version


---

## App Engine Standard vs Flexible environment

### Table

| Concept  | Standard | Flexible |
| ----------- | ----------- | ----------- |
| Source Code | Specific versions of limited languages | Provides flexibility by custom containers
| Scaling | Basic/Manual/Automatic | Manual/Automatic
| Network | Executes in serverless environment | Executes inside VPC
| Minimum Scaling | ***Scales to zero*** | ***Min 1 instance***


***Note:*** App Engine Standard is best for traffic with large spikes, Scaling to zero during no demand periods

App Engine Standard environment can be configured in a app.yaml file within the local project.

### Important Commands

``` bash
gcloud app deploy # Deploys the app in the current folder

gcloud app browse # Retrieve the app engine ID

gcloud app services set-traffic s1 --splits=v2=.5,v1=.5 # Splits 50% traffic between the two versions 


```