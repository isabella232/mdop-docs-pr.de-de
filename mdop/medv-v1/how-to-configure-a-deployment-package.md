---
title: So konfigurieren Sie ein Bereitstellungspaket
description: So konfigurieren Sie ein Bereitstellungspaket
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811461"
---
# So konfigurieren Sie ein Bereitstellungspaket


Der Verpackungs-Assistent führt Sie durch die Erstellung eines Pakets, indem Sie einen Ordner auf dem lokalen Computer erstellen und alle erforderlichen Installationsdateien in den einzelnen Ordner übertragen. Der Inhalt des Ordners kann dann zur Verteilung auf mehrere Wechselmedienlaufwerke verschoben werden.

**Hinweis:**  
Ein einzelnes Paket kann keine Installationsdateien für x86-und x64-Systeme enthalten.



## Erstellen eines Bereitstellungspakets


**So erstellen Sie ein Bereitstellungspaket**

1. Überprüfen Sie im Modul **Bilder** , dass Sie mindestens ein lokal verpacktes Bild erstellt haben.

2. Klicken Sie im Menü **Extras** auf **Verpackungs-Assistent**.

3. Klicken Sie auf der Willkommensseite des **Verpackungs-Assistenten** auf **weiter**.

4. Aktivieren Sie auf der Seite **Workspace Image** das Kontrollkästchen **Bild in das Paket einbeziehen** , um ein Bild in das Paket einzubeziehen.

   Das Feld " **Bild** " ist aktiviert.

   **Hinweis:**  
   In einem MED-V-Paket ist kein Bild erforderlich; das Paket kann ohne ein Bild erstellt werden. In einem solchen Fall sollte das Bild auf den Server hochgeladen werden, damit es später über das Netzwerk auf den Client heruntergeladen oder in einen Ordner mit Vorstufen für Bilder verschoben werden kann.



5. Klicken Sie **auf die** Bildliste, um alle verfügbaren Bilder anzuzeigen. Wählen Sie das Bild aus, das in das Paket kopiert werden soll. Klicken Sie auf **Aktualisieren** , um die Liste der verfügbaren Bilder zu aktualisieren.

6. Klicken Sie auf **Weiter**.

7. Wählen Sie auf der Seite **Med-v-Installationseinstellungen** die Med-v-Installationsdatei aus, indem Sie eine der folgenden Aktionen ausführen:

   -   Geben Sie im Feld **MED-V-Installationsdatei** den vollständigen Pfad zu dem Verzeichnis ein, in dem sich die Installationsdatei befindet.

   -   Klicken Sie auf **...** , um zu dem Verzeichnis zu navigieren, in dem sich die Installationsdatei befindet.

   **Hinweis:**  
   Dieses Feld ist obligatorisch, und der Assistent wird nicht ohne gültigen Dateinamen fortgesetzt.



8. Geben Sie im Feld **Serveradresse** den Servernamen oder die IP-Adresse ein.

9. Geben Sie im Feld **Server Port** den Serverport ein.

10. Aktivieren Sie das Kontrollkästchen **Server wird über HTTPS zugegriffen** , um eine HTTPS-Verbindung zum Herstellen einer Verbindung mit dem Server zu fordern.

11. Führen Sie eine der folgenden Aktionen aus:

    -   Klicken Sie auf **Standardinstallationseinstellungen**, und klicken Sie dann auf **weiter** , um fortzufahren, und behalten Sie die Standardeinstellungen bei.

    -   Klicken Sie auf **benutzerdefinierte Installationseinstellungen**, und klicken Sie dann auf **weiter** , um die Installationseinstellungen anzupassen.

        1.  Geben Sie auf der Seite **benutzerdefinierte Einstellungen für die Med-v-Installation** im Feld **Installationsordner** den Pfad des Ordners ein, in dem die Med-v-Dateien auf dem Hostcomputer installiert werden.

            **Hinweis:**  
            Es wird empfohlen, Variablen im Pfad anstelle von Konstanten zu verwenden, die von Computer zu Computer unterschiedlich sein können.

            Verwenden Sie beispielsweise *%ProgramFiles%\\MED-V* anstelle von *c:\\MED-V*.



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. Aktivieren Sie auf der Seite **Zusätzliche Installationen** das Kontrollkästchen **Installation der Virtualisierungssoftware einbeziehen** , um die Installation von Virtual PC in das Paket einzubeziehen.

    Das Feld " **Installationsdatei** " ist aktiviert. Geben Sie den vollständigen Pfad der Installationsdatei für die Virtualisierungssoftware ein, oder klicken Sie auf **...** , um das Verzeichnis zu durchsuchen.

13. Aktivieren Sie das Kontrollkästchen **Installation von Virtual PC QFE einbeziehen** , um die Installation des Virtual PC-Updates in das Paket einzubeziehen.

    Das Feld " **Installationsdatei** " ist aktiviert. Geben Sie den vollständigen Pfad der Installationsdatei für das Virtual PC-Update ein, oder klicken Sie auf **...** , um zum Verzeichnis zu wechseln.

14. Aktivieren Sie das Kontrollkästchen **Installation von Microsoft .NET Framework 2,0** , um die Installation von Microsoft .NET Framework 2,0 in das Paket einzubeziehen.

    Das Feld " **Installationsdatei** " ist aktiviert. Geben Sie den vollständigen Pfad der Installationsdatei für Microsoft .NET Framework 2,0 ein, oder klicken Sie auf **...** , um zum Verzeichnis zu navigieren.

15. Klicken Sie auf **Weiter**.

16. Wählen Sie auf der Seite **Finalize** den Speicherort aus, an dem das Paket gespeichert werden soll, indem Sie eine der folgenden Aktionen ausführen:

    -   Geben Sie im Feld **Paket Ziel** den vollständigen Pfad zu dem Verzeichnis ein, in dem das Paket gespeichert werden soll.

    -   Klicken Sie auf **...** , um zu dem Verzeichnis zu navigieren, in dem die Installationsdateien gespeichert werden sollen.

    **Hinweis:**  
    Das Erstellen des Pakets kann mehr Speicherplatz als die tatsächliche Paketgröße beanspruchen. Es wird daher empfohlen, das Paket auf der Festplatte zu erstellen. Nachdem das Paket erstellt wurde, kann es auf den USB-Anschluss kopiert werden.



17. Geben Sie im Feld **Paketname** einen Namen für das Paket ein.

18. Klicken Sie auf **Fertig stellen** , um das Paket zu erstellen.

    Das Paket wird erstellt. Dies kann einige Minuten dauern.

    Nachdem das Paket erstellt wurde, wird eine Meldung angezeigt, in der Sie darüber informiert werden, dass es erfolgreich abgeschlossen wurde.

**Hinweis:**  
Wenn Sie alle Dateien lokal und nicht direkt auf dem Wechselmedium gespeichert haben, stellen Sie sicher, dass Sie nur den Inhalt des Ordners und nicht den Ordner selbst auf die Wechselmedien kopieren.



**Hinweis:**  
Die Wechselmedien müssen groß genug sein, damit der Inhalt des Pakets maximal drei Viertel des Speichers der Wechselmedien beansprucht.



**Hinweis:**  
Beim Erstellen des Pakets ist möglicherweise eine bis zu doppelte Größe der tatsächlichen Paketgröße erforderlich, wenn der Build abgeschlossen ist.



## Verwandte Themen


[Erstellen eines MED-V-Images](creating-a-med-v-image.md)









