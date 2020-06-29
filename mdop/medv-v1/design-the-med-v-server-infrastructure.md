---
title: Entwerfen der MED-V-Server-Infrastruktur
description: Entwerfen der MED-V-Server-Infrastruktur
author: dansimp
ms.assetid: 2781040f-880e-4e16-945d-a38c0adb4151
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4ba4c38328c5484b7daa292f9fc33a4e59824327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810402"
---
# Entwerfen der MED-V-Server-Infrastruktur


In diesem Thema entwerfen Sie die Serverinfrastruktur für jede MED-V-Instanz. Dies umfasst die Ermittlung, ob die SQL Server-Instanz auf dem MED-V-Server oder auf einem Remoteserver vorhanden ist, sowie die Größe der SQL Server-Datenbank. Darüber hinaus ermitteln Sie den Speicherort der Verwaltungskonsole.

## Entwerfen und Platzieren des Servers für jede MED-V-Instanz


Der MED-V-Server implementiert Richtlinien und speichert Zustands-und Verlaufsdaten zu Ihren Clients.

### Formularfaktor

MED-V empfiehlt die Verwendung eines Dual-Core-CPU-Servers mit 2,8 GHz mit 2 GB Arbeitsspeicher. Diese Empfehlung basiert auf der Annahme, dass der Med-v-Server auf einem dedizierten Computer ausgeführt wird und dass SQL Server und die Med-v-Verwaltungskonsole auf separaten Computern ausgeführt werden.

Angesichts dieser Arbeitsauslastung sollte der MED-V-Server relativ leicht geladen werden. Wenn keine spezifischen architektonischen Anleitungen für den Server-Formularfaktor vorhanden sind, entwerfen Sie den Server mithilfe der MED-V-Empfehlung, wobei der Arbeitsspeicher dem standardmäßigen Formularfaktor der Organisation entspricht. Der Med-v-Server kann auf einem virtuellen Computer (VM) unter Windows Server2008 Hyper-v ausgeführt werden. Wenn Sie eine VM verwenden, stellen Sie sicher, dass Sie auf CPU-und Arbeitsspeicherressourcen zugreift, die den für einen physikalischen Computer angegebenen entsprechen.

Die für den Med-v-Server erforderliche Festplattenkapazität muss ausreichen, um die Konfigurationsdateien des Med-v-Arbeitsbereichs zu speichern. Ein MED-V-Arbeitsbereich kann nur einen virtuellen Computer und eine Richtlinie für einen oder mehrere Benutzer verwenden. Daher hängt die Anzahl der zu speichernden MED-V-Arbeitsbereiche davon ab, in welchem Maß unterschiedliche Richtlinien für verschiedene Benutzer des gleichen virtuellen Computers erforderlich sind, sowie die Anzahl der VMS, die verwendet werden sollen. Die XML-Dateien im Med-v-Arbeitsbereich sind für einen typischen Med-v-Arbeitsbereich um 30KB groß. Um die erforderliche Datenträgerkapazität zu ermitteln, Multiplizieren Sie 30 KB mit der Anzahl der Med-v-Arbeitsbereiche, die vom Med-v-Server gespeichert werden.

Die wichtigsten Netzwerkverbindungen des MED-V-Servers sind die Links zu den Clients, sodass der Server an einem Netzwerkspeicherort platziert wird, der die meiste verfügbare Bandbreite und die stabilsten Links zu seinen Clients bereitstellt.

### Fehlertoleranz

In einer Med-v-Instanz kann nur ein aktiver Med-v-Server vorhanden sein, und Med-v enthält keine Standardfunktionen zum Platzieren des Servers in einem Microsoft Cluster Server (MSCS)-Cluster, um Fehlertoleranz bereitzustellen. Ein passiver Sicherungsserver kann manuell konfiguriert werden.

Um zu entscheiden, ob ein passiver Sicherungsserver für die Med-v-Instanz manuell konfiguriert werden soll, ermitteln Sie, ob Benutzer die Med-v-Bilder im Offlinemodus verwenden dürfen. Informationen zum Offlinemodus finden Sie unter [so wird es gemacht: Konfigurieren eines Domänenbenutzers oder einer Gruppe](how-to-configure-a-domain-user-or-groupmedvv2.md). Wenn Benutzer nicht in der Lage sind, offline zu arbeiten, können Sie im Fall eines Med-v-Serverfehlers nicht weiter arbeiten, auch wenn der Med-v-Arbeitsbereich bereits auf dem Client gestartet wurde. Wenn Offlinearbeit zulässig ist, ermitteln Sie für jeden MED-V-Arbeitsbereich, wie lange der Client offline arbeiten darf, bevor er authentifiziert werden muss. Dies ist die maximale Zeitspanne, die der Server nicht verfügbar sein kann.

## Entwerfen und Platzieren der SQL Server-Datenbank


Der MED-V-Server verwendet die SQL Server-Datenbank zum Speichern des Clientstatus und der Ereignisse. Sie können die SQL Server-Datenbank auf demselben Computer wie der MED-V-Server installieren, oder Sie können Sie auf einem separaten Server mit SQL Server platzieren, der optional Remote sein kann. Sie können die Datenbank für andere MED-V-Instanzen freigeben, in dem Fall, dass Ereignisse und Warnungen dieser Instanzen in derselben Datenbank gespeichert werden, und Berichte werden Ereignisse aus allen Instanzen umfassen. Sie können die Datenbank in einer vorhandenen SQL Server-Instanz installieren, und die Datenbanken anderer MED-V-Server können sich in derselben Instanz befinden.

Wenn Sie den Datenbankserver an einem Speicherort ablegen, der vom MED-V-Server entfernt ist, können Berichte über Netzwerke, die nicht genügend Bandbreite aufweisen, in der Konsole langsam geladen werden und möglicherweise nicht die neuesten Daten von Clients anzeigen. Beziehen Sie sich auf die Erwartungen des Organisations Diensts, die Sie unter [Definieren des Projektumfangs](define-the-project-scope.md) festgelegt haben, und verwenden Sie diese Informationen, um zu entscheiden, wo die SQL Server-Datenbank platziert werden soll.

### Formularfaktor

Wenn Sie SQL Server auf dem gleichen Server wie Med-v ausführen und SQL Server nur zum Speichern von Daten für diesen Server verwendet wird, beginnen Sie mit der Med-v-Empfehlung, und fügen Sie Ressourcen für die SQL Server-Auslastung hinzu. Wenn in SQL Serverereignisse und Warnungen von mehr als einer MED-V-Instanz gespeichert werden, finden Sie Informationen zum Skalieren des Server Formularfaktors im Leitfaden zur [Infrastrukturplanung und-Entwurf von Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) (http://go.Microsoft.com/fwlink/?linkid=163302).

Die Größe der Datenbank hängt von der Anzahl der Clientereignisse ab, die in der Datenbank gespeichert werden. Ereignisse werden durch den normalen Betrieb des Clients erstellt, beispielsweise wenn ein Med-v-Arbeitsbereich gestartet wird oder wenn ein Fehler im Med-v-Arbeitsbereich vorliegt. Das Standardintervall, in dem der Clientereignisse sendet, beträgt 1 Minute.

Um die Größe der Datenbank zu schätzen, legen Sie Folgendes fest:

-   Die Anzahl der Clients in der MED-V-Instanz. Der Höchstwert ist 5.000.

-   Typische ankunftsrate des Ereignisses. Diese Gebühr hängt vom Client Nutzungsverhalten ab, beträgt aber ca. 15 bis 20 Ereignisse pro Tag pro Client.

-   Ereignisgröße Die Größe beträgt in der Regel rund 200 bytes.

-   Speicher Betrag. Die Anzahl von Tagen, für die Ereignisse gespeichert werden.

Multiplizieren Sie diese Werte zusammen, um die Größe des erforderlichen Datenspeichers in Bytes zu berechnen, und fügen Sie dann einen Sicherheitsfaktor hinzu, um Folgendes zu berücksichtigen:

-   Fehler, die in kurzer Zeit eine große Anzahl von Ereignissen von einem Client erstellen können.

-   Datenbanktabelle und organisatorischer Bereich.

Verwenden Sie zum Näherungswert der IOPS-Anforderung (Infrastructure Optimization pro Sekunde) die obigen Werte, und multiplizieren Sie die typische ankunftsrate des Ereignisses mit der Anzahl der Clients in der Instanz. Dadurch ergibt sich die Anzahl der Datensätze, die pro Tag geschrieben werden können. Dividieren Sie diese Zahl durch 86.400, um die Anzahl der pro Sekunde geschriebenen Datensätze abzuleiten. Wenn eine Schreiboperation mit einem Single Infrastructure Optimization (IO)-Vorgang gleichgesetzt werden kann, ist diese Zahl die erforderliche Schreib-IOPS. Hinzufügen eines Puffers für die Bericht Erstellungs Aktivität Dies ist schwer zu ermitteln, hängt jedoch von der Anzahl der Konsolen ab, die mit der Instanz verwendet werden, und der Häufigkeit, mit der Sie zum Generieren von Berichten verwendet werden.

### Fehlertoleranz

Wenn der MED-V-Client ausgeführt wird und der Server nicht verfügbar ist, werden Ereignisse auf dem Client gesichert, und Berichte sind in der Verwaltungskonsole nicht verfügbar. Beziehen Sie sich auf die Erwartungen des Unternehmens, die in [Definieren des Projektumfangs](define-the-project-scope.md) festgelegt sind, um zu entscheiden, ob der Entwurf einer fehlertoleranten SQL Server-Infrastruktur erforderlich ist.

MED-V bietet keine Unterstützung für die Ausführung von SQL Server in einem MSCS-Cluster. Um einen warmen Standbymodus bereitzustellen und Datenverluste bei einem Fehler zu vermeiden, können Sie SQL Server in einer Protokollversandkonfiguration platzieren. Informationen zum Protokollversand finden Sie im Leitfaden zur [Infrastrukturplanung und-Entwurf von Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) ( https://go.microsoft.com/fwlink/?LinkId=163302) .

## Entwerfen der Verwaltungskonsole


Ein Teil der Funktionalität der Med-v-Verwaltungskonsole besteht darin, VMS zu testen, bevor Sie für die Verteilung an Med-v-Clients verpackt werden. Daher sollte die Verwaltungskonsole mit einem Formularfaktor entworfen werden, der dem Formfaktor eines typischen MED-V-Clientcomputers so ähnlich wie möglich ähnelt.

Die Verwaltungskonsolenanwendung wird zusammen mit dem MED-V-Client installiert und verwendet Microsoft Virtual PC2007 SP1 mit dem Hotfix, der im Microsoft Knowledge Base-Artikel 974918 beschrieben wird. Ein Clientbetriebssystem muss verwendet werden. die Med-v-Verwaltungskonsole kann nicht auf dem gleichen System wie der Med-v-Server ausgeführt werden.

Sie können keine Verwaltungskonsole für mehrere MED-V-Serverinstanzen freigeben. Die Adresse des Med-v-Servers wird während der Installation des Med-v-Clients der Verwaltungskonsole angegeben. Dies kann nach der Installation geändert werden, jedoch kann die Verwaltungskonsole zu einem beliebigen Zeitpunkt nur mit einem einzelnen MED-V-Server funktionieren.

Sie können mehrere Verwaltungskonsolen mit einem einzelnen MED-V-Server verwenden. Um Konflikte zu vermeiden, wird ein Mechanismus zur Verfügung gestellt, der andere Konsolenbenutzer benachrichtigt, wenn eine Konsole Änderungen an einem MED-V-Arbeitsbereich vorgenommen hat.

Ermitteln Sie für jede MED-V-Instanz, wie viele Verwaltungskonsolen benötigt werden und wo Sie gespeichert werden. Wählen Sie einen typischen MED-V-Client-Formularfaktor aus, der für die Verwaltungskonsole verwendet werden soll.

## Verwandte Themen


[Von MED-V 1.0 SP1 unterstützte Konfigurationen](med-v-10-sp1-supported-configurationsmedv-10-sp1.md)

[Konfigurieren von MED-V-Server für den Clustermodus](configuring-med-v-server-for-cluster-mode.md)

[So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole](how-to-install-med-v-client-and-med-v-management-console.md)

[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

 

 





