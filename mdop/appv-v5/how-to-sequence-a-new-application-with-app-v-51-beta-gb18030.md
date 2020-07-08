---
title: So sequenzieren Sie eine neue Anwendung mit App-V 5.1
description: So sequenzieren Sie eine neue Anwendung mit App-V 5.1
author: dansimp
ms.assetid: 7d7699b1-0cb8-450d-94e7-5af937e16c21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43edd9357e31f4884ed7baec3d35fa01bf2abe54
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805186"
---
# So sequenzieren Sie eine neue Anwendung mit App-V 5.1


**Zu überprüfen oder zu tun, bevor Sie mit der Sequenzierung beginnen**

1.  Ermitteln Sie den Typ des virtualisierten Anwendungspakets, das Sie erstellen möchten:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Anwendungstyp</th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Standard</p></td>
    <td align="left"><p>Erstellt ein Paket, das eine Anwendung oder eine Suite von Anwendungen enthält. Dies ist die bevorzugte Option für die meisten Anwendungstypen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Add-on oder Plug-in</p></td>
    <td align="left"><p>Erstellt ein Paket, das die Funktionalität einer Standardanwendung erweitert, beispielsweise ein Plug-in für Microsoft Excel. Darüber hinaus können Sie Plug-Ins für nativ installierte Anwendungen oder ein anderes Paket verwenden, das mithilfe von Verbindungsgruppen verknüpft ist.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Middleware</p></td>
    <td align="left"><p>Erstellt ein Paket, das für eine Standardanwendung, beispielsweise Java, erforderlich ist. Middleware-Pakete werden für Verknüpfungen mit anderen Paketen mithilfe von Verbindungsgruppen verwendet.</p></td>
    </tr>
    </tbody>
    </table>



2.  Kopieren Sie alle erforderlichen Installationsdateien auf den Computer, auf dem der Sequencer ausgeführt wird.

3.  Erstellen Sie ein Sicherungsabbild Ihrer virtuellen Umgebung, bevor Sie eine Anwendung sequenzieren, und kehren Sie dann jedes Mal wieder zu diesem Bild zurück, nachdem Sie die Sequenzierung einer Anwendung abgeschlossen haben.

4.  Überprüfen Sie die folgenden Elemente:

    -   Wenn ein Anwendungs Installationsprogramm den Sicherheitszugriff auf eine neue oder vorhandene Datei oder ein vorhandenes Verzeichnis ändert, werden diese Änderungen nicht im Paket erfasst.

    -   Wenn kurze Pfade für das Zielvolumen des virtualisierten Pakets deaktiviert wurden, müssen Sie das Paket auch auf ein Volume abbilden, das erstellt wurde und bei dem die Short-Pfade deaktiviert sind. Dies kann nicht das System Volume sein.

> [!NOTE]  
> App-V 5. x Sequencer kann keine Anwendungen mit Dateinamen abgleichen, die "CO_ &lt; x &gt; " entsprechen, wobei x eine beliebige Zahl ist. Fehler 0x8007139F wird generiert.

**So Sequenzieren Sie eine neue Standardanwendung**

1.  Klicken Sie auf dem Computer, auf dem der Sequencer ausgeführt wird, auf **Alle Programme**, und klicken Sie dann auf **Microsoft Application Virtualization**, und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie im Sequencer auf **Neues virtuelles Anwendungspaket erstellen**. Wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.

3.  Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt oder dass das Paket unnötige Daten enthält. Sie sollten alle potenziellen Probleme beheben, bevor Sie fortfahren. Nachdem Sie Korrekturen vorgenommen haben, klicken Sie auf **Aktualisieren** , um die aktualisierten Informationen anzuzeigen. Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.

    > [!IMPORTANT]
    > Wenn Sie die Virenscansoftware deaktivieren müssen, sollten Sie zuerst den Computer scannen, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder böswilligen Dateien hinzugefügt werden können.



~~~
> [!NOTE]  
> There is currently no way to disable Windows Defender in Windows 10. If you receive a warning, you can safely ignore it. It is unlikely that Windows Defender will affect sequencing at all.
~~~



4. Klicken Sie auf der Seite **Typ der Anwendung** auf das Kontrollkästchen **Standardanwendung (Standard)** , und klicken Sie dann auf **weiter**.

5. Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an.

   > [!NOTE]  
   > Wenn das angegebene Anwendungs Installationsprogramm den Sicherheitszugriff auf eine Datei oder ein Verzeichnis ändert, vorhandene oder neue, werden die zugehörigen Änderungen nicht in das Paket aufgenommen.



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll. Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll. Der Paket Name wird in der App-V 5,0-Verwaltungskonsole angezeigt.

   Klicken Sie auf **Weiter**.

7. Wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, können Sie auf der **Installations** Seite fortfahren, die Anwendung zu installieren, damit der Sequencer den Installationsvorgang überwachen kann.

   > [!IMPORTANT]
   > Sie sollten Anwendungen immer an einem sicheren Ort installieren und sicherstellen, dass während der Überwachung keine anderen Benutzer am Computer angemeldet sind, auf dem der Sequencer ausgeführt wird.



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. Warten Sie auf der **Installations** Seite, während der Sequencer das virtualisierte Anwendungspaket konfiguriert.

9. Führen Sie auf der Seite **Software konfigurieren** optional die Programme aus, die im Paket enthalten sind. In diesem Schritt können Sie alle erforderlichen Lizenz-oder Konfigurationsaufgaben ausführen, bevor Sie das Paket auf Zielcomputern bereitstellen und ausführen. Wenn Sie alle Programme auf einmal ausführen möchten, wählen Sie mindestens ein Programm aus, und klicken Sie dann auf **alle ausführen**. Wenn Sie bestimmte Programme ausführen möchten, wählen Sie das Programm oder die Programme aus, und klicken Sie dann auf **ausgewählt ausführen**. Führen Sie die erforderlichen Konfigurationsaufgaben aus, und schließen Sie dann die Anwendungen. Möglicherweise müssen Sie einige Minuten warten, bis alle Programme ausgeführt werden.

   > [!NOTE]  
   > Wenn Sie Aufgaben der ersten Verwendung für eine Anwendung ausführen möchten, die in der Liste nicht zur Verfügung steht, öffnen Sie die Anwendung. Die zugehörigen Informationen werden in diesem Schritt erfasst.



~~~
Click **Next**.
~~~

10. Auf der Seite " **Installationsbericht** " können Sie Informationen zum virtualisierten Anwendungspaket, das Sie gerade sequenziert haben, überprüfen. Doppelklicken Sie in **zusätzlichen Informationen**auf ein Ereignis, um detailliertere Informationen zu erhalten. Klicken Sie auf **weiter**, um fortzufahren.

11. Die Seite " **Anpassen** " wird angezeigt. Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie **jetzt beenden** aus, und fahren Sie mit Schritt 14 dieses Verfahrens fort. Wenn Sie eine der folgenden Anpassungen ausführen möchten, wählen Sie **Anpassen**aus.

    -   Vorbereiten des virtuellen Pakets für Streaming. Durch Streaming wird die Benutzerfreundlichkeit verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern ausgeführt wird.

    -   Geben Sie die Betriebssysteme an, die dieses Paket ausführen können.

    Klicken Sie auf **Weiter**.

12. Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann. Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden. Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden, und klicken Sie dann auf **weiter**.

   > [!NOTE]  
   > Wenn Sie während dieses Schritts keine Anwendungen öffnen, ist die standardmäßige Streaming-Methode eine bedarfsgesteuerte Streaming-Übermittlung. Das bedeutet, dass Anwendungen nach und nach heruntergeladen werden, bis Sie geöffnet werden können, und je nachdem, wie das Laden des Hintergrunds konfiguriert wird, wird die restliche Anwendung geladen.



13. Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann. Wenn Sie zulassen möchten, dass alle unterstützten Betriebssysteme in Ihrer Umgebung dieses Paket ausführen können, wählen Sie zulassen, dass **Dieses Paket unter einem beliebigen Betriebssystem ausgeführt**wird. Wenn Sie dieses Paket so konfigurieren möchten, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, wählen Sie zulassen, dass **Dieses Paket nur unter den folgenden Betriebssystemen ausgeführt** wird, und wählen Sie die Betriebssysteme aus, die dieses Paket ausführen können. Klicken Sie auf **Weiter**.

   > [!IMPORTANT]
   > Stellen Sie sicher, dass die hier angegebenen Betriebssysteme von der Anwendung unterstützt werden, die Sie sequenzieren.



14. Die Seite **Paket erstellen** wird angezeigt. Wenn Sie das Paket ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern mit dem Paket-Editor zu ändern**. Mit dieser Option wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

   Wenn Sie das Paket sofort speichern möchten, wählen Sie **das Paket jetzt speichern** (Standard) aus. Fügen Sie optionale **Kommentare** hinzu, die dem Paket zugeordnet werden sollen. Kommentare sind hilfreich, um die Programmversion und weitere Informationen zum Paket zu identifizieren.

   > [!IMPORTANT]
   > Das System unterstützt keine nicht druckbaren Zeichen in **Kommentaren** und **Beschreibungen**.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. Die Seite **Fertigstellung** wird angezeigt. Überprüfen Sie die Informationen im Bereich **Bericht des virtuellen Anwendungspakets** nach Bedarf, und klicken Sie dann auf **Schließen**. Diese Informationen sind auch in der **Report.xml** -Datei verfügbar, die sich in dem Verzeichnis befindet, in dem das Paket erstellt wurde.

   Das Paket steht jetzt im Sequencer zur Verfügung.

   > [!IMPORTANT]
   > Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.



**So Sequenzieren Sie eine Add-on-oder Plug-in-Anwendung**

1. > [!NOTE]  
   > Bevor Sie das folgende Verfahren ausführen, installieren Sie die übergeordnete Anwendung lokal auf dem Computer, auf dem der Sequencer ausgeführt wird. Wenn Sie die übergeordnete Anwendung virtualisiert haben, können Sie die Schritte im Add-on-oder Plug-in-Workflow ausführen, um die übergeordnete Anwendung auf dem Computer zu entpacken.
   >
   > Wenn Sie beispielsweise ein Plug-in für Microsoft Excel sequenzieren, installieren Sie Microsoft Excel lokal auf dem Computer, auf dem der Sequencer ausgeführt wird. Installieren Sie die übergeordnete Anwendung auch im gleichen Verzeichnis, in dem die Anwendung auf den Zielcomputern installiert ist. Wenn das Plug-in oder Add-on mit einem vorhandenen virtuellen Anwendungspaket verwendet werden soll, installieren Sie die Anwendung auf dem virtuellen Anwendungs Laufwerk, das beim Erstellen des übergeordneten virtuellen Anwendungspakets verwendet wurde.



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. *<strong><em>Klicken Sie im Sequencer auf * </em> Neues virtuelles Anwendungspaket erstellen </strong> . Wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.

3. Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die möglicherweise dazu führen, dass die Paketerstellung fehlschlägt oder dass das Paket unnötige Daten enthält. Sie sollten alle potenziellen Probleme beheben, bevor Sie fortfahren. Nachdem Sie Korrekturen vorgenommen haben, klicken Sie auf **Aktualisieren** , um die aktualisierten Informationen anzuzeigen. Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.

   > [!IMPORTANT]
   > Wenn Sie die Virenscansoftware deaktivieren müssen, sollten Sie zuerst den Computer scannen, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder böswilligen Dateien hinzugefügt werden können.



4. Wählen Sie auf der Seite **Art der Anwendung** **Add-on oder Plug-in**aus, und klicken Sie dann auf **weiter**.

5. Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für das Add-on oder das Plug-in an. Wenn das Add-on oder Plug-in keine zugeordnete Installationsdatei enthält und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.

6. Stellen Sie auf der Seite **primäre Installation** sicher, dass die primäre Anwendung auf dem Computer installiert ist, auf dem der Sequencer ausgeführt wird. Alternativ können Sie ein vorhandenes Paket erweitern, das lokal auf dem Computer gespeichert wurde, auf dem der Sequencer ausgeführt wird. Klicken Sie dazu auf **Paket erweitern**, und wählen Sie dann das Paket aus. Nachdem Sie das übergeordnete Programm erweitert oder installiert haben, wählen Sie **Ich habe das primäre übergeordnete Programm installiert**aus.

   Klicken Sie auf **Weiter**.

7. Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll. Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll. Der Paket Name wird in der App-V 5,0-Verwaltungskonsole angezeigt.

   Klicken Sie auf **Weiter**.

8. Wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, können Sie auf der **Installations** Seite mit der Installation des Plug-ins oder der Add-in-Anwendung fortfahren, damit der Sequencer den Installationsvorgang überwachen kann. Verwenden Sie den Installationsprozess der Anwendung, um die Installation durchzuführen. Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen** , und führen Sie die zusätzlichen Installationsdateien aus. Wenn Sie die Installation abgeschlossen haben, wählen Sie **Ich habe die Installation abgeschlossen**aus, und klicken Sie dann auf **weiter**.

9. Auf der Seite **Installationsbericht** können Sie Informationen zu dem soeben sequenzierten virtuellen Anwendungspaket überprüfen. Eine detailliertere Erläuterung der Informationen, die in **zusätzlichen Informationen**angezeigt werden, finden Sie, indem Sie auf das Ereignis doppelklicken. Nachdem Sie die Informationen überprüft haben, klicken Sie auf **weiter**.

10. Die Seite " **Anpassen** " wird angezeigt. Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie **jetzt beenden** aus, und fahren Sie mit Schritt 12 dieses Verfahrens fort. Wenn Sie eine der folgenden Anpassungen ausführen möchten, wählen Sie **Anpassen**aus.

    -   Optimieren Sie, wie das Paket in einem langsamen oder unzuverlässigen Netzwerk ausgeführt wird.

    -   Geben Sie die Betriebssysteme an, die dieses Paket ausführen können.

    Klicken Sie auf **Weiter**.

11. Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann. Durch Streaming wird die Erfahrung verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern in Netzwerken mit hoher Latenz ausgeführt wird. Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden. Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden. Sie können das Paket auch so konfigurieren, dass es vor dem Öffnen vollständig heruntergeladen werden muss, indem Sie das Kontrollkästchen **zu herunterzuladende Anwendungen erzwingen** auswählen. Klicken Sie auf **Weiter**.

    > [!NOTE]  
    > Falls erforderlich, können Sie verhindern, dass eine Anwendung während dieses Schritts geladen wird. Klicken Sie im Dialogfeld **Anwendungsstart** auf **Beenden** , und aktivieren Sie eines der Kontrollkästchen: **alle Anwendungen beenden** oder **nur diese Anwendung beenden**.



12. Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann. Wenn Sie zulassen möchten, dass alle unterstützten Betriebssysteme in Ihrer Umgebung dieses Paket ausführen können, aktivieren Sie das Kontrollkästchen **Dieses Paket kann auf einem beliebigen Betriebssystem ausgeführt** werden. Um dieses Paket so zu konfigurieren, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, aktivieren Sie das Kontrollkästchen **Dieses Paket nur auf den folgenden Betriebssystemen ausführen lassen** , und wählen Sie dann die Betriebssysteme aus, die dieses Paket ausführen können. Klicken Sie auf **Weiter**.

13. Die Seite **Paket erstellen** wird angezeigt. Wenn Sie das Paket ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern über das Kontrollkästchen Paket-Editor zu ändern** . Mit dieser Option wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

    Wenn Sie das Paket sofort speichern möchten, wählen Sie **das Paket jetzt speichern**aus. Optional können Sie eine **Beschreibung** hinzufügen, die dem Paket zugeordnet ist. Beschreibungen sind hilfreich, um die Version und andere Informationen zum Paket zu identifizieren.

    > [!IMPORTANT]
    > Das System unterstützt keine nicht druckbaren Zeichen in Kommentaren und Beschreibungen.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**So Sequenzieren Sie eine Middleware-Anwendung**

1. Klicken Sie auf dem Computer, auf dem der Sequencer ausgeführt wird, auf **Alle Programme**, und klicken Sie dann auf **Microsoft Application Virtualization**, und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.

2. *<strong><em>Klicken Sie im Sequencer auf * </em> Neues virtuelles Anwendungspaket erstellen </strong> . Wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.

3. Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt oder dass das Paket unnötige Daten enthält. Sie sollten alle potenziellen Probleme beheben, bevor Sie fortfahren. Nachdem Sie Korrekturen vorgenommen haben, klicken Sie auf **Aktualisieren** , um die aktualisierten Informationen anzuzeigen. Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.

   > [!IMPORTANT]
   > Wenn Sie die Virenscansoftware deaktivieren müssen, sollten Sie zuerst den Computer scannen, auf dem der App-V 5,0-Sequenzer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden können.



4. Wählen Sie auf der Seite **Art der Anwendung** **Middleware**aus, und klicken Sie dann auf **weiter**.

5. Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an. Wenn die Anwendung keine zugeordnete Installationsdatei hat und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.

6. Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll. Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll. Der Paket Name wird in der App-V 5,0-Verwaltungskonsole angezeigt.

   Klicken Sie auf **Weiter**.

7. Wenn das Installationsprogramm für Sequencer und Middleware bereit ist, können Sie auf der **Installations** Seite fortfahren, die Anwendung zu installieren, damit der Sequencer den Installationsvorgang überwachen kann. Verwenden Sie den Installationsprozess der Anwendung, um die Installation durchzuführen. Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen**, um die zusätzlichen Installationsdateien zu suchen und auszuführen. Wenn Sie die Installation abgeschlossen haben, aktivieren Sie das Kontrollkästchen **Ich habe die Installation abgeschlossen** , und klicken Sie dann auf **weiter**.

8. Warten Sie auf der **Installations** Seite, während der Sequencer das virtuelle Anwendungspaket konfiguriert.

9. Auf der Seite **Installationsbericht** können Sie Informationen zu dem soeben sequenzierten virtuellen Anwendungspaket überprüfen. Doppelklicken Sie in **zusätzlichen Informationen**auf ein Ereignis, um detailliertere Informationen zu erhalten. Klicken Sie auf **weiter**, um fortzufahren.

10. Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann. Wenn Sie alle unterstützten Betriebssysteme in Ihrer Umgebung zum Ausführen dieses Pakets aktivieren möchten, aktivieren Sie das Kontrollkästchen **Dieses Paket kann auf einem beliebigen Betriebssystem ausgeführt** werden. Wenn Sie dieses Paket so konfigurieren möchten, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, aktivieren Sie das Kontrollkästchen **Dieses Paket darf nur auf dem folgenden Betriebssystem ausgeführt** werden, und wählen Sie die Betriebssysteme aus, mit denen dieses Paket ausgeführt werden kann. Klicken Sie auf **Weiter**.

11. Auf der Seite **Paket erstellen** wird angezeigt. Wenn Sie das Paket ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern mit dem Paket-Editor zu ändern**. Mit dieser Option wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

    Wenn Sie das Paket sofort speichern möchten, wählen Sie **das Paket jetzt speichern**aus. Optional können Sie eine **Beschreibung** hinzufügen, die dem Paket zugeordnet werden soll. Beschreibungen sind hilfreich, um die Programmversion und weitere Informationen über das Paket zu identifizieren.

    > [!IMPORTANT]
    > Das System unterstützt keine nicht druckbaren Zeichen in Kommentaren und Beschreibungen.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. Die Seite **Fertigstellung** wird angezeigt. Überprüfen Sie die Informationen im Bereich **Bericht des virtuellen Anwendungspakets** nach Bedarf, und klicken Sie dann auf **Schließen**. Diese Informationen sind auch in der **Report.xml** -Datei verfügbar, die sich in dem in Schritt 11 dieses Verfahrens angegebenen Verzeichnis befindet.

   Das Paket steht jetzt im Sequencer zur Verfügung. Um die Paketeigenschaften zu bearbeiten, klicken Sie auf **Bearbeiten \ [Package Name \]**.

   > [!IMPORTANT]
   > Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)









