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

**Pricing and Total Cost of Ownership (TCO) calculators**
* Pricing calculator: To estimate the cost of any provisioned resources, including compute, storage, and associated network costs. You can even account for different storage options like storage type, access tier, and redundancy. Nothing is provisioned when you add resources to the pricing calculator, and you won't be charged for any services you select.
![alt text](https://github.com/viviensiu/Azure/blob/main/images/price-calculator.png)
* TCO calculator: Helps compare the costs for running an on-premises infrastructure compared to an Azure Cloud infrastructure.  You enter your current infrastructure configuration, including servers, databases, storage, and outbound network traffic, plus power and IT labor costs. The TCO calculator then compares the anticipated costs for your current environment with the same Azure environment.
![alt text](https://github.com/viviensiu/Azure/blob/main/images/total-cost-ownership.png)

**Microsoft Cost Management tool**
* Cost Management: Service to quickly check Azure resource costs, create alerts based on resource spend, and create budgets that can be used to automate management of resources. This helps to stay aware of your resource costs and prevent surprise costs.
* Cost analysis: Subset of Cost Management to provide a quick visual for your Azure costs. You can quickly view the total cost in a variety of different ways, including by billing cycle, region, resource, and so on. 