---
title: So lokalisieren Sie „HelpdeskURL“ für das Self-Service-Portal
description: So lokalisieren Sie „HelpdeskURL“ für das Self-Service-Portal
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811917"
---
# <span data-ttu-id="27995-103">So lokalisieren Sie „HelpdeskURL“ für das Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="27995-103">How to Localize the Self-Service Portal “HelpdeskURL”</span></span>


<span data-ttu-id="27995-104">Sie können eine lokalisierte Version der Self-Service-Portal-URL so konfigurieren, dass Sie Endbenutzern standardmäßig angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="27995-104">You can configure a localized version of the Self-Service Portal URL to display to end users by default.</span></span> <span data-ttu-id="27995-105">Die URL des Self-Service-Portals wird durch den Parameter **HelpdeskURL**dargestellt.</span><span class="sxs-lookup"><span data-stu-id="27995-105">The Self-Service Portal URL is represented by the parameter **HelpdeskURL**.</span></span>

<span data-ttu-id="27995-106">Wenn Sie eine lokalisierte Version erstellen, wie in den folgenden Anleitungen beschrieben, findet und zeigt die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) die lokalisierte Version an.</span><span class="sxs-lookup"><span data-stu-id="27995-106">If you create a localized version, as described in the following instructions, Microsoft BitLocker Administration and Monitoring (MBAM) finds and displays the localized version.</span></span> <span data-ttu-id="27995-107">Wenn MBAM keine lokalisierte Version findet, wird die für den Parameter **HelpDeskURL**konfigurierte URL angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27995-107">If MBAM does not find a localized version, it displays the URL that is configured for the parameter **HelpDeskURL**.</span></span>

<span data-ttu-id="27995-108">**Hinweis**  In den folgenden Anleitungen ist *Selfservice* der Standardname für das virtuelle Verzeichnis für das Self-Service-Portal.</span><span class="sxs-lookup"><span data-stu-id="27995-108">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="27995-109">Wenn Sie das Self-Service-Portal konfiguriert haben, haben Sie möglicherweise einen anderen Namen verwendet.</span><span class="sxs-lookup"><span data-stu-id="27995-109">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="27995-110">So lokalisieren Sie die Self-Service-Portal-URL</span><span class="sxs-lookup"><span data-stu-id="27995-110">To localize the Self-Service Portal URL</span></span>**

1.  <span data-ttu-id="27995-111">Navigieren Sie auf dem Server, auf dem Sie das Self-Service-Portal konfiguriert haben, zu **Websites** &gt; **Microsoft BitLocker-Verwaltung und überwachen** von &gt; **Selfservice** - &gt; **Anwendungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="27995-111">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="27995-112">Klicken Sie im Bereich **Aktionen** auf **Hinzufügen** , um das Dialogfeld **Anwendungseinstellung hinzufügen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="27995-112">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="27995-113">Geben Sie im Feld **Name den Namen** **HelpdeskURL**\ _ &lt; *Language*ein &gt; , wobei &lt; *Sprache* &gt; der geeignete Sprachcode für die URL ist.</span><span class="sxs-lookup"><span data-stu-id="27995-113">In the **Name** field, type **HelpdeskURL**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the URL.</span></span>

    <span data-ttu-id="27995-114">Wenn Sie beispielsweise eine lokalisierte Version des `HelpdeskURL` Werts in Spanisch erstellen möchten, benennen Sie den Parameter **HelpdeskURL \ _ES-es**.</span><span class="sxs-lookup"><span data-stu-id="27995-114">For example, to create a localized version of the `HelpdeskURL` value in Spanish, name the parameter **HelpdeskURL\_es-es**.</span></span>

    <span data-ttu-id="27995-115">Der Name des Sprach Ordners kann auch der sprachneutrale Name **es** anstelle von **es-es**sein.</span><span class="sxs-lookup"><span data-stu-id="27995-115">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="27995-116">Wenn der Browser des Endbenutzers auf **es-es** festgelegt ist und dieser Ordner nicht vorhanden ist, wird das übergeordnete Gebietsschema (wie in .net definiert) rekursiv abgerufen und überprüft, und es wird in &lt; MBAM Self-Service-Installationsverzeichnis &gt;\\SelfServiceWebsite\\es\\Notice.txt, bevor es endgültig zur Standard Notice.txt Datei wird.</span><span class="sxs-lookup"><span data-stu-id="27995-116">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="27995-117">Dieser rekursiven Fallback imitiert die Load-Regeln für .NET-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="27995-117">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="27995-118">Eine Liste der gültigen Sprachcodes, die Sie verwenden können, finden Sie unter [National Language Support (NLS)-API-Referenz](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="27995-118">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="27995-119">Geben Sie im Feld **Wert** die lokalisierte Version des Werts ein, der `HelpdeskURL` Endbenutzern angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="27995-119">In the **Value** field, type the localized version of the `HelpdeskURL` value that you want to display to end users.</span></span>



## <span data-ttu-id="27995-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="27995-120">Related topics</span></span>


[<span data-ttu-id="27995-121">Anpassen des Self-Service-Portals für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="27995-121">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 
## <span data-ttu-id="27995-122">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="27995-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="27995-123">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="27995-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="27995-124">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="27995-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




