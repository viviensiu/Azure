## Microsoft Azure Fundamentals: Describe Azure identity, access, and security

**Azure directory services**
* Microsoft Entra ID and Microsoft Entra Domain Services.

**Microsoft Entra ID**
* Microsoft Entra ID: Cloud-based identity and access management (IAM) service.
* Active Directory: On-premise Window server's identity and access management (IAM) service.
* Could also help to maintain your on-premises Active Directory deployment. This works by connecting Active Directory with Microsoft Entra ID, and Microsoft helps to detect suspicious sign-in attempts, e.g. from unknown locations or devices at no extra cost (AD doesn't monitor sign-in attempts).
* **Note**: Having both AD and Entra ID means that you need to maintain 2 identity sets. However, you could connect AD and Entra ID to maintain a consistent identity experience, such as connect them using Microsoft Entra Connect.
* Microsoft Entra Connect: synchronizes user identities between on-premises Active Directory and Microsoft Entra ID, to allow using features like SSO, multifactor authentication, and self-service password reset under both systems.
* Microsoft Entra ID is for:
    * IT administrators: Control access to applications and resources based on their business requirements.
    * App developers: Provide a standards-based approach for adding functionality to applications that they build, such as adding SSO functionality to an app or enabling an app to work with a user's existing credentials.
    * Users: Manage identities and maintenance like self-service password reset.
    * Online service subscribers: Account authentication for subscribers of Microsoft 365, Microsoft Office 365, Azure, and Microsoft Dynamics CRM Online.
* Microsoft Entra ID provides services such as:
    * Authentication: Verifying identity, self-service password reset, multifactor authentication, a custom list of banned passwords, and smart lockout services.
    * Single sign-on (SSO).
    * Application management: Manage your cloud and on-premises apps. Features like Application Proxy, SaaS apps, the My Apps portal, and single sign-on provide a better user experience.
    * Device management: Supports the registration of devices. Registration enables devices to be managed through tools like Microsoft Intune. It also allows for device-based Conditional Access policies to restrict access attempts to only those coming from known devices, regardless of the requesting user account.

**Microsoft Entra Domain Services**
* A service that provides managed domain services such as domain join, group policy, lightweight directory access protocol (LDAP), and Kerberos/NTLM authentication. 
* Benefit of domain services without the need to deploy, manage, and patch domain controllers (DCs) in the cloud.
* Why do you need this? To run legacy applications in the cloud that can't use modern authentication methods, or where you don't want directory lookups to always go back to an on-premises AD DS environment. 
* Integrates with your existing Microsoft Entra tenant, so users can sign into services and applications connected to the managed domain using their existing credentials. 
* How does MEDS work:
    * Create a MEDS managed domain and define a unique namespace to be the domain name.
    * 2 Windows Server domain controllers are then deployed into your selected Azure region as a replica set. The DCs are managed by Azure as part of the managed domain.
* Information synchronization:
    * One-way sync. from Microsoft Entra ID to Microsoft Entra Domain Services. Resources created directly inside MEDS are NOT sync back to Entra ID.
    * In a hybrid environment with an on-premises AD DS environment, Microsoft Entra Connect synchronizes identity information with Microsoft Entra ID, which is then synchronized to the managed domain. See image below:
    ![alt text](https://github.com/viviensiu/Azure/blob/main/images/azure-active-directory-sync-topology.png)