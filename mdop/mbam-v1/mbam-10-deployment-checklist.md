---
title: Prüfliste für die Bereitstellung von MBAM 1.0
description: Prüfliste für die Bereitstellung von MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804301"
---
# <span data-ttu-id="02d9d-103">Prüfliste für die Bereitstellung von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="02d9d-103">MBAM 1.0 Deployment Checklist</span></span>


<span data-ttu-id="02d9d-104">Diese Checkliste dient zur Vereinfachung der Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM).</span><span class="sxs-lookup"><span data-stu-id="02d9d-104">This checklist is designed to facilitate your deployment of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

**<span data-ttu-id="02d9d-105">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="02d9d-105">Note</span></span>**  
<span data-ttu-id="02d9d-106">In dieser Checkliste werden die empfohlenen Schritte sowie eine Liste der Elemente auf höherer Ebene erläutert, die beim Bereitstellen der MBAM-Features berücksichtigt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="02d9d-106">This checklist outlines the recommended steps and provides a high-level list of items to consider when you deploy the MBAM features.</span></span> <span data-ttu-id="02d9d-107">Wir empfehlen, dass Sie diese Checkliste in ein Kalkulationstabellenprogramm kopieren und für Ihre speziellen Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="02d9d-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your specific needs.</span></span>



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
<th align="left"><span data-ttu-id="02d9d-108">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="02d9d-108">Task</span></span></th>
<th align="left"><span data-ttu-id="02d9d-109">Verweise</span><span class="sxs-lookup"><span data-stu-id="02d9d-109">References</span></span></th>
<th align="left"><span data-ttu-id="02d9d-110">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="02d9d-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="02d9d-111">Führen Sie die Planungsphase aus, um die Computing-Umgebung für die MBAM-Bereitstellung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="02d9d-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)"><span data-ttu-id="02d9d-112">Prüfliste für die Planung von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="02d9d-112">MBAM 1.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="02d9d-113">Überprüfen Sie die Informationen zu MBAM-unterstützten Konfigurationen, um sicherzustellen, dass Ihre ausgewählten Client-und Server Computer für die MBAM-Feature-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="02d9d-113">Review the information on MBAM supported configurations to make sure that your selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="02d9d-114">Von MBAM 1.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="02d9d-114">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="02d9d-115">Führen Sie MBAM-Setup aus, um die MBAM-Server Features in der folgenden Reihenfolge bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="02d9d-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="02d9d-116">Wiederherstellungs-und Hardware Datenbank</span><span class="sxs-lookup"><span data-stu-id="02d9d-116">Recovery and Hardware Database</span></span></p></li>
<li><p><span data-ttu-id="02d9d-117">Kompatibilitäts Status-Datenbank</span><span class="sxs-lookup"><span data-stu-id="02d9d-117">Compliance Status Database</span></span></p></li>
<li><p><span data-ttu-id="02d9d-118">Konformitätsprüfung und Berichte</span><span class="sxs-lookup"><span data-stu-id="02d9d-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="02d9d-119">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="02d9d-119">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="02d9d-120">MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="02d9d-120">MBAM Group Policy Template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="02d9d-121">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="02d9d-121">Note</span></span></strong><br/><p><span data-ttu-id="02d9d-122">Verfolgen Sie die Namen der Server, auf denen die einzelnen Features installiert sind.</span><span class="sxs-lookup"><span data-stu-id="02d9d-122">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="02d9d-123">Sie werden diese Informationen während des Installationsvorgangs verwenden.</span><span class="sxs-lookup"><span data-stu-id="02d9d-123">You will use this information throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)"><span data-ttu-id="02d9d-124">Bereitstellen der Serverinfrastruktur von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="02d9d-124">Deploying the MBAM 1.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="02d9d-125">Hinzufügen von Sicherheitsgruppen für Active Directory-Domänendienste, die während der Planungsphase erstellt wurden, zu den entsprechenden lokalen MBAM Server Feature-Administratoren Gruppen auf den entsprechenden Servern.</span><span class="sxs-lookup"><span data-stu-id="02d9d-125">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on the appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="02d9d-126">Planen von MBAM 1,0-Administratorrollen </a> und <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Verwalten von MBAM-Administratorrollen</span><span class="sxs-lookup"><span data-stu-id="02d9d-126">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="02d9d-127">Erstellen und Bereitstellen der erforderlichen MBAM-Gruppenrichtlinienobjekte</span><span class="sxs-lookup"><span data-stu-id="02d9d-127">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="02d9d-128">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="02d9d-128">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="02d9d-129">Bereitstellen der MBAM-Client Software.</span><span class="sxs-lookup"><span data-stu-id="02d9d-129">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="02d9d-130">Bereitstellen des MBAM 1.0-Clients</span><span class="sxs-lookup"><span data-stu-id="02d9d-130">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="02d9d-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="02d9d-131">Related topics</span></span>


[<span data-ttu-id="02d9d-132">Bereitstellen von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="02d9d-132">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)









