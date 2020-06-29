---
title: Bearbeiten von UE-V-Einstellungsortvorlagen mit dem UE-V-Generator
description: Bearbeiten von UE-V-Einstellungsortvorlagen mit dem UE-V-Generator
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812160"
---
# <span data-ttu-id="62f3e-103">Bearbeiten von UE-V-Einstellungsortvorlagen mit dem UE-V-Generator</span><span class="sxs-lookup"><span data-stu-id="62f3e-103">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="62f3e-104">Verwenden Sie den Microsoft User Experience Virtualization (UE-V)-Generator, um Einstellungen für Standort Vorlagen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="62f3e-104">Use the Microsoft User Experience Virtualization (UE-V) Generator to edit settings location templates.</span></span> <span data-ttu-id="62f3e-105">Wenn die überarbeiteten Einstellungen den Vorlagen mithilfe des UE-V-Generators hinzugefügt werden, werden die Versionsinformationen in der Vorlage automatisch aktualisiert, um sicherzustellen, dass alle im Unternehmen bereitgestellten Vorlagen ordnungsgemäß aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="62f3e-105">When the revised settings are added to the templates using the UE-V Generator, the version information within the template is automatically updated to ensure that any existing templates deployed in the enterprise are updated correctly.</span></span>

**<span data-ttu-id="62f3e-106">So bearbeiten Sie eine Standort Vorlage für UE-v-Einstellungen mit dem UE-v-Generator</span><span class="sxs-lookup"><span data-stu-id="62f3e-106">How to edit a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="62f3e-107">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="62f3e-107">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="62f3e-108">Klicken Sie auf **Vorlage für Einstellungen bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="62f3e-108">Click **Edit a settings location template**.</span></span>

3.  <span data-ttu-id="62f3e-109">Wählen Sie in der Liste der zuletzt verwendeten Vorlagen die Vorlage aus, die bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="62f3e-109">In the list of recently used templates, select the template to be edited.</span></span> <span data-ttu-id="62f3e-110">**Wechseln Sie** Alternativ zur Einstellungs Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="62f3e-110">Alternatively, **Browse** to the settings template file.</span></span> <span data-ttu-id="62f3e-111">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-111">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="62f3e-112">Überprüfen Sie die **Eigenschaften**, die **Registrierungs** Speicherorte und die Speicherorte der **Dateien** für die Einstellungs Vorlage.</span><span class="sxs-lookup"><span data-stu-id="62f3e-112">Review the **Properties**, **Registry** locations, and **Files** locations for the settings template.</span></span> <span data-ttu-id="62f3e-113">Bearbeiten Sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="62f3e-113">Edit as needed.</span></span>

    -   <span data-ttu-id="62f3e-114">Auf der Registerkarte **Eigenschaften** können Sie die folgenden Eigenschaften anzeigen und bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="62f3e-114">The **Properties** tab allows you to view and edit the following properties:</span></span>

        -   <span data-ttu-id="62f3e-115">**Anwendungsname**: der Anwendungsname, der in der Beschreibung der Programmdatei Eigenschaften geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="62f3e-115">**Application name**: The application name written in the description of the program file properties.</span></span>

        -   <span data-ttu-id="62f3e-116">**Programmname**: der Name des Programms, das aus den Programmdatei Eigenschaften übernommen wurde.</span><span class="sxs-lookup"><span data-stu-id="62f3e-116">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="62f3e-117">Dieser Name hat in der Regel die Erweiterung ". exe".</span><span class="sxs-lookup"><span data-stu-id="62f3e-117">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="62f3e-118">**Produktversion**: die Produktversionsnummer der exe-Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="62f3e-118">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="62f3e-119">Mit dieser Eigenschaft können Sie zusammen mit der **Dateiversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-119">This property, together with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="62f3e-120">Diese Eigenschaft akzeptiert eine Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="62f3e-120">This property accepts a major version number.</span></span> <span data-ttu-id="62f3e-121">Wenn diese Eigenschaft leer ist, gilt die Vorlage für die Einstellungsposition für alle Versionen des Produkts.</span><span class="sxs-lookup"><span data-stu-id="62f3e-121">If this property is empty, then the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="62f3e-122">**Dateiversion**: die Dateiversionsnummer the.exe Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="62f3e-122">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="62f3e-123">Mit dieser Eigenschaft können Sie zusammen mit der **Produktversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-123">This property, along with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="62f3e-124">Diese Eigenschaft akzeptiert eine Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="62f3e-124">This property accepts a major version number.</span></span> <span data-ttu-id="62f3e-125">Wenn diese Eigenschaft leer ist, wird die Vorlage für die Einstellungsposition auf alle Versionen des Programms angewendet.</span><span class="sxs-lookup"><span data-stu-id="62f3e-125">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="62f3e-126">**Name der Vorlagen Autorin** (optional): der Name des Autors der Einstellungs Vorlage.</span><span class="sxs-lookup"><span data-stu-id="62f3e-126">**Template author name** (optional): The name of the settings template author.</span></span>

        -   <span data-ttu-id="62f3e-127">**E-Mail-Vorlage für Vorlagenautor** (optional): die e-Mail-Adresse der Vorlage "Speicherort für Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="62f3e-127">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="62f3e-128">Auf der Registerkarte " **Registrierung** " sind der **Schlüssel** und der **Bereich** der Registrierungsspeicherorte aufgeführt, die in der Vorlage "einstellungensort" enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="62f3e-128">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="62f3e-129">Sie können die Registrierungsspeicherorte mithilfe des Dropdownmenüs " **Aufgaben** " bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="62f3e-129">You can edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="62f3e-130">Aufgaben umfassen das Hinzufügen neuer Schlüssel, das Bearbeiten des Namens oder des Bereichs vorhandener Schlüssel, das Löschen von Schlüsseln und das Durchsuchen der Registrierung, in der sich die Schlüssel befinden.</span><span class="sxs-lookup"><span data-stu-id="62f3e-130">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry in which the keys are located.</span></span> <span data-ttu-id="62f3e-131">Wenn Sie den Bereich für die Registrierung definieren, können Sie den Bereich **alle Einstellungen** verwenden, um alle Registrierungseinstellungen unter dem angegebenen Schlüssel einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-131">When you define the scope for the registry, you can use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="62f3e-132">Verwenden Sie **alle Einstellungen** und unter **Schlüssel** , um alle Registrierungseinstellungen unter den angegebenen Tasten, Unterschlüsseln und Unterschlüssel Einstellungen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-132">Use **All Settings** and **Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="62f3e-133">Auf der Registerkarte " **Dateien** " werden der Dateipfad und die Dateimaske der Dateispeicherorte aufgeführt, die in der Vorlage für die Einstellungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="62f3e-133">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="62f3e-134">Sie können die Dateispeicherorte mithilfe des Dropdownmenüs " **Aufgaben** " bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="62f3e-134">You can edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="62f3e-135">Zu den Aufgaben für Dateispeicherorte gehören das Hinzufügen neuer Dateien oder Ordnerspeicherorte, das Bearbeiten des Bereichs vorhandener Dateien oder Ordner, das Löschen von Dateien oder Ordnern sowie das Öffnen des ausgewählten Speicherorts im Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="62f3e-135">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="62f3e-136">Wenn Sie alle Dateien in den angegebenen Ordner einbeziehen möchten, lassen Sie die Dateimaske leer.</span><span class="sxs-lookup"><span data-stu-id="62f3e-136">To include all files in the specified folder, leave the file mask empty.</span></span>

5.  <span data-ttu-id="62f3e-137">Klicken Sie auf **Speichern** , um die Änderungen an der Vorlage Speicherort für Einstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="62f3e-137">Click **Save** to save the changes to the settings location template.</span></span>

6.  <span data-ttu-id="62f3e-138">Klicken Sie auf **Schließen** , um den Assistenten für Einstellungs Vorlagen zu schließen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-138">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="62f3e-139">Beenden Sie die UE-V-Generator Anwendung.</span><span class="sxs-lookup"><span data-stu-id="62f3e-139">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="62f3e-140">Nachdem Sie die Vorlage für die Einstellungsposition für eine Anwendung bearbeitet haben, sollten Sie die Vorlage testen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-140">After editing the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="62f3e-141">Stellen Sie die überarbeiteten Einstellungen-Speicherort Vorlage in einer Lab-Umgebung bereit, bevor Sie Sie in der Produktion im Unternehmen einsetzen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-141">Deploy the revised settings location template in a lab environment before putting it into production in the enterprise.</span></span>

**<span data-ttu-id="62f3e-142">Manuelles Bearbeiten einer Speicherort Vorlage für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="62f3e-142">How to manually edit a settings location template</span></span>**

1.  <span data-ttu-id="62f3e-143">Erstellen Sie eine lokale Kopie der Vorlage für die Einstellungsposition (XML-Datei).</span><span class="sxs-lookup"><span data-stu-id="62f3e-143">Create a local copy of the settings location template (.xml file).</span></span> <span data-ttu-id="62f3e-144">Standort Vorlagen für UE-V-Einstellungen sind XML-Dateien, die die Speicherorte identifizieren, an denen Anwendungseinstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="62f3e-144">UE-V settings location templates are .xml files identifying the locations where application store settings values.</span></span>

2.  <span data-ttu-id="62f3e-145">Öffnen Sie die Datei mit einem XML-Editor für die Speicherort Vorlage für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-145">Open the settings location template file with an XML editor.</span></span>

3.  <span data-ttu-id="62f3e-146">Bearbeiten Sie die Vorlagendatei für die Einstellungsposition.</span><span class="sxs-lookup"><span data-stu-id="62f3e-146">Edit the settings location template file.</span></span> <span data-ttu-id="62f3e-147">Alle Änderungen müssen der in SettingsLocationTempate. XSD definierten UE-V-Schemadatei entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62f3e-147">All changes must conform to the UE-V schema file defined in SettingsLocationTempate.xsd.</span></span> <span data-ttu-id="62f3e-148">Eine Kopie der XSD-Datei befindet sich `\ProgramData\Microsoft\UEV\Templates` standardmäßig in.</span><span class="sxs-lookup"><span data-stu-id="62f3e-148">A copy of the .xsd file is located in `\ProgramData\Microsoft\UEV\Templates` by default.</span></span>

4.  <span data-ttu-id="62f3e-149">Speichern Sie die Vorlagendatei für die Einstellungsposition, und schließen Sie den XML-Editor.</span><span class="sxs-lookup"><span data-stu-id="62f3e-149">Save the settings location template file and close the XML editor.</span></span>

5.  <span data-ttu-id="62f3e-150">Überprüfen Sie die Speicherort Vorlagendatei für geänderte Einstellungen mit dem UE-V-Generator.</span><span class="sxs-lookup"><span data-stu-id="62f3e-150">Validate the modified settings location template file with the UE-V Generator.</span></span> <span data-ttu-id="62f3e-151">Weitere Informationen zum Überprüfen mit dem UE-v-Generator finden Sie unter über [Prüfen von Standort Vorlagen für UE-v-Einstellungen mit dem UE-v-Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span><span class="sxs-lookup"><span data-stu-id="62f3e-151">For more information about validating with the UE-V Generator, see [Validate UE-V Settings Location Templates with UE-V Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span></span>

## <span data-ttu-id="62f3e-152">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="62f3e-152">Related topics</span></span>


[<span data-ttu-id="62f3e-153">Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator</span><span class="sxs-lookup"><span data-stu-id="62f3e-153">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="62f3e-154">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="62f3e-154">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





