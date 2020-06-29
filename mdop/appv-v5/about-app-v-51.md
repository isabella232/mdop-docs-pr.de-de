---
title: Informationen zu App-V 5.1
description: Informationen zu App-V 5.1
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806110"
---
# <span data-ttu-id="5234e-103">Informationen zu App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5234e-103">About App-V 5.1</span></span>


<span data-ttu-id="5234e-104">Verwenden Sie die folgenden Abschnitte, um Informationen zu bedeutenden Änderungen zu überprüfen, die für Application Virtualization (App-V) 5,1 gelten:</span><span class="sxs-lookup"><span data-stu-id="5234e-104">Use the following sections to review information about significant changes that apply to Application Virtualization (App-V) 5.1:</span></span>

[<span data-ttu-id="5234e-105">App-V 5,1-Softwarevoraussetzungen und unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5234e-105">App-V 5.1 software prerequisites and supported configurations</span></span>](#bkmk-51-prereq-configs)

[<span data-ttu-id="5234e-106">Migrieren zu App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-106">Migrating to App-V 5.1</span></span>](#bkmk-migrate-to-51)

[<span data-ttu-id="5234e-107">Neuerungen in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-107">What’s New in App-V 5.1</span></span>](#bkmk-whatsnew)

[<span data-ttu-id="5234e-108">App-V-Unterstützung für Windows 10</span><span class="sxs-lookup"><span data-stu-id="5234e-108">App-V support for Windows 10</span></span>](#bkmk-win10support)

[<span data-ttu-id="5234e-109">Änderungen der App-V-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="5234e-109">App-V Management Console Changes</span></span>](#bkmk-mgmtconsole)

[<span data-ttu-id="5234e-110">Verbesserungen des Sequencers</span><span class="sxs-lookup"><span data-stu-id="5234e-110">Sequencer Improvements</span></span>](#bkmk-seqimprove)

[<span data-ttu-id="5234e-111">Verbesserungen beim Paket Konverter</span><span class="sxs-lookup"><span data-stu-id="5234e-111">Improvements to Package Converter</span></span>](#bkmk-pkgconvimprove)

[<span data-ttu-id="5234e-112">Unterstützung für mehrere Skripts in einem einzelnen Ereignisauslöser</span><span class="sxs-lookup"><span data-stu-id="5234e-112">Support for multiple scripts on a single event trigger</span></span>](#bkmk-supmultscripts)

[<span data-ttu-id="5234e-113">Hartcodierter Pfad zum Installationsordner wird an das virtuelle Dateisystem-Stammverzeichnis umgeleitet</span><span class="sxs-lookup"><span data-stu-id="5234e-113">Hardcoded path to installation folder is redirected to virtual file system root</span></span>](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a><span data-ttu-id="5234e-114">App-V 5,1-Softwarevoraussetzungen und unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5234e-114">App-V 5.1 software prerequisites and supported configurations</span></span>


<span data-ttu-id="5234e-115">Unter den folgenden Links finden Sie die Voraussetzungen für die App-V 5,1-Software und die unterstützten Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="5234e-115">See the following links for the App-V 5.1 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5234e-116">Links zu Voraussetzungen und unterstützten Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5234e-116">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="5234e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5234e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)"><span data-ttu-id="5234e-118">Voraussetzungen für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5234e-118">App-V 5.1 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="5234e-119">Erforderliche Software, die Sie vor dem Starten der App-V 5,1-Installation installieren müssen</span><span class="sxs-lookup"><span data-stu-id="5234e-119">Prerequisite software that you must install before starting the App-V 5.1 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="5234e-120">App-V 5.1 – Unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5234e-120">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="5234e-121">Unterstützte Betriebssysteme und Hardwareanforderungen für App-V Server, Sequencer und Client Komponenten</span><span class="sxs-lookup"><span data-stu-id="5234e-121">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="5234e-122">**Unterstützung für die Verwendung von Configuration Manager mit App-V:** App-V 5,1 unterstützt System Center 2012 R2 Configuration Manager SP1.</span><span class="sxs-lookup"><span data-stu-id="5234e-122">**Support for using Configuration Manager with App-V:** App-V 5.1 supports System Center 2012 R2 Configuration Manager SP1.</span></span> <span data-ttu-id="5234e-123">Informationen zum Integrieren ihrer App-v-Umgebung in Configuration Manager und Configuration Manager finden Sie unter [Planen der APP-v-Integration in Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5234e-123">See [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) for information about integrating your App-V environment with Configuration Manager and Configuration Manager.</span></span>

## <a href="" id="bkmk-migrate-to-51"></a><span data-ttu-id="5234e-124">Migrieren zu App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-124">Migrating to App-V 5.1</span></span>


<span data-ttu-id="5234e-125">Verwenden Sie die folgenden Informationen, um aus früheren Versionen auf App-V 5,1 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-125">Use the following information to upgrade to App-V 5.1 from earlier versions.</span></span> <span data-ttu-id="5234e-126">Weitere Informationen finden Sie unter [Migrieren zu App-V 5,1 aus einer früheren Version](migrating-to-app-v-51-from-a-previous-version.md) .</span><span class="sxs-lookup"><span data-stu-id="5234e-126">See [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md) for more information.</span></span>

### <span data-ttu-id="5234e-127">Vor dem Starten des Upgrades</span><span class="sxs-lookup"><span data-stu-id="5234e-127">Before you start the upgrade</span></span>

<span data-ttu-id="5234e-128">Überprüfen Sie die folgenden Informationen, bevor Sie das Upgrade starten:</span><span class="sxs-lookup"><span data-stu-id="5234e-128">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5234e-129">Zu überprüfende Elemente vor dem Upgrade</span><span class="sxs-lookup"><span data-stu-id="5234e-129">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="5234e-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5234e-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-131">Zu aktualisierbare Komponenten in beliebiger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="5234e-131">Components to upgrade, in any order</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="5234e-132">App-V-Server</span><span class="sxs-lookup"><span data-stu-id="5234e-132">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="5234e-133">Sequencer</span><span class="sxs-lookup"><span data-stu-id="5234e-133">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="5234e-134">App-v Client oder App-v Remote Desktop Dienste (RDS)-Client</span><span class="sxs-lookup"><span data-stu-id="5234e-134">App-V Client or App-V Remote Desktop Services (RDS) Client</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="5234e-135">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5234e-135">Note</span></span></strong><br/><p><span data-ttu-id="5234e-136">Vor App-v 5,0 SP2 wurde die Client Verwaltungsbenutzeroberfläche mit der APP-v-Clientinstallation bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5234e-136">Prior to App-V 5.0 SP2, the Client Management User Interface (UI) was provided with the App-V Client installation.</span></span> <span data-ttu-id="5234e-137">Für App-V 5,0 SP2-Installationen (oder höher) können Sie die Benutzeroberfläche der Clientverwaltung verwenden, indem Sie die <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> Benutzeroberflächenanwendung Application Virtualization 5,0 Client herunterladen </a> .</span><span class="sxs-lookup"><span data-stu-id="5234e-137">For App-V 5.0 SP2 installations (or later), you can use the Client Management UI by downloading from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5234e-138">Aktualisieren von App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="5234e-138">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-139">Sie müssen zuerst auf App-V 5,0 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-139">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="5234e-140">Sie können nicht direkt von App-v 4. x auf App-v 5,1 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-140">You cannot upgrade directly from App-V 4.x to App-V 5.1.</span></span> <span data-ttu-id="5234e-141">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="5234e-141">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="5234e-142">"Unterschiede zwischen App-v 4,6 und App-v 5,0" in der <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> App-v 5,0</span><span class="sxs-lookup"><span data-stu-id="5234e-142">“Differences between App-V 4.6 and App-V 5.0” in <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">About App-V 5.0</span></span></a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="5234e-143">Planen der Migration von einer früheren Version von App-V</span><span class="sxs-lookup"><span data-stu-id="5234e-143">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-144">Aktualisieren von App-V 5,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5234e-144">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-145">Sie können direkt von einer der folgenden Versionen auf App-V 5,1 aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="5234e-145">You can upgrade to App-V 5.1 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="5234e-146">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="5234e-146">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="5234e-147">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="5234e-147">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="5234e-148">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="5234e-148">App-V 5.0 SP2</span></span></p></li>
<li><p><span data-ttu-id="5234e-149">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="5234e-149">App-V 5.0 SP3</span></span></p></li>
</ul>
<p><span data-ttu-id="5234e-150">Führen Sie die Schritte in den verbleibenden Abschnitten dieses Themas aus, um auf App-V 5,1 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-150">To upgrade to App-V 5.1, follow the steps in the remaining sections of this topic.</span></span></p>
<p><span data-ttu-id="5234e-151">Pakete und Verbindungsgruppen funktionieren weiterhin mit App-V 5,1, wie dies derzeit der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="5234e-151">Packages and connection groups will continue to work with App-V 5.1 as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="5234e-152">Schritte zum Upgrade der App-V-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="5234e-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="5234e-153">Führen Sie die folgenden Schritte aus, um die einzelnen Komponenten der APP-v-Infrastruktur auf App-v 5,1 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.1.</span></span> <span data-ttu-id="5234e-154">Die folgende Reihenfolge ist nur ein Vorschlag; Sie können Komponenten in beliebiger Reihenfolge aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-154">The following order is only a suggestion; you may upgrade components in any order.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5234e-155">Schritt</span><span class="sxs-lookup"><span data-stu-id="5234e-155">Step</span></span></th>
<th align="left"><span data-ttu-id="5234e-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5234e-156">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-157">Schritt 1: Aktualisieren Sie den App-V-Server.</span><span class="sxs-lookup"><span data-stu-id="5234e-157">Step 1: Upgrade the App-V Server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5234e-158">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5234e-158">Note</span></span></strong><br/><p><span data-ttu-id="5234e-159">Wenn Sie den App-V-Server nicht verwenden, überspringen Sie diesen Schritt, und fahren Sie mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="5234e-159">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="5234e-160">Führen Sie folgende Schritte aus: </span><span class="sxs-lookup"><span data-stu-id="5234e-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="5234e-161">Führen Sie eine der folgenden Aktionen aus, je nachdem, welche Methode Sie verwenden, um die Verwaltungsdatenbank und/oder die Berichtsdatenbank zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="5234e-161">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5234e-162">Daten Bank Aktualisierungsmethode</span><span class="sxs-lookup"><span data-stu-id="5234e-162">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="5234e-163">Schritt</span><span class="sxs-lookup"><span data-stu-id="5234e-163">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-164">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5234e-164">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-165">Überspringen Sie diesen Schritt, und wechseln Sie zu Schritt 2, "Wenn Sie den App-V-Server aktualisieren..."</span><span class="sxs-lookup"><span data-stu-id="5234e-165">Skip this step and go to step 2, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5234e-166">SQL-Skripts</span><span class="sxs-lookup"><span data-stu-id="5234e-166">SQL scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-167">Führen Sie die Schritte unter <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> Vorgehensweise zum Bereitstellen der App-V-Datenbanken mithilfe von SQL-Skripts aus </a> .</span><span class="sxs-lookup"><span data-stu-id="5234e-167">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<li><p><span data-ttu-id="5234e-168">Wenn Sie den App-v-Server vom APP-v 5,0 SP1-Hotfix-Paket 3 oder höher aktualisieren, führen Sie die Schritte in Abschnitt <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> Überprüfen der Registrierungsschlüssel nach der Installation des App-v 5,0 SP3-Servers aus </a> .</span><span class="sxs-lookup"><span data-stu-id="5234e-168">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="5234e-169">Führen Sie die Schritte unter <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> Bereitstellen des App-V 5,1-Servers aus.</span><span class="sxs-lookup"><span data-stu-id="5234e-169">Follow the steps in <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5234e-170">Schritt 2: Aktualisieren Sie den App-V-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="5234e-170">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-171">Weitere Informationen finden Sie unter <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Installieren des Sequencers </a> .</span><span class="sxs-lookup"><span data-stu-id="5234e-171">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-172">Schritt 3: Aktualisieren Sie den App-v-Client oder den App-v-RDS-Client.</span><span class="sxs-lookup"><span data-stu-id="5234e-172">Step 3: Upgrade the App-V Client or App-V RDS Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-173">Weitere Informationen finden Sie unter <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> Bereitstellen des App-V-Clients </a> .</span><span class="sxs-lookup"><span data-stu-id="5234e-173">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5234e-174">Konvertieren von Paketen, die mit einer früheren Version von App-V erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="5234e-174">Converting packages created using a prior version of App-V</span></span>

<span data-ttu-id="5234e-175">Verwenden Sie das Paket Konverter-Dienstprogramm, um virtuelle Anwendungspakete zu aktualisieren, die mit den Versionen von App-v vor App-v 5,0 erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5234e-175">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="5234e-176">Der Paket Konverter verwendet PowerShell zum Konvertieren von Paketen und kann die Automatisierung des Prozesses unterstützen, wenn viele Pakete vorhanden sind, für die eine Konvertierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5234e-176">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

**<span data-ttu-id="5234e-177">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5234e-177">Note</span></span>**  
<span data-ttu-id="5234e-178">App-v 5,1-Pakete sind genauso wie App-v 5,0-Pakete.</span><span class="sxs-lookup"><span data-stu-id="5234e-178">App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="5234e-179">Es wurde keine Änderung des Paketformats zwischen den Versionen vorgenommen, und daher ist es nicht erforderlich, App-v 5,0-Pakete in App-v 5,1-Pakete zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-179">There has been no change in the package format between the versions and so there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>



## <a href="" id="bkmk-whatsnew"></a><span data-ttu-id="5234e-180">Neuerungen in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-180">What’s New in App-V 5.1</span></span>


<span data-ttu-id="5234e-181">Diese Abschnitte gelten für Benutzer, die bereits mit App-v vertraut sind und wissen möchten, was sich in App-v 5,1 geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5234e-181">These sections are for users who are already familiar with App-V and want to know what has changed in App-V 5.1.</span></span> <span data-ttu-id="5234e-182">Wenn Sie noch nicht mit App-v vertraut sind, sollten Sie zunächst die [Planung für App-v 5,1](planning-for-app-v-51.md)lesen.</span><span class="sxs-lookup"><span data-stu-id="5234e-182">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.1](planning-for-app-v-51.md).</span></span>

### <a href="" id="bkmk-win10support"></a><span data-ttu-id="5234e-183">App-V-Unterstützung für Windows 10</span><span class="sxs-lookup"><span data-stu-id="5234e-183">App-V support for Windows 10</span></span>

<span data-ttu-id="5234e-184">Die folgende Tabelle enthält die Windows 10-Unterstützung für App-V.</span><span class="sxs-lookup"><span data-stu-id="5234e-184">The following table lists the Windows 10 support for App-V.</span></span> <span data-ttu-id="5234e-185">Windows 10 wird in den Versionen von App-v vor App-v 5,1 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5234e-185">Windows 10 is not supported in versions of App-V prior to App-V 5.1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5234e-186">Komponente</span><span class="sxs-lookup"><span data-stu-id="5234e-186">Component</span></span></th>
<th align="left"><span data-ttu-id="5234e-187">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5234e-187">App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="5234e-188">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="5234e-188">App-V 5.0</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-189">App-V-Client</span><span class="sxs-lookup"><span data-stu-id="5234e-189">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-190">Ja</span><span class="sxs-lookup"><span data-stu-id="5234e-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-191">Nein</span><span class="sxs-lookup"><span data-stu-id="5234e-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5234e-192">App-V RDS-Client</span><span class="sxs-lookup"><span data-stu-id="5234e-192">App-V RDS Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-193">Ja</span><span class="sxs-lookup"><span data-stu-id="5234e-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-194">Nein</span><span class="sxs-lookup"><span data-stu-id="5234e-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-195">App-V-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="5234e-195">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-196">Ja</span><span class="sxs-lookup"><span data-stu-id="5234e-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-197">Nein</span><span class="sxs-lookup"><span data-stu-id="5234e-197">No</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a><span data-ttu-id="5234e-198">Änderungen der App-V-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="5234e-198">App-V Management Console Changes</span></span>

<span data-ttu-id="5234e-199">In diesem Abschnitt werden die aktuelle und die vorherige Funktionalität der App-V-Verwaltungskonsole verglichen.</span><span class="sxs-lookup"><span data-stu-id="5234e-199">This section compares the App-V Management Console’s current and previous functionality.</span></span>

### <span data-ttu-id="5234e-200">Silverlight ist nicht mehr erforderlich</span><span class="sxs-lookup"><span data-stu-id="5234e-200">Silverlight is no longer required</span></span>

<span data-ttu-id="5234e-201">Für die Benutzeroberfläche der Verwaltungskonsole ist Silverlight nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5234e-201">The Management Console UI no longer requires Silverlight.</span></span> <span data-ttu-id="5234e-202">Die 5,1-Verwaltungskonsole ist auf HTML5 und JavaScript aufgebaut.</span><span class="sxs-lookup"><span data-stu-id="5234e-202">The 5.1 Management Console is built on HTML5 and Javascript.</span></span>

### <span data-ttu-id="5234e-203">Benachrichtigungen und Nachrichten werden in einem Dialogfeld einzeln angezeigt</span><span class="sxs-lookup"><span data-stu-id="5234e-203">Notifications and messages are displayed individually in a dialog box</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5234e-204">Neu in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-204">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="5234e-205">Vor App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-205">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5234e-206">Indikator für die Anzahl der Nachrichten:</span><span class="sxs-lookup"><span data-stu-id="5234e-206">Number of messages indicator:</span></span></strong></p>
<p><span data-ttu-id="5234e-207">Auf der Titelleiste der App-V-Verwaltungskonsole wird nun neben einem Kennzeichnungssymbol eine Zahl angezeigt, die die Anzahl der Nachrichten angibt, die gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5234e-207">On the title bar of the App-V Management Console, a number is now displayed next to a flag icon to indicate the number of messages that are waiting to be read.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-208">Sie können jeweils nur eine Nachricht oder einen Fehler sehen, und Sie konnten nicht feststellen, wie viele Nachrichten vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="5234e-208">You could see only one message or error at a time, and you were unable to determine how many messages there were.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5234e-209">Nachrichtendarstellung:</span><span class="sxs-lookup"><span data-stu-id="5234e-209">Message appearance:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5234e-210">Nachrichten, die eine Benutzereingabe erfordern, werden in einem separaten Dialogfeld angezeigt, das oben auf der aktuellen Seite angezeigt wird, die Sie gerade anzeigen, und eine Antwort anfordern, bevor Sie Sie schließen können.</span><span class="sxs-lookup"><span data-stu-id="5234e-210">Messages that require user input appear in a separate dialog box that displays on top of the current page that you were viewing, and require a response before you can dismiss them.</span></span></p></li>
<li><p><span data-ttu-id="5234e-211">Nachrichten und Fehler werden in einer Liste mit einer unter dem anderen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5234e-211">Messages and errors appear in a list, with one beneath the other.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="5234e-212">Sie können jeweils nur eine Nachricht oder einen Fehler sehen.</span><span class="sxs-lookup"><span data-stu-id="5234e-212">You could see only one message or error at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5234e-213">Nachrichten werden nicht mehr angezeigt:</span><span class="sxs-lookup"><span data-stu-id="5234e-213">Dismissing messages:</span></span></strong></p>
<p><span data-ttu-id="5234e-214">Verwenden Sie den <strong> Link alle verwerfen, </strong> um alle Nachrichten und Fehler gleichzeitig zu schließen oder einzeln zu schließen.</span><span class="sxs-lookup"><span data-stu-id="5234e-214">Use the <strong>Dismiss All</strong> link to dismiss all messages and errors at one time, or dismiss them one at a time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-215">Sie können Nachrichten und Fehler nur jeweils einzeln entlassen.</span><span class="sxs-lookup"><span data-stu-id="5234e-215">You could dismiss messages and errors only one at a time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5234e-216">Konsolenseiten sind nun getrennte URLs</span><span class="sxs-lookup"><span data-stu-id="5234e-216">Console pages are now separate URLs</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5234e-217">Neu in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-217">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="5234e-218">Vor App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-218">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-219">Jede Seite in der Konsole hat eine andere URL, mit der Sie bestimmte Seiten für den schnellen Zugriff in Zukunft mit einer Textmarke versehen können.</span><span class="sxs-lookup"><span data-stu-id="5234e-219">Each page in the console has a different URL, which enables you to bookmark specific pages for quick access in the future.</span></span></p>
<p><span data-ttu-id="5234e-220">Die Zahl, die in einigen URLs angezeigt wird, gibt das jeweilige Paket an.</span><span class="sxs-lookup"><span data-stu-id="5234e-220">The number that appears in some URLs indicates the specific package.</span></span> <span data-ttu-id="5234e-221">Diese Nummern sind eindeutig.</span><span class="sxs-lookup"><span data-stu-id="5234e-221">These numbers are unique.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-222">Auf alle Konsolenseiten wird über die gleiche URL zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="5234e-222">All console pages are accessed through the same URL.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5234e-223">Neue, getrennte Seite für Verbindungsgruppen und Menüoption</span><span class="sxs-lookup"><span data-stu-id="5234e-223">New, separate CONNECTION GROUPS page and menu option</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5234e-224">Neu in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-224">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="5234e-225">Vor App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-225">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-226">Die Seite "Verbindungsgruppen" ist jetzt Teil des Hauptmenüs, auf der gleichen Ebene wie die Seite "Pakete".</span><span class="sxs-lookup"><span data-stu-id="5234e-226">The CONNECTION GROUPS page is now part of the main menu, at the same level as the PACKAGES page.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-227">Wenn Sie die Seite Verbindungsgruppen öffnen möchten, navigieren Sie auf der Seite Pakete.</span><span class="sxs-lookup"><span data-stu-id="5234e-227">To open the CONNECTION GROUPS page, you navigate through the PACKAGES page.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5234e-228">Menü Optionen für Pakete wurden geändert</span><span class="sxs-lookup"><span data-stu-id="5234e-228">Menu options for packages have changed</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5234e-229">Neu in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-229">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="5234e-230">Vor App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5234e-230">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5234e-231">Die folgenden Optionen sind jetzt Schaltflächen, die unten auf der Seite "Pakete" angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="5234e-231">The following options are now buttons that appear at the bottom of the PACKAGES page:</span></span></p>
<ul>
<li><p><span data-ttu-id="5234e-232">Hinzufügen oder aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5234e-232">Add or Upgrade</span></span></p></li>
<li><p><span data-ttu-id="5234e-233">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="5234e-233">Publish</span></span></p></li>
<li><p><span data-ttu-id="5234e-234">Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="5234e-234">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="5234e-235">Delete</span><span class="sxs-lookup"><span data-stu-id="5234e-235">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="5234e-236">Die folgenden Optionen werden weiterhin angezeigt, wenn Sie mit der rechten Maustaste auf ein Paket klicken, um das Dropdown-Kontextmenü zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="5234e-236">The following options will still appear when you right-click a package to open the drop-down context menu:</span></span></p>
<ul>
<li><p><span data-ttu-id="5234e-237">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="5234e-237">Publish</span></span></p></li>
<li><p><span data-ttu-id="5234e-238">Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="5234e-238">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="5234e-239">Bearbeiten von anzeigen Zugriffen</span><span class="sxs-lookup"><span data-stu-id="5234e-239">Edit AD Access</span></span></p></li>
<li><p><span data-ttu-id="5234e-240">Bearbeiten der Bereitstellungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="5234e-240">Edit Deployment Config</span></span></p></li>
<li><p><span data-ttu-id="5234e-241">Bereitstellungskonfiguration übertragen von...</span><span class="sxs-lookup"><span data-stu-id="5234e-241">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="5234e-242">Zugriff und Konfiguration übertragen von...</span><span class="sxs-lookup"><span data-stu-id="5234e-242">Transfer access and configuration from…</span></span></p></li>
<li><p><span data-ttu-id="5234e-243">Delete</span><span class="sxs-lookup"><span data-stu-id="5234e-243">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="5234e-244">Wenn Sie auf <strong> Löschen klicken, </strong> um ein Paket zu entfernen, wird ein Dialogfeld geöffnet, in dem Sie aufgefordert werden, zu bestätigen, dass Sie das Paket löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="5234e-244">When you click <strong>Delete</strong> to remove a package, a dialog box opens and asks you to confirm that you want to delete the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5234e-245">Die <strong> Option zum Hinzufügen oder aktualisieren </strong> war eine Schaltfläche oben rechts auf der Seite "Pakete".</span><span class="sxs-lookup"><span data-stu-id="5234e-245">The <strong>Add or Upgrade</strong> option was a button at the top right of the PACKAGES page.</span></span></p>
<p><span data-ttu-id="5234e-246">Die <strong> Optionen zum Veröffentlichen, Aufheben der </strong> <strong> Veröffentlichung </strong> und zum <strong> Löschen </strong> waren nur verfügbar, wenn Sie in der Liste Pakete mit der rechten Maustaste auf einen Paketnamen geklickt haben.</span><span class="sxs-lookup"><span data-stu-id="5234e-246">The <strong>Publish</strong>, <strong>Unpublish</strong>, and <strong>Delete</strong> options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5234e-247">Die folgenden Paketvorgänge sind jetzt Schaltflächen auf der Paketdetailseite für jedes Paket:</span><span class="sxs-lookup"><span data-stu-id="5234e-247">The following package operations are now buttons on the package details page for each package:</span></span></p>
<ul>
<li><p><span data-ttu-id="5234e-248">Übertragen (Dropdownmenü mit den folgenden Optionen):</span><span class="sxs-lookup"><span data-stu-id="5234e-248">Transfer (drop-down menu with the following options):</span></span></p>
<ul>
<li><p><span data-ttu-id="5234e-249">Bereitstellungskonfiguration übertragen von...</span><span class="sxs-lookup"><span data-stu-id="5234e-249">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="5234e-250">Zugriff und Konfiguration übertragen von...</span><span class="sxs-lookup"><span data-stu-id="5234e-250">Transfer access and configuration from…</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="5234e-251">Bearbeiten (Verbindungsgruppen und anzeigen Zugriff)</span><span class="sxs-lookup"><span data-stu-id="5234e-251">Edit (connection groups and AD Access)</span></span></p></li>
<li><p><span data-ttu-id="5234e-252">Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="5234e-252">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="5234e-253">Delete</span><span class="sxs-lookup"><span data-stu-id="5234e-253">Delete</span></span></p></li>
<li><p><span data-ttu-id="5234e-254">Bearbeiten der Standardkonfiguration</span><span class="sxs-lookup"><span data-stu-id="5234e-254">Edit Default Configuration</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="5234e-255">Diese Paketoptionen waren nur verfügbar, wenn Sie in der Liste Pakete mit der rechten Maustaste auf einen Paketnamen geklickt haben.</span><span class="sxs-lookup"><span data-stu-id="5234e-255">These package options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5234e-256">Symbole im linken Bereich haben neue Farben und Text</span><span class="sxs-lookup"><span data-stu-id="5234e-256">Icons in left pane have new colors and text</span></span>

<span data-ttu-id="5234e-257">Die Farben der Symbole im linken Bereich wurden geändert, und Text wurde hinzugefügt, damit die Symbole mit anderen Microsoft-Produkten konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="5234e-257">The colors of the icons in the left pane have been changed, and text added, to make the icons consistent with other Microsoft products.</span></span>

### <span data-ttu-id="5234e-258">Die Übersichtsseite wurde entfernt</span><span class="sxs-lookup"><span data-stu-id="5234e-258">Overview page has been removed</span></span>

<span data-ttu-id="5234e-259">Im linken Bereich der Verwaltungskonsole wurden die Menüoption Übersicht und die zugehörige Übersichtsseite entfernt.</span><span class="sxs-lookup"><span data-stu-id="5234e-259">In the left pane of the Management Console, the OVERVIEW menu option and its associated OVERVIEW page have been removed.</span></span>

### <a href="" id="bkmk-seqimprove"></a><span data-ttu-id="5234e-260">Verbesserungen des Sequencers</span><span class="sxs-lookup"><span data-stu-id="5234e-260">Sequencer Improvements</span></span>

<span data-ttu-id="5234e-261">Die folgenden Verbesserungen wurden am Paket-Editor im App-V 5,1-Sequenzer vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5234e-261">The following improvements have been made to the package editor in the App-V 5.1 Sequencer.</span></span>

### <span data-ttu-id="5234e-262">Importieren und Exportieren der Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="5234e-262">Import and export the manifest file</span></span>

<span data-ttu-id="5234e-263">Sie können die AppxManifest.xml-Datei importieren und exportieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-263">You can import and export the AppxManifest.xml file.</span></span> <span data-ttu-id="5234e-264">Um die Manifestdatei zu exportieren, wählen Sie die Registerkarte **erweitert** aus, und klicken Sie im Feld Manifestdatei auf **exportieren...**. Sie können Änderungen an der Manifestdatei vornehmen, beispielsweise das Entfernen von Shell-Erweiterungen oder das Bearbeiten von Dateitypzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="5234e-264">To export the manifest file, select the **Advanced** tab and in the Manifest File box, click **Export...**. You can make changes to the manifest file, such as removing shell extensions or editing file type associations.</span></span>

<span data-ttu-id="5234e-265">Nachdem Sie Ihre Änderungen vorgenommen haben, klicken Sie auf **importieren...** und wählen Sie die Datei aus, die Sie bearbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="5234e-265">After you make your changes, click **Import...** and select the file you edited.</span></span> <span data-ttu-id="5234e-266">Nachdem Sie das Dokument erfolgreich wieder in importiert haben, wird die Manifestdatei im Paket-Editor sofort aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5234e-266">After you successfully import it back in, the manifest file is immediately updated within the package editor.</span></span>

**<span data-ttu-id="5234e-267">Achtung</span><span class="sxs-lookup"><span data-stu-id="5234e-267">Caution</span></span>**  
<span data-ttu-id="5234e-268">Wenn Sie die Datei importieren, werden Ihre Änderungen mit dem XML-Schema überprüft.</span><span class="sxs-lookup"><span data-stu-id="5234e-268">When you import the file, your changes are validated against the XML schema.</span></span> <span data-ttu-id="5234e-269">Wenn die Datei nicht gültig ist, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5234e-269">If the file is not valid, you will receive an error.</span></span> <span data-ttu-id="5234e-270">Beachten Sie, dass es möglich ist, eine Datei zu importieren, die mit dem XML-Schema überprüft wird, die aber möglicherweise aus anderen Gründen noch nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5234e-270">Be aware that it is possible to import a file that is validated against the XML schema, but that might still fail to run for other reasons.</span></span>



### <span data-ttu-id="5234e-271">Hinzufügen von Windows 10 zu Betriebssystemliste</span><span class="sxs-lookup"><span data-stu-id="5234e-271">Addition of Windows 10 to operating systems list</span></span>

<span data-ttu-id="5234e-272">Auf der Registerkarte Bereitstellung wurden die Windows-10 32-Bit-und Windows 10-64-Bit der Liste der Betriebssysteme hinzugefügt, für die Sie ein Paket sequenzieren können.</span><span class="sxs-lookup"><span data-stu-id="5234e-272">In the Deployment tab, Windows 10 32-bit and Windows 10-64 bit have been added to the list of operating systems for which you can sequence a package.</span></span> <span data-ttu-id="5234e-273">Wenn Sie **ein beliebiges Betriebs System**auswählen, wird Windows 10 automatisch in die Betriebssysteme aufgenommen, die vom sequenzierten Paket unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5234e-273">If you select **Any Operating System**, Windows 10 is automatically included among the operating systems that the sequenced package will support.</span></span>

### <span data-ttu-id="5234e-274">Aktueller Pfad wird unten im virtuellen Registrierungs-Editor angezeigt</span><span class="sxs-lookup"><span data-stu-id="5234e-274">Current path displays at bottom of virtual registry editor</span></span>

<span data-ttu-id="5234e-275">Auf der Registerkarte virtuelle Registrierung wird der Pfad nun unten im virtuellen Registrierungs-Editor angezeigt, mit dem Sie den aktuell ausgewählten Schlüssel ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="5234e-275">In the Virtual Registry tab, the path now displays at the bottom of the virtual registry editor, which enables you to determine the currently selected key.</span></span> <span data-ttu-id="5234e-276">Zuvor mussten Sie durch die Registrierungsstruktur scrollen, um den aktuell ausgewählten Schlüssel zu finden.</span><span class="sxs-lookup"><span data-stu-id="5234e-276">Previously, you had to scroll through the registry tree to find the currently selected key.</span></span>

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a><span data-ttu-id="5234e-277">Kombiniertes Dialogfeld "suchen und ersetzen" und im virtuellen Registrierungs-Editor hinzugefügte Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="5234e-277">Combined “find and replace” dialog box and shortcut keys added in virtual registry editor</span></span>

<span data-ttu-id="5234e-278">Im virtuellen Registrierungs-Editor wurden Tastenkombinationen für die Option suchen (STRG + F) hinzugefügt, und ein Dialogfeld, in dem die Aufgaben "suchen" und "ersetzen" kombiniert wurden, wurde hinzugefügt, damit Sie Werte und Daten suchen und ersetzen können.</span><span class="sxs-lookup"><span data-stu-id="5234e-278">In the virtual registry editor, shortcut keys have been added for the Find option (Ctrl+F), and a dialog box that combines the “find” and “replace” tasks has been added to enable you to find and replace values and data.</span></span> <span data-ttu-id="5234e-279">Wenn Sie auf dieses kombinierte Dialogfeld zugreifen möchten, wählen Sie einen Schlüssel aus, und führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="5234e-279">To access this combined dialog box, select a key and do one of the following:</span></span>

-   <span data-ttu-id="5234e-280">Drücken Sie **STRG + H** .</span><span class="sxs-lookup"><span data-stu-id="5234e-280">Press **Ctrl+H**</span></span>

-   <span data-ttu-id="5234e-281">Klicken Sie mit der rechten Maustaste auf einen Schlüssel, und wählen Sie **ersetzen**aus.</span><span class="sxs-lookup"><span data-stu-id="5234e-281">Right-click a key and select **Replace**.</span></span>

-   <span data-ttu-id="5234e-282">Wählen **View** Sie &gt; **virtueller Registrierungs** &gt; **Austausch**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="5234e-282">Select **View** &gt; **Virtual Registry** &gt; **Replace**.</span></span>

<span data-ttu-id="5234e-283">Zuvor war das Dialogfeld "ersetzen" nicht vorhanden, und Sie mussten Änderungen manuell vornehmen.</span><span class="sxs-lookup"><span data-stu-id="5234e-283">Previously, the “Replace” dialog box did not exist, and you had to make changes manually.</span></span>

### <span data-ttu-id="5234e-284">Erfolgreiches Umbenennen von Registrierungsschlüsseln und Paketdateien</span><span class="sxs-lookup"><span data-stu-id="5234e-284">Rename registry keys and package files successfully</span></span>

<span data-ttu-id="5234e-285">Sie können virtuelle Registrierungsschlüssel und Dateien umbenennen, ohne dass ein Sequencer-Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="5234e-285">You can rename virtual registry keys and files without experiencing Sequencer issues.</span></span> <span data-ttu-id="5234e-286">Zuvor hat der Sequencer nicht mehr funktioniert, wenn Sie versucht haben, einen Schlüssel umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="5234e-286">Previously, the Sequencer stopped working if you tried to rename a key.</span></span>

### <span data-ttu-id="5234e-287">Importieren und Exportieren von virtuellen Registrierungsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="5234e-287">Import and export virtual registry keys</span></span>

<span data-ttu-id="5234e-288">Sie können virtuelle Registrierungsschlüssel importieren und exportieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-288">You can import and export virtual registry keys.</span></span> <span data-ttu-id="5234e-289">Wenn Sie einen Schlüssel importieren möchten, klicken Sie mit der rechten Maustaste auf den Knoten, unter dem Sie den Schlüssel importieren möchten, navigieren Sie zu dem zu importierenden Schlüssel, und klicken Sie dann auf **importieren**.</span><span class="sxs-lookup"><span data-stu-id="5234e-289">To import a key, right-click the node under which to import the key, navigate to the key you want to import, and then click **Import**.</span></span> <span data-ttu-id="5234e-290">Um einen Schlüssel zu exportieren, klicken Sie mit der rechten Maustaste auf den Schlüssel, und wählen Sie **exportieren**aus.</span><span class="sxs-lookup"><span data-stu-id="5234e-290">To export a key, right-click the key and select **Export**.</span></span>

### <span data-ttu-id="5234e-291">Importieren eines Verzeichnisses in das virtuelle Dateisystem</span><span class="sxs-lookup"><span data-stu-id="5234e-291">Import a directory into the virtual file system</span></span>

<span data-ttu-id="5234e-292">Sie können ein Verzeichnis in VFS importieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-292">You can import a directory into the VFS.</span></span> <span data-ttu-id="5234e-293">Wenn Sie ein Verzeichnis importieren möchten, klicken Sie auf die Registerkarte **Paketdateien** , und klicken Sie dann auf **View** &gt; **Virtuelles Datei System** - &gt; **Importverzeichnis**anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5234e-293">To import a directory, click the **Package Files** tab, and then click **View** &gt; **Virtual File System** &gt; **Import Directory**.</span></span> <span data-ttu-id="5234e-294">Wenn Sie versuchen, ein Verzeichnis zu importieren, das Dateien enthält, die sich bereits im VFS befinden, schlägt der Import fehl, und es wird eine erläuternde Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5234e-294">If you try to import a directory that contains files that are already in the VFS, the import fails, and an explanatory message is displayed.</span></span> <span data-ttu-id="5234e-295">Vor App-V 5,1 konnten keine Verzeichnisse importiert werden.</span><span class="sxs-lookup"><span data-stu-id="5234e-295">Prior to App-V 5.1, you could not import directories.</span></span>

### <span data-ttu-id="5234e-296">Importieren oder Exportieren einer VFS-Datei, ohne Sie löschen und dann wieder zum Paket hinzufügen zu müssen</span><span class="sxs-lookup"><span data-stu-id="5234e-296">Import or export a VFS file without having to delete and then add it back to the package</span></span>

<span data-ttu-id="5234e-297">Sie können Dateien aus dem VFS importieren oder exportieren, ohne die Datei löschen und dann wieder zum Paket hinzufügen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5234e-297">You can import files to or export files from the VFS without having to delete the file and then add it back to the package.</span></span> <span data-ttu-id="5234e-298">So können Sie beispielsweise dieses Feature verwenden, um ein Änderungsprotokoll in ein lokales Laufwerk zu exportieren, die Datei mit einem externen Editor zu bearbeiten und dann die Datei in VFS erneut zu importieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-298">For example, you might use this feature to export a change log to a local drive, edit the file using an external editor, and then re-import the file into the VFS.</span></span>

<span data-ttu-id="5234e-299">Wenn Sie eine Datei exportieren möchten, wählen Sie die Registerkarte **Paketdateien** aus, klicken Sie mit der rechten Maustaste auf die Datei im VFS, klicken Sie auf **exportieren**, und wählen Sie einen Exportspeicherort aus, aus dem Sie Ihre Änderungen vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="5234e-299">To export a file, select the **Package Files** tab, right-click the file in the VFS, click **Export**, and choose an export location from which you can make your edits.</span></span>

<span data-ttu-id="5234e-300">Wenn Sie eine Datei importieren möchten, wählen Sie die Registerkarte **Paketdateien** aus, und klicken Sie mit der rechten Maustaste auf die Datei, die Sie exportiert haben.</span><span class="sxs-lookup"><span data-stu-id="5234e-300">To import a file, select the **Package Files** tab and right-click the file that you had exported.</span></span> <span data-ttu-id="5234e-301">Navigieren Sie zu der Datei, die Sie bearbeitet haben, und klicken Sie dann auf **importieren**.</span><span class="sxs-lookup"><span data-stu-id="5234e-301">Browse to the file that you edited, and then click **Import**.</span></span> <span data-ttu-id="5234e-302">Mit der importierten Datei wird die vorhandene Datei überschrieben.</span><span class="sxs-lookup"><span data-stu-id="5234e-302">The imported file will overwrite the existing file.</span></span>

<span data-ttu-id="5234e-303">Nachdem Sie eine Datei importiert haben, müssen Sie das Paket speichern, indem Sie auf **Datei** &gt; **Speichern**klicken.</span><span class="sxs-lookup"><span data-stu-id="5234e-303">After you import a file, you must save the package by clicking **File** &gt; **Save**.</span></span>

### <span data-ttu-id="5234e-304">Menü zum Hinzufügen einer Paketdatei wurde verschoben</span><span class="sxs-lookup"><span data-stu-id="5234e-304">Menu for adding a package file has moved</span></span>

<span data-ttu-id="5234e-305">Die Menüoption zum Hinzufügen einer Paketdatei wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="5234e-305">The menu option for adding a package file has been moved.</span></span> <span data-ttu-id="5234e-306">Um die Option hinzufügen zu finden, **Wählen Sie die** Registerkarte **Paketdateien** aus, und klicken Sie dann auf &gt; **virtuelle Datei System** &gt; **Datei hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="5234e-306">To find the Add option, select the **Package Files** tab, then click **View** &gt; **Virtual File System** &gt; **Add File**.</span></span> <span data-ttu-id="5234e-307">Zuvor haben Sie mit der rechten Maustaste auf einen Ordner unter dem VFS-Knoten geklickt und dann **Datei hinzufügen**ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5234e-307">Previously, you right-clicked a folder under the VFS node, and chose **Add File**.</span></span>

### <span data-ttu-id="5234e-308">Virtueller Registrierungsknoten erweitert die Computer-und Benutzer Strukturen standardmäßig</span><span class="sxs-lookup"><span data-stu-id="5234e-308">Virtual registry node expands MACHINE and USER hives by default</span></span>

<span data-ttu-id="5234e-309">Wenn Sie die virtuelle Registrierung öffnen, werden die Computer-und Benutzer Strukturen unterhalb des Registrierungs Knotens der obersten Ebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5234e-309">When you open the virtual registry, the MACHINE and USER hives are shown below the top-level REGISTRY node.</span></span> <span data-ttu-id="5234e-310">Zuvor mussten Sie den Registrierungsknoten erweitern, um die darunter befindlichen Strukturen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5234e-310">Previously, you had to expand the REGISTRY node to show the hives beneath.</span></span>

### <span data-ttu-id="5234e-311">Aktivieren oder Deaktivieren von Browser Helper-Objekten</span><span class="sxs-lookup"><span data-stu-id="5234e-311">Enable or disable Browser Helper Objects</span></span>

<span data-ttu-id="5234e-312">Sie können Browser Hilfsobjekte aktivieren oder deaktivieren, indem Sie auf der Registerkarte Erweitert der Sequencer-Benutzeroberfläche ein neues Kontrollkästchen aktivieren, Browser Hilfsobjekte aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-312">You can enable or disable Browser Helper Objects by selecting a new check box, Enable Browser Helper Objects, on the Advanced tab of the Sequencer user interface.</span></span> <span data-ttu-id="5234e-313">Wenn Browser-helferobjekte:</span><span class="sxs-lookup"><span data-stu-id="5234e-313">If Browser Helper Objects:</span></span>

-   <span data-ttu-id="5234e-314">Im Paket vorhanden und aktiviert sind, ist das Kontrollkästchen standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5234e-314">Exist in the package and are enabled, the check box is selected by default.</span></span>

-   <span data-ttu-id="5234e-315">Im Paket vorhanden und deaktiviert sind, ist das Kontrollkästchen standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5234e-315">Exist in the package and are disabled, the check box is clear by default.</span></span>

-   <span data-ttu-id="5234e-316">Im Paket vorhanden ist, mit einem oder mehreren aktivierten und einem oder mehreren deaktivierten, ist das Kontrollkästchen standardmäßig auf unbestimmt eingestellt.</span><span class="sxs-lookup"><span data-stu-id="5234e-316">Exist in the package, with one or more enabled and one or more disabled, the check box is set to indeterminate by default.</span></span>

-   <span data-ttu-id="5234e-317">Im Paket nicht vorhanden ist, ist das Kontrollkästchen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5234e-317">Do not exist in the package, the check box is disabled.</span></span>

### <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="5234e-318">Verbesserungen beim Paket Konverter</span><span class="sxs-lookup"><span data-stu-id="5234e-318">Improvements to Package Converter</span></span>

<span data-ttu-id="5234e-319">Sie können jetzt den Paket Konverter verwenden, um App-V 4,6-Pakete zu konvertieren, die Skripts enthalten, und Registrierungsinformationen und Skripts aus den Dateien des Quell-OSD sind jetzt in der Ausgabe des Paket Konverters enthalten.</span><span class="sxs-lookup"><span data-stu-id="5234e-319">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="5234e-320">Weitere Informationen, einschließlich Beispielen, finden Sie unter [Migrieren zu App-V 5,1 aus einer früheren Version](migrating-to-app-v-51-from-a-previous-version.md).</span><span class="sxs-lookup"><span data-stu-id="5234e-320">For more information including examples, see [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md).</span></span>

### <a href="" id="bkmk-supmultscripts"></a><span data-ttu-id="5234e-321">Unterstützung für mehrere Skripts in einem einzelnen Ereignisauslöser</span><span class="sxs-lookup"><span data-stu-id="5234e-321">Support for multiple scripts on a single event trigger</span></span>

<span data-ttu-id="5234e-322">App-v 5,1 unterstützt die Verwendung mehrerer Skripts für einen einzelnen Ereignisauslöser für App-v-Pakete, einschließlich der Pakete, die Sie von App-v 4,6 in App-v 5,0 oder höher konvertieren.</span><span class="sxs-lookup"><span data-stu-id="5234e-322">App-V 5.1 supports the use of multiple scripts on a single event trigger for App-V packages, including packages that you are converting from App-V 4.6 to App-V 5.0 or later.</span></span> <span data-ttu-id="5234e-323">Um die Verwendung mehrerer Skripts zu ermöglichen, verwendet App-v 5,1 eine Skript Startanwendung mit dem Namen ScriptRunner.exe, die als Teil der APP-v-Clientinstallation installiert wird.</span><span class="sxs-lookup"><span data-stu-id="5234e-323">To enable the use of multiple scripts, App-V 5.1 uses a script launcher application, named ScriptRunner.exe, which is installed as part of the App-V client installation.</span></span>

<span data-ttu-id="5234e-324">Weitere Informationen, einschließlich einer Liste der Ereignisauslöser und des Kontexts, unter dem Skripts ausgeführt werden können, finden Sie im Abschnitt Skripts in der [dynamischen Konfiguration von App-V 5,1](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="5234e-324">For more information, including a list of event triggers and the context under which scripts can be run, see the Scripts section in [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

### <a href="" id="bkmk-hardcodepath"></a><span data-ttu-id="5234e-325">Hartcodierter Pfad zum Installationsordner wird an das virtuelle Dateisystem-Stammverzeichnis umgeleitet</span><span class="sxs-lookup"><span data-stu-id="5234e-325">Hardcoded path to installation folder is redirected to virtual file system root</span></span>

<span data-ttu-id="5234e-326">Wenn Sie Pakete von App-v 4,6 in 5,1 konvertieren, kann das App-v 5,1-Paket auf das hart codierte Laufwerk zugreifen, das Sie beim Erstellen von 4,6-Paketen verwenden mussten.</span><span class="sxs-lookup"><span data-stu-id="5234e-326">When you convert packages from App-V 4.6 to 5.1, the App-V 5.1 package can access the hardcoded drive that you were required to use when you created 4.6 packages.</span></span> <span data-ttu-id="5234e-327">Der Laufwerkbuchstabe ist das Laufwerk, das Sie als Installationslaufwerk auf dem 4,6-Sequenzcomputer ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="5234e-327">The drive letter will be the drive you selected as the installation drive on the 4.6 sequencing machine.</span></span> <span data-ttu-id="5234e-328">(Der standardmäßige Laufwerkbuchstabe ist Q:\\.)</span><span class="sxs-lookup"><span data-stu-id="5234e-328">(The default drive letter is Q:\\.)</span></span>

<span data-ttu-id="5234e-329">Zuvor wurde der 4,6-Stammordner nicht erkannt, und der Zugriff auf App-V 5,0-Pakete war nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="5234e-329">Previously, the 4.6 root folder was not recognized and could not be accessed by App-V 5.0 packages.</span></span> <span data-ttu-id="5234e-330">App-v 5,1-Pakete können über den vollständigen Pfad auf hart codierte Dateien zugreifen oder Dateien unter dem App-V 4,6-Installations Stamm programmgesteuert auflisten.</span><span class="sxs-lookup"><span data-stu-id="5234e-330">App-V 5.1 packages can access hardcoded files by their full path or can programmatically enumerate files under the App-V 4.6 installation root.</span></span>

<span data-ttu-id="5234e-331">**Technische Informationen:** Der APP-v 5,1-Paket Konverter speichert den App-v 4,6-Installations Stammordner und die kurzen Ordnernamen in der FilesystemMetadata.xml-Datei im File System-Element.</span><span class="sxs-lookup"><span data-stu-id="5234e-331">**Technical Details:** The App-V 5.1 package converter will save the App-V 4.6 installation root folder and short folder names in the FilesystemMetadata.xml file in the Filesystem element.</span></span> <span data-ttu-id="5234e-332">Wenn der APP-v 5,1-Client den virtuellen Prozess erstellt, werden Anforderungen aus dem App-v 4,6-Installations Stamm dem virtuellen Dateisystem Stamm zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5234e-332">When the App-V 5.1 client creates the virtual process, it will map requests from the App-V 4.6 installation root to the virtual file system root.</span></span>

## <span data-ttu-id="5234e-333">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="5234e-333">How to Get MDOP Technologies</span></span>


<span data-ttu-id="5234e-334">App-V ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="5234e-334">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="5234e-335">MDOP ist Teil von Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="5234e-335">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="5234e-336">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="5234e-336">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="5234e-337">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5234e-337">Related topics</span></span>


[<span data-ttu-id="5234e-338">Versionshinweise für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5234e-338">Release Notes for App-V 5.1</span></span>](release-notes-for-app-v-51.md)









