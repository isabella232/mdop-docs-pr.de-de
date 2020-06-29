---
title: So installieren Sie MED-V-Client
description: So installieren Sie MED-V-Client
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812208"
---
# So installieren Sie MED-V-Client


In einem Bereitstellungspaket basierten Szenario ist die MED-V-Clientinstallation im Bereitstellungspaket enthalten und direkt aus dem Paket installiert.

**Wichtig**  
Wenn Sie ein Bereitstellungspaket verwenden, das kein Bild enthält, stellen Sie sicher, dass das Bild vor der Installation des Bereitstellungspakets in das Web hochgeladen oder in den Ordner Pre-stage verschoben wird.



**So installieren Sie ein Bereitstellungspaket**

1.  Führen Sie eine der folgenden Aktionen aus:

    -   Laden Sie das MED-V-Paket aus dem Web herunter.

    -   Legen Sie die Bereitstellung USB oder DVD in das Hostlaufwerk ein.

2.  Wenn MED-V nicht automatisch gestartet wird, doppelklicken Sie auf MED-VAutoInstaller.exe.

    Es wird ein Dialogfeld angezeigt, in dem die Komponenten aufgelistet sind, die bereits installiert sind und die derzeit installiert sind.

    **Hinweis:**  
    Wenn eine Version des Microsoft Virtual PC, die nicht unterstützt wird, auf dem Hostcomputer vorhanden ist, wird eine Meldung angezeigt, in der Sie darüber informiert werden, dass die vorhandene Version deinstalliert und das Installationsprogramm erneut ausgeführt werden soll.



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. Falls erforderlich, starten Sie den Computer neu.

   Nach Abschluss der Installation wird MED-V gestartet, und es wird eine Meldung angezeigt, in der Sie darüber informiert werden, dass die Installation abgeschlossen ist.

4. Melden Sie sich bei MED-V mit dem folgenden Benutzernamen und Kennwort an:

   -   Geben Sie den Domänennamen und den Benutzernamen gefolgt vom Kennwort des Domänenbenutzers ein, der mit MED-V arbeiten darf.

       Beispiel: "Domäne \ _name \\user\ _name"; "Kennwort"

## Verwandte Themen


[So konfigurieren Sie ein Bereitstellungspaket](how-to-configure-a-deployment-package.md)

[So laden Sie ein MED-V-Bild auf den Server hoch](how-to-upload-a-med-v-image-to-the-server.md)

[Befehlszeilenreferenz für die Clientinstallation](client-installation-command-line-reference.md)









