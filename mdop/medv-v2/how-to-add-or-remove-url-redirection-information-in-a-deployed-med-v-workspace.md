---
title: So fügen Sie URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich hinzu bzw. entfernen Sie sie
description: So fügen Sie URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich hinzu bzw. entfernen Sie sie
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811758"
---
# So fügen Sie URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich hinzu bzw. entfernen Sie sie


Zum Bearbeiten von URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich empfehlen wir, die Systemregistrierung mithilfe von Gruppenrichtlinien zu aktualisieren. Obwohl wir dies nicht empfehlen, können Sie den MED-V-Arbeitsbereich auch mit den aktualisierten URL-Umleitungsinformationen neu erstellen und erneut bereitstellen.

Der Registrierungsschlüssel befindet sich normalerweise unter:

Computer\\HKEY\ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\userexperience

Der folgende mehrteilige Zeichenfolgenwert muss vorhanden sein: `RedirectUrls`

Die Wertdaten für `RedirectUrls` ist eine Liste aller URLs, die Sie bei der Erstellung des Med-v-Arbeitsbereichs Pakets mithilfe des **Med-v-Arbeitsbereichs Pakets**für die Umleitung angegeben haben. Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).

Sie können URL-Umleitungsinformationen hinzufügen und entfernen, indem Sie eine der folgenden Aufgaben ausführen:

-   [Bearbeiten des Registrierungsschlüssels für die URL-Umleitung und Bereitstellen mithilfe von Gruppenrichtlinien](#bkmk-editreg)

-   [Bearbeiten der Textdatei für die URL-Umleitung und erneutes Erstellen des MED-V-Arbeitsbereichs](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**So aktualisieren Sie URL-Umleitungsinformationen mithilfe von Gruppenrichtlinien**

1.  Bearbeiten Sie den Namen des Registrierungsschlüssel-mehrteiligen Zeichenfolgenwerts `RedirectUrls` . Dieser Wert befindet sich normalerweise unter:

    Computer\\HKEY\ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\userexperience

    Wenn Sie dem Registrierungsschlüssel URLs hinzufügen, geben Sie diese pro Zeile ein, wie es beim Aufbau des MED-V-Arbeitsbereichs Pakets erforderlich war. Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).

2.  Bereitstellen des aktualisierten Registrierungsschlüssels mithilfe von Gruppenrichtlinien Weitere Informationen zum Verwenden von Gruppenrichtlinien finden Sie unter [Gruppenrichtlinien-Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

**Hinweis**  Diese Methode zum Bearbeiten von URL-Umleitungsinformationen ist ein bewährtes MED-V-Verfahren.

 

<a href="" id="bkmk-edittext"></a>**So erstellen Sie den MED-V-Arbeitsbereich mithilfe einer aktualisierten URL-Textdatei neu**

-   Eine weitere Methode zum Hinzufügen und Entfernen von URLs aus der Umleitungsliste besteht darin, die URL-Umleitungs Text Datei zu aktualisieren und dann zum Erstellen eines neuen MED-V-Arbeitsbereichs zu verwenden. Anschließend können Sie den MED-V-Arbeitsbereich wie zuvor mithilfe Ihres Standard Bereitstellungsprozesses wie einem ESD-System erneut bereitstellen.

    **Wichtig**  Diese Methode zur Bearbeitung von URL-Umleitungsinformationen wird nicht empfohlen. Darüber hinaus muss die erstmalige Einrichtung erneut ausgeführt werden, und alle auf dem virtuellen Computer gespeicherten Daten gehen verloren, wenn Sie den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen.

     

## Verwandte Themen


[So testen Sie die URL-Umleitung](how-to-test-url-redirection.md)

[Verwalten von Anwendungen, die in MED-V-Arbeitsbereichen bereitgestellt werden](managing-applications-deployed-to-med-v-workspaces.md)

[Erstellen eines MED-V-Arbeitsbereichspakets](create-a-med-v-workspace-package.md)

 

 





