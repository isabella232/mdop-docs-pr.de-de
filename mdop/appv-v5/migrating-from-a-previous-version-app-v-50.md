---
title: Migrieren von einer früheren Version
description: Migrieren von einer früheren Version
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805066"
---
# Migrieren von einer früheren Version


Mit App-v 5,0 können Sie Ihre vorhandene App-v 4,6-Infrastruktur auf die flexiblere, integrierte und einfacher zu verwaltende App-v 5,0-Infrastruktur migrieren.

Wenn Sie Ihre Migrationsstrategie planen, sollten Sie die folgenden Abschnitte in Frage stellen:

**Hinweis**  Weitere Informationen zu den Unterschieden zwischen App-v 4,6 und App-v 5,0 finden Sie unter **Unterschiede zwischen App-v 4,6 und App-v 5,0 im Abschnitt** [über APP-v 5,0](about-app-v-50.md).

 

## Konvertieren von Paketen, die mit einer früheren Version von App-V erstellt wurden


Verwenden Sie das Paket Konverter-Dienstprogramm, um virtuelle Anwendungspakete zu aktualisieren, die mit früheren Versionen von App-V erstellt wurden. Der Paket Konverter verwendet PowerShell zum Konvertieren von Paketen und kann die Automatisierung des Prozesses unterstützen, wenn viele Pakete vorhanden sind, für die eine Konvertierung erforderlich ist.

**Wichtig**  Nachdem Sie ein vorhandenes Paket konvertiert haben, sollten Sie das Paket vor der Bereitstellung des Pakets testen, um sicherzustellen, dass der Konvertierungsvorgang erfolgreich war.

 

**Was Sie wissen müssen, bevor Sie vorhandene Pakete konvertieren**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Problem</th>
<th align="left">Problemumgehung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paket Skripts werden nicht konvertiert.</p></td>
<td align="left"><p>Testen Sie das konvertierte Paket. Falls erforderlich, konvertieren Sie das Skript.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Überschreibungen für die Paket Registrierungseinstellung werden nicht konvertiert.</p></td>
<td align="left"><p>Testen Sie das konvertierte Paket. Fügen Sie bei Bedarf Registrierungs Überschreibungen erneut hinzu.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Virtuelle Pakete, die DSC verwenden, werden nach der Konvertierung nicht verknüpft.</p></td>
<td align="left"><p>Verknüpfen Sie die Pakete mithilfe von Verbindungsgruppen. Siehe <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> Verwalten von Verbindungsgruppen </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Während der Konvertierung werden Umgebungsvariablen Konflikte erkannt.</p></td>
<td align="left"><p>Beheben Sie alle Konflikte in der zugehörigen <strong> OSD- </strong> Datei.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Während der Konvertierung werden hart codierte Pfade erkannt.</p></td>
<td align="left"><p>Hart codierte Pfade sind schwierig, richtig zu konvertieren. Der Paket Konverter erkennt Pakete mit Dateien, die hart codierte Pfade enthalten, und gibt diese zurück. Zeigen Sie die Datei mit dem hartcodierten Pfad an, und ermitteln Sie, ob das Paket die Datei erfordert. Wenn dies der Fall ist, empfiehlt es sich, das Paket neu zu sequenzieren.</p></td>
</tr>
</tbody>
</table>

 

Beim Konvertieren einer Paketprüfung auf fehlerhafte Dateien oder Verknüpfungen. Suchen Sie das Element in App-V 4,6-Paket. Möglicherweise ist es ein hartcodierter Pfad. Konvertieren Sie den Pfad.

**Hinweis**  Es wird empfohlen, den App-V 5,0-Sequenzer zum Konvertieren kritischer Anwendungen oder Anwendungen zu verwenden, die Features nutzen müssen. Lesen Sie, [wie Sie eine neue Anwendung mit App-V 5,0 Sequenzieren](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).

Wenn ein konvertiertes Paket nicht geöffnet wird, nachdem Sie es konvertiert haben, empfiehlt es sich auch, die Anwendung mithilfe des App-V 5,0-Sequencers neu zu sequenzieren.

 

[So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## Migrieren von Clients


In der folgenden Tabelle wird die empfohlene Methode zum Aktualisieren von Clients angezeigt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aktualisieren Ihrer Umgebung auf App-v 4.6 SP2</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Überlegungen zur Implementierung und zum Upgrade von Application Virtualization </a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Installieren Sie den App-V 5,0-Client mit aktivierter Koexistenz.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)">Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf </a> demselben Computer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenzieren und Rollout von App-V 5,0-Paketen. Bei Bedarf können Sie die Veröffentlichung von App-V 4,6-Paketen aufheben.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)">So wird es gemacht: Sequenzierung einer neuen Anwendung mit APP- </a> V 5,0</p></td>
</tr>
</tbody>
</table>

 

**Wichtig**  Sie müssen App-v 4.6 SP3 ausführen, um den Koexistenzmodus verwenden zu können. Wenn Sie ein Paket sequenzieren, müssen Sie außerdem die Einstellung für die Verwaltungsautorität konfigurieren, die sich in der **Benutzerkonfiguration** befindet, die sich im Abschnitt **Benutzerkonfiguration** befindet.

 

## Migrieren der vollständigen Infrastruktur des App-V 5,0-Servers


Es gibt keine direkte Methode zum Upgrade auf eine vollständige App-V 5,0-Infrastruktur. Verwenden Sie die Informationen im folgenden Abschnitt, um Informationen zum Upgrade des App-V-Servers zu erhalten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aktualisieren Sie Ihre Umgebung auf App-v 4.6 SP3.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Überlegungen zur Implementierung und zum Upgrade von Application Virtualization </a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Bereitstellen der App-V 5,0-Version des Clients</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">Bereitstellen des App-V </a> -Clients</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installieren Sie den App-V 5,0-Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">Bereitstellen des App-V 5,0 </a> -Servers</p></td>
</tr>
<tr class="even">
<td align="left"><p>Migrieren vorhandener Pakete</p></td>
<td align="left"><p>Weitere Informationen finden Sie unter <strong> Konvertieren von Paketen, die mit einer früheren Version von App-V </strong> in diesem Artikel erstellt wurden.</p></td>
</tr>
</tbody>
</table>

 

## Zusätzliche Migrationsaufgaben


Sie können auch zusätzliche Migrationsaufgaben wie die Neukonfiguration von Endpunkten und das Öffnen eines Pakets ausführen, das mit einer früheren Version auf einem Computer mit dem App-V 5,0-Client erstellt wurde. Die folgenden Links enthalten weitere Informationen zum Ausführen dieser Aufgaben.

[So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.0-Paket für alle Benutzer eines bestimmten Computers](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## Weitere Ressourcen für die Ausführung von App-V-Migrationsaufgaben


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

[Ein vereinfachtes Upgrade-Verfahren für Microsoft App-V 5,1-Verwaltungs Server](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





