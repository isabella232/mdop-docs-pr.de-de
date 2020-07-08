---
title: Zusätzliche Komponenten für virtuelle Anwendungspakete
description: Zusätzliche Komponenten für virtuelle Anwendungspakete
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806163"
---
# Zusätzliche Komponenten für virtuelle Anwendungspakete


Der App-V-Sequenzer hat ein Verzeichnis gefunden, das 64-Bit-und 32-Bit-Dateien und/oder DLL-Dateien (Dynamic Link Library) enthält, die von der gleichen parallelen Assembly abhängig sind. In der Regel erstellt der Sequencer private nebeneinander angeordnete Assemblys für alle öffentlichen Assemblys, die vom Paket verwendet werden. Es ist jedoch nicht möglich, 32-Bit-und 64-Bit-Versionen der privaten Assemblys im gleichen Verzeichnis zu erstellen.

Wenn der Sequencer einen einzelnen Konflikt erkennt, führt er die folgenden Aktionen aus:

-   Entfernen Sie alle vorhandenen 64-Bit-privaten Assemblys im gesamten Paket, unabhängig davon, ob das Verzeichnis einen Konflikt aufweist.

-   Erstellen Sie nur 32-Bit-Versionen der privaten nebeneinander angeordneten Assemblys.

Sie sollten die öffentlichen Versionen aller erforderlichen 64-Bit-Assemblys auf dem Computer, auf dem der Sequencer ausgeführt wird, und auf allen App-V-Clientcomputern nativ installieren.

Um die erforderlichen vorhandenen öffentlichen Assemblys zu finden, öffnen Sie das Verzeichnis, in dem das Paket gespeichert ist, und suchen Sie im **VFS** -Ordner. Wenn beispielsweise der Paketstamm **Q:\\MyApp**ist, suchen Sie beim Sequenzieren der Anwendung in **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** , und suchen Sie alle vorhandenen öffentlichen Assemblys. Die 64-Bit-Versionen dieser Dateien beginnen immer mit dem folgenden Text am Anfang des manifestnamens: **amd64.**... Der genaue Name und die Version der Assembly finden Sie in der zugehörigen Manifestdatei.

Verwenden Sie einen der folgenden Links, um die richtige Version der erforderlichen Voraussetzungen herunterzuladen und zu installieren:

-   [Microsoft Visual C++ 2005 Redistributable Package (x64)](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [Microsoft Visual C++ 2005 SP1 Redistributable Package (x64)](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [Microsoft Visual C++ 2008 Redistributable Package (x64)](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





