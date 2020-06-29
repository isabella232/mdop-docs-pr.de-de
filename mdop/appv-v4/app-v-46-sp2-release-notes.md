---
title: App-V 4.6 SP2 – Versionshinweise
description: App-V 4.6 SP2 – Versionshinweise
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809298"
---
# <span data-ttu-id="7cbb1-103">App-V 4.6 SP2 – Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="7cbb1-103">App-V 4.6 SP2 Release Notes</span></span>


**<span data-ttu-id="7cbb1-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="7cbb1-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Application Virtualization (App-V) 4.6 SP2 installieren.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-105">Read these release notes thoroughly before you install Microsoft Application Virtualization (App-V)4.6 SP2.</span></span>

<span data-ttu-id="7cbb1-106">Diese Anmerkungen zu dieser Version enthalten Informationen, die zur erfolgreichen Installation von Application Virtualization 4,6 SP2 erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-106">These release notes contain information that is required to successfully install Application Virtualization 4.6 SP2.</span></span> <span data-ttu-id="7cbb1-107">Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="7cbb1-108">Wenn es einen Unterschied zwischen diesen Versionshinweisen und einer anderen APP-v 4.6 SP2-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-108">If there is a difference between these release notes and other App-V4.6SP2 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="7cbb1-109">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="7cbb1-110">Informationen zur Produktdokumentation</span><span class="sxs-lookup"><span data-stu-id="7cbb1-110">About the Product Documentation</span></span>


<span data-ttu-id="7cbb1-111">Weitere Informationen zur Dokumentation für App-V finden Sie auf der Seite [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) auf Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-111">For more information about documentation for App-V, see the [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) page on Microsoft TechNet.</span></span>

## <span data-ttu-id="7cbb1-112">Abgeben von Feedback</span><span class="sxs-lookup"><span data-stu-id="7cbb1-112">Providing feedback</span></span>


<span data-ttu-id="7cbb1-113">Wir sind an Ihrem Feedback zu app-v 4.6 SP2 interessiert.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-113">We are interested in your feedback on App-V4.6SP2.</span></span> <span data-ttu-id="7cbb1-114">Sie können Ihr Feedback an senden <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="7cbb1-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="7cbb1-115">**Hinweis**  Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback wird uns helfen, zukünftige Änderungen für unsere Dokumentation und Produktversionen zu planen.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-115">**Note** This email address is not a support channel, but your feedback will help us to plan future changes for our documentation and product releases.</span></span>

 

<span data-ttu-id="7cbb1-116">Die neuesten Informationen zu MDOP und weiteren Lernressourcen finden Sie auf der Seite [MDOP-Informationen](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="7cbb1-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="7cbb1-117">Wenn Sie weitere Informationen zu neuen Updates oder Feedback geben möchten, folgen Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="7cbb1-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a><span data-ttu-id="7cbb1-118">Bekannte Probleme mit App-v 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="7cbb1-118">Known Issues with App-V4.6SP2</span></span>


### <span data-ttu-id="7cbb1-119">Die Unterstützung für kurze Dateinamen ist für physikalische Laufwerke ohne System deaktiviert, wenn Sie eine Sequenz</span><span class="sxs-lookup"><span data-stu-id="7cbb1-119">Short file name support is disabled for non-system physical drives when you sequence</span></span>

<span data-ttu-id="7cbb1-120">Wenn Sie eine Sequenz unter Windows 8 oder Windows Server 2012 ablaufen, ist die Unterstützung für kurze Dateinamen (8,3) standardmäßig für physikalische Laufwerke ohne System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-120">When you sequence on Windows 8 or Windows Server 2012, support for short file names (8.3) is disabled by default for non-system physical drives.</span></span>

<span data-ttu-id="7cbb1-121">Das dem primären virtuellen Anwendungsverzeichnis zugeordnete physikalische Laufwerk (beispielsweise "Q:\\appname") auf der Sequenz Station muss eine Unterstützung für kurze Dateinamen (8,3) bereitstellen, damit der APP-v 4.6 SP2-Sequenzer beim Erstellen von virtuellen Anwendungspaketen kurze Dateinamen generiert.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-121">The underlying physical drive associated with the primary virtual application directory (for example, “Q:\\appname”) on the sequencing station must provide short file name (8.3) support in order for the App-V4.6SP2 Sequencer to generate short file names when creating virtual application packages.</span></span> <span data-ttu-id="7cbb1-122">Die Unterstützung für kurze Dateinamen (8,3) ist standardmäßig für physikalische Laufwerke ohne System unter Windows 8 oder Windows Server 2012 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-122">Short file name (8.3) support is disabled by default for non-system physical drives on Windows 8 or Windows Server 2012.</span></span>

<span data-ttu-id="7cbb1-123">**Problemumgehung:** Aktivieren Sie die Unterstützung für kurze Dateinamen (8,3) auf nicht-System physikalischen Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-123">**Workaround:** Enable short file name (8.3) support on non-system physical drives.</span></span> <span data-ttu-id="7cbb1-124">Sie können den folgenden Befehl verwenden, um eine kurze Dateinamen Unterstützung unter Windows 8 oder Windows Server 2012 zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-124">You can use the following command to enable short file name support on Windows 8 or Windows Server 2012.</span></span>

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

<span data-ttu-id="7cbb1-125">Verwenden Sie beispielsweise den folgenden Befehl, wenn der Laufwerkbuchstabe "Q:" lautet:</span><span class="sxs-lookup"><span data-stu-id="7cbb1-125">For example, use the following command if the drive letter is “Q:”:</span></span>

``` syntax
fsutil 8dot3name set Q: 0
```

<span data-ttu-id="7cbb1-126">**Hinweis**  Sie müssen diese Einstellung auf dem App-v-Client nicht ändern, da das App-v-Dateisystem in Windows 8 oder Windows Server 2012 kurze Pfade richtig verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-126">**Note** You do not need to change this setting on the App-V client because the App-V file system properly handles short paths on Windows 8 or Windows Server 2012.</span></span>

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> <span data-ttu-id="7cbb1-127">App-V überschreibt den Standardhandler für Dateityp-oder Protokollzuordnungen unter Windows 8 nicht</span><span class="sxs-lookup"><span data-stu-id="7cbb1-127">App-V does not override the default handler for file type or protocol associations on Windows 8</span></span>

<span data-ttu-id="7cbb1-128">Wenn Sie mithilfe von **Standardprogrammen** in der **System** Steuerung unter Windows 8 eine Standardanwendung auswählen, werden die zugeordneten Dateitypzuordnungen für diese Anwendung nicht von App-V überschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-128">If you select a default application by using **Default Programs** in **Control Panel** on Windows 8, App-V will not override the associated file type associations for that application.</span></span>

<span data-ttu-id="7cbb1-129">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-129">**Workaround:** None.</span></span>

### <span data-ttu-id="7cbb1-130">Virtualisierte Outlook 2010 wird nicht als Option für mailto-klickable-Links unter Windows 8 angeboten</span><span class="sxs-lookup"><span data-stu-id="7cbb1-130">Virtualized Outlook 2010 is not offered as an option for mailto clickable links on Windows 8</span></span>

<span data-ttu-id="7cbb1-131">Die mailto-Shell-Erweiterung bietet keine virtualisierten Outlook 2010 unter Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-131">The mailto shell extension does not offer virtualized Outlook 2010 on Windows 8.</span></span> <span data-ttu-id="7cbb1-132">Wenn Sie beispielsweise auf eine mailto:-Verknüpfung von virtualisierten Outlook 2010 klicken, die unter Windows 8 ausgeführt wird, wird kein neues e-Mail-Fenster erstellt.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-132">For example, if you click a mailto: link from virtualized Outlook 2010 that is running on Windows 8, a new email window is not created.</span></span> <span data-ttu-id="7cbb1-133">Diese Option funktioniert unter Windows 7 und früheren Versionen des Windows-Betriebssystems ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-133">This option works correctly on Windows 7 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="7cbb1-134">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-134">**Workaround:** None.</span></span>

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> <span data-ttu-id="7cbb1-135">Application Virtualization 4,6 SP2-Update wird nicht in allen Gebietsschemas angeboten, die Microsoft Update verwenden</span><span class="sxs-lookup"><span data-stu-id="7cbb1-135">Application Virtualization 4.6 SP2 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="7cbb1-136">Wenn Sie Microsoft Update verwenden, steht das Update für App-v 4.6 SP2 für die folgenden Sprachgebietsschemas nicht zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="7cbb1-136">When you use Microsoft Update, the update for App-V4.6SP2 is not available for the following language locales:</span></span>

-   <span data-ttu-id="7cbb1-137">Kasachisch</span><span class="sxs-lookup"><span data-stu-id="7cbb1-137">Kazakh</span></span>

-   <span data-ttu-id="7cbb1-138">Hindi</span><span class="sxs-lookup"><span data-stu-id="7cbb1-138">Hindi</span></span>

-   <span data-ttu-id="7cbb1-139">Serbisch-Kyrillisch</span><span class="sxs-lookup"><span data-stu-id="7cbb1-139">Serbian-Cyrillic</span></span>

<span data-ttu-id="7cbb1-140">**Problemumgehung:** Wenn Sie Microsoft Windows Server Update Services (WSUS) verwenden, verwenden Sie die englische Version des Updates, oder laden Sie das Update aus dem Microsoft Update-Katalog herunter.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-140">**Workaround:** If you are using Microsoft Windows Server Update Services (WSUS), use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

## <span data-ttu-id="7cbb1-141">Anmerkungen zu dieser Version Copyright-Informationen</span><span class="sxs-lookup"><span data-stu-id="7cbb1-141">Release Notes Copyright Information</span></span>


<span data-ttu-id="7cbb1-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="7cbb1-143">Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-143">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="7cbb1-144">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7cbb1-144">Related topics</span></span>


[<span data-ttu-id="7cbb1-145">Informationen zu Microsoft Application Virtualization 4.6SP2</span><span class="sxs-lookup"><span data-stu-id="7cbb1-145">About Microsoft Application Virtualization 4.6 SP2</span></span>](about-microsoft-application-virtualization-46-sp2.md)

 

 





