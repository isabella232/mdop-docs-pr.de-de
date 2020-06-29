---
title: Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0
description: Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808608"
---
# <span data-ttu-id="112fe-103">Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="112fe-103">Planning for Custom Template Deployment for UE-V 1.0</span></span>


<span data-ttu-id="112fe-104">Microsoft User Experience Virtualization (UE-v) verwendet Einstellungen-Standort Vorlagen (XML-Dateien), die die Einstellungen definieren, die von UE-v erfasst und angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="112fe-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="112fe-105">Sie können den UE-v-Generator verwenden, um benutzerdefinierte Standort Vorlagen für Einstellungen zu erstellen, mit denen Benutzer die Einstellungen anderer Anwendungen als die in den Standard-UE-V-Vorlagen enthaltenen Einstellungen durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="112fe-105">You can use the UE-V Generator to create custom settings location templates that let users roam the settings of applications other than those that are included in the default UE-V templates.</span></span> <span data-ttu-id="112fe-106">Nachdem Sie die benutzerdefinierte Vorlage getestet haben, um sicherzustellen, dass die Anwendungseinstellungen in einer Testumgebung ordnungsgemäß durchlaufen, können Sie diese Einstellungen Speicherort Vorlagen auf Computern im Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="112fe-106">After you test the custom template to ensure that the application settings roam correctly in a test environment, you can deploy these settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="112fe-107">Sie können die Speicherort Vorlagen für benutzerdefinierte Einstellungen mit einer vorhandenen Bereitstellungsinfrastruktur wie Enterprise Software Distribution (ESD), Gruppenrichtlinieneinstellungen oder durch Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="112fe-107">You can deploy your custom settings location templates with an existing deployment infrastructure, such as Enterprise Software Distribution (ESD), with Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="112fe-108">Vorlagen, die mithilfe von ESD-oder Gruppenrichtlinien bereitgestellt werden, müssen bei UE-V WMI oder PowerShell registriert sein.</span><span class="sxs-lookup"><span data-stu-id="112fe-108">Templates that are deployed by using ESD or Group Policy must be registered with UE-V WMI or PowerShell.</span></span>

## <span data-ttu-id="112fe-109">Vorlagenkatalog für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="112fe-109">Settings template catalog</span></span>


<span data-ttu-id="112fe-110">Der Katalog der Benutzeroberflächen-Virtualisierungs-Einstellungen ist ein Ordnerpfad auf UE-V-Computern oder eine SMB-Netzwerkfreigabe (Server Message Block), in der alle Speicherorte für benutzerdefinierte Einstellungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="112fe-110">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="112fe-111">Der UE-V-Agent ruft neue oder aktualisierte Vorlagen von diesem Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="112fe-111">The UE-V agent retrieves new or updated templates from this location.</span></span> <span data-ttu-id="112fe-112">Der UE-V-Agent überprüft diesen Speicherort einmal täglich und aktualisiert sein Synchronisierungsverhalten basierend auf den Vorlagen in diesem Ordner.</span><span class="sxs-lookup"><span data-stu-id="112fe-112">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="112fe-113">Vorlagen, die seit dem letzten Überprüfen des Ordners in diesem Ordner hinzugefügt oder aktualisiert wurden, werden vom UE-V-Agent registriert.</span><span class="sxs-lookup"><span data-stu-id="112fe-113">Templates that were added or updated in this folder since the last time that the folder was checked are registered by the UE-V agent.</span></span> <span data-ttu-id="112fe-114">Der UE-V-Agent hebt die Registrierung von Vorlagen auf, die aus diesem Ordner entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="112fe-114">The UE-V agent deregisters templates that are removed from this folder.</span></span> <span data-ttu-id="112fe-115">Standardmäßig werden Vorlagen um 3:30 Uhr einmal pro Tag registriert und nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="112fe-115">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="112fe-116">Ortszeit durch den Aufgabenplaner.</span><span class="sxs-lookup"><span data-stu-id="112fe-116">local time by the task scheduler.</span></span> <span data-ttu-id="112fe-117">Weitere Informationen zu den UE-v-Aufgaben finden Sie unter [Ändern der Häufigkeit von geplanten UE-v-Aufgaben](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="112fe-117">For more information about the UE-V tasks, see [Changing the Frequency of UE-V Scheduled Tasks](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span></span>

<span data-ttu-id="112fe-118">Sie können den Katalogpfad der Einstellungs Vorlage mithilfe der Befehlszeilenoptionen "installieren", "Gruppenrichtlinie", "WMI" oder "PowerShell" konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="112fe-118">You can configure the settings template catalog path by using the install command-line options, Group Policy, WMI, or PowerShell.</span></span> <span data-ttu-id="112fe-119">Vorlagen, die im Katalogpfad für Einstellungs Vorlagen gespeichert sind, werden automatisch von einem geplanten Vorgang registriert und nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="112fe-119">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span> <span data-ttu-id="112fe-120">Sie können diesen geplanten Task nach Bedarf anpassen.</span><span class="sxs-lookup"><span data-stu-id="112fe-120">You can customize this scheduled task as needed.</span></span>

## <span data-ttu-id="112fe-121">Ersetzen der standardmäßigen Microsoft-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="112fe-121">Replace the default Microsoft templates</span></span>


<span data-ttu-id="112fe-122">Der UE-V-Agent installiert eine Standardgruppe von Einstellungen-Standort Vorlagen für allgemeine Microsoft-Anwendungen und Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="112fe-122">The UE-V agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="112fe-123">Wenn Ihr Unternehmen angepasste Versionen dieser Vorlagen benötigt, kann der UE-V-Agent so konfiguriert werden, dass ein Einstellungs Vorlagenkatalog verwendet wird, und Sie sollten die standardmäßigen Microsoft-Vorlagen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="112fe-123">If your enterprise needs customized versions of these templates, the UE-V agent can be configured to use a settings template catalog and you should then replace the default Microsoft templates.</span></span>

<span data-ttu-id="112fe-124">Während der Installation des UE-V-Agents kann der Befehlszeilenparameter `RegisterMSTemplates` verwendet werden, um die Registrierung der Microsoft-Standardvorlagen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="112fe-124">During the installation of the UE-V agent, the command-line parameter, `RegisterMSTemplates`, can be used to disable the registration of the default Microsoft templates.</span></span> <span data-ttu-id="112fe-125">Weitere Informationen zum Einrichten der UE-v-Parameter finden Sie unter [Planen der UE-v-Konfigurationsmethoden](planning-for-ue-v-configuration-methods.md).</span><span class="sxs-lookup"><span data-stu-id="112fe-125">For more information about how to set the UE-V parameters, see [Planning for UE-V Configuration Methods](planning-for-ue-v-configuration-methods.md).</span></span>

<span data-ttu-id="112fe-126">Wenn Sie Gruppenrichtlinien zum Konfigurieren des Katalog Pfads für Einstellungs Vorlagen verwenden, können Sie auswählen, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="112fe-126">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="112fe-127">Wenn Sie die Richtlinieneinstellungen so konfigurieren, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden, werden alle Microsoft-Standardvorlagen, die vom UE-V-Agent installiert werden, auf dem Computer gelöscht, und es werden nur die Vorlagen verwendet, die sich im Katalog der Einstellungs Vorlagen befinden.</span><span class="sxs-lookup"><span data-stu-id="112fe-127">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V agent will be deleted from the computer, and only the templates that are located in the settings template catalog will be used.</span></span> <span data-ttu-id="112fe-128">Um die standardmäßige Microsoft-Vorlage außer Kraft setzen zu können, muss die Konfigurationseinstellung UE-V-Agent `RegisterMSTemplates` auf true festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="112fe-128">The UE-V Agent configuration setting `RegisterMSTemplates` must be set to true in order to override the default Microsoft template.</span></span>

<span data-ttu-id="112fe-129">**Hinweis**  Wenn Sie diese Richtlinieneinstellung nach der Aktivierung deaktivieren, wird der UE-V-Agent die standardmäßigen Microsoft-Vorlagen nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="112fe-129">**Note** If you disable this policy setting after it has been enabled, the UE-V agent will not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="112fe-130">Wenn im Einstellungs Vorlagenkatalog angepasste Vorlagen vorhanden sind, die die gleiche ID wie die standardmäßigen Microsoft-Vorlagen verwenden und der UE-V-Agent nicht so konfiguriert ist, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden, werden die Microsoft-Vorlagen im Katalog ignoriert.</span><span class="sxs-lookup"><span data-stu-id="112fe-130">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V agent is not configured to replace the default Microsoft templates, the Microsoft templates in the catalog will be ignored.</span></span>

<span data-ttu-id="112fe-131">Sie können die Standardvorlagen auch mithilfe der Features UE-V PowerShell ersetzen.</span><span class="sxs-lookup"><span data-stu-id="112fe-131">You can also replace the default templates by using the UE-V PowerShell features.</span></span> <span data-ttu-id="112fe-132">Wenn Sie die standardmäßige Microsoft-Vorlage durch PowerShell ersetzen möchten, heben Sie die Registrierung aller Microsoft-Standardvorlagen auf, und registrieren Sie dann die angepassten Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="112fe-132">To replace the default Microsoft Template with PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="112fe-133">**Hinweis**  Alte Einstellungs Pakete verbleiben im Einstellungs Speicherort, auch wenn neue Einstellungs Vorlagen für eine Anwendung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="112fe-133">**Note** Old settings packages remain in the settings storage location even if new settings templates are deployed for an application.</span></span> <span data-ttu-id="112fe-134">Diese Pakete werden nicht vom Agenten gelesen, aber auch nicht automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="112fe-134">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <span data-ttu-id="112fe-135">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="112fe-135">Related topics</span></span>


[<span data-ttu-id="112fe-136">Planen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="112fe-136">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="112fe-137">Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="112fe-137">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

[<span data-ttu-id="112fe-138">Planen für UE-V-Konfigurationsmethoden</span><span class="sxs-lookup"><span data-stu-id="112fe-138">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

<span data-ttu-id="112fe-139">Planen der Bereitstellung von benutzerdefinierten Vorlagen</span><span class="sxs-lookup"><span data-stu-id="112fe-139">Planning for Custom Template Deployment</span></span>
 

 





