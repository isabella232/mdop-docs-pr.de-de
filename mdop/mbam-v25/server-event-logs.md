---
title: Serverereignisprotokolle
description: Serverereignisprotokolle
author: dansimp
ms.assetid: 04e724d2-28cc-4fa8-86a1-0d4ab0234b11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 269e9b4bc2644fae4dc5796652c7587bb0ef6076
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809922"
---
# Serverereignisprotokolle


Die Tabellen in diesem Abschnitt enthalten Informationen zu den Ereignis-IDs des MBAM-Server Protokolls.

## Konfiguration


Die folgende Tabelle enthält Nachrichten und Informationen zur Problembehandlung für Ereignis-IDs, die während der Konfiguration auf dem MBAM-Server auftreten können.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ereignis-ID</th>
<th align="left">Source</th>
<th align="left">Ereignissymbol</th>
<th align="left">Meldung</th>
<th align="left">Problembehandlung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>VssRegistrationException</p></td>
<td align="left"><p>Während der VSS-Registrierung wurde eine Ausnahme ausgelöst.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>VssDeregistrationException</p></td>
<td align="left"><p>Während der VSS-Deregistrierung wurde eine Ausnahme ausgelöst.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>300</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CmdletError</p></td>
<td align="left"><p>Fehler beim Entfernen des Ordners.</p></td>
<td align="left"><p>Gibt an, dass beim Ausführen einer Aufgabe ein Abbruchfehler aufgetreten ist. Überprüfen Sie andere Ereignismeldungen im Protokoll, um das MBAM-Setup weiter zu diagnostizieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>301</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>cmdletUnexpectedError</p></td>
<td align="left"><p>Unerwarteter Cmdlet-Fehler.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>302</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CmdletWarning</p></td>
<td align="left"><p>Cmdlet-Warnung.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>303</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>CmdletInformation</p></td>
<td align="left"><p>Cmdlet-Informationen.</p></td>
<td align="left"><p>Nur Informationsdaten; keine Problembehandlung erforderlich. Das Ereignis zeigt an, dass eine Aufgabe durch die Cmdlets wie enabling\disabling eines Features oder Abbrechen eines Vorgangs erfolgt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>400</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ConfiguratorError</p></td>
<td align="left"><p>Konfigurator-Fehler.</p></td>
<td align="left"><p>Gibt an, dass beim Starten des MBAM-Konfigurators ein Fehler aufgetreten ist. Stellen Sie sicher, dass der Benutzer über die erforderlichen Berechtigungen zum Starten des MBAM-Konfigurators verfügt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>401</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ConfiguratorUnexpectedError</p></td>
<td align="left"><p>Unerwarteter Konfigurator-Fehler.</p></td>
<td align="left"><p>Gibt an, dass beim Ausführen einer MBAM-Konfigurationsaufgabe ein Abbruchfehler aufgetreten ist. Die Fehlermeldung enthält weitere Details zum Fehler. Überprüfen Sie andere Fehlermeldungen im Ereignisprotokoll, um das MBAM-Setup weiter zu diagnostizieren. Bekannte Fehler sind:</p>
<ul>
<li><p>Fehler beim Abrufen oder Überprüfen eines vom Benutzer ausgewählten Zertifikats</p></li>
<li><p>Fehler beim Analysieren der Berichts-URL</p></li>
<li><p>Fehler beim Öffnen von Ereignisprotokollen für den Benutzer</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>402</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ConfiguratorWarning</p></td>
<td align="left"><p>Konfigurator-Warnung.</p></td>
<td align="left"><p>Gibt an, dass eine MBAM-Konfigurationsaufgabe nicht wie erwartet abgeschlossen ist, aber nicht vollständig fehlschlägt. Zu den bekannten Aufgaben gehören fehlendes Zertifikat im Speicher LocalMachine\MY-Store, das im Webanwendungs Feature konfiguriert wurde, oder ein Timeout für eine ausstehende Aufgabe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>410</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>ConfiguratorInformation</p></td>
<td align="left"><p>Informationen zum Konfigurator.</p></td>
<td align="left"><p>Nur Informationsdaten; keine Problembehandlung erforderlich. Das Ereignis zeigt an, dass eine Aufgabe vom MBAM-Konfigurator aufgerufen wird. Bekannte Aufgaben sind unter anderem:</p>
<ul>
<li><p>Starten des Konfigurators</p></li>
<li><p>Überprüfen der Softwarevoraussetzungen für ein MBAM-Feature</p></li>
<li><p>Überprüfen von Parametern für ein MBAM-Feature</p></li>
<li><p>Enabling\disabling\committing eines MBAM-Features</p></li>
<li><p>Generieren eines PowerShell-Skripts aus der Konfiguration</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>500</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>WebProviderUnexpectedError</p></td>
<td align="left"><p>Unerwarteter Fehler des Webanwendungs Anbieters.</p></td>
<td align="left"><p>Gibt an, dass beim Aktivieren und Konfigurieren einer MBAM-Website oder eines Webdiensts in IIS ein Fehler aufgetreten ist. Bekannte Fehler sind:</p>
<ul>
<li><p>Fehler beim Auffinden des IIS www-Stammordners</p></li>
<li><p>Fehler beim Zugriff auf die IIS-Konfiguration in web.config aufgrund fehlerhafter Dateien oder fehlender Einstellungen</p></li>
<li><p>Fehler beim Erstellen oder Entfernen einer Webanwendung</p></li>
<li><p>IIS-Zugriffsverletzung</p></li>
</ul>
<p>Dieser Fehler wird auch protokolliert, wenn MBAM nicht auf Active Directory (AD) zugreifen kann, um Benutzerkonten zu überprüfen. Überprüfen Sie, ob IIS installiert, ordnungsgemäß konfiguriert und der IIS-Dienst ausgeführt wird. Überprüfen Sie, ob alle MBAM-Software Voraussetzungsprüfungen erfolgreich sind. Überprüfen Sie, ob der Benutzer über die richtigen Berechtigungen zum Erstellen von Webanwendungen auf der IIS-Instanz verfügt. Überprüfen Sie, ob der Benutzer Zugriff auf Benutzerkonto Objekte in AD hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p>501</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>WebProviderError</p></td>
<td align="left"><p>Unerwarteter Fehler des Webanwendungs Anbieters.</p></td>
<td align="left"><p>Gibt an, dass bei der Aktivierung, Deaktivierung oder Konfiguration einer MBAM-Website oder eines Webdiensts in IIS ein Fehler aufgetreten ist. Bekannte Fehler sind:</p>
<ul>
<li><p>Fehler beim Lesen von grundlegenden oder WSHttp Bindungsinformationen aus IIS</p></li>
<li><p>Fehlender Identitätsabschnitt oder DNS-Eintrag im Abschnitt "Identität" in IIS-Konfigurationsdateien</p></li>
<li><p>Fehler beim Öffnen des Registrierungsschlüssels HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>Fehler beim Lesen des Werts PathWWWRoot aus dem Registrierungsschlüssel HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>Der Benutzer versucht, einen virtuellen Verzeichnisnamen mit einem reservierten Namen für MBAM anzugeben.</p></li>
</ul>
<p>Überprüfen Sie, ob IIS installiert und ordnungsgemäß konfiguriert ist. Überprüfen Sie, ob der Registrierungsschlüssel HKLM\SOFTWARE\Microsoft\InetStp: PathWWWRoot vorhanden und barrierefrei ist. Überprüfen Sie, ob die Bindungsinformationen in IIS nicht beschädigt sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>502</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>WebProviderWarning</p></td>
<td align="left"><p>Warnung des Webanwendungs Anbieters.</p></td>
<td align="left"><p>Gibt an, dass beim Aktivieren einer MBAM-Website oder eines Webdiensts ein nicht Abbruchfehler aufgetreten ist. Bekannte Fehler sind:</p>
<ul>
<li><p>Fehler beim Zugriff auf AD zur Überprüfung des Dienstprinzipalnamens (SPN) im App-Pool Konto</p></li>
<li><p>Fehler bei der Überprüfung des SPN, da er mehreren Konten in AD zugewiesen ist</p></li>
<li><p>Fehler beim Registrieren eines SPN für das App-Pool-Konto in AD</p></li>
<li><p>SPN ist in einem anderen Konto als dem App-Pool in AD registriert.</p></li>
<li><p>Fehler beim Entfernen von SPN aus dem App-Pool-Konto in AD während eines Rollback-Vorgangs</p></li>
<li><p>Fehler beim Überprüfen, ob der IIS_IUSRS Gruppe die Berechtigung "als Batch anmelden" auf dem IIS-Server gewährt wurde</p></li>
</ul>
<p>Die Ereignismeldung enthält weitere Informationen zu dem jeweiligen Fehler. Überprüfen Sie, ob AD von dem Server erreichbar ist, auf dem MBAM Setup ausgeführt wird. Überprüfen Sie, ob der Benutzer, der das MBAM-Setup ausführt, über Leseberechtigungen für das App-Pool Konto in AD verfügt. Wenn ein SPN bereits im App-Pool Konto in AD registriert ist, stellen Sie sicher, dass er nicht für andere Konten registriert ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>503</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>WebProviderInformation</p></td>
<td align="left"><p>Informationen zum Anbieter von Webanwendungen. Beschreibung</p></td>
<td align="left"><p>Nur Informationsdaten; keine Problembehandlung erforderlich. Das Ereignis zeigt an, dass eine Aufgabe vom MBAM-Setup aufgerufen wird. Zu den bekannten Aufgaben zählen das Abrufen der IIS-Konfiguration wie Bindungsinformationen und Stammwebsite sowie das Konfigurieren des Dienstprinzipalnamens (SPN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>600</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupUnexpectedError</p></td>
<td align="left"><p>Unerwarteter Setup-Fehler.</p></td>
<td align="left"><p>Gibt an, dass ein Abbruchfehler beim enabling\disabling oder Konfigurieren eines MBAM-Features aufgetreten ist. Bekannte Fehler sind:</p>
<ul>
<li><p>Fehler beim Rollback einer Aufgabe nach einem Fehler</p></li>
<li><p>Fehler beim Lesen aus der Registrierung</p></li>
<li><p>Fehler beim Erstellen oder Löschen eines Ordners im Dateisystem</p></li>
<li><p>Fehler beim Lesen der SQL-Versionsinformationen</p></li>
<li><p>Fehler beim Registrieren von VSS Writer in SQL</p></li>
</ul>
<p>Die Ereignismeldung enthält weitere Informationen zu dem jeweiligen Fehler. Überprüfen Sie, ob alle MBAM-Software Voraussetzungs Überprüfungen bestehen. Stellen Sie sicher, dass der Registrierungspfad MBAM, falls vorhanden, HKEY_LOCAL_MACHINE \software\microsoft\mbam-Server und alle Unterschlüssel lesbar sind. Überprüfen Sie, ob AD von dem Server erreichbar ist, auf dem MBAM Setup ausgeführt wird. Überprüfen Sie, ob der Benutzer, der das MBAM-Setup ausführt, über Leseberechtigungen in AD verfügt.</p>
<p>Wenn Sie eine erfolgreiche VSS-Writer-Registrierung durchführen möchten, stellen Sie sicher, dass eine unterstützte Version von SQL installiert ist und für den Benutzer, der das MBAM-Setup ausführt, eine Instanz verfügbar ist. Wenn Sie ein MBAM-Feature deaktivieren oder MBAM deinstallieren, stellen Sie sicher, dass alle Dateien wie Protokolldateien und web.config Dateien geschlossen sind, damit MBAM ihre Websites und Webdienste entfernen kann.</p></td>
</tr>
<tr class="even">
<td align="left"><p>601</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupError</p></td>
<td align="left"><p>Setup-Fehler.</p></td>
<td align="left"><p>Gibt an, dass ein Abbruchfehler beim enabling\disabling oder Konfigurieren eines MBAM-Features aufgetreten ist. Bekannte Fehler sind:</p>
<ul>
<li><p>Fehler beim Lesen der MBAM-Konfiguration in IIS</p></li>
<li><p>Abschnitt "korrupter appSettings" in IIS-Konfiguration oder falsch konfigurierten Einstellungen</p></li>
<li><p>Fehler beim Überprüfen des Hostnamens</p></li>
<li><p>Fehler beim Lesen der SQL-Versionsinformationen</p></li>
<li><p>Fehler beim Registrieren von VSS Writer in SQL</p></li>
</ul>
<p>Die Ereignismeldung enthält weitere Informationen zu dem jeweiligen Fehler. Überprüfen Sie, ob IIS installiert und ordnungsgemäß konfiguriert ist. Überprüfen Sie, ob alle MBAM-Software Voraussetzungs Überprüfungen bestehen. Wenn Sie eine erfolgreiche VSS-Writer-Registrierung durchführen möchten, stellen Sie sicher, dass eine unterstützte Version von SQL installiert ist und für den Benutzer, der das MBAM-Setup ausführt, eine Instanz verfügbar ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>602</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupWarning</p></td>
<td align="left"><p>Setup Warnung.</p></td>
<td align="left"><p>Gibt an, dass beim enabling\disabling oder Konfigurieren eines MBAM-Features wie Configuration Manager (cm)-Integration oder MBAM-Webanwendung ein nicht Abbruchfehler aufgetreten ist. Bekannte Fehler sind: Fehler beim Löschen von MBAM-Berichten aus dem SRS-Rollen Punkt im cm und Fehler beim Auflösen eines Hostnamens vom Domänencontroller. Die Ereignismeldung enthält weitere Informationen zu dem jeweiligen Fehler.</p>
<p>Überprüfen Sie, ob AD von dem Server erreichbar ist, auf dem MBAM Setup ausgeführt wird. Überprüfen Sie, ob der Benutzer, der das MBAM-Setup ausführt, Berechtigungen für die SSRS-Instanz entfernt hat, die als SRS-Rollen Punkt in cm konfiguriert ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>603</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>SetupInformation</p></td>
<td align="left"><p>Einrichtungsinformationen.</p></td>
<td align="left"><p>Nur Informationsdaten; keine Problembehandlung erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>605</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>WebProviderSoftwareCheckFailure</p></td>
<td align="left"><p>Die Webanwendung kann nicht aktiviert werden, da eine oder mehrere Softwareabhängigkeiten nicht erfüllt werden.</p></td>
<td align="left"><p>Während der Installation von MBAM Web Site/Web Service überprüft MBAM Setup, ob die erforderlichen Voraussetzungen vorhanden sind. Diese Meldung weist darauf hin, dass MBAM die angeforderte Website/den Webdienst nicht installieren konnte, da die erforderliche Voraussetzung fehlt. Weitere Informationen zu fehlenden Voraussetzungen finden Sie unter Fehlermeldungen vor dieser Nachricht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>606</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupParameterValidationFailure</p></td>
<td align="left"><p>Der Parameter, der zum Aktivieren des Server Features erforderlich ist, wurde entweder nicht angegeben oder hat die Validierung nicht übergeben.</p></td>
<td align="left"><p>Gibt an, dass der Parameter, der zum Konfigurieren eines MBAM-Features erforderlich ist, entweder nicht angegeben wurde oder die Validierung nicht erfolgreich war.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>607</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupParameterValidationFailureWithError</p></td>
<td align="left"><p>Beim Versuch, angegebenen Parameter zu überprüfen, der zum Aktivieren des Server Features erforderlich ist, ist ein Fehler aufgetreten.</p></td>
<td align="left"><p>Gibt an, dass beim Versuch, den angegebenen Parameter zu überprüfen, der zum Aktivieren des Server Features erforderlich ist, ein Fehler aufgetreten ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>700</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderUnexpectedError</p></td>
<td align="left"><p>Unerwarteter Fehler des DB-Anbieters.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>701</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderError</p></td>
<td align="left"><p>DB-Anbieterfehler.</p></td>
<td align="left"><p>Die im Abschnitt EventDetails enthaltene Nachricht sollte weitere Informationen zum tatsächlichen Fehler bereitstellen. Dies sind einige der zu überprüfenden Bereiche:</p>
<ul>
<li><p>MBAM-Setup konnte keine Verbindung mit der Datenbank herstellen, wobei die angegebenen Verbindungsinformationen verwendet wurden. Überprüfen Sie die Verbindungszeichen folgen Details, die MBAM-Setup bereitgestellt wird.</p></li>
<li><p>MBAM Setup konnte keine Verbindung mit der angegebenen Datenbank unter Verwendung der angegebenen Domänenkonto Anmeldeinformationen herstellen. Überprüfen Sie, ob der Benutzername und das Kennwort des Domänenkontos gültig sind.</p></li>
<li><p>MBAM Setup konnte keine Verbindung mit der angegebenen Datenbank unter Verwendung der angegebenen Domänenkonto Anmeldeinformationen herstellen. Überprüfen Sie, ob das bereitgestellte Domänenkonto über die erforderlichen Berechtigungen zum Herstellen einer Verbindung mit der MBAM-Datenbank verfügt.</p></li>
<li><p>MBAM DAC PAC schlägt fehl, wenn eine neuere Version der MBAM-Datenbank bereits installiert ist. Stellen Sie sicher, dass auf dem angegebenen SQL Server keine neue Version von MBAM DBS vorhanden ist.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>702</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderWarning</p></td>
<td align="left"><p>Warnung des DB-Anbieters.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>703</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>DbProviderInformation</p></td>
<td align="left"><p>Informationen zum DB-Anbieter.</p></td>
<td align="left"><p>Nur Informationsdaten; keine Problembehandlung erforderlich.</p></td>
</tr>
<tr class="even">
<td align="left"><p>704</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderDacError</p></td>
<td align="left"><p>Beim Bereitstellen der Datenebenen-Anwendung ist ein Fehler aufgetreten.</p></td>
<td align="left"><p>MBAM Pakete Ihre Datenbanken als Datenebenen-Anwendungen und versucht, Sie mit Microsoft. SqlServer. DAC. DacServices zu registrieren. Die Fehlermeldung im Kontext wird vom DAC-Dienst gemeldet. Das Ereignis sollte detaillierte Informationen zu den Ursachen enthalten. Lesen Sie die Informationen in der Fehlermeldung, um das Problem zu beheben und zu beheben.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>705</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderDacWarning</p></td>
<td align="left"><p>Beim Bereitstellen der Datenebenen-Anwendung ist eine Warnung aufgetreten.</p></td>
<td align="left"><p>MBAM Pakete Ihre Datenbanken als Datenebene-Anwendung und versucht, Sie mit Microsoft. SqlServer. DAC. DacServices zu registrieren. Die Warnmeldung im Kontext wird vom DAC-Dienst gemeldet. Das Ereignis sollte detaillierte Informationen zu den Ursachen enthalten. Lesen Sie die Informationen in der Warnmeldung, um das Problem zu beheben und zu beheben.</p></td>
</tr>
<tr class="even">
<td align="left"><p>706</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>DbProviderDacInformation</p></td>
<td align="left"><p>Beim Bereitstellen der Datenebenen-Anwendung wurde eine Nachricht ausgelöst.</p></td>
<td align="left"><p>Nur Informationsdaten; keine Problembehandlung erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>800</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ReportProviderUnexpectedError</p></td>
<td align="left"><p>Unerwarteter Fehler des Berichts Anbieters.</p></td>
<td align="left"><p>Unerwarteter Fehler des Berichts Anbieters. Beschreibung {exceptionDetails} Dies sind einige der möglichen Ausnahmedetails:</p>
<p><strong>Beim Abrufen des Namens des Verzeichnisses ist ein Fehler aufgetreten &#39; {DirectoryName} &#39;</strong></p>
<p><strong>Beim Abrufen von Dateien für das Verzeichnis &#39; {DirectoryName} ist eine Ausnahme aufgetreten &#39;</strong></p>
<p><strong>Beim Auflisten von Verzeichnissen im Verzeichnis &#39; {DirectoryName} ist eine Ausnahme aufgetreten &#39;</strong></p>
<p><strong>Beim Lesen aller Bytes für Datei &#39; {filename} ist eine Ausnahme aufgetreten &#39;</strong></p>
<p>Während der MBAM-Installation entpackt MBAM Setup alle Berichtsdateien in den angegebenen Installationspfad. Im Rahmen der Berichts Installation versucht das Installationsmodul, auf die entpackten Berichtsdateien im Installationspfad zuzugreifen und mit SQL Reporting Services zu kommunizieren, um die Berichtsdateien zu veröffentlichen. Die obigen Fehler treten auf, wenn MBAM nicht auf die Dateien/Ordner im entpackten Installationspfad zugreifen kann. Hier sind einige Tipps zur Behebung dieses Problems:</p>
<ul>
<li><p>Überprüfen Sie, ob MBAM installiert ist.</p></li>
<li><p>Überprüfen Sie, ob der Registrierungsschlüssel HKEY_LOCAL_MACHINE \software\microsoft\mbam Server\InstallationPath vorhanden ist und für den ausführenden Benutzer barrierefrei ist.</p></li>
<li><p>Überprüfen Sie, ob der Pfad zu Berichtsdateien unter MBAM Installationspfad 248 Zeichen nicht überschreitet.</p></li>
<li><p>Überprüfen Sie, ob der MBAM-Setup Ordner oder die Dateien, die in MBAM-Installationspfad enthalten sind, seit der Installation nicht geändert wurden.</p></li>
<li><p>Überprüfen Sie, ob der Benutzer, der das Setup ausführt, autorisiert ist, den MBAM-Installationsordner zu lesen.</p></li>
</ul>
<p><strong>Die Reporting Services-Konnektivität ist fehlgeschlagen. {exceptionDetails}</strong></p>
<p>Während der Installation von MBAM-Berichten versucht Module, mit SSRS-Webdiensten zu kommunizieren, um Ordner zu erstellen und Berichte zu veröffentlichen. Die obige Meldung zeigt an, dass MBAM keine SSRS-Webdienste finden oder mit Ihnen kommunizieren konnte. Hier sind einige Tipps zur Behebung dieses Problems:</p>
<ul>
<li><p>Überprüfen Sie, ob SSRS auf dem angegebenen Computer installiert ist.</p></li>
<li><p>Überprüfen Sie mithilfe der SSRS-Konsole, ob SSRS aktiviert ist und ausgeführt wird.</p></li>
<li><p>Überprüfen Sie, ob der Benutzer, der das Setup ausführt, für den Zugriff auf SSRS autorisiert ist.</p></li>
</ul>
<p><strong>Fehler beim Entfernen der MBAM-Berichte unter Verwendung der Reporting Services-Instanz-URL &#39; {SSRSInstanceUrl} &#39;. Stellen Sie sicher, dass die für MBAM-Berichte erforderliche SSRS-Instanz ausgeführt und ordnungsgemäß konfiguriert ist.</strong></p>
<p>Wenn die MBAM-Installation fehlschlägt oder wenn der Benutzer MBAM-Berichterstellungsfeatures deaktiviert, entfernt das Setupmodul SSRS-Berichte. Die obige Meldung zeigt an, dass MBAM keine SSRS-Berichte entfernt hat. Hier sind einige Tipps zur Behebung dieses Problems:</p>
<ul>
<li><p>Überprüfen Sie, ob SSRS auf dem angegebenen Computer installiert ist.</p></li>
<li><p>Überprüfen Sie mithilfe der SSRS-Konsole, ob SSRS aktiviert ist und ausgeführt wird.</p></li>
<li><p>Überprüfen Sie, ob der Benutzer, der das Setup ausführt, für den Zugriff auf SSRS autorisiert ist.</p></li>
</ul>
<p><strong>Beim Veröffentlichen von Berichten ist ein Fehler aufgetreten. {exceptionDetails}.</strong></p>
<p>Während der Installation von MBAM-Berichten versucht Module, mit SSRS-Webdiensten zu kommunizieren, um Ordner zu erstellen und Berichte zu veröffentlichen. Die obige Meldung weist darauf hin, dass der SSRS-Webdienst beim Veröffentlichen von Berichten gemeldet und eine Ausnahme ausgelöst hat. Hier sind einige Tipps zur Behebung dieses Problems:</p>
<ul>
<li><p>Überprüfen Sie mithilfe der SSRS-Konsole, ob SSRS aktiviert ist und ausgeführt wird.</p></li>
<li><p>Überprüfen Sie, ob der Benutzer, der das Setup ausführt, autorisiert ist, auf Berichte in SSRS zuzugreifen/zu veröffentlichen.</p></li>
</ul>
<p><strong>Eine Richtlinie für den Gruppenbenutzernamen &#39; {username} &#39; bereits vorhanden ist. Falls dies nicht korrekt ist, überarbeiten Sie den Berichterstellungsdienst manuell auf doppelte oder ungültige Richtlinien.</strong></p>
<p>Nach dem Veröffentlichen von MBAM-Berichten versucht MBAM Setup, eine MBAM-Berichtsbenutzer Rolle zu erstellen (sofern Sie nicht bereits vorhanden ist), und legt die entsprechende Benutzerrichtlinie fest. Der obige Fehler weist darauf hin, dass der SSRS-Webdienst beim Einrichten der Benutzerrollen Richtlinie für Berichte eine Ausnahme ausgelöst hat. Befolgen Sie die Anweisungen in der Ereignismeldung, und verweisen Sie auf &quot; <a href="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;ProdVer=8.00&amp;EvtID=rsInvalidPolicyDefinition&amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;LCID=1033&amp;quot" data-raw-source="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;amp;ProdVer=8.00&amp;amp;EvtID=rsInvalidPolicyDefinition&amp;amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;amp;LCID=1033&amp;quot"> https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp ; ProdVer = 8,00 &amp; EvtID = rsInvalidPolicyDefinition &amp; EvtSrc = Microsoft. ReportingServices. Diagnostics. ErrorStrings. resources. Strings &amp; LCID = 1033&quot </a> ; für weitere Hilfe.</p>
<p><strong>Beim Überprüfen des Zugriffs auf SSRS {exceptionDetails} ist ein Fehler aufgetreten.</strong></p>
<p>Im Rahmen der Voraussetzungen Überprüfung überprüft MBAM-Setup, ob der Benutzer über die erforderlichen Berechtigungen zum Zugriff auf/Erstellen des Ordners unter SSRS verfügt. Die Fehlermeldung weist darauf hin, dass bei der Überprüfung des Zugriffs auf SSRS eine Ausnahme aufgetreten ist. Hinweise zum Debuggen finden Sie in den Ausnahmedetails.</p>
<p><strong>Beim Überprüfen der SSRS-URL ist ein SOAP-Fehler aufgetreten. {exceptionDetails}</strong></p>
<p><strong>Beim Überprüfen der SSRS-URL ist ein Webfehler aufgetreten. {exceptionDetails}</strong></p>
<p><strong>Beim Überprüfen der SSRS-URL ist ein HTTP/HTTPS-Fehler aufgetreten. {exceptionDetails}</strong></p>
<p><strong>Beim Überprüfen der SSRS-URL ist ein Fehler aufgetreten. {exceptionDetails}</strong></p>
<p>Im Rahmen der Voraussetzungsprüfung ruft MBAM Setup URLs ab, die der angegebenen SSRS-Instanz zugeordnet sind, und versucht, mit dem SSRS-Webdienst zu kommunizieren. Die obige Fehlermeldung weist darauf hin, dass der SSRS-Webdienst bei der angegebenen URL eine Ausnahme ausgelöst hat, weitere Informationen finden Sie unter Ausnahmedetails. Dies sind einige Tipps zum Beheben von Problemen mit der SSRS-Kommunikation.</p>
<ul>
<li><p>Überprüfen Sie, ob SSRS auf dem angegebenen Computer installiert ist.</p></li>
<li><p>Überprüfen Sie mithilfe der SSRS-Konsole, ob SSRS aktiviert ist und ausgeführt wird.</p></li>
<li><p>Überprüfen Sie, ob der Benutzer, der das Setup ausführt, für den Zugriff auf SSRS autorisiert ist.</p></li>
</ul>
<p><strong>Beim Abrufen der SSRS-Version ist ein Fehler aufgetreten. {exceptionDetails}</strong></p>
<p>Im Rahmen der Voraussetzungsprüfung fragt MBAM Setup WMI ab, um die Versionsnummer abzurufen, die der angegebenen SSRS-Instanz zugeordnet ist. Die obige Fehlermeldung weist darauf hin, dass beim Abfragen von WMI eine Ausnahme aufgetreten ist. Weitere Informationen finden Sie unter exceptionDetails. Dies sind einige Prüfungen, die Sie ausführen können:</p>
<ul>
<li><p>Überprüfen Sie, ob SSRS mit dem angegebenen Instanznamen auf dem angegebenen Computer installiert ist.</p></li>
<li><p>Überprüfen Sie mithilfe der SSRS-Konsole, ob SSRS aktiviert ist und ausgeführt wird.</p></li>
<li><p>Überprüfen Sie, ob der Benutzer, der das Setup ausführt, zur Abfrage der SSRS-Klasse unter WMI-Namespace autorisiert ist.</p></li>
</ul>
<p><strong>Der aktuelle Benutzer ist nicht berechtigt, auf den WMI-Namespace &#39; {ssrsWMINamespace} &#39; zuzugreifen.</strong></p>
<p><strong>Beim Aufzählen des Namespace &#39; {ssrsWMINamespace} &#39; ist ein Fehler aufgetreten. Der RPC-Server für SSRS-WMI-Anbieter auf dem lokalen Host wurde nicht gefunden.</strong></p>
<p><strong>Beim Aufzählen des Namespace &#39; {ssrsNamespace} &#39; ist ein Fehler aufgetreten. Es konnte keine Instanz von SSRS auf dem lokalen Host gefunden werden.</strong></p>
<p><strong>Beim Zugriff auf WMI ist ein Fehler aufgetreten. RPC-Server zum Beispiel &#39; {ssrsInstance} &#39; wurde nicht gefunden.</strong></p>
<p><strong>Beim Zugriff auf WMI ist ein Fehler aufgetreten. Der Instanzname &#39; {ssrsInstanceName} &#39; ist nicht korrekt.</strong></p>
<p><strong>Beim Zugriff auf WMI ist ein Fehler aufgetreten. Instanz &#39; {ssrsInstanceName} &#39; auf dem lokalen Host konnte nicht gefunden werden.</strong></p>
<p>Im Rahmen der Voraussetzungsprüfung fragt MBAM Setup WMI ab, um den WMI-Namespace abzurufen, der einer bestimmten Instanz zugeordnet ist. Die obige Fehlermeldung weist darauf hin, dass bei der Abfrage von WMI eine Ausnahme aufgetreten ist. Weitere Informationen finden Sie unter exceptionDetails. Dies sind einige Prüfungen, die Sie ausführen können:</p>
<ul>
<li><p>Überprüfen Sie, ob SSRS mit dem angegebenen Instanznamen auf dem angegebenen Computer installiert ist.</p></li>
<li><p>Überprüfen Sie mithilfe der SSRS-Konsole, ob SSRS aktiviert ist und ausgeführt wird.</p></li>
<li><p>Überprüfen Sie, ob der Benutzer, der das Setup ausführt, für den Zugriff auf/Abfrage der SSRS-Klasse unter WMI-Namespace autorisiert ist.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>801</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ReportProviderError</p></td>
<td align="left"><p>Unerwarteter Fehler des Berichts Anbieters.</p></td>
<td align="left"><p>Angesichts des SQL Server Reporting Services-Instanznamens versucht MBAM, den WMI-Namespace zu finden, der der Berichterstellungsinstanz entspricht, und eine Verbindung herzustellen. Dieser Fehler tritt auf, wenn MBAM auf eine Ausnahme stößt, wenn MBAM nach dem WMI-Namespace von SSRS sucht oder versucht, eine Verbindung herzustellen. Lesen Sie die Informationen in den im MBAM-Setup Kanal angemeldeten Fehlermeldungen, bevor Sie diese Meldung erhalten, um weitere Details anzuzeigen. Hier sind einige Dinge, die Sie überprüfen können:</p>
<ul>
<li><p>Überprüfen, ob SSRS mit dem bereitgestellten Instanznamen in Betrieb ist</p></li>
<li><p>Überprüfen Sie, ob das Benutzerkonto, auf dem die MBAM-Installation ausgeführt wird, über die erforderlichen Berechtigungen zum Abfragen/Herstellen einer Verbindung mit SSRS</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>802</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ReportProviderWarning</p></td>
<td align="left"><p>Warnung des Berichts Anbieters.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>803</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>ReportProviderInformation</p></td>
<td align="left"><p>Informationen zum Berichts Anbieter.</p></td>
<td align="left"><p>Nur Informationsdaten; keine Problembehandlung erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>900</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CMProviderUnexpectedError</p></td>
<td align="left"><p>CM-Anbieter unerwarteter Fehler.</p></td>
<td align="left"><p>Gibt an, dass ein Abbruchfehler aufgetreten ist, während enabling\disabling oder das Configuration Manager (cm)-Integrations Feature in MBAM konfiguriert wurde. Bekannte Fehler sind:</p>
<ul>
<li><p>Fehler beim Herstellen einer Verbindung mit dem cm-Standortserver über den SMS-Anbieter</p></li>
<li><p>Fehler beim Lesen aus der Registrierung</p></li>
<li><p>Fehler beim Erstellen oder Löschen eines Ordners im Dateisystem</p></li>
<li><p>Fehler beim Auffinden der Configuration Manager-Konsoleninstallation auf dem lokalen Computer</p></li>
<li><p>Fehler beim Abrufen von Informationen für die SSRS-Instanz, die als SRS-Rollen Punkt in cm konfiguriert ist</p></li>
</ul>
<p>Die Ereignismeldung enthält weitere Informationen zu dem jeweiligen Fehler. Überprüfen Sie, ob alle MBAM-Software Voraussetzungs Überprüfungen bestehen. Überprüfen Sie, ob der Registrierungspfad MBAM, falls vorhanden, HKEY_LOCAL_MACHINE \software\microsoft\mbam-Server und alle Unterschlüssel lesbar sind. Überprüfen Sie, ob MBAM in eine unterstützte Version von Configuration Manager integriert ist. Überprüfen Sie, ob die Configuration Manager-Konsole auf dem Computer installiert ist, auf dem das MBAM-Setup aufgerufen wird, und dass die Konsole zum Herstellen einer Verbindung mit dem Ziel-cm-Standort Server verwendet werden kann. Überprüfen Sie, ob eine gültige SSRS-Instanz als SRS-Rollen Punkt in cm konfiguriert ist und dass der Benutzer, der das MBAM-Setup ausführt, über read\write-Berechtigungen für die SSRS-Instanz verfügt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>901</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CMProviderError</p></td>
<td align="left"><p>CM-Anbieter unerwarteter Fehler.</p></td>
<td align="left"><p>Gibt an, dass ein Abbruchfehler aufgetreten ist, während enabling\disabling oder das Configuration Manager (cm)-Integrations Feature in MBAM konfiguriert wurde. Bekannte Fehler sind:</p>
<ul>
<li><p>Fehler beim Herstellen einer Verbindung mit dem cm-Standort Server über den SMS-Anbieter</p></li>
<li><p>Fehler beim Lesen aus der Registrierung</p></li>
<li><p>Fehler beim Erstellen oder Löschen eines Ordners im Dateisystem</p></li>
<li><p>Fehler beim Auffinden der Configuration Manager-Konsoleninstallation auf dem lokalen Computer</p></li>
<li><p>fehlender ConfigMgr-Ordner in SSRS als Stammordner für die SRS-Rollen Punkt Berichte</p></li>
<li><p>fehlende freigegebene ConfigMgr-Datenquelle in SSRS</p></li>
<li><p>Fehler beim Bereitstellen von SSRS-Berichten in der SSRS-Instanz, die als SRS-Rollen Punkt in cm konfiguriert ist</p></li>
<li><p>Fehler beim Erstellen von Konfigurationselementen und Baselines in cm</p></li>
</ul>
<p>Die Ereignismeldung enthält weitere Informationen zu dem jeweiligen Fehler. Überprüfen Sie, ob alle MBAM-Software Voraussetzungs Überprüfungen bestehen. Überprüfen Sie, ob der Registrierungspfad MBAM, falls vorhanden, HKEY_LOCAL_MACHINE \software\microsoft\mbam-Server und alle Unterschlüssel lesbar sind. Überprüfen Sie, ob MBAM in eine unterstützte Version von Configuration Manager integriert ist. Überprüfen Sie, ob die Configuration Manager-Konsole auf dem Computer installiert ist, auf dem das MBAM-Setup aufgerufen wird, und dass die Konsole zum Herstellen einer Verbindung mit dem Ziel-cm-Standort Server verwendet werden kann. Überprüfen Sie, ob der Benutzer über die erforderlichen read\write-Berechtigungen zum Erstellen von Konfigurationselementen, Baselines und Auflistungen in cm verfügt. Überprüfen Sie, ob eine gültige SSRS-Instanz als SRS-Rollen Punkt in cm konfiguriert ist und dass der Benutzer, der das MBAM-Setup ausführt, über read\write-Berechtigungen für die SSRS-Instanz verfügt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>902</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>CMProviderWarning</p></td>
<td align="left"><p>CM-Anbieter Warnung.</p></td>
<td align="left"><p>Gibt an, dass beim Aktivieren des Configuration Manager (cm)-Integrationsfeatures ein nicht Abbruchfehler aufgetreten ist. Bekannte Fehler sind: Fehler beim Commit für Sammlungsregeln in der MBAM-Sammlung unterstützte Computer in cm und andere Fehler im Zusammenhang mit SSRS und Netzwerk.</p>
<p>Die Ereignismeldung enthält weitere Informationen zu dem jeweiligen Fehler. Einige Vorgänge, die diese Warnung verursacht haben, werden nach der Warnung zurückgezogen. Wenn nach mehreren Wiederholungen der Fehler weiterhin auftritt, wird MBAM möglicherweise mit einem tatsächlichen Fehler beendet. Überprüfen Sie andere Ereignismeldungen im Protokoll, um das MBAM-Setup weiter zu diagnostizieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>903</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/betriebsbereit</p></td>
<td align="left"><p>CMProviderInformation</p></td>
<td align="left"><p>Informationen zum cm-Anbieter.</p></td>
<td align="left"><p>Nur Informationsdaten; keine Problembehandlung erforderlich.</p></td>
</tr>
</tbody>
</table>

 

## Vorgang


Die folgende Tabelle enthält Nachrichten und Informationen zur Problembehandlung für Ereignis-IDs, die während der Ausführung von MBAM auftreten können.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ereignis-ID</th>
<th align="left">Source</th>
<th align="left">Ereignis Symbol</th>
<th align="left">Meldung</th>
<th align="left">Problembehandlung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>1</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>WebAppSpnError</p></td>
<td align="left"><p>Anwendung: {Sitename} {VirtualDirectory} fehlt die folgenden Dienstprinzipalnamen (SPNs): {ListOfSpns} registrieren Sie die erforderlichen SPNs für das Konto: {ExecutionAccount}.</p></td>
<td align="left"><p>Damit die integrierte Windows-Authentifizierung erfolgreich ausgeführt werden kann, müssen die erforderlichen SPNs vorhanden sein. Diese Meldung weist darauf hin, dass der für MBAM-Anwendung erforderliche SPN nicht ordnungsgemäß konfiguriert wurde. Details in diesem Ereignis sollten weitere Informationen enthalten.</p>
<p>Weitere Informationen finden Sie unter "Dienstprinzipal Name (SPN)" in <a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams)"> MBAM 2,5-Server Voraussetzungen für eigenständige und Configuration Manager-Integrations Topologien </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>4</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/betriebsbereit</p></td>
<td align="left"><p>PerformanceCounterError</p></td>
<td align="left"><p>Beim Abrufen eines Leistungsindikators ist ein Fehler aufgetreten.</p>
<p>Nachricht: {Event Message} Category: {CategoryOfPerformanceCounter} Leistungsindikator: {NameOfPerformanceCounter} Instanz: {Name der Leistungsindikatorkategorie Instanz} Ausnahme: {ExceptionThrown}</p>
<p>Die Ablaufverfolgungsnachricht enthält die eigentliche Ausnahmemeldung, die teilweise hier erläutert wird:</p>
<p><strong>ArgumentNullException </strong> : Diese Ausnahme wird ausgelöst, wenn die Kategorie, der Zähler oder die Instanz des angeforderten Leistungsindikators ungültig ist.</p>
<p><strong>System. InvalidOperationException </strong> : CategoryName ist eine leere Zeichenfolge ( &quot; &quot; ).-oder-counterName ist eine leere Zeichenfolge ( &quot; &quot; ).</p>
<p>– oder – die angeforderte Berechtigungseinstellung für Lesen/Schreiben ist für diesen Leistungsindikator ungültig.</p>
<p>– oder – die angegebene Kategorie ist nicht vorhanden (Wenn ReadOnly wahr ist).</p>
<p>– oder – die angegebene Kategorie ist keine benutzerdefinierte .NET Framework-Kategorie (Wenn ReadOnly auf false festgelegt ist).</p>
<p>– oder – die angegebene Kategorie wird als Multi-instance markiert und erfordert, dass der Leistungsindikator mit einem Instanznamen erstellt wird.</p>
<p>-oder-InstanceName ist mehr als 127 Zeichen.</p>
<p>-oder-CategoryName und CounterName wurden in verschiedene Sprachen lokalisiert.</p>
<p><strong>System. ComponentModel. Win32Exception </strong> : beim Zugriff auf eine System-API ist ein Fehler aufgetreten.</p>
<p><strong>System. PlatformNotSupportedException </strong> : die Plattform ist Windows 98 oder Windows Millennium Edition (Me), die keine Leistungsindikatoren unterstützt.</p>
<p><strong>System. UnauthorizedAccessException </strong> : Code, der ohne Administratorrechte ausgeführt wird, hat versucht, einen Leistungsindikator zu lesen.</p></td>
<td align="left"><p>Die in dem Ereignis enthaltene Meldung enthält weitere Details zur ausgelösten Ausnahme. Wenn eine System. UnauthorizedAccessException-Ausnahme ausgelöst wurde, überprüfen Sie, ob MBAM-Ausführungskonto (app-Pool) Zugriff auf Leistungsindikator-APIs hat.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>100</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>AdminServiceRecoveryDbError</p></td>
<td align="left"><p><strong>GetMachineUsers </strong> : beim Abrufen von Benutzerinformationen aus der Datenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>GetRecoveryKey </strong> : beim Abrufen des Wiederherstellungsschlüssels aus der Datenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>GetRecoveryKey </strong> : beim Abrufen von Benutzerinformationen aus der Datenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>GetRecoveryKeyIds </strong> : beim Abrufen von Wiederherstellungsschlüssel-IDs aus der Datenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>GetTpmHashForUser </strong> : beim Abrufen von TPM-Hash Daten aus der Wiederherstellungsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>GetTpmHashForUser </strong> : beim Abrufen von TPM-Hash Daten aus der Wiederherstellungsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>QueryDriveRecoveryData </strong> : Es ist ein Fehler aufgetreten, während Daten zur Laufwerk Wiederherstellung aus der Datenbank erhalten werden. Nachricht: {Nachricht}-oder-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : beim Abrufen von Wiederherstellungsschlüssel-IDs aus der Datenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>QueryVolumeUsers </strong> : beim Abrufen von Benutzerinformationen aus der Datenbank ist ein Fehler aufgetreten.</p></td>
<td align="left"><p>Diese Meldung wird protokolliert, wenn bei der Kommunikation mit der MBAM-Wiederherstellungsdatenbank eine Ausnahme vorliegt. Lesen Sie die in der Ablaufverfolgung enthaltenen Informationen, um bestimmte Details zur Ausnahme abzurufen.</p>
<p>Detaillierte Schritte zur Problembehandlung finden Sie im TechNet-Artikel <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Problembehandlung beim Herstellen einer Verbindung mit dem SQL Server-Datenbankmodul </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>101</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>AdminServiceComplianceDbError</p></td>
<td align="left"><p><strong>GetRecoveryKey </strong> : bei der Protokollierung eines Überwachungsereignisses in der Kompatibilitätsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>GetRecoveryKeyIds </strong> : bei der Protokollierung eines Überwachungsereignisses in der Kompatibilitätsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>GetTpmHashForUser </strong> : bei der Protokollierung eines Überwachungsereignisses in der Kompatibilitätsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : bei der Protokollierung eines Überwachungsereignisses in der Kompatibilitätsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>QueryDriveRecoveryData </strong> : bei der Protokollierung eines Überwachungsereignisses in der Kompatibilitätsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}</p></td>
<td align="left"><p>Diese Meldung wird protokolliert, wenn beim kommunizieren der MBAM-Kompatibilitätsdatenbank eine Ausnahme vorliegt. Lesen Sie die in der Ablaufverfolgung enthaltenen Informationen, um bestimmte Details zur Ausnahme abzurufen.</p>
<p>Detaillierte Schritte zur Problembehandlung finden Sie im TechNet-Artikel <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Problembehandlung beim Herstellen einer Verbindung mit dem SQL Server-Datenbankmodul </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>102</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>AgentServiceRecoveryDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Diese Meldung zeigt eine Ausnahme an, wenn der MBAM-Agent-Dienst versucht, mit der Wiederherstellungsdatenbank zu kommunizieren. Lesen Sie die im Ereignis enthaltene Nachricht, um bestimmte Informationen zur Ausnahme abzurufen.</p>
<p>Weitere Informationen finden Sie im TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> -Artikel Problembehandlung beim Herstellen einer Verbindung mit dem SQL Server-Datenbankmodul </a> , um zu überprüfen, ob das MBAM-App-Pool Konto über die erforderlichen Berechtigungen zum Herstellen einer Verbindung oder Ausführung in MBAM-Wiederherstellungs</p></td>
</tr>
<tr class="even">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>AgentServiceError</p></td>
<td align="left"><p>Clientcomputerkonto oder Daten Migrationsbenutzerkonto konnte nicht erkannt werden. – oder –</p>
<p>Fehler bei der Kontoüberprüfung bei der Identität des Anrufers.</p></td>
<td align="left"><p>Wenn ein Anruf an die PostKeyRecoveryInfo- &quot; &quot; , &quot; IsRecoveryKeyResetRequired-, CommitRecoveryKeyRest- &quot; &quot; &quot; oder &quot; GetTpmHash &quot; -Webmethoden für MBAM-Agent-Dienste erfolgt, ruft er den Aufrufer-Kontext ab, um die Anmeldeinformationen für den Aufrufer abzurufen. Wenn der Aufrufer-Kontext null oder leer ist, können die MBAM-Agentendienst Protokolle das &quot; Clientcomputerkonto oder das Benutzerkonto für die Datenmigration nicht ermitteln.&quot;</p>
<p>Die &quot; Überprüfung des Nachrichten Kontos für die Identität des Anrufers ist fehlgeschlagen &quot; , wenn die Webmethode den Aufrufer zu einem Computerkonto erwartet und der Anrufer kein Computerkonto ist, oder wenn die Webmethode dem Aufrufer als Benutzerkonto dient und der Aufrufer kein Benutzerkonto oder Mitglied des Gruppenkontos für die Datenmigration ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>StatusServiceComplianceDbConfigError</p></td>
<td align="left"><p>&quot;Die Verbindungszeichenfolge der Kompatibilitätsdatenbank in der Registrierung ist leer.&quot;</p></td>
<td align="left"><p>Diese Meldung wird protokolliert, wenn die Kompatibilitäts-DB-Verbindungszeichenfolge ungültig ist.</p>
<p>Überprüfen Sie den Wert im Registrierungsschlüssel HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString</p></td>
</tr>
<tr class="even">
<td align="left"><p>105</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>StatusServiceComplianceDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Dieser Fehler zeigt an, dass MBAM-Websites/-Webdienste keine Verbindung mit der MBAMCompliance-Datenbank herstellen konnten.</p>
<p>Informationen zur <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Problembehandlung beim Herstellen einer Verbindung mit dem SQL Server-Datenbankmodul finden Sie im TechNet </a> -Artikel so stellen Sie sicher, dass das IIS-App-Pool Konto eine Verbindung mit der MBAM-Kompatibilitätsdatenbank herstellen kann</p></td>
</tr>
<tr class="odd">
<td align="left"><p>106</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>HelpdeskError</p></td>
<td align="left"><p>Die Anforderung an URL {URL} hat einen internen Fehler verursacht. – oder –</p>
<p>Beim Abrufen von Ausführungskontext Informationen ist ein Fehler aufgetreten. Die SPN-Registrierung (Service Principal Name) konnte nicht überprüft werden. – oder –</p>
<p>Beim Überprüfen der SPN-Registrierung (Service Principal Name) ist ein Fehler aufgetreten.</p></td>
<td align="left"><p>Gibt an, dass in der Helpdesk-Anwendung eine nicht behandelte Ausnahme ausgelöst wurde. Überprüfen Sie die Protokolleinträge im operativen Kanal des MBAM-Administrators, um die spezifische Ausnahme zu finden. oder</p>
<p>Während des Ladevorgangs der anfänglichen Helpdesk-Website wird eine SPN-Prüfung durchgeführt. Zum Überprüfen von SPN benötigt der Helpdesk Ausführungskonto Informationen, IIS-Sitename und ApplicationVirtualPath entsprechend der Helpdesk-Website. Diese Fehlermeldung wird protokolliert, wenn mindestens eine dieser Fehlermeldungen ungültig ist oder fehlt. oder</p>
<p>Diese Meldung zeigt an, dass beim Durchführen der SPN-Überprüfung eine Sicherheitsausnahme ausgelöst wird. Beziehen Sie sich auf die im Abschnitt Ereignisdetails enthaltene Ausnahme.</p></td>
</tr>
<tr class="even">
<td align="left"><p>107</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>SelfServicePortalError</p></td>
<td align="left"><p>Beim Abrufen des Wiederherstellungsschlüssels für einen Benutzer ist ein Fehler aufgetreten. EventDetails: {ExceptionMessage}-oder-</p>
<p>Beim Abrufen von Ausführungskontext Informationen ist ein Fehler aufgetreten. Die SPN-Registrierung (Service Principal Name) konnte nicht überprüft werden. EventDetails: User: {username Identity} Anwendung: {SiteName\ApplicationVirtualPath}-oder-</p>
<p>Beim Überprüfen der SPN-Registrierung (Service Principal Name) ist ein Fehler aufgetreten. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>Gibt an, dass eine unerwartete Ausnahme ausgelöst wurde, als eine Anforderung zum Abrufen des Wiederherstellungsschlüssels gestellt wurde. Weitere Informationen finden Sie im Abschnitt "Ereignisdetails". Wenn die Ablaufverfolgung im MBAM-Helpdesk aktiviert ist, verweisen Sie auf Ablaufverfolgungsdaten, um detaillierte Ausnahmemeldungen zu erhalten. oder</p>
<p>Während eines anfänglichen Ladevorgangs Ruft das Self-Service-Portal (SSP) Ausführungskonto Informationen, IIS-Sitename und ApplicationVirtualPath ab, die der Self-Service-Website entsprechen, um SPN zu überprüfen. Diese Fehlermeldung wird protokolliert, wenn eine oder mehrere dieser Fehler ungültig sind. oder</p>
<p>Diese Meldung weist darauf hin, dass beim Durchführen der SPN-Überprüfung eine Sicherheitsausnahme ausgelöst wurde. Beziehen Sie sich auf die im Abschnitt Ereignisdetails enthaltene Ausnahme.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>108</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>DomainControllerError</p></td>
<td align="left"><p>Beim Auflösen des Domänennamens {Domain Name} ist ein Fehler aufgetreten, ein Speicherzuordnungsfehler ist aufgetreten. – oder –</p>
<p>DsGetDcName-Methode konnte nicht aufgerufen werden. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>Um den Domänennamen zu beheben, nutzt MBAM die &quot; DsGetDcName &quot; -Windows-API. Diese Meldung wird protokolliert &quot; , wenn &quot; DsGetDcName &quot; ERROR_NOT_ENOUGH_MEMORY zurückgibt &quot; , die auf einen Speicherzuordnungsfehler hinweisen. oder</p>
<p>Diese Meldung zeigt an, dass &quot; die DsGetDcName- &quot; API-Methode im Hostsystem nicht verfügbar ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>109</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>WebAppRecoveryDbError</p></td>
<td align="left"><p>Beim Lesen der Konfiguration der Wiederherstellungsdatenbank ist ein Fehler aufgetreten. Die Verbindungszeichenfolge zur Wiederherstellungsdatenbank ist nicht konfiguriert. Nachricht: {Nachricht}-oder-</p>
<p><strong>DoesUserHaveMatchingRecoveryKey </strong> : beim Abrufen von Wiederherstellungsschlüssel-IDs für einen Benutzer ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>QueryDriveRecoveryData </strong> : Fehler beim Abrufen von Daten zur Laufwerkswiederherstellung. Nachricht: {Nachricht}-oder-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : beim Abrufen von Wiederherstellungsschlüssel-IDs für einen Benutzer ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p>Beim Abrufen des TPM-Kennworthashs aus der Wiederherstellungsdatenbank ist ein Fehler aufgetreten. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>Diese Meldung weist darauf hin, dass die Verbindungszeichenfolgen-Informationen zur Wiederherstellungsdatenbank unter &quot; HKLM\Software\Microsoft\MBAM Server\Web\RecoveryDBConnectionString &quot; ungültig sind. Überprüfen Sie den angegebenen Registrierungsschlüsselwert. oder</p>
<p>Wenn eine der verbleibenden Nachrichten protokolliert wird, lesen Sie die Schritte zur Problembehandlung im TechNet-Artikel Problembehandlung beim Herstellen einer Verbindung <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> mit dem SQL Server-Datenbankmodul, </a> um zu überprüfen, ob eine Verbindung mit der MBAM-Wiederherstellungsdatenbank vom IIS-Server mithilfe der APP-Pool Anmeldeinformationen hergestellt werden kann.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>110</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>WebAppComplianceDbError</p></td>
<td align="left"><p>Beim Lesen der Konfiguration der Kompatibilitätsdatenbank ist ein Fehler aufgetreten. Die Verbindungszeichenfolge zur Kompatibilitätsdatenbank ist nicht konfiguriert. – oder –</p>
<p><strong>GetRecoveryKeyForCurrentUser </strong> : bei der Protokollierung eines Überwachungsereignisses in der Kompatibilitätsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : bei der Protokollierung eines Überwachungsereignisses in der Kompatibilitätsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}-oder-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : bei der Protokollierung eines Überwachungsereignisses in der Kompatibilitätsdatenbank ist ein Fehler aufgetreten. Nachricht: {Nachricht}</p></td>
<td align="left"><p>Diese Meldung zeigt an, dass die Informationen zur Konformitäts-DB-Verbindungszeichenfolge unter &quot; HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString &quot; ungültig sind. Überprüfen Sie den Wert, der dem obigen Registrierungsschlüssel entspricht. oder</p>
<p>Wenn eine der verbleibenden Nachrichten protokolliert wird, lesen Sie die im TechNet-Artikel aufgelisteten Schritte zur Problembehandlung beim Herstellen einer Verbindung <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> mit dem SQL Server-Datenbankmodul, </a> um zu überprüfen, ob eine Verbindung mit der MBAM-Kompatibilitätsdatenbank von IIS-Server mithilfe der APP-Pool Anmeldeinformationen hergestellt werden kann.</p></td>
</tr>
<tr class="even">
<td align="left"><p>111</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>WebAppDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Diese Fehler deuten auf eine der beiden folgenden Bedingungen hin:</p>
<ul>
<li><p>MBAM-Websites/Webdienste konnten keine Verbindung mit MBAMCompliance oder MBAMRecovery-Datenbank herstellen.</p></li>
<li><p>MBAM Websites/Webdienste-Ausführungskonto (app-Pool Konto) konnte die gespeicherte GetVersion-Prozedur in MBAMCompliance oder MBAMRecovery-Datenbank nicht ausführen</p></li>
</ul>
<p>Die im Ereignis enthaltene Nachricht enthält weitere Details zur Ausnahme.</p>
<p>Lesen Sie die Schritte zur Problembehandlung, die im TechNet-Artikel Problembehandlung beim <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Herstellen einer Verbindung mit dem SQL Server-Datenbankmodul aufgeführt sind, </a> um zu überprüfen, ob das MBAM-Ausführungskonto (app-Pool Konto) eine Verbindung mit MBAM-Konformitäts-/Wiederherstellungsdatenbank herstellen kann und über Berechtigungen zum Ausführen der gespeicherten Prozedur GetVersion verfügt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>112</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Administrator</p></td>
<td align="left"><p>WebAppError</p></td>
<td align="left"><p>Beim Überprüfen der SPN-Registrierung (Service Principal Name) ist ein Fehler aufgetreten. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>Um die SPN-Überprüfung durchzuführen, fragt MBAM Active Directory ab, um eine Liste von SPNs zugeordnete Ausführungskonto abzurufen. MBAM fragt auch die &quot;ApplicationHost.configab &quot; , um MBAM-Websitebindungen zu erhalten. Diese Fehlermeldung weist darauf hin, dass MBAM nicht mit Active Directory kommunizieren konnte, oder die applicationHost.config Datei konnte nicht geladen werden.</p>
<p>Überprüfen Sie, ob das Ausführungskonto (app-Pool Konto) über die Berechtigung zum Abfragen von AD oder ApplicationHost.config Datei verfügt. Überprüfen Sie auch die Website Bindungseinträge in ApplicationHost.config-Datei.</p></td>
</tr>
<tr class="even">
<td align="left"><p>200</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/betriebsbereit</p></td>
<td align="left"><p>HelpDeskInformation</p></td>
<td align="left"><p>Die Verwaltungswebsite-Anwendung wurde erfolgreich gefunden und mit einer unterstützten Version der Wiederherstellungsdatenbank verbunden. – oder –</p>
<p>Die Verwaltungswebsite-Anwendung wurde erfolgreich gefunden und mit einer unterstützten Version der Kompatibilitätsdatenbank verbunden.</p></td>
<td align="left"><p>Zeigt eine erfolgreiche Verbindung mit der Datenbank für die Wiederherstellung/Compliance von der MBAM Helpdesk-Website an.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>201</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/betriebsbereit</p></td>
<td align="left"><p>SelfServicePortalInformation</p></td>
<td align="left"><p>Die Self-Service-Portal-Anwendung wurde erfolgreich gefunden und mit einer unterstützten Version der Wiederherstellungsdatenbank verbunden. – oder –</p>
<p>Die Self-Service-Portal-Anwendung wurde erfolgreich gefunden und mit einer unterstützten Version der Kompatibilitätsdatenbank verbunden.</p></td>
<td align="left"><p>Zeigt eine erfolgreiche Verbindung mit der Datenbank für die Wiederherstellung/Konformität aus dem Self-Service-Portal von MBAM an.</p></td>
</tr>
<tr class="even">
<td align="left"><p>202</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/betriebsbereit</p></td>
<td align="left"><p>WebAppInformation</p></td>
<td align="left"><p>Die SPNs der Anwendung sind ordnungsgemäß registriert.</p></td>
<td align="left"><p>Gibt an, dass die für die MBAM-Helpdesk-Website erforderlichen SPNs für das ausgeführte Konto ordnungsgemäß registriert sind.</p></td>
</tr>
</tbody>
</table>

 


## Verwandte Themen


[Technische Referenz für MBAM2.5](technical-reference-for-mbam-25.md)

[Client-Ereignisprotokolle](client-event-logs.md)

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





