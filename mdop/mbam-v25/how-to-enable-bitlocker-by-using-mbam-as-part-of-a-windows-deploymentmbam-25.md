---
title: So aktivieren Sie BitLocker im Rahmen einer Windows-Bereitstellung mithilfe von MBAM
description: So aktivieren Sie BitLocker im Rahmen einer Windows-Bereitstellung mithilfe von MBAM
author: dansimp
ms.assetid: 7609ad7a-bb06-47be-b186-0a2db787c8a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: cd4086ca6bb2ea8d253ea3b743f4efe7efbbb6c1
ms.sourcegitcommit: 325c4b77f9a9df0f3de268457fed06184623bb94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "11626182"
---
# <a name="how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deployment"></a>So aktivieren Sie BitLocker im Rahmen einer Windows-Bereitstellung mithilfe von MBAM

> [!IMPORTANT]
> Diese Anweisungen beziehen sich nicht auf configuration Manager BitLocker Management. Das `Invoke-MbamClientDeployment.ps1` PowerShell-Skript wird für die Verwendung mit BitLocker-Verwaltung in Configuration Manager nicht unterstützt. Dies umfasst das Einfügen von BitLocker-Wiederherstellungsschlüsseln während einer Configuration Manager-Tasksequenz. Darüber hinaus verwendet configuration Manager BitLocker Management ab Configuration Manager Current Branch 2103 nicht mehr die MbaM-Schlüsselwiederherstellungsdienste-Website, um Schlüssel zu escrow. Der Versuch, das `Invoke-MbamClientDeployment.ps1` PowerShell-Skript mit Configuration Manager Current Branch 2103 oder höher zu verwenden, kann zu schwerwiegenden Problemen mit der Configuration Manager-Website führen. Bekannte Probleme sind die Erstellung einer großen Menge von Richtlinien, die auf alle Geräte ausgerichtet sind, was zu Richtlinienstürmen führen kann. Dies führt zu einer schwerwiegenden Beeinträchtigung der Leistung in Configuration Manager in erster Linie in SQL und mit Verwaltungspunkten.

In diesem Thema wird erläutert, wie Sie BitLocker auf dem Computer eines Endbenutzers mithilfe von MBAM als Teil Ihres Windows Imageerstellungs- und Bereitstellungsprozesses aktivieren. Wenn beim Neustart (nach Abschluss der Installationsphase) ein schwarzer Bildschirm angezeigt wird, der angibt, dass das Laufwerk nicht entsperrt werden kann, lesen Sie [frühere Windows Versionen nach dem Schritt "Setup Windows und Configuration Manager" nicht starten, wenn BitLocker vor der Bereitstellung mit Windows 10, Version 1511, verwendet wird.](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo)

**Voraussetzungen:**

-   Ein vorhandener Windows Image-Bereitstellungsprozess – Microsoft Deployment Toolkit (MDT), Microsoft System Center Configuration Manager oder ein anderes Imageerstellungstool oder -verfahren – muss vorhanden sein.

-   TPM muss im BIOS aktiviert und für das Betriebssystem sichtbar sein

-   MBAM-Serverinfrastruktur muss eingerichtet sein und darauf zugegriffen werden können

-   Die für BitLocker erforderliche Systempartition muss erstellt werden.

-   Der Computer muss während der Imageerstellung domänenverbunden sein, bevor MBAM BitLocker vollständig aktiviert.

**So aktivieren Sie BitLocker mit MBAM 2.5 SP1 als Teil einer Windows Bereitstellung**

1. In MBAM 2.5 SP1 wird empfohlen, BitLocker während einer Windows Bereitstellung mithilfe des `Invoke-MbamClientDeployment.ps1` PowerShell-Skripts zu aktivieren.

   -   Das `Invoke-MbamClientDeployment.ps1` Skript setzt BitLocker während des Imageerstellungsprozesses um. Wenn dies für die BitLocker-Richtlinie erforderlich ist, fordert der MBAM-Agent den Domänenbenutzer sofort auf, eine PIN oder ein Kennwort zu erstellen, wenn sich der Domänenbenutzer nach der Imageerstellung zum ersten Mal anmeldet.

   -   Einfache Verwendung mit MDT-, System Center Configuration Manager- oder eigenständigen Imageerstellungsprozessen

   -   Kompatibel mit PowerShell 2.0 oder höher

   -   Verschlüsseln des Betriebssystemvolumes mit TPM-Schlüsselschutz

   -   BitLocker-Vorabbereitstellung vollständig unterstützen

   -   Optional verschlüsseln von FDDs

   -   Escrow TPM OwnerAuth For Windows 7, MBAM must own the TPM for escrow to occur.
   For Windows 8.1, Windows 10 RTM and Windows 10 version 1511, escrow of TPM OwnerAuth is supported.
   Für Windows 10, Version 1607 oder höher, können nur Windows den Besitz des TPM übernehmen. In addiiton behält Windows das TPM-Besitzerkennwort bei der Bereitstellung des TPM nicht bei. Weitere Details finden Sie [unter TPM-Besitzerkennwort.](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password)

   -   Escrow-Wiederherstellungsschlüssel und Wiederherstellungsschlüsselpakete

   -   Verschlüsselungsstatus sofort melden

   -   Neue WMI-Anbieter

   -   Detaillierte Protokollierung

   -   Robuste Fehlerbehandlung

   Sie können das `Invoke-MbamClientDeployment.ps1` Skript aus Microsoft.com Download [Center](https://www.microsoft.com/download/details.aspx?id=54439)herunterladen. Dies ist das Hauptskript, das Ihr Bereitstellungssystem aufruft, um die BitLocker-Laufwerkverschlüsselung zu konfigurieren und Wiederherstellungsschlüssel mit dem MBAM-Server aufzuzeichnen.

   **WMI-Bereitstellungsmethoden für MBAM:** Die folgenden WMI-Methoden wurden in MBAM 2.5 SP1 hinzugefügt, um die Aktivierung von BitLocker mithilfe des `Invoke-MbamClientDeployment.ps1` PowerShell-Skripts zu unterstützen.

   <a href="" id="mbam-machine-wmi-class"></a>**MBAM\_Machine WMI-Klasse** 
    **PrepareTpmAndEscrowOwnerAuth:** Liest die TPM OwnerAuth und sendet sie mithilfe des MBAM-Wiederherstellungsdiensts an die MBAM-Wiederherstellungsdatenbank. Wenn das TPM nicht im Besitz ist und die automatische Bereitstellung nicht aktiviert ist, generiert es einen TPM OwnerAuth und übernimmt den Besitz. Wenn ein Fehler auftritt, wird ein Fehlercode für die Problembehandlung zurückgegeben.

   **Hinweis** Für Windows 10, Version 1607 oder höher, können nur Windows den Besitz des TPM übernehmen. In addiiton behält Windows das TPM-Besitzerkennwort bei der Bereitstellung des TPM nicht bei. Weitere Details finden Sie [unter TPM-Besitzerkennwort.](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password)

| Parameter | Beschreibung |
| -------- | ----------- |
| RecoveryServiceEndPoint | Eine Zeichenfolge, die den MBAM-Wiederherstellungsdienst-Endpunkt angibt. |

Nachfolgend sehen Sie eine Liste der häufigsten Fehlermeldungen:

| Allgemeine Rückgabewerte | Fehlermeldung |
| -------------------- | ------------- |
|  **S_ok**<br />0 (0x0) | Die Methode war erfolgreich. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | TPM ist auf dem Computer nicht vorhanden oder in der BIOS-Konfiguration deaktiviert. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | TPM befindet sich nicht im richtigen Zustand (aktiviert, aktiviert und Besitzerinstallation zulässig). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM kann den Besitz von TPM nicht übernehmen, da die automatische Bereitstellung aussteht. Versuchen Sie es erneut, nachdem die automatische Bereitstellung abgeschlossen ist. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM kann den TPM-Besitzerautorisierungswert nicht lesen. Der Wert wurde möglicherweise nach einer erfolgreichen Escrow entfernt. Auf Windows 7 kann MBAM den Wert nicht lesen, wenn das TPM im Besitz anderer ist. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | Der Computer muss neu gestartet werden, um TPM auf den richtigen Zustand festzulegen. Möglicherweise müssen Sie den Computer manuell neu starten. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | Der Computer muss heruntergefahren und wieder aktiviert werden, um TPM auf den richtigen Zustand festzulegen. Möglicherweise müssen Sie den Computer manuell neu starten. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | Der Zugriff wurde vom Remoteendpunkt verweigert. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Der Remoteendpunkt ist nicht vorhanden oder konnte nicht gefunden werden. |
| **WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | Der Remoteendpunkt konnte die Anforderung nicht verarbeiten. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Der Remoteendpunkt war nicht erreichbar. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Eine Nachricht mit einem Fehler wurde vom Remoteendpunkt empfangen. Stellen Sie sicher, dass Sie eine Verbindung mit dem richtigen Dienstendpunkt herstellen. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | Die Url der Endpunktadresse ist ungültig. Die URL muss mit "http" oder "https" beginnen. |

   **ReportStatus:** Liest den Compliancestatus des Volumes und sendet ihn mithilfe des MBAM-Statusberichtsdiensts an die MBAM-Konformitätsstatusdatenbank. Der Status umfasst Verschlüsselungsstärke, Schutzart, Schutzstatus und Verschlüsselungsstatus. Wenn ein Fehler auftritt, wird ein Fehlercode für die Problembehandlung zurückgegeben.

   | Parameter | Beschreibung |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Eine Zeichenfolge, die den Endpunkt des MBAM-Statusberichtsdiensts angibt. |

   Nachfolgend sehen Sie eine Liste der häufigsten Fehlermeldungen:

   | Allgemeine Rückgabewerte | Fehlermeldung |
   | -------------------- | ------------- |
   | **S_ok**<br /> 0 (0x0) | Die Methode war erfolgreich. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | Der Zugriff wurde vom Remoteendpunkt verweigert.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Der Remoteendpunkt ist nicht vorhanden oder konnte nicht gefunden werden. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | Der Remoteendpunkt konnte die Anforderung nicht verarbeiten. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Der Remoteendpunkt war nicht erreichbar. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Eine Nachricht mit einem Fehler wurde vom Remoteendpunkt empfangen. Stellen Sie sicher, dass Sie eine Verbindung mit dem richtigen Dienstendpunkt herstellen. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | Die Url der Endpunktadresse ist ungültig. Die URL muss mit "http" oder "https" beginnen. |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM\_Volume WMI-Klasse** **EscrowRecoveryKey:** Liest das numerische Wiederherstellungskennwort und das Schlüsselpaket des Volumes und sendet sie mithilfe des MBAM-Wiederherstellungsdiensts an die MBAM-Wiederherstellungsdatenbank. Wenn ein Fehler auftritt, wird ein Fehlercode für die Problembehandlung zurückgegeben.

   | Parameter | Beschreibung |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Eine Zeichenfolge, die den MBAM-Wiederherstellungsdienst-Endpunkt angibt. |

   Nachfolgend sehen Sie eine Liste der häufigsten Fehlermeldungen:

   | Allgemeine Rückgabewerte | Fehlermeldung |
   | -------------------- | ------------- |
   | **S_ok**<br />0 (0x0) | Die Methode war erfolgreich. |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | Das Volume ist gesperrt. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | Für das Volume wurde keine numerische Kennwortschutzvorrichtung gefunden. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | Der Zugriff wurde vom Remoteendpunkt verweigert. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Der Remoteendpunkt ist nicht vorhanden oder konnte nicht gefunden werden. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | Der Remoteendpunkt konnte die Anforderung nicht verarbeiten. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Der Remoteendpunkt war nicht erreichbar. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Eine Nachricht mit einem Fehler wurde vom Remoteendpunkt empfangen. Stellen Sie sicher, dass Sie eine Verbindung mit dem richtigen Dienstendpunkt herstellen. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | Die Url der Endpunktadresse ist ungültig. Die URL muss mit "http" oder "https" beginnen. |
     

2. **Bereitstellen von MBAM mithilfe von Microsoft Deployment Toolkit (MDT) und PowerShell**

   1.  Erstellen Sie in MDT eine neue Bereitstellungsfreigabe, oder öffnen Sie eine vorhandene Bereitstellungsfreigabe.

       **Hinweis:**  
       Das `Invoke-MbamClientDeployment.ps1` PowerShell-Skript kann mit jedem Imageerstellungsprozess oder -tool verwendet werden. In diesem Abschnitt wird gezeigt, wie Sie es mit mdt integrieren, aber die Schritte ähneln der Integration in andere Prozesse oder Tools.

       **Achtung**  
       Wenn Sie die BitLocker-Vorabbereitstellung (WinPE) verwenden und den TPM-Besitzerautorisierungswert beibehalten möchten, müssen Sie das `SaveWinPETpmOwnerAuth.wsf` Skript in WinPE unmittelbar vor dem Neustart der Installation im vollständigen Betriebssystem hinzufügen. **Wenn Sie dieses Skript nicht verwenden, verlieren Sie den TPM-Besitzerautorisierungswert beim Neustart.**

   2.  In `Invoke-MbamClientDeployment.ps1` ** &lt; DeploymentShare &gt; \\Scripts**kopieren. Wenn Sie die Vorabbereitstellung verwenden, kopieren Sie die `SaveWinPETpmOwnerAuth.wsf` Datei in ** &lt; DeploymentShare &gt; \\Scripts.**

   3.  Fügen Sie die MBAM 2.5 SP1-Clientanwendung dem Knoten "Anwendungen" in der Bereitstellungsfreigabe hinzu.

       1.  Klicken Sie unter dem Knoten **"Anwendungen"** auf **"Neue Anwendung".**

       2.  Wählen Sie **Anwendung mit Quelldateien**aus. Klicken Sie auf **Weiter**.

       3.  Geben Sie unter **Anwendungsname**"MBAM 2.5 SP1 Client" ein. Klicken Sie auf **Weiter**.

       4.  Navigieren Sie zum Verzeichnis mit `MBAMClientSetup-<Version>.msi` . Klicken Sie auf **Weiter**.

       5.  Geben Sie "MBAM 2.5 SP1 Client" als das zu erstellende Verzeichnis ein. Klicken Sie auf **Weiter**.

       6.  Geben Sie `msiexec /i MBAMClientSetup-<Version>.msi /quiet` an der Befehlszeile ein. Klicken Sie auf **Weiter**.

       7.  Akzeptieren Sie die verbleibenden Standardwerte, um den Assistenten für neue Anwendungen abzuschließen.

   4.  Klicken Sie in MDT mit der rechten Maustaste auf den Namen der Bereitstellungsfreigabe, und klicken Sie auf **"Eigenschaften".** Klicken Sie auf die Registerkarte **"Regeln".** Fügen Sie die folgenden Zeilen hinzu:

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Klicken Sie auf "OK", um das Fenster zu schließen.

   5.  Bearbeiten Sie unter dem Knoten Tasksequenzen eine vorhandene Tasksequenz, die für Windows Bereitstellung verwendet wird. Wenn Sie möchten, können Sie eine neue Tasksequenz erstellen, indem Sie mit der rechten Maustaste auf den Knoten **"Tasksequenzen"** klicken, **"Neue Tasksequenz"** auswählen und den Assistenten abschließen.

       Führen Sie auf der Registerkarte **Tasksequenz** der ausgewählten Tasksequenz die folgenden Schritte aus:

       1.  Aktivieren Sie unter dem Ordner **"Vorinstallation"** die optionale Aufgabe **"BitLocker (Offline) aktivieren",** wenn BitLocker in WinPE aktiviert werden soll, wodurch nur der verwendete Speicherplatz verschlüsselt wird.

       2.  Führen Sie die folgenden Schritte aus, um TPM OwnerAuth bei Verwendung der Vorabbereitstellung beizubehalten und MBAM zu einem späteren Zeitpunkt das Ausscrown zu ermöglichen:

           1.  Suchen des **Installationsschritts für das Betriebssystem**

           2.  Hinzufügen eines neuen **Befehlszeilenschritts "Ausführen"** danach

           3.  Benennen des Schritts **"Tpm OwnerAuth beibehalten"**

           4.  Legen Sie die Befehlszeile auf `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **Hinweis fest:** Für Windows 10, Version 1607 oder höher, können nur Windows den Besitz des TPM übernehmen. In addiiton behält Windows das TPM-Besitzerkennwort bei der Bereitstellung des TPM nicht bei. Weitere Details finden Sie [unter TPM-Besitzerkennwort.](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password)

       3.  Löschen Sie im Ordner **"Zustandswiederherstellung"** die **Aufgabe "BitLocker aktivieren".**

       4.  Erstellen Sie im Ordner **"Zustandswiederherstellung"** unter **"Benutzerdefinierte Aufgaben"** eine neue **Aufgabe "Anwendung installieren",** und nennen Sie sie **"MBAM-Agent installieren".** Klicken Sie auf das Optionsfeld **"Einzelne Anwendung installieren",** und navigieren Sie zu der zuvor erstellten MBAM 2.5 SP1-Clientanwendung.

       5.  Erstellen Sie im Ordner **"Zustandswiederherstellung"** unter **"Benutzerdefinierte Aufgaben"** eine neue **PowerShell-Skriptaufgabe ausführen** (nach dem Schritt der MBAM 2.5 SP1-Clientanwendung) mit den folgenden Einstellungen (aktualisieren Sie die Parameter entsprechend Ihrer Umgebung):

           -   Name: Konfigurieren von BitLocker für MBAM

           -   PowerShell-Skript: `Invoke-MbamClientDeployment.ps1`

           -   Parameter:

               <table>
               <colgroup>
               <col width="33%" />
               <col width="33%" />
               <col width="33%" />
               </colgroup>
               <tbody>
               <tr class="odd">
               <td align="left"><p>-RecoveryServiceEndpoint</p></td>
               <td align="left"><p>Erforderlich</p></td>
               <td align="left"><p>MBAM-Wiederherstellungsdienst-Endpunkt</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>Optional</p></td>
               <td align="left"><p>Endpunkt des MBAM-Statusberichtsdiensts</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Optional</p></td>
               <td align="left"><p>Verschlüsselungsmethode (Standard: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, dass Datenvolumes und Escrow-Datenvolumes wiederherstellungsschlüssel verschlüsselt werden sollen</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, bis die Verschlüsselung abgeschlossen ist</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, dass das Bereitstellungsskript die angehaltene Verschlüsselung nicht fortsetzt</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Geben Sie an, dass der Fehler bei der TPM-Besitzerauthentifizierung ignoriert werden soll. Sie sollte in Szenarien verwendet werden, in denen MBAM die TPM-Besitzerauthentifizierung nicht lesen kann, z. B. wenn die automatische TPM-Bereitstellung aktiviert ist.</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, dass der Fehler bei der Escrow des Volumewiederherstellungsschlüssels ignoriert werden soll</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, dass Statusberichtsfehler ignoriert werden sollen</p></td>
               </tr>
               </tbody>
               </table>

                 

**So aktivieren Sie BitLocker mit MBAM 2.5 oder früher als Teil einer Windows-Bereitstellung**

1.  Installieren Sie den MBAM-Client. Anweisungen finden Sie unter ["Bereitstellen des MBAM-Clients mithilfe einer Befehlszeile".](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

2.  Verknüpfen Sie den Computer mit einer Domäne (empfohlen).

    -   Wenn der Computer keiner Domäne angehört, wird das Wiederherstellungskennwort nicht im MBAM-Schlüsselwiederherstellungsdienst gespeichert. Standardmäßig lässt MBAM keine Verschlüsselung zu, es sei denn, der Wiederherstellungsschlüssel kann gespeichert werden.

    -   Wenn ein Computer im Wiederherstellungsmodus gestartet wird, bevor der Wiederherstellungsschlüssel auf dem MBAM-Server gespeichert wird, ist keine Wiederherstellungsmethode verfügbar, und der Computer muss neu erstellt werden.

3.  Öffnen Sie eine Eingabeaufforderung als Administrator, und beenden Sie den MBAM-Dienst.

4.  Legen Sie den Dienst auf **"Manuell"** oder **"Bei Bedarf"** fest, indem Sie die folgenden Befehle eingeben:

    **net stop mbamagent**

    **sc config mbamagent start= demand**

5.  Legen Sie die Registrierungswerte so fest, dass der MBAM-Client die Gruppenrichtlinieneinstellungen ignoriert und stattdessen die Verschlüsselung so festlegt, dass die Zeit gestartet wird, zu der Windows auf diesem Clientcomputer bereitgestellt wird.

    **Achtung**  
    In diesem Schritt wird beschrieben, wie Sie die Windows-Registrierung ändern. Die falsche Verwendung des Registrierungs-Editors kann zu schwerwiegenden Problemen führen, bei denen Sie Windows neu installieren müssen. Wir können nicht garantieren, dass Probleme, die sich aus der falschen Verwendung des Registrierungs-Editors ergeben, behoben werden können. Verwenden Sie den Registrierungs-Editor auf eigenes Risiko.

    1.  Legen Sie das TPM nur für **die Betriebssystemverschlüsselung**fest, führen Sie Regedit.exe aus, und importieren Sie dann die Registrierungsschlüsselvorlage aus "C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg".

    2.  Wechseln Sie in Regedit.exe zu HKLM\\SOFTWARE\\Microsoft\\MBAM, und konfigurieren Sie die Einstellungen, die in der folgenden Tabelle aufgeführt sind.

        **Hinweis:**  
        Hier können Sie Gruppenrichtlinieneinstellungen oder Registrierungswerte für MBAM festlegen. Diese Einstellungen setzen zuvor festgelegte Werte außer Kraft.

        Konfigurationseinstellungen für Registrierungseintrag

        DeploymentTime

        0 = Aus

        1 = Richtlinieneinstellungen für die Bereitstellungszeit verwenden (Standardeinstellung) – Verwenden Sie diese Einstellung, um die Verschlüsselung zu dem Zeitpunkt zu aktivieren, Windows auf dem Clientcomputer bereitgestellt wird.

        UseKeyRecoveryService

        0 = Schlüsselescrow nicht verwenden (die nächsten beiden Registrierungseinträge sind in diesem Fall nicht erforderlich)

        1 = Schlüsselescrow im Schlüsselwiederherstellungssystem verwenden (Standard)

        Dies ist die empfohlene Einstellung, mit der MBAM die Wiederherstellungsschlüssel speichern kann. Der Computer muss in der Lage sein, mit dem MBAM-Schlüsselwiederherstellungsdienst zu kommunizieren. Stellen Sie sicher, dass der Computer mit dem Dienst kommunizieren kann, bevor Sie fortfahren.

        KeyRecoveryOptions

        0 = Nur Wiederherstellungsschlüssel hochladen

        1 = Lädt Wiederherstellungsschlüssel und Schlüsselwiederherstellungspaket hoch (Standard)

        KeyRecoveryServiceEndPoint

        Legen Sie diesen Wert auf die URL für den Server fest, auf dem der Schlüsselwiederherstellungsdienst ausgeführt wird, z. B. http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.


6.  Der MBAM-Client startet das System während der MBAM-Clientbereitstellung neu. Wenn Sie für diesen Neustart bereit sind, führen Sie den folgenden Befehl an einer Eingabeaufforderung als Administrator aus:

    **net start mbamagent**

7.  Wenn die Computer neu gestartet werden und sie vom BIOS aufgefordert werden, akzeptieren Sie die TPM-Änderung.

8.  Wenn Sie bereit sind, die Verschlüsselung zu starten, öffnen Sie während der Windows Clientbetriebssystem-Imageerstellung eine Eingabeaufforderung als Administrator, und geben Sie die folgenden Befehle ein, um den Start auf **"Automatisch"** festzulegen und den MBAM-Client-Agent neu zu starten:

    **sc config mbamagent start= auto**

    **net start mbamagent**

9.  Um die Registrierungswerte für die Umgehung zu löschen, führen Sie Regedit.exe aus, und wechseln Sie zum Registrierungseintrag "HKLM\\SOFTWARE\\Microsoft". Klicken Sie mit der rechten Maustaste auf den **MBAM-Knoten,** und klicken Sie dann auf **"Löschen".**

## <a name="related-topics"></a>Verwandte Themen

[Bereitstellen des MBAM 2.5-Clients](deploying-the-mbam-25-client.md)

[Planen der Clientbereitstellung für MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## <a name="got-a-suggestion-for-mbam"></a>Haben Sie einen Vorschlag für MBAM?
- Hier können Sie [Vorschläge](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)hinzufügen oder abstimmen.
- Verwenden Sie für MBAM-Probleme das [MBAM TechNet-Forum.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)
