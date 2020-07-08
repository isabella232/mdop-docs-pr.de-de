---
title: MED-V-Ereignisprotokollmeldungen
description: MED-V-Ereignisprotokollmeldungen
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809739"
---
# MED-V-Ereignisprotokollmeldungen


Die Protokolldateien für Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 bieten detaillierte Informationen dazu, wie Sie Med-v in Ihrem Unternehmen bereitstellen und verwalten, und helfen dabei, die Funktionalität zu überprüfen oder Probleme zu beheben.

## Ereignis-IDs


Im folgenden finden Sie eine Liste der Med-v-Ereignis-IDs, die Ihnen bei der Behandlung von Problemen helfen können, die beim Bereitstellen oder Verwalten von Med-v auftreten können.

### FTS

Zeigt die Ereignis-IDs für die erstmalige Einrichtung an.

### Ereignis-ID 3066

Der Vorgang zum Starten des virtuellen Computers ist fehlgeschlagen.

<a href="" id="description"></a>**Beschreibung**  
Bei der virtuellen Festplatte (VHD), die Sie zum Erstellen eines MED-V-Arbeitsbereichs verwenden, besteht ein potenzielles Problem.

<a href="" id="solution"></a>**Lösung**  
Überprüfen Sie, ob Sie einen virtuellen Computer mit der VHD für MED-V erstellen können und ob er gestartet werden kann.

### Ereignis-ID 3071

Fehler beim Vorbereiten der virtuellen Maschine.

<a href="" id="description"></a>**Beschreibung**  
Bei der erstmaligen Einrichtung ist ein Problem aufgetreten, das möglicherweise von vielen unterschiedlichen Problemen verursacht wurde. Dazu gehören Probleme mit der Netzwerkverbindung.

<a href="" id="solution"></a>**Lösung**  
Starten Sie den MED-V-Host-Agent neu, um die erstmalige Einrichtung erneut auszuführen.

### Ereignis-ID 3078

Fehler beim Vorbereiten der virtuellen Maschine.

<a href="" id="description"></a>**Beschreibung**  
Bei der VHD, die Sie zum Erstellen eines MED-V-Arbeitsbereichs verwenden, besteht ein potenzielles Problem.

<a href="" id="solution"></a>**Lösung**  
Überprüfen Sie, ob Sie einen virtuellen Computer mit der VHD für MED-V erstellen können und ob er gestartet werden kann.

### Ereignis-ID 3079

Erneutes Testen der Vorbereitung virtueller Computer

<a href="" id="description"></a>**Beschreibung**  
MED-V versucht, den virtuellen Computer vorzubereiten.

<a href="" id="solution"></a>**Lösung**  
Es ist keine Aktion erforderlich. Lassen Sie die erstmalige Einrichtung fertig.

### Ereignis-ID 3080

Der Client wurde beim Vorbereiten des virtuellen Computers angehalten.

<a href="" id="description"></a>**Beschreibung**  
MED-V wird bei dem Versuch, den virtuellen Computer vorzubereiten, unerwartet beendet.

<a href="" id="solution"></a>**Lösung**  
Starten Sie den MED-V-Host-Agent, und lassen Sie das erstmalige Setup abgeschlossen

### Ereignis-ID 3084

Der virtuelle Computer ist ungültig. Das erstmalige Setup muss erneut ausgeführt werden.

<a href="" id="description"></a>**Beschreibung**  
Der MED-V-Host-Agent hat ein Problem mit dem virtuellen Computer festgestellt.

<a href="" id="solution"></a>**Lösung**  
Es ist keine Aktion erforderlich. Lassen Sie die erstmalige Einrichtung fertig.

### Ereignis-ID 3099

Fehler beim Aufrufen des virtuellen Computers für Start.

<a href="" id="description"></a>**Beschreibung**  
Bei der VHD, die Sie zum Erstellen eines MED-V-Arbeitsbereichs verwenden, besteht ein potenzielles Problem.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass Sie einen virtuellen Computer mit der VHD für MED-V erstellen und öffnen können.

### VM-Verwaltung

### Ereignis-ID 4022

VMManagerException schwerwiegender Fehler beim Ausgeben des Befehls an VM.

<a href="" id="description"></a>**Beschreibung**  
Der Endbenutzer hat versucht, Med-v durch abmelden oder durch Herunterfahren des Med-v-Hosts zu beenden, und die VMTaskTimeout-Konfigurationseinstellung wurde überschritten.

<a href="" id="solution"></a>**Lösung**  
Starten Sie MED-V neu.

### Ereignis-ID 4028

Timeout des VM-Vorgangs.

<a href="" id="description"></a>**Beschreibung**  
Der Endbenutzer hat versucht, MED-V durch abmelden oder durch Herunterfahren des Hosts zu beenden, und die VMTaskTimeout-Konfigurationseinstellung wurde überschritten.

<a href="" id="solution"></a>**Lösung**  
Starten Sie MED-V neu.

### Ereignis-ID 4038

Vmsal hat eine Fehlermeldung an den Benutzer gesendet.

<a href="" id="description"></a>**Beschreibung**  
Dem Endbenutzer wird eine Fehlermeldung angezeigt, die besagt, dass die virtuelle Anwendung von MED-V nicht gestartet werden konnte.

<a href="" id="solution"></a>**Lösung**  
Wenn der Fehler mindestens zwei Mal hintereinander protokolliert wird, beenden Sie MED-V, und stellen Sie eine Verbindung mit dem virtuellen Computer mithilfe der Windows Virtual PC-Konsole her, und versuchen Sie, die Anwendung im Vollbildmodus zu starten.

### Ereignis-ID 4040

Wiederverwendung von Ergänzungen, da Terminal Services im Gast nicht initialisiert wird.

<a href="" id="description"></a>**Beschreibung**  
MED-V hat den virtuellen Computer neu gestartet, weil die Remote Desktop Dienste auf dem virtuellen Computer nicht initialisiert wurden.

<a href="" id="solution"></a>**Lösung**  
Wenn der Fehler mindestens zwei Mal hintereinander protokolliert wird, beenden Sie MED-V, und stellen Sie eine Verbindung mit dem virtuellen Computer mithilfe der Windows Virtual PC-Konsole her.

### Ereignis-ID 4042

Fehler beim wieder verwenden von Zusätzen im Gast.

<a href="" id="description"></a>**Beschreibung**  
MED-V konnte keine virtuellen Computer Erweiterungen auf dem virtuellen Computer wieder verwenden.

<a href="" id="solution"></a>**Lösung**  
Wenn der Fehler mindestens zwei Mal hintereinander protokolliert wird, beenden Sie MED-V, und stellen Sie eine Verbindung mit dem virtuellen Computer mithilfe der Windows Virtual PC-Konsole her.

### Ereignis-ID 4043

Fehler beim Zurücksetzen des abgelaufenen Kennworts auf dem virtuellen Computer.

<a href="" id="description"></a>**Beschreibung**  
Der Endbenutzer hat das Kennwort auf dem virtuellen Computer nicht zurückgesetzt, bevor es abgelaufen ist. Daher kann der Benutzer möglicherweise nicht auf Netzwerkressourcen zugreifen oder Arbeit speichern.

<a href="" id="solution"></a>**Lösung**  
Beenden Sie den MED-V-Gast, und starten Sie ihn erneut.

### URL-Umleitung

### Ereignis-ID 5005

VM-Name konnte nicht aus der Konfiguration abgerufen werden. Gast Browser kann nicht gestartet werden.

<a href="" id="description"></a>**Beschreibung**  
Die URL-Umleitung konnte den MED-V-Arbeitsbereichsnamen nicht aus der Konfiguration abrufen. Daher kann Windows Virtual PC nicht darüber informiert werden, dass die umgeleitete URL im MED-V Workspace-Browser geöffnet wird.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass der Name des MED-V-Arbeitsbereichs festgesetzt ist und er dem Namen eines virtuellen Computers im C:\\Users\\- &lt; *Benutzer* &gt; \\Virtual Machines-Verzeichnis entspricht. Der Name des MED-V-Arbeitsbereichs befindet sich unter HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Wenn der Benutzer beispielsweise "Matt" ist und der Arbeitsbereichsname "mattsworkspace" lautet, sollte der Wert von HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name "mattsworkspace" sein, und es sollte eine Datei mit dem Namen C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.

### Ereignis-ID 5006

Fehler beim Erstellen des Pipes-Servers.

<a href="" id="description"></a>**Beschreibung**  
Der URL-Umleitungsdienst konnte den Kanalserver für die Kommunikation mit Internet Explorer nicht erstellen.

<a href="" id="solution"></a>**Lösung**  
Überprüfen Sie die Systemereignisprotokolle auf Versuche, eine Datei oder Ressource zu erstellen, deren Pfad wie folgt beginnt: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" und endet mit dem Benutzernamen und dem Domänennamen des Benutzers. Wenn dies im Ereignisprotokoll nicht vorhanden ist, starten Sie den Computer neu.

### ConfigMgr (Gast)

### Ereignis-ID 7001

Die Konfigurationsdaten des Host Netzwerks sind nicht ordnungsgemäß formatiert.

<a href="" id="description"></a>**Beschreibung**  
Entweder die vom Host empfangene Netzwerkkonfiguration ist eine falsch formatierte XML-Zeichenfolge, oder die vom Host zurückgegebenen Netzwerkinformationen können nicht in ein XML-Dokument geschrieben werden.

<a href="" id="solution"></a>**Lösung**  
Starten Sie den Hostcomputer und den virtuellen Computer neu.

### Ereignis-ID 7005

Eine Änderung der Host Netzwerkkonfiguration wurde erkannt, konnte aber nicht angewendet werden, da die Konfigurationsdaten des Host Netzwerks nicht ordnungsgemäß formatiert wurden.

<a href="" id="description"></a>**Beschreibung**  
Eine Änderung an der Host Netzwerkkonfiguration wurde dem virtuellen Computer mitgeteilt, konnte aber aufgrund eines Fehlers nicht auf dem virtuellen Computer verarbeitet werden. Dieser Fehler kann durch falsch formatierte Daten oder die Unfähigkeit verursacht werden, die Informationen in der WMI-CCMNetworkAdapter-Instanz (Windows Management Instrumentation) zu setzen.

<a href="" id="solution"></a>**Lösung**  
Starten Sie den Host und den virtuellen Computer neu.

### ConfigMgr (Host)

### Ereignis-ID 8006

Der virtuelle Computer konnte nicht gefunden werden.

<a href="" id="description"></a>**Beschreibung**  
Windows Virtual PC 7 kann den virtuellen Computer nicht finden. Der virtuelle Computer wurde möglicherweise gelöscht, verschoben, entfernt oder der Zugriff wurde verweigert.

<a href="" id="solution"></a>**Lösung**  
Installieren Sie den virtuellen Computer erneut.

### Ereignis-ID 8008

Die Netzwerkkonfigurationsinformationen der Arbeitsstation konnten nicht abgerufen werden.

<a href="" id="description"></a>**Beschreibung**  
Netzwerkkonfigurationsinformationen konnten nicht vom MED-V-Host erfasst werden, wahrscheinlich wegen eines Systemanruf Fehlers in .NET Framework. Dieser Fehler kann auch auftreten, wenn die vom MED-V-Host zurückgegebenen Netzwerkinformationen nicht in ein XML-Dokument geschrieben werden können.

<a href="" id="solution"></a>**Lösung**  
Starten Sie die Host Arbeitsstation neu.

### Ereignis-ID 8010

Die Netzwerkkonfigurationsdaten konnten auf dem virtuellen Computer nicht eingerichtet werden.

<a href="" id="description"></a>**Beschreibung**  
Die MED-V-hostnetwork-Adressübersetzung (NAT) konnte nicht an den virtuellen Computer übermittelt werden, wahrscheinlich, weil sich der virtuelle Computer in einem fehlerhaften Zustand befindet oder die Windows Virtual PC-Erweiterungen nicht installiert oder aktiviert wurden.

<a href="" id="solution"></a>**Lösung**  
Beenden Sie den virtuellen Computer, und starten Sie ihn erneut. Darüber hinaus müssen Sie möglicherweise den virtuellen Computer erneut installieren.

### Ereignis-ID 8011

Die Netzwerkkonfigurationsdaten konnten auf dem virtuellen Computer nicht zurückgesetzt werden.

<a href="" id="description"></a>**Beschreibung**  
Die MED-V-hostnetwork-Konfiguration (Bridged) konnte nicht an den virtuellen Computer übermittelt werden, wahrscheinlich, weil sich der virtuelle Computer in einem fehlerhaften Zustand befindet oder die Windows Virtual PC-Erweiterungen nicht installiert oder aktiviert wurden.

<a href="" id="solution"></a>**Lösung**  
Beenden Sie den virtuellen Computer, und starten Sie ihn erneut. Darüber hinaus müssen Sie möglicherweise den virtuellen Computer erneut installieren.

### Druckerumleitung

### Ereignis-ID 9001

Fehler bei der Datei Berechtigung.

<a href="" id="description"></a>**Beschreibung**  
Der Endbenutzer ist nicht berechtigt, auf den Ordner zuzugreifen, der zum Öffnen oder Erstellen der MED-V-Druckerdatei zum Lesen erforderlich ist.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass auf den User\\AppData\\-Pfad zugegriffen werden kann und dass der Benutzer die Berechtigung zum Lesen und schreiben hat. Wenn der Benutzer beispielsweise "Matt" ist, sollte der Pfad C:\\Users\\Matt\\AppData\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen. Und falls vorhanden, sollten der Pfad C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen.

### Ereignis-ID 9002

Fehler bei der Datei Berechtigung.

<a href="" id="description"></a>**Beschreibung**  
Der Endbenutzer ist nicht berechtigt, auf den Ordner zuzugreifen, der zum Öffnen oder Erstellen der MED-V-Druckerdatei zum Schreiben erforderlich ist.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass auf den User\\AppData\\-Pfad zugegriffen werden kann und dass der Benutzer die Berechtigung zum Lesen und schreiben besitzt. Wenn der Benutzer beispielsweise "Matt" ist, sollte der Pfad C:\\Users\\Matt\\AppData\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen. Und falls vorhanden, sollten der Pfad C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen.

### Ereignis-ID 9004

Der Pfad zum Speichern von MEDV-Drucker Dateien konnte nicht erstellt werden.

<a href="" id="description"></a>**Beschreibung**  
Der Drucker Umleitungsdienst konnte nicht auf Dateien zugreifen oder Verzeichnisse erstellen, die zum Speichern der Druckerinformationen erforderlich sind.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass auf den User\\AppData\\-Pfad zugegriffen werden kann und dass der Benutzer die Berechtigung zum Lesen und schreiben hat. Wenn der Benutzer beispielsweise "Matt" ist, sollte der Pfad C:\\Users\\Matt\\AppData\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen. Und falls vorhanden, sollten der Pfad C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen.

### Ereignis-ID 9005

VM-Name konnte nicht aus der Konfiguration abgerufen werden. Gast-Installationsprogramm kann nicht gestartet werden. MED-V kann nicht aktualisiert werden – kein Host Netzwerk erkannt.

<a href="" id="description"></a>**Beschreibung**  
Der Drucker Umleitungsdienst konnte den Med-v-Arbeitsbereichsnamen nicht aus der Med-v-Konfiguration abrufen und kann Windows Virtual PC nicht informieren, um das Installationsprogramm auf dem Med-v-Gast zu starten.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass der Name des MED-V-Arbeitsbereichs festgesetzt ist und er dem Namen eines virtuellen Computers im C:\\Users\\- &lt; *Benutzer* &gt; \\Virtual Machines-Verzeichnis entspricht. Der Name des MED-V-Arbeitsbereichs befindet sich unter HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Wenn der Benutzer beispielsweise "Matt" ist und der Arbeitsbereichsname "mattsworkspace" lautet, sollte der Wert von HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name "mattsworkspace" sein, und es sollte eine Datei mit dem Namen C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.

### Anwendungsveröffentlichung

### Ereignis-ID 10015

Beim Abgleichvorgang ist ein Dateisystemfehler aufgetreten. Der Prozess "abstimmen" verarbeitet nicht den Datei &lt; *Namen* &gt; , sondern verarbeitet weiterhin alle anderen Änderungen.

<a href="" id="description"></a>**Beschreibung**  
Beim Erstellen oder Löschen einer Verknüpfung ist ein nicht autorisierter Zugriffs-oder e/a-Fehler aufgetreten.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass auf den Dateipfad zugegriffen werden kann und der Benutzer über die Berechtigungen zum Erstellen oder Löschen der angegebenen Datei verfügt.

### Ereignis-ID 10021

Fehler &lt; *Fehler \ _information* &gt; für den Dateivorgangs &lt; *Vorgang \ _name* für &gt; den Datei &lt; *Namen* &gt; .

<a href="" id="description"></a>**Beschreibung**  
Beim Erstellen oder Löschen einer Verknüpfung ist ein nicht autorisierter Zugriffs-oder e/a-Fehler aufgetreten.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass auf den Dateipfad zugegriffen werden kann und der Benutzer über die Berechtigungen zum Erstellen oder Löschen der angegebenen Datei verfügt.

### Gast-Patches

### Ereignis-ID 11001

Nachricht zur Verwendung der Weckfunktion für Gäste

<a href="" id="description"></a>**Beschreibung**  
MedvHost.exe mit der Option "/GuestWakeup" falsch ausgeführt wurde oder der Befehl falsch formatiert ist.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass der Befehl mit dem folgenden Format ausgeführt wird:

Medvhost.exe/GuestWakeup/d: &lt; *Duration \ _in \ _minutes* &gt; /v: " &lt; *Arbeitsbereich \ _name* &gt; ", wobei

&lt;*Dauer \ _in \ _minutes* &gt; Gibt an, wie viele Minuten die virtuelle Maschine wach bleiben soll (Standard ist 240) und

&lt;*Arbeitsbereich \ _name* &gt; der Name des virtuellen Computers, der geweckt werden soll.

### Ereignis-ID 11002

MED-V kann nicht aktualisiert werden – kein Host Netzwerk erkannt.

<a href="" id="description"></a>**Beschreibung**  
Gast-Patches konnten nicht abgeschlossen werden, da keine Host-Netzwerkverbindung gefunden wurde.

<a href="" id="solution"></a>**Lösung**  
Verbinden Sie den MED-V-Host mit einer aktiven Netzwerkverbindung, bevor Sie den Gast-Patch ausführen.

### Ereignis-ID 11003

Der MED-V-Host, der nicht auf einem/C-powerFailed ausgeführt wird, kann nicht aktualisiert werden, um einen Kanalserver zu erstellen.

<a href="" id="description"></a>**Beschreibung**  
Guest-Patches konnten nicht abgeschlossen werden, da der Host anscheinend auf Akkustrom und nicht auf einem Netzkabel läuft.

<a href="" id="solution"></a>**Lösung**  
Verbinden Sie den Hostcomputer mit einem Netzkabel, bevor Sie den Gast Patchen ausführen.

### Client-UX

### Ereignis-ID 14003

Die folgende Tray-Statusmeldung war zu lang und konnte nicht angezeigt werden: &lt; *Tray \ _status \ _message*&gt;

<a href="" id="description"></a>**Beschreibung**  
MED-V hat eine unerwartete Zeichenfolge erstellt, die für die QuickInfo-oder Sprechblasenmeldung der Taskleiste zu lang war. Daher wurde die angezeigte Nachricht abgeschnitten.

<a href="" id="solution"></a>**Lösung**  
Dies ist ein seltener Fehler, der auftreten kann, wenn MED-V den QuickInfo-Text nach dem Zufallsprinzip erstellt. Es gibt keine Lösung.

### Ereignis-ID 14004

MED-V wurde aufgrund einer nicht behandelten Ausnahme angehalten.

<a href="" id="description"></a>**Beschreibung**  
Eine nicht behandelte Ausnahme hat dazu geführt, dass MED-V unerwartet beendet wird.

<a href="" id="solution"></a>**Lösung**  
Starten Sie MED-V neu.

### Ereignis-ID 14005

Der Server hat versucht, Mutex zu erstellen, aber bereits vorhanden.

<a href="" id="description"></a>**Beschreibung**  
Eine zweite Instanz von MedvHost.exe bleibt im Arbeitsspeicher hängen.

<a href="" id="solution"></a>**Lösung**  
Öffnen Sie Task Manager, und beenden Sie alle MedvHost.exe Prozesse.

### Ereignis-ID 14006

Fehler beim Ändern oder Löschen der Registrierungswert &lt; *Registrierung \ _Value* &gt; .

<a href="" id="description"></a>**Beschreibung**  
MED-V kann den angegebenen Eintrag in der Registrierung nicht ändern.

<a href="" id="solution"></a>**Lösung**  
Stellen Sie sicher, dass Sie MED-V mit administrativen Anmeldeinformationen installieren oder deinstallieren.

### Ereignis-ID 14007

Die angegebene Datei ( &lt; *filename* &gt; ) ist ungültig.

<a href="" id="description"></a>**Beschreibung**  
Während der Installation oder Deinstallation wurde eine beschädigte temporäre Datei an den MED-V-Host übergeben.

<a href="" id="solution"></a>**Lösung**  
Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut.

### Ereignis-ID 14008

Datei nicht gefunden: &lt; *Dateiname* &gt; .

<a href="" id="description"></a>**Beschreibung**  
Während der Installation oder Deinstallation wurde ein Pfad einer erforderlichen temporären Datei nicht gefunden.

<a href="" id="solution"></a>**Lösung**  
Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut.

### Ereignis-ID 14009

Parameterdatei Dateiname kann nicht gelesen werden &lt; *filename* &gt; .

<a href="" id="description"></a>**Beschreibung**  
Während des Installations-oder Deinstallationsvorgangs konnte MED-V keine temporäre Datei lesen.

<a href="" id="solution"></a>**Lösung**  
Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut. Stellen Sie außerdem sicher, dass der Benutzer über die erforderlichen Rechte und Berechtigungen für den temporären Ordner verfügt.

### Ereignis-ID 14010

Fehler beim Deserialisieren der Parameterdatei &lt; *Dateiname* &gt; .

<a href="" id="description"></a>**Beschreibung**  
Während des Installations-oder Deinstallationsprozesses hat MED-V eine beschädigte temporäre Datei gefunden.

<a href="" id="solution"></a>**Lösung**  
Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut. Stellen Sie außerdem sicher, dass der Benutzer über die erforderlichen Rechte und Berechtigungen für den temporären Ordner verfügt.

### Ereignis-ID 14011

Unerwarteter Fehler beim Deserialisieren der Parameterdatei &lt; *Dateiname* &gt; .

<a href="" id="description"></a>**Beschreibung**  
Während des Installations-oder Deinstallationsprozesses hat MED-V eine beschädigte temporäre Datei gefunden.

<a href="" id="solution"></a>**Lösung**  
Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut. Stellen Sie außerdem sicher, dass der Benutzer über die erforderlichen Rechte und Berechtigungen für den temporären Ordner verfügt.

### Ereignis-ID 14012

Unerwarteter Fehler, wenn Einstellungs Rechte für Ordner &lt; *Ordner \ _name* &gt; für Benutzer Benutzer &lt; *Name* &gt; .

<a href="" id="description"></a>**Beschreibung**  
Es tritt ein Fehler auf, wenn MED-V während der Installation nicht in der Lage ist, Rechte und Berechtigungen für bestimmte Ordner festzulegen.

<a href="" id="solution"></a>**Lösung**  
Überprüfen Sie die Administratorrechte für die folgenden Ordner:

@"%ProgramData%\\Microsoft\\Medv\\AllUsers"

@"%ProgramData%\\Microsoft\\Medv\\MedvLock"

@"%ProgramData%\\Microsoft\\Medv\\Monitoring"

### Ereignis-ID 14013

Unerwarteter Fehler beim Erstellen einer Sperrdatei.

<a href="" id="description"></a>**Beschreibung**  
Es tritt ein Fehler auf, wenn MED-V während der Installation keine Datei im @ "%ProgramData%\\Microsoft\\Medv\\MedvLock"-Ordner erstellen kann.

<a href="" id="solution"></a>**Lösung**  
Überprüfen Sie die Administratorrechte für den MedvLock-Ordner.

## Verwandte Themen


[Problembehandlung für MED-V](troubleshooting-med-vmedv2.md)

 

 





