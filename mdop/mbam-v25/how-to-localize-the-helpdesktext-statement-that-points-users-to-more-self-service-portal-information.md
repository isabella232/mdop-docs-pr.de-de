---
title: So lokalisieren Sie die HelpdeskText-Anweisung, mit der Benutzer auf weitere Informationen zum Self-Service-Portal verwiesen werden
description: So lokalisieren Sie die HelpdeskText-Anweisung, mit der Benutzer auf weitere Informationen zum Self-Service-Portal verwiesen werden
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809946"
---
# <span data-ttu-id="c840d-103">So lokalisieren Sie die HelpdeskText-Anweisung, mit der Benutzer auf weitere Informationen zum Self-Service-Portal verwiesen werden</span><span class="sxs-lookup"><span data-stu-id="c840d-103">How to Localize the “HelpdeskText” Statement that Points Users to More Self-Service Portal Information</span></span>


<span data-ttu-id="c840d-104">Sie können eine lokalisierte Version der Self-Service-Portal-"HelpdeskText"-Anweisung konfigurieren, die Endbenutzer darüber informiert, wie Sie bei Verwendung des Self-Service-Portals zusätzliche Hilfe erhalten.</span><span class="sxs-lookup"><span data-stu-id="c840d-104">You can configure a localized version of the Self-Service Portal "HelpdeskText" statement, which informs end users about how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="c840d-105">Wenn Sie lokalisierten Text für die Anweisung konfigurieren, wie in den folgenden Anleitungen beschrieben, zeigt MBAM die lokalisierte Version an.</span><span class="sxs-lookup"><span data-stu-id="c840d-105">If you configure localized text for the statement, as described in the following instructions, MBAM displays the localized version.</span></span> <span data-ttu-id="c840d-106">Wenn MBAM die lokalisierte Version nicht findet, wird der Wert im **HelpdeskText** -Parameter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c840d-106">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

<span data-ttu-id="c840d-107">**Hinweis**  In den folgenden Anleitungen ist *Selfservice* der Standardname für das virtuelle Verzeichnis für das Self-Service-Portal.</span><span class="sxs-lookup"><span data-stu-id="c840d-107">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="c840d-108">Wenn Sie das Self-Service-Portal konfiguriert haben, haben Sie möglicherweise einen anderen Namen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c840d-108">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="c840d-109">So zeigen Sie eine lokalisierte Version der HelpdeskText-Anweisung an</span><span class="sxs-lookup"><span data-stu-id="c840d-109">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="c840d-110">Navigieren Sie auf dem Server, auf dem Sie das Self-Service-Portal konfiguriert haben, zu **Websites** &gt; **Microsoft BitLocker-Verwaltung und überwachen** von &gt; **Selfservice** - &gt; **Anwendungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="c840d-110">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="c840d-111">Klicken Sie im Bereich **Aktionen** auf **Hinzufügen** , um das Dialogfeld **Anwendungseinstellung hinzufügen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c840d-111">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="c840d-112">Geben Sie im Feld **Name den Namen** **HelpdeskText**\ _ &lt; *Language*ein &gt; , wobei &lt; *Sprache* &gt; der für den Text geeignete Sprachcode ist.</span><span class="sxs-lookup"><span data-stu-id="c840d-112">In the **Name** field, type **HelpdeskText**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the text.</span></span>

    <span data-ttu-id="c840d-113">Um beispielsweise eine lokalisierte HelpdeskText-Anweisung in Spanisch zu erstellen, benennen Sie den Parameter **HelpdeskText \ _ES-es**.</span><span class="sxs-lookup"><span data-stu-id="c840d-113">For example, to create a localized HelpdeskText statement in Spanish, name the parameter **HelpdeskText\_es-es**.</span></span>

    <span data-ttu-id="c840d-114">Der Name des Sprach Ordners kann auch der sprachneutrale Name **es** anstelle von **es-es**sein.</span><span class="sxs-lookup"><span data-stu-id="c840d-114">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="c840d-115">Wenn der Browser des Endbenutzers auf **es-es** festgelegt ist und dieser Ordner nicht vorhanden ist, wird das übergeordnete Gebietsschema (wie in .net definiert) rekursiv abgerufen und überprüft, und es wird in &lt; MBAM Self-Service-Installationsverzeichnis &gt;\\SelfServiceWebsite\\es\\Notice.txt, bevor es endgültig zur Standard Notice.txt Datei wird.</span><span class="sxs-lookup"><span data-stu-id="c840d-115">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="c840d-116">Dieser rekursiven Fallback imitiert die Load-Regeln für .NET-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c840d-116">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="c840d-117">Eine Liste der gültigen Sprachcodes, die Sie verwenden können, finden Sie unter [National Language Support (NLS)-API-Referenz](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="c840d-117">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="c840d-118">Geben Sie im Feld **Wert** den lokalisierten Text ein, der Endbenutzern angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c840d-118">In the **Value** field, type the localized text that you want to display to end users.</span></span>



## <span data-ttu-id="c840d-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c840d-119">Related topics</span></span>


[<span data-ttu-id="c840d-120">Anpassen des Self-Service-Portals für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="c840d-120">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 

## <span data-ttu-id="c840d-121">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="c840d-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c840d-122">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="c840d-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="c840d-123">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c840d-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



