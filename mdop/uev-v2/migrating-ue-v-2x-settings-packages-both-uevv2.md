---
title: Migrieren von UE-V 2. x-Einstellungspaketen
description: Migrieren von UE-V 2. x-Einstellungspaketen
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811203"
---
# <span data-ttu-id="16ed4-103">Migrieren von UE-V 2. x-Einstellungspaketen</span><span class="sxs-lookup"><span data-stu-id="16ed4-103">Migrating UE-V 2.x Settings Packages</span></span>


<span data-ttu-id="16ed4-104">Im Lebenszyklus einer Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 oder 2,1 SP1-Bereitstellung müssen Sie möglicherweise die Benutzer Einstellungs Pakete neu positionieren, wenn Sie zu einem neuen Server migrieren oder Sicherungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="16ed4-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 deployment, you might have to relocate the user settings packages either when you migrate to a new server or when you perform backups.</span></span> <span data-ttu-id="16ed4-105">Einstellungs Pakete müssen möglicherweise in den folgenden Szenarien migriert werden:</span><span class="sxs-lookup"><span data-stu-id="16ed4-105">Settings packages might have to be migrated in the following scenarios:</span></span>

-   <span data-ttu-id="16ed4-106">Upgrade vorhandener Server Hardware auf einen moderneren Server.</span><span class="sxs-lookup"><span data-stu-id="16ed4-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="16ed4-107">Migration einer Einstellungen-Speicherorts Freigabe von einem Testserver zu einem Produktionsserver.</span><span class="sxs-lookup"><span data-stu-id="16ed4-107">Migration of a settings storage location share from a test server to a production server.</span></span>

<span data-ttu-id="16ed4-108">Durch einfaches Kopieren der Dateien und Ordner bleiben die Sicherheitseinstellungen und-Berechtigungen nicht erhalten.</span><span class="sxs-lookup"><span data-stu-id="16ed4-108">Simply copying the files and folders does not preserve the security settings and permissions.</span></span> <span data-ttu-id="16ed4-109">In den folgenden Schritten wird beschrieben, wie Sie das Einstellungspaket zusammen mit den Berechtigungen für das NTFS-Dateisystem ordnungsgemäß auf eine neue Freigabe kopieren.</span><span class="sxs-lookup"><span data-stu-id="16ed4-109">The following steps describe how to correctly copy the settings package along with their NTFS file system permissions to a new share.</span></span>

**<span data-ttu-id="16ed4-110">So erhalten Sie die UE-V 2-Einstellungs Pakete beim Migrieren zu einem neuen Server</span><span class="sxs-lookup"><span data-stu-id="16ed4-110">To preserve UE-V 2 settings packages when you migrate to a new server</span></span>**

1.  <span data-ttu-id="16ed4-111">Erstellen Sie an einem neuen Speicherort auf einem anderen Server einen neuen Ordner, beispielsweise "meine Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="16ed4-111">In a new location on a different server, create a new folder, for example, MySettings.</span></span>

2.  <span data-ttu-id="16ed4-112">Deaktivieren der Freigabe für die alte Ordnerfreigabe auf dem alten Server</span><span class="sxs-lookup"><span data-stu-id="16ed4-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="16ed4-113">So kopieren Sie die vorhandenen Einstellungs Pakete auf den neuen Server mit Robocopy</span><span class="sxs-lookup"><span data-stu-id="16ed4-113">To copy the existing settings packages to the new server with Robocopy</span></span>

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="16ed4-114">**Hinweis**  Öffnen Sie MySettings.txt mit einer Protokollanzeige wie Trace32, um den Kopierfortschritt zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="16ed4-114">**Note** To monitor the copy progress, open MySettings.txt with a log viewer such as Trace32.</span></span>

     

4.  <span data-ttu-id="16ed4-115">Erteilen Sie der neuen Freigabeberechtigungen für Freigabeebenen.</span><span class="sxs-lookup"><span data-stu-id="16ed4-115">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="16ed4-116">Belasse die NTFS-Dateisystemberechtigungen, wie Sie von Robocopy eingestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="16ed4-116">Leave the NTFS file system permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="16ed4-117">Aktualisieren Sie auf Computern, auf denen der UE-V-Agent ausgeführt wird, die **SettingsStoragePath** -Konfigurationseinstellung auf den UNC-Pfad (Universal Naming Convention) der neuen Freigabe.</span><span class="sxs-lookup"><span data-stu-id="16ed4-117">On computers that run the UE-V Agent, update the **SettingsStoragePath** configuration setting to the Universal Naming Convention (UNC) path of the new share.</span></span>

    <span data-ttu-id="16ed4-118">Sie **haben einen Vorschlag für UE-V**?</span><span class="sxs-lookup"><span data-stu-id="16ed4-118">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="16ed4-119">[Hier](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="16ed4-119">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="16ed4-120">**Haben Sie ein UE-V-Problem**?</span><span class="sxs-lookup"><span data-stu-id="16ed4-120">**Got a UE-V issue**?</span></span> <span data-ttu-id="16ed4-121">Verwenden Sie das [UE-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="16ed4-121">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="16ed4-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="16ed4-122">Related topics</span></span>


[<span data-ttu-id="16ed4-123">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="16ed4-123">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





