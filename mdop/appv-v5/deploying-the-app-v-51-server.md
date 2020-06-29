---
title: Bereitstellen des App-V 5.1-Servers
description: Bereitstellen des App-V 5.1-Servers
author: dansimp
ms.assetid: 987b61dc-00d6-49ba-8f1b-92d7b948e702
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bcff2a3211ea3e2f666aff1d6f2ad919509aa3a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805822"
---
# Bereitstellen des App-V 5.1-Servers

Sie können die 5,1-Server Features von Microsoft Application Virtualization (App-V) mithilfe verschiedener Bereitstellungskonfigurationen installieren, die in diesem Thema beschrieben werden. Bevor Sie die Server Features installieren, lesen Sie den Abschnitt Server der [Sicherheitsüberlegungen zu App-V 5,1](app-v-51-security-considerations.md).

Informationen zum Bereitstellen des App-v-Servers finden Sie unter Informationen [zu app-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).

> [!IMPORTANT]
> Bevor Sie die App-V 5,1-Server installieren und konfigurieren, müssen Sie einen Port angeben, in dem die einzelnen Komponenten gehostet werden. Sie müssen auch die zugehörigen Firewallregeln hinzufügen, damit eingehende Anforderungen auf die angegebenen Ports zugreifen können. Das Installationsprogramm ändert keine Firewalleinstellungen.

## <a href="" id="---------app-v-5-1-server-overview"></a> App-V 5,1 Server – Übersicht

Der App-V 5,1-Server besteht aus fünf Komponenten. Jede Komponente dient in der App-V 5,1-Umgebung einem anderen Zweck. Jede der fünf Komponenten wird hier kurz beschrieben:

- Verwaltungs Server – bietet allgemeine Verwaltungsfunktionen für die App-V 5,1-Infrastruktur.
- Verwaltungsdatenbank – ermöglicht die Bereitstellung von Datenbankbereitstellungen für die App-V 5,1-Verwaltung.
- Publishing Server – bietet Hosting-und Streamingfunktionen für virtuelle Anwendungen.
- Reporting Server – bietet App-V 5,1 Reporting Services.
- Berichtsdatenbank – ermöglicht die Bereitstellung von Datenbanken für App-V 5,1-Berichterstellung.

## <a href="" id="---------app-v-5-1-stand-alone-deployment"></a> App-V 5,1 eigenständige Bereitstellung

Die eigenständige App-V 5,1-Bereitstellung bietet eine gute Topologie für eine kleine Bereitstellung oder eine Testumgebung. Wenn Sie diese Art von Implementierung verwenden, werden alle Server Komponenten auf einem einzelnen Computer bereitgestellt. Die Dienste und zugehörigen Datenbanken konkurrieren um die Ressourcen auf dem Computer, auf dem die App-V 5,1-Komponenten ausgeführt werden. Daher sollten Sie diese Topologie nicht für größere Bereitstellungen verwenden.

[So stellen Sie den App-V 5.1-Server bereit](how-to-deploy-the-app-v-51-server.md)

[So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit](how-to-deploy-the-app-v-51-server-using-a-script.md)

## <a href="" id="---------app-v-5-1-server-distributed-deployment"></a> App-V 5,1 Server – verteilte Bereitstellung

Die verteilte Bereitstellungstopologie kann eine große App-V 5,1-Clientbasis unterstützen, sodass Sie Ihre Umgebung einfacher verwalten und skalieren können. Wenn Sie diese Art der Bereitstellung verwenden, werden die App-V 5,1-Server Komponenten basierend auf der Struktur und den Anforderungen der Organisation auf mehreren Computern bereitgestellt.

[So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

[So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit](how-to-deploy-the-app-v-51-server-using-a-script.md)

[So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

## Verwenden einer ESD-Lösung (Enterprise Software Distribution) und App-V 5,1

Sie können die APP-v 5,1-Clients und-Pakete auch mithilfe eines ESD bereitstellen, ohne APP-v 5,1 bereitstellen zu müssen. Die vollständigen Funktionen für die Integration sind je nach verwendetem ESD unterschiedlich.

> [!NOTE]
> Der APP-v 5,1-Berichtsserver und die Berichtsdatenbank können neben dem ESD weiterhin bereitgestellt werden, um die Berichtsdaten von den App-v 5,1-Clients zu erfassen. Die anderen drei Server Komponenten sollten jedoch nicht bereitgestellt werden, da Sie mit der ESD-Funktionalität in Konflikt stehen.

[Bereitstellen von App-V 5.1-Paketen mithilfe einer ESD-Lösung (Electronic Software Distribution)](deploying-app-v-51-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-1-server-logs"></a> App-V 5,1-Server Protokolle

Sie können APP-v 5,1 Server-Protokollinformationen verwenden, um bei der Verwendung von App-v 5,1 bei der Behandlung von Server Installations-und Betriebsereignissen zu helfen. Die serverbezogenen Protokollinformationen können mit der **Ereignisanzeige**überprüft werden. In der folgenden Zeile wird der spezifische Pfad für Server bezogene Ereignisse angezeigt:

**Ereignisanzeige \ \ Anwendungen und Dienstprotokolle \ \ Microsoft \ \ App V**

Zugeordnete Setupprotokolle werden im folgenden Verzeichnis gespeichert:

**Temp**

In App-V 5,0 SP3 wurden einige Protokolle konsolidiert und verschoben. Informationen finden Sie unter [App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

## <a href="" id="---------app-v-5-1-reporting"></a> App-V 5,1-Berichterstellung

App-v 5,1-Berichterstellung ermöglicht es App-v 5,1-Clients, Daten zu sammeln und dann zurückzusenden, damit Sie in einem zentralen Repository gespeichert werden. Sie können diese Informationen verwenden, um eine bessere Sicht auf die Verwendung der virtuellen Anwendung in Ihrer Organisation zu erhalten. In der folgenden Liste werden einige der Arten von Informationen angezeigt, die der App-V 5,1-Client sammelt:

- Informationen zu dem Computer, auf dem der App-V 5,1-Client ausgeführt wird.
- Informationen zu virtualisierten Paketen auf einem bestimmten Computer, auf dem der App-V 5,1-Client ausgeführt wird.
- Informationen zum Öffnen und Herunterfahren des Pakets für einen bestimmten Benutzer.

Die Berichterstattungs Informationen werden so lange verwaltet, bis Sie erfolgreich an die Berichtsserver-Datenbank gesendet werden. Nachdem sich die Daten in der Datenbank befinden, können Sie Microsoft SQL Server Reporting Services verwenden, um alle erforderlichen Berichte zu generieren.

Wenn Sie Berichtsinformationen abrufen möchten, müssen Sie Microsoft SQL Server Reporting Services (SSRS) verwenden, das in Microsoft SQL verfügbar ist. SSRS wird nicht installiert, wenn Sie den App-V 5,1-Berichtsserver installieren und separat bereitgestellt werden muss, um die zugehörigen Berichte zu generieren.

Verwenden Sie den folgenden Link, um weitere Informationen [zur App-V 5,1-Berichterstellung](about-app-v-51-reporting.md)zu erhalten.

[So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)

## Weitere Ressourcen für den App-V-Server

[Bereitstellen von App-V 5.1](deploying-app-v-51.md)
