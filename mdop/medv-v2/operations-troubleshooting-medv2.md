---
title: Problembehandlung bei Vorgängen
description: Problembehandlung bei Vorgängen
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804454"
---
# Problembehandlung bei Vorgängen


Dieses Thema enthält Informationen, die Sie bei der Behandlung allgemeiner operativer Probleme in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 verwenden können.

## Behandeln von Problemen bei MED-V-Vorgängen


Im folgenden finden Sie einige Probleme, die Endbenutzer beim Ausführen von MED-V und Lösungen zur Behebung dieser Probleme auftreten können:

Die **Dokumentations Umleitung schlägt fehl**. Dieses Problem tritt in der Regel auf, wenn der Ordner "eigene Dateien" des Endbenutzers auf einen Netzwerkspeicherort verweist. Das Erstellen einer Freigabe aus einem anderen freigegebenen Ordner wird von Windows nicht unterstützt. Wenn ein Laufwerk oder ein Ordner an den Gast umgeleitet wird, erstellt RDP\\Windows Virtual PC eine Freigabe für diesen Ordner. Wenn der Ordner "eigene Dateien" auf dem Host bereits auf eine Freigabe zeigt, kann RDP\\Windows Virtual PC daher keine Freigabe einer Freigabe erstellen.

Eine weitere mögliche Ursache für dieses Problem besteht darin, dass die Anmeldeinformationen, die zum Herstellen einer Verbindung mit der Netzwerkressource erforderlich sind, möglicherweise von den Domänenanmeldeinformationen des Benutzers abweichen. Möglicherweise erkennt MED-V, dass Dokumente auf dem Host umgeleitet werden, senden Sie diese Informationen an den Gast, und versuchen Sie dann, die Netzwerkressource erneut zu verbinden. Wenn sich die Anmeldeinformationen des Benutzers nicht authentifizieren, versucht MED-V möglicherweise nicht mehr, sich zu authentifizieren.

**Lösung**

Führen Sie eine der folgenden Aktionen aus, um dieses Problem zu beheben:

-   Setzen Sie das Stammverzeichnis des Benutzers in Active Directory. Der Gast und der Host sollten dann eine Verbindung mit der gleichen Netzwerkressource herstellen.

-   Anstatt den Ordner "eigene Dateien" an einen UNC-Pfad umzuleiten, ordnen Sie ihn einem Laufwerksbuchstaben zu (auf dem Host ordnen Sie ein Laufwerk zu, das auf die Netzwerkressource verweist). Der Ordner "eigene Dateien" kann dann so festgesetzt werden, dass der Laufwerkbuchstabe anstelle des UNC-Pfads verwendet wird. Der Gast wird dann wie erwartet auf das gleiche zugeordnete Laufwerk umgeleitet.

-   Erstellen Sie ein Startskript im Gast, das den Ordner "eigene Dateien" an die Netzwerkressource umleitet und bei Bedarf zusätzliche Anmeldeinformationen bereitstellt.

Die **URL-Umleitung schlägt fehl**. Eine URL, die Sie für die Umleitung vom Host zum Gast angegeben haben, wird nicht wie beabsichtigt umgeleitet oder gibt eine Fehlermeldung zurück, die angibt, dass die Website nicht vorhanden ist.

**Lösung**

Dieser Fehler kann auftreten, wenn in den URL-Umleitungsinformationen ein Rechtschreibfehler oder eine falsche Verwendung von Zeichen wie Sternchen (\ *) vorliegt. Überprüfen Sie den Registrierungswert auf URL-Umleitung, und korrigieren Sie alle Fehler.

Der Registrierungsschlüssel wird aufgerufen `RedirectUrls` und befindet sich normalerweise unter:

Computer\\HKEY\ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\userexperience

**Symbol in der Taskleiste irreführend**. Standardmäßig ist das Symbol, das auf der Taskleiste eines Endbenutzers für veröffentlichte Anwendungen und umgeleitete URLs angezeigt wird, das Symbol für Windows Virtual PC. Wenn ein Endbenutzer dieses Standardverhalten nicht kennt, kann er verwirrt werden, wenn Sie die Taskleiste suchen, um die Anwendung zu finden.

**Lösung**

Die einzige Möglichkeit, dieses Standardverhalten zu vermeiden, besteht darin, die Benutzereinstellungen für die Taskleisteneigenschaften wie folgt zu ändern:

1.  Klicken Sie mit der rechten Maustaste auf die Taskleiste, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld **Eigenschaften von Taskleiste und Startmenü** auf die Registerkarte **Taskleiste** .

3.  Wählen Sie in der Dropdownleiste für das Feld **Schaltflächen für die Taskleiste** die Option **nie kombinieren**aus.

4.  Klicken Sie auf **OK**.

Die erwarteten Symbole für veröffentlichte Anwendungen und umgeleitete URLs werden angezeigt.

**Warnung wird ausgegeben, wenn der zweite Benutzer versucht, sich anzumelden oder wenn der virtuelle Computer verwendet wird**. Eine Warnmeldung wird ausgegeben, wenn sich ein zweiter Benutzer bei einem Med-v-Arbeitsbereich anmeldet, während ein erster Benutzer noch Med-v ausführt. Die Warnung wird auch ausgegeben, wenn MED-V gestartet wird, während der virtuelle Computer verwendet wird, beispielsweise, wenn der virtuelle Computer über den Windows Virtual PC im **Startmenü** gestartet wurde. Wenn der Endbenutzer die Warnmeldung annimmt, wird MED-V heruntergefahren.

**Lösung**

Ein Endbenutzer muss sicherstellen, dass alle anderen Benutzer von MED-V abgemeldet werden, bevor Sie versuchen, sich anzumelden. Dadurch wird sichergestellt, dass keine andere Instanz von MED-V ausgeführt wird und dass Windows Virtual PC nicht die Kontrolle über den virtuellen Computer hat.

**Akustische Signale während der erstmaligen Einrichtung**. Gelegentlich werden Pieptöne abgehört, während MED-V beim erstmaligen Einrichten ausgeführt wird. Dies kann für einen Endbenutzer verwirrend sein. Die Pieptöne stammen vom virtuellen Computer, wenn bestimmte Aktionen wie das Herunterfahren ausgeführt werden.

**Lösung**

Sie können den Signalton Dienst beenden, indem Sie am Anfang jeder Startsequenz für den virtuellen Computer den Befehl "net stop Beep" angeben. Sie können den Signalton Dienst auch deaktivieren, indem Sie den Befehl "SC config Beep Start = disabled" angeben. Sie können diese Befehle entweder vor dem Versiegeln des Bilds oder als Teil von Sysprep angeben.

**Mehrere Netzwerkverbindungen, die für MED-V-Arbeitsbereiche im Überbrückungsmodus erstellt wurden**. Wenn die erstmalige Einrichtung einen MED-V-Arbeitsbereich erstellt, der für den NAT-Modus konfiguriert ist, wird nur eine einzige Netzwerkverbindung in Windows Virtual PC erstellt. Wenn allerdings das erstmalige Setup einen Med-v-Arbeitsbereich erstellt, der für den Überbrückungsmodus konfiguriert ist, wird für jeden auf dem Computer installierten Netzwerkadapter eine separate Netzwerkverbindung erstellt, weil Med-v nicht ermitteln kann, welcher Netzwerkadapter aktiv ist. Dadurch wird auch sichergestellt, dass Roaming-Benutzer immer über einen Netzwerkadapter für verdrahtete und drahtlose Verbindungen verfügen.

**Lösung**

Keine

**Die MED-V-Anwendung reagiert beim Schließen zu lange nicht**mehr. In einigen Fällen reagiert eine MED-V-Anwendung nicht mehr, wenn Sie versucht, Sie zu schließen.

**Lösung**

Sie können die Zeitdauer angeben, die MED-V wartet, um nicht reagierende Anwendungen zu schließen, indem Sie den WaitToKillAppTimeout-Registrierungsschlüssel auf dem virtuellen Gastcomputer festlegen. Weitere Informationen finden Sie unter so wird es [gemacht: verbessern der Zeit für das Herunterfahren, damit Prozesse in Windows XP ordnungsgemäß beendet werden können](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .

**Durch Umbenennen einer veröffentlichten Anwendungsverknüpfung auf dem virtuellen Gastcomputer wird der veröffentlichte Name im Host nicht geändert**. Wenn Sie eine Anwendung veröffentlichen, indem Sie eine Verknüpfung erstellen und dann die Verknüpfung auf der virtuellen Gastmaschine umbenennen, verbleibt der ursprüngliche Anwendungsname **im Startmenü des Hosts.** Das Programm wird weiterhin erwartungsgemäß ausgeführt, jedoch behält das Programm immer den ursprünglichen Namen bei.

**Lösung**

Keine Dies ist ein bekanntes Verhalten von Windows Virtual PC.

Wenn Sie **eine Verknüpfung auf dem virtuellen Gastcomputer verschieben, wird der Speicherort im Startmenü des Host Computers nicht aktualisiert**. MED-V-Anwendungsverknüpfungen, die im **Start** Menü des Hostcomputers veröffentlicht werden, werden in der Registrierung katalogisiert. Wenn Sie eine Anwendungsverknüpfung in einen Unterordner verschieben, wird die Registrierung nicht aktualisiert, um die Änderung wiederzugeben.

**Lösung**

Führen Sie die folgenden Schritte aus, um den Speicherort einer MED-V-Anwendungsverknüpfung zu ändern:

1.  Wenn Med-v ausgeführt wird, öffnen Sie Windows-Explorer auf dem virtuellen Med-v Guest-Computer.

2.  Navigieren Sie zum Verzeichnis "%ALLUSERSPROFILE%\\Start Menu\\Programs".

3.  Verschieben Sie die Anwendungsverknüpfungen aus den Ordnern "Startmenü" oder "Programme".

4.  Überprüfen Sie nach ungefähr 30 Sekunden, ob die Verknüpfungen aus dem **Startmenü** des Hostcomputers entfernt wurden.

5.  Verschieben Sie die Anwendungsverknüpfungen wieder in die neuen Programmordner unter dem Verzeichnis Start Menu\\Programs.

6.  Überprüfen Sie nach ungefähr 30 Sekunden, ob die Verknüpfungen im **Startmenü** des Hostcomputers aktualisiert wurden.

**Veröffentlichte Anwendungen können ein Timeout aufweisen, nachdem Sie im Leerlauf sitzen**. In einigen Fällen können veröffentlichte Anwendungen ausfallen, wenn Sie sich längere Zeit im Leerlauf befinden. Diese Situation tritt nur auf, wenn IPSec aktiviert ist und der MED-V-Arbeitsbereich für den NAT-Modus konfiguriert ist. Diese Situation tritt nicht auf, wenn Sie im Überbrückungsmodus ausgeführt werden.

**Lösung**

Deaktivieren Sie IPSec, wenn Sie den MED-V-Arbeitsbereich im NAT-Modus ausführen.

**Das Anheften einer veröffentlichten Anwendung an die Taskleiste umgeht MED-V**. Wenn ein Endbenutzer eine veröffentlichte Anwendung an die Taskleiste anstiftet und dann die Anwendung schließt, wird MED-V beim nächsten Öffnen der Anwendung über das Taskleistensymbol umgangen. Stattdessen wird die Anwendung direkt in einem VMSAL-Fenster geöffnet.

**Lösung**

Anheften Sie die in MED-V veröffentlichten Anwendungen nicht an die Taskleiste.

## Verwandte Themen


[Bewährte Sicherheitsmethoden für MED-V-Vorgänge](security-best-practices-for-med-v-operations.md)

[Problembehandlung bei der Bereitstellung](deployment-troubleshooting.md)

 

 





