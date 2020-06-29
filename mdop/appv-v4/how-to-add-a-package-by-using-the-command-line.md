---
title: So fügen Sie ein Paket über die Befehlszeile hinzu
description: So fügen Sie ein Paket über die Befehlszeile hinzu
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808737"
---
# So fügen Sie ein Paket über die Befehlszeile hinzu


In den folgenden Verfahren sind die Schritte aufgeführt, die zum Hinzufügen eines virtuellen Anwendungspakets zum Application Virtualization (App-V)-Client auf einem bestimmten Computer erforderlich sind.

**So fügen Sie ein virtuelles Anwendungspaket für einen bestimmten Benutzer hinzu**

-   Führen Sie den folgenden Befehl unter dem Benutzerkonto der Person aus, die das Paket erhalten soll. Mit dem Befehl wird das Paket für diesen Benutzer hinzugefügt und veröffentlicht.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**So fügen Sie ein virtuelles Anwendungspaket für alle Benutzer hinzu**

-   Führen Sie den folgenden Befehl unter einem Konto mit Administratorrechten aus. Das Paket wird für alle Benutzer auf dem Computer hinzugefügt und veröffentlicht.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**So fügen Sie ein Paket mit einem elektronischen Softwareverteilungssystem hinzu**

1.  Wenn Sie ein elektronisches Softwareverteilungssystem verwenden, das die Befehle unter dem **System** Konto des Computers ausführt, wird das Paket nur für dieses Konto veröffentlicht, es sei denn, Sie verwenden den/Global-Schalter. Führen Sie den folgenden Befehl aus, um das Paket für alle Benutzer auf dem Computer hinzuzufügen und zu veröffentlichen:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    Wenn Sie das Paket nur für bestimmte Benutzer hinzufügen möchten, führen Sie den Befehl **Paket hinzufügen** aus, und veröffentlichen Sie dann das Paket für jeden Benutzer explizit, indem Sie den folgenden Befehl zum **veröffentlichen** des Pakets unter dem Benutzerkonto jeder Person ausführen:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    Durch die Veröffentlichung des Pakets ohne den globalen Parameter wird dem Benutzer der Zugriff auf die Anwendungen im Paket gewährt, und die im Manifest aufgelisteten Dateitypen und Verknüpfungen werden im Profil des Benutzers veröffentlicht. Die erforderlichen Berechtigungen sind "Verwalten von Dateitypzuordnungen" (**ManageTypes**) und "Veröffentlichungs Verknüpfungen" (**PublishShortcut**).

## Verwandte Themen


[So löschen Sie alle virtuelle Anwendungen über die Befehlszeile](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[So entfernen Sie ein Paket über die Befehlszeile](how-to-remove-a-package-by-using-the-command-line.md)

 

 





