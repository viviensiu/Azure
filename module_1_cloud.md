**What is cloud computing?**
- Delivery of computing services over the internet, such as common IT infrastructure plus IoT, ML and AI.
- Services are hosted in data centers owned by cloud providers.
- You only pay for only the service you used.
- Upkeep is managed by cloud providers, e.g. backup, OS updates, 24/7 SLA
- Services typically vary by cloud providers, however, all providers would provide these 2 services:
    - Compute power: how much processing your computer can do.
    - Storage.

**Shared responsibility model**
* In traditional data centers, companies are responsible for: 
    - Maintaining the physical space, security, maintaining or replacing the servers. 
    - Infrastructure and software needed to keep the datacenter up and running. 
    - Keeping all systems patched and on the correct version.
* Shared responsibility model divides these between cloud provider and consumer:
    - Cloud provider: Physical security, power, cooling, and network connectivity
    - Consumer: Data and information stored in the cloud, and access security.
* In some situations, the shared responsibility model may difer, example:
    - Cloud SQL database: Cloud provider maintains the actual database, while consumer is responsible for the data that gets ingested into the database.
    - If you deployed a virtual machine and installed an SQL database on it, you’d be responsible for database patches and updates, as well as maintaining the data and information stored in the database.
* The shared responsibility model is heavily tied into the cloud service types: 
    - IaaS: Infrastructure as a service, 
    - PaaS: Platform as a service, 
    - SaaS: Software as a service.
![shared responsibilities of IaaS, PaaS, SaaS](https://raw.githubusercontent.com/viviensiu/Azure/main/images/shared-responsibility.svg)
* When using a cloud provider, you’ll always be responsible for:
    - The information and data stored in the cloud
    - Devices that are allowed to connect to your cloud (cell phones, computers, and so on)
    - The accounts and identities of the people, services, and devices within your organization

* The cloud provider is always responsible for:
    - The physical datacenter
    - The physical network
    - The physical hosts
* Your service model will determine responsibility for things like:
    - Operating systems
    - Network controls
    - Applications
    - Identity and infrastructure