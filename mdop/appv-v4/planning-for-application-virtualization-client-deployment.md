---
title: Planen der Bereitstellung von Application Virtualization Client
description: Planen der Bereitstellung von Application Virtualization Client
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806512"
---
# Planen der Bereitstellung von Application Virtualization Client


Nachdem Sie entschieden haben, wie Sie virtuelle Anwendungspakete auf Ihren Endbenutzercomputern veröffentlichen und bereitstellen, sollten Sie die Bereitstellung der Application Virtualization-Client Software planen.

Application Virtualization Client ist die Komponente, in der die virtuellen Anwendungen tatsächlich ausgeführt werden. Der Application Virtualization-Client ermöglicht Benutzern die Interaktion mit Symbolen und das Doppelklicken auf Dateitypen, um eine virtuelle Anwendung zu starten. Darüber hinaus wird das Streaming der Anwendungsinhalte von einem Streamingserver verarbeitet und zwischengespeichert, bevor die Anwendung gestartet wird. Der Anwendungsinhalt ist so strukturiert, dass der gesamte Inhalt, der zum Starten der Anwendung und zur Behandlung der anfänglichen Benutzerinteraktion benötigt wird, zuerst an den Endbenutzercomputer gestreamt wird. Es gibt zwei verschiedene Arten von Application Virtualization-Client Software: den Application Virtualization Client für Remotedesktopdienste (ehemals Terminal Dienste), der auf Server Systemen für den Remote Desktop-Sitzungshost (RDSession-Host) und dem Application Virtualization-Desktop Client verwendet wird, der für alle anderen Computer verwendet wird.

Der Application Virtualization-Client sollte zur Installationszeit entweder in der Application Virtualization-Verwaltungskonsole oder über die Befehlszeile des Installationsprogramms mit einer Reihe wichtiger Einstellungen konfiguriert werden, einschließlich der folgenden:

-   Speicherorte der Symbole für alle Anwendungen

-   Der Speicherort der OSD-Datei, die die Paketdefinitionsinformationen enthält.

-   Die Inhaltsquelle der Anwendung.

-   Das Kommunikationsprotokoll, das beim Abrufen der vorhergehenden Elemente verwendet werden soll.

-   Die zu verwendende Cachegröße und-Verwaltungsmethode.

Um die Bereitstellung der Application Virtualization-Client Software zu beschleunigen, wenn Sie eine ESD-Lösung (Electronic Software Distribution) verwenden, müssen die vorhergehenden Einstellungen im Voraus sorgfältig definiert werden. Dies ist besonders wichtig, wenn Sie Computer in verschiedenen Niederlassungen haben, deren Clients für die Verwendung unterschiedlicher Quellspeicherorte konfiguriert werden müssen.

**Hinweis:**  
-   Die Werte für Symbolposition und OSD-Datei sind ein wichtiger Faktor, der bei der Auswahl der Veröffentlichungsmethode berücksichtigt werden muss, egal, ob Sie Windows Installer oder SFTMIME verwenden. Die Einstellung für die Inhaltsquelle der Anwendung wird durch Ihre Wahl der Streaming-Methode definiert.

-   Wenn Sie sicherstellen möchten, dass der Cache über genügend Speicherplatz für alle Pakete verfügt, die möglicherweise bereitgestellt werden, verwenden Sie die Einstellung Speicher **Platz für freien Speicherplatz verwenden** , wenn Sie den Client so konfigurieren, dass der Cache nach Bedarf erweitert werden kann. Sie können aber auch im voraus ermitteln, wie viel Speicherplatz für den App-V-Cache benötigt wird, und die Cachegröße zur Installationszeit entsprechend festlegen. Weitere Informationen zum Cache Space Management-Feature finden Sie unter **Verwenden des Cache-Speicherplatz Verwaltungsfeatures** im Microsoft Application Virtualization (App-V)-Betriebsleitfaden.

-   Während der Veröffentlichungs-und http (S)-Streaming-Vorgänge verwenden App-V 4,5 SP1-Clients die Proxyservereinstellungen, die in Internet Explorer auf dem Computer des Benutzers konfiguriert sind.

Weitere Informationen zum Konfigurieren der Client Installationsparameter finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).

 

Schließlich müssen Sie ermitteln, wie die Application Virtualization-Desktop Client Software für die Desktop Clients bereitgestellt wird. Obwohl es möglich ist, den Application Virtualization Desktop Client manuell auf jedem Computer bereitzustellen, müssten die meisten Organisationen dies über einen automatisierten Prozess durchführen. Bei einer mittleren oder großen Organisation ist möglicherweise ein ESD-System in Betrieb, was eine ideale Möglichkeit zum Bereitstellen des Clients darstellt. Wenn kein ESD-System vorhanden ist, können Sie die Standardmethode zur Installation von Software in Ihrer Organisation verwenden. Zu den Auswahlmöglichkeiten gehören Gruppenrichtlinien oder verschiedene Skripttechniken. Je nach Anzahl und Größe der Offices, die Sie haben, kann dieser Bereitstellungsprozess komplex sein, und es ist wichtig, dass Sie einen strukturierten Ansatz Unternehmen, um sicherzustellen, dass alle Computer einen Client mit der richtigen Konfiguration installieren.

## Verwandte Themen


[Planen der Bereitstellung von Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

[So installieren Sie den Client über die Befehlszeile](how-to-install-the-client-by-using-the-command-line-new.md)

[So veröffentlichen Sie eine virtuelle Anwendung auf dem Client](how-to-publish-a-virtual-application-on-the-client.md)

[So aktualisieren Sie Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)

[So deinstallieren Sie App-V Client](how-to-uninstall-the-app-v-client.md)

 

 





