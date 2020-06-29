---
title: So setzen Sie den Dateisystemcache zurück
description: So setzen Sie den Dateisystemcache zurück
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806816"
---
# So setzen Sie den Dateisystemcache zurück


Das Zurücksetzen des Dateisystemcaches sollte in der Regel nicht erforderlich sein. Wenn Sie den Dateisystemcache allerdings, vielleicht zur Problembehandlung, vollständig zurücksetzen müssen, können Sie das folgende Verfahren verwenden. Zum Ausführen dieser Aktion sind Administratorrechte erforderlich.

**So setzen Sie den Dateisystemcache zurück**

1.  Setzen Sie den folgenden Registrierungswert auf 0 (null):

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\state

2.  Starten Sie den Computer neu.

## Verwandte Themen


[So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





