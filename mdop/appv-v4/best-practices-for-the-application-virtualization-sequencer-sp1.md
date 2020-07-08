---
title: Bewährte Methoden für Application Virtualization Sequencer
description: Bewährte Methoden für Application Virtualization Sequencer
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809091"
---
# Bewährte Methoden für Application Virtualization Sequencer


In diesem Thema finden Sie bewährte Methoden zum Ausführen des Microsoft Application Virtualization (App-V)-Sequencers. Überprüfen und berücksichtigen Sie bei der Planung und Verwendung des Sequencers in Ihrer Umgebung die folgenden Empfehlungen.

## Bewährte Methoden für die Sequenzierung von Computer Konfigurationen


Bei der Konfiguration des Computers, auf dem der App-V-Sequencer ausgeführt wird, sollten die folgenden bewährten Methoden berücksichtigt werden:

-   **Sequenz auf einem Computer mit einer ähnlichen Konfiguration, auf der eine frühere Version des Betriebssystems als auf den Zielcomputern ausgeführt wird.**

    Stellen Sie sicher, dass auf dem Computer, auf dem der Sequencer ausgeführt wird, eine frühere Version des Betriebssystems als auf den Zielcomputern ausgeführt wird. Dazu gehören die Versionen des Service Packs und Updates. Wenn beispielsweise auf den Zielcomputern Windows Vista und WindowsXP ausgeführt werden, sollten Sie Anwendungen auf einem Computer mit WindowsXP sequenzieren. Die Möglichkeit zur Sequenzierung auf einem Betriebssystem und zum Ausführen der virtualisierten Anwendung unter einem anderen Betriebssystem ist nicht garantiert und hängt von der jeweiligen Anwendung und dem jeweiligen Betriebssystem ab. Wenn Probleme auftreten, müssen Sie möglicherweise eine Sequenz unter der gleichen Betriebssystemumgebung ausführen, auf der der App-V-Client ausgeführt wird.

-   **Konfigurieren Sie den Computer, auf dem der Sequencer ausgeführt wird, mit mehreren Partitionen.**

    Sie sollten den Computer, auf dem der Sequencer ausgeführt wird, mit mindestens zwei primären Partitionen konfigurieren. Die erste Partition (**C:**) sollte das Betriebssystem enthalten und mit dem NTFS-Dateisystem formatiert werden. Die zweite Partition (**Q:**) wird als Zielpfad für die Installation der virtuellen Anwendung verwendet und sollte auch mit dem NTFS-Dateisystem formatiert werden.

-   **Konfigurieren Sie das temporäre Verzeichnis mit genügend freiem Speicherplatz.**

    Der Sequencer verwendet das Verzeichnis **% tmp%** oder **% Temp%** und das **Scratch** -Verzeichnis, um temporäre Dateien während der Sequenzierung zu speichern. Sie sollten diese Verzeichnisse auf dem Computer, auf dem der Sequencer ausgeführt wird, mit freiem Speicherplatz konfigurieren, der den geschätzten Anwendungs Installationsanforderungen entspricht. Sie können den Speicherort des **Scratch** -Verzeichnisses überprüfen, indem Sie die Sequencer-Konsole öffnen und **Tools**, **Optionen**und dann die Registerkarte **Pfade** auswählen. die Konfiguration der temporären Verzeichnisse und des **Scratch** -Verzeichnisses auf verschiedenen Festplattenpartitionen kann die Leistung während der Sequenzierung verbessern.

-   **Sequenz Anwendungen mithilfe von Microsoft VirtualPC**

    Die meisten Anwendungen werden mehrmals sequenziert. Um dies zu erleichtern, sollten Sie die Sequenzierung auf einem Computer in einer virtuellen Umgebung in Frage stellen. Auf diese Weise können Sie eine Anwendung sequenzieren und mit minimaler Neukonfiguration auf dem Computer, auf dem der Sequencer ausgeführt wird, zu einem sauberen Zustand zurückkehren.

    Wenn Sie Microsoft Hyper-v in Ihrer Umgebung ausführen, wird der APP-v-Sequencer ausgeführt, wenn der virtuelle Hyper-v-Computer ausgeführt wird:

    -   angehalten und fortgesetzt.

    -   hat den Zustand gespeichert und wiederhergestellt.

    -   als Snapshot gespeichert und wiederhergestellt.

    -   im Rahmen einer Livemigration zu einer anderen Hardware migriert.

-   **Bevor Sie eine neue Anwendung sequenzieren, fahren Sie andere ausgeführte Programme herunter.**

    Prozesse und geplante Aufgaben, die normalerweise auf dem Sequenzcomputer ausgeführt werden, können den Sequenzierungsprozess verlangsamen und dazu führen, dass bei der Sequenzierung irrelevante Daten gesammelt werden. Alle unnötigen Anwendungen und Programme sollten geschlossen werden, bevor Sie mit der Sequenzierung beginnen.

-   **Sequenz auf einem Computer, auf dem die Terminal Dienste ausgeführt werden**

    Sie sollten den Installationsmodus nicht auf einem Computer konfigurieren, auf dem die Terminal Dienste ausgeführt werden, bevor Sie den Sequencer installieren.

## Bewährte Methoden für die Sequenzierung


Bei der Sequenzierung einer neuen Anwendung sollten die folgenden bewährten Methoden berücksichtigt werden:

-   

    **Hinweis**  Wenn Sie mit App-V 4,6 SP1 arbeiten, müssen Sie keine Sequenz zu einem Verzeichnis ausführen, das der 8,3-Benennungskonvention folgt.

     

-   **Sequenz zu einem eindeutigen Verzeichnis, das der 8,3-Benennungskonvention folgt.**

    Sie sollten alle Anwendungen in einem Verzeichnis abgleichen, das der 8,3-Benennungskonvention folgt. Der angegebene Verzeichnisname darf nicht mehr als acht Zeichen enthalten, gefolgt von einer dreistelligen Dateinamenerweiterung – beispielsweise **Q:\\MYAPP. ABC**.

-   **Sequenz in einen Zielordner im Stammverzeichnis des Laufwerks, nicht in ein Unterverzeichnis.**

    Wenn die Anwendungssuite mehrere Teile enthält, installieren Sie die einzelnen Anwendungen in einem Unterverzeichnis des Hauptverzeichnisses. Wenn beispielsweise ein Paket zusammen mit einem Client eine Anwendung enthält, verwenden Sie **Q:\\AppSuite** als Hauptverzeichnis, und Sequenzieren Sie die Hauptanwendung zu **Q:\\AppSuite\\Main**, und führen Sie den Client zu **Q:\\AppSuite\\Client**aus.

-   **Konfigurieren und testen Sie die Anwendung während der Installationsphase.**

    Zum Abschluss der Installation einer Anwendung müssen häufig mehrere manuelle Schritte ausgeführt werden, die nicht Teil des Installationsvorgangs der Anwendung sind. Diese Schritte können die Konfiguration einer Verbindung zu einer Datenbank oder das Kopieren aktualisierter Dateien beinhalten. Führen Sie diese Konfigurationen während der Installationsphase aus, und führen Sie dann die Anwendung aus, um sicherzustellen, dass Sie funktioniert.

-   **Führen Sie die Anwendung, falls erforderlich, mehrmals aus, bis das Programm stabil ist.**

    Sie sollten die Anwendung während der Installation mehrmals ausführen, um sicherzustellen, dass alle zugehörigen Registrierungs-und Dialogfeld Konfigurationen abgeschlossen sind. Wenn Sie die Anwendung während der Installation mehrmals öffnen, wird sichergestellt, dass nur die relevanten Anwendungsfeatures in den **primären Feature-Block**geladen werden.

-   **Deaktivieren Sie alle automatischen Update Features, die der Anwendung zugeordnet sind.**

    Einige Anwendungen können während der Installation automatisch auf die neuesten Updates überprüfen. Wenn Sie die Versionsverwaltung virtueller Anwendungspakete unterstützen möchten, sollten Sie diese Funktion während der Sequenzierung deaktivieren. Wenn Updates erforderlich sind, sollten Sie ein neues virtuelles Anwendungspaket mit den zugehörigen Updates sequenzieren.

## Verwandte Themen


[Planen der Bereitstellung von Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

 

 





