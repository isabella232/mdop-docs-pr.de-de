---
title: Bereitstellen des App-V 5.0-Servers
description: Bereitstellen des App-V 5.0-Servers
author: dansimp
ms.assetid: a47f0dc8-2971-4e4d-8d57-6b69bbed4b63
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8fb65015a172a88d5e27d377037348dbc044654
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805828"
---
# Bereitstellen des App-V 5.0-Servers


Sie können die App-V 5,0-Server Features mithilfe verschiedener Bereitstellungskonfigurationen installieren, die in diesem Thema beschrieben werden. Bevor Sie die Server Features installieren, lesen Sie den Abschnitt Server der [Sicherheitsüberlegungen zu App-V 5,0](app-v-50-security-considerations.md).

Informationen zum Bereitstellen des App-v 5,0 SP3-Servers finden Sie unter [Informationen zu app-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).

**Wichtig**  Bevor Sie die App-V 5,0-Server installieren und konfigurieren, müssen Sie einen Port angeben, in dem die einzelnen Komponenten gehostet werden. Sie müssen auch die zugehörigen Firewallregeln hinzufügen, damit eingehende Anforderungen auf die angegebenen Ports zugreifen können. Das Installationsprogramm ändert keine Firewalleinstellungen.

 

## <a href="" id="---------app-v-5-0-server-overview"></a> App-V 5,0 Server – Übersicht


Der App-V 5,0-Server besteht aus fünf Komponenten. Jede Komponente dient in der App-V 5,0-Umgebung einem anderen Zweck. Jede der fünf Komponenten wird hier kurz beschrieben:

-   Verwaltungs Server – bietet allgemeine Verwaltungsfunktionen für die App-V 5,0-Infrastruktur.

-   Verwaltungsdatenbank – ermöglicht die Bereitstellung von Datenbankbereitstellungen für die App-V 5,0-Verwaltung.

-   Publishing Server – bietet Hosting-und Streamingfunktionen für virtuelle Anwendungen.

-   Reporting Server – bietet App-V 5,0 Reporting Services.

-   Berichtsdatenbank – ermöglicht die Bereitstellung von Datenbanken für App-V 5,0-Berichterstellung.

## <a href="" id="---------app-v-5-0-stand-alone-deployment"></a> App-V 5,0 eigenständige Bereitstellung


Die eigenständige App-V 5,0-Bereitstellung bietet eine gute Topologie für eine kleine Bereitstellung oder eine Testumgebung. Wenn Sie diese Art von Implementierung verwenden, werden alle Server Komponenten auf einem einzelnen Computer bereitgestellt. Die Dienste und zugehörigen Datenbanken konkurrieren um die Ressourcen auf dem Computer, auf dem die App-V 5,0-Komponenten ausgeführt werden. Daher sollten Sie diese Topologie nicht für größere Bereitstellungen verwenden.

[So stellen Sie den App-V 5.0-Server bereit](how-to-deploy-the-app-v-50-server-50sp3.md)

[So stellen Sie den App-V 5.0-Server mithilfe eines Skripts bereit](how-to-deploy-the-app-v-50-server-using-a-script.md)

## <a href="" id="---------app-v-5-0-server-distributed-deployment"></a> App-V 5,0 Server – verteilte Bereitstellung


Die verteilte Bereitstellungstopologie kann eine große App-V 5,0-Clientbasis unterstützen, sodass Sie Ihre Umgebung einfacher verwalten und skalieren können. Wenn Sie diese Art der Bereitstellung verwenden, werden die App-V 5,0-Server Komponenten basierend auf der Struktur und den Anforderungen der Organisation auf mehreren Computern bereitgestellt.

[So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

[So stellen Sie den App-V 5.0-Server mithilfe eines Skripts bereit](how-to-deploy-the-app-v-50-server-using-a-script.md)

[So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer](how-to-install-the-publishing-server-on-a-remote-computer.md)

[So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

## Verwenden einer ESD-Lösung (Enterprise Software Distribution) und App-V 5,0


Sie können die APP-v 5,0-Clients und-Pakete auch mithilfe eines ESD bereitstellen, ohne APP-v 5,0 bereitstellen zu müssen. Die vollständigen Funktionen für die Integration sind je nach verwendetem ESD unterschiedlich.

**Hinweis**  Der APP-v 5,0-Berichtsserver und die Berichtsdatenbank können neben dem ESD weiterhin bereitgestellt werden, um die Berichtsdaten von den App-v 5,0-Clients zu erfassen. Die anderen drei Server Komponenten sollten jedoch nicht bereitgestellt werden, da Sie mit der ESD-Funktionalität in Konflikt stehen.

 

[Bereitstellen von App-V 5.0-Paketen mithilfe einer ESD-Lösung (Electronic Software Distribution)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-0-server-logs"></a> App-V 5,0-Server Protokolle


Sie können APP-v 5,0 Server-Protokollinformationen verwenden, um bei der Verwendung von App-v 5,0 bei der Behandlung von Server Installations-und Betriebsereignissen zu helfen. Die serverbezogenen Protokollinformationen können mit der **Ereignisanzeige**überprüft werden. In der folgenden Zeile wird der spezifische Pfad für Server bezogene Ereignisse angezeigt:

**Ereignisanzeige \ \ Anwendungen und Dienstprotokolle \ \ Microsoft \ \ App V**

Zugeordnete Setupprotokolle werden im folgenden Verzeichnis gespeichert:

**Temp**

In App-V 5,0 SP3 wurden einige Protokolle konsolidiert und verschoben. Informationen finden Sie unter [App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

## <a href="" id="---------app-v-5-0-reporting"></a> App-V 5,0-Berichterstellung


App-v 5,0-Berichterstellung ermöglicht es App-v 5,0-Clients, Daten zu sammeln und dann zurückzusenden, damit Sie in einem zentralen Repository gespeichert werden. Sie können diese Informationen verwenden, um eine bessere Sicht auf die Verwendung der virtuellen Anwendung in Ihrer Organisation zu erhalten. In der folgenden Liste werden einige der Arten von Informationen angezeigt, die der App-V 5,0-Client sammelt:

-   Informationen zu dem Computer, auf dem der App-V 5,0-Client ausgeführt wird.

-   Informationen zu virtualisierten Paketen auf einem bestimmten Computer, auf dem der App-V 5,0-Client ausgeführt wird.

-   Informationen zum Öffnen und Herunterfahren des Pakets für einen bestimmten Benutzer.

Die Berichterstattungs Informationen werden so lange verwaltet, bis Sie erfolgreich an die Berichtsserver-Datenbank gesendet werden. Nachdem sich die Daten in der Datenbank befinden, können Sie Microsoft SQL Server Reporting Services verwenden, um alle erforderlichen Berichte zu generieren.

Wenn Sie Berichtsinformationen abrufen möchten, müssen Sie Microsoft SQL Server Reporting Services (SSRS) verwenden, das in Microsoft SQL verfügbar ist. SSRS wird nicht installiert, wenn Sie den App-V 5,0-Berichtsserver installieren und separat bereitgestellt werden muss, um die zugehörigen Berichte zu generieren.

Verwenden Sie den folgenden Link, um weitere Informationen [zur App-V 5,0-Berichterstellung](about-app-v-50-reporting.md)zu erhalten.

[So aktivieren Sie die Berichterstellung auf dem App-V 5.0-Client mithilfe von PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

## Weitere Ressourcen für den App-V-Server


[Bereitstellen von App-V 5.0](deploying-app-v-50.md)






 

 





