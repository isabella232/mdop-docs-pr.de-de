---
title: Erstellen und Verwalten virtualisierter App-V 5.1-Anwendungen
description: Erstellen und Verwalten virtualisierter App-V 5.1-Anwendungen
author: dansimp
ms.assetid: 26be4331-88eb-4cfb-9d82-e63d7ee54576
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 207529fb5d5333694d31a82f44f08b35513dd4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805915"
---
# Erstellen und Verwalten virtualisierter App-V 5.1-Anwendungen


Nachdem Sie den Microsoft Application Virtualization (App-V) 5,1-Sequenzer ordnungsgemäß bereitgestellt haben, können Sie ihn zum Überwachen und Aufzeichnen des Installations-und Setupprozesses verwenden, damit eine Anwendung als virtualisierte Anwendung ausgeführt werden kann.

**Hinweis**  Weitere Informationen zum Konfigurieren des App-V 5,1-Sequencers, zum Sequenzieren bewährter Methoden und ein Beispiel für das Erstellen und Aktualisieren einer virtuellen Anwendung finden Sie im [Microsoft Application Virtualization 5,0-Sequenzierungs Handbuch](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V%205.0%20Sequencing%20Guide.docx).

**Hinweis** App-V 5. x Sequencer kann keine Anwendungen mit Dateinamen abgleichen, die "CO_ &lt; x &gt; " entsprechen, wobei x eine beliebige Zahl ist. Fehler 0x8007139F wird generiert.

## Sequenzieren einer Anwendung


Mit dem App-V 5,1-Sequenzer können Sie die folgenden Aufgaben ausführen:

-   Erstellen Sie virtuelle Pakete, die auf Computern mit dem App-V 5,1-Client bereitgestellt werden können.

-   Aktualisieren vorhandener Pakete Sie können ein vorhandenes Paket auf dem Computer erweitern, auf dem der Sequencer ausgeführt wird, und dann die Anwendung aktualisieren, um eine neuere Version zu erstellen.

-   Bearbeiten von Konfigurationsinformationen, die einem vorhandenen Paket zugeordnet sind. So können Sie beispielsweise eine Verknüpfung hinzufügen oder eine Dateitypzuordnung ändern.

    **Hinweis**  Sie müssen Verknüpfungen erstellen und diese an einem verfügbaren Netzwerkspeicherort speichern, um Roaming zu ermöglichen. Wenn eine Verknüpfung erstellt und an einem privaten Speicherort gespeichert wird, muss das Paket lokal auf dem Computer veröffentlicht werden, auf dem der App-V 5,1-Client ausgeführt wird.
 
-   Umwandeln vorhandener virtueller Pakete

Der Sequencer verwendet das% **tmp% \ \ Scratch** oder **% Temp% \ \ Scratch** -Verzeichnis und das **Temp** -Verzeichnis, um temporäre Dateien während der Sequenzierung zu speichern. Auf dem Computer, auf dem der Sequencer ausgeführt wird, sollten Sie diese Verzeichnisse mit freiem Speicherplatz konfigurieren, der den geschätzten Anwendungs Installationsanforderungen entspricht. Das Konfigurieren der temporären Verzeichnisse und des temporären Verzeichnisses auf unterschiedlichen Festplattenpartitionen kann zur Verbesserung der Leistung während der Sequenzierung beitragen.

Wenn Sie den Sequencer zum Erstellen einer neuen virtuellen Anwendung verwenden, werden die folgenden aufgelisteten Dateien erstellt. Diese Dateien umfassen das App-V 5,1-Paket.

-   MSI-Datei. Diese Windows Installer-Datei (MSI) wird vom Sequencer erstellt und zum Installieren des virtuellen Pakets auf Zielcomputern verwendet.

-   Report.xml-Datei. In dieser Datei speichert der Sequencer alle Probleme, Warnungen und Fehler, die während der Sequenzierung ermittelt wurden. Nachdem das Paket erstellt wurde, werden die Informationen angezeigt. Diesen Bericht können Sie uns zur Diagnose und zur Problembehebung entnehmen.

-   AppV-Datei. Dies ist die virtuelle Anwendungsdatei.

-   Konfigurationsdatei für die Bereitstellung. Die Konfigurationsdatei für die Bereitstellung bestimmt, wie die virtuelle Anwendung auf den Zielcomputern bereitgestellt wird.

-   Konfigurationsdatei für Benutzer. Die Benutzerkonfigurationsdatei legt fest, wie die virtuelle Anwendung auf Zielcomputern ausgeführt werden soll.

**Wichtig**  Sie müssen die Ordner% tmp% und% Temp% konfigurieren, die vom Paket Konverter als sicherer Speicherort und Verzeichnis verwendet werden. Ein sicherer Standort kann nur von einem Administrator abgerufen werden. Wenn Sie das Paket sequenzieren, sollten Sie darüber hinaus das Paket an einem sicheren Speicherort speichern, oder Sie müssen sicherstellen, dass kein anderer Benutzer während des Konvertierungs-und Überwachungsprozesses angemeldet werden darf. 

Das Dialogfeld " **Optionen** " in der Sequencer-Konsole enthält die folgenden Registerkarten:

-   **Allgemein**. Verwenden Sie diese Registerkarte, um die Ausführung von Microsoft-Updates während der Sequenzierung zu aktivieren. Wählen Sie **Paket Version an filename anfügen** aus, um die Sequenz so zu konfigurieren, dass dem virtualisierten Paket, das sequenziert wird, eine Versionsnummer hinzugefügt wird. Wählen Sie **der Quelle von Paket Beschleunigern immer vertrauen** aus, um virtualisierte Pakete mithilfe eines Paket Beschleunigers zu erstellen, ohne zur Autorisierung aufgefordert zu werden.

    **Wichtig**  Mit App-v 4.6 erstellte Paket Beschleuniger werden von App-v 5,1 nicht unterstützt.     

-   **Analysieren von Elementen** Auf dieser Registerkarte werden die zugehörigen Dateipfad-Speicherorte angezeigt, die in der virtuellen Umgebung analysiert oder in Tokens umgewandelt werden. Token sind hilfreich beim Hinzufügen von Dateien auf der Registerkarte **Paketdateien** in der **erweiterten Bearbeitung**.

-   **Ausschlusselemente**. Auf dieser Registerkarte können Sie angeben, welche Ordner und Verzeichnisse während der Sequenzierung nicht überwacht werden sollen. Wenn Sie lokale Anwendungsdaten hinzufügen möchten, die im lokalen app-Datenordner im Paket gespeichert sind, klicken Sie auf **neu** , und geben Sie den Speicherort und den zugehörigen **Zuordnungstyp**an. Diese Option ist für einige Pakete erforderlich.

App-V 5,1 unterstützt Anwendungen, die Microsoft Windows-Dienste umfassen. Wenn eine Anwendung einen Windows-Dienst enthält, wird der Dienst in das sequenzierte virtuelle Paket aufgenommen, solange er während der Überwachung durch den Sequencer installiert wird. Wenn eine virtuelle Anwendung beim anfänglichen ausführen einen Windows-Dienst erstellt, muss die Anwendung später nach der Installation ausgeführt werden, während der Sequencer überwacht wird, damit der Windows-Dienst dem Paket hinzugefügt wird. Nur Dienste, die unter dem lokalen System Konto ausgeführt werden, werden unterstützt. Dienste, die für Autostart oder verzögerter Autostart konfiguriert sind, werden gestartet, bevor die erste virtuelle Anwendung in einem Paket innerhalb der virtuellen Umgebung des Pakets ausgeführt wird. Windows-Dienste, die so konfiguriert sind, dass Sie bei Bedarf von einer Anwendung gestartet werden, werden gestartet, wenn die virtuelle Anwendung im Paket den Dienst über API-Aufruf startet.

[So sequenzieren Sie eine neue Anwendung mit App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)

## <a href="" id="---------app-v-5-1-shell-extension-support"></a> App-V 5.1-Unterstützung für Shell-Erweiterungen


App-V 5.1 unterstützt Shell-Erweiterungen. Shell-Erweiterungen werden während der Sequenzierung erkannt und in das Paket eingebettet.

Shell-Erweiterungen werden während des Sequenz Prozesses automatisch in das Paket eingebettet. Wenn das Paket veröffentlicht wird, gibt die Shell-Erweiterung Benutzern dieselbe Funktionalität wie bei der lokalen Installation der Anwendung.

**Voraussetzungen für die Verwendung von Shell-Erweiterungen:**

-   Pakete, die eingebettete Shell-Erweiterungen enthalten, müssen global veröffentlicht werden. Die Anwendung erfordert keine zusätzliche Einrichtung oder Konfiguration auf dem Client, um die Shell-Erweiterungsfunktion zu aktivieren.

-   Die "Bitanzahl" der Anwendung, des Sequencers und des App-V-Clients müssen übereinstimmen, oder die Shell-Erweiterungen funktionieren nicht. Beispiel:

    -   Die Version der Anwendung ist 64-Bit.

    -   Der Sequencer wird auf einem 64-Bit-Computer ausgeführt.

    -   Das Paket wird an einen 64-Bit-App-V-Clientcomputer übermittelt.

In der folgenden Tabelle sind die unterstützten Shell-Erweiterungen aufgeführt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Handler</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Kontextmenü Handler</p></td>
<td align="left"><p>Fügt dem Kontextmenü Menüelemente hinzu. Sie wird aufgerufen, bevor das Kontextmenü angezeigt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Drag & Drop-Handler</p></td>
<td align="left"><p>Steuert die Aktion, bei der mit der rechten Maustaste, ziehen und ablegen und das Kontextmenü geändert wird, das angezeigt wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ablegen eines Ziel Handlers</p></td>
<td align="left"><p>Steuert die Aktion, nachdem ein Datenobjekt gezogen und über ein Ablageziel wie eine Datei abgelegt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Datenobjekt-Handler</p></td>
<td align="left"><p>Steuert die Aktion, nachdem eine Datei in die Zwischenablage kopiert oder auf einem Ablageziel gezogen und abgelegt wurde. Sie kann dem Ablageziel zusätzliche Zwischenablageformate zur Verfügung stellen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eigenschaftentabellen-Handler</p></td>
<td align="left"><p>Ersetzt oder fügt Seiten in das DialogfeldEigenschaften Fenster eines Objekts ein.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Infotipp-Handler</p></td>
<td align="left"><p>Ermöglicht das Abrufen von Flags und Infotipp-Informationen für ein Element und das Anzeigen des Elements in einer Popup-QuickInfo, wenn Sie den Mauszeiger bewegen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spalten Handler</p></td>
<td align="left"><p>Ermöglicht das Erstellen und Anzeigen benutzerdefinierter Spalten in der <strong> Windows-Explorer-Detailansicht </strong> . Sie kann zum Erweitern von Sortierung und Gruppierung verwendet werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Vorschauhandler</p></td>
<td align="left"><p>Ermöglicht das Anzeigen einer Vorschau einer Datei im Vorschaubereich von Windows-Explorer.</p></td>
</tr>
</tbody>
</table>

## Unterstützung für die Dateierweiterung beim Schreiben (Kuh)

Die Dateierweiterungen Copy on Write (Cow) ermöglichen es App-V 5,1, dynamisch an bestimmte Speicherorte zu schreiben, die im virtuellen Paket enthalten sind, während es verwendet wird.

In der folgenden Tabelle werden die Dateitypen angezeigt, die in einem virtuellen Paket unter dem VFS-Verzeichnis vorhanden sein können, aber auf dem Computer, auf dem der App-V 5,1-Client ausgeführt wird, nicht aktualisiert werden können. Alle anderen Dateien und Verzeichnisse können geändert werden.

| Dateityp     |               |               |               |               |               |
|------------   |-------------  |-------------  |------------   |------------   |------------   |
| . acm          | . ASA          | .asp          | . aspx         | AX           | BAT          |
| .cer          | .chm          | . CLB          | .cmd          | .cnt          | . cnv          |
| .com          | .cpl          | . CPX          | .crt          | .dll          | .drv          |
| . ESC          | EXE          | .fon          | .grp          | .hlp          | .hta          |
| . IME          | INF          | INS          | .isp          | . its          | .js           |
| .jse          | .lnk          | .msc          | .msi          | .msp          | .mst          |
| . MUI          | . nls          | .ocx          | . PAL          | .pcd          | .pif          |
| .reg          | .scf          | .scr          | . SCT          | .shb          | .shs          |
| .sys          | . tlb          | . tsp          | .url          | .vb           | .vbe          |
| .vbs          | .vsmacros     | .ws           | .wsf          | .wsh          |               |


## Ändern eines vorhandenen virtuellen Anwendungspakets


Sie können den Sequencer verwenden, um ein vorhandenes Paket zu ändern. Der Computer, auf dem Sie dies tun, sollte der Chiparchitektur des Computers entsprechen, den Sie zum Erstellen der Anwendung verwendet haben. Wenn Sie beispielsweise ein Paket zunächst auf einem Computer mit einem 64-Bit-Betriebssystem sequenziert haben, sollten Sie das Paket auf einem Computer ändern, auf dem ein 64-Bit-Betriebssystem ausgeführt wird.

[So ändern Sie ein vorhandenes virtuelles Anwendungspaket](how-to-modify-an-existing-virtual-application-package-51.md)

## Erstellen einer Projektvorlage


Bei einer appvt-Datei handelt es sich um eine Projektvorlage, die verwendet werden kann, um häufig angewendete, angepasste Einstellungen zu speichern. Sie können diese Einstellungen dann einfacher für zukünftige Sequenzen verwenden.

App-v 5,1-Projektvorlagen unterscheiden sich von App-v 5,1-Anwendungs Beschleunigern, da App-v 5,1-Anwendungs Beschleuniger anwendungsspezifisch sind und App-v 5,1-Projektvorlagen auf mehrere Anwendungen angewendet werden können. Darüber hinaus können Sie keine Projektvorlage verwenden, wenn Sie ein Paket Beschleuniger zum Erstellen eines virtuellen Anwendungspakets verwenden. Die folgenden allgemeinen Einstellungen werden mit einer App-V 5,1-Projektvorlage gespeichert:

Eine Vorlage kann mehrere Einstellungen wie folgt angeben und speichern:

-   **Erweiterte Überwachungsoptionen**. Ermöglicht die Ausführung von Microsoft Update während der Überwachung. Speichert Einstellungen für lokale interaktionsoptionen zulassen

-   **Allgemeine Optionen**. Aktiviert die Verwendung von **Windows Installer**und **fügt die Paket Version an filename an**.

-   **Ausschlusselemente.** Enthält die Ausschlussmuster Liste.

[So erstellen und verwenden Sie eine Projektvorlage](how-to-create-and-use-a-project-template51.md)

## Erstellen eines Paket Beschleunigers


**Hinweis**  Paket Beschleuniger, die mit einer früheren Version von App-v erstellt wurden, müssen mit App-v 5,1 neu erstellt werden.

Sie können App-V 5,1-Paket Beschleuniger verwenden, um automatisch neue virtuelle Anwendungspakete zu generieren. Nachdem Sie erfolgreich einen Paket Beschleuniger erstellt haben, können Sie den Paket Beschleuniger wieder verwenden und freigeben.

In einigen Fällen müssen Sie möglicherweise die Anwendung lokal auf dem Computer installieren, auf dem der Sequencer ausgeführt wird, um den Paket Beschleuniger zu erstellen. In solchen Fällen sollten Sie zunächst versuchen, den Paket Beschleuniger mit dem Installationsmedium zu erstellen. Wenn mehrere fehlende Dateien erforderlich sind, sollten Sie die Anwendung lokal auf dem Computer installieren, auf dem der Sequencer ausgeführt wird, und dann den Paket Beschleuniger erstellen.

Nachdem Sie erfolgreich einen Paket Beschleuniger erstellt haben, können Sie den Paket Beschleuniger wieder verwenden und freigeben. Das Erstellen von App-V 5,1-Paket Beschleunigern ist eine erweiterte Aufgabe. Paket Beschleuniger können Kennwort-und benutzerspezifische Informationen enthalten. Daher müssen Sie Paket Beschleuniger und die zugehörigen Installationsmedien an einem sicheren Speicherort speichern, und Sie sollten den Paket Beschleuniger nach der Erstellung digital signieren, damit der Herausgeber überprüft werden kann, wenn der App-V 5,1-Paket Beschleuniger angewendet wird.

[So erstellen Sie einen Package Accelerator](how-to-create-a-package-accelerator51.md)

[So erstellen Sie ein virtuelles Anwendungspaket mit einem App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)

## Sequenzer-Fehlerberichterstattung


Der App-V 5,1-Sequenzer kann häufige Sequenzierungs Probleme während der Sequenzierung erkennen. Auf der Seite " **Installationsbericht** " am Ende des Sequenz-Assistenten werden in Abhängigkeit vom Schweregrad des Problems diagnostische Nachrichten angezeigt, die in **Fehler**, **Warnungen**und **Informationen** kategorisiert sind.

Weitere Informationen zu Sequenz Fehlern finden Sie auch unter Verwendung der Windows-Ereignisanzeige.


## <a href="" id="other-resources-for-the-app-v-5-1-sequencer-"></a>Weitere Ressourcen für den App-V 5,1-Sequenzer


-   [Vorgänge für App-V 5.1](operations-for-app-v-51.md)

