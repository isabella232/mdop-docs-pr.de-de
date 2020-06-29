---
title: So aktualisieren Sie ein Paket
description: So aktualisieren Sie ein Paket
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806732"
---
# So aktualisieren Sie ein Paket


Der Vorgang für ein automatisches Upgrade ist derselbe wie beim Hinzufügen einer Paketversion in der Application Virtualization Server-Verwaltungskonsole. Eine automatische Aktualisierung wird durchgeführt, wenn Sie die Anwendung in einem vorhandenen Paket umsequenzieren. Dann können Sie diese neue Version Ihren Servern für Streaming hinzufügen.

Wenn Sie ein Paket mit einer neuen Version aktualisieren, können Sie die vorhandene Version beibehalten oder löschen und nur die neueste Version belassen. Möglicherweise möchten Sie die alte Version für die Kompatibilität mit älteren Dokumenten beibehalten, oder Sie können die neue Version testen, bevor Sie für alle Benutzer verfügbar gemacht wird.

**So aktualisieren Sie ein Paket automatisch**

1.  Kopieren Sie die neue SFT-Datei in den Content-Ordner von Application Virtualization Server.

    **Hinweis**  Wenn die Neusequenzierung keine Features hinzugefügt hat, die die Dateien "Open Software Descriptor (OSD)", "Symbol (ICO)" oder "Sequencer Project (SPRJ)" geändert haben, müssen Sie diese nicht kopieren. Sie können diese Dateien einbeziehen, wenn Sie möchten, dass alle diese Dateien das gleiche Datum aufweisen.

     

2.  Erweitern Sie im linken Bereich der Application Virtualization Server-Verwaltungskonsole **Pakete**.

3.  Klicken Sie mit der rechten Maustaste auf das Paket, das Sie aktualisieren möchten, und wählen Sie **Version hinzufügen**aus.

4.  Suchen Sie im Dialogfeld **Paket Version hinzufügen** nach, oder geben Sie den vollständigen Pfadnamen für die neue Anwendungsversion in den **vollständigen Pfad für das Feld Datei** ein. Hierbei muss es sich um eine SFT-Datei handeln.

5.  Klicken Sie auf **Weiter**.

6.  Im Dialogfeld " **Zusammenfassung** " wird der Speicherort der Datei angezeigt, und Sie werden aufgefordert, die Datei dort zu kopieren, wenn dies noch nicht geschehen ist. Klicken Sie auf **Fertig stellen** , nachdem Sie die Informationen überprüft haben.

    Die neue Version ist nun fertig und kann gestreamt werden.

## Verwandte Themen


[So verwalten Sie die Pakete in der Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





