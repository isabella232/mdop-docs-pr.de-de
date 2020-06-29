---
title: So stellen Sie ein Arbeitsbereich-Image bereit
description: So stellen Sie ein Arbeitsbereich-Image bereit
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812094"
---
# <span data-ttu-id="56ccc-103">So stellen Sie ein Arbeitsbereich-Image bereit</span><span class="sxs-lookup"><span data-stu-id="56ccc-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="56ccc-104">Bei Verwendung eines Enterprise-Softwareverteilungssystems kann ein neues Bild auf Clientcomputern auf eine der folgenden Arten bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="56ccc-104">When using an enterprise software distribution system, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="56ccc-105">Web-Download</span><span class="sxs-lookup"><span data-stu-id="56ccc-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="56ccc-106">Pre-Staging von Bildern</span><span class="sxs-lookup"><span data-stu-id="56ccc-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="56ccc-107">Bereitstellen eines Arbeitsbereichs Bilds über das Web</span><span class="sxs-lookup"><span data-stu-id="56ccc-107">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="56ccc-108">So stellen Sie ein Arbeitsbereichs Bild über das Web bereit</span><span class="sxs-lookup"><span data-stu-id="56ccc-108">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="56ccc-109">Laden Sie das MED-V-Abbild auf den Server hoch.</span><span class="sxs-lookup"><span data-stu-id="56ccc-109">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="56ccc-110">Informationen zum Hochladen des Bilds finden Sie unter [Hochladen eines MED-V-Bilds auf den Server](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="56ccc-110">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="56ccc-111">Installieren Sie mithilfe Ihres Softwareverteilungssystems für Unternehmen das MED-V-Client. MSI-Paket auf den Computern der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="56ccc-111">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="56ccc-112">Informationen zum Installieren des Med-v Client. msi-Pakets finden Sie unter [so wird es gemacht: Installieren des Med-v-Clients](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="56ccc-112">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="56ccc-113">Der MED-V-Client wird zum ersten Mal installiert und gestartet.</span><span class="sxs-lookup"><span data-stu-id="56ccc-113">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="56ccc-114">Beim erstmaligen Start downloadet der Client das Bild von der Serveradresse, die in der Clientinstallation angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="56ccc-114">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="56ccc-115">So wird es gemacht: Bereitstellen eines Arbeitsbereichs Abbilds mithilfe von Bild Pre-Staging</span><span class="sxs-lookup"><span data-stu-id="56ccc-115">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="56ccc-116">So stellen Sie ein Arbeitsbereichs Bild mithilfe der vorbereitenden Bilder bereit</span><span class="sxs-lookup"><span data-stu-id="56ccc-116">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="56ccc-117">Erstellen Sie einen Bild-Pre-stage-Ordner, und drücken Sie das Bild in den Ordner.</span><span class="sxs-lookup"><span data-stu-id="56ccc-117">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="56ccc-118">Informationen zum Konfigurieren der Vorabbereitstellung von Bildern finden Sie unter [Konfigurieren der vorinszenierung von Bildern](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="56ccc-118">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="56ccc-119">Installieren Sie mithilfe Ihres Softwareverteilungssystems für Unternehmen das MED-V-Client. MSI-Paket auf den Computern der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="56ccc-119">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="56ccc-120">Informationen zum Installieren des Med-v Client. msi-Pakets finden Sie unter [so wird es gemacht: Installieren des Med-v-Clients](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="56ccc-120">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="56ccc-121">Der MED-V-Client wird zum ersten Mal installiert und gestartet.</span><span class="sxs-lookup"><span data-stu-id="56ccc-121">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="56ccc-122">Beim erstmaligen Start ruft der Client das Bild aus dem in der Clientinstallation angegebenen Pre-stage-Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="56ccc-122">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <span data-ttu-id="56ccc-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="56ccc-123">Related topics</span></span>


[<span data-ttu-id="56ccc-124">So konfigurieren Sie den Image-Web-Verteilungsserver</span><span class="sxs-lookup"><span data-stu-id="56ccc-124">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





