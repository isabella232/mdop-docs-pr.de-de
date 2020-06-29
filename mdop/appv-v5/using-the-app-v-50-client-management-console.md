---
title: Verwenden der App-V 5.0 Client Management Console
description: Verwenden der App-V 5.0 Client Management Console
author: dansimp
ms.assetid: 36398307-57dd-40f3-9d4f-b09f44fd37c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8541e5bc59334b9074a3940dad7cdf0114205d4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804844"
---
# <span data-ttu-id="85d23-103">Verwenden der App-V 5.0 Client Management Console</span><span class="sxs-lookup"><span data-stu-id="85d23-103">Using the App-V 5.0 Client Management Console</span></span>


<span data-ttu-id="85d23-104">In diesem Thema finden Sie Informationen dazu, wie Sie den App-V 5,0-Client konfigurieren und verwalten können.</span><span class="sxs-lookup"><span data-stu-id="85d23-104">This topic provides information about how you can configure and manage the App-V 5.0 client.</span></span>

## <span data-ttu-id="85d23-105">Ändern der App-V 5,0-Clientkonfiguration</span><span class="sxs-lookup"><span data-stu-id="85d23-105">Modify App-V 5.0 client configuration</span></span>


<span data-ttu-id="85d23-106">Der App-V 5,0-Client verfügt über zugeordnete Einstellungen, die konfiguriert werden können, um zu bestimmen, wie der Client in Ihrer Umgebung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="85d23-106">The App-V 5.0 client has associated settings that can be configured to determine how the client will run in your environment.</span></span> <span data-ttu-id="85d23-107">Sie können diese Einstellungen auf dem Computer verwalten, auf dem der Client ausgeführt wird, oder mithilfe von PowerShell oder Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="85d23-107">You can manage these settings on the computer that runs the client or by using PowerShell or Group Policy.</span></span> <span data-ttu-id="85d23-108">Weitere Informationen zum Ändern des Clients mithilfe der PowerShell oder der Gruppenrichtlinienkonfiguration finden Sie unter [Ändern der Clientkonfiguration mithilfe von PowerShell](how-to-modify-client-configuration-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="85d23-108">For more information about how to modify the client using PowerShell or Group Policy configuration see, [How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell.md).</span></span>

## <a href="" id="the-app-v-5-0-client-management-console-"></a><span data-ttu-id="85d23-109">Die App-V 5,0-Clientverwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="85d23-109">The App-V 5.0 client management console</span></span>


<span data-ttu-id="85d23-110">Mithilfe der APP-v 5,0-Clientverwaltungskonsole können Sie Informationen zum App-v 5,0-Client abrufen oder bestimmte Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="85d23-110">You can obtain information about the App-V 5.0 client or perform specific tasks by using the App-V 5.0 client management console.</span></span> <span data-ttu-id="85d23-111">Viele der Aufgaben, die Sie in der Clientverwaltungskonsole ausführen können, können Sie auch mithilfe von PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="85d23-111">Many of the tasks that you can perform in the client management console you can also perform by using PowerShell.</span></span> <span data-ttu-id="85d23-112">Die zugehörigen PowerShell-Cmdlets für jede Aktion werden auch in der folgenden Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="85d23-112">The associated PowerShell cmdlets for each action are also displayed in the following table.</span></span> <span data-ttu-id="85d23-113">Weitere Informationen zur Verwendung von PowerShell finden Sie unter [Verwalten von App-V mithilfe von PowerShell](administering-app-v-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="85d23-113">For more information about how to use PowerShell, see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

<span data-ttu-id="85d23-114">Die Clientverwaltungskonsole enthält die folgenden beschriebenen Hauptregisterkarten.</span><span class="sxs-lookup"><span data-stu-id="85d23-114">The client management console contains the following described main tabs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="85d23-115">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="85d23-115">Tab</span></span></th>
<th align="left"><span data-ttu-id="85d23-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85d23-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85d23-117">Übersicht</span><span class="sxs-lookup"><span data-stu-id="85d23-117">Overview</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d23-118">Die <strong> </strong> Registerkarte "Übersicht" enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="85d23-118">The <strong>Overview</strong> tab contains the following elements:</span></span></p>
<ul>
<li><p><span data-ttu-id="85d23-119">Update – verwenden Sie die <strong> Kachel "Aktualisieren" </strong> , um eine virtualisierte Anwendung zu aktualisieren oder ein neues virtualisiertes Paket zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="85d23-119">Update – Use the <strong>Update</strong> tile to refresh a virtualized application or to receive a new virtualized package.</span></span></p>
<p><span data-ttu-id="85d23-120">Die <strong> Letzte Aktualisierung </strong> zeigt die aktuelle Version des virtualisierten Pakets an.</span><span class="sxs-lookup"><span data-stu-id="85d23-120">The <strong>Last Refresh</strong> displays the current version of the virtualized package.</span></span></p></li>
<li><p><span data-ttu-id="85d23-121">Laden Sie alle virtuellen Anwendungen herunter – verwenden Sie die <strong> Download </strong> Kachel, um alle Pakete herunterzuladen, die für den aktuellen Benutzer bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="85d23-121">Download all virtual applications – Use the <strong>Download</strong> tile to download all of the packages provisioned to the current user.</span></span></p>
<p><span data-ttu-id="85d23-122">(Zugehöriges PowerShell-Cmdlet: <strong> Mount-AppvClientPackage </strong> )</span><span class="sxs-lookup"><span data-stu-id="85d23-122">(Associated PowerShell cmdlet: <strong>Mount-AppvClientPackage</strong>)</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="85d23-123">Offline arbeiten – verwenden Sie diese Kachel, um alle automatischen und manuellen Updates für virtuelle Anwendungen zu verbieten.</span><span class="sxs-lookup"><span data-stu-id="85d23-123">Work Offline – Use this tile to disallow all automatic and manual virtual application updates.</span></span></p>
<p><span data-ttu-id="85d23-124">(Zugehöriges PowerShell-Cmdlet: <strong> Satz-AppvPublishServer – UserRefreshEnabled – GlobalRefreshEnabled </strong> )</span><span class="sxs-lookup"><span data-stu-id="85d23-124">(Associated PowerShell cmdlet: <strong>Set-AppvPublishServer –UserRefreshEnabled –GlobalRefreshEnabled</strong>)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85d23-125">Virtuelle apps</span><span class="sxs-lookup"><span data-stu-id="85d23-125">Virtual Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d23-126"><strong> </strong> Auf der Registerkarte Virtuelle apps werden alle Pakete angezeigt, die für den Benutzer veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="85d23-126">The <strong>VIRTUAL APPS</strong> tab displays all of the packages that have been published to the user.</span></span> <span data-ttu-id="85d23-127">Sie können auch auf ein bestimmtes Paket klicken und alle Anwendungen anzeigen, die Teil dieses Pakets sind.</span><span class="sxs-lookup"><span data-stu-id="85d23-127">You can also click a specific package and see all of the applications that are part of that package.</span></span> <span data-ttu-id="85d23-128">Damit werden Informationen zu Paketen angezeigt, die derzeit verwendet werden und wie viele Pakete von jedem Paket auf den Computer heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="85d23-128">This displays information about packages that are currently in use and how much of each package has been downloaded to the computer.</span></span> <span data-ttu-id="85d23-129">Sie können auch Paketdownloads starten und beenden.</span><span class="sxs-lookup"><span data-stu-id="85d23-129">You can also start and stop package downloads.</span></span> <span data-ttu-id="85d23-130">Darüber hinaus können Sie den Benutzerstatus reparieren.</span><span class="sxs-lookup"><span data-stu-id="85d23-130">Additionally, you can repair the user state.</span></span> <span data-ttu-id="85d23-131">Bei einer Reparatur werden alle Benutzerdaten gelöscht, die einem Paket zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="85d23-131">A repair will delete all user data that is associated with a package.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85d23-132">App-Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="85d23-132">App Connection Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d23-133"><strong> </strong> Auf der Registerkarte "App-Verbindungsgruppen" werden alle Verbindungsgruppen angezeigt, die für den aktuellen Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="85d23-133">The <strong>APP CONNECTION GROUPS</strong> tab displays all of the connection groups that are available to the current user.</span></span> <span data-ttu-id="85d23-134">Klicken Sie auf eine bestimmte Verbindungsgruppe, um alle Pakete anzuzeigen, die Teil der ausgewählten Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="85d23-134">Click a specific connection group to see all of the packages that are part of the selected group.</span></span> <span data-ttu-id="85d23-135">Damit werden Informationen zu Verbindungsgruppen angezeigt, die bereits verwendet werden, und der Inhalt der Verbindungsgruppe, die auf den Computer heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="85d23-135">This displays information about connection groups that are already in use and how much of the connection group contents have been downloaded to the computer.</span></span> <span data-ttu-id="85d23-136">Darüber hinaus können Sie Verbindungsgruppen Downloads starten und beenden.</span><span class="sxs-lookup"><span data-stu-id="85d23-136">Additionally, you can start and stop connection group downloads.</span></span> <span data-ttu-id="85d23-137">Sie können diesen Abschnitt verwenden, um eine Reparatur zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="85d23-137">You can use this section to initiate a repair.</span></span> <span data-ttu-id="85d23-138">Bei einer Reparatur wird der gesamte Benutzerstatus entfernt, dem eine Verbindungsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="85d23-138">A repair will remove all of the user state that is associated a connection group.</span></span></p>
<p><span data-ttu-id="85d23-139">(Zugeordnete PowerShell-Cmdlets: Download- <strong> Mount-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="85d23-139">(Associated PowerShell cmdlets: Download - <strong>Mount-AppvClientConnectionGroup</strong>.</span></span> <span data-ttu-id="85d23-140">Reparieren- <strong> AppvClientConnectionGroup </strong> .)</span><span class="sxs-lookup"><span data-stu-id="85d23-140">Repair -<strong>AppvClientConnectionGroup</strong>.)</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

[<span data-ttu-id="85d23-141">So greifen Sie auf die Client-Verwaltungskonsole zu</span><span class="sxs-lookup"><span data-stu-id="85d23-141">How to Access the Client Management Console</span></span>](how-to-access-the-client-management-console.md)

[<span data-ttu-id="85d23-142">So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="85d23-142">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-beta.md)






## <span data-ttu-id="85d23-143">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="85d23-143">Related topics</span></span>


[<span data-ttu-id="85d23-144">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="85d23-144">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





