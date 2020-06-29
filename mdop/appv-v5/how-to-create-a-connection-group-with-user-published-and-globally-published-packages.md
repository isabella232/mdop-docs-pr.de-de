---
title: So erstellen Sie eine Verbindungsgruppe mit von Benutzern und global veröffentlichten Paketen
description: So erstellen Sie eine Verbindungsgruppe mit von Benutzern und global veröffentlichten Paketen
author: dansimp
ms.assetid: 82f7ea7f-7b14-4506-8940-fdcd6c3e117f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: c98981180133881909db17d19cb42771f94bd66a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805663"
---
# <span data-ttu-id="a7730-103">So erstellen Sie eine Verbindungsgruppe mit von Benutzern und global veröffentlichten Paketen</span><span class="sxs-lookup"><span data-stu-id="a7730-103">How to Create a Connection Group with User-Published and Globally Published Packages</span></span>
<span data-ttu-id="a7730-104">Mit einer der folgenden Methoden können Sie Benutzer berechtigte Verbindungsgruppen erstellen, die sowohl von Benutzern veröffentlichte als auch Global veröffentlichte Pakete enthalten:</span><span class="sxs-lookup"><span data-stu-id="a7730-104">You can create user-entitled connection groups that contain both user-published and globally published packages, using either of the following methods:</span></span>

-   [<span data-ttu-id="a7730-105">Verwenden von PowerShell-Cmdlets zum Erstellen der Benutzer berechtigten Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="a7730-105">How to use PowerShell cmdlets to create the user-entitled connection groups</span></span>](#bkmk-posh-userentitled-cg)

-   [<span data-ttu-id="a7730-106">Verwenden des App-V-Servers zum Erstellen der Benutzer berechtigten Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="a7730-106">How to use the App-V Server to create the user-entitled connection groups</span></span>](#bkmk-appvserver-userentitled-cg)

**<span data-ttu-id="a7730-107">Was Sie wissen sollten, bevor Sie beginnen:</span><span class="sxs-lookup"><span data-stu-id="a7730-107">What to know before you start:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7730-108">Nicht unterstützte Szenarien und potenzielle Probleme</span><span class="sxs-lookup"><span data-stu-id="a7730-108">Unsupported scenarios and potential issues</span></span></th>
<th align="left"><span data-ttu-id="a7730-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="a7730-109">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7730-110">Sie können keine von Benutzern veröffentlichten Pakete in Global berechtigte Verbindungsgruppen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="a7730-110">You cannot include user-published packages in globally entitled connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7730-111">Bei der Verbindungsgruppe tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a7730-111">The connection group will fail.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7730-112">Wenn Sie ein Paket auf globaler Ebene veröffentlichen und dann eine von Benutzern veröffentlichte Verbindungsgruppe erstellen, in der Sie dieses Paket nicht optional erstellt haben, können Sie weiterhin <strong> die Veröffentlichung von "Publish-AppvClientPackage &lt; Package-Global" ausführen, &gt; </strong> um die Veröffentlichung des Pakets aufzuheben, auch wenn dieses Paket in einer anderen Verbindungsgruppe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a7730-112">If you publish a package globally and then create a user-published connection group in which you’ve made that package non-optional, you can still run <strong>Unpublish-AppvClientPackage &lt;package&gt; -global</strong> to unpublish the package, even when that package is being used in another connection group.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7730-113">Wenn das Paket von anderen Verbindungsgruppen verwendet wird, schlägt das Paket in diesen Verbindungsgruppen fehl.</span><span class="sxs-lookup"><span data-stu-id="a7730-113">If any other connection groups are using that package, the package will fail in those connection groups.</span></span></p>
<p><span data-ttu-id="a7730-114">Um die Veröffentlichung eines nicht optionalen Pakets, das in einer anderen Verbindungsgruppe verwendet wird, unbeabsichtigt zu verhindern, empfehlen wir, dass Sie die Verbindungsgruppen nachvollziehen, in denen Sie ein nicht optionales Paket verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="a7730-114">To avoid inadvertently unpublishing a non-optional package that is being used in another connection group, we recommend that you track the connection groups in which you’ve used a non-optional package.</span></span></p></td>
</tr>
</tbody>
</table>

 
<a href="" id="bkmk-posh-userentitled-cg"></a>**<span data-ttu-id="a7730-115">Verwenden von PowerShell-Cmdlets zum Erstellen von Benutzer berechtigten Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="a7730-115">How to use PowerShell cmdlets to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="a7730-116">Verwenden Sie die folgenden Befehle, um Pakete hinzuzufügen und zu veröffentlichen:</span><span class="sxs-lookup"><span data-stu-id="a7730-116">Add and publish packages by using the following commands:</span></span>

    **<span data-ttu-id="a7730-117">Add-AppvClientPackage package1 \ _AppV \ _File \ _Path</span><span class="sxs-lookup"><span data-stu-id="a7730-117">Add-AppvClientPackage Package1\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="a7730-118">Add-AppvClientPackage Package2 \ _AppV \ _File \ _Path</span><span class="sxs-lookup"><span data-stu-id="a7730-118">Add-AppvClientPackage Package2\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="a7730-119">Publish-AppvClientPackage-Package-package1 \ _ID-Version package1 \ _Version ID – Global</span><span class="sxs-lookup"><span data-stu-id="a7730-119">Publish-AppvClientPackage -PackageId Package1\_ID-VersionId Package1\_Version ID -Global</span></span>**

    **<span data-ttu-id="a7730-120">Publish-AppvClientPackage-Package-Package2 \ _ID-VersionIdPackage2 \ _ID</span><span class="sxs-lookup"><span data-stu-id="a7730-120">Publish-AppvClientPackage -PackageId Package2\_ID -VersionIdPackage2\_ID</span></span>**

2.  <span data-ttu-id="a7730-121">Erstellen Sie die XML-Datei der Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a7730-121">Create the connection group XML file.</span></span> <span data-ttu-id="a7730-122">Weitere Informationen finden Sie unter [Informationen zur Verbindungsgruppen Datei](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="a7730-122">For more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

3.  <span data-ttu-id="a7730-123">Fügen Sie die Verbindungsgruppe mithilfe der folgenden Befehle hinzu, und veröffentlichen Sie Sie:</span><span class="sxs-lookup"><span data-stu-id="a7730-123">Add and publish the connection group by using the following commands:</span></span>

    **<span data-ttu-id="a7730-124">Add-AppvClientConnectionGroup Connection \ _Group \ _XML \ _File \ _Path</span><span class="sxs-lookup"><span data-stu-id="a7730-124">Add-AppvClientConnectionGroup Connection\_Group\_XML\_file\_Path</span></span>**

    **<span data-ttu-id="a7730-125">Aktivieren-AppvClientConnectionGroup-Gruppen-CG \ _Group \ _ID-Version-Nr CG \ _Version \ _ID</span><span class="sxs-lookup"><span data-stu-id="a7730-125">Enable-AppvClientConnectionGroup -GroupId CG\_Group\_ID-VersionId CG\_Version\_ID</span></span>**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**<span data-ttu-id="a7730-126">Verwenden des App-V-Servers zum Erstellen von Benutzer berechtigten Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="a7730-126">How to use the App-V Server to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="a7730-127">Öffnen Sie die App-V 5,0-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="a7730-127">Open the App-V 5.0 Management Console.</span></span>

2.  <span data-ttu-id="a7730-128">Befolgen Sie die Anweisungen unter [Veröffentlichen eines Pakets mithilfe der Verwaltungskonsole](how-to-publish-a-package-by-using-the-management-console-50.md) , um Pakete Global und für den Benutzer zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a7730-128">Follow the instructions in [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md) to publish packages globally and to the user.</span></span>

3.  <span data-ttu-id="a7730-129">Befolgen Sie die Anweisungen unter [Erstellen einer Verbindungsgruppe](how-to-create-a-connection-group.md) , um die Verbindungsgruppe zu erstellen, und fügen Sie die von Benutzern veröffentlichten und Global veröffentlichten Pakete hinzu.</span><span class="sxs-lookup"><span data-stu-id="a7730-129">Follow the instructions in [How to Create a Connection Group](how-to-create-a-connection-group.md) to create the connection group, and add the user-published and globally published packages.</span></span>

    <span data-ttu-id="a7730-130">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="a7730-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a7730-131">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="a7730-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a7730-132">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="a7730-132">Got an App-V issue?</span></span>** <span data-ttu-id="a7730-133">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a7730-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a7730-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a7730-134">Related topics</span></span>


[<span data-ttu-id="a7730-135">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="a7730-135">Managing Connection Groups</span></span>](managing-connection-groups.md)

[<span data-ttu-id="a7730-136">So verwenden Sie optionale Pakete in Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="a7730-136">How to Use Optional Packages in Connection Groups</span></span>](how-to-use-optional-packages-in-connection-groups.md)

 

 





