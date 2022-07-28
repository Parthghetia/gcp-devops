# GKE
![image](https://user-images.githubusercontent.com/43883264/180875415-9be8a30e-3256-4948-9cec-544744a7a521.png)

#### Kubernetes Components Breakdown

##### Kube-apiserver
The API server is a component of the Kubernetes control plane that exposes the Kubernetes API. The API server is the front end for the Kubernetes control plane.

##### ETCD
Consistent and highly-available key value store used as Kubernetes' backing store for all cluster data.

##### Kube-Scheduler
Control plane component that watches for newly created Pods with no assigned node, and selects a node for them to run on.

##### Kube-controller-manager
![image](https://user-images.githubusercontent.com/43883264/180875864-087ffba2-8c3d-40d1-855b-398d1f76dce5.png)

##### Cloud Controller Manager
- A Kubernetes control plane component that embeds cloud-specific control logic. The cloud controller manager lets you link your cluster into your cloud provider's API, and separates out the components that interact with that cloud platform from components that only interact with your cluster.
The cloud-controller-manager only runs controllers that are specific to your cloud provider. 
- If you are running Kubernetes on your own premises, or in a learning environment inside your own PC, the cluster does not have a cloud controller manager.

#### Components of Kubernetes Node
![image](https://user-images.githubusercontent.com/43883264/180876187-3cfcd53c-450d-43bd-852d-a8c7a863a586.png)

##### Kubelet
An agent that runs on each node in the cluster. It makes sure that containers are running in a Pod.

##### Kube-proxy
kube-proxy is a network proxy that runs on each node in your cluster, implementing part of the Kubernetes Service concept.

kube-proxy maintains network rules on nodes. These network rules allow network communication to your Pods from network sessions inside or outside of your cluster.

##### Container Runtime
The container runtime is the software that is responsible for running containers.


## Creating a GKE Cluster

Choose Standard option below:

![image](https://user-images.githubusercontent.com/43883264/181051424-9968dcf4-ebb6-412a-9d53-5560cab53709.png) 

![image](https://user-images.githubusercontent.com/43883264/181051600-0d7e46bc-cc8e-4e28-a17c-34217040aebc.png)

![image](https://user-images.githubusercontent.com/43883264/181051677-ba66835d-3af3-44bf-b139-62e057dbf69d.png)

![image](https://user-images.githubusercontent.com/43883264/181051835-673c0909-25a7-41d4-a925-c7e7739d6a24.png)

- More detailed stuff, go google and some yet to come

- Once cluster is up. Now comes in more of the kubernetes stuff here: https://github.com/Parthghetia/k8sTestingArena/tree/master/k8s-in-action

## Monitoring, Logging and Debugging
- A really handy command here is a command that can be used to check the logs of different pods using a label selector as below

```bash
 kubectl logs --selector app=nginx
2022/07/26 16:11:59 [notice] 1#1: using the "epoll" event method
2022/07/26 16:11:59 [notice] 1#1: nginx/1.23.1
2022/07/26 16:11:59 [notice] 1#1: built by gcc 10.2.1 20210110 (Debian 10.2.1-6)
2022/07/26 16:11:59 [notice] 1#1: OS: Linux 5.10.90+
2022/07/26 16:11:59 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2022/07/26 16:11:59 [notice] 1#1: start worker processes
2022/07/26 16:11:59 [notice] 1#1: start worker process 31
..........
```

## Building a stateless application

![image](https://user-images.githubusercontent.com/43883264/181076319-0cc87e77-65b7-4c95-ac8e-1dc3c136b42e.png)

- All the files for this folder are right here: [
](https://github.com/ACloudGuru-Resources/Course_GKE_Beginner_To_Pro/tree/master/Chapter_Three/Lecture_1_Lab/redisdemo)

- Here is the kubernetes tutorial for that if ever needed: http://pwittrock.github.io/docs/tutorials/stateless-application/guestbook/


## Liveness and readiness probes
#### Liveness Probes

![image](https://user-images.githubusercontent.com/43883264/181600527-41da5043-cec1-459e-b7b4-db9751f6d7ed.png)

Sample yaml definition:

![image](https://user-images.githubusercontent.com/43883264/181600593-c7f312a8-d9ec-4e8e-ac3b-f71343a88f31.png)

#### Readiness Probes
![image](https://user-images.githubusercontent.com/43883264/181600765-65970ad2-2f1e-44ae-ae24-87e4e9bcde49.png)

Sample yaml definition:
![image](https://user-images.githubusercontent.com/43883264/181600819-950325d1-07db-42b6-8eef-268659d597a0.png)

Sample yaml definition with both liveness and readiness probes defined:

![image](https://user-images.githubusercontent.com/43883264/181600913-423f1d84-680a-49e1-b730-1f91f1d0fea8.png)

#### Probe Configuration

![image](https://user-images.githubusercontent.com/43883264/181601042-cb8594da-9c58-497c-8b6c-b27bde01c383.png)

## Accessing external services from inside the pods
- One way is by using service endpoints like below:

![image](https://user-images.githubusercontent.com/43883264/181601475-109b25d5-292e-43af-b2dd-f3e121d7e462.png)



- All the files for this folder are right here: [
