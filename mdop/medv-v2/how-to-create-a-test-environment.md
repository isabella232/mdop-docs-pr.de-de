---
title: So erstellen Sie eine Testumgebung
description: So erstellen Sie eine Testumgebung
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812265"
---
# <span data-ttu-id="f5daf-103">So erstellen Sie eine Testumgebung</span><span class="sxs-lookup"><span data-stu-id="f5daf-103">How to Create a Test Environment</span></span>


<span data-ttu-id="f5daf-104">Im folgenden finden Sie einige Schritte und Anweisungen, die Sie beim Erstellen einer Testumgebung unterstützen, die Sie verwenden können, um Ihr MED-V Workspace-Paket lokal zu testen, bevor Sie es im gesamten Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f5daf-104">The following are some steps and instructions to help you create a test environment that you can use to test your MED-V workspace package locally before deploying it throughout your enterprise.</span></span> <span data-ttu-id="f5daf-105">Dieser Abschnitt enthält Anleitungen zum Erstellen einer Testumgebung, entweder manuell oder mithilfe eines elektronischen Softwareverteilungssystems.</span><span class="sxs-lookup"><span data-stu-id="f5daf-105">This section provides guidance about how to create a test environment, either manually or by using an electronic software distribution system.</span></span>

**<span data-ttu-id="f5daf-106">So erstellen Sie eine Testumgebung mithilfe eines ESD</span><span class="sxs-lookup"><span data-stu-id="f5daf-106">To create a test environment by using an ESD</span></span>**

1.  <span data-ttu-id="f5daf-107">Verwenden Sie die Methode des Unternehmens zur Bereitstellung von Software im gesamten Unternehmen, um die folgenden erforderlichen Komponenten auf einem Testcomputer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f5daf-107">Use your company’s method of deploying software throughout the enterprise to deploy the following necessary components to a test computer.</span></span> <span data-ttu-id="f5daf-108">Installieren Sie Sie in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="f5daf-108">Install them in the following order:</span></span>

    -   <span data-ttu-id="f5daf-109">**Windows Virtual PC** – Falls noch nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="f5daf-109">**Windows Virtual PC** – if not already installed.</span></span> <span data-ttu-id="f5daf-110">Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.</span><span class="sxs-lookup"><span data-stu-id="f5daf-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="f5daf-111">**Windows Virtual PC-Ergänzungen und-Updates**– Falls noch nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="f5daf-111">**Windows Virtual PC Additions and Updates**– if not already installed.</span></span> <span data-ttu-id="f5daf-112">Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.</span><span class="sxs-lookup"><span data-stu-id="f5daf-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="f5daf-113">**Installationsdatei des Med-v-Host-Agents** – installiert den Host-Agent (Med-v \ _HostAgent \ _setup Installationsdatei).</span><span class="sxs-lookup"><span data-stu-id="f5daf-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="f5daf-114">Weitere Informationen finden Sie unter [Manuelles Installieren des MED-V-Host-Agents](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="f5daf-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    -   <span data-ttu-id="f5daf-115">Das **Med-v Workspace-Installationsprogramm, die VHD und die Setup-Datei** , die im **Med-v-Arbeitsbereichs Paket**erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5daf-115">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="f5daf-116">Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="f5daf-116">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        <span data-ttu-id="f5daf-117">**Wichtig**  Das ausführbare Programm für VHD und Setup muss sich im gleichen Ordner wie das MED-V Workspace-Installationsprogramm befinden.</span><span class="sxs-lookup"><span data-stu-id="f5daf-117">**Important** The VHD and Setup executable program must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="f5daf-118">Installieren Sie dann das MED-V Workspace-Installationsprogramm, indem Sie setup.exe ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5daf-118">Then, install the MED-V workspace installer by running setup.exe.</span></span>

         

2.  <span data-ttu-id="f5daf-119">Nachdem alle Komponenten auf dem Testcomputer installiert wurden, führen Sie den MED-V-Host-Agent aus, um die erstmalige Einrichtung zu starten.</span><span class="sxs-lookup"><span data-stu-id="f5daf-119">After all of the components are installed on the test computer, run the MED-V Host Agent to start first time setup.</span></span>

    <span data-ttu-id="f5daf-120">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **MED-V-Host-Agent**.</span><span class="sxs-lookup"><span data-stu-id="f5daf-120">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

    <span data-ttu-id="f5daf-121">**Hinweis**  Wenn Sie den MED-V-Host-Agent nicht physisch auf dem Testcomputer ausführen können, wird das erstmalige Setup beim nächsten Neustart des Computers automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="f5daf-121">**Note** If you cannot physically run the MED-V Host Agent on the test computer, first time setup starts automatically the next time that the computer restarts.</span></span>

     

<span data-ttu-id="f5daf-122">Das erstmalige Setup wird gestartet, und es kann zehn Minuten oder mehr dauern, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f5daf-122">First time setup starts and can take ten minutes or more to finish.</span></span>

<span data-ttu-id="f5daf-123">Informationen zum Testen Ihrer Konfigurationseinstellungen bei der erstmaligen Einrichtung von Setup finden Sie unter [Überprüfen der Einstellungen für die erstmalige Einrichtung](how-to-verify-first-time-setup-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f5daf-123">For information about testing your configuration settings when first time setup is running, see [How to Verify First Time Setup Settings](how-to-verify-first-time-setup-settings.md).</span></span>

**<span data-ttu-id="f5daf-124">So erstellen Sie eine Testumgebung manuell</span><span class="sxs-lookup"><span data-stu-id="f5daf-124">To create a test environment manually</span></span>**

1.  <span data-ttu-id="f5daf-125">Installieren Sie den Med-v-Host-Agent in einer lokalen Testumgebung, die Med-v-Voraussetzungen enthält, beispielsweise Windows Virtual PC mit Ergänzungen und Updates.</span><span class="sxs-lookup"><span data-stu-id="f5daf-125">Install the MED-V Host Agent in a local test environment that includes MED-V prerequisites, such as Windows Virtual PC with additions and updates.</span></span> <span data-ttu-id="f5daf-126">Informationen finden Sie unter [Manuelles Installieren des MED-V-Host-Agents](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="f5daf-126">For information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

2.  <span data-ttu-id="f5daf-127">Kopieren Sie die MED-V Workspace-Dateien in Ihre Testumgebung.</span><span class="sxs-lookup"><span data-stu-id="f5daf-127">Copy the MED-V workspace files to your test environment.</span></span> <span data-ttu-id="f5daf-128">Die Med-v-Arbeitsbereichsdateien befinden sich im Zielordner, den Sie im **Med-v Workspace-Paketer**angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="f5daf-128">The MED-V workspace files are located in the destination folder that you specified in the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="f5daf-129">**Wichtig**  Das ausführbare Programm für VHD und Setup muss sich im gleichen Ordner wie das MED-V Workspace-Installationsprogramm in Ihrer Testumgebung befinden.</span><span class="sxs-lookup"><span data-stu-id="f5daf-129">**Important** The VHD and Setup executable program must be in the same folder on your test environment as the MED-V workspace installer.</span></span>

     

3.  <span data-ttu-id="f5daf-130">Installieren Sie den MED-V-Arbeitsbereich, indem Sie setup.exe ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5daf-130">Install the MED-V workspace by running setup.exe.</span></span>

4.  <span data-ttu-id="f5daf-131">Starten Sie die erstmalige Einrichtung, indem Sie den MED-V-Host-Agent ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5daf-131">Start first time setup by running the MED-V Host Agent.</span></span>

    <span data-ttu-id="f5daf-132">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **MED-V-Host-Agent**.</span><span class="sxs-lookup"><span data-stu-id="f5daf-132">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="f5daf-133">Das erstmalige Setup wird gestartet, und je nach Größe der festgelegten VHD kann es einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="f5daf-133">First time setup starts and might take several minutes to complete, depending on the size of the VHD specified.</span></span>

<span data-ttu-id="f5daf-134">Nun können Sie die verschiedenen Einstellungen für Konfiguration, Anwendungsveröffentlichung und URL-Umleitung testen, die Sie für Ihren MED-V-Arbeitsbereich angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="f5daf-134">You are now ready to test the different settings for configuration, application publishing, and URL redirection that you specified for your MED-V workspace.</span></span>

<span data-ttu-id="f5daf-135">**Hinweis**  Standardmäßig überschreibt MED-V die Richtlinie für die Bildschirmsperre im Gast.</span><span class="sxs-lookup"><span data-stu-id="f5daf-135">**Note** By default, MED-V overrides the screen lock policy in the guest.</span></span> <span data-ttu-id="f5daf-136">Dies stellt jedoch kein Sicherheitsproblem dar, da der Hostcomputer weiterhin die Richtlinie für die Bildschirmsperre berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f5daf-136">However, this does not pose a security problem because the host computer still honors the screen lock policy.</span></span>

 

## <span data-ttu-id="f5daf-137">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f5daf-137">Related topics</span></span>


[<span data-ttu-id="f5daf-138">So überprüfen Sie erstmalige Einstellungen für das Setup</span><span class="sxs-lookup"><span data-stu-id="f5daf-138">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="f5daf-139">So testen Sie die Anwendungsveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="f5daf-139">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="f5daf-140">So testen Sie die URL-Umleitung</span><span class="sxs-lookup"><span data-stu-id="f5daf-140">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

 

 





