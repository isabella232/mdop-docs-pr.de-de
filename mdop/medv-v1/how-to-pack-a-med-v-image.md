---
title: So packen Sie ein MED-V-Image
description: So packen Sie ein MED-V-Image
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810699"
---
# <span data-ttu-id="4faab-103">So packen Sie ein MED-V-Image</span><span class="sxs-lookup"><span data-stu-id="4faab-103">How to Pack a MED-V Image</span></span>


<span data-ttu-id="4faab-104">Ein MED-V-Abbild muss gepackt sein, bevor es einem Bereitstellungspaket hinzugefügt oder auf den Server hochgeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4faab-104">A MED-V image must be packed before it can be added to a deployment package or uploaded to the server.</span></span>

**<span data-ttu-id="4faab-105">So erstellen Sie ein komprimiertes MED-V-Bild</span><span class="sxs-lookup"><span data-stu-id="4faab-105">To create a packed MED-V image</span></span>**

1.  <span data-ttu-id="4faab-106">Klicken Sie auf die Schaltfläche " **Bilder** Verwaltung".</span><span class="sxs-lookup"><span data-stu-id="4faab-106">Click the **Images** management button.</span></span>

2.  <span data-ttu-id="4faab-107">Klicken Sie im Modul **Bilder** im Bereich **lokal verpackte Bilder** auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="4faab-107">In the **Images** module, in the **Local Packed Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="4faab-108">Wählen Sie im Dialogfeld **komprimierte Bild Erstellung** das Bild des virtuellen Computers aus, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="4faab-108">In the **Packed Image Creation** dialog box, select the virtual machine image by doing one of the following:</span></span>

    -   <span data-ttu-id="4faab-109">Geben Sie im Feld **Basisbild-Datei** den vollständigen Pfad zu dem Verzeichnis ein, in dem sich das für MED-V vorbereitete Microsoft Virtual PC-Abbild befindet.</span><span class="sxs-lookup"><span data-stu-id="4faab-109">In the **Base image file** field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="4faab-110">Klicken Sie auf **Durchsuchen** , um zu dem Verzeichnis zu navigieren, in dem sich das für MED-V vorbereitete Microsoft Virtual PC-Abbild befindet.</span><span class="sxs-lookup"><span data-stu-id="4faab-110">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="4faab-111">Geben Sie den Namen des neuen Bilds an, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="4faab-111">Specify the name of the new image by doing one of the following:</span></span>

    -   <span data-ttu-id="4faab-112">Geben Sie im Feld **Image Name** den gewünschten Namen ein.</span><span class="sxs-lookup"><span data-stu-id="4faab-112">In the **Image name** field, type the desired name.</span></span>

        **<span data-ttu-id="4faab-113">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4faab-113">Note</span></span>**  
        <span data-ttu-id="4faab-114">Die folgenden Zeichen können im Bildnamen nicht enthalten sein: Leerzeichen " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="4faab-114">The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. <span data-ttu-id="4faab-115">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4faab-115">Click **OK**.</span></span>

   <span data-ttu-id="4faab-116">Auf dem Hostcomputer wird ein neues MED-V-gepacktes Bild mit den Eigenschaften erstellt, die in der folgenden Tabelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4faab-116">A new MED-V packed image is created on your host computer with the properties defined in the following table.</span></span>

**<span data-ttu-id="4faab-117">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4faab-117">Note</span></span>**  
<span data-ttu-id="4faab-118">In den **lokalen gepackten Bildern** und **gepackten Bildern** in den Server Bereichen wird die neueste Version der einzelnen Bilder als übergeordneter Knoten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4faab-118">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="4faab-119">Klicken Sie auf den übergeordneten Knoten, um alle anderen vorhandenen Versionen des Bilds anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4faab-119">Click the parent node to view all other existing versions of the image.</span></span>



**<span data-ttu-id="4faab-120">Eigenschaften für lokal verpackte Bilder</span><span class="sxs-lookup"><span data-stu-id="4faab-120">Local Packed Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4faab-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4faab-121">Property</span></span></th>
<th align="left"><span data-ttu-id="4faab-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4faab-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4faab-123">Name des Bilds</span><span class="sxs-lookup"><span data-stu-id="4faab-123">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="4faab-124">Der Name des gepackten Bilds, wie es beim Erstellen des Bilds durch den Administrator definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4faab-124">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4faab-125">Version</span><span class="sxs-lookup"><span data-stu-id="4faab-125">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="4faab-126">Die Version des angezeigten Bilds.</span><span class="sxs-lookup"><span data-stu-id="4faab-126">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4faab-127">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4faab-127">Note</span></span></strong><br/><p><span data-ttu-id="4faab-128">Alle vorherigen Versionen werden beibehalten, es sei denn, Sie werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4faab-128">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4faab-129">Dateigröße (komprimiert)</span><span class="sxs-lookup"><span data-stu-id="4faab-129">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4faab-130">Die physische komprimierte Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="4faab-130">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4faab-131">Bildgröße (unkomprimiert)</span><span class="sxs-lookup"><span data-stu-id="4faab-131">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4faab-132">Die physikalische unkomprimierte Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="4faab-132">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4faab-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4faab-133">Related topics</span></span>


[<span data-ttu-id="4faab-134">So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="4faab-134">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="4faab-135">Über die Benutzeroberfläche der MED-V-Management-Konsole</span><span class="sxs-lookup"><span data-stu-id="4faab-135">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="4faab-136">Erstellen eines virtuellen PC-Images für MED-V</span><span class="sxs-lookup"><span data-stu-id="4faab-136">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)









