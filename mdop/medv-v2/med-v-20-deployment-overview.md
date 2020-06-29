---
title: Übersicht über die Bereitstellung von MED-V 2.0
description: Übersicht über die Bereitstellung von MED-V 2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811557"
---
# Übersicht über die Bereitstellung von MED-V 2.0


Dieser Abschnitt enthält allgemeine Informationen und Anweisungen zum Installieren und Bereitstellen von Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Übersicht


Med-v 2,0 basiert auf einem Anwendungsmodell, bei dem die gleichen Methoden, die Sie zum Bereitstellen von Anwendungen verwenden, zum Bereitstellen und Verwalten von Med-v verwendet werden können. Eine bereitgestellte Med-v-Lösung umfasst zwei Komponenten: den Med-v-Host-Agent und den Gast-Agent. Der Med-v-Host-Agent ist auf dem Windows 7-Desktop installiert, und der Med-v-Gast-Agent ist unter Windows XP innerhalb des Med-v-Arbeitsbereichs installiert. Med-v enthält auch einen Med-v-Arbeitsbereichs-Packager, der die Informationen und Tools bereitstellt, die für das Erstellen und Konfigurieren von Med-v-Arbeitsbereichen erforderlich sind.

**Wichtig**  
Med-v unterstützt nur die Installation des Med-v-Arbeitsbereichs Pakets, des Med-v-Host-Agents und des Med-v-Arbeitsbereichs für alle Benutzer. Wenn Sie Med-v nur für den aktuellen Benutzer installieren, indem Sie **ALLUSERS = ""** auswählen, werden Fehler bei der Installation der Komponenten und beim Einrichten des Med-v-Arbeitsbereichs verursacht.



### Die MED-V-Installationsdateien

Med-v umfasst die folgenden Installationsdateien, die für die Ausführung von Med-v erforderlich sind:

**Die Installationsdatei des MED-V-Host-Agents**

Die Installationsdatei des Host-Agents hat den Namen MED-V\_HostAgent\_Setup.exe. Diese Datei wird im Rahmen ihrer unternehmensweiten Bereitstellung von MED-V auf jedem relevanten Endbenutzercomputer verteilt und installiert.

**Die Installationsdatei des MED-V-Arbeitsbereichs Pakets**

Die Installationsdatei des MED-V-Arbeitsbereichs-Packagers hat den Namen MED-V\_WorkspacePackager\_Setup.exe. Verwenden Sie diese Datei, um den MED-V Workspace-Paketer auf einem Computer zu installieren, auf dem Sie über Administratorrechte und-Berechtigungen verfügen. Der Desktopadministrator verwendet den Med-v Workspace-Paketer zum Erstellen und Verwalten von Med-v-Arbeitsbereichen.

**Hinweis:**  
Der MED-V-Gast-Agent wird während der erstmaligen Einrichtung automatisch installiert.



### Der MED-V-Bereitstellungsprozess

Im folgenden wird eine allgemeine Übersicht über den MED-V-Installations-und Bereitstellungsprozess beschrieben:

1.  Installieren Sie den Med-v Workspace-Paketer auf dem Computer, auf dem Sie über administrative Anmeldeinformationen verfügen und die Sie zum Erstellen der Med-v-Arbeitsbereichs Pakete verwenden werden. Weitere Informationen finden Sie unter [so wird es gemacht: Installieren des MED-V-Arbeitsbereichs Pakets](how-to-install-the-med-v-workspace-packager.md).

2.  Bereiten Sie Ihr Med-v-Abbild vor, und erstellen Sie Ihre Med-v-Arbeitsbereichs Pakete mithilfe des Med-v-Arbeitsbereichs-Packagers. Weitere Informationen finden Sie unter [Operationen für MED-V](operations-for-med-v.md).

3.  Stellen Sie die erforderlichen MED-V-Komponenten im gesamten Unternehmen bereit. Die erforderlichen Komponenten von Med-v sind Windows Virtual PC, der Med-v-Host-Agent und der Med-v-Arbeitsbereich.

**Wichtig**  
Für die Installation der MED-V-Komponenten sind Administratoranmeldeinformationen erforderlich. Wenn ein Endbenutzer MED-V installiert, werden Sie aufgefordert, administrative Anmeldeinformationen einzugeben. Alternativ können Administratoranmeldeinformationen im Kontext bereitgestellt werden, wenn Sie mit einem ESD-System (Electronic Software Distribution) installieren.



### Die MED-V-Komponenten

Die MED-V-Komponenten, die Sie im gesamten Unternehmen bereitstellen, umfassen Folgendes:

**Windows Virtual PC**

MED-V-Funktionen in Windows Virtual PC-Bildern für Ihre kompatibilitätslösung. Windows Virtual PC und das Update für Windows 7 (KB977206) sind erforderlich. Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.

**Die Installationsdatei des MED-V-Host-Agents**

MED-V\_HostAgent\_Setup.exe.

**Die Installationsdateien für den MED-V-Arbeitsbereich**

Die Installationsdateien für den Med-v-Arbeitsbereich werden erstellt, wenn Sie Ihr Med-v-Arbeitsbereichs Paket erstellen, das Folgendes umfasst:

Ein setup.exe ausführbares Programm, das die Installation des MED-V-Arbeitsbereichs ausführt

Ein &lt; MED-V \ _workspace \ _name &gt; . MSI-Installationsprogramm

Eine &lt; VHD \ _FileName &gt; . medv-Datei, bei der es sich um die komprimierte virtuelle Festplatte handelt

Die Dateien für Konfigurationseinstellungen ( &lt; Arbeitsbereich \ _name &gt; . reg und &lt; Arbeitsbereich \ _name &gt; . ps1)

Zum Bereitstellen von MED-V kopieren Sie alle erforderlichen Installationsdateien auf den Hostcomputer oder auf eine Freigabe, auf die der Hostcomputer zugreifen kann. Führen Sie die Komponenten Installationsdateien für Windows Virtual PC, den Med-v-Host-Agent und den Med-v-Arbeitsbereich aus. Starten Sie dann den Med-v-Host-Agent, um die erstmalige Einrichtung von Med-v abzuschließen.

Sie können die Installation manuell durchführen. Wir empfehlen jedoch, dass Sie eine elektronische Softwareverteilungsmethode verwenden, um die Bereitstellung der Komponenten zu automatisieren. Weitere Informationen finden Sie unter [Bereitstellen eines MED-V-Arbeitsbereichs über ein elektronisches Software Verteilungs System](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).

**Hinweis:**  
Informationen zu den verfügbaren Befehlszeilenargumenten, um die Installationsoptionen zu steuern, finden Sie unter [Befehlszeilenoptionen für MED-V-Installationsdateien](command-line-options-for-med-v-installation-files.md).



## Bereitstellungsschritte


Wenn Sie MED-V im gesamten Unternehmen bereitstellen, gibt es zwei Hauptaspekte: Installation und Erstmaliges Einrichten.

### Installation

1.  **Windows Virtual PC** – während der Installation überprüft MED-V für Windows Virtual PC und das erforderliche Update für Windows 7 (KB977206). Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.

    Sie können diese als Teil der Windows 7-Installationen installieren, bevor Sie Med-v installieren, oder Sie können Sie als Teil der Med-v-Verteilung installieren. MED-V enthält jedoch keinen Mechanismus für die Bereitstellung; Sie müssen mithilfe eines ESD-Systems (Electronic Software Distribution) oder als Teil des Windows 7-Images bereitgestellt werden.

    **Wichtig**  
    Wenn Sie die Med-v-Komponenten mithilfe einer Batchdatei installieren, empfiehlt es sich, festzulegen, dass Windows Virtual PC und der Windows Virtual PC-Hotfix nach dem Med-v-Host-Agent und den Med-v-Arbeitsbereichs Paketdateien installiert werden. Dies bedeutet, dass Windows Update keinen Eingriff in den Installationsvorgang verursacht, da ein Neustart erforderlich ist.



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. **Med-v-Host-Agent** – installieren Sie den Med-v-Host-Agent auf dem Windows 7-Computer, auf dem Med-v ausgeführt wird. Diese muss vor der Installation des MED-V-Arbeitsbereichs installiert werden, und es wird überprüft, ob Windows Virtual PC installiert ist.

3. **Med-v Workspace** – Sie erstellen die Dateien, die in dieser Installation erforderlich sind, mithilfe des Med-v-Arbeitsbereichs Pakets: die setup.exe-, medv-und MSI-Dateien. Führen Sie setup.exe aus, um den MED-V-Arbeitsbereich zu installieren. Dadurch werden die anderen Dateien nach Bedarf ausgelöst. Die Installation platziert einen Eintrag in der Registrierung unter dem Schlüssel "lokaler Computer ausführen", um den Med-v-Host-Agent zu starten, der immer Med-v ausführt, wenn Windows gestartet wird.

   **Wichtig**  
   Die Installation des MED-V-Arbeitsbereichs kann vom Endbenutzer interaktiv oder lautlos über ein elektronisches Softwareverteilungssystem ausgeführt werden. Die Installation des Med-v-Arbeitsbereichs erfordert administrative Anmeldeinformationen, sodass Endbenutzer Administratoren Ihrer Computer sein müssen, um den Med-v-Arbeitsbereich zu installieren. Alternativ wird ein elektronisches Softwareverteilungssystem in der Regel im Systemkontext ausgeführt und verfügt über ausreichende Berechtigungen.



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### Erstmaliges Einrichten

Nachdem Med-v und die erforderlichen Komponenten installiert sind, muss Med-v konfiguriert sein. Die Konfiguration von MED-V wird als Erstmaliges Einrichten bezeichnet. Mithilfe des **MED-V-Arbeitsbereichs Pakets**können Sie die erstmalige Einrichtung so konfigurieren, dass Sie automatisch oder interaktiv ausgeführt wird. Bei der erstmaligen Einrichtung von Med-v müssen Endbenutzer Ihr Kennwort eingeben, um sich bei dem Med-v-Arbeitsbereich zu authentifizieren, aber ansonsten kann der Benutzer fast unsichtbar sein. Benachrichtigungen werden im Infobereich angezeigt, beispielsweise wenn die erstmalige Einrichtung abgeschlossen ist und Anwendungen bereit sind. Im folgenden finden Sie die Aktionen, die bei der erstmaligen Einrichtung von MED-V auftreten:

1.  Die virtuelle Festplatte muss konfiguriert sein. Das Mini Setup wird ausgeführt und erweitert das Windows XP-Abbild. In der Regel tritt dies in einem ausgeblendeten Fenster auf, aber MED-V kann für die Anzeige während dieser Konfiguration konfiguriert werden.

2.  Nach Abschluss der Mini Installation können Sie Befehle ausführen, die für eine zusätzliche Konfiguration erforderlich sind, beispielsweise die Installation von ESD-Software oder anderen Anwendungen oder das Konfigurieren des Bilds. Diese können in der Datei "Sysprep. inf" aufgerufen werden, sind dort aber nicht erforderlich. Weitere Informationen finden Sie unter [Konfigurieren eines Windows Virtual PC-Images für MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

3.  Ftscompletion.exe wird als letzter Schritt in der Konfiguration ausgeführt. Dieser Vorgang schließt die Med-v-Konfiguration ab, fügt den Benutzer der RDP-Gruppe hinzu, um den Zugriff auf den Med-v-Arbeitsbereich zu ermöglichen, Protokolle zu kopieren, signalisiert Med-v, dass der Med-v-Arbeitsbereich bereit ist, und startet dann den Med-v-Arbeitsbereich neu. Durch diesen Vorgang kann der Benutzer auch als Administrator des Med-v-Arbeitsbereichs hinzugefügt werden, wenn dieser beim Erstellen des Med-v-Arbeitsbereichs konfiguriert wurde. Ftscompletion.exe wird in der Regel über die Sysprep-, INF-Datei aufgerufen, kann aber auch über eine andere Methode wie ein Skript ausgeführt werden. Ftscompletion.exe muss jedoch die letzte Aktion sein, die ausgeführt wird, wenn die Workstation konfiguriert ist. Weitere Informationen finden Sie unter [Konfigurieren eines Windows Virtual PC-Images für MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

4.  Nachdem der MED-V-Arbeitsbereich durch Ftscompletion.exe neu gestartet wurde, ist der Endbenutzer angemeldet. Wenn Sie Ihr Kennwort bei der erstmaligen Einrichtung nicht gespeichert haben, werden Sie erneut dazu aufgefordert. Der MED-V-Arbeitsbereich wird dann gestartet und für den Benutzer konfiguriert. Die Konfiguration umfasst das Anwenden von Gruppenrichtlinien.

    Es wird empfohlen, nur die Richtlinien anzuwenden, die in einer Anwendungs Kompatibilitätsumgebung für Windows XP sinnvoll sind. Beispielsweise müssen Desktop Personalisierungsrichtlinien normalerweise nicht angewendet werden und sollten deaktiviert sein. Weitere Informationen zum Zulassen nur lokaler Profile finden Sie unter [Gruppenrichtlinieneinstellungen für Roaming-Benutzerprofile](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

Nach Abschluss der erstmaligen Einrichtung wird der Endbenutzer benachrichtigt, dass die veröffentlichten Anwendungen bereit sind. Sie können dann über das **Startmenü** auf die im MED-V-Arbeitsbereich installierten Anwendungen zugreifen.

## Verwandte Themen


[Vorbereiten der Bereitstellungsumgebung für MED-V](prepare-the-deployment-environment-for-med-v.md)

[Bereitstellung von MED-V](deployment-of-med-v.md)









