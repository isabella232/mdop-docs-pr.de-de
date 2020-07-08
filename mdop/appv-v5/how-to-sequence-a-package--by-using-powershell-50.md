---
title: Sequenzierung eines Pakets mithilfe von PowerShell
description: Sequenzierung eines Pakets mithilfe von PowerShell
author: dansimp
ms.assetid: b41feed9-d1c5-48a3-940c-9a21d594f4f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbb9641ba75eda4d190892fa2bd0043c92ed9006
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805174"
---
# Sequenzierung eines Pakets mithilfe von PowerShell


Gehen Sie wie folgt vor, um ein neues App-V 5,0-Paket mit PowerShell zu erstellen.

**Hinweis**  Bevor Sie dieses Verfahren verwenden, müssen Sie die zugehörigen Installationsdateien auf den Computer kopieren, auf dem der Sequencer ausgeführt wird, und Sie haben den Sequencer-Abschnitt der [Planung für den App-V 5,0-Sequenzer und die Client Bereitstellung](planning-for-the-app-v-50-sequencer-and-client-deployment.md)gelesen und verstanden.

 

**So erstellen Sie eine neue virtuelle Anwendung mithilfe von PowerShell**

1.  Installieren Sie den App-V 5,0-Sequenzer. Weitere Informationen zum Installieren des Sequencers finden Sie unter [Installieren des Sequencers](how-to-install-the-sequencer-beta-gb18030.md).

2.  Klicken Sie auf **Start** , und geben Sie **PowerShell**ein, um eine PowerShell-Konsole zu öffnen. Klicken Sie mit der rechten Maustaste auf **Windows PowerShell**, und wählen Sie **Als Administrator ausführen** aus.

3.  Verwenden Sie die PowerShell-Konsole, und geben Sie Folgendes ein: **Import-Module appvsequencer**.

4.  Verwenden Sie zum Erstellen eines Pakets das Cmdlet **New-AppvSequencerPackage** . Die folgenden Parameter sind erforderlich, um ein Paket zu erstellen:

    -   **Name** – gibt den Namen des Pakets an.

    -   **PrimaryVirtualApplicationDirectory** – gibt den Pfad zu dem Verzeichnis an, das zum Installieren der Anwendung verwendet wird. Dieser Pfad muss vorhanden sein.

    -   **Installer** – gibt den Pfad zum zugehörigen Anwendungs Installationsprogramm an.

    -   **Path** – gibt das Ausgabeverzeichnis für das Paket an.

    Beispiel:

    **New-AppvSequencerPackage – Name Name &lt; des Package &gt; -PrimaryVirtualApplicationDirectory- &lt; Pfads zum Paket-root &gt; -Installer- &lt; Pfad zum ausführbaren Installer &gt; -OutputPath- &lt; Verzeichnis des Ausgabepfads&gt;**

    Warten Sie, bis der Sequencer das Paket erstellt hat. Das Erstellen eines Pakets mit PowerShell kann Zeit in Anspruch nehmen. Wenn das Paket nicht erfolgreich erstellt wurde, wird ein Fehler zurückgegeben.

    In der folgenden Liste werden zusätzliche optionale Parameter angezeigt, die mit dem Cmdlet **New-AppvSequencerPackage** verwendet werden können:

    -   AcceleratorFilePath – gibt den Pfad zur Beschleuniger. CAB-Datei an, um ein Paket zu generieren.

    -   InstalledFilesPath – gibt den Pfad an, in dem die lokal installierten Dateien der Anwendung gespeichert werden.

    -   InstallMediaPath – gibt den Pfad an, in dem sich das Installationsmedium befindet

    -   TemplateFilePath – gibt den Pfad zu einer Vorlagendatei an, wenn Sie den Sequenz Prozess anpassen möchten.

    -   FullLoad – gibt an, dass das Paket vollständig auf den Computer heruntergeladen werden muss, auf dem die App-V 5,0 ausgeführt wird, bevor es geöffnet werden kann.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Verwalten von App-V mithilfe von PowerShell](administering-app-v-by-using-powershell.md)

 

 





