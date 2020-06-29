---
title: So aktualisieren Sie ein Paket
description: So aktualisieren Sie ein Paket
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806732"
---
# <span data-ttu-id="1abf8-103">So aktualisieren Sie ein Paket</span><span class="sxs-lookup"><span data-stu-id="1abf8-103">How to Upgrade a Package</span></span>


<span data-ttu-id="1abf8-104">Der Vorgang für ein automatisches Upgrade ist derselbe wie beim Hinzufügen einer Paketversion in der Application Virtualization Server-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="1abf8-104">The process for an automatic upgrade is the same as for adding a package version in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="1abf8-105">Eine automatische Aktualisierung wird durchgeführt, wenn Sie die Anwendung in einem vorhandenen Paket umsequenzieren.</span><span class="sxs-lookup"><span data-stu-id="1abf8-105">An automatic upgrade is performed when you resequence the application in an existing package.</span></span> <span data-ttu-id="1abf8-106">Dann können Sie diese neue Version Ihren Servern für Streaming hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1abf8-106">Then you can add this new version to your servers for streaming.</span></span>

<span data-ttu-id="1abf8-107">Wenn Sie ein Paket mit einer neuen Version aktualisieren, können Sie die vorhandene Version beibehalten oder löschen und nur die neueste Version belassen.</span><span class="sxs-lookup"><span data-stu-id="1abf8-107">When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="1abf8-108">Möglicherweise möchten Sie die alte Version für die Kompatibilität mit älteren Dokumenten beibehalten, oder Sie können die neue Version testen, bevor Sie für alle Benutzer verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="1abf8-108">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

**<span data-ttu-id="1abf8-109">So aktualisieren Sie ein Paket automatisch</span><span class="sxs-lookup"><span data-stu-id="1abf8-109">To upgrade a package automatically</span></span>**

1.  <span data-ttu-id="1abf8-110">Kopieren Sie die neue SFT-Datei in den Content-Ordner von Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="1abf8-110">Copy the new SFT file to the Application Virtualization Server's content folder.</span></span>

    <span data-ttu-id="1abf8-111">**Hinweis**  Wenn die Neusequenzierung keine Features hinzugefügt hat, die die Dateien "Open Software Descriptor (OSD)", "Symbol (ICO)" oder "Sequencer Project (SPRJ)" geändert haben, müssen Sie diese nicht kopieren.</span><span class="sxs-lookup"><span data-stu-id="1abf8-111">**Note** If resequencing did not add features that changed the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="1abf8-112">Sie können diese Dateien einbeziehen, wenn Sie möchten, dass alle diese Dateien das gleiche Datum aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1abf8-112">You can include these files if you want all these files to display the same date.</span></span>

     

2.  <span data-ttu-id="1abf8-113">Erweitern Sie im linken Bereich der Application Virtualization Server-Verwaltungskonsole **Pakete**.</span><span class="sxs-lookup"><span data-stu-id="1abf8-113">In left pane of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

3.  <span data-ttu-id="1abf8-114">Klicken Sie mit der rechten Maustaste auf das Paket, das Sie aktualisieren möchten, und wählen Sie **Version hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="1abf8-114">Right-click the package you want to upgrade, and select **Add Version**.</span></span>

4.  <span data-ttu-id="1abf8-115">Suchen Sie im Dialogfeld **Paket Version hinzufügen** nach, oder geben Sie den vollständigen Pfadnamen für die neue Anwendungsversion in den **vollständigen Pfad für das Feld Datei** ein.</span><span class="sxs-lookup"><span data-stu-id="1abf8-115">In the **Add Package Version** dialog box, browse for or type the full path name for the new application version in the **Full Path for the file** field.</span></span> <span data-ttu-id="1abf8-116">Hierbei muss es sich um eine SFT-Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="1abf8-116">This must be an SFT file.</span></span>

5.  <span data-ttu-id="1abf8-117">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="1abf8-117">Click **Next**.</span></span>

6.  <span data-ttu-id="1abf8-118">Im Dialogfeld " **Zusammenfassung** " wird der Speicherort der Datei angezeigt, und Sie werden aufgefordert, die Datei dort zu kopieren, wenn dies noch nicht geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="1abf8-118">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="1abf8-119">Klicken Sie auf **Fertig stellen** , nachdem Sie die Informationen überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="1abf8-119">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="1abf8-120">Die neue Version ist nun fertig und kann gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="1abf8-120">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="1abf8-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1abf8-121">Related topics</span></span>


[<span data-ttu-id="1abf8-122">So verwalten Sie die Pakete in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="1abf8-122">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





