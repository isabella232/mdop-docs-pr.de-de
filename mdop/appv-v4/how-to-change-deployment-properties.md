---
title: So ändern Sie die Bereitstellungseigenschaften
description: So ändern Sie die Bereitstellungseigenschaften
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807356"
---
# <span data-ttu-id="acb40-103">So ändern Sie die Bereitstellungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="acb40-103">How to Change Deployment Properties</span></span>


<span data-ttu-id="acb40-104">Mit den folgenden Verfahren können Sie die Informationen zur **Bereitstellungs** Registerkarte für eine von Ihnen sequenzierte Anwendung ändern, einschließlich der Application Virtualization Server-URL, der für die virtualisierten Anwendungen erforderlichen Betriebssysteme und der Ausgabeoptionen für die zu installierende virtuelle Anwendung.</span><span class="sxs-lookup"><span data-stu-id="acb40-104">You can use the following procedures to change the **Deployment** tab information for an application you are sequencing, including the Application Virtualization server URL, the operating systems required by the virtualized applications, and the output options for the virtual application to be installed.</span></span>

**<span data-ttu-id="acb40-105">So ändern Sie die Server-URL</span><span class="sxs-lookup"><span data-stu-id="acb40-105">To change the server URL</span></span>**

1.  <span data-ttu-id="acb40-106">Wählen Sie das Streaming-Protokoll aus dem Dropdown-Listenfeld aus.</span><span class="sxs-lookup"><span data-stu-id="acb40-106">Select the streaming protocol from the drop-down list box.</span></span>

2.  <span data-ttu-id="acb40-107">Geben Sie den Hostnamen des Virtual Application Servers oder des Load Balancer der Servergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="acb40-107">Enter the host name of the virtual application server or the server group's load balancer.</span></span> <span data-ttu-id="acb40-108">Sie können den tatsächlichen Hostnamen oder die IP-Adresse verwenden.</span><span class="sxs-lookup"><span data-stu-id="acb40-108">You can use the actual host name or IP address.</span></span>

3.  <span data-ttu-id="acb40-109">Geben Sie die Portnummer an, auf der der Virtual Application Server oder Load Balancer auf eine Application Virtualization Desktop Client-Anforderung für die gestreamte Anwendung wartet.</span><span class="sxs-lookup"><span data-stu-id="acb40-109">Specify the port number on which the virtual application server or load balancer will listen for an Application Virtualization Desktop Client request for the streamed application.</span></span>

4.  <span data-ttu-id="acb40-110">Geben Sie den relativen Pfad auf dem virtuellen Anwendungsserver an, auf dem das Softwarepaket gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="acb40-110">Specify the relative path on the virtual application server where the software package is stored.</span></span>

**<span data-ttu-id="acb40-111">So ändern Sie die Anforderungen der Anwendungs Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="acb40-111">To change the application operating systems requirements</span></span>**

1.  <span data-ttu-id="acb40-112">Wenn Sie das erforderliche Betriebssystem (en) hinzufügen möchten, wählen Sie es in der Liste **Verfügbare** aus, und klicken Sie auf die Pfeilschaltfläche, die auf das **ausgewählte** Betriebssystem Listen-Steuerelement zeigt.</span><span class="sxs-lookup"><span data-stu-id="acb40-112">To add the required operating system(s), select it in the **Available** list and click the arrow button pointing to the **Selected** operating systems list control.</span></span>

2.  <span data-ttu-id="acb40-113">Wenn Sie ein Betriebssystem entfernen möchten, wählen Sie es im **ausgewählten** Listensteuerelement aus, und klicken Sie auf die Pfeilschaltfläche, die auf das Listensteuerelement **Verfügbare** Betriebssysteme zeigt.</span><span class="sxs-lookup"><span data-stu-id="acb40-113">To remove an operating system, select it in the **Selected** list control, and click the arrow button pointing to the **Available** operating systems list control.</span></span>

**<span data-ttu-id="acb40-114">So ändern Sie die Optionen für die Anwendungsausgabe</span><span class="sxs-lookup"><span data-stu-id="acb40-114">To change the application output options</span></span>**

1.  <span data-ttu-id="acb40-115">Wählen Sie in der Dropdownliste **Komprimierungsalgorithmus** die Komprimierungsmethode aus, die beim Streaming der Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="acb40-115">From the **Compression Algorithm** drop-down list, select the compression method to use when streaming the application.</span></span>

2.  <span data-ttu-id="acb40-116">Aktivieren Sie das Kontrollkästchen **Sicherheitsdeskriptoren erzwingen** , um sicherzustellen, dass Sicherheitsbeschreibungen der verpackten Anwendungen bei der Bereitstellung erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="acb40-116">Select the **Enforce Security Descriptors** check box to ensure security descriptors of the packaged applications are enforced when deployed.</span></span>

3.  <span data-ttu-id="acb40-117">Wählen Sie **Differenzdatei generieren** aus, um eine Differenzdatei für die Anwendung aus der vorherigen sequenzierten Version zu generieren.</span><span class="sxs-lookup"><span data-stu-id="acb40-117">Select **Generate Difference File** to generate a difference file for the application from the previous sequenced version.</span></span>

4.  <span data-ttu-id="acb40-118">Wählen Sie **Microsoft Windows Installer-Paket (MSI) generieren** aus, um ein Installationsprogrammpaket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="acb40-118">Select **Generate Microsoft Windows Installer (MSI) Package** to create an installer package.</span></span>

## <span data-ttu-id="acb40-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="acb40-119">Related topics</span></span>


[<span data-ttu-id="acb40-120">Informationen zur Registerkarte „Bereitstellung“</span><span class="sxs-lookup"><span data-stu-id="acb40-120">About the Deployment Tab</span></span>](about-the-deployment-tab.md)

[<span data-ttu-id="acb40-121">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="acb40-121">Sequencer Console</span></span>](sequencer-console.md)

 

 





