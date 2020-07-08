---
title: Starten und Beenden des AGPM-Diensts
description: Starten und Beenden des AGPM-Diensts
author: dansimp
ms.assetid: 769aa0ce-224a-446f-9958-9518af4ad159
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 33e797182d49157da0fe8f36dce17b4b35cdd623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807460"
---
# Starten und Beenden des AGPM-Diensts


Der AGPM-Dienst ist ein Windows-Dienst, der als Sicherheitsproxy fungiert und den Clientzugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivierungs-und Produktionsumgebung verwaltet.

**Wichtig**  Durch das Beenden oder Deaktivieren des AGPM-Diensts können AGPM-Clients keine Vorgänge (wie das Auflisten oder Bearbeiten von GPOs) über den Server ausführen.

 

Ein Benutzerkonto mit Zugriff auf den AGPM-Server (der Computer, auf dem der AGPM-Dienst installiert ist) ist erforderlich, um dieses Verfahren ausführen zu können.

**So starten oder beenden Sie den AGPM-Dienst**

1.  Klicken Sie auf dem Computer, auf dem Microsoft Advanced Group Policy Management-Server (und daher der AGPM-Dienst) installiert ist, auf **Start**, klicken Sie auf **System**Steuerung, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Dienste**.

2.  Klicken Sie in der Liste der Dienste mit der rechten Maustaste auf **AGPM-Dienst** , und wählen Sie **starten**, **neu starten**oder **Beenden**aus.

    **Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem. Dadurch kann der Start des AGPM-Diensts verhindert werden. Informationen zum Ändern der Einstellungen für den Dienst finden Sie unter [Verwalten des AGPM-Diensts](managing-the-agpm-service.md).

     

### Weitere Verweise

-   [Verwalten des AGPM-Dienstes](managing-the-agpm-service.md)

 

 





