---
title: So entfernen Sie ein Paket über die Befehlszeile
description: So entfernen Sie ein Paket über die Befehlszeile
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806860"
---
# So entfernen Sie ein Paket über die Befehlszeile


Sie können die folgenden Befehlszeilenverfahren zum Löschen eines virtuellen Anwendungspakets aus dem Application Virtualization (App-V)-Client auf einem bestimmten Computer verwenden.

**So löschen Sie ein virtuelles Anwendungspaket für alle Benutzer**

-   Wenn das Paket zuvor für alle Benutzer mithilfe des/Global-Schalters hinzugefügt wurde, verwenden Sie den folgenden Befehl, um das Paket und die globalen Dateitypen und Verknüpfungen zu löschen. Es sind Administrator Rechte erforderlich. In diesem Fall wird der/Global-Schalter nicht benötigt, da der Befehl immer ein globales Löschen des Pakets ausführt.

    `SFTMIME DELETE PACKAGE:”name”`

**So löschen Sie ein Paket, das zuvor für einzelne Benutzer hinzugefügt wurde**

1.  Wenn das Paket zuvor für einzelne Benutzer hinzugefügt wurde, stehen Ihnen mehrere Optionen zur Auswahl.

    Führen Sie den folgenden Befehl einmal unter dem Benutzerkonto jeder Person aus, in der das Paket veröffentlicht wurde. Dadurch wird dem Benutzer der Zugriff auf die Anwendungen verweigert, wenn er auf einen anderen Computer wechselt. Sie löscht die Einstellungen, Verknüpfungen und Dateitypen des jeweiligen Benutzers aus dem Profil und beendet die Hintergrund Auslastung unter dem Kontext des Benutzers.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  Alternativ können Sie den folgenden Befehl unter dem Benutzerkonto jeder Person ausführen, in der das Paket veröffentlicht wurde.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    Führen Sie dann diesen Befehl für das Paket aus.

    `SFTMIME DELETE PACKAGE:”name”`

    Dadurch wird das Paket vollständig entfernt, und es werden alle Benutzereinstellungen, Verknüpfungen und Dateitypen aus ihren Profilen gelöscht. Wenn das Paket anschließend erneut hinzugefügt wird, müssen die Benutzer die Einstellungen erneut angeben. Zum Ausführen dieses Befehls ist nur die Berechtigung "Delete Applications" (**DeleteApp**) erforderlich.

3.  Als dritte Alternative können Sie einfach den Befehl **Paket löschen** ausführen, ohne den Befehl **Paket veröffentlichen** zu verwenden. In diesem Fall werden Dateitypen und Tastenkombinationen für jeden Benutzer ausgeblendet und nicht gelöscht, und die Benutzereinstellungen bleiben erhalten. Wenn das Paket anschließend für den Benutzer erneut hinzugefügt wird, werden die Dateitypen und Verknüpfungen wiederhergestellt, und die Benutzereinstellungen werden erneut angewendet.

## Verwandte Themen


[So fügen Sie ein Paket über die Befehlszeile hinzu](how-to-add-a-package-by-using-the-command-line.md)

[So löschen Sie alle virtuelle Anwendungen über die Befehlszeile](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





