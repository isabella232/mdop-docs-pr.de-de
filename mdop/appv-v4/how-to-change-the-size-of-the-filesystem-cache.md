---
title: So ändern Sie die Größe des Dateisystemcaches
description: So ändern Sie die Größe des Dateisystemcaches
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807332"
---
# So ändern Sie die Größe des Dateisystemcaches


Sie können die Größe des Dateisystemcaches über die Befehlszeile ändern. Für diese Aktion ist ein vollständiges Zurücksetzen des Caches erforderlich, und es sind Administratorrechte erforderlich.

**So ändern Sie die Größe des Dateisystemcaches**

1.  Setzen Sie den folgenden Registrierungswert auf 0 (null):

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\state

2.  Setzen Sie den folgenden Registrierungswert auf die maximale Cachegröße in MB, die für die Speicherung der Pakete erforderlich ist, beispielsweise 8192 MB:

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\filesize

3.  Starten Sie den Computer neu.

## Verwandte Themen


[So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





