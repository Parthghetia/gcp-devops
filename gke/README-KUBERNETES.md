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

![image](https://user-images.githubusercontent.com/43883264/181601907-d4d73c00-c0d2-4906-95f5-68323e693e63.png)

- If the pods need to access the service they can always do so using the internal DNS like so: 

![image](https://user-images.githubusercontent.com/43883264/181602046-5da4e627-9ef6-4260-8645-c907602c7acd.png)

- Services can also map to external FQDNs and no endpoints needed

![image](https://user-images.githubusercontent.com/43883264/181602226-5322b001-f88f-44ce-a71e-3f0cf6c5b796.png)

- Here is another example for a rabbit MQ service with multiple endpoints

![image](https://user-images.githubusercontent.com/43883264/181602330-9d90383d-74a6-47bb-8e78-7f9fe268c338.png)

- Another way to access external services is by using sidecar containers like so:

![image](https://user-images.githubusercontent.com/43883264/181602428-11feed8b-34e6-4ab8-a198-9ecdba78b17c.png)

## Volumes and Persistent Storage

![image](https://user-images.githubusercontent.com/43883264/181602968-2eb02990-a0ce-45a6-9a6b-26b75248a2bb.png)

- What are PVs (can be skipped)

![image](https://user-images.githubusercontent.com/43883264/181603129-490e3332-eb48-4a4d-81dd-1a5becd3cbcd.png)

- Here are PV and PVC yaml definitions

![image](https://user-images.githubusercontent.com/43883264/181603263-1d6c22a7-8b49-40b5-985e-51882a0e9c7b.png)

![image](https://user-images.githubusercontent.com/43883264/181603286-8ef76c21-9208-48ce-9385-4124f24a594d.png)

- However, GKE is powerful enough to create the volume on its own automatically if you just declare your PV (a plus for GKE)

![image](https://user-images.githubusercontent.com/43883264/181603479-c3cde6e8-62fe-488a-9632-e35049066170.png)

- You can optionally define storage classes to easily attach to pods

![image](https://user-images.githubusercontent.com/43883264/181603675-a636da21-e912-4730-b7e7-3a924f959792.png)

- Volume access modes include:

![image](https://user-images.githubusercontent.com/43883264/181603826-72d2a28d-250c-4c40-a1b9-5a1f5401e654.png)

- Here are some constraints to using GCS for your kubernetes clusters

![image](https://user-images.githubusercontent.com/43883264/181604075-3ce55766-e13d-403c-be26-351451a409e8.png)

- And here are the alternatives to that

![image](https://user-images.githubusercontent.com/43883264/181604293-4e60ca02-7a00-4e24-95f5-c8f2d5938cea.png)

## ConfigMaps and Secrets

#### Secrets

![image](https://user-images.githubusercontent.com/43883264/181604764-151ae61e-7189-4689-8314-0b61318edfef.png)

#### ConfigMaps

![image](https://user-images.githubusercontent.com/43883264/181604947-3d2a4bf6-9edc-4478-864e-b14c5ee82940.png)

![image](https://user-images.githubusercontent.com/43883264/181605026-958c36f5-1867-4e40-a286-c7259f88ab09.png)

- Here is how to do in a container

![image](https://user-images.githubusercontent.com/43883264/181605066-6532d770-ad8f-4da5-a762-30638d952307.png)

![image](https://user-images.githubusercontent.com/43883264/181605143-3609f3be-2243-4402-b491-2bde96b425eb.png)

- Configmaps can also store entire configuration files

![image](https://user-images.githubusercontent.com/43883264/181605235-8d21a602-4311-475f-9eaf-545d80e59c49.png)

![image](https://user-images.githubusercontent.com/43883264/181605284-7ade5a6a-1553-4eab-be71-6648087f14d7.png)

## Deployment Patterns

![image](https://user-images.githubusercontent.com/43883264/181605961-8466581a-2ac0-4690-9ddb-2e898faffec8.png)

#### Rolling Update Strategy

![image](https://user-images.githubusercontent.com/43883264/181606101-8ee08316-b6b5-47b4-abfa-432bfc8a3166.png)

#### Canary Deployments

![image](https://user-images.githubusercontent.com/43883264/181606428-15105ad3-89ab-43f3-b753-04ccb50de529.png)

- yaml definition for canary deployments

![image](https://user-images.githubusercontent.com/43883264/181606453-77060483-009b-4b59-893f-0184b909b4fc.png)

#### Blue-Green Deployments
![image](https://user-images.githubusercontent.com/43883264/181606703-19ddb440-b515-48e6-bb04-1433bb699ef5.png)


## Autoscale in Kubernetes

![image](https://user-images.githubusercontent.com/43883264/181607128-cbaeb445-30dc-481e-bab8-e12c657d164d.png)

#### Horizontal Pod Autoscaler

![image](https://user-images.githubusercontent.com/43883264/181607255-54870ad4-887e-4f9d-925f-da91faee9e3d.png)

- Sample yaml definition for HPA

![image](https://user-images.githubusercontent.com/43883264/181607336-150e6f58-2192-46fc-a457-d9ac521dc1d1.png)


#### Vertical Pod Autoscaler
![image](https://user-images.githubusercontent.com/43883264/181607455-b51a69ac-269f-4b84-9716-0857df197aa9.png)

- Sample yaml definition for VPA

#### Cluster Autoscaler

![image](https://user-images.githubusercontent.com/43883264/181607653-ec0aaa65-254d-4c45-85bc-bc6acf77a48e.png)

## Best practices around autoscaling

![image](https://user-images.githubusercontent.com/43883264/181607829-a65f6406-7201-497b-9a39-c41632e43d2f.png)



# Helm
![image](https://user-images.githubusercontent.com/43883264/181653084-8fb39e6c-6bfb-4e97-b494-4acee522f6e1.png)

- How to use helm

![image](https://user-images.githubusercontent.com/43883264/181653146-545e2e4a-d29e-4924-95c8-82379e101cbe.png)

- Helm chart breakdown

![image](https://user-images.githubusercontent.com/43883264/181653306-4e0ab21a-7537-49aa-a9dc-6015c3a10575.png)

![image](https://user-images.githubusercontent.com/43883264/181653395-80c6be5c-6a3e-42f4-9f22-e8c4202080e6.png)

- There are other helpful helm commands like `helm update` or `helm delete` as well as `helm status` . These are all the commands that can be used to play with a release



# Advanced Ingress Control
## Ingress
![image](https://user-images.githubusercontent.com/43883264/181653575-fbaac6b0-0612-4fcd-8115-c3bf43c9cf87.png)

## Ingress Controller
![image](https://user-images.githubusercontent.com/43883264/181653611-964a5826-e2c6-4f12-8f26-2364c0382425.png)
- Here is how to use an ingress controller using a diag

![image](https://user-images.githubusercontent.com/43883264/181653713-3e455dac-1e96-4c35-bea3-80d536f80691.png)

![image](https://user-images.githubusercontent.com/43883264/181653743-1cea682a-78f6-47f3-8115-c45cfc1af44b.png)

#### NGINX Ingress Controller

![image](https://user-images.githubusercontent.com/43883264/181653824-69f45543-9d34-47b4-acc3-357058ad3527.png)

# High Availability Clusters and Workloads

### Regional GKE Clusters

![image](https://user-images.githubusercontent.com/43883264/181653898-3e108fb9-fb64-42a5-9c54-532e9739019b.png)

### Regional Persistent Storage

![image](https://user-images.githubusercontent.com/43883264/181654013-dd26c247-f53c-436b-80c7-b9162bdc4f36.png)

- Here is how to achieve that

![image](https://user-images.githubusercontent.com/43883264/181654087-a2078dce-c152-4f01-b24f-4f8888e7d913.png)

### Multi-Cluster Ingress

![image](https://user-images.githubusercontent.com/43883264/181654309-948d1883-e5bf-404a-8c83-d4b2b9733c2c.png)

# Running a secure GKE cluster

![image](https://user-images.githubusercontent.com/43883264/181654441-12e9ba50-9974-407f-96ff-7fcc35bfe932.png)

- Securing your GKE Cluster

![image](https://user-images.githubusercontent.com/43883264/181654493-d0c144b5-f1de-4855-8a26-e4811a34b2e7.png)


![image](https://user-images.githubusercontent.com/43883264/181654013-dd26c247-f53c-436b-80c7-b9162bdc4f36.png)

#### RBAC

![image](https://user-images.githubusercontent.com/43883264/181654568-f6ffe68f-5f16-461c-84a2-d68516201fc4.png)

Basic RBAC role definition

![image](https://user-images.githubusercontent.com/43883264/181654620-c60fcd28-fdd9-4254-ac44-58bba21c441c.png)

Basic Cluster Role

![image](https://user-images.githubusercontent.com/43883264/181654654-37aff45a-f83c-4225-afb7-238d3479086d.png)


#### Pod Security Policies

![image](https://user-images.githubusercontent.com/43883264/181654863-540f629d-b8b6-49d9-a830-910390dbfaf9.png)

- Sample Pod Security Policy definition

![image](https://user-images.githubusercontent.com/43883264/181654976-393c150c-2209-4cb5-940f-3e1708951338.png)

![image](https://user-images.githubusercontent.com/43883264/181655000-705175b5-552b-4675-8804-3ea26a5e0d12.png)


#### Network Policies

![image](https://user-images.githubusercontent.com/43883264/181655096-16c131b5-2fa7-4a4e-b392-5e21dad6934c.png)

- Here is an example network policy yaml definition

![image](https://user-images.githubusercontent.com/43883264/181655126-99949c6f-a363-4ed1-8d33-dfd791bc46a2.png)

![image](https://user-images.githubusercontent.com/43883264/181655147-c36e3ff3-b58a-48c3-9f05-160baeb4d01e.png)

#### Workload Identity

![image](https://user-images.githubusercontent.com/43883264/181655242-adbaea9b-0f16-45d1-8534-a5ca22d93518.png)

# Stateful applications and workloads

- Stateful vs stateless

![image](https://user-images.githubusercontent.com/43883264/181655388-00c6a010-5643-4f1a-86c2-a7e452a6a57b.png)

- That is why k8s has statefulsets

![image](https://user-images.githubusercontent.com/43883264/181655464-d1df8e5c-4fc6-48b2-8b39-a2099f95b8c2.png)

- Sample definition of a statefulset

![image](https://user-images.githubusercontent.com/43883264/181655515-8d3d6085-5ca8-4b05-ba3b-7d14c698df86.png)

# Finite Tasks and Init Containers

#### Jobs and CronJobs

![image](https://user-images.githubusercontent.com/43883264/181656147-ead1ab8e-6f95-4ac6-85a0-c43662eaf361.png)

- Sample job manifest

![image](https://user-images.githubusercontent.com/43883264/181656175-c6e19f96-1bd1-4b57-9909-a83aee1e2ca8.png)

![image](https://user-images.githubusercontent.com/43883264/181656228-c94da2cc-7181-4e33-bc39-8fb7aaa6fa78.png)


- Sample cron job manifest

![image](https://user-images.githubusercontent.com/43883264/181656267-d448001d-3e37-4b45-a974-72b33aefaff8.png)

#### Init Containers

![image](https://user-images.githubusercontent.com/43883264/181656482-de61811c-3628-4a3f-89eb-5f8c7c49da6a.png)

- Sample init container manifest

![image](https://user-images.githubusercontent.com/43883264/181656507-fc2e6b01-9102-4bf6-a4cc-7ac35c273554.png)










