---
title: Entfernen von MBAM-Serverfunktionen oder -software
description: Entfernen von MBAM-Serverfunktionen oder -software
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810879"
---
# <span data-ttu-id="e9fe4-103">Entfernen von MBAM-Serverfunktionen oder -software</span><span class="sxs-lookup"><span data-stu-id="e9fe4-103">Removing MBAM Server Features or Software</span></span>


<span data-ttu-id="e9fe4-104">In diesen Anweisungen wird erläutert, wie Software und Features aus der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-104">These instructions explain how to remove software and features from Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="e9fe4-105">Wenn Sie die MBAM-Server Features entfernen, werden nur die konfigurierten Features vom Server entfernt, nicht die MBAM-Server Software.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-105">If you remove MBAM Server features, only the configured features are removed from the server, not the MBAM Server software.</span></span> <span data-ttu-id="e9fe4-106">Wenn Sie die MBAM-Server Software entfernen, werden die Software und alle MBAM-Server Features, die Sie auf diesem Server konfiguriert haben, entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-106">If you remove the MBAM Server software, the software and any MBAM Server features that you configured on that server are removed.</span></span>

<span data-ttu-id="e9fe4-107">**Hinweis**  Um zu verhindern, dass Daten versehentlich entfernt werden, bietet MBAM keinen Mechanismus zum Entfernen der Datenbanken. Sie müssen dies manuell tun.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-107">**Note** To prevent the accidental removal of data, MBAM provides no mechanism for removing the databases; you must do that manually.</span></span>

 

## <a href="" id="bkmk-removeserverfeatures"></a><span data-ttu-id="e9fe4-108">Entfernen von MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="e9fe4-108">Removing MBAM Server features</span></span>


<span data-ttu-id="e9fe4-109">Sie können eine der folgenden Methoden verwenden, um von Ihnen konfigurierte MBAM-Server Features zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="e9fe4-109">You can use either of the following methods to remove MBAM Server features that you have configured:</span></span>

-   <span data-ttu-id="e9fe4-110">MBAM-Serverkonfigurations-Assistent</span><span class="sxs-lookup"><span data-stu-id="e9fe4-110">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="e9fe4-111">Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9fe4-111">Windows PowerShell cmdlets</span></span>

### <span data-ttu-id="e9fe4-112">Verwenden des MBAM-Serverkonfigurations-Assistenten zum Entfernen von Features</span><span class="sxs-lookup"><span data-stu-id="e9fe4-112">Using the MBAM Server Configuration wizard to remove features</span></span>

<span data-ttu-id="e9fe4-113">Befolgen Sie diese Anweisungen, um den MBAM-Serverkonfigurations-Assistenten zu verwenden, um konfigurierte MBAM-Server Features von einem Server zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-113">Follow these instructions to use the MBAM Server Configuration wizard to remove configured MBAM Server features from a server.</span></span>

**<span data-ttu-id="e9fe4-114">So entfernen Sie MBAM-Features mithilfe des Assistenten</span><span class="sxs-lookup"><span data-stu-id="e9fe4-114">To remove MBAM features by using the wizard</span></span>**

1.  <span data-ttu-id="e9fe4-115">Wählen Sie auf dem Server, auf dem Sie Features entfernen möchten, die Option **MBAM Server Configuration** aus, um den Konfigurations-Assistenten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-115">On the server where you want to remove features, select **MBAM Server Configuration** to open the configuration wizard.</span></span>

2.  <span data-ttu-id="e9fe4-116">Klicken Sie auf **Features entfernen**, wählen Sie die zu entfernenden Features aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-116">Click **Remove Features**, select the features to remove, and then click **Next**.</span></span> <span data-ttu-id="e9fe4-117">Auf einer **Zusammenfassungs** Seite werden die Features angezeigt, die Sie zum Entfernen ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-117">A **Summary** page displays the features you selected for removal.</span></span>

3.  <span data-ttu-id="e9fe4-118">Klicken Sie auf **Entfernen** , um das Entfernen der Features zu starten, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-118">Click **Remove** to start removing the features, and then click **Close**.</span></span>

### <span data-ttu-id="e9fe4-119">Verwenden von Windows PowerShell zum Entfernen von Features</span><span class="sxs-lookup"><span data-stu-id="e9fe4-119">Using Windows PowerShell to remove features</span></span>

<span data-ttu-id="e9fe4-120">Führen Sie die folgenden Schritte als allgemeine Anleitung zum Entfernen von MBAM-Server Features mithilfe von Windows PowerShell-Cmdlets aus.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-120">Use the following steps as a general guide to remove MBAM Server features by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="e9fe4-121">So entfernen Sie MBAM-Features mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e9fe4-121">To remove MBAM features by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="e9fe4-122">Bevor Sie Features entfernen, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-122">Before removing any features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="e9fe4-123">Verwenden Sie die folgenden Cmdlets, um die MBAM-Server Features zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="e9fe4-123">Use the following cmdlets to remove MBAM Server features:</span></span>

    -   <span data-ttu-id="e9fe4-124">Deaktivieren-MbamReport</span><span class="sxs-lookup"><span data-stu-id="e9fe4-124">Disable-MbamReport</span></span>

    -   <span data-ttu-id="e9fe4-125">Deaktivieren-MbamWebApplication</span><span class="sxs-lookup"><span data-stu-id="e9fe4-125">Disable-MbamWebApplication</span></span>

    -   <span data-ttu-id="e9fe4-126">Deaktivieren-MbamCMIntegration</span><span class="sxs-lookup"><span data-stu-id="e9fe4-126">Disable-MbamCMIntegration</span></span>

    <span data-ttu-id="e9fe4-127">Wenn Sie Hilfe zu Windows PowerShell-Cmdlets erhalten möchten, geben Sie **Get-Help-** &lt; *Cmdlet* ein, &gt; oder lesen Sie die Seite [Automatisierung des Microsoft-Desktop Optimierungs Pakets mit Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) für die MBAM Windows PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-127">To get help with Windows PowerShell cmdlets, type **Get-Help** &lt;*cmdlet*&gt; or see the [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) page for the MBAM Windows PowerShell cmdlets.</span></span>

## <span data-ttu-id="e9fe4-128">Entfernen der MBAM-Server Software</span><span class="sxs-lookup"><span data-stu-id="e9fe4-128">Removing MBAM Server software</span></span>


<span data-ttu-id="e9fe4-129">Führen Sie die folgenden Schritte aus, um die MBAM-Server Software und alle MBAM-Server Features zu entfernen, die Sie auf diesem Server konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-129">Use the following steps to remove the MBAM Server software and any MBAM Server features that you configured on that server.</span></span>

**<span data-ttu-id="e9fe4-130">So entfernen Sie die MBAM-Server Software</span><span class="sxs-lookup"><span data-stu-id="e9fe4-130">To remove the MBAM Server software</span></span>**

1.  <span data-ttu-id="e9fe4-131">Führen Sie auf dem Server, auf dem Sie die MBAM-Server Software deinstallieren möchten, **MBAMserversetup.exe** aus, um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung zu starten.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-131">On the server where you want to uninstall the MBAM Server software, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="e9fe4-132">Wählen Sie **deinstallieren**aus, und folgen Sie den restlichen Eingabeaufforderungen, um den Vorgang der Deinstallation der MBAM-Server Software abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-132">Select **Uninstall**, and follow the remaining prompts to complete the process of uninstalling the MBAM Server software.</span></span>



## <span data-ttu-id="e9fe4-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e9fe4-133">Related topics</span></span>


[<span data-ttu-id="e9fe4-134">Bereitstellen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e9fe4-134">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

 

 

## <span data-ttu-id="e9fe4-135">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="e9fe4-135">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e9fe4-136">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="e9fe4-136">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e9fe4-137">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e9fe4-137">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



