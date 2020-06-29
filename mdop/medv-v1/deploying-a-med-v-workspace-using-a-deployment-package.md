---
title: Bereitstellen eines MED-V-Arbeitsbereichs mit einem Bereitstellungspaket
description: Bereitstellen eines MED-V-Arbeitsbereichs mit einem Bereitstellungspaket
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810072"
---
# <span data-ttu-id="d2149-103">Bereitstellen eines MED-V-Arbeitsbereichs mit einem Bereitstellungspaket</span><span class="sxs-lookup"><span data-stu-id="d2149-103">Deploying a MED-V Workspace Using a Deployment Package</span></span>


<span data-ttu-id="d2149-104">Die Installation des Bereitstellungspakets bietet eine Methode zum Installieren des MED-V-Clients zusammen mit allen erforderlichen Voraussetzungen sowie sämtlichen vom Administrator vordefinierten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="d2149-104">The deployment package installation provides a method of installing MED-V client together with all its required prerequisites as well as any settings predefined by the administrator.</span></span>

<span data-ttu-id="d2149-105">Wenn Sie ein Bereitstellungspaket verwenden, wird das Paket über ein freigegebenes Netzwerk oder Wechselmedien verteilt.</span><span class="sxs-lookup"><span data-stu-id="d2149-105">When using a deployment package, the package is distributed via a shared network or removable media.</span></span> <span data-ttu-id="d2149-106">Das Bild kann im Paket enthalten sein oder separat verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d2149-106">The image can be included in the package or can be distributed separately.</span></span>

<span data-ttu-id="d2149-107">Bevor Sie ein Bereitstellungspaket erstellen, stellen Sie sicher, dass Sie ein MED-V-Abbild erstellt haben, das bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2149-107">Before creating a deployment package, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="d2149-108">Weitere Informationen zum Erstellen eines Med-v-Bilds finden Sie unter [Erstellen eines Med-v-Bilds](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="d2149-108">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="d2149-109">Nachdem das MED-V-Abbild vorbereitet wurde, sollten Sie die beste Methode zum Verteilen des Bilds in Ihrer Umgebung in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="d2149-109">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="d2149-110">Das Bild kann auf eine der folgenden Arten verteilt werden:</span><span class="sxs-lookup"><span data-stu-id="d2149-110">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="d2149-111">Im Web heruntergeladen und per Webdownload verteilt, optional mit Trim-Transfer-Technologie.</span><span class="sxs-lookup"><span data-stu-id="d2149-111">Uploaded to the Web and distributed via Web download, optionally using Trim Transfer technology.</span></span>

-   <span data-ttu-id="d2149-112">Wird mithilfe von Bild Pre-Staging verteilt.</span><span class="sxs-lookup"><span data-stu-id="d2149-112">Distributed using image pre-staging.</span></span>

-   <span data-ttu-id="d2149-113">Im Bereitstellungspaket enthalten und zusammen mit allen anderen MED-V-Komponenten verteilt.</span><span class="sxs-lookup"><span data-stu-id="d2149-113">Included in the deployment package and distributed together with all the other MED-V components.</span></span>

<span data-ttu-id="d2149-114">Wenn das Bild in das Paket aufgenommen wird, sind keine weiteren Konfigurationen für das Bild erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d2149-114">If the image will be included in the package, no other configurations are necessary for the image.</span></span> <span data-ttu-id="d2149-115">Wenn das Bild nicht im Bereitstellungspaket enthalten sein soll, führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="d2149-115">If the image will not be included in the deployment package, do one of the following:</span></span>

-   <span data-ttu-id="d2149-116">Wenn Sie das Bild über das Web bereitstellen, laden Sie das MED-V-Abbild auf den Bild-webverteilungs Server hoch.</span><span class="sxs-lookup"><span data-stu-id="d2149-116">If you are deploying the image via the Web, upload the MED-V image to the image Web distribution server.</span></span> <span data-ttu-id="d2149-117">Informationen zum Konfigurieren eines Image Web Distribution-Servers finden Sie unter [Konfigurieren des Image Web Distribution-Servers](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="d2149-117">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="d2149-118">Informationen zum Hochladen eines Bilds auf den Server finden Sie unter [Hochladen eines MED-V-Images auf den](how-to-upload-a-med-v-image-to-the-server.md)Server.</span><span class="sxs-lookup"><span data-stu-id="d2149-118">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

-   <span data-ttu-id="d2149-119">Wenn Sie das Bild über Pre-Staging für das Bild bereitstellen, konfigurieren Sie den Ordner "Pre-stage", und drücken Sie das MED-V-Bild in den Ordner.</span><span class="sxs-lookup"><span data-stu-id="d2149-119">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="d2149-120">Weitere Informationen zum Konfigurieren der vorinszenierung von Bildern finden Sie unter [Konfigurieren der vorinszenierung von Bildern](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="d2149-120">For more information on configuring the image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="d2149-121">**Hinweis**  Wenn Sie die vorinszenierung von Bildern verwenden, ist es wichtig, vor dem Erstellen des Bereitstellungspakets den Pre-stage-Ordner des Bilds zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d2149-121">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to creating the deployment package.</span></span> <span data-ttu-id="d2149-122">Der Ordnerpfad muss im Bereitstellungspaket enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="d2149-122">The folder path needs to be included in the deployment package.</span></span>

 

<span data-ttu-id="d2149-123">Erstellen Sie schließlich das Bereitstellungspaket.</span><span class="sxs-lookup"><span data-stu-id="d2149-123">Finally, create the deployment package.</span></span> <span data-ttu-id="d2149-124">Weitere Informationen zum Erstellen eines Bereitstellungspakets finden Sie unter [Konfigurieren eines Bereitstellungspakets](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="d2149-124">For more information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span> <span data-ttu-id="d2149-125">Nachdem das Paket abgeschlossen ist, verteilen Sie es für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d2149-125">After the package is complete, distribute it for deployment.</span></span>

<span data-ttu-id="d2149-126">Nachdem das Bereitstellungspaket verteilt wurde, kann der MED-V-Client installiert und das Bild bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d2149-126">After the deployment package is distributed, MED-V client can be installed and the image deployed.</span></span> <span data-ttu-id="d2149-127">Weitere Informationen zum Installieren des Med-v-Clients finden Sie unter [so wird es gemacht: Installieren des Med-v-Clients](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="d2149-127">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span> <span data-ttu-id="d2149-128">Weitere Informationen zum Bereitstellen des Bilds finden Sie unter [Bereitstellen eines Arbeitsbereichs Bilds](how-to-deploy-a-workspace-imagedeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="d2149-128">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imagedeployment-package.md).</span></span>

 

 





