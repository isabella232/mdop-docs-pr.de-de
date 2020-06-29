---
title: So verschieben Sie die MBAM 2.5-Websites
description: So verschieben Sie die MBAM 2.5-Websites
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811341"
---
# <span data-ttu-id="8e31e-103">So verschieben Sie die MBAM 2.5-Websites</span><span class="sxs-lookup"><span data-stu-id="8e31e-103">How to Move the MBAM 2.5 Websites</span></span>


<span data-ttu-id="8e31e-104">Gehen Sie wie folgt vor, um die folgenden MBAM-Websites von einem Computer auf einen anderen zu verschieben, um die folgenden Features von Server a auf Server B zu verschieben:</span><span class="sxs-lookup"><span data-stu-id="8e31e-104">Use these procedures to move the following MBAM websites from one computer to another, that is, to move the following features from Server A to Server B:</span></span>

-   <span data-ttu-id="8e31e-105">Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="8e31e-105">Administration and Monitoring Website</span></span>

-   <span data-ttu-id="8e31e-106">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="8e31e-106">Self-Service Portal</span></span>

<span data-ttu-id="8e31e-107">**Wichtig**  Während der Konfiguration beider Websites müssen Sie die gleiche Verbindungszeichenfolge, die Berichts-URL, Gruppenkonten und das Webdienst-Anwendungspool-Domänenkonto als diejenigen angeben, die Sie aktuell verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e31e-107">**Important** During the configuration of both websites, you must provide the same connection string, Reports URL, group accounts, and web service application pool domain account as the ones that you are currently using.</span></span> <span data-ttu-id="8e31e-108">Wenn Sie nicht die gleichen Werte verwenden, können Sie nicht auf einige Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8e31e-108">If you don’t use the same values, you cannot access some of the servers.</span></span> <span data-ttu-id="8e31e-109">Verwenden Sie zum Abrufen der aktuellen Werte das Windows PowerShell-Cmdlet " **Get-MbamWebApplication** ".</span><span class="sxs-lookup"><span data-stu-id="8e31e-109">To get the current values, use the **Get-MbamWebApplication** Windows PowerShell cmdlet.</span></span>

 

**<span data-ttu-id="8e31e-110">So verschieben Sie die Website "Verwaltung und Überwachung" auf einen anderen Server</span><span class="sxs-lookup"><span data-stu-id="8e31e-110">To move the Administration and Monitoring Website to another server</span></span>**

1.  <span data-ttu-id="8e31e-111">Installieren Sie auf Server B die MBAM 2,5-Server Software.</span><span class="sxs-lookup"><span data-stu-id="8e31e-111">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="8e31e-112">Anweisungen hierzu finden Sie unter [Installieren der MBAM 2,5-Server Software](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="8e31e-112">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="8e31e-113">Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das Feature **Website Verwaltung und Überwachung** aus.</span><span class="sxs-lookup"><span data-stu-id="8e31e-113">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Administration and Monitoring Website** feature.</span></span>

    <span data-ttu-id="8e31e-114">Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamWebApplication** verwenden, um die Website Verwaltung und Überwachung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8e31e-114">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="8e31e-115">Anweisungen zum Konfigurieren der Website "Verwaltung und Überwachung" finden Sie unter [Konfigurieren der MBAM 2,5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8e31e-115">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

**<span data-ttu-id="8e31e-116">So verschieben Sie das Self-Service-Portal auf einen anderen Server</span><span class="sxs-lookup"><span data-stu-id="8e31e-116">To move the Self-Service Portal to another server</span></span>**

1.  <span data-ttu-id="8e31e-117">Installieren Sie auf Server B die MBAM 2,5-Server Software.</span><span class="sxs-lookup"><span data-stu-id="8e31e-117">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="8e31e-118">Anweisungen hierzu finden Sie unter [Installieren der MBAM 2,5-Server Software](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="8e31e-118">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="8e31e-119">Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das **Self-Service-Portal-** Feature aus.</span><span class="sxs-lookup"><span data-stu-id="8e31e-119">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Self-Service Portal** feature.</span></span>

    <span data-ttu-id="8e31e-120">Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamWebApplication** verwenden, um das Self-Service-Portal zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8e31e-120">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Self-Service Portal.</span></span>

    <span data-ttu-id="8e31e-121">Anweisungen zum Konfigurieren der Website "Verwaltung und Überwachung" finden Sie unter [Konfigurieren der MBAM 2,5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8e31e-121">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

3.  <span data-ttu-id="8e31e-122">Wenn die Clientcomputer in Ihrer Organisation nicht auf das Microsoft Content Delivery Network zugreifen können, müssen Sie auch die JavaScript-Dateien verschieben.</span><span class="sxs-lookup"><span data-stu-id="8e31e-122">If the client computers in your organization do not have access to the Microsoft Content Delivery Network, you also have to move the JavaScript files.</span></span> <span data-ttu-id="8e31e-123">Weitere Informationen finden Sie unter [Konfigurieren des Self-Service-Portals, wenn Client Computer nicht auf das Microsoft Content Delivery Network zugreifen können](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) .</span><span class="sxs-lookup"><span data-stu-id="8e31e-123">See [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) for more information.</span></span>

4.  <span data-ttu-id="8e31e-124">Passen Sie das Self-Service-Portal für Ihre Organisation an.</span><span class="sxs-lookup"><span data-stu-id="8e31e-124">Customize the Self-Service Portal for your organization.</span></span> <span data-ttu-id="8e31e-125">Verwenden Sie die Anweisungen unter [Anpassen des Self-Service-Portals für Ihre Organisation](customizing-the-self-service-portal-for-your-organization.md) , um Ihre aktuellen Anpassungen zu überprüfen und benutzerdefinierte Einstellungen im Self-Server-Portal auf Server B zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8e31e-125">Use the instructions in [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md) to review your current customizations and to configure custom settings on the Self-Server Portal on Server B.</span></span>



## <span data-ttu-id="8e31e-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8e31e-126">Related topics</span></span>


[<span data-ttu-id="8e31e-127">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="8e31e-127">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="8e31e-128">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8e31e-128">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="8e31e-129">Verschieben von MBAM 2.5-Funktionen auf einen anderen Server</span><span class="sxs-lookup"><span data-stu-id="8e31e-129">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 

## <span data-ttu-id="8e31e-130">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="8e31e-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8e31e-131">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="8e31e-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8e31e-132">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8e31e-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





