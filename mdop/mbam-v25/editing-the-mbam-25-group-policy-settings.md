---
title: Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5
description: Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804346"
---
# <span data-ttu-id="fce02-103">Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fce02-103">Editing the MBAM 2.5 Group Policy Settings</span></span>


<span data-ttu-id="fce02-104">Zur erfolgreichen Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) müssen Sie folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="fce02-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fce02-105">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="fce02-105">Task</span></span></th>
<th align="left"><span data-ttu-id="fce02-106">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fce02-106">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fce02-107">Kopieren Sie die MBAM 2,5-Gruppenrichtlinienvorlagen.</span><span class="sxs-lookup"><span data-stu-id="fce02-107">Copy the MBAM 2.5 Group Policy Templates.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="fce02-108">Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fce02-108">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fce02-109">Ermitteln Sie, welche Gruppenrichtlinienobjekte (GPOs) Sie in ihrer MBAM-Implementierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="fce02-109">Determine which Group Policy Objects (GPOs) you want to use in your MBAM implementation.</span></span> <span data-ttu-id="fce02-110">Je nach den Anforderungen Ihrer Organisation müssen Sie möglicherweise zusätzliche Gruppenrichtlinieneinstellungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fce02-110">Based on the needs of your organization, you might have to configure additional Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="fce02-111">Planen von MBAM 2,5-Gruppenrichtlinienanforderungen </a> – enthält Beschreibungen der GPOs</span><span class="sxs-lookup"><span data-stu-id="fce02-111">Planning for MBAM 2.5 Group Policy Requirements</a> – contains descriptions of the GPOs</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fce02-112">Festlegen der Gruppenrichtlinieneinstellungen für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="fce02-112">Set the Group Policy settings for your organization.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fce02-113">**Wichtig**  Ändern Sie die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten nicht, oder MBAM wird nicht ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="fce02-113">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="fce02-114">Wenn Sie die Gruppenrichtlinieneinstellungen im MDOP- **MBAM (BitLocker-Verwaltungsknoten)** konfigurieren, konfiguriert MBAM automatisch die **BitLocker-Laufwerk Verschlüsselungs** Einstellungen für Sie.</span><span class="sxs-lookup"><span data-stu-id="fce02-114">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="fce02-115">So bearbeiten Sie die MBAM-Client Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="fce02-115">To edit MBAM Client Group Policy settings</span></span>**

1.  <span data-ttu-id="fce02-116">Stellen Sie auf einem Computer, auf dem die MBAM-Gruppenrichtlinienvorlagen installiert sind, sicher, dass die MBAM-Dienste aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="fce02-116">On a computer that has the MBAM Group Policy Templates installed, make sure that MBAM Services are enabled.</span></span>

2.  <span data-ttu-id="fce02-117">Wenn Sie die Gruppenrichtlinien-Verwaltungskonsole (GPMC. msc) oder das Microsoft Advanced Group Policy Management MDOP-Produkt auf einem Computer verwenden, auf dem die MBAM-Gruppenrichtlinienvorlagen installiert sind, wählen Sie **Computer Konfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung)** aus.</span><span class="sxs-lookup"><span data-stu-id="fce02-117">Using the Group Policy Management Console (GPMC.msc) or the Microsoft Advanced Group Policy Management MDOP product on a computer with the MBAM Group Policy Templates installed, select **Computer configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="fce02-118">Bearbeiten Sie die Gruppenrichtlinieneinstellungen, die zum Aktivieren von MBAM-Clientdiensten auf Clientcomputern erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fce02-118">Edit the Group Policy settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="fce02-119">Wählen Sie für jede Richtlinie in der folgenden Tabelle **Richtliniengruppe**aus, klicken Sie auf die gewünschte **Richt** Linie, und konfigurieren Sie dann die Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="fce02-119">For each policy in the following table, select **Policy Group**, click the **Policy** you want, and then configure the settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="fce02-120">Richtliniengruppe</span><span class="sxs-lookup"><span data-stu-id="fce02-120">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="fce02-121">Richtlinie</span><span class="sxs-lookup"><span data-stu-id="fce02-121">Policy</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fce02-122">Clientverwaltung</span><span class="sxs-lookup"><span data-stu-id="fce02-122">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fce02-123">Konfigurieren von MBAM-Diensten</span><span class="sxs-lookup"><span data-stu-id="fce02-123">Configure MBAM Services</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fce02-124">Betriebs System Laufwerk</span><span class="sxs-lookup"><span data-stu-id="fce02-124">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fce02-125">Verschlüsselungseinstellungen für das Betriebssystemlaufwerk</span><span class="sxs-lookup"><span data-stu-id="fce02-125">Operating system drive encryption settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fce02-126">Wechsellaufwerk</span><span class="sxs-lookup"><span data-stu-id="fce02-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fce02-127">Steuern der Verwendung von BitLocker auf Wechseldatenträgern</span><span class="sxs-lookup"><span data-stu-id="fce02-127">Control use of BitLocker on removable drives</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fce02-128">Festes Laufwerk</span><span class="sxs-lookup"><span data-stu-id="fce02-128">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fce02-129">Steuern der Verwendung von BitLocker auf Festplatten</span><span class="sxs-lookup"><span data-stu-id="fce02-129">Control use of BitLocker on fixed drives</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="fce02-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="fce02-130">Related topics</span></span>


[<span data-ttu-id="fce02-131">Planen der Gruppenrichtlinienanforderungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fce02-131">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

[<span data-ttu-id="fce02-132">Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fce02-132">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

 
## <span data-ttu-id="fce02-133">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="fce02-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="fce02-134">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="fce02-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="fce02-135">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="fce02-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





