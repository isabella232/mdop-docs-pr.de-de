---
title: Bereitstellen eines MED-V-Arbeitsbereichs über ein Enterprise Software Distribution-System
description: Bereitstellen eines MED-V-Arbeitsbereichs über ein Enterprise Software Distribution-System
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810069"
---
# <span data-ttu-id="dbf99-103">Bereitstellen eines MED-V-Arbeitsbereichs über ein Enterprise Software Distribution-System</span><span class="sxs-lookup"><span data-stu-id="dbf99-103">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>


<span data-ttu-id="dbf99-104">Der MED-V-Client kann mithilfe eines Unternehmenssoftware Verteilungssystems wie Microsoft System Center Configuration Manager verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="dbf99-104">MED-V client can be distributed using an enterprise software distribution system, such as Microsoft System Center Configuration Manager.</span></span>

<span data-ttu-id="dbf99-105">**Hinweis**  Wenn Med-v mithilfe von Microsoft System Center Configuration Manager installiert wird, legen Sie beim Erstellen eines Pakets für med-v den Ausführungsmodus auf Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="dbf99-105">**Note** If MED-V is installed by using Microsoft System Center Configuration Manager, when creating a package for MED-V, set the run mode to administrative rights.</span></span>

 

<span data-ttu-id="dbf99-106">Bevor Sie Med-v mithilfe eines Enterprise-Softwareverteilungssystems bereitstellen, stellen Sie sicher, dass Sie ein Med-v-Abbild erstellt haben, das bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dbf99-106">Before deploying MED-V using an enterprise software distribution system, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="dbf99-107">Weitere Informationen zum Erstellen eines Med-v-Bilds finden Sie unter [Erstellen eines Med-v-Bilds](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="dbf99-107">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="dbf99-108">Nachdem das MED-V-Abbild vorbereitet wurde, sollten Sie die beste Methode zum Verteilen des Bilds in Ihrer Umgebung in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="dbf99-108">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="dbf99-109">Das Bild kann auf eine der folgenden Arten verteilt werden:</span><span class="sxs-lookup"><span data-stu-id="dbf99-109">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="dbf99-110">Im Web heruntergeladen und per Webdownload vertrieben, optional mit Trim-Transfer-Technologie.</span><span class="sxs-lookup"><span data-stu-id="dbf99-110">Uploaded to the Web and distributed via Web download, optionally utilizing Trim Transfer technology.</span></span>

-   <span data-ttu-id="dbf99-111">Wird mithilfe von Bild Pre-Staging verteilt.</span><span class="sxs-lookup"><span data-stu-id="dbf99-111">Distributed using image pre-staging.</span></span>

## <span data-ttu-id="dbf99-112">Bereitstellen des Bilds über das Web</span><span class="sxs-lookup"><span data-stu-id="dbf99-112">Deploying the Image via the Web</span></span>


<span data-ttu-id="dbf99-113">Wenn Sie das Bild über das Web bereitstellen, laden Sie das MED-V-Abbild auf einen Bild-webverteilungs Server hoch.</span><span class="sxs-lookup"><span data-stu-id="dbf99-113">If you are deploying the image via the Web, upload the MED-V image to an image Web distribution server.</span></span> <span data-ttu-id="dbf99-114">Informationen zum Konfigurieren eines Image Web Distribution-Servers finden Sie unter [Konfigurieren des Image Web Distribution-Servers](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="dbf99-114">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="dbf99-115">Informationen zum Hochladen eines Bilds auf den Server finden Sie unter [Hochladen eines MED-V-Images auf den](how-to-upload-a-med-v-image-to-the-server.md)Server.</span><span class="sxs-lookup"><span data-stu-id="dbf99-115">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

## <span data-ttu-id="dbf99-116">Bereitstellen des Bilds über Pre-Staging</span><span class="sxs-lookup"><span data-stu-id="dbf99-116">Deploying the Image via Pre-staging</span></span>


<span data-ttu-id="dbf99-117">Wenn Sie das Bild über Pre-Staging für das Bild bereitstellen, konfigurieren Sie den Ordner "Pre-stage", und drücken Sie das MED-V-Bild in den Ordner.</span><span class="sxs-lookup"><span data-stu-id="dbf99-117">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="dbf99-118">Weitere Informationen zum Konfigurieren von Bild Pre-Staging finden Sie unter [so wird es gemacht: Konfigurieren der Vorabbereitstellung von Bildern](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="dbf99-118">For more information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="dbf99-119">**Hinweis**  Wenn Sie die vorinszenierung von Bildern verwenden, ist es wichtig, vor dem pushen des Client. msi-Pakets den Pre-stage-Ordner des Bilds zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dbf99-119">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to pushing the client .msi package.</span></span> <span data-ttu-id="dbf99-120">Der Pfad des Ordners muss im Client. MSI-Paket enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="dbf99-120">The folder path needs to be included in the client .msi package.</span></span>

 

<span data-ttu-id="dbf99-121">Und schließlich: Pushen Sie das Client. MSI-Paket mithilfe Ihres Software Verteilungs Centers für Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="dbf99-121">Finally, push the client .msi package using your enterprise software distribution center.</span></span> <span data-ttu-id="dbf99-122">MED-V kann dann installiert und das Bild bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dbf99-122">MED-V can then be installed and the image deployed.</span></span> <span data-ttu-id="dbf99-123">Weitere Informationen zum Installieren des Med-v-Clients finden Sie unter [so wird es gemacht: Installieren des Med-v-Clients](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="dbf99-123">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span> <span data-ttu-id="dbf99-124">Weitere Informationen zum Bereitstellen des Bilds finden Sie unter [Bereitstellen eines Arbeitsbereichs Bilds](how-to-deploy-a-workspace-imageesds.md).</span><span class="sxs-lookup"><span data-stu-id="dbf99-124">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imageesds.md).</span></span>

 

 





