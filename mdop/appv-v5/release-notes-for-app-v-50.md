---
title: Versionshinweise für App-V 5.0
description: Versionshinweise für App-V 5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804889"
---
# <span data-ttu-id="ff42f-103">Versionshinweise für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ff42f-103">Release Notes for App-V 5.0</span></span>


**<span data-ttu-id="ff42f-104">Drücken Sie STRG + F, um nach einem bestimmten Problem in diesen Versionshinweisen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ff42f-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="ff42f-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie App-V 5,0 installieren.</span><span class="sxs-lookup"><span data-stu-id="ff42f-105">Read these release notes thoroughly before you install App-V 5.0.</span></span>

<span data-ttu-id="ff42f-106">Diese Versionshinweise enthalten Informationen, die erforderlich sind, um App-V 5,0 erfolgreich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ff42f-106">These release notes contain information that is required to successfully install App-V 5.0.</span></span> <span data-ttu-id="ff42f-107">Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ff42f-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="ff42f-108">Wenn es einen Unterschied zwischen diesen Anmerkungen zu dieser Version und einer anderen App-V 5,0-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="ff42f-108">If there is a difference between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="ff42f-109">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ff42f-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="ff42f-110">Informationen zur Produktdokumentation</span><span class="sxs-lookup"><span data-stu-id="ff42f-110">About the Product Documentation</span></span>


<span data-ttu-id="ff42f-111">Informationen zur APP-v 5,0-Dokumentation finden Sie auf der APP-v 5,0-Startseite auf der Microsoft TechNet-Website.</span><span class="sxs-lookup"><span data-stu-id="ff42f-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="ff42f-112">Feedback geben</span><span class="sxs-lookup"><span data-stu-id="ff42f-112">Provide Feedback</span></span>


<span data-ttu-id="ff42f-113">Wir sind an Ihrem Feedback zu App-V 5,0 interessiert.</span><span class="sxs-lookup"><span data-stu-id="ff42f-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="ff42f-114">Sie können Ihr Feedback an senden <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="ff42f-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="ff42f-115">**Hinweis**  Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback wird uns helfen, zukünftige Änderungen in unseren Dokumentations-und Produktversionen zu planen.</span><span class="sxs-lookup"><span data-stu-id="ff42f-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="ff42f-116">Die neuesten Informationen zu MDOP und weiteren Lernressourcen finden Sie auf der Seite [MDOP-Informationen](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="ff42f-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="ff42f-117">Wenn Sie weitere Informationen zu neuen Updates oder Feedback geben möchten, folgen Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="ff42f-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="ff42f-118">Bekannte Probleme mit App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ff42f-118">Known Issues with App-V 5.0</span></span>


<span data-ttu-id="ff42f-119">Dieser Abschnitt enthält Versionshinweise zu den bekannten Problemen mit App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ff42f-119">This section contains release notes about the known issues with App-V 5.0.</span></span>

### <span data-ttu-id="ff42f-120">Beim Verwenden von Server-PowerShell-Cmdlets kann das Hinzufügen von Paketen nicht beendet werden</span><span class="sxs-lookup"><span data-stu-id="ff42f-120">Unable to terminate adding packages when using server PowerShell cmdlets</span></span>

<span data-ttu-id="ff42f-121">Wenn Sie ein Paket mit PowerShell hinzufügen, gibt es keine Methode, um das Hinzufügen neuer Pakete zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ff42f-121">When you add a package using PowerShell, there is no method to exit adding new packages.</span></span>

<span data-ttu-id="ff42f-122">Problemumgehung: um das Hinzufügen von Paketen zu beenden, drücken Sie die **EINGABETASTE** , nachdem Sie das endgültige Paket hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="ff42f-122">WORKAROUND: To stop adding packages, press **enter** after you have added the final package.</span></span>

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> <span data-ttu-id="ff42f-123">App-V 5,0-Client lehnt Pakete von Servern ab, deren SSL-Zertifikat gesperrt wurde</span><span class="sxs-lookup"><span data-stu-id="ff42f-123">App-V 5.0 client rejects packages from servers whose SSL certificate has been revoked</span></span>

<span data-ttu-id="ff42f-124">Wenn das HTTPS-Protokoll verwendet wird, lehnt der App-V 5,0-Clientstandard mäßig Pakete von Servern ab, deren SSL-Zertifikat widerrufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ff42f-124">When using the HTTPS protocol, the App-V 5.0 client will by default reject packages from servers whose SSL certificate has been revoked.</span></span> <span data-ttu-id="ff42f-125">Dieses Verhalten kann durch die Konfiguration deaktiviert werden, indem Sie die **VerifyCertificateRevocationList** -Einstellung ändern.</span><span class="sxs-lookup"><span data-stu-id="ff42f-125">This behavior can be turned off through configuration by modifying the **VerifyCertificateRevocationList** setting.</span></span> <span data-ttu-id="ff42f-126">Das Anwenden einer neuen Konfiguration für diese Einstellung wird erst wirksam, nachdem der App-V 5,0-Dienst neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="ff42f-126">Applying new configuration for this setting will not take effect until the App-V 5.0 service is restarted.</span></span>

<span data-ttu-id="ff42f-127">Problemumgehung: Starten Sie den App-V 5,0-Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="ff42f-127">WORKAROUND: Restart the App-V 5.0 service.</span></span>

## <span data-ttu-id="ff42f-128">Anmerkungen zu dieser Version Copyright-Informationen</span><span class="sxs-lookup"><span data-stu-id="ff42f-128">Release Notes Copyright Information</span></span>


<span data-ttu-id="ff42f-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe.</span><span class="sxs-lookup"><span data-stu-id="ff42f-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="ff42f-130">Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.</span><span class="sxs-lookup"><span data-stu-id="ff42f-130">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="ff42f-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ff42f-131">Related topics</span></span>


[<span data-ttu-id="ff42f-132">Informationen zu App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ff42f-132">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





