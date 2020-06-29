---
title: Konfigurieren von erweiterten Einstellungen mit Windows PowerShell
description: Konfigurieren von erweiterten Einstellungen mit Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812328"
---
# <span data-ttu-id="759fc-103">Konfigurieren von erweiterten Einstellungen mit Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="759fc-103">Configuring Advanced Settings by Using Windows PowerShell</span></span>


<span data-ttu-id="759fc-104">Das von Ihnen erstellte Med-v-Arbeitsbereichs Paket enthält eine Windows PowerShell-Skriptdatei (ps1), die Sie bearbeiten können, bevor Sie Ihr Med-v-Arbeitsbereichs Paket testen und bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="759fc-104">The MED-V workspace package that you create includes a Windows PowerShell script (.ps1) file that you can edit before you test and deploy your MED-V workspace package.</span></span> <span data-ttu-id="759fc-105">Dieser Abschnitt enthält Informationen und Anleitungen, die Ihnen bei der Verwaltung von Med-v-Konfigurationseinstellungen mithilfe von Windows PowerShell helfen, bevor Sie die Med-v-Arbeitsbereiche bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="759fc-105">This section provides information and guidance to help you manage MED-V configuration settings by using Windows PowerShell before you deploy the MED-V workspaces.</span></span>

## <span data-ttu-id="759fc-106">Verwenden von Windows PowerShell-Cmdlets in MED-V</span><span class="sxs-lookup"><span data-stu-id="759fc-106">Using Windows PowerShell Cmdlets in MED-V</span></span>


<span data-ttu-id="759fc-107">Die folgenden Windows PowerShell-Cmdlets stehen in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="759fc-107">The following Windows PowerShell cmdlets are available in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

**<span data-ttu-id="759fc-108">Neu – MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="759fc-108">New-MedvConfiguration</span></span>**

**<span data-ttu-id="759fc-109">Export-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="759fc-109">Export-MedvConfiguration</span></span>**

**<span data-ttu-id="759fc-110">Neu – MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="759fc-110">New-MedvWorkspace</span></span>**

**<span data-ttu-id="759fc-111">Export-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="759fc-111">Export-MedvWorkspace</span></span>**

<span data-ttu-id="759fc-112">Wenn Sie auf Windows PowerShell-Cmdlets für med-v zugreifen möchten, öffnen Sie Windows PowerShell, und geben Sie den folgenden Befehl ein, um die Med-v-Module zu importieren.</span><span class="sxs-lookup"><span data-stu-id="759fc-112">To access Windows PowerShell cmdlets for MED-V, open Windows PowerShell and type the following command to import the MED-V modules.</span></span>

``` syntax
Import-Module microsoft.medv
```

<span data-ttu-id="759fc-113">Nachdem die Module importiert wurden, können Sie mithilfe der Windows PowerShell-Standardhilfe Befehle **Mann** oder **Get-Help**auf die Inline Hilfe für die Cmdlets zugreifen.</span><span class="sxs-lookup"><span data-stu-id="759fc-113">After the modules are imported, you can access inline help for the cmdlets by using the standard Windows PowerShell Help commands, **man** or **get-help**.</span></span> <span data-ttu-id="759fc-114">Wenn Sie beispielsweise auf eine Beschreibung des Cmdlets **New-MedvConfiguration** einschließlich einer vollständigen Liste der verfügbaren Parameter zugreifen möchten, geben Sie den folgenden Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="759fc-114">For example, to access a description of the **New-MedvConfiguration** cmdlet including a complete list of available parameters, type the following command.</span></span>

``` syntax
get-help New-MedvConfiguration
```

<span data-ttu-id="759fc-115">Sie können auch Hilfe zu bestimmten Parametern anzeigen.</span><span class="sxs-lookup"><span data-stu-id="759fc-115">You can also view help for specific parameters.</span></span> <span data-ttu-id="759fc-116">Wenn Sie beispielsweise Hilfe für den Parameter VmMemory anzeigen möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="759fc-116">For example, to view help for the parameter VmMemory, type the following:</span></span>

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

<span data-ttu-id="759fc-117">Um eine Liste aller MED-V-Konfigurationseinstellungen und deren Standardeinstellungen anzuzeigen, geben Sie den folgenden Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="759fc-117">To view a list of all MED-V configuration settings and their defaults, type the following command.</span></span>

``` syntax
New-MedvConfiguration -ForceDefaults
```

<span data-ttu-id="759fc-118">Um eine Liste aller MED-V-Konfigurationseinstellungen und deren aktuellen Werte anzuzeigen, geben Sie den folgenden Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="759fc-118">To view a list of all MED-V configuration settings and their current values, type the following command.</span></span>

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## <span data-ttu-id="759fc-119">Erstellen eines MED-V-Arbeitsbereichs mit benutzerdefinierten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="759fc-119">Creating a MED-V Workspace with Custom Settings</span></span>


<span data-ttu-id="759fc-120">Nachdem Sie ein Med-v-Arbeitsbereichs Paket erfolgreich mithilfe des Med-v-Arbeitsbereichs-Packagers erstellt haben, wird ein Windows PowerShell-Skript in dem Ordner generiert, den Sie zum Speichern der Packager-Dateien angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="759fc-120">After you successfully create a MED-V workspace package by using the MED-V Workspace Packager, a Windows PowerShell script is generated in the folder you specified for saving your packager files.</span></span> <span data-ttu-id="759fc-121">Der Inhalt dieses Skripts zeigt einige der verfügbaren MED-V-Konfigurationseinstellungen, die Sie bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="759fc-121">The contents of this script show some of the available MED-V configuration settings that you can edit.</span></span>

<span data-ttu-id="759fc-122">Mit den folgenden Schritten können Sie das Skript anpassen und es dann in Windows PowerShell ausführen, um einen MED-V-Arbeitsbereich mit den neuen Einstellungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="759fc-122">Following these steps, you can customize the script and then run it in Windows PowerShell to create a MED-V workspace with the new settings.</span></span>

<span data-ttu-id="759fc-123">**Wichtig**  Führen Sie Windows PowerShell mit administrativen Anmeldeinformationen aus, und stellen Sie sicher, dass die Windows PowerShell-Ausführungsrichtlinie die Ausführung von Skripts ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="759fc-123">**Important** Run Windows PowerShell with administrative credentials, and ensure that the Windows PowerShell execution policy allows the running of scripts.</span></span>

1.  <span data-ttu-id="759fc-124">Bearbeiten Sie das Windows PowerShell-Skript, das vom MED-V Workspace-Paket erstellt wurde, oder erstellen Sie ein neues Skript mit den gewünschten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="759fc-124">Edit the Windows PowerShell script that was generated by the MED-V Workspace Packager, or author a new script with the configuration settings that you want.</span></span>

2.  <span data-ttu-id="759fc-125">Führen Sie Windows PowerShell mit administrativen Anmeldeinformationen aus, und geben Sie an der Eingabeaufforderung den folgenden Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="759fc-125">Run Windows PowerShell with administrative credentials and at the command prompt, type the following command.</span></span>

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    <span data-ttu-id="759fc-126">Dieser Befehl führt das Windows PowerShell-Skript aus und führt das Cmdlet **New-MedvWorkspace** aus, um ein neues MED-V-Arbeitsbereichs Paket zu generieren.</span><span class="sxs-lookup"><span data-stu-id="759fc-126">This command runs the Windows PowerShell script and runs the **New-MedvWorkspace** cmdlet to generate a new MED-V workspace package.</span></span> <span data-ttu-id="759fc-127">Die neuen Packager-Dateien werden in dem Ordner gespeichert, den Sie ursprünglich für das Speichern Ihrer MED-V Workspace-Paketdateien angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="759fc-127">The new packager files are saved in the folder that you originally specified for storing your MED-V Workspace Packager files.</span></span> <span data-ttu-id="759fc-128">Weitere Hilfe zu diesem Cmdlet finden Sie in der Hilfe zu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="759fc-128">For additional help about this cmdlet, see the Windows PowerShell Help.</span></span>

 

## <span data-ttu-id="759fc-129">Exportieren einer MED-V-Konfiguration in eine Registrierungsdatei</span><span class="sxs-lookup"><span data-stu-id="759fc-129">Exporting a MED-V Configuration to a Registry File</span></span>


<span data-ttu-id="759fc-130">Sie können die Med-v-Konfigurationseinstellungen aktualisieren, nachdem der Med-v-Arbeitsbereich installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="759fc-130">You can update MED-V configuration settings after the MED-V workspace is installed.</span></span> <span data-ttu-id="759fc-131">Verwenden Sie das Cmdlet **New-MedvConfiguration** , um die Parameter anzugeben, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="759fc-131">Use the **New-MedvConfiguration** cmdlet to specify the parameters that you want to change.</span></span> <span data-ttu-id="759fc-132">Geben Sie beispielsweise die folgenden Befehle ein, um eine Registrierungsdatei zu erstellen, die die Speichereinstellung für den virtuellen Computer ändert.</span><span class="sxs-lookup"><span data-stu-id="759fc-132">For example, to create a registry file that changes the virtual machine memory setting, type the following commands.</span></span>

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

<span data-ttu-id="759fc-133">Sie können die resultierende Registrierungsdatei vom Hostcomputer in einen MED-V-Arbeitsbereich importieren, um die neuen Konfigurationseinstellungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="759fc-133">You can import the resultant registry file from the host computer to a MED-V workspace to apply the new configuration settings.</span></span>

## <span data-ttu-id="759fc-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="759fc-134">Related topics</span></span>


[<span data-ttu-id="759fc-135">Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="759fc-135">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="759fc-136">Testen und Bereitstellen des MED-V-Arbeitsbereichspakets</span><span class="sxs-lookup"><span data-stu-id="759fc-136">Test And Deploy the MED-V Workspace Package</span></span>](test-and-deploy-the-med-v-workspace-package.md)

 

 





