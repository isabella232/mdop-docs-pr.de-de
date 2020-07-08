---
title: So fügen Sie ein Paketversion hinzu
description: So fügen Sie ein Paketversion hinzu
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808734"
---
# So fügen Sie ein Paketversion hinzu


Wenn Sie in der Application Virtualization Server Management Console eine Neusequenzierung eines Pakets durchführen, können Sie mit dem folgenden Verfahren die neue Version Ihren Servern für Streaming hinzufügen.

**Hinweis**  Wenn Sie ein Paket mit einer neuen Version aktualisieren, können Sie die vorhandene Version beibehalten oder löschen und nur die neueste Version belassen. Möglicherweise möchten Sie die alte Version für die Kompatibilität mit älteren Dokumenten beibehalten, oder Sie können die neue Version testen, bevor Sie für alle Benutzer verfügbar gemacht wird.

 

**So fügen Sie eine Paketversion hinzu**

1.  Kopieren Sie die neue SFT-Datei in den Inhaltsordner des Anwendungsservers. Wenn die Neusequenzierung keine Änderungen an den Dateien "Open Software Descriptor (OSD)", "Symbol (ICO)" oder "Sequencer Project (SPRJ)" hinzufügt, müssen Sie diese nicht kopieren. Sie können diese Dateien einbeziehen, wenn Sie möchten, dass alle Dateien das gleiche Datum aufweisen.

2.  Erweitern Sie im linken Bereich der Application Virtualization Server-Verwaltungskonsole den Knoten **Pakete** .

3.  Klicken Sie mit der rechten Maustaste auf das Paket, das Sie aktualisieren möchten, und wählen Sie **Version hinzufügen**aus.

4.  Suchen Sie im Dialogfeld **Paket Version hinzufügen** nach, oder geben Sie den Pfadnamen für die neue Anwendungsdatei im Feld **Vollständiger Pfad für Paketdatei** ein. Hierbei muss es sich um eine SFT-Datei handeln.

5.  Klicken Sie auf **Weiter**.

6.  Im Dialogfeld " **Zusammenfassung** " wird der Speicherort der Datei angezeigt, und Sie werden aufgefordert, die Datei dort zu kopieren, wenn dies noch nicht geschehen ist. Klicken Sie auf **Fertig stellen** , nachdem Sie die Informationen überprüft haben.

    Die neue Version ist nun fertig und kann gestreamt werden.

## Verwandte Themen


[So löschen Sie ein Paket](how-to-delete-a-packageserver.md)

[So verwalten Sie die Pakete in der Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





