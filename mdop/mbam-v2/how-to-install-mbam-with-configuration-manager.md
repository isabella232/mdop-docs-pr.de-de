---
title: So installieren Sie MBAM mit dem Konfigurations-Manager
description: So installieren Sie MBAM mit dem Konfigurations-Manager
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810969"
---
# So installieren Sie MBAM mit dem Konfigurations-Manager


In diesem Abschnitt werden die Schritte zum Installieren von MBAM mit Configuration Manager unter Verwendung der empfohlenen Konfiguration beschrieben, die in [Erste Schritte mit MBAM mit Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)veranschaulicht wird. Die Schritte sind in die folgenden Aufgaben gegliedert:

-   Installieren und Konfigurieren von MBAM auf dem Configuration Manager-Server

-   Installieren der Wiederherstellungs-und Überwachungsdatenbanken auf dem Daten Bank Server

-   Installieren der Verwaltungs-und Überwachungsserver Features auf dem Verwaltungs-und Überwachungsserver

Bevor Sie mit der Installation beginnen, stellen Sie sicher, dass Sie die erforderlichen MOF-Dateien bearbeitet oder erstellt haben. Anweisungen hierzu finden Sie unter [erstellen oder Bearbeiten von MOF-Dateien](how-to-create-or-edit-the-mof-files.md).

**Wichtig**  Wenn Sie eine nicht standardmäßige SQL Server Reporting Services (SSRS)-Instanz verwenden, müssen Sie das MBAM-Setup mithilfe der folgenden Befehlszeile starten, um die benannte SSRS-Instanz anzugeben:

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**So installieren Sie MBAM auf dem Configuration Manager-Server**

1.  Führen Sie auf dem Configuration Manager-Server **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.

    **Hinweis**  Um die Setupprotokolldateien zu erhalten, müssen Sie das msiexec-Paket und die Option **/l** &lt; Location verwenden, &gt; um Configuration Manager zu installieren. Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.

    Zusätzliche Setupprotokolldateien werden im Ordner% Temp% auf dem Computer des Benutzers erstellt, der Configuration Manager installiert.

     

2.  Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.

3.  Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

4.  Wählen Sie auf der Seite **Topologie Auswahl** die Option **System Center Configuration Manager-Integration**aus, und klicken Sie dann auf **weiter**.

5.  Wählen Sie auf der Seite **zu installierende Features auswählen** die Option **System Center Configuration Manager-Integration**aus.

    **Hinweis**  Klicken Sie auf der Seite **Voraussetzungen prüfen** auf **weiter** , nachdem der Installations-Assistent die Voraussetzungen für die Installation überprüft hat, und bestätigt, dass keine vorhanden sind. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen klicken.**

     

6.  Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**. Bei Verwendung von Microsoft Updates werden die automatischen Updates in Windows nicht aktiviert.

7.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

8.  Überprüfen Sie auf der Seite **Installationszusammenfassung** die Liste der Features, die installiert werden sollen, und klicken Sie auf **Installieren** , um mit der Installation der MBAM-Features zu beginnen. Klicken Sie auf **zurück** , um durch den Assistenten zurückzukehren, wenn Sie die Installationseinstellungen überprüfen oder ändern müssen, oder klicken Sie auf **Abbrechen** , um Setup zu beenden. Setup installiert die MBAM-Features und benachrichtigt Sie, dass die Installation abgeschlossen ist.

9.  Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.

**So installieren Sie die Wiederherstellungs-und Überwachungsdatenbanken auf dem Daten Bank Server**

1.  Führen Sie auf dem Daten Bank Server **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.

2.  Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.

3.  Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

4.  Wählen Sie auf der Seite **Topologie Auswahl** die **System Center Configuration Manager-Integrations** Topologie aus, und klicken Sie dann auf **weiter**.

5.  Wählen Sie in der Liste der zu installierenden Features die Option **Wiederherstellungsdatenbank** und **Überwachungsdatenbank**aus, und deaktivieren Sie die restlichen Features.

    **Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an. Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken. Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.

     

6.  Geben Sie auf der Seite " **Wiederherstellungsdatenbank konfigurieren** " die Namen der Computer an, auf denen das Feature "Verwaltungs-und Überwachungs Server" ausgeführt werden soll. Nach der Bereitstellung des Verwaltungs-und Überwachungs Server Features wird mit dem Domänenkonto eine Verbindung mit der Datenbank hergestellt.

7.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

8.  Geben Sie den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert werden sollen. Sie müssen außerdem angeben, an welcher Stelle die Datenbank gespeichert werden soll und wo sich die Protokollinformationen befinden sollen.

9.  Klicken Sie auf **weiter** , um mit dem MBAM Setup-Installations-Assistenten fortzufahren.

10. Geben Sie auf der Seite **Audit Database konfigurieren** das Benutzerkonto an, das für den Zugriff auf die Datenbank für Berichte verwendet wird.

11. Geben Sie die Computernamen der Computer an, auf denen der Verwaltungs-und Überwachungs Server und die Überwachungsberichte ausgeführt werden. Nachdem die Verwaltungs-und Überwachungs-und Überwachungsberichts Features bereitgestellt wurden, werden Ihre Domänenkonten zum Herstellen einer Verbindung mit den Datenbanken verwendet.

    **Hinweis**  Wenn Sie die Überwachungsdatenbank ohne das Feature Überwachungsberichte installieren, müssen Sie auf dem Überwachungsdaten Bank Computer eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Microsoft SQL Server-Port zu aktivieren. Die Standardportnummer ist 1433.

     

12. Geben Sie den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Überwachungsdaten gespeichert werden sollen. Sie müssen außerdem angeben, wo sich die Datenbank-und Protokollinformationen befinden sollen.

13. Klicken Sie auf **Installieren** , um die Installation zu starten, und klicken Sie dann auf **Fertig stellen** , um die Installation abzuschließen.

**So installieren Sie die Verwaltungs-und Überwachungsserver Features auf dem Verwaltungs-und Überwachungsserver**

1.  Führen Sie auf dem Verwaltungs-und Überwachungs Server **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.

2.  Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.

3.  Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

4.  Wählen Sie auf der Seite **Topologie Auswahl** die **System Center Configuration Manager-Integrations** Topologie aus, und klicken Sie dann auf **weiter**.

5.  Wählen Sie in der Liste der zu installierenden Features **Administration und Monitoring Server** und **Self-Service Portal**aus, und deaktivieren Sie die restlichen Funktionen.

    **Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an. Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken. Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.

     

6.  Installieren Sie das Self-Service-Portal, indem Sie die Schritte im Abschnitt **So installieren Sie das Self-Service-Portal** unter [so wird es gemacht: Installieren und Konfigurieren von MBAM auf verteilten Servern](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).

    **Hinweis**  Wenn die Clientcomputer nicht auf das Microsoft Content Delivery Network (CDN) zugreifen können, wodurch dem Self-Service-Portal der erforderliche Zugriff auf bestimmte JavaScript-Dateien gewährt wird, führen Sie die Schritte unter **so konfigurieren Sie das Self-Service-Portal aus, wenn Endbenutzer nicht auf den Abschnitt Microsoft Content Delivery Network zugreifen können** , [wie Sie MBAM auf verteilten Servern installieren und konfigurieren](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) können, um das Self-Service-Portal so zu konfigurieren, dass es von einer barrierefreien Quelle aus

     

7.  Installieren Sie die Verwaltungs-und Überwachungsserver Features, indem Sie die Schritte im Abschnitt **So installieren Sie den Verwaltungs-und Überwachungsserver-Feature** unter Installieren [und Konfigurieren von MBAM auf verteilten Servern](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md)ausführen.

8.  Klicken Sie auf **Fertig stellen** , um die Installation abzuschließen.

## Verwandte Themen


[So überprüfen Sie die MBAM-Installation mit dem Konfigurations-Manager](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[Bereitstellen von MBAM mit dem Konfigurations-Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





