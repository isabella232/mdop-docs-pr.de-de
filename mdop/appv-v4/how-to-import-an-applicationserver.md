---
title: So importieren Sie eine Anwendung
description: So importieren Sie eine Anwendung
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807092"
---
# <span data-ttu-id="8785d-103">So importieren Sie eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="8785d-103">How to Import an Application</span></span>


<span data-ttu-id="8785d-104">In der Regel importieren Sie Anwendungen, damit Sie von einem Application Virtualization-Verwaltungs Server für den Datenstrom zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8785d-104">Typically, you import applications to make them available to stream from an Application Virtualization Management Server.</span></span> <span data-ttu-id="8785d-105">Sie können eine Anwendung auch manuell hinzufügen, aber Sie müssen genaue, detaillierte Informationen zur Anwendung angeben.</span><span class="sxs-lookup"><span data-stu-id="8785d-105">You can also add an application manually, but you must provide precise, detailed information about the application to do so.</span></span> <span data-ttu-id="8785d-106">Weitere Informationen finden Sie unter [Manuelles Hinzufügen einer Anwendung](how-to-manually-add-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="8785d-106">For more information, see [How to Manually Add an Application](how-to-manually-add-an-application.md).</span></span>

<span data-ttu-id="8785d-107">**Hinweis**  Damit Sie eine Anwendung importieren können, muss Ihre sequenzierte Datei "Open Software Descriptor (OSD)" oder die zugehörige Sequencer Project-Datei (SPRJ) auf dem Server verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="8785d-107">**Note** To import an application, you must have its sequenced Open Software Descriptor (OSD) file or its Sequencer Project (SPRJ) file available on the server.</span></span>

 

<span data-ttu-id="8785d-108">Wenn Sie eine Anwendung importieren, sollten Sie sicherstellen, dass der Server mit einem Wert im Feld " **Standardinhalts Pfad** " auf der Registerkarte " **Allgemein** " des Dialogfelds " **System Optionen** " konfiguriert ist (barrierefrei durch Klicken mit der rechten Maustaste auf den Knoten **Application Virtualization System** in der App-V Server-Konsole).</span><span class="sxs-lookup"><span data-stu-id="8785d-108">When importing an application, you should make sure the server is configured with a value in the **Default Content Path** field on the **General** tab of the **System Options** dialog (accessible by right-clicking the **Application Virtualization System** node in the App-V Server Console).</span></span> <span data-ttu-id="8785d-109">Der Wert des Standardinhalts Pfads definiert, wo die Anwendungen importiert werden, und während des Importvorgangs wird dieser Wert verwendet, um die in der OSD-Datei für die SFT-Datei definierten Pfade und die Symbol Verknüpfungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8785d-109">The default content path value defines where the applications will be imported, and during the import process, this value is used to modify the paths defined in the OSD file for the SFT file and for the icon shortcuts.</span></span> <span data-ttu-id="8785d-110">In der OSD-Datei wird der Pfad für die SFT-Datei im Eintrag CODEBASE-HREF angegeben, und der Pfad für die Symbole wird im Eintrag Verknüpfungen angegeben.</span><span class="sxs-lookup"><span data-stu-id="8785d-110">In the OSD file, the path for the SFT file is specified in the CODEBASE HREF entry and the path for the icons is specified in the SHORTCUTS entry.</span></span>

<span data-ttu-id="8785d-111">Während des Importvorgangs werden das Protokoll, der Server und, falls vorhanden, der in diesen beiden Pfaden in der OSD-Datei angegebene Port durch den Wert aus dem standardmäßigen Inhaltspfad ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8785d-111">During the import process, the protocol, server, and, if present, port specified in these two paths in the OSD file will be replaced with the value from the default content path.</span></span> <span data-ttu-id="8785d-112">In der folgenden Tabelle finden Sie ein Beispiel dafür, wie der Importpfad betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="8785d-112">The following table provides an example of how the import path will be affected.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8785d-113">Standardinhalts Pfad</span><span class="sxs-lookup"><span data-stu-id="8785d-113">Default Content Path</span></span></th>
<th align="left"><span data-ttu-id="8785d-114">OSD-Datei CodeBase href</span><span class="sxs-lookup"><span data-stu-id="8785d-114">OSD File CODEBASE HREF</span></span></th>
<th align="left"><span data-ttu-id="8785d-115">Resultierender Wert</span><span class="sxs-lookup"><span data-stu-id="8785d-115">Resulting Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8785d-116">\server\content &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="8785d-116">\server\content&lt;/p&gt;</span></span></td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p><span data-ttu-id="8785d-117">\server\content\myFolder\package.sft</span><span class="sxs-lookup"><span data-stu-id="8785d-117">\server\content\myFolder\package.sft</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="8785d-118">So importieren Sie eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="8785d-118">To import an application</span></span>**

1.  <span data-ttu-id="8785d-119">Klicken Sie im linken Bereich mit der rechten Maustaste auf den Knoten **Anwendungen** , und wählen Sie **Anwendungen importieren**aus.</span><span class="sxs-lookup"><span data-stu-id="8785d-119">Right-click the **Applications** node in the left pane, and choose **Import Applications**.</span></span>

2.  <span data-ttu-id="8785d-120">Navigieren Sie im Dialogfeld **Öffnen** zur SPRJ-oder OSD-Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8785d-120">In the **Open** dialog box, navigate to the application's SPRJ or OSD file.</span></span> <span data-ttu-id="8785d-121">Markieren Sie die Datei, und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="8785d-121">Highlight the file and click **Open**.</span></span>

3.  <span data-ttu-id="8785d-122">Stellen Sie sicher, dass im **Assistenten für neue Anwendungen**das Kontrollkästchen **aktiviert** für Anwendungen aktiviert ist, die Sie streamen möchten.</span><span class="sxs-lookup"><span data-stu-id="8785d-122">In the **New Application Wizard**, be sure the **Enabled** box is selected for applications you want to stream.</span></span> <span data-ttu-id="8785d-123">Dort können Sie auch eine Beschreibung eingeben und die Server-und Dateipfade überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8785d-123">There you can also enter a description and verify the server and file paths.</span></span> <span data-ttu-id="8785d-124">Wenn Sie Lizenz-und Servergruppen eingerichtet haben, können Sie auch diese auswählen.</span><span class="sxs-lookup"><span data-stu-id="8785d-124">Also, if you have set up license and server groups, you can select those.</span></span>

4.  <span data-ttu-id="8785d-125">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8785d-125">Click **Next**.</span></span>

5.  <span data-ttu-id="8785d-126">Aktivieren Sie auf dem Bildschirm **veröffentlichte Verknüpfungen** die Kontrollkästchen für die Speicherorte, an denen die Anwendungsverknüpfungen auf den Clientcomputern angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8785d-126">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers.</span></span>

6.  <span data-ttu-id="8785d-127">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8785d-127">Click **Next**.</span></span>

7.  <span data-ttu-id="8785d-128">Auf dem Bildschirm " **Dateizuordnungen** " können Sie dieser Anwendung neue Dateizuordnungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8785d-128">In the **File Associations** screen, you can add new file associations to this application.</span></span> <span data-ttu-id="8785d-129">Klicken Sie dazu auf **Hinzufügen**, geben Sie die Durchwahl (ohne einen vorhergehenden Punkt) ein, geben Sie eine Beschreibung ein, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8785d-129">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

    <span data-ttu-id="8785d-130">**Hinweis**  Mit Sequencer 4,0 sequenzierte Anwendungen füllen das Dialogfeld **Dateizuordnungen** auf, wenn Sie Sie über die Verwaltungskonsole importieren oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="8785d-130">**Note** Applications sequenced with Sequencer 4.0 populate the **File Associations** dialog box when you import or create them through the management console.</span></span> <span data-ttu-id="8785d-131">Anwendungen mit vorherigen Sequenzer-Versions Paketen funktionieren nicht.</span><span class="sxs-lookup"><span data-stu-id="8785d-131">Applications with previous Sequencer version packages do not.</span></span>

     

8.  <span data-ttu-id="8785d-132">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8785d-132">Click **Next**.</span></span>

9.  <span data-ttu-id="8785d-133">Klicken Sie im Bildschirm **Zugriffsberechtigungen** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8785d-133">In the **Access Permissions** screen, click **Add**.</span></span>

10. <span data-ttu-id="8785d-134">Füllen Sie das Dialogfeld **Gruppen auswählen aus** .</span><span class="sxs-lookup"><span data-stu-id="8785d-134">Complete the **Select Groups** dialog box.</span></span> <span data-ttu-id="8785d-135">Wenn Sie fertig sind, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8785d-135">When you finish, click **OK**.</span></span>

11. <span data-ttu-id="8785d-136">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8785d-136">Click **Next**.</span></span>

12. <span data-ttu-id="8785d-137">Auf dem **Zusammenfassungs** Bildschirm können Sie die Importeinstellungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8785d-137">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="8785d-138">Klicken Sie auf **Fertig stellen**, oder klicken Sie auf **zurück** , um den Import zu ändern, oder auf **Abbrechen** , um den Importvorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="8785d-138">Click **Finish**, or click **Back** to change the import or click **Cancel** to cancel the import.</span></span>

## <span data-ttu-id="8785d-139">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8785d-139">Related topics</span></span>


[<span data-ttu-id="8785d-140">So verwalten Sie Anwendungsgruppen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="8785d-140">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="8785d-141">So verwalten Sie Anwendungen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="8785d-141">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="8785d-142">So fügen Sie eine Anwendung manuell hinzu</span><span class="sxs-lookup"><span data-stu-id="8785d-142">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 





