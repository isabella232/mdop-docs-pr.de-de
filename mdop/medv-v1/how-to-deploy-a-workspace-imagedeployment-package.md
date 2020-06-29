---
title: So stellen Sie ein Arbeitsbereich-Image bereit
description: So stellen Sie ein Arbeitsbereich-Image bereit
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812100"
---
# <span data-ttu-id="9a32e-103">So stellen Sie ein Arbeitsbereich-Image bereit</span><span class="sxs-lookup"><span data-stu-id="9a32e-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="9a32e-104">Wenn Sie ein Bereitstellungspaket verwenden, kann ein neues Bild auf Clientcomputern auf eine der folgenden Arten bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="9a32e-104">When using a deployment package, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="9a32e-105">Web-Download</span><span class="sxs-lookup"><span data-stu-id="9a32e-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="9a32e-106">Pre-Staging von Bildern</span><span class="sxs-lookup"><span data-stu-id="9a32e-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [<span data-ttu-id="9a32e-107">Bereitstellen des Bilds im Bereitstellungspaket</span><span class="sxs-lookup"><span data-stu-id="9a32e-107">Deploying the image inside the deployment package</span></span>](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="9a32e-108">Bereitstellen eines Arbeitsbereichs Bilds über das Web</span><span class="sxs-lookup"><span data-stu-id="9a32e-108">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="9a32e-109">So stellen Sie ein Arbeitsbereichs Bild über das Web bereit</span><span class="sxs-lookup"><span data-stu-id="9a32e-109">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="9a32e-110">Laden Sie das MED-V-Abbild auf den Server hoch.</span><span class="sxs-lookup"><span data-stu-id="9a32e-110">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="9a32e-111">Informationen zum Hochladen des Bilds finden Sie unter [Hochladen eines MED-V-Bilds auf den Server](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="9a32e-111">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="9a32e-112">Erstellen Sie ein Bereitstellungspaket, und fügen Sie den Serverpfad zum Speicherort des Bilds ein.</span><span class="sxs-lookup"><span data-stu-id="9a32e-112">Create a deployment package, and include the server path to the location of the image.</span></span>

    <span data-ttu-id="9a32e-113">Informationen zum Erstellen eines Bereitstellungspakets finden Sie unter [Konfigurieren eines Bereitstellungspakets](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="9a32e-113">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="9a32e-114">Bereitstellen des Pakets für Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="9a32e-114">Deploy the package to end users.</span></span>

    <span data-ttu-id="9a32e-115">Informationen zum Bereitstellen des Pakets finden Sie unter [so wird es gemacht: Installieren des MED-V-Clients](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="9a32e-115">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="9a32e-116">Der MED-V-Client wird zum ersten Mal installiert und gestartet.</span><span class="sxs-lookup"><span data-stu-id="9a32e-116">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="9a32e-117">Beim erstmaligen Start downloadet der Client das Bild von der Serveradresse, die in der Clientinstallation angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9a32e-117">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="9a32e-118">So wird es gemacht: Bereitstellen eines Arbeitsbereichs Abbilds mithilfe von Bild Pre-Staging</span><span class="sxs-lookup"><span data-stu-id="9a32e-118">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="9a32e-119">So stellen Sie ein Arbeitsbereichs Bild mithilfe der vorbereitenden Bilder bereit</span><span class="sxs-lookup"><span data-stu-id="9a32e-119">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="9a32e-120">Erstellen Sie einen Bild-Pre-stage-Ordner, und drücken Sie das Bild in den Ordner.</span><span class="sxs-lookup"><span data-stu-id="9a32e-120">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="9a32e-121">Informationen zum Konfigurieren der Vorabbereitstellung von Bildern finden Sie unter [Konfigurieren der vorinszenierung von Bildern](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="9a32e-121">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="9a32e-122">Erstellen Sie ein Bereitstellungspaket, und fügen Sie den Pfad in den Ordner "Pre-stage" des Bilds ein.</span><span class="sxs-lookup"><span data-stu-id="9a32e-122">Create a deployment package, and include the path to the image pre-stage folder.</span></span>

    <span data-ttu-id="9a32e-123">Informationen zum Erstellen eines Bereitstellungspakets finden Sie unter [Konfigurieren eines Bereitstellungspakets](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="9a32e-123">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="9a32e-124">Bereitstellen des Pakets für Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="9a32e-124">Deploy the package to end users.</span></span>

    <span data-ttu-id="9a32e-125">Informationen zum Bereitstellen des Pakets finden Sie unter [so wird es gemacht: Installieren des MED-V-Clients](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="9a32e-125">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="9a32e-126">Der MED-V-Client wird zum ersten Mal installiert und gestartet.</span><span class="sxs-lookup"><span data-stu-id="9a32e-126">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="9a32e-127">Beim erstmaligen Start ruft der Client das Bild aus dem in der Clientinstallation angegebenen Pre-stage-Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="9a32e-127">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a><span data-ttu-id="9a32e-128">Bereitstellen eines Arbeitsbereichs Bilds mithilfe eines Bereitstellungspakets</span><span class="sxs-lookup"><span data-stu-id="9a32e-128">How to Deploy a Workspace Image Using a Deployment Package</span></span>


**<span data-ttu-id="9a32e-129">So stellen Sie ein Arbeitsbereichs Bild mithilfe eines Bereitstellungspakets bereit</span><span class="sxs-lookup"><span data-stu-id="9a32e-129">To deploy a workspace image using a deployment package</span></span>**

1.  <span data-ttu-id="9a32e-130">Erstellen Sie ein Bereitstellungspaket, und fügen Sie das Bild in das Paket ein.</span><span class="sxs-lookup"><span data-stu-id="9a32e-130">Create a deployment package, and include the image in the package.</span></span>

    <span data-ttu-id="9a32e-131">Informationen zum Erstellen eines Bereitstellungspakets finden Sie unter [Konfigurieren eines Bereitstellungspakets](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="9a32e-131">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

2.  <span data-ttu-id="9a32e-132">Bereitstellen des Pakets für Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="9a32e-132">Deploy the package to end users.</span></span>

    <span data-ttu-id="9a32e-133">Informationen zum Bereitstellen des Pakets finden Sie unter [so wird es gemacht: Installieren des MED-V-Clients](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="9a32e-133">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="9a32e-134">Das Bild wird als Teil der Paketinstallation in den Host importiert.</span><span class="sxs-lookup"><span data-stu-id="9a32e-134">The image is imported to the host as part of the package installation.</span></span>

## <span data-ttu-id="9a32e-135">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9a32e-135">Related topics</span></span>


[<span data-ttu-id="9a32e-136">So konfigurieren Sie den Image-Web-Verteilungsserver</span><span class="sxs-lookup"><span data-stu-id="9a32e-136">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

[<span data-ttu-id="9a32e-137">So konfigurieren Sie ein Bereitstellungspaket</span><span class="sxs-lookup"><span data-stu-id="9a32e-137">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

 

 





