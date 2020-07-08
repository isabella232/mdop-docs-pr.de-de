---
title: Planen der Speicherung und Bereitstellung des DaRT 8.0-Wiederherstellungsabbilds
description: Planen der Speicherung und Bereitstellung des DaRT 8.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: 939fbe17-0e30-4c85-8782-5b84d69442a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e5cca90c644eb3edf233564c474d2601d4227fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808638"
---
# Planen der Speicherung und Bereitstellung des DaRT 8.0-Wiederherstellungsabbilds


Sie können das Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsabbild mithilfe der folgenden Methoden speichern und bereitstellen. Berücksichtigen Sie die vor-und Nachteile der einzelnen Methoden, wenn Sie die Methode ermitteln, die Sie verwenden werden. Berücksichtigen Sie auch Ihre Infrastruktur-und Supportmitarbeiter. Wenn Sie über eine kleine Infrastruktur verfügen, möchten Sie möglicherweise Dart 8,0 mithilfe von Wechselmedien bereitstellen, da das Wiederherstellungsabbild immer verfügbar ist, wenn Sie es auf der lokalen Festplatte installieren.

Wenn Ihre Organisation Active Directory-Domänendienste (AD DS) verwendet, möchten Sie möglicherweise Wiederherstellungs Bilder mithilfe von Windows DS als Netzwerkdienst bereitstellen. Wiederherstellungs Bilder sind immer für jeden angeschlossenen Computer verfügbar. Sie können mehrere Bilder aus Windows DS bereitstellen und alle an einem zentralen Ort verwalten.

**Hinweis**  Möglicherweise möchten Sie in Ihrer Organisation mehr als eine Methode verwenden. So können Sie beispielsweise für die meisten Situationen in DART von einer Remotepartition Booten und einen USB-Stick zur Verfügung stellen, falls der Endbenutzercomputer keine Verbindung mit dem Netzwerk herstellen kann.

 

Die folgende Tabelle zeigt einige vor-und Nachteile der einzelnen Methoden der Verwendung von Dart in Ihrer Organisation.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode zum Booten in DART</th>
<th align="left">Vorteile</th>
<th align="left">Nachteile</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Wechselmedien</strong></p>
<p>Das Wiederherstellungsabbild wird auf eine CD, DVD oder ein USB-Laufwerk geschrieben, damit das Supportpersonal die Wiederherstellungstools auf dem unstable-Computer nutzen kann.</p></td>
<td align="left"><p>Unterstützt Szenarien, in denen der Master Boot Record (MBR) beschädigt ist und Sie nicht auf die Festplatte zugreifen können, und unterstützt Fälle, in denen keine Netzwerkverbindung vorhanden ist.</p>
<p>Ermöglicht Ihnen das Erstellen mehrerer Wiederherstellungs Bilder mit verschiedenen Tools, um unterschiedliche Supportstufen bereitzustellen.</p>
<p>Bietet ein integriertes Tool zum Brennen von Wiederherstellungs Bildern auf Wechselmedien.</p></td>
<td align="left"><p>Erfordert, dass die Supportmitarbeiter physisch am Endbenutzercomputer sind, um in DART zu booten.</p>
<p>Erfordert Zeit und Wartung, um mehrere Medien mit unterschiedlichen Konfigurationen für 32-Bit-und 64-Bit-Computer zu erstellen.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Von einer Remote-(Netzwerk-) Partition</strong></p>
<p>Das Wiederherstellungsabbild wird auf einem Netzwerkstart Server wie Windows-Bereitstellungsdienste (Windows Deployment Services, Windows DS) gehostet, mit dem Benutzer oder Mitarbeiter des Supports Sie bei Bedarf auf Computer streamen können.</p></td>
<td align="left"><p>Für alle Computer verfügbar, die Zugriff auf den Netzwerk Boot Server haben.</p>
<p>Wiederherstellungs Bilder werden auf einem zentralen Server gehostet, der zentralisierte Updates ermöglicht.</p>
<p>Zentralisierte Helpdesk-Mitarbeiter können Reparaturen mithilfe der Remotekonnektivität bereitstellen.</p>
<p>Kein lokaler Speicherbedarf für die Clients.</p>
<p>Möglichkeit zum Erstellen mehrerer Wiederherstellungs Bilder mit unterschiedlichen Tools für bestimmte Supportebenen.</p></td>
<td align="left"><p>Die Notwendigkeit, die Windows DS-Infrastruktur zu sichern, um sicherzustellen, dass reguläre Benutzer nur das DART-Wiederherstellungsabbild und nicht den vollständigen Betriebssystem-Bilderstellungs Prozess starten können.</p>
<p></p>
<p></p>
<p>Erfordert, dass der Endbenutzercomputer zur Laufzeit mit dem Netzwerk verbunden ist.</p>
<p>Erfordert, dass das Wiederherstellungsabbild über das Netzwerk gebracht wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Von einer Wiederherstellungspartition auf der lokalen Festplatte</strong></p>
<p>Das Wiederherstellungsabbild wird entweder manuell oder mithilfe elektronischer Softwareverteilungssysteme wie System Center Configuration Manager auf einer lokalen Festplatte installiert.</p></td>
<td align="left"><p>Das Wiederherstellungsabbild steht immer zur Verfügung, da es auf dem Computer vorab bereitgestellt wird.</p>
<p>Zentralisierte Helpdesk-Mitarbeiter können mithilfe der Remote Verbindung Support bereitstellen.</p>
<p>Das Wiederherstellungsabbild wird zentral verwaltet und bereitgestellt.</p>
<p>Weitere Wiederherstellungsschlüssel Anforderungen auf Computern, die durch die Windows BitLocker-Laufwerkverschlüsselung geschützt sind, werden eliminiert.</p></td>
<td align="left"><p>Lokaler Speicher ist erforderlich.</p>
<p>Es wird empfohlen, eine dedizierte, unverschlüsselte Partition für die Bildplatzierung zur Wiederherstellung zu finden, um das Risiko einer fehlgeschlagenen Startpartition zu verringern.</p>
<p>Beim Aktualisieren von DART müssen Sie alle Computer in Ihrem Unternehmen anstatt nur eine Partition (im Netzwerk) oder ein Wechsel Gerät aktualisieren.</p>
<p>Weitere Überlegungen sind erforderlich, wenn Sie das Wiederherstellungsabbild bereitstellen, nachdem BitLocker aktiviert wurde.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Planen der Bereitstellung von DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





