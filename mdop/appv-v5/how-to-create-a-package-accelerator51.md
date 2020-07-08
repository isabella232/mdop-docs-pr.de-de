---
title: So erstellen Sie einen Package Accelerator
description: So erstellen Sie einen Package Accelerator
author: dansimp
ms.assetid: b61f3581-7933-443e-b872-a96bed9ff8d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6893f2e9bb9db473d285026015c3399fb0074015
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805597"
---
# So erstellen Sie einen Package Accelerator


App-V 5,1-Paket Beschleuniger generieren automatisch neue virtuelle Anwendungspakete.

**Hinweis:**  
Sie können PowerShell zum Erstellen eines Paket Beschleunigers verwenden. Weitere Informationen finden Sie unter [Erstellen eines Paket Beschleunigers mithilfe von PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md).



Gehen Sie wie folgt vor, um einen Paket Beschleuniger zu erstellen.

**Wichtig**  
Paket Beschleuniger können Kennwort-und benutzerspezifische Informationen enthalten. Daher müssen Sie Paket Beschleuniger und die zugehörigen Installationsmedien an einem sicheren Speicherort speichern, und Sie sollten den Paket Beschleuniger nach der Erstellung digital signieren, damit der Herausgeber überprüft werden kann, wenn der App-V 5,1-Paket Beschleuniger angewendet wird.



**Wichtig**  
Bevor Sie mit der folgenden Vorgehensweise beginnen, sollten Sie die folgenden Schritte ausführen:

-   Kopieren Sie das virtuelle Anwendungspaket, das Sie zum Erstellen des Paket Beschleunigers verwenden, lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.

-   Kopieren Sie alle erforderlichen Installationsdateien, die dem virtuellen Anwendungspaket zugeordnet sind, auf den Computer, auf dem der Sequencer ausgeführt wird.



**So erstellen Sie einen Paket Beschleuniger**

1.  **Wichtig**  
    Der App-V 5,1-Sequenzer gewährt der Softwareanwendung, die Sie zum Erstellen des Paket Beschleunigers verwenden, keine Lizenzrechte. Sie müssen sich an alle Endbenutzer-Lizenzbestimmungen für die von Ihnen verwendete Anwendung halten. Sie müssen sicherstellen, dass die Lizenzbestimmungen der Softwareanwendung es Ihnen ermöglichen, mithilfe von App-V 5,1 Sequencer einen Paket Beschleuniger zu erstellen.



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. Wenn Sie den App-v 5,1-Assistenten zum **Erstellen von Paket Beschleunigern** starten möchten, klicken Sie in der APP-v 5,1-Sequenzer-Konsole auf **Extras**  /  **Beschleuniger erstellen**.

3. Klicken Sie auf der Seite **Paket auswählen** zum Angeben eines vorhandenen virtuellen Anwendungspakets, das zum Erstellen des Paket Beschleunigers verwendet werden soll, auf **Durchsuchen**, und suchen Sie das vorhandene virtuelle Anwendungspaket (AppV-Datei).

   **Tipp**  
   Kopieren Sie die Dateien, die dem virtuellen Anwendungspaket zugeordnet sind, das Sie lokal für den Computer verwenden möchten, auf dem der Sequencer ausgeführt wird.



~~~
Click **Next**.
~~~

4. Klicken Sie auf der Seite **Installationsdateien** auf **Durchsuchen**, um den Ordner mit den Installationsdateien anzugeben, die Sie zum Erstellen des ursprünglichen virtuellen Anwendungspakets verwendet haben, und wählen Sie dann das Verzeichnis aus, das die Installationsdateien enthält.

   **Tipp**  
   Kopieren Sie den Ordner, der die erforderlichen Installationsdateien enthält, auf den Computer, auf dem der Sequencer ausgeführt wird.



5. Wenn die Anwendung bereits auf dem Computer installiert ist, auf dem der Sequencer ausgeführt wird, wählen Sie im **lokalen System installierte Dateien**aus, um die Installationsdatei anzugeben. Um diese Option verwenden zu können, muss die Anwendung bereits im Standardinstallationspfad installiert sein.

6. Überprüfen Sie auf der Seite **Gathering Information** die Dateien, die sich nicht in dem auf der Seite **Installationsdateien** dieses Assistenten angegebenen Speicherort befinden. Wenn die angezeigten Dateien nicht erforderlich sind, wählen Sie **diese Dateien entfernen**aus, und klicken Sie dann auf **weiter**. Wenn die Dateien erforderlich sind, klicken Sie auf **zurück** , und kopieren Sie die erforderlichen Dateien in das auf der Seite **Installationsdateien** angegebene Verzeichnis.

   **Hinweis:**  
   Sie müssen entweder die nicht benötigten Dateien entfernen oder auf **zurück** klicken und die erforderlichen Dateien suchen, um zur nächsten Seite des Assistenten zu gelangen.



7. Überprüfen Sie auf der Seite **"Dateien auswählen** " sorgfältig die gefundenen Dateien, und löschen Sie alle Dateien, die aus dem Paket Beschleuniger entfernt werden sollen. Wählen Sie nur Dateien aus, die erforderlich sind, damit die Anwendung erfolgreich ausgeführt werden kann, und klicken Sie dann auf **weiter**.

8. Vergewissern Sie sich auf der Seite **Anwendungen überprüfen** , dass alle Installationsdateien angezeigt werden, die zum Erstellen des Pakets erforderlich sind. Wenn der Paket Beschleuniger zum Erstellen eines neuen Pakets verwendet wird, sind alle im Bereich **Anwendungen** angezeigten Installationsdateien erforderlich, um das Paket zu erstellen.

   Falls erforderlich, klicken Sie auf **Hinzufügen**, um weitere Installationsprogrammdateien hinzuzufügen. Wenn Sie nicht benötigte Installationsdateien entfernen möchten, wählen Sie die Installationsdatei aus, und klicken Sie dann auf **Löschen**. Wenn Sie die Eigenschaften bearbeiten möchten, die einem Installationsprogramm zugeordnet sind, klicken Sie auf **Bearbeiten**. Die in diesem Schritt angegebenen Installationsdateien sind erforderlich, wenn der Paket Beschleuniger zum Erstellen eines neuen virtuellen Anwendungspakets verwendet wird. Nachdem Sie die angezeigten Informationen bestätigt haben, klicken Sie auf **weiter**.

9. Klicken Sie auf der Seite **"Anleitungen auswählen** " auf **Durchsuchen**, um eine Datei anzugeben, die Informationen zur Funktionsweise des Paket Beschleunigers enthält. Diese Datei kann beispielsweise Informationen dazu enthalten, wie der Computer, auf dem der Sequencer ausgeführt wird, konfiguriert werden soll, Anwendungs Voraussetzungs Informationen für Zielcomputer und allgemeine Hinweise. Sie sollten alle erforderlichen Informationen für die erfolgreiche Anwendung des Paket Beschleunigers angeben. Die ausgewählte Datei muss im Rich-Text-Format (RTF) oder im Textdateiformat (txt) vorliegen. Klicken Sie auf **Weiter**.

10. Klicken Sie auf der Seite **Paket Beschleuniger erstellen** auf **Durchsuchen** , um anzugeben, wo der Paket Beschleuniger gespeichert werden soll, und wählen Sie das Verzeichnis aus.

11. Klicken Sie auf der Seite **Fertigstellung** auf **Schließen**, um den Assistenten zum **Erstellen von Paket Beschleunigern** zu schließen.

   **Wichtig**  
   Wenn Sie sicherstellen möchten, dass der Paket Beschleuniger so sicher wie möglich ist und der Herausgeber überprüft werden kann, wenn der Paket Beschleuniger angewendet wird, sollten Sie immer den Paket Beschleuniger digital signieren.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

[So erstellen Sie ein virtuelles Anwendungspaket mit einem App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)









