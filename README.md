# Notes
## Introduction to Compute Engine
![image](https://user-images.githubusercontent.com/43883264/177053904-d234b12b-c489-421e-b047-9550fa57f537.png)

##### GCP Machine Types
![image](https://user-images.githubusercontent.com/43883264/177123458-79c626d8-5097-4a99-b32b-4c20b58e6303.png)

## VPC
- Simple VPC example
![image](https://user-images.githubusercontent.com/43883264/177054109-e89f6ff6-037b-46d1-9f63-a2c44702f3fe.png)

- A sample VPC Design
![image](https://user-images.githubusercontent.com/43883264/177119764-649a84b2-8c6c-4c30-bbff-a24c807ebeeb.png)
- Let's see how to create a VPC Network
**NOTE: The Private Google Access button - this can help set whether VMs in this subnet can access Google Services without assigning external IP addresses or not**

![image](https://user-images.githubusercontent.com/43883264/177120408-151a4e90-34f3-48b6-ab79-0af1f98e98c5.png)
(No DNS Server policy was selected for this example)
![image](https://user-images.githubusercontent.com/43883264/177120541-98f269c9-f40b-4624-b31f-5ea0f30f0444.png)

## Databases on GCP
- Why do we separate out databases?
![image](https://user-images.githubusercontent.com/43883264/177054270-e62643db-3dcc-45aa-9faf-44ea87111823.png)

## What are managed services on GCP
- This is stuff that Google deals with e.g CPU, RAM, Storage upgrades or whatever
- Example of one managed service offered by Google:
![image](https://user-images.githubusercontent.com/43883264/177056580-137d941d-3f63-4a85-bce3-18c11f1abc51.png)

## GCP Global Physical Infra
- So different regions have a number of zones as below:
![image](https://user-images.githubusercontent.com/43883264/177056790-92f5f9ec-f15b-41b5-ba16-3373e132160b.png)
- How are zones and regions different and relate to "The Cloud Advantage"
![image](https://user-images.githubusercontent.com/43883264/177056820-e0eff95b-239b-4d5a-99a2-4c5bbca06dce.png)

## What's different on Google Cloud
![image](https://user-images.githubusercontent.com/43883264/177057201-d76c6cc9-8655-49cd-bebc-eba37eebd8d4.png)

## Google Cloud APIs
- These are the already enabled APIs and Services
![image](https://user-images.githubusercontent.com/43883264/177057339-e0b62c1a-b0e2-40c5-8313-b02559c0f094.png)
- Let's head over to the library and see what we have there:

![image](https://user-images.githubusercontent.com/43883264/177057364-5888fd0d-60a6-4a0e-a5bb-c6afa869289e.png)

- Let's try enabling an API - Cloud SQL (in this case)
![image](https://user-images.githubusercontent.com/43883264/177057383-87cd5678-b76a-4c41-86d4-c164481a0265.png)
![image](https://user-images.githubusercontent.com/43883264/177057390-54e8402f-3804-41ad-a66c-d37663b5cb31.png)

## IAM (Identity and Access Management)
- Basically creating users and roles and giving a user custom access in order to practise the least privilege approach

## Google Cloud Organizations
![image](https://user-images.githubusercontent.com/43883264/177118603-e67de263-e861-4f6c-8ccf-9e228fd046c6.png)

## Google Cloud Projects
![image](https://user-images.githubusercontent.com/43883264/177118835-e7a9770f-68a9-49ef-80ce-c968b7319620.png)
- Here's how to create a project within an Org
![image](https://user-images.githubusercontent.com/43883264/177119104-18ebf870-f858-441a-8f73-235a978c4063.png)

## Cloud Storage
- How to create a cloud storage bucket
![image](https://user-images.githubusercontent.com/43883264/177132691-54f08f76-0925-44aa-abbc-124081cf1629.png)
- You can then choose the desired storage class for your bucket
![image](https://user-images.githubusercontent.com/43883264/177133125-cd8dda2d-d9a0-4246-ab5a-a3096b9eeae0.png)
#### STORAGE CLASSES
![image](https://user-images.githubusercontent.com/43883264/177904801-9a69fd60-df2f-499b-b572-e3fa00e26462.png)

1. Standard Storage - is best for data that is frequently accessed ("hot" data) and/or stored for only brief periods of time
2. Nearline Storage -  is a low-cost, highly durable storage service for storing infrequently accessed data. Nearline storage is a better choice than Standard storage in scenarios where slightly lower availability, a 30-day minimum storage duration
- You then can choose how to control access over the objects stored in the bucket and costs for data access are acceptable trade-offs for lowered at-rest storage costs
3. Coldline Storage -  Coldline storage is a better choice than Standard storage or Nearline storage in scenarios where slightly lower availability, a 90-day minimum storage duration, and higher costs for data access are acceptable trade-offs for lowered at-rest storage costs.
4. Archive Storage -  is the lowest-cost, highly durable storage service for data archiving, online backup, and disaster recovery
 
![image](https://user-images.githubusercontent.com/43883264/177133330-a3fc3912-ee28-42c0-b1ab-ea5abc6f0467.png)
-> Fine grained means - you can actually create ACLs to allow access to users who only created their own objects. Uniform is self expl
- You can then choose how you want to encrypt your objects
![image](https://user-images.githubusercontent.com/43883264/177133569-e2ea2d54-98a7-4ef5-a5d6-29014123262d.png)

- Now let's see once a bucket is created how we can edit the permissions on the bucket
![image](https://user-images.githubusercontent.com/43883264/177133862-80452380-0ce9-48bc-847d-ba18eb79c5db.png)
![image](https://user-images.githubusercontent.com/43883264/177133903-bd206428-db63-457f-84fa-1cdc5d8e087d.png)
![image](https://user-images.githubusercontent.com/43883264/177133994-b94c78e3-5f4d-493b-a577-b8a2427a3c45.png)
- The last two steps allow for public access to viewing the bucket contents

## Database Service in GCP
- We have two types of DBs
1. Relational - structured data
2. Non-Relational - non-structured data - uses a storage model that is specific to the data being stored

### What GCP offers
#### Relational DBs
1. Cloud SQL - SQL database for mysql,sql and postgres engines
2. Cloud Spanner - globally distributed DB service with unlimited scaling
![image](https://user-images.githubusercontent.com/43883264/178050332-18bc86ad-42af-461c-9782-204583cea51b.png)


#### Non Relational DBs
1. Big Table - for large analytical and operational workloads
2. Firestore - fully managed document DB for developing application
3. Memory Store - highly available in memory service for redic and memcache
![image](https://user-images.githubusercontent.com/43883264/178050382-d0746efd-6204-4a5c-a962-7d9863497cd6.png)

### Databases - Hands On
![image](https://user-images.githubusercontent.com/43883264/178050870-e57d2a34-ca94-479b-b202-416ee4dc7d58.png)
![image](https://user-images.githubusercontent.com/43883264/178050897-590f18c5-63ee-4451-9adc-fb7992a974ca.png)
![image](https://user-images.githubusercontent.com/43883264/178051091-119899fd-6f0d-4239-9b2a-ba9b48656549.png)
![image](https://user-images.githubusercontent.com/43883264/178051236-75833906-e575-483e-94d3-614c78ca8c0f.png)
![image](https://user-images.githubusercontent.com/43883264/178051291-463bb44e-ec50-4ba5-a5df-76aebf50eb9e.png)
![image](https://user-images.githubusercontent.com/43883264/178051657-a9a9149c-50cd-423c-8614-11d66935b8d6.png)
![image](https://user-images.githubusercontent.com/43883264/178051787-11cbfe28-cd99-4083-ab73-b05b2425eacd.png)
Success!
![image](https://user-images.githubusercontent.com/43883264/178051897-b3ef9585-7c92-4d4d-b191-a2fc19ae9efc.png)

## Big Data and Messaging
### Big Query
