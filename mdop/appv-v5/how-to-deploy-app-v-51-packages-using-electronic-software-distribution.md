---
title: Bereitstellen von App-V 5.1-Paketen mithilfe einer ESD-Lösung (Electronic Software Distribution)
description: Bereitstellen von App-V 5.1-Paketen mithilfe einer ESD-Lösung (Electronic Software Distribution)
author: dansimp
ms.assetid: e1957a5a-1f18-42da-b2c1-a5ae5a4cca7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a9ed5fbb264f8fb9676d7fa18fe4de8019ea8e79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805537"
---
# Bereitstellen von App-V 5.1-Paketen mithilfe einer ESD-Lösung (Electronic Software Distribution)


Sie können ein ESD-System (Electronic Software Distribution) verwenden, um App-v 5,1-virtuelle Anwendungen für App-v-Clients bereitzustellen. Einzelheiten finden Sie in der Dokumentation, die mit dem von Ihnen verwendeten ESD-Dokument zur Verfügung steht.

Komponentenanforderungen und Optionen für die Verwendung eines ESD zur Bereitstellung von App-v-Paketen finden Sie unter [Planen der Bereitstellung von App-v 5,1 mit einem elektronischen Software Verteilungs System](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).

Verwenden Sie eine der folgenden Methoden, um Pakete auf App-V-Clientcomputern mit einem ESD-Code zu veröffentlichen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Funktionen, die von einem Drittanbieter-ESD bereitgestellt werden</p></td>
<td align="left"><p>Verwenden Sie die Funktionalität in einem Drittanbieter-ESD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Eigenständiges Windows Installer</p></td>
<td align="left"><p>Installieren Sie die Anwendung auf dem Zielclientcomputer mithilfe der zugehörigen Windows Installer-Datei (MSI), die bei der ersten Sequenzierung einer Anwendung erstellt wird. Die Windows Installer-Datei enthält die zugehörigen App-V 5,1-Paketdatei Informationen, die zum Konfigurieren eines Pakets verwendet werden, und kopiert die erforderlichen Paketdateien auf den Client.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Verwenden Sie PowerShell-Cmdlets zum Bereitstellen virtualisierter Anwendungen. Weitere Informationen zur Verwendung von PowerShell und App-v 5,1 finden Sie unter <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)"> Verwalten von App-v 5,1 mithilfe von PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

 

**So stellen Sie App-V 5,1-Pakete mithilfe eines ESD bereit**

1.  Installieren Sie den App-V 5,1-Sequenzer auf einem Computer in Ihrer Umgebung. Weitere Informationen zum Installieren des Sequencers finden Sie unter [so wird es gemacht: Installieren des Sequencers](how-to-install-the-sequencer-51beta-gb18030.md).

2.  Verwenden Sie den App-V 5,1-Sequenzer zum Erstellen einer virtuellen Anwendung. Informationen zum Erstellen einer virtuellen Anwendung finden Sie unter [Erstellen und Verwalten von virtualisierten Anwendungen in App-V 5,1](creating-and-managing-app-v-51-virtualized-applications.md).

3.  Nachdem Sie die virtuelle Anwendung erstellt haben, müssen Sie das Paket mithilfe ihrer ESD-Lösung bereitstellen.

    Wenn Sie den System Center Configuration Manager verwenden, überprüfen Sie zunächst [die Einführung in die Anwendungsverwaltung in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) , um Informationen zur Verwendung von App-V 5,1 und dem System Center2012-Konfigurations-Manager zu erhalten.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





