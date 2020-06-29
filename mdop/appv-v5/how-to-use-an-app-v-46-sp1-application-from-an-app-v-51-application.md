---
title: Verwenden einer APP-v 4,6-Anwendung aus einer APP-v 5,1-Anwendung
description: Verwenden einer APP-v 4,6-Anwendung aus einer APP-v 5,1-Anwendung
author: dansimp
ms.assetid: 909b4391-762b-4988-b0cf-32b67f1fcf0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: c0d308dcae33b02c089c101ffcd5041b2e665f59
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805126"
---
# Verwenden einer APP-v 4,6-Anwendung aus einer APP-v 5,1-Anwendung

*Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen. Das folgende gilt für ein App-V 4,6 SP3-Paket.

Gehen Sie wie folgt vor, um eine APP-v 4.6-Anwendung mit App-v 5,1-Anwendungen auf einem eigenständigen Client auszuführen.

**Hinweis**  Bei diesem Verfahren wird davon ausgegangen, dass Sie die neueste Version von App-V 4,6 ausführen.

**So führen Sie Anwendungen auf einem eigenständigen Client aus**

1.  Wählen Sie in Ihrer Umgebung zwei Anwendungen aus, die von einander geöffnet werden können. Beispiel: Microsoft Outlook und Adobe Acrobat Reader. Sie können auf eine mit Adobe Acrobat erstellte e-Mail-Anlage zugreifen.

2.  Konvertieren Sie die Pakete, oder erstellen Sie ein neues Paket für eine der Anwendungen mit dem App-V 5,1-Format. Weitere Informationen zum Konvertieren von Paketen finden Sie unter [Migrieren von Erweiterungspunkten aus einem App-v 4,6-Paket zu einem konvertierten App-v 5,1-Paket für alle Benutzer auf einem bestimmten Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md) oder zum [Migrieren von Erweiterungspunkten aus einem App-v 4,6-Paket zu app-v 5,1 für einen bestimmten Benutzer](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).

3.  Hinzufügen und Bereitstellen des Pakets mithilfe der App-V 5,1-Verwaltungskonsole. Weitere Informationen zum Hinzufügen und Bereitstellen von Paketen finden Sie unter [Hinzufügen oder Aktualisieren von Paketen mithilfe der Verwaltungskonsole](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) und [Konfigurieren des Zugriffs auf Pakete mithilfe der Verwaltungskonsole](how-to-configure-access-to-packages-by-using-the-management-console-51.md).

4.  Die konvertierte Anwendung wird jetzt mit App-V 5,1 ausgeführt, und Sie können eine Anwendung von der anderen öffnen. Wenn Sie beispielsweise ein Microsoft Office-Paket in ein App-v 5,1-Paket konvertiert haben und Adobe Acrobat weiterhin als App-v 4.6-Paket ausgeführt wird, können Sie eine Adobe Acrobat Reader-Anlage mit Microsoft Outlook öffnen.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





