---
title: Ändern Sie den Port, den der AGPM-Dienst überwacht
description: Ändern Sie den Port, den der AGPM-Dienst überwacht
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808327"
---
# Ändern Sie den Port, den der AGPM-Dienst überwacht


Der AGPM-Dienst ist ein Windows-Dienst, der als Sicherheitsproxy fungiert und den Clientzugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivierungs-und Produktionsumgebung verwaltet. Standardmäßig überwacht der AGPM-Dienst Port 4600. Sie können diesen Port ändern, indem Sie die erweiterte Archivindexdatei für die Gruppenrichtlinienverwaltung (AGPM) für jedes Archiv ändern.

**Hinweis**  Bevor Sie den Port ändern, auf dem der AGPM-Dienst lauscht, wird empfohlen, die AGPM Archive-Indexdatei (gpostate.xml) zu sichern. Diese Datei befindet sich in dem Ordner, der während der Installation des erweiterten Gruppenrichtlinien-Verwaltungsservers als Archivierungspfad eingegeben wurde. Standardmäßig ist dieser Speicherort dieser Datei% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml auf dem AGPM-Server. Wenn Sie nicht wissen, auf welchem Computer das Archiv gehostet wird, können Sie das Verfahren zum Ändern des Archiv Pfads zum Anzeigen des aktuellen Archiv Pfads ausführen. Weitere Informationen finden Sie unter [Ändern des Archiv Pfads](modify-the-archive-path.md).

 

Ein Benutzerkonto mit Zugriff auf den AGPM-Server (der Computer, auf dem der AGPM-Dienst installiert ist) und die Archivindexdatei sind erforderlich, um dieses Verfahren ausführen zu können.

**So ändern Sie den Port, den der AGPM-Dienst überwacht**

1.  Öffnen Sie auf dem Computer, der das Archiv hostet, die Archivindexdatei (gpostate.xml) in einem Text-Editor.

2.  Suchen Sie in der Datei nach **AGPM: Port = "4600"**.

3.  Ersetzen Sie **4600** durch den Port, den der AGPM-Dienst abhören soll; Speichern und schließen Sie dann die Datei.

4.  Starten Sie auf dem AGPM-Server den AGPM-Dienst neu. (Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service.md).)

5.  Ändern Sie den Port in der AGPM-Server Verbindung für jeden Gruppenrichtlinienadministrator. (Weitere Informationen finden Sie unter [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection.md).)

6.  Wiederholen Sie diesen Vorgang für jeden Archivierungs-und AGPM-Server.

### Weitere Verweise

-   [Verwalten des AGPM-Dienstes](managing-the-agpm-service.md)

 

 





