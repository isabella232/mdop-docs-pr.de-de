---
title: So aktualisieren Sie Application Virtualization Client
description: So aktualisieren Sie Application Virtualization Client
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806712"
---
# So aktualisieren Sie Application Virtualization Client


Sie können die folgenden Verfahren zum Upgrade des Application Virtualization (app-v)-Desktop Clients oder des App-v-Clients für Remote Desktop Dienste (ehemals Terminal Dienste) verwenden. Sie aktualisieren den Client, indem Sie eine neue Version über die zuvor installierte ältere Version installieren. Wenn Sie die Clients aktualisieren, werden die Einstellungen des Benutzers für virtuelle Anwendungen automatisch von der Installationssoftware beibehalten und migriert. Zum Ausführen des Setup-Programms sind Administratorrechte erforderlich.

**Hinweis**  Während des Upgrades auf Application Virtualization (App-V) 4.5 oder höhere Versionen werden die Berechtigungen für den Registrierungsschlüssel HKCU geändert. Aus diesem Grund verlieren Benutzer die zuvor festgelegten Benutzerkonfigurationen wie Benutzer konfigurierte Einstellungen für den getrennten Modus. Wenn der Benutzer nicht aktiv vom Konfigurieren des Verhaltens der Clientbenutzeroberfläche durch eine Berechtigungs Sperre eingeschränkt wird, kann der Benutzer diese Einstellungen nach einer Veröffentlichungsaktualisierung zurücksetzen.

 

**Wichtig**  Wenn Sie auf Version 4.6 oder eine neuere Version des App-V-Clients aktualisieren, müssen Sie das richtige Installationsprogramm für das Betriebssystem des Computers, 32-Bit oder 64-Bit verwenden. Bei der Installation tritt ein Fehler auf, und es wird eine Fehlermeldung angezeigt, wenn Sie das falsche Installationsprogramm verwenden.

 

**So aktualisieren Sie den Application Virtualization-Desktop Client**

1.  Beenden Sie alle virtuellen Anwendungen, klicken Sie mit der rechten Maustaste auf das App-V-Desktop Client Symbol, das im Windows-Desktopbenachrichtigungsbereich angezeigt wird, und wählen Sie **Beenden** aus, um den vorhandenen Client zu beenden.

2.  Nachdem Sie die richtige Installationsarchiv Datei abgerufen und auf Ihrem Computer gespeichert haben, doppelklicken Sie darauf, um das Archiv zu erweitern.

3.  Suchen Sie nach der setup.exe-Datei, und doppelklicken Sie auf setup.exe, um die Installation zu starten.

4.  Der Assistent überprüft das System, um sicherzustellen, dass alle erforderlichen Software installiert ist, und fordert Sie auf, eine der folgenden Komponenten zu installieren, wenn Sie nicht vorhanden sind:

    -   Microsoft VisualC + + 2005SP1-Paket (x86)

    -   Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

    -   Microsoft-Anwendungsfehler Berichterstattung

    **Hinweis**  Für Version 4.6 und höher wird der Assistent auch die folgende Softwarevoraussetzungen installieren:

    -   Microsoft VisualC + + 2008SP1-Paket (x86)

     

5.  Klicken Sie auf **Installieren**. Der Installationsfortschritt wird angezeigt, und der Status wechselt von " **Ausstehend** " in " **Installieren**". Der Installationsstatus ändert sich **in erfolgreich,** wenn jeder Schritt erfolgreich abgeschlossen wurde.

6.  Wenn das Dialogfeld **Application Virtualization Desktop Client** angezeigt wird und eine Meldung angezeigt wird, die besagt, dass eine ältere Version des Clients auf dem Computer gefunden wurde, klicken Sie auf **weiter** , um auf die neue Version zu aktualisieren.

7.  Wenn der Bildschirm " **Lizenzvertrag** " angezeigt wird, lesen Sie den Lizenzvertrag, und wenn Sie damit einverstanden sind, klicken Sie auf **Ich stimme den Bedingungen des Lizenzvertrags**zu, und klicken Sie dann auf **weiter**.

8.  Wenn der InstallShield-Assistent das Dialogfeld " **bereit zum Upgrade des Programms** " anzeigt, klicken Sie auf **Upgrade** , um mit dem Upgrade zu beginnen. Auf dem nächsten Bildschirm wird angezeigt, dass der Client installiert wird.

    **Warnung**  Wenn Sie das Clientprogramm in Schritt 1 nicht heruntergefahren haben, wird möglicherweise eine Warnung " **Dateien in Verwendung** " angezeigt. Wenn dies der Fall ist, klicken Sie mit der rechten Maustaste auf das App-V-Clientsymbol, das im Desktopbenachrichtigungsbereich angezeigt wird, und wählen Sie **Beenden** aus, um den vorhandenen Client zu beenden. Klicken Sie dann auf wieder **holen** , um den Vorgang fortzusetzen.

     

9.  Wenn die Installation erfolgreich abgeschlossen wurde, werden Sie aufgefordert, den Computer neu zu starten. Sie müssen den Computer neu starten, um die Installation abzuschließen.

    **Vorsicht**  Wenn das Upgrade aus irgendeinem Grund fehlschlägt, müssen Sie den Computer neu starten, bevor Sie das Upgrade erneut versuchen.

     

**So aktualisieren Sie den Application Virtualization-Client mithilfe der Befehlszeile**

1.  Wenn Sie den App-V-Client mithilfe des setup.msi-Programms aktualisieren, stellen Sie sicher, dass alle erforderlichen Softwarekomponenten installiert wurden.

    **Wichtig**  
    -   Für Version 4.6 und höher des App-V-Clients überprüft das setup.msi-Programm das System und schlägt mit einer Fehlermeldung fehl, die darauf hinweist, dass die Installation nicht fortgesetzt werden kann, wenn die erforderliche Software nicht installiert ist.

    -   Für App-V Version 4.6 können Befehlszeilenparameter während eines Upgrades nicht verwendet werden und werden ignoriert.

     

2.  Im folgenden Befehlszeilenbeispiel wird die setup.msi-Datei verwendet, um den App-V-Client zu aktualisieren. Sie müssen das richtige Clientinstallationsprogramm verwenden, je nachdem, ob Sie den App-v-Desktop Client oder den App-v-Client für Remote Desktop Dienste (ehemals Terminal Dienste) aktualisieren.

    **msiexec.exe/i "setup.msi"**

    **Wichtig**  Die Anführungszeichen sind nur erforderlich, wenn der Wert ein Leerzeichen enthält. Aus Gründen der Konsistenz werden alle Instanzen im vorherigen Beispiel als Anführungszeichen angezeigt.

     

**So aktualisieren Sie den Application Virtualization-Client für Remote Desktop Dienste**

1.  Befolgen Sie die Standardrichtlinien Ihrer Organisation zum Installieren oder Aktualisieren von Anwendungen auf dem Remote Desktop-Sitzungshost Server (RDSession-Host). Wenn das System Teil einer Farm ist, entfernen Sie den RDSession-Host aus der Serverfarm.

2.  Um den App-V-Client für Remote Desktop Dienste (vormals Terminal Dienste) zu aktualisieren, müssen Sie die Befehlszeile verwenden, da Sie den Client nicht manuell auf dem RDSession-Host aktualisieren können.

    **Hinweis**  In App-V Version 4,6 und höher können Sie zusätzlich zur Verwendung der Befehlszeile zum Upgrade des Clients auch eine Remote Desktop Sitzung verwenden. Zum Starten der Remote Desktop Sitzung sind keine speziellen Parameter erforderlich.

     

3.  Nachdem der Client für das Upgrade der Remote Desktop Dienste abgeschlossen ist, starten Sie den Computer neu, und melden Sie sich beim RDSession-Host an.

4.  Nachdem das System neu gestartet wurde, fügen Sie den Server der Serverfarm hinzu.

    **Vorsicht**  Wenn das Upgrade aus irgendeinem Grund fehlschlägt, müssen Sie den Computer neu starten, bevor Sie das Upgrade erneut versuchen.

     

## Verwandte Themen


[Bereitstellung von Application Virtualization und Upgrade Aspekte](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





