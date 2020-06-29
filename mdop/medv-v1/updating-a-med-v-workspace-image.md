---
title: Aktualisieren eines MED-V-Arbeitsbereich-Images
description: Aktualisieren eines MED-V-Arbeitsbereich-Images
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811404"
---
# <span data-ttu-id="8a654-103">Aktualisieren eines MED-V-Arbeitsbereich-Images</span><span class="sxs-lookup"><span data-stu-id="8a654-103">Updating a MED-V Workspace Image</span></span>


<span data-ttu-id="8a654-104">Ein Bild kann auf eine der folgenden Arten aktualisiert werden:</span><span class="sxs-lookup"><span data-stu-id="8a654-104">An image can be updated in one of the following ways:</span></span>

-   <span data-ttu-id="8a654-105">Das Update kann über Ihr Unternehmenssoftware-Verteilungssystem an das Gastbetriebssystem übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="8a654-105">The update can be pushed to the guest operating system using your enterprise software distribution system.</span></span>

-   <span data-ttu-id="8a654-106">Das Update kann auf den Image Web Distribution-Server hochgeladen und dann vom Client heruntergeladen und auf das MED-V-Abbild angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a654-106">The update can be uploaded to the image Web distribution server, and then downloaded by the client and applied to the MED-V image.</span></span>

-   <span data-ttu-id="8a654-107">Das MED-V-Basis Bild kann aktualisiert und erneut bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8a654-107">The MED-V base image can be updated and redeployed.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a><span data-ttu-id="8a654-108">Aktualisieren eines MED-V-Images mithilfe eines Unternehmens Software Verteilungssystems</span><span class="sxs-lookup"><span data-stu-id="8a654-108">How to Update a MED-V Image Using an Enterprise Software Distribution System</span></span>


**<span data-ttu-id="8a654-109">So aktualisieren Sie ein MED-V-Abbild mithilfe eines Enterprise-Softwareverteilungssystems</span><span class="sxs-lookup"><span data-stu-id="8a654-109">To update a MED-V image using an enterprise software distribution system</span></span>**

-   <span data-ttu-id="8a654-110">Lesen Sie die Dokumentation des Systems, das Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a654-110">Refer to the documentation of the system you are using.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a><span data-ttu-id="8a654-111">Aktualisieren eines MED-V-Bilds mit dem Web-Download</span><span class="sxs-lookup"><span data-stu-id="8a654-111">How to Update a MED-V Image Using Web Download</span></span>


**<span data-ttu-id="8a654-112">So aktualisieren Sie ein MED-V-Bild mit dem Web-Download</span><span class="sxs-lookup"><span data-stu-id="8a654-112">To update a MED-V image using Web download</span></span>**

1.  <span data-ttu-id="8a654-113">Stellen Sie in der Med-v-Verwaltung auf der Registerkarte **virtueller Computer** sicher, dass die folgenden Einstellungen auf die Med-v-Arbeitsbereichs Richtlinien angewendet werden, die mit dem zu aktualisierenden Med-v-Bild verknüpft sind:</span><span class="sxs-lookup"><span data-stu-id="8a654-113">In MED-V management, on the **Virtual Machine** tab, ensure that the following settings are applied to the MED-V workspace policies that are associated with the MED-V image being updated:</span></span>

    -   <span data-ttu-id="8a654-114">Das Kontrollkästchen **Update vorschlagen, wenn eine neue Version verfügbar ist** , ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a654-114">The **Suggest update when a new version is available** check box is selected.</span></span>

    -   <span data-ttu-id="8a654-115">Optional können die Clients das Kontrollkästchen **beim Herunterladen von Bildern für diesen Arbeitsbereich auf die Option "Übertragung kürzen" verwenden** .</span><span class="sxs-lookup"><span data-stu-id="8a654-115">Optionally, the **Clients should use Trim Transfer when downloading images for this Workspace** check box is selected.</span></span>

    <span data-ttu-id="8a654-116">Weitere Informationen finden Sie unter [Anwenden von Einstellungen für virtuelle Computer auf einen MED-V-Arbeitsbereich](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="8a654-116">For more information, see [How to Apply Virtual Machine Settings to a MED-V Workspace](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span></span>

2.  <span data-ttu-id="8a654-117">Laden Sie das Image-Update auf den Image Web Distribution-Server hoch.</span><span class="sxs-lookup"><span data-stu-id="8a654-117">Upload the image update to the image Web distribution server.</span></span>

    <span data-ttu-id="8a654-118">Alle Clients mit Bildern, die aktualisiert werden müssen, laden das Update automatisch herunter und wenden es auf das Bild an.</span><span class="sxs-lookup"><span data-stu-id="8a654-118">All clients with images that need to be updated automatically download the update and apply it to the image.</span></span>

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a><span data-ttu-id="8a654-119">Aktualisieren eines MED-V-Basis Bilds</span><span class="sxs-lookup"><span data-stu-id="8a654-119">How to Update a MED-V Base Image</span></span>


**<span data-ttu-id="8a654-120">So aktualisieren Sie ein MED-V-Basis Bild</span><span class="sxs-lookup"><span data-stu-id="8a654-120">To update a MED-V base image</span></span>**

1.  <span data-ttu-id="8a654-121">Öffnen Sie das vorhandene Bild in Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="8a654-121">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="8a654-122">Nehmen Sie die erforderlichen Änderungen am Bild vor, und aktualisieren Sie das Bild (beispielsweise die Installation neuer Software).</span><span class="sxs-lookup"><span data-stu-id="8a654-122">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="8a654-123">Schließen Sie den virtuellen PC2007.</span><span class="sxs-lookup"><span data-stu-id="8a654-123">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="8a654-124">Testen Sie das Bild.</span><span class="sxs-lookup"><span data-stu-id="8a654-124">Test the image.</span></span>

5.  <span data-ttu-id="8a654-125">Nachdem das Bild getestet wurde, packen Sie es mit dem gleichen Namen wie das vorhandene Bild in das lokale Repository ein.</span><span class="sxs-lookup"><span data-stu-id="8a654-125">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="8a654-126">**Hinweis**  Wenn Sie dem Bild einen anderen Namen als die vorhandene Version geben, wird anstelle einer neuen Version des vorhandenen Bilds ein neues Bild erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a654-126">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="8a654-127">Laden Sie die neue Version auf den Server hoch, schieben Sie Sie in den Ordner "Pre-stage" des Bilds, oder verteilen Sie Sie über ein Bereitstellungspaket.</span><span class="sxs-lookup"><span data-stu-id="8a654-127">Upload the new version to the server, push it to the image pre-stage folder, or distribute it via a deployment package.</span></span>

## <span data-ttu-id="8a654-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8a654-128">Related topics</span></span>


[<span data-ttu-id="8a654-129">Erstellen eines MED-V-Images</span><span class="sxs-lookup"><span data-stu-id="8a654-129">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="8a654-130">So aktualisieren Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="8a654-130">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)

[<span data-ttu-id="8a654-131">Konfigurieren von MED-V-Arbeitsbereichsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="8a654-131">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="8a654-132">So konfigurieren Sie den Image-Web-Verteilungsserver</span><span class="sxs-lookup"><span data-stu-id="8a654-132">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





