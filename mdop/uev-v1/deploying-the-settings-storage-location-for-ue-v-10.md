---
title: Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0
description: Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811875"
---
# <span data-ttu-id="25f74-103">Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="25f74-103">Deploying the Settings Storage Location for UE-V 1.0</span></span>


<span data-ttu-id="25f74-104">Die Bereitstellung von Microsoft User Experience Virtualization (UE-V) erfordert einen Speicherort für Einstellungen, in dem die Benutzereinstellungen in einer Einstellungspaket Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="25f74-104">Microsoft User Experience Virtualization (UE-V) deployment requires a settings storage location where the user settings are stored in a settings package file.</span></span> <span data-ttu-id="25f74-105">Der Speicherort für Einstellungen kann auf eine der folgenden zwei Arten konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="25f74-105">The settings storage location can be configured in one of the following two ways:</span></span>

-   <span data-ttu-id="25f74-106">**Active Directory-Basisverzeichnis** – wenn für den Benutzer in Active Directory ein Home-Verzeichnis definiert ist, verwendet der UE-V-Agent diesen Speicherort zum Speichern von Einstellungen für Standort Pakete.</span><span class="sxs-lookup"><span data-stu-id="25f74-106">**Active Directory home directory** – if a home directory is defined for the user in Active Directory, the UE-V agent will use this location to store settings location packages.</span></span> <span data-ttu-id="25f74-107">Der UE-V-Agent erstellt dynamisch den benutzerspezifischen Speicherordner unter dem Stammverzeichnis des Basisverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="25f74-107">The UE-V agent dynamically creates the user-specific storage folder below the root of the home directory.</span></span> <span data-ttu-id="25f74-108">Der Agent verwendet nur das Home-Verzeichnis des Active Directory, wenn kein Speicherort für Einstellungen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="25f74-108">The agent only uses the home directory of the Active Directory if a settings storage location is not defined.</span></span>

-   <span data-ttu-id="25f74-109">**Erstellen einer Speicherfreigabe für Einstellungen** – die Speicherfreigabe für Einstellungen ist eine standardmäßige Netzwerkfreigabe, auf die UE-V-Benutzer zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="25f74-109">**Create a settings storage share** – the settings storage share is a standard network share that is accessible by UE-V users.</span></span>

## <span data-ttu-id="25f74-110">Bereitstelleneiner Speicherfreigabe für UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="25f74-110">Deploy a UE-V settings storage share</span></span>


<span data-ttu-id="25f74-111">Wenn Sie die Speicherfreigabe für Einstellungen erstellen, sollten Sie den Zugriff nur auf Benutzer beschränken, die Zugriff benötigen.</span><span class="sxs-lookup"><span data-stu-id="25f74-111">When you create the settings storage share, you should limit access only to users that need access.</span></span> <span data-ttu-id="25f74-112">Die erforderlichen Berechtigungen werden in den folgenden Tabellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="25f74-112">The necessary permissions are shown in the tables below.</span></span>

**<span data-ttu-id="25f74-113">So stellen Sie die UE-V-Netzwerkfreigabe bereit</span><span class="sxs-lookup"><span data-stu-id="25f74-113">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="25f74-114">Erstellen Sie eine neue Sicherheitsgruppe für UE-V-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="25f74-114">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="25f74-115">Erstellen Sie einen neuen Ordner auf dem zentral gelegenen Computer, auf dem die UE-v-Einstellungs Pakete gespeichert werden, und erteilen Sie den UE-v-Benutzern dann Gruppen Berechtigungen für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="25f74-115">Create a new folder on the centrally located computer that will store the UE-V settings packages, and then grant the UE-V users with group permissions to the folder.</span></span> <span data-ttu-id="25f74-116">Der Administrator, der UE-V unterstützt, benötigt Berechtigungen für diesen freigegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="25f74-116">The administrator supporting UE-V will need permissions to this shared folder.</span></span>

3.  <span data-ttu-id="25f74-117">Legen Sie die folgenden SMB-Berechtigungen (Freigabeebene) für den Ordner für die Einstellung des Speicherorts fest:</span><span class="sxs-lookup"><span data-stu-id="25f74-117">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="25f74-118">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="25f74-118">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="25f74-119">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="25f74-119">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="25f74-120">Jeder</span><span class="sxs-lookup"><span data-stu-id="25f74-120">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="25f74-121">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="25f74-121">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="25f74-122">Sicherheitsgruppe der UE-V-Benutzer</span><span class="sxs-lookup"><span data-stu-id="25f74-122">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="25f74-123">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="25f74-123">Full Control</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="25f74-124">Legen Sie die folgenden NTFS-Berechtigungen für den Ordner "Settings Storage Location":</span><span class="sxs-lookup"><span data-stu-id="25f74-124">Set the following NTFS permissions for the settings storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="25f74-125">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="25f74-125">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="25f74-126">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="25f74-126">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="25f74-127">Ordner</span><span class="sxs-lookup"><span data-stu-id="25f74-127">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="25f74-128">Ersteller/Besitzer</span><span class="sxs-lookup"><span data-stu-id="25f74-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="25f74-129">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="25f74-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="25f74-130">Nur Unterordner und Dateien</span><span class="sxs-lookup"><span data-stu-id="25f74-130">Subfolders and Files Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="25f74-131">Sicherheitsgruppe der UE-V-Benutzer</span><span class="sxs-lookup"><span data-stu-id="25f74-131">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="25f74-132">Ordner auflisten/Daten lesen, Ordner erstellen/Daten anfügen</span><span class="sxs-lookup"><span data-stu-id="25f74-132">List Folder/Read Data, Create Folders/Append Data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="25f74-133">Nur diesen Ordner</span><span class="sxs-lookup"><span data-stu-id="25f74-133">This Folder Only</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

5.  <span data-ttu-id="25f74-134">Klicken Sie auf **OK** , um die Dialogfelder zu schließen.</span><span class="sxs-lookup"><span data-stu-id="25f74-134">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="25f74-135">Diese Berechtigungskonfiguration ermöglicht Benutzern das Erstellen von Ordnern für den Einstellungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="25f74-135">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="25f74-136">Der UE-V-Agent erstellt und sichert einen `settingspackage` Ordner, während er im Kontext des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25f74-136">The UE-V agent creates and secures a `settingspackage` folder while running in the context of the user.</span></span> <span data-ttu-id="25f74-137">Der Benutzer erhält die vollständige Kontrolle über seinen `settingspackage` Ordner.</span><span class="sxs-lookup"><span data-stu-id="25f74-137">The user receives full control to their `settingspackage` folder.</span></span> <span data-ttu-id="25f74-138">Andere Benutzer erben keinen Zugriff auf diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="25f74-138">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="25f74-139">Es ist nicht erforderlich, einzelne Benutzerverzeichnisse zu erstellen und zu sichern, da dies automatisch vom Agent erfolgt, der im Kontext des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25f74-139">You do not need to create and secure individual user directories, because this will be done automatically by the agent that runs in the context of the user.</span></span>

<span data-ttu-id="25f74-140">**Hinweis**  Zusätzliche Sicherheit kann konfiguriert werden, wenn ein Windows-Server für die Speicherfreigabe "Einstellungen" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="25f74-140">**Note** Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="25f74-141">UE-V kann so konfiguriert werden, dass entweder die Gruppe des lokalen Administrators oder der aktuelle Benutzer der Besitzer des Ordners ist, in dem die Einstellungs Pakete gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="25f74-141">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="25f74-142">Führen Sie die folgenden Schritte aus, um zusätzliche Sicherheit zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="25f74-142">To enable additional security complete the following:</span></span>

1.  <span data-ttu-id="25f74-143">Fügen Sie einen Registrierungsschlüssel " **reg \ _DWORD** " mit dem Namen "RepositoryOwnerCheckEnabled" zu **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**</span><span class="sxs-lookup"><span data-stu-id="25f74-143">Add a **REG\_DWORD** registry key named "RepositoryOwnerCheckEnabled" to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration.**</span></span>

2.  <span data-ttu-id="25f74-144">Stellen Sie den Registrierungsschlüsselwert auf 1 ein.</span><span class="sxs-lookup"><span data-stu-id="25f74-144">Set registry key value to 1.</span></span>

 

## <span data-ttu-id="25f74-145">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="25f74-145">Related topics</span></span>


[<span data-ttu-id="25f74-146">Bereitstellen von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="25f74-146">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="25f74-147">Unterstützte Konfigurationen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="25f74-147">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

<span data-ttu-id="25f74-148">Bereitstellen des zentralen Speichers für die Einstellungen für Benutzeroberflächen-Virtualisierungs-Vorlagen und-Einstellungen Pakete [beim Installieren des UE-V-Generators](installing-the-ue-v-generator.md)</span><span class="sxs-lookup"><span data-stu-id="25f74-148">Deploy the Central Storage for User Experience Virtualization Settings Templates and Settings Packages [Installing the UE-V Generator](installing-the-ue-v-generator.md)</span></span>

[<span data-ttu-id="25f74-149">Bereitstellen von UE-V-Agent</span><span class="sxs-lookup"><span data-stu-id="25f74-149">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

 

 





