---
title: Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an
description: Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an
author: dansimp
ms.assetid: 78fe0f15-4a36-41e3-96d6-7d5aa77c1e06
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49beb7ea4afe46c9b0f1640152c786d7c6ba8663
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805729"
---
# Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an


Die Konfigurationsdatei für die dynamische Bereitstellung wird angewendet, wenn ein Paket hinzugefügt oder auf einen Computer mit dem App-V 5,1-Client gesetzt wird, bevor das Paket veröffentlicht wurde. Die Datei konfiguriert die Standardeinstellungen für das Paket für alle Benutzer auf dem Computer, auf dem der App-V 5,1-Client ausgeführt wird. In diesem Abschnitt werden die Schritte beschrieben, die für die Verwendung einer Konfigurationsdatei für die Bereitstellung verwendet werden. Das Verfahren basiert auf dem folgenden Beispiel und setzt voraus, dass die folgenden Paket-und Konfigurationsdateien auf einem Computer vorhanden sind:

**c:\\Packages\\Contoso\\MyApp.appv**

**c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

**So wenden Sie die Konfigurationsdatei für die Bereitstellung mit PowerShell an**

-   Wenn Sie einen neuen Standardsatz von Konfigurationen für alle Benutzer angeben möchten, die das Paket auf einem bestimmten Computer ausführen sollen, geben Sie mithilfe einer PowerShell-Konsole Folgendes ein:

    **Add-AppVClientPackage – Path c:\\Packages\\Contoso\\MyApp.AppV-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

    **Hinweis:**  
    Mit diesem Befehl wird das resultierende Objekt in $pkg erfasst. Wenn das Paket bereits auf dem Computer vorhanden ist, kann das Cmdlet " **Set-AppVclientPackage** " verwendet werden, um das Bereitstellungs Konfigurationsdokument anzuwenden:

    **Satz-AppVClientPackage – Name MyApp – Path c:\\Packages\\Contoso\\MyApp.AppV-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)









