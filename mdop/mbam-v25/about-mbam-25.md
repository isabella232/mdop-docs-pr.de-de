---
title: Informationen zu MBAM 2.5
description: Informationen zu MBAM 2.5
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810420"
---
# Informationen zu MBAM 2.5


Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 bietet eine vereinfachte Verwaltungsoberfläche für die BitLocker-Laufwerkverschlüsselung. BitLocker bietet erweiterten Schutz vor Datendiebstahl oder Datengefährdung für Computer, die verloren gehen oder gestohlen werden. BitLocker verschlüsselt alle Daten, die auf den Volumes und Laufwerken des Windows-Betriebssystems gespeichert sind, und konfigurierte Datenlaufwerke.

## Übersicht über MBAM


MBAM 2,5 verfügt über die folgenden Features:

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

 

## <a href="" id="what-s-new-in-mbam-2-5"></a>Neuerungen in MBAM 2,5


In diesem Abschnitt werden die neuen Features in MBAM 2,5 beschrieben.

### Unterstützung für Microsoft SQL Server 2014

MBAM fügt zusätzlich zur gleichen Software, die in früheren Versionen von MBAM unterstützt wird, Unterstützung für Microsoft SQL Server 2014 hinzu.

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> MBAM-Gruppenrichtlinienvorlagen, die separat heruntergeladen wurden

Die Vorlagen für MBAM-Gruppenrichtlinien müssen separat aus der MBAM-Installation heruntergeladen werden. In früheren Versionen von MBAM umfasste das MBAM-Installationsprogramm eine MBAM-Richtlinienvorlage, die die erforderlichen MBAM-spezifischen Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) enthielt, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Diese GPOs wurden aus dem MBAM-Installationsprogramm entfernt. Sie laden die GPOs jetzt herunter, indem Sie die [MDOP-Gruppenrichtlinien (ADMX)-Vorlagen abrufen](https://go.microsoft.com/fwlink/p/?LinkId=393941) und auf einen Server oder eine Arbeitsstation kopieren, bevor Sie mit der Installation des MBAM-Clients beginnen. Sie können die Vorlagen für Gruppenrichtlinien auf alle Server oder Workstations kopieren, auf denen eine unterstützte Version des Windows-Servers oder Windows-Betriebssystems ausgeführt wird.

**Wichtig**  Ändern Sie die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten nicht, oder MBAM wird nicht ordnungsgemäß funktionieren. Wenn Sie die Gruppenrichtlinieneinstellungen im MDOP- **MBAM (BitLocker-Verwaltungsknoten)** konfigurieren, konfiguriert MBAM automatisch die BitLocker-Laufwerk Verschlüsselungseinstellungen für Sie.

 

Die Vorlagendateien, die Sie auf einen Server oder eine Workstation kopieren müssen, sind:

-   BitLockerManagement. ADML

-   BitLockerManagement. ADMX

-   BitLockerUserManagement. ADML

-   BitLockerUserManagement. ADMX

Kopieren Sie die Vorlagendateien an die Stelle, die Ihren Anforderungen am besten entspricht. Für die sprachspezifischen Dateien, die in einen sprachspezifischen Ordner kopiert werden müssen, ist die Gruppenrichtlinien-Verwaltungskonsole erforderlich, um die Dateien anzuzeigen.

- Wenn Sie die Vorlagendateien lokal auf einem Server oder einer Arbeitsstation installieren möchten, kopieren Sie die Dateien an einen der folgenden Speicherorte.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Dateityp</th>
  <th align="left">Dateispeicherort</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>sprachneutral (ADMX)</p></td>
  <td align="left"><p><em>% systemroot% </em> \policyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>sprachspezifisch (. ADML)</p></td>
  <td align="left"><p><em>% systemroot% </em> \policyDefinitions [ <em> MUIculture </em> ] (beispielsweise wird die spezifische Datei für die US-englische Sprache in <em> % systemroot% &lt; /EM policyDefinitions\en-US gespeichert &gt; )</p></td>
  </tr>
  </tbody>
  </table>

     

- Wenn Sie die Vorlagen für alle Gruppenrichtlinienadministratoren in einer Domäne verfügbar machen möchten, kopieren Sie die Dateien an einen der folgenden Speicherorte auf einem Domänencontroller.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Dateityp</th>
  <th align="left">Speicherort der Domänencontroller Datei</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>Sprachneutral (ADMX)</p></td>
  <td align="left"><p><em>% systemroot% </em> sysvol\domain\policies\PolicyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>Sprachspezifisch (. ADML)</p></td>
  <td align="left"><p><em>% systemroot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (Beispiel: die sprachspezifische US-Datei wird in <em> % systemroot% \sysvol\domain\policies\PolicyDefinitions\en-US gespeichert </em> )</p></td>
  </tr>
  </tbody>
  </table>

     

Weitere Informationen zu Vorlagendateien finden Sie unter [Verwalten von Gruppenrichtlinien-ADMX-Dateien – Schritt-für-Schritt-Anleitung](https://go.microsoft.com/fwlink/?LinkId=392818).

### Möglichkeit zum Erzwingen von Verschlüsselungsrichtlinien für Betriebssystem-und fest Netzlaufwerke

Mit MBAM 2.5 können Sie Verschlüsselungsrichtlinien für das Betriebssystem und feste Datenlaufwerke für Computer in Ihrer Organisation erzwingen und die Anzahl der Tage begrenzen, die Endbenutzer eine Verschiebung der Anforderung zur Einhaltung der MBAM-Verschlüsselungsrichtlinien anfordern können.

Damit Sie die Verschlüsselungsrichtlinien Erzwingung konfigurieren können, wurde eine neue Gruppenrichtlinieneinstellung namens Verschlüsselungsrichtlinien Erzwingungseinstellungen für Betriebssystemlaufwerke und fest Netzlaufwerke hinzugefügt. Diese Richtlinie wird in der folgenden Tabelle beschrieben.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gruppenrichtlinieneinstellung</th>
<th align="left">Beschreibung</th>
<th align="left">Zum Konfigurieren dieser Einstellung verwendeter Gruppenrichtlinien Knoten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Einstellungen für die Verschlüsselungsrichtlinien Erzwingung (Betriebs System Laufwerk)</p></td>
<td align="left"><p>Verwenden Sie für diese Einstellung die Option <strong> Konfigurieren der Anzahl der nicht Konformitäts kulanztage für Betriebssystemlaufwerke </strong> , um einen Kulanzzeitraum zu konfigurieren.</p>
<p>Der Kulanzzeitraum gibt die Anzahl der Tage an, die Endbenutzer die Einhaltung der MBAM-Richtlinien für Ihr Betriebssystemlaufwerk verschieben können, nachdem das Laufwerk zunächst als nicht kompatibel erkannt wurde.</p>
<p>Nach Ablauf der konfigurierten Kulanzzeit können Benutzer die erforderliche Aktion nicht verschieben oder eine Ausnahme von ihr anfordern.</p>
<p>Wenn Benutzerinteraktionen erforderlich sind (wenn Sie beispielsweise das TPM (Trusted Platform Module) +-PIN verwenden oder einen Kennwortschutz verwenden), wird ein Dialogfeld angezeigt, und die Benutzer können es erst schließen, wenn Sie die erforderlichen Informationen bereitstellen. Wenn es sich bei dem Protector nur um ein TPM handelt, beginnt die Verschlüsselung sofort im Hintergrund ohne Benutzereingaben.</p>
<p>Benutzer können keine Ausnahmen über den BitLocker-Verschlüsselungs-Assistenten anfordern. Stattdessen müssen Sie sich an den Helpdesk wenden oder den von Ihrer Organisation verwendeten Prozess für Ausnahmeanforderungen verwenden.</p></td>
<td align="left"><p>Computerkonfigurations &gt; Richtlinien &gt; Administrative Vorlagen &gt; Windows Components &gt; MDOP MBAM (BitLocker-Verwaltungs-) &gt; Betriebs System Laufwerk</p></td>
</tr>
<tr class="even">
<td align="left"><p>Einstellungen für die Verschlüsselungsrichtlinien Erzwingung (feste Datenlaufwerke)</p></td>
<td align="left"><p>Verwenden Sie für diese Einstellung die Option <strong> Konfigurieren Sie die Anzahl der kulanztage für Nichtkonformität für Festplatten, </strong> um einen Kulanzzeitraum zu konfigurieren.</p>
<p>Der Kulanzzeitraum gibt an, wie viele Tage Endbenutzer die Einhaltung der MBAM-Richtlinien für ihr festes Laufwerk verschieben können, nachdem das Laufwerk zunächst als nicht kompatibel erkannt wurde.</p>
<p>Die Nachfrist beginnt, wenn das festgelegte Laufwerk als nicht kompatibel festgelegt wurde. Wenn Sie die automatische Sperrung verwenden, wird die Richtlinie erst erzwungen, wenn das Betriebssystemlaufwerk kompatibel ist. Wenn Sie die automatische Sperrung jedoch nicht verwenden, kann die Verschlüsselung des festen Datenlaufwerks beginnen, bevor das Betriebssystemlaufwerk vollständig verschlüsselt ist.</p>
<p>Nach Ablauf der konfigurierten Kulanzzeit können Benutzer die erforderliche Aktion nicht verschieben oder eine Ausnahme von ihr anfordern. Wenn Benutzerinteraktionen erforderlich sind, wird ein Dialogfeld angezeigt, und Benutzer können es erst dann schließen, wenn Sie die erforderlichen Informationen bereitstellen.</p></td>
<td align="left"><p>Computerkonfigurations &gt; Richtlinien &gt; Administrative Vorlagen &gt; Windows Components &gt; MDOP MBAM (BitLocker-Verwaltung) &gt; festes Laufwerk</p></td>
</tr>
</tbody>
</table>

 

### Möglichkeit zum Bereitstelleneiner URL im BitLocker-Laufwerk Verschlüsselungs-Assistenten, um auf Ihre Sicherheitsrichtlinie zu verweisen

Mit einer neuen Gruppenrichtlinieneinstellung, **die die URL für den Link "Sicherheitsrichtlinie" enthält**, können Sie eine URL konfigurieren, die Endbenutzern als Link " **Unternehmenssicherheitsrichtlinie**" angezeigt wird. Dieser Link wird angezeigt, wenn MBAM Benutzer zur Verschlüsselung eines Volumes auffordert.

Wenn Sie diese Richtlinieneinstellung aktivieren, können Sie die URL für den Link für die **Sicherheitsrichtlinie für Unternehmen** konfigurieren. Wenn Sie diese Richtlinieneinstellung deaktivieren oder nicht konfigurieren, wird der Link **Unternehmenssicherheitsrichtlinie** für die Benutzer nicht angezeigt.

Die neue Gruppenrichtlinieneinstellung befindet sich im folgenden GPO-Knoten: **Computerkonfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung) &gt; Client Verwaltung**.

### Unterstützung für FIPS-konforme Wiederherstellungsschlüssel

Mbam 2.5 unterstützt FIPS-konforme BitLocker-Wiederherstellungsschlüssel (Federal Information Processing Standard) auf Geräten, auf denen das BetriebssystemWindows 8.1 ausgeführt wird. Der Wiederherstellungsschlüssel war in früheren Versionen von Windows nicht FIPS-kompatibel. Diese Erweiterung verbessert den Wiederherstellungsprozess in Organisationen, die FIPS-Konformität erfordern, da Endbenutzer das Self-Service-Portal oder die Verwaltungs-und Überwachungs Website (Help Desk) verwenden können, um Ihre Laufwerke wiederherzustellen, wenn Sie Ihre PIN oder Ihr Kennwort vergessen oder aus ihren Computern ausgeschlossen werden. Das neue FIPS-Konformitäts Feature erstreckt sich nicht auf Kennwortschutz.

Um die FIPS-Konformität in Ihrer Organisation zu aktivieren, müssen Sie die FIPS-Gruppenrichtlinieneinstellungen (Federal Information Processing Standard) konfigurieren. Konfigurationsanweisungen finden Sie unter [BitLocker-Gruppenrichtlinieneinstellungen](https://go.microsoft.com/fwlink/?LinkId=393560).

Bei Clientcomputern, auf denen das Windows8-oder Windows7-Betriebssystem ohne den [installierten BitLocker-Hotfix](https://support.microsoft.com/kb/3015477)ausgeführt wird, verwenden IT-Administratoren weiterhin die Daten Wiederherstellungs-Agents (DRA) in FIPS-kompatiblen Umgebungen. Informationen zu DRA finden Sie unter [Verwenden von Daten Wiederherstellungs-Agents mit BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

Informationen zum herunterladen und Installieren des BitLocker-Hotfixes für Windows 7-und Windows 8-Computer finden Sie unter [Hotfix-Paket 2 für die BitLocker-Verwaltung und-Überwachung 2,5](https://support.microsoft.com/kb/3015477) .

### Unterstützung für Bereitstellungen mit höherer Verfügbarkeit

MBAM unterstützt die folgenden Szenarien mit hoher Verfügbarkeit zusätzlich zu den Standard Topologien für zwei Server und Configuration Manager-Integration:

-   Verfügbarkeitsgruppen für SQL Server-AlwaysOn

-   SQL Server-Clustering

-   Netzwerklastenausgleich (NLB)

-   SQL Server-Spiegelung

-   VSS-Sicherung (Volume Shadow Copy Service)

Weitere Informationen zu diesen Features finden Sie unter [Planen der MBAM 2,5-Höchstverfügbarkeit](planning-for-mbam-25-high-availability.md).

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a>Verwaltung von Rollen für die Verwaltung und Überwachung der Website geändert

In mbam 2.5 müssen Sie Sicherheitsgruppen in Active Directory-Domänendiensten (Adds) erstellen, um die Rollen zu verwalten, die Zugriffsrechte für die Website Verwaltung und Überwachung bereitstellen. Rollen ermöglichen Benutzern, die sich in bestimmten Sicherheitsgruppen befinden, verschiedene Aufgaben auf der Website auszuführen, wie etwa das Anzeigen von Berichten oder das unterstützen der Wiederherstellung verschlüsselter Laufwerke durch Endbenutzer. In früheren Versionen von MBAM wurden Rollen mithilfe lokaler Gruppen verwaltet.

In MBAM 2.5 ersetzt der Ausdruck "Rollen" den Ausdruck "Administratorrollen", der in früheren Versionen von MBAM verwendet wurde. Darüber hinaus wurde in MBAM 2.5 die Rolle "MBAM-System Administratoren" entfernt.

In der folgenden Tabelle sind die Sicherheitsgruppen aufgeführt, die Sie in AD DS erstellen müssen. Sie können einen beliebigen Namen für die Sicherheitsgruppen verwenden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Rolle</th>
<th align="left">Zugriffsrechte für diese Rolle auf der Website "Verwaltung und Überwachung"</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM Helpdesk-Benutzer</p></td>
<td align="left"><p>Bietet Zugriff auf die Bereiche Manage TPM und Drive Recovery der MBAM-Verwaltungs-und-Überwachungs Website. Benutzer, die auf diese Bereiche zugreifen können, müssen alle Felder ausfüllen, wenn Sie einen Bereich verwenden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM-Berichtsbenutzer</p></td>
<td align="left"><p>Bietet Zugriff auf die Berichte auf der Website Verwaltung und Überwachung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM Advanced Helpdesk-Benutzer</p></td>
<td align="left"><p>Bietet Zugriff auf alle Bereiche auf der Website Verwaltung und Überwachung. Benutzer in dieser Gruppe müssen nur den Wiederherstellungsschlüssel eingeben, nicht die Domäne und den Benutzernamen des Endbenutzers, wenn Sie den Endbenutzern helfen, Ihre Laufwerke wiederherzustellen. Wenn ein Benutzer ein Mitglied der Gruppe "MBAM Helpdesk-Benutzer" und der Gruppe "Erweiterte Helpdesk-Benutzer" von MBAM ist, überschreiben die Berechtigungen der Gruppe "Erweiterte Helpdesk-Benutzer" die Berechtigungen der Gruppe "MBAM Helpdesk-Benutzer".</p></td>
</tr>
</tbody>
</table>

 

Nachdem Sie die Sicherheitsgruppen in "hinzugefügt" erstellt haben, weisen Sie der entsprechenden Sicherheitsgruppe Benutzer und/oder Gruppen zu, um die entsprechende Zugriffsebene auf die Website Verwaltung und Überwachung zu ermöglichen. Damit Personen mit jeder Rolle auf die Verwaltungs-und Überwachungs Website zugreifen können, müssen Sie auch jede Sicherheitsgruppe angeben, wenn Sie die Verwaltungs-und Überwachungs Website konfigurieren.

### Windows PowerShell-Cmdlets zum Konfigurieren von MBAM-Server Features

Mit Windows PowerShell-Cmdlets für MBAM 2.5 können Sie die MBAM-Server Features konfigurieren und verwalten. Jedes Feature verfügt über ein entsprechendes Windows PowerShell-Cmdlet, das Sie zum Aktivieren oder Deaktivieren von Features oder zum Abrufen von Informationen über das Feature verwenden können.

Voraussetzungen und Voraussetzungen für die Verwendung von Windows PowerShell finden Sie unter [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

**So laden Sie die MBAM 2,5-Hilfe für Windows PowerShell-Cmdlets nach der Installation der MBAM-Server Software**

1.  Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).

2.  Geben Sie **Update-Help-Module Microsoft. MBAM**.

Die Windows PowerShell-Hilfe für MBAM ist in den folgenden Formaten verfügbar:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows PowerShell-Hilfeformat</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Geben Sie an einer Windows PowerShell-Eingabeaufforderung <strong> Get-Help- </strong> &lt; <em> Cmdlet ein.</em>&gt;</p></td>
<td align="left"><p>Wenn Sie die neuesten Windows PowerShell-Cmdlets hochladen möchten, befolgen Sie die Anweisungen im vorherigen Abschnitt zum Laden der Windows PowerShell-Hilfe für MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Auf TechNet als Webseiten</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Im Download Center als Word. docx-Datei</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Im Download Center als PDF-Datei</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### Unterstützung für reine ASCII-und erweiterte Pins sowie die Möglichkeit, sequenzielle und wiederholte Zeichen zu verhindern

**Erweiterte Pins für Startgruppen Richtlinieneinstellung zulassen**

Die Gruppenrichtlinieneinstellung " **Erweiterte Pins für den Start zulassen**" ermöglicht es Ihnen, zu konfigurieren, ob erweiterte Start Pins für BitLocker verwendet werden. Erweiterte Start Pins ermöglichen Benutzern die Eingabe von Schlüsseln auf einer vollständigen Tastatur, einschließlich Groß-und Kleinbuchstaben, Symbolen, Zahlen und Leerzeichen. Wenn Sie diese Richtlinieneinstellung aktivieren, werden alle neuen BitLocker-startpins, die festgelegt sind, mit erweiterten Pins ergänzt. Wenn Sie diese Richtlinieneinstellung deaktivieren oder nicht konfigurieren, können erweiterte Pins nicht verwendet werden.

Nicht alle Computer unterstützen den Eintrag verbesserter Pins in der Pre-Boot Execution Environment (PXE). Bevor Sie diese Gruppenrichtlinieneinstellung für Ihre Organisation aktivieren, führen Sie während des BitLocker-Setupvorgangs eine Systemüberprüfung durch, um sicherzustellen, dass das BIOS des Computers die Verwendung der vollständigen Tastatur in PXE unterstützt. Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppenrichtlinienanforderungen](planning-for-mbam-25-group-policy-requirements.md).

**Kontrollkästchen nur ASCII-Pins erforderlich**

Die Gruppenrichtlinieneinstellung **Erweiterte Pins für Start zulassen** enthält auch das Kontrollkästchen **nur ASCII-Pins erforderlich** . Wenn die Computer in Ihrer Organisation die Verwendung der Volltastatur in PXE nicht unterstützen, können Sie die Gruppenrichtlinieneinstellung **Erweiterte Pins für Start zulassen** aktivieren, und aktivieren Sie dann das Kontrollkästchen **nur-ASCII-Pins anfordern** , um zu erzwingen, dass für erweiterte Pins nur druckbare ASCII-Zeichen verwendet werden.

**Erzwungene Verwendung von nicht sequenziellen und nicht wiederholenden Zeichen**

Mbam 2.5 verhindert, dass Endbenutzer Pins erstellen, die aus wiederholenden Zahlen (wie 1111) oder sequenziellen Zahlen (wie 1234) bestehen. Wenn Endbenutzer versuchen, ein Kennwort einzugeben, das drei oder mehr Wiederholungs-oder fortlaufende Nummern enthält, zeigt der BitLocker-Laufwerk Verschlüsselungs-Assistent eine Fehlermeldung an und verhindert, dass Benutzer eine PIN mit den verbotenen Zeichen eingeben.

### Hinzufügen des DRA-Zertifikats zum BitLocker-Computer Kompatibilitätsbericht

Ein neuer Protector-Typ, das DRA-Zertifikat (Data Recovery Agent), wurde dem BitLocker-Computer Kompatibilitätsbericht in Configuration Manager hinzugefügt. Dieser Protector-Typ gilt für Betriebssystemlaufwerke und wird in der Spalte " **Protector-Typen** " im Abschnitt " **Computer Lautstärke (n)** " angezeigt.

### Unterstützung für Multi-Forest-Support Bereitstellungen

MBAM 2,5 unterstützt die folgenden Typen von Bereitstellungen mit mehreren Gesamtstrukturen:

-   Einzelne Gesamtstruktur mit einer einzelnen Domäne

-   Einzelne Gesamtstruktur mit einer einzelnen Struktur und mehreren Domänen

-   Einzelne Gesamtstruktur mit mehreren Strukturen und nicht zusammengefügten Namespaces

-   Mehrere Gesamtstrukturen in einer zentralen Gesamtstrukturtopologie

-   Mehrere Gesamtstrukturen in einer Ressourcengesamtstruktur-Topologie

Es gibt keine Unterstützung für die Gesamtstruktur Migration (von einer einzelnen zu mehreren, von mehreren zu einer, zu einer Ressource in der gesamten Gesamtstruktur usw.) oder zum Upgrade oder Downgrade.

Die Voraussetzungen für die Bereitstellung von MBAM in Multi-Forest-Bereitstellungen sind:

-   Die Gesamtstruktur muss unter unterstützten Versionen von Windows Server ausgeführt werden.

-   Eine bidirektionale oder unidirektionale Vertrauensstellung ist erforderlich. Unidirektionale Vertrauensstellungen setzen voraus, dass die Domäne des Servers der Domäne des Clients vertraut. Anders ausgedrückt: die Domäne des Servers verweist auf die Domäne des Clients.

### MBAM-Client Unterstützung für verschlüsselte Festplatten

MBAM unterstützt BitLocker auf verschlüsselten Festplatten, die die TCG-Spezifikationsanforderungen für Opal-und IEEE-1667-Standards erfüllen. Wenn BitLocker auf diesen Geräten aktiviert ist, generiert es Schlüssel und führt Verwaltungsfunktionen auf dem verschlüsselten Laufwerk aus. Weitere Informationen finden Sie unter [verschlüsselte Festplatte](https://technet.microsoft.com/library/hh831627.aspx) .

## So erhalten Sie MDOP-Technologien


MBAM ist ein Bestandteil des Microsoft-Desktop Optimierungs Pakets (MDOP). MDOP ist Teil des Microsoft Software Assurance-Programms. Weitere Informationen zum Microsoft Software Assurance-Programm und zum Erwerb der MDOP finden Sie unter [wie erhalte ich MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## <a href="" id="---------mbam-2-5-release-notes"></a> MBAM 2,5-Versionshinweise


Weitere Informationen und aktuelle Neuigkeiten, die nicht in dieser Dokumentation enthalten sind, finden Sie unter [Versionshinweise zu MBAM 2,5](release-notes-for-mbam-25.md).

## Sie haben einen Vorschlag für MBAM?
- Senden Sie [uns](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub)Ihr Feedback. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Verwandte Themen


[Microsoft BitLocker Administration and Monitoring 2.5](index.md)

[Erste Schritte mit MBAM 2.5](getting-started-with-mbam-25.md)

 

 





