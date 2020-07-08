---
title: Anwenden von Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich
description: Anwenden von Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811803"
---
# Anwenden von Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich


Administratoren können die Netzwerkeinstellungen für jeden MED-V-Arbeitsbereich definieren.

Alle Netzwerkeinstellungen sind im **Richtlinien** Modul auf der Registerkarte **Netzwerk** konfiguriert.

**So wenden Sie Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich an**

1.  Klicken Sie auf den MED-V-Arbeitsbereich, den Sie konfigurieren möchten.

2.  Konfigurieren Sie im Bereich " **Netzwerk** " die Einstellungen, wie in der folgenden Tabelle beschrieben.

3.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

**MED-V Workspace-Netzwerkeigenschaften**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Eigenschaft</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TCP/IP-Eigenschaften</p></td>
<td align="left"><ul>
<li><p><strong>Verwenden Sie die IP-Adresse (NAT) </strong> des Hosts – der Arbeitsbereich verwendet NAT, um die IP-Adresse des Hosts für ausgehenden Datenverkehr freizugeben.</p></li>
<li><p><strong>Verwenden Sie eine andere IP-Adresse als Host (Bridge) </strong> – der MED-V-Arbeitsbereich hat eine eigene Netzwerkadresse, die normalerweise über DHCP abgerufen wird.</p></li>
</ul>
<p>Aktivieren Sie das <strong> Kontrollkästchen mehrere Adapter in den Arbeitsbereich zuordnen </strong> , wenn auf dem Hostcomputer mehrere Adapter vorhanden sind. Es wird empfohlen, diese Konfiguration zu verwenden, wenn der Host zwischen verschiedenen Netzwerken mit unterschiedlichen Adaptern wechselt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DNS-Server</p></td>
<td align="left"><ul>
<li><p><strong>Nicht ändern </strong> – die DNS-Einstellungen, die auf dem virtuellen Computer mit dem MED-V Workspace festgesetzt werden, werden nicht geändert.</p></li>
<li><p><strong>Verwenden der Host-DNS-Adresse </strong> – die DNS-Einstellungen für den MED-V-Arbeitsbereich werden so synchronisiert, dass Sie den Einstellungen des Hosts entsprechen. Die DNS-Synchronisierung ist dynamisch. Sie wird in regelmäßigen Abständen mit dem Host synchronisiert, sodass Sie im MED-V-Arbeitsbereich dynamisch geändert wird, wenn Sie auf dem Host geändert wird.</p></li>
<li><p><strong>Verwenden bestimmter DNS-Adressen </strong> – der MED-V-Arbeitsbereich verwendet ein bestimmtes DNS, wie angegeben.</p>
<p><strong> </strong> Geben Sie in den Feldern Primär und <strong> Sekundär </strong> die primären und sekundären DNS-Adressen ein.</p>
<p>Aktivieren Sie das <strong> Kontrollkästchen Host-DNS-Adressen anfügen </strong> , um den Host an die konfigurierten DNS-Adressen anzufügen.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Zuweisen von DNS-Suffixen</p></td>
<td align="left"><ul>
<li><p><strong>Weisen Sie die folgenden Suffixe </strong> zu: Aktivieren Sie dieses Kontrollkästchen, um bestimmte DNS-Suffixe zuzuweisen; geben Sie im Feld ein Suffix oder mehrere Suffixe durch Kommas getrennt ein.</p></li>
<li><p><strong>Anfügen von Host Suffixen </strong> – Aktivieren Sie dieses Kontrollkästchen, um die Host Suffixe an die DNS-Adresse anzufügen.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Erstellen eines MED-V-Arbeitsbereichs](creating-a-med-v-workspacemedv-10-sp1.md)

[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

 

 





