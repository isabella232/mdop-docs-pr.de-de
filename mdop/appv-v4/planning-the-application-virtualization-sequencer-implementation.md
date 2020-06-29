---
title: Planen der Application Virtualization Sequencer-Implementierung
description: Planen der Application Virtualization Sequencer-Implementierung
author: dansimp
ms.assetid: 052f32fe-ad13-4921-a8ce-4a657eb2b2bf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac62991e290dcd2da1c42f025a19365bda239fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806488"
---
# Planen der Application Virtualization Sequencer-Implementierung


Sequenzierung, der Prozess, der von Application Virtualization zum Erstellen von virtuellen Anwendungen und Anwendungspaketen verwendet wird, erfordert die Verwendung eines Computers, auf dem die Application Virtualization Sequencer-Software installiert ist.

Während des Sequenz Prozesses wird der Sequencer in den Monitormodus versetzt, und die zu sequenzierte Anwendung wird auf dem Sequenzcomputer installiert. Als nächstes wird die sequenzierte Anwendung gestartet, und die wichtigsten und häufig verwendeten Funktionen werden ausgeübt, damit der Überwachungsprozess den primären Funktionsbaustein konfigurieren kann, der den Mindestinhalt in einem Anwendungspaket enthält, der für die Ausführung einer Anwendung erforderlich ist. Wenn diese Schritte abgeschlossen sind, wird der Überwachungsmodus angehalten, und die sequenzierte Anwendung wird gespeichert und getestet, um die ordnungsgemäße Verwendung zu überprüfen.

Beachten Sie bei der Entscheidung, welche Anwendungen für die Sequenzierung ausgewählt werden sollen, dass bestimmte Anwendungen nicht sequenziert werden können. Dazu gehören bestimmte Teile des Windows-Betriebssystems wie Internet Explorer, Gerätetreiber und Anwendungen, mit denen Dienste beim Booten gestartet werden.

Schritt-für-Schritt-Informationen zum Installieren des Sequencers finden Sie unter so wird es [gemacht: Installieren des Application Virtualization Sequencers](how-to-install-the-application-virtualization-sequencer.md).

**Wichtig**  Der gesamte Sequenzierungsprozessplan sollte vom Sicherheitsteam Ihres Unternehmens überprüft und genehmigt werden. Sequencer-Vorgänge werden in der Regel getrennt von der Produktionsumgebung in einer Übungseinheit aufbewahrt. Dies kann je nach Ihren geschäftlichen Anforderungen so einfach oder umfassend wie erforderlich sein. Die Sequenzierung von Computern benötigt Verbindungen mit dem Unternehmensnetzwerk, um fertige Pakete auf die Produktionsserver zu kopieren. Da Sie jedoch in der Regel ohne Virenschutz betrieben werden, dürfen Sie nicht ungeschützt im Unternehmensnetzwerk sein – beispielsweise können Sie hinter einer Firewall oder in einem isolierten Netzwerksegment arbeiten. Die Verwendung virtueller Computer, die für die Freigabe eines isolierten virtuellen Netzwerks konfiguriert sind, ist möglicherweise auch ein akzeptabler Ansatz. Befolgen Sie die Sicherheitsrichtlinien Ihres Unternehmens, um diese Situation sicher zu beheben.

 

Zu den wichtigsten Schritten bei der Planung des Sequenzierungsprozesses gehören die folgenden:

-   Bedenken Sie die Anzahl der Anwendungen, die Sie monatlich erwarten, die Größe dieser Anwendungen, und fügen Sie eine Genehmigung für die Sequenzierung zukünftiger Updates hinzu. Pakete können bis zu 4 GB groß, komprimiert oder unkomprimiert sein.

-   Vorbereiten und dokumentieren eines methodisch wiederholbaren Prozesses für Ihre Organisation, der bei der Sequenzierung der einzelnen Anwendungen befolgt werden soll. Dies sollte die Verwendung einer Checkliste für jeden Testlauf sowie einen Versionskontrollprozess beinhalten. Die Verwendung eines Nachverfolgungsprotokolls für jede sequenzierte Anwendung ist auch sehr hilfreich, wenn Sie mögliche technische Probleme mit einem Paket untersuchen.

-   Verwenden Sie für die Sequenzierung von Anwendungen leistungsstarke Computer, die für den Verarbeitungs Durchsatz optimiert sind, mit mindestens 4 GB Arbeitsspeicher und einer schnellen CPU (3 GHz oder schneller). Schnelle Festplatten und die Verwendung separater Datenträger-Volumes können auch die Leistung verbessern. Virtuelle Computer eignen sich ideal für die Sequenzierung, da Sie einfach zurückgesetzt werden können, oder Sie können einen physikalischen Computer mit einem sauberen Bild auf einer lokalen Partition verwenden, um eine schnelle erneute Abbilderstellung zu ermöglichen, nachdem jeder Paket Sequenz Vorgang abgeschlossen wurde.

    **Wichtig**  Das Ausführen des App-V-Sequencers im abgesicherten Modus wird nicht unterstützt.

     

-   Stellen Sie sicher, dass Sie die Betriebsumgebung der sequenzierten Anwendung verstehen, einschließlich Integrations Elementen wie Microsoft Office oder der Java-Laufzeitumgebung, da dadurch häufig festgestellt wird, ob vor dem Sequenzieren der Anwendung etwas auf dem Sequenzcomputer installiert werden muss.

-   Stellen Sie sicher, dass jeder neue Sequenz Vorgang immer mit einem sauberen Basis Bild beginnt. Stellen Sie sicher, dass der Sequenzcomputer zurückgesetzt wurde, indem Sie entweder das gespeicherte Bild auf einem physikalischen Computer wiederherstellen oder einen virtuellen Computer neu starten, nachdem alle Änderungen verworfen wurden. Vor dem Speichern sollten die neuesten Updates von Windows Update angewendet werden.

-   Deaktivieren Sie alle auf dem Sequenzcomputer, die den Installations Überwachungsprozess stören können, wie Antivirus-Scanner und Windows Update, da eine stabile Plattform während des Sequenz Prozesses erforderlich ist. Da dieser Schritt erhebliche Sicherheitsrisiken verursacht, stellen Sie sicher, dass die richtigen Vorkehrungen getroffen werden, um den Computer und das Netzwerk sowie das sequenzierte Anwendungspaket zu schützen. Wir empfehlen, dass Sie eine Antivirus-Untersuchung von Anwendungspaketen durchführen, bevor Sie sequenziert werden.

-   Einfügen eines detaillierten Prozesses zum Testen jeder Anwendung nach der Sequenzierung Das Testen der sequenzierten Anwendung bestimmt, ob Sie ordnungsgemäß funktioniert, und ist ein wesentlicher Bestandteil des Prozesses, bevor die virtualisierte Anwendung für Endbenutzer bereitgestellt wird. Als letzten Schritt beim Testen vor der umfassenden Bereitstellung für Endbenutzer sollten Sie auch eine Pilotbereitstellung für eine Testgruppe planen.

-   Wenn Sie sequenzierte Anwendungen testen, wählen Sie Computer Geräte desselben Typs aus, und führen Sie die gleichen Betriebssysteme aus, die in der Produktionsumgebung des Unternehmens verwendet werden. Solange Sie ordnungsgemäß konfiguriert sind, können entweder virtuelle Computer oder physische Computer verwendet werden.

## Verwandte Themen


[Hardware- und Softwareanforderungen für Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)

[So installieren Sie Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)

[So aktualisieren Sie Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

[Übersicht über Sicherheit und Schutz](security-and-protection-overview.md)

 

 





