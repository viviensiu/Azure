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
* **Summary**: When using a cloud provider, you’ll always be responsible for:
    - The information and data stored in the cloud
    - Devices that are allowed to connect to your cloud (cell phones, computers, and so on)
    - The accounts and identities of the people, services, and devices within your organization

* The cloud provider is always responsible for:
    - The physical datacenter
    - The physical network
    - The physical hosts
* Your service model will determine responsibility for things like:
    - Operating systems (IaaS: customer, PaaS and SaaS: Microsoft)
    - Network controls (IaaS: customer, PaaS: shared, SaaS: Microsoft)
    - Applications (IaaS: customer, PaaS: shared, SaaS: Microsoft)
    - Identity and infrastructure (IaaS: customer, PaaS and SaaS: shared)

**Cloud models**
* 3 types: Private, Public, Hybrid.
* **Private Cloud**:
    - Used by a single entity
    - Pros: Greater control
    - Cons: Greater cost, fewer benefits compared to a public cloud.
    - Could be hosted from on site datacenter, dedicated datacenter offsite, or even by a third party that has dedicated that datacenter to your company.
* **Public Cloud**:
    - Built, controlled, and maintained by a third-party cloud provider.
    - Anyone that wants to purchase cloud services can access and use resources.
* **Hybrid Cloud**:
    - Uses both public and private clouds in an inter-connected environment. 
    - Can be used to allow a private cloud to surge for temporary demand by deploying public cloud resources. 
    - Can be used to provide an extra layer of security. For example, users can flexibly choose which services to keep in public cloud and which to deploy to their private cloud infrastructure.
| Public cloud | Private cloud | Hybrid cloud |
| No capital expenditures to scale up | Organizations have complete control over resources and security | Provides the most flexibility |
| Applications can be quickly provisioned and deprovisioned | Data is not collocated with other organizations’ data | Organizations determine where to run their applications |
| Organizations pay only for what they use | Hardware must be purchased for startup and maintenance | Organizations control security, compliance, or legal requirements |
| Organizations don’t have complete control over resources and security | Organizations are responsible for hardware maintenance and updates | |
* **Other Cloud models**
    - Multi-cloud: multiple cloud providers
* **Azure Arc**: Manages private/public/hybrid/multi-cloud environments.
* **Azure VMware Solution**: allows redeploy, extend and run VMWare workloads that was established in private cloud when the private cloud is migrated to in public cloud (Azure)