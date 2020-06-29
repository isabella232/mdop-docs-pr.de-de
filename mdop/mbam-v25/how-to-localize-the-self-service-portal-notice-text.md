---
title: So lokalisieren Sie den Hinweistext für das Self-Service-Portal
description: So lokalisieren Sie den Hinweistext für das Self-Service-Portal
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811920"
---
# <span data-ttu-id="baceb-103">So lokalisieren Sie den Hinweistext für das Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="baceb-103">How to Localize the Self-Service Portal Notice Text</span></span>


<span data-ttu-id="baceb-104">Sie können lokalisierten Benachrichtigungstext so konfigurieren, dass er für Endbenutzer standardmäßig im Self-Service-Portal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="baceb-104">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="baceb-105">Die Notice.txt-Datei, die den Hinweistext anzeigt, befindet sich im folgenden Stammverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="baceb-105">The Notice.txt file that displays the notice text is in the following root directory:</span></span>

<span data-ttu-id="baceb-106">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website</span><span class="sxs-lookup"><span data-stu-id="baceb-106">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="baceb-107">Wenn Sie lokalisierten Hinweistext anzeigen möchten, erstellen Sie eine lokalisierte Notice.txt Datei, und speichern Sie Sie dann unter einem bestimmten Sprachordner im folgenden Beispielverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="baceb-107">To display localized notice text, you create a localized Notice.txt file, and then save it under a specific language folder in the following example directory:</span></span>

<span data-ttu-id="baceb-108">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website</span><span class="sxs-lookup"><span data-stu-id="baceb-108">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="baceb-109">**Hinweis**  Sie können den Pfad mithilfe des **NoticeTextPath** -Elements in den **Anwendungseinstellungen**konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="baceb-109">**Note** You can configure the path by using the **NoticeTextPath** item in **Application Settings**.</span></span>

 

<span data-ttu-id="baceb-110">MBAM zeigt den Hinweistext auf der Grundlage der folgenden Regeln an:</span><span class="sxs-lookup"><span data-stu-id="baceb-110">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="baceb-111">Wenn Sie eine lokalisierte **Notice.txt** Datei im entsprechenden Sprachordner erstellen, zeigt MBAM den lokalisierten Hinweistext an, wenn die Standard **Notice.txt** Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="baceb-111">If you create a localized **Notice.txt** file in the appropriate language folder, MBAM displays the localized notice text if the default **Notice.txt** file exists.</span></span> <span data-ttu-id="baceb-112">Wenn die Standard **Notice.txt** Datei fehlt, wird eine Meldung angezeigt, die besagt, dass die Standarddatei nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="baceb-112">If the default **Notice.txt** file is missing, a message displays indicating that the default file is missing.</span></span>

-   <span data-ttu-id="baceb-113">Wenn MBAM keine lokalisierte Version der Notice.txt-Datei findet, wird der Text in der standardmäßigen Notice.txt Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="baceb-113">If MBAM does not find a localized version of the Notice.txt file, it displays the text in the default Notice.txt file.</span></span>

-   <span data-ttu-id="baceb-114">Wenn MBAM keine Standard Notice.txt Datei findet, wird der Standardtext im Self-Service-Portal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="baceb-114">If MBAM does not find a default Notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

<span data-ttu-id="baceb-115">**Hinweis**  Wenn der Browser eines Endbenutzers auf eine Sprache festgesetzt ist, die keinen entsprechenden Unterordner "Sprache" oder Notice.txt hat, wird der Text in der Notice.txt Datei im folgenden Stammverzeichnis angezeigt:</span><span class="sxs-lookup"><span data-stu-id="baceb-115">**Note** If an end user’s browser is set to a language that does not have a corresponding language subfolder or Notice.txt, the text in the Notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="baceb-116">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website</span><span class="sxs-lookup"><span data-stu-id="baceb-116">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

 

**<span data-ttu-id="baceb-117">So erstellen Sie eine lokalisierte Notice.txt-Datei</span><span class="sxs-lookup"><span data-stu-id="baceb-117">To create a localized Notice.txt file</span></span>**

1.  <span data-ttu-id="baceb-118">Erstellen Sie auf dem Server, auf dem Sie das Self-Service-Portal konfiguriert haben, einen &lt; *sprach* &gt; Ordner im folgenden Beispielverzeichnis, wobei &lt; *Sprache* &gt; den Namen der lokalisierten Sprache darstellt:</span><span class="sxs-lookup"><span data-stu-id="baceb-118">On the server where you configured the Self-Service Portal, create a &lt;*Language*&gt; folder in the following example directory, where &lt;*Language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="baceb-119">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website</span><span class="sxs-lookup"><span data-stu-id="baceb-119">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

    <span data-ttu-id="baceb-120">**Hinweis**  Da einige Sprachordner bereits vorhanden sind, müssen Sie möglicherweise keinen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="baceb-120">**Note** Some language folders already exist, so you might not have to create a folder.</span></span> <span data-ttu-id="baceb-121">Wenn Sie einen Sprachordner erstellen müssen, finden Sie unter [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) eine Liste der gültigen Namen, die Sie für den &lt; *sprach* &gt; Ordner verwenden können.</span><span class="sxs-lookup"><span data-stu-id="baceb-121">If you do have to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*Language*&gt; folder.</span></span>

     

2.  <span data-ttu-id="baceb-122">Erstellen Sie eine Notice.txt-Datei, die den lokalisierten Benachrichtigungstext enthält.</span><span class="sxs-lookup"><span data-stu-id="baceb-122">Create a Notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="baceb-123">Speichern Sie die Notice.txt Datei im &lt; Ordner *Sprache* &gt; .</span><span class="sxs-lookup"><span data-stu-id="baceb-123">Save the Notice.txt file in the &lt;*Language*&gt; folder.</span></span> <span data-ttu-id="baceb-124">Wenn Sie beispielsweise eine lokalisierte Notice.txt Datei in Spanisch erstellen möchten, speichern Sie die lokalisierte Notice.txt Datei im folgenden Beispielverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="baceb-124">For example, to create a localized Notice.txt file in Spanish, save the localized Notice.txt file in the following example directory:</span></span>

    <span data-ttu-id="baceb-125">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\Es-es</span><span class="sxs-lookup"><span data-stu-id="baceb-125">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\Es-es</span></span>

    <span data-ttu-id="baceb-126">Der Name des Sprach Ordners kann auch der sprachneutrale Name **es** anstelle von **es-es**sein.</span><span class="sxs-lookup"><span data-stu-id="baceb-126">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="baceb-127">Wenn der Browser des Endbenutzers auf **es-es** festgelegt ist und dieser Ordner nicht vorhanden ist, wird das übergeordnete Gebietsschema (wie in .net definiert) rekursiv abgerufen und überprüft, und es wird in &lt; MBAM Self-Service-Installationsverzeichnis &gt;\\SelfServiceWebsite\\es\\Notice.txt, bevor es endgültig zur Standard Notice.txt Datei wird.</span><span class="sxs-lookup"><span data-stu-id="baceb-127">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="baceb-128">Dieser rekursiven Fallback imitiert die Load-Regeln für .NET-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="baceb-128">This recursive fallback mimics the .NET resource loading rules.</span></span>



## <span data-ttu-id="baceb-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="baceb-129">Related topics</span></span>


[<span data-ttu-id="baceb-130">Anpassen des Self-Service-Portals für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="baceb-130">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

## <span data-ttu-id="baceb-131">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="baceb-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="baceb-132">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="baceb-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="baceb-133">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="baceb-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





