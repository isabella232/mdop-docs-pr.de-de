---
title: Planen für die Bereitstellung von App-V 5.0-Sequencer und -Client
description: Planen für die Bereitstellung von App-V 5.0-Sequencer und -Client
author: dansimp
ms.assetid: 57a604ad-90e1-4d32-86bb-eafff59aa43a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8c6f7c4d717acad014f079e51a7013a57766d9ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804997"
---
# Planen für die Bereitstellung von App-V 5.0-Sequencer und -Client


Bevor Sie mit der Verwendung von Microsoft Application Virtualization (app-v) 5,0 beginnen können, müssen Sie den App-v 5,0-Sequenzer, den App-v 5,0-Client und optional den freigegebenen App-v 5,0-Inhaltsspeicher installieren. In den folgenden Abschnitten wird die Planung dieser Installationen behandelt.

## Planen der Bereitstellung von App-V 5,0 Sequencer


App-V 5,0 verwendet einen Prozess, der als Sequenzierung bezeichnet wird, um virtualisierte Anwendungen und Anwendungspakete zu erstellen. Die Sequenzierung erfordert die Verwendung eines Computers, auf dem der App-V 5,0-Sequenzer ausgeführt wird.

**Hinweis**  Informationen zu den neuen Funktionen von App-v 5,0 Sequencer finden Sie im Abschnitt " **Änderungen am Sequenzer** " der [Neuerungen in App-v 5,0](whats-new-in-app-v-50.md).

 

Der Computer, auf dem der App-V 5,0-Sequenzer ausgeführt wird, muss die Mindestsystemanforderungen erfüllen. Eine Liste dieser Anforderungen finden Sie unter [unterstützte App-V 5,0-Konfigurationen](app-v-50-supported-configurations.md).

Im Idealfall sollten Sie den Sequencer auf einem Computer installieren, der als virtueller Computer ausgeführt wird. So können Sie den Computer, auf dem der Sequencer ausgeführt wird, einfacher wieder in einen "sauberen" Zustand versetzen, bevor Sie eine andere Anwendung sequenzieren. Wenn Sie den Sequencer mithilfe eines virtuellen Computers installieren, sollten Sie die folgenden Schritte ausführen:

1.  Installieren Sie alle zugehörigen Sequenzer-Voraussetzungen.

2.  Installieren Sie den Sequencer.

3.  Erstellen Sie eine "Momentaufnahme" der Umgebung.

**Wichtig**  Sie sollten das Sicherheitsteam Ihres Unternehmens überprüfen und den Sequenzierungsprozessplan genehmigen. Aus Sicherheitsgründen sollten Sie die Sequencer-Vorgänge in einer Lab-Umgebung beibehalten, die von der Produktionsumgebung getrennt ist. Die Separations Anordnung kann je nach Ihren geschäftlichen Anforderungen so einfach oder so umfassend wie erforderlich sein. Die Sequenzierungs Computer müssen in der Lage sein, eine Verbindung mit dem Unternehmensnetzwerk herzustellen, um fertige Pakete auf die Produktionsserver zu kopieren. Da die Sequenzierungs Computer in der Regel ohne Virenschutz betrieben werden, dürfen Sie jedoch nicht ungeschützt im Unternehmensnetzwerk sein. So können Sie beispielsweise hinter einer Firewall oder in einem isolierten Netzwerksegment arbeiten. Möglicherweise können Sie auch virtuelle Computer verwenden, die für die Freigabe eines isolierten virtuellen Netzwerks konfiguriert sind. Befolgen Sie die Sicherheitsrichtlinien Ihres Unternehmens, um diese Probleme sicher zu beheben.

 

[So installieren Sie den Sequencer](how-to-install-the-sequencer-beta-gb18030.md)

## Planen der App-V 5,0-Clientbereitstellung


Wenn Sie virtualisierte Pakete auf Zielcomputern ausführen möchten, müssen Sie den App-V 5,0-Client auf den Zielcomputern installieren. Der App-V 5,0-Client ist die Komponente, die eine virtualisierte Anwendung auf einem Zielcomputer ausführt. Der Client ermöglicht Benutzern die Interaktion mit Symbolen und bestimmten Dateitypen, um virtualisierte Anwendungen zu starten. Der Client hilft auch beim Abrufen von Anwendungsinhalten vom Verwaltungsserver und Zwischenspeichern des Inhalts, bevor der Client die Anwendung startet. Es gibt zwei verschiedene Clienttypen: den Client für Remotedesktopdienste, der auf Servern mit dem Host für Remotedesktopsitzungen (RD-Sitzungshost) und dem App-V 5,0-Client verwendet wird, der für alle anderen Computer verwendet wird.

Der App-V 5,0-Client sollte entweder über die Installer-Befehlszeile oder mithilfe eines PowerShell-Skripts konfiguriert werden, nachdem die Installation abgeschlossen ist.

Die Einstellungen müssen im Voraus sorgfältig definiert werden, um die Bereitstellung der App-V 5,0-Client Software zu beschleunigen. Dies ist besonders wichtig, wenn Sie Computer in verschiedenen Niederlassungen haben, in denen die Clients für die Verwendung unterschiedlicher Quellspeicherorte konfiguriert sein müssen.

Darüber hinaus müssen Sie festlegen, wie die Client Software bereitgestellt werden soll. Obwohl es möglich ist, den Client manuell auf jedem Computer bereitzustellen, bevorzugen die meisten Organisationen den Client mithilfe eines automatisierten Prozesses. Eine größere Organisation verfügt möglicherweise über ein ESD-System (Operational Electronic Software Distribution), das ein ideales Client Bereitstellungssystem ist. Wenn kein ESD-System vorhanden ist, können Sie die Standardmethode für die Installation von Software in Ihrer Organisation verwenden. Mögliche Methoden sind Gruppenrichtlinien oder verschiedene Skripttechniken. Je nach Anzahl und unterschiedlichen Speicherorten auf Ihren Clientcomputern kann dieser Bereitstellungsprozess komplex sein. Sie müssen einen strukturierten Ansatz verwenden, um sicherzustellen, dass der Client mit der richtigen Konfiguration auf allen Computern installiert wird.

Eine Liste der Mindestanforderungen für Clients finden Sie unter [App-V 5,0-Voraussetzungen](app-v-50-prerequisites.md).

[So stellen Sie App-V-Client bereit](how-to-deploy-the-app-v-client-gb18030.md)

## <a href="" id="bkmk-client-coexist"></a>Planen der Koexistenz von App-V-Clients


Sie können den App-v 5,0-Client nebeneinander mit dem App-v 4,6-Client bereitstellen. Für die Client Koexistenz müssen virtualisierte Anwendungen entweder mithilfe einer Bereitstellungs Konfigurationsdatei oder einer Benutzerkonfigurationsdatei hinzugefügt oder veröffentlicht werden, da in diesen Konfigurationsdateien bestimmte Einstellungen vorhanden sind, die so konfiguriert werden müssen, dass APP-v 5,0 mit App-v 4.6-Clients funktioniert. Wenn ein Paket entweder mit dem Client oder dem Server aktualisiert wird, muss das Paket die Konfigurationsdatei erneut übermitteln. Dies gilt für alle Pakete, die über eine entsprechende Konfigurationsdatei verfügen, sodass Sie nicht speziell für die Client Koexistenz gelten. Wenn Sie die Konfigurationsdatei jedoch während des Paket Upgrades nicht übermitteln, funktioniert der Paket Zustand in Koexistenz-Szenarien nicht wie erwartet.

App-V 5,0 Dynamic Configuration-Dateien passen ein Paket für einen bestimmten Benutzer an. Sie müssen die Dynamic User Configuration-Datei (XML) oder die Konfigurationsdatei für die dynamische Bereitstellung erstellen, bevor Sie Sie verwenden können. Um die Datei zu erstellen, muss eine erweiterte manuelle Operation ausgeführt werden.

Wenn eine Dynamic User-Konfigurationsdatei verwendet wird, wird keine der App-V 5,0-Informationen für die Erweiterung in der Manifestdatei verwendet. Dies bedeutet, dass die Dynamic User-Konfigurationsdatei alles für die Erweiterung enthalten muss, die für App-V 5,0 in der Manifestdatei spezifisch ist, sowie die Änderungen, die Sie vornehmen möchten, beispielsweise Löschungen und Updates. Weitere Informationen zum Erstellen einer benutzerdefinierten Konfigurationsdatei finden Sie unter [Erstellen einer benutzerdefinierten Konfigurationsdatei mithilfe der App-V 5,0-Verwaltungskonsole](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).

[Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## <a href="" id="bkmk-plan-for-scs"></a>Planen des freigegebenen Inhaltsspeichers für App-V 5,0 (SCS)


Der freigegebene Inhaltsspeicher Modus von App-v 5,0 ermöglicht dem Computer, auf dem der APP-v 5,0-Client ausgeführt wird, virtualisierte Anwendungen auszuführen, und keiner der Paketinhalte wird auf dem Computer gespeichert, auf dem der APP-v 5,0-Client ausgeführt wird. Virtuelle Anwendungen werden auf die Zielcomputer nur gestreamt, wenn Sie vom Client angefordert werden.

In der folgenden Liste sind einige der Vorteile der Verwendung des freigegebenen Inhaltsspeichers von App-V 5,0 aufgeführt:

-   Reduzierte Anwendungskonflikte zwischen apps und mehreren Benutzern und damit ein verringerter Bedarf an Regressionstests

-   Beschleunigte Anwendungsbereitstellung durch Verringerung des Bereitstellungsrisikos

-   Vereinfachte Profilverwaltung

[So installieren Sie den App-V 5.0-Client für den SCS-Modus (Shared Content Store)](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)






## <a href="" id="other-resources-for-the-app-v-5-0-deployment-"></a>Weitere Ressourcen für die App-V 5,0-Bereitstellung


[Planen der Bereitstellung von App-V](planning-to-deploy-app-v.md)

 

 





