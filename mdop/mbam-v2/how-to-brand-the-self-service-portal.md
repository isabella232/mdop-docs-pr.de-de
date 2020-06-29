---
title: So führen Sie das Branding für das Self-Service-Portal durch
description: So führen Sie das Branding für das Self-Service-Portal durch
author: dansimp
ms.assetid: 3ef9e951-7c42-4f7f-b131-3765d39b3207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe4f4efc5852042671711ba5780cc78055957ba8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810981"
---
# <span data-ttu-id="b5a92-103">So führen Sie das Branding für das Self-Service-Portal durch</span><span class="sxs-lookup"><span data-stu-id="b5a92-103">How to Brand the Self-Service Portal</span></span>


<span data-ttu-id="b5a92-104">Nachdem Sie das Self-Service-Portal für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) installiert haben, können Sie das Self-Service-Portal mit dem Namen Ihres Unternehmens, der Helpdesk-URL und dem Text "Notice" versehen.</span><span class="sxs-lookup"><span data-stu-id="b5a92-104">After you install the Microsoft BitLocker Administration and Monitoring (MBAM) Self-Service Portal, you can brand the Self-Service Portal with your company name, Help Desk URL, and “notice” text.</span></span> <span data-ttu-id="b5a92-105">Sie können auch die Einstellung Sitzungs Timeout ändern, damit die Sitzung des Endbenutzers nach einem bestimmten Zeitraum der Inaktivität abläuft.</span><span class="sxs-lookup"><span data-stu-id="b5a92-105">You can also change the Session Timeout setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="b5a92-106">So richten Sie das Sitzungstimeout und das Branding für das Self-Service-Portal ein</span><span class="sxs-lookup"><span data-stu-id="b5a92-106">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="b5a92-107">Wenn Sie den Timeoutzeitraum für die Sitzung des Endbenutzers festzulegen möchten, starten Sie den **Internet Informationsdienste-Manager**, oder führen Sie **inetmgr.exe**aus.</span><span class="sxs-lookup"><span data-stu-id="b5a92-107">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="b5a92-108">Navigieren Sie zu **Websites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung** &gt; **Selfservice** &gt; **ASP.net** - &gt; **Sitzungszustand**, und ändern Sie den **Timeout** Wert unter **Cookieeinstellungen** auf die Anzahl der Minuten, nach denen die Self-Service-Portal Sitzung des Endbenutzers abläuft.</span><span class="sxs-lookup"><span data-stu-id="b5a92-108">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session will expire.</span></span> <span data-ttu-id="b5a92-109">Der Standardwert beträgt5.</span><span class="sxs-lookup"><span data-stu-id="b5a92-109">The default is 5.</span></span> <span data-ttu-id="b5a92-110">Um die Einstellung so zu deaktivieren, dass kein Timeout vorhanden ist, legen Sie den Wert auf **0**fest.</span><span class="sxs-lookup"><span data-stu-id="b5a92-110">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="b5a92-111">Wenn Sie die Branding-Elemente für das Self-Service-Portal einrichten möchten, starten Sie den **Internet Informationsdienste-Manager**, oder führen Sie **inetmgr.exe**aus.</span><span class="sxs-lookup"><span data-stu-id="b5a92-111">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="b5a92-112">Navigieren Sie zu **Websites** &gt; **Microsoft BitLocker-Verwaltungs-und Überwachungs** &gt; **Selfservice** - &gt; **Anwendungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="b5a92-112">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="b5a92-113">Wählen Sie in der Spalte **Name** das Element aus, das Sie ändern möchten, und ändern Sie den Standardwert entsprechend dem Namen, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b5a92-113">From the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="b5a92-114">In der folgenden Tabelle sind die Werte aufgeführt, die Sie festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="b5a92-114">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="b5a92-115">Achtung</span><span class="sxs-lookup"><span data-stu-id="b5a92-115">Caution</span></span>**  
    <span data-ttu-id="b5a92-116">Ändern Sie den Wert in der Spalte Name (CompanyName \ \*) nicht, da dadurch das Self-Service-Portal nicht mehr funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b5a92-116">Do not change the value in the Name column (CompanyName\*), as it will cause the Self-Service Portal to stop working.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CompanyName*</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText*</p></td>
<td align="left"><p>Contact Help Desk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl*</p></td>
<td align="left"><p>Http://www.microsoft.com</p></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.2.min.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MicrosoftAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/3.5/MicrosoftAjax.js</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftMvcAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/mvc/2.0/MicrosoftMvcValidation.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the Notice text either by using the IIS Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>
~~~



## <span data-ttu-id="b5a92-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b5a92-117">Related topics</span></span>


[<span data-ttu-id="b5a92-118">Bereitstellen der Serverinfrastruktur von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b5a92-118">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









