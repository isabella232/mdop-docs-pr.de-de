---
title: Versionshinweise für MBAM 1.0
description: Versionshinweise für MBAM 1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811509"
---
# Versionshinweise für MBAM 1.0


**Drücken Sie STRG + F, um nach einem bestimmten Problem in diesen Versionshinweisen zu suchen.**

Lesen Sie diese Versionshinweise gründlich, bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) installieren.

Diese Versionshinweise enthalten Informationen, die zur erfolgreichen Installation von MBAM erforderlich sind. Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer MBAM-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Informationen zur Produktdokumentation


Informationen zur MBAM-Dokumentation finden Sie auf der MBAM-Startseite auf der Microsoft TechNet-Website.

Eine herunterladbare Kopie der MBAM-Dokumentation finden Sie <https://go.microsoft.com/fwlink/p/?LinkId=225356> im Microsoft Download Center.

## Feedback geben


Wir sind an Ihrem Feedback zu MBAM interessiert. Sie können Ihr Feedback an senden <mdopdocs@microsoft.com> .

**Hinweis**  Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback wird uns helfen, zukünftige Änderungen in unseren Dokumentations-und Produktversionen zu planen.

 

Die neuesten Informationen zu MDOP und weiteren Lernressourcen finden Sie auf der Seite [MDOP-Informationen](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Wenn Sie weitere Informationen zu neuen Updates oder Feedback geben möchten, folgen Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Bekannte Probleme mit MBAM 1,0


Dieser Abschnitt enthält Versionshinweise zu den bekannten Problemen bei der Einrichtung und Installation von MBAM.

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a>Wenn Sie während des Setups die Option "Zertifikat zum Verschlüsseln der Netzwerkkommunikation verwenden" auswählen, können vorhandene Datenbankverbindungen und abhängige Anwendungen nicht mehr funktionieren.

Sie können MBAM für eine **verschlüsselte Netzwerkkommunikation** konfigurieren, nachdem Sie die Wiederherstellungs-und Hardware Datenbank oder die Kompatibilitäts Status-Datenbankfeatures installiert haben. Wenn Sie MBAM für die verschlüsselte Netzwerkkommunikation konfigurieren, konfiguriert MBAM Setup die Instanz von SQL Server-Datenbankmodul für die Verwendung von Secure Sockets Layer (SSL) für die Kommunikation zwischen der betreffenden Datenbank und dem Verwaltungs-und Überwachungsserver sowie den Funktionen für Compliance-und Überwachungsberichts Server.

-   Wenn die Instanz des SQL Server-Datenbankmoduls noch nicht für die Verwendung von SSL konfiguriert ist, wird Sie von MBAM Setup so konfiguriert. Dadurch kann verhindert werden, dass Anwendungen, die versuchen, nicht MBAM-Datenbanken auf der Instanz von SQL Server-Datenbankmodul zu verwenden, die Kommunikation mit ihren Datenbanken verhindern.

-   Wenn die Instanz des SQL Server-Datenbankmoduls bereits für die Verwendung von SSL konfiguriert ist, ist Sie für die Verwendung des Zertifikats konfiguriert, das der Benutzer während der Installation ausgewählt hat. Wenn sich dieses Zertifikat von dem bereits verwendeten unterscheidet, kann es verhindern, dass Anwendungen, die SQL Server-Datenbanken auf der Instanz des SQL Server-Datenbankmoduls verwenden, ausgeführt werden.

**Problemumgehung:** Keine

### MBAM-Setup schlägt während der Installation fehl, wenn Sie ein lokales Administrator Konto verwenden

MBAM-Setup schlägt fehl, wenn Sie ein lokales Administrator Konto verwenden. Die Protokolldatei enthält die folgenden Informationen:

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

**Problemumgehung:** Verwenden Sie bei der Installation von MBAM ein Domänenkonto mit administrativen Anmeldeinformationen auf dem Server Computer.

### MBAM-Setup konfiguriert die Instanz von SQL Server-Datenbankmodul neu, um SSL nicht zu verwenden, wenn Sie "Netzwerkkommunikation nicht verschlüsseln" auswählen.

Wenn Sie entweder die Wiederherstellungs-und Hardware Datenbank oder die Kompatibilitäts Status Datenbank installieren, können Sie mithilfe von Setup MBAM konfigurieren, indem Sie die **verschlüsselte Netzwerkkommunikation**auswählen. Wenn Sie sich entschließen, die Netzwerkkommunikation zu verschlüsseln, konfiguriert MBAM Setup die Instanz von SQL Server-Datenbankmodul neu, sodass SSL nicht verwendet wird.

-   Wenn die Instanz des SQL Server-Datenbankmoduls bereits für die Verwendung von SSL konfiguriert ist, deaktiviert das MBAM-Setup SSL für die Instanz des SQL Server-Datenbankmoduls. Dadurch wird die Kommunikationssicherheit zwischen den Anwendungen geändert, die Datenbanken verwenden, die nicht mit MBAM-Datenbanken in der Instanz von SQL Server-Datenbankmodul verknüpft sind.

**Problemumgehung:** Keine

### Fehlende Voraussetzung für die Internetinformationsdienste (IIS)-Verwaltungsskripts und Tools-Webserver Feature

MBAM-Setup ist vom IIS-Verwaltungsskripts und Tools-Webserver Feature abhängig, ist aber keine erzwungene Voraussetzung. Mit dem Server-Setup können Sie MBAM installieren, wenn dieses Feature nicht vorhanden ist. Dies führt jedoch dazu, dass der VSS-Writer des Sicherungsdiensts MBAM gestartet und dann beendet wird, da er nicht die Windows-Verwaltungsinstrumentation (WMI) und den Internet Informationsdienste (IIS)-Anbieter finden kann. Es ist keine Fehlermeldung für diese Bedingung vorhanden, es sei denn, dies geschieht im Ereignisprotokoll. Die Installation von MBAM ohne IIS-Verwaltungsskripts und-Tools führt dazu, dass die Sicherungsvorgänge nicht für MBAM ausgeführt werden.

**Problemumgehung:** Stellen Sie sicher, dass das Feature IIS-Verwaltungsskripts und Tools-Webserver installiert ist, bevor Sie das MBAM-Setup starten.

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a>MBAM-Setup reagiert nicht mehr während der Phase "ausgewählte Features installieren", wenn Setup für die Verwendung eines Zertifikats konfiguriert ist

MBAM-Setup reagiert während der **Installation der ausgewählten Features** -Phase des Setups nicht mehr. Dies tritt während der Installation der Wiederherstellungs-und Hardware Datenbank oder der Kompatibilitäts Status Datenbank auf, nachdem Sie die Option **Zertifikat zum Verschlüsseln der Netzwerkkommunikation verwenden** ausgewählt haben. Darüber hinaus reagiert das MBAM-Setup nicht mehr, wenn die Instanz des SQL Server-Datenbankmoduls nicht auf das Zertifikat zugreifen kann, das während des Setups angegeben wurde.

**Problemumgehung:** Aktualisieren Sie die Berechtigungen für das Zertifikat, damit der Windows-Dienst für die anwendbare Instanz von SQL Server-Datenbankmodul auf das Zertifikat zugreifen kann. Sie können auch das Konto ändern, unter dem die Instanz des SQL Server-Datenbankmoduls ausgeführt wird, damit Datenbankmodul das Zertifikat verwenden kann. Wenn Sie die Berechtigungen für das Zertifikat ermitteln möchten, geben Sie an der Eingabeaufforderung den folgenden Befehl ein: **certutil-v-Store My**

### MBAM-Setup wird angehalten, wenn Sie SQL Server Reporting Services installieren

Wenn Sie während der MBAM-Installation eine Instanz von SQL Server Reporting Services (SSRS) auswählen und die SSRS-Instanz nicht verfügbar oder falsch konfiguriert ist, wird das MBAM-Setup möglicherweise bis zu einer Minute angehalten, während es versucht, mit der SSRS-Instanz zu kommunizieren.

**Problemumgehung:** Warten Sie mindestens eine Minute, bis das MBAM-Setup fortgesetzt wird, während das Setup-Programm versucht, sich mit der Instanz von SSRS in Verbindung zu setzen.

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a>Der Administrations-und Überwachungs Server wird nach dem Setup nicht ausgeführt

Nachdem das MBAM-Setup die Verwaltungs-und Überwachungs Server Funktion erfolgreich installiert hat, zeigt MBAM Fehlermeldungen an, wenn Sie versuchen, auf die MBAM-Administratorwebsite zuzugreifen. Dieses Problem tritt aus einem der folgenden Gründe auf:

-   Eine oder mehrere Voraussetzungen für den Verwaltungs-und Überwachungs Server wurden nach der MBAM-Installation entfernt.

-   Eine oder mehrere Voraussetzungen wurden auf dem Server installiert, und später wurden Sie entfernt, bevor Sie das MBAM-Setup ausführen.

**Problemumgehung:** Überprüfen Sie die MBAM-Dokumentation, und stellen Sie sicher, dass alle MBAM-Voraussetzungen installiert sind.

### Wenn Sie während des Setups auf "Dokumentations Verknüpfungen" klicken, wird nach Abschluss des Setups ein Anwendungsfehler angezeigt

Wenn Sie während des Setups auf einen Link zur Dokumentation klicken und dann das Setup-Programm schließen, indem Sie auf **Abbrechen** oder **Fertig stellen** klicken, nachdem das Setup erfolgreich abgeschlossen wurde, wird eine Fehlermeldung mit der Anwendung angezeigt. Das Problem wird durch einen Zugriffsverletzungsfehler im Windows-Aufgabenplaner verursacht.

**Problemumgehung:** Keine. Sie können diesen Fehler ignorieren.

### Fehler MBAM-Setup entfernt keine neuen Datenbanken

Wenn das MBAM-Setup fehlschlägt, entfernt Setup die neu erstellten Datenbanken möglicherweise nicht. Dies kann bei nachfolgenden Installationen zu Fehlern führen.

**Problemumgehung:** Wählen Sie bei der nachfolgenden Installation einen anderen Namen für die Datenbankinstanz aus.

### MBAM-Setup erkennt keine gültigen Netzwerklastenausgleich-Cluster Zertifikate

Während der Installation von MBAM Administration and Monitoring Server wird das Cluster Zertifikat bei Auswahl der Option Netzwerk Verschlüsselung nicht als gültiges Zertifikat erkannt. Sie wird als gültig erkannt, wenn das Zertifikat für die Kommunikation mit der Datenbank installiert ist, aber für die Kommunikation durch den Lastenausgleichscluster abgelehnt wurde.

**Problemumgehung:** Überprüfen Sie, ob die dem Zertifikat zugeordnete Zertifikatsperrliste (Certificate Revocation List, CRL) barrierefrei ist, oder verwenden Sie ein Zertifikat, das keine Validierung mithilfe der CRL erfordert.

## Anmerkungen zu dieser Version Copyright-Informationen


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe. Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.



## Verwandte Themen


[Informationen zu MBAM 1.0](about-mbam-10.md)

 

 





