---
title: Konfigurieren der Installationsvoraussetzungen
description: Konfigurieren der Installationsvoraussetzungen
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807855"
---
# <span data-ttu-id="1e872-103">Konfigurieren der Installationsvoraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1e872-103">Configure Installation Prerequisites</span></span>


<span data-ttu-id="1e872-104">Die folgenden Anweisungen sind Voraussetzungen für die Installation und Verwendung von Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="1e872-104">The following instructions are prerequisites for installing and using Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

[<span data-ttu-id="1e872-105">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e872-105">Windows Virtual PC</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[<span data-ttu-id="1e872-106">Windows Virtual PC-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="1e872-106">Windows Virtual PC Update</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[<span data-ttu-id="1e872-107">Antivirus/Backup Software-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1e872-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a><span data-ttu-id="1e872-108">Installieren und Konfigurieren von Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e872-108">How to Install and Configure Windows Virtual PC</span></span>


<span data-ttu-id="1e872-109">**Wichtig**  Wenn bereits eine Version von Virtual PC für Windows auf dem Hostcomputer vorhanden ist, müssen Sie Sie deinstallieren, bevor Sie Windows Virtual PC installieren.</span><span class="sxs-lookup"><span data-stu-id="1e872-109">**Important** If a version of Virtual PC for Windows already exists on the host computer, you must uninstall it before you install Windows Virtual PC.</span></span>

 

**<span data-ttu-id="1e872-110">So installieren Sie Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e872-110">To install Windows Virtual PC</span></span>**

1.  <span data-ttu-id="1e872-111">Laden Sie [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) aus dem Microsoft Download Center herunter ( https://go.microsoft.com/fwlink/?LinkId=195918) .</span><span class="sxs-lookup"><span data-stu-id="1e872-111">Download [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195918).</span></span>

2.  <span data-ttu-id="1e872-112">Führen Sie die Installationsdatei auf dem Hostcomputer aus, und führen Sie die Schritte im Assistenten aus.</span><span class="sxs-lookup"><span data-stu-id="1e872-112">Run the installation file on the host computer, and follow the steps in the wizard.</span></span>

<span data-ttu-id="1e872-113">**Wichtig**  Windows Virtual PC enthält das Integrationskomponentenpaket, das Features bereitstellt, die die Interaktion zwischen der virtuellen Umgebung und dem physikalischen Computer verbessern.</span><span class="sxs-lookup"><span data-stu-id="1e872-113">**Important** Windows Virtual PC includes the Integration Components package, which provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="1e872-114">So können Sie beispielsweise die Maus zwischen dem Host und den Gastcomputern bewegen.</span><span class="sxs-lookup"><span data-stu-id="1e872-114">For example, it lets your mouse move between the host and the guest computers.</span></span> <span data-ttu-id="1e872-115">Für MED-V ist die Installation des Integrationskomponentenpakets erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1e872-115">MED-V requires the installation of the Integration Components package.</span></span>

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a><span data-ttu-id="1e872-116">Installieren und Konfigurieren des Windows Virtual PC-Updates</span><span class="sxs-lookup"><span data-stu-id="1e872-116">How to Install and Configure the Windows Virtual PC Update</span></span>


<span data-ttu-id="1e872-117">Das Microsoft-Update, das dem Artikel KB977206 zugeordnet ist, aktiviert den Windows XP-Modus für Computer ohne Hardware unterstützte Virtualisierungs-Technologie (HAV).</span><span class="sxs-lookup"><span data-stu-id="1e872-117">The Microsoft update associated with article KB977206 enables Windows XP Mode for computers without hardware-assisted virtualization (HAV) technology.</span></span> <span data-ttu-id="1e872-118">Wir empfehlen, dieses Update zu installieren, da einige Integrationsfeatures möglicherweise nicht ordnungsgemäß funktionieren, wenn das Integrationskomponentenpaket im Gastbetriebssystem nicht mit der Version von Windows Virtual PC übereinstimmt, die auf dem Hostcomputer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e872-118">We recommended that you install this update because some integration features might not work correctly if the Integration Components package in the guest operating system do not match the version of Windows Virtual PC that is installed on the host computer.</span></span>

<span data-ttu-id="1e872-119">**Wichtig**  Sie müssen dieses Update nicht installieren, wenn Sie MED-V auf Hostcomputern installieren, auf denen Windows 7 mit Service Pack 1 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e872-119">**Important** You do not have to install this update when you are installing MED-V on host computers that are running Windows 7 with Service Pack 1.</span></span>

 

<span data-ttu-id="1e872-120">**Tipp**  Neben dem hier aufgelisteten Update empfehlen wir, dass Sie alle verfügbaren Windows Virtual PC-Updates überprüfen und diese Updates anwenden, die für Ihre Umgebung geeignet oder erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1e872-120">**Tip** In addition to the update listed here, we recommend that you review all available Windows Virtual PC updates and apply those updates that are appropriate or necessary for your environment.</span></span>

 

**<span data-ttu-id="1e872-121">So installieren Sie das Windows Virtual PC-Update</span><span class="sxs-lookup"><span data-stu-id="1e872-121">To install the Windows Virtual PC Update</span></span>**

1.  <span data-ttu-id="1e872-122">Laden Sie das erforderliche Windows Virtual PC-Update aus dem Microsoft Download Center herunter.</span><span class="sxs-lookup"><span data-stu-id="1e872-122">Download the required Windows Virtual PC update from the Microsoft Download Center.</span></span>

    <span data-ttu-id="1e872-123">[32-Bit-Update](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .</span><span class="sxs-lookup"><span data-stu-id="1e872-123">[32-bit Update](https://go.microsoft.com/fwlink/?LinkId=195919) (https://go.microsoft.com/fwlink/?LinkId=195919).</span></span>

    <span data-ttu-id="1e872-124">[64-Bit-Update](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .</span><span class="sxs-lookup"><span data-stu-id="1e872-124">[64-bit Update](https://go.microsoft.com/fwlink/?LinkId=195920) (https://go.microsoft.com/fwlink/?LinkId=195920).</span></span>

2.  <span data-ttu-id="1e872-125">Führen Sie die Installationsdatei auf dem Hostcomputer im erweiterten Modus aus, und führen Sie die Schritte im Assistenten aus.</span><span class="sxs-lookup"><span data-stu-id="1e872-125">Run the installation file on the host computer in elevated mode, and follow the steps in the wizard.</span></span>

    <span data-ttu-id="1e872-126">Weitere Informationen zum Hotfix-Paket für Windows Virtual PC finden Sie im [Artikel 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .</span><span class="sxs-lookup"><span data-stu-id="1e872-126">For more information about the hotfix package for Windows Virtual PC, see [article 977206](https://go.microsoft.com/fwlink/?LinkId=195921) (https://go.microsoft.com/fwlink/?LinkId=195921).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="1e872-127">So konfigurieren Sie Antivirus/Sicherungs Software</span><span class="sxs-lookup"><span data-stu-id="1e872-127">How to Configure Antivirus/Backup Software</span></span>


<span data-ttu-id="1e872-128">Um zu verhindern, dass Antivirus-Aktivitäten die Leistung des virtuellen Desktops beeinträchtigen, empfehlen wir, wo Sie können, die folgenden Typen von virtuellen Maschinen von einem beliebigen Antivirus-oder Sicherungsprozess auszuschließen, der auf dem Hostcomputer ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="1e872-128">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend, where you can, to exclude the following virtual machine file types from any antivirus or backup process that is running on the host computer:</span></span>

-   <span data-ttu-id="1e872-129">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="1e872-129">\*.VMC</span></span>

-   <span data-ttu-id="1e872-130">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="1e872-130">\*.VUD</span></span>

-   <span data-ttu-id="1e872-131">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="1e872-131">\*.VSV</span></span>

-   <span data-ttu-id="1e872-132">\*. VHD</span><span class="sxs-lookup"><span data-stu-id="1e872-132">\*.VHD</span></span>

## <span data-ttu-id="1e872-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1e872-133">Related topics</span></span>


[<span data-ttu-id="1e872-134">Konfigurieren der Umgebungsvoraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1e872-134">Configure Environment Prerequisites</span></span>](configure-environment-prerequisites.md)

[<span data-ttu-id="1e872-135">High-Level-Architektur</span><span class="sxs-lookup"><span data-stu-id="1e872-135">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="1e872-136">Von MED 2.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="1e872-136">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





