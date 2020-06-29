---
title: Prüfliste für die Bereitstellung von MBAM 2.0
description: Prüfliste für die Bereitstellung von MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811755"
---
# <span data-ttu-id="c49d8-103">Prüfliste für die Bereitstellung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c49d8-103">MBAM 2.0 Deployment Checklist</span></span>


<span data-ttu-id="c49d8-104">Diese Checkliste kann verwendet werden, um Sie während der Microsoft BitLocker-MBAM-Bereitstellung mit einer eigenständigen Topologie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c49d8-104">This checklist can be used to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="c49d8-105">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="c49d8-105">Note</span></span>**  
<span data-ttu-id="c49d8-106">In dieser Checkliste werden die empfohlenen Schritte und eine Liste der Elemente auf höherer Ebene erläutert, die beim Bereitstellen von Microsoft BitLocker-Verwaltungs-und-Überwachungsfeatures berücksichtigt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="c49d8-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="c49d8-107">Es wird empfohlen, dass Sie diese Checkliste in ein Kalkulationstabellenprogramm kopieren und für ihre Verwendung anpassen.</span><span class="sxs-lookup"><span data-stu-id="c49d8-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="c49d8-108">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c49d8-108">Task</span></span></th>
<th align="left"><span data-ttu-id="c49d8-109">Verweise</span><span class="sxs-lookup"><span data-stu-id="c49d8-109">References</span></span></th>
<th align="left"><span data-ttu-id="c49d8-110">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="c49d8-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c49d8-111">Führen Sie die Planungsphase aus, um die Computing-Umgebung für die MBAM-Bereitstellung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="c49d8-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)"><span data-ttu-id="c49d8-112">Prüfliste für die Planung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c49d8-112">MBAM 2.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c49d8-113">Überprüfen Sie die MBAM unterstützten Konfigurationsinformationen, um sicherzustellen, dass ausgewählte Client-und Server Computer für die MBAM-Feature-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c49d8-113">Review the MBAM supported configurations information to make sure selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="c49d8-114">Von MBAM 2.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="c49d8-114">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c49d8-115">Führen Sie MBAM-Setup aus, um die MBAM-Server Features in der folgenden Reihenfolge bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="c49d8-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="c49d8-116">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="c49d8-116">Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="c49d8-117">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="c49d8-117">Compliance and Audit Database</span></span></p></li>
<li><p><span data-ttu-id="c49d8-118">Konformitätsprüfung und Berichte</span><span class="sxs-lookup"><span data-stu-id="c49d8-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="c49d8-119">Self-Service-Server</span><span class="sxs-lookup"><span data-stu-id="c49d8-119">Self-Service Server</span></span></p></li>
<li><p><span data-ttu-id="c49d8-120">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="c49d8-120">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="c49d8-121">MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="c49d8-121">MBAM Group Policy template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="c49d8-122">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="c49d8-122">Note</span></span></strong><br/><p><span data-ttu-id="c49d8-123">Verfolgen Sie die Namen der Server, auf denen die einzelnen Features installiert sind.</span><span class="sxs-lookup"><span data-stu-id="c49d8-123">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="c49d8-124">Diese Informationen werden während des Installationsvorgangs verwendet.</span><span class="sxs-lookup"><span data-stu-id="c49d8-124">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)"><span data-ttu-id="c49d8-125">Bereitstellen der Serverinfrastruktur von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c49d8-125">Deploying the MBAM 2.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c49d8-126">Hinzufügen von Sicherheitsgruppen für Active Directory-Domänendienste, die während der Planungsphase erstellt wurden, zu den entsprechenden lokalen MBAM Server Feature-Administratoren Gruppen auf den entsprechenden Servern.</span><span class="sxs-lookup"><span data-stu-id="c49d8-126">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="c49d8-127">Planen von MBAM 2,0-Administratorrollen </a> und <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Verwalten von MBAM-Administratorrollen</span><span class="sxs-lookup"><span data-stu-id="c49d8-127">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c49d8-128">Erstellen und Bereitstellen erforderlicher MBAM-Gruppenrichtlinienobjekte</span><span class="sxs-lookup"><span data-stu-id="c49d8-128">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="c49d8-129">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c49d8-129">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c49d8-130">Bereitstellen der MBAM-Client Software.</span><span class="sxs-lookup"><span data-stu-id="c49d8-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="c49d8-131">Bereitstellen des MBAM 2.0-Clients</span><span class="sxs-lookup"><span data-stu-id="c49d8-131">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c49d8-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c49d8-132">Related topics</span></span>


[<span data-ttu-id="c49d8-133">Bereitstellen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c49d8-133">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)









