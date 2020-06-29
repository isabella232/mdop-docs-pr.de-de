---
title: Wiederherstellen von Anwendungs- und Windows-Einstellungen, die mit UE-V 1.0 synchronisiert sind
description: Wiederherstellen von Anwendungs- und Windows-Einstellungen, die mit UE-V 1.0 synchronisiert sind
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804181"
---
# <span data-ttu-id="60f59-103">Wiederherstellen von Anwendungs- und Windows-Einstellungen, die mit UE-V 1.0 synchronisiert sind</span><span class="sxs-lookup"><span data-stu-id="60f59-103">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>


<span data-ttu-id="60f59-104">WMI-und PowerShell-Features von Microsoft User Experience Virtualization (UE-V) bieten die Möglichkeit zum Wiederherstellen von Einstellungspaketen.</span><span class="sxs-lookup"><span data-stu-id="60f59-104">WMI and PowerShell features of Microsoft User Experience Virtualization (UE-V) provide the ability to restore settings packages.</span></span> <span data-ttu-id="60f59-105">Mit WMI-und PowerShell-Befehlen können Sie die Anwendungs-und Windows-Einstellungen auf die Einstellungswerte zurücksetzen, die sich auf dem Computer befanden, als die Anwendung zum ersten Mal nach der Installation des UE-V-Agents gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="60f59-105">WMI and PowerShell commands allow you to restore application and Windows settings to the settings values that were on the computer the first time the application launched after the UE-V Agent was installed.</span></span> <span data-ttu-id="60f59-106">Diese Wiederherstellungsaktion wird für einzelne Anwendungs-oder Windows-Einstellungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60f59-106">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="60f59-107">Die Einstellungen werden wiederhergestellt, wenn die Anwendung das nächste Mal ausgeführt wird oder wenn sich der Benutzer beim Betriebssystem anmeldet.</span><span class="sxs-lookup"><span data-stu-id="60f59-107">The settings are restored the next time that the application is run or when the user logs on to the operating system.</span></span>

**<span data-ttu-id="60f59-108">So stellen Sie Anwendungseinstellungen und Windows-Einstellungen mit PowerShell wieder her</span><span class="sxs-lookup"><span data-stu-id="60f59-108">To restore application settings and Windows settings with PowerShell</span></span>**

1.  <span data-ttu-id="60f59-109">Öffnen Sie das Windows PowerShell-Fenster.</span><span class="sxs-lookup"><span data-stu-id="60f59-109">Open the Windows PowerShell window.</span></span> <span data-ttu-id="60f59-110">Zum Importieren des Microsoft UE-V PowerShell-Moduls geben Sie den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="60f59-110">To import the Microsoft UE-V PowerShell module, enter the following command:</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="60f59-111">Geben Sie das folgende PowerShell-Cmdlet ein, um die Anwendungseinstellungen und Windows-Einstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="60f59-111">Enter the following PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="60f59-112">PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="60f59-112">PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="60f59-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60f59-113">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="60f59-114">Wiederherstellen – UevUserSetting</span><span class="sxs-lookup"><span data-stu-id="60f59-114">Restore-UevUserSetting</span></span></p></td>
    <td align="left"><p><span data-ttu-id="60f59-115">Wiederherstellen der Benutzereinstellungen für eine Anwendung oder Wiederherstellen einer Gruppe von Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="60f59-115">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="60f59-116">So stellen Sie Anwendungseinstellungen und Windows-Einstellungen mit WMI wieder her</span><span class="sxs-lookup"><span data-stu-id="60f59-116">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="60f59-117">Öffnen Sie ein PowerShell-Fenster.</span><span class="sxs-lookup"><span data-stu-id="60f59-117">Open a PowerShell window.</span></span>

2.  <span data-ttu-id="60f59-118">Geben Sie den folgenden WMI-Befehl ein, um Anwendungseinstellungen und Windows-Einstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="60f59-118">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="60f59-119">WMI-Befehl</span><span class="sxs-lookup"><span data-stu-id="60f59-119">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="60f59-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60f59-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="60f59-121">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class UserSettings-Name RestoreByTemplateId-argumentlist &lt; template_ID&gt;</span><span class="sxs-lookup"><span data-stu-id="60f59-121">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="60f59-122">Wiederherstellen der Benutzereinstellungen für eine Anwendung oder Wiederherstellen einer Gruppe von Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="60f59-122">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="60f59-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="60f59-123">Related topics</span></span>


[<span data-ttu-id="60f59-124">Verwalten von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="60f59-124">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="60f59-125">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="60f59-125">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





