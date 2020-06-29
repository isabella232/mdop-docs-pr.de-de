---
title: So starten, beenden und starten Sie einen MED-V-Arbeitsbereich neu
description: So starten, beenden und starten Sie einen MED-V-Arbeitsbereich neu
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811326"
---
# So starten, beenden und starten Sie einen MED-V-Arbeitsbereich neu


**So starten Sie einen MED-V-Arbeitsbereich**

1.  Klicken Sie im Infobereich mit der rechten Maustaste auf das MED-V-Symbol.

2.  Klicken Sie im Untermenü auf **Arbeitsbereich starten**.

    -   Wenn mehrere MED-V-Arbeitsbereiche auf dem Computer ausgeführt werden, wird das Fenster **Arbeitsbereichs Auswahl** angezeigt.

        1.  Wählen Sie einen MED-V-Arbeitsbereich aus.

        2.  Aktivieren Sie das Kontrollkästchen **ausgewählten Arbeitsbereich ohne Aufforderung starten** , um dieses Fenster beim nächsten Start des Clients zu überspringen und den ausgewählten MED-V-Arbeitsbereich automatisch zu öffnen.

        3.  Klicken Sie auf **OK**.

    Das Fenster **Arbeitsbereichs Authentifizierung starten** wird angezeigt.

    -   Wenn auf dem Computer mehrere med-v-Arbeitsbereiche vorhanden sind und Sie sich für die Verwendung eines angegebenen Med-v-Arbeitsbereichs entschieden haben, wird das in der folgenden Abbildung dargestellte Fenster angezeigt.

        ![](images/medv-logon.gif)

    -   Wenn auf dem Computer nur ein MED-V-Arbeitsbereich vorhanden ist, steht die Option "zuletzt verwendeter Arbeitsbereich starten" nicht zur Verfügung.

3.  Geben Sie die Anmeldeinformationen Ihres Domänenbenutzers ein.

    **Hinweis**  Wenn ein MED-V-Arbeitsbereich zum ersten Mal gestartet wird, sollte sich der Benutzername im folgenden Format befinden: &lt; Domänenname- &gt; \\ &lt; Benutzername &gt; .

     

4.  Wählen Sie **mein Kennwort speichern** aus, um Ihr Kennwort zwischen den Sitzungen zu speichern.

    **Hinweis**  Um das Feature Kennwort speichern zu aktivieren, muss das EnableSavePassword-Attribut in der ClientSettings.xml Datei auf true festgelegt sein. Die Datei befindet sich im Ordner *Servers\\Configuration Server\\* .

     

5.  Deaktivieren Sie das Kontrollkästchen **zuletzt verwendeten Arbeitsbereich starten** , um einen anderen MED-V-Arbeitsbereich auszuwählen.

6.  Klicken Sie auf **OK**.

    Je nach Konfiguration des MED-V-Arbeitsbereichs werden mehrere Status Bildschirme angezeigt.

    Der Bildschirm **Startbereich** wird angezeigt.

**So starten Sie einen MED-V-Arbeitsbereich neu**

1.  Wenn der Client ausgeführt wird, klicken Sie im Infobereich mit der rechten Maustaste auf das MED-V-Symbol.

2.  Klicken Sie im Untermenü auf **Arbeitsbereich neu starten**.

    Der Arbeitsbereich MED-V wird neu gestartet.

    -   In einem beständigen MED-V-Arbeitsbereich wird der virtuelle Computer heruntergefahren und neu gestartet.

    -   In einem revertible MED-V-Arbeitsbereich wird der virtuelle Computer nicht tatsächlich heruntergefahren; Stattdessen wird der ursprüngliche Zustand zurückgegeben.

**So beenden Sie einen MED-V-Arbeitsbereich**

1.  Klicken Sie im Infobereich mit der rechten Maustaste auf das MED-V-Symbol.

2.  Klicken Sie im Untermenü auf **Arbeitsbereich beenden**.

    Der MED-V-Arbeitsbereich wurde angehalten.

## Verwandte Themen


[So starten und beenden Sie den MED-V-Client](how-to-start-and-exit-the-med-v-client.md)

 

 





