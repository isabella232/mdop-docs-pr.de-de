---
title: Planen der Bereitstellung des App-V 5.0-Servers
description: Planen der Bereitstellung des App-V 5.0-Servers
author: dansimp
ms.assetid: fd89b324-3961-471a-ad90-c8f9ae7a8155
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06c7c17fd081b89337bbecd31f20f6796338f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804991"
---
# Planen der Bereitstellung des App-V 5.0-Servers


Die Microsoft Application Virtualization (App-V) 5,0 Server-Infrastruktur besteht aus einer Reihe spezieller Features, die basierend auf den Anforderungen des Unternehmens auf einem oder mehreren Server Computern installiert werden können.

## Planen der App-V 5,0-Server Bereitstellung


Der App-V 5,0-Server besteht aus den folgenden Features:

-   Verwaltungs Server – bietet allgemeine Verwaltungsfunktionen für die App-V 5,0-Infrastruktur.

-   Verwaltungsdatenbank – ermöglicht die Bereitstellung von Datenbankbereitstellungen für die App-V 5,0-Verwaltung.

-   Publishing Server – bietet Hosting-und Streamingfunktionen für virtuelle Anwendungen.

-   Reporting Server – bietet App-V 5,0 Reporting Services.

-   Berichtsdatenbank – ermöglicht die Bereitstellung von Datenbanken für App-V 5,0-Berichterstellung.

In der folgenden Liste werden die empfohlenen Methoden zum Installieren der App-V 5,0-Serverinfrastruktur angezeigt:

-   Installieren Sie den App-V 5,0-Server. Weitere Informationen finden Sie unter [Bereitstellen des App-V 5,0-Servers](how-to-deploy-the-app-v-50-server-50sp3.md).

-   Installieren Sie die Datenbank-, Berichterstattungs-und Verwaltungsfeatures auf separaten Computern. Weitere Informationen finden Sie unter [so wird es gemacht: Installieren der Verwaltungs-und Berichtsdatenbanken auf separaten Computern über die Verwaltungs-und Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md).

-   Verwenden Sie Electronic Software Distribution (ESD). Weitere Informationen finden Sie unter [Bereitstellen von App-V 5,0-Paketen mithilfe der elektronischen Software Verteilung](how-to-deploy-app-v-50-packages-using-electronic-software-distribution.md).

-   Installieren Sie alle Server Features auf einem einzelnen Computer.

## <a href="" id="---------app-v-5-0-server-interaction"></a> App-V 5,0-Server Interaktion


Dieser Abschnitt enthält Informationen dazu, wie die verschiedenen App-V 5,0-Serverrollen miteinander interagieren.

Der App-V 5,0-Verwaltungs Server enthält das Repository der Pakete und deren zugewiesene Konfigurationen. Bei Veröffentlichungsservern, die beim Verwaltungs Server registriert sind, werden die zugehörigen Metadaten den Veröffentlichungsservern zur Verwendung bereitgestellt, wenn Veröffentlichungs Aktualisierungsanforderungen von Computern mit dem App-V 5,0-Client empfangen werden. App-V 5,0-Publishing Server, die von einem einzelnen Verwaltungsserver verwaltet werden, können verschiedene Clients bedienen und unterschiedliche Websitenamen und Portbindungen aufweisen. Darüber hinaus sind alle Veröffentlichungsserver, die vom gleichen Verwaltungs Server verwaltet werden, Replikate voneinander.

**Hinweis**  Der Verwaltungs Server führt keinen Lastenausgleich aus. Die zugehörigen Metadaten werden einfach an den Veröffentlichungsserver übergeben, um Sie für die Verarbeitung von Clientanforderungen zu verwenden.

 

## Server bezogene Protokolle und externe Features


Im folgenden werden Informationen zu serverbezogenen Protokollen angezeigt, die von den App-V 5,0-Servern verwendet werden. Die Tabelle enthält auch den Berichterstellungsmechanismus für die einzelnen Servertypen.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Servertyp</th>
<th align="left">Protokolle</th>
<th align="left">Erforderliche externe Features</th>
<th align="left">Berichterstellung</th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IIS-Server</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Diese Server-Protokoll-Kombination erfordert einen Mechanismus zum Synchronisieren des Inhalts zwischen dem Management-Server und dem Streaming-Server. Verwenden Sie bei Verwendung von http oder HTTPS einen IIS-Server und eine Firewall, um den Server vor der Gefährdung durch das Internet zu schützen.</p></td>
<td align="left"><p>Intern</p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p>Datei</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>Diese Server-Protokoll-Kombination erfordert Unterstützung, um den Inhalt zwischen dem Verwaltungsserver und dem Streamingserver zu synchronisieren. Verwenden Sie einen Clientcomputer mit Dateifreigabe-oder Streaming-Funktion.</p></td>
<td align="left"><p>Intern</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## Verwandte Themen


[Planen der Bereitstellung von App-V](planning-to-deploy-app-v.md)

[Bereitstellen des App-V 5.0-Servers](deploying-the-app-v-50-server.md)

 

 





