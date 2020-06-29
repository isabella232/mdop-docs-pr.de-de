---
title: So stellen Sie einen MED-V-Arbeitsbereich manuell bereit
description: So stellen Sie einen MED-V-Arbeitsbereich manuell bereit
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812259"
---
# <span data-ttu-id="66fac-103">So stellen Sie einen MED-V-Arbeitsbereich manuell bereit</span><span class="sxs-lookup"><span data-stu-id="66fac-103">How to Deploy a MED-V Workspace Manually</span></span>


<span data-ttu-id="66fac-104">In einigen Fällen möchten Sie möglicherweise Ihren MED-V-Arbeitsbereich manuell bereitstellen, beispielsweise wenn Ihr Unternehmen kein elektronisches Softwareverteilungssystem zum Bereitstellen von Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="66fac-104">In some instances, you might want to deploy your MED-V workspace manually, for example, if your company does not use an electronic software distribution system to deploy applications.</span></span>

<span data-ttu-id="66fac-105">Dieser Abschnitt enthält Anweisungen dazu, wie Sie einen MED-V-Arbeitsbereich manuell bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="66fac-105">This section provides instruction about how to manually deploy a MED-V workspace.</span></span>

**<span data-ttu-id="66fac-106">So stellen Sie einen MED-V-Arbeitsbereich manuell bereit</span><span class="sxs-lookup"><span data-stu-id="66fac-106">To deploy a MED-V workspace manually</span></span>**

1.  <span data-ttu-id="66fac-107">Kopieren Sie alle erforderlichen Anwendungen und die MED-V Workspace-Paketdateien auf ein freigegebenes Laufwerk oder auf eine DVD.</span><span class="sxs-lookup"><span data-stu-id="66fac-107">Copy all prerequisite applications and the MED-V workspace package files to a shared drive or to a DVD.</span></span> <span data-ttu-id="66fac-108">Die folgende Liste enthält die erforderlichen Anwendungen und Dateien.</span><span class="sxs-lookup"><span data-stu-id="66fac-108">The following is a list of the required applications and files.</span></span>

    -   <span data-ttu-id="66fac-109">**Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="66fac-109">**Windows Virtual PC**.</span></span> <span data-ttu-id="66fac-110">Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.</span><span class="sxs-lookup"><span data-stu-id="66fac-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="66fac-111">**Windows Virtual PC-Ergänzungen und-Updates**.</span><span class="sxs-lookup"><span data-stu-id="66fac-111">**Windows Virtual PC Additions and Updates**.</span></span> <span data-ttu-id="66fac-112">Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.</span><span class="sxs-lookup"><span data-stu-id="66fac-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="66fac-113">**Installationsdatei des Med-v-Host-Agents** – installiert den Host-Agent (Med-v \ _HostAgent \ _setup Installationsdatei).</span><span class="sxs-lookup"><span data-stu-id="66fac-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span>

        **<span data-ttu-id="66fac-114">Warnung</span><span class="sxs-lookup"><span data-stu-id="66fac-114">Warning</span></span>**  
        <span data-ttu-id="66fac-115">Schließen Sie Internet Explorer, bevor Sie den MED-V-Host-Agent installieren, andernfalls können Konflikte später bei der URL-Umleitung auftreten.</span><span class="sxs-lookup"><span data-stu-id="66fac-115">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="66fac-116">Sie können dies auch tun, indem Sie während einer Verteilung einen Neustart des Computers angeben.</span><span class="sxs-lookup"><span data-stu-id="66fac-116">You can also do this by specifying a computer restart during a distribution.</span></span>



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. <span data-ttu-id="66fac-117">Installieren Sie die folgenden in der angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="66fac-117">Install the following in the order listed.</span></span> <span data-ttu-id="66fac-118">Der Endbenutzer kann diese Aufgabe manuell ausführen, oder Sie können ein Skript erstellen, um Folgendes zu installieren:</span><span class="sxs-lookup"><span data-stu-id="66fac-118">The end user can perform this task manually or you can create a script to install the following:</span></span>

   -   <span data-ttu-id="66fac-119">Windows Virtual PC und die Windows Virtual PC-Ergänzungen und-Updates.</span><span class="sxs-lookup"><span data-stu-id="66fac-119">Windows Virtual PC and the Windows Virtual PC additions and updates.</span></span> <span data-ttu-id="66fac-120">Ein Neustart des Computers ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="66fac-120">A computer restart is required.</span></span>

   -   <span data-ttu-id="66fac-121">Der MED-V-Host-Agent.</span><span class="sxs-lookup"><span data-stu-id="66fac-121">The MED-V Host Agent.</span></span>

       **<span data-ttu-id="66fac-122">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="66fac-122">Note</span></span>**  
       <span data-ttu-id="66fac-123">Wenn Sie ausgeführt wird, muss Internet Explorer neu gestartet werden, bevor die Installation des MED-V-Host-Agents abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="66fac-123">If it is running, Internet Explorer must be restarted before the installation of the MED-V Host Agent can finish.</span></span>



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. <span data-ttu-id="66fac-124">Führen Sie die erstmalige Einrichtung durch.</span><span class="sxs-lookup"><span data-stu-id="66fac-124">Complete first time setup.</span></span>

   <span data-ttu-id="66fac-125">Nachdem Sie den Med-v-Arbeitsbereich installiert haben, haben Sie die Möglichkeit, Med-v zu starten.</span><span class="sxs-lookup"><span data-stu-id="66fac-125">After the MED-V workspace is installed, you have the option of starting MED-V.</span></span> <span data-ttu-id="66fac-126">Dadurch wird der MED-V-Host-Agent gestartet.</span><span class="sxs-lookup"><span data-stu-id="66fac-126">This starts the MED-V Host Agent.</span></span> <span data-ttu-id="66fac-127">Sie können entweder Med-v zu diesem Zeitpunkt starten oder den Med-v-Host-Agent später starten, um die erstmalige Einrichtung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="66fac-127">You can either start MED-V at that time, or start the MED-V Host Agent later to complete first time setup.</span></span>

   <span data-ttu-id="66fac-128">Klicken Sie zum Starten des Med-v-Host-Agents auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **Med-v-Host-Agent**.</span><span class="sxs-lookup"><span data-stu-id="66fac-128">To start the MED-V Host Agent, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

## <span data-ttu-id="66fac-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="66fac-129">Related topics</span></span>


[<span data-ttu-id="66fac-130">So stellen Sie einen MED-V-Arbeitsbereich über eines elektronischen Softwareverteilungssystem bereit</span><span class="sxs-lookup"><span data-stu-id="66fac-130">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="66fac-131">So stellen Sie einen MED-V-Arbeitsbereich in ein Windows 7-Image bereit</span><span class="sxs-lookup"><span data-stu-id="66fac-131">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[<span data-ttu-id="66fac-132">Bereitstellen des MED-V-Arbeitsbereichspakets</span><span class="sxs-lookup"><span data-stu-id="66fac-132">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)









