---
title: Informationen zu MBAM 2.0
description: Informationen zu MBAM 2.0
author: dansimp
ms.assetid: b43a0ba9-1c83-4854-a2c5-14eea0070e36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7bdf24d1f375dd1fa8b18ac90c2fc49d2887c6c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810483"
---
# Informationen zu MBAM 2.0


Microsoft BitLockerAdministration and Monitoring (MBAM) 2.0 bietet eine vereinfachte Verwaltungsschnittstelle zur BitLocker-Laufwerkverschlüsselung. BitLocker bietet erweiterten Schutz vor Datendiebstahl oder Datengefährdung für Computer, die verloren gehen oder gestohlen werden. BitLocker verschlüsselt alle Daten, die auf dem Windows-Betriebssystemvolume gespeichert sind, und konfigurierte Datenmengen.

## Informationen zu mbam 2.0


BitLockerAdministration und Monitoring 2.0 erzwingt die BitLocker-Verschlüsselungsrichtlinien Optionen, die Sie für Ihr Unternehmen festzulegen, überwacht die Kompatibilität von Clientcomputern mit diesen Richtlinien und berichtet über den Verschlüsselungsstatus von Unternehmens-und einzelnen Computern. Darüber hinaus können Sie mit MBAM auf die Wiederherstellungsschlüssel Informationen zugreifen, wenn Benutzer Ihre PIN oder Ihr Kennwort vergessen oder wenn sich der BIOS-oder Boot-Eintrag geändert hat.

**Hinweis**  BitLocker wird in diesem Leitfaden nicht ausführlich behandelt. Eine Übersicht über BitLocker finden Sie unter [Übersicht über die BitLocker-Laufwerkverschlüsselung](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

Die folgenden Gruppen sind möglicherweise an der Verwendung von MBAM für die Verwaltung von BitLocker interessiert:

-   Administratoren, IT-Sicherheitsexperten und Compliance Officer, die dafür verantwortlich sind, sicherzustellen, dass vertrauliche Daten nicht ohne Autorisierung freigegeben werden

-   Administratoren, die für die Computersicherheit in Remote-oder Zweigstellen zuständig sind

-   Administratoren, die für Clientcomputer mit Windows verantwortlich sind

## <a href="" id="what-s-new-in-mbam-2-0"></a>Neuerungen in mbam 2.0


Mbam 2.0 bietet die folgenden neuen Features und Funktionen.

### Integration von System Center Configuration Manager in MBAM

MBAM unterstützt jetzt die Integration in System Center Configuration Manager. Durch diese Integration wird die MBAM-Kompatibilitäts Infrastruktur in die systemeigene Umgebung von Configuration Manager verschoben. IT-Administratoren, die Configuration Manager in Ihrem Unternehmen verwenden, können nun den Konformitätsstatus Ihres Unternehmens in der Microsoft Management Console anzeigen und in Berichte einen Drilldown ausführen, um einzelne Computer anzuzeigen.

### Hardware Kompatibilität steht nur in der Configuration Manager-Integrations Topologie zur Verfügung.

Die Integration von Configuration Manager in MBAM ermöglicht Configuration Manager-Funktionen, die die Verwendung bestimmter Hardwaretypen mit MBAM zulassen oder verbieten, und bietet mehr Flexibilität als die Hardwarekompatibilität, die in MBAM 1,0 zur Verfügung stand. IT-Administratoren können eigene Sammlungen erstellen, um die Hardware zu begrenzen und die MBAM-Konfigurationsbasislinie für diese Auflistungen bereitzustellen. Die MBAM-Hardwarekompatibilität, die in MBAM 1,0 vorhanden war, ist jetzt nur in der MBAM Configuration Manager-Topologie verfügbar und wird über Configuration Manager verwaltet.

### Flexible Richtlinie für Protektoren

Computer, die bereits mit einem Protector verschlüsselt sind (beispielsweise TPM + PIN oder automatische Sperrung und Kennwort) und eine MBAM-Richtlinie erhalten, die eine Teilmenge dieser Verschlüsselung erfordert (beispielsweise TPM oder Auto-Unlock), gelten als kompatibel. Im obigen Beispiel werden PIN und Kennwort nicht automatisch entfernt, es sei denn, der IT-Administrator definiert diese Features ausdrücklich als nicht mehr zulässig.

Computer, die nicht verschlüsselt sind und eine MBAM-Richtlinie erhalten (beispielsweise TPM oder automatische Sperrung), werden entsprechend verschlüsselt. Benutzern, die lokale Administratoren sind, ist es gestattet, die BitLocker-Tools (Control Panel-Element BitLocker Drive Encryption oder Manage-BDE) zum Hinzufügen oder Ändern vorhandener Schutzelemente (beispielsweise TPM + PIN oder Auto-Unlock und Kennwort) zu verwenden. Sie bleiben nur dann kompatibel, wenn Sie von MBAM-Richtlinien ausdrücklich definiert werden.

### Möglichkeit zum Upgrade des MBAM-Clients

Der mbam 2.0-Client Windows Installer erkennt die Version des vorhandenen Clients und führt die erforderlichen Schritte aus, um aus früheren Versionen auf den mbam 2.0-Client zu aktualisieren.

### Möglichkeit zum Upgrade des MBAM-Servers aus früheren Versionen

Sie können die MBAM 2.0-Server Infrastruktur aus früheren Versionen von MBAM wie folgt aktualisieren:

**Manueller in-Place-Server Austausch** – Sie müssen die vorhandene MBAM-Serverinfrastruktur manuell deinstallieren und dann die MBAM 2,0-Serverinfrastruktur installieren. Sie müssen die Datenbanken nicht entfernen, um das Upgrade durchzuführen. Stattdessen wählen Sie die vorhandenen Datenbanken aus, die von der vorherigen Version des MBAM-Clients erstellt wurden. Die MBAM 2.0-Upgrade-Installation migriert dann die vorhandenen Datenbanken zu MBAM 2,0.

**Upgrade des verteilten Clients** – Wenn Sie die eigenständige MBAM-Topologie verwenden, können Sie die MBAM-Clients nach der Installation der MBAM 2,0-Server Infrastruktur schrittweise aktualisieren. Der MBAM 2,0-Server erkennt die Version des vorhandenen Clients und führt die erforderlichen Schritte aus, um auf den 2,0-Client zu aktualisieren.

Nachdem Sie die MBAM 2,0-Serverinfrastruktur aktualisiert haben, melden MBAM 1,0-Clients weiterhin erfolgreich an den MBAM 2,0-Server, indem Sie Wiederherstellungsdaten überwachen, aber die Compliance basiert auf den Richtlinien in MBAM 1,0. Sie müssen Clients auf MBAM 2,0 aktualisieren, damit Clientcomputer die Kompatibilität mit den MBAM 2,0-Richtlinien exakt melden. Sie können die Clients auf den MBAM 2,0-Client aktualisieren, ohne den vorherigen Client zu deinstallieren, und der Client beginnt, MBAM 2,0-Richtlinien anzuwenden und zu melden.

Wenn Sie MBAM mit Configuration Manager verwenden, müssen Sie die MBAM 1,0-Clients auf MBAM 2,0 aktualisieren.

### <a href="" id="mbam-support-for-bitlocker-s-enterprise-scenarios-on-the-windows-8-platform"></a>MBAM-Unterstützung für BitLocker-Enterprise-Szenarien auf der Windows 8-Plattform

MBAM unterstützt das Windows 8-Betriebssystem als Zielplattform für die MBAM-Client Installation. Mit dieser Unterstützung können IT-Administratoren den MBAM-Agent installieren, Windows 8-Betriebssystemlaufwerke verschlüsseln und über die Kompatibilität der Computer Berichten. MBAM nutzt die TPM-und TPM +-PIN-Protektoren, um das Windows 8-Betriebssystem genauso zu verwalten wie das BetriebssystemWindows 7. Mbam 2.0 bietet zudem Unterstützung für die Verschlüsselung von Windows to go-Clients.

### Hinzufügen des Self-Service-Portals

Endbenutzer können jetzt das Self-Service-Portal verwenden, um Ihre Wiederherstellungsschlüssel wiederherzustellen. Das Self-Service-Portal kann auf einem einzelnen Server mit den anderen MBAM-Features bereitgestellt werden, oder auf einem separaten Server, der IT-Administratoren die Flexibilität bietet, das Self-Server-Portal den Benutzern nach Bedarf verfügbar zu machen. Nachdem das Self-Service-Portal Benutzer authentifiziert hat, müssen die Benutzer nur die ersten acht Ziffern der Wiederherstellungsschlüssel-ID eingeben, um den Wiederherstellungsschlüssel zu erhalten.

MBAM sichert auch den Schlüssel, indem Benutzer die Schlüssel nur für die Computer wiederherstellen können, auf denen Sie Benutzer sind, wodurch das Risiko verringert wird, dass andere Benutzer nicht autorisierten Zugriff erhalten.

### Möglichkeit zum automatischen fortsetzen des BitLocker-Schutzes aus einem angehalten Zustand

MBAM ermöglicht es IT-Administratoren nicht mehr, BitLocker für längere Zeit angehalten und ungeschützt zu halten. Wenn ein IT-Administrator BitLocker unterbricht, aktiviert MBAM ihn automatisch, wenn der Computer neu gestartet wird, wodurch das Risiko verringert wird, dass der Computer angegriffen werden kann.

### Feste Datenlaufwerke können so konfiguriert werden, dass Sie ohne Kennwort automatisch freigegeben werden.

Eine Richtlinie mit festem Datenlaufwerk (Diskettenlaufwerk) kann jetzt so konfiguriert werden, dass die automatische Freigabe des Laufwerks ohne Kennwort ermöglicht wird. Benutzer werden nicht zur Eingabe eines Kennworts aufgefordert, bevor das Diskettenlaufwerk verschlüsselt wird, und das Diskettenlaufwerk wird mit dem Betriebssystemlaufwerk gesichert und automatisch gesperrt.

## <a href="" id="---------mbam-2-0-release-notes"></a> Mbam 2.0-Versionshinweise


Weitere Informationen sowie aktuelle Neuigkeiten, die nicht in der Dokumentation enthalten sind, finden Sie in den Versionshinweisen [zu MBAM 2,0](release-notes-for-mbam-20-mbam-2.md).

## So erhalten Sie mbam 2.0


Diese Technologie ist Teil des Microsoft Desktop Optimization Pack (MDOP). Unternehmenskunden können MDOP mit Microsoft Software Assurance erhalten. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049)

## Verwandte Themen


[Erste Schritte mit MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





