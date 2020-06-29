---
title: Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an
description: Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an
author: dansimp
ms.assetid: 78fe0f15-4a36-41e3-96d6-7d5aa77c1e06
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49beb7ea4afe46c9b0f1640152c786d7c6ba8663
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805729"
---
# <span data-ttu-id="81184-103">Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an</span><span class="sxs-lookup"><span data-stu-id="81184-103">How to Apply the Deployment Configuration File by Using PowerShell</span></span>


<span data-ttu-id="81184-104">Die Konfigurationsdatei für die dynamische Bereitstellung wird angewendet, wenn ein Paket hinzugefügt oder auf einen Computer mit dem App-V 5,1-Client gesetzt wird, bevor das Paket veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="81184-104">The dynamic deployment configuration file is applied when a package is added or set to a computer running the App-V 5.1 client before the package has been published.</span></span> <span data-ttu-id="81184-105">Die Datei konfiguriert die Standardeinstellungen für das Paket für alle Benutzer auf dem Computer, auf dem der App-V 5,1-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81184-105">The file configures the default settings for package for all users on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="81184-106">In diesem Abschnitt werden die Schritte beschrieben, die für die Verwendung einer Konfigurationsdatei für die Bereitstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81184-106">This section describes the steps used to use a deployment configuration file.</span></span> <span data-ttu-id="81184-107">Das Verfahren basiert auf dem folgenden Beispiel und setzt voraus, dass die folgenden Paket-und Konfigurationsdateien auf einem Computer vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="81184-107">The procedure is based on the following example and assumes the following package and configuration files exist on a computer:</span></span>

**<span data-ttu-id="81184-108">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="81184-108">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="81184-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="81184-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

**<span data-ttu-id="81184-110">So wenden Sie die Konfigurationsdatei für die Bereitstellung mit PowerShell an</span><span class="sxs-lookup"><span data-stu-id="81184-110">To Apply the Deployment Configuration File Using PowerShell</span></span>**

-   <span data-ttu-id="81184-111">Wenn Sie einen neuen Standardsatz von Konfigurationen für alle Benutzer angeben möchten, die das Paket auf einem bestimmten Computer ausführen sollen, geben Sie mithilfe einer PowerShell-Konsole Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="81184-111">To specify a new default set of configurations for all users who will run the package on a specific computer, using a PowerShell console type the following:</span></span>

    **<span data-ttu-id="81184-112">Add-AppVClientPackage – Path c:\\Packages\\Contoso\\MyApp.AppV-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="81184-112">Add-AppVClientPackage –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

    **<span data-ttu-id="81184-113">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="81184-113">Note</span></span>**  
    <span data-ttu-id="81184-114">Mit diesem Befehl wird das resultierende Objekt in $pkg erfasst.</span><span class="sxs-lookup"><span data-stu-id="81184-114">This command captures the resulting object into $pkg.</span></span> <span data-ttu-id="81184-115">Wenn das Paket bereits auf dem Computer vorhanden ist, kann das Cmdlet " **Set-AppVclientPackage** " verwendet werden, um das Bereitstellungs Konfigurationsdokument anzuwenden:</span><span class="sxs-lookup"><span data-stu-id="81184-115">If the package is already present on the computer, the **Set-AppVclientPackage** cmdlet can be used to apply the deployment configuration document:</span></span>

    **<span data-ttu-id="81184-116">Satz-AppVClientPackage – Name MyApp – Path c:\\Packages\\Contoso\\MyApp.AppV-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="81184-116">Set-AppVClientPackage –Name Myapp –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="81184-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="81184-117">Related topics</span></span>


[<span data-ttu-id="81184-118">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="81184-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









