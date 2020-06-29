---
title: So legen Sie das Brandings für das Self-Service-Portal und Sitzungszeitlimits fest
description: So legen Sie das Brandings für das Self-Service-Portal und Sitzungszeitlimits fest
author: dansimp
ms.assetid: 031eedfc-fade-4d2f-8771-b329e1d38c0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e222880b2d5557ef15cd7a4efd6421b9972541f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804298"
---
# <span data-ttu-id="0323c-103">So legen Sie das Brandings für das Self-Service-Portal und Sitzungszeitlimits fest</span><span class="sxs-lookup"><span data-stu-id="0323c-103">How to Set the Self-Service Portal Branding and Session Time-out</span></span>


<span data-ttu-id="0323c-104">Nachdem Sie das Self-Service-Portal konfiguriert haben, können Sie es mit dem Namen Ihres Unternehmens, der Helpdesk-URL und dem Text "Notice" versehen.</span><span class="sxs-lookup"><span data-stu-id="0323c-104">After you configure the Self-Service Portal, you can brand it with your company name, Help Desk URL, and "notice" text.</span></span> <span data-ttu-id="0323c-105">Sie können auch die Einstellung Sitzungstimeout ändern, damit die Sitzung des Endbenutzers nach einem bestimmten Zeitraum der Inaktivität abläuft.</span><span class="sxs-lookup"><span data-stu-id="0323c-105">You can also change the Session Time-out setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="0323c-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="0323c-106">Note</span></span>**  
<span data-ttu-id="0323c-107">Sie können das Self-Service-Portal auch mithilfe des Windows PowerShell-Cmdlets **enable-MbamWebApplication** oder des MBAM-Serverkonfigurations-Assistenten Marken.</span><span class="sxs-lookup"><span data-stu-id="0323c-107">You can also brand the Self-Service Portal by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="0323c-108">Anweisungen zur Verwendung des Assistenten finden Sie unter [Konfigurieren der MBAM 2,5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="0323c-108">For instructions on using the wizard, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>



**<span data-ttu-id="0323c-109">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="0323c-109">Note</span></span>**  
<span data-ttu-id="0323c-110">In den folgenden Anleitungen ist *Selfservice* der Standardname für das virtuelle Verzeichnis für das Self-Service-Portal.</span><span class="sxs-lookup"><span data-stu-id="0323c-110">In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="0323c-111">Wenn Sie das Self-Service-Portal konfiguriert haben, haben Sie möglicherweise einen anderen Namen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0323c-111">You might have used a different name when you configured the Self-Service Portal.</span></span>



**<span data-ttu-id="0323c-112">So richten Sie das Sitzungstimeout und das Branding für das Self-Service-Portal ein</span><span class="sxs-lookup"><span data-stu-id="0323c-112">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="0323c-113">Wenn Sie den Timeoutzeitraum für die Sitzung des Endbenutzers festzulegen möchten, starten Sie den **Internet Informationsdienste-Manager**, oder führen Sie **inetmgr.exe**aus.</span><span class="sxs-lookup"><span data-stu-id="0323c-113">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="0323c-114">Navigieren Sie zu **Websites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung** &gt; **Selfservice** &gt; **ASP.net** - &gt; **Sitzungszustand**, und ändern Sie den **Timeout** Wert unter **Cookieeinstellungen** auf die Anzahl der Minuten, nach denen die Self-Service-Portal Sitzung des Endbenutzers abläuft.</span><span class="sxs-lookup"><span data-stu-id="0323c-114">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session expires.</span></span> <span data-ttu-id="0323c-115">Der Standardwert ist " **5**".</span><span class="sxs-lookup"><span data-stu-id="0323c-115">The default value is **5**.</span></span> <span data-ttu-id="0323c-116">Um die Einstellung so zu deaktivieren, dass kein Timeout vorhanden ist, legen Sie den Wert auf **0**fest.</span><span class="sxs-lookup"><span data-stu-id="0323c-116">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="0323c-117">Wenn Sie die Branding-Elemente für das Self-Service-Portal einrichten möchten, starten Sie den **Internet Informationsdienste-Manager** , oder führen Sie **inetmgr.exe**aus.</span><span class="sxs-lookup"><span data-stu-id="0323c-117">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager** or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="0323c-118">Navigieren Sie zu **Websites** &gt; **Microsoft BitLocker-Verwaltungs-und Überwachungs** &gt; **Selfservice** - &gt; **Anwendungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="0323c-118">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="0323c-119">Wählen Sie in der Spalte **Name** das Element aus, das Sie ändern möchten, und ändern Sie den Standardwert entsprechend dem Namen, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="0323c-119">In the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="0323c-120">In der folgenden Tabelle sind die Werte aufgeführt, die Sie festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="0323c-120">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="0323c-121">Achtung</span><span class="sxs-lookup"><span data-stu-id="0323c-121">Caution</span></span>**  
    <span data-ttu-id="0323c-122">Ändern Sie den Wert in der Spalte Name (CompanyName \ \*) nicht, da das Self-Service-Portal nicht mehr funktioniert.</span><span class="sxs-lookup"><span data-stu-id="0323c-122">Do not change the value in the Name column (CompanyName\*), as it will cause Self-Service Portal to stop working.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ClientValidationEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>CompanyName</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DisplayNotice</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText</p></td>
<td align="left"><p>Contact Helpdesk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl</p></td>
<td align="left"><p>#</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, the HelpdeskUrl default value is empty.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390515](//go.microsoft.com/fwlink/?LinkID=390515)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery-1.10.2.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>jQueryValidatePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390516](//go.microsoft.com/fwlink/?LinkID=390516)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryValidateUnobtrusivePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390517](//go.microsoft.com/fwlink/?LinkID=390517)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.unobtrusive.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the notice text either by using the Internet Information Services (IIS) Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>UnobtrusiveJavaScriptEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
</tbody>
</table>
~~~





## <span data-ttu-id="0323c-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0323c-123">Related topics</span></span>


[<span data-ttu-id="0323c-124">Anpassen des Self-Service-Portals für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="0323c-124">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)



## <span data-ttu-id="0323c-125">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="0323c-125">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0323c-126">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="0323c-126">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0323c-127">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="0323c-127">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





