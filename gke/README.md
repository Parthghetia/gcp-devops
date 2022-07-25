# Kubernetes Engine Fundamentals

![image](https://user-images.githubusercontent.com/43883264/179424824-5db91f95-c4ae-448e-b5de-5faaca1040ce.png)

![image](https://user-images.githubusercontent.com/43883264/179424831-bda134ae-c51c-4a12-888c-54fff6fbb450.png)

- Google has a built in API that can be used in order to deploy apps to GKE

![image](https://user-images.githubusercontent.com/43883264/179424899-4b225c59-6120-464b-afee-357ef235e7fb.png)

- Google Cloud Registry is what is used in order to push the images

- Here are the options we have for GKE

![image](https://user-images.githubusercontent.com/43883264/179424974-56263a64-fd6b-408b-888a-998afdb49ca4.png)

#### What are containers?

Containers start life as an image

![image](https://user-images.githubusercontent.com/43883264/180853793-1b9964dc-bc36-4f84-9471-e0ebb643f4db.png)

#### What is a Dockerfile?

![image](https://user-images.githubusercontent.com/43883264/180854072-63b6fcf4-9564-4cc9-8f10-589c74293dbb.png)

#### Dockerfile breakdown

![image](https://user-images.githubusercontent.com/43883264/180854209-10855be4-68ac-4f12-b5d4-fb8787f69cdf.png)

- So looking at the diag below, you'll notice on the right a breakdown of how files are layered one on top of another in order to build the container.
- The first layer is the Ubuntu image, followed by the files that were copied, the topmost layer shows us what changed when the MAKE command is run

![image](https://user-images.githubusercontent.com/43883264/180854619-62575a48-5dc6-480e-bae0-74dd95fb0b8b.png)

