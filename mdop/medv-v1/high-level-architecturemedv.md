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
# <span data-ttu-id="293ac-103">High-Level-Architektur</span><span class="sxs-lookup"><span data-stu-id="293ac-103">High-Level Architecture</span></span>


<span data-ttu-id="293ac-104">Die MED-V-Lösung umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="293ac-104">The MED-V solution comprises the following elements:</span></span>

-   <span data-ttu-id="293ac-105">**Vom Administrator definierter virtueller Computer**– kapselt eine vollständige Desktopumgebung, einschließlich eines Betriebssystems, von Anwendungen sowie optionaler Verwaltungs-und Sicherheitstools.</span><span class="sxs-lookup"><span data-stu-id="293ac-105">**Administrator-defined virtual machine**—Encapsulates a full desktop environment, including an operating system, applications, and optional management and security tools.</span></span>

-   <span data-ttu-id="293ac-106">**Bild-Repository**– speichert alle virtuellen Bilder auf einem standardmäßigen IIS-Server und ermöglicht mithilfe der Trim-Transfer-Technologie die Versionsverwaltung virtueller Bilder, den Client-authentifizierten Bild Abruf und den effizienten Download (eines neuen Bilds oder Updates).</span><span class="sxs-lookup"><span data-stu-id="293ac-106">**Image repository**—Stores all virtual images on a standard IIS server and enables virtual images version management, client-authenticated image retrieval, and efficient download (of a new image or updates) via Trim Transfer technology.</span></span>

-   <span data-ttu-id="293ac-107">**Verwaltungsserver**– ordnet virtuelle Bilder aus dem Bild-Repository zusammen mit Administrator Nutzungsrichtlinien an Active Directory® Benutzer oder Gruppen an.</span><span class="sxs-lookup"><span data-stu-id="293ac-107">**Management server**—Associates virtual images from the image repository along with administrator usage policies to Active Directory® users or groups.</span></span> <span data-ttu-id="293ac-108">Der Verwaltungsserver aggregiert auch die Ereignisse von Clients und speichert Sie für Überwachungs-und Berichterstattungs Zwecke in einer externen Datenbank (Microsoft SQL Server®).</span><span class="sxs-lookup"><span data-stu-id="293ac-108">The management server also aggregates clients' events and stores them in an external database (Microsoft SQL Server®) for monitoring and reporting purposes.</span></span>

-   <span data-ttu-id="293ac-109">**Verwaltungskonsole**– ermöglicht Administratoren die Steuerung des Verwaltungsservers und des Image-Repositorys.</span><span class="sxs-lookup"><span data-stu-id="293ac-109">**Management console**—Enables administrators to control the management server and the image repository.</span></span>

-   **<span data-ttu-id="293ac-110">Endbenutzer Client</span><span class="sxs-lookup"><span data-stu-id="293ac-110">End-user client</span></span>**

    1.  <span data-ttu-id="293ac-111">Lebenszyklus virtueller Bilder – Authentifizierung, Bild Abruf, Erzwingung von Nutzungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="293ac-111">Virtual image life-cycle—Authentication, image retrieval, enforcement of usage policies.</span></span>

    2.  <span data-ttu-id="293ac-112">Virtual Machine Session Management – starten, beenden und Sperren des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="293ac-112">Virtual machine session management—Start, stop, lock the virtual machine.</span></span>

    3.  <span data-ttu-id="293ac-113">Einfache Desktop Nutzung – Anwendungen, die auf dem virtuellen Computer installiert sind, sind über das standardmäßige Desktop-Startmenü nahtlos verfügbar und in andere Anwendungen auf dem Desktop des Benutzers integriert.</span><span class="sxs-lookup"><span data-stu-id="293ac-113">Single desktop experience—Applications installed in the virtual machine seamlessly available through the standard desktop Start menu and integrated with other applications on the user desktop.</span></span>

<span data-ttu-id="293ac-114">Die gesamte Kommunikation zwischen dem Client und den Servern (Verwaltungsserver und Image-Repository) wird über einem standardmäßigen HTTP-oder HTTPS-Kanal durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="293ac-114">All communication between the client and the servers (management server and image repository) is carried on top of a standard HTTP or HTTPS channel.</span></span>

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





