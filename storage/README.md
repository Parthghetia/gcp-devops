# Managing Storage and Databases
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
 
 # Cloud Datastore Fundamentals - Non-Relational Data
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


# Handling Relational Data via Cloud SQL

![image](https://user-images.githubusercontent.com/43883264/180624187-e91c33b4-20e7-4113-bb70-dd217fdf3642.png)


- Here is the console at first hand

![image](https://user-images.githubusercontent.com/43883264/180624230-2a100af6-fa84-454f-b12e-2c8822eb4253.png)

- You can add HA by clicking the button right there ^

![image](https://user-images.githubusercontent.com/43883264/180624251-5012827f-fa04-43cc-8574-17db24399560.png)

- Let's go through the process of setting up a Cloud SQL instance

![image](https://user-images.githubusercontent.com/43883264/180624275-9e03f884-7812-4547-a52e-0e5e25b7546c.png)

![image](https://user-images.githubusercontent.com/43883264/180624296-5e8a1e6d-5917-4931-8d4e-59365d1942af.png)

![image](https://user-images.githubusercontent.com/43883264/180624310-9d36f230-95cf-43a2-9460-555a475d0123.png)

![image](https://user-images.githubusercontent.com/43883264/180624314-3a5955c8-6960-40de-8c96-52d6df2aa79b.png)

![image](https://user-images.githubusercontent.com/43883264/180624330-3de2f195-730b-4e99-bb9f-bb5ee6f6da54.png)

# NoSql Management with Cloud BigTable
![image](https://user-images.githubusercontent.com/43883264/180624404-b0a67889-0fc4-4063-a123-6ab1389d2613.png)

## Cloud BigTable Hands On
![image](https://user-images.githubusercontent.com/43883264/180624495-3f3e56e0-0843-436c-92e0-a31edb1c0dc2.png)

![image](https://user-images.githubusercontent.com/43883264/180624512-7bd650cc-68c8-4295-bc5f-ae0e1fcf67c8.png)

- This is how to work with a CBT instance and to read and write data to CBT

https://cloud.google.com/bigtable/docs/create-instance-write-data-hbase-shell

## Cloud Spanner
![image](https://user-images.githubusercontent.com/43883264/180624619-3d1a8d16-7d82-4aee-aa96-89653e1ea982.png)

#### Cloud Spanner - Hands On
![image](https://user-images.githubusercontent.com/43883264/180624663-1c5bc787-47cb-4602-9ff1-f7d212f6563a.png)

![image](https://user-images.githubusercontent.com/43883264/180624668-c96c2fa0-04a4-4a29-9392-9eb862376a5a.png)
- Let's create an instance

![image](https://user-images.githubusercontent.com/43883264/180624759-46bff6b4-dc6c-4953-8996-2c7e89747f77.png)

- This is how to drill down into the instance we have already set up

![image](https://user-images.githubusercontent.com/43883264/180624774-f70c098d-82e6-4f6e-94a9-26defd8d0524.png)

![image](https://user-images.githubusercontent.com/43883264/180624759-46bff6b4-dc6c-4953-8996-2c7e89747f77.png)

# Cloud MemoryStore Fundamentals
![image](https://user-images.githubusercontent.com/43883264/180624807-3776eaea-a317-4419-b60f-09c081c790fd.png)

### Cloud MemoryStore - Hands On

![image](https://user-images.githubusercontent.com/43883264/180624819-bdf269c8-ebe4-4ba9-8473-1091a702c10e.png)

![image](https://user-images.githubusercontent.com/43883264/180624837-dab61ba4-e82d-4698-b777-7bed92bcce8c.png)

- Here's how to create one instance (Note how you cannot change the tier once the instance is created

![image](https://user-images.githubusercontent.com/43883264/180624899-2dced5a9-ef29-4fb3-8e10-c26ded65cc8b.png)
