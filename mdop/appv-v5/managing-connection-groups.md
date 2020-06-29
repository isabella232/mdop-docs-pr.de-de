---
title: Verwalten von Verbindungsgruppen
description: Verwalten von Verbindungsgruppen
author: dansimp
ms.assetid: 1a9c8f26-f421-4b70-b7e2-da8118e8198c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2e57b9dbe56072e6049e8fabef5705c374d022c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805084"
---
# <span data-ttu-id="44eeb-103">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="44eeb-103">Managing Connection Groups</span></span>


<span data-ttu-id="44eeb-104">Mithilfe von Verbindungsgruppen können die Anwendungen innerhalb eines Pakets in der virtuellen Umgebung miteinander interagieren, während Sie vom restlichen System isoliert bleiben.</span><span class="sxs-lookup"><span data-stu-id="44eeb-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="44eeb-105">Mithilfe von Verbindungsgruppen können Administratoren Pakete unabhängig voneinander verwalten und vermeiden, dass Sie die gleiche Anwendung mehrmals auf einem Clientcomputer hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="44eeb-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="44eeb-106">**Hinweis**  In früheren Versionen von App-V 5,0 wurden Verbindungsgruppen als dynamische Suite-Komposition bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="44eeb-106">**Note** In previous versions of App-V 5.0, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="44eeb-107">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="44eeb-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md)"><span data-ttu-id="44eeb-108">Über die virtuelle Verbindungsgruppenumgebung</span><span class="sxs-lookup"><span data-stu-id="44eeb-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="44eeb-109">Beschreibt die virtuelle Umgebung der Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="44eeb-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file.md)"><span data-ttu-id="44eeb-110">Über die Verbindungsgruppendatei</span><span class="sxs-lookup"><span data-stu-id="44eeb-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="44eeb-111">Beschreibt die Verbindungsgruppen Datei.</span><span class="sxs-lookup"><span data-stu-id="44eeb-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group.md)"><span data-ttu-id="44eeb-112">So erstellen Sie eine Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="44eeb-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="44eeb-113">Erläutert, wie eine neue Verbindungsgruppe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="44eeb-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="44eeb-114">So erstellen Sie eine Verbindungsgruppe mit von Benutzern und global veröffentlichten Paketen</span><span class="sxs-lookup"><span data-stu-id="44eeb-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="44eeb-115">Es wird erläutert, wie Sie eine neue Verbindungsgruppe erstellen, die eine Kombination aus Paketen enthält, die für den Benutzer veröffentlicht und Global veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="44eeb-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group.md)"><span data-ttu-id="44eeb-116">So löschen Sie eine Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="44eeb-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="44eeb-117">Es wird erläutert, wie eine Verbindungsgruppe gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="44eeb-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group.md)"><span data-ttu-id="44eeb-118">So veröffentlichen Sie eine Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="44eeb-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="44eeb-119">Erläutert, wie eine Verbindungsgruppe veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="44eeb-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="44eeb-120">Weitere Ressourcen für App-V 5,0-Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="44eeb-120">Other resources for App-V 5.0 connection groups</span></span>


-   [<span data-ttu-id="44eeb-121">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="44eeb-121">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





