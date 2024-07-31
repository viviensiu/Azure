## Microsoft Azure Fundamentals: Describe Azure compute and networking services

**Azure virtual machines**
- VM: Provides IaaS in the form of a virtualized server. No hardware maintenance, however you still need to configure, update, and maintain the software.
- VMs are an ideal choice when you need:
    * Total control over the operating system (OS).
    * The ability to run custom software.
    * To use custom hosting configurations.
- An image is a template used to create a VM and may already include an OS and other software, like development tools or web hosting environments.
- You can even create or use an already created image to rapidly provision VMs.

**Scale VMs in Azure**
- Azure can manage the grouping of VMs for you with features such as scale sets and availability sets.
- Virtual machine scale sets: 
    * Create and manage a group of identical, load-balanced VMs.
    * Scale sets allow you to centrally manage, configure, and update a large number of VMs in minutes.
    * The number of VM instances can automatically increase or decrease in response to demand, or you can set it to scale based on a defined schedule.
    * Automatically deploy a load balancer.
- Availability sets:
    * Ensure that VMs stagger updates and have varied power and network connectivity, preventing you from losing all your VMs with a single network or power failure. 
    * Group VMs in 2 way: update domain and fault domain.
    * Update domain: groups VMs that can be rebooted at the same time. 
    * Fault domain: groups VMs by common power source and network switch. By default, an availability set will split your VMs across up to 3 fault domains. This helps protect against a physical power or networking failure by having VMs in different fault domains.
    * No additional cost for configuring an availability set.

**Examples of when to use VMs**
- During testing and development.
- When running applications in the cloud.
- When extending your datacenter to the cloud.
- During disaster recovery.

**Move to the cloud with VMs**
- lift and shift by creating an image of the physical server and host it within the VM.

**VM Resources**
- Size (purpose, number of processor cores, and amount of RAM)
- Storage disks (hard disk drives, solid state drives, etc.)
- Networking (virtual network, public IP address, and port configuration)