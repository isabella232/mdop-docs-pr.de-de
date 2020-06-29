---
title: Infos zu MBAM 2.0 SP1
description: Infos zu MBAM 2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810024"
---
# Infos zu MBAM 2.0 SP1

In diesem Thema werden die Änderungen in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 Service Pack 1 (SP1) beschrieben. Eine allgemeine Beschreibung von MBAM finden Sie unter [Erste Schritte mit MBAM 2,0](getting-started-with-mbam-20-mbam-2.md).

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a>Neuerungen in MBAM 2,0 SP1

Diese Version von MBAM bietet die folgenden neuen Features und Funktionen.

### Unterstützung für Windows 8,1, Windows Server 2012 R2 und System Center 2012 R2-Konfigurations-Manager

Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 Service Pack 1 (SP1) bietet Unterstützung für Windows 8,1, Windows Server 2012 R2 und System Center 2012 R2-Konfigurations-Manager.

### Unterstützung für Microsoft SQL Server 2008 R2 SP2

Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 Service Pack 1 (SP1) fügt Unterstützung für Microsoft SQL Server 2008 R2 SP2 hinzu. Sie müssen Microsoft SQL Server 2008 R2 oder höher verwenden, wenn Sie Microsoft System Center Configuration Manager 2007 R2 ausführen.

### Kundenfeedback-Rollup

MBAM 2,0 SP1 enthält ein Rollup mit Korrekturen zur Behebung von Problemen, die seit der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0-Version gefunden wurden. Im Rahmen dieser Änderungen wird das Feld Computer Name nun in den Berichten BitLocker Computer Compliance und BitLocker Enterprise Compliance Details angezeigt, wenn Sie MBAM mit Microsoft System Center Configuration Manager 2007 ausführen.

### Firewall-Ausnahme muss für Ports für das Self-Service-Portal und die Website "Verwaltung und Überwachung" eingerichtet werden.

Wenn Sie das Self-Service-Portal und die Verwaltungs-und Überwachungs Website konfigurieren, müssen Sie eine Firewall-Ausnahme festlegen, um die Kommunikation über die angegebenen Ports zu ermöglichen. Zuvor hat die MBAM-Server Installation die Ports automatisch in der Windows-Firewall geöffnet.

### Speicherort von MBAM-Berichten in Configuration Manager geändert

MBAM-Berichte für die integrierte Configuration Manager-Topologie sind jetzt unter Unterordner innerhalb des MBAM-Knotens verfügbar. Die Namen der Unterordner stellen die Sprache der Berichte innerhalb des Unterordners dar.

### Möglichkeit zum Installieren von MBAM auf einem primären Standortserver bei der Installation von MBAM mit Configuration Manager

Sie können MBAM auf einem primären Standortserver oder einem Website Server für die Zentraladministration installieren, wenn Sie MBAM mit der integrierten Configuration Manager-Topologie installieren. Zuvor mussten Sie MBAM auf einem Website Server der Zentraladministration installieren.

**Wichtig**  
Der Server, auf dem Sie MBAM installieren, muss der oberste Ebene Server in Ihrer Hierarchie sein.



Die MBAM-Installation funktioniert unterschiedlich für Microsoft System Center Configuration Manager 2007 und Microsoft System Center 2012 Configuration Manager wie folgt:

-   **Configuration Manager 2007** : Wenn Sie MBAM auf einem primären Standortserver installieren, der Teil einer größeren Configuration Manager-Hierarchie ist und über einen zentralen Standort übergeordneten Server verfügt, löst MBAM den übergeordneten zentralen Standortserver auf und führt alle Installationsaktionen auf dem übergeordneten Server aus. Zu den Installationsaktionen gehören das Überprüfen von Voraussetzungen und das Installieren der Configuration Manager-Objekte und-Berichte. Wenn Sie beispielsweise MBAM auf einem primären Standortserver installieren, der ein untergeordnetes Element eines übergeordneten zentralen Standortservers ist, installiert MBAM alle Configuration Manager-Objekte und-Berichte auf dem übergeordneten Server. Wenn Sie MBAM auf dem übergeordneten Server installieren, führt MBAM alle Installationsaktionen auf dem übergeordneten Server aus.

-   **System Center 2012-Konfigurations-Manager** : Wenn Sie MBAM auf einem primären Standortserver oder auf einem zentralen Administrationsserver installieren, führt MBAM alle Installationsaktionen auf diesem Website Server aus.

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> Die Configuration Manager-Konsole muss auf dem Computer installiert sein, auf dem Sie den MBAM-Server installieren.

Wenn Sie MBAM mit der integrierten Configuration Manager-Topologie installieren, müssen Sie die Configuration Manager-Konsole auf dem Computer installieren, auf dem MBAM installiert wird. Wenn Sie die empfohlene Architektur verwenden, die unter [Erste Schritte – verwenden von MBAM mit Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)beschrieben wird, würden Sie MBAM auf dem primären Configuration Manager-Standort Server installieren.

### Neue Setup-Befehlszeilenparameter für die integrierte Configuration Manager-Topologie

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Befehlszeilen Parameter</th>
<th align="left">Beschreibung</th>
<th align="left">Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CM_SSRS_REMOTE_SERVER_NAME</p></td>
<td align="left"><p>Ermöglicht es Ihnen, die Configuration Manager-Berichte auf einem Remoteserver für SQL Server Reporting Services (SSRS) zu installieren, der Teil desselben Configuration Manager-Standorts ist, auf dem MBAM installiert ist. Sie können den Wert auf den vollqualifizierten Domänennamen des Remote-SSRS-Punkt Rollen Servers einstellen.</p></td>
<td align="left"><p>MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</p></td>
</tr>
<tr class="even">
<td align="left"><p>CM_REPORTS_ONLY</p></td>
<td align="left"><p>Ermöglicht es Ihnen, nur die Configuration Manager-Berichte zu installieren, ohne andere Configuration Manager-Objekte wie die Basisplan-, Sammlungs-und Konfigurationselemente.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Sie müssen diesen Parameter mit dem CM_REPORTS_COLLECTION_ID-Parameter kombinieren.</p>
</div>
<div>

</div>
<p>Gültige Parameterwerte:</p>
<ul>
<li><p>Wahr</p></li>
<li><p>False</p></li>
</ul>
<p>Sie können diesen Parameter mit dem CM_SSRS_REMOTE_SERVER_NAME-Parameter kombinieren, wenn Sie die Berichte nur auf einem Remote-SSRS-Punkt Rollen Server installieren möchten.</p>
<p>Wenn Sie den Parameter nicht festlegen oder auf "false" festlegen, installiert MBAM Setup alle Configuration Manager-Objekte, einschließlich der Berichte.</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CM_REPORTS_COLLECTION_ID</p></td>
<td align="left"><p>Eine vorhandene Sammlungs-ID, die die Sammlung identifiziert, für die Berichterstattungs Kompatibilitätsdaten angezeigt werden. Sie können eine beliebige Sammlungs-ID angeben. Sie müssen die Sammlungs-ID "MBAM-unterstützte Computer" nicht verwenden.</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
</tbody>
</table>



### Möglichkeit zum Aktivieren oder Deaktivieren des Self-Service-Portal-Notiztexts

Mit MBAM 2,0 SP1 können Sie den Hinweistext im Self-Service-Portal deaktivieren. Zuvor wurde der Hinweistext standardmäßig angezeigt, und Sie können ihn nicht deaktivieren.

**So deaktivieren Sie den Hinweistext**

1.  Öffnen Sie auf dem Server, auf dem Sie das Self-Service-Portal installiert haben, Internet Informationsdienste (IIS), und navigieren Sie zu **Websites &gt; Microsoft BitLocker-Verwaltungs-und Überwachungs &gt; Selfservice- &gt; Anwendungseinstellungen**.

2.  Wählen Sie in der Spalte **Name** die Option **DisplayNotice**aus, und legen Sie den Wert auf **false**fest.

### Möglichkeit zum Lokalisieren der HelpdeskText-Anweisung, die Benutzer auf mehr Self-Service-Portal Informationen verweist

Sie können eine lokalisierte Version der Self-Service-Portal-Anweisung "HelpdeskText" konfigurieren, in der Endbenutzer erfahren, wie Sie bei Verwendung des Self-Service-Portals weitere Hilfe erhalten. Wenn Sie lokalisierten Text für die Anweisung konfigurieren, wie in den folgenden Anleitungen beschrieben, wird in MBAM die lokalisierte Version angezeigt. Wenn MBAM die lokalisierte Version nicht findet, wird der Wert im **HelpdeskText** -Parameter angezeigt.

**So zeigen Sie eine lokalisierte Version der HelpdeskText-Anweisung an**

1.  Öffnen Sie auf dem Server, auf dem Sie das Self-Service-Portal installiert haben, IIS, und navigieren Sie zu **Websites &gt; Microsoft BitLocker-Verwaltungs-und Überwachungs &gt; Selfservice- &gt; Anwendungseinstellungen**.

2.  Klicken Sie im Bereich **Aktionen** auf **Hinzufügen** , um das Dialogfeld **Anwendungseinstellung hinzufügen** zu öffnen.

3.  Geben Sie im Feld **Name den Namen** **HelpdeskText**\ _ &lt; *Language*ein &gt; , wobei &lt; *Sprache* &gt; der für den Text geeignete Sprachcode ist. Wenn Sie beispielsweise eine lokalisierte HelpdeskText-Anweisung in Spanisch erstellen möchten, benennen Sie den Parameter HelpdeskText \ _ES-es. Eine Liste der gültigen Sprachcodes, die Sie verwenden können, finden Sie unter [National Language Support (NLS)-API-Referenz](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Geben Sie im Feld **Wert** den lokalisierten Text ein, der Endbenutzern angezeigt werden soll.

### Möglichkeit zum Lokalisieren des Self-Service-Portals HelpdeskURL

Sie können eine lokalisierte Version des Self-Service-Portals HelpdeskURL konfigurieren, damit die Endbenutzer standardmäßig angezeigt werden. Wenn Sie eine lokalisierte Version erstellen, wie in den folgenden Anleitungen beschrieben, findet MBAM die lokalisierte Version und zeigt Sie an. Wenn MBAM keine lokalisierte Version findet, wird die für den HelpDeskURL-Parameter konfigurierte URL angezeigt.

**So zeigen Sie einen lokalisierten HelpdeskURL an**

1.  Öffnen Sie auf dem Server, auf dem Sie das Self-Service-Portal installiert haben, IIS, und navigieren Sie zu **Websites &gt; Microsoft BitLocker-Verwaltungs-und Überwachungs &gt; Selfservice- &gt; Anwendungseinstellungen**.

2.  Klicken Sie im Bereich **Aktionen** auf **Hinzufügen** , um das Dialogfeld **Anwendungseinstellung hinzufügen** zu öffnen.

3.  Geben Sie im Feld **Name den Namen** **HelpdeskURL**\ _ &lt; *Language*ein &gt; , wobei &lt; *Sprache* &gt; der geeignete Sprachcode für die URL ist. Wenn Sie beispielsweise einen lokalisierten HelpdeskURL in Spanisch erstellen möchten, benennen Sie den Parameter HelpdeskURL \ _ES-es. Eine Liste der gültigen Sprachcodes, die Sie verwenden können, finden Sie unter [National Language Support (NLS)-API-Referenz](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Geben Sie im Feld **Wert** den lokalisierten HelpdeskURL ein, der den Endbenutzern angezeigt werden soll.

### Möglichkeit zum Lokalisieren des Self-Service-Portal-Notiztexts

Sie können lokalisierten Benachrichtigungstext so konfigurieren, dass er für Endbenutzer standardmäßig im Self-Service-Portal angezeigt wird. Die notice.txt-Datei, die den Hinweistext anzeigt, befindet sich im folgenden Stammverzeichnis:

&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\

Wenn Sie lokalisierten Hinweistext anzeigen möchten, erstellen Sie eine lokalisierte notice.txt Datei, und speichern Sie Sie unter einem bestimmten Sprachordner im folgenden Verzeichnis:

&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\

MBAM zeigt den Hinweistext auf der Grundlage der folgenden Regeln an:

-   Wenn Sie eine lokalisierte notice.txt Datei im entsprechenden Sprachordner erstellen, zeigt MBAM den lokalisierten Hinweistext an.

-   Wenn MBAM keine lokalisierte Version der notice.txt-Datei findet, wird der Text in der standardmäßigen notice.txt Datei angezeigt.

-   Wenn MBAM keine Standard notice.txt Datei findet, wird der Standardtext im Self-Service-Portal angezeigt.

**Hinweis:**  
Wenn der Browser eines Endbenutzers auf eine Sprache festgesetzt ist, die keinen entsprechenden Unterordner "Sprache" oder notice.txt hat, wird der Text in der notice.txt Datei im folgenden Stammverzeichnis angezeigt:

&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\



**So erstellen Sie eine lokalisierte notice.txt-Datei**

1.  Erstellen Sie auf dem Server, auf dem Sie das Self-Service-Portal installiert haben, einen &lt; *sprach* &gt; Ordner im folgenden Verzeichnis, wobei &lt; *Sprache* &gt; den Namen der lokalisierten Sprache darstellt:

    &lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\

    **Hinweis:**  
    Da einige Sprachordner bereits vorhanden sind, müssen Sie möglicherweise keine erstellen. Wenn Sie einen Sprachordner erstellen müssen, finden Sie unter [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) eine Liste der gültigen Namen, die Sie für den &lt; *sprach* &gt; Ordner verwenden können.



2.  Erstellen Sie eine notice.txt-Datei, die den lokalisierten Benachrichtigungstext enthält.

3.  Speichern Sie die notice.txt Datei im &lt; Ordner *Sprache* &gt; . Wenn Sie beispielsweise eine lokalisierte notice.txt Datei in Spanisch erstellen möchten, speichern Sie die lokalisierte notice.txt Datei im folgenden Ordner:

    &lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\es-es

## Upgrade auf MBAM 2,0 SP1


Sie können von jeder vorherigen Version von MBAM auf MBAM 2,0 SP1 aktualisieren.

### Aktualisieren der MBAM-Infrastruktur

Sie können die MBAM-Server Infrastruktur wie folgt auf MBAM 2,0 SP1 aktualisieren:

**Manueller in-Place-Server Austausch**: Sie müssen die vorhandene MBAM-Serverinfrastruktur manuell deinstallieren und dann die MBAM 2,0 SP1-Serverinfrastruktur installieren. Sie müssen die Datenbanken nicht entfernen, um das Upgrade durchzuführen. Stattdessen wählen Sie die vorhandenen Datenbanken aus, die von der vorherigen Version von MBAM erstellt wurden. Die MBAM 2,0 SP1-Upgrade-Installation migriert dann die vorhandenen Datenbanken zu MBAM 2,0 SP1.

**Upgrade des verteilten Clients**: Wenn Sie die eigenständige MBAM-Topologie verwenden, können Sie die MBAM-Clients nach der Installation der MBAM 2,0 SP1-Server Infrastruktur schrittweise aktualisieren.

Nachdem Sie die MBAM-Server Infrastruktur aktualisiert haben, werden MBAM 1,0-oder 2,0-Clients dem MBAM 2,0 SP1-Server erfolgreich Bericht erstatten und die Wiederherstellungsdaten speichern, die Compliance basiert jedoch auf den Richtlinien, die für die derzeit installierte MBAM-Client Version verfügbar sind. Um die Berichterstellung für MBAM 2,0 SP1-Richtlinien zu aktivieren, müssen Sie Clientcomputer auf MBAM 2,0 SP1 aktualisieren. Sie können die Clientcomputer auf den MBAM 2,0 SP1-Client aktualisieren, ohne den vorherigen Client zu deinstallieren, und der Client wird basierend auf den MBAM 2,0 SP1-Richtlinien mit der Anwendung und dem Bericht beginnen.

Weitere Informationen zum Aktualisieren der MBAM-Server finden Sie unter [Upgrade von früheren Versionen von MBAM](upgrading-from-previous-versions-of-mbam.md).

### Aktualisieren des MBAM-Clients auf MBAM 2,0 SP1

Um Endbenutzercomputer auf den MBAM 2,0 SP1-Client zu aktualisieren, führen Sie **MbamClientSetup.exe** auf jedem Clientcomputer aus. Das Installationsprogramm aktualisiert den Client automatisch auf den MBAM 2,0 SP1-Client. Nach der Installation müssen Clientcomputer nicht neu gestartet werden, und der MBAM 2,0 SP1-Client beginnt, die Richtlinien für MBAM 2,0 SP1 anzuwenden und zu melden.

Wenn Sie MBAM mit Configuration Manager verwenden, müssen Sie die MBAM-Clientcomputer auf MBAM 2,0 SP1 aktualisieren.

Weitere Informationen zum Aktualisieren der MBAM-Clientcomputer finden Sie unter [Upgrade von früheren Versionen von MBAM](upgrading-from-previous-versions-of-mbam.md).

## Installieren oder Aktualisieren auf MBAM 2,0 SP1 mit Configuration Manager


In diesem Abschnitt werden die Anforderungen beschrieben, die bei der Installation von MBAM 2,0 SP1 als neue Installation oder als Upgrade auf eine vorherige MBAM 2,0 SP1-Installation auftreten.

### Erforderliche Dateien für die Installation von MBAM 2,0 SP1, wenn Sie MBAM mit Configuration Manager verwenden

Wenn Sie MBAM zum ersten Mal installieren und MBAM 2,0 SP1 mit System Center Configuration Manager verwenden, müssen Sie MOF-Dateien erstellen oder bearbeiten, damit MBAM mit Configuration Manager ordnungsgemäß funktioniert.

-   **Datei "Configuration. mof"**

    -   Wenn Sie Configuration Manager 2007 verwenden, müssen Sie die Datei "Configuration. mof" Bearbeiten, indem Sie Schritt 3 aus dem Element **Aktualisieren der Datei "Configuration. mof" ausführen, wenn Sie ein Upgrade auf MBAM 2,0 SP1 durchführen und MBAM mit Configuration Manager 2007 verwenden**, das diesem Element folgt.

    -   Wenn Sie den System Center 2012-Konfigurations-Manager verwenden, bearbeiten Sie die Datei "Configuration. mof", indem Sie die Anweisungen unter [Bearbeiten der Datei "Configuration. MOF](edit-the-configurationmof-file.md)" befolgen.

-   **SMS \ _def. MOF-Datei** – folgen Sie den Anweisungen unter [erstellen oder Bearbeiten der SMS \ _def. MOF-Datei](create-or-edit-the-sms-defmof-file.md).

### Aktualisieren Sie die Datei "Configuration. mof", wenn Sie ein Upgrade auf MBAM 2,0 SP1 durchführen und MBAM mit Configuration Manager 2007 verwenden.

Wenn Sie ein Upgrade auf MBAM 2,0 SP1 durchführt und MBAM mit Configuration Manager 2007 verwenden, müssen Sie die Datei "Configuration. mof" aktualisieren, um sicherzustellen, dass MBAM 2,0 SP1 ordnungsgemäß funktioniert.

**So aktualisieren Sie die Datei "Configuration. mof":**

1.  Navigieren Sie auf dem Configuration Manager-Server zum Speicherort der Datei "Configuration. mof":

    &lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv\\

    Bei einer Standardinstallation ist der Installationsspeicherort%SystemDrive%\\Program-Dateien (x86) \\Microsoft-Konfigurations-Manager.

2.  Überprüfen Sie den Codeblock, den Sie an die Datei "Configuration. mof" angefügt haben, und löschen Sie ihn. Der Codeblock ähnelt dem im folgenden Schritt gezeigten Code.

3.  Kopieren Sie den folgenden Codebaustein, und fügen Sie ihn dann an die Datei "Configuration. mof" an, um der Datei die folgenden erforderlichen MBAM-Klassen hinzuzufügen:

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### Übersetzung von MBAM 2,0 SP1

MBAM 2,0 SP1 steht nun in den folgenden Sprachen zur Verfügung:

-   Englisch (USA) en-US
-   Französisch (Frankreich) fr-FR
-   Italienisch (Italien) IT-IT
-   Deutsch (Deutschland) de-de
-   Spanisch, internationale Sortierung (Spanien) es-es
-   Koreanisch (Korea) ko-kr
-   Japanisch (Japan) ja-JP
-   Portugiesisch (Brasilien) pt-br
-   Russisch (Russland) ru-ru
-   Chinesisch (traditionell) zh-tw
-   Chinesisch (vereinfacht) zh-cn

## So erhalten Sie MDOP-Technologien

MBAM 2,0 SP1 ist Teil des Microsoft Desktop Optimization Pack (MDOP). MDOP ist Teil von Microsoft Software Assurance. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Verwandte Themen

[Versionshinweise für MBAM 2.0SP1](release-notes-for-mbam-20-sp1.md)









