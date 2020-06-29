---
title: So erstellen Sie eine Verbindungsgruppe
description: So erstellen Sie eine Verbindungsgruppe
author: dansimp
ms.assetid: 9d272052-2d28-4e41-989c-89610482a0ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 816fc3b37be056ed54a88c394ef64fa1edaf47ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805654"
---
# <span data-ttu-id="ca4d0-103">So erstellen Sie eine Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="ca4d0-103">How to Create a Connection Group</span></span>


<span data-ttu-id="ca4d0-104">Führen Sie die folgenden Schritte aus, um mithilfe der App-V-Verwaltungskonsole eine Verbindungsgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="ca4d0-105">Informationen zum Verwenden von PowerShell zum Erstellen von Verbindungsgruppen finden Sie unter [Verwalten von Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="ca4d0-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span></span>

<span data-ttu-id="ca4d0-106">Wenn Sie Pakete in einer Verbindungsgruppe platzieren, werden deren Paketstamm Pfade zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="ca4d0-107">Wenn Sie Pakete entfernen, behalten nur die restlichen Pakete den zusammengeführten Stamm bei.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="ca4d0-108">So erstellen Sie eine Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="ca4d0-108">To create a connection group</span></span>**

1.  <span data-ttu-id="ca4d0-109">Wählen Sie in der App-V 5,0-Verwaltungskonsole **Pakete**aus.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-109">In the App-V 5.0 Management Console, select **Packages**.</span></span>

2.  <span data-ttu-id="ca4d0-110">Wählen Sie **Verbindungsgruppen** aus, um die Verbindungsgruppen Bibliothek anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-110">Select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

3.  <span data-ttu-id="ca4d0-111">Wählen Sie **Verbindungsgruppe hinzufügen** aus, um eine neue Verbindungsgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-111">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

4.  <span data-ttu-id="ca4d0-112">Geben Sie im Bereich **Neue Verbindungsgruppe** eine Beschreibung für die Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-112">In the **New Connection Group** pane, type a description for the group.</span></span>

5.  <span data-ttu-id="ca4d0-113">Klicken Sie im Bereich **verbundene Pakete** auf **Bearbeiten** , um der Verbindungsgruppe eine neue Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-113">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

6.  <span data-ttu-id="ca4d0-114">Wählen Sie im Bereich **gesamte Bibliothek der Pakete** die Anwendung aus, die hinzugefügt werden soll, und klicken Sie auf den Pfeil, um die Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-114">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="ca4d0-115">Um eine Anwendung zu entfernen, wählen Sie die Anwendung aus, die im Bereich **Pakete in** entfernt werden soll, und klicken Sie auf den Pfeil.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-115">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="ca4d0-116">Verwenden Sie die Pfeile im Bereich " **Pakete** ", um die Priorität für die Anwendungen in ihrer Verbindungsgruppe zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-116">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="ca4d0-117">**Wichtig**  Standardmäßig werden die Access-Konfigurationen für Active Directory-Domänendienste, die einer bestimmten Anwendung zugeordnet sind, nicht zur Verbindungsgruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-117">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="ca4d0-118">Wenn Sie die Active Directory-Zugriffskonfiguration übertragen möchten, wählen Sie **Paketzugriff für Gruppen Zugriff hinzufügen**aus, der sich im Bereich **Pakete im** befindet.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-118">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

7.  <span data-ttu-id="ca4d0-119">Nachdem Sie alle Anwendungen hinzugefügt und Active Directory-Zugriff konfiguriert haben, klicken Sie auf über **nehmen**.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-119">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="ca4d0-120">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="ca4d0-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ca4d0-121">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="ca4d0-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ca4d0-122">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="ca4d0-122">Got an App-V issue?</span></span>** <span data-ttu-id="ca4d0-123">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ca4d0-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ca4d0-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ca4d0-124">Related topics</span></span>


[<span data-ttu-id="ca4d0-125">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ca4d0-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="ca4d0-126">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="ca4d0-126">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





