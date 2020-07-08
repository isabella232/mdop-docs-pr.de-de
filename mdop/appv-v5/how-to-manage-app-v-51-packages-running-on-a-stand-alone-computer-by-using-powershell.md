---
title: So verwalten Sie App-V 5.1-Pakete auf einem eigenständigen Computer mithilfe von PowerShell
description: So verwalten Sie App-V 5.1-Pakete auf einem eigenständigen Computer mithilfe von PowerShell
author: dansimp
ms.assetid: c3fd06f6-102f-43d1-a577-d5ced6ac537d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b454014da4e5f349af913d3fea8ea3837598a039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805336"
---
# So verwalten Sie App-V 5.1-Pakete auf einem eigenständigen Computer mithilfe von PowerShell


In den folgenden Abschnitten wird erläutert, wie verschiedene Verwaltungsaufgaben auf einem eigenständigen Clientcomputer mithilfe von PowerShell durchgeführt werden:

-   [So geben Sie eine Liste der Pakete zurück](#bkmk-return-pkgs-standalone-posh)

-   [So fügen Sie ein Paket hinzu](#bkmk-add-pkgs-standalone-posh)

-   [So veröffentlichen Sie ein Paket](#bkmk-pub-pkg-standalone-posh)

-   [So veröffentlichen Sie ein Paket für einen bestimmten Benutzer](#bkmk-pub-pkg-a-user-standalone-posh)

-   [So fügen Sie ein Paket hinzu und veröffentlichen es](#bkmk-add-pub-pkg-standalone-posh)

-   [So heben Sie die Veröffentlichung eines vorhandenen Pakets auf](#bkmk-unpub-pkg-standalone-posh)

-   [So heben Sie die Veröffentlichung eines Pakets für einen bestimmten Benutzer auf](#bkmk-unpub-pkg-specfc-use)

-   [So entfernen Sie ein vorhandenes Paket](#bkmk-remove-pkg-standalone-posh)

-   [So aktivieren Sie nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen](#bkmk-admins-pub-pkgs)

-   [Grundlegendes zu ausstehenden Paketen (UserPending und GlobalPending)](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a>So geben Sie eine Liste der Pakete zurück


Verwenden Sie die folgenden Informationen, um eine Liste der Pakete zurückzugeben, die für einen bestimmten Benutzer berechtigt sind:

**Cmdlet**: Get-AppvClientPackage

**Parameter**:-Name-Version-Package-Version-Version-Nr.

**Beispiel**: Get-AppvClientPackage – Name "ContosoApplication" – Version 2

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a>So fügen Sie ein Paket hinzu


Verwenden Sie die folgenden Informationen, um einem Computer ein Paket hinzuzufügen.

**Wichtig**  In diesem Beispiel wird nur ein Paket hinzugefügt. Das Paket wird nicht für den Benutzer oder den Computer veröffentlicht.

 

**Cmdlet**: Add-AppvClientPackage

**Beispiel**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a>So veröffentlichen Sie ein Paket


Verwenden Sie die folgenden Informationen, um ein Paket zu veröffentlichen, das einem bestimmten Benutzer oder Global einem beliebigen Benutzer auf dem Computer hinzugefügt wurde.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Veröffentlichungsmethode</th>
<th align="left">Cmdlet und Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Veröffentlichen für den Benutzer</p></td>
<td align="left"><p><strong>Cmdlet </strong> : Publish-AppvClientPackage</p>
<p><strong>Beispiel </strong> : Publish-AppvClientPackage "ContosoApplication"</p></td>
</tr>
<tr class="even">
<td align="left"><p>Global publizieren</p></td>
<td align="left"><p><strong>Cmdlet </strong> : Publish-AppvClientPackage</p>
<p><strong>Beispiel </strong> : Publish-AppvClientPackage "ContosoApplication" – Global</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a>So veröffentlichen Sie ein Paket für einen bestimmten Benutzer


**Hinweis**  Sie müssen App-V 5,0 SP2-Hotfix-Paket 5 oder höher verwenden, um diesen Parameter zu verwenden.

 

Ein Administrator kann ein Paket für einen bestimmten Benutzer veröffentlichen, indem er den optionalen **– Users** -Parameter mit dem Cmdlet **Publish-AppvClientPackage** angibt, wobei **-Benutzer-** ID die Sicherheits-ID (SID) des Endbenutzers darstellt.

So verwenden Sie diesen Parameter:

-   Sie können dieses Cmdlet in der Benutzer-oder Administrator Sitzung ausführen.

-   Sie müssen mit administrativen Anmeldeinformationen angemeldet sein, um den Parameter verwenden zu können.

-   Der Endbenutzer muss angemeldet sein.

-   Sie müssen die Sicherheits-ID (Security Identifier, SID) des Endbenutzers angeben.

**Cmdlet**: Publish-AppvClientPackage

**Beispiel**: Publish-AppvClientPackage "ContosoApplication"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a>So fügen Sie ein Paket hinzu und veröffentlichen es


Verwenden Sie die folgenden Informationen zum Hinzufügen eines Pakets zu einem Computer, und veröffentlichen Sie es für den Benutzer.

**Cmdlet**: Add-AppvClientPackage

**Beispiel**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publish-AppvClientPackage

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a>So heben Sie die Veröffentlichung eines vorhandenen Pakets auf


Verwenden Sie die folgenden Informationen zum Aufheben der Veröffentlichung eines Pakets, das für einen Benutzer berechtigt ist, das Paket aber nicht vom Computer entfernt wurde.

**Cmdlet**: Unpublish-AppvClientPackage

**Beispiel**: Unpublish-AppvClientPackage "ContosoApplication"

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a>So heben Sie die Veröffentlichung eines Pakets für einen bestimmten Benutzer auf


**Hinweis**  Sie müssen App-V 5,0 SP2-Hotfix-Paket 5 oder höher verwenden, um diesen Parameter zu verwenden.

 

Ein Administrator kann die Veröffentlichung eines Pakets für einen bestimmten Benutzer mit dem optionalen **– Users** -Parameter mit dem Cmdlet " **UNPUBLISH-AppvClientPackage** " aufheben, wobei **-Benutzer-** ID die Sicherheits-ID (SID) des Endbenutzers darstellt.

So verwenden Sie diesen Parameter:

-   Sie können dieses Cmdlet in der Benutzer-oder Administrator Sitzung ausführen.

-   Sie müssen mit administrativen Anmeldeinformationen angemeldet sein, um den Parameter verwenden zu können.

-   Der Endbenutzer muss angemeldet sein.

-   Sie müssen die Sicherheits-ID (Security Identifier, SID) des Endbenutzers angeben.

**Cmdlet**: Unpublish-AppvClientPackage

**Beispiel**: Unpublish-AppvClientPackage "ContosoApplication"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a>So entfernen Sie ein vorhandenes Paket


Verwenden Sie die folgenden Informationen, um ein Paket vom Computer zu entfernen.

**Cmdlet**: Remove-AppvClientPackage

**Beispiel**: Remove-AppvClientPackage "ContosoApplication"

**Hinweis**  App-V-Cmdlets wurden Variablen für die vorherigen Beispiele nur zur besseren Übersichtlichkeit zugewiesen. Zuordnung ist keine Anforderung. Die meisten Cmdlets können so kombiniert werden [, wie Sie zum Hinzufügen und Veröffentlichen eines Pakets](#bkmk-add-pub-pkg-standalone-posh)angezeigt werden. Ein ausführliches Lernprogramm finden Sie unter [App-V 5,0 Client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).

 

## <a href="" id="bkmk-admins-pub-pkgs"></a>So aktivieren Sie nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen


**Hinweis** 
 **Dieses Feature wird ab App-V 5,0 SP3 unterstützt.**

 

Verwenden Sie das folgende Cmdlet und den folgenden Parameter, um nur Administratoren (nicht Endbenutzern) das veröffentlichen oder Aufheben der Veröffentlichung von Paketen zu ermöglichen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Cmdlet</strong></p></td>
<td align="left"><p>Satz-AppvClientConfiguration</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Parameter</strong></p></td>
<td align="left"><p>-RequirePublishAsAdmin</p>
<p>Parameter Werte:</p>
<ul>
<li><p>0-falsch</p></li>
<li><p>1-wahr</p></li>
</ul>
<p><strong>Beispiel: </strong> : Satz-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

Informationen zum Verwenden der App-V-Verwaltungskonsole zum Einrichten dieser Konfiguration finden Sie unter [Veröffentlichen eines Pakets mithilfe der Verwaltungskonsole](how-to-publish-a-package-by-using-the-management-console-51.md).

## <a href="" id="bkmk-understd-pend-pkgs"></a>Grundlegendes zu ausstehenden Paketen (UserPending und GlobalPending)


**Ab App-V 5,0 SP2**: Wenn Sie ein PowerShell-Cmdlet ausführen, das sich auf ein aktuell verwendetes Paket auswirkt, wird die Aufgabe, die Sie durchführen möchten, in einem ausstehenden Zustand angeordnet. Wenn Sie beispielsweise versuchen, ein Paket zu veröffentlichen, wenn eine Anwendung in diesem Paket verwendet wird, und dann **Get-AppvClientPackage**ausführen, wird der ausstehende Status in der Ausgabe des Cmdlets wie folgt angezeigt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ausgabeelement für Cmdlet</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>UserPending</p></td>
<td align="left"><p>Gibt an, ob das aufgelistete Paket eine ausstehende Aufgabe aufweist, die auf den Benutzer angewendet wird:</p>
<ul>
<li><p>Wahr</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalPending</p></td>
<td align="left"><p>Gibt an, ob das aufgelistete Paket eine ausstehende Aufgabe aufweist, die Global auf den Computer angewendet wird:</p>
<ul>
<li><p>Wahr</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Die ausstehende Aufgabe wird später entsprechend den folgenden Regeln ausgeführt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Art der Hintergrundaufgabe</th>
<th align="left">Anwendbare Regel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Benutzerbasierte Aufgaben, beispielsweise die Veröffentlichung eines Pakets für einen Benutzer</p></td>
<td align="left"><p>Die ausstehende Aufgabe wird ausgeführt, nachdem sich der Benutzer abgemeldet hat und sich dann wieder anmeldet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Global basierender Vorgang, beispielsweise Aktivieren einer Verbindungsgruppe Global</p></td>
<td align="left"><p>Die ausstehende Aufgabe wird ausgeführt, wenn der Computer heruntergefahren und neu gestartet wird.</p></td>
</tr>
</tbody>
</table>

 

Weitere Informationen zu ausstehenden Aufgaben finden Sie unter [Informationen zu App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).

Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

[Verwalten von App-V 5.1 mithilfe von PowerShell](administering-app-v-51-by-using-powershell.md)

 

 





