---
title: Suchen und Filtern der GPO-Liste
description: Suchen und Filtern der GPO-Liste
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808236"
---
# <span data-ttu-id="71ffb-103">Suchen und Filtern der GPO-Liste</span><span class="sxs-lookup"><span data-stu-id="71ffb-103">Search and Filter the List of GPOs</span></span>


<span data-ttu-id="71ffb-104">In Advanced Group Policy Management (AGPM) können Sie die Liste der Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) und deren Attribute durchsuchen, um die Liste der angezeigten GPOs zu filtern.</span><span class="sxs-lookup"><span data-stu-id="71ffb-104">In Advanced Group Policy Management (AGPM), you can search the list of Group Policy Objects (GPOs) and their attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="71ffb-105">So können Sie beispielsweise nach GPOs mit einem bestimmten Namen, Zustand oder Kommentar suchen.</span><span class="sxs-lookup"><span data-stu-id="71ffb-105">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="71ffb-106">Sie können auch nach GPOs suchen, die zuletzt von einem bestimmten Gruppenrichtlinienadministrator oder an einem bestimmten Datum geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="71ffb-106">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

## <span data-ttu-id="71ffb-107">Durchführen einer komplexen Suche</span><span class="sxs-lookup"><span data-stu-id="71ffb-107">Performing a complex search</span></span>


<span data-ttu-id="71ffb-108">Sie können eine komplexe Suche mit dem Format GPO- *Attribut 1: Suchzeichenfolge 1 GPO-Attribut 2: Suchzeichenfolge 2 durchführen. Suchzeichenfolgen für alle Spalten*.</span><span class="sxs-lookup"><span data-stu-id="71ffb-108">You can perform a complex search by using the format *GPO attribute 1: search string 1 GPO attribute 2: search string 2…all-column search strings*.</span></span> <span data-ttu-id="71ffb-109">Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="71ffb-109">The search is not case-sensitive.</span></span>

-   <span data-ttu-id="71ffb-110">**GPO-Attribut:** Eine Spaltenüberschrift in der Liste der Gruppenrichtlinienobjekte in AGPM, ausgenommen **Computer Version** oder **Benutzerversion**.</span><span class="sxs-lookup"><span data-stu-id="71ffb-110">**GPO attribute:** Any column heading in the list of GPOs in AGPM other than **Computer Version** or **User Version**.</span></span> <span data-ttu-id="71ffb-111">Zu den GPO-Attributen gehören der Name des Gruppenrichtlinienobjekts, der Status, der Benutzer, der das Gruppenrichtlinienobjekt zuletzt geändert hat, Datum und Uhrzeit, zu dem das GPO zuletzt geändert wurde, Kommentar, GPO-Status und WMI-Filter, die auf das Gruppenrichtlinienobjekt angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="71ffb-111">GPO attributes include the GPO name, state, user who most recently changed the GPO, date and time when the GPO was most recently changed, comment, GPO status, and WMI filter applied to the GPO.</span></span>

-   <span data-ttu-id="71ffb-112">**Suchzeichenfolge:** Text, der in der angegebenen Spalte durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="71ffb-112">**Search string:** Text for which to search in the specified column.</span></span> <span data-ttu-id="71ffb-113">Wenn eine Zeichenfolge Leerzeichen enthält, müssen Sie die Zeichenfolge mit Anführungszeichen einschließen.</span><span class="sxs-lookup"><span data-stu-id="71ffb-113">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

-   <span data-ttu-id="71ffb-114">**Suchzeichenfolgen für alle Spalten:** Text, für den in allen Spalten in der Liste der Gruppenrichtlinienobjekte in AGPM außer der **Computer Version** und der **Benutzerversion**gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="71ffb-114">**All-column search strings:** Text for which to search in all columns in the list of GPOs in AGPM other than **Computer Version** and **User Version**.</span></span> <span data-ttu-id="71ffb-115">Sie können mehrere Zeichenfolgen, die durch Leerzeichengetrennt sind, einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="71ffb-115">You can include multiple strings separated by spaces.</span></span> <span data-ttu-id="71ffb-116">Wenn eine Zeichenfolge Leerzeichen enthält, müssen Sie die Zeichenfolge mit Anführungszeichen einschließen.</span><span class="sxs-lookup"><span data-stu-id="71ffb-116">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

<span data-ttu-id="71ffb-117">Jedes GPO-Attribut und jedes Suchzeichenfolgen-paar sowie jede Suchzeichenfolge für alle Spalten werden mithilfe eines logischen und-Vorgangs kombiniert.</span><span class="sxs-lookup"><span data-stu-id="71ffb-117">Each GPO attribute and search string pair and each all-column search string are combined by using a logical AND operation.</span></span> <span data-ttu-id="71ffb-118">Das Ergebnis ist eine Liste aller GPOs, für die jedes angegebene Attribut die angegebene Suchzeichenfolge enthält und für die alle Spalten-Suchzeichenfolgen in mindestens einer Spalte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="71ffb-118">The result is a list of all GPOs for which each specified attribute includes the specified search string and for which any all-column search strings appear in at least one column.</span></span> <span data-ttu-id="71ffb-119">Die Suche gibt alle partiellen Übereinstimmungen für Zeichenfolgen zurück, sodass Sie einen Teil eines GPO-namens oder Benutzernamens eingeben und eine Liste aller GPOs anzeigen können, die diesen Text in seinem Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="71ffb-119">The search returns any partial matches for strings so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="71ffb-120">Im folgenden finden Sie Beispiele für Suchvorgänge:</span><span class="sxs-lookup"><span data-stu-id="71ffb-120">The following are examples of searches:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="71ffb-121">Beschreibung des Suchergebnisses</span><span class="sxs-lookup"><span data-stu-id="71ffb-121">Description of search result</span></span></th>
<th align="left"><span data-ttu-id="71ffb-122">Suchabfrage</span><span class="sxs-lookup"><span data-stu-id="71ffb-122">Search query</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71ffb-123">Alle GPOs mit Namen, die die Text <strong> Sicherheit </strong> und <strong> Nordamerika enthalten </strong> .</span><span class="sxs-lookup"><span data-stu-id="71ffb-123">All GPOs with names that include the text <strong>security</strong> and <strong>North America</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="71ffb-124">Name: </strong><strong> Sicherheits </strong><strong> Name: </strong> &quot; <strong> Nordamerika</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="71ffb-124">name:</strong><strong>security</strong><strong>name:</strong>&quot;<strong>North America</strong>&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71ffb-125">Alle ausgecheckten GPOs.</span><span class="sxs-lookup"><span data-stu-id="71ffb-125">All checked out GPOs.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="71ffb-126">Status: </strong> &quot; <strong> ausgecheckt</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="71ffb-126">state:</strong>&quot;<strong>checked out</strong>&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71ffb-127">Alle GPOs, die zuletzt vom Benutzer mit dem Namen <strong> Administrator geändert </strong> und zuletzt innerhalb des vorherigen Monats geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="71ffb-127">All GPOs most recently changed by the user named <strong>Administrator</strong> and most recently changed within the previous month.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="71ffb-128">geändert von: </strong><strong> Administrator </strong><strong> Änderungsdatum: </strong><strong> lastmonth</span><span class="sxs-lookup"><span data-stu-id="71ffb-128">changed by:</strong><strong>Administrator</strong><strong>change date:</strong><strong>lastmonth</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71ffb-129">Alle GPOs, in denen die <strong> Word </strong> -Firewall im letzten Kommentar enthalten ist und in der die Word- <strong> Sicherheit </strong> in einer beliebigen Spalte angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="71ffb-129">All GPOs in which the word <strong>firewall</strong> is included in the most recent comment and in which the word <strong>security</strong> appears in any column.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="71ffb-130">Kommentar: </strong><strong> Firewall- </strong><strong> Sicherheit</span><span class="sxs-lookup"><span data-stu-id="71ffb-130">comment:</strong><strong>firewall</strong><strong>security</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71ffb-131">Alle GPOs, deren Status <strong> alle Einstellungen deaktiviert ist </strong> .</span><span class="sxs-lookup"><span data-stu-id="71ffb-131">All GPOs that have a status of <strong>All Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="71ffb-132">GPO-Status: </strong><strong> alle</span><span class="sxs-lookup"><span data-stu-id="71ffb-132">gpo status:</strong><strong>all</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71ffb-133">Alle GPOs, auf die ein WMI-Filter mit dem Namen " <strong> mein WMI-Filter" </strong> angewendet wurde und die den Status der <strong> Benutzerkonfigurationseinstellungen deaktiviert haben </strong> .</span><span class="sxs-lookup"><span data-stu-id="71ffb-133">All GPOs that have a WMI filter named <strong>My WMI Filter</strong> applied and that have a status of <strong>User Configuration Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="71ffb-134">WMI-Filter: </strong> &quot; <strong> mein WMI-Filter- </strong> &quot; <strong> GPO-Status: </strong><strong> Benutzer</span><span class="sxs-lookup"><span data-stu-id="71ffb-134">wmi filter:</strong>&quot;<strong>My WMI Filter</strong>&quot;<strong>gpo status:</strong><strong>user</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="71ffb-135">Angeben von Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="71ffb-135">Specifying dates</span></span>


<span data-ttu-id="71ffb-136">Sie können nach GPOs suchen, die an einem bestimmten Datum, zu einem bestimmten Zeitpunkt oder während einer Zeitspanne geändert wurden, indem Sie dieselben speziellen Begriffe verwenden, die bei der Suche in Windows zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="71ffb-136">You can search for GPOs changed on a specific date, at a specific time, or during a span of time by using the same special terms available when you search in Windows.</span></span> <span data-ttu-id="71ffb-137">Wenn Sie ein bestimmtes Datum oder eine bestimmte Uhrzeit eingeben, müssen Sie das Format verwenden, das in der Spalte **Änderungsdatum** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="71ffb-137">If entering a specific date or time, you must use the format that is used in the **Change Date** column.</span></span> <span data-ttu-id="71ffb-138">Im folgenden finden Sie Beispiele für Suchvorgänge in der Spalte **Änderungsdatum** :</span><span class="sxs-lookup"><span data-stu-id="71ffb-138">The following are examples of searches of the **Change Date** column:</span></span>

-   <span data-ttu-id="71ffb-139">**Änderungsdatum:\*\*\*\*10/10/2009**</span><span class="sxs-lookup"><span data-stu-id="71ffb-139">**change date:\*\*\*\*10/10/2009**</span></span>

-   <span data-ttu-id="71ffb-140">**Änderungsdatum:\*\*\*\*10/10/2009 9:00:00 am**</span><span class="sxs-lookup"><span data-stu-id="71ffb-140">**change date:\*\*\*\*10/10/2009 9:00:00 AM**</span></span>

-   <span data-ttu-id="71ffb-141">**Änderungsdatum:\*\*\*\*thisWeek**</span><span class="sxs-lookup"><span data-stu-id="71ffb-141">**change date:\*\*\*\*thisweek**</span></span>

<span data-ttu-id="71ffb-142">Wenn Sie die Spalte **Änderungsdatum** durchsuchen, können Sie die folgenden speziellen Begriffe verwenden, bei denen die Groß-/Kleinschreibung nicht berücksichtigt wird:</span><span class="sxs-lookup"><span data-stu-id="71ffb-142">You can use the following special terms, which are not case-sensitive, when you search the **Change Date** column:</span></span>

-   **<span data-ttu-id="71ffb-143">Today</span><span class="sxs-lookup"><span data-stu-id="71ffb-143">Today</span></span>**

-   **<span data-ttu-id="71ffb-144">Gestern</span><span class="sxs-lookup"><span data-stu-id="71ffb-144">Yesterday</span></span>**

-   **<span data-ttu-id="71ffb-145">ThisWeek</span><span class="sxs-lookup"><span data-stu-id="71ffb-145">ThisWeek</span></span>**

-   **<span data-ttu-id="71ffb-146">LastWeek</span><span class="sxs-lookup"><span data-stu-id="71ffb-146">LastWeek</span></span>**

-   **<span data-ttu-id="71ffb-147">ThisMonth</span><span class="sxs-lookup"><span data-stu-id="71ffb-147">ThisMonth</span></span>**

-   **<span data-ttu-id="71ffb-148">LastMonth</span><span class="sxs-lookup"><span data-stu-id="71ffb-148">LastMonth</span></span>**

-   **<span data-ttu-id="71ffb-149">TwoMonths</span><span class="sxs-lookup"><span data-stu-id="71ffb-149">TwoMonths</span></span>**

-   **<span data-ttu-id="71ffb-150">ThreeMonths</span><span class="sxs-lookup"><span data-stu-id="71ffb-150">ThreeMonths</span></span>**

-   **<span data-ttu-id="71ffb-151">ThisYear</span><span class="sxs-lookup"><span data-stu-id="71ffb-151">ThisYear</span></span>**

-   **<span data-ttu-id="71ffb-152">Vorjahres</span><span class="sxs-lookup"><span data-stu-id="71ffb-152">LastYear</span></span>**

### <span data-ttu-id="71ffb-153">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="71ffb-153">Additional considerations</span></span>

-   <span data-ttu-id="71ffb-154">Standardmäßig müssen Sie ein Prüfer, ein Bearbeiter, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="71ffb-154">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="71ffb-155">Insbesondere müssen Sie über die Berechtigung **Listeninhalte** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="71ffb-155">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="71ffb-156">Weitere Informationen zu GPOs-Attributen finden Sie unter [Features für Inhalts Registerkarten](contents-tab-features-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="71ffb-156">For more information about GPO attributes, see [Contents Tab Features](contents-tab-features-agpm40.md).</span></span>

### <span data-ttu-id="71ffb-157">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="71ffb-157">Additional references</span></span>

-   [<span data-ttu-id="71ffb-158">Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="71ffb-158">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





