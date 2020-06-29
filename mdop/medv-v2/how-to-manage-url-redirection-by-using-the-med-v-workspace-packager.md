---
title: So verwalten Sie URL-Umleitungen mit dem Arbeitsbereichs-Packager für MED-V
description: So verwalten Sie URL-Umleitungen mit dem Arbeitsbereichs-Packager für MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810783"
---
# So verwalten Sie URL-Umleitungen mit dem Arbeitsbereichs-Packager für MED-V


Sie können den Med-v-Arbeitsbereichs Paketdienst verwenden, um die URL-Umleitung im Med-v-Arbeitsbereich zu verwalten.

**So verwalten Sie die Umleitung von Webadressen in einem MED-V-Arbeitsbereich**

1.  Klicken Sie zum Öffnen des **Med-v Workspace-Pakets**auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **Med-v Workspace Packager**.

2.  Klicken Sie im Hauptbereich des **MED-V Workspace-Pakets** auf **Web-Umleitung verwalten**.

3.  Im Fenster **Web-Umleitung verwalten** können Sie eine Liste der URLs eingeben, einfügen oder importieren, die im MED-V-Arbeitsbereich an Internet Explorer umgeleitet werden.

    **Hinweis:**  
    Die URL-Umleitung in MED-V unterstützt nur die Protokolle http und HTTPS. MED-V bietet keine Unterstützung für FTP oder andere Protokolle.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. Klicken Sie auf **Speichern unter...** , um die aktualisierten URL-Umleitungs Dateien im angegebenen Ordner zu speichern. MED-V erstellt eine Registrierungsdatei, die die aktualisierten URL-Umleitungsinformationen enthält. Bereitstellen des aktualisierten Registrierungsschlüssels mithilfe von Gruppenrichtlinien Weitere Informationen zum Verwenden von Gruppenrichtlinien finden Sie unter [Gruppenrichtlinien-Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   Med-v erstellt auch ein Windows PowerShell-Skript im angegebenen Ordner, das Sie zum erneuten Erstellen des aktualisierten MED-V-Arbeitsbereichs Pakets verwenden können.

## Verwandte Themen


[So fügen Sie URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich hinzu bzw. entfernen Sie sie](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[Verwalten von MED-V-URL-Umleitungen](manage-med-v-url-redirection.md)









