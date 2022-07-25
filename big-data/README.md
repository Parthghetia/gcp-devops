# BigData

# Big Query

- BigQuery is a fully-managed, serverless data warehouse that enables scalable analysis over petabytes of data. 

- It is a Platform as a Service that supports querying using ANSI SQL. It also has built-in machine learning capabilities.

![image](https://user-images.githubusercontent.com/43883264/180685874-989fd11b-852f-41db-a870-27a97bd9afb2.png)

- Some initial Hands On can be found here:

https://github.com/Parthghetia/gcp-devops/blob/main/README.md#big-query

- Some more public queries can be found here:

![image](https://user-images.githubusercontent.com/43883264/180687427-7e3d71df-a962-4e75-afe2-6155414e67ea.png)

# Cloud DataFlow - Data Processing

- Here is what Cloud Dataflow can do
- Some more info here:

https://github.com/Parthghetia/gcp-devops/blob/main/README.md#google-dataflow

![image](https://user-images.githubusercontent.com/43883264/180688691-fbc9bbd3-64c2-46a4-b325-665ea4cedd4a.png)

![image](https://user-images.githubusercontent.com/43883264/180691048-b9f756f6-1216-4f87-8cc5-82148db0c072.png)

## Dataflow Console - Sample Jobs/Pipelines

![image](https://user-images.githubusercontent.com/43883264/180691190-9443fd9d-9421-4a7e-b98f-645d38d76df6.png)

![image](https://user-images.githubusercontent.com/43883264/180691396-21e716ad-ba9c-4275-8c2b-be777b532dbc.png)

- Let's see how we can create a job from templates

![image](https://user-images.githubusercontent.com/43883264/180691748-39723aab-6130-4fa8-969d-982457997547.png)

# Cloud DataProc - Data Processing
![image](https://user-images.githubusercontent.com/43883264/180692159-086dcef3-2afd-4c74-96ea-99a90761dbb6.png)

- When a decision needs to be made on which Data Processing platform to be used Dataflow vs Dataproc

![image](https://user-images.githubusercontent.com/43883264/180692424-895f6c85-516d-46e1-bbf2-2d2d253fb4a9.png)

## Cloud DataProc - On the console
![image](https://user-images.githubusercontent.com/43883264/180692547-acc2a83e-c22b-4949-80d3-6bb198768525.png)
![image](https://user-images.githubusercontent.com/43883264/180692564-0990bd57-f90b-482e-b199-5719375c6403.png)
![image](https://user-images.githubusercontent.com/43883264/180692613-342c660c-d28a-4972-847d-8532973c70d8.png)
![image](https://user-images.githubusercontent.com/43883264/180692627-bdcd6583-6f05-45cf-9ed8-e2c4dd2a9696.png)

- Let's see how to create a cluster

![image](https://user-images.githubusercontent.com/43883264/180692681-fd2892f7-2246-49bf-b6ff-8373bccf9bb0.png)

- Advanced options:

![image](https://user-images.githubusercontent.com/43883264/180692863-88817f05-ea46-4b01-ae10-9490079fe025.png)

- Here's how to submit a job

![image](https://user-images.githubusercontent.com/43883264/180693011-eb79f008-69bb-4806-9dd9-34032da8193c.png)


# Pub/Sub - Messaging
- Pub/Sub works as a messaging middleware for traditional service integration or a simple communication medium for modern microservices


![image](https://user-images.githubusercontent.com/43883264/180693197-9c92b327-2c4b-4e55-b573-2c4f80e8dd32.png)

![image](https://user-images.githubusercontent.com/43883264/180693323-b612611c-3368-4036-be38-93d15d7a2285.png)

- How it works

![image](https://user-images.githubusercontent.com/43883264/180693410-46f326d2-6ee3-47d1-8988-89bdb833185b.png)

- With pub/sub we start by creating a topic then a subscription. Some details here: https://github.com/Parthghetia/gcp-devops/blob/main/README.md#google-cloud-pubsub and more to follow

- Remember, you can create a topic and a subscription but you need a subscriber in order to pull the information. Also you can easily pull messages from a topic using the following gcloud command

`gcloud pubsub subscriptions pull <name of sub>`

## Handling Streaming Messages with Cloud Pub/Sub - Hands On

![image](https://user-images.githubusercontent.com/43883264/180694481-c89982c2-c34c-4aa9-9b8f-9386c5a8f5e6.png)

![image](https://user-images.githubusercontent.com/43883264/180694466-ea891e82-05f3-48f4-969c-09cde55444a2.png)

![image](https://user-images.githubusercontent.com/43883264/180694367-3370f56a-84d6-40b3-9a48-0bb2a41570e4.png)


## More Big Data Services
### Cloud DataLab

![image](https://user-images.githubusercontent.com/43883264/180693927-a445ccdc-4e9b-4f67-bccc-b5880762a8f6.png)

## Cloud Data Studio
![image](https://user-images.githubusercontent.com/43883264/180693958-0e2b204c-f1e7-4301-9fba-478a7173d868.png)

More about Cloud DataLab and Cloud Studio Here: https://learn.acloud.guru/course/b60292df-bf88-44f0-95e7-d8695494c4cb/learn/49f8be6b-c769-4cee-ac00-9bfe62ba4270/fcf3ed7d-43b3-4cd4-9517-2265c53dc388/watch





