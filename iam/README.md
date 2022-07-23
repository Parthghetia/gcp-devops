# Google Cloud Identity Fundamentals
- Cloud identity helps add another hierarchy to the Google Cloud Organization, this is called Folders

![image](https://user-images.githubusercontent.com/43883264/180619102-aaf7f5cd-ded2-447d-b63f-50e79df0ef76.png)

- Now let's check it out in the console:

![image](https://user-images.githubusercontent.com/43883264/179438387-b19523a4-be52-48cf-ace8-1a44fcc37703.png)

![image](https://user-images.githubusercontent.com/43883264/179438431-50c7f379-5a37-46cd-b741-0faf088a9ba6.png)

- Remember that policy inheritance flows down the hierarchy and that any Roles and policies appied let's say at the Org level would trickle down the structure

# IAM
Cloud IAM Fundamentals

![image](https://user-images.githubusercontent.com/43883264/180617268-38e686db-473d-4c8b-845f-87390873c9d6.png)

![image](https://user-images.githubusercontent.com/43883264/180617304-0922c1f3-031f-44b6-bfa4-7cc092c1e25b.png)

- Up top is a screenshot of the options and selections you would get in IAM in GCP

![image](https://user-images.githubusercontent.com/43883264/180617555-f1168728-5697-4496-9771-cfc02edaac2d.png)



- How to create a service account - basically we are trying to mimic what a person can be able to do but in form of a service account: (same as in k8s)
![image](https://user-images.githubusercontent.com/43883264/180617463-38541662-020a-4b0e-ac8e-8177eaa82879.png)

- Here is a set of pre-defined roles that are already setup
![image](https://user-images.githubusercontent.com/43883264/180617483-5f87ba09-6161-4bcd-bf3c-94cef92d6db0.png)

### Cloud KMS
- This is what is used to encrypt stuff and keep them secure. Basically a key-store
![image](https://user-images.githubusercontent.com/43883264/180617665-2ae8026e-4856-4c17-a33f-5f2c5fdf1f44.png)

![image](https://user-images.githubusercontent.com/43883264/180617700-a79e3dfe-6228-4da5-9696-836600a59209.png)
![image](https://user-images.githubusercontent.com/43883264/180617732-38e66bd2-bd2a-4d2b-b91a-21e39d3bbc26.png)
- How to create a key ring/key


![image](https://user-images.githubusercontent.com/43883264/180617834-c38e03b3-c66d-4569-93f7-8355c579139e.png)

![image](https://user-images.githubusercontent.com/43883264/180617665-2ae8026e-4856-4c17-a33f-5f2c5fdf1f44.png)
- You could then assign permissions based on what you wish once the keys are created as below
![image](https://user-images.githubusercontent.com/43883264/180617880-d972145e-e4a1-464f-9cdf-3103b636214f.png)

### Cloud IAP
![image](https://user-images.githubusercontent.com/43883264/180617905-19b8e441-34e7-4cd3-a92a-8dc724b5e189.png)

![image](https://user-images.githubusercontent.com/43883264/180619241-7082ebf0-2bc6-4b53-88f1-508b834e2331.png)

![image](https://user-images.githubusercontent.com/43883264/180618342-ebf632c8-258c-4682-b26c-a43586127ec3.png)
 
- When an application or resource is protected by IAP, it can only be accessed through the proxy by principals, also known as users, who have the correct Identity and Access Management (IAM) role. When you grant a user access to an application or resource by IAP, they're subject to the fine-grained access controls implemented by the product in use without requiring a VPN. When a user tries to access an IAP-secured resource, IAP performs authentication and authorization checks.
- More here: https://cloud.google.com/iap/docs/concepts-overview

