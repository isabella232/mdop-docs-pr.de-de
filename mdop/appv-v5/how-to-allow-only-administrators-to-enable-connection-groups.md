---
title: So schränken Sie die Aktivierung von Verbindungsgruppen auf Administratoren ein
description: So schränken Sie die Aktivierung von Verbindungsgruppen auf Administratoren ein
author: dansimp
ms.assetid: 60e62426-624f-4f26-851e-41cd78520883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53461d5c93bf246210c7427c95a8bbe8acca9cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805744"
---
# So schränken Sie die Aktivierung von Verbindungsgruppen auf Administratoren ein


Sie können den App-V-Client so konfigurieren, dass nur Administratoren (nicht Endbenutzer) Verbindungsgruppen aktivieren oder deaktivieren können. In früheren Versionen von App-V konnten Sie nicht verhindern, dass Endbenutzer diese Aufgaben ausführen.

**Hinweis** 
 **Dieses Feature wird ab App-V 5,0 SP3 unterstützt.**

 

Verwenden Sie eine der folgenden Methoden, damit nur Administratoren Verbindungsgruppen aktivieren oder deaktivieren können.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Schritte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gruppenrichtlinieneinstellung</p></td>
<td align="left"><p>Aktivieren Sie die Gruppenrichtlinieneinstellung "Veröffentlichung als Administrator anfordern", die sich im folgenden Gruppenrichtlinien-Objektknoten befindet:</p>
<p><strong>Computerkonfigurations &gt; Richtlinien &gt; , administrative Vorlagen &gt; &gt; , System App-V &gt; Publishing</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell-Cmdlet</p></td>
<td align="left"><p>Führen Sie das <strong> Cmdlet "Satz-AppvClientConfiguration </strong> " mit dem <strong> Parameter "– RequirePublishAsAdmin" aus </strong> .</p>
<p>Parameter Werte:</p>
<ul>
<li><p>0-falsch</p></li>
<li><p>1-wahr</p></li>
</ul>
<p><strong>Beispiel: </strong> : Satz-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Verwalten von Verbindungsgruppen](managing-connection-groups.md)

 

 





