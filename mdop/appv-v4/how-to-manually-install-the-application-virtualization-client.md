---
title: So installieren Sie Application Virtualization Client manuell
description: So installieren Sie Application Virtualization Client manuell
author: dansimp
ms.assetid: bb67f70b-d525-4317-b254-e4f084c717ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cb41b5e51bd33c377b17c088e97cb54f1a57685
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806964"
---
# So installieren Sie Application Virtualization Client manuell

Es gibt zwei Arten von Application Virtualization Client-Komponenten: den Application Virtualization Desktop Client, der für die Installation auf Desktopcomputern vorgesehen ist, und den Application Virtualization Client für Remotedesktopdienste (ehemals Terminal Dienste), den Sie auf Servern mit dem Host für Remotedesktopsitzungen installieren können. Obwohl die beiden Client Installationsprogramme unterschiedlich sind, können Sie das folgende Verfahren verwenden, um den Application Virtualization-Desktop Client auf einem einzelnen Desktopcomputer oder dem Application Virtualization Client für Remote Desktop Dienste auf einem einzigen Host für Remotedesktopsitzungen-Server manuell zu installieren. In einer Produktionsumgebung wird der Application Virtualization-Desktop Client höchstwahrscheinlich auf mehreren Desktopcomputern mit einem automatisierten Skript Installationsvorgang installiert. Informationen dazu, wie Sie mehrere Clients mithilfe eines Skript Installationsprozesses installieren, finden Sie unter [so wird es gemacht: Installieren des Clients mithilfe der Befehlszeile](how-to-install-the-client-by-using-the-command-line-new.md).

**Hinweis:**  
1. Wenn Sie den Application Virtualization-Client für Remote Desktop Dienste-Software auf einem Host für Remotedesktopsitzungen-Server installieren, empfehlen Sie Benutzern, die über eine offene RDP-oder ICA-Clientsitzung mit dem Host für Remotedesktopsitzungen verfügen, ihre Arbeit zu speichern und ihre Sitzungen zu schließen. In einer Remote Desktop Sitzung können Sie den Client manuell installieren. Weitere Informationen zum Upgrade des Clients finden Sie unter [Aktualisieren des Application Virtualization-Clients](how-to-upgrade-the-application-virtualization-client.md).

2. Wenn auf dem Computer des Benutzers eine Konfiguration vorhanden ist, die vom Client Installationspfad abhängt, beachten Sie, dass der 4,5-Client für Application Virtualization (App-V) einen anderen Installationsordner als frühere Versionen verwendet. Standardmäßig wird eine neue Installation des Application Virtualization (App-V) 4,5-Clients im \\Program c:\\Programme\\Microsoft Application Virtualization Client-Ordner installiert. Wenn eine frühere Version des Clients bereits installiert ist, führt die Installation des App-V-Clients ein Upgrade in den vorhandenen Installationsordner durch.

**Hinweis:**  
Für App-v Version 4,6 und höher wird beim Installieren des App-v-Clients SFTLDR.DLL im Windows\\system32-Verzeichnis installiert. Wenn der App-V-Client auf einem 64-Bit-System installiert ist, wird SFTLDR\_WOW64.DLL im Windows\\SysWOW64-Verzeichnis installiert.

**So installieren Sie Application Virtualization Desktop Client manuell**

1. Nachdem Sie die richtige Installationsarchiv Datei abgerufen und auf Ihrem Computer gespeichert haben, vergewissern Sie sich, dass Sie mit einem Konto angemeldet sind, das über Administratorrechte auf dem Computer verfügt, und doppelklicken Sie auf die Datei, um das Archiv zu erweitern.

2. Wählen Sie den Ordner aus, in dem die Dateien gespeichert werden sollen, und öffnen Sie dann den Ordner, nachdem die Dateien kopiert wurden.

3. Lesen Sie gegebenenfalls die Anmerkungen zu dieser Version.

4. Suchen Sie nach der setup.exe-Datei, und doppelklicken Sie auf setup.exe, um die Installation zu starten.

5. Der Assistent überprüft das System, um sicherzustellen, dass alle erforderlichen Software installiert ist, und wenn einer der folgenden Punkte fehlt, werden Sie vom Assistenten automatisch aufgefordert, Sie zu installieren:

    - Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)

    - Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)

    - Microsoft-Anwendungsfehler Berichterstattung

    **Hinweis:**  
    Für App-V, Version 4,6 und höher, wird der Assistent auch Microsoft Visual C++ 2008 SP1 Redistributable Package (x86) installieren.

    Weitere Informationen zur Installation von Microsoft Visual C++ 2008 SP1 Redistributable Package (x86) finden Sie unter [https://go.microsoft.com/fwlink/?LinkId=150700](https://go.microsoft.com/fwlink/?LinkId=150700) .

    Wenn Sie dazu aufgefordert werden, klicken Sie auf **Installieren**. Der Installationsfortschritt wird angezeigt, und der Status wechselt von " **Ausstehend** " in " **Installieren**". Der Installationsstatus ändert sich **in erfolgreich,** wenn jeder Schritt erfolgreich abgeschlossen wurde.

6. Wenn der **Microsoft Application Virtualization Desktop Client – InstallShield-Assistent** angezeigt wird, klicken Sie auf **weiter**.

7. Der Bildschirm **Lizenzvertrag** wird angezeigt. Lesen Sie den Lizenzvertrag, und wenn Sie damit einverstanden sind, klicken Sie auf **Ich stimme den Bedingungen des Lizenzvertrags** zu, und klicken Sie dann auf **weiter**.

   Optional können Sie auf die Schaltfläche klicken, um die Datenschutzerklärung zu lesen. Sie müssen mit dem Internet verbunden sein, um auf die Datenschutzerklärung zugreifen zu können.

8. Wählen Sie auf dem Bildschirm **Setup-Typ** den Setuptyp aus. Klicken Sie auf **typisch** , um die Standardprogramm Werte zu verwenden, oder klicken Sie auf **Benutzerdefiniert** , wenn Sie die Programmeinstellungen während der Installation konfigurieren möchten.

9. Wenn Sie " **Standard**" auswählen, wird auf dem nächsten Bildschirm die **Installation des Programms bereit**angezeigt. Klicken Sie auf **Installieren** , um mit der Installation zu beginnen.

10. Wenn Sie **Benutzerdefiniert**auswählen, wird der Bildschirm **Zielordner** angezeigt.

11. Klicken Sie auf dem Bildschirm **Zielordner** auf **weiter** , um den Standardordner zu übernehmen, oder auf **ändern** , um den Bildschirm **aktuellen Zielordner ändern** anzuzeigen. Navigieren Sie zu oder geben Sie im Feld **Ordner Name** den Zielordner ein, klicken Sie auf **OK**, und klicken Sie dann auf **weiter**.

12. Klicken Sie im Bildschirm **Application Virtualization Data Location** auf **Next (weiter** ), um die Standarddatenspeicher Orte zu übernehmen, oder führen Sie die folgenden Aktionen aus, um zu ändern, wo die Daten gespeichert sind:

    1. Klicken Sie auf **ändern**, und navigieren Sie dann zu, oder geben Sie im Feld **globale Datenposition** den Zielordner für den globalen Datenspeicherort ein, und klicken Sie auf **OK**. Im globalen Datenverzeichnis speichert Application Virtualization Desktop Client die Daten, die von allen Benutzern auf dem Computer freigegeben werden, wie OSD-Dateien und SFT-Dateidaten.

    2. Wenn Sie den zu verwendenden Laufwerkbuchstaben ändern möchten, wählen Sie den bevorzugten Laufwerkbuchstaben aus der Dropdownliste aus.

    3. Geben Sie einen neuen Pfad zum Speichern der benutzerspezifischen Daten im Feld **benutzerspezifische Datenposition** ein, wenn Sie die Datenposition ändern möchten. Im Benutzerdatenverzeichnis speichert Application Virtualization Desktop Client benutzerspezifische Informationen, wie persönliche Einstellungen für virtualisierte Anwendungen.

       **Hinweis:**  
       Dieser Pfad muss für jeden Benutzer unterschiedlich sein, daher sollte er eine benutzerspezifische Umgebungsvariable oder ein zugeordnetes Laufwerk oder etwas anderes enthalten, das in einen eindeutigen Pfad für jeden Benutzer aufgelöst wird.

    4. Wenn Sie die gewünschten Änderungen vorgenommen haben, klicken Sie auf **weiter**.

13. Auf dem Bildschirm " **Cachegrößen Einstellungen** " können Sie die Standardcachegröße akzeptieren oder ändern. Klicken Sie auf eines der folgenden Optionsfelder, um auszuwählen, wie der Cache Speicherplatz verwaltet werden soll:

    1. **Verwenden Sie die maximale Cachegröße**. Geben Sie einen numerischen Wert von 100 – 1048576 (1 TB) im Feld **Maximale Größe (MB)** ein, um die maximale Größe des Caches anzugeben.

    2. **Grenzwert für freien Speicherplatz verwenden**. Geben Sie einen numerischen Wert ein, um die Menge an freiem Speicherplatz in MB anzugeben, die der Application Virtualization-Client auf dem Datenträger verfügbar bleiben muss. Dadurch kann der Cache größer werden, bis der freie Speicherplatz diesen Grenzwert erreicht hat. Der im **verbleibenden freien Speicherplatz** angezeigte Wert gibt an, wie viel Speicherplatz zurzeit nicht verwendet wird.

    **Wichtig**  
    Wenn Sie sicherstellen möchten, dass der Cache über genügend Speicherplatz für alle Pakete verfügt, die möglicherweise bereitgestellt werden, verwenden Sie die Einstellung Speicher **Platz für freien Speicherplatz verwenden** , wenn Sie den Client so konfigurieren, dass der Cache nach Bedarf erweitert werden kann. Sie können aber auch im voraus ermitteln, wie viel Speicherplatz für den App-V-Cache benötigt wird, und die Cachegröße zur Installationszeit entsprechend festlegen. Weitere Informationen zum Cache Space Management-Feature finden Sie im Microsoft Application Virtualization (App-V)-Betriebshandbuch unter so wird es **gemacht: Verwenden des Cache-Speicherplatz Verwaltungsfeatures**.

    Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

14. In den folgenden Abschnitten des Bildschirms zur **Laufzeit-Paket Richtlinienkonfiguration** können Sie die Parameter ändern, die sich darauf auswirken, wie sich der Application Virtualization-Client während der Laufzeit verhält:

    1. **Stamm der Anwendungsquelle**. Gibt den Speicherort von SFT-Dateien an. Bei Verwendung werden die Abschnitte Protokoll, Server und Port der CODEBASE-HREF-URL in der OSD-Datei außer Kraft gesetzt.

    2. **Anwendungsautorisierung** Wenn **Benutzerautorisierung erforderlich ist, auch wenn zwischengespeichert** aktiviert ist, müssen Benutzer eine Verbindung mit einem Server herstellen und Ihre Anmeldeinformationen mindestens einmal überprüfen, bevor Sie die einzelnen virtuellen Anwendungen starten können.

    3. **Streaming aus Datei zulassen**. Gibt an, ob das Streaming aus einer Datei aktiviert wird, unabhängig davon, wie das Stamm Feld der **Anwendungsquelle** verwendet wird. Wenn diese Option nicht aktiviert ist, ist das Streaming aus Dateien deaktiviert. Dies muss überprüft werden, wenn der **Anwendungsquellen Stamm** einen UNC-Pfad im Formular \\\\server\\share. enthält.

    4. **Anwendung automatisch laden** Steuert, wann und wie das automatische Laden von Anwendungen im Hintergrund ausgeführt wird.

       **Hinweis:**  
       Wenn Sie den App-V-Client für die Verwendung mit einem schreibgeschützten Cache installieren, beispielsweise bei einer VDI-Server Implementierung, legen Sie die Anwendungen **auf Automatisches Laden** so, dass **Anwendungen nicht automatisch geladen** werden, um zu verhindern, dass der Client versucht, Anwendungen im schreibgeschützten Cache zu aktualisieren.

    Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

15. Aktivieren Sie auf dem Bildschirm **Veröffentlichungsserver** das Kontrollkästchen **jetzt einen Veröffentlichungsserver einrichten** , wenn Sie einen Veröffentlichungsserver definieren möchten, oder klicken Sie auf **weiter** , wenn Sie diesen Vorgang später ausführen möchten. Um einen Veröffentlichungsserver zu definieren, geben Sie die folgenden Informationen an:

    1. **Anzeigename**– geben Sie den Namen ein, der für den Server angezeigt werden soll.

    2. **Typ**– wählen Sie in der Dropdownliste der Servertypen den Servertyp aus.

    3. **Hostname** und **Port**– geben Sie den Hostnamen und den Port in die entsprechenden Felder ein. Wenn Sie in der Dropdownliste einen Servertyp auswählen, wird das Feld Port automatisch mit den Standardportnummern ausgefüllt. Wenn Sie eine Portnummer ändern möchten, klicken Sie in der Liste auf den Servertyp, und ändern Sie die Portnummer entsprechend Ihren Anforderungen.

    4. **Path**: Wenn Sie entweder den **Standard-HTTP-Server** oder den **erweiterten Security http-Server**ausgewählt haben, müssen Sie den vollständigen Pfad zu der XML-Datei eingeben, die Veröffentlichungsdaten in diesem Feld enthält. Wenn Sie entweder **Application Virtualization Server** oder **Enhanced Security Application Virtualization Server**auswählen, ist dieses Feld nicht aktiv.

    5. Diesen **Server automatisch kontaktieren, um die Einstellungen zu aktualisieren, wenn sich ein Benutzer anmeldet**– aktivieren Sie dieses Kontrollkästchen, wenn Sie möchten, dass dieser Server automatisch abgefragt wird, wenn sich Benutzer beim Application Virtualization-Client bei Ihrem Konto anmelden.

    6. Klicken Sie nach Abschluss der Konfigurationsschritte auf **weiter**.

16. Klicken Sie auf dem Bildschirm **bereit zum Installieren des Programms** auf **Installieren**. Es wird ein Bildschirm mit dem Status der Installation angezeigt.

17. Klicken Sie auf dem Bildschirm **Installationsassistent abgeschlossen** auf **Fertig stellen**.

    **Hinweis:**  
    Wenn die Installation aus irgendeinem Grund fehlschlägt, müssen Sie den Computer möglicherweise neu starten, bevor Sie die Installation erneut versuchen.

## Verwandte Themen

[So installieren Sie den Client über die Befehlszeile](how-to-install-the-client-by-using-the-command-line-new.md)

[Übersicht über die Szenarien für die eigenständige Bereitstellung](stand-alone-delivery-scenario-overview.md)
