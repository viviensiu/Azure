## Cloud Concepts: Describe the benefits of using Cloud Services

**Benefits of high availability and scalability in the cloud**
When building or deploying a cloud application, two of the biggest considerations are:
    - Uptime (or Availability) 
    - Ability to handle demand (or scale).
**High availability**
- High availability focuses on ensuring maximum availability, regardless of disruptions or events.
- You’ll need to account for service availability guarantees for your services and applications on cloud. Azure is a highly available cloud environment with uptime guarantees depending on the service. These guarantees are part of the service-level agreements (SLAs).
**Azure SLA** (a.k.a uptime) is measured in % for the service or application's availability. 
- The SLA agreement contains info on downtime, customer's entitlement if SLA is not met.
- It's not possible to meet 100% SLA due to:
    - no downtime available for maintenance or upgrade.
    - every components would require a backup with zero interuptions to customer.
- Hence commonly available SLAs are 99%, 99.9%, 99.95%, 99.99%.
- 99% SLA: A total of cumulated hours e.g. 1.6H downtime per week, or 7.2H per month.
- 99.9% SLA: 10 mins downtime per week, or 43.2 mins per month.
- All Azure services have their own SLA, hence it's suggested to study them and consider if these SLAs meet your business criticality expectations.
**Scalability**
- Ability to adjust resources to meet demand. Scale up to meet increased traffic demands or scale down to reduce costs.
- 2 varieties: 
    - **Vertical scaling**: Increasing or decreasing the **capabilities** of resources, e.g. processing power CPU or RAM.
    - **Horizontal scaling**: Adding or Subtracting the **number** of deployed resources, e.g. VM or containers.