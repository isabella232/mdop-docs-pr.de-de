---
title: Planen der Migration von einer früheren Version von App-V
description: Planen der Migration von einer früheren Version von App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805000"
---
# Planen der Migration von einer früheren Version von App-V


Verwenden Sie die folgenden Informationen, um die Migration zu Microsoft Application Virtualization (app-v) 5,1 aus früheren Versionen von App-v zu planen.

## Migrationsanforderungen


Überprüfen Sie vor dem Starten von Upgrades die folgenden Voraussetzungen:

-   Wenn Sie ein Upgrade von einer älteren Version als App-v 4,6 SP2 durchführen, aktualisieren Sie zuerst auf Version App-v 4,6 SP3, bevor Sie auf App-v 5,1 oder höher aktualisieren. Aktualisieren Sie in diesem Szenario zuerst die App-V-Clients, und aktualisieren Sie dann die Server Komponenten.
**Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen.

-   App-v 5,1 unterstützt nur Pakete, die mit App-v 5,0 oder App-v 5,1 erstellt wurden, oder Pakete, die in das **AppV** -Format konvertiert wurden.

-   Wenn Sie den App-v-Server von App-v 5,0 SP1 aktualisieren, lesen Sie [Informationen zu app-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) .

## Gleichzeitige Ausführung des App-v 5,1-Clients mit App-v 4,6


Sie können den App-v 5,1-Client gleichzeitig auf demselben Computer mit dem App-v 4.6 SP3-Client ausführen.

Wenn Sie vorhandene App-V-Clients ausführen, haben Sie folgende Möglichkeiten:

-   Konvertieren Sie ein App-v 4,6 SP3-Paket in das App-v 5,1-Format, und veröffentlichen Sie beide Pakete, wenn beide Clients ausgeführt werden.

-   Definieren Sie die Migrations Richtlinie für das konvertierte Paket, sodass das konvertierte App-v 5,1-Paket die Dateitypzuordnungen und Verknüpfungen aus dem App-v 4,6-Paket übernimmt.

### Unterstützte Koexistenz-Szenarien

In der folgenden Tabelle werden die unterstützten App-V-Koexistenz-Szenarien dargestellt. Wir empfehlen, dass Sie die neuesten verfügbaren Updates einer bestimmten Version installieren, wenn Sie vorhandene Clients ausführen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V 4,6-Clienttyp</th>
<th align="left">App-V 5,1-Clienttyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,6 SP3</p></td>
<td align="left"><p>App-V 5.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 SP3 RDS</p></td>
<td align="left"><p>App-V 5,1 RDS</p></td>
</tr>
</tbody>
</table>

 

### Voraussetzungen für die Ausführung von vorhandenen Clients

Damit Sie vorhandene Clients ausführen können, müssen Sie:

-   Installieren Sie den App-v 4.6-Client, bevor Sie den App-v 5,1-Client installieren.

-   Aktivieren Sie die Gruppenrichtlinieneinstellung **Migrationsmodus aktivieren** , die sich im Knoten Koexistenz des **App-V-** &gt; **Clients** befindet. Informationen zum Bereitstellen der ADMX-Vorlage finden Sie unter [herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX)](https://technet.microsoft.com/library/dn659707.aspx).

**Hinweis**  App-v 5,1-Pakete können parallel zu app-v 4,6-Paketen ausgeführt werden, wenn Sie über nebeneinander vorhandene Installationen von App-v 5,1 und 4,6 verfügen. App-v 5,1-Pakete können jedoch nicht mit App-v 4,6-Paketen in derselben virtuellen Umgebung interagieren.

 

### Client Downloads und-Dokumentation

Die folgende Tabelle enthält Links zu den App-V 4,6-Clientdownloads und zur TechNet-Dokumentation zu den Versionen. Zu den Downloads gehören die App-V "reguläre" und RDS-Clients. Die TechNet-Dokumentation zum App-V-Client gilt für beide Clients, sofern nicht anders angegeben.

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V-Version</th>
<th align="left">Link zur TechNet-Dokumentation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)">Informationen zu Microsoft Application Virtualization 4.6SP3</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)">Informationen zu Microsoft Application Virtualization 5,1</a></p></td>
</tr>
</tbody>
</table>

 

Weitere Informationen zum Konfigurieren der Koexistenz von App-V 5,1-Clients finden Sie unter:

-   [Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf demselben Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [App-V 5,0 Koexistenz und Migration](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a>Konvertieren von Paketen der vorherigen Version mithilfe des Paket Konverters


Bevor Sie ein Paket, das mit App-4.6 SP2 oder früher erstellt wurde, zu App-V 5,1 migrieren, überprüfen Sie die folgenden Voraussetzungen:

-   Sie müssen das Paket in das **AppV-** Dateiformat konvertieren.

-   Der Paket Konverter unterstützt nur die direkte Konvertierung von Paketen, die mithilfe von App-V 4,5 und höher erstellt wurden. Wenn Sie den Paket Konverter für ein Paket verwenden möchten, das mit einer früheren Version erstellt wurde, müssen Sie eine APP-v 4.5 oder höhere Version des Sequencers verwenden, um das Paket zu aktualisieren, und dann können Sie die Paketkonvertierung durchführen.

Weitere Informationen zur Verwendung des Paket Konverters zum Konvertieren eines Pakets finden Sie unter so wird es [gemacht: Konvertieren eines Pakets, das in einer früheren Version von App-V erstellt wurde](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md). Nachdem Sie die Datei konvertiert haben, können Sie Sie auf Zielcomputern bereitstellen, auf denen der App-V 5,1-Client ausgeführt wird.






## Verwandte Themen


[Planen der Bereitstellung von App-V](planning-to-deploy-app-v51.md)

 

 





