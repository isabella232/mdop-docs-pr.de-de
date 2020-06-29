---
title: Informationen zu App-V 5.0 SP3
description: Informationen zu App-V 5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806120"
---
# <span data-ttu-id="c424c-103">Informationen zu App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="c424c-103">About App-V 5.0 SP3</span></span>


<span data-ttu-id="c424c-104">Verwenden Sie die folgenden Abschnitte, um Informationen zu bedeutenden Änderungen zu überprüfen, die für Microsoft Application Virtualization (App-V) 5,0 SP3 gelten:</span><span class="sxs-lookup"><span data-stu-id="c424c-104">Use the following sections to review information about significant changes that apply to Microsoft Application Virtualization (App-V) 5.0 SP3:</span></span>

-   [<span data-ttu-id="c424c-105">Software-Voraussetzungen und unterstützte Konfigurationen für App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="c424c-105">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>](#bkmk-sp3-prereq-configs)

-   [<span data-ttu-id="c424c-106">Migrieren zu App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="c424c-106">Migrating to App-V 5.0 SP3</span></span>](#bkmk-migrate-to-50sp3)

-   [<span data-ttu-id="c424c-107">Die XML-Datei für eine manuell erstellte Verbindungsgruppe erfordert ein Update auf ein Schema</span><span class="sxs-lookup"><span data-stu-id="c424c-107">Manually created connection group xml file requires update to schema</span></span>](#bkmk-update-schema-cg)

-   [<span data-ttu-id="c424c-108">Verbesserungen an Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="c424c-108">Improvements to connection groups</span></span>](#bkmk-cg-improvements)

-   [<span data-ttu-id="c424c-109">Administratoren können Pakete für einen bestimmten Benutzer veröffentlichen und deren Veröffentlichung aufheben.</span><span class="sxs-lookup"><span data-stu-id="c424c-109">Administrators can publish and unpublish packages for a specific user</span></span>](#bkmk-usersid-pub-pkgs-specf-user)

-   [<span data-ttu-id="c424c-110">Nur Administratoren das Veröffentlichen und Aufheben der Veröffentlichung von Paketen ermöglichen</span><span class="sxs-lookup"><span data-stu-id="c424c-110">Enable only administrators to publish and unpublish packages</span></span>](#bkmk-admins-only-pub-unpub-pkgs)

-   [<span data-ttu-id="c424c-111">RunVirtual-Registrierungsschlüssel unterstützt Pakete, die für den Benutzer veröffentlicht werden</span><span class="sxs-lookup"><span data-stu-id="c424c-111">RunVirtual registry key supports packages that are published to the user</span></span>](#bkmk-runvirtual-reg-key)

-   [<span data-ttu-id="c424c-112">Neue PowerShell-Cmdlets und Hilfe zu aktualisierbaren Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c424c-112">New PowerShell cmdlets and updateable cmdlet help</span></span>](#bkmk-posh-cmdlets-help)

-   [<span data-ttu-id="c424c-113">Primäres virtuelles Anwendungsverzeichnis (PVAD) ist ausgeblendet, kann aber aktiviert werden</span><span class="sxs-lookup"><span data-stu-id="c424c-113">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>](#bkmk-pvad-hidden)

-   [<span data-ttu-id="c424c-114">Clientversion ist erforderlich, um die App-V-Veröffentlichungsmetadaten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c424c-114">ClientVersion is required to view App-V publishing metadata</span></span>](#bkmk-pub-metadata-clientversion)

-   [<span data-ttu-id="c424c-115">App-V-Ereignisprotokolle wurden konsolidiert</span><span class="sxs-lookup"><span data-stu-id="c424c-115">App-V event logs have been consolidated</span></span>](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a><span data-ttu-id="c424c-116">Software-Voraussetzungen und unterstützte Konfigurationen für App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="c424c-116">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>


<span data-ttu-id="c424c-117">Unter den folgenden Links finden Sie die Voraussetzungen für die App-V 5,0 SP3 und die unterstützten Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c424c-117">See the following links for the App-V 5.0 SP3 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-118">Links zu Voraussetzungen und unterstützten Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="c424c-118">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="c424c-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424c-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)"><span data-ttu-id="c424c-120">Voraussetzungen für App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="c424c-120">App-V 5.0 SP3 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="c424c-121">Erforderliche Software, die Sie vor dem Starten der App-V 5,0 SP3-Installation installieren müssen</span><span class="sxs-lookup"><span data-stu-id="c424c-121">Prerequisite software that you must install before starting the App-V 5.0 SP3 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"><span data-ttu-id="c424c-122">Unterstützte App-V 5.0 SP3-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="c424c-122">App-V 5.0 SP3 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="c424c-123">Unterstützte Betriebssysteme und Hardwareanforderungen für App-V Server, Sequencer und Client Komponenten</span><span class="sxs-lookup"><span data-stu-id="c424c-123">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a><span data-ttu-id="c424c-124">Migrieren zu App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="c424c-124">Migrating to App-V 5.0 SP3</span></span>


<span data-ttu-id="c424c-125">Verwenden Sie die folgenden Informationen, um aus früheren Versionen auf App-V 5,0 SP3 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c424c-125">Use the following information to upgrade to App-V 5.0 SP3 from earlier versions.</span></span>

### <span data-ttu-id="c424c-126">Vor dem Starten des Upgrades</span><span class="sxs-lookup"><span data-stu-id="c424c-126">Before you start the upgrade</span></span>

<span data-ttu-id="c424c-127">Überprüfen Sie die folgenden Informationen, bevor Sie das Upgrade starten:</span><span class="sxs-lookup"><span data-stu-id="c424c-127">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-128">Zu überprüfende Elemente vor dem Upgrade</span><span class="sxs-lookup"><span data-stu-id="c424c-128">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="c424c-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424c-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-130">Zu aktualisierbare Komponenten</span><span class="sxs-lookup"><span data-stu-id="c424c-130">Components to upgrade</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="c424c-131">App-V-Server</span><span class="sxs-lookup"><span data-stu-id="c424c-131">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="c424c-132">Sequencer</span><span class="sxs-lookup"><span data-stu-id="c424c-132">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="c424c-133">App-v Client oder App-v Remote Desktop Dienste (RDS)-Client</span><span class="sxs-lookup"><span data-stu-id="c424c-133">App-V client or App-V Remote Desktop Services (RDS) client</span></span></p></li>
<li><p><span data-ttu-id="c424c-134">Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="c424c-134">Connection groups</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="c424c-135">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="c424c-135">Note</span></span></strong><br/><p><span data-ttu-id="c424c-136">Wenn Sie die App-V-Clientbenutzeroberfläche verwenden möchten, laden Sie die vorhandene Version aus der <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> Microsoft Application Virtualization 5,0-Client-UI-Anwendung herunter </a> .</span><span class="sxs-lookup"><span data-stu-id="c424c-136">To use the App-V client user interface, download the existing version from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Microsoft Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-137">Aktualisieren von App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="c424c-137">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-138">Sie müssen zuerst auf App-V 5,0 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c424c-138">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="c424c-139">Sie können nicht direkt von App-v 4. x auf App-v 5,0 SP3 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c424c-139">You cannot upgrade directly from App-V 4.x to App-V 5.0 SP3.</span></span></p>
<p><span data-ttu-id="c424c-140">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="c424c-140">For more information, see:</span></span></p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"><span data-ttu-id="c424c-141">Informationen zu App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c424c-141">About App-V 5.0</span></span></a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="c424c-142">Planen der Migration von einer früheren Version von App-V</span><span class="sxs-lookup"><span data-stu-id="c424c-142">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-143">Aktualisieren von App-V 5,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c424c-143">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-144">Sie können direkt von einer der folgenden Versionen auf App-V 5,0 SP3 aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="c424c-144">You can upgrade to App-V 5.0 SP3 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="c424c-145">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c424c-145">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="c424c-146">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c424c-146">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="c424c-147">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="c424c-147">App-V 5.0 SP2</span></span></p></li>
</ul>
<p><span data-ttu-id="c424c-148">Führen Sie die Schritte in den verbleibenden Abschnitten dieses Artikels aus, um auf App-V 5,0 SP3 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c424c-148">To upgrade to App-V 5.0 SP3, follow the steps in the remaining sections of this article.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-149">Erforderliche Änderungen an Paketen und Verbindungsgruppen nach dem Upgrade</span><span class="sxs-lookup"><span data-stu-id="c424c-149">Required changes to packages and connection groups after upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-150">Keine</span><span class="sxs-lookup"><span data-stu-id="c424c-150">None.</span></span> <span data-ttu-id="c424c-151">Pakete und Verbindungsgruppen funktionieren weiterhin wie bisher.</span><span class="sxs-lookup"><span data-stu-id="c424c-151">Packages and connection groups will continue to work as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="c424c-152">Schritte zum Upgrade der App-V-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="c424c-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="c424c-153">Führen Sie die folgenden Schritte aus, um die einzelnen Komponenten der APP-v-Infrastruktur auf App-v 5,0 SP3 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c424c-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.0 SP3.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-154">Schritt</span><span class="sxs-lookup"><span data-stu-id="c424c-154">Step</span></span></th>
<th align="left"><span data-ttu-id="c424c-155">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c424c-155">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-156">Schritt 1: Aktualisieren Sie den App-V-Server.</span><span class="sxs-lookup"><span data-stu-id="c424c-156">Step 1: Upgrade the App-V Server.</span></span></p>
<p><span data-ttu-id="c424c-157">Wenn Sie den App-V-Server nicht verwenden, überspringen Sie diesen Schritt, und fahren Sie mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="c424c-157">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c424c-158">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="c424c-158">Note</span></span></strong><br/><p><span data-ttu-id="c424c-159">Der APP-v 5,0 SP3-Client ist mit dem App-v 5,0 SP1-Server kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c424c-159">The App-V 5.0 SP3 client is compatible with the App-V 5.0 SP1 Server.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c424c-160">Führen Sie folgende Schritte aus: </span><span class="sxs-lookup"><span data-stu-id="c424c-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="c424c-161">Lesen Sie die <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> Versionshinweise für App-v 5,0 SP3 </a> für Probleme, die sich auf die Installation des App-v-Servers auswirken können.</span><span class="sxs-lookup"><span data-stu-id="c424c-161">Review the <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)">Release Notes for App-V 5.0 SP3</a> for issues that may affect the App-V Server installation.</span></span></p></li>
<li><p><span data-ttu-id="c424c-162">Führen Sie eine der folgenden Aktionen aus, je nachdem, welche Methode Sie verwenden, um die Verwaltungsdatenbank und/oder die Berichtsdatenbank zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="c424c-162">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-163">Daten Bank Aktualisierungsmethode</span><span class="sxs-lookup"><span data-stu-id="c424c-163">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="c424c-164">Schritt</span><span class="sxs-lookup"><span data-stu-id="c424c-164">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-165">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c424c-165">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-166">Überspringen Sie diesen Schritt, und wechseln Sie zu Schritt 3, "Wenn Sie den App-V-Server aktualisieren..."</span><span class="sxs-lookup"><span data-stu-id="c424c-166">Skip this step and go to step 3, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-167">SQL-Skripts</span><span class="sxs-lookup"><span data-stu-id="c424c-167">SQL scripts</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c424c-168">Verwaltungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="c424c-168">Management database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c424c-169">Informationen zum Installieren oder Aktualisieren finden Sie unter <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> SQL-Skripts zum Installieren oder Aktualisieren der App-V 5,0 SP3-Verwaltungs Server-Datenbank Fehler </a> .</span><span class="sxs-lookup"><span data-stu-id="c424c-169">To install or upgrade, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c424c-170">Berichtsdatenbank</span><span class="sxs-lookup"><span data-stu-id="c424c-170">Reporting database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c424c-171">Führen Sie die Schritte unter <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> Vorgehensweise zum Bereitstellen der App-V-Datenbanken mithilfe von SQL-Skripts aus </a> .</span><span class="sxs-lookup"><span data-stu-id="c424c-171">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p><span data-ttu-id="c424c-172">Wenn Sie den App-v-Server vom APP-v 5,0 SP1-Hotfix-Paket 3 oder höher aktualisieren, führen Sie die Schritte in Abschnitt <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> Überprüfen der Registrierungsschlüssel nach der Installation des App-v 5,0 SP3-Servers aus </a> .</span><span class="sxs-lookup"><span data-stu-id="c424c-172">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="c424c-173">Führen Sie die Schritte unter <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> Bereitstellen des App-V 5,0-Servers aus </a> .</span><span class="sxs-lookup"><span data-stu-id="c424c-173">Follow the steps in <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-174">Schritt 2: Aktualisieren Sie den App-V-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="c424c-174">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-175">Weitere Informationen finden Sie unter <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Installieren des Sequencers </a> .</span><span class="sxs-lookup"><span data-stu-id="c424c-175">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-176">Schritt 3: Aktualisieren Sie den App-v-Client oder den App-v-RDS-Client.</span><span class="sxs-lookup"><span data-stu-id="c424c-176">Step 3: Upgrade the App-V client or App-V RDS client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-177">Weitere Informationen finden Sie unter <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> Bereitstellen des App-V-Clients </a> .</span><span class="sxs-lookup"><span data-stu-id="c424c-177">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a><span data-ttu-id="c424c-178">Überprüfen der Registrierungsschlüssel vor der Installation des App-V 5,0 SP3-Servers</span><span class="sxs-lookup"><span data-stu-id="c424c-178">Check registry keys before installing the App-V 5.0 SP3 Server</span></span>

<span data-ttu-id="c424c-179">Dies ist Schritt 3 aus der vorhergehenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c424c-179">This is step 3 from the previous table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c424c-180">Wenn dieser Schritt erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="c424c-180">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c424c-181">Sie Aktualisieren von App-V SP1 mit allen nachfolgenden Hotfix-Paketen, die Sie mithilfe einer MSP-Datei installiert haben.</span><span class="sxs-lookup"><span data-stu-id="c424c-181">You are upgrading from App-V SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c424c-182">Für welche Komponenten muss dieser Schritt ausgeführt werden?</span><span class="sxs-lookup"><span data-stu-id="c424c-182">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c424c-183">Nur die App-V Server-Komponenten, die Sie aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c424c-183">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c424c-184">Wenn Sie diesen Schritt ausführen müssen</span><span class="sxs-lookup"><span data-stu-id="c424c-184">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c424c-185">Vor dem Upgrade des App-v-Servers auf App-v 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="c424c-185">Before you upgrade the App-V Server to App-V 5.0 SP3</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c424c-186">Was Sie tun müssen</span><span class="sxs-lookup"><span data-stu-id="c424c-186">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c424c-187">Aktualisieren Sie anhand der Informationen in den folgenden Tabellen jeden Registrierungsschlüsselwert unter <code>HKLM\Software\Microsoft\AppV\Server</code> mit dem Wert, den Sie in der ursprünglichen Server Installation angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="c424c-187">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="c424c-188">Durch das Abschließen dieses Schritts werden Registrierungswerte wiederhergestellt, die möglicherweise entfernt wurden, als App-V SP1-Hotfix-Pakete installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c424c-188">Completing this step restores registry values that may have been removed when App-V SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="c424c-189">ManagementDatabase-Taste</span><span class="sxs-lookup"><span data-stu-id="c424c-189">ManagementDatabase key</span></span>**

<span data-ttu-id="c424c-190">Wenn Sie die Verwaltungsdatenbank installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="c424c-190">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-191">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="c424c-191">Key name</span></span></th>
<th align="left"><span data-ttu-id="c424c-192">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424c-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="c424c-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-194">Beschreibt, ob ein öffentliches Zugriffskonto für den Zugriff auf nicht lokale Verwaltungs Datenbanken erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-194">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="c424c-195">Value ist auf "1" gesetzt, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-195">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-196">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c424c-196">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-197">Der Name der Verwaltungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c424c-197">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c424c-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-199">Konto, das für den Lesezugriff auf die Verwaltungsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c424c-199">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="c424c-200">Wird verwendet <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-200">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="c424c-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-202">Secure Identifier (SID) des Kontos, das für den Zugriff auf die Verwaltungsdatenbank für Read (Public) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c424c-202">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="c424c-203">Wird verwendet <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-203">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-204">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c424c-204">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-205">SQL Server-Instanz für die Verwaltungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c424c-205">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="c424c-206">Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="c424c-206">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c424c-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-208">Konto, das für den Schreibzugriff (Administrator) für die Verwaltungsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c424c-208">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="c424c-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-210">Secure Identifier (SID) des Kontos, das für den Schreibzugriff (Administrator) auf die Verwaltungsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c424c-210">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c424c-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-212">Verwaltungsserver-Remotecomputer Konto (Domain\Account).</span><span class="sxs-lookup"><span data-stu-id="c424c-212">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c424c-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-214">Installations Administrator-Anmeldung für den Verwaltungsserver (Domain\Account).</span><span class="sxs-lookup"><span data-stu-id="c424c-214">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c424c-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-216">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c424c-216">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="c424c-217">1 </strong> – der Verwaltungsdienst befindet sich auf dem lokalen Computer, das heißt, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT ist leer.</span><span class="sxs-lookup"><span data-stu-id="c424c-217">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="c424c-218">0 </strong> - der Verwaltungsdienst befindet sich auf einem anderen Computer als auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c424c-218">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="c424c-219">Managementservice-Taste</span><span class="sxs-lookup"><span data-stu-id="c424c-219">ManagementService key</span></span>**

<span data-ttu-id="c424c-220">Wenn Sie den Verwaltungsserver installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="c424c-220">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-221">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="c424c-221">Key name</span></span></th>
<th align="left"><span data-ttu-id="c424c-222">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424c-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-223">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c424c-223">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-224">Active Directory-Domänendienste (AD DS)-Gruppe oder-Konto, das zum Verwalten von App-V (Domain\Account) autorisiert ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-224">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-225">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c424c-225">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-226">SQL Server-Instanz, die die Verwaltungsdatenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="c424c-226">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="c424c-227">Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="c424c-227">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-228">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c424c-228">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-229">Der Name des Remote-SQL-Servers mit der Verwaltungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c424c-229">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="c424c-230">Wenn der Wert leer ist, wird der lokale Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="c424c-230">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="c424c-231">ReportingDatabase-Taste</span><span class="sxs-lookup"><span data-stu-id="c424c-231">ReportingDatabase key</span></span>**

<span data-ttu-id="c424c-232">Wenn Sie die Berichtsdatenbank installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="c424c-232">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-233">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="c424c-233">Key name</span></span></th>
<th align="left"><span data-ttu-id="c424c-234">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424c-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="c424c-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-236">Beschreibt, ob ein öffentliches Zugriffskonto für den Zugriff auf nicht lokale Berichtsdatenbanken erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-236">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="c424c-237">Value ist auf "1" gesetzt, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-237">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-238">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c424c-238">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-239">Der Name der Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c424c-239">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c424c-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-241">Konto, das für den Lesezugriff auf die Berichtsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c424c-241">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="c424c-242">Wird verwendet <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-242">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="c424c-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-244">Secure Identifier (SID) des Kontos, das für den Zugriff auf die Berichtsdatenbank gelesen (öffentlich) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c424c-244">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="c424c-245">Wird verwendet <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-245">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-246">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c424c-246">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-247">SQL Server-Instanz für die Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c424c-247">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="c424c-248">Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="c424c-248">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c424c-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="c424c-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c424c-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-252">Reporting Server-Remotecomputer Konto (Domain\Account).</span><span class="sxs-lookup"><span data-stu-id="c424c-252">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c424c-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-254">Installations Administrator-Anmeldung für den Berichtsserver (Domain\Account).</span><span class="sxs-lookup"><span data-stu-id="c424c-254">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c424c-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-256">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c424c-256">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="c424c-257">1 </strong> – der Berichterstattungsdienst befindet sich auf dem lokalen Computer, das heißt, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT ist leer.</span><span class="sxs-lookup"><span data-stu-id="c424c-257">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="c424c-258">0 </strong> - der Berichterstattungsdienst befindet sich auf einem anderen Computer als auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c424c-258">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="c424c-259">ReportingService-Taste</span><span class="sxs-lookup"><span data-stu-id="c424c-259">ReportingService key</span></span>**

<span data-ttu-id="c424c-260">Wenn Sie den Berichtsserver installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="c424c-260">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-261">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="c424c-261">Key name</span></span></th>
<th align="left"><span data-ttu-id="c424c-262">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424c-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-263">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c424c-263">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-264">SQL Server-Instanz für die Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c424c-264">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="c424c-265">Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="c424c-265">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-266">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c424c-266">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-267">Der Name des Remote-SQL-Servers mit der Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c424c-267">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="c424c-268">Wenn der Wert leer ist, wird der lokale Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="c424c-268">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a><span data-ttu-id="c424c-269">Die XML-Datei für eine manuell erstellte Verbindungsgruppe erfordert ein Update auf ein Schema</span><span class="sxs-lookup"><span data-stu-id="c424c-269">Manually created connection group xml file requires update to schema</span></span>


<span data-ttu-id="c424c-270">Wenn Sie die Verbindungsgruppen-XML-Datei manuell erstellen und die neuen Features "optionale Pakete" und "Verwenden einer beliebigen Version" verwenden möchten, die unter [Verbesserungen der Verbindungsgruppen](#bkmk-cg-improvements)beschrieben werden, müssen Sie das folgende Schema in der XML-Datei angeben:</span><span class="sxs-lookup"><span data-stu-id="c424c-270">If you are manually creating the connection group XML file, and want to use the new “optional packages” and “use any version” features that are described in [Improvements to connection groups](#bkmk-cg-improvements), you must specify the following schema in the XML file:</span></span>

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

<span data-ttu-id="c424c-271">Beispiele und weitere Informationen finden Sie unter Informationen zur [Verbindungsgruppen Datei](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="c424c-271">For examples and more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

## <a href="" id="bkmk-cg-improvements"></a><span data-ttu-id="c424c-272">Verbesserungen an Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="c424c-272">Improvements to connection groups</span></span>


<span data-ttu-id="c424c-273">Sie können Verbindungsgruppen einfacher verwalten, indem Sie optionale Pakete und andere Verbesserungen verwenden, die in App-V 5,0 SP3 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c424c-273">You can manage connection groups more easily by using optional packages and other improvements that have been added in App-V 5.0 SP3.</span></span> <span data-ttu-id="c424c-274">In der folgenden Tabelle werden die Aufgaben zusammengefasst, die Sie mithilfe der neuen Verbindungsgruppen Features ausführen können, sowie Links zu ausführlicheren Informationen zu den einzelnen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="c424c-274">The following table summarizes the tasks that you can perform by using the new connection group features, and links to more detailed information about each task.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-275">Aufgabe/Funktion</span><span class="sxs-lookup"><span data-stu-id="c424c-275">Task/feature</span></span></th>
<th align="left"><span data-ttu-id="c424c-276">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424c-276">Description</span></span></th>
<th align="left"><span data-ttu-id="c424c-277">Links zu weiteren Informationen</span><span class="sxs-lookup"><span data-stu-id="c424c-277">Links to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-278">Aktivieren einer Verbindungsgruppe zum einbeziehen Optionaler Pakete</span><span class="sxs-lookup"><span data-stu-id="c424c-278">Enable a connection group to include optional packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-279">Durch die Verwendung optionaler Pakete in einer Verbindungsgruppe können Sie anhand der Anwendungen, auf die Benutzer Anspruch haben, dynamisch ermitteln, welche Anwendungen in der virtuellen Umgebung der Verbindungsgruppe enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c424c-279">Including optional packages in a connection group enables you to dynamically determine which applications will be included in the connection group’s virtual environment, based on the applications that users are entitled to.</span></span></p>
<p><span data-ttu-id="c424c-280">Sie müssen nicht so viele Verbindungsgruppen verwalten, da Sie optionale und nicht optionale Pakete in derselben Verbindungsgruppe kombinieren können.</span><span class="sxs-lookup"><span data-stu-id="c424c-280">You don’t need to manage as many connection groups because you can mix optional and non-optional packages in the same connection group.</span></span> <span data-ttu-id="c424c-281">Durch das Mischen von Paketen können verschiedene Benutzergruppen dieselbe Verbindungsgruppe verwenden, auch wenn die Benutzer möglicherweise nur ein Paket gemeinsam haben.</span><span class="sxs-lookup"><span data-stu-id="c424c-281">Mixing packages allows different groups of users to use the same connection group, even though users might have only one package in common.</span></span></p>
<p><strong><span data-ttu-id="c424c-282">Beispiel </strong> : Sie können ein Paket mit Microsoft Office für alle Benutzer aktivieren, aber verschiedene optionale Pakete, die unterschiedliche Office-Plug-ins enthalten, für verschiedene Teilmengen von Benutzern aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c424c-282">Example</strong>: You can enable a package with Microsoft Office for all users, but enable different optional packages, which contain different Office plug-ins, to different subsets of users.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="c424c-283">So verwenden Sie optionale Pakete in Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="c424c-283">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-284">Aufheben der Veröffentlichung oder Löschen eines optionalen Pakets, ohne die Verbindungsgruppe zu ändern</span><span class="sxs-lookup"><span data-stu-id="c424c-284">Unpublish or delete an optional package without changing the connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-285">Aufheben der Veröffentlichung oder Löschung oder Aufheben der Veröffentlichung und erneuten Veröffentlichung eines optionalen Pakets, das sich in einer Verbindungsgruppe befindet, ohne die Verbindungsgruppe auf dem App-V-Client deaktivieren oder erneut aktivieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c424c-285">Unpublish or delete, or unpublish and republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V client.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="c424c-286">So verwenden Sie optionale Pakete in Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="c424c-286">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-287">Veröffentlichen von Verbindungsgruppen, die von Benutzern veröffentlichte und Global veröffentlichte Pakete enthalten</span><span class="sxs-lookup"><span data-stu-id="c424c-287">Publish connection groups that contain user-published and globally published packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-288">Erstellen einer vom Benutzer veröffentlichten Verbindungsgruppe, die von Benutzern veröffentlichte und Global veröffentlichte Pakete enthält</span><span class="sxs-lookup"><span data-stu-id="c424c-288">Create a user-published connection group that contains user-published and globally published packages.</span></span></p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="c424c-289">So erstellen Sie eine Verbindungsgruppe mit von Benutzern und global veröffentlichten Paketen</span><span class="sxs-lookup"><span data-stu-id="c424c-289">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-290">Veranlassen, dass eine Verbindungsgruppe die Paketversion ignoriert</span><span class="sxs-lookup"><span data-stu-id="c424c-290">Make a connection group ignore the package version</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-291">Konfigurieren Sie eine Verbindungsgruppe, um eine beliebige Version eines Pakets zu akzeptieren, mit der Sie ein Paket aktualisieren können, ohne die Verbindungsgruppe deaktivieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c424c-291">Configure a connection group to accept any version of a package, which enables you to upgrade a package without having to disable the connection group.</span></span> <span data-ttu-id="c424c-292">Wenn ein optionales Paket mit einer falschen Version in der Verbindungsgruppe vorhanden ist, wird das Paket ignoriert und verhindert, dass die virtuelle Umgebung der Verbindungsgruppe nicht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c424c-292">In addition, if there is an optional package with an incorrect version in the connection group, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)"><span data-ttu-id="c424c-293">So stellen Sie sicher, dass eine Verbindungsgruppe die Paketversion ignoriert</span><span class="sxs-lookup"><span data-stu-id="c424c-293">How to Make a Connection Group Ignore the Package Version</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-294">Einschränken der Veröffentlichungsfunktionen von Endbenutzern</span><span class="sxs-lookup"><span data-stu-id="c424c-294">Limit end users’ publishing capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-295">Aktivieren Sie nur Administratoren (nicht Endbenutzer), um Pakete zu veröffentlichen und Verbindungsgruppen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c424c-295">Enable only administrators (not end users) to publish packages and to enable connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-296">Informationen zu Verbindungsgruppen finden Sie unter <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> so wird es gemacht: zulassen, dass nur Administratoren Verbindungsgruppen aktivieren</span><span class="sxs-lookup"><span data-stu-id="c424c-296">For information about connection groups, see <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)">How to Allow Only Administrators to Enable Connection Groups</span></span></a></p>
<p><span data-ttu-id="c424c-297">Informationen zu Paketen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="c424c-297">For information about packages, see the following articles:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-298">Methode</span><span class="sxs-lookup"><span data-stu-id="c424c-298">Method</span></span></th>
<th align="left"><span data-ttu-id="c424c-299">Link zu weiteren Informationen</span><span class="sxs-lookup"><span data-stu-id="c424c-299">Link to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-300">Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="c424c-300">Management console</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="c424c-301">So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket</span><span class="sxs-lookup"><span data-stu-id="c424c-301">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-302">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c424c-302">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="c424c-303">So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="c424c-303">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-304">Elektronisches Software-Delivery-System von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="c424c-304">Third-party electronic software delivery system</span></span></p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)"><span data-ttu-id="c424c-305">So schränken Sie die Veröffentlichung von Paketen mithilfe einer ESD auf Administratoren ein</span><span class="sxs-lookup"><span data-stu-id="c424c-305">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-306">Aktivieren oder Deaktivieren einer Verbindungsgruppe für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="c424c-306">Enable or disable a connection group for a specific user</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-307">Administratoren können eine Verbindungsgruppe für einen bestimmten Benutzer aktivieren oder deaktivieren, indem Sie den optionalen <strong> -User- </strong> Parameter mit den folgenden Cmdlets verwenden:</span><span class="sxs-lookup"><span data-stu-id="c424c-307">Administrators can enable or disable a connection group for a specific user by using the optional <strong>–UserSID</strong> parameter with the following cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="c424c-308">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="c424c-308">Enable-AppVClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="c424c-309">Deaktivieren-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="c424c-309">Disable-AppVClientConnectionGroup</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)"><span data-ttu-id="c424c-310">So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="c424c-310">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-311">Zusammenführen identischer Paket Pfade zu einem virtuellen Verzeichnis in Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="c424c-311">Merging identical package paths into one virtual directory in connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-312">Wenn zwei oder mehr Pakete in einer Verbindungsgruppe identische Verzeichnispfade enthalten, werden die Pfade in einem einzigen virtuellen Verzeichnis innerhalb der virtuellen Umgebung der Verbindungsgruppe zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="c424c-312">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span></p>
<p><span data-ttu-id="c424c-313">Dieses Zusammenführen von Pfaden ermöglicht es einer Anwendung in einem Paket, auf Dateien zuzugreifen, die in einem anderen Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c424c-313">This merging of paths allows an application in one package to access files that are in a different package.</span></span></p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)"><span data-ttu-id="c424c-314">Über die virtuelle Verbindungsgruppenumgebung</span><span class="sxs-lookup"><span data-stu-id="c424c-314">About the Connection Group Virtual Environment</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a><span data-ttu-id="c424c-315">Administratoren können Pakete für einen bestimmten Benutzer veröffentlichen und deren Veröffentlichung aufheben.</span><span class="sxs-lookup"><span data-stu-id="c424c-315">Administrators can publish and unpublish packages for a specific user</span></span>


<span data-ttu-id="c424c-316">Administratoren können mithilfe der folgenden Cmdlets Pakete für einen bestimmten Benutzer veröffentlichen oder deren Veröffentlichung aufheben.</span><span class="sxs-lookup"><span data-stu-id="c424c-316">Administrators can use the following cmdlets to publish or unpublish packages for a specific user.</span></span> <span data-ttu-id="c424c-317">Um die Cmdlets zu verwenden, geben Sie den **-User-ID-** Parameter und dann die Sicherheits-ID (SID) des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="c424c-317">To use the cmdlets, enter the **–UserSID** parameter, followed by the user’s security identifier (SID).</span></span> <span data-ttu-id="c424c-318">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="c424c-318">For more information, see:</span></span>

-   [<span data-ttu-id="c424c-319">So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="c424c-319">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="c424c-320">So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="c424c-320">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-321">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c424c-321">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="c424c-322">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c424c-322">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-323">Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c424c-323">Publish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-324">Publish-AppvClientPackage "ContosoApplication"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="c424c-324">Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-325">Veröffentlichung aufheben – AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c424c-325">Unpublish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-326">UNPUBLISH-AppvClientPackage "ContosoApplication"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="c424c-326">Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a><span data-ttu-id="c424c-327">Nur Administratoren das Veröffentlichen und Aufheben der Veröffentlichung von Paketen ermöglichen</span><span class="sxs-lookup"><span data-stu-id="c424c-327">Enable only administrators to publish and unpublish packages</span></span>


<span data-ttu-id="c424c-328">Mit einer der folgenden Methoden können Sie nur Administratoren (nicht Endbenutzern) das Veröffentlichen und Aufheben der Veröffentlichung von Paketen ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="c424c-328">You can enable only administrators (not end users) to publish and unpublish packages by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-329">Methode</span><span class="sxs-lookup"><span data-stu-id="c424c-329">Method</span></span></th>
<th align="left"><span data-ttu-id="c424c-330">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c424c-330">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-331">Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="c424c-331">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-332">Navigieren Sie zum folgenden Gruppenrichtlinien-Objektknoten:</span><span class="sxs-lookup"><span data-stu-id="c424c-332">Navigate to the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="c424c-333">Computerkonfigurations &gt; Richtlinien &gt; Administrative Vorlagen &gt; System &gt; App-V &gt; Publishing </strong> .</span><span class="sxs-lookup"><span data-stu-id="c424c-333">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</strong>.</span></span></p>
<p><span data-ttu-id="c424c-334">Aktivieren Sie die <strong> </strong> Gruppenrichtlinieneinstellung Veröffentlichung als Administrator anfordern.</span><span class="sxs-lookup"><span data-stu-id="c424c-334">Enable the <strong>Require publish as administrator</strong> Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-335">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c424c-335">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)"><span data-ttu-id="c424c-336">So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="c424c-336">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a><span data-ttu-id="c424c-337">RunVirtual-Registrierungsschlüssel unterstützt Pakete, die für den Benutzer veröffentlicht werden</span><span class="sxs-lookup"><span data-stu-id="c424c-337">RunVirtual registry key supports packages that are published to the user</span></span>


<span data-ttu-id="c424c-338">App-V 5,0 SP3 bietet Unterstützung für die Verwendung des **RunVirtual** -Registrierungsschlüssels mit virtualisierten Anwendungen, die in vom Benutzer veröffentlichten Paketen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c424c-338">App-V 5.0 SP3 adds support for using the **RunVirtual** registry key with virtualized applications that are in user-published packages.</span></span> <span data-ttu-id="c424c-339">Mit dem Registrierungsschlüssel **RunVirtual** können Sie eine lokal installierte Anwendung in einer virtuellen Umgebung sowie Anwendungen ausführen, die mithilfe von App-V virtualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c424c-339">The **RunVirtual** registry key lets you run a locally installed application in a virtual environment, along with applications that have been virtualized by using App-V.</span></span>

<span data-ttu-id="c424c-340">Zuvor mussten die virtualisierten Anwendungen in App-V-Paketen Global veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="c424c-340">Previously, the virtualized applications in App-V packages had to be published globally.</span></span> <span data-ttu-id="c424c-341">Weitere Informationen zu **RunVirtual** und zu anderen Methoden zum Ausführen lokal installierter Anwendungen in einer virtuellen Umgebung mit virtualisierten Anwendungen finden Sie unter [Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierten Anwendungen](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="c424c-341">For more about **RunVirtual** and about other methods of running locally installed applications in a virtual environment with virtualized applications, see [Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span></span>

## <a href="" id="bkmk-posh-cmdlets-help"></a><span data-ttu-id="c424c-342">Neue PowerShell-Cmdlets und Hilfe zu aktualisierbaren Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c424c-342">New PowerShell cmdlets and updateable cmdlet help</span></span>


<span data-ttu-id="c424c-343">Neue PowerShell-Cmdlets und Hilfe zu aktualisierbaren Cmdlets sind in App-V 5,0 SP3 enthalten.</span><span class="sxs-lookup"><span data-stu-id="c424c-343">New PowerShell cmdlets and updateable cmdlet help are included in App-V 5.0 SP3.</span></span> <span data-ttu-id="c424c-344">Informationen zum Herunterladen der Cmdlet-Module finden Sie unter [Laden der PowerShell-Cmdlets und Abrufen der Cmdlet-Hilfe](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span><span class="sxs-lookup"><span data-stu-id="c424c-344">To download the cmdlet modules, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span></span>

### <span data-ttu-id="c424c-345">Neue App-V 5,0 SP3-Cmdlets für Server-PowerShell</span><span class="sxs-lookup"><span data-stu-id="c424c-345">New App-V 5.0 SP3 Server PowerShell cmdlets</span></span>

<span data-ttu-id="c424c-346">Neue Windows PowerShell-Cmdlets für den App-V-Server wurden hinzugefügt, um Sie beim Verwalten von Verbindungsgruppen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c424c-346">New Windows PowerShell cmdlets for the App-V Server have been added to help you manage connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-347">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c424c-347">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="c424c-348">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424c-348">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-349">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="c424c-349">Add-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-350">Fügt ein Paket an das Ende einer Verbindungsgruppe&#39;s-Paketliste an und ermöglicht Ihnen, das Paket als optional und/oder ohne Version innerhalb der Verbindungsgruppe zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c424c-350">Appends a package to the end of a connection group&#39;s package list and enables you to configure the package as optional and/or with no version within the connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-351">Satz-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="c424c-351">Set-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-352">Ermöglicht es Ihnen, Details zum Verbindungsgruppen Paket zu bearbeiten, beispielsweise, ob es optional ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-352">Enables you to edit details about the connection group package, such as whether it is optional.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-353">Remove-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="c424c-353">Remove-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-354">Entfernt ein Paket aus einer Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c424c-354">Removes a package from a connection group.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="c424c-355">Aufrufen von Hilfe zu den PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c424c-355">Getting help for the PowerShell cmdlets</span></span>

<span data-ttu-id="c424c-356">Die Hilfe zu einem Cmdlet steht in den folgenden Formaten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="c424c-356">Cmdlet help is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-357">Format</span><span class="sxs-lookup"><span data-stu-id="c424c-357">Format</span></span></th>
<th align="left"><span data-ttu-id="c424c-358">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424c-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-359">Als herunterladbares Modul</span><span class="sxs-lookup"><span data-stu-id="c424c-359">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-360">So erhalten Sie die neueste Hilfe nach dem Herunterladen des Cmdlet-Moduls:</span><span class="sxs-lookup"><span data-stu-id="c424c-360">To get the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="c424c-361">Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="c424c-361">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="c424c-362">Geben Sie einen der folgenden Befehle ein, um die Cmdlets für das gewünschte Modul zu laden:</span><span class="sxs-lookup"><span data-stu-id="c424c-362">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-363">App-V-Komponente</span><span class="sxs-lookup"><span data-stu-id="c424c-363">App-V component</span></span></th>
<th align="left"><span data-ttu-id="c424c-364">Befehl zum eingeben</span><span class="sxs-lookup"><span data-stu-id="c424c-364">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-365">App-V-Server</span><span class="sxs-lookup"><span data-stu-id="c424c-365">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-366">Update-Hilfe-Modul AppvServer</span><span class="sxs-lookup"><span data-stu-id="c424c-366">Update-Help-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-367">App-V-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="c424c-367">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-368">Update-Hilfe-Modul AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="c424c-368">Update-Help-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-369">App-V-Client</span><span class="sxs-lookup"><span data-stu-id="c424c-369">App-V client</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-370">Update-Hilfe-Modul AppvClient</span><span class="sxs-lookup"><span data-stu-id="c424c-370">Update-Help-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-371">Auf TechNet als Web-Seiten</span><span class="sxs-lookup"><span data-stu-id="c424c-371">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-372">Weitere Informationen finden Sie unter App-V-Knoten unter <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Microsoft Desktop Optimization Pack-Automatisierung mit Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="c424c-372">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="c424c-373">Weitere Informationen finden Sie unter [Laden der PowerShell-Cmdlets und Abrufen der Cmdlet-Hilfe](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span><span class="sxs-lookup"><span data-stu-id="c424c-373">For more information, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span></span>

## <a href="" id="bkmk-pvad-hidden"></a><span data-ttu-id="c424c-374">Primäres virtuelles Anwendungsverzeichnis (PVAD) ist ausgeblendet, kann aber aktiviert werden</span><span class="sxs-lookup"><span data-stu-id="c424c-374">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>


<span data-ttu-id="c424c-375">Das primäre Virtual Application Directory (PVAD) ist in App-V 5,0 SP3 ausgeblendet, Sie können es aber wieder aktivieren und mit einer der folgenden Methoden sichtbar machen:</span><span class="sxs-lookup"><span data-stu-id="c424c-375">The primary virtual application directory (PVAD) is hidden in App-V 5.0 SP3, but you can turn it back on and make it visible by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-376">Methode</span><span class="sxs-lookup"><span data-stu-id="c424c-376">Method</span></span></th>
<th align="left"><span data-ttu-id="c424c-377">Schritte</span><span class="sxs-lookup"><span data-stu-id="c424c-377">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c424c-378">Verwenden eines Befehlszeilenparameters</span><span class="sxs-lookup"><span data-stu-id="c424c-378">Use a command line parameter</span></span></p></td>
<td align="left"><p><span data-ttu-id="c424c-379">Übergeben <strong> Sie den Parameter – EnablePVADControl </strong> an den <strong>Sequencer.exe</strong> .</span><span class="sxs-lookup"><span data-stu-id="c424c-379">Pass the <strong>–EnablePVADControl</strong> parameter to the <strong>Sequencer.exe</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c424c-380">Erstellen eines Registrierungsunterschlüssels</span><span class="sxs-lookup"><span data-stu-id="c424c-380">Create a registry subkey</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="c424c-381">Navigieren Sie im Registrierungs-Editor zu:</span><span class="sxs-lookup"><span data-stu-id="c424c-381">In the Registry Editor, navigate to:</span></span> <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong><span data-ttu-id="c424c-382">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="c424c-382">Note</span></span></strong><br/><p><span data-ttu-id="c424c-383">Wenn der unter <code>Compatibility</code> Schlüssel nicht vorhanden ist, müssen Sie ihn erstellen.</span><span class="sxs-lookup"><span data-stu-id="c424c-383">If the <code>Compatibility</code> subkey doesn’t exist, you must create it.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="c424c-384">Erstellen Sie einen DWORD-Wert mit dem Namen <strong> EnablePVADControl </strong> , und legen Sie den Wert auf <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="c424c-384">Create a DWORD Value named <strong>EnablePVADControl</strong>, and set the value to <strong>1</strong>.</span></span></p>
<p><span data-ttu-id="c424c-385">Der Wert <strong> 0 </strong> bedeutet, dass PVAD ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="c424c-385">A value of <strong>0</strong> means that PVAD is hidden.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>



<span data-ttu-id="c424c-386">**Weitere Informationen zu PVAD:** Wenn Sie zum Erstellen eines Pakets den Sequencer verwenden, können Sie einen beliebigen Installationspfad für das Paket eingeben.</span><span class="sxs-lookup"><span data-stu-id="c424c-386">**More about PVAD:** When you use the Sequencer to create a package, you can enter any installation path for the package.</span></span> <span data-ttu-id="c424c-387">In früheren Versionen von App-V mussten Sie das primäre Virtual Application Directory (PVAD) der Anwendung als Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="c424c-387">In past versions of App-V, you were required to specify the primary virtual application directory (PVAD) of the application as the path.</span></span> <span data-ttu-id="c424c-388">PVAD ist das Verzeichnis, in dem Sie normalerweise eine Anwendung auf Ihrem lokalen Computer installieren würden, wenn Sie App-V nicht verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="c424c-388">PVAD is the directory to which you would typically install an application on your local computer if you weren’t using App-V.</span></span> <span data-ttu-id="c424c-389">Wenn Sie beispielsweise Office auf einem Computer installiert haben, wäre das PVAD in der Regel c:\\Programme c:\\Programme\\Microsoft Office\\.</span><span class="sxs-lookup"><span data-stu-id="c424c-389">For example, if you were installing Office on a computer, the PVAD typically would be C:\\Program Files\\Microsoft Office\\.</span></span>

## <a href="" id="bkmk-pub-metadata-clientversion"></a><span data-ttu-id="c424c-390">Clientversion ist erforderlich, um die App-V-Veröffentlichungsmetadaten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c424c-390">ClientVersion is required to view App-V publishing metadata</span></span>


<span data-ttu-id="c424c-391">In App-v 5,0 SP3 müssen Sie die folgenden Werte in der Adresse angeben, wenn Sie den App-v-Veröffentlichungsserver nach Metadaten Abfragen:</span><span class="sxs-lookup"><span data-stu-id="c424c-391">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c424c-392">Wert</span><span class="sxs-lookup"><span data-stu-id="c424c-392">Value</span></span></th>
<th align="left"><span data-ttu-id="c424c-393">Zusätzliche Details</span><span class="sxs-lookup"><span data-stu-id="c424c-393">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c424c-394">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="c424c-394">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c424c-395">Wenn Sie den <strong> Clientversion </strong> -Parameter aus der Abfrage weglassen, schließen die Metadaten die neuen App-V 5,0 SP3-Features aus.</span><span class="sxs-lookup"><span data-stu-id="c424c-395">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c424c-396">Kunden</span><span class="sxs-lookup"><span data-stu-id="c424c-396">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c424c-397">Sie müssen diesen Wert nur angeben, wenn Sie beim Sequenzieren des Pakets bestimmte Clientbetriebssysteme auswählen.</span><span class="sxs-lookup"><span data-stu-id="c424c-397">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="c424c-398">Wenn Sie die Standardeinstellung (alle Betriebssysteme) auswählen, geben Sie diesen Wert in der Abfrage nicht an.</span><span class="sxs-lookup"><span data-stu-id="c424c-398">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="c424c-399">Wenn Sie den <strong> Client </strong> -Parameter aus der Abfrage weglassen, werden nur die Pakete, die für die Unterstützung eines beliebigen Betriebssystems sequenziert wurden, in den Metadaten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c424c-399">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="c424c-400">Syntax und Beispiele für diese Abfrage finden Sie unter [Anzeigen von App-V Server-Veröffentlichungsmetadaten](viewing-app-v-server-publishing-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="c424c-400">For syntax and examples of this query, see [Viewing App-V Server Publishing Metadata](viewing-app-v-server-publishing-metadata.md).</span></span>

## <a href="" id="bkmk-event-logs-moved"></a><span data-ttu-id="c424c-401">App-V-Ereignisprotokolle wurden konsolidiert</span><span class="sxs-lookup"><span data-stu-id="c424c-401">App-V event logs have been consolidated</span></span>


<span data-ttu-id="c424c-402">Die folgenden Ereignisprotokolle, die sich zuvor bei **Applications and Services Logs/Microsoft/AppV/ &lt; App-V &gt; -Komponenten**befanden, wurden in **Anwendungen und Dienstprotokolle/Microsoft/AppV/ServiceLog**verschoben.</span><span class="sxs-lookup"><span data-stu-id="c424c-402">The following event logs, previously located at **Applications and Services Logs/Microsoft/AppV/&lt;App-V component&gt;**, have been moved to **Applications and Services Logs/Microsoft/AppV/ServiceLog**.</span></span>

<span data-ttu-id="c424c-403">Wenn Sie die Protokolle anzeigen möchten **, wählen Sie** &gt; in der Ereignisanzeige Anwendung die Option **Analyse-und Debug-Protokolle** anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="c424c-403">To view the logs, select **View** &gt; **Show Analytic and Debug Logs** in the Event Viewer application.</span></span>

<span data-ttu-id="c424c-404">Client-catalog Client-Integration Client-Orchestrierungs Client-PackageConfig Client-Scripting Client-Service Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary-Subsysteme-ActiveX-Subsysteme-AppPath-Subsystem-com-Subsysteme-FTA</span><span class="sxs-lookup"><span data-stu-id="c424c-404">Client-Catalog Client-Integration Client-Orchestration Client-PackageConfig Client-Scripting Client-Service Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary Subsystems-ActiveX Subsystems-AppPath Subsystems-Com Subsystems-fta</span></span>

## <span data-ttu-id="c424c-405">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="c424c-405">How to Get MDOP Technologies</span></span>


<span data-ttu-id="c424c-406">App-V ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="c424c-406">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="c424c-407">MDOP ist Teil von Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="c424c-407">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="c424c-408">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="c424c-408">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="c424c-409">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c424c-409">Related topics</span></span>


[<span data-ttu-id="c424c-410">Versionshinweise für App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="c424c-410">Release Notes for App-V 5.0 SP3</span></span>](release-notes-for-app-v-50-sp3.md)









