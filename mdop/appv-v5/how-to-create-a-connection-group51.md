---
title: So erstellen Sie eine Verbindungsgruppe
description: So erstellen Sie eine Verbindungsgruppe
author: dansimp
ms.assetid: 221e2eed-7ebb-42e3-b3d6-11c37c0578e6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f20b3e71c7c0b72d66700bbad945860112ffd03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805648"
---
# <span data-ttu-id="acdb5-103">So erstellen Sie eine Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="acdb5-103">How to Create a Connection Group</span></span>


<span data-ttu-id="acdb5-104">Führen Sie die folgenden Schritte aus, um mithilfe der App-V-Verwaltungskonsole eine Verbindungsgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="acdb5-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="acdb5-105">Informationen zum Verwenden von PowerShell zum Erstellen von Verbindungsgruppen finden Sie unter [Verwalten von Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="acdb5-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span></span>

<span data-ttu-id="acdb5-106">Wenn Sie Pakete in einer Verbindungsgruppe platzieren, werden deren Paketstamm Pfade zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="acdb5-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="acdb5-107">Wenn Sie Pakete entfernen, behalten nur die restlichen Pakete den zusammengeführten Stamm bei.</span><span class="sxs-lookup"><span data-stu-id="acdb5-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="acdb5-108">So erstellen Sie eine Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="acdb5-108">To create a connection group</span></span>**

1.  <span data-ttu-id="acdb5-109">Wählen Sie in der App-V 5,1-Verwaltungskonsole **Verbindungsgruppen** aus, um die Bibliothek Verbindungsgruppen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="acdb5-109">In the App-V 5.1 Management Console, select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

2.  <span data-ttu-id="acdb5-110">Wählen Sie **Verbindungsgruppe hinzufügen** aus, um eine neue Verbindungsgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="acdb5-110">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

3.  <span data-ttu-id="acdb5-111">Geben Sie im Bereich **Neue Verbindungsgruppe** eine Beschreibung für die Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="acdb5-111">In the **New Connection Group** pane, type a description for the group.</span></span>

4.  <span data-ttu-id="acdb5-112">Klicken Sie im Bereich **verbundene Pakete** auf **Bearbeiten** , um der Verbindungsgruppe eine neue Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="acdb5-112">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

5.  <span data-ttu-id="acdb5-113">Wählen Sie im Bereich **gesamte Bibliothek der Pakete** die Anwendung aus, die hinzugefügt werden soll, und klicken Sie auf den Pfeil, um die Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="acdb5-113">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="acdb5-114">Um eine Anwendung zu entfernen, wählen Sie die Anwendung aus, die im Bereich **Pakete in** entfernt werden soll, und klicken Sie auf den Pfeil.</span><span class="sxs-lookup"><span data-stu-id="acdb5-114">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="acdb5-115">Verwenden Sie die Pfeile im Bereich " **Pakete** ", um die Priorität für die Anwendungen in ihrer Verbindungsgruppe zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="acdb5-115">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="acdb5-116">**Wichtig**  Standardmäßig werden die Access-Konfigurationen für Active Directory-Domänendienste, die einer bestimmten Anwendung zugeordnet sind, nicht zur Verbindungsgruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="acdb5-116">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="acdb5-117">Wenn Sie die Active Directory-Zugriffskonfiguration übertragen möchten, wählen Sie **Paketzugriff für Gruppen Zugriff hinzufügen**aus, der sich im Bereich **Pakete im** befindet.</span><span class="sxs-lookup"><span data-stu-id="acdb5-117">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

6.  <span data-ttu-id="acdb5-118">Nachdem Sie alle Anwendungen hinzugefügt und Active Directory-Zugriff konfiguriert haben, klicken Sie auf über **nehmen**.</span><span class="sxs-lookup"><span data-stu-id="acdb5-118">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="acdb5-119">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="acdb5-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="acdb5-120">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="acdb5-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="acdb5-121">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="acdb5-121">Got an App-V issue?</span></span>** <span data-ttu-id="acdb5-122">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="acdb5-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="acdb5-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="acdb5-123">Related topics</span></span>


[<span data-ttu-id="acdb5-124">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="acdb5-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="acdb5-125">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="acdb5-125">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





