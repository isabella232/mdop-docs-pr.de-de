---
title: Prüfliste für das Auswerten von branchspezifischen Anwendungen für UE-V 1.0
description: Prüfliste für das Auswerten von branchspezifischen Anwendungen für UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811767"
---
# <span data-ttu-id="f6374-103">Prüfliste für das Auswerten von branchspezifischen Anwendungen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f6374-103">Checklist for Evaluating Line-of-Business Applications for UE-V 1.0</span></span>


<span data-ttu-id="f6374-104">Wenn Sie auswerten möchten, welche Branchenanwendungen in Ihre UE-V-Bereitstellung einbezogen werden sollen, sollten Sie Folgendes berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="f6374-104">To evaluate which line-of-business applications should be included in your UE-V deployment, consider the following:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="f6374-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6374-105">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f6374-106">Enthält diese Anwendung Einstellungen, die vom Benutzer angepasst werden können?</span><span class="sxs-lookup"><span data-stu-id="f6374-106">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f6374-107">Ist es wichtig, dass der Benutzer diese Einstellungen durchstreift?</span><span class="sxs-lookup"><span data-stu-id="f6374-107">Is it important for the user that these settings roam?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f6374-108">Werden diese Benutzereinstellungen bereits von einer Anwendungs Verwaltungs-oder Einstellungsrichtlinien Lösung verwaltet?</span><span class="sxs-lookup"><span data-stu-id="f6374-108">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="f6374-109">UE-V wendet Anwendungseinstellungen beim Start von Anwendungen und Windows-Einstellungen bei Anmeldung, entsperren oder Remote Verbindungsereignissen an.</span><span class="sxs-lookup"><span data-stu-id="f6374-109">UE-V applies application settings at application launch and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="f6374-110">Wenn Sie UE-V mit anderen Einstellungen-Richtlinien Lösungen verwenden, kann es vorkommen, dass Benutzer in Roaming-Einstellungen inkonsistent sind.</span><span class="sxs-lookup"><span data-stu-id="f6374-110">If you use UE-V with other settings policy solutions, users might experience inconsistency across roamed settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f6374-111">Sind die Anwendungseinstellungen für den Computer spezifisch?</span><span class="sxs-lookup"><span data-stu-id="f6374-111">Are the application settings specific to the computer?</span></span> <span data-ttu-id="f6374-112">Anwendungseinstellungen und Anpassungen, die Hardware oder bestimmten Computerkonfigurationen zugeordnet sind, werden nicht konsistent in Sitzungen durchlaufen und können zu einer unzureichenden Anwendungsumgebung führen.</span><span class="sxs-lookup"><span data-stu-id="f6374-112">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently roam across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f6374-113">Speichert die Anwendung die Einstellungen im Verzeichnis "Programme" oder im Dateiverzeichnis, das sich im <strong> </strong> Verzeichnis Benutzer \ [Benutzername] \ <strong> AppData LocalLow befindet </strong>  \  <strong> </strong> ?</span><span class="sxs-lookup"><span data-stu-id="f6374-113">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong> \ [User name] \ <strong>AppData</strong> \ <strong>LocalLow</strong> directory?</span></span> <span data-ttu-id="f6374-114">Anwendungsdaten, die an einem dieser Speicherorte gespeichert sind, sollten normalerweise nicht mit dem Benutzer Roaming durchlaufen, da diese Daten für den Computer spezifisch sind oder weil die Daten für die Roaming-Datei zu groß sind.</span><span class="sxs-lookup"><span data-stu-id="f6374-114">Application data that is stored in either of these locations usually should not roam with the user, because this data is specific to the computer or because the data is too large to roam.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f6374-115">Speichert die Anwendung alle Einstellungen in einer Datei, die andere Anwendungsdaten enthält, die nicht durchlaufen werden sollen?</span><span class="sxs-lookup"><span data-stu-id="f6374-115">Does the application store any settings in a file that contains other application data that should not roam?</span></span> <span data-ttu-id="f6374-116">UE-V synchronisiert Dateien als einzelne Einheit.</span><span class="sxs-lookup"><span data-stu-id="f6374-116">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="f6374-117">Wenn Einstellungen in Dateien gespeichert werden, die Anwendungsdaten außer Einstellungen enthalten, kann das Synchronisieren dieser zusätzlichen Daten zu einer unzureichenden Anwendungsumgebung führen.</span><span class="sxs-lookup"><span data-stu-id="f6374-117">If settings are stored in files that include application data other than settings, then synchronizing this additional data may cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f6374-118">Wie groß sind die Dateien, die die Einstellungen enthalten?</span><span class="sxs-lookup"><span data-stu-id="f6374-118">How large are the files that contain the settings?</span></span> <span data-ttu-id="f6374-119">Die Leistung der Synchronisierung von Einstellungen kann von umfangreichen Dateien beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="f6374-119">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="f6374-120">Das einbeziehen großer Dateien kann sich auf die Leistung der Synchronisierung von Einstellungen auswirken.</span><span class="sxs-lookup"><span data-stu-id="f6374-120">Including large files can impact the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f6374-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f6374-121">Related topics</span></span>


[<span data-ttu-id="f6374-122">Planen für UE-V-Konfigurationsmethoden</span><span class="sxs-lookup"><span data-stu-id="f6374-122">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

[<span data-ttu-id="f6374-123">Planen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f6374-123">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

 

 





