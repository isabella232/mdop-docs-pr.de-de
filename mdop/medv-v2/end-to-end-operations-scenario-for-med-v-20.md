---
title: End-to-End-Vorgangsszenario für MED-V 2.0
description: End-to-End-Vorgangsszenario für MED-V 2.0
author: dansimp
ms.assetid: 1d87f5f3-9fc5-4731-8bd1-c155714f34ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90a7c2135ad27040ed87dac980b67321eb771574
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811593"
---
# End-to-End-Vorgangsszenario für MED-V 2.0


Dieses Beispielszenario für Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 unterstützt Sie beim Bereitstellen und Verwalten von Med-v mithilfe mehrerer Szenarien, die End-to-End verwendet werden. Sie können sich dieses Beispielszenario als eine Fallstudie vorstellen, die dazu beiträgt, die einzelnen Szenarien und Prozeduren im Kontext zu platzieren.

Dieser Abschnitt enthält grundlegende Informationen und Anweisungen zum Erstellen, bereitstellen und Verwalten von MED-V-Arbeitsbereichen als End-to-End-Lösung in Ihrem Unternehmen.

## Schritt-für-Schritt-Szenario für MED-V-Vorgänge


Zu den schrittweisen Verfahren, die Sie in einem MED-V-Szenario ausführen, gehören die folgenden:

-   [Erstellen eines Windows Virtual PC-Images für med-v](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc) überprüft, wie ein Windows Virtual PC-Abbild für med-v erstellt und konfiguriert wird. Bevor Sie einen Med-v-Arbeitsbereich für Benutzer bereitstellen können, müssen Sie zuerst eine virtuelle Festplatte (VHD) vorbereiten, die Sie zum Erstellen des Med-v Workspace-Installationspakets für med-v verwenden.

-   [Erstellen eines Windows Virtual PC-Images für MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingwindowsxpontovpc) überprüft, wie Sie das BetriebssystemWindows XP SP3 auf Ihrem Windows Virtual PC-Abbild installieren. Für med-v muss Windows XP SP3 auf dem Windows Virtual PC-Abbild installiert sein, bevor Sie den Med-v-Arbeitsbereich erstellen.

-   [Erstellen eines Windows Virtual PC-Images für med-v](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingnet) überprüft, wie Sie das .NET Framework 3,5 SP1 und das Update KB959209 manuell in das Windows Virtual PC-Abbild installieren, das Sie für die Verwendung mit Med-v vorbereiten. MED-V erfordert .NET Framework 3,5 SP1 und das Update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) behebt verschiedene bekannte Anwendungskompatibilitätsprobleme.

-   [Erstellen eines Windows Virtual PC-Images für med-v](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-applypatchestovpc) überprüft, wie Sie Ihr Windows XP-Abbild mit den neuesten Softwareupdates und anderen Hotfixes aktualisieren können, die für die Ausführung von Med-v erforderlich oder wichtig sind.

-   [Erstellen eines Windows Virtual PC-Images für MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installintegration) überprüft, wie das Integrationskomponenten-Paket in Ihrem Windows XP-Abbild installiert wird. Diese Funktionen bieten Features, die die Interaktion zwischen der virtuellen Umgebung und dem physikalischen Computer verbessern.

-   Beim [Installieren von Anwendungen auf einem Windows Virtual PC-Bild](installing-applications-on-a-windows-virtual-pc-image.md) wird erläutert, wie Sie bestimmte Arten von Software auf Ihrem Windows XP-Abbild installieren können, die bei der Ausführung von MED-V hilfreich sind, beispielsweise ein elektronisches Softwareverteilungssystem und eine Antivirus-Software.

-   Beim [Konfigurieren eines Windows Virtual PC-Images für med-v](configuring-a-windows-virtual-pc-image-for-med-v.md) wird erläutert, wie Sie das Bild mithilfe von Sysprep konfigurieren, um sicherzustellen, dass es für med-v verwendet werden kann. Das vorbereitete Med-v-Bild wird dann zum Erstellen Ihres Med-v-Arbeitsbereichs Pakets verwendet.

-   [Erstellen eines Med-v Workspace-Pakets](create-a-med-v-workspace-package.md) hier erfahren Sie, wie Sie das Med-v Workspace-Paket erstellen, das Sie im gesamten Unternehmen bereitstellen. Sie stellen das Med-v Workspace-Paket bereit, um den Med-v-Arbeitsbereich auf Endbenutzercomputern zu installieren. Ein Med-v-Arbeitsbereich ist die Windows XP-Desktopumgebung, von der Endbenutzer mit dem virtuellen Computer interagieren, der von Med-v bereitgestellt wird.

-   Beim [Testen des Med-v Workspace-Pakets](testing-the-med-v-workspace-package.md) wird erläutert, wie Sie eine Testumgebung erstellen, in der Sie die Funktionalität des Med-v Workspace-Pakets testen können, beispielsweise Einstellungen für die erstmalige Einrichtung und Anwendungsveröffentlichung. Nachdem Sie das Testen des MED-V-Arbeitsbereichs Pakets abgeschlossen haben und überprüft haben, dass es wie beabsichtigt funktioniert, können Sie es im gesamten Unternehmen bereitstellen.

-   [Beim Bereitstellen des Med-v-Arbeitsbereichs Pakets](deploying-the-med-v-workspace-package.md) wird erläutert, wie der Med-v-Arbeitsbereich mithilfe eines elektronischen Softwareverteilungssystems oder in einem Windows 7-Abbild bereitgestellt wird. Oder wenn Sie es vorziehen, zeigt Ihnen dieser Abschnitt auch, wie Sie den MED-V-Arbeitsbereich manuell bereitstellen können.

-   [Überwachen von Med-v-Arbeitsbereichen](monitor-med-v-workspaces.md) überprüft, wie Sie die Bereitstellung von Med-v-Arbeitsbereichen überwachen, um zu ermitteln, ob das erstmalige Setup erfolgreich abgeschlossen wurde. Das Überwachen des Erfolgs der erstmaligen Einrichtung ist wichtig, da sich MED-V erst dann in einem brauchbaren Zustand befindet, wenn die erstmalige Einrichtung erfolgreich abgeschlossen wurde. In diesem Abschnitt wird auch gezeigt, wie Sie Ihre Umgebung einrichten können, um die Netzwerkänderungen zu erkennen, die sich auf MED-V auswirken können.

-   [Verwalten von Med-v Workspace-Anwendungen](manage-med-v-workspace-applications.md) überprüft, wie Anwendungen in einem bereitgestellten Med-v-Arbeitsbereich installiert und entfernt oder veröffentlicht werden. In diesem Abschnitt wird auch gezeigt, wie Sie Software in einem MED-V-Arbeitsbereich manuell aktualisieren und wie Sie automatische Updates verwalten. Der MED-V-Arbeitsbereich ist ein virtueller Computer, der ein separates Betriebssystem enthält, dessen automatischer Softwareupdateprozess genau wie die physischen Computer in Ihrem Unternehmen verwaltet werden muss.

-   [Verwalten der Med-v-URL-Umleitung](manage-med-v-url-redirection.md) überprüft, wie Sie Webadressen-Umleitungseinstellungen für den bereitgestellten Med-v-Arbeitsbereich hinzufügen und entfernen. Sie können URL-Umleitungsinformationen über die Registrierung oder durch erneutes Erstellen des MED-V-Arbeitsbereichs hinzufügen oder entfernen. Sie können auch den Assistenten für den MED-V-Arbeitsbereichs-Paketdienst verwenden, um die Webadressen Umleitung zu verwalten.

-   [Verwalten von Med-v Workspace-Einstellungen](manage-med-v-workspace-settings.md) überprüft, wie Sie Med-v-Konfigurationseinstellungen mithilfe des Med-v-Arbeitsbereichs-Packagers anzeigen und bearbeiten. In diesem Abschnitt werden alle konfigurierbaren MED-V-Registrierungsschlüssel aufgelistet, die jeweils den Typ, den Standard und die Beschreibung enthalten. Dieser Abschnitt enthält auch Informationen zum Verwalten von Druckern in MED-V-Arbeitsbereichen. In Med-v 2,0 bietet die Druckerumleitung Benutzern eine konsistente Druckfunktionalität zwischen dem Med-v-virtuellen Computer und dem Hostcomputer.

## Verwandte Themen


[Vorgänge für MED-V](operations-for-med-v.md)

[End-to-End-Planungszenario für MED-V 2.0](end-to-end-planning-scenario-for-med-v-20.md)

[End-to-End-Bereitstellungsszenario für MED-V 2.0](end-to-end-deployment-scenario-for-med-v-20.md)

 

 





