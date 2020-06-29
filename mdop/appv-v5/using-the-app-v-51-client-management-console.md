---
title: Verwenden der App-V 5.1 Client Management Console
description: Verwenden der App-V 5.1 Client Management Console
author: dansimp
ms.assetid: be6d4e35-5701-4f9a-ba8a-bede12662cf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63dd75395cdfef1aebae30b364f77465ba8a9882
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804841"
---
# Verwenden der App-V 5.1 Client Management Console


Dieses Thema enthält Informationen dazu, wie Sie den Microsoft Application Virtualization (App-V) 5,1-Client konfigurieren und verwalten können.

## Ändern der App-V 5,1-Clientkonfiguration


Der App-V 5,1-Client verfügt über zugeordnete Einstellungen, die konfiguriert werden können, um zu bestimmen, wie der Client in Ihrer Umgebung ausgeführt werden soll. Sie können diese Einstellungen auf dem Computer verwalten, auf dem der Client ausgeführt wird, oder mithilfe von PowerShell oder Gruppenrichtlinien. Weitere Informationen zum Ändern des Clients mithilfe der PowerShell oder der Gruppenrichtlinienkonfiguration finden Sie unter [Ändern der Clientkonfiguration mithilfe von PowerShell](how-to-modify-client-configuration-by-using-powershell51.md).

## <a href="" id="the-app-v-5-1-client-management-console-"></a>Die App-V 5,1-Clientverwaltungskonsole


Mithilfe der APP-v 5,1-Clientverwaltungskonsole können Sie Informationen zum App-v 5,1-Client abrufen oder bestimmte Aufgaben ausführen. Viele der Aufgaben, die Sie in der Clientverwaltungskonsole ausführen können, können Sie auch mithilfe von PowerShell ausführen. Die zugehörigen PowerShell-Cmdlets für jede Aktion werden auch in der folgenden Tabelle angezeigt. Weitere Informationen zur Verwendung von PowerShell finden Sie unter [Verwalten von App-V 5,1 mithilfe von PowerShell](administering-app-v-51-by-using-powershell.md).

Die Clientverwaltungskonsole enthält die folgenden beschriebenen Hauptregisterkarten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Registerkarte</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Übersicht</p></td>
<td align="left"><p>Die <strong> </strong> Registerkarte "Übersicht" enthält die folgenden Elemente:</p>
<ul>
<li><p>Update – verwenden Sie die <strong> Kachel "Aktualisieren" </strong> , um eine virtualisierte Anwendung zu aktualisieren oder ein neues virtualisiertes Paket zu erhalten.</p>
<p>Die <strong> Letzte Aktualisierung </strong> zeigt die aktuelle Version des virtualisierten Pakets an.</p></li>
<li><p>Laden Sie alle virtuellen Anwendungen herunter – verwenden Sie die <strong> Download </strong> Kachel, um alle Pakete herunterzuladen, die für den aktuellen Benutzer bereitgestellt wurden.</p>
<p>(Zugehöriges PowerShell-Cmdlet: <strong> Mount-AppvClientPackage </strong> )</p>
<p></p></li>
<li><p>Offline arbeiten – verwenden Sie diese Kachel, um alle automatischen und manuellen Updates für virtuelle Anwendungen zu verbieten.</p>
<p>(Zugehöriges PowerShell-Cmdlet: <strong> Satz-AppvPublishServer – UserRefreshEnabled – GlobalRefreshEnabled </strong> )</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Virtuelle apps</p></td>
<td align="left"><p><strong> </strong> Auf der Registerkarte Virtuelle apps werden alle Pakete angezeigt, die für den Benutzer veröffentlicht wurden. Sie können auch auf ein bestimmtes Paket klicken und alle Anwendungen anzeigen, die Teil dieses Pakets sind. Damit werden Informationen zu Paketen angezeigt, die derzeit verwendet werden und wie viele Pakete von jedem Paket auf den Computer heruntergeladen wurden. Sie können auch Paketdownloads starten und beenden. Darüber hinaus können Sie den Benutzerstatus reparieren. Bei einer Reparatur werden alle Benutzerdaten gelöscht, die einem Paket zugeordnet sind.</p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-Verbindungsgruppen</p></td>
<td align="left"><p><strong> </strong> Auf der Registerkarte "App-Verbindungsgruppen" werden alle Verbindungsgruppen angezeigt, die für den aktuellen Benutzer verfügbar sind. Klicken Sie auf eine bestimmte Verbindungsgruppe, um alle Pakete anzuzeigen, die Teil der ausgewählten Gruppe sind. Damit werden Informationen zu Verbindungsgruppen angezeigt, die bereits verwendet werden, und der Inhalt der Verbindungsgruppe, die auf den Computer heruntergeladen wurde. Darüber hinaus können Sie Verbindungsgruppen Downloads starten und beenden. Sie können diesen Abschnitt verwenden, um eine Reparatur zu initiieren. Bei einer Reparatur wird der gesamte Benutzerstatus entfernt, dem eine Verbindungsgruppe zugeordnet ist.</p>
<p>(Zugeordnete PowerShell-Cmdlets: Download- <strong> Mount-AppvClientConnectionGroup </strong> . Reparieren- <strong> AppvClientConnectionGroup </strong> .)</p>
<p></p></td>
</tr>
</tbody>
</table>

 

[So greifen Sie auf die Client-Verwaltungskonsole zu](how-to-access-the-client-management-console51.md)

[So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-51.md)






## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





