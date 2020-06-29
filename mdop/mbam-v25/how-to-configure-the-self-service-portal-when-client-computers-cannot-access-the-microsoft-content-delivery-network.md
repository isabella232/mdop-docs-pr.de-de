---
title: So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können
description: So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810588"
---
# <span data-ttu-id="19ceb-103">So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können</span><span class="sxs-lookup"><span data-stu-id="19ceb-103">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>


<span data-ttu-id="19ceb-104">Befolgen Sie diese Anweisungen, wenn die Clientcomputer in Ihrer Organisation nicht auf das Microsoft AJAX Content Delivery Network (CDN) zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="19ceb-104">Follow these instructions if the client computers in your organization do not have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

**<span data-ttu-id="19ceb-105">Gründe für die Konfiguration:</span><span class="sxs-lookup"><span data-stu-id="19ceb-105">Why you need to configure this:</span></span>**

<span data-ttu-id="19ceb-106">Ihre Clientcomputer benötigen Zugriff auf das CDN, wodurch dem Self-Service-Portal der erforderliche Zugriff auf bestimmte JavaScript-Dateien gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="19ceb-106">Your client computers need access to the CDN, which gives the Self-Service Portal the required access to certain JavaScript files.</span></span> <span data-ttu-id="19ceb-107">Wenn Sie das Self-Service-Portal nicht konfigurieren, wenn Clientcomputer nicht auf CDN zugreifen können, werden nur der Firmenname und das Konto angezeigt, unter dem sich der Endbenutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="19ceb-107">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which the end user logs in will be displayed.</span></span> <span data-ttu-id="19ceb-108">Es wird keine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19ceb-108">No error message will be shown.</span></span>

<span data-ttu-id="19ceb-109">**Hinweis**  In MBAM 2,5 SP1 sind die JavaScript-Dateien im Produkt enthalten, und Sie müssen die Anweisungen in diesem Abschnitt nicht befolgen, um den SSP so zu konfigurieren, dass Clients unterstützt werden, die nicht auf das Internet zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="19ceb-109">**Note** In MBAM 2.5 SP1, the JavaScript files are included in the product, and you do not need to follow the instructions in this section to configure the SSP to support clients that cannot access the internet.</span></span>

 

**<span data-ttu-id="19ceb-110">Konfigurieren des Self-Service-Portals, wenn Clientcomputer nicht auf das CDN zugreifen können</span><span class="sxs-lookup"><span data-stu-id="19ceb-110">How to configure the Self-Service Portal when client computers cannot access the CDN</span></span>**

1. <span data-ttu-id="19ceb-111">Laden Sie die folgenden JavaScript-Dateien aus dem CDN herunter:</span><span class="sxs-lookup"><span data-stu-id="19ceb-111">Download the following JavaScript files from the CDN:</span></span>

   -   [<span data-ttu-id="19ceb-112">jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="19ceb-112">jQuery-1.10.2.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [<span data-ttu-id="19ceb-113">jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="19ceb-113">jQuery.validate.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [<span data-ttu-id="19ceb-114">jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="19ceb-114">jQuery.validate.unobtrusive.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390517)

2. <span data-ttu-id="19ceb-115">Kopieren Sie die JavaScript-Dateien in das Verzeichnis **Skripts** des Self-Service-Portals.</span><span class="sxs-lookup"><span data-stu-id="19ceb-115">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="19ceb-116">Dieses Verzeichnis befindet sich in <em> &lt; MBAM Self-Service-Installationsverzeichnis &gt; \\ </em> Self-Service Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="19ceb-116">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

3. <span data-ttu-id="19ceb-117">Öffnen Sie Internet Informationsdienste (IIS)-Manager.</span><span class="sxs-lookup"><span data-stu-id="19ceb-117">Open Internet Information Services (IIS) Manager.</span></span>

4. <span data-ttu-id="19ceb-118">Erweitern Sie **Sites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung**, und markieren Sie **Selfservice**.</span><span class="sxs-lookup"><span data-stu-id="19ceb-118">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="19ceb-119">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="19ceb-119">Note</span></span>**  
   <span data-ttu-id="19ceb-120">*Selfservice* ist der Name des virtuellen Standardverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="19ceb-120">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="19ceb-121">Wenn Sie während der Konfiguration einen anderen Namen für dieses Verzeichnis gewählt haben, denken Sie daran, *Selfservice* in diesen Anweisungen durch den von Ihnen gewählten Namen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="19ceb-121">If you chose a different name for this directory during the configuration, remember to replace *SelfService* in these instructions with the name you chose.</span></span>

     

5. <span data-ttu-id="19ceb-122">Doppelklicken Sie im mittleren Bereich auf **Anwendungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="19ceb-122">In the middle pane, double-click **Application Settings**.</span></span>

6. <span data-ttu-id="19ceb-123">Bearbeiten Sie für jedes Element in der folgenden Liste die Anwendungseinstellungen, um auf den neuen Speicherort zu verweisen, indem Sie/ &lt; *virtuelles Verzeichnis* &gt; /durch/Selfservice/(oder einen beliebigen Namen, den Sie während der Konfiguration ausgewählt haben) ersetzen.</span><span class="sxs-lookup"><span data-stu-id="19ceb-123">For each item in the following list, edit the application settings to reference the new location by replacing /&lt;*virtual directory*&gt;/ with /SelfService/ (or whatever name you chose during configuration).</span></span> <span data-ttu-id="19ceb-124">Beispielsweise ist der Pfad des virtuellen Verzeichnisses mit/Selfservice/Scripts/jQuery-1.10.2.min.js vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="19ceb-124">For example, the virtual directory path will be similar to /selfservice/Scripts/ jQuery-1.10.2.min.js.</span></span>

   -   <span data-ttu-id="19ceb-125">jQueryPath:/ &lt; *virtuelles Verzeichnis* &gt; /Scripts/jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="19ceb-125">jQueryPath: /&lt;*virtual directory*&gt;/Scripts/jQuery-1.10.2.min.js</span></span>

   -   <span data-ttu-id="19ceb-126">jQueryValidatePath:/ &lt; *virtuelles Verzeichnis* &gt; /Scripts/jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="19ceb-126">jQueryValidatePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.min.js</span></span>

   -   <span data-ttu-id="19ceb-127">jQueryValidateUnobtrusivePath:/ &lt; *virtuelles Verzeichnis* &gt; /Scripts/jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="19ceb-127">jQueryValidateUnobtrusivePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.unobtrusive.min.js</span></span>



## <span data-ttu-id="19ceb-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="19ceb-128">Related topics</span></span>


[<span data-ttu-id="19ceb-129">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="19ceb-129">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

 

## <span data-ttu-id="19ceb-130">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="19ceb-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="19ceb-131">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="19ceb-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="19ceb-132">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="19ceb-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





