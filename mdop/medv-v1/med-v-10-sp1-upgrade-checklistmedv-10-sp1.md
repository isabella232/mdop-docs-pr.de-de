---
title: Upgradeprüfliste für MED-V 1.0 SP1
description: Upgradeprüfliste für MED-V 1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812253"
---
# <span data-ttu-id="948d3-103">Upgradeprüfliste für MED-V 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="948d3-103">MED-V 1.0 SP1 Upgrade Checklist</span></span>


<span data-ttu-id="948d3-104">Um Microsoft Enterprise Desktop Virtualization (Med-v) 1.0 auf Med-v 1.0 Service Pack1 (SP1) zu aktualisieren, muss der Client aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="948d3-104">To upgrade Microsoft Enterprise Desktop Virtualization (MED-V)1.0 to MED-V1.0 Service Pack1 (SP1), the client must be upgraded.</span></span> <span data-ttu-id="948d3-105">Optional kann der Server aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="948d3-105">The server can optionally be upgraded.</span></span>

## <span data-ttu-id="948d3-106">Server Upgrade</span><span class="sxs-lookup"><span data-stu-id="948d3-106">Server Upgrade</span></span>


**<span data-ttu-id="948d3-107">So aktualisieren Sie den Med-v 1.0-Server auf Med-v 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="948d3-107">To upgrade the MED-V1.0 server to MED-V1.0 SP1</span></span>**

1.  <span data-ttu-id="948d3-108">Sichern Sie die folgenden Dateien, die sich im Verzeichnis \* &lt; INSTALLDIR &gt; /Servers/ConfigurationServer\* befinden:</span><span class="sxs-lookup"><span data-stu-id="948d3-108">Back up the following files that are located in the *&lt;InstallDir&gt; / Servers / ConfigurationServer* directory:</span></span>

    -   <span data-ttu-id="948d3-109">OrganizationalPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="948d3-109">OrganizationalPolicy.XML</span></span>

    -   <span data-ttu-id="948d3-110">ClientPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="948d3-110">ClientPolicy.XML</span></span>

    -   <span data-ttu-id="948d3-111">WorkspaceKeys.XML</span><span class="sxs-lookup"><span data-stu-id="948d3-111">WorkspaceKeys.XML</span></span>

2.  <span data-ttu-id="948d3-112">Sichern Sie die \* &lt; INSTALLDIR &gt; /Server/ServerSettings.xml-\* Datei.</span><span class="sxs-lookup"><span data-stu-id="948d3-112">Back up the *&lt;InstallDir&gt; / Servers / ServerSettings.xml* file.</span></span>

3.  <span data-ttu-id="948d3-113">Deinstallieren Sie den Med-v 1.0-Server.</span><span class="sxs-lookup"><span data-stu-id="948d3-113">Uninstall the MED-V1.0 server.</span></span>

4.  <span data-ttu-id="948d3-114">Installieren Sie den Med-v 1.0 SP1-Server.</span><span class="sxs-lookup"><span data-stu-id="948d3-114">Install the MED-V1.0 SP1 server.</span></span>

5.  <span data-ttu-id="948d3-115">Stellen Sie die Sicherungsdateien in den entsprechenden Verzeichnissen wieder her.</span><span class="sxs-lookup"><span data-stu-id="948d3-115">Restore the backup files to the appropriate directories.</span></span>

6.  <span data-ttu-id="948d3-116">Starten Sie den MED-V-Server Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="948d3-116">Restart the MED-V server service.</span></span>

<span data-ttu-id="948d3-117">**Hinweis**  Wenn die Serverkonfiguration vom Standardwert geändert wurde, werden die Dateien möglicherweise an einem anderen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="948d3-117">**Note** If the server configuration has been changed from the default, the files might be stored in a different location.</span></span>

 

## <span data-ttu-id="948d3-118">Client Upgrade</span><span class="sxs-lookup"><span data-stu-id="948d3-118">Client Upgrade</span></span>


<span data-ttu-id="948d3-119">Wenn Sie den Med-v 1.0-Client auf Med-v 1.0 SP1 aktualisieren möchten, installieren Sie die MSP-Datei auf einem Med-v 1.0-Client.</span><span class="sxs-lookup"><span data-stu-id="948d3-119">To upgrade the MED-V1.0 client to MED-V1.0 SP1, install the .msp file on a MED-V1.0 client.</span></span> <span data-ttu-id="948d3-120">Der Client und MED-V werden automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="948d3-120">The client and MED-V are automatically upgraded.</span></span>

 

 





