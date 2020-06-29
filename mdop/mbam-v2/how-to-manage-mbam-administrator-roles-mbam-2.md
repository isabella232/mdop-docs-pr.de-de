---
title: So verwalten Sie MBAM-Administratorrollen
description: So verwalten Sie MBAM-Administratorrollen
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810963"
---
# So verwalten Sie MBAM-Administratorrollen


Nachdem die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) für alle Server Features abgeschlossen ist, müssen Administrator Benutzern Zugriff auf Sie gewährt werden. Als bewährte Methode sollten Administratoren, die die Microsoft BitLocker-Verwaltungs-und-Überwachungs Server Features verwalten oder verwenden, den Sicherheitsgruppen für Domänendienste zugewiesen werden, und diese Gruppen sollten dann der entsprechenden administrativen lokalen Gruppe MBAM hinzugefügt werden.

**So verwalten Sie MBAM-Administrator Rollenmitgliedschaften**

1.  Zuweisen von administrativen Benutzern zu Sicherheitsgruppen in den Active Directory-Domänendiensten

2.  Fügen Sie den Rollen für MBAM administrative lokale Gruppen auf dem MBAM-Server für die jeweiligen Features Active Directory-Sicherheitsgruppen hinzu.

    -   **MBAM-System Administratoren** haben Zugriff auf alle MBAM-Features auf der MBAM-Verwaltungs-und-Überwachungs Website.

    -   **MBAM Helpdesk-Benutzer** haben Zugriff auf die Optionen "TPM verwalten" und "Drive Recovery" auf der MBAM-Website, müssen aber alle Felder ausfüllen, wenn Sie eine der beiden Optionen verwenden.

    -   **MBAM-Berichtsbenutzer** haben Zugriff auf die Konformitäts-und Überwachungsberichte auf der MBAM-Website.

    -   **MBAM Advanced Helpdesk-Benutzer** haben Zugriff auf die Optionen "TPM verwalten" und "Drive Recovery" auf der MBAM-Website für Verwaltung und Überwachung, sind aber nicht verpflichtet, alle Felder auszufüllen, wenn Sie eine der beiden Optionen verwenden.

    Weitere Informationen zu Rollen für die Microsoft BitLocker-Verwaltung und-Überwachung finden Sie unter [Planen von MBAM 2,0-Administrator Rollen](planning-for-mbam-20-administrator-roles-mbam-2.md).

## Verwandte Themen


[Verwalten von MBAM 2.0-Funktionen](administering-mbam-20-features-mbam-2.md)

 

 





