---
title: So erstellen Sie App-V Package Accelerators (App-V 4.6 SP1)
description: So erstellen Sie App-V Package Accelerators (App-V 4.6 SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807187"
---
# So erstellen Sie App-V Package Accelerators (App-V 4.6 SP1)


Sie können App-V-Paket Beschleuniger verwenden, um automatisch ein neues virtuelles Anwendungspaket zu generieren. Nachdem Sie erfolgreich einen Paket Beschleuniger erstellt haben, können Sie den Paket Beschleuniger wieder verwenden und freigeben. Weitere Informationen zu Paket Beschleunigern finden Sie unter [Informationen zu app-v-Paket Beschleunigern (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md). Das Erstellen von App-V-Paket Beschleunigern ist eine erweiterte Aufgabe. Paket Beschleuniger können Kennwort-und benutzerspezifische Informationen enthalten. Daher müssen Sie Paket Beschleuniger und die zugehörigen Installationsmedien an einem sicheren Speicherort speichern, und Sie sollten den Paket Beschleuniger nach der Erstellung digital signieren, damit der Herausgeber überprüft werden kann, wenn der App-V-Paket Beschleuniger angewendet wird.

In einigen Fällen müssen Sie möglicherweise die Anwendung lokal auf dem Computer installieren, auf dem der Sequencer ausgeführt wird, um den Paket Beschleuniger zu erstellen. Versuchen Sie zunächst, den Paket Beschleuniger mithilfe des Installationsmediums zu erstellen, und wenn es eine Reihe fehlender Dateien gibt, die erforderlich sind, installieren Sie die Anwendung lokal auf dem Computer, auf dem der Sequencer ausgeführt wird, und erstellen Sie dann den Paket Beschleuniger.

**Wichtig**  
Bevor Sie mit der folgenden Vorgehensweise beginnen, sollten Sie die folgenden Schritte ausführen:

-   Kopieren Sie das virtuelle Anwendungspaket, das Sie zum Erstellen des Paket Beschleunigers verwenden müssen, lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.

-   Kopieren Sie alle erforderlichen Installationsdateien, die dem virtuellen Anwendungspaket zugeordnet sind, auf den Computer, auf dem der Sequencer ausgeführt wird.



**Wichtig**  
Disclaimer: Microsoft Application Virtualization Sequencer gibt Ihnen keine Lizenzrechte für die Softwareanwendung, die Sie zum Erstellen eines Paket Beschleunigers verwenden. Sie müssen sich an alle Endnutzer-Lizenzbestimmungen für diese Anwendung halten. Sie müssen sicherstellen, dass die Lizenzbestimmungen der Softwareanwendung es Ihnen ermöglichen, mithilfe von Application Virtualization Sequencer einen Paket Beschleuniger zu erstellen.



**So erstellen Sie einen App-V-Paket Beschleuniger**

1.  Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie zum Starten des App-v-Assistenten zum **Erstellen von Paket Beschleunigern** im App-v-Sequenzer auf **Extras**, die  /  **Paket Beschleuniger erstellen**.

3.  Klicken Sie auf der Seite **Paket auswählen** zum Angeben eines vorhandenen virtuellen Anwendungspakets, das zum Erstellen des Paket Beschleunigers verwendet werden soll, auf **Durchsuchen**, und suchen Sie das vorhandene virtuelle Anwendungspaket (SPRJ-Datei).

    **Tipp**  
    Kopieren Sie die Dateien, die dem virtuellen Anwendungspaket zugeordnet sind, das Sie lokal für den Computer verwenden möchten, auf dem der Sequencer ausgeführt wird.



~~~
Click **Next**.
~~~

4. Klicken Sie auf der Seite **Installationsdateien** auf **Durchsuchen**, um den Ordner mit den Installationsdateien anzugeben, die Sie zum Erstellen des ursprünglichen virtuellen Anwendungspakets verwendet haben, und wählen Sie dann das Verzeichnis aus, das die Installationsdateien enthält.

   **Tipp**  
   Kopieren Sie den Ordner, der die erforderlichen Installationsdateien enthält, auf den Computer, auf dem der Sequencer ausgeführt wird.



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. Überprüfen Sie auf der Seite **Gathering Information** die Dateien, die sich nicht in dem auf der Seite **Installationsdateien** dieses Assistenten angegebenen Speicherort befinden. Wenn die angezeigten Dateien nicht erforderlich sind, wählen Sie **diese Dateien entfernen**aus, und klicken Sie dann auf **weiter**. Wenn die Dateien erforderlich sind, klicken Sie auf **zurück** , und kopieren Sie die erforderlichen Dateien in das auf der Seite **Installationsdateien** angegebene Verzeichnis.

   **Hinweis:**  
   Sie müssen entweder die nicht benötigten Dateien entfernen oder auf **zurück** klicken und die erforderlichen Dateien suchen, um zur nächsten Seite des Assistenten zu gelangen.



6. Überprüfen Sie auf der Seite **"Dateien auswählen** " sorgfältig die gefundenen Dateien, und löschen Sie alle Dateien, die aus dem Paket Beschleuniger entfernt werden sollen. Wählen Sie nur Dateien aus, die erforderlich sind, damit die Anwendung erfolgreich ausgeführt werden kann, und klicken Sie dann auf **weiter**.

7. Vergewissern Sie sich auf der Seite **Anwendungen überprüfen** , dass alle Installationsdateien angezeigt werden, die zum Erstellen des Pakets erforderlich sind. Wenn der Paket Beschleuniger zum Erstellen eines neuen Pakets verwendet wird, sind alle im Bereich **Anwendungen** angezeigten Installationsdateien erforderlich, um das Paket zu erstellen.

   Falls erforderlich, klicken Sie auf **Hinzufügen**, um weitere Installationsprogrammdateien hinzuzufügen. Wenn Sie nicht benötigte Installationsdateien entfernen möchten, wählen Sie die Installationsdatei aus, und klicken Sie dann auf **Löschen**. Wenn Sie die Eigenschaften bearbeiten möchten, die einem Installationsprogramm zugeordnet sind, klicken Sie auf **Bearbeiten**. Die in diesem Schritt angegebenen Installationsdateien sind erforderlich, wenn der Paket Beschleuniger zum Erstellen eines neuen virtuellen Anwendungspakets verwendet wird. Nachdem Sie die angezeigten Informationen bestätigt haben, klicken Sie auf **weiter**.

8. Klicken Sie auf der Seite **"Anleitungen auswählen** " auf **Durchsuchen**, um eine Datei anzugeben, die Informationen zur Funktionsweise des Paket Beschleunigers enthält. Diese Datei kann beispielsweise Informationen dazu enthalten, wie der Computer, auf dem der Sequencer ausgeführt wird, konfiguriert werden soll, Anwendungs Voraussetzungs Informationen für Zielcomputer und allgemeine Hinweise. Sie sollten alle erforderlichen Informationen für die erfolgreiche Anwendung des Paket Beschleunigers angeben. Die ausgewählte Datei muss im Rich-Text-Format (RTF) oder im Textdateiformat (txt) vorliegen. Klicken Sie auf **Weiter**.

9. Klicken Sie auf der Seite **Paket Beschleuniger erstellen** auf **Durchsuchen** , um anzugeben, wo der Paket Beschleuniger gespeichert werden soll, und wählen Sie das Verzeichnis aus.

10. Klicken Sie auf der Seite **Fertigstellung** auf **Schließen**, um den Assistenten zum **Erstellen von Paket Beschleunigern** zu schließen.

   **Wichtig**  
   Wenn Sie sicherstellen möchten, dass der Paket Beschleuniger so sicher wie möglich ist und der Herausgeber überprüft werden kann, wenn der Paket Beschleuniger angewendet wird, sollten Sie immer den Paket Beschleuniger digital signieren.



## Verwandte Themen


Konfigurieren des Application Virtualization Sequencer (app-v 4,6 SP1) so wird es [gemacht: Anwenden eines Paket Beschleunigers zum Erstellen eines virtuellen Anwendungspakets (app-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)









