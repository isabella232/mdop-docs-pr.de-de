---
title: Informationen zu Microsoft Application Virtualization 4.6SP2
description: Informationen zu Microsoft Application Virtualization 4.6SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808139"
---
# <span data-ttu-id="ce16e-103">Informationen zu Microsoft Application Virtualization 4.6SP2</span><span class="sxs-lookup"><span data-stu-id="ce16e-103">About Microsoft Application Virtualization 4.6 SP2</span></span>


<span data-ttu-id="ce16e-104">Microsoft Application Virtualization (App-V) 4.6 SP2 bietet verschiedene Verbesserungen und neue Features, die in diesem Thema beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ce16e-104">Microsoft Application Virtualization (App-V)4.6 SP2 provides several enhancements and new features, which are described in this topic.</span></span>

<span data-ttu-id="ce16e-105">**Vorsicht**  In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern.</span><span class="sxs-lookup"><span data-stu-id="ce16e-105">**Caution** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="ce16e-106">Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="ce16e-106">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="ce16e-107">Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce16e-107">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="ce16e-108">Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="ce16e-108">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="ce16e-109">Ändern Sie die Registrierung auf Ihr eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="ce16e-109">Change the registry at your own risk.</span></span>

 

**<span data-ttu-id="ce16e-110">Unterstützung für Windows 8 und Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ce16e-110">Support for Windows 8 and Windows Server 2012</span></span>**

<span data-ttu-id="ce16e-111">App-v 4.6 SP2 bietet Unterstützung für Windows 8-und Windows Server 2012-Remote Desktop Dienste.</span><span class="sxs-lookup"><span data-stu-id="ce16e-111">App-V4.6SP2 adds support for Windows 8 and Windows Server 2012 Remote Desktop Services.</span></span>

**<span data-ttu-id="ce16e-112">Unterstützung für die Koexistenz mit App-V 5,0-Client</span><span class="sxs-lookup"><span data-stu-id="ce16e-112">Support for coexistence with App-V 5.0 client</span></span>**

<span data-ttu-id="ce16e-113">App-v 4.6 SP2 bietet Unterstützung für die Koexistenz mit dem Microsoft Application Virtualization 5,0-Client.</span><span class="sxs-lookup"><span data-stu-id="ce16e-113">App-V4.6SP2 provides support for coexistence with the Microsoft Application Virtualization 5.0 client.</span></span> <span data-ttu-id="ce16e-114">Lesen Sie die APP-v 5,0-Dokumentation, um Anweisungen zum Konfigurieren des App-v 5,0-Clients für die Koexistenz mit dem App-v 4.6 SP2-Client zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ce16e-114">Review the App-V 5.0 documentation for instructions on how to configure the App-V 5.0 client for coexistence with the App-V4.6SP2 client.</span></span> <span data-ttu-id="ce16e-115">Weitere Informationen zu App-V 5,0 finden Sie unter [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) auf TechNet.</span><span class="sxs-lookup"><span data-stu-id="ce16e-115">For more information about App-V 5.0, see [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) on TechNet.</span></span>

**<span data-ttu-id="ce16e-116">Möglichkeit zum Virtualisieren von Adobe Reader X mit dem geschützten Modus</span><span class="sxs-lookup"><span data-stu-id="ce16e-116">Ability to virtualize Adobe Reader X with Protected Mode</span></span>**

<span data-ttu-id="ce16e-117">Mit den folgenden Verfahren können Sie Adobe Reader X mit aktiviertem Feature für geschützten Modus virtualisieren.</span><span class="sxs-lookup"><span data-stu-id="ce16e-117">You can virtualize Adobe Reader X with its Protected Mode feature turned on by using the following procedures.</span></span> <span data-ttu-id="ce16e-118">Zuvor mussten Sie den geschützten Modus deaktivieren, um Adobe Reader X zu virtualisieren.</span><span class="sxs-lookup"><span data-stu-id="ce16e-118">Previously you had to disable Protected Mode in order to virtualize Adobe Reader X.</span></span>

<span data-ttu-id="ce16e-119">Bevor Sie den App-V-Sequencer starten, erstellen Sie den folgenden Registrierungswert unter HKEY \ _LOCAL \ _MACHINE Verzeichnis \\software \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span><span class="sxs-lookup"><span data-stu-id="ce16e-119">Before launching the App-V Sequencer, create the following registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ce16e-120">Name</span><span class="sxs-lookup"><span data-stu-id="ce16e-120">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="ce16e-121">Typ</span><span class="sxs-lookup"><span data-stu-id="ce16e-121">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="ce16e-122">Daten</span><span class="sxs-lookup"><span data-stu-id="ce16e-122">Data</span></span></p></td>
<td align="left"><p><span data-ttu-id="ce16e-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce16e-123">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ce16e-124">EnableVFSPassthrough</span><span class="sxs-lookup"><span data-stu-id="ce16e-124">EnableVFSPassthrough</span></span></p></td>
<td align="left"><p><span data-ttu-id="ce16e-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="ce16e-125">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="ce16e-126">1</span><span class="sxs-lookup"><span data-stu-id="ce16e-126">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ce16e-127">Legen Sie diesen Wert auf 1, um <strong> </strong> Adobe Reader X im geschützten Modus während der Startphase zu starten.</span><span class="sxs-lookup"><span data-stu-id="ce16e-127">Set this value to <strong>1</strong> in order to start Adobe Reader X in Protected Mode during the launch phase.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ce16e-128">**Hinweis**  Erstellen Sie auf einem Computer, auf dem ein 64-Bit-Betriebssystem ausgeführt wird, den Registrierungswert unter HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\systemguard\\overrides.</span><span class="sxs-lookup"><span data-stu-id="ce16e-128">**Note** On a computer running a 64-bit operating system, create the registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span></span>

 

<span data-ttu-id="ce16e-129">Fügen Sie für jede OSD-Datei in Ihrem Adobe Reader X-Paket die folgenden Elemente unter dem &lt; Richtlinien &gt; Element hinzu:</span><span class="sxs-lookup"><span data-stu-id="ce16e-129">For each OSD-file in your Adobe Reader X package, add the following items under the &lt;POLICIES&gt; element:</span></span>

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**<span data-ttu-id="ce16e-130">Befehlszeilenparameter für neuen Sequenzer</span><span class="sxs-lookup"><span data-stu-id="ce16e-130">New Sequencer command-line parameter</span></span>**

<span data-ttu-id="ce16e-131">Wenn Sie einen Paket Beschleuniger (PA) über die Sequencer-GUI erstellen, können Sie eine RTF-oder txt-Datei auswählen, die dem Administrator, der den Paket Beschleuniger anwendet, Verpackungs-und Bereitstellungsanleitungen zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="ce16e-131">When you create a Package Accelerator (PA) through the Sequencer GUI, you can select an RTF or TXT file that provides packaging and deployment guidance to the administrators who will apply the Package Accelerator.</span></span> <span data-ttu-id="ce16e-132">Diese Funktionalität steht nun über die Sequencer-CLI zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ce16e-132">This functionality is now available using the Sequencer CLI.</span></span>

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

<span data-ttu-id="ce16e-133">Geben Sie einen Pfad zu einer RTF-oder txt-Datei an, die beim Erstellen eines Paket Beschleunigers Verpackungs-und Bereitstellungsanleitungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ce16e-133">Specify a path to an RTF or TXT file that provides packaging and deployment guidance when creating a Package Accelerator.</span></span>

**<span data-ttu-id="ce16e-134">Die Microsoft-Anwendungsfehler Berichterstattung muss nicht mehr installiert werden</span><span class="sxs-lookup"><span data-stu-id="ce16e-134">Microsoft Application Error Reporting no longer needs to be installed</span></span>**

<span data-ttu-id="ce16e-135">Wenn Sie den App-v 4.6 SP2-Client mithilfe von setup.msi installieren, müssen Sie die Microsoft-Anwendungsfehler Berichterstattung (dw20shared.msi) nicht mehr installieren.</span><span class="sxs-lookup"><span data-stu-id="ce16e-135">When you are installing the App-V4.6SP2 client by using setup.msi, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="ce16e-136">App-v 4.6 SP2 verwendet jetzt die Microsoft-Fehlerberichterstattung.</span><span class="sxs-lookup"><span data-stu-id="ce16e-136">App-V4.6SP2 now uses Microsoft Error Reporting.</span></span> <span data-ttu-id="ce16e-137">Weitere Informationen finden Sie unter [so wird es gemacht: Installieren des App-V-Clients mithilfe von Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span><span class="sxs-lookup"><span data-stu-id="ce16e-137">For more information, see [How to Install the App-V Client by Using Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span></span>

**<span data-ttu-id="ce16e-138">Kundenfeedback und Hotfix-Rollup</span><span class="sxs-lookup"><span data-stu-id="ce16e-138">Customer feedback and hotfix rollup</span></span>**

<span data-ttu-id="ce16e-139">App-v 4.6 SP2 enthält ein Rollup von Korrekturen, um Probleme zu beheben, die seit der APP-v 4,6 SP1-Version gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="ce16e-139">App-V4.6SP2 includes a rollup of fixes to address issues found since the App-V 4.6 SP1 release.</span></span> <span data-ttu-id="ce16e-140">App-v 4.6 SP2 enthält die neuesten Fixes bis einschließlich Microsoft Application Virtualization 4,6 SP1 Hotfix 6.</span><span class="sxs-lookup"><span data-stu-id="ce16e-140">App-V4.6SP2 contains the latest fixes up to and including Microsoft Application Virtualization 4.6 SP1 Hotfix 6.</span></span>

## <span data-ttu-id="ce16e-141">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="ce16e-141">In This Section</span></span>


<a href="" id="app-v-4-6-sp2-release-notes"></a>[<span data-ttu-id="ce16e-142">App-V 4.6 SP2 – Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="ce16e-142">App-V 4.6 SP2 Release Notes</span></span>](https://go.microsoft.com/fwlink/?LinkId=267600)  
<span data-ttu-id="ce16e-143">Bietet die aktuellsten Informationen zu bekannten Problemen mit App-v 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="ce16e-143">Provides the most up-to-date information about known issues with App-V4.6SP2.</span></span>

 

 





