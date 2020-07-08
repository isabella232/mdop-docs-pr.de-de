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
# So führen Sie das Branding für das Self-Service-Portal durch


Nachdem Sie das Self-Service-Portal für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) installiert haben, können Sie das Self-Service-Portal mit dem Namen Ihres Unternehmens, der Helpdesk-URL und dem Text "Notice" versehen. Sie können auch die Einstellung Sitzungs Timeout ändern, damit die Sitzung des Endbenutzers nach einem bestimmten Zeitraum der Inaktivität abläuft.

**So richten Sie das Sitzungstimeout und das Branding für das Self-Service-Portal ein**

1.  Wenn Sie den Timeoutzeitraum für die Sitzung des Endbenutzers festzulegen möchten, starten Sie den **Internet Informationsdienste-Manager**, oder führen Sie **inetmgr.exe**aus.

2.  Navigieren Sie zu **Websites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung** &gt; **Selfservice** &gt; **ASP.net** - &gt; **Sitzungszustand**, und ändern Sie den **Timeout** Wert unter **Cookieeinstellungen** auf die Anzahl der Minuten, nach denen die Self-Service-Portal Sitzung des Endbenutzers abläuft. Der Standardwert beträgt5. Um die Einstellung so zu deaktivieren, dass kein Timeout vorhanden ist, legen Sie den Wert auf **0**fest.

3.  Wenn Sie die Branding-Elemente für das Self-Service-Portal einrichten möchten, starten Sie den **Internet Informationsdienste-Manager**, oder führen Sie **inetmgr.exe**aus.

4.  Navigieren Sie zu **Websites** &gt; **Microsoft BitLocker-Verwaltungs-und Überwachungs** &gt; **Selfservice** - &gt; **Anwendungseinstellungen**.

5.  Wählen Sie in der Spalte **Name** das Element aus, das Sie ändern möchten, und ändern Sie den Standardwert entsprechend dem Namen, den Sie verwenden möchten. In der folgenden Tabelle sind die Werte aufgeführt, die Sie festgelegt haben.

    **Achtung**  
    Ändern Sie den Wert in der Spalte Name (CompanyName \ *) nicht, da dadurch das Self-Service-Portal nicht mehr funktioniert.



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



## Verwandte Themen


[Bereitstellen der Serverinfrastruktur von MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









