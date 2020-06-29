---
title: So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0
description: So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810462"
---
# <span data-ttu-id="a2e69-103">So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a2e69-103">How to Edit MBAM 1.0 GPO Settings</span></span>


<span data-ttu-id="a2e69-104">Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erfolgreich bereitstellen möchten, müssen Sie zunächst die Gruppenrichtlinien ermitteln, die Sie bei der Implementierung der Microsoft BitLocker-Verwaltung und-Überwachung verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="a2e69-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="a2e69-105">Weitere Informationen zu den verschiedenen verfügbaren Richtlinien finden Sie unter [Planen von MBAM 1,0-Gruppenrichtlinienanforderungen](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a2e69-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="a2e69-106">Nachdem Sie die Richtlinien festgelegt haben, die Sie verwenden möchten, müssen Sie ein oder mehrere Gruppenrichtlinienobjekte, die die MBAM-Richtlinieneinstellungen enthalten, ändern.</span><span class="sxs-lookup"><span data-stu-id="a2e69-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the MBAM policy settings.</span></span>

<span data-ttu-id="a2e69-107">In den folgenden Schritten wird beschrieben, wie Sie die Standardeinstellungen für Gruppenrichtlinienobjekte konfigurieren, damit MBAM die BitLocker-Verschlüsselung für die Clientcomputer Ihrer Organisation verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a2e69-107">The following steps describe how to configure the basic, recommended Group Policy object (GPO) settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="a2e69-108">So bearbeiten Sie die Einstellungen für das MBAM-Client-GPO</span><span class="sxs-lookup"><span data-stu-id="a2e69-108">To edit the MBAM Client GPO settings</span></span>**

1.  <span data-ttu-id="a2e69-109">Stellen Sie auf einem Computer, auf dem MBAM-Gruppenrichtlinienvorlage installiert ist, sicher, dass MBAM-Dienste aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="a2e69-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="a2e69-110">Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (GPMC. msc) oder das erweiterte MDOP-Produkt für Gruppenrichtlinienverwaltung (AGPM) für diese Aktionen: Wählen Sie **Computer Konfiguration**aus, wählen Sie **Richtlinien**aus, klicken Sie auf **Administrative Vorlagen**, wählen Sie **Windows-Komponenten**aus, und klicken Sie dann auf **MDOP MBAM (BitLocker-Verwaltung)**.</span><span class="sxs-lookup"><span data-stu-id="a2e69-110">Use the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product for these actions: Select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="a2e69-111">Bearbeiten Sie die Einstellungen für Gruppenrichtlinienobjekte, die zum Aktivieren von MBAM-Clientdiensten auf Clientcomputern erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a2e69-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="a2e69-112">Wählen Sie für jede Richtlinie in der folgenden Tabelle die Option **Richtliniengruppe**aus, klicken Sie auf die **Richtlinie**, und konfigurieren Sie dann die **Einstellung**.</span><span class="sxs-lookup"><span data-stu-id="a2e69-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**.</span></span>

    <span data-ttu-id="a2e69-113">Richtliniengruppe</span><span class="sxs-lookup"><span data-stu-id="a2e69-113">Policy Group</span></span>

    <span data-ttu-id="a2e69-114">Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a2e69-114">Policy</span></span>

    <span data-ttu-id="a2e69-115">Einstellung</span><span class="sxs-lookup"><span data-stu-id="a2e69-115">Setting</span></span>

    <span data-ttu-id="a2e69-116">Clientverwaltung</span><span class="sxs-lookup"><span data-stu-id="a2e69-116">Client Management</span></span>

    <span data-ttu-id="a2e69-117">Konfigurieren von MBAM-Diensten</span><span class="sxs-lookup"><span data-stu-id="a2e69-117">Configure MBAM Services</span></span>

    <span data-ttu-id="a2e69-118">Aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2e69-118">Enabled.</span></span> <span data-ttu-id="a2e69-119">Legen Sie **MBAM-Wiederherstellungs-und Hardware Dienstendpunkt** , und **Wählen Sie BitLocker-Wiederherstellungsinformationen speichern aus**.</span><span class="sxs-lookup"><span data-stu-id="a2e69-119">Set **MBAM Recovery and Hardware service endpoint** and **Select BitLocker recovery information to store**.</span></span>

    <span data-ttu-id="a2e69-120">Setzen Sie den **MBAM-Konformitäts Dienstendpunkt** , und **Geben Sie die Häufigkeit des Statusberichts in (Minuten) ein**.</span><span class="sxs-lookup"><span data-stu-id="a2e69-120">Set **MBAM compliance service endpoint** and **Enter status report frequency in (minutes)**.</span></span>

    <span data-ttu-id="a2e69-121">Hardware Kompatibilitätsüberprüfung zulassen</span><span class="sxs-lookup"><span data-stu-id="a2e69-121">Allow hardware compatibility checking</span></span>

    <span data-ttu-id="a2e69-122">Deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2e69-122">Disabled.</span></span> <span data-ttu-id="a2e69-123">Diese Richtlinie ist standardmäßig aktiviert, wird aber für eine grundlegende MBAM-Implementierung nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="a2e69-123">This policy is enabled by default, but is not needed for a basic MBAM implementation.</span></span>

    <span data-ttu-id="a2e69-124">Betriebs System Laufwerk</span><span class="sxs-lookup"><span data-stu-id="a2e69-124">Operating System Drive</span></span>

    <span data-ttu-id="a2e69-125">Verschlüsselungseinstellungen für das Betriebssystemlaufwerk</span><span class="sxs-lookup"><span data-stu-id="a2e69-125">Operating system drive encryption settings</span></span>

    <span data-ttu-id="a2e69-126">Aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2e69-126">Enabled.</span></span> <span data-ttu-id="a2e69-127">Legen **Sie SELECT Protector für das Betriebssystemlaufwerk**fest.</span><span class="sxs-lookup"><span data-stu-id="a2e69-127">Set **Select protector for operating system drive**.</span></span> <span data-ttu-id="a2e69-128">Dies ist erforderlich, um Betriebssystemlaufwerks Daten auf dem MBAM-Schlüssel Wiederherstellungsserver zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a2e69-128">This is required to save operating system drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="a2e69-129">Wechsellaufwerk</span><span class="sxs-lookup"><span data-stu-id="a2e69-129">Removable Drive</span></span>

    <span data-ttu-id="a2e69-130">Steuern der Verwendung von BitLocker auf Wechseldatenträgern</span><span class="sxs-lookup"><span data-stu-id="a2e69-130">Control Use of BitLocker on removable drives</span></span>

    <span data-ttu-id="a2e69-131">Aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2e69-131">Enabled.</span></span> <span data-ttu-id="a2e69-132">Diese Vorgehensweise ist erforderlich, wenn MBAM Wechseldatenträger auf dem MBAM-Schlüssel Wiederherstellungsserver speichert.</span><span class="sxs-lookup"><span data-stu-id="a2e69-132">This is required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="a2e69-133">Festes Laufwerk</span><span class="sxs-lookup"><span data-stu-id="a2e69-133">Fixed Drive</span></span>

    <span data-ttu-id="a2e69-134">Steuern der Verwendung von BitLocker auf Festplatten</span><span class="sxs-lookup"><span data-stu-id="a2e69-134">Control Use of BitLocker on fixed drives</span></span>

    <span data-ttu-id="a2e69-135">Aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2e69-135">Enabled.</span></span> <span data-ttu-id="a2e69-136">Diese Vorgehensweise ist erforderlich, wenn MBAM Festplatten-Daten auf dem MBAM-Schlüssel Wiederherstellungsserver speichert.</span><span class="sxs-lookup"><span data-stu-id="a2e69-136">This is required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="a2e69-137">Legen **Sie fest, wie BitLocker-geschützte Laufwerke wiederhergestellt** und **Daten Wiederherstellungs-Agent zugelassen**werden können.</span><span class="sxs-lookup"><span data-stu-id="a2e69-137">Set **Choose how BitLocker-protected drives can be recovered** and **Allow data recovery agent**.</span></span>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="a2e69-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a2e69-138">Related topics</span></span>


[<span data-ttu-id="a2e69-139">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a2e69-139">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)









