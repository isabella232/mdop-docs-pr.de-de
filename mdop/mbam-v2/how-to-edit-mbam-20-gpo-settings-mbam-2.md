---
title: So bearbeiten Sie GPO-Einstellungen für MBAM 2.0
description: So bearbeiten Sie GPO-Einstellungen für MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810345"
---
# <span data-ttu-id="ba503-103">So bearbeiten Sie GPO-Einstellungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ba503-103">How to Edit MBAM 2.0 GPO Settings</span></span>


<span data-ttu-id="ba503-104">Zur erfolgreichen Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) müssen Sie zunächst die Gruppenrichtlinien ermitteln, die Sie bei der Implementierung der Microsoft BitLocker-Verwaltung und-Überwachung verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="ba503-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="ba503-105">Weitere Informationen zu den verschiedenen verfügbaren Richtlinien finden Sie unter [Planen von MBAM 2,0-Gruppenrichtlinienanforderungen](planning-for-mbam-20-group-policy-requirements-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="ba503-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="ba503-106">Nachdem Sie die Richtlinien festgelegt haben, die Sie verwenden möchten, müssen Sie ein oder mehrere Gruppenrichtlinienobjekte ändern, die die Richtlinieneinstellungen für MBAM enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba503-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the policy settings for MBAM.</span></span>

<span data-ttu-id="ba503-107">Mit den folgenden Schritten können Sie die grundlegenden, empfohlenen GPO-Einstellungen so konfigurieren, dass MBAM die BitLocker-Verschlüsselung für die Clientcomputer Ihrer Organisation verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ba503-107">You can use the following steps to configure the basic, recommended GPO settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="ba503-108">So bearbeiten Sie MBAM-Client-GPO-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ba503-108">To Edit MBAM Client GPO Settings</span></span>**

1.  <span data-ttu-id="ba503-109">Stellen Sie auf einem Computer, auf dem MBAM-Gruppenrichtlinienvorlage installiert ist, sicher, dass MBAM-Dienste aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="ba503-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="ba503-110">Wenn Sie die Gruppenrichtlinien-Verwaltungskonsole (GPMC. msc) oder das Advanced Group Policy Management (AGPM)-MDOP-Produkt auf einem Computer verwenden, auf dem die MBAM-Gruppenrichtlinienvorlage installiert ist, wählen Sie **Computerkonfiguration**, **Richtlinien**aus, klicken Sie auf **Administrative Vorlagen**, wählen Sie **Windows-Komponenten**aus, und klicken Sie dann auf **MDOP MBAM (BitLocker-Verwaltung)**.</span><span class="sxs-lookup"><span data-stu-id="ba503-110">Using the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product on a computer with the MBAM Group Policy template installed, select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="ba503-111">Bearbeiten Sie die Einstellungen für Gruppenrichtlinienobjekte, die zum Aktivieren von MBAM-Clientdiensten auf Clientcomputern erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ba503-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="ba503-112">Wählen Sie für jede Richtlinie in der folgenden Tabelle die Option **Richtliniengruppe**aus, klicken Sie auf die **Richtlinie**, und konfigurieren Sie dann die **Einstellung**:</span><span class="sxs-lookup"><span data-stu-id="ba503-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="ba503-113">Richtliniengruppe</span><span class="sxs-lookup"><span data-stu-id="ba503-113">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="ba503-114">Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ba503-114">Policy</span></span></th>
    <th align="left"><span data-ttu-id="ba503-115">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ba503-115">Setting</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ba503-116">Clientverwaltung</span><span class="sxs-lookup"><span data-stu-id="ba503-116">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ba503-117">Konfigurieren von MBAM-Diensten</span><span class="sxs-lookup"><span data-stu-id="ba503-117">Configure MBAM Services</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ba503-118">Aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba503-118">Enabled.</span></span> <span data-ttu-id="ba503-119">Legen <strong> Sie MBAM-Wiederherstellungs-und Hardware Dienstendpunkt </strong> , und <strong> Wählen Sie BitLocker-Wiederherstellungsinformationen speichern aus </strong> .</span><span class="sxs-lookup"><span data-stu-id="ba503-119">Set <strong>MBAM Recovery and Hardware service endpoint</strong> and <strong>Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="ba503-120">Setzen <strong> Sie den MBAM-Konformitäts Dienstendpunkt </strong> , und geben Sie die Häufigkeit des Statusberichts in (Minuten) ein.</span><span class="sxs-lookup"><span data-stu-id="ba503-120">Set <strong>MBAM compliance service endpoint</strong> and Enter status report frequency in (minutes).</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ba503-121">Betriebs System Laufwerk</span><span class="sxs-lookup"><span data-stu-id="ba503-121">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ba503-122">Verschlüsselungseinstellungen für das Betriebssystemlaufwerk</span><span class="sxs-lookup"><span data-stu-id="ba503-122">Operating system drive encryption settings</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ba503-123">Aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba503-123">Enabled.</span></span> <span data-ttu-id="ba503-124">Legen <strong> Sie SELECT Protector für das Betriebssystemlaufwerk fest </strong> .</span><span class="sxs-lookup"><span data-stu-id="ba503-124">Set <strong>Select protector for operating system drive</strong>.</span></span> <span data-ttu-id="ba503-125">Erforderlich, um Betriebssystemlaufwerks Daten auf dem MBAMKey-Wiederherstellungsserver zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ba503-125">Required to save operating system drive data to the MBAMKey Recovery server.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ba503-126">Wechsellaufwerk</span><span class="sxs-lookup"><span data-stu-id="ba503-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ba503-127">Steuern der Verwendung von BitLocker auf Wechseldatenträgern</span><span class="sxs-lookup"><span data-stu-id="ba503-127">Control Use of BitLocker on removable drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ba503-128">Aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba503-128">Enabled.</span></span> <span data-ttu-id="ba503-129">Erforderlich, wenn MBAM Wechseldatenträger-Daten auf dem MBAM-Schlüssel Wiederherstellungsserver speichert.</span><span class="sxs-lookup"><span data-stu-id="ba503-129">Required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ba503-130">Festes Laufwerk</span><span class="sxs-lookup"><span data-stu-id="ba503-130">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ba503-131">Steuern der Verwendung von BitLocker auf Festplatten</span><span class="sxs-lookup"><span data-stu-id="ba503-131">Control Use of BitLocker on fixed drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ba503-132">Aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba503-132">Enabled.</span></span> <span data-ttu-id="ba503-133">Erforderlich, wenn MBAM Festplatten-Daten auf dem MBAM-Schlüssel Wiederherstellungsserver speichert.</span><span class="sxs-lookup"><span data-stu-id="ba503-133">Required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span></p>
    <p><span data-ttu-id="ba503-134">Legen <strong> Sie fest, wie BitLocker-geschützte Laufwerke wiederhergestellt </strong> und <strong> Daten Wiederherstellungs-Agent zugelassen werden können </strong> .</span><span class="sxs-lookup"><span data-stu-id="ba503-134">Set <strong>Choose how BitLocker-protected drives can be recovered</strong> and <strong>Allow data recovery agent</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="ba503-135">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ba503-135">Related topics</span></span>


[<span data-ttu-id="ba503-136">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ba503-136">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)









