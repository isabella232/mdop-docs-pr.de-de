---
title: Grundlegende Informationen zu BitLocker-Verschlüsselungsoptionen und BitLocker-Laufwerkverschlüsselungselementen in der Systemsteuerung
description: Grundlegende Informationen zu BitLocker-Verschlüsselungsoptionen und BitLocker-Laufwerkverschlüsselungselementen in der Systemsteuerung
author: dansimp
ms.assetid: f8a01cc2-0c77-48b9-8351-8194e80b0cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739b65680ebfdf19f006ee8f3079f7c7e602f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804478"
---
# Grundlegende Informationen zu BitLocker-Verschlüsselungsoptionen und BitLocker-Laufwerkverschlüsselungselementen in der Systemsteuerung


In diesem Thema werden die Elemente der **BitLocker-Verschlüsselungsoptionen** und der **BitLocker Drive Encryption** -Systemsteuerung beschrieben und erläutert:

-   Erstellen dieser Elemente

-   Aufgaben, die Sie ausführen können

-   **Verwalten von BitLocker** Kontextmenü "mit der rechten Maustaste klicken", wenn es im Vergleich zu "ausgeblendet" angezeigt wird, und festlegen, dass es standardmäßig angezeigt werden soll

## BitLocker-Verschlüsselungsoptionen und Elemente des Control Panels für BitLocker-Laufwerkverschlüsselung


In der folgenden Tabelle sind die Aufgaben aufgeführt, die Sie in den einzelnen Control Panel-Elementen ausführen können, und es wird beschrieben, wie diese Elemente erstellt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">BitLocker-Verschlüsselungsoptionen (MBAM)</th>
<th align="left">BitLocker-Laufwerkverschlüsselung (Windows)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aufgaben, die Sie ausführen können</p></td>
<td align="left"><ul>
<li><p>Ändern Ihrer PIN oder Ihres Kennworts</p></li>
<li><p>Überprüfen des Verschlüsselungsstatus für ein Laufwerk</p></li>
<li><p>Öffnen der TPM-Verwaltungskonsole</p></li>
<li><p>BitLocker aktivieren</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Sperren des Schutzes für ein Laufwerk</p></li>
<li><p>Sichern des Wiederherstellungsschlüssels</p></li>
<li><p>Ändern der PIN</p></li>
<li><p>Deaktivieren von BitLocker für ein Laufwerk</p></li>
<li><p>Aktivieren von BitLocker für ein Laufwerk</p></li>
<li><p>Öffnen der TPM-Verwaltungskonsole</p></li>
<li><p>Entschlüsseln eines Laufwerks (wird nur angezeigt, wenn der MBAM-Client nicht installiert ist)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Erstellen des Elements "Systemsteuerung"</p></td>
<td align="left"><p>Wird in der Systemsteuerung erstellt, wenn Sie den MBAM-Client installieren. Dieses Element kann nicht ausgeblendet werden.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Dieses Element wird zusätzlich zu dem standardmäßigen Control Panel-Element für die BitLocker-Laufwerkverschlüsselung angezeigt, aber nicht ersetzt.</p>
</div>
<div>

</div></td>
<td align="left"><p>Wird standardmäßig in der Systemsteuerung als Teil des Windows-Betriebssystems angezeigt, Sie können es aber ausblenden.</p>
<p>Informationen dazu finden Sie unter <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)"> Ausblenden des Standardelements für die BitLocker-Laufwerkverschlüsselung in der Systemsteuerung </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="-manage-bitlocker--shortcut-menu"></a>Kontextmenü "BitLocker verwalten"


In der folgenden Tabelle wird beschrieben, wie sich das Kontextmenü **BitLocker verwalten** unterscheidet, je nachdem, ob der MBAM-Client installiert ist. Der Begriff "Kontextmenü" bezieht sich auf Optionen, die angezeigt werden, wenn Sie mit der rechten Maustaste auf ein Laufwerk im Windows-Explorer klicken.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Wenn der MBAM-Client installiert ist</th>
<th align="left">Wenn der MBAM-Client nicht installiert ist</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sichtbarkeit des Kontextmenüs</p></td>
<td align="left"><p>Die Option "BitLocker verwalten" ist ausgeblendet.</p>
<p>Wenn Sie die Option "BitLocker verwalten" im Kontextmenü sichtbar machen möchten, in dem die Option zum Entschlüsseln eines Laufwerks angezeigt wird, löschen Sie den folgenden Registrierungsschlüssel:</p>
<pre class="syntax" space="preserve"><code>HKEY_CLASSES_ROOT\Drive\Shell\manage-bde \REG_SZ LegacyDisable</code></pre></td>
<td align="left"><p>Die Option "BitLocker verwalten" wird im Kontextmenü angezeigt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Was Benutzer tun können</p></td>
<td align="left"><p>Wenn die Verknüpfung ausgeblendet ist, können Benutzer das BitLocker Drive Encryption Control Panel-Element öffnen, aber die Option zum Entschlüsseln eines Laufwerks steht nicht zur Verfügung.</p></td>
<td align="left"><p>Wenn die Verknüpfung angezeigt wird, wird durch Auswählen der <strong> Option BitLocker verwalten </strong> das Kontrollfeld Element für die BitLocker-Laufwerkverschlüsselung geöffnet, in dem die Option zum Entschlüsseln eines Laufwerks angezeigt wird.</p></td>
</tr>
</tbody>
</table>




## Verwandte Themen


[Verwalten von MBAM 2.5-Funktionen](administering-mbam-25-features.md)



## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





