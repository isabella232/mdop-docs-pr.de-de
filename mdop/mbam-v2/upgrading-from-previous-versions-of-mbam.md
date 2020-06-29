---
title: Aktualisieren von früheren MBAM-Versionen
description: Aktualisieren von früheren MBAM-Versionen
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810177"
---
# Aktualisieren von früheren MBAM-Versionen


Sie können die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der eigenständigen Topologie oder der Configuration Manager-Topologie auf MBAM 2.0 aktualisieren, indem Sie wie folgt vorgehen:

-   **Manueller in-Place-Server Austausch** – um den MBAM-Server zu aktualisieren, deinstallieren Sie MBAM manuell mithilfe des Installationsprogramms oder der Systemsteuerung, und installieren Sie dann die MBAM 2.0-Infrastruktur. Sie müssen die Datenbanken nicht entfernen. Bei der Deinstallation des MBAM 1,0-Servers bleiben die MBAM-Datenbanken intakt. Wenn Sie dieselben Datenbanken angeben, die von MBAM 1,0 verwendet wurden, behält die MBAM 2.0-Installation MBAM 1,0-Daten in den Datenbanken bei und wandelt die Datenbanken in die Arbeit mit MBAM 2.0 um.

-   **Upgrade des verteilten Clients** – Wenn Sie die eigenständige MBAM-Topologie verwenden, können Sie die MBAM-Clients nach der Installation der MBAM 2,0-Server Infrastruktur schrittweise aktualisieren. Der MBAM 2,0-Server erkennt die Version des vorhandenen Clients und führt die erforderlichen Schritte aus, um auf den 2,0-Client zu aktualisieren.

    Nachdem Sie die MBAM 2,0-Serverinfrastruktur aktualisiert haben, melden MBAM 1,0-Clients weiterhin erfolgreich an den MBAM 2,0-Server, indem Sie Wiederherstellungsdaten überwachen, aber die Compliance basiert auf den Richtlinien in MBAM 1,0. Sie müssen Clients auf MBAM 2,0 aktualisieren, damit Clientcomputer die Kompatibilität mit den MBAM 2,0-Richtlinien exakt melden. Sie können die Clients auf den MBAM 2,0-Client aktualisieren, ohne den vorherigen Client zu deinstallieren, und der Client beginnt, MBAM 2,0-Richtlinien anzuwenden und zu melden.

    Wenn Sie MBAM mit Configuration Manager verwenden, müssen Sie die MBAM 1,0-Clients auf MBAM 2,0 aktualisieren.

## Aktualisieren von MBAM von einer Architektur mit zwei Servern


Führen Sie die folgenden Anweisungen aus, um eine frühere Version von MBAM zu aktualisieren, wenn Sie eine Architektur mit zwei Servern verwenden, bei der ein Server die Microsoft SQL Server-Komponenten hostet und der andere Server die Websites und Dienste hostet.

**So aktualisieren Sie MBAM von einer Architektur mit zwei Servern**

1.  Wählen Sie auf dem Server mit den SQL Server-Features in der Systemsteuerung die Option **Programme und Features**aus, und deinstallieren Sie dann die **Microsoft BitLocker-Verwaltung und-Überwachung**. Die Datenbank für die Wiederherstellung und die Konformitäts-und Überwachungsdatenbank bleiben unverändert.

2.  Führen Sie **MBAMSetup.exe** für Version MBAM 2,0 aus, und wählen Sie optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.

3.  Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

4.  Wählen Sie auf der Seite **Topologie Auswahl** die **eigenständige** oder **System Center Configuration Manager-Integrations** Topologie aus, und klicken Sie dann auf **weiter**.

5.  Deaktivieren Sie auf der Seite **zu installierende Features auswählen** die Features **Self-Service Server** und **Administration und Monitoring Server** , und klicken Sie dann auf **weiter**.

6.  Warten Sie, bis die Voraussetzungen für die Prüfung abgeschlossen sind, und klicken Sie dann auf **weiter**. Wenn eine fehlende Voraussetzung erkannt wird, beheben Sie die fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.

7.  Geben Sie auf dem Konto für den **Zugriff auf die Seite MBAM-Datenbanken** den Computernamen für den Server ein, der die Websites und Dienste hosten soll, und klicken Sie dann auf **weiter**.

8.  Geben Sie auf der Seite " **Wiederherstellungsdatenbank konfigurieren** " den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert werden. Sie müssen außerdem angeben, wo sich die Datenbankdateien und Protokollinformationen befinden sollen.

9.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

10. Geben Sie auf der Seite **Compliance-und Überwachungsdatenbank konfigurieren** den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert werden.

11. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

12. Geben Sie auf der Seite **Compliance-und Überwachungsberichte konfigurieren** die SQL Server Reporting Services-Instanz an, in der die Kompatibilitäts-und Überwachungsberichte installiert werden, und geben Sie ein Domänenbenutzerkonto und ein Kennwort für den Zugriff auf die Datenbank Compliance und Audit an. Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft. Das Benutzerkonto kann auf alle Daten zugreifen, die der Gruppe MBAM-Berichte Benutzer zur Verfügung stehen.

13. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

14. Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**. Damit werden die automatischen Updates in Windows nicht aktiviert. Wenn Sie zuvor entschieden haben, Microsoft Update für dieses Produkt oder ein anderes Produkt zu verwenden, wird die Seite Microsoft Update nicht angezeigt.

15. Überprüfen Sie auf der Seite **Installationszusammenfassung** die Features, die installiert werden sollen, und klicken Sie dann auf **Installieren** , um die Installation zu starten.

**So deinstallieren Sie die Verwaltungs-und Überwachungs Server Features und führen das Upgrade durch**

1.  Wählen Sie auf dem Computer, der die Verwaltungs-und Überwachungs Server Features hostet, in der Systemsteuerung die Option **Programme und Features**aus, und deinstallieren Sie MBAM, um die zuvor installierten Websites und Dienste zu entfernen.

2.  Führen Sie die **MBAMSetup.exe** für Version 2,0 aus, und wählen Sie optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.

3.  Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

4.  Wählen Sie auf der Seite **Topologie Auswahl** die **eigenständige** oder **System Center Configuration Manager-Integrations** Topologie aus, und klicken Sie dann auf **weiter**.

5.  Deaktivieren Sie auf der Seite **zu installierende Features auswählen** die Features **Recovery Database** und **Compliance und Audit Database** sowie **Compliance und Überwachungsberichte** , und klicken Sie dann auf **weiter**.

6.  Warten Sie, bis die Voraussetzungen für die Prüfung abgeschlossen sind, und klicken Sie dann auf **weiter**. Wenn eine fehlende Voraussetzung erkannt wird, beheben Sie zuerst die fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.

7.  Wählen Sie auf der Seite **Netzwerk Kommunikationssicherheit konfigurieren** aus, ob die SSL-Verschlüsselung (Secure Socket Layer) für die Websites und Dienste verwendet werden soll. Wenn Sie sich entschließen, die Kommunikation zu verschlüsseln, wählen Sie das Zertifizierungsstellenzertifikat aus, das Sie für die Verschlüsselung verwenden möchten.

    **Hinweis**  Das Zertifikat muss vor diesem Schritt erstellt werden, damit Sie es auf dieser Seite auswählen können.

     

8.  Geben Sie auf der Seite **Konfigurieren Sie den Speicherort der Kompatibilitäts Status Datenbank** den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert sind. Sie müssen außerdem angeben, wo sich die Datenbankdateien und Protokollinformationen befinden sollen.

9.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

10. Geben Sie auf der Seite **Konfigurieren Sie den Speicherort der Wiederherstellungsdatenbank** an den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert sind.

11. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

12. Geben Sie auf der Seite **Compliance-und Überwachungsberichte konfigurieren** die URL für die Berichterstellungsinstanz ein, die Sie auf dem anderen Server konfiguriert haben. Verwenden Sie die Schaltfläche **Testen** , um zu überprüfen, ob Sie die Website erreichen können.

13. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

14. Geben Sie auf der Seite **Self-Service-Portal konfigurieren** die Portnummer, den Hostnamen, den Namen des virtuellen Verzeichnisses und den Installationspfad für das Self-Service-Portal ein.

    **Hinweis**  Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungs Server sein, sofern Sie keinen eindeutigen Hostheadernamen angeben.

     

15. Geben Sie auf der Seite **Verwaltungs-und Überwachungs Server konfigurieren** das gewünschte virtuelle Verzeichnis für die Helpdesk-Website an.

16. Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**. In diesem Schritt werden die automatischen Updates in Windows nicht aktiviert. Wenn Sie zuvor entschieden haben, Microsoft Update für dieses Produkt oder ein anderes Produkt zu verwenden, wird die Seite Microsoft Update nicht angezeigt.

17. Überprüfen Sie auf der Seite **Installationszusammenfassung** die Features, die installiert werden sollen, und klicken Sie dann auf **Installieren** , um die Installation zu starten.

18. Um zu überprüfen, ob das Upgrade erfolgreich war, stellen Sie sicher, dass Sie jede Website von einem anderen Computer in der Domäne erreichen können.

## Aktualisieren des MBAM-Clients auf Endbenutzercomputern


Führen Sie **MbamClientSetup.exe** auf jedem Clientcomputer aus, um die Endbenutzercomputer auf den MBAM 2,0-Client zu aktualisieren. Das Installationsprogramm aktualisiert den Client automatisch auf den MBAM 2,0-Client. Sie können den MBAM-Client über ein elektronisches Softwareverteilungssystem, Tools wie Active Directory-Domänendienste oder System Center Configuration Manager installieren.

Gehen Sie wie folgt vor, um das Client Upgrade zu überprüfen:

1.  Warten Sie, bis der konfigurierte Berichtszyklus endet, und starten Sie dann **SQL Server Management Studio** auf dem SQL Server-Computer.

2.  Starten Sie **SQL Server Management Studio**auf dem SQL Server-Computer.

3.  Überprüfen Sie, ob die Tabelle **RecoveryAndHardwareCore. Machines** eine Zeile enthält, die den Computernamen des Endbenutzers anzeigt.

## Verwandte Themen


[Bereitstellen von MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





