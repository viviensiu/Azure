## Microsoft Azure Fundamentals: Describe Azure storage accounts
* Provides a unique namespace for your Azure Storage data that's accessible from anywhere in the world over HTTP or HTTPS. Data in this account is secure, highly available, durable, and massively scalable.
* To create a storage account, you need to pick:
    * Storage account type: This determines your services and redundancy options, and impact your use cases.

| Type |	Supported services |	Redundancy Options |	Usage |
|------|-----------------------|-----------------------|----------|
| Standard general-purpose v2 | Blob Storage (including Data Lake Storage), Queue Storage, Table Storage, and Azure Files | LRS, GRS, RA-GRS, ZRS, GZRS, RA-GZRS | Standard storage account type for blobs, file shares, queues, and tables. Recommended for most scenarios using Azure Storage. If you want support for network file system (NFS) in Azure Files, use the premium file shares account type. |
| Premium block blobs | Blob Storage (including Data Lake Storage) | LRS, ZRS | Premium storage account type for block blobs and append blobs. Recommended for scenarios with high transaction rates or that use smaller objects or require consistently low storage latency. | 
| Premium file shares | Azure Files	LRS, ZRS | Premium storage account type for file shares only. Recommended for enterprise or high-performance scale applications. Use this account type if you want a storage account that supports both Server Message Block (SMB) and NFS file shares. |
| Premium page blobs | Page blobs only | LRS | Premium storage account type for page blobs only.|

* Redundancy options:
    * Locally redundant storage (LRS).
    * Geo-redundant storage (GRS).
    * Read-access geo-redundant storage (RA-GRS).
    * Zone-redundant storage (ZRS).
    * Geo-zone-redundant storage (GZRS).
    * Read-access geo-zone-redundant storage (RA-GZRS).

**Storage account endpoints**
* The combination of the storage account name and the Azure Storage service endpoint forms the endpoints for your storage account.
* The following table shows the endpoint format for Azure Storage services.

| Storage service | Endpoint |
|-----------------|-----------------------|
| Blob Storage | ```https://<storage-account-name>.blob.core.windows.net``` |
| Data Lake Storage Gen2 | ```https://<storage-account-name>.dfs.core.windows.net``` |
| Azure Files | ```https://<storage-account-name>.file.core.windows.net``` |
| Queue Storage | ```https://<storage-account-name>.queue.core.windows.net``` |
| Table Storage | ```https://<storage-account-name>.table.core.windows.net``` |