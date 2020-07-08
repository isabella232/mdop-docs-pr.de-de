---
title: Bereitstellen von App-V 5.0-Sequencer und -Client
description: Bereitstellen von App-V 5.0-Sequencer und -Client
author: dansimp
ms.assetid: 84cc84bd-5bc0-41aa-9519-0ded2932c078
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 647ea12018bf966592b9e831d532c7c08093d367
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805846"
---
# Bereitstellen von App-V 5.0-Sequencer und -Client


Mit dem App-V 5,0-Sequenzer und-Client können Administratoren virtualisierte Anwendungen virtualisieren und ausführen.

## Bereitstellen des Clients


Der App-V 5,0-Client ist die Komponente, die eine virtualisierte Anwendung auf einem Zielcomputer ausführt. Der Client ermöglicht Benutzern die Interaktion mit Symbolen und das Doppelklicken auf Dateitypen, damit Sie eine virtualisierte Anwendung starten können. Der Client kann auch den Inhalt der virtuellen Anwendung vom Verwaltungsserver abrufen.

[So stellen Sie App-V-Client bereit](how-to-deploy-the-app-v-client-gb18030.md)

[So deinstallieren Sie den App-V 5.0-Client](how-to-uninstall-the-app-v-50-client.md)

[Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## Client Konfigurationseinstellungen


Der App-V 5,0-Client speichert seine Konfiguration in der Registrierung. Sie können einige nützliche Informationen zu dem Client sammeln, wenn Sie das Format der Daten in der Registrierung verstehen. Sie können auch viele Clientaktionen konfigurieren, indem Sie Registrierungseinträge ändern.

[Informationen über Clientkonfigurationseinstellungen](about-client-configuration-settings.md)

## Konfigurieren des Clients mithilfe der ADMX-Vorlage und der Gruppenrichtlinie


Sie können die Vorlage Microsoft ADMX verwenden, um die Clienteinstellungen für den App-V 5,0-Client und den Remote Desktop Dienste-Client zu konfigurieren. Die ADMX-Vorlage verwaltet allgemeine Clientkonfigurationen mithilfe einer vorhandenen Gruppenrichtlinieninfrastruktur und umfasst Einstellungen für die App-V 5,0-Clientkonfiguration.

**Wichtig**  Sie können die App-V 5,0 ADMX-Vorlage aus dem Microsoft Download Center abrufen.

 

Nachdem Sie die ADMX-Vorlage heruntergeladen und installiert haben, führen Sie die folgenden Schritte auf dem Computer aus, den Sie zum Verwalten von Gruppenrichtlinien verwenden werden. Dies ist normalerweise der Domänen Controller.

1.  Speichern Sie die **ADMX-** Datei im folgenden Verzeichnis: **Windows \ \ PolicyDefinitions**

2.  Speichern Sie die **ADML-** Datei im folgenden Verzeichnis: **Windows \ \ PolicyDefinitions \ \ &lt; Language Directory &gt; **

Nachdem Sie die vorherigen Schritte ausgeführt haben, können Sie die Einstellungen für die App-V 5,0-Clientkonfiguration über die **Gruppenrichtlinien-Verwaltungs** Konsole verwalten.

Der App-V 5,0-Client speichert auch seine Konfiguration in der Registrierung. Sie können einige nützliche Informationen zu dem Client sammeln, wenn Sie das Format der Daten in der Registrierung verstehen. Sie können auch viele Clientaktionen konfigurieren, indem Sie Registrierungseinträge ändern.

[So ändern Sie die App-V 5.0-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

## Bereitstellen des Clients mithilfe des freigegebenen Inhaltsspeicher Modus


Der APP-v 5,0 Shared Content Store (SCS)-Modus ermöglicht es den SCS-App-v 5,0-Clients, virtualisierte Anwendungen auszuführen, ohne die zugehörigen Paketdaten lokal zu speichern. Alle erforderlichen virtualisierten Paketdaten werden über das Netzwerk übertragen. Daher sollten Sie den SCS-Modus nur in Umgebungen mit einer schnellen Verbindung verwenden. Sowohl die Remote Desktop Dienste (RDS) als auch die Standard Version des App-V 5,0-Clients werden im SCS-Modus unterstützt.

**Wichtig**  Wenn der APP-v 5,0-Client so konfiguriert ist, dass er im SCS-Modus ausgeführt wird, muss der Speicherort, von dem die APP-v 5,0-Pakete gestreamt werden, verfügbar sein, andernfalls schlägt das virtualisierte Paket fehl. Darüber hinaus empfehlen wir die Bereitstellung virtualisierter Anwendungen nicht auf Computern, auf denen der App-V 5,0-Client im SCS-Modus über das Internet ausgeführt wird.

 

Darüber hinaus ist das SCS kein physikalischer Speicherort, der virtualisierte Pakete enthält. Dieser Modus ermöglicht es dem App-V 5,0-Client, die erforderlichen virtualisierten Paketdaten über das Netzwerk zu streamen.

Der SCS-Modus ist in den folgenden Szenarien hilfreich:

-   VDI-Bereitstellungen (Virtual Desktop Infrastructure)

-   Remote Desktop Dienste (RDS)-Bereitstellungen

Um SCS in Ihrer Umgebung verwenden zu können, müssen Sie den App-V 5,0-Client aktivieren, damit er im SCS-Modus ausgeführt wird. Diese Einstellung sollte während der Installation angegeben werden. Standardmäßig ist der Client nicht für die Verwendung des SCS-Modus konfiguriert. Wenn Sie beabsichtigen, SCS zu verwenden, sollten Sie den Client mithilfe des vorgeschlagenen Verfahrens installieren. Sie können jedoch einen vorhandenen APP-v 5,0-Client so konfigurieren, dass er im SCS-Modus ausgeführt wird, indem Sie den folgenden PowerShell-Befehl auf dem Computer eingeben, auf dem der APP-v 5,0-Client ausgeführt wird:

**Satz-AppvClientConfiguration-SharedContentStoreMode 1**

Es kann vorkommen, dass der Administrator einige virtuelle Anwendungen auf dem Computer vorlädt, auf dem der App-V 5,0-Client im SCS-Modus ausgeführt wird. Dies kann mit PowerShell-Befehlen durchgeführt werden, um das Paket hinzuzufügen, zu veröffentlichen und bereitzustellen. Wenn ein Paket beispielsweise auf allen Computern bereits vorinstalliert ist, kann der Administrator das Paket mithilfe von PowerShell-Befehlen hinzufügen, veröffentlichen und bereitstellen. Das Paket konnte nicht über das Netzwerk gestreamt werden, da es lokal gespeichert werden würde.

[So installieren Sie den App-V 5.0-Client für den SCS-Modus (Shared Content Store)](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)

## Bereitstellen des Sequencers


Der Sequencer ist ein Tool, mit dem Standardanwendungen in virtuelle Pakete für die Bereitstellung auf Computern konvertiert werden, auf denen der App-V 5,0-Client ausgeführt wird. Der Sequencer hilft bei der Bereitstellungeines einfachen und vorhersehbaren Konvertierungsprozesses mit minimalen Änderungen an vorherigen Sequenzierungs Workflows. Darüber hinaus ermöglicht der Sequencer Benutzern die einfachere Konfiguration von Anwendungen, um Verbindungen virtualisierter Anwendungen zu ermöglichen.

Eine Liste der Änderungen im App-v 5,0-Sequenzer finden Sie unter [Neuerungen in App-v 5,0](whats-new-in-app-v-50.md).

[So installieren Sie den Sequencer](how-to-install-the-sequencer-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-client-and-sequencer-logs"></a> App-V 5,0-Client-und-Sequenzer-Protokolle


Sie können die Protokollinformationen für App-v 5,0-Sequencer verwenden, um bei der Behandlung von Sequencer-Installations-und-Betriebsereignissen bei Verwendung von App-v 5,0 zu helfen. Die Sequencer-bezogenen Protokollinformationen können mit der **Ereignisanzeige**überprüft werden. In der folgenden Zeile wird der spezifische Pfad für Sequenzer bezogene Ereignisse angezeigt:

**Ereignisanzeige \ \ Anwendungen und Dienstprotokolle \ \ Microsoft \ \ App V**. Sequencer-bezogene Ereignisse werden **AppV \ _Sequencer**vorangestellt. Client bezogene Ereignisse werden **AppV \ _Client**vorangestellt.

In App-V 5,0 SP3 wurden einige Protokolle konsolidiert. Informationen finden Sie unter [App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

## Weitere Ressourcen für die Bereitstellung von Sequencer und Client


[Bereitstellen von App-V 5.0](deploying-app-v-50.md)

[Planen für App-V 5.0](planning-for-app-v-50-rc.md)






 

 





