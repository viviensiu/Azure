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

**Azure Virtual Desktop** 
- Desktop and application virtualization service that runs on the cloud. It enables you to use a cloud-hosted version of Windows from any location.
- Works on any devices: Windows, MacOS, iOS, Android from any modern browser.
- Separates OS, apps and data from local hardware and run on remote server instead.
- Windows 10 or Windows 11 Enterprise multi-session, the only Windows client-based operating system that enables multiple concurrent users on a single VM.
- Supports OneNote and Microsoft 365.
- Centralized security management for users' desktops with Microsoft Entra ID. You can enable multifactor authentication to secure user sign-ins. You can also secure access to data by assigning granular role-based access controls (RBACs) to users.

**Azure containers**
- Enables multiple instances of an application on a single host machine, unlike VM which are limited to a single OS.
- Unlike virtual machines, you don't manage the operating system for a container. It bundles a single app and its dependencies.
- VM virtualise the hardware, while containers virtualise the OS.
- Containers are lightweight and designed to be created, scaled out, and stopped dynamically.
- It can be orchestrated with cluster orchestration.
- Azure Container Instances: 
    - PaaS offering.
    - Upload your containers and then the service will run the containers for you.
- Azure Container Apps: 
    - PaaS offering and similar to Azure Container Instances.
    - Extra benefits such as the ability to incorporate load balancing and scaling.
- Azure Kubernetes Service (AKS):
    - Container orchestration service. An orchestration service manages the lifecycle of containers. 
- Containers are used to create solutions by using a microservice architecture, where architecture breaks solution into smaller, independent pieces. This allows you to separate portions of your app into logical sections that can be maintained, scaled, or updated independently.

**Azure Functions** 
- An event-driven, serverless compute option that doesn’t require maintaining virtual machines or containers.
- Key component of serverless computing, can also be used in server env.
- VM and containers are required to be up at all times for an app to function, however, AZ functions wakes up the app when there's event hence it frees up resources when not in use.
- Functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less.
- Benefits:
    - Scale automatically based on demand.
    - Runs your code when it's triggered and automatically deallocates resources when the function is finished. Only charged based on the CPU used.
    - Can be either stateless or stateful: Stateless (the default), fresh restart on each event. For Stateful (called Durable Functions), a context is passed through the function to track prior activity.

**Application hosting options**
- Other than VM and containers, you could also explore:
- **Azure App Service**: 
    - HTTP-based service to build and host web apps, background web jobs, mobile back-ends, and RESTful APIs in the programming language of your choice without managing infrastructure.
    - Supports Windows and Linux.
    - Automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model.
    - Deployment and management are integrated into the platform.
    - Endpoints can be secured.
    - Sites can be scaled quickly to handle high traffic loads.
    - The built-in load balancing and traffic manager provide high availability.
    - Types of web app: ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, or Python.
    - API apps: Full Swagger support and the ability to package and publish your API in Azure Marketplace. API apps can be consumed from any HTTP- or HTTPS-based client.
    - Web jobs: Run a program (.exe, Java, PHP, Python, or Node.js) or script (.cmd, .bat, PowerShell, or Bash) either scheduled or triggered.
    - Mobile app: Provides a backend for iOS or Android. Store mobile app data in a cloud-based SQL database. Authenticate customers against common social providers. Send push notifications. Execute custom back-end logic in C# or Node.js.there's SDK support for native iOS and Android, Xamarin, and React native apps.
