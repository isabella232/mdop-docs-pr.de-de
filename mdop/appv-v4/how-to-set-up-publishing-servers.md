---
title: So richten Sie Veröffentlichungsserver ein
description: So richten Sie Veröffentlichungsserver ein
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806743"
---
# So richten Sie Veröffentlichungsserver ein


Mit den folgenden Verfahren können Sie Application Virtualization Server direkt über die Client Verwaltungskonsole hinzufügen und konfigurieren.

**So fügen Sie einen Anwendungsveröffentlichungsserver hinzu**

1.  Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste, und wählen Sie im Popupmenü den Eintrag neuer **Server** aus, um den Assistenten für neue Application Virtualization Server zu starten, oder klicken Sie alternativ mit der rechten Maustaste auf den Knoten **Publishing Server** , und wählen Sie dann im Popupmenü den Eintrag **neuer Server** aus.

2.  Geben Sie auf Seite 1 des Assistenten den Namen des Servers in das Feld **Anzeigename** ein, und wählen Sie in der Dropdownliste **Type** den Servertyp aus. In der Dropdownliste der Servertypen können Sie **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **Standard HTTP Server**oder **Enhanced Security http Server** auswählen.

3.  Klicken Sie auf **Weiter**.

4.  Geben Sie auf Seite 2 des Assistenten die entsprechenden Informationen in die Felder **Hostname** und **Port** ein. Das Feld " **Pfad** " kann für Application Virtualization-Server nicht bearbeitet werden. Sie müssen einen Pfad für den Standard-HTTP-Server oder den erweiterten Security http-Server eingeben.

5.  Klicken Sie auf **Fertig stellen** , um den Server hinzuzufügen.

**So richten Sie einen Anwendungsveröffentlichungsserver ein**

1.  Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste auf den gewünschten Server, und wählen Sie im Popupmenü **Eigenschaften** aus.

2.  Klicken Sie auf die Registerkarte **Allgemein** , auf der Sie den Servernamen ändern, einen Typ aus der Dropdownliste der Servertypen auswählen und den Hostnamen und den Port angeben können. Wenn der Servertyp Standard-HTTP-Server oder Enhanced Security http Server ist, kann das Feld **path** ebenfalls bearbeitet werden.

3.  Klicken Sie auf die Registerkarte **Aktualisieren** , auf der das Kontrollkästchen **Veröffentlichung bei Benutzeranmeldung aktualisieren** standardmäßig aktiviert ist. Wenn Sie die Aktualisierungsrate ändern möchten, aktivieren Sie das Kontrollkästchen **Veröffentlichungs alle aktualisieren** , und geben Sie eine Zahl ein, die die Häufigkeit im Feld darstellt. Wählen Sie dann im Dropdownmenü die Option **Minuten**, **Stunden**und **Tage** aus. (Die Mindestzeitdauer, die Sie eingeben können, beträgt 30 Minuten.)

4.  Klicken Sie auf über **nehmen** , um die Konfiguration zu ändern.

5.  Wenn Sie die Veröffentlichung beendet haben, klicken Sie auf **OK** , um das Dialogfeld zu schließen und zur Client Verwaltungskonsole zurückzukehren.

## Verwandte Themen


[So deaktivieren oder ändern Sie Einstellungen für den unterbrochenen Betriebsmodus](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





