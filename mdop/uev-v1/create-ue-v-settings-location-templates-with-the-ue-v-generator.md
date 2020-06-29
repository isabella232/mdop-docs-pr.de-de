---
title: Erstellen von UE-V-Einstellungsortvorlagen mit UE-V-Generator
description: Erstellen von UE-V-Einstellungsortvorlagen mit UE-V-Generator
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811878"
---
# <span data-ttu-id="11ad5-103">Erstellen von UE-V-Einstellungsortvorlagen mit UE-V-Generator</span><span class="sxs-lookup"><span data-stu-id="11ad5-103">Create UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="11ad5-104">Microsoft User Experience Virtualization (UE-V) verwendet *Einstellungen für Standort Vorlagen* , um Anwendungseinstellungen zwischen Benutzercomputern zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-104">Microsoft User Experience Virtualization (UE-V) uses *settings location templates* to roam application settings between user computers.</span></span> <span data-ttu-id="11ad5-105">Einige Standardeinstellungen für Standort Vorlagen sind in der Virtualisierung der Benutzeroberfläche enthalten.</span><span class="sxs-lookup"><span data-stu-id="11ad5-105">Some standard settings location templates are included with User Experience Virtualization.</span></span> <span data-ttu-id="11ad5-106">Sie können mit dem UE-V-Generator auch benutzerdefinierte Standort Vorlagen erstellen, bearbeiten oder überprüfen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-106">You can also create, edit, or validate custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="11ad5-107">Der UE-V-Generator überwacht eine Anwendung, um die Speicherorte, an denen die Anwendung Ihre Einstellungen speichert, zu ermitteln und zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-107">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="11ad5-108">Die Anwendung, die überwacht wird, muss eine herkömmliche Anwendung sein.</span><span class="sxs-lookup"><span data-stu-id="11ad5-108">The application that is being monitored must be a traditional application.</span></span> <span data-ttu-id="11ad5-109">Der UE-V-Generator kann keine Vorlage für eine Einstellungsposition aus den folgenden Anwendungstypen erstellen:</span><span class="sxs-lookup"><span data-stu-id="11ad5-109">The UE-V Generator cannot create a settings location template from the following application types:</span></span>

-   <span data-ttu-id="11ad5-110">Virtualisierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="11ad5-110">Virtualized applications</span></span>

-   <span data-ttu-id="11ad5-111">Über die Terminaldienste angebotene Anwendung</span><span class="sxs-lookup"><span data-stu-id="11ad5-111">Application offered through terminal services</span></span>

-   <span data-ttu-id="11ad5-112">Java-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="11ad5-112">Java applications</span></span>

-   <span data-ttu-id="11ad5-113">Windows 8-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="11ad5-113">Windows 8 applications</span></span>

<span data-ttu-id="11ad5-114">**Hinweis**  UE-V-Vorlagen können nicht aus virtualisierten Anwendungen oder Terminaldienste-Anwendungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="11ad5-114">**Note** UE-V templates cannot be created from virtualized applications or terminal services applications.</span></span> <span data-ttu-id="11ad5-115">Einstellungen, die mithilfe der Vorlagen synchronisiert werden, können jedoch auf diese Anwendungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="11ad5-115">However, settings synchronized using the templates can be applied to those applications.</span></span> <span data-ttu-id="11ad5-116">Öffnen Sie zum Erstellen von Vorlagen, die die Virtual Desktop Infrastructure (VDI)-und Terminaldienste-Anwendungen unterstützen, eine Windows Installer-Datei (MSI)-Version der Anwendung mit dem UE-V-Generator.</span><span class="sxs-lookup"><span data-stu-id="11ad5-116">To create templates that support Virtual Desktop Infrastructure (VDI) and terminal services applications, open a Windows Installer File (.msi) version of the application with UE-V Generator.</span></span>

 

**<span data-ttu-id="11ad5-117">Ausgeschlossene Speicherorte</span><span class="sxs-lookup"><span data-stu-id="11ad5-117">Excluded Locations</span></span>**

<span data-ttu-id="11ad5-118">Der Ermittlungsprozess schließt Speicherorte aus, die häufig Anwendungssoftware Dateien speichern, die nicht gut zwischen Benutzercomputern oder Umgebungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="11ad5-118">The discovery process excludes locations which commonly store application software files that do not roam well between user computers or environments.</span></span> <span data-ttu-id="11ad5-119">Folgende Punkte sind ausgeschlossen:</span><span class="sxs-lookup"><span data-stu-id="11ad5-119">The following are excluded:</span></span>

-   <span data-ttu-id="11ad5-120">HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, für die der angemeldete Benutzer keine Werte schreiben kann</span><span class="sxs-lookup"><span data-stu-id="11ad5-120">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="11ad5-121">HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, die der Kernfunktionalität des Windows-Betriebssystems zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="11ad5-121">HKEY\_CURRENT\_USER registry keys and files associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="11ad5-122">Alle Registrierungsschlüssel, die sich im HKEY \ _LOCAL \ _MACHINE Hive befinden</span><span class="sxs-lookup"><span data-stu-id="11ad5-122">All registry keys located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="11ad5-123">Dateien, die sich in Verzeichnissen von Programmdateien befinden</span><span class="sxs-lookup"><span data-stu-id="11ad5-123">Files located in Program Files directories</span></span>

-   <span data-ttu-id="11ad5-124">Dateien, die sich in den Benutzern befinden \ \ \ [Benutzername \] \ \ APPDATA \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="11ad5-124">Files located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="11ad5-125">Windows-Betriebssystemdateien in% SystemRoot%</span><span class="sxs-lookup"><span data-stu-id="11ad5-125">Windows operating system files located in %systemroot%</span></span>

<span data-ttu-id="11ad5-126">Wenn Registrierungsschlüssel und Dateien, die in diesen ausgeschlossenen Speicherorten gespeichert sind, benötigt werden, um die Anwendungseinstellungen zu durchlaufen, können Administratoren die Speicherorte während des Vorlagen Erstellungsprozesses manuell zur Einstellungs Speicherort Vorlage hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-126">If registry keys and files stored in these excluded locations are required in order to roam application settings, administrators can manually add the locations to the settings location template during the template creation process.</span></span>

## <span data-ttu-id="11ad5-127">Erstellen von UE-V-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="11ad5-127">Create UE-V templates</span></span>


<span data-ttu-id="11ad5-128">Verwenden Sie den UE-V-Generator zum Erstellen von Einstellungen-Speicherort Vorlagen für Branchenanwendungen oder andere Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-128">Use the UE-V Generator to create settings location templates for line-of-business applications or other applications.</span></span> <span data-ttu-id="11ad5-129">Nachdem die Vorlage für eine Anwendung erstellt wurde, können Sie die Vorlage auf Computern bereitstellen, damit Benutzer die Einstellungen für diese Anwendung durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="11ad5-129">After the template for an application is created, you can deploy the template to computers so users can roam the settings for that application.</span></span>

**<span data-ttu-id="11ad5-130">So erstellen Sie eine Standort Vorlage für UE-v-Einstellungen mit dem UE-v-Generator</span><span class="sxs-lookup"><span data-stu-id="11ad5-130">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="11ad5-131">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="11ad5-131">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="11ad5-132">Klicken Sie auf **Vorlage zum Erstellen einer Einstellungsposition**.</span><span class="sxs-lookup"><span data-stu-id="11ad5-132">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="11ad5-133">Geben Sie die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="11ad5-133">Specify the application.</span></span> <span data-ttu-id="11ad5-134">Navigieren Sie zum Dateipfad der Anwendung (. exe) oder der Anwendungsverknüpfung (. lnk), für die Sie eine Vorlage für eine Einstellungsposition erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="11ad5-134">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="11ad5-135">Geben Sie die Befehlszeilenargumente (sofern vorhanden) und das Arbeitsverzeichnis an, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="11ad5-135">Specify the command line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="11ad5-136">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-136">Click **Next** to continue.</span></span>

    <span data-ttu-id="11ad5-137">**Hinweis**  Bevor die Anwendung gestartet wird, zeigt das System eine Aufforderung zur **Steuerung des Benutzerkontos**an.</span><span class="sxs-lookup"><span data-stu-id="11ad5-137">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="11ad5-138">Zum Überwachen der Registrierungs-und Dateispeicherorte, die die Anwendung zum Speichern von Einstellungen verwendet, ist eine Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="11ad5-138">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="11ad5-139">Schließen Sie die Anwendung, nachdem die Anwendung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="11ad5-139">After the application starts, close the application.</span></span> <span data-ttu-id="11ad5-140">Der UE-V-Generator zeichnet die Speicherorte auf, an denen die Anwendung die Einstellungen speichert.</span><span class="sxs-lookup"><span data-stu-id="11ad5-140">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="11ad5-141">Klicken Sie nach Abschluss des Prozesses auf **weiter** , um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="11ad5-141">After the process is complete, click **Next** to continue.</span></span>

6.  <span data-ttu-id="11ad5-142">Überprüfen Sie, und aktivieren Sie die Kontrollkästchen neben den entsprechenden Registrierungseinstellungen für Speicherorte und Einstellungen für die Dateispeicherorte für diese Anwendung.</span><span class="sxs-lookup"><span data-stu-id="11ad5-142">Review and select the check boxes next to the appropriate registry settings locations and settings file locations to roam for this application.</span></span> <span data-ttu-id="11ad5-143">Die Liste enthält die folgenden beiden Kategorien für die Einstellungen für die Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="11ad5-143">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="11ad5-144">**Standard**: Anwendungseinstellungen, die in der Registrierung unter dem HKEY \ _CURRENT \ _User Schlüssel oder in den Dateiordnern unter \ \ **Users** \ \ \ [Benutzername \] \ \ **AppData**  \\  **Roaming**gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="11ad5-144">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="11ad5-145">Der UE-V-Generator enthält standardmäßig diese Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-145">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="11ad5-146">Nicht **Standard**: Anwendungseinstellungen, die außerhalb der Speicherorte gespeichert sind, die in den bewährten Methoden für Einstellungsdaten Speicher angegeben sind (optional).</span><span class="sxs-lookup"><span data-stu-id="11ad5-146">**Nonstandard**: Application settings that are stored outside the locations specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="11ad5-147">Dazu gehören Dateien und Ordner unter **Benutzer** \ \ \ [Benutzername \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="11ad5-147">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="11ad5-148">Überprüfen Sie diese Speicherorte, um zu bestimmen, ob Sie Sie in die Vorlage für den Einstellungs Speicherort einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="11ad5-148">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="11ad5-149">Aktivieren Sie die Kontrollkästchen Speicherorte, um Sie einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-149">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="11ad5-150">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-150">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="11ad5-151">Überprüfen und bearbeiten Sie alle **Eigenschaften**, **Registrierungs** Speicherorte und **Datei** Speicherorte für die Vorlage Speicherort für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-151">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="11ad5-152">Bearbeiten Sie die folgenden Eigenschaften auf der Registerkarte " **Eigenschaften** ":</span><span class="sxs-lookup"><span data-stu-id="11ad5-152">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="11ad5-153">**Anwendungsname**: der Anwendungsname, der in der Beschreibung der Programmdatei Eigenschaften geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="11ad5-153">**Application Name**: The application name written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="11ad5-154">**Programmname**: der Name des Programms, das aus den Programmdatei Eigenschaften übernommen wurde.</span><span class="sxs-lookup"><span data-stu-id="11ad5-154">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="11ad5-155">Dieser Name hat in der Regel die Erweiterung ". exe".</span><span class="sxs-lookup"><span data-stu-id="11ad5-155">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="11ad5-156">**Produktversion**: die Produktversionsnummer der exe-Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="11ad5-156">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="11ad5-157">Mit dieser Eigenschaft können Sie in Verbindung mit der Dateiversion ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-157">This property, in conjunction with the File version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="11ad5-158">Diese Eigenschaft akzeptiert eine Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="11ad5-158">This property accepts a major version number.</span></span> <span data-ttu-id="11ad5-159">Wenn diese Eigenschaft leer ist, wird die Vorlage für die Einstellungsposition auf alle Versionen des Produkts angewendet.</span><span class="sxs-lookup"><span data-stu-id="11ad5-159">If this property is empty, the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="11ad5-160">**Dateiversion**: die Dateiversionsnummer the.exe Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="11ad5-160">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="11ad5-161">Mit dieser Eigenschaft können Sie in Verbindung mit der Produktversion ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-161">This property, in conjunction with the Product version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="11ad5-162">Diese Eigenschaft akzeptiert eine Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="11ad5-162">This property accepts a major version number.</span></span> <span data-ttu-id="11ad5-163">Wenn diese Eigenschaft leer ist, wird die Vorlage für die Einstellungsposition auf alle Versionen des Programms angewendet.</span><span class="sxs-lookup"><span data-stu-id="11ad5-163">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="11ad5-164">**Name der Vorlagen Autorin** (optional): der Name der Vorlage für den Speicherort der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-164">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="11ad5-165">**E-Mail-Vorlage für Vorlagenautor** (optional): die e-Mail-Adresse der Vorlage "Speicherort für Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="11ad5-165">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="11ad5-166">Auf der Registerkarte " **Registrierung** " sind der **Schlüssel** und der **Bereich** der Registrierungsspeicherorte aufgeführt, die in der Vorlage "einstellungensort" enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="11ad5-166">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="11ad5-167">Bearbeiten Sie die Registrierungsspeicherorte mithilfe des Dropdownmenüs **Aufgaben** .</span><span class="sxs-lookup"><span data-stu-id="11ad5-167">Edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="11ad5-168">Aufgaben umfassen das Hinzufügen neuer Schlüssel, das Bearbeiten des Namens oder des Bereichs vorhandener Schlüssel, das Löschen von Schlüsseln und das Durchsuchen der Registrierung, in der sich die Schlüssel befinden.</span><span class="sxs-lookup"><span data-stu-id="11ad5-168">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry where the keys are located.</span></span> <span data-ttu-id="11ad5-169">Verwenden Sie den Bereich **alle Einstellungen** , um alle Registrierungseinstellungen unter dem angegebenen Schlüssel einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-169">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="11ad5-170">Verwenden Sie **alle Einstellungen und Unterschlüssel** , um alle Registrierungseinstellungen unter den angegebenen Tasten, Unterschlüsseln und Unterschlüssel Einstellungen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-170">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="11ad5-171">Auf der Registerkarte " **Dateien** " werden der Dateipfad und die Dateimaske der Dateispeicherorte aufgeführt, die in der Vorlage für die Einstellungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="11ad5-171">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="11ad5-172">Bearbeiten Sie die Dateispeicherorte mithilfe des Dropdownmenüs **Aufgaben** .</span><span class="sxs-lookup"><span data-stu-id="11ad5-172">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="11ad5-173">Zu den Aufgaben für Dateispeicherorte gehören das Hinzufügen neuer Dateien oder Ordnerspeicherorte, das Bearbeiten des Bereichs vorhandener Dateien oder Ordner, das Löschen von Dateien oder Ordnern sowie das Öffnen des ausgewählten Speicherorts im Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="11ad5-173">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="11ad5-174">Lassen Sie die Dateimaske leer, um alle Dateien in den angegebenen Ordner einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-174">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="11ad5-175">Klicken Sie auf dem Computer auf die Vorlage Speicherort für Einstellungen **Erstellen** und speichern.</span><span class="sxs-lookup"><span data-stu-id="11ad5-175">Click **Create** and save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="11ad5-176">Klicken Sie auf **Schließen** , um den Assistenten für Einstellungs Vorlagen zu schließen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-176">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="11ad5-177">Beenden Sie die UE-V-Generator Anwendung.</span><span class="sxs-lookup"><span data-stu-id="11ad5-177">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="11ad5-178">Nachdem Sie die Vorlage für die Einstellungsposition für eine Anwendung erstellt haben, sollten Sie die Vorlage testen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-178">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="11ad5-179">Stellen Sie die Vorlage in einer Lab-Umgebung bereit, bevor Sie Sie in der Produktion im Unternehmen einsetzen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-179">Deploy the template in a lab environment before putting it into production in the enterprise.</span></span>

## <span data-ttu-id="11ad5-180">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="11ad5-180">Related topics</span></span>


[<span data-ttu-id="11ad5-181">Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator</span><span class="sxs-lookup"><span data-stu-id="11ad5-181">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="11ad5-182">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="11ad5-182">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





