---
title: Bereitstellen des Katalogs für Einstellungsvorlagen für UE-V 1.0
description: Bereitstellen des Katalogs für Einstellungsvorlagen für UE-V 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811872"
---
# <span data-ttu-id="7fed4-103">Bereitstellen des Katalogs für Einstellungsvorlagen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7fed4-103">Deploying the Settings Template Catalog for UE-V 1.0</span></span>


<span data-ttu-id="7fed4-104">Speicherort Vorlagen für benutzerdefinierte Einstellungen können auf einem Ordnerpfad auf Microsoft User Experience Virtualization (UE-V)-Computern oder auf einer SMB-Netzwerkfreigabe (Server Message Block) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7fed4-104">Custom settings location templates can be stored on a folder path on Microsoft User Experience Virtualization (UE-V) computers or on a Server Message Block (SMB) network share.</span></span> <span data-ttu-id="7fed4-105">Ein geplanter Task auf dem Computer sucht nach neuen oder aktualisierten Vorlagen von diesem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="7fed4-105">A scheduled task on the computer checks for new or updated templates from this location.</span></span> <span data-ttu-id="7fed4-106">Der Task überprüft diesen Ort einmal täglich und aktualisiert sein Synchronisierungsverhalten auf der Grundlage der Vorlagen in diesem Ordner.</span><span class="sxs-lookup"><span data-stu-id="7fed4-106">The task checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="7fed4-107">Vorlagen, die seit der letzten Überprüfung in diesem Ordner hinzugefügt oder aktualisiert wurden, werden vom UE-V-Agent registriert.</span><span class="sxs-lookup"><span data-stu-id="7fed4-107">Templates that are added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="7fed4-108">Der UE-V-Agent hebt die Registrierung von Vorlagen auf, die aus diesem Ordner entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="7fed4-108">The UE-V agent deregisters templates that were removed from this folder.</span></span> <span data-ttu-id="7fed4-109">Der geplante Task wird als System ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fed4-109">The scheduled task runs as SYSTEM.</span></span> <span data-ttu-id="7fed4-110">Die Netzwerkfreigabe muss mindestens die Berechtigungen für die Gruppe "Domänencomputer" erteilen.</span><span class="sxs-lookup"><span data-stu-id="7fed4-110">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="7fed4-111">Erteilen Sie außerdem Zugriffsberechtigungen für den Netzwerkfreigabeordner für Administratoren, die die gespeicherten Vorlagen verwalten sollen.</span><span class="sxs-lookup"><span data-stu-id="7fed4-111">In addition, grant access permissions for the network share folder to administrators who will manage the stored templates.</span></span> <span data-ttu-id="7fed4-112">Weitere Informationen zu Vorlagen für benutzerdefinierte Einstellungen finden Sie unter [Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="7fed4-112">For more information about custom setting location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

**<span data-ttu-id="7fed4-113">So konfigurieren Sie den Vorlagenkatalog für die Einstellungen für UE-V</span><span class="sxs-lookup"><span data-stu-id="7fed4-113">To configure the settings template catalog for UE-V</span></span>**

1.  <span data-ttu-id="7fed4-114">Erstellen Sie einen neuen Ordner auf dem Computer, auf dem der Vorlagenkatalog für UE-V-Einstellungen gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fed4-114">Create a new folder on the computer that will store the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="7fed4-115">Legen Sie die folgenden SMB-Berechtigungen (Freigabeebene) für den Katalogordner "Einstellungs Vorlagen" ein.</span><span class="sxs-lookup"><span data-stu-id="7fed4-115">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="7fed4-116">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="7fed4-116">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="7fed4-117">Berechtigungen empfehlen</span><span class="sxs-lookup"><span data-stu-id="7fed4-117">Recommend permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7fed4-118">Jeder</span><span class="sxs-lookup"><span data-stu-id="7fed4-118">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-119">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7fed4-119">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7fed4-120">Domänencomputer</span><span class="sxs-lookup"><span data-stu-id="7fed4-120">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-121">Lesen von Berechtigungsstufen</span><span class="sxs-lookup"><span data-stu-id="7fed4-121">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7fed4-122">Administratoren</span><span class="sxs-lookup"><span data-stu-id="7fed4-122">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-123">Berechtigungsstufen für Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fed4-123">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="7fed4-124">Legen Sie die folgenden NTFS-Berechtigungen für den Katalogordner "Settings" (Einstellungen).</span><span class="sxs-lookup"><span data-stu-id="7fed4-124">Set the following NTFS permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7fed4-125">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="7fed4-125">User Account</span></span></th>
    <th align="left"><span data-ttu-id="7fed4-126">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7fed4-126">Recommended Permissions</span></span></th>
    <th align="left"><span data-ttu-id="7fed4-127">Anwenden auf</span><span class="sxs-lookup"><span data-stu-id="7fed4-127">Apply To</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7fed4-128">Ersteller/Besitzer</span><span class="sxs-lookup"><span data-stu-id="7fed4-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-129">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="7fed4-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-130">Dieser Ordner, Unterordner und Dateien</span><span class="sxs-lookup"><span data-stu-id="7fed4-130">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7fed4-131">Domänencomputer</span><span class="sxs-lookup"><span data-stu-id="7fed4-131">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-132">Ordnerinhalte auflisten und lesen</span><span class="sxs-lookup"><span data-stu-id="7fed4-132">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-133">Dieser Ordner, Unterordner und Dateien</span><span class="sxs-lookup"><span data-stu-id="7fed4-133">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7fed4-134">Jeder</span><span class="sxs-lookup"><span data-stu-id="7fed4-134">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-135">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7fed4-135">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-136">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7fed4-136">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7fed4-137">Administratoren</span><span class="sxs-lookup"><span data-stu-id="7fed4-137">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-138">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="7fed4-138">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7fed4-139">Dieser Ordner, Unterordner und Dateien</span><span class="sxs-lookup"><span data-stu-id="7fed4-139">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="7fed4-140">Klicken Sie auf **OK** , um die Dialogfelder zu schließen.</span><span class="sxs-lookup"><span data-stu-id="7fed4-140">Click **OK** to close the dialog boxes.</span></span>

## <span data-ttu-id="7fed4-141">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7fed4-141">Related topics</span></span>


[<span data-ttu-id="7fed4-142">Bereitstellen von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7fed4-142">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="7fed4-143">Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7fed4-143">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





