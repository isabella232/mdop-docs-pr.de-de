---
title: So erstellen und testen Sie ein MED-V-Image
description: So erstellen und testen Sie ein MED-V-Image
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812118"
---
# <span data-ttu-id="337ab-103">So erstellen und testen Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="337ab-103">How to Create and Test a MED-V Image</span></span>


<span data-ttu-id="337ab-104">Der Med-v-Administrator erstellt ein Med-v-Abbild, damit es hochgeladen, einem Med-v-Arbeitsbereich zugeordnet und dann an den Client über das Web verteilt, zu einem Med-v-Paket hinzugefügt oder über ein Drittanbietersystem auf den Client heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="337ab-104">The MED-V administrator creates a MED-V image so that it can be uploaded, associated with a MED-V workspace, and then distributed to the client over the Web, added to a MED-V package, or downloaded to the client by using a third-party system.</span></span> <span data-ttu-id="337ab-105">Es wird empfohlen, zunächst ein Testbild zu erstellen und es auf dem MED-V-Client zu testen, bevor es bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="337ab-105">It is recommended to first create a test image and test it on MED-V client before deploying it.</span></span>

<span data-ttu-id="337ab-106">Beim Erstellen eines MED-V-Bilds durchläuft es die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="337ab-106">When creating a MED-V image, it goes through the following stages:</span></span>

1.  <span data-ttu-id="337ab-107">**Lokales Test Abbild**– ein grundlegendes Bild, das lokal getestet werden kann.</span><span class="sxs-lookup"><span data-stu-id="337ab-107">**Local test image**—A basic image that can be tested locally.</span></span>

2.  <span data-ttu-id="337ab-108">**Lokal verpacktes Bild**– nachdem das Bild getestet wurde, wird das Bild vor dem Testen gepackt.</span><span class="sxs-lookup"><span data-stu-id="337ab-108">**Local packed image**—After the image is tested, the image is packed as it existed prior to testing.</span></span> <span data-ttu-id="337ab-109">Im gepackten Bild sind keine Änderungen enthalten, die während der Tests vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="337ab-109">No changes made during testing are included in the packed image.</span></span>

3.  <span data-ttu-id="337ab-110">**Gepacktes Bild auf dem Server**– das komprimierte Bild wird auf den Server hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="337ab-110">**Packed image on server**—The packed image is uploaded to the server.</span></span>

## <span data-ttu-id="337ab-111">Erstellen eines MED-V-Test Bilds</span><span class="sxs-lookup"><span data-stu-id="337ab-111">How to Create a MED-V Test Image</span></span>


**<span data-ttu-id="337ab-112">So erstellen Sie ein neues MED-V-Testbild</span><span class="sxs-lookup"><span data-stu-id="337ab-112">To create a new MED-V test image</span></span>**

1.  <span data-ttu-id="337ab-113">Klicken Sie auf die Schaltfläche " **Bilder** Verwaltung".</span><span class="sxs-lookup"><span data-stu-id="337ab-113">Click the **Images** management button.</span></span>

    <span data-ttu-id="337ab-114">Das Modul **Bilder** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="337ab-114">The **Images** module appears.</span></span>

    -   <span data-ttu-id="337ab-115">Das Modul **Bilder** besteht aus den folgenden Bereichen:</span><span class="sxs-lookup"><span data-stu-id="337ab-115">The **Images** module consists of the following panes:</span></span>

        -   <span data-ttu-id="337ab-116">**Lokale Test Bilder**– lokale ungepackte Bilder.</span><span class="sxs-lookup"><span data-stu-id="337ab-116">**Local Test Images**—Local unpacked images.</span></span>

        -   <span data-ttu-id="337ab-117">**Lokal verpackte Bilder**– alle komprimierten Bilder auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="337ab-117">**Local Packed Images**—All packed images on the local computer.</span></span>

        -   <span data-ttu-id="337ab-118">**Komprimierte Bilder auf dem Server**– alle Bilder, die gepackt und auf den Server hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="337ab-118">**Packed Images on Server**—All images that have been packed and uploaded to the server.</span></span>

    -   <span data-ttu-id="337ab-119">In den **lokalen gepackten Bildern** und **gepackten Bildern** in den Server Bereichen wird die neueste Version der einzelnen Bilder als übergeordneter Knoten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="337ab-119">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="337ab-120">Klicken Sie auf den übergeordneten Knoten, um alle anderen vorhandenen Versionen des Bilds anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="337ab-120">Click the parent node to view all other existing versions of the image.</span></span>

2.  <span data-ttu-id="337ab-121">Klicken Sie im Bereich **lokale Test Bilder** auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="337ab-121">In the **Local Test Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="337ab-122">Wählen Sie im Dialogfeld **Bild Erstellung testen** das Bild des virtuellen Computers aus, das Sie als MED-V-Testbild konfigurieren möchten, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="337ab-122">On the **Test Image Creation** dialog box, select the virtual machine image that you want to configure as a MED-V test image by doing one of the following:</span></span>

    -   <span data-ttu-id="337ab-123">Geben Sie im Feld **Basisbild** -Datei den vollständigen Pfad zu dem Verzeichnis ein, in dem sich das für MED-V vorbereitete Microsoft Virtual PC-Abbild befindet.</span><span class="sxs-lookup"><span data-stu-id="337ab-123">In the **Base image** file field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="337ab-124">Klicken Sie auf **Durchsuchen** , um zu dem Verzeichnis zu navigieren, in dem sich das für MED-V vorbereitete Microsoft Virtual PC-Abbild befindet.</span><span class="sxs-lookup"><span data-stu-id="337ab-124">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="337ab-125">Geben Sie im Feld **Image Name** den gewünschten Namen ein, oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="337ab-125">In the **Image name** field, type or select the desired name.</span></span>

    <span data-ttu-id="337ab-126">**Hinweis**  Die folgenden Zeichen können im Bildnamen nicht enthalten sein: Leerzeichen " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="337ab-126">**Note** The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>

     

5.  <span data-ttu-id="337ab-127">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="337ab-127">Click **OK**.</span></span>

    <span data-ttu-id="337ab-128">Auf dem Hostcomputer wird ein neues MED-V-Testbild mit den Eigenschaften erstellt, die in der folgenden Tabelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="337ab-128">A new MED-V test image is created on your host computer with the properties defined in the following table.</span></span>

    <span data-ttu-id="337ab-129">Weitere Informationen zum Konfigurieren des Med-v Workspace-Bilds finden Sie unter [Konfigurieren von Med-v-Arbeitsbereichs Richtlinien](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="337ab-129">For more information about configuring the MED-V workspace image, refer to [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

**<span data-ttu-id="337ab-130">Eigenschaften für lokale Test Bilder</span><span class="sxs-lookup"><span data-stu-id="337ab-130">Local Test Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="337ab-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="337ab-131">Property</span></span></th>
<th align="left"><span data-ttu-id="337ab-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="337ab-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="337ab-133">Name des Bilds</span><span class="sxs-lookup"><span data-stu-id="337ab-133">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="337ab-134">Der Name des Testbilds, wie es beim Erstellen des Bilds durch den Administrator definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="337ab-134">The name of the test image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="337ab-135">Bild Pfad</span><span class="sxs-lookup"><span data-stu-id="337ab-135">Image Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="337ab-136">Der lokale Pfad des Test Bilds.</span><span class="sxs-lookup"><span data-stu-id="337ab-136">The local path of the test image.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="337ab-137">Erstellt</span><span class="sxs-lookup"><span data-stu-id="337ab-137">Created</span></span></p></td>
<td align="left"><p><span data-ttu-id="337ab-138">Das Datum, an dem das Testbild erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="337ab-138">The date the test image was created.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="337ab-139">Testen eines Med-v-Bilds vom Med-v-Client</span><span class="sxs-lookup"><span data-stu-id="337ab-139">How to Test a MED-V Image from the MED-V Client</span></span>


<span data-ttu-id="337ab-140">Nachdem ein MED-V-Testbild erstellt wurde, verwenden Sie das folgende Verfahren, um das Bild lokal zu testen.</span><span class="sxs-lookup"><span data-stu-id="337ab-140">After a MED-V test image is created, use the following procedure to test the image locally.</span></span>

**<span data-ttu-id="337ab-141">So testen Sie ein MED-V-Bild</span><span class="sxs-lookup"><span data-stu-id="337ab-141">To test a MED-V image</span></span>**

1.  <span data-ttu-id="337ab-142">Klicken Sie auf die Schaltfläche **Richtlinien** Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="337ab-142">Click the **Policy** management button.</span></span>

2.  <span data-ttu-id="337ab-143">Weisen Sie im **Richtlinien** Modul das Med-v-Testbild einem Med-v-Arbeitsbereich zu, indem Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="337ab-143">In the **Policy** module, assign the MED-V test image to a MED-V workspace by doing the following:</span></span>

    1.  <span data-ttu-id="337ab-144">Klicken Sie auf die Registerkarte **virtueller Computer** .</span><span class="sxs-lookup"><span data-stu-id="337ab-144">Click the **Virtual Machine** tab.</span></span>

    2.  <span data-ttu-id="337ab-145">Wählen Sie im Feld **zugewiesene Bild** das von Ihnen erstellte MED-V-Testbild aus.</span><span class="sxs-lookup"><span data-stu-id="337ab-145">In the **Assigned Image** field, select the MED-V test image you created.</span></span> <span data-ttu-id="337ab-146">Wenn das Testbild nicht in der Liste aufgeführt ist, klicken Sie auf **Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="337ab-146">If your test image is not in the list, click **Refresh**.</span></span>

    3.  <span data-ttu-id="337ab-147">Klicken Sie auf der Symbolleiste auf **Änderungen speichern**.</span><span class="sxs-lookup"><span data-stu-id="337ab-147">On the toolbar, click **Save changes**.</span></span>

3.  <span data-ttu-id="337ab-148">Konfigurieren Sie alle anderen MED-V Workspace-Einstellungen, die getestet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="337ab-148">Configure any other MED-V workspace settings to be tested.</span></span> <span data-ttu-id="337ab-149">Weitere Informationen finden Sie unter [Konfigurieren von MED-V-Arbeitsbereichs Richtlinien](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="337ab-149">For more information, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

4.  <span data-ttu-id="337ab-150">Starten Sie den MED-V-Client.</span><span class="sxs-lookup"><span data-stu-id="337ab-150">Start MED-V client.</span></span>

5.  <span data-ttu-id="337ab-151">Klicken Sie im Dialogfeld **Test Bestätigung bestätigen** auf **Testbild verwenden**.</span><span class="sxs-lookup"><span data-stu-id="337ab-151">In the **Confirm Running Test** confirmation box, click **Use Test Image**.</span></span>

6.  <span data-ttu-id="337ab-152">Testen Sie das MED-V Workspace-Testbild.</span><span class="sxs-lookup"><span data-stu-id="337ab-152">Test the MED-V workspace test image.</span></span>

    <span data-ttu-id="337ab-153">Informationen zum Starten und Ausführen des Med-v-Clients finden Sie unter [Med-v-Client Vorgänge](med-v-client-operations.md).</span><span class="sxs-lookup"><span data-stu-id="337ab-153">For information about starting and running MED-V client, see [MED-V Client Operations](med-v-client-operations.md).</span></span>

<span data-ttu-id="337ab-154">**Hinweis**  Öffnen Sie beim Testen eines Bilds nicht VPC, und nehmen Sie Änderungen am Bild vor.</span><span class="sxs-lookup"><span data-stu-id="337ab-154">**Note** While testing an image, do not open VPC and make changes to the image.</span></span>

 

<span data-ttu-id="337ab-155">**Hinweis**  Beim Testen eines Bilds werden keine Änderungen zwischen den Sitzungen auf dem Bild gespeichert. Stattdessen werden Sie in einer separaten, temporären Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="337ab-155">**Note** When testing an image, no changes are saved to the image between sessions; instead, they are saved in a separate, temporary file.</span></span> <span data-ttu-id="337ab-156">Dadurch wird sichergestellt, dass das Bild, wenn es in der Produktionsumgebung verpackt und ausgeführt wird, das ursprüngliche, saubere Bild darstellt.</span><span class="sxs-lookup"><span data-stu-id="337ab-156">This is to ensure that when the image is packed and run on the production environment, it is the original, clean image.</span></span>

 

## <span data-ttu-id="337ab-157">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="337ab-157">Related topics</span></span>


[<span data-ttu-id="337ab-158">Erstellen eines virtuellen PC-Images für MED-V</span><span class="sxs-lookup"><span data-stu-id="337ab-158">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="337ab-159">Erstellen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="337ab-159">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="337ab-160">Konfigurieren von MED-V-Arbeitsbereichsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="337ab-160">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="337ab-161">MED-V-Client-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="337ab-161">MED-V Client Operations</span></span>](med-v-client-operations.md)

 

 





