---
title: So fügen Sie mithilfe der Verwaltungskonsole Pakete hinzu oder aktualisieren sie
description: So fügen Sie mithilfe der Verwaltungskonsole Pakete hinzu oder aktualisieren sie
author: dansimp
ms.assetid: 4e389d7e-f402-44a7-bc4c-42c2a8440573
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 583ac07168c44c7d0a605b81512ae01a6d979db2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805750"
---
# <span data-ttu-id="2d60d-103">So fügen Sie mithilfe der Verwaltungskonsole Pakete hinzu oder aktualisieren sie</span><span class="sxs-lookup"><span data-stu-id="2d60d-103">How to Add or Upgrade Packages by Using the Management Console</span></span>


<span data-ttu-id="2d60d-104">Sie können das folgende Verfahren zum Hinzufügen oder Aktualisieren eines Pakets zur App-V 5,0-Verwaltungskonsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d60d-104">You can the following procedure to add or upgrade a package to the App-V 5.0 Management Console.</span></span> <span data-ttu-id="2d60d-105">Führen Sie die folgenden Schritte aus, um ein Paket zu aktualisieren, das bereits in der Management Console vorhanden ist, und importieren Sie das aktualisierte Paket mit dem gleichen Paket **Namen**.</span><span class="sxs-lookup"><span data-stu-id="2d60d-105">To upgrade a package that already exists in the Management Console, use the following steps and import the upgraded package using the same package **Name**.</span></span>

**<span data-ttu-id="2d60d-106">So fügen Sie der Verwaltungskonsole ein Paket hinzu</span><span class="sxs-lookup"><span data-stu-id="2d60d-106">To add a package to the Management Console</span></span>**

1.  <span data-ttu-id="2d60d-107">Klicken Sie im Navigationsbereich der Management Console-Anzeige auf die Registerkarte **Pakete** .</span><span class="sxs-lookup"><span data-stu-id="2d60d-107">Click the **Packages** tab in the navigation pane of the Management Console display.</span></span>

    <span data-ttu-id="2d60d-108">Die Konsole zeigt die Liste der Pakete an, die dem Server hinzugefügt wurden, sowie Statusinformationen zu den einzelnen Paketen.</span><span class="sxs-lookup"><span data-stu-id="2d60d-108">The console displays the list of packages that have been added to the server along with status information about each package.</span></span> <span data-ttu-id="2d60d-109">Wenn ein Paket ausgewählt ist, werden im Bereich **Pakete** detaillierte Informationen zu dem Paket angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2d60d-109">When a package is selected, detailed information about the package is displayed in the **PACKAGES** pane.</span></span>

    <span data-ttu-id="2d60d-110">Klicken Sie auf das Dropdown-Listenfeld nicht **gruppiert** , und geben Sie an, wie die Pakete in der Konsole angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d60d-110">Click the **Ungrouped** drop-down list box and specify how the packages are to be displayed in the console.</span></span> <span data-ttu-id="2d60d-111">Sie können auch auf die zugehörige Spaltenüberschrift klicken, um die Pakete zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="2d60d-111">You can also click the associated column header to sort the packages.</span></span>

2.  <span data-ttu-id="2d60d-112">Um das Paket anzugeben, das Sie hinzufügen möchten, klicken Sie auf **Pakete hinzufügen oder aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="2d60d-112">To specify the package you want to add, click **Add or Upgrade Packages**.</span></span>

3.  <span data-ttu-id="2d60d-113">Geben Sie den vollständigen Pfad zu dem Paket ein, das Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="2d60d-113">Type the full path to the package that you want to add.</span></span> <span data-ttu-id="2d60d-114">Verwenden Sie das UNC-oder http-Pfadformat, beispielsweise **\\\\servername\\sharename\\foldername\\packagename.AppV** oder **http://server.1234/file.appv** , und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2d60d-114">Use the UNC or HTTP path format, for example **\\\\servername\\sharename\\foldername\\packagename.appv** or **http://server.1234/file.appv**, and then click **Add**.</span></span>

    <span data-ttu-id="2d60d-115">**Wichtig**  Sie müssen ein Paket mit der Dateinamenerweiterung **AppV** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2d60d-115">**Important** You must select a package with the **.appv** file name extension.</span></span>

     

4.  <span data-ttu-id="2d60d-116">Auf der Seite wird die Statusmeldung " \*\* &lt; Paketname &gt; " hinzugefügt\*\*.</span><span class="sxs-lookup"><span data-stu-id="2d60d-116">The page displays the status message **Adding &lt;Packagename&gt;**.</span></span> <span data-ttu-id="2d60d-117">Klicken Sie auf **Status importieren** , um den Status eines importierten Pakets zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2d60d-117">Click **IMPORT STATUS** to check the status of a package that you have imported.</span></span>

    <span data-ttu-id="2d60d-118">Klicken Sie auf **OK** , um das Paket hinzuzufügen und die Seite **Paket hinzufügen** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="2d60d-118">Click **OK** to add the package and close the **Add Package** page.</span></span> <span data-ttu-id="2d60d-119">Wenn während des Imports ein Fehler aufgetreten ist, klicken Sie auf der Seite **Paketimport** auf **Detail** , um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2d60d-119">If there was an error during the import, click **Detail** on the **Package Import** page for more information.</span></span> <span data-ttu-id="2d60d-120">Das neu hinzugefügte Paket steht jetzt im Bereich **Pakete** zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2d60d-120">The newly added package is now available in the **PACKAGES** pane.</span></span>

5.  <span data-ttu-id="2d60d-121">Klicken Sie auf **Schließen** , um die Seite " **Pakete hinzufügen oder aktualisieren** " zu schließen.</span><span class="sxs-lookup"><span data-stu-id="2d60d-121">Click **Close** to close the **Add or Upgrade Packages** page.</span></span>

    <span data-ttu-id="2d60d-122">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="2d60d-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2d60d-123">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="2d60d-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2d60d-124">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="2d60d-124">Got an App-V issue?</span></span>** <span data-ttu-id="2d60d-125">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2d60d-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2d60d-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2d60d-126">Related topics</span></span>


[<span data-ttu-id="2d60d-127">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2d60d-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





