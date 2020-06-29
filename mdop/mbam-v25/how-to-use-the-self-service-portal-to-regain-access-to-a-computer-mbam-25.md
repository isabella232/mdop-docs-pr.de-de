---
title: So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können
description: So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811914"
---
# So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können


Das Self-Service-Portal ist eine Website, die von IT-Administratoren im Rahmen Ihrer Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5-Bereitstellung konfiguriert wird. Die Website ermöglicht es Endbenutzern, den Zugriff auf Ihre Computer unabhängig voneinander wiederherzustellen, wenn Sie von Windows ausgeschlossen werden. Das Self-Service-Portal erfordert keine Unterstützung durch das Helpdesk-Personal.

Die folgenden Anweisungen werden aus der Perspektive der Endbenutzer geschrieben, aber die Informationen können für IT-Administratoren nützlich sein, um Sie zu verstehen.

**Wichtig**  Ein Endbenutzer muss sich physisch mindestens einmal erfolgreich am Computer (nicht Remote) angemeldet haben, um seinen Schlüssel über das Self-Service-Portal wiederherstellen zu können. Andernfalls müssen Sie das Helpdesk-Portal für die Schlüsselwiederherstellung verwenden.

 

Endbenutzer können Aussperrungen erfahren, wenn Sie:

-   Kennwort oder PIN vergessen

-   Ändern von Betriebssystemdateien, dem BIOS oder dem Trusted Platform Module (TPM)

**Hinweis**  Wenn der IT-Administrator einen Timeout für den IIS-Sitzungszustand konfiguriert hat, wird im Self-Service-Portal 60 Sekunden vor dem Timeout eine Meldung angezeigt.

 

**So verwenden Sie das Self-Service-Portal zum wieder Zugriff auf einen Computer**

1.  Geben Sie im Feld **Wiederherstellungs KeyId** eine der 32-stelligen BitLocker-Schlüssel-IDs ein, die auf dem BitLocker-Wiederherstellungsbildschirm Ihres Computers angezeigt werden. Wenn die ersten acht Ziffern mit mehreren Schlüsseln übereinstimmen, wird eine Meldung angezeigt, in der Sie alle 32-Ziffern der Wiederherstellungsschlüssel-ID eingeben müssen.

2.  Wählen Sie im Feld **Grund** einen Grund für Ihre Anforderung für den Wiederherstellungsschlüssel aus.

3.  Klicken Sie auf **Schlüssel abrufen**. Ihr BitLocker-Wiederherstellungsschlüssel wird im Feld **BitLocker-Wiederherstellungsschlüssel** angezeigt.

4.  Geben Sie den 48-stelligen Code in den BitLocker-Wiederherstellungsbildschirm auf dem Computer ein, um wieder Zugriff auf den Computer zu erhalten.



## Verwandte Themen


[Durchführen der BitLocker-Verwaltung mit MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





