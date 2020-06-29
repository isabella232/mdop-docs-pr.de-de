---
title: So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können
description: So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811539"
---
# So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können


Wenn Endbenutzer von BitLocker von Windows gesperrt werden, weil Sie Ihr Kennwort oder Ihre PIN vergessen haben, oder weil Sie die Betriebssystemdateien geändert oder das BIOS oder das Trusted Platform Module (TPM) geändert haben, können Sie das Self-Service-Portal verwenden, um wieder Zugriff auf Windows zu erhalten, ohne den Helpdesk um Unterstützung bitten zu müssen.

**Hinweis**  Wenn der IT-Administrator einen Timeout für den IIS-Sitzungszustand konfiguriert hat, wird eine Meldung 60 Sekunden vor dem Timeout angezeigt.

 

**Hinweis**  Diese Anweisungen sind für und aus der Perspektive von Endbenutzern geschrieben.

 

**So verwenden Sie das Self-Service-Portal zum wieder Zugriff auf einen Computer**

1.  Geben Sie im Feld **Wiederherstellungs KeyId** eine der 32-stelligen BitLocker-Schlüssel-IDs ein, die auf dem BitLocker-Wiederherstellungsbildschirm Ihres Computers angezeigt werden.

    **Hinweis**  Wenn die ersten acht Ziffern mit mehreren Schlüsseln übereinstimmen, wird eine Meldung angezeigt, in der Sie alle 32-Ziffern der Wiederherstellungsschlüssel-ID eingeben müssen.

     

2.  Wählen Sie im Feld **Grund** einen Grund für Ihre Anforderung für den Wiederherstellungsschlüssel aus.

3.  Klicken Sie auf **Schlüssel abrufen**. Ihr BitLocker-Wiederherstellungsschlüssel wird im Feld "Ihr BitLocker-Wiederherstellungsschlüssel" angezeigt.

4.  Geben Sie den 48-stelligen Code in den BitLocker-Wiederherstellungsbildschirm auf dem Computer ein, um wieder Zugriff auf den Computer zu erhalten.

## Verwandte Themen


[Verwalten von BitLocker mit MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





