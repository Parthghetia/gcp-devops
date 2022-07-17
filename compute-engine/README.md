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

## Creating a disk
image.png