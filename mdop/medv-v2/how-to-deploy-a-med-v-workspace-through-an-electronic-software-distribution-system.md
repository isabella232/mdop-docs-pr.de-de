---
title: So stellen Sie einen MED-V-Arbeitsbereich über eines elektronischen Softwareverteilungssystem bereit
description: So stellen Sie einen MED-V-Arbeitsbereich über eines elektronischen Softwareverteilungssystem bereit
author: dansimp
ms.assetid: b5134c35-e1de-470c-93f8-ead6218d9dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56d21b0c2f010f63c04056d9fadd7763531bd9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804643"
---
# So stellen Sie einen MED-V-Arbeitsbereich über eines elektronischen Softwareverteilungssystem bereit


Ein elektronisches Softwareverteilungssystem wurde entwickelt, um Software effizient auf viele verschiedene Computer über langsame oder schnelle Netzwerkverbindungen zu verschieben. Der folgende Abschnitt enthält Informationen und Anweisungen, die Ihnen bei der Bereitstellung Ihres MED-V-Arbeitsbereichs in Ihrem Unternehmen mithilfe eines Softwareverteilungssystems helfen.

**Hinweis:**  
Je nachdem, welche softwareverteilungslösung Sie verwenden, müssen Sie mit den Anforderungen ihrer jeweiligen Lösung vertraut sein. Wenn Sie System Center Configuration Manager 2007 R2 oder eine neuere Version verwenden, lesen Sie die [Configuration Manager-Dokumentationsbibliothek](https://go.microsoft.com/fwlink/?LinkId=66999) in der Microsoft Technical Library ( https://go.microsoft.com/fwlink/?LinkId=66999) .



**Wichtig**  
Wenn Sie System Center Configuration Manager 2007 SP2 verwenden und ihre MED-V-Arbeitsbereiche für den Betrieb im **NAT** -Modus konfiguriert sind, werden die virtuellen Computer als Internet basierte Clients klassifiziert und können nicht die nächstgelegenen Verteilungspunkte finden, von denen Inhalte heruntergeladen werden sollen.

Der [Hotfix zum Verbessern der Funktionalität für VMS, die von Med-v verwaltet werden](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) fügt neue Funktionen zu virtuellen Computern hinzu, die von Med-v verwaltet werden und für den Betrieb im **NAT** -Modus konfiguriert sind. Mit der neuen Funktionalität können virtuelle Maschinen auf die nächstgelegenen Verteilungspunkte zugreifen. Daher kann der Administrator den virtuellen Computer und den Hostcomputer auf die gleiche Weise verwalten. Dieser Hotfix muss zuerst auf dem Website Server und dann auf dem Client installiert werden.

Das Update ist öffentlich verfügbar. Möglicherweise werden Sie jedoch aufgefordert, eine Vereinbarung für Microsoft-Dienste zu akzeptieren. Folgen Sie den Anweisungen auf den nachfolgenden Webseiten, um diesen Hotfix abzurufen.



Sie können die MED-V-Komponenten auch zusammen mithilfe einer Batchdatei bereitstellen, dies erfordert jedoch einen Neustart nach der Installation von Windows Virtual PC. Um diese Anforderung zu umgehen, können Sie einen einzelnen Neustart angeben, nachdem alle Komponenten installiert wurden. Der einzelne Neustart startet auch automatisch Med-v, weil die Med-v Workspace-Installation einen Eintrag im RUNKEY platziert.

**So stellen Sie einen MED-V-Arbeitsbereich mithilfe eines Softwareverteilungssystems bereit**

1.  Definieren Sie eine Gruppe von Computern und Benutzern im elektronischen Softwareverteilungssystem als Zielgruppe von Computern/Benutzern.

2.  Erstellen Sie Pakete für jede Microsoft-Installationsdatei, die verteilt werden soll. Im folgenden finden Sie die erforderlichen Dateien und die Reihenfolge, in der Sie installiert werden müssen:

    1.  **Windows Virtual PC** – wenn noch nicht installiert (ein Neustart des Computers ist erforderlich) Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.

    2.  **Windows Virtual PC-Ergänzungen und-Updates** – Falls noch nicht installiert. Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.

    3.  **Installationsdatei des Med-v-Host-Agents** – installiert den Host-Agent (Med-v \ _HostAgent \ _setup Installationsdatei). Weitere Informationen finden Sie unter [Manuelles Installieren des MED-V-Host-Agents](how-to-manually-install-the-med-v-host-agent.md).

        **Warnung**  
        Schließen Sie Internet Explorer, bevor Sie den MED-V-Host-Agent installieren, andernfalls können Konflikte später bei der URL-Umleitung auftreten. Sie können dies auch tun, indem Sie während einer Verteilung einen Neustart des Computers angeben.



    4.  Das **Med-v Workspace-Installationsprogramm, die VHD und die Setup-Datei** , die im **Med-v-Arbeitsbereichs Paket**erstellt wurde. Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).

        **Wichtig**  
        Die komprimierte virtuelle Festplattendatei (. medv) und das ausführbare Setup Programm (setup.exe) müssen sich im gleichen Ordner wie das MED-V Workspace-Installationsprogramm befinden. Installieren Sie dann das MED-V Workspace-Installationsprogramm, indem Sie setup.exe ausführen.



~~~
    **Tip**  
    Because problems can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



3. Konfigurieren Sie die Pakete so, dass Sie im unbeaufsichtigten Modus ausgeführt werden (es ist keine Benutzerinteraktion erforderlich).

   Wenn Sie im unbeaufsichtigten Modus ausgeführt wird, wird die Aufforderung zum Schließen von Internet Explorer, wenn Sie ausgeführt wird, und die Aufforderung zum Starten des MED-V-Host-Agents beseitigt. Beide Aktionen werden ausgeführt, wenn der Computer neu gestartet wird.

   **Hinweis:**  
   Bei der Installation von Windows Virtual PC müssen Sie den Computer neu starten. Wenn Sie den Neustart unterdrücken und die erforderlichen Voraussetzungen für die Installation von MED-V ignorieren, können Sie einen einzelnen Installationsvorgang erstellen und alle Komponenten gleichzeitig installieren. Sie können dies auch über Befehlszeilenargumente tun. Ein Beispiel für diese Argumente finden Sie unter [Bereitstellen der MED-V-Komponenten über ein elektronisches Software Verteilungs System](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md#bkmk-batch). MED-V wird automatisch gestartet, wenn der Computer neu gestartet wird.



4. Installieren Sie MED-V und die zugehörigen Komponenten, bevor Sie Windows Virtual PC installieren. Lesen Sie die Beispielbatchdatei weiter unten in diesem Thema.

   **Wichtig**  
   Wählen Sie die Option **\ _PREREQUISITES ignorieren** aus, wie in der Beispielbatchdatei gezeigt, damit die MED-V-Komponenten vor den erforderlichen VPC-Komponenten installiert werden können. Installieren Sie die MED-V-Komponenten in dieser Reihenfolge, um den einmaligen Neustart zu ermöglichen.



5. Ermitteln Sie alle anderen Anforderungen, die für die Installation und für Ihr Softwareverteilungssystem wie Zielplattformen und den freien Speicherplatz erforderlich sind.

6. Weisen Sie die Pakete der Zielgruppe von Computern/Benutzern zu.

   Wenn Computer ausgeführt werden, erkennt der Client für Softwareverteilungssysteme, dass neue Pakete verfügbar sind, und beginnt, die Pakete pro Definition und Anforderungen zu installieren. Die Installationen sollten sequenziell in Silent ausgeführt werden. Wir empfehlen, dass dies als ein einzelner Prozess ausgeführt wird, für den kein Neustart erforderlich ist, bis alle Pakete installiert sind.

7. Nachdem die Installation abgeschlossen ist, starten Sie die aktualisierten Computer neu.

   Je nach Softwareverteilungssystem können Sie einen Neustart des Computers planen, oder die Endbenutzer können die Computer während der regulären Arbeit manuell neu starten. Nachdem der Computer neu gestartet wurde, wird MED-V automatisch gestartet, wenn sich ein Endbenutzer anmeldet. Wenn MED-V zum ersten Mal gestartet wird, wird die erstmalige Einrichtung ausgeführt.

Das erstmalige Setup wird gestartet und kann einige Minuten dauern, abhängig von der Größe der von Ihnen angegebenen virtuellen Festplatte und der Anzahl der Richtlinien, die beim Start auf den MED-V Workspace angewendet wurden. Der Endbenutzer kann den Fortschritt nachverfolgen, indem er das MED-V-Symbol im Infobereich ansieht. Weitere Informationen zum erstmaligen Einrichten finden Sie unter [Übersicht über die Bereitstellung von MED-V 2,0](med-v-20-deployment-overview.md).

**So installieren Sie den MED-V-Arbeitsbereich mithilfe einer Batchdatei**

1.  Führen Sie die Installation an einer Eingabeaufforderung mit Administratorrechten aus.

2.  Stellen Sie die einzelnen Komponenten in einem einzigen Verzeichnis bereit. Wenn Sie von einer Netzwerkfreigabe ausführen, ist eine längere Zeit erforderlich, um die medv-Datei zu dekomprimieren.

3.  Als bewährte Methode können Sie angeben, dass Windows Virtual PC und der Windows Virtual PC-Hotfix nach dem Med-v-Host-Agent und den Med-v-Arbeitsbereichs Paketdateien installiert werden. Dies bedeutet, dass Windows Update keinen Eingriff in den Installationsvorgang verursacht, da ein Neustart erforderlich ist.

4.  Starten Sie den Computer nach Abschluss der Batchdatei neu.

Nach dem Neustart wird der Benutzer aufgefordert, das erstmalige Setup auszuführen und die Konfiguration von MED-V abzuschließen.

Im folgenden Beispiel wird mit den angegebenen Argumenten gezeigt, wie Sie 64-Bit-MED-V-Komponenten in einem einzigen Prozess installieren:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Argument</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/norestart</p></td>
<td align="left"><p>Verhindert, dass die Installation von Windows Virtual PC und dem Windows Virtual PC-Update den Hostcomputer neu startet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Quiet</p></td>
<td align="left"><p>Installiert die MED-V-Komponenten im stillen Modus ohne Benutzerinteraktion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Qn</p></td>
<td align="left"><p>Installiert die MED-V-Komponenten ohne eine Benutzeroberfläche.</p></td>
</tr>
<tr class="even">
<td align="left"><p>IGNORE_PREREQUISITES</p></td>
<td align="left"><p>Installationen ohne Überprüfung auf Windows Virtual PC.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Geben Sie dieses Argument nur an, wenn Sie Windows Virtual PC als Teil dieser Installation installieren.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>OVERWRITEVHD</p></td>
<td align="left"><p>Erzwingt die Installation des MED-V-Arbeitsbereichs und verhindert eventuelle Eingabeaufforderungen.</p></td>
</tr>
</tbody>
</table>



## Beispiel


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## Verwandte Themen


[Übersicht über die Bereitstellung von MED-V 2.0](med-v-20-deployment-overview.md)

[So stellen Sie einen MED-V-Arbeitsbereich in ein Windows 7-Image bereit](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)









