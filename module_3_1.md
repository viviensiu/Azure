## Microsoft Azure Fundamentals: Describe cost management in Azure

**Factors that affect costs in Azure**
* Azure shifts development costs from the capital expense (CapEx) to an operational expense (OpEx) of renting infrastructure as you need it, whether it’s compute, storage, networking, and so on. TOpEx cost can be impacted by many factors such as:
    * Resource type
    * Consumption
    * Maintenance
    * Geography
    * Subscription type
    * Azure Marketplace
* Resource type: Its costs are influenced by the type of resource, the settings of the resource and the Azure region. When you provision an Azure resource, Azure creates metered instances for that resource. The meters track the resources' usage and generate a usage record that is used to calculate your bill.
    * Example of blob storage: Changing its settings and region produce different costs. ![alt text](https://github.com/viviensiu/Azure/blob/main/images/blob-storage.png)
    * Example of a VM: Using different OS licenses, hardwares e.g. processor, num. of CPUs, storage and network results in different costs. ![alt text](https://github.com/viviensiu/Azure/blob/main/images/virtual-machine-settings.png)
* Consumption: Generally you pay-as-you-go for what you use, so it fluctuates around usage. However you could also commit to using a set amount of cloud resources in advance and receiving discounts up to 72% on those “reserved” resources. With the back-up of pay-as-you-go, if you see a sudden surge in demand that eclipses what you’ve pre-reserved, you just pay for the additional resources in excess of your reservation. This model allows you to recognize significant savings on reliable, consistent workloads while also having the flexibility to rapidly increase your cloud footprint as the need arises.
* Maintenance: When you deprovision some resource like a VM, the accompanying resources such as network and storage may not deprovision at the same time. By keeping an eye on your resources and making sure you’re not keeping around resources that are no longer needed, you can help control cloud costs.
* Geography: There are global pricing difference due to the cost of power, labor, taxes, and fees vary depending on the location. Hence Azure resources can differ in costs to deploy depending on the region. Network traffic is also impacted based on geography. For example, it’s less expensive to move information within Europe than to move information from Europe to Asia or South America.
* Network Traffic: Billing zones are a factor in the costs of some services, as data transfer pricing (inbound and outbound) are based on zones. A zone is a geographical grouping of Azure regions for billing purposes.
* Subscription type: Costs are affected by the usage allowances in your subscription, e.g. a free trial subscription offers access to a number of Azure products that are free for 12 months. It also includes $200 credit to spend within your first 30 days of sign-up. You'll get access to more than 25 products that are always free (based on resource and region availability).
* Azure Marketplace: A place to purchase Azure-based solutions and services from third-party vendors. You may pay for not only the Azure services that you’re using, but also the services or expertise of the third-party vendor. Billing structures are set by the vendor. These solutions are certified and compliant with Azure policies and standards. Certification policies may vary based on the service or solution type and Azure service involved.

