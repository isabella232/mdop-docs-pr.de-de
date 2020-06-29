---
title: So verwalten Sie MBAM-Administratorrollen
description: So verwalten Sie MBAM-Administratorrollen
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804625"
---
# So verwalten Sie MBAM-Administratorrollen


Nachdem das Setup für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) für alle Server Features abgeschlossen ist, müssen Administrator Benutzern Zugriff auf diese Server Features gewährt werden. Als bewährte Methode sollten Administratoren, die die MBAM-Server Features verwalten oder verwenden, Active Directory-Sicherheitsgruppen zugewiesen werden, und diese Gruppen sollten der entsprechenden administrativen lokalen Gruppe MBAM hinzugefügt werden.

**So verwalten Sie MBAM-Administrator Rollenmitgliedschaften**

1.  Zuweisen von administrativen Benutzern zu Sicherheitsgruppen in ActiveDirectoryDomain-Diensten.

2.  Fügen Sie den Rollen für MBAM administrative lokale Gruppen auf dem Microsoft BitLocker-Verwaltungs-und-Überwachungsserver für die jeweiligen Features ActiveDirectoryDomain-Dienst Sicherheitsgruppen hinzu. Die Benutzerrollen lauten wie folgt:

    -   **MBAM-System Administratoren** haben Zugriff auf alle Microsoft BitLocker-Verwaltungs-und-Überwachungsfeatures auf der MBAM-Verwaltungswebsite.

    -   **MBAM-Hardware Benutzer** können auf die Hardware Kompatibilitätsfeatures auf der MBAM-Verwaltungswebsite zugreifen.

    -   **MBAM Helpdesk-Benutzer** haben Zugriff auf die Optionen "TPM verwalten" und "Drive Recovery" auf der MBAM-Verwaltungswebsite, müssen aber alle Felder ausfüllen, wenn Sie eine der beiden Optionen verwenden.

    -   **MBAM-Berichtsbenutzer** haben Zugriff auf die Konformitäts-und Überwachungsberichte auf der MBAM-Verwaltungswebsite.

    -   **MBAM Advanced Helpdesk verwendet** Zugriff auf die Optionen "TPM verwalten" und "Drive Recovery" auf der MBAM-Verwaltungswebsite. Diese Benutzer müssen nicht alle Felder ausfüllen, wenn Sie eine der beiden Optionen verwenden.

    Weitere Informationen zu Rollen für die Microsoft BitLocker-Verwaltung und-Überwachung finden Sie unter [Planen von MBAM 1,0-Administrator Rollen](planning-for-mbam-10-administrator-roles.md).

## Verwandte Themen


[Verwalten von MBAM 1.0-Funktionen](administering-mbam-10-features.md)

 

 





