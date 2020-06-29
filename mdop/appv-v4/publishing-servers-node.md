---
title: Knoten „Veröffentlichungsserver“
description: Knoten „Veröffentlichungsserver“
author: dansimp
ms.assetid: b5823c6c-15bc-4e8d-aeeb-acc366ffedd1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c001e246c63919773d29a2317d5a43937c0813f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806451"
---
# <span data-ttu-id="c1485-103">Knoten „Veröffentlichungsserver“</span><span class="sxs-lookup"><span data-stu-id="c1485-103">Publishing Servers Node</span></span>


<span data-ttu-id="c1485-104">Der Knoten **Publishing Servers** befindet sich eine Ebene unterhalb des Knotens **Application Virtualization** im **Bereich** Bereich der Application Virtualization Client-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="c1485-104">The **Publishing Servers** node is one level below the **Application Virtualization** node in the **Scope** pane of the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="c1485-105">Wenn Sie diesen Knoten auswählen, wird im **Ergebnis** Bereich eine Liste der Veröffentlichungsserver angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1485-105">When you select this node, the **Results** pane displays a list of publishing servers.</span></span>

<span data-ttu-id="c1485-106">Klicken Sie mit der rechten Maustaste auf den Knoten **Publishing Servers** , um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="c1485-106">Right-click the **Publishing Servers** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-server"></a>**<span data-ttu-id="c1485-107">Neuer Server</span><span class="sxs-lookup"><span data-stu-id="c1485-107">New Server</span></span>**  
<span data-ttu-id="c1485-108">Dieses Menüelement zeigt den Assistenten für neue Server an.</span><span class="sxs-lookup"><span data-stu-id="c1485-108">This menu item displays the New Server Wizard.</span></span> <span data-ttu-id="c1485-109">Dieser Assistent besteht aus zwei Seiten:</span><span class="sxs-lookup"><span data-stu-id="c1485-109">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="c1485-110">Geben Sie einen Serveranzeigenamen und Servertyp ein:</span><span class="sxs-lookup"><span data-stu-id="c1485-110">Enter a server display name and server type:</span></span>

    -   <span data-ttu-id="c1485-111">**Anzeigename**: Geben Sie einen Namen ein, der für den Server angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1485-111">**Display Name**—Enter a name that you want displayed for the server.</span></span> <span data-ttu-id="c1485-112">Dieses Feld ist standardmäßig leer.</span><span class="sxs-lookup"><span data-stu-id="c1485-112">This field is blank by default.</span></span>

    -   <span data-ttu-id="c1485-113">**Typ**– wählen Sie in der Dropdownliste der Servertypen den Servertyp aus.</span><span class="sxs-lookup"><span data-stu-id="c1485-113">**Type**—Choose the server type from the drop-down list of server types.</span></span>

2.  <span data-ttu-id="c1485-114">Geben Sie die Verbindungseinstellungen für den Server an:</span><span class="sxs-lookup"><span data-stu-id="c1485-114">Specify the connection settings for the server:</span></span>

    -   <span data-ttu-id="c1485-115">**Hostname**: Geben Sie den Namen oder die IP-Adresse des Servers ein.</span><span class="sxs-lookup"><span data-stu-id="c1485-115">**Host Name**—Enter the name or IP address for the server.</span></span>

    -   <span data-ttu-id="c1485-116">**Port**: Geben Sie einen numerischen Wert ein, der der Portnummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="c1485-116">**Port**—Enter a numeric value that corresponds to the port number.</span></span> <span data-ttu-id="c1485-117">Der Standardwert ist 554, wenn der Servertyp "Application Virtualization Server" und 80 ist, wenn der Servertyp "Standard-HTTP-Server" lautet.</span><span class="sxs-lookup"><span data-stu-id="c1485-117">The default value is 554 if the server type is "Application Virtualization Server" and 80 if the server type is "Standard HTTP Server."</span></span>

    -   <span data-ttu-id="c1485-118">**Path**: Dieses Feld ist standardmäßig "/" und schreibgeschützt, wenn der Servertyp "Application Virtualization Server" oder "Enhanced Security Application Virtualization Server" lautet.</span><span class="sxs-lookup"><span data-stu-id="c1485-118">**Path**—This field defaults to "/" and is read-only when the server type is "Application Virtualization Server" or “Enhanced Security Application Virtualization Server”.</span></span> <span data-ttu-id="c1485-119">Wenn der Servertyp "Standard-HTTP-Server" oder "Enhanced Security http Server" lautet, kann das Feld **path** ebenfalls bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c1485-119">When the server type is “Standard HTTP Server” or “Enhanced Security HTTP Server”, the **Path** field is also editable.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="c1485-120">Neues Fenster von hier</span><span class="sxs-lookup"><span data-stu-id="c1485-120">New Window from Here</span></span>**  
<span data-ttu-id="c1485-121">Wählen Sie dieses Menüelement aus, um eine neue Verwaltungskonsole mit dem ausgewählten Knoten als Stammknoten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c1485-121">Select this menu item to open a new management console with the selected node as the root node.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="c1485-122">Liste exportieren</span><span class="sxs-lookup"><span data-stu-id="c1485-122">Export List</span></span>**  
<span data-ttu-id="c1485-123">Mit diesem Menüelement können Sie eine tabstoppgetrennte Textdatei erstellen, die den Inhalt des **Ergebnis** Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="c1485-123">You can use this menu item to create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="c1485-124">Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="c1485-124">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="c1485-125">Ansicht</span><span class="sxs-lookup"><span data-stu-id="c1485-125">View</span></span>**  
<span data-ttu-id="c1485-126">In dieser Popupliste mit Menüelementen können Sie die Darstellung und den Inhalt des **Ergebnis** Bereichs ändern.</span><span class="sxs-lookup"><span data-stu-id="c1485-126">This pop-up list of menu items enables you to change the appearance and content of the **Results** pane.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="c1485-127">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c1485-127">Refresh</span></span>**  
<span data-ttu-id="c1485-128">Wählen Sie dieses Element aus, um die Verwaltungskonsole zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c1485-128">Select this item to refresh the management console.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="c1485-129">Hilfe</span><span class="sxs-lookup"><span data-stu-id="c1485-129">Help</span></span>**  
<span data-ttu-id="c1485-130">Dieses Element zeigt das Hilfesystem für die Verwaltungskonsole an.</span><span class="sxs-lookup"><span data-stu-id="c1485-130">This item displays the help system for the management console.</span></span>

## <span data-ttu-id="c1485-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c1485-131">Related topics</span></span>


[<span data-ttu-id="c1485-132">Bereich "Ergebnisse" der Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="c1485-132">Publishing Servers Results Pane</span></span>](publishing-servers-results-pane.md)

[<span data-ttu-id="c1485-133">Spalten des Bereichs "Ergebnisse" der Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="c1485-133">Publishing Servers Results Pane Columns</span></span>](publishing-servers-results-pane-columns.md)

 

 





