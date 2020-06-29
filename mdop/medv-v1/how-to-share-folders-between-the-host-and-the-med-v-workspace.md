---
title: So teilen Sie Ordner zwischen dem Host und dem MED-V-Arbeitsbereich
description: So teilen Sie Ordner zwischen dem Host und dem MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811344"
---
# So teilen Sie Ordner zwischen dem Host und dem MED-V-Arbeitsbereich


Sie können Ordner zwischen dem Host und dem MED-V-Arbeitsbereich freigeben. Die freigegebenen Ordner können wie folgt gespeichert werden:

-   Ein externer Computer im Netzwerk

-   Der Hostcomputer

Die folgenden Verfahren veranschaulichen, wie Sie Ordner zwischen dem Host und dem MED-V-Arbeitsbereich freigeben.

**So geben Sie im Netzwerk befindliche Ordner frei**

1.  Konfigurieren Sie MED-V im vollständigen Desktopmodus.

2.  Klicken Sie in MED-V-Verwaltung auf der Registerkarte Netzwerk auf **andere IP-Adresse als Host verwenden (Bridge)**.

3.  Gehen Sie auf dem Hostcomputer wie folgt vor:

    1.  Klicken Sie in der Systemsteuerung auf **Netzwerkstatus und Aufgaben anzeigen**, und wählen Sie **Netzwerkermittlung** auf **ein aus**.

    2.  Klicken Sie im Startmenü mit der rechten Maustaste auf **Computer**, und klicken Sie auf **Netzlaufwerk zuordnen**.

    3.  Wählen Sie im Dialogfeld **Netzlaufwerk zuordnen** im Feld **Laufwerk** ein Laufwerk aus.

        **Hinweis**  Stellen Sie sicher, dass derselbe Laufwerkbuchstabe nicht auf beiden Computern verwendet wird.

         

    4.  Klicken Sie auf **Browse**.

    5.  Navigieren Sie im Dialogfeld **Ordner suchen** zum freigegebenen Laufwerk, und klicken Sie auf **OK**.

    6.  Klicken Sie auf **Fertig stellen**.

4.  Wiederholen Sie Schritt 3 im MED-V-Arbeitsbereich. Zeigen Sie auf das gleiche Laufwerk wie auf dem Hostcomputer.

**So geben Sie auf dem Host befindliche Ordner frei**

1.  Konfigurieren Sie den Ordner, der mit den entsprechenden Berechtigungen freigegeben werden soll.

2.  Wechseln Sie im MED-V-Arbeitsbereich zu **meine Netzwerkumgebung** , und suchen Sie den freigegebenen Ordner.

3.  Suchen Sie im MED-V-Arbeitsbereich den freigegebenen Ordner.

**Hinweis**  Stellen Sie sicher, dass sich der Host-und der MED-V-Arbeitsbereichs Computer in derselben Domäne oder Arbeitsgruppe befinden.

 

 

 





