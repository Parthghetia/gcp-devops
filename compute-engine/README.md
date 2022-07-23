## Compute Engine
- How to create a normal instance and all the options
![image](https://user-images.githubusercontent.com/43883264/179421954-d2aa7577-749d-4952-ace1-1253f0db82c6.png)
![image](https://user-images.githubusercontent.com/43883264/179421976-33f551c9-a280-4b17-9eec-0fdbccd9e12f.png)
- Under boot disk you got the following options
![image](https://user-images.githubusercontent.com/43883264/179421982-c90ad847-8436-4d3c-bece-6240976f7737.png)

## Instance groups
- There are two types:
![image](https://user-images.githubusercontent.com/43883264/179422076-629333c9-40bc-46f2-a9c3-d8b40075954d.png)
#### When to use Managed Instance Groups
![image](https://user-images.githubusercontent.com/43883264/179422091-11830668-c4d1-4867-b135-5ce32ebb842f.png)
- Benefits of using Managed Instance Groups would be:
1. Keeping VM instances running - MIG automatically creates mistakenly deleted VMs
2. Application based auto-healing - setup app based health check to help your instances heal
3. Regional Coverage - regional MIGs helps you setup access across different regions
4. Load Balancing - MIGs can help load balance across all your VMs
- All the above points are encompassed under HA. More benefits would include:
1. Scalability - autoscaled VMs can automatically grow when needed based on demand/time and other factors
2. Automated Updates - MIG automatic updater basically let's you safely deploy new versions of your application using flexible rollout scenarios, Such as rolling updates or canary updates
3. Support for stateful workloads - You can use MIGs for building highly available deployments and automating operation of applications with stateful data or configuration, such as databases, DNS servers, legacy monolith applications, or long-running batch computations with checkpointing. Stateful MIGs preserve each instance's unique state (instance name, attached persistent disks, and metadata) on machine restart, recreation, auto-healing, and update events.

#### Unmanaged Instance Groups
- Unmanaged instance groups can contain heterogeneous instances that you can arbitrarily add and remove from the group. Unmanaged instance groups do not offer autoscaling, autohealing, rolling update support, multi-zone support etc

## Instance Templates 
- An instance template is a resource that you can use to create virtual machine (VM) instances and managed instance groups (MIGs)
- Instance templates are designed to create instances with identical configurations. So you cannot update an existing instance template or change an instance template after you create it.

- Here are some of the other services that are provided by Compute Engine:

![image](https://user-images.githubusercontent.com/43883264/179422516-52f517b1-4e9b-4dd3-9ac7-cc92c5030066.png)

## Google Cloud TPUs (Tensor Processing Unit)
![image](https://user-images.githubusercontent.com/43883264/179422537-2fc564d6-2363-4c31-aac8-0750127155e3.png)

## Health Checks
![image](https://user-images.githubusercontent.com/43883264/179422586-cb7b74c8-f8f5-47a2-9acb-fae0e81bda63.png)

## Zones
![image](https://user-images.githubusercontent.com/43883264/179422597-0e67420d-a5c5-4957-9ec2-d35da13d859d.png)

## Operations
- Shows all that you do in Compute Engine

![image](https://user-images.githubusercontent.com/43883264/179422616-414901fc-d512-44d7-a266-e58836d86b0a.png)

## Compute Engine Settings
![image](https://user-images.githubusercontent.com/43883264/179422641-599fdf41-7cd2-46b6-88ec-47d9393dc25e.png)

-> All networking settings will be found in VPC


## Hands On - Setting up a web server on Compute Engine using Windows Server
![image](https://user-images.githubusercontent.com/43883264/180065112-7bdee57c-a690-40ba-a2aa-b8ac0750159e.png)
![image](https://user-images.githubusercontent.com/43883264/180065165-22b59e8f-2c1a-441c-9ac5-718bf74827ab.png)
