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
# So legen Sie das Brandings für das Self-Service-Portal und Sitzungszeitlimits fest


Nachdem Sie das Self-Service-Portal konfiguriert haben, können Sie es mit dem Namen Ihres Unternehmens, der Helpdesk-URL und dem Text "Notice" versehen. Sie können auch die Einstellung Sitzungstimeout ändern, damit die Sitzung des Endbenutzers nach einem bestimmten Zeitraum der Inaktivität abläuft.

**Hinweis:**  
Sie können das Self-Service-Portal auch mithilfe des Windows PowerShell-Cmdlets **enable-MbamWebApplication** oder des MBAM-Serverkonfigurations-Assistenten Marken. Anweisungen zur Verwendung des Assistenten finden Sie unter [Konfigurieren der MBAM 2,5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md).



**Hinweis:**  
In den folgenden Anleitungen ist *Selfservice* der Standardname für das virtuelle Verzeichnis für das Self-Service-Portal. Wenn Sie das Self-Service-Portal konfiguriert haben, haben Sie möglicherweise einen anderen Namen verwendet.



**So richten Sie das Sitzungstimeout und das Branding für das Self-Service-Portal ein**

1.  Wenn Sie den Timeoutzeitraum für die Sitzung des Endbenutzers festzulegen möchten, starten Sie den **Internet Informationsdienste-Manager**, oder führen Sie **inetmgr.exe**aus.

2.  Navigieren Sie zu **Websites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung** &gt; **Selfservice** &gt; **ASP.net** - &gt; **Sitzungszustand**, und ändern Sie den **Timeout** Wert unter **Cookieeinstellungen** auf die Anzahl der Minuten, nach denen die Self-Service-Portal Sitzung des Endbenutzers abläuft. Der Standardwert ist " **5**". Um die Einstellung so zu deaktivieren, dass kein Timeout vorhanden ist, legen Sie den Wert auf **0**fest.

3.  Wenn Sie die Branding-Elemente für das Self-Service-Portal einrichten möchten, starten Sie den **Internet Informationsdienste-Manager** , oder führen Sie **inetmgr.exe**aus.

4.  Navigieren Sie zu **Websites** &gt; **Microsoft BitLocker-Verwaltungs-und Überwachungs** &gt; **Selfservice** - &gt; **Anwendungseinstellungen**.

5.  Wählen Sie in der Spalte **Name** das Element aus, das Sie ändern möchten, und ändern Sie den Standardwert entsprechend dem Namen, den Sie verwenden möchten. In der folgenden Tabelle sind die Werte aufgeführt, die Sie festgelegt haben.

    **Achtung**  
    Ändern Sie den Wert in der Spalte Name (CompanyName \ *) nicht, da das Self-Service-Portal nicht mehr funktioniert.



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





## Verwandte Themen


[Anpassen des Self-Service-Portals für Ihre Organisation](customizing-the-self-service-portal-for-your-organization.md)



## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





