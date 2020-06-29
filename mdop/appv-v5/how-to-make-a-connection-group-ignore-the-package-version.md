---
title: So stellen Sie sicher, dass eine Verbindungsgruppe die Paketversion ignoriert
description: So stellen Sie sicher, dass eine Verbindungsgruppe die Paketversion ignoriert
author: dansimp
ms.assetid: 6ebc1bff-d190-4f4c-a6da-e09a4cca7874
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b64d1938419aef184c5df667bf71b8157de0450a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805369"
---
# <span data-ttu-id="ecf5f-103">So stellen Sie sicher, dass eine Verbindungsgruppe die Paketversion ignoriert</span><span class="sxs-lookup"><span data-stu-id="ecf5f-103">How to Make a Connection Group Ignore the Package Version</span></span>


<span data-ttu-id="ecf5f-104">Microsoft Application Virtualization (App-V) 5,0 SP3 ermöglicht es Ihnen, eine Verbindungsgruppe so zu konfigurieren, dass Sie eine beliebige Version eines Pakets verwendet, wodurch Paketaktualisierungen vereinfacht und die Anzahl der zu erstellenden Verbindungsgruppen verringert wird.</span><span class="sxs-lookup"><span data-stu-id="ecf5f-104">Microsoft Application Virtualization (App-V) 5.0 SP3 enables you to configure a connection group to use any version of a package, which simplifies package upgrades and reduces the number of connection groups you need to create.</span></span>

<span data-ttu-id="ecf5f-105">Zum Upgrade eines Pakets in früheren Versionen von App-V mussten mehrere Schritte ausgeführt werden, einschließlich der Deaktivierung der Verbindungsgruppe und der Änderung der XML-Definitionsdatei der Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ecf5f-105">To upgrade a package in earlier versions of App-V, you had to perform several steps, including disabling the connection group and modifying the connection group’s XML definition file.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ecf5f-106">Aufgabenbeschreibung mit App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="ecf5f-106">Task description with App-V 5.0 SP3</span></span></th>
<th align="left"><span data-ttu-id="ecf5f-107">Durchführen der Aufgabe mit App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="ecf5f-107">How to perform the task with App-V 5.0 SP3</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ecf5f-108">Sie können eine Verbindungsgruppe so konfigurieren, dass Sie eine beliebige Version eines Pakets akzeptiert, mit der Sie das Paket aktualisieren können, ohne die Verbindungsgruppe deaktivieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ecf5f-108">You can configure a connection group to accept any version of a package, which enables you to upgrade the package without having to disable the connection group.</span></span></p>
<p><strong><span data-ttu-id="ecf5f-109">Funktionsweise des Features:</span><span class="sxs-lookup"><span data-stu-id="ecf5f-109">How the feature works:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="ecf5f-110">Wenn die Verbindungsgruppe Zugriff auf mehrere Versionen eines Pakets hat, wird die neueste Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="ecf5f-110">If the connection group has access to multiple versions of a package, the latest version is used.</span></span></p></li>
<li><p><span data-ttu-id="ecf5f-111">Wenn die Verbindungsgruppe ein optionales Paket enthält, das eine falsche Version aufweist, wird das Paket ignoriert und verhindert, dass die virtuelle Umgebung der Verbindungsgruppe nicht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ecf5f-111">If the connection group contains an optional package that has an incorrect version, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></li>
<li><p><span data-ttu-id="ecf5f-112">Wenn die Verbindungsgruppe ein nicht optionales Paket enthält, das eine falsche Version aufweist, kann die virtuelle Umgebung der Verbindungsgruppe nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ecf5f-112">If the connection group contains a non-optional package that has an incorrect version, the connection group’s virtual environment cannot be created.</span></span></p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ecf5f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="ecf5f-113">Method</span></span></th>
<th align="left"><span data-ttu-id="ecf5f-114">Schritte</span><span class="sxs-lookup"><span data-stu-id="ecf5f-114">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ecf5f-115">App-V Server – Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="ecf5f-115">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="ecf5f-116">Wählen Sie in der Verwaltungskonsole <strong> Pakete für </strong> &gt; <strong> Verbindungsgruppen aus </strong> .</span><span class="sxs-lookup"><span data-stu-id="ecf5f-116">In the Management Console, select <strong>PACKAGES</strong> &gt; <strong>CONNECTION GROUPS</strong>.</span></span></p></li>
<li><p><span data-ttu-id="ecf5f-117">Wählen Sie in der Bibliothek Verbindungsgruppen die richtige Verbindungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="ecf5f-117">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="ecf5f-118">Klicken <strong> Sie </strong> im Bereich verbundene Pakete auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ecf5f-118">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="ecf5f-119">Aktivieren Sie <strong> </strong> das Kontrollkästchen beliebige Version verwenden neben dem Paketnamen, und klicken Sie auf über <strong> nehmen </strong> .</span><span class="sxs-lookup"><span data-stu-id="ecf5f-119">Select <strong>Use Any Version</strong> check box next to the package name, and click <strong>Apply</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="ecf5f-120">Weitere Informationen zum Hinzufügen oder Aktualisieren von Paketen finden Sie unter so wird es <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)"> gemacht: Hinzufügen oder Aktualisieren von Paketen mithilfe der Verwaltungskonsole </a> .</span><span class="sxs-lookup"><span data-stu-id="ecf5f-120">For more about adding or upgrading packages, see <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)">How to Add or Upgrade Packages by Using the Management Console</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ecf5f-121">App-V-Client auf einem eigenständigen Computer</span><span class="sxs-lookup"><span data-stu-id="ecf5f-121">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="ecf5f-122">Erstellen Sie das XML-Dokument der Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ecf5f-122">Create the connection group XML document.</span></span></p></li>
<li><p><span data-ttu-id="ecf5f-123">Um das Paket zu aktualisieren, setzen Sie das <strong> Package </strong> Tag-Attribut <strong> </strong> auf ein Sternchen ( <strong>\*</strong> ).</span><span class="sxs-lookup"><span data-stu-id="ecf5f-123">For the package to be upgraded, set the <strong>Package</strong> tag attribute <strong>VersionID</strong> to an asterisk (<strong>\*</strong>).</span></span></p></li>
<li><p><span data-ttu-id="ecf5f-124">Verwenden Sie das folgende Cmdlet, um die Verbindungsgruppe hinzuzufügen, und fügen Sie den Pfad zum XML-Dokument der Verbindungsgruppe hinzu:</span><span class="sxs-lookup"><span data-stu-id="ecf5f-124">Use the following cmdlet to add the connection group, and include the path to the connection group XML document:</span></span></p>
<p><strong><span data-ttu-id="ecf5f-125">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="ecf5f-125">Add-AppvClientConnectionGroup</span></span></strong></p></li>
<li><p><span data-ttu-id="ecf5f-126">Wenn Sie ein Paket aktualisieren, verwenden Sie die folgenden Cmdlets zum Entfernen des alten Pakets, Hinzufügen des aktualisierten Pakets und Veröffentlichen des aktualisierten Pakets:</span><span class="sxs-lookup"><span data-stu-id="ecf5f-126">When you upgrade a package, use the following cmdlets to remove the old package, add the upgraded package, and publish the upgraded package:</span></span></p>
<ul>
<li><p><span data-ttu-id="ecf5f-127">RemoveAppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="ecf5f-127">RemoveAppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="ecf5f-128">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="ecf5f-128">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="ecf5f-129">Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="ecf5f-129">Publish-AppvClientPackage</span></span></p></li>
</ul></li>
</ol>
<p><span data-ttu-id="ecf5f-130">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="ecf5f-130">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="ecf5f-131">Die XML-Beispieldatei, <strong> Verbindungsgruppen-XML-Datei mit optionalen Paketen </strong> , in diesem Abschnitt: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"> Verwenden optionaler Pakete in Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="ecf5f-131">The example XML file, <strong>Connection group XML file with optional packages</strong>, in this section: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">How to Use Optional Packages in Connection Groups</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="ecf5f-132">So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="ecf5f-132">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="ecf5f-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ecf5f-133">Related topics</span></span>


[<span data-ttu-id="ecf5f-134">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="ecf5f-134">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





