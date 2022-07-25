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

- More about Docker and Dockerfiles here: https://github.com/Parthghetia/k8sTestingArena/tree/master/k8s-in-action/c1/docker-simple-node-app

- Some more useful docker commands

![image](https://user-images.githubusercontent.com/43883264/180855477-ce1bc2f0-b704-469c-be92-7abd1ce23fc1.png)

#### Docker - Hands On - Lab

![image](https://user-images.githubusercontent.com/43883264/180855659-f35cae39-a024-47e7-8372-fdd9af2237fe.png)

- All the files required for the lab are stored in the folder `sample-docker-app` and the app is built using the following command `docker build -t myapp .`

- You can see a list of the docker images as below. You'll see 2 images, the one you built and the one you inherited from

```bash
ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$ docker images
REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
myapp        latest    010cf627ecd9   3 minutes ago   880MB
python       3.5       3687eb5ea744   22 months ago   871MB
```

- We can also check more history of our app by using the docker history command as below

```bash 
docker history myapp
IMAGE          CREATED         CREATED BY                                      SIZE      COMMENT
010cf627ecd9   4 minutes ago   /bin/sh -c #(nop)  CMD ["python" "-u" "serve…   0B
b62c8b66a423   4 minutes ago   /bin/sh -c pip install -r requirements.txt      9.07MB
c9234b526c4c   4 minutes ago   /bin/sh -c #(nop) WORKDIR /app                  0B
c2d862279753   4 minutes ago   /bin/sh -c #(nop) COPY dir:b82f303f90abe12bf…   499B
3687eb5ea744   22 months ago   /bin/sh -c #(nop)  CMD ["python3"]              0B
<missing>      22 months ago   /bin/sh -c set -ex;   wget -O get-pip.py "$P…   7.24MB
<missing>      22 months ago   /bin/sh -c #(nop)  ENV PYTHON_GET_PIP_SHA256…   0B
<missing>      22 months ago   /bin/sh -c #(nop)  ENV PYTHON_GET_PIP_URL=ht…   0B
<missing>      22 months ago   /bin/sh -c #(nop)  ENV PYTHON_PIP_VERSION=20…   0B
<missing>      22 months ago   /bin/sh -c cd /usr/local/bin  && ln -s idle3…   32B
<missing>      22 months ago   /bin/sh -c set -ex   && wget -O python.tar.x…   42.3MB
<missing>      22 months ago   /bin/sh -c #(nop)  ENV PYTHON_VERSION=3.5.10    0B
<missing>      22 months ago   /bin/sh -c #(nop)  ENV GPG_KEY=97FC712E4C024…   0B
<missing>      22 months ago   /bin/sh -c apt-get update && apt-get install…   17.9MB
<missing>      22 months ago   /bin/sh -c #(nop)  ENV LANG=C.UTF-8             0B
<missing>      22 months ago   /bin/sh -c #(nop)  ENV PATH=/usr/local/bin:/…   0B
<missing>      22 months ago   /bin/sh -c set -ex;  apt-get update;  apt-ge…   510MB
<missing>      22 months ago   /bin/sh -c apt-get update && apt-get install…   146MB
<missing>      22 months ago   /bin/sh -c set -ex;  if ! command -v gpg > /…   17.5MB
<missing>      22 months ago   /bin/sh -c apt-get update && apt-get install…   16.5MB
<missing>      22 months ago   /bin/sh -c #(nop)  CMD ["bash"]                 0B
<missing>      22 months ago   /bin/sh -c #(nop) ADD file:07a6578d6f507bd9c…   114MB
```

- We can now run our docker container using the following commands

```bash
ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$ docker run -d -p 8888:8888 myapp
3474c0c1d073a414ecbce39e79c14b1ed9ea572931421d2b2a1376c2429d1b6c
ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$ docker ps
CONTAINER ID   IMAGE     COMMAND                 CREATED         STATUS         PORTS                    NAMES
3474c0c1d073   myapp     "python -u server.py"   6 seconds ago   Up 5 seconds   0.0.0.0:8888->8888/tcp   vibrant_bohr
ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$ curl http://localhost:8888
Hello, world
ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$ docker logs vibrant_bohr
HTTPServerRequest(protocol='http', host='localhost:8888', method='GET', uri='/', version='HTTP/1.1', remote_ip='172.18.0.1'
ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$ docker exec -it vibrant_bohr /bin/bash
root@3474c0c1d073:/app# ls
Dockerfile  requirements.txt  server.py
root@3474c0c1d073:/app#

```
- Now remember that any files created in the container only stays there until the container lives. So you could create a file within the container and if you remove it. It would be gone. However if you only stop the container and start it again. The file would be there.

- Now let's push our image to a registry:

```bash
ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$ docker images
REPOSITORY                  TAG       IMAGE ID       CREATED          SIZE
gcr.io/parth-ghetia/myapp   latest    010cf627ecd9   17 minutes ago   880MB
myapp                       latest    010cf627ecd9   17 minutes ago   880MB
python                      3.5       3687eb5ea744   22 months ago    871MB

ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$ docker tag myapp gcr.io/pacific-primer-356202/myapp

ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$ docker push gcr.io/pacific-primer-356202/myapp
Using default tag: latest
The push refers to repository [gcr.io/pacific-primer-356202/myapp]
90c36ad0a067: Pushed
54bbfff52dd0: Pushed
95d78f868723: Pushed
493fa57d210f: Pushed
5aed5e63d645: Pushed
97be79495d2a: Pushed
a995c5106335: Layer already exists
17bdf5e22660: Layer already exists
d37096232ed8: Layer already exists
6add0d2b5482: Layer already exists
4ef54afed780: Layer already exists
latest: digest: sha256:1d84a182231c9e850dcf31c2fbbaa9ce6a59fa984f275edfd8921eff1914d3aa size: 2635
ghetiapa@cloudshell:~/parth-docker-sample-app (pacific-primer-356202)$
```
- You can now see your image on GCP and can deploy from there too to let's say GKE

![image](https://user-images.githubusercontent.com/43883264/180860467-2b97faed-31ee-4487-8ca3-8d9bc4b1e491.png)
