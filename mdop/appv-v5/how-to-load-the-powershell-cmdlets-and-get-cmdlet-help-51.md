---
title: So laden Sie die PowerShell-Cmdlets und rufen die Cmdlet-Hilfe auf
description: So laden Sie die PowerShell-Cmdlets und rufen die Cmdlet-Hilfe auf
author: dansimp
ms.assetid: b6ae5460-2c3a-4030-b132-394d9d5a541e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 32b5bb26331f204acffbf96ea119ac4209c3cd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805360"
---
# So laden Sie die PowerShell-Cmdlets und rufen die Cmdlet-Hilfe auf


Inhalt dieses Themas:

-   [Voraussetzungen für die Verwendung von PowerShell-Cmdlets](#bkmk-reqs-using-posh)

-   [Laden der PowerShell-Cmdlets](#bkmk-load-cmdlets)

-   [Aufrufen von Hilfe zu den PowerShell-Cmdlets](#bkmk-get-cmdlet-help)

-   [Anzeigen der Hilfe zu einem PowerShell-Cmdlet](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a>Voraussetzungen für die Verwendung von PowerShell-Cmdlets


Überprüfen Sie die folgenden Voraussetzungen für die Verwendung der App-V PowerShell-Cmdlets:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Anforderung</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Benutzer können App-V Server-Cmdlets nur ausführen, wenn Sie Ihnen Zugriff gewähren, indem Sie eine der folgenden Methoden verwenden:</p></td>
<td align="left"><ul>
<li><p><strong>Wenn Sie den App-V-Server bereitstellen und konfigurieren </strong> :</p>
<p>Geben Sie eine Active Directory-Gruppe oder einen einzelnen Benutzer an, der über die Berechtigungen zum Verwalten der App-V-Umgebung verfügt. Hier erfahren Sie <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> , wie der App-V 5,1-Server bereitgestellt wird </a> .</p></li>
<li><p><strong>Nachdem Sie den App-V-Server bereitgestellt haben </strong> :</p>
<p>Verwenden Sie die App-V-Verwaltungskonsole, um eine zusätzliche Active Directory-Gruppe oder einen weiteren Benutzer hinzuzufügen. Informationen dazu finden Sie unter <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)"> Hinzufügen oder Entfernen eines Administrators mithilfe der Verwaltungskonsole </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cmdlets, die eine Eingabeaufforderung mit erhöhten Rechten erfordern</p></td>
<td align="left"><ul>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
<li><p>Satz-AppvClientConfiguration</p></li>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Remove-AppvClientConnectionGroup</p></li>
<li><p>Add-AppvPublishingServer</p></li>
<li><p>Remove-AppvPublishingServer</p></li>
<li><p>Senden-AppvClientReport</p></li>
<li><p>Satz-AppvClientMode</p></li>
<li><p>Satz-AppvClientPackage</p></li>
<li><p>Satz-AppvPublishingServer</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Cmdlets, die Endbenutzer ausführen können, es sei denn, Sie konfigurieren Sie so, dass eine Eingabeaufforderung mit erhöhten Rechten erforderlich ist</p></td>
<td align="left"><ul>
<li><p>Publish-AppvClientPackage</p></li>
<li><p>Veröffentlichung aufheben – AppvClientPackage</p></li>
</ul>
<p>Verwenden Sie eine der folgenden Methoden, um diese Cmdlets so zu konfigurieren, dass eine Eingabeaufforderung mit erhöhten Rechten erforderlich ist:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Weitere Ressourcen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Führen Sie das <strong> Cmdlet "Satz-AppvClientConfiguration </strong> " mit dem <strong> -RequirePublishAsAdmin- </strong> Parameter aus.</p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg)">So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell</a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">So verwalten Sie App-V 5.1-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Aktivieren Sie die Gruppenrichtlinieneinstellung "als Administrator veröffentlichen" für App-V-Clients.</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-51.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md)">So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a>Laden der PowerShell-Cmdlets

So laden Sie die PowerShell-Cmdlet-Module:

1.  Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).

2.  Geben Sie einen der folgenden Befehle ein, um die Cmdlets für das gewünschte Modul zu laden:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V-Komponente</th>
<th align="left">Befehl zum eingeben</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V-Server</p></td>
<td align="left"><p>Import-Modul AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V-Sequenzer</p></td>
<td align="left"><p>Import-Modul AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V-Client</p></td>
<td align="left"><p>Import-Modul AppvClient</p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-get-cmdlet-help"></a>Aufrufen von Hilfe zu den PowerShell-Cmdlets
Ab App-V 5,0 SP3 steht die Hilfe für das Cmdlet in zwei Formaten zur Verfügung:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Format</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Als herunterladbares Modul</p></td>
<td align="left"><p>So laden Sie die neueste Hilfe herunter, nachdem Sie das Cmdlet-Modul heruntergeladen haben:</p>
<ol>
<li><p>Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).</p></li>
<li><p>Geben Sie einen der folgenden Befehle ein, um die Cmdlets für das gewünschte Modul zu laden:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V-Komponente</th>
<th align="left">Befehl zum eingeben</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V-Server</p></td>
<td align="left"><p>Update-Hilfe-Modul AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V-Sequenzer</p></td>
<td align="left"><p>Update-Hilfe-Modul AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V-Client</p></td>
<td align="left"><p>Update-Hilfe-Modul AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Auf TechNet als Web-Seiten</p></td>
<td align="left"><p>Weitere Informationen finden Sie unter App-V-Knoten unter <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Microsoft Desktop Optimization Pack-Automatisierung mit Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-display-help-cmdlet"></a>Anzeigen der Hilfe zu einem PowerShell-Cmdlet
So zeigen Sie Hilfe zu einem bestimmten PowerShell-Cmdlet an:

1.  Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).

2.  Geben **Sie Get-Help-** &lt; *Cmdlet*ein &gt; , beispielsweise **Get-Help Publish-AppvClientPackage**.

Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





