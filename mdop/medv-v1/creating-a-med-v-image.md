---
title: Erstellen eines MED-V-Images
description: Erstellen eines MED-V-Images
author: dansimp
ms.assetid: 7cbbcd22-83f5-4b60-825f-781b4c6a2d36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de1c2cd87d85bbe2fc40b9007eba8f86d2ed6f60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804274"
---
# <span data-ttu-id="56537-103">Erstellen eines MED-V-Images</span><span class="sxs-lookup"><span data-stu-id="56537-103">Creating a MED-V Image</span></span>


## <span data-ttu-id="56537-104">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="56537-104">In This Section</span></span>


<span data-ttu-id="56537-105">In diesem Abschnitt wird beschrieben, wie Sie ein Med-v-Abbild auf einem Computer konfigurieren, auf dem die Med-v-Client-und Med-v-Verwaltungsanwendung installiert ist, und erläutert Folgendes:</span><span class="sxs-lookup"><span data-stu-id="56537-105">This section describes how to configure a MED-V image on a computer on which the MED-V client and MED-V management application are installed, and explains the following:</span></span>

<a href="" id="how-to-create-and-test-a-med-v-image"></a>[<span data-ttu-id="56537-106">So erstellen und testen Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="56537-106">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)  
<span data-ttu-id="56537-107">Beschreibt, wie Sie ein MED-V-Bild erstellen und das Bild dann lokal testen.</span><span class="sxs-lookup"><span data-stu-id="56537-107">Describes how to create a MED-V image, and then test the image locally.</span></span>

<a href="" id="how-to-pack-a-med-v-image"></a>[<span data-ttu-id="56537-108">So packen Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="56537-108">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)  
<span data-ttu-id="56537-109">Beschreibt, wie Sie ein MED-V-Abbild Verpacken, damit es einem Bereitstellungspaket hinzugefügt oder auf den Server hochgeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="56537-109">Describes how to pack a MED-V image so that it can be added to a deployment package or uploaded to the server.</span></span>

<a href="" id="how-to-upload-a-med-v-image-to-the-server"></a>[<span data-ttu-id="56537-110">So laden Sie ein MED-V-Bild auf den Server hoch</span><span class="sxs-lookup"><span data-stu-id="56537-110">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)  
<span data-ttu-id="56537-111">Beschreibt, wie ein MED-V-Abbild auf den Server hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="56537-111">Describes how to upload a MED-V image to the server.</span></span>

<a href="" id="how-to-localize-a-med-v-image"></a>[<span data-ttu-id="56537-112">So lokalisieren Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="56537-112">How to Localize a MED-V Image</span></span>](how-to-localize-a-med-v-image.md)  
<span data-ttu-id="56537-113">Beschreibt, wie Sie ein MED-V-Bild lokalisieren, indem Sie das Bild extrahieren oder herunterladen.</span><span class="sxs-lookup"><span data-stu-id="56537-113">Describes how to localize a MED-V image either through extracting or downloading the image.</span></span>

<a href="" id="how-to-update-a-med-v-image"></a>[<span data-ttu-id="56537-114">So aktualisieren Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="56537-114">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)  
<span data-ttu-id="56537-115">Beschreibt, wie Sie ein MED-V-Abbild aktualisieren, um eine neue Version des Bilds zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="56537-115">Describes how to update a MED-V image to create a new version of the image.</span></span>

<a href="" id="how-to-delete-a-med-v-image"></a>[<span data-ttu-id="56537-116">So löschen Sie ein Image MED-V</span><span class="sxs-lookup"><span data-stu-id="56537-116">How to Delete a MED-V Image</span></span>](how-to-delete-a-med-v-image.md)  
<span data-ttu-id="56537-117">Beschreibt, wie Sie ein MED-V-Bild löschen.</span><span class="sxs-lookup"><span data-stu-id="56537-117">Describes how to delete a MED-V image.</span></span>

<span data-ttu-id="56537-118">**Hinweis**  Nachdem das Med-v-Abbild konfiguriert wurde, sollte der Computer nicht Teil einer Domäne sein, da das Verfahren für die Join-Domäne auf dem Client nach der Bereitstellung im Rahmen der Einrichtung des Med-v-Arbeitsbereichs ausgeführt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="56537-118">**Note** After the MED-V image is configured, the computer should not be part of a domain because the join domain procedure should be performed on the client after the deployment, as part of the MED-V workspace setup.</span></span>

 

 

 





