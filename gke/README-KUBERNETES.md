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
