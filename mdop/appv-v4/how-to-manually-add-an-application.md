---
title: So fügen Sie eine Anwendung manuell hinzu
description: So fügen Sie eine Anwendung manuell hinzu
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806971"
---
# <span data-ttu-id="067de-103">So fügen Sie eine Anwendung manuell hinzu</span><span class="sxs-lookup"><span data-stu-id="067de-103">How to Manually Add an Application</span></span>


<span data-ttu-id="067de-104">Beim Hinzufügen einer Anwendung zum Application Virtualization Management Server wird empfohlen, Sie zu importieren.</span><span class="sxs-lookup"><span data-stu-id="067de-104">When adding an application to the Application Virtualization Management Server, it is recommended that you import it.</span></span> <span data-ttu-id="067de-105">Sie können eine Anwendung manuell hinzufügen, aber Sie müssen die genauen, detaillierten Informationen über die in diesem Abschnitt aufgerufene Anwendung angeben.</span><span class="sxs-lookup"><span data-stu-id="067de-105">You can add an application manually, but you must provide the precise, detailed information about the application called for in this section.</span></span>

**<span data-ttu-id="067de-106">So fügen Sie eine neue Anwendung manuell hinzu</span><span class="sxs-lookup"><span data-stu-id="067de-106">To manually add a new application</span></span>**

1.  <span data-ttu-id="067de-107">Klicken Sie im linken Bereich mit der rechten Maustaste auf den Knoten **Anwendungen** , und wählen Sie **neue Anwendung**aus.</span><span class="sxs-lookup"><span data-stu-id="067de-107">In the left pane, right-click the **Applications** node and choose **New Application**.</span></span>

2.  <span data-ttu-id="067de-108">Füllen Sie im **Assistenten für neue Anwendungen**das Dialogfeld **Allgemeine Informationen** aus:</span><span class="sxs-lookup"><span data-stu-id="067de-108">In the **New Application Wizard**, complete the **General Information** dialog box:</span></span>

    1.  <span data-ttu-id="067de-109">**Anwendungsname**: Geben Sie den Namen ein, der den Benutzern angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="067de-109">**Application Name**—Type the name you want the users to see.</span></span>

    2.  <span data-ttu-id="067de-110">**Version**– geben Sie die Anwendungsversion ein.</span><span class="sxs-lookup"><span data-stu-id="067de-110">**Version**—Type the application version.</span></span>

    3.  <span data-ttu-id="067de-111">**Aktiviert**– dieses Feld muss ausgewählt sein, um die Anwendung nach der Erstellung zu streamen.</span><span class="sxs-lookup"><span data-stu-id="067de-111">**Enabled**—This box must be selected to stream the application after you create it.</span></span>

    4.  <span data-ttu-id="067de-112">**Beschreibung**: Geben Sie eine optionale Beschreibung für die administrative Verwendung ein.</span><span class="sxs-lookup"><span data-stu-id="067de-112">**Description**—Type an optional description for administrative use.</span></span>

    5.  <span data-ttu-id="067de-113">**OSD-Pfad**: Durchsuchen Sie das Netzwerk zur OSD-Datei (Open Software Descriptor) der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="067de-113">**OSD Path**—Browse the network to the application's Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="067de-114">Diese Datei muss sich in einem freigegebenen Netzwerkordner befinden.</span><span class="sxs-lookup"><span data-stu-id="067de-114">This file must be in a shared network folder.</span></span>

    6.  <span data-ttu-id="067de-115">**Symbolpfad**– navigieren Sie zur ICO-Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="067de-115">**Icon Path**—Browse to the application's ICO file.</span></span>

    7.  <span data-ttu-id="067de-116">**Anwendungslizenzgruppe**– Wenn Sie Lizenzgruppen eingerichtet haben, können Sie die Anwendung einer anderen zuweisen, indem Sie Sie in der Dropdownliste auswählen.</span><span class="sxs-lookup"><span data-stu-id="067de-116">**Application License Group**—If you have set up license groups, you can assign the application to one by selecting it in the pull-down list.</span></span>

    8.  <span data-ttu-id="067de-117">**Servergruppe**: Wenn Sie über mehrere Application Virtualization-Server verfügen, können Sie die Anwendung einer anderen zuweisen, indem Sie Sie in der Dropdownliste auswählen.</span><span class="sxs-lookup"><span data-stu-id="067de-117">**Server Group**—If you have multiple Application Virtualization Servers, you can assign the application to one by selecting it in the pull-down list.</span></span>

3.  <span data-ttu-id="067de-118">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="067de-118">Click **Next**.</span></span>

4.  <span data-ttu-id="067de-119">Wählen Sie im Dialogfeld **Paket auswählen** das zugehörige Paket aus, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="067de-119">In the **Select Package** dialog box, select the related package and click **Next**.</span></span>

5.  <span data-ttu-id="067de-120">Aktivieren Sie auf dem Bildschirm **veröffentlichte Verknüpfungen** die Kontrollkästchen für die Speicherorte, an denen die Anwendungsverknüpfungen auf den Clientcomputern angezeigt werden sollen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="067de-120">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers and click **Next**.</span></span>

6.  <span data-ttu-id="067de-121">Auf dem Bildschirm " **Dateizuordnungen** " können Sie dieser Anwendung neue Typendatei Zuordnungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="067de-121">In the **File Associations** screen, you can add new type file associations to this application.</span></span> <span data-ttu-id="067de-122">Klicken Sie dazu auf **Hinzufügen**, geben Sie die Durchwahl (ohne einen vorhergehenden Punkt) ein, geben Sie eine Beschreibung ein, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="067de-122">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

7.  <span data-ttu-id="067de-123">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="067de-123">Click **Next**.</span></span>

8.  <span data-ttu-id="067de-124">Klicken Sie im Dialogfeld **Zugriffsberechtigungen** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="067de-124">In the **Access Permissions** dialog box, click **Add**.</span></span>

9.  <span data-ttu-id="067de-125">Navigieren Sie im Dialogfeld **Benutzergruppe hinzufügen/bearbeiten** zur Gruppe Benutzer.</span><span class="sxs-lookup"><span data-stu-id="067de-125">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="067de-126">Sie können auch die Domäne und die Gruppe eingeben, indem Sie die Informationen in die entsprechenden Felder eingeben.</span><span class="sxs-lookup"><span data-stu-id="067de-126">You can also enter the domain and group by typing the information in the respective fields.</span></span> <span data-ttu-id="067de-127">Wenn Sie fertig sind, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="067de-127">When you finish, click **OK**.</span></span> <span data-ttu-id="067de-128">Sie können weitere Gruppen mit denselben Seiten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="067de-128">You can add other groups with the same pages.</span></span>

10. <span data-ttu-id="067de-129">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="067de-129">Click **Next**.</span></span>

11. <span data-ttu-id="067de-130">Auf dem **Zusammenfassungs** Bildschirm können Sie die Importeinstellungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="067de-130">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="067de-131">Klicken Sie auf **Fertig stellen** , um die Anwendung hinzuzufügen, klicken Sie auf **zurück** , um die Informationen zu ändern, oder klicken Sie auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="067de-131">Click **Finish** to add the application, click **Back** to change the information, or click **Cancel**.</span></span>

## <span data-ttu-id="067de-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="067de-132">Related topics</span></span>


[<span data-ttu-id="067de-133">So verwalten Sie Anwendungen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="067de-133">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





