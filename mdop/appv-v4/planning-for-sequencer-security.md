---
title: Planen der Sequencer-Sicherheit
description: Planen der Sequencer-Sicherheit
author: dansimp
ms.assetid: 8043cb02-476d-4c28-a850-903a8ac5b2d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bf1e85e24d93d373add38b5efe51ceb40faae24e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806496"
---
# Planen der Sequencer-Sicherheit


Integrieren Sie Empfohlene Implementierungsmethoden so früh wie möglich bei der Konfiguration von Application Virtualization (App-V), damit Ihre Sequencer-Implementierung funktionsfähig und sicherer ist. Wenn Sie den Sequencer bereits konfiguriert haben, verwenden Sie die folgenden Best Practice-Richtlinien, um Ihre Entwurfsentscheidungen erneut zu überprüfen und Sie aus Sicherheitsgesichtspunkten zu analysieren.

**Wichtig**  
Der App-V-Sequencer sammelt und stellt alle auf dem Computer, auf dem Sequencer ausgeführt wird, gespeicherten Anwendungsinformationen bereit. Stellen Sie sicher, dass alle Benutzer, die auf den Computer zugreifen, auf dem der Sequencer ausgeführt wird, über Administratorrechte verfügen. Benutzer mit Anmeldeinformationen für ein Benutzerkonto sollten keinen Zugriff auf Paketinhalte und Paketdateien haben. Wenn Sie eine Sequenzierung auf einem Computer ausführen, auf dem Remote Desktop Dienste (vormals Terminal Dienste) ausgeführt werden, stellen Sie sicher, dass es sich um einen Computer handelt, der für die Sequenzierung vorgesehen ist, und dass Benutzer mit Anmeldeinformationen des Benutzerkontos während der Sequenzierung nicht damit verbunden sind.



## Bewährte Methoden für Sequencer-Sicherheit


Bedenken Sie die folgenden Szenarien und die zugehörigen bewährten Methoden beim Implementieren und Verwenden von Application Virtualization (App-V) Sequencer:

-   **Virenprüfung auf dem Computer, auf dem der Sequencer ausgeführt**wird – es wird empfohlen, den Computer, auf dem der Sequencer ausgeführt wird, auf Viren zu überprüfen und dann alle Antivirus-und Malware Erkennungssoftware auf dem Computer zu deaktivieren, auf dem der Sequencer läuft, während des Sequenz Prozesses. Dadurch wird der Sequenzierungsprozess beschleunigt, und die Antivirensoftware und die Antimalwaresoftware verhindern, dass der Sequenzierungsprozess beeinträchtigt wird. Installieren Sie als nächstes das sequenzierte Paket auf einem Computer, auf dem der Sequencer nicht ausgeführt wird, und überprüfen Sie nach der erfolgreichen Installation diesen Computer auf Viren. Wenn Viren gefunden werden, sollte der Hersteller der Software kontaktiert werden, um Sie über die infizierten Quelldateien zu informieren und eine aktualisierte Installationsquelle ohne Viren anzufordern. Optional kann der Sequenzer nach der Installationsphase gescannt werden, und wenn ein Virus gefunden wird, sollte der Softwarehersteller wie oben beschrieben kontaktiert werden.

    **Hinweis:**  
    Wenn ein Virus in einer Anwendung erkannt wird, sollte die Anwendung nicht auf Zielcomputern bereitgestellt werden.



-   **Aufzeichnen von Zugriffssteuerungslisten (ACLs) für NTFS-Dateien**– der App-V-Sequenzer zeichnet NTFS-Dateisystemberechtigungen für die Dateien auf, die während der Installation des Produkts überwacht werden. Mit dieser Funktion können Sie das beabsichtigte Verhalten der Anwendung genauer replizieren, als ob Sie lokal installiert und nicht virtualisiert wurde. In einigen Szenarien speichert eine Anwendung möglicherweise Informationen, auf die Benutzer nicht in den Anwendungsdateien zugreifen sollten. Eine Anwendung könnte beispielsweise Anmeldeinformationen in einer Datei innerhalb der Anwendung speichern. Wenn für das Paket keine ACLs erzwungen werden, kann ein Benutzer diese Informationen potenziell außerhalb der Anwendung anzeigen und verwenden.

    **Hinweis:**  
    Sie sollten keine Anwendungen sequenzieren, in denen unverschlüsselte sicherheitsspezifische Informationen wie Kennwörter gespeichert sind usw.



~~~
During the installation phase, you can modify the default permissions of the files if necessary. After completion of the sequencing process, but before saving the package, you can choose whether to enforce security descriptors that were captured during the installation of the application. By default, App-V will enforce the security descriptors specified during the installation of the application. If you turn off security descriptor enforcement, you should test the application to ensure the removal of associated Access Control Lists (ACL) will not cause the application to perform unexpectedly.
~~~

-   **Sequencer erfasst keine Registrierungs-ACLs**, obwohl der Sequencer die NTFS-Dateisystem-ACLs während der Installationsphase der Sequenzierung erfasst, werden die ACLs für die Registrierung nicht erfasst. Die Benutzer haben vollständigen Zugriff auf alle Registrierungsschlüssel für virtuelle Anwendungen mit Ausnahme von Diensten. Wenn ein Benutzer jedoch die Registrierung einer virtuellen Anwendung ändert, wird die Änderung in einem bestimmten Speicher (**uservol \ _sftfs \ _V1. pkg**) gespeichert und wirkt sich nicht auf andere Benutzer aus.

-   **Anwendungsdienste**– App-V bietet Unterstützung für Anwendungsdienste, die Teil einer virtualisierten Anwendung sind. In der virtuellen Umgebung ist jedoch der Sicherheitskontext, in dem Sie ausgeführt werden, limitiert. Die einzigen in einer virtuellen Umgebung unterstützten Sicherheitskontexte sind lokales System, lokaler Dienst und Netzwerkdienst. Wenn bei der Sequenzierung ein Sicherheitskontext für einen anderen als den drei unterstützten Anwendungsdienst angegeben ist, wird der Sicherheitskontext des lokalen Systems in der virtuellen Umgebung angewendet. Wenn der Anwendungsdienst so konfiguriert ist, dass er entweder den lokalen Dienst oder den Netzwerkdienst verwendet, wird er in der virtuellen Umgebung berücksichtigt. Die Konfiguration des Dienstkontos kann während des Sequenz Prozesses mithilfe dieser drei Sicherheitskontexte erfolgen.

-   **Beibehaltene Sicherheitsinformationen**: bei der Sequenzierung von Anwendungen können Sie die Anwendung als Benutzer installieren, oder Sie können eine automatisierte Methode zum Installieren der Anwendung während der Überwachung entwickeln. Alle Elemente, die nicht aus dem Paket ausgeschlossen werden, werden als Teil des Pakets erfasst, sodass die Anwendung über die erforderlichen Ressourcen verfügt, um in einer virtualisierten Umgebung ausgeführt zu werden. Einige Anwendungen speichern vertrauliche Sicherheitsinformationen (wie Kennwörter) während der Installation; bei ungeschützter Beibehaltung dieser Sicherheitsinformationen können andere Benutzer mit Zugriff auf das Paket darauf zugreifen. Wenn bei der Installation bei einer Anwendungsinstallation ein Kennwort oder andere sicherheitsrelevante Informationen abgefragt werden, überprüfen Sie die Dokumentation, um sicherzustellen, dass Sie entweder nicht beibehalten (nach der Installation entfernt) wird oder, wenn Sie beibehalten wird, dass Sie geschützt (verschlüsselt) ist.

-   **Sichern von virtuellen Anwendungspaketen**– speichern Sie immer virtuelle Anwendungspakete an einem sicheren Speicherort im Netzwerk, um zu verhindern, dass das Paket manipuliert oder beschädigt wird.

## Verwandte Themen


[Planen der Sicherheit und von Schutzmaßnahmen](planning-for-security-and-protection.md)









