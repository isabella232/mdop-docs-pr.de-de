---
title: Erste Schritte mit App-V 5.0
description: Erste Schritte mit App-V 5.0
author: dansimp
ms.assetid: 3e16eafb-ce95-4d06-b214-fe0f4b1b495f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7979c81b7b57107f824b96d9fef8049a00c5b08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805813"
---
# <span data-ttu-id="101e4-103">Erste Schritte mit App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="101e4-103">Getting Started with App-V 5.0</span></span>


<span data-ttu-id="101e4-104">App-V 5,0 ermöglicht Administratoren das bereitstellen, aktualisieren und unterstützen von Anwendungen als Dienste in Echtzeit – bedarfsbasiert.</span><span class="sxs-lookup"><span data-stu-id="101e4-104">App-V 5.0 enables administrators to deploy, update, and support applications as services in real time, on an as-needed basis.</span></span> <span data-ttu-id="101e4-105">Einzelne Anwendungen werden von lokal installierten Produkten in Zentral verwaltete Dienste transformiert und sind überall verfügbar, ohne Computer vorkonfigurieren oder Betriebssystemeinstellungen ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="101e4-105">Individual applications are transformed from locally installed products into centrally managed services and are available wherever you need, without the need to preconfigure computers or to change operating system settings.</span></span>

<span data-ttu-id="101e4-106">App-V umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="101e4-106">App-V consists of the following elements:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="101e4-107">Element</span><span class="sxs-lookup"><span data-stu-id="101e4-107">Element</span></span></th>
<th align="left"><span data-ttu-id="101e4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="101e4-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="101e4-109">App-V-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="101e4-109">App-V Management Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="101e4-110">Bietet einen zentralen Speicherort für die Verwaltung der APP-v-Infrastruktur, die virtuelle Anwendungen sowohl für den App-v-Desktop Client als auch für den Remote Desktop Dienste-Client (ehemals Terminal Dienste) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="101e4-110">Provides a central location for managing the App-V infrastructure, which delivers virtual applications to both the App-V Desktop Client and the Remote Desktop Services (formerly Terminal Services) Client.</span></span></p></li>
<li><p><span data-ttu-id="101e4-111">Verwendet Microsoft SQL Server® für seinen Datenspeicher, in dem mindestens ein App-V-Verwaltungsserver einen einzelnen SQL Server-Datenspeicher freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="101e4-111">Uses Microsoft SQL Server® for its data store, where one or more App-V Management servers can share a single SQL Server data store.</span></span></p></li>
<li><p><span data-ttu-id="101e4-112">Authentifiziert Anforderungen und bietet Sicherheit, Dosierung, Überwachung und Datenerfassung.</span><span class="sxs-lookup"><span data-stu-id="101e4-112">Authenticates requests and provides security, metering, monitoring, and data gathering.</span></span> <span data-ttu-id="101e4-113">Der Server verwendet Active Directory und unterstützende Tools zum Verwalten von Benutzern und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="101e4-113">The server uses Active Directory and supporting tools to manage users and applications.</span></span></p></li>
<li><p><span data-ttu-id="101e4-114">Verfügt über eine auf Silverlight® basierende Verwaltungswebsite, über die Sie die App-V-Infrastruktur von einem beliebigen Computer aus konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="101e4-114">Has a Silverlight®-based management site, which enables you to configure the App-V infrastructure from any computer.</span></span> <span data-ttu-id="101e4-115">Sie können Anwendungen hinzufügen und entfernen, Tastenkombinationen bearbeiten, Benutzern und Gruppen Zugriffsberechtigungen zuweisen und Verbindungsgruppen erstellen.</span><span class="sxs-lookup"><span data-stu-id="101e4-115">You can add and remove applications, manipulate shortcuts, assign access permissions to users and groups, and create connection groups.</span></span></p></li>
<li><p><span data-ttu-id="101e4-116">Ermöglicht die Kommunikation zwischen der App-V Web Management Console und dem SQL Server-Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="101e4-116">Enables communication between the App-V Web Management Console and the SQL Server data store.</span></span> <span data-ttu-id="101e4-117">Diese Komponenten können je nach erforderlicher Systemarchitektur auf einem einzelnen Server Computer oder auf einem oder mehreren separaten Computern installiert werden.</span><span class="sxs-lookup"><span data-stu-id="101e4-117">These components can all be installed on a single server computer, or on one or more separate computers, depending on the required system architecture.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="101e4-118">App-V-Veröffentlichungs Server</span><span class="sxs-lookup"><span data-stu-id="101e4-118">App-V Publishing Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="101e4-119">Bietet App-V-Clients mit berechtigten Anwendungen für den jeweiligen Benutzer</span><span class="sxs-lookup"><span data-stu-id="101e4-119">Provides App-V Clients with entitled applications for the specific user</span></span></p></li>
<li><p><span data-ttu-id="101e4-120">Hostet das virtuelle Anwendungspaket für Streaming.</span><span class="sxs-lookup"><span data-stu-id="101e4-120">Hosts the virtual application package for streaming.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="101e4-121">App-V-Desktop Client</span><span class="sxs-lookup"><span data-stu-id="101e4-121">App-V Desktop Client</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="101e4-122">Ruft virtuelle Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="101e4-122">Retrieves virtual applications</span></span></p></li>
<li><p><span data-ttu-id="101e4-123">Veröffentlicht die Anwendungen auf den Clients</span><span class="sxs-lookup"><span data-stu-id="101e4-123">Publishes the applications on the clients</span></span></p></li>
<li><p><span data-ttu-id="101e4-124">Richtet virtuelle Umgebungen zur Laufzeit automatisch auf Windows-Endpunkten ein und verwaltet Sie.</span><span class="sxs-lookup"><span data-stu-id="101e4-124">Automatically sets up and manages virtual environments at runtime on Windows endpoints.</span></span></p></li>
<li><p><span data-ttu-id="101e4-125">Speichert benutzerspezifische Einstellungen für virtuelle Anwendungen wie Registrierungs-und Dateiänderungen in den Profilen jedes Benutzers&#39;s.</span><span class="sxs-lookup"><span data-stu-id="101e4-125">Stores user-specific virtual application settings, such as registry and file changes, in each user&#39;s profile.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="101e4-126">App-V Remote Desktop Dienste (RDS)-Client</span><span class="sxs-lookup"><span data-stu-id="101e4-126">App-V Remote Desktop Services (RDS) Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="101e4-127">Ermöglicht es Remote Desktop-Sitzungs Host Servern, die Funktionen des App-V-Desktop Clients für freigegebene Desktopsitzungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="101e4-127">Enables Remote Desktop Session Host servers to use the capabilities of the App-V Desktop Client for shared desktop sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="101e4-128">App-V-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="101e4-128">App-V Sequencer</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="101e4-129">Ist ein auf Assistenten basierendes Tool, mit dem Sie herkömmliche Anwendungen in virtuelle Anwendungen umwandeln können.</span><span class="sxs-lookup"><span data-stu-id="101e4-129">Is a wizard-based tool that you use to transform traditional applications into virtual applications.</span></span></p></li>
<li><p><span data-ttu-id="101e4-130">Erstellt die Anwendung "Package", die sich aus:</span><span class="sxs-lookup"><span data-stu-id="101e4-130">Produces the application “package,” which consists of:</span></span></p>
<ol>
<li><p><span data-ttu-id="101e4-131">eine sequenzierte Anwendungsdatei (APPV)</span><span class="sxs-lookup"><span data-stu-id="101e4-131">a sequenced application (APPV) file</span></span></p></li>
<li><p><span data-ttu-id="101e4-132">eine Windows Installer-Datei (MSI), die für Clients bereitgestellt werden kann, die für eigenständigen Betrieb konfiguriert sind</span><span class="sxs-lookup"><span data-stu-id="101e4-132">a Windows Installer file (MSI) that can be deployed to clients configured for stand-alone operation</span></span></p></li>
<li><p><span data-ttu-id="101e4-133">Mehrere XML-Dateien, einschließlich Report.XML, PackageName_DeploymentConfig.XML und PackageName_UserConfig.XML.</span><span class="sxs-lookup"><span data-stu-id="101e4-133">Several XML files including Report.XML, PackageName_DeploymentConfig.XML, and PackageName_UserConfig.XML.</span></span> <span data-ttu-id="101e4-134">Die XML-Dateien userconfig und DeploymentConfig werden verwendet, um benutzerdefinierte Änderungen am Standardverhalten des Pakets zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="101e4-134">The UserConfig and DeploymentConfig XML files are used to configure custom changes to the default behavior of the package.</span></span></p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="101e4-135">Weitere Informationen zu diesen Elementen finden Sie unter [hochstufige Architektur für App-V 5,0](high-level-architecture-for-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="101e4-135">For more information about these elements, see [High Level Architecture for App-V 5.0](high-level-architecture-for-app-v-50.md).</span></span>

<span data-ttu-id="101e4-136">Wenn Sie mit diesem Produkt noch nicht vertraut sind, empfehlen wir Ihnen, die Dokumentation gründlich zu lesen.</span><span class="sxs-lookup"><span data-stu-id="101e4-136">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="101e4-137">Bevor Sie die Anwendung in einer Produktionsumgebung bereitstellen, empfehlen wir auch, den Bereitstellungsplan in einer Testnetzwerkumgebung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="101e4-137">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="101e4-138">Sie können auch erwägen, eine Klasse über relevante Technologien zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="101e4-138">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="101e4-139">Weitere Informationen zu Microsoft-Schulungsmöglichkeiten finden Sie in der Microsoft-Schulungsübersicht unter <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="101e4-139">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="101e4-140">**Hinweis**  Eine herunterladbare Version des Administratorhandbuchs steht nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="101e4-140">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="101e4-141">Sie können sich jedoch mit einem speziellen Modus der TechNet-Bibliothek vertraut machen, der es Ihnen ermöglicht, Artikel auszuwählen, Sie in einer Sammlung zu gruppieren, zu drucken oder in eine Datei unter (zu exportieren <https://go.microsoft.com/fwlink/?LinkId=272491> https://go.microsoft.com/fwlink/?LinkId=272491) .</span><span class="sxs-lookup"><span data-stu-id="101e4-141">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272491> (https://go.microsoft.com/fwlink/?LinkId=272491).</span></span>

 

<span data-ttu-id="101e4-142">Dieser Abschnitt des App-v 5,0-Administrator Handbuchs enthält allgemeine Informationen zu app-v 5,0, um Ihnen ein grundlegendes Verständnis des Produkts zu vermitteln, bevor Sie mit der Bereitstellungsplanung beginnen.</span><span class="sxs-lookup"><span data-stu-id="101e4-142">This section of the App-V 5.0 Administrator’s Guide includes high-level information about App-V 5.0 to provide you with a basic understanding of the product before you begin the deployment planning.</span></span>

## <span data-ttu-id="101e4-143">Erste Schritte mit App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="101e4-143">Getting started with App-V 5.0</span></span>


-   [<span data-ttu-id="101e4-144">Informationen zu App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="101e4-144">About App-V 5.0</span></span>](about-app-v-50.md)

    <span data-ttu-id="101e4-145">Bietet eine allgemeine Übersicht über App-V 5,0 und die Art und Weise, wie Sie in Ihrer Organisation verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="101e4-145">Provides a high-level overview of App-V 5.0 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="101e4-146">Informationen zu App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="101e4-146">About App-V 5.0 SP1</span></span>](about-app-v-50-sp1.md)

    <span data-ttu-id="101e4-147">Bietet eine allgemeine Übersicht über App-V 5.0 SP1 und die Art und Weise, wie Sie in Ihrer Organisation verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="101e4-147">Provides a high-level overview of App-V 5.0SP1 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="101e4-148">Informationen zu App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="101e4-148">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

    <span data-ttu-id="101e4-149">Bietet eine allgemeine Übersicht über App-V 5.0 SP2 und die Art und Weise, wie Sie in Ihrer Organisation verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="101e4-149">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="101e4-150">Informationen zu App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="101e4-150">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

    <span data-ttu-id="101e4-151">Bietet eine allgemeine Übersicht über App-V 5.0 SP2 und die Art und Weise, wie Sie in Ihrer Organisation verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="101e4-151">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="101e4-152">Evaluieren von App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="101e4-152">Evaluating App-V 5.0</span></span>](evaluating-app-v-50.md)

    <span data-ttu-id="101e4-153">Bietet Informationen dazu, wie Sie App-V 5,0 für die Verwendung in Ihrer Organisation am besten auswerten können.</span><span class="sxs-lookup"><span data-stu-id="101e4-153">Provides information about how you can best evaluate App-V 5.0 for use in your organization.</span></span>

-   [<span data-ttu-id="101e4-154">High-Level-Architektur für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="101e4-154">High Level Architecture for App-V 5.0</span></span>](high-level-architecture-for-app-v-50.md)

    <span data-ttu-id="101e4-155">Enthält eine Beschreibung der App-V 5,0-Features und ihrer Zusammenarbeit.</span><span class="sxs-lookup"><span data-stu-id="101e4-155">Provides a description of the App-V 5.0 features and how they work together.</span></span>

-   [<span data-ttu-id="101e4-156">Barrierefreiheit von App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="101e4-156">Accessibility for App-V 5.0</span></span>](accessibility-for-app-v-50.md)

    <span data-ttu-id="101e4-157">Bietet Informationen zu Features und Diensten, mit denen dieses Produkt und die zugehörige Dokumentation für Personen mit Behinderungen barrierefreier sind.</span><span class="sxs-lookup"><span data-stu-id="101e4-157">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="101e4-158">Weitere Ressourcen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="101e4-158">Other resources for this product</span></span>


-   [<span data-ttu-id="101e4-159">Microsoft Application Virtualization 5,0-Administrator Handbuch</span><span class="sxs-lookup"><span data-stu-id="101e4-159">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="101e4-160">Planen für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="101e4-160">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)

-   [<span data-ttu-id="101e4-161">Bereitstellen von App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="101e4-161">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

-   [<span data-ttu-id="101e4-162">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="101e4-162">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

-   [<span data-ttu-id="101e4-163">Problembehandlung bei App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="101e4-163">Troubleshooting App-V 5.0</span></span>](troubleshooting-app-v-50.md)






 

 





