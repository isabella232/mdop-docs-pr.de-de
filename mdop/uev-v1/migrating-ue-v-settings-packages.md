---
title: Migrieren von UE-V-Einstellungspaketen
description: Migrieren von UE-V-Einstellungspaketen
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809817"
---
# <span data-ttu-id="e3d70-103">Migrieren von UE-V-Einstellungspaketen</span><span class="sxs-lookup"><span data-stu-id="e3d70-103">Migrating UE-V Settings Packages</span></span>


<span data-ttu-id="e3d70-104">Im Lebenszyklus einer Microsoft User Experience Virtualization (UE-V)-Bereitstellung müssen Sie möglicherweise die Benutzer Einstellungs Pakete bei der Migration zu einem neuen Server oder zu Sicherungszwecken neu positionieren.</span><span class="sxs-lookup"><span data-stu-id="e3d70-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) deployment, you might need to relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span> <span data-ttu-id="e3d70-105">Die Migration von Einstellungspaketen kann in den folgenden Szenarien erforderlich sein:</span><span class="sxs-lookup"><span data-stu-id="e3d70-105">Migration of settings packages might be needed in the following scenarios:</span></span>

-   <span data-ttu-id="e3d70-106">Upgrade vorhandener Server Hardware auf einen moderneren Server.</span><span class="sxs-lookup"><span data-stu-id="e3d70-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="e3d70-107">Migration einer Speicherorts Freigabe für Einstellungen aus einer Übungseinheit auf einen Produktionsserver.</span><span class="sxs-lookup"><span data-stu-id="e3d70-107">Migration of a settings storage location share from a lab to a production server.</span></span>

<span data-ttu-id="e3d70-108">Durch einfaches Kopieren der Dateien und Ordner bleiben die Sicherheitseinstellungen und-Berechtigungen nicht erhalten.</span><span class="sxs-lookup"><span data-stu-id="e3d70-108">Simply copying the files and folders will not preserve the security settings and permissions.</span></span> <span data-ttu-id="e3d70-109">Mit den folgenden Schritten werden die Einstellungen-Paketdateien mit ihren NTFS-Berechtigungen ordnungsgemäß auf eine neue Freigabe kopiert.</span><span class="sxs-lookup"><span data-stu-id="e3d70-109">The following described steps will properly copy the settings package files with their NTFS permissions to a new share.</span></span>

**<span data-ttu-id="e3d70-110">Beibehalten der UE-V-Einstellungs Pakete beim Migrieren zu einem neuen Server</span><span class="sxs-lookup"><span data-stu-id="e3d70-110">How to preserve UE-V settings packages when migrating to a new server</span></span>**

1.  <span data-ttu-id="e3d70-111">Erstellen Sie an einem neuen Speicherort auf einem anderen Server einen neuen Ordner. Beispiel: MySettings.</span><span class="sxs-lookup"><span data-stu-id="e3d70-111">In a new location on a different server, create a new folder; for example, MySettings.</span></span>

2.  <span data-ttu-id="e3d70-112">Deaktivieren der Freigabe für die alte Ordnerfreigabe auf dem alten Server</span><span class="sxs-lookup"><span data-stu-id="e3d70-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="e3d70-113">Verschieben Sie die vorhandenen Einstellungs Pakete über die Befehlszeile auf den neuen Server mit Robocopy.</span><span class="sxs-lookup"><span data-stu-id="e3d70-113">Move the existing settings packages to the new server with Robocopy from the command line.</span></span> <span data-ttu-id="e3d70-114">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e3d70-114">For example:</span></span>

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="e3d70-115">**Hinweis**  Öffnen Sie MySettings.txt mit einem Protokolldatei Leser wie Trace32, um den Kopierfortschritt zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="e3d70-115">**Note** To monitor the copy progress, open MySettings.txt with a log file reader such as Trace32.</span></span>

     

4.  <span data-ttu-id="e3d70-116">Erteilen Sie der neuen Freigabeberechtigungen für Freigabeebenen.</span><span class="sxs-lookup"><span data-stu-id="e3d70-116">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="e3d70-117">Übernehmen Sie die NTFS-Berechtigungen, wie Sie von Robocopy eingestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e3d70-117">Leave the NTFS permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="e3d70-118">Aktualisieren Sie auf Computern, auf denen der UE-V-Agent ausgeführt wird, die SettingsStoragePath-Konfigurationseinstellung auf den UNC-Pfad der neuen Freigabe.</span><span class="sxs-lookup"><span data-stu-id="e3d70-118">On computers that run the UE-V agent, update the SettingsStoragePath configuration setting to the UNC path of the new share.</span></span>

## <span data-ttu-id="e3d70-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e3d70-119">Related topics</span></span>


[<span data-ttu-id="e3d70-120">Verwalten von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e3d70-120">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="e3d70-121">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e3d70-121">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





