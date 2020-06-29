---
title: Problembehandlung von AGPM-Upgrades
description: Problembehandlung von AGPM-Upgrades
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807431"
---
# <span data-ttu-id="01420-103">Problembehandlung von AGPM-Upgrades</span><span class="sxs-lookup"><span data-stu-id="01420-103">Troubleshooting AGPM Upgrades</span></span>

<span data-ttu-id="01420-104">In diesem Abschnitt werden häufig auftretende Probleme aufgeführt, die beim Upgrade des Advanced Group Policy Management (AGPM)-Servers auf eine neuere Version (beispielsweise AGPM 4,0 auf AGPM 4,3) auftreten können.</span><span class="sxs-lookup"><span data-stu-id="01420-104">This section lists common issues that you may encounter when you upgrade your Advanced Group Policy Management (AGPM) server to a newer version (e.g. AGPM 4.0 to AGPM 4.3).</span></span> <span data-ttu-id="01420-105">Wenn Sie Probleme diagnostizieren möchten, die hier nicht aufgeführt sind, ist es möglicherweise hilfreich, die [Problembehandlung für AGPM](troubleshooting-agpm-agpm40.md) anzuzeigen oder einem AGPM-Administrator (Vollzugriff) die Protokollierung und Ablaufverfolgung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="01420-105">To diagnose issues not listed here, it may be helpful to view the [Troubleshooting AGPM](troubleshooting-agpm-agpm40.md) or for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="01420-106">Weitere Informationen finden Sie unter [Konfigurieren der Protokollierung und Ablaufverfolgung](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="01420-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

## <span data-ttu-id="01420-107">Welche Probleme haben Sie?</span><span class="sxs-lookup"><span data-stu-id="01420-107">What problems are you having?</span></span>

-   [<span data-ttu-id="01420-108">Fehler beim Generieren eines HTML-GPO-Unterschiedsberichts (Fehlercode 80004003)</span><span class="sxs-lookup"><span data-stu-id="01420-108">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a><span data-ttu-id="01420-109">Fehler beim Generieren eines HTML-GPO-Unterschiedsberichts (Fehlercode 80004003)</span><span class="sxs-lookup"><span data-stu-id="01420-109">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>

-   <span data-ttu-id="01420-110">**Ursache**: Sie haben das AGPM-Upgrade-Paket mit einem falschen Konto installiert.</span><span class="sxs-lookup"><span data-stu-id="01420-110">**Cause**: You have installed the AGPM upgrade package with an incorrect account.</span></span>

-   <span data-ttu-id="01420-111">**Lösung**: Sie müssen ein AGPM-Administrator sein, um dieses Problem beheben zu können.</span><span class="sxs-lookup"><span data-stu-id="01420-111">**Solution**: You will need to be an AGPM administrator in order to fix this issue.</span></span>
    
    -   <span data-ttu-id="01420-112">Stellen Sie sicher, dass Sie den Benutzernamen & Kennwort Ihres **AGPM-Dienstkontos**kennen.</span><span class="sxs-lookup"><span data-stu-id="01420-112">Ensure you know the username & password of your **AGPM service account**.</span></span>

    -   <span data-ttu-id="01420-113">Melden Sie sich auf Ihrem AGPM-Server interaktiv als AGPM-Dienstkonto an.</span><span class="sxs-lookup"><span data-stu-id="01420-113">Log onto your AGPM server interactively as your AGPM service account.</span></span>
        
        -   <span data-ttu-id="01420-114">Dies ist wichtig, da die Installation fehlschlägt, wenn Sie ein anderes Konto verwenden.</span><span class="sxs-lookup"><span data-stu-id="01420-114">This is critically important, as the install will fail if you use a different account.</span></span>

    -   <span data-ttu-id="01420-115">Beenden Sie den AGPM-Dienst.</span><span class="sxs-lookup"><span data-stu-id="01420-115">Shutdown the AGPM service.</span></span>
    
    -   <span data-ttu-id="01420-116">Installieren Sie den erforderlichen Hotfix.</span><span class="sxs-lookup"><span data-stu-id="01420-116">Install the required hotfix.</span></span>
    
    -   <span data-ttu-id="01420-117">Stellen Sie mit einem AGPM-Client eine Verbindung mit AGPM her, um zu testen, ob Ihre Differenz Berichte nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="01420-117">Connect to AGPM using an AGPM client to test that your difference reports are now functioning.</span></span>
    
## <span data-ttu-id="01420-118">Installieren des Hotfix-Pakets 1 für Microsoft Advanced Group Policy Management 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="01420-118">Install Hotfix Package 1 for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>
    
<span data-ttu-id="01420-119">**In diesem Hotfix behobenes Problem**: AGPM kann keine Differenz Berichte generieren, wenn neue Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) gesteuert oder verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="01420-119">**Issue fixed in this hotfix**: AGPM can't generate difference reports when it controls or manages new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="01420-120">So **erhalten Sie dieses Update**: Installieren Sie die neueste Version des Microsoft-Desktop Optimierungs Pakets ([März 2017-Wartungsversion](https://www.microsoft.com/download/details.aspx?id=54967)).</span><span class="sxs-lookup"><span data-stu-id="01420-120">**How to get this update**: Install the latest version of Microsoft Desktop Optimization Pack ([March 2017 Servicing Release](https://www.microsoft.com/download/details.aspx?id=54967)).</span></span> <span data-ttu-id="01420-121">Weitere Informationen finden Sie unter [KB 4014009](https://support.microsoft.com/help/4014009/) .</span><span class="sxs-lookup"><span data-stu-id="01420-121">See [KB 4014009](https://support.microsoft.com/help/4014009/) for more information.</span></span>

<span data-ttu-id="01420-122">Genauer gesagt: Sie können auswählen, dass nur die erste Datei in `AGPM4.0SP1_Server_X64_KB4014009.exe` der nach dem Drücken der Schaltfläche herunterladen angezeigten Liste heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="01420-122">More specifically, you can choose to download only the first file, `AGPM4.0SP1_Server_X64_KB4014009.exe`, from the list presented after pressing the download button.</span></span>
      
<span data-ttu-id="01420-123">Der Download-Link zum Microsoft-Desktop Optimierungspaket (März 2017-Wartungsversion) finden Sie [hier](https://www.microsoft.com/download/details.aspx?id=54967).</span><span class="sxs-lookup"><span data-stu-id="01420-123">The download link to the Microsoft Desktop Optimization Pack (March 2017 Servicing Release) can be found [here](https://www.microsoft.com/download/details.aspx?id=54967).</span></span>
      
      
## <span data-ttu-id="01420-124">Verweis Link</span><span class="sxs-lookup"><span data-stu-id="01420-124">Reference link</span></span>
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
