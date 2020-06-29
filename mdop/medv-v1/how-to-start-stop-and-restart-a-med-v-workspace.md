---
title: So starten, beenden und starten Sie einen MED-V-Arbeitsbereich neu
description: So starten, beenden und starten Sie einen MED-V-Arbeitsbereich neu
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811326"
---
# <span data-ttu-id="07994-103">So starten, beenden und starten Sie einen MED-V-Arbeitsbereich neu</span><span class="sxs-lookup"><span data-stu-id="07994-103">How to Start, Stop, and Restart a MED-V Workspace</span></span>


**<span data-ttu-id="07994-104">So starten Sie einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="07994-104">To start a MED-V workspace</span></span>**

1.  <span data-ttu-id="07994-105">Klicken Sie im Infobereich mit der rechten Maustaste auf das MED-V-Symbol.</span><span class="sxs-lookup"><span data-stu-id="07994-105">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="07994-106">Klicken Sie im Untermenü auf **Arbeitsbereich starten**.</span><span class="sxs-lookup"><span data-stu-id="07994-106">On the submenu, click **Start Workspace**.</span></span>

    -   <span data-ttu-id="07994-107">Wenn mehrere MED-V-Arbeitsbereiche auf dem Computer ausgeführt werden, wird das Fenster **Arbeitsbereichs Auswahl** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07994-107">If there are multiple MED-V workspaces running on the computer, the **Workspace Selection** window appears.</span></span>

        1.  <span data-ttu-id="07994-108">Wählen Sie einen MED-V-Arbeitsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="07994-108">Select a MED-V workspace.</span></span>

        2.  <span data-ttu-id="07994-109">Aktivieren Sie das Kontrollkästchen **ausgewählten Arbeitsbereich ohne Aufforderung starten** , um dieses Fenster beim nächsten Start des Clients zu überspringen und den ausgewählten MED-V-Arbeitsbereich automatisch zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="07994-109">Select the **Start the selected Workspace without asking me** check box to skip this window the next time the client is started and to automatically open the selected MED-V workspace.</span></span>

        3.  <span data-ttu-id="07994-110">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="07994-110">Click **OK**.</span></span>

    <span data-ttu-id="07994-111">Das Fenster **Arbeitsbereichs Authentifizierung starten** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07994-111">The **Start Workspace Authentication** window appears.</span></span>

    -   <span data-ttu-id="07994-112">Wenn auf dem Computer mehrere med-v-Arbeitsbereiche vorhanden sind und Sie sich für die Verwendung eines angegebenen Med-v-Arbeitsbereichs entschieden haben, wird das in der folgenden Abbildung dargestellte Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07994-112">If there are several MED-V workspaces on the computer and you have opted to use a specified MED-V workspace, the window shown in the following figure appears.</span></span>

        ![](images/medv-logon.gif)

    -   <span data-ttu-id="07994-113">Wenn auf dem Computer nur ein MED-V-Arbeitsbereich vorhanden ist, steht die Option "zuletzt verwendeter Arbeitsbereich starten" nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="07994-113">If there is only one MED-V workspace on the computer, the “Start last used Workspace” option is unavailable.</span></span>

3.  <span data-ttu-id="07994-114">Geben Sie die Anmeldeinformationen Ihres Domänenbenutzers ein.</span><span class="sxs-lookup"><span data-stu-id="07994-114">Type in your domain user credentials.</span></span>

    <span data-ttu-id="07994-115">**Hinweis**  Wenn ein MED-V-Arbeitsbereich zum ersten Mal gestartet wird, sollte sich der Benutzername im folgenden Format befinden: &lt; Domänenname- &gt; \\ &lt; Benutzername &gt; .</span><span class="sxs-lookup"><span data-stu-id="07994-115">**Note** The first time a MED-V workspace is started, the user name should be in the following format: &lt;domain name&gt;\\&lt;user name&gt;.</span></span>

     

4.  <span data-ttu-id="07994-116">Wählen Sie **mein Kennwort speichern** aus, um Ihr Kennwort zwischen den Sitzungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="07994-116">Select **Save my password** to save your password between sessions.</span></span>

    <span data-ttu-id="07994-117">**Hinweis**  Um das Feature Kennwort speichern zu aktivieren, muss das EnableSavePassword-Attribut in der ClientSettings.xml Datei auf true festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="07994-117">**Note** To enable the save password feature, the EnableSavePassword attribute must be set to True in the ClientSettings.xml file.</span></span> <span data-ttu-id="07994-118">Die Datei befindet sich im Ordner *Servers\\Configuration Server\\* .</span><span class="sxs-lookup"><span data-stu-id="07994-118">The file can be found in the *Servers\\Configuration Server\\* folder.</span></span>

     

5.  <span data-ttu-id="07994-119">Deaktivieren Sie das Kontrollkästchen **zuletzt verwendeten Arbeitsbereich starten** , um einen anderen MED-V-Arbeitsbereich auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="07994-119">Clear the **Start last used workspace** check box to choose a different MED-V workspace.</span></span>

6.  <span data-ttu-id="07994-120">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="07994-120">Click **OK**.</span></span>

    <span data-ttu-id="07994-121">Je nach Konfiguration des MED-V-Arbeitsbereichs werden mehrere Status Bildschirme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07994-121">Several status screens appear depending on the MED-V workspace configuration.</span></span>

    <span data-ttu-id="07994-122">Der Bildschirm **Startbereich** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07994-122">The **Starting Workspace** screen appears.</span></span>

**<span data-ttu-id="07994-123">So starten Sie einen MED-V-Arbeitsbereich neu</span><span class="sxs-lookup"><span data-stu-id="07994-123">To restart a MED-V workspace</span></span>**

1.  <span data-ttu-id="07994-124">Wenn der Client ausgeführt wird, klicken Sie im Infobereich mit der rechten Maustaste auf das MED-V-Symbol.</span><span class="sxs-lookup"><span data-stu-id="07994-124">When the client is running, in the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="07994-125">Klicken Sie im Untermenü auf **Arbeitsbereich neu starten**.</span><span class="sxs-lookup"><span data-stu-id="07994-125">On the submenu, click **Restart Workspace**.</span></span>

    <span data-ttu-id="07994-126">Der Arbeitsbereich MED-V wird neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="07994-126">The MED-V workspace is restarted.</span></span>

    -   <span data-ttu-id="07994-127">In einem beständigen MED-V-Arbeitsbereich wird der virtuelle Computer heruntergefahren und neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="07994-127">In a persistent MED-V workspace, the virtual machine is shut down and then restarted.</span></span>

    -   <span data-ttu-id="07994-128">In einem revertible MED-V-Arbeitsbereich wird der virtuelle Computer nicht tatsächlich heruntergefahren; Stattdessen wird der ursprüngliche Zustand zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="07994-128">In a revertible MED-V workspace, the virtual machine does not actually shut down; instead, it returns to its original state.</span></span>

**<span data-ttu-id="07994-129">So beenden Sie einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="07994-129">To stop a MED-V workspace</span></span>**

1.  <span data-ttu-id="07994-130">Klicken Sie im Infobereich mit der rechten Maustaste auf das MED-V-Symbol.</span><span class="sxs-lookup"><span data-stu-id="07994-130">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="07994-131">Klicken Sie im Untermenü auf **Arbeitsbereich beenden**.</span><span class="sxs-lookup"><span data-stu-id="07994-131">On the submenu, click **Stop Workspace**.</span></span>

    <span data-ttu-id="07994-132">Der MED-V-Arbeitsbereich wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="07994-132">The MED-V workspace is stopped.</span></span>

## <span data-ttu-id="07994-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="07994-133">Related topics</span></span>


[<span data-ttu-id="07994-134">So starten und beenden Sie den MED-V-Client</span><span class="sxs-lookup"><span data-stu-id="07994-134">How to Start and Exit the MED-V Client</span></span>](how-to-start-and-exit-the-med-v-client.md)

 

 





