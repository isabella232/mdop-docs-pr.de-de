---
title: So testen Sie die URL-Umleitung
description: So testen Sie die URL-Umleitung
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810561"
---
# So testen Sie die URL-Umleitung


Nachdem Ihr Test der erstmaligen Einrichtung abgeschlossen wurde, können Sie überprüfen, ob die URL-Umleitungsfunktion wie erwartet funktioniert, indem Sie die folgenden Aufgaben ausführen.

**Wichtig**  Der MED-V-Host-Agent muss ausgeführt werden, damit die URL-Umleitung ordnungsgemäß funktioniert.

<a href="" id="bkmk-urlredir"></a>**So testen Sie die URL-Umleitung**

1.  Öffnen Sie einen Internet Explorer-Browser auf dem Hostcomputer, und geben Sie eine URL ein, die Sie für die Umleitung angegeben haben.

2.  Überprüfen Sie, ob die Webseite auf dem virtuellen Gastcomputer in Internet Explorer geöffnet wird.

3.  Wiederholen Sie diesen Vorgang für jede URL, die Sie testen möchten.

**So testen Sie, ob eine URL hinzugefügt oder entfernt werden kann**

1.  Hinzufügen oder Entfernen einer URL aus dem MED-V-Arbeitsbereich

    Informationen zum Hinzufügen und Entfernen von URLs für die Umleitung in einem Med-v-Arbeitsbereich finden Sie unter [Verwalten der Med-v-URL-Umleitung](manage-med-v-url-redirection.md).

2.  Wenn Sie der Umleitungsliste eine URL hinzugefügt haben, wiederholen Sie die Schritte in [, um die URL-Umleitung zu testen](#bkmk-urlredir) , um zu überprüfen, ob die neue URL wie beabsichtigt umgeleitet wird.

3.  Wenn Sie eine URL aus der Umleitungsliste entfernt haben, überprüfen Sie, ob Sie entfernt wurde, indem Sie die folgenden Schritte ausführen:

    1.  Öffnen Sie einen Internet Explorer-Browser auf dem Hostcomputer, und geben Sie die URL ein, die Sie aus der Umleitungsliste entfernt haben.

    2.  Überprüfen Sie, ob die Webseite in Internet Explorer auf dem Hostcomputer und nicht auf dem virtuellen Gastcomputer geöffnet ist.

        **Hinweis**  Es kann einige Sekunden dauern, bis die URL-Umleitungs Änderungen stattfinden.

**Hinweis**  Wenn bei der Überprüfung Ihrer URL-Umleitungseinstellungen Probleme auftreten, lesen Sie [Problembehandlung bei Vorgängen](operations-troubleshooting-medv2.md).

Nachdem Sie das Testen der URL-Umleitung in Ihrem MED-V-Arbeitsbereich abgeschlossen haben, können Sie andere Konfigurationen testen, um zu überprüfen, ob Sie wie beabsichtigt funktionieren.

Nachdem Sie das Testen des Med-v-Arbeitsbereichs Pakets abgeschlossen haben und überprüft haben, dass es wie beabsichtigt funktioniert, können Sie den Med-v-Arbeitsbereich für Ihr Unternehmen bereitstellen.

## Verwandte Themen

[So testen Sie die Anwendungsveröffentlichung](how-to-test-application-publishing.md)

[So überprüfen Sie erstmalige Einstellungen für das Setup](how-to-verify-first-time-setup-settings.md)

[Bereitstellen des MED-V-Arbeitsbereichspakets](deploying-the-med-v-workspace-package.md)

 

 





