---
title: Planen der Speicherung und Bereitstellung des DaRT 7.0-Wiederherstellungsabbilds
description: Planen der Speicherung und Bereitstellung des DaRT 7.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809571"
---
# Planen der Speicherung und Bereitstellung des DaRT 7.0-Wiederherstellungsabbilds


Verwenden Sie die Informationen in diesem Abschnitt, wenn Sie beabsichtigen, das Microsoft Diagnostics and Recovery Toolset (Dart) 7-Wiederherstellungsabbild zu speichern und bereitzustellen.

## Planen des Speicherns und Bereitstellens des DART-Wiederherstellungs Bilds


Sie können das DART-Wiederherstellungsabbild mithilfe der folgenden Methoden speichern und bereitstellen. Berücksichtigen Sie die vor-und Nachteile der einzelnen Methoden, wenn Sie die Methode ermitteln, die Sie verwenden werden. Denken Sie auch daran, wie Sie Dart in Ihrem Unternehmen verwenden möchten.

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
<td align="left"><p>Von einer CD oder DVD</p></td>
<td align="left"><p>Unterstützt Szenarien, in denen der Master Boot Record (MBR) beschädigt ist und Sie nicht auf die Festplatte zugreifen können. Unterstützt auch Fälle, in denen keine Netzwerkverbindung vorhanden ist.</p>
<p>Diese Vorgehensweise ist für Benutzer mit früheren DART-Versionen am besten bekannt, und eine CD oder DVD kann direkt aus dem <strong> Dart-Wiederherstellungsbild-Assistenten gebrannt werden </strong> .</p></td>
<td align="left"><p>Erfordert, dass eine Person mit Zugriff auf die CD oder DVD physisch auf dem Computer des Endbenutzers ist, um in DART zu booten.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Über einen USB-Stick (USB-Stick)</p></td>
<td align="left"><p>Bietet dieselben Vorteile wie das Booten von einer CD oder DVD und bietet auch Unterstützung für Computer, die kein CD-oder DVD-Laufwerk besitzen.</p></td>
<td align="left"><p>Erfordert die Formatierung des USB-Flashlaufwerks, bevor Sie es zum Starten in DART verwenden können. Erfordert auch, dass eine Person mit Zugriff auf das USB-Flashlaufwerk physisch auf dem Computer des Endbenutzers ist, um in DART zu booten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Von einer Remote-(Netzwerk-) Partition</p></td>
<td align="left"><p>Ermöglicht das Booten in Dart, ohne dass eine CD, DVD oder ein USB-Laufwerk benötigt wird. Ermöglicht auch einfache Upgrades von Dart, da nur ein Dateispeicherort zu aktualisieren ist.</p></td>
<td align="left"><p>Funktioniert nicht, wenn der Computer des Endbenutzers nicht mit dem Netzwerk verbunden ist.</p>
<p>Für Endbenutzer weithin verfügbar und erfordern möglicherweise zusätzliche Sicherheitsüberlegungen, wenn Sie das Wiederherstellungsabbild erstellen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Von einer Wiederherstellungspartition</p></td>
<td align="left"><p>Mit dieser Option können Sie in DART Booten, ohne eine CD, DVD oder ein USB-Flashlaufwerk zu benötigen, das Instanzen enthält, in denen keine Netzwerkkonnektivität vorhanden ist.</p>
<p>Darüber hinaus können Sie mithilfe von automatisierten Verteilungstools wie Microsoft Endpoint Configuration Manager als Teil Ihres standardmäßigen Windows-Abbild Prozesses implementiert und verwaltet werden.</p></td>
<td align="left"><p>Beim Aktualisieren von DART müssen Sie alle Computer in Ihrem Unternehmen anstatt nur eine Partition (im Netzwerk) oder ein Gerät (CD, DVD oder USB-Flashlaufwerk) aktualisieren.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Planen der Bereitstellung von DaRT 7.0](planning-to-deploy-dart-70.md)

 

 





