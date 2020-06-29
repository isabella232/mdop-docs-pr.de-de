---
title: So laden Sie ein MED-V-Bild auf den Server hoch
description: So laden Sie ein MED-V-Bild auf den Server hoch
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811314"
---
# <span data-ttu-id="286de-103">So laden Sie ein MED-V-Bild auf den Server hoch</span><span class="sxs-lookup"><span data-stu-id="286de-103">How to Upload a MED-V Image to the Server</span></span>


<span data-ttu-id="286de-104">Nachdem ein MED-V-Abbild getestet wurde, kann es gepackt und dann auf den Server hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="286de-104">After a MED-V image has been tested, it can be packed and then uploaded to the server.</span></span> <span data-ttu-id="286de-105">Informationen zum Konfigurieren eines Image Web Distribution-Servers finden Sie unter [Konfigurieren des Image Web Distribution-Servers](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="286de-105">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span>

<span data-ttu-id="286de-106">Sobald ein MED-V-Abbild gepackt und auf den Server hochgeladen wurde, kann es mithilfe eines Enterprise-Software Verteilungs Centers an Benutzer verteilt werden, oder es kann von Benutzern mithilfe eines Bereitstellungspakets heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="286de-106">Once a MED-V image is packed and uploaded to the server, it can be distributed to users by using an enterprise software distribution center, or it can be downloaded by users using a deployment package.</span></span> <span data-ttu-id="286de-107">Informationen zur Bereitstellung mithilfe eines Software Verteilungs Centers für Unternehmen finden Sie unter [Bereitstellen eines MED-V-Arbeitsbereichs mithilfe eines Softwareverteilungssystems für Unternehmen](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="286de-107">For information on deployment using an enterprise software distribution center, see [Deploying a MED-V Workspace Using an Enterprise Software Distribution System](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span></span> <span data-ttu-id="286de-108">Informationen zur Bereitstellung mithilfe eines Pakets finden Sie unter [Bereitstellen eines MED-V-Arbeitsbereichs mithilfe eines Bereitstellungspakets](deploying-a-med-v-workspace-using-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="286de-108">For information on deployment using a package, see [Deploying a MED-V Workspace Using a Deployment Package](deploying-a-med-v-workspace-using-a-deployment-package.md).</span></span>

**<span data-ttu-id="286de-109">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="286de-109">Note</span></span>**  
<span data-ttu-id="286de-110">Bevor Sie ein Bild hochladen, stellen Sie sicher, dass in Ihren Browsereinstellungen kein WebProxy definiert ist und dass Windows Update zurzeit nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="286de-110">Before uploading an image, verify that a Web proxy is not defined in your browser settings and that Windows Update is not currently running.</span></span>



**<span data-ttu-id="286de-111">So laden Sie ein MED-V-Abbild auf den Server hoch</span><span class="sxs-lookup"><span data-stu-id="286de-111">To upload a MED-V image to the server</span></span>**

1.  <span data-ttu-id="286de-112">Wählen Sie im Bereich **lokal verpackte Bilder** das erstellte Bild aus.</span><span class="sxs-lookup"><span data-stu-id="286de-112">In the **Local Packed Images** pane, select the image you created.</span></span>

2.  <span data-ttu-id="286de-113">Klicken Sie auf **hochladen**.</span><span class="sxs-lookup"><span data-stu-id="286de-113">Click **Upload**.</span></span>

    <span data-ttu-id="286de-114">Das Bild wird auf den Server hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="286de-114">The image is uploaded to the server.</span></span> <span data-ttu-id="286de-115">Dies kann sehr viel Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="286de-115">This might take a considerable amount of time.</span></span>

    <span data-ttu-id="286de-116">Bilder auf dem Server sind mit den Eigenschaften definiert, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="286de-116">Images on the server are defined with the properties listed in the following table.</span></span>

**<span data-ttu-id="286de-117">Komprimierte Bilder auf Server Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="286de-117">Packed Images on Server Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="286de-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="286de-118">Property</span></span></th>
<th align="left"><span data-ttu-id="286de-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="286de-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="286de-120">Name des Bilds</span><span class="sxs-lookup"><span data-stu-id="286de-120">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="286de-121">Der Name des gepackten Bilds, wie es beim Erstellen des Bilds durch den Administrator definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="286de-121">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="286de-122">Version</span><span class="sxs-lookup"><span data-stu-id="286de-122">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="286de-123">Die Version des angezeigten Bilds.</span><span class="sxs-lookup"><span data-stu-id="286de-123">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="286de-124">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="286de-124">Note</span></span></strong><br/><p><span data-ttu-id="286de-125">Alle vorherigen Versionen werden beibehalten, es sei denn, Sie werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="286de-125">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="286de-126">Dateigröße (komprimiert)</span><span class="sxs-lookup"><span data-stu-id="286de-126">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="286de-127">Die physische komprimierte Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="286de-127">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="286de-128">Bildgröße (unkomprimiert)</span><span class="sxs-lookup"><span data-stu-id="286de-128">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="286de-129">Die physikalische unkomprimierte Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="286de-129">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="286de-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="286de-130">Related topics</span></span>


[<span data-ttu-id="286de-131">So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="286de-131">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="286de-132">Über die Benutzeroberfläche der MED-V-Management-Konsole</span><span class="sxs-lookup"><span data-stu-id="286de-132">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="286de-133">Erstellen eines virtuellen PC-Images für MED-V</span><span class="sxs-lookup"><span data-stu-id="286de-133">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="286de-134">So packen Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="286de-134">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)









