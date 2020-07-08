---
title: Versionshinweise für MBAM 2.5
description: Versionshinweise für MBAM 2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810882"
---
# Versionshinweise für MBAM 2.5


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 installieren. Diese Versionshinweise enthalten Informationen, die zur erfolgreichen Installation von MBAM erforderlich sind, und können Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn sich diese Versionshinweise von der anderen MBAM 2,5-Dokumentation unterscheiden, sollten Sie die neueste Änderung als autorisierend ansehen. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## <a href="" id="---------mbam-2-5-known-issues"></a> MBAM 2,5 bekannte Probleme


Dieser Abschnitt enthält Anmerkungen zu dieser Version von MBAM 2,5.

### Webbrowser wird versehentlich als Administrator ausgeführt

Hilfe Links im MBAM Server-Konfigurationstool können dazu führen, dass Browserfenster mit Administratorrechten geöffnet werden.

**Problemumgehung:** Aktivieren Sie Internet Explorer Enhanced Security Configuration (IESC), oder schließen Sie den Webbrowser, bevor Sie zu anderen Websites navigieren.

**Hinweis**  Dies ist in MBAM 2,5 SP1 behoben.

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> MBAM-Berichte als nicht kompatibel ein Client, der mit AES 256-Bit-Verschlüsselungsschlüsseln und Diffusor verschlüsselt ist

Wenn auf einem Computer der MBAM 2,5-Client installiert ist und mithilfe des AES 256-Bit mit Diffusor-Verschlüsselungsstärke verschlüsselt wird, wird der MBAM-Client in den MBAM-Konformitätsberichten als nicht kompatibel gemeldet.

**Problemumgehung:** Installieren Sie den Hotfix unter [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> MBAM kann ein Volume nicht verschlüsseln und meldet einen Fehler, wenn Sie auf einem Tablet-Gerät ein TPM + PIN Protector festzulegen

Wenn Endbenutzer versuchen, eine TPM + PIN-Beschützer auf einem Tablet-Gerät festzulegen, kann MBAM nicht verschlüsselt werden, und es wird ein Fehler gemeldet. Dieses Problem tritt auf, weil Tablet-Geräte nicht über eine Pre-Boot-Umgebungs Tastatur verfügen.

**Problemumgehung:** Aktivieren Sie die Option **Verwendung der BitLocker-Authentifizierung aktivieren, die für die Gruppenrichtlinieneinstellung Vorstart Tastatureingabe erforderlich** ist. Diese Einstellung ist eine BitLocker-Gruppenrichtlinieneinstellung und steht in den MBAM-Gruppenrichtlinienvorlagen nicht zur Verfügung.

### Benutzerprinzipalname ist für alle Dienstkonten erforderlich

Für alle Dienstkonten in MBAM muss ein Benutzerprinzipalname (User Principal Name, UPN) eingerichtet werden. Wenn Sie einen UPN für ein Konto nicht erstellen, wird während des Konfigurationsprozesses eine Fehlermeldung angezeigt, die besagt, dass der Benutzer oder die Gruppe nicht in Active Directory gefunden wurde.

**Problemumgehung:** Fügen Sie den UPN dem Dienstkonto hinzu.

### Self-Service-Portal erfordert zusätzliche Konfiguration, wenn Clientcomputer nicht auf das Microsoft AJAX Content Delivery Network zugreifen können

Wenn Ihre Clientcomputer keinen Zugriff auf das Microsoft AJAX Content Delivery Network (CDN) haben, das dem Self-Service-Portal den für bestimmte JavaScript-Dateien erforderlichen Zugriff gewährt, müssen Sie das Self-Service-Portal so konfigurieren, dass es von einer barrierefreien Quelle aus auf die JavaScript-Dateien verweist. Wenn Sie das Self-Service-Portal nicht konfigurieren, wenn Clientcomputer nicht auf CDN zugreifen können, werden nur der Firmenname und das Konto angezeigt, unter dem Sie sich angemeldet haben. Es wird keine Fehlermeldung angezeigt.

**Problemumgehung:** Installieren Sie MBAM 2,5 SP1. oder konfigurieren Sie das Self-Service-Portal, indem Sie die folgenden Anweisungen ausführen: [Konfigurieren des Self-Service-Portals, wenn Client Computer nicht auf das Microsoft Content Delivery Network zugreifen können](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).

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

### Verwendeter Speicherplatz nur die Verschlüsselung funktioniert nicht ordnungsgemäß

Wenn Sie einen Computer nach der Installation des MBAM-Clients zum ersten Mal verschlüsseln und eine Gruppenrichtlinieneinstellung zum Implementieren der nur verwendeter Speicherplatz Verschlüsselung konfiguriert haben, verschlüsselt MBAM fälschlicherweise den gesamten Datenträger, anstatt nur den verwendeten Speicherplatz der Festplatte zu verschlüsseln. Wenn ein Computer bereits mit verwendetem Speicherplatz verschlüsselt ist, wenn Sie den MBAM-Client installieren, und Sie dieselbe Gruppenrichtlinieneinstellung konfiguriert haben, meldet MBAM, dass das Laufwerk richtig verschlüsselt ist, und versucht nicht, das Laufwerk erneut zu verschlüsseln.

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

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a>Hotfixes und Knowledge Base-Artikel für MBAM 2,5


Diese Tabelle enthält die Hotfixes und KB-Artikel für MBAM 2,5.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>KB-Artikel</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2975636</p></td>
<td align="left"><p>Hotfix-Paket 1 für Microsoft BitLocker-Verwaltung und-Überwachung 2,5</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)">support.microsoft.com/kb/2975636/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>3015477</p></td>
<td align="left"><p>Hotfix-Paket 2 für die BitLocker-Verwaltung und-Überwachung 2,5</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)">support.microsoft.com/kb/3015477</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3011022</p></td>
<td align="left"><p>MBAM 2,5-Installation oder Configuration Manager-Berichterstellung schlägt fehl, wenn der Name der SSRS-Instanz einen Unterstrich enthält</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)">support.microsoft.com/kb/3011022/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2756402</p></td>
<td align="left"><p>MBAM-Client schlägt mit Ereignis-ID 4 und Fehlercode 0x8004100E in der Ereignisbeschreibung fehl</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Fehler beim Öffnen von Enterprise-oder Computer Kompatibilitätsberichten in MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>MBAM 2,0-Setup schlägt während des Configuration Manager-Integrationsszenarios mit SQL Server 2008 fehl</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2975472</p></td>
<td align="left"><p>SQL-Deadlocks, wenn viele MBAM-Clients eine Verbindung mit der MBAM-Wiederherstellungsdatenbank herstellen</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)">support.microsoft.com/kb/2975472/EN-US</a></p></td>
</tr>
</tbody>
</table>

 


## Verwandte Themen


[Informationen zu MBAM 2.5](about-mbam-25.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





