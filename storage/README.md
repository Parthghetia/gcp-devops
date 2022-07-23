## Managing Storage and Databases
![image](https://user-images.githubusercontent.com/43883264/180623070-c016f183-15e5-4fca-96c4-4a8f9dde2c9c.png)

- Here is a set of storage classes defined for a bunch of projects plus the storage configured for all these options


![image](https://user-images.githubusercontent.com/43883264/180623167-cfea3c40-4e7b-4fca-9e1d-b3710607103a.png)

- A question that arises from this is the lifecycle rules for a bucket. This is what they mean

![image](https://user-images.githubusercontent.com/43883264/180623180-669bd675-f608-47fc-b599-de8096729a2c.png)

- While creating a bucket there are some things to consider here:

![image](https://user-images.githubusercontent.com/43883264/180623230-91ee7bee-2bff-46ce-9e0a-e3df7c0e56fa.png)

 ### NO-SQL Databases vs SQL Databases - Relational vs Non-Relational Databases
 NoSQL (“non SQL” or “not only SQL”) databases were developed with a focus on scaling, fast queries, allowing for frequent application changes, and making programming simpler for developers. Relational databases accessed with SQL (Structured Query Language) were developed with a focus on reducing data duplication as storage was much more costly than developer time. SQL databases tend to have rigid, complex, tabular schemas and typically require expensive vertical scaling.
 
 Here's what Google has to offer in terms of DBs
 https://github.com/Parthghetia/gcp-devops/blob/main/README.md#database-service-in-gcp
 
 ## Cloud Datastore Fundamentals - Non-Relational Data
 ![image](https://user-images.githubusercontent.com/43883264/180623552-8d24b562-421c-4548-9e57-fe3f7d314509.png)

- Let's take a look at Cloud Datastore first hand:

![image](https://user-images.githubusercontent.com/43883264/180623607-f970cdc3-c4b9-4627-b502-ecc86373b174.png)

- Here is a filled Datastore:

![image](https://user-images.githubusercontent.com/43883264/180623616-43559cba-4b7a-4154-861a-d976a51103c0.png)

- Here is what an entity looks like:

![image](https://user-images.githubusercontent.com/43883264/180623634-9b9de89b-21be-4d94-8925-124bca58b514.png)

- Here is how you can add a property to an entity:

![image](https://user-images.githubusercontent.com/43883264/180623684-08385dd6-deb6-4d78-974a-8b8c5f2335fb.png)

- And you can now see that in the entity list

![image](https://user-images.githubusercontent.com/43883264/180623693-2a087b64-d721-4343-9334-9124ec7a858d.png)

- If you wanna use the SQL based querying language you can use that through toggling the language button up there as shown below:
![image](https://user-images.githubusercontent.com/43883264/180623787-054d2144-aed6-45d1-b808-78e6c8cca893.png)


