---
title: Informationen zur Registerkarte „Bereitstellung“
description: Informationen zur Registerkarte „Bereitstellung“
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808116"
---
# Informationen zur Registerkarte „Bereitstellung“


Verwenden Sie die Registerkarte **Bereitstellung** in der Application Virtualization Sequencer Console, um die Informationen für eine Anwendung zu ändern, die Sie gerade abgleichen möchten. Diese Registerkarte enthält die folgenden Elemente.

## Server-URL


Verwenden Sie die **Server-URL** -Steuerelemente, um die Konfigurationseinstellungen für den virtuellen Anwendungsserver anzugeben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Steuerelement</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Protokoll</strong></p></td>
<td align="left"><p>Ermöglicht Ihnen, das Protokoll auszuwählen, das das sequenzierte Anwendungspaket von einem virtuellen Anwendungsserver zu einem Application Virtualization-Desktop Client streamen soll. Die folgenden Protokolle stehen zur Verfügung:</p>
<ul>
<li><p><strong>RTSP </strong> – der Standardwert gibt an, dass das Echt Zeit Streaming-Protokoll den Austausch von Virtualisierungs fähigen Anwendungen steuert.</p></li>
<li><p><strong>RTSPS </strong> – gibt an, dass das Echt Zeit Streaming-Protokoll mit Transport Schicht Sicherheit den Austausch eines sequenzierten Anwendungspakets steuert.</p></li>
<li><p><strong>Datei </strong> : gibt an, dass die sequenzierte Anwendung von einer Dateifreigabe gestreamt wird.</p></li>
<li><p><strong>HTTPS </strong> : gibt an, dass das sichere Hypertext-Transport Protokoll den Austausch eines Pakets steuert.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Hostname</strong></p></td>
<td align="left"><p>Ermöglicht Ihnen, den virtuellen Anwendungsserver oder das Load Balancer vor einer Gruppe virtueller Anwendungsserver auszuwählen, die das Softwarepaket an einen Application Virtualization Desktop-Client streamen. Sie müssen dieses Element zum Erstellen eines sequenzierten Anwendungspakets ausfüllen, doch können Sie von der Standardumgebungsvariable% SFT_SOFTGRIDSERVER% auf den tatsächlichen Hostnamen oder die IP-Adresse eines virtuellen Anwendungsservers umstellen.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie keine statischen Hostnamen oder IP-Adressen angeben, müssen Sie auf jedem Application Virtualization-Desktop Client eine Umgebungsvariable mit dem Namen SFT_SOFTGRIDSERVER einrichten. Der Wert muss der Hostname oder die IP-Adresse des Virtual Application Servers oder Load Balancer sein, bei dem es sich um die Quelle der Anwendungen dieses Client&#39;s handelt. Sie sollten diese Umgebungsvariable zu einer Systemvariablen anstatt zu einer Benutzervariablen machen. Jede Application Virtualization Desktop Client-Sitzung, die während der Zuweisung dieser Variable auf diesem Computer ausgeführt wird, muss geschlossen und dann geöffnet werden, damit die wieder aufgenommene Sitzung über die neue Anwendungsquelle informiert wird.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Port</strong></p></td>
<td align="left"><p>Ermöglicht es Ihnen, den Port anzugeben, auf dem der Virtual Application Server oder das Load Balancer auf eine Application Virtualization Desktop Client&#39;s-Anforderung für das Paket lauscht. Diese Informationen sind zum Erstellen eines Pakets erforderlich, können aber geändert werden. Der Standardport ist 554.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Pfad</strong></p></td>
<td align="left"><p>Ermöglicht es Ihnen, den relativen Pfad auf dem virtuellen Anwendungsserver anzugeben, in dem das Softwarepaket gespeichert ist und von dem es gestreamt wird. Diese Informationen sind erforderlich, um ein Paket zu erstellen, wenn die SFT-Datei in einem Unterverzeichnis des Inhalts gespeichert werden soll. Andernfalls sind diese Informationen nicht erforderlich.</p></td>
</tr>
</tbody>
</table>



## Betriebssysteme


Verwenden Sie die Steuerelemente für **Betriebssysteme** , um die Betriebssystemanforderungen der Anwendung anzugeben. Wenn ein Application Virtualization Desktop-Client keines der ausgewählten Betriebssysteme unterstützt, wird die Anwendung nicht gestartet.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Steuerelemente</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Verfügbare Betriebssysteme</strong></p></td>
<td align="left"><p>Zeigt eine Liste der Betriebssysteme an, die die Anwendungen im Paket unterstützen können.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ausgewählte Betriebssysteme</strong></p></td>
<td align="left"><p>Zeigt eine Liste der ausgewählten Betriebssysteme an, die die Anwendungen im Paket unterstützen.</p></td>
</tr>
</tbody>
</table>



## Ausgabeoptionen


Verwenden Sie die Steuerelemente für **Ausgabeoptionen** , um die Ausgabeoptionen für die Anwendung anzugeben, die installiert werden soll.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Steuerelement</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Komprimierungsalgorithmus</strong></p></td>
<td align="left"><p>Hiermit wählen Sie die Methode zum Komprimieren der SFT-Datei für das Streaming in einem Netzwerk aus. Wählen Sie eine der folgenden Komprimierungsmethoden aus:</p>
<ul>
<li><p><strong>Komprimiert </strong> : gibt an, dass die SFT-Datei im zlib-Format komprimiert werden soll <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> </a> .</p></li>
<li><p><strong>Nicht komprimiert </strong> – Standard; gibt an, dass die SFT-Datei nicht komprimiert werden soll.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Erzwingen von Sicherheitsbeschreibungen</strong></p></td>
<td align="left"><p>Wählen Sie diese Option aus, um Sicherheitsbeschreibungen der Anwendungen im Paket zu erzwingen, nachdem Sie für den Client bereitgestellt wurden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Generieren des Microsoft Windows Installer-Pakets (MSI)</strong></p></td>
<td align="left"><p>Wählen Sie aus, ob Sie ein sequenziertes Anwendungspaket mit dem Windows Installer installieren oder bereitstellen möchten. Wenn Sie mit dem Sequencer Änderungen vorgenommen haben, werden die Änderungen nicht in die Windows Installer-Datei übernommen. Die Windows Installer-Datei wird immer unter Verwendung der auf der Festplatte gespeicherten SFT-Datei erstellt.</p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[So ändern Sie die Bereitstellungseigenschaften](how-to-change-deployment-properties.md)

[Sequencer Console](sequencer-console.md)









