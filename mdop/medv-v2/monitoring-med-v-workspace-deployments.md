---
title: Überwachen von MED-V Workspace-Bereitstellungen
description: Überwachen von MED-V Workspace-Bereitstellungen
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812220"
---
# <span data-ttu-id="1f8ec-103">Überwachen von MED-V Workspace-Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="1f8ec-103">Monitoring MED-V Workspace Deployments</span></span>


<span data-ttu-id="1f8ec-104">Mit dem Überwachungsfeature in Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 können Sie Abfragen für einzelne Med-v-Arbeitsbereiche ausführen, um zu ermitteln, ob das erstmalige Setup im gesamten Unternehmen erfolgreich war, nachdem die Med-v-Arbeitsbereiche bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-104">The monitoring feature in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 lets you run queries on individual MED-V workspaces to determine whether first time setup succeeded throughout your enterprise after the MED-V workspaces are deployed.</span></span> <span data-ttu-id="1f8ec-105">Das Überwachen des Erfolgs der erstmaligen Einrichtung ist wichtig, da sich MED-V erst dann in einem brauchbaren Zustand befindet, wenn die erstmalige Einrichtung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-105">Monitoring the success of first time setup is important because MED-V is not in a usable state until first time setup has been completed successfully.</span></span>

<span data-ttu-id="1f8ec-106">Dieser Abschnitt enthält Informationen und Anleitungen, die Ihnen bei der Überwachung des Erfolgs oder des Fehlers bei der erstmaligen Einrichtung helfen.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-106">This section provides information and instruction to assist you in monitoring the success or failure of first time setup.</span></span>

## <span data-ttu-id="1f8ec-107">So überwachen Sie MED-V-Arbeitsbereichs Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="1f8ec-107">To monitor MED-V workspace deployments</span></span>


<span data-ttu-id="1f8ec-108">Das Überwachungsfeature besteht aus einem gekoppelten in-Process-WMI-Anbieter (Windows Management Instrumentation), den Sie mithilfe der WMI-Abfragesprache Abfragen können, um den Status der erstmaligen Einrichtung für alle Endbenutzer in einem MED-V-Arbeitsbereich zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-108">The monitoring feature consists of a coupled in-process Windows Management Instrumentation (WMI) provider that you can query using WMI Query Language to discover the status of first time setup for all end users on a MED-V workspace.</span></span>

<span data-ttu-id="1f8ec-109">Der WMI-Anbieter wird mithilfe des WMI-Anbieter Erweiterungs Frameworks von Microsoft .NET Framework 3,5 implementiert.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-109">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span> <span data-ttu-id="1f8ec-110">Der WMI-Anbieter wird im Kontext von LocalService ausgeführt und speichert den erstmaligen Setup Status sicher unter \\ProgramData.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-110">The WMI provider executes in the context of LocalService and stores the first time setup state securely under \\ProgramData.</span></span>

<span data-ttu-id="1f8ec-111">Der WMI-Anbieter wird im **root\\microsoft\\medv** -Namespace implementiert und implementiert die Klasse **FTS \ _Status**, die die Methode **SetFtsState**verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-111">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **FTS\_Status**, which exposes the method **SetFtsState**.</span></span> <span data-ttu-id="1f8ec-112">MED-V verwendet **SetFtsState** zum Einrichten des erstmaligen Setup Zustands.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-112">MED-V uses **SetFtsState** to set the first time setup state.</span></span>

<span data-ttu-id="1f8ec-113">Die Klasse enthält die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-113">The class contains the following properties.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1f8ec-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f8ec-114">Property</span></span></th>
<th align="left"><span data-ttu-id="1f8ec-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f8ec-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1f8ec-116">Computer</span><span class="sxs-lookup"><span data-stu-id="1f8ec-116">Machine</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="1f8ec-117">Schreibgeschützte </strong> Eigenschaft, die den Namen des virtuellen Gastcomputers enthält, der beim erstmaligen Einrichten bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-117">Read Only</strong> property that contains the name of the guest virtual machine provisioned by first time setup.</span></span> <span data-ttu-id="1f8ec-118">Dieser Schlüssel enthält den Namen, den der Gast beim erstmaligen Setup-Fehler gehabt hätte.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-118">This key contains the name that the guest would have had on first time setup failure.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1f8ec-119">Statuscode</span><span class="sxs-lookup"><span data-stu-id="1f8ec-119">StatusCode</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="1f8ec-120">Schreibgeschützte </strong> Eigenschaft, die NULL enthält, wenn die erstmalige Einrichtung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-120">Read Only</strong> property that contains zero if first time setup succeeded.</span></span> <span data-ttu-id="1f8ec-121">Jeder andere zurückgegebene Wert entspricht der Ereignis-ID des protokollierten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-121">Any other value returned equals the event ID for the error that is logged.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1f8ec-122">Zeit</span><span class="sxs-lookup"><span data-stu-id="1f8ec-122">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1f8ec-123">Die UTC-Zeit, die das erstmalige Einrichten abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-123">The UTC time that first time setup completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1f8ec-124">Benutzer</span><span class="sxs-lookup"><span data-stu-id="1f8ec-124">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1f8ec-125">Der Benutzer, für den die erstmalige Einrichtung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-125">The user for which first time setup was run.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1f8ec-126">Der folgende Code zeigt die MOF-Datei (Managed Object Format), die die **FTS \ _Status** Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-126">The following code shows the Managed Object Format (MOF) file that defines the **FTS\_Status** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

<span data-ttu-id="1f8ec-127">Da es in erster Linie um die MED-V-Arbeitsbereiche geht, bei denen die erstmalige Einrichtung nicht erfolgreich abgeschlossen wurde, können Sie Ihre Abfrage so schreiben, dass nur die Fehler zurückgegeben werden, die bei der erstmaligen Einrichtung fehlgeschlagen sind, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="1f8ec-127">Because your main concern is most likely those MED-V workspaces for which first time setup was not completed successfully, you can write your query to only return those that failed first time setup, for example:</span></span>

``` syntax
Select * from FTS_Status where StatusCode != 0
```

<span data-ttu-id="1f8ec-128">In diesem Fall gibt das Überwachungsfeature eine Liste der MED-V-Arbeitsbereiche zurück, bei denen die erstmalige Einrichtung fehlgeschlagen ist, die Sie verwenden können, um den Fehler durch geeignete Aktionen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="1f8ec-128">In this case, the monitoring feature returns a list of those MED-V workspaces that failed first time setup, which you can use to take the appropriate actions to resolve the failure.</span></span>

## <span data-ttu-id="1f8ec-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1f8ec-129">Related topics</span></span>


[<span data-ttu-id="1f8ec-130">Überwachen von MED-V-Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="1f8ec-130">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="1f8ec-131">So überprüfen Sie erstmalige Einstellungen für das Setup</span><span class="sxs-lookup"><span data-stu-id="1f8ec-131">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

 

 





