---
title: Über die virtuelle Verbindungsgruppenumgebung
description: Über die virtuelle Verbindungsgruppenumgebung
author: dansimp
ms.assetid: b7bb0e3d-8cd5-45a9-b84e-c9ab4196a18c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43f30c2100fc982170f15c305b03cd338b5d8afd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806062"
---
# Über die virtuelle Verbindungsgruppenumgebung


**In diesem Thema:**

-   [Ermitteln der Paketpriorität](#bkmk-pkg-priority-deter)

-   [Zusammenführen identischer Paket Pfade zu einem virtuellen Verzeichnis in Verbindungsgruppen](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a>Ermitteln der Paketpriorität


Die virtuelle Umgebung und Ihr aktueller Zustand sind der Verbindungsgruppe zugeordnet, nicht den einzelnen Paketen. Wenn ein App-V-Paket aus der Verbindungsgruppe entfernt wird, wird der Zustand, der als Teil der Verbindungsgruppe vorhanden war, nicht mit dem Paket migriert.

Wenn das gleiche Paket Bestandteil von zwei verschiedenen Verbindungsgruppen ist, müssen Sie angeben, welche Verbindungsgruppe App-V verwenden soll. So können Sie beispielsweise zwei Pakete in einer Verbindungsgruppe haben, die jeweils denselben Registrierungs-DWORD-Wert definieren.

Die verwendete Verbindungsgruppe basiert auf der Reihenfolge, in der ein Paket im **AppConnectionGroup** -XML-Dokument angezeigt wird:

-   Das erste Paket hat die höchste Priorität.

-   Das zweite Paket hat die zweithöchste Priorität.

Sehen Sie sich den folgenden Beispielabschnitt an:

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

Angenommen, derselbe DWORD-Wert ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) wird im ersten und dritten Paket definiert, beispielsweise:

-   Paket 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5

-   Paket 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10

Da Paket 1 zuerst angezeigt wird, weist die virtuelle Umgebung des AppConnectionGroup den einzelnen DWORD-Wert 5 auf (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5). Das bedeutet, dass die virtuellen Anwendungen in Paket 1, Paket 2 und Paket 3 alle den Wert 5 sehen, wenn Sie eine Abfrage nach HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.

Andere virtuelle Umgebungs Ressourcen werden in ähnlicher Weise aufgelöst, aber der übliche Fall ist, dass die Kollisionen in der Registrierung auftreten.

## <a href="" id="bkmk-merged-root-ve-exp"></a>Zusammenführen identischer Paket Pfade zu einem virtuellen Verzeichnis in Verbindungsgruppen


Wenn zwei oder mehr Pakete in einer Verbindungsgruppe identische Verzeichnispfade enthalten, werden die Pfade in einem einzigen virtuellen Verzeichnis innerhalb der virtuellen Umgebung der Verbindungsgruppe zusammengeführt. Dieses Zusammenführen von Pfaden ermöglicht es einer Anwendung in einem Paket, auf Dateien zuzugreifen, die in einem anderen Paket enthalten sind.

Wenn Sie ein Paket aus einer Verbindungsgruppe entfernen, können die Anwendungen in diesem entfernten Paket nicht mehr auf Dateien in den verbleibenden Paketen in der Verbindungsgruppe zugreifen.

Die Reihenfolge, in der APP-v den Namen einer Datei in der Verbindungsgruppe nachschlägt, wird in der Reihenfolge angegeben, in der die APP-v-Pakete in der Manifestdatei der Verbindungsgruppe aufgeführt sind.

Das folgende Beispiel zeigt die Reihenfolge und Beziehung einer Dateinamen Suche in einer Verbindungsgruppe für **Paket a** und **Paket B**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paket A</th>
<th align="left">Paket B</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>C:\Windows\System32</p></td>
<td align="left"><p>C:\Windows\System32</p></td>
</tr>
<tr class="even">
<td align="left"><p>C:\AppTest</p></td>
<td align="left"><p>C:\AppTest</p></td>
</tr>
</tbody>
</table>

 

Wenn in dem obigen Beispiel eine virtualisierte Anwendung versucht, eine bestimmte Datei zu finden, wird Paket a zuerst nach einem übereinstimmenden Dateipfad durchsucht. Wenn kein übereinstimmender Pfad gefunden wird, wird Paket B mithilfe der folgenden Zuordnungsregeln durchsucht:

-   Wenn eine Datei mit dem Namen **test.txt** in der gleichen virtuellen Ordnerhierarchie in beiden Anwendungspaketen vorhanden ist, wird die erste übereinstimmende Datei verwendet.

-   Wenn eine Datei mit dem Namen **bar.txt** in der virtuellen Ordnerhierarchie eines Anwendungspakets vorhanden ist, aber nicht im anderen, wird die erste übereinstimmende Datei verwendet.






## Verwandte Themen


[Verwalten von Verbindungsgruppen](managing-connection-groups51.md)

 

 





