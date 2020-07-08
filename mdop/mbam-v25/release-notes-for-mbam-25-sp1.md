---
title: Versionshinweise für MBAM 2.5SP1
description: Versionshinweise für MBAM 2.5SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810885"
---
# Versionshinweise für MBAM 2.5SP1


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 installieren. Diese Versionshinweise enthalten Informationen, die zur erfolgreichen Installation von MBAM erforderlich sind, und können Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn sich diese Versionshinweise von der anderen MBAM 2,5 SP1-Dokumentation unterscheiden, sollten Sie die neueste Änderung als autorisierend ansehen. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> Bekannte Probleme mit MBAM 2,5 SP1


Dieser Abschnitt enthält Anmerkungen zu dieser Version von MBAM 2,5 SP1.

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a>PowerShell Read-AD \ *-Cmdlets geben kein Feedback, wenn der Benutzer nicht über ausreichende Rechte verfügt

Wenn ein Benutzer, der versucht, die PowerShell-Cmdlets "Read-AD \ *" für den MBAM-Server zu verwenden, nicht über Benutzerrechte zum Lesen der Active Directory-Wiederherstellungsinformationen oder zum Lesen der TPM-Informationen verfügt, werden die Cmdlets dem Benutzer keinen Fehler oder keine Warnung bereitstellen.

**Problemumgehung:** Verwenden Sie nur die PowerShell Read-AD \ *-Cmdlets, wenn Sie über die erforderlichen Benutzerrechte verfügen.

### MBAM Active Directory (AD)-Migrations-Cmdlets rufen keine Datenträger Wiederherstellungsinformationen ab

Bei MBAM Active Directory (AD)-Migrations Cmdlets können keine Datenträger Wiederherstellungsinformationen für Computer in Organisationseinheiten abgerufen werden, wenn der Schrägstrich (/) Teil des ou-namens ist. Wiederholte AD-Pulls schlagen fehl, wenn bei diesem Fehler ein Pipeline Abbruchfehler auftritt.

**Technische Informationen:** Dieser Fehler wird angezeigt, wenn Sie den Befehl ausführen:

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

Darüber hinaus sieht die Ausnahmestapelüberwachung `Error[0].Exception.StackTrace` wie folgt aus:

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

**Problemumgehung:** Führen Sie eine der folgenden Aufgaben aus, um dieses Problem zu beheben:

-   Benennen Sie die OU um, um den Schrägstrich zu entfernen, und führen Sie dann das Skript aus.

-   Wenn Sie eine problematische ou aus dem Sicherungsprozess ausschließen möchten, suchen Sie nach einer Liste von OUs, deren Namen nicht das Schrägstrichzeichen enthalten. Führen Sie das Skript in diesen OUs, jeweils eine OU, aus.

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> MBAM kann ein Volume nicht verschlüsseln und meldet einen Fehler, wenn Sie auf einem Tablet-Gerät ein TPM + PIN Protector festzulegen

Wenn Endbenutzer versuchen, eine TPM + PIN-Beschützer auf einem Tablet-Gerät festzulegen, kann MBAM nicht verschlüsselt werden, und es wird ein Fehler gemeldet. Dieses Problem tritt auf, weil Tablet-Geräte nicht über eine Pre-Boot-Umgebungs Tastatur verfügen.

**Problemumgehung:** Aktivieren Sie die Option **Verwendung der BitLocker-Authentifizierung aktivieren, die für die Gruppenrichtlinieneinstellung Vorstart Tastatureingabe erforderlich** ist. Diese Einstellung ist eine BitLocker-Gruppenrichtlinieneinstellung und steht in den MBAM-Gruppenrichtlinienvorlagen nicht zur Verfügung.

### Benutzerprinzipalname ist für alle Dienstkonten erforderlich

Für alle Dienstkonten in MBAM muss ein Benutzerprinzipalname (User Principal Name, UPN) eingerichtet werden. Wenn Sie einen UPN für ein Konto nicht erstellen, wird während des Konfigurationsprozesses eine Fehlermeldung angezeigt, die besagt, dass der Benutzer oder die Gruppe nicht in Active Directory gefunden wurde.

**Problemumgehung:** Fügen Sie den UPN dem Dienstkonto hinzu.

### Self-Service-Portal und die Verwaltungs-und Überwachungs Website werden nicht geöffnet, nachdem Sie IIS auf .NET Framework 4,5 aktualisiert haben

Wenn Sie Internet Informationsdienste (IIS) auf das Microsoft .NET Framework 4,5 aktualisieren, werden das Self-Service-Portal und die Website Verwaltung und Überwachung nicht geöffnet.

**Problemumgehung:** Lesen Sie den Artikel [Fehlermeldung nach der Installation von .NET Framework 4,0: "der Typ konnte nicht geladen werden" System. ServiceModel. Activation. HttpModule "](https://go.microsoft.com/fwlink/?LinkId=393568).

### Website "Verwaltung und Überwachung" zeigt die Fehlermeldung "Bericht kann nicht gefunden werden" an, wenn Berichte nicht konfiguriert sind

Wenn Sie die Website Verwaltung und Überwachung konfigurieren und dann versuchen, einen Bericht anzuzeigen, ohne zuerst das Feature Berichte zu konfigurieren, wird eine Fehlermeldung angezeigt, die besagt, dass der Bericht nicht gefunden werden kann.

**Problemumgehung:** Konfigurieren Sie das Feature Berichte, bevor Sie die Webanwendungen konfigurieren.

### Berichte auf der Website "Verwaltung und Überwachung" zeigen eine Warnung an, wenn SSL in SSRS nicht konfiguriert ist

Wenn SQL Server Reporting Services (SSRS) nicht für die Verwendung von Secure Socket Layer (SSL) konfiguriert wurde, wird die URL für das Feature Berichte auf http anstatt auf HTTPS festgelegt, wenn Sie den MBAM-Server konfigurieren. Wenn Sie dann die Website Verwaltung und Überwachung öffnen und einen Bericht auswählen, wird die folgende Fehlermeldung angezeigt: "nur sicherer Inhalt wird angezeigt."

**Problemumgehung:** Klicken Sie auf **alle Inhalte anzeigen**, um den Bericht anzuzeigen. Um dieses Problem zu beheben, wechseln Sie zum MBAM-Computer, auf dem SQL Server Reporting Services installiert ist, führen Sie **Reporting Services-Konfigurations-Manager**aus, und klicken Sie dann auf **Webdienst-URL**. Wählen Sie das entsprechende SSL-Zertifikat für den Server aus, geben Sie den entsprechenden SSL-Port ein (der Standardport ist 443), und klicken Sie dann auf über **nehmen**.

### Wenn Sie im Bericht zur BitLocker-Konformitätszusammenfassung auf "zurück" klicken, wird möglicherweise ein Fehler ausgelöst.

Wenn Sie einen Drilldown in einen BitLocker-Kompatibilitäts Zusammenfassungsbericht ausführen und dann im SSRS-Bericht auf den Link **zurück** klicken, wird möglicherweise ein Fehler ausgelöst.

**Problemumgehung:** Keine.

### Die Verschlüsselungsstärke wird im BitLocker-Computer Kompatibilitätsbericht falsch angezeigt

Wenn Sie keine bestimmte Verschlüsselungsstärke in den Gruppenrichtlinienobjekten " **Laufwerksverschlüsselung auswählen" und "Verschlüsselungsstärke"** festlegen, wird im BitLocker-Computer Kompatibilitätsbericht in der Configuration Manager-Integrations Topologie immer "unbekannt" für die Verschlüsselungsstärke angezeigt, selbst wenn die Verschlüsselungsstärke den Standardwert der 128-Bit-Verschlüsselung verwendet. Der Bericht zeigt die richtige Verschlüsselungsstärke an, wenn Sie eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt festlegen.

**Problemumgehung:** Legen Sie immer eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt **Auswählen von Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke** fest.

### Kompatibilitäts Status Verteilung nach Laufwerks zeigt alte Daten an, nachdem Sie Konfigurationselemente aktualisiert haben

Nachdem Sie MBAM-Konfigurationselemente in SystemCenter2012 ConfigurationManager aktualisiert haben, werden auf dem BitLocker Enterprise Compliance-Dashboard Daten angezeigt, die auf Informationen aus älteren Versionen der Konfigurationselemente basieren.

**Problemumgehung:** Keine. Änderungen der MBAM-Konfigurationselemente werden nicht unterstützt, und der Bericht wird möglicherweise nicht wie erwartet angezeigt.

### Verbesserte Sicherheitskonfiguration kann dazu führen, dass Berichte eine Fehlermeldung falsch anzeigen

Wenn Internet Explorer Enhanced Security Configuration (ESC) aktiviert ist, wird möglicherweise eine Fehlermeldung "Zugriff verweigert" angezeigt, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen. Standardmäßig ist ESC aktiviert, um den Server zu schützen, indem die Anfälligkeit des Servers für potenzielle Angriffe verringert wird, die über Webinhalte und Anwendungsskripts auftreten können.

**Problemumgehung:** Wenn die Fehlermeldung "Zugriff verweigert" angezeigt wird, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen, können Sie ein Gruppenrichtlinienobjekt festlegen oder den Standardwert manuell in Ihrem Bild ändern, um die erweiterte Sicherheitskonfiguration zu deaktivieren. Sie können auch die Berichte auf einem anderen Computer anzeigen, auf dem ESC nicht aktiviert ist.

### Unterstützung für den BitLocker-XTS-AES-Verschlüsselungsalgorithmus
BitLocker hat Unterstützung für den XTS-AES-Verschlüsselungsalgorithmus in Windows 10, Version 1511, hinzugefügt. Mit HF02 hat MBAM Clientunterstützung für diese BitLocker-Option hinzugefügt, und in HF04 wurde die serverseitige Unterstützung hinzugefügt. Es gibt jedoch eine bekannte Einschränkung:

* Kunden müssen dieselbe Verschlüsselungsstärke für Betriebssystem-und Daten-Volumes auf demselben Computer verwenden.
Bei Verwendung unterschiedlicher Verschlüsselungsstärken meldet MBAM den Computer als **nicht kompatibel**.

### Self-Service-Portal fügt automatisch "-" bei Schlüssel-ID-Eintrag hinzu
Ab HF02 fügt das MBAM Self-Service-Portal automatisch den Schlüssel-ID-Eintrag "-" hinzu.  
**Hinweis:** Der Server muss neu konfiguriert werden, damit das JavaScript wirksam wird.

### MBAM 2,5 SP1-Berichte funktionieren/werden nicht ordnungsgemäß gerendert
Die Seite "Berichte" wird nicht ordnungsgemäß gerendert, wenn SSRS in SQL Server 2016 Edition gehostet wird. 
Zum Beispiel: Durchsuchen des Helpdesks – klicken auf Berichte – (hervorgehobener Anteil hat "x"), der dies mit Fiddler weiter ausgräbt – es sieht so aus, als ob wir auf Berichte klicken – er ruft die Seite SSRS mit dem HTML 4,0-Rendering-Format auf.

**Problemumgehung:** Sehen Sie sich den Website-Master-Code an und beachten Sie, dass der X-UA-Modus als IE8 diktiert wurde. Da IE8 weit hinter dem Ende des Lebens liegt und der Kunde IE11 verwendet. Aktualisieren Sie die Einstellung auf den folgenden Code. Auf diese Weise kann die Website IE11-Rendering-Technologien verwenden

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

Die ursprüngliche Einstellung lautet: 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


Aus diesem Grund wurde das Problem bei anderen Browsern wie Chrome, Firefox usw. nicht angezeigt.



## Verwandte Themen


[Informationen zu MBAM 2.5](about-mbam-25.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





