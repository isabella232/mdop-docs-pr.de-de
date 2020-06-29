---
title: So importieren Sie eine Anwendung
description: So importieren Sie eine Anwendung
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807092"
---
# So importieren Sie eine Anwendung


In der Regel importieren Sie Anwendungen, damit Sie von einem Application Virtualization-Verwaltungs Server für den Datenstrom zur Verfügung stehen. Sie können eine Anwendung auch manuell hinzufügen, aber Sie müssen genaue, detaillierte Informationen zur Anwendung angeben. Weitere Informationen finden Sie unter [Manuelles Hinzufügen einer Anwendung](how-to-manually-add-an-application.md).

**Hinweis**  Damit Sie eine Anwendung importieren können, muss Ihre sequenzierte Datei "Open Software Descriptor (OSD)" oder die zugehörige Sequencer Project-Datei (SPRJ) auf dem Server verfügbar sein.

 

Wenn Sie eine Anwendung importieren, sollten Sie sicherstellen, dass der Server mit einem Wert im Feld " **Standardinhalts Pfad** " auf der Registerkarte " **Allgemein** " des Dialogfelds " **System Optionen** " konfiguriert ist (barrierefrei durch Klicken mit der rechten Maustaste auf den Knoten **Application Virtualization System** in der App-V Server-Konsole). Der Wert des Standardinhalts Pfads definiert, wo die Anwendungen importiert werden, und während des Importvorgangs wird dieser Wert verwendet, um die in der OSD-Datei für die SFT-Datei definierten Pfade und die Symbol Verknüpfungen zu ändern. In der OSD-Datei wird der Pfad für die SFT-Datei im Eintrag CODEBASE-HREF angegeben, und der Pfad für die Symbole wird im Eintrag Verknüpfungen angegeben.

Während des Importvorgangs werden das Protokoll, der Server und, falls vorhanden, der in diesen beiden Pfaden in der OSD-Datei angegebene Port durch den Wert aus dem standardmäßigen Inhaltspfad ersetzt. In der folgenden Tabelle finden Sie ein Beispiel dafür, wie der Importpfad betroffen ist.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Standardinhalts Pfad</th>
<th align="left">OSD-Datei CodeBase href</th>
<th align="left">Resultierender Wert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\server\content &lt; /p&gt;</td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p>\server\content\myFolder\package.sft</p></td>
</tr>
</tbody>
</table>

 

**So importieren Sie eine Anwendung**

1.  Klicken Sie im linken Bereich mit der rechten Maustaste auf den Knoten **Anwendungen** , und wählen Sie **Anwendungen importieren**aus.

2.  Navigieren Sie im Dialogfeld **Öffnen** zur SPRJ-oder OSD-Datei der Anwendung. Markieren Sie die Datei, und klicken Sie auf **Öffnen**.

3.  Stellen Sie sicher, dass im **Assistenten für neue Anwendungen**das Kontrollkästchen **aktiviert** für Anwendungen aktiviert ist, die Sie streamen möchten. Dort können Sie auch eine Beschreibung eingeben und die Server-und Dateipfade überprüfen. Wenn Sie Lizenz-und Servergruppen eingerichtet haben, können Sie auch diese auswählen.

4.  Klicken Sie auf **Weiter**.

5.  Aktivieren Sie auf dem Bildschirm **veröffentlichte Verknüpfungen** die Kontrollkästchen für die Speicherorte, an denen die Anwendungsverknüpfungen auf den Clientcomputern angezeigt werden sollen.

6.  Klicken Sie auf **Weiter**.

7.  Auf dem Bildschirm " **Dateizuordnungen** " können Sie dieser Anwendung neue Dateizuordnungen hinzufügen. Klicken Sie dazu auf **Hinzufügen**, geben Sie die Durchwahl (ohne einen vorhergehenden Punkt) ein, geben Sie eine Beschreibung ein, und klicken Sie auf **OK**.

    **Hinweis**  Mit Sequencer 4,0 sequenzierte Anwendungen füllen das Dialogfeld **Dateizuordnungen** auf, wenn Sie Sie über die Verwaltungskonsole importieren oder erstellen. Anwendungen mit vorherigen Sequenzer-Versions Paketen funktionieren nicht.

     

8.  Klicken Sie auf **Weiter**.

9.  Klicken Sie im Bildschirm **Zugriffsberechtigungen** auf **Hinzufügen**.

10. Füllen Sie das Dialogfeld **Gruppen auswählen aus** . Wenn Sie fertig sind, klicken Sie auf **OK**.

11. Klicken Sie auf **Weiter**.

12. Auf dem **Zusammenfassungs** Bildschirm können Sie die Importeinstellungen überprüfen. Klicken Sie auf **Fertig stellen**, oder klicken Sie auf **zurück** , um den Import zu ändern, oder auf **Abbrechen** , um den Importvorgang abzubrechen.

## Verwandte Themen


[So verwalten Sie Anwendungsgruppen in der Server Management Console](how-to-manage-application-groups-in-the-server-management-console.md)

[So verwalten Sie Anwendungen in der Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

[So fügen Sie eine Anwendung manuell hinzu](how-to-manually-add-an-application.md)

 

 





