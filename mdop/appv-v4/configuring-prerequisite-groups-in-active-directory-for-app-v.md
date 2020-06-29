---
title: Konfigurieren von erforderlichen Gruppen in Active Directory für App-V
description: Konfigurieren von erforderlichen Gruppen in Active Directory für App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809010"
---
# <span data-ttu-id="1d319-103">Konfigurieren von erforderlichen Gruppen in Active Directory für App-V</span><span class="sxs-lookup"><span data-stu-id="1d319-103">Configuring Prerequisite Groups in Active Directory for App-V</span></span>


<span data-ttu-id="1d319-104">Bevor Sie den Microsoft Application Virtualization (App-V)-Verwaltungs Server installieren, müssen Sie die folgenden Objekte in Active Directory erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d319-104">Before you install the Microsoft Application Virtualization (App-V) Management Server, you must create the following objects in Active Directory.</span></span> <span data-ttu-id="1d319-105">App-V verwendet Active Directory-Gruppen, um den Zugriff auf Anwendungen und administrative Funktionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="1d319-105">App-V uses Active Directory groups to control access to applications and administrative functions.</span></span> <span data-ttu-id="1d319-106">Sie werden diese Gruppen während des Server Installationsvorgangs und beim Veröffentlichen von Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d319-106">You will use these groups during the server installation process and when publishing applications.</span></span>

## <span data-ttu-id="1d319-107">Konfigurieren von erforderlichen Gruppen in Active Directory für Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="1d319-107">Configuring Prerequisite Groups in Active Directory for Application Virtualization</span></span>


<span data-ttu-id="1d319-108">In dieser Tabelle sind die Active Directory-Gruppen aufgeführt, die für die Installation von App-V erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1d319-108">This table lists the Active Directory groups that are required for installing App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1d319-109">Objekt</span><span class="sxs-lookup"><span data-stu-id="1d319-109">Object</span></span></th>
<th align="left"><span data-ttu-id="1d319-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d319-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1d319-111">Organisationseinheit (OU)</span><span class="sxs-lookup"><span data-stu-id="1d319-111">Organizational Unit (OU)</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d319-112">Erstellen Sie eine OU in Active Directory für die speziellen Gruppen, die für App-V erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1d319-112">Create an OU in Active Directory for the specific groups required for App-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1d319-113">App-V-administrative Gruppe</span><span class="sxs-lookup"><span data-stu-id="1d319-113">App-V Administrative Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d319-114">Während der Installation des App-v-Verwaltungsservers müssen Sie eine Active Directory-Gruppe auswählen, die als App-v-Administratorgruppe verwendet werden soll, um den administrativen Zugriff auf die Verwaltungskonsole zu steuern.</span><span class="sxs-lookup"><span data-stu-id="1d319-114">During installation of the App-V Management Server, you must select an Active Directory group to use as the App-V Administrators group to control administrative access to the Management Console.</span></span> <span data-ttu-id="1d319-115">Erstellen Sie eine Sicherheitsgruppe für App-V-Administratoren, und fügen Sie dieser Gruppe alle Benutzer hinzu, die die Verwaltungskonsole verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="1d319-115">Create a security group for App-V administrators, and add to this group every user who needs to use the Management Console.</span></span> <span data-ttu-id="1d319-116">Sie können diese Gruppe nicht direkt über das App-V Management Server-Installationsprogramm erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d319-116">You cannot create this group directly from the App-V Management Server installer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1d319-117">App-V-Benutzergruppe</span><span class="sxs-lookup"><span data-stu-id="1d319-117">App-V Users Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d319-118">App-v setzt voraus, dass jedes Benutzerkonto, das auf App-v-Funktionen zugreift, Mitglied einer Anbieterrichtlinie ist, die einer einzelnen Gruppe für den allgemeinen Platt Form Zugriff zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1d319-118">App-V requires that every User account that accesses App-V functions be a member of a provider policy associated with a single group for general platform access.</span></span> <span data-ttu-id="1d319-119">Verwenden einer vorhandenen Gruppe beispielsweise Domänenbenutzer, wenn alle Benutzer Zugriff auf App-V haben oder eine neue Gruppe erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="1d319-119">Use an existing group; for example, Domain Users, if all users are to have access to App-V, or create a new group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1d319-120">Anwendungsgruppen</span><span class="sxs-lookup"><span data-stu-id="1d319-120">Application Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d319-121">App-V ordnet das Recht zur Verwendung einer einzelnen Anwendung mit einer Active Directory-Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="1d319-121">App-V associates the right to use an individual application with an Active Directory group.</span></span> <span data-ttu-id="1d319-122">Erstellen Sie für jede Anwendung eine Active Directory-Gruppe, und weisen Sie Benutzer diesen Gruppen nach Bedarf zu, um den Benutzer Zugriff auf die Anwendungen zu kontrollieren.</span><span class="sxs-lookup"><span data-stu-id="1d319-122">Create an Active Directory group for each application, and assign users to these groups as needed to control user access to the applications.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1d319-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1d319-123">Related topics</span></span>


[<span data-ttu-id="1d319-124">Bereitstellungsanforderungen für Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="1d319-124">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="1d319-125">Konfigurieren von Windows Server 2008 für App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="1d319-125">How to Configure Windows Server 2008 for App-V Management Servers</span></span>](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





