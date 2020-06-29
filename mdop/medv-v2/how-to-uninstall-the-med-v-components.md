---
title: So deinstallieren Sie die MED-V-Komponenten
description: So deinstallieren Sie die MED-V-Komponenten
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804670"
---
# So deinstallieren Sie die MED-V-Komponenten


Unter bestimmten Umständen möchten Sie möglicherweise die Microsoft Enterprise Desktop Virtualization (MED-V) 2,0-Komponenten in Ihrem Unternehmen ganz oder teilweise deinstallieren. Sie haben beispielsweise alle Kompatibilitätsprobleme des Anwendungs Betriebssystems behoben, oder Sie möchten einen anderen MED-V-Arbeitsbereich in Ihrem Unternehmen bereitstellen.

In der Regel können Sie Ihr ESD-System (Electronic Software Distribution) so konfigurieren, dass die MED-V-Komponenten mithilfe eines Windows-basierten Installationsprogramms deinstalliert werden. Alternativ können Sie alle oder einige MED-V-Komponenten manuell deinstallieren.

**Wichtig**  Bevor Sie den Med-v-Host-Agent deinstallieren können, müssen Sie zunächst alle installierten Med-v-Arbeitsbereiche deinstallieren.

 

Führen Sie die folgenden Verfahren aus, um die MED-V-Komponenten aus Ihrem Unternehmen zu deinstallieren.

**So deinstallieren Sie MED-V mithilfe eines elektronischen Softwareverteilungssystems**

1.  Verwenden Sie Ihr ESD-System, um ein Skript zu verteilen, das das uninstall.exe ausführbare Programm für jeden MED-V-Arbeitsbereich aufruft, den Sie deinstallieren möchten. Die Datei befindet sich unter C:\\ProgramData\\Microsoft\\Medv\\Workspace. Sie können ein Flag so einrichten, dass das Programm zum Deinstallieren der ausführbaren Datei automatisch ausgeführt wird, damit Endbenutzer die Deinstallation nicht kennen.

2.  Erstellen Sie ein Paket, um die Installationsdatei des Med-v-Host-Agents auf jedem Computer zu verteilen, auf dem ein Med-v-Arbeitsbereich deinstalliert wurde. Konfigurieren Sie das Paket so, dass die Deinstallation im unbeaufsichtigten Modus ausgeführt wird.

Der ESD-Client erkennt, wann die neuen Pakete verfügbar sind, und beginnt, die Pakete pro Definition und Anforderungen zu deinstallieren.

**So deinstallieren Sie einen MED-V-Arbeitsbereich manuell**

1.  Klicken Sie auf dem Hostcomputer auf **Start**, klicken Sie auf **System**Steuerung, und klicken Sie dann auf **Programme und Funktionen**.

2.  Wählen Sie im Fenster **Programme und Funktionen** den MED-V-Arbeitsbereich aus, den Sie entfernen möchten, und klicken Sie dann auf **deinstallieren**. (Der Med-v Workspace hat den Namen "Med-v Workspace- &lt; *Arbeitsbereich \ _name* &gt; "). Der &lt; *Arbeitsbereich \ _name* &gt; **Setup-Assistent** wird geöffnet.

3.  Klicken Sie im **Setup-Assistenten**auf **weiter**, und klicken Sie dann auf **Entfernen**.

4.  Wenn Sie dies bevorzugen, aktivieren Sie das Kontrollkästchen, um den von MED-V erstellten Master-VHD-Datenträger und die differenzierenden Datenträger zu löschen. Dies ist nicht erforderlich, gibt aber Speicherplatz frei, nachdem die Deinstallation abgeschlossen ist.

5.  Klicken Sie auf **Entfernen**.

    **Hinweis**  Wenn MED-V zurzeit ausgeführt wird, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob Sie es beenden möchten. Klicken Sie auf **Ja** , um die Deinstallation fortzusetzen. Klicken Sie auf **Nein** , um die Deinstallation abzubrechen.

     

Alternativ können Sie einen MED-V-Arbeitsbereich entfernen, indem Sie die `uninstall.exe` Datei ausführen, die sich normalerweise unter C:\\ProgramData\\Microsoft\\Medv\\Workspace. befindet.

**So deinstallieren Sie den MED-V-Host-Agent manuell**

1.  Klicken Sie auf dem Windows 7-Hostcomputer auf **Start**, klicken Sie auf **System**Steuerung, und klicken Sie dann auf **Programme und Funktionen**.

2.  Wählen Sie im Fenster **Programme und Funktionen** den **MED-V-Host-Agent**aus, und klicken Sie dann auf **deinstallieren**.

    Der Windows Installer entfernt den MED-V-Host-Agent.

    **Hinweis**  Wenn Sie versuchen, den Med-v-Host-Agent zu deinstallieren, bevor Sie den Med-v-Arbeitsbereich deinstallieren, wird ein Dialogfeld angezeigt, das besagt, dass Sie zuerst den Med-v-Arbeitsbereich deinstallieren müssen. Klicken Sie auf **OK**, um den Vorgang fortzusetzen.

     

**So deinstallieren Sie den MED-V Workspace-Paketer manuell**

1.  Klicken Sie auf dem Hostcomputer auf **Start**, klicken Sie auf **System**Steuerung, und klicken Sie dann auf **Programme und Funktionen**.

2.  Wählen Sie im Fenster **Programme und Features** den Eintrag **MED-V Workspace Packager**aus, und klicken Sie dann auf **deinstallieren**.

    Der Windows Installer entfernt den MED-V Workspace-Paketer.

    **Hinweis**  Sie können den Med-v-Arbeitsbereichs-Packager jederzeit deinstallieren, ohne die bereitgestellten Med-v-Arbeitsbereiche zu beeinflussen.

     

## Verwandte Themen


[Bereitstellen der MED-V-Komponenten](deploy-the-med-v-components.md)

 

 





