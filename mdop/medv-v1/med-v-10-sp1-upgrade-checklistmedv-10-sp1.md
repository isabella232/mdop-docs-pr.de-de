---
title: Upgradeprüfliste für MED-V 1.0 SP1
description: Upgradeprüfliste für MED-V 1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812253"
---
# Upgradeprüfliste für MED-V 1.0 SP1


Um Microsoft Enterprise Desktop Virtualization (Med-v) 1.0 auf Med-v 1.0 Service Pack1 (SP1) zu aktualisieren, muss der Client aktualisiert werden. Optional kann der Server aktualisiert werden.

## Server Upgrade


**So aktualisieren Sie den Med-v 1.0-Server auf Med-v 1.0 SP1**

1.  Sichern Sie die folgenden Dateien, die sich im Verzeichnis * &lt; INSTALLDIR &gt; /Servers/ConfigurationServer* befinden:

    -   OrganizationalPolicy.XML

    -   ClientPolicy.XML

    -   WorkspaceKeys.XML

2.  Sichern Sie die * &lt; INSTALLDIR &gt; /Server/ServerSettings.xml-* Datei.

3.  Deinstallieren Sie den Med-v 1.0-Server.

4.  Installieren Sie den Med-v 1.0 SP1-Server.

5.  Stellen Sie die Sicherungsdateien in den entsprechenden Verzeichnissen wieder her.

6.  Starten Sie den MED-V-Server Dienst erneut.

**Hinweis**  Wenn die Serverkonfiguration vom Standardwert geändert wurde, werden die Dateien möglicherweise an einem anderen Speicherort gespeichert.

 

## Client Upgrade


Wenn Sie den Med-v 1.0-Client auf Med-v 1.0 SP1 aktualisieren möchten, installieren Sie die MSP-Datei auf einem Med-v 1.0-Client. Der Client und MED-V werden automatisch aktualisiert.

 

 





