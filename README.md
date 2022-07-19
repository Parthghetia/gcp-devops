# GCP Intro
## CloudLauncher
- Marketplace for GCP

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

## Google Cloud APIs and Services
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
- Servelesss, highly scalable and cost-effective big data warehouse designed for business agility
- In the Console, go to Big Data then head on Big Query
![image](https://user-images.githubusercontent.com/43883264/178120169-b78de822-5fb2-4015-b93c-893d4ebdd74a.png)

- This console is used to basically query big data-sets. In this example, we are going to query a public data sets to query a Public DataSet that stores names in the US.
- This the query used in the Demo
```sql
SELECT
  name, gender,
  SUM(number) AS total
FROM
  `bigquery-public-data.usa_names.usa_1910_2013`
GROUP BY
  name, gender
ORDER BY
  total DESC
LIMIT
  10
```
![image](https://user-images.githubusercontent.com/43883264/178120211-10b0e019-01bb-4c12-b23e-b41a57c6f8b2.png)

## Google Dataflow
- Is a fully managed service for executing Apache Beam Pipelines within the Google Cloud Platform
- What is Apache Beam? This is an open source, unified model and set of language-specific SDKs for defining and executing data processing workflows, and also data ingestion
![image](https://user-images.githubusercontent.com/43883264/178120399-a0eda439-cce7-4c3c-b15b-61c3a498a6ec.png)
- Here is an example data pipeline
![image](https://user-images.githubusercontent.com/43883264/178120425-61f0fb7f-db9f-462d-a38b-f4b9747e8fb1.png)
- And an how data flow looks like

## Google Cloud Pub/Sub
- This is a fully managed real-time messaging service that allows you to send and receive messages between independent applications
![image](https://user-images.githubusercontent.com/43883264/178120556-f0dcc3b9-b20d-48ce-b718-88d5408bd2c6.png)

- You have 3 components to a cloud pub/sub
- More about pub/sub https://cloud.google.com/pubsub/docs/overview
1. Topic 
2. Subscription
3. The message itself

- Pub/sub integrates with Google DataFlow and BigQuery to create a streaming pipeline. 

Pub/Sub Creating a topic
![image](https://user-images.githubusercontent.com/43883264/178120668-54d8b4dd-bd29-4f5b-84f4-62580cbb5791.png)
- Once a topic is created we can create a subscription as below
![image](https://user-images.githubusercontent.com/43883264/178120716-2f9ad627-3bcc-4386-8ab0-49f028b16fce.png)
![image](https://user-images.githubusercontent.com/43883264/178120757-e2c4b36b-7fa3-4283-8e81-dbf70b5f873e.png)
![image](https://user-images.githubusercontent.com/43883264/178120767-1fbd38ab-94f3-48f9-b12e-bcb30909fc18.png)

- Once a topic and sub is created, let's try publishing a message 
- Go to your topic and hit publish message...
![image](https://user-images.githubusercontent.com/43883264/178120787-a98026b3-42ec-4c77-beb5-ce7ab4748f34.png)

- Once the message is published we are going to pull the message as a subscriber
- You just go to the subscription page and hit pull and you'll see your message
![image](https://user-images.githubusercontent.com/43883264/178120851-8bba4d76-a0c6-4918-997d-78d8ecac7cf8.png)

## Google Cloud Security
- G Cloud provideds Data Storage Security by providing encryption for data at rest and data in transit as well

## GCP Monitoring
- Cloud Monitoring Handles this
![image](https://user-images.githubusercontent.com/43883264/178121099-2668be0c-e102-40ec-8e19-85fcfa7e1df4.png)
- You can also monitor AWS resources.
- Let's check it out 
![image](https://user-images.githubusercontent.com/43883264/178121124-e8702ddd-cea6-4f99-a097-6d572e145020.png)
- How to set up an uptime check

![image](https://user-images.githubusercontent.com/43883264/178121149-31b69da0-ed63-490e-99ce-ff8628407aa1.png)

## Machine Learning and AI on GCP
- What is machine learning -> Basically a system that tries to learn patterns and behaviours from daily usage
- What is AI? This is where we use the data learnt earlier to try and predict patterns and workflows

Google Cloud has an open source tool known for this called TensorFlow
- Here is a look at Machine Learning an AI pipeline with GCP
![image](https://user-images.githubusercontent.com/43883264/178121256-d0ed0f3c-8f89-44f8-a236-f75bb3e10848.png)


## Cost Control on GCP
### Billing Resource Org Basics
- Let's once again take a look at the GCP Hierarchy

![image](https://user-images.githubusercontent.com/43883264/178121478-b531870a-7046-4679-8fc9-c92451bb8cb3.png)
- Why does this matter from a billing account perspective
![image](https://user-images.githubusercontent.com/43883264/178121592-3d01f2ff-c6db-41fd-926f-a33f5ef99235.png)
- Sample Billing Account for an org
![image](https://user-images.githubusercontent.com/43883264/178121611-3d455351-e141-409f-abdf-d96f6882e40c.png)
NOTE: You cannot associate multiple billing accounts to one project

### Controlling Billing Access with IAM Roles
![image](https://user-images.githubusercontent.com/43883264/178122298-ed3d6b75-323e-4a7c-a15f-cfc91d240982.png)
 
 ### IAM Access Scopes
 ![image](https://user-images.githubusercontent.com/43883264/178122510-b0365811-ddf2-4ddf-874d-5884c426a5b0.png)
 
## Hands On Billing Accounts and IAM
- Here is a user in a GCP Org that shows him as a billing account admin
![image](https://user-images.githubusercontent.com/43883264/178161248-d4edcf2a-d733-450d-8d62-17bcabf62f86.png)
- We then go to the account management page in the bottom
![image](https://user-images.githubusercontent.com/43883264/178161284-f9f93f40-3187-44b1-90a0-61f3328424e4.png)
- Here on the right you can see the membership in this billing account
![image](https://user-images.githubusercontent.com/43883264/178161327-e3a19677-4695-45b3-bef2-23b15ed697cd.png)

- Now let's go ahead and add a new user to our organization. We are going to assign some IAM permissions to this user as Billing User in this organization. Let's see how to do that:
![image](https://user-images.githubusercontent.com/43883264/178161402-5f7efb1a-2236-4493-86f8-48c922cd306a.png)

- If we now go back to the billing account management page, you'll now see the new user in there
![image](https://user-images.githubusercontent.com/43883264/178161413-4ef5487d-e951-4b31-8efd-c98abe5ed969.png)
- Something new we are going to try here is. Let's try and assign our new user to be a Billing Account Admin but from them Billing Account Management page and not IAM
- What happens here is. This user Bob, will be a Billing Account User throughout the organization but he will be let's say a Billing Account Administrator in this Billing Account only
![image](https://user-images.githubusercontent.com/43883264/178161516-1d26a124-5bf9-4046-9f2b-85485d64e18c.png)

## Billing Reports
- This report what are we actually spending
![image](https://user-images.githubusercontent.com/43883264/178162041-6bf02073-094d-48e7-9368-499b0dbe1d5f.png)
- You can use legit filters to actually determine what is the cost of the usage and what actually caused a spike let's say at the end of the month and drill deeper

## Exporting Billing Data to Big Query
- Why Big Query
![image](https://user-images.githubusercontent.com/43883264/178162379-2f70d5c8-e104-459c-8203-d645f3aa328b.png)
- How to export Billing Data in BigQuery
![image](https://user-images.githubusercontent.com/43883264/178162409-64c70453-b535-4736-a26d-ef1f5e5059f5.png)

### Hands On - How to Export Data to Big Query
![image](https://user-images.githubusercontent.com/43883264/178162430-aabc731f-df82-42fc-9bce-1e26f990940c.png)
- The above console is where you would actually export Big Query data to but before that we gotta create a Dataset. So let's see how to do that:

- In Big Query, select your project in the Big Query Menu and then click create Dataset as below:
![image](https://user-images.githubusercontent.com/43883264/178162485-f42736ea-32ad-4ea3-8923-29422fa93d59.png)
![image](https://user-images.githubusercontent.com/43883264/178162494-e3de5676-076e-496b-b825-2f8469a7f230.png)

- We will then go back to the billing dashboard as below and that's it!
![image](https://user-images.githubusercontent.com/43883264/178162554-af5ebc33-af86-45a3-b051-346a36d86716.png)
NOTE: Only newer data will be sent to Big Query but older data will not be sent
- Here is some sample billing data that was sent to Big Query
![image](https://user-images.githubusercontent.com/43883264/178162598-5f0453e7-e096-4809-86ac-f758da1977e3.png)

## Billing Alerts with Budgets
- How Budgets and alerts work:
 ![image](https://user-images.githubusercontent.com/43883264/178163818-57af0c7e-1219-43a0-8e2b-b136ecd63e70.png)

## Hands On - Setting up Budgets and Alerts
![image](https://user-images.githubusercontent.com/43883264/178163921-42109657-d4f7-4a1e-a8b7-9537121ba9e2.png)
![image](https://user-images.githubusercontent.com/43883264/178163928-4f84e047-16e0-4f44-bce2-64e173b0e9d3.png)
![image](https://user-images.githubusercontent.com/43883264/178163960-a3c385c3-3673-4607-8d6b-ca0e29a2b196.png)

## Cost Reduction Tools - GCP
![image](https://user-images.githubusercontent.com/43883264/178390066-26b2fbdb-86f6-405f-9339-4a57d4bb10ec.png)

#### RightSizing VMs
![image](https://user-images.githubusercontent.com/43883264/178390390-c1037368-a816-4ad9-a4cd-309160ef1293.png)

#### Sustained Use Discounts
![image](https://user-images.githubusercontent.com/43883264/178390552-beff2ad9-d285-466c-87c8-557bc37d790c.png)
![image](https://user-images.githubusercontent.com/43883264/178390677-7bfbe2d7-07e5-4c9e-b4f7-19d833de93d2.png)
For more info:
https://cloud.google.com/compute/docs/sustained-use-discounts
#### Committed Use Discounts
![image](https://user-images.githubusercontent.com/43883264/178390879-a826d248-f9ac-4211-bb58-aa249ddc6b87.png)

#### Preemptible VMs
![image](https://user-images.githubusercontent.com/43883264/178391018-cf08ff0d-ce19-42f8-8dc6-cb776e41fa72.png)

#### Cloud Storage Classes
![image](https://user-images.githubusercontent.com/43883264/178391203-cd8df793-a9ef-4ec7-a735-7f404a027e94.png)

#### Cloud Storage Lifecycle Policies
![image](https://user-images.githubusercontent.com/43883264/178391389-32b78ea6-2f3b-4aa6-bd4d-8b71addb79be.png)

#### Free Tier Resources
![image](https://user-images.githubusercontent.com/43883264/178391539-f366b3ea-6545-4384-9791-2a3c8fd79e26.png)



