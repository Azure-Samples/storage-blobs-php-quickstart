---
services: storage
platforms: php
author: roygara
---

# Transfer objects to and from Azure Blob storage using PHP

This repository contains a simple sample project to help you getting started with Azure storage using .NET as the development language.

## Prerequisites

To complete this tutorial:

To complete this quickstart: 
* Install [PHP](http://php.net/downloads.php)
* Install [The Azure SDK for PHP](../../php-download-sdk.md)

If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.

## Create a storage account using the Azure portal

First, create a new general-purpose storage account to use for this quickstart. 

1. Go to the [Azure portal](https://portal.azure.com/#create/Microsoft.StorageAccount-ARM) and log in using your Azure account. 
2. Enter a unique name for your storage account. Keep these rules in mind for naming your storage account:
    - The name must be between 3 and 24 characters in length.
    - The name may contain numbers and lowercase letters only.
3. Make sure that the following default values are set: 
    - **Deployment model** is set to **Resource manager**.
    - **Account kind** is set to **General purpose**.
    - **Performance** is set to **Standard**.
    - **Replication** is set to **Locally Redundant storage (LRS)**.
4. Select your subscription. 
5. For **Resource group**, create a new one and give it a unique name. 
6. Select the **Location** to use for your storage account.
7. Check **Pin to dashboard** and click **Create** to create your storage account. 

After your storage account is created, it is pinned to the dashboard. Click on it to open it. Under **Settings**, click **Access keys**. Select the primary key and copy the associated **Connection string** to the clipboard, then paste it into a text editor for later use.

## Put the connection string in an environment variable

This solution requires a connection string be stored in an environment variable securely on the machine running the sample. Follow one of the examples below depending on your Operating System to create the environment variable. If using windows close out of your open IDE or shell and restart it to be able to read the environment variable.

### Linux

```bash
export storageconnectionstring="<yourconnectionstring>"
```
### Windows

```cmd
setx storageconnectionstring "<yourconnectionstring>"
```

At this point, you can run this application. It creates its own file to upload and download, and then cleans up after itself by deleting everything at the end.

## More information

The [Azure storage documentation](https://docs.microsoft.com/azure/storage/) includes a rich set of tutorials and conceptual articles, which serve as a good complement to the samples.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.