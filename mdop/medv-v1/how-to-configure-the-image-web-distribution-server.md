---
title: So konfigurieren Sie den Image-Web-Verteilungsserver
description: So konfigurieren Sie den Image-Web-Verteilungsserver
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810987"
---
# <span data-ttu-id="60a09-103">So konfigurieren Sie den Image-Web-Verteilungsserver</span><span class="sxs-lookup"><span data-stu-id="60a09-103">How to Configure the Image Web Distribution Server</span></span>


<span data-ttu-id="60a09-104">Bei einem Bild-Repository handelt es sich um einen optionalen Server, der für die Bildverteilung verwendet wird (wobei Administratoren neue Bilder hochladen und Clientcomputer alle 15 Minuten den Server überprüfen und das Bild aktualisieren, wenn ein neues verfügbar ist).</span><span class="sxs-lookup"><span data-stu-id="60a09-104">An image repository is an optional server that is used for image distribution (where administrators upload new images and client computers check the server every 15 minutes and update their image if a new one is available).</span></span>

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


<span data-ttu-id="60a09-105">Für einen Bildverteilungsserver ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="60a09-105">An image distribution server requires the following:</span></span>

-   <span data-ttu-id="60a09-106">Internetinformationsdienste (IIS) – Informationen finden Sie unter [Internetinformationsdienste](https://go.microsoft.com/fwlink/?LinkId=142995).</span><span class="sxs-lookup"><span data-stu-id="60a09-106">Internet Information Services (IIS)—For information, see [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).</span></span>

    <span data-ttu-id="60a09-107">Wählen Sie während der IIS-Installation beim Hinzufügen von Rollendiensten die folgenden unterstützten Authentifizierungsmethoden aus:</span><span class="sxs-lookup"><span data-stu-id="60a09-107">During the IIS installation, when adding role services, select the following supported authentication methods:</span></span>

    -   **<span data-ttu-id="60a09-108">Standardauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="60a09-108">Basic Authentication</span></span>**

    -   **<span data-ttu-id="60a09-109">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="60a09-109">Windows Authentication</span></span>**

    -   **<span data-ttu-id="60a09-110">Authentifizierung der Client Zertifikatzuordnung</span><span class="sxs-lookup"><span data-stu-id="60a09-110">Client Certificate Mapping Authentication</span></span>**

    <span data-ttu-id="60a09-111">Schließen Sie beim Konfigurieren von IIS Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="60a09-111">When configuring IIS, include the following:</span></span>

    -   <span data-ttu-id="60a09-112">Fügen Sie ein virtuelles Verzeichnis mit dem Alias " **MEDVImages**" hinzu.</span><span class="sxs-lookup"><span data-stu-id="60a09-112">Add a virtual directory, with the alias named **MEDVImages**.</span></span> <span data-ttu-id="60a09-113">Der physikalische Pfad sollte auf die Position der Bilder verweisen.</span><span class="sxs-lookup"><span data-stu-id="60a09-113">The physical path should point to the location of the images.</span></span>

    -   <span data-ttu-id="60a09-114">Aktivieren Sie Bits.</span><span class="sxs-lookup"><span data-stu-id="60a09-114">Enable BITS.</span></span>

    -   <span data-ttu-id="60a09-115">Fügen Sie die folgenden MIME-Typen hinzu:</span><span class="sxs-lookup"><span data-stu-id="60a09-115">Add the following MIME types:</span></span>

        -   **<span data-ttu-id="60a09-116">. CKM (Application/Oktett-Stream)</span><span class="sxs-lookup"><span data-stu-id="60a09-116">.ckm (application/octet-stream)</span></span>**

        -   <span data-ttu-id="60a09-117">**. Index (Application/Oktett-Stream**)</span><span class="sxs-lookup"><span data-stu-id="60a09-117">**.index (application/octet-stream**)</span></span>

    -   <span data-ttu-id="60a09-118">Fügen Sie auf der MED-V-Website **jedem Benutzer**Leseberechtigungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="60a09-118">On the MED-V site, add read permissions to **Everyone**.</span></span>

    -   <span data-ttu-id="60a09-119">Starten Sie IIS neu.</span><span class="sxs-lookup"><span data-stu-id="60a09-119">Restart IIS.</span></span>

-   <span data-ttu-id="60a09-120">BITS-Servererweiterungen für IIS – Informationen finden Sie unter [Installieren von BITS-Servererweiterungen](https://go.microsoft.com/fwlink/?LinkId=142996).</span><span class="sxs-lookup"><span data-stu-id="60a09-120">BITS Server Extensions for IIS—For information, see [Install BITS Server Extensions](https://go.microsoft.com/fwlink/?LinkId=142996).</span></span>

## <span data-ttu-id="60a09-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="60a09-121">Related topics</span></span>


[<span data-ttu-id="60a09-122">Unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="60a09-122">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="60a09-123">Entwerfen Sie die MED-V-Image-Repositorys</span><span class="sxs-lookup"><span data-stu-id="60a09-123">Design the MED-V Image Repositories</span></span>](design-the-med-v-image-repositories.md)

 

 





