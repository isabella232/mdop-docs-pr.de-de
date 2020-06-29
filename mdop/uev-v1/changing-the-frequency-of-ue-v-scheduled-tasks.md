---
title: Ändern der Häufigkeit von geplanten UE-V-Aufgaben
description: Ändern der Häufigkeit von geplanten UE-V-Aufgaben
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809505"
---
# <span data-ttu-id="e2973-103">Ändern der Häufigkeit von geplanten UE-V-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="e2973-103">Changing the Frequency of UE-V Scheduled Tasks</span></span>


<span data-ttu-id="e2973-104">Der Microsoft User Experience Virtualization (UE-v)-Agent-Installationsprogramm, AgentSetup.exe, erstellt zwei geplante Aufgaben während der Installation des UE-v-Agents.</span><span class="sxs-lookup"><span data-stu-id="e2973-104">The Microsoft User Experience Virtualization (UE-V) Agent installer, AgentSetup.exe, creates two scheduled tasks during the UE-V Agent installation.</span></span> <span data-ttu-id="e2973-105">Bei den beiden Aufgaben handelt es sich um den Aufgabenbereich " **automatische Aktualisierungs Vorlage** " und die Einstellung "Speicherort **Status** ".</span><span class="sxs-lookup"><span data-stu-id="e2973-105">The two tasks are the **Template Auto Update** task and the **Setting Storage Location Status** task.</span></span> <span data-ttu-id="e2973-106">Diese geplanten Aufgaben können mit den UE-V-Tools nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="e2973-106">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="e2973-107">Administratoren, die die geplante Aufgabe für diese Elemente ändern möchten, können ein Skript erstellen, das die Schtasks.exe Befehlszeilenoptionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2973-107">Administrators who wish to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="e2973-108">Weitere Informationen zu Schtasks.exe finden Sie unter [so wird es gemacht: Verwenden von schtasks, exe zum Planen von Aufgaben in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="e2973-108">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

## <span data-ttu-id="e2973-109">Automatische Aktualisierung der Vorlage</span><span class="sxs-lookup"><span data-stu-id="e2973-109">Template Auto-Update</span></span>


<span data-ttu-id="e2973-110">Mit dem **automatischen Aktualisierungs** Vorgang der Vorlage wird der Einstellungs Vorlagenkatalog auf neue, aktualisierte oder entfernte Vorlagen überprüft.</span><span class="sxs-lookup"><span data-stu-id="e2973-110">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="e2973-111">Diese Aufgabe wird nur ausgeführt, wenn die SettingsTemplateCatalog konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="e2973-111">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="e2973-112">Der Task " **Automatische Aktualisierung der Vorlage** " führt die ApplySettingsCatalog.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.</span><span class="sxs-lookup"><span data-stu-id="e2973-112">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent install directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e2973-113">Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="e2973-113">Task name</span></span></th>
<th align="left"><span data-ttu-id="e2973-114">Standardauslöser</span><span class="sxs-lookup"><span data-stu-id="e2973-114">Default trigger</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e2973-115">\Microsoft\UE-V\Template Auto Update</span><span class="sxs-lookup"><span data-stu-id="e2973-115">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2973-116">3:30 Uhr pro Tag</span><span class="sxs-lookup"><span data-stu-id="e2973-116">3:30 AM every day</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e2973-117">**Beispiel:** Mit dem folgenden Befehl wird der Agent so konfiguriert, dass der Katalog Speicher für Einstellungs Vorlagen stündlich überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="e2973-117">**Example:** The following command configures the agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## <span data-ttu-id="e2973-118">Status des Speicherorts für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e2973-118">Settings Storage Location Status</span></span>


<span data-ttu-id="e2973-119">Die Aufgabe **Speicherorts Status festlegen** führt die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="e2973-119">The **Setting Storage Location Status** task performs the following actions:</span></span>

1.  <span data-ttu-id="e2973-120">Überprüft, ob die UE-V-Ordner noch mit dem Feature Offlinedateien angeheftet oder registriert sind.</span><span class="sxs-lookup"><span data-stu-id="e2973-120">Checks to make sure the UE-V folders are still pinned or registered with the offline files feature.</span></span>

2.  <span data-ttu-id="e2973-121">Überprüft, ob der Speicherort für Einstellungen offline oder Online ist.</span><span class="sxs-lookup"><span data-stu-id="e2973-121">Checks whether the settings storage location is offline or online.</span></span>

3.  <span data-ttu-id="e2973-122">Erzwingt eine Synchronisierung für das angegebene Intervall anstelle des Standardintervalls für Offlinedateien.</span><span class="sxs-lookup"><span data-stu-id="e2973-122">Forces a synchronization on the specified interval instead of the default interval for offline files.</span></span>

4.  <span data-ttu-id="e2973-123">Synchronisiert alle Einstellungs Pakete, die so konfiguriert sind, dass Sie vorab abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e2973-123">Synchronizes any settings packages that are configured to be pre-fetched.</span></span>

5.  <span data-ttu-id="e2973-124">Überprüft, ob sich der Pfad des Active Directory-Basisverzeichnisses geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e2973-124">Checks if the Active Directory home directory path has changed.</span></span>

6.  <span data-ttu-id="e2973-125">Schreibt die Speicherkonfiguration für aktuelle Einstellungen unter dem folgenden Speicherort</span><span class="sxs-lookup"><span data-stu-id="e2973-125">Writes the current settings storage configuration under the following location</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="e2973-126">Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="e2973-126">Task name</span></span></th>
    <th align="left"><span data-ttu-id="e2973-127">Standardauslöser</span><span class="sxs-lookup"><span data-stu-id="e2973-127">Default trigger</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e2973-128">Status des \Microsoft\UE-V\Settings-Speicherorts</span><span class="sxs-lookup"><span data-stu-id="e2973-128">\Microsoft\UE-V\Settings Storage Location Status</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e2973-129">Bei der Anmeldung eines beliebigen Benutzers – nach dem auslösen, wiederholen Sie alle 30 Minuten auf unbestimmte Zeit.</span><span class="sxs-lookup"><span data-stu-id="e2973-129">At logon of any user – After triggered, repeat every 30 minutes indefinitely.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="e2973-130">**Beispiel:** Mit dem folgenden Befehl wird der Agent so konfiguriert, dass die Aktion über stündlich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2973-130">**Example:** The following command configures the agent to run the action above every hour.</span></span>

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## <span data-ttu-id="e2973-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e2973-131">Related topics</span></span>


[<span data-ttu-id="e2973-132">Verwalten von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e2973-132">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="e2973-133">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e2973-133">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





