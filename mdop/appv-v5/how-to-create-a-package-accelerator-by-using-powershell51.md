---
title: So erstellen Sie einen Package Accelerator mithilfe von PowerShell
description: So erstellen Sie einen Package Accelerator mithilfe von PowerShell
author: dansimp
ms.assetid: 0cb98394-4477-4193-8c5f-1c1773c7263a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 347572343cff058a7494574035464d66c4d61be4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805609"
---
# So erstellen Sie einen Package Accelerator mithilfe von PowerShell


App-V 5,1-Paket Beschleuniger Sequenzieren automatisch große, komplexe Anwendungen. Darüber hinaus müssen Sie beim Anwenden eines App-V 5,1-Paket Beschleunigers nicht immer eine Anwendung manuell installieren, um das virtualisierte Paket zu erstellen.

**So erstellen Sie einen Paket Beschleuniger**

1.  Installieren Sie den App-V 5,1-Sequenzer. Weitere Informationen zum Installieren des Sequencers finden Sie unter [Installieren des Sequencers](how-to-install-the-sequencer-51beta-gb18030.md).

2.  Klicken Sie auf **Start** , und geben Sie **PowerShell**ein, um eine PowerShell-Konsole zu öffnen. Klicken Sie mit der rechten Maustaste auf **Windows PowerShell**, und wählen Sie **Als Administrator ausführen** aus. Verwenden Sie das Cmdlet **New-AppvPackageAccelerator** .

3.  Wenn Sie einen Paket Beschleuniger erstellen möchten, stellen Sie sicher, dass Sie über das AppV-Paket verfügen, um eine Zugriffstaste von den Installationsmedien oder Installationsdateien sowie optional eine Read Me-Datei für die Benutzer des Beschleunigers zu erstellen. Die folgenden Parameter sind erforderlich, um das Paket Beschleuniger-Cmdlet zu verwenden:

    -   **InstalledFilesPath** – gibt den Anwendungs Installationspfad an.

    -   **Installer** – gibt den Pfad zu den Anwendungs Installationsmedien an.

    -   **InputPackagePath** – gibt den Pfad zum AppV-Paket an.

    -   **Path** – gibt das Ausgabeverzeichnis für das Paket an.

    Im folgenden Beispiel wird gezeigt, wie Sie einen Paket Beschleuniger mit einem AppV-Paket und den Installationsmedien erstellen können:

    **New-AppvPackageAccelerator-InputPackagePath &lt; path to the. AppV Datei &gt; -Installer- &lt; Pfad zur ausführbaren Installationsprogramm &gt; -Pfad &lt; Verzeichnis des Ausgabepfads&gt;**

    Zusätzliche optionale Parameter, die mit dem Cmdlet **New-AppvPackageAccelerator** verwendet werden können, werden in der folgenden Liste angezeigt:

    -   **AcceleratorDescriptionFile** – gibt den Pfad zu den vom Benutzer erstellten Paket Beschleuniger Anweisungen an. Die Anweisungen für den Paket Beschleuniger sind **txt-** oder **RTF** -Beschreibungsdateien, die mit dem mit dem Paket Beschleuniger erstellten Paket verpackt werden.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Verwalten von App-V 5.1 mithilfe von PowerShell](administering-app-v-51-by-using-powershell.md)

 

 





