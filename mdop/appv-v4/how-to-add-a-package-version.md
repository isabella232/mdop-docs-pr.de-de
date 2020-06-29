---
title: So fügen Sie ein Paketversion hinzu
description: So fügen Sie ein Paketversion hinzu
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808734"
---
# <span data-ttu-id="8c551-103">So fügen Sie ein Paketversion hinzu</span><span class="sxs-lookup"><span data-stu-id="8c551-103">How to Add a Package Version</span></span>


<span data-ttu-id="8c551-104">Wenn Sie in der Application Virtualization Server Management Console eine Neusequenzierung eines Pakets durchführen, können Sie mit dem folgenden Verfahren die neue Version Ihren Servern für Streaming hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c551-104">In the Application Virtualization Server Management Console, when you resequence a package, you can use the following procedure to add the new version to your servers for streaming.</span></span>

<span data-ttu-id="8c551-105">**Hinweis**  Wenn Sie ein Paket mit einer neuen Version aktualisieren, können Sie die vorhandene Version beibehalten oder löschen und nur die neueste Version belassen.</span><span class="sxs-lookup"><span data-stu-id="8c551-105">**Note** When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="8c551-106">Möglicherweise möchten Sie die alte Version für die Kompatibilität mit älteren Dokumenten beibehalten, oder Sie können die neue Version testen, bevor Sie für alle Benutzer verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="8c551-106">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

 

**<span data-ttu-id="8c551-107">So fügen Sie eine Paketversion hinzu</span><span class="sxs-lookup"><span data-stu-id="8c551-107">To add a package version</span></span>**

1.  <span data-ttu-id="8c551-108">Kopieren Sie die neue SFT-Datei in den Inhaltsordner des Anwendungsservers.</span><span class="sxs-lookup"><span data-stu-id="8c551-108">Copy the new SFT file to the application server's content folder.</span></span> <span data-ttu-id="8c551-109">Wenn die Neusequenzierung keine Änderungen an den Dateien "Open Software Descriptor (OSD)", "Symbol (ICO)" oder "Sequencer Project (SPRJ)" hinzufügt, müssen Sie diese nicht kopieren.</span><span class="sxs-lookup"><span data-stu-id="8c551-109">If resequencing did not add changes to the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="8c551-110">Sie können diese Dateien einbeziehen, wenn Sie möchten, dass alle Dateien das gleiche Datum aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8c551-110">You can include those files if you want all the files to display the same date.</span></span>

2.  <span data-ttu-id="8c551-111">Erweitern Sie im linken Bereich der Application Virtualization Server-Verwaltungskonsole den Knoten **Pakete** .</span><span class="sxs-lookup"><span data-stu-id="8c551-111">In left pane of the Application Virtualization Server Management Console, expand the **Packages** node.</span></span>

3.  <span data-ttu-id="8c551-112">Klicken Sie mit der rechten Maustaste auf das Paket, das Sie aktualisieren möchten, und wählen Sie **Version hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="8c551-112">Right-click the package you want to upgrade, and choose **Add Version**.</span></span>

4.  <span data-ttu-id="8c551-113">Suchen Sie im Dialogfeld **Paket Version hinzufügen** nach, oder geben Sie den Pfadnamen für die neue Anwendungsdatei im Feld **Vollständiger Pfad für Paketdatei** ein.</span><span class="sxs-lookup"><span data-stu-id="8c551-113">In the **Add Package Version** dialog box, browse for or type the path name for the new application file in the **Full path for package file** field.</span></span> <span data-ttu-id="8c551-114">Hierbei muss es sich um eine SFT-Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="8c551-114">This must be an SFT file.</span></span>

5.  <span data-ttu-id="8c551-115">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c551-115">Click **Next**.</span></span>

6.  <span data-ttu-id="8c551-116">Im Dialogfeld " **Zusammenfassung** " wird der Speicherort der Datei angezeigt, und Sie werden aufgefordert, die Datei dort zu kopieren, wenn dies noch nicht geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="8c551-116">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="8c551-117">Klicken Sie auf **Fertig stellen** , nachdem Sie die Informationen überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="8c551-117">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="8c551-118">Die neue Version ist nun fertig und kann gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="8c551-118">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="8c551-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8c551-119">Related topics</span></span>


[<span data-ttu-id="8c551-120">So löschen Sie ein Paket</span><span class="sxs-lookup"><span data-stu-id="8c551-120">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="8c551-121">So verwalten Sie die Pakete in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="8c551-121">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





