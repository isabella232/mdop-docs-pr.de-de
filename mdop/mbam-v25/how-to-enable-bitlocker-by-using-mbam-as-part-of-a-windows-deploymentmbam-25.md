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
ms.openlocfilehash: 4b2cbf333c705088d0a068521fb65e99551bb1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811629"
---
# So aktivieren Sie BitLocker im Rahmen einer Windows-Bereitstellung mithilfe von MBAM


In diesem Thema wird erläutert, wie Sie BitLocker auf dem Computer eines Endbenutzers mithilfe von MBAM als Teil des Windows-Imaging-und Bereitstellungsprozesses aktivieren. Wenn beim Neustart (nach Abschluss der Installationsphase) ein schwarzer Bildschirm angezeigt wird, der besagt, dass das Laufwerk nicht entsperrt werden kann, lesen Sie [frühere Windows-Versionen werden nicht nach dem Schritt "Setup Windows und Configuration Manager" gestartet, wenn BitLocker mit Windows 10, Version 1511, verwendet wird](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo).

**Voraussetzungen:**

-   Ein vorhandener Windows-Abbild Bereitstellungsprozess – Microsoft Deployment Toolkit (MDT), Microsoft System Center Configuration Manager oder ein anderes Imaging-Tool oder-Verfahren – muss vorhanden sein.

-   TPM muss im BIOS aktiviert und für das Betriebssystem sichtbar sein.

-   MBAM-Serverinfrastruktur muss vorhanden und barrierefrei sein

-   Die von BitLocker erforderliche Systempartition muss erstellt werden.

-   Der Computer muss während der Bildgebung einer Domäne beigetreten sein, bevor MBAM BitLocker vollständig aktiviert.

**So aktivieren Sie BitLocker mithilfe von MBAM 2,5 SP1 als Teil einer Windows-Bereitstellung**

1. In MBAM 2,5 SP1 verwenden Sie das PowerShell-Skript als empfohlene Vorgehensweise zum Aktivieren von BitLocker während einer Windows-Bereitstellung `Invoke-MbamClientDeployment.ps1` .

   -   Das `Invoke-MbamClientDeployment.ps1` Skript ergreift BitLocker während des Imaging-Prozesses. Wenn Sie von der BitLocker-Richtlinie benötigt wird, fordert der MBAM-Agent sofort den Domänenbenutzer auf, eine PIN oder ein Kennwort zu erstellen, wenn sich der Domänenbenutzer zuerst nach der Bildbearbeitung anmeldet.

   -   Einfache Verwendung mit MDT, System Center Configuration Manager oder eigenständigen Imaging-Prozessen

   -   Kompatibel mit PowerShell 2,0 oder höher

   -   Verschlüsseln des BS-Volumes mit TPM-Schlüsselschutz

   -   Vollständige Unterstützung der BitLocker-Vorabbereitstellung

   -   Optionales Verschlüsseln von FDDs

   -   Escrow-TPM-OwnerAuth für Windows 7 muss MBAM das TPM besitzen, damit Escrow ausgeführt werden kann.
   Für Windows 8,1, Windows 10 RTM und Windows 10, Version 1511, wird der Treuhandservice für TPM-OwnerAuth unterstützt.
   Für Windows 10, Version 1607 oder höher, kann nur Windows den Besitz des TPM übernehmen. In addiiton wird Windows das TPM-Besitzerkennwort beim Bereitstellen des TPMs nicht beibehalten. Weitere Informationen finden Sie unter [TPM-Besitzerkennwort](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

   -   Escrow-Wiederherstellungsschlüssel und Wiederherstellungsschlüssel Pakete

   -   Sofortiges melden des Verschlüsselungsstatus

   -   Neue WMI-Anbieter

   -   Detaillierte Protokollierung

   -   Robuste Fehlerbehandlung

   Sie können das `Invoke-MbamClientDeployment.ps1` Skript im [Microsoft.com-Download Center](https://www.microsoft.com/download/details.aspx?id=54439)herunterladen. Dies ist das Hauptskript, das vom Bereitstellungssystem aufgerufen wird, um die BitLocker-Laufwerkverschlüsselung zu konfigurieren und Wiederherstellungsschlüssel mit dem MBAM-Server aufzuzeichnen.

   **WMI-Bereitstellungsmethoden für MBAM:** Die folgenden WMI-Methoden wurden in MBAM 2,5 SP1 hinzugefügt, um die Aktivierung von BitLocker mithilfe des `Invoke-MbamClientDeployment.ps1` PowerShell-Skripts zu unterstützen.

   <a href="" id="mbam-machine-wmi-class"></a>**MBAM \ _Machine WMI-Klasse** 
    **PrepareTpmAndEscrowOwnerAuth:** Liest die TPM-OwnerAuth und sendet Sie mithilfe des MBAM-Wiederherstellungs Diensts an die MBAM-Wiederherstellungsdatenbank. Wenn das TPM nicht im Besitz ist und die automatische Bereitstellung nicht aktiviert ist, wird ein TPM-OwnerAuth generiert und der Besitz übernommen. Wenn dies nicht der Fall ist, wird ein Fehlercode zur Problembehandlung zurückgegeben.

   **Hinweis** Für Windows 10, Version 1607 oder höher, kann nur Windows den Besitz des TPM übernehmen. In addiiton wird Windows das TPM-Besitzerkennwort beim Bereitstellen des TPMs nicht beibehalten. Weitere Informationen finden Sie unter [TPM-Besitzerkennwort](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

| Parameter | Beschreibung |
| -------- | ----------- |
| RecoveryServiceEndPoint | Eine Zeichenfolge, die den MBAM-Wiederherstellungs Dienstendpunkt angibt. |

Nachfolgend finden Sie eine Liste häufig auftretender Fehlermeldungen:

| Allgemeine Rückgabewerte | Fehlermeldung |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0x0) | Die Methode war erfolgreich. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | TPM ist auf dem Computer nicht vorhanden oder in der BIOS-Konfiguration deaktiviert. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | TPM befindet sich nicht im richtigen Zustand (aktiviert, aktiviert und die Besitzer Installation ist zulässig). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM kann den Besitz von TPM nicht übernehmen, da die automatische Bereitstellung aussteht. Versuchen Sie es erneut, nachdem die automatische Bereitstellung abgeschlossen ist. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM kann den TPM-Besitzerautorisierungswert nicht lesen. Der Wert wurde möglicherweise nach einem erfolgreichen Escrow entfernt. Unter Windows 7 kann MBAM den Wert nicht lesen, wenn das TPM im Besitz anderer Personen ist. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | Der Computer muss neu gestartet werden, um TPM auf den richtigen Zustand festzulegen. Möglicherweise müssen Sie den Computer manuell neu starten. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | Der Computer muss heruntergefahren und wieder aktiviert werden, um TPM auf den richtigen Zustand festzulegen. Möglicherweise müssen Sie den Computer manuell neu starten. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | Der Remoteendpunkt hat Zugriff verweigert. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Der Remoteendpunkt ist nicht vorhanden oder konnte nicht gefunden werden. |
| * * WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | Der Remoteendpunkt konnte die Anforderung nicht verarbeiten. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Der Remoteendpunkt war nicht erreichbar. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Eine Nachricht mit einem Fehler wurde vom Remoteendpunkt empfangen. Stellen Sie sicher, dass Sie mit dem richtigen Dienstendpunkt verbunden sind. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | Die Endpunktadressen-URL ist ungültig. Die URL muss mit "http" oder "https" beginnen. |

   **Report Status:** Liest den Kompatibilitätsstatus des Volumes und sendet ihn mithilfe des MBAM-Statusberichts Diensts an die MBAM-Konformitätsstatus-Datenbank. Der Status umfasst Verschlüsselungsstärke, Protector-Typ, Protector-Zustand und Verschlüsselungsstatus. Wenn dies nicht der Fall ist, wird ein Fehlercode zur Problembehandlung zurückgegeben.

   | Parameter | Beschreibung |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Eine Zeichenfolge, die den MBAM-Status Berichterstattungsdienst Endpunkt angibt. |

   Nachfolgend finden Sie eine Liste häufig auftretender Fehlermeldungen:

   | Allgemeine Rückgabewerte | Fehlermeldung |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0x0) | Die Methode war erfolgreich. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | Der Remoteendpunkt hat Zugriff verweigert.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Der Remoteendpunkt ist nicht vorhanden oder konnte nicht gefunden werden. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | Der Remoteendpunkt konnte die Anforderung nicht verarbeiten. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Der Remoteendpunkt war nicht erreichbar. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Eine Nachricht mit einem Fehler wurde vom Remoteendpunkt empfangen. Stellen Sie sicher, dass Sie mit dem richtigen Dienstendpunkt verbunden sind. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | Die Endpunktadressen-URL ist ungültig. Die URL muss mit "http" oder "https" beginnen. |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM \ _Volume WMI class** **EscrowRecoveryKey:** liest das numerische Wiederherstellungskennwort und das Schlüsselpaket des Volumes und sendet Sie mithilfe des MBAM-Wiederherstellungs Diensts an die MBAM-Wiederherstellungsdatenbank. Wenn dies nicht der Fall ist, wird ein Fehlercode zur Problembehandlung zurückgegeben.

   | Parameter | Beschreibung |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Eine Zeichenfolge, die den MBAM-Wiederherstellungs Dienstendpunkt angibt. |

   Nachfolgend finden Sie eine Liste häufig auftretender Fehlermeldungen:

   | Allgemeine Rückgabewerte | Fehlermeldung |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0x0) | Die Methode war erfolgreich. |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | Die Lautstärke ist gesperrt. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | Für das Volume wurde kein numerischer Kennwortschutz gefunden. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | Der Remoteendpunkt hat Zugriff verweigert. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Der Remoteendpunkt ist nicht vorhanden oder konnte nicht gefunden werden. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | Der Remoteendpunkt konnte die Anforderung nicht verarbeiten. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Der Remoteendpunkt war nicht erreichbar. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Eine Nachricht mit einem Fehler wurde vom Remoteendpunkt empfangen. Stellen Sie sicher, dass Sie mit dem richtigen Dienstendpunkt verbunden sind. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | Die Endpunktadressen-URL ist ungültig. Die URL muss mit "http" oder "https" beginnen. |
     

2. **Bereitstellen von MBAM mithilfe von Microsoft Deployment Toolkit (MDT) und PowerShell**

   1.  Erstellen Sie in MDT eine neue Bereitstellungsfreigabe, oder öffnen Sie eine vorhandene Bereitstellungsfreigabe.

       **Hinweis:**  
       Das `Invoke-MbamClientDeployment.ps1` PowerShell-Skript kann mit jedem imagingprozess oder Tool verwendet werden. In diesem Abschnitt wird gezeigt, wie Sie mithilfe von MDT integriert werden, doch die Schritte ähneln der Integration in andere Prozesse oder Tools.

       **Achtung**  
       Wenn Sie BitLocker (Pre-Provisioning, WinPE) verwenden und den TPM-Besitzerautorisierungswert beibehalten möchten, müssen Sie das `SaveWinPETpmOwnerAuth.wsf` Skript in WinPE unmittelbar vor dem Neustart der Installation in das vollständige Betriebssystem hinzufügen. **Wenn Sie dieses Skript nicht verwenden, gehen beim Neustart der TPM-Besitzerautorisierungswert verloren.**

   2.  Kopieren `Invoke-MbamClientDeployment.ps1` Sie den ** &lt; DeploymentShare- &gt; \\Scripts**. Wenn Sie die Vorabbereitstellung verwenden, kopieren Sie die `SaveWinPETpmOwnerAuth.wsf` Datei in ** &lt; DeploymentShare &gt; \\Scripts**.

   3.  Fügen Sie die MBAM 2,5 SP1-Clientanwendung dem Applications-Knoten in der Bereitstellungsfreigabe hinzu.

       1.  Klicken Sie unter dem Knoten **Anwendungen** auf **neue Anwendung**.

       2.  Wählen Sie **Anwendung mit Quelldateien**aus. Klicken Sie auf **Weiter**.

       3.  Geben Sie unter **Anwendungs Name den Namen**"MBAM 2,5 SP1-Client" ein. Klicken Sie auf **Weiter**.

       4.  Navigieren Sie zu dem Verzeichnis, in dem sich die `MBAMClientSetup-<Version>.msi` . Klicken Sie auf **Weiter**.

       5.  Geben Sie "MBAM 2,5 SP1-Client" als zu Erstell Verzeichnis ein. Klicken Sie auf **Weiter**.

       6.  Geben Sie `msiexec /i MBAMClientSetup-<Version>.msi /quiet` in der Befehlszeile ein. Klicken Sie auf **Weiter**.

       7.  Übernehmen Sie die verbleibenden Standardeinstellungen, um den Assistenten für neue Anwendungen abzuschließen.

   4.  Klicken Sie in MDT mit der rechten Maustaste auf den Namen der Bereitstellungsfreigabe, und klicken Sie auf **Eigenschaften**. Klicken Sie auf die Registerkarte **Regeln** . Fügen Sie die folgenden Zeilen hinzu:

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Klicken Sie auf OK, um das Fenster zu schließen.

   5.  Bearbeiten Sie unter dem Knoten Tasksequenzen eine vorhandene Tasksequenz, die für die Windows-Bereitstellung verwendet wird. Wenn Sie möchten, können Sie eine neue Tasksequenz erstellen, indem Sie mit der rechten Maustaste auf den Knoten **Tasksequenzen** klicken, **neue Tasksequenz**auswählen und den Assistenten abschließen.

       Führen Sie auf der Registerkarte **Tasksequenz** der ausgewählten Tasksequenz die folgenden Schritte aus:

       1.  Aktivieren Sie im Ordner **Vorinstallation** den optionalen Task **BitLocker aktivieren (offline)** , wenn BitLocker in WinPE aktiviert werden soll, wodurch nur der verwendete Speicherplatz verschlüsselt wird.

       2.  Gehen Sie wie folgt vor, um die TPM-OwnerAuth bei Verwendung der Vorabbereitstellung zu speichern und MBAM zu einem späteren Zeitpunkt zu übernehmen:

           1.  Suchen des Schritts zum **Installieren des Betriebssystems**

           2.  Hinzufügen eines neuen **Befehlszeilenbefehls Zeile** nach dem Ausführen

           3.  Benennen des Schritts **Persist TPM OwnerAuth**

           4.  Legen Sie die Befehlszeile fest `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **:** für Windows 10, Version 1607 oder höher, kann nur Windows den Besitz des TPM übernehmen. In addiiton wird Windows das TPM-Besitzerkennwort beim Bereitstellen des TPMs nicht beibehalten. Weitere Informationen finden Sie unter [TPM-Besitzerkennwort](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

       3.  Löschen Sie im Ordner **Zustands Wiederherstellung** die Aufgabe **BitLocker aktivieren** .

       4.  Erstellen Sie im Ordner **Zustands Wiederherstellung** unter **benutzerdefinierte Aufgaben**eine neue Aufgabe für die **Installationsanwendung** , und nennen Sie Sie **MBAM-Agent installieren**. Klicken Sie auf das Optionsfeld **einzelne Anwendung installieren** , und navigieren Sie zu der zuvor erstellten MBAM 2,5 SP1-Clientanwendung.

       5.  Erstellen Sie im Ordner **Zustands Wiederherstellung** unter **benutzerdefinierte Aufgaben**einen neuen **PowerShell-Skripttask ausführen** (nach dem MBAM 2,5 SP1-Client anwendungsschritt) mit den folgenden Einstellungen (aktualisieren Sie die Parameter entsprechend Ihrer Umgebung):

           -   Name: Konfigurieren von BitLocker für MBAM

           -   PowerShell-Skript: `Invoke-MbamClientDeployment.ps1`

           -   Parameter

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
               <td align="left"><p>MBAM-Wiederherstellungs Dienstendpunkt</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>Optional</p></td>
               <td align="left"><p>MBAM-Status Berichterstattungsdienst Endpunkt</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Optional</p></td>
               <td align="left"><p>Verschlüsselungsmethode (Standard: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, dass Datenvolumen und Escrow-Datenvolumen-Wiederherstellungsschlüssel (s) verschlüsselt werden sollen</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, dass die Verschlüsselung abgewartet werden soll</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, dass das Bereitstellungsskript die angehaltene Verschlüsselung nicht fortsetzen wird</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Geben Sie an, dass der TPM-Besitzer-AUTH-Fehler ignoriert werden soll. Sie sollte in den Szenarien verwendet werden, in denen MBAM nicht in der Lage ist, die TPM-Besitzer Authentifizierung zu lesen, beispielsweise wenn die automatische TPM-Bereitstellung aktiviert ist.</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, dass der Datenträger Wiederherstellungsschlüssel-Fehler ignoriert werden soll</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Schalter</p></td>
               <td align="left"><p>Angeben, dass Fehler bei der Statusmeldung ignoriert werden</p></td>
               </tr>
               </tbody>
               </table>

                 

**So aktivieren Sie BitLocker mithilfe von MBAM 2,5 oder früher als Teil einer Windows-Bereitstellung**

1.  Installieren Sie den MBAM-Client. Anweisungen hierzu finden Sie unter [Bereitstellen des MBAM-Clients mithilfe einer Befehlszeile](how-to-deploy-the-mbam-client-by-using-a-command-line.md).

2.  Verbinden Sie den Computer mit einer Domäne (empfohlen).

    -   Wenn der Computer nicht zu einer Domäne gehört, wird das Wiederherstellungskennwort nicht im MBAM-Schlüssel Wiederherstellungs Dienst gespeichert. Standardmäßig lässt MBAM keine Verschlüsselung zu, es sei denn, der Wiederherstellungsschlüssel kann gespeichert werden.

    -   Wenn ein Computer im Wiederherstellungsmodus gestartet wird, bevor der Wiederherstellungsschlüssel auf dem MBAM-Server gespeichert wird, steht keine Wiederherstellungsmethode zur Verfügung, und der Computer muss wiederhergestellt werden.

3.  Öffnen Sie eine Eingabeaufforderung als Administrator, und beenden Sie den MBAM-Dienst.

4.  Stellen Sie den Dienst auf **manuell** oder **bei Bedarf** ein, indem Sie die folgenden Befehle eingeben:

    **NET STOP mbamagent**

    **SC config mbamagent Start = Demand**

5.  Legen Sie die Registrierungswerte so fest, dass der MBAM-Client die Gruppenrichtlinieneinstellungen ignoriert, und legt stattdessen die Verschlüsselung fest, um die Zeit zu starten, die Windows auf diesem Clientcomputer bereitgestellt wird.

    **Vorsicht**  In diesem Schritt wird beschrieben, wie die Windows-Registrierung geändert wird. Das falsche Verwenden des Registrierungs-Editors kann zu schwerwiegenden Problemen führen, bei denen eine Neuinstallation von Windows erforderlich ist. Wir können nicht garantieren, dass Probleme, die sich aus der fehlerhaften Verwendung des Registrierungs-Editors ergeben, behoben werden können. Verwenden Sie den Registrierungs-Editor auf eigenes Risiko.

    1.  Setzen Sie das TPM **nur für das Betriebssystem Verschlüsselung**, führen Sie Regedit.exe aus, und importieren Sie dann die Registrierungsschlüssel Vorlage aus c:\\Programme Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

    2.  Wechseln Sie in Regedit.exe zu HKLM\\SOFTWARE\\Microsoft\\MBAM, und konfigurieren Sie die Einstellungen, die in der folgenden Tabelle aufgeführt sind.

        **Hinweis**  Hier können Sie Gruppenrichtlinieneinstellungen oder Registrierungswerte in Bezug auf MBAM festlegen. Diese Einstellungen überschreiben zuvor eingestellte Werte.

        Konfigurationseinstellungen für Registrierungseinträge

        Bereitstellung

        0 = aus

        1 = Verwenden von Bereitstellungszeit Richtlinieneinstellungen (Standard) – verwenden Sie diese Einstellung, um die Verschlüsselung zu dem Zeitpunkt zu aktivieren, zu dem Windows auf dem Clientcomputer bereitgestellt wird.

        UseKeyRecoveryService

        0 = Schlüssel Escrow nicht verwenden (die nächsten beiden Registrierungseinträge sind in diesem Fall nicht erforderlich)

        1 = Verwenden des Schlüssels Escrow in Key Recovery System (Standard)

        Dies ist die empfohlene Einstellung, die es MBAM ermöglicht, die Wiederherstellungsschlüssel zu speichern. Der Computer muss in der Lage sein, mit dem MBAM-Schlüssel Wiederherstellungs Dienst zu kommunizieren. Vergewissern Sie sich, dass der Computer mit dem Dienst kommunizieren kann, bevor Sie fortfahren.

        Keyrecoveryoptions

        0 = nur Uploads des Wiederherstellungsschlüssels

        1 = Uploads-Wiederherstellungsschlüssel und Schlüssel Wiederherstellungs Paket (Standard)

        KeyRecoveryServiceEndPoint

        Setzen Sie diesen Wert auf die URL für den Server, auf dem der Schlüssel Wiederherstellungs Dienst ausgeführt wird, beispielsweise http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.


6.  Der MBAM-Client startet das System während der MBAM-Clientbereitstellung neu. Wenn Sie für diesen Neustart bereit sind, führen Sie den folgenden Befehl an einer Eingabeaufforderung als Administrator aus:

    **NET Start mbamagent**

7.  Wenn die Computer neu gestartet werden und das BIOS Sie auffordert, übernehmen Sie die TPM-Änderung.

8.  Öffnen Sie während des Windows-Client-Betriebssystem-Imaging-Prozesses, wenn Sie bereit sind, die Verschlüsselung zu starten, eine Eingabeaufforderung als Administrator, und geben Sie die folgenden Befehle ein, um den Start auf **Automatic** zu setzen und den MBAM-Client-Agent erneut zu starten:

    **SC config mbamagent Start = automatisch**

    **NET Start mbamagent**

9.  Wenn Sie die Umgehungs Registrierungswerte löschen möchten, führen Sie Regedit.exe aus, und wechseln Sie zum Registrierungseintrag HKLM\\SOFTWARE\\Microsoft. Klicken Sie mit der rechten Maustaste auf den **MBAM** -Knoten, und klicken Sie dann auf **Löschen**.

## Verwandte Themen

[Bereitstellen des MBAM 2.5-Clients](deploying-the-mbam-25-client.md)

[Planen der Clientbereitstellung für MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
