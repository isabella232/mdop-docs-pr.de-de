---
title: Erforderliche Komponenten MED-V-Installation
description: Erforderliche Komponenten MED-V-Installation
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810873"
---
# <span data-ttu-id="bb842-103">Erforderliche Komponenten MED-V-Installation</span><span class="sxs-lookup"><span data-stu-id="bb842-103">MED-V Installation Prerequisites</span></span>


<span data-ttu-id="bb842-104">Im folgenden sind die Voraussetzungen für die Installation von MED-V zu finden:</span><span class="sxs-lookup"><span data-stu-id="bb842-104">The following are prerequisites for installing MED-V:</span></span>

[<span data-ttu-id="bb842-105">Active Directory-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb842-105">Active Directory Requirements</span></span>](#bkmk-activedirectoryrequirements)

[<span data-ttu-id="bb842-106">Berichtsdatenbank</span><span class="sxs-lookup"><span data-stu-id="bb842-106">Report Database</span></span>](#bkmk-howtoinstallthereportdatabase)

[<span data-ttu-id="bb842-107">Antivirus/Backup Software-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="bb842-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

[<span data-ttu-id="bb842-108">Microsoft Virtual PC 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="bb842-108">Microsoft Virtual PC 2007 SP1</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a><span data-ttu-id="bb842-109">Active Directory-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb842-109">Active Directory Requirements</span></span>


<span data-ttu-id="bb842-110">Wenn Benutzer nicht zur gleichen Domäne gehören, zu der der Server gehört, muss bei der Konfiguration des MED-V-Servers eine Vertrauensstellung zwischen den Domänen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="bb842-110">When configuring the MED-V server, if users are not part of the same domain the server belongs to, a trust must be set between the domains.</span></span>

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a><span data-ttu-id="bb842-111">Installieren der Berichtsdatenbank</span><span class="sxs-lookup"><span data-stu-id="bb842-111">How to Install the Report Database</span></span>


<span data-ttu-id="bb842-112">Die Berichtsdatenbank ist zum Speichern aller MED-V-Arbeitsbereichs Protokolle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bb842-112">The report database is required for storing all MED-V workspace logs.</span></span> <span data-ttu-id="bb842-113">Die Protokolldatenbank wird dann zum Generieren von MED-V-Berichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb842-113">The log database is then used for generating MED-V reports.</span></span> <span data-ttu-id="bb842-114">Informationen zu Berichten finden Sie unter [MED-V-Berichterstellung](med-v-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="bb842-114">For information about reports, see [MED-V Reporting](med-v-reporting.md).</span></span>

<span data-ttu-id="bb842-115">SQL Server kann auf dem gleichen Server wie der MED-V-Server oder auf einem Remoteserver installiert werden.</span><span class="sxs-lookup"><span data-stu-id="bb842-115">SQL Server can be installed on the same server as the MED-V server or on a remote server.</span></span> <span data-ttu-id="bb842-116">Wenn Sie auf einem Remoteserver installieren, lesen Sie [Installieren von SQL Server auf einem Remote](#bkmk-installingsqlserveronaremoteserver)Server.</span><span class="sxs-lookup"><span data-stu-id="bb842-116">If installing on a remote server, see [Installing SQL Server on a Remote Server](#bkmk-installingsqlserveronaremoteserver).</span></span>

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a><span data-ttu-id="bb842-117">Installieren von SQL Server auf einem Remote Server</span><span class="sxs-lookup"><span data-stu-id="bb842-117">Installing SQL Server on a Remote Server</span></span>

**<span data-ttu-id="bb842-118">So installieren Sie SQL Server auf einem Remoteserver</span><span class="sxs-lookup"><span data-stu-id="bb842-118">To install SQL Server on a remote server</span></span>**

1.  <span data-ttu-id="bb842-119">Konfigurieren Sie auf dem Remoteserver Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bb842-119">Configure the following on the remote server:</span></span>

    -   <span data-ttu-id="bb842-120">Instanzname – Standardinstanz</span><span class="sxs-lookup"><span data-stu-id="bb842-120">Instance name—Default instance</span></span>

    -   <span data-ttu-id="bb842-121">Authentifizierungsmodus – gemischter Modus</span><span class="sxs-lookup"><span data-stu-id="bb842-121">Authentication mode—Mixed mode</span></span>

    -   <span data-ttu-id="bb842-122">Benutzer – der erstellte Standardbenutzer ist "SA"</span><span class="sxs-lookup"><span data-stu-id="bb842-122">User—The default user created is “sa”</span></span>

    -   <span data-ttu-id="bb842-123">Kennwort – gewünschtes Kennwort</span><span class="sxs-lookup"><span data-stu-id="bb842-123">Password—Desired password</span></span>

    -   <span data-ttu-id="bb842-124">Sortierungseinstellungen – Standard</span><span class="sxs-lookup"><span data-stu-id="bb842-124">Collation Settings—Default</span></span>

    -   <span data-ttu-id="bb842-125">Fehler in den Verwendungsberichts Einstellungen – Standard</span><span class="sxs-lookup"><span data-stu-id="bb842-125">Error in usage report settings—Default</span></span>

2.  <span data-ttu-id="bb842-126">Installieren Sie die folgenden Dateien auf dem MED-V-Server:</span><span class="sxs-lookup"><span data-stu-id="bb842-126">Install the following files on the MED-V server:</span></span>

    -   <span data-ttu-id="bb842-127">Wenn Sie die Voraussetzungen für die Management Pack Objects-Sammlung für Microsoft SQL Server2008 installieren möchten, laden Sie [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) aus dem Microsoft Download Center herunter.</span><span class="sxs-lookup"><span data-stu-id="bb842-127">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2008, download [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bb842-128">Wenn Sie die Voraussetzungen für die Management Pack Objects-Sammlung für Microsoft SQL Server2005 installieren möchten, laden Sie [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) aus dem Microsoft Download Center herunter.</span><span class="sxs-lookup"><span data-stu-id="bb842-128">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bb842-129">Wenn Sie die erforderlichen dll-Dateien für Microsoft SQL Server2008 installieren möchten, laden Sie die [Microsoft SQL Server 2008 Management Objects-Sammlung](https://go.microsoft.com/fwlink/?LinkId=164041) aus dem Microsoft Download Center herunter.</span><span class="sxs-lookup"><span data-stu-id="bb842-129">To install the required dll files for Microsoft SQL Server2008, download [Microsoft SQL Server 2008 Management Objects Collection](https://go.microsoft.com/fwlink/?LinkId=164041) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bb842-130">Wenn Sie die erforderlichen dll-Dateien für Microsoft SQL Server2005 installieren möchten, laden Sie [Microsoft SQL Server2005-Verwaltungsobjekte](https://go.microsoft.com/fwlink/?LinkId=164040) aus dem Microsoft Download Center herunter.</span><span class="sxs-lookup"><span data-stu-id="bb842-130">To install the required dll files for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bb842-131">Zum Installieren der eigenständigen Installationspakete, die zusätzlichen Nutzen für SQL Server2008 bieten, laden Sie das [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) aus dem Microsoft Download Center herunter.</span><span class="sxs-lookup"><span data-stu-id="bb842-131">To install the stand-alone install packages that provide additional value for SQL Server2008, download the [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bb842-132">Zum Installieren der eigenständigen Installationspakete, die zusätzlichen Nutzen für SQL Server2005 bieten, laden Sie das [Feature Pack für Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) aus dem Microsoft Download Center herunter.</span><span class="sxs-lookup"><span data-stu-id="bb842-132">To install the stand-alone install packages that provide additional value for SQL Server2005, download the [Feature Pack for Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) from the Microsoft Download Center.</span></span>

    <span data-ttu-id="bb842-133">Weitere Informationen zu diesen Dateien finden Sie unter [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) im Microsoft Download Center ( https://go.microsoft.com/fwlink/?LinkId=163960) oder im [Feature Pack für Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) im Microsoft Download Center ( https://go.microsoft.com/fwlink/?LinkId=163961) .</span><span class="sxs-lookup"><span data-stu-id="bb842-133">For more information about these files, see [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163960) or [Feature Pack for Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163961).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="bb842-134">Antivirus/Backup Software-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="bb842-134">Antivirus/Backup Software Configuration</span></span>


<span data-ttu-id="bb842-135">Um zu verhindern, dass Antivirenprogramme die Leistung des virtuellen Desktops beeinträchtigen, empfiehlt es sich, die folgenden virtuellen Computerdatei Typen von jeder Antivirus-oder Sicherungsverarbeitung auszuschließen, die auf dem Host ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="bb842-135">To prevent antivirus activity from affecting the performance of the virtual desktop, it is recommended where possible to exclude the following virtual machine file types from any antivirus or backup processing running on the host:</span></span>

-   <span data-ttu-id="bb842-136">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="bb842-136">\*.VMC</span></span>

-   <span data-ttu-id="bb842-137">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="bb842-137">\*.VUD</span></span>

-   <span data-ttu-id="bb842-138">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="bb842-138">\*.VSV</span></span>

-   <span data-ttu-id="bb842-139">\*. CKM</span><span class="sxs-lookup"><span data-stu-id="bb842-139">\*.CKM</span></span>

-   <span data-ttu-id="bb842-140">\*. EVHD</span><span class="sxs-lookup"><span data-stu-id="bb842-140">\*.EVHD</span></span>

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a><span data-ttu-id="bb842-141">Installieren und Konfigurieren von Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="bb842-141">How to Install and Configure Microsoft Virtual PC2007 SP1</span></span>


<span data-ttu-id="bb842-142">**Wichtig**  Wenn Virtual PC für Windows auf dem Hostcomputer vorhanden ist, deinstallieren Sie es vor der Installation von Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="bb842-142">**Important** If Virtual PC for Windows exists on the host computer, uninstall it before installing Virtual PC2007 SP1.</span></span>

 

**<span data-ttu-id="bb842-143">So installieren Sie Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="bb842-143">To install Microsoft Virtual PC2007 SP1</span></span>**

1.  <span data-ttu-id="bb842-144">Laden Sie virtuelles PC2007 SP1 aus dem Microsoft Download Center [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994)herunter.</span><span class="sxs-lookup"><span data-stu-id="bb842-144">Download Virtual PC2007 SP1 from the Microsoft Download Center [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span></span>

2.  <span data-ttu-id="bb842-145">Führen Sie die Installationsdatei auf dem Hostcomputer aus, und folgen Sie den Anweisungen des Assistenten.</span><span class="sxs-lookup"><span data-stu-id="bb842-145">Run the installation file on the host computer, and follow the wizard.</span></span>

3.  <span data-ttu-id="bb842-146">Installieren des Virtual PC2007 SP1-Updates auf dem Hostcomputer im erweiterten Modus</span><span class="sxs-lookup"><span data-stu-id="bb842-146">Install Virtual PC2007 SP1 update on the host computer in elevated mode.</span></span>

    <span data-ttu-id="bb842-147">Weitere Informationen finden Sie in [der Beschreibung des Hotfix-Pakets für Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span><span class="sxs-lookup"><span data-stu-id="bb842-147">For more information, see [the description of the hotfix package for Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span></span>

    <span data-ttu-id="bb842-148">**Hinweis**  Das virtuelle PC2007 SP1-Update ist für die Ausführung von Virtual PC2007 SP1 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bb842-148">**Note** The Virtual PC2007 SP1 update is required for running Virtual PC2007 SP1.</span></span>

     

## <span data-ttu-id="bb842-149">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="bb842-149">Related topics</span></span>


[<span data-ttu-id="bb842-150">Unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="bb842-150">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

 

 





