---
title: So sichern Sie einen MED-V-Server und stellen ihn wieder her
description: So sichern Sie einen MED-V-Server und stellen ihn wieder her
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809745"
---
# So sichern Sie einen MED-V-Server und stellen ihn wieder her


XML-Dateien, die sich auf dem Server befinden, können gesichert und dann wiederhergestellt werden, wenn Daten auf dem Server verloren gehen.

**So sichern Sie einen MED-V-Server**

-   Sichern Sie die folgenden Dateien in * &lt; INSTALLDIR &gt; \\Servers\\ConfigurationServer*:

    **Hinweis**  Wenn die Konfiguration von der Standardeinstellung geändert wurde, werden die Dateien möglicherweise an einem anderen Speicherort gespeichert.

     

    -   ClientPolicy.xml

    -   ClientSettings.xml

    -   ConfigurationFiles.xml

    -   OrganizationPolicy.xml

    -   WorkspaceKeys.xml

    **Hinweis**  Die ServerSettings.xml-Datei kann ebenfalls gesichert werden. Wenn jedoch eine bestimmte Konfiguration geändert wurde (beispielsweise auf dem ursprünglichen Server befindet sich das MED-V VMS-Verzeichnis in "*C:\\Vms*", und ein solches Verzeichnis ist auf dem neuen Server nicht vorhanden), kann dies zu einem Fehler führen.

     

**So stellen Sie einen MED-V-Server wieder her**

1.  Installieren Sie einen neuen MED-V-Server.

2.  Kopieren Sie die Sicherungsdateien in das folgende Verzeichnis:

    *&lt;INSTALLDIR &gt; \\Servers\\ConfigurationServer*

3.  Starten Sie den MED-V-Dienst erneut.

 

 





