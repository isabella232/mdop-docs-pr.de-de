---
title: So stellen Sie App-V-Client bereit
description: So stellen Sie App-V-Client bereit
ms.author: dansimp
author: dansimp
ms.assetid: 9c4e67ae-ddaf-4e23-8c16-72d029a74a27
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/05/2018
ms.openlocfilehash: 4e246e13bf59f167eade77200afd866c6a3c41fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805489"
---
# So stellen Sie App-V-Client bereit


Gehen Sie wie folgt vor, um den Microsoft Application Virtualization (App-V) 5,0-Client und den Remote Desktop Dienste-Client zu installieren. Sie müssen die Version des Clients installieren, die dem Betriebssystem des Zielcomputers entspricht.

<a href="" id="bkmk-clt-install-prereqs"></a>**Was zu tun ist, bevor Sie beginnen**

1. Überprüfen und installieren Sie die erforderlichen Softwarevoraussetzungen:

   Installieren Sie die erforderliche Software, die der Version von App-V entspricht, die Sie installieren:

   - [Informationen zu App-V 5.0 SP3](about-app-v-50-sp3.md)

   - App-v 5,0 SP1 und App-v 5,0 SP2 – keine neuen Voraussetzungen in diesen Versionen

   - [Voraussetzungen für App-V 5.0](app-v-50-prerequisites.md)

2. Überprüfen Sie die Client Koexistenz und die nicht unterstützten Szenarios, wie Sie für Ihre Installation gelten:


   |                                               |                                                                                                                            |
   |-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
   |      Bereitstellen von nebeneinander vorhandenen App-V-Clients       | [Planen für die Bereitstellung von App-V 5.0-Sequencer und -Client](planning-for-the-app-v-50-sequencer-and-client-deployment.md) |
   | Nicht unterstützte oder begrenzte Installationsszenarien |                         [Unterstützte App-V 5.0-Konfigurationen](app-v-50-supported-configurations.md)                         |

   ---

3. Überprüfen Sie die Speicherorte für Clientregistrierung, Protokoll und Informationen zur Problembehandlung:

#### Client Registrierungsinformationen
<ul><li>Standardmäßig werden die Clientinformationen nach der Installation des App-V 5,0-Clients in der Registrierung im folgenden Registrierungsschlüssel gespeichert:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\APPV\CLIENT</code></li><li>Wenn Sie ein virtualisiertes Paket auf einem Computer bereitstellen, auf dem der App-V-Client ausgeführt wird, werden die zugehörigen Paketdaten an folgendem Speicherort gespeichert:<p><p><code>C:\ProgramData\App-V</code><p><p>Sie können diesen Speicherort jedoch mit dem folgenden Registrierungsschlüssel neu konfigurieren:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\SOFTWARE\MICROSOFT\APPV\CLIENT\STREAMING\PACKAGEINSTALLATIONROOT</code></li></ul>

#### Client Protokolldateien                  
<ul><li>Suchen Sie für Protokolldateiinformationen, die dem App-V 5,0-Client zugeordnet sind, im folgenden Protokoll:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV</code></li><li>In App-V 5,0 SP3 wurden einige Protokolle konsolidiert und an den folgenden Speicherort verschoben:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</code><p><p>Eine Liste der verschobenen Protokolle finden Sie unter [Informationen zu App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</li><li>Pakete, die derzeit auf Computern gespeichert sind, auf denen der App-V 5,0-Client ausgeführt wird, werden an folgendem Speicherort gespeichert:<p><p><code>C:\ProgramData\App-V\<<em>package id</em>>\<<em>version id</em>></code></li></ul>

#### Informationen zur Problembehandlung bei der Client Installation
- Sehen Sie sich das Fehlerprotokoll im Ordner **% Temp%** an. 
- Wenn Sie die Protokolldateien überprüfen möchten, klicken Sie auf **Start**, geben Sie **% Temp%** ein, und suchen Sie dann nach dem **appv_ Protokoll**. 

## So installieren Sie den App-V 5,0-Client

1. Kopieren Sie die App-V 5,0-Clientinstallationsdatei auf den Computer, auf dem Sie installiert werden soll.<p><p>Wählen Sie eine der folgenden Clienttypen aus:


   |                  Clienttyp                  |          Zu verwendende Datei          |
   |-----------------------------------------------|-------------------------------|
   |        Standard Version des Clients         |   **appv_client_setup.exe**   |
   | Version des Clients für Remote Desktop Dienste | **appv_client_setup_rds.exe** |

   ---

2. Doppelklicken Sie auf die Installationsdatei, und klicken Sie auf **Installieren**. Vor Beginn der Installation überprüft das Installationsprogramm den Computer auf alle fehlenden [App-V 5,0-Voraussetzungen](app-v-50-prerequisites.md).

3. Überprüfen und akzeptieren Sie die Software-Lizenzbestimmungen, wählen Sie aus, ob Sie Microsoft Update verwenden möchten und ob Sie am Programm zur Verbesserung der Benutzerfreundlichkeit von Microsoft teilnehmen möchten, und klicken Sie auf **Installieren**.

4. Klicken Sie auf der Seite **Setup erfolgreich abgeschlossen** auf **Schließen**.

   Bei der Installation werden die folgenden Einträge für den App-V-Client in **Programmen**erstellt:

   -   **EXE**

   -   **.msi**

   -   **Sprachpaket**

   >[!NOTE]
   >Nach der Installation kann nur die exe-Datei deinstalliert werden.


## So installieren Sie den App-V 5,0-Client mithilfe eines Skripts

1. Installieren Sie alle erforderlichen Softwarevoraussetzungen auf den Zielcomputern. Schauen Sie [sich an, was Sie vor Beginn tun sollten](#bkmk-clt-install-prereqs). Wenn Sie den Client mithilfe einer MSI-Datei installieren, schlägt die Installation fehl, wenn keine Voraussetzungen vorhanden sind.

2. Wenn Sie ein Skript zum Installieren des App-V 5,0-Clients verwenden möchten, verwenden Sie die folgenden Parameter mit **appv\_client\_setup.exe**.

   >[!NOTE]
   >Der Client Windows Installer (MSI) unterstützt den gleichen Satz von Schaltern, mit Ausnahme des **/Log** -Parameters.

   |                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   |----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |           /INSTALLDIR            |                                                                                                                                                               Gibt das Installationsverzeichnis an. Beispielanwendung:<p><p>**/INSTALLDIR = C:\Program Files\AppV-Client**                                                                                                                                                                |
   |            /CEIPOPTIN            |                                                                                                                                                          Ermöglicht die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit. Beispielanwendung:<p><p>**/CEIPOPTIN = [0 \ | 1 \]**                                                                                                                                                           |
   |             /MUOPTIN             |                                                                                                                                                                                 Aktiviert Microsoft Update. Beispielanwendung:<p><p>**/MUOPTIN = [0 \ | 1 \]**                                                                                                                                                                                  |
   |     /PACKAGEINSTALLATIONROOT     |                                                                                                                                         Gibt das Verzeichnis an, in dem alle neuen Anwendungen und Updates installiert werden sollen. Beispielanwendung: <p><p>**/PACKAGEINSTALLATIONROOT = ' C:\app-V-Pakete '**                                                                                                                                         |
   |        /PACKAGESOURCEROOT        |                                                                                                                                                  Überschreibt den Quellspeicherort zum Herunterladen von Paketinhalten. Beispielanwendung:<p><p>**/PACKAGESOURCEROOT = ' <http://packageStore> '**                                                                                                                                                  |
   |            /AUTOLOAD             |                                                                                           Gibt an, wie neue Pakete von App-V 5,0 auf einem bestimmten Computer geladen werden. Die folgenden Optionen sind aktiviert: [1]; Alle Pakete automatisch laden [2]; oder laden Sie keine Pakete automatisch [0]. Beispielanwendung:<p><p>**/AUTOLOAD = [0 \ | 1 \ | 2 \]**                                                                                           |
   |     /SHAREDCONTENTSTOREMODE      |                                                                                                                                           Gibt an, dass Streaming-Paketinhalt nicht auf der lokalen Festplatte gespeichert werden soll. Beispielanwendung: <p><p>**/SHAREDCONTENTSTOREMODE = [0 \ | 1 \]**                                                                                                                                            |
   |          /MIGRATIONMODE          |                                                                                                                     Ermöglicht es dem App-V 5,0-Client, die Verknüpfungen und FTA zu ändern, die den Paketen zugeordnet sind, die mit einer früheren Version erstellt wurden. Beispielanwendung:<p><p>**/MIGRATIONMODE = [0 \ | 1 \]**                                                                                                                     |
   |      /ENABLEPACKAGESCRIPTS       |                                                                                                                                   Aktiviert die Skripts, die in der Datei des paketmanifests oder der Konfigurationsdateien definiert sind, die ausgeführt werden sollen. Beispielanwendung:<p><p>**/ENABLEPACKAGESCRIPTS = [0 \ | 1 \]**                                                                                                                                   |
   |    /ROAMINGREGISTRYEXCLUSIONS    |                                                                                                                                      Gibt die Registrierungspfade an, die nicht mit einem Benutzerprofil durchlaufen werden. Beispielanwendung:<p><p>**/ROAMINGREGISTRYEXCLUSIONS = software\classes; Software\Clients**                                                                                                                                      |
   |      /ROAMINGFILEEXCLUSIONS      |                                                                                                                                  Gibt die Dateipfade relativ zu% User Profile% an, die nicht mit dem Profil eines Benutzers Roamen. Beispielanwendung: <p><p>**/ROAMINGFILEEXCLUSIONS ' Desktop; meine Bilder '**                                                                                                                                   |
   |   /S [1-5] PUBLISHINGSERVERNAME    |                                                                                                                                                           Zeigt den Namen des Veröffentlichungsservers an. Beispielanwendung:<p><p>**/S2PUBLISHINGSERVERNAME = MyPublishingServer**                                                                                                                                                            |
   |    /S [1-5] PUBLISHINGSERVERURL    |                                                                                                                                                                Zeigt die URL des Veröffentlichungsservers an. Beispielanwendung:<p><p>**/S2PUBLISHINGSERVERURL = \\pubserver**                                                                                                                                                                |
   |   /S [1-5] GLOBALREFRESHENABLED    |                                                                                                                                                                    Aktiviert eine globale Veröffentlichungsaktualisierung. Beispielanwendung:<p><p>**/S2GLOBALREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                     |
   |   /S [1-5] GLOBALREFRESHONLOGON    |                                                                                                                                                             Initiiert eine globale Veröffentlichungsaktualisierung, wenn sich ein Benutzer anmeldet. Beispielanwendung:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                              |
   |   /S [1-5] GLOBALREFRESHINTERVAL   |                                                                                                                                         Gibt das Aktualisierungsintervall für die Veröffentlichung an, wobei **0** angibt, dass Sie nicht regelmäßig aktualisiert werden. Verwendungsbeispiel: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   | /S [1-5] GLOBALREFRESHINTERVALUNIT |                                                                                                                                                            Gibt die Intervalleinheit an (Stunden [0], Tage [1]). Beispielanwendung:<p><p>**/S2GLOBALREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                            |
   |    /S [1-5] USERREFRESHENABLED     |                                                                                                                                                                          Aktiviert die Aktualisierung der Benutzer Veröffentlichung. Beispiel Verwendung: **/S2USERREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                          |
   |    /S [1-5] USERREFRESHONLOGON     |                                                                                                                                                              Initiiert eine Aktualisierung der Benutzer Veröffentlichung, wenn sich ein Benutzer anmeldet. Beispielanwendung:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                               |
   |    /S [1-5] USERREFRESHINTERVAL    |                                                                                                                                         Gibt das Aktualisierungsintervall für die Veröffentlichung an, wobei **0** angibt, dass Sie nicht regelmäßig aktualisiert werden. Verwendungsbeispiel: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   |  /S [1-5] USERREFRESHINTERVALUNIT  |                                                                                                                                                             Gibt die Intervalleinheit an (Stunden [0], Tage [1]). Beispielanwendung:<p><p>**/S2USERREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                             |
   |               /Log               |                                                                                                                                                Gibt einen Speicherort an, an dem die Protokollinformationen gespeichert werden. Der Standardspeicherort ist% Temp%. Beispielanwendung:<p><p>**/Log C:\logs\log.log**                                                                                                                                                |
   |                /q                |                                                                                                                                                                                                Gibt eine unbeaufsichtigte Installation an.                                                                                                                                                                                                |
   |             /Repair              |                                                                                                                                                                                               Repariert eine vorherige Clientinstallation.                                                                                                                                                                                               |
   |            /NORESTART            | Verhindert, dass der Computer nach der Clientinstallation neu gestartet wird.<p><p>Der Parameter verhindert, dass der Computer des Endbenutzers nach jedem Update neu gestartet wird, und Sie können den Neustart nach Belieben planen. So können Sie beispielsweise App-V 5,0 SPX installieren und dann das Hotfix-Paket Y installieren, ohne nach der Installation des Service Packs einen Neustart durchführen zu müssen. Nach der Installation müssen Sie den Computer neu starten, bevor Sie App-V verwenden. |
   |            /Uninstall            |                                                                                                                                                                                                       Deinstalliert den Client.                                                                                                                                                                                                        |
   |           /ACCEPTEULA            |                                                                                                                                              Akzeptiert den Lizenzvertrag. Dies ist für eine unbeaufsichtigte Installation erforderlich. Beispielanwendung:<p><p>**/ACCEPTEULA** oder **/ACCEPTEULA = 1**                                                                                                                                               |
   |             /LAYOUT              |                                                                                                                               Gibt die zugeordnete Layout-Aktion an. Außerdem werden die Windows Installer-Dateien (MSI) und Skriptdateien in einen Ordner extrahiert, ohne App-V 5,0 zu installieren. Es wird kein Wert erwartet.                                                                                                                                |
   |            /LAYOUTDIR            |                                                                                                                                                 Gibt das layoutverzeichnis an. Erfordert einen Zeichenfolgenwert. Beispielanwendung:<p><p>**/LAYOUTDIR = "C:\Application Virtualization Client"**                                                                                                                                                  |
   |          /?,/h,/Help           |                                                                                                                                                                                      Fordert Hilfe zu den vorherigen Installationsparametern an.                                                                                                                                                                                      |

   ---

## So installieren Sie den App-V 5,0-Client mithilfe der Windows Installer-Datei (MSI)

1. Installieren Sie die erforderlichen Voraussetzungen auf den Zielcomputern. Schauen Sie [sich an, was Sie vor Beginn tun sollten](#bkmk-clt-install-prereqs). Wenn keine Voraussetzungen erfüllt sind, schlägt die Installation fehl.

2. Stellen Sie sicher, dass die Zielcomputer keine ausstehenden Neustarts haben, bevor Sie den Client mithilfe der App-V 5,0 Windows Installer-Dateien (MSI) installieren. Die Windows Installer-Dateien kennzeichnen keinen ausstehenden Neustart.

3. Stellen Sie eine der folgenden Windows Installer-Dateien auf dem Zielcomputer bereit. Die von Ihnen angegebene Datei muss der Konfiguration des Zielcomputers entsprechen.


   |                       Art der Bereitstellung                        |      Diese Datei bereitstellen       |
   |-----------------------------------------------------------------|-----------------------------|
   | Auf dem Computer befindet sich ein Microsoft Windows-32-Bit-Betriebssystem |   appv_client_MSI_x86.msi   |
   | Auf dem Computer befindet sich ein Microsoft Windows-64-Bit-Betriebssystem |   appv_client_MSI_x64.msi   |
   | Sie stellen den App-V 5,0-Client für Remote Desktop Dienste bereit.  | appv_client_rds_MSI_x64.msi |

   ---

4. Wählen Sie anhand der Informationen in der folgenden Tabelle auf der Grundlage der gewünschten Sprache für den Zielcomputer das entsprechende Sprachpaket **. msi** aus, das Sie installieren möchten. **Xxxx** in der Tabelle bezieht sich auf das Zielgebietsschema des Sprachpakets.

   **Was Sie wissen sollten, bevor Sie beginnen:** 

   -  Die Sprachpakete sind sowohl für den standardmäßigen App-v 5,0-Client als auch für die Remote Desktop Dienste-Version des App-v 5,0-Clients üblich.

   -  Wenn Sie den App-V 5,0-Client mithilfe der **exe**-Datei installieren, wird vom Installationsprogramm nur das Sprachpaket bereitgestellt, das dem auf dem Zielcomputer ausgeführten Betriebssystem entspricht.

   -  Zum Bereitstellen weiterer Sprachpakete auf einem Zielcomputer verwenden Sie das Verfahren **zum Installieren des App-V 5,0-Clients mithilfe der Windows Installer-Datei (MSI)**.

   |                       Art der Bereitstellung                        |       Diese Datei bereitstellen       |
   |-----------------------------------------------------------------|------------------------------|
   | Auf dem Computer befindet sich ein Microsoft Windows-32-Bit-Betriebssystem | appv_client_LP_xxxx_ x86.msi |
   | Auf dem Computer befindet sich ein Microsoft Windows-64-Bit-Betriebssystem | appv_client_LP_xxxx_ x64.msi |

   ---

   Sie **haben einen Vorschlag für App-V**? [Vorschläge](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)hinzufügen oder abstimmen. <p><p>**Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Bereitstellen von App-V 5.0](deploying-app-v-50.md)

[Informationen über Clientkonfigurationseinstellungen](about-client-configuration-settings.md)

[So deinstallieren Sie den App-V 5.0-Client](how-to-uninstall-the-app-v-50-client.md)
