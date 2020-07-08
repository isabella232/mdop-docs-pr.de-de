---
title: Bewährte Methoden für MED-V 2.0
description: Bewährte Methoden für MED-V 2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811560"
---
# Bewährte Methoden für MED-V 2.0


Wenn Sie MED-V in Ihrem Unternehmen planen, bereitstellen und verwalten, finden Sie möglicherweise die Empfehlungen für bewährte Methoden als hilfreich.

### Konfigurieren der erstmaligen Einrichtung für die unbeaufsichtigte Ausführung

Obwohl Sie alle gewünschten Einstellungen angeben können, ist es eine bewährte Methode von MED-V, die Datei "Sysprep. inf" zu erstellen, damit das erstmalige Setup im **unbeaufsichtigten** Modus ausgeführt werden kann. Dies erfordert, dass Sie alle erforderlichen Einstellungsinformationen angeben, während Sie den **Setup-Manager-** Assistenten fortsetzen. Weitere Informationen zum Konfigurieren des Med-v-Images finden Sie unter [Konfigurieren eines Windows Virtual PC-Images für med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Deaktivieren von Wiederherstellungspunkten auf dem virtuellen Computer

Bevor Sie das MED-V Workspace-Paket erstellen, empfehlen wir, die Wiederherstellungspunkte auf dem virtuellen Computer zu deaktivieren, um zu verhindern, dass der differenzierende Datenträger unbegrenzt wächst. Weitere Informationen finden Sie unter [so wird es gemacht: deaktivieren und Aktivieren der System Wiederherstellung unter Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

### Konfigurieren von MED-V-Bildern für die Verwendung lokaler Profile

Es wird empfohlen, nur die Richtlinien anzuwenden, die in einer Anwendungs Kompatibilitätsumgebung für Windows XP sinnvoll sind. Beispielsweise müssen die Richtlinien für die Desktop Anpassung normalerweise nicht angewendet werden und sollten deaktiviert sein. Weitere Informationen zum Zulassen nur lokaler Profile finden Sie unter [Gruppenrichtlinieneinstellungen für Roaming-Benutzerprofile](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

### Konfigurieren einer Leistungs Aktualisierung für Gruppenrichtlinien

Standardmäßig wird die Gruppenrichtlinie jeweils um ein Byte auf einen Computer heruntergeladen. Dies verursacht Verzögerungen, wenn MED-V zur Domäne hinzugefügt wird. Wenn Sie die Leistung von Gruppenrichtlinien erhöhen möchten, empfiehlt es sich, den folgenden Registrierungsschlüsselwert auf die Registrierung festzulegen:

Registrierungsunterschlüssel: HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\windows NT\\CurrentVersion\\Winlogon

Eintrag: BufferPolicyReads

Geben Sie Folgendes ein: DWORD

Wert: 1

### Verteilen des rechtlichen Hinweises über Gruppenrichtlinien anstelle des MED-V-Bilds

Wenn Endbenutzern vor dem Zugriff auf MED-V eine Vereinbarung zum Service Level (SLA) angezeigt werden soll, empfehlen wir, dass Sie die SLA später über Gruppenrichtlinien erzwingen, damit die SLA dem Endbenutzer nach Abschluss der erstmaligen Einrichtung angezeigt wird.

**Vorsicht**  Obwohl es bewährte Methode ist, das erstmalige Einrichten im **unbeaufsichtigten** Modus durchzuführen, wenn Sie sich entscheiden, die lokale Richtlinie oder den Registrierungseintrag so festzulegen, dass Sie eine SLA in Ihr Abbild (virtuelle Festplatte) einschließt, müssen Sie auch angeben, dass die erstmalige Einrichtung im **beaufsichtigten** Modus ausgeführt wird oder dass die erstmalige Einrichtung fehlschlagen kann.

 

### Komprimieren der virtuellen Festplatte

Wir empfehlen, dass Sie Ihre virtuelle Festplatte komprimieren, um leeren Speicherplatz freizugeben und die Größe der virtuellen Festplatte zu verringern. Weitere Informationen zum Komprimieren Ihrer virtuellen Festplatte finden Sie unter [Komprimieren der virtuellen MED-V-Festplatte](compacting-the-med-v-virtual-hard-disk.md).

### Konfigurieren des virtuellen Computers zum Neustart auf dem Bluescreen-Absturz

Wir empfehlen, dass Sie den virtuellen Computer des MED-V-Arbeitsbereichs so konfigurieren, dass er automatisch neu gestartet wird, wenn ein Absturz des blauen Bildschirms auftritt. Wenn Sie diese Einstellung im Gast konfigurieren möchten, legen Sie den Wert für den AutoReboot im HKEY \ _LOCAL \ _MACHINE \\system\\currentcontrolset\\control\\crashcontrol-Taste auf "1" fest.

Sie können diese Einstellung auch konfigurieren, indem Sie auf **Start**und **dann auf**Systemsteuerung und dann auf **System**klicken. Klicken Sie dann im **Start-und Wiederherstellungs** Bereich der Registerkarte **erweitert** auf **Einstellungen**. Aktivieren Sie das Kontrollkästchen **automatisch neu starten** , und klicken Sie auf **OK**.

### MED-V-Bild vor dem versiegeln sichern

Wir empfehlen, dass Sie eine Sicherungskopie des MED-V-Bilds erstellen, bevor Sie es versiegeln. Weitere Informationen zum Abdichten Ihres Med-v-Bilds finden Sie unter [Konfigurieren eines Windows Virtual PC-Images für med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Installieren von Windows Virtual PC zuletzt bei der Installation aus einer Batchdatei

Wenn Sie die Med-v-Komponenten mithilfe einer Batchdatei installieren, geben Sie an, dass Windows Virtual PC und der Windows Virtual PC-Hotfix nach dem Med-v-Host-Agent und den Med-v-Arbeitsbereichs Paketdateien installiert werden. Dadurch wird sichergestellt, dass Windows Update keinen Eingriff in den Installationsvorgang verursacht, da ein Neustart erforderlich ist.

### Installieren des MED-V-Arbeitsbereichs aus dem lokalen Ordner

Aufgrund von Problemen, die bei der Installation von Med-v von einem Netzwerkspeicherort auftreten können, empfiehlt es sich, die Setupdateien des Med-v-Arbeitsbereichs lokal zu kopieren und dann setup.exe auszuführen.

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a>Verwalten der Druckerumleitung nur auf eine Weise

Wenn ein Drucker manuell auf dem virtuellen MED-V-Gastcomputer installiert ist und der gleiche Drucker später auf dem Hostcomputer installiert ist, ist das Ergebnis, dass er zwei Mal im Gast installiert ist. Um dies zu vermeiden, empfehlen wir, dass Sie die Druckerumleitung nur auf eine Art und Weise verwalten: Deaktivieren Sie die Umleitung, und installieren Sie Drucker manuell auf dem Gast, oder aktivieren Sie die Umleitung, und installieren Sie Drucker nicht manuell auf dem Gast.

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a>Konfigurieren von Einstellungen für MED-V Guest-Patches

Sie können steuern, wann und wie lange der virtuelle MED-V-Computer aufwacht, um automatische Updates zu erhalten, indem Sie die entsprechenden Konfigurationswerte in der Registrierung definieren. Eine optimale Methode für med-v besteht darin, das Aktivierungsintervall so festzulegen, dass es dem Zeitpunkt entspricht, zu dem Sie reguläre Updates für MED-V Virtual Machines geplant haben. Darüber hinaus empfiehlt es sich, diese Einstellungen so zu konfigurieren, dass Sie dem Verhalten des Hostcomputers ähneln.

Weitere Informationen zum Konfigurieren von Einstellungen für med-v Guest-Patches finden Sie unter [Verwalten von automatischen Updates für med-v-Arbeitsbereiche](managing-automatic-updates-for-med-v-workspaces.md).

### Konfigurieren von Antivirus/Sicherungssoftware

Um zu verhindern, dass Antivirenprogramme die Leistung des virtuellen Desktops beeinträchtigen, empfehlen wir, dass Sie die folgenden virtuellen Computerdatei Typen von einem beliebigen Antivirus-oder Sicherungsprozess ausschließen, der auf dem MED-V-Hostcomputer ausgeführt wird:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. VHD

## Verwandte Themen


[Sicherheit und Schutz für MED-V](security-and-protection-for-med-v.md)

 

 





