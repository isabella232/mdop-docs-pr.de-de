---
title: So installieren Sie den MED-V-Host-Agent manuell
description: So installieren Sie den MED-V-Host-Agent manuell
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804571"
---
# <span data-ttu-id="1d90c-103">So installieren Sie den MED-V-Host-Agent manuell</span><span class="sxs-lookup"><span data-stu-id="1d90c-103">How to Manually Install the MED-V Host Agent</span></span>


<span data-ttu-id="1d90c-104">Es gibt zwei getrennte, aber verwandte Komponenten für die Microsoft Enterprise Desktop Virtualization (Med-v) 2,0-Lösung: den Med-v-Host-Agent und den Gast-Agent.</span><span class="sxs-lookup"><span data-stu-id="1d90c-104">There are two separate but related components to the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="1d90c-105">Der Host-Agent befindet sich auf dem Hostcomputer (dem Computer eines Benutzers, auf dem Windows 7 ausgeführt wird) und stellt einen Kanal für die Kommunikation mit dem Med-v-Gast bereit (dem virtuellen Med-v-Computer, der auf dem Hostcomputer ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="1d90c-105">The Host Agent resides on the host computer (a user’s computer that is running Windows 7) and provides a channel to communicate with the MED-V guest (the MED-V virtual machine running in the host computer).</span></span> <span data-ttu-id="1d90c-106">Darüber hinaus bietet es bestimmte MED-V-verwandte Funktionen, wie etwa die Anwendungsveröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="1d90c-106">It also provides certain MED-V related functionality, such as application publishing.</span></span>

<span data-ttu-id="1d90c-107">In der Regel stellen und installieren Sie den MED-V-Host-Agent unter Verwendung der bevorzugten Software Bereitstellungsmethode Ihres Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="1d90c-107">Typically, you deploy and install the MED-V Host Agent by using your company’s preferred method of provisioning software.</span></span> <span data-ttu-id="1d90c-108">Vor der Bereitstellung von MED-V im gesamten Unternehmen empfiehlt es sich jedoch, den Host-Agent lokal für Tests zu installieren.</span><span class="sxs-lookup"><span data-stu-id="1d90c-108">However, before deploying MED-V across your enterprise, you might prefer to install the Host Agent locally for testing.</span></span> <span data-ttu-id="1d90c-109">In diesem Abschnitt finden Sie Schritt-für-Schritt-Anweisungen für die manuelle Installation des MED-V-Host-Agents.</span><span class="sxs-lookup"><span data-stu-id="1d90c-109">This section provides step-by-step instructions for manually installing the MED-V Host Agent.</span></span>

<span data-ttu-id="1d90c-110">**Hinweis**  Der MED-V-Gast-Agent wird während der erstmaligen Einrichtung automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="1d90c-110">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<span data-ttu-id="1d90c-111">**Wichtig**  Schließen Sie Internet Explorer, bevor Sie den MED-V-Host-Agent installieren, andernfalls können Konflikte später bei der URL-Umleitung auftreten.</span><span class="sxs-lookup"><span data-stu-id="1d90c-111">**Important** Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="1d90c-112">Sie können dies auch tun, indem Sie während einer Verteilung einen Neustart des Computers angeben.</span><span class="sxs-lookup"><span data-stu-id="1d90c-112">You can also do this by specifying a computer restart during a distribution.</span></span>

 

**<span data-ttu-id="1d90c-113">So installieren Sie den MED-V-Host-Agent</span><span class="sxs-lookup"><span data-stu-id="1d90c-113">To install the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="1d90c-114">Suchen Sie die MED-V-Installationsdateien, die Sie im Rahmen des Software Downloads erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="1d90c-114">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="1d90c-115">Doppelklicken Sie auf die MED-V \ _HostAgent \ _setup Installationsdatei.</span><span class="sxs-lookup"><span data-stu-id="1d90c-115">Double-click the MED-V\_HostAgent\_Setup installation file.</span></span>

    <span data-ttu-id="1d90c-116">Der **Microsoft Enterprise Desktop Virtualization (MED-V)-Setup-** Assistent wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1d90c-116">The **Microsoft Enterprise Desktop Virtualization (MED-V) Host Agent Setup** wizard opens.</span></span> <span data-ttu-id="1d90c-117">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="1d90c-117">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="1d90c-118">Akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1d90c-118">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="1d90c-119">Wählen Sie den Zielordner für die Installation des MED-V-Host-Agents aus.</span><span class="sxs-lookup"><span data-stu-id="1d90c-119">Select the destination folder for installing the MED-V Host Agent.</span></span> <span data-ttu-id="1d90c-120">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="1d90c-120">Click **Next**.</span></span>

5.  <span data-ttu-id="1d90c-121">Klicken Sie auf **Installieren**, um mit der Installation des Host-Agents zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="1d90c-121">To begin the Host Agent installation, click **Install**.</span></span>

6.  <span data-ttu-id="1d90c-122">Nachdem die Installation erfolgreich abgeschlossen wurde, klicken Sie auf **Fertig stellen** , um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="1d90c-122">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="1d90c-123">Um zu überprüfen, ob die Installation des Host-Agents erfolgreich war, klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **MED-V-Host-Agent**.</span><span class="sxs-lookup"><span data-stu-id="1d90c-123">To verify that the installation of the Host Agent was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="1d90c-124">**Hinweis**  Bis ein Med-v-Arbeitsbereich installiert ist, kann der Med-v-Host-Agent gestartet und ausgeführt werden, bietet jedoch keine Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="1d90c-124">**Note** Until a MED-V workspace is installed, the MED-V Host Agent can be started and runs, but provides no functionality.</span></span>

 

## <span data-ttu-id="1d90c-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1d90c-125">Related topics</span></span>


[<span data-ttu-id="1d90c-126">So stellen Sie die MED-V-Komponenten über ein elektronisches Softwareverteilungssystem bereit</span><span class="sxs-lookup"><span data-stu-id="1d90c-126">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="1d90c-127">So installieren Sie den Arbeitsbereichs-Packager für MED-V</span><span class="sxs-lookup"><span data-stu-id="1d90c-127">How to Install the MED-V Workspace Packager</span></span>](how-to-install-the-med-v-workspace-packager.md)

[<span data-ttu-id="1d90c-128">So deinstallieren Sie die MED-V-Komponenten</span><span class="sxs-lookup"><span data-stu-id="1d90c-128">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 





