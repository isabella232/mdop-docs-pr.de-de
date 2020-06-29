---
title: High-Level-Architektur
description: High-Level-Architektur
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811614"
---
# High-Level-Architektur


Die MED-V-Lösung umfasst die folgenden Elemente:

-   **Vom Administrator definierter virtueller Computer**– kapselt eine vollständige Desktopumgebung, einschließlich eines Betriebssystems, von Anwendungen sowie optionaler Verwaltungs-und Sicherheitstools.

-   **Bild-Repository**– speichert alle virtuellen Bilder auf einem standardmäßigen IIS-Server und ermöglicht mithilfe der Trim-Transfer-Technologie die Versionsverwaltung virtueller Bilder, den Client-authentifizierten Bild Abruf und den effizienten Download (eines neuen Bilds oder Updates).

-   **Verwaltungsserver**– ordnet virtuelle Bilder aus dem Bild-Repository zusammen mit Administrator Nutzungsrichtlinien an Active Directory® Benutzer oder Gruppen an. Der Verwaltungsserver aggregiert auch die Ereignisse von Clients und speichert Sie für Überwachungs-und Berichterstattungs Zwecke in einer externen Datenbank (Microsoft SQL Server®).

-   **Verwaltungskonsole**– ermöglicht Administratoren die Steuerung des Verwaltungsservers und des Image-Repositorys.

-   **Endbenutzer Client**

    1.  Lebenszyklus virtueller Bilder – Authentifizierung, Bild Abruf, Erzwingung von Nutzungsrichtlinien.

    2.  Virtual Machine Session Management – starten, beenden und Sperren des virtuellen Computers.

    3.  Einfache Desktop Nutzung – Anwendungen, die auf dem virtuellen Computer installiert sind, sind über das standardmäßige Desktop-Startmenü nahtlos verfügbar und in andere Anwendungen auf dem Desktop des Benutzers integriert.

Die gesamte Kommunikation zwischen dem Client und den Servern (Verwaltungsserver und Image-Repository) wird über einem standardmäßigen HTTP-oder HTTPS-Kanal durchgeführt.

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





