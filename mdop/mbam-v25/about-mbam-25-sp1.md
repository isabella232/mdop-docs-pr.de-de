---
title: Infos zu MBAM 2.5 SP1
description: Infos zu MBAM 2.5 SP1
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810162"
---
# Infos zu MBAM 2.5 SP1


MBAM 2,5 SP1 bietet eine vereinfachte Verwaltungsoberfläche für die BitLocker-Laufwerkverschlüsselung. BitLocker bietet erweiterten Schutz vor Datendiebstahl oder Datengefährdung für Computer, die verloren gehen oder gestohlen werden. BitLocker verschlüsselt alle Daten, die auf dem Windows-Betriebssystem gespeichert sind, und Laufwerke und konfigurierte Datenlaufwerke.

## Übersicht über MBAM


MBAM 2,5 SP1 bietet die folgenden Features:

-   Administratoren können die Verschlüsselung von Volumes auf Clientcomputern unternehmensweit automatisieren.

-   Sicherheitsbeauftragte können den Kompatibilitätszustand einzelner Computer oder sogar des ganzen Unternehmens schnell ermitteln.

-   Berichterstellung und Hardwareverwaltung können zentral mit Microsoft System Center Configuration Manager erfolgen.

-   Verringert die Arbeitsbelastung des Helpdesks, um Endbenutzern die BitLocker-PIN-und Wiederherstellungsschlüssel Anforderungen zu unterstützen.

-   Endbenutzer können verschlüsselte Geräte mithilfe des Self-Service-Portals eigenständig wiederherstellen.

-   Ermöglicht es Sicherheitsbeauftragten, den Zugriff auf die Wiederherstellung wichtiger Informationen einfach zu überwachen.

-   Windows Enterprise-Benutzer können standortunabhängig arbeiten und sich dabei darauf verlassen, dass ihre Unternehmensdaten geschützt sind.

MBAM erzwingt die BitLocker-Verschlüsselungsrichtlinien Optionen, die Sie für Ihr Unternehmen festzulegen, überwacht die Kompatibilität von Clientcomputern mit diesen Richtlinien und meldet den Verschlüsselungsstatus der Computer des Unternehmens und der einzelnen Personen. Darüber hinaus können Sie mit MBAM auf die Wiederherstellungsschlüssel Informationen zugreifen, wenn Benutzer Ihre PIN oder Ihr Kennwort vergessen oder wenn sich die BIOS-oder Startdatensätze ändern.

Die folgenden Gruppen sind möglicherweise an der Verwendung von MBAM für die Verwaltung von BitLocker interessiert:

-   Administratoren, IT-Sicherheitsexperten und Compliance Officer, die dafür verantwortlich sind, sicherzustellen, dass vertrauliche Daten nicht ohne Autorisierung freigegeben werden

-   Administratoren, die für die Computersicherheit in Remote-oder Zweigstellen zuständig sind

-   Administratoren, die für Clientcomputer mit Windows verantwortlich sind

**Hinweis**  BitLocker wird in dieser MBAM-Dokumentation nicht ausführlich erläutert. Weitere Informationen finden Sie unter [Übersicht über die BitLocker-Laufwerkverschlüsselung](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a>Neuerungen in MBAM 2,5 SP1


In diesem Abschnitt werden die neuen Features in MBAM 2,5 SP1 beschrieben.

### Neu unterstützte Sprachen für den MBAM 2,5 SP1-Client

Die folgenden zusätzlichen Sprachen werden jetzt in MBAM 2,5 SP1 nur für den MBAM-Client unterstützt, einschließlich des Self-Service-Portals:

Tschechische Republik (Tschechien) cs-cz

Dänisch (Dänemark) da-DK

Niederländisch (Niederlande) nl-nl

Finnisch (Finnland) fi-fi

Griechisch (Griechenland) el-gr

Ungarisch (Ungarn) hu-hu

Norwegisch, Nynorsk (Norwegen) NB-Nein

Polnisch (Polen) pl-pl

Portugiesisch (Portugal) pt-pt

Slowakisch (Slowakei) sk-SK

Slowenisch (Slowenien) SL-SI

SV-SE für Schwedisch (Schweden)

Türkisch (Türkei) tr-TR

Eine Liste aller für Client und Server unterstützten Sprachen in MBAM 2,5 und MBAM 2,5 SP1 finden Sie unter [unterstützte Konfigurationen in MBAM 2,5](mbam-25-supported-configurations.md).

### Unterstützung für Windows 10

MBAM 2,5 SP1 bietet zusätzlich zu der Software, die in früheren Versionen von MBAM unterstützt wird, Unterstützung für Windows 10 und Windows Server 2016.

Windows 10 wird sowohl in MBAM 2,5 als auch in MBAM 2,5 SP1 unterstützt.

### Unterstützung für Microsoft SQL Server 2014 SP1

MBAM 2,5 SP1 bietet zusätzlich zu der Software, die in früheren Versionen von MBAM unterstützt wird, Unterstützung für Microsoft SQL Server 2014 SP1.

### MBAM wird nicht mehr mit separatem MSI ausgeliefert

Ab MBAM 2,5 SP1 ist eine separate MSI-Version nicht mehr im MBAM-Produkt enthalten. Sie können die MSI-Datei jedoch aus der ausführbaren Datei (. exe) extrahieren, die im Lieferumfang des Produkts enthalten ist.

### MBAM können OwnerAuth-Kennwörter über Escrow-Konto ohne TPM besitzen

Wenn MBAM das TPM zuvor nicht besitzt, konnte das TPM-OwnerAuth nicht an die MBAM-Datenbank überlassen werden. Um MBAM für das TPM zu konfigurieren und die Kennwörter zu speichern, mussten Sie die TPM-automatische Bereitstellung deaktivieren und das TPM auf dem Clientcomputer löschen.

In Windows 8 und höher kann MBAM 2,5 SP1 nun die OwnerAuth-Kennwörter über einen Treuhandservice verwerten, ohne das TPM besitzen zu müssen. Während des Starts des Diensts MBAM Abfragen, ob das TPM bereits im Besitz ist, und wenn dies der Fall ist, fordert es die Kennwörter des Betriebssystems an. Die Kennwörter werden dann in der MBAM-Datenbank gespeichert. Darüber hinaus muss die Gruppenrichtlinie so eingestellt sein, dass die OwnerAuth nicht lokal gelöscht werden.

In Windows 7 muss MBAM das TPM besitzen, damit TPM-OwnerAuth-Informationen automatisch in der MBAM-Datenbank gespeichert werden. Wenn MBAM nicht über die TPM-und Active Directory (AD)-Sicherung des TPM verfügt, das über Gruppenrichtlinien konfiguriert ist, müssen Sie die **MBAM Active Directory (AD)-Daten Import-Cmdlets** verwenden, um die TPM-OwnerAuth aus AD in die MBAM-Datenbank zu kopieren. Hierbei handelt es sich um fünf neue PowerShell-Cmdlets, die MBAM-Datenbanken mit den in Active Directory gespeicherten Informationen zur Volume-Wiederherstellung und den TPM-Besitzern vorab ausfüllen.

Weitere Informationen finden Sie unter [Sicherheitsüberlegungen zu MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).

### MBAM kann das TPM nach einer Sperrung automatisch entsperren

Auf Computern mit TPM 1,2 können Sie jetzt MBAM so konfigurieren, dass das TPM bei einer Sperrung automatisch freigegeben wird. Wenn die Funktion zum automatischen Zurücksetzen der TPM-Sperrung aktiviert ist, kann MBAM feststellen, dass ein Benutzer gesperrt ist, und das OwnerAuth-Kennwort aus der MBAM-Datenbank abrufen, um das TPM automatisch für den Benutzer zu entsperren.

Dieses Feature muss sowohl auf der Serverseite als auch in den Gruppenrichtlinien auf der Clientseite aktiviert sein. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen zu MBAM 2,5](mbam-25-security-considerations.md#bkmk-autounlock).

### Unterstützung für FIPS-kompatiblen BitLocker-Kennwortschutz

In mbam 2.5 wurde die Unterstützung für FIPS (Federal Information Processing Standard)-kompatible BitLocker-Wiederherstellungsschlüssel auf Geräten mit dem Betriebssystem Windows 8,1 hinzugefügt. Windows hat jedoch FIPS-konforme Wiederherstellungsschlüssel in Windows 7 nicht implementiert. Daher ist für Windows 7-und Windows 8-Geräte weiterhin ein Daten Wiederherstellungs-Agent (DRA)-Schutz für die Wiederherstellung erforderlich.

Das Windows-Team hat FIPS-konforme Wiederherstellungsschlüssel mit einem Hotfix und MBAM 2,5 SP1 ebenfalls unterstützt.

**Hinweis**  Auf Client Computern, auf denen das Windows8-Betriebssystem ausgeführt wird, ist weiterhin eine DRA-Schutzkomponente erforderlich, da der Hotfix nicht auf dieses Betriebssystem portiert wurde. Informationen zum herunterladen und Installieren des BitLocker-Hotfixes für Windows 7-und Windows 8-Computer finden Sie unter [Hotfix-Paket 2 für die BitLocker-Verwaltung und-Überwachung 2,5](https://support.microsoft.com/kb/3015477) . Informationen zu DRA finden Sie unter [Verwenden von Daten Wiederherstellungs-Agents mit BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

 

Um die FIPS-Konformität in Ihrer Organisation zu aktivieren, müssen Sie die FIPS-Gruppenrichtlinieneinstellungen (Federal Information Processing Standard) konfigurieren. Konfigurationsanweisungen finden Sie unter [BitLocker-Gruppenrichtlinieneinstellungen](https://go.microsoft.com/fwlink/?LinkId=393560).

### Anpassen der Pre-Boot-Wiederherstellungs Nachricht und-URL mit der neuen Gruppenrichtlinieneinstellung

Mit einer neuen Gruppenrichtlinieneinstellung, **Konfiguration der Pre-Boot-Wiederherstellungs Nachricht und-URL**, können Sie eine benutzerdefinierte Wiederherstellungs Nachricht konfigurieren oder eine URL angeben, die auf dem BitLocker-Wiederherstellungsbildschirm vor dem Start angezeigt wird, wenn das Betriebssystemlaufwerk gesperrt ist. Diese Einstellung steht nur auf Clientcomputern mit Windows 10 zur Verfügung.

Wenn Sie diese Richtlinieneinstellung aktivieren, können Sie eine der folgenden Optionen für die Wiederherstellungs Nachricht vor dem Start auswählen:

-   **Benutzerdefinierte Wiederherstellungs Nachricht verwenden**: Wählen Sie diese Option aus, um eine benutzerdefinierte Nachricht in den BitLocker-Wiederherstellungsbildschirm vor dem Start einzubeziehen.

-   **Benutzerdefinierte Wiederherstellungs-URL verwenden**: Wählen Sie diese Option aus, um die Standard-URL zu ersetzen, die auf dem BitLocker-Wiederherstellungsbildschirm vor dem Start angezeigt wird.

-   **Standard-Wiederherstellungs Nachricht und-URL verwenden**: Wählen Sie diese Option aus, um die standardmäßige BitLocker-Wiederherstellungs Nachricht und-URL im Pre-Boot BitLocker-Wiederherstellungsbildschirm anzuzeigen Wenn Sie zuvor eine benutzerdefinierte Wiederherstellungs Nachricht oder-URL konfiguriert haben und die Standardnachricht wiederherstellen möchten, müssen Sie diese Richtlinie aktivieren und diese Option auswählen.

Die neue Gruppenrichtlinieneinstellung befindet sich im folgenden GPO-Knoten: **Computerkonfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)-** &gt; **Betriebs System Laufwerk**. Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppenrichtlinienanforderungen](planning-for-mbam-25-group-policy-requirements.md).

### MBAM hat Unterstützung für die verwendete Speicherplatz Verschlüsselung hinzugefügt

Wenn Sie in MBAM 2,5 SP1 die gebrauchte Speicherplatz Verschlüsselung über BitLocker-Gruppenrichtlinien aktivieren, ehrt der MBAM-Client diesen.

Diese Gruppenrichtlinieneinstellung wird **auf Betriebssystemlaufwerken als Erzwingen des Laufwerk Verschlüsselungstyps** bezeichnet und befindet sich im folgenden GPO-Knoten: **Computerkonfigurations** - &gt; **Administrative Vorlagen** &gt; **Windows-Komponenten** &gt; **BitLocker Drive Encryption** - &gt; **Betriebssystemlaufwerke**. Wenn Sie diese Richtlinie aktivieren und den Verschlüsselungstyp als **nur verwendeter Speicherplatz Verschlüsselung**auswählen, wird die Richtlinie von MBAM berücksichtigt, und BitLocker verschlüsselt nur den auf dem Volume verwendeten Speicherplatz.

Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppenrichtlinienanforderungen](planning-for-mbam-25-group-policy-requirements.md).

### MBAM-Client Unterstützung für verschlüsselte Festplatten

MBAM unterstützt BitLocker auf verschlüsselten Festplatten, die die TCG-Spezifikationsanforderungen für Opal-und IEEE-1667-Standards erfüllen. Wenn BitLocker auf diesen Geräten aktiviert ist, generiert es Schlüssel und führt Verwaltungsfunktionen auf dem verschlüsselten Laufwerk aus. Weitere Informationen finden Sie unter [verschlüsselte Festplatte](https://technet.microsoft.com/library/hh831627.aspx) .

### Delegierungs Konfiguration wird beim Registrieren von SPNs nicht mehr benötigt

Die Anforderung zum Konfigurieren einer beschränkten Delegierung für SPNs, die Sie für das Anwendungspoolkonto registrieren, ist in MBAM 2,5 SP1 nicht mehr erforderlich. Es ist jedoch weiterhin eine Voraussetzung für MBAM 2,5.

### Aktivieren von BitLocker mithilfe von MBAM als Teil einer Windows-Bereitstellung

In MBAM 2,5 SP1 können Sie ein PowerShell-Skript verwenden, um die BitLocker-Laufwerkverschlüsselung und die Escrow-Wiederherstellungsschlüssel für den MBAM-Server zu konfigurieren.

Weitere Informationen finden Sie unter so wird [es gemacht: Aktivieren von BitLocker mithilfe von MBAM als Teil einer Windows-Bereitstellung](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

### Self-Service-Portal kann mithilfe von PowerShell oder dem SSP-Anpassungs-Assistenten angepasst werden

Ab MBAM 2,5 SP1 kann das Self-Service-Portal mithilfe des Anpassungs-Assistenten und mithilfe von PowerShell konfiguriert werden. Weitere Informationen finden Sie unter [Konfigurieren der MBAM 2,5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md).

### Webbrowser wird nicht mehr versehentlich als Administrator ausgeführt

Ein Problem in MBAM 2,5 hat dazu geführt, dass die Hilfe Links im Serverkonfigurations Tool dazu führen, dass Browserfenster mit Administratorrechten geöffnet werden. Dieses Problem wurde in MBAM 2,5 SP1 behoben.

### Sie müssen die JavaScript-Dateien nicht mehr herunterladen, um das Self-Service-Portal zu konfigurieren, wenn auf das CDN nicht zugegriffen werden kann.

In MBAM 2,5 und früheren Versionen mussten die für die Konfiguration des Self-Service-Portals verwendeten jQuery-Dateien im Voraus aus dem CDN heruntergeladen werden, wenn Clients, die auf das Self-Service-Portal zugreifen, keinen Internetzugriff hatten. In MBAM 2,5 SP1 sind alle JavaScript-Dateien im Produkt enthalten, daher ist das Herunterladen unnötig.

### Berichte können im Berichts-Generator 3,0 geöffnet werden

In MBAM 2,5 SP1 wurden die Berichte auf das neueste Schema der Berichtsdefinitionssprache aktualisiert, sodass Benutzer die Berichte im Berichts-Generator 3,0 öffnen und anpassen und diese sofort speichern können, ohne die Berichtsdatei zu beschädigen.

### Neue PowerShell-Cmdlets

Mit den neuen PowerShell-Cmdlets für MBAM 2,5 SP1 können Sie verschiedene MBAM-Features wie Datenbanken, Berichte und Webanwendungen konfigurieren und verwalten. Jedes Feature verfügt über ein entsprechendes PowerShell-Cmdlet, das Sie zum Aktivieren oder Deaktivieren von Features oder zum Abrufen von Informationen über das Feature verwenden können.

Die folgenden Cmdlets wurden für MBAM 2,5 SP1 implementiert:

-   Write-MbamTpmInformation

-   Write-MbamRecoveryInformation

-   Lesen-ADTpmInformation

-   Lesen-ADRecoveryInformation

-   Write-MbamComputerUser

Die folgenden Parameter wurden in den Cmdlets Enable-MbamWebApplication und Test-MbamWebApplication für MBAM 2,5 SP1 implementiert:

-   DataMigrationAccessGroup

-   TpmAutoUnlock

Informationen zu den Cmdlets finden Sie unter Hilfe zu den [MBAM 2,5-Sicherheitsüberlegungen](mbam-25-security-considerations.md) und [Microsoft BitLocker-Cmdlets für Verwaltung und Überwachung](https://technet.microsoft.com/library/dn720418.aspx).

### MBAM-Agent erkennt Präsentationsmodus

Der MBAM-Agent kann erkennen, wenn sich der Computer im Präsentationsmodus befindet, und vermeiden, dass die MBAM-Benutzeroberfläche zu diesem Zeitpunkt aufgerufen wird.

### MBAM-Agent-Dienst ist jetzt für die Verwendung des verzögerten Starts konfiguriert

Nach der Installation wird der Dienst den MBAM-Agent-Dienst so einrichten, dass er den verzögerten Start verwendet, wodurch die Zeit verkürzt wird, die zum Starten von Windows benötigt wird.

### Gesperrte feste Datenvolumina werden jetzt als kompatibel gemeldet

Die Logik für die Kompatibilitäts Berechnung für die Volumes "gesperrte feste Daten" wurde geändert, um die Volumes als "kompatibel" zu melden, aber mit einem Protector-Zustand und einem Verschlüsselungsstatus von "unbekannt" und mit einem Kompatibilitäts Status ("Volume ist gesperrt"). Zuvor wurden gesperrte Volumes als "nicht kompatibel", als Schutzstatus "verschlüsselt", als Verschlüsselungsstatus "unbekannt" und als Kompatibilitätsstatus Detail "ein unbekannter Fehler" gemeldet.


## So erhalten Sie MDOP-Technologien


MBAM ist ein Bestandteil des Microsoft-Desktop Optimierungs Pakets (MDOP). MDOP ist Teil des Microsoft Software Assurance-Programms. Weitere Informationen zum Microsoft Software Assurance-Programm und zum Erwerb der MDOP finden Sie unter [wie erhalte ich MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## MBAM 2,5 SP1-Versionshinweise


Weitere Informationen und aktuelle Neuigkeiten, die nicht in dieser Dokumentation enthalten sind, finden Sie unter [Versionshinweise zu MBAM 2,5 SP1](release-notes-for-mbam-25-sp1.md).

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Verwandte Themen


[Microsoft BitLocker Administration and Monitoring 2.5](index.md)

[Erste Schritte mit MBAM 2.5](getting-started-with-mbam-25.md)

 

 





