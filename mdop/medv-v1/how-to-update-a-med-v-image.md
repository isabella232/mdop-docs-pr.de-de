---
title: So aktualisieren Sie ein MED-V-Image
description: So aktualisieren Sie ein MED-V-Image
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804271"
---
# <span data-ttu-id="11338-103">So aktualisieren Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="11338-103">How to Update a MED-V Image</span></span>


## <span data-ttu-id="11338-104">So aktualisieren Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="11338-104">How to Update a MED-V Image</span></span>


<span data-ttu-id="11338-105">Ein vorhandenes MED-V-Bild kann aktualisiert werden, wodurch eine neue Version des Bilds erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="11338-105">An existing MED-V image can be updated, thereby creating a new version of the image.</span></span> <span data-ttu-id="11338-106">Die neue Version kann dann auf Clientcomputern bereitgestellt werden, um das vorhandene Bild zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="11338-106">The new version can then be deployed on client computers, replacing the existing image.</span></span>

<span data-ttu-id="11338-107">**Hinweis**  Wenn eine neue Version auf dem Client bereitgestellt wird, wird das vorhandene Bild überschrieben.</span><span class="sxs-lookup"><span data-stu-id="11338-107">**Note** When a new version is deployed on the client, it overwrites the existing image.</span></span> <span data-ttu-id="11338-108">Stellen Sie beim Aktualisieren eines Bilds sicher, dass keine Daten auf dem Client gespeichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="11338-108">When updating an image, ensure that no data on the client needs to be saved.</span></span>

 

**<span data-ttu-id="11338-109">So aktualisieren Sie ein MED-V-Bild</span><span class="sxs-lookup"><span data-stu-id="11338-109">To update a MED-V image</span></span>**

1.  <span data-ttu-id="11338-110">Öffnen Sie das vorhandene Bild in Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="11338-110">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="11338-111">Nehmen Sie die erforderlichen Änderungen am Bild vor, und aktualisieren Sie das Bild (beispielsweise die Installation neuer Software).</span><span class="sxs-lookup"><span data-stu-id="11338-111">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="11338-112">Schließen Sie den virtuellen PC2007.</span><span class="sxs-lookup"><span data-stu-id="11338-112">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="11338-113">Testen Sie das Bild.</span><span class="sxs-lookup"><span data-stu-id="11338-113">Test the image.</span></span>

5.  <span data-ttu-id="11338-114">Nachdem das Bild getestet wurde, packen Sie es mit dem gleichen Namen wie das vorhandene Bild in das lokale Repository ein.</span><span class="sxs-lookup"><span data-stu-id="11338-114">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="11338-115">**Hinweis**  Wenn Sie dem Bild einen anderen Namen als die vorhandene Version geben, wird anstelle einer neuen Version des vorhandenen Bilds ein neues Bild erstellt.</span><span class="sxs-lookup"><span data-stu-id="11338-115">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="11338-116">Laden Sie die neue Version auf den Server hoch, oder verteilen Sie Sie über ein Bereitstellungspaket.</span><span class="sxs-lookup"><span data-stu-id="11338-116">Upload the new version to the server or distribute it via a deployment package.</span></span>

## <span data-ttu-id="11338-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="11338-117">Related topics</span></span>


[<span data-ttu-id="11338-118">Erstellen eines virtuellen PC-Images für MED-V</span><span class="sxs-lookup"><span data-stu-id="11338-118">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="11338-119">So erstellen und testen Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="11338-119">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)

[<span data-ttu-id="11338-120">So packen Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="11338-120">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)

[<span data-ttu-id="11338-121">So laden Sie ein MED-V-Bild auf den Server hoch</span><span class="sxs-lookup"><span data-stu-id="11338-121">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="11338-122">Aktualisieren eines MED-V-Arbeitsbereich-Images</span><span class="sxs-lookup"><span data-stu-id="11338-122">Updating a MED-V Workspace Image</span></span>](updating-a-med-v-workspace-image.md)

 

 





