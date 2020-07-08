---
title: So konfigurieren Sie den Client für die Unterstützung von MIT Kerberos-Bereichen
description: So konfigurieren Sie den Client für die Unterstützung von MIT Kerberos-Bereichen
author: dansimp
ms.assetid: 46102f4c-270c-4115-8eb4-7ff5ae3be32d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ae5cd73d00f340bc50070fdd0a5fd3e038cc3789
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807256"
---
# So konfigurieren Sie den Client für die Unterstützung von MIT Kerberos-Bereichen


In Application Virtualization (App-V) 4,5 SP1 wurde die Unterstützung für mit Kerberos-Realms hinzugefügt. In diesem Thema finden Sie detaillierte Informationen dazu, wie Sie diese Unterstützung aktivieren können.

**So aktivieren Sie die Unterstützung für mit Kerberos-Realms**

-   Erstellen Sie wie folgt einen neuen Registrierungsschlüssel mit dem Namen **UseMitKerberos** vom Typ DWORD, und legen Sie ihn auf den Wert 1 fest.

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\usemitkerberos

 

 





