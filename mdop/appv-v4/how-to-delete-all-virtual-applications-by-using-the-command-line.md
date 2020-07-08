---
title: So löschen Sie alle virtuelle Anwendungen über die Befehlszeile
description: So löschen Sie alle virtuelle Anwendungen über die Befehlszeile
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807147"
---
# So löschen Sie alle virtuelle Anwendungen über die Befehlszeile


Mit dem folgenden Verfahren können Sie alle virtuellen Anwendungen von einem bestimmten Computer löschen.

**Hinweis**  Wenn alle Anwendungen aus einem Paket gelöscht werden, löscht der Application Virtualization (App-V)-Client auch das Paket.

 

**So löschen Sie alle Anwendungen**

-   Führen Sie den folgenden Befehl aus, um alle Anwendungen für das Benutzerkonto zu löschen, unter dem der Befehl ausgeführt wird. Wenn Sie den Befehl mit dem optionalen/Global-Schalter ausführen und ein Konto mit Administratorrechten verwenden, werden alle Anwendungen für alle Benutzer gelöscht.

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    **Hinweis**  Wenn alle Anwendungen aus einem Paket gelöscht werden, löscht der Application Virtualization (App-V)-Client auch das Paket.

     

## Verwandte Themen


[So fügen Sie ein Paket über die Befehlszeile hinzu](how-to-add-a-package-by-using-the-command-line.md)

[So entfernen Sie ein Paket über die Befehlszeile](how-to-remove-a-package-by-using-the-command-line.md)

 

 





