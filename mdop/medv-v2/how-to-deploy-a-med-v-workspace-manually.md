---
title: So stellen Sie einen MED-V-Arbeitsbereich manuell bereit
description: So stellen Sie einen MED-V-Arbeitsbereich manuell bereit
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812259"
---
# So stellen Sie einen MED-V-Arbeitsbereich manuell bereit


In einigen Fällen möchten Sie möglicherweise Ihren MED-V-Arbeitsbereich manuell bereitstellen, beispielsweise wenn Ihr Unternehmen kein elektronisches Softwareverteilungssystem zum Bereitstellen von Anwendungen verwendet.

Dieser Abschnitt enthält Anweisungen dazu, wie Sie einen MED-V-Arbeitsbereich manuell bereitstellen.

**So stellen Sie einen MED-V-Arbeitsbereich manuell bereit**

1.  Kopieren Sie alle erforderlichen Anwendungen und die MED-V Workspace-Paketdateien auf ein freigegebenes Laufwerk oder auf eine DVD. Die folgende Liste enthält die erforderlichen Anwendungen und Dateien.

    -   **Windows Virtual PC**. Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.

    -   **Windows Virtual PC-Ergänzungen und-Updates**. Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.

    -   **Installationsdatei des Med-v-Host-Agents** – installiert den Host-Agent (Med-v \ _HostAgent \ _setup Installationsdatei).

        **Warnung**  
        Schließen Sie Internet Explorer, bevor Sie den MED-V-Host-Agent installieren, andernfalls können Konflikte später bei der URL-Umleitung auftreten. Sie können dies auch tun, indem Sie während einer Verteilung einen Neustart des Computers angeben.



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. Installieren Sie die folgenden in der angegebenen Reihenfolge. Der Endbenutzer kann diese Aufgabe manuell ausführen, oder Sie können ein Skript erstellen, um Folgendes zu installieren:

   -   Windows Virtual PC und die Windows Virtual PC-Ergänzungen und-Updates. Ein Neustart des Computers ist erforderlich.

   -   Der MED-V-Host-Agent.

       **Hinweis:**  
       Wenn Sie ausgeführt wird, muss Internet Explorer neu gestartet werden, bevor die Installation des MED-V-Host-Agents abgeschlossen werden kann.



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. Führen Sie die erstmalige Einrichtung durch.

   Nachdem Sie den Med-v-Arbeitsbereich installiert haben, haben Sie die Möglichkeit, Med-v zu starten. Dadurch wird der MED-V-Host-Agent gestartet. Sie können entweder Med-v zu diesem Zeitpunkt starten oder den Med-v-Host-Agent später starten, um die erstmalige Einrichtung abzuschließen.

   Klicken Sie zum Starten des Med-v-Host-Agents auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **Med-v-Host-Agent**.

## Verwandte Themen


[So stellen Sie einen MED-V-Arbeitsbereich über eines elektronischen Softwareverteilungssystem bereit](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[So stellen Sie einen MED-V-Arbeitsbereich in ein Windows 7-Image bereit](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[Bereitstellen des MED-V-Arbeitsbereichspakets](deploying-the-med-v-workspace-package.md)









