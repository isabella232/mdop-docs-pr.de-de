---
title: Informationen zu App-V 5.0 SP2
description: Informationen zu App-V 5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806127"
---
# <span data-ttu-id="69c8d-103">Informationen zu App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="69c8d-103">About App-V 5.0 SP2</span></span>


<span data-ttu-id="69c8d-104">App-V 5.0 SP2 bietet eine verbesserte integrierte Plattform, eine flexiblere Virtualisierung und ein leistungsstarkes Management für virtualisierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="69c8d-104">App-V 5.0SP2 provides an improved integrated platform, more flexible virtualization, and powerful management for virtualized applications.</span></span> <span data-ttu-id="69c8d-105">Weitere Informationen finden Sie unter [App-V 5,0 Overview](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .</span><span class="sxs-lookup"><span data-stu-id="69c8d-105">For more information see, [App-V 5.0 Overview](https://go.microsoft.com/fwlink/p/?LinkId=325265) (https://go.microsoft.com/fwlink/?LinkId=325265).</span></span>

## <span data-ttu-id="69c8d-106">Änderungen in der Standard mäßigen App-V 5.0 SP2-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="69c8d-106">Changes in Standard App-V 5.0SP2 Functionality</span></span>


<span data-ttu-id="69c8d-107">Die folgenden Abschnitte enthalten Informationen zu den Änderungen der Standardfunktionen für App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="69c8d-107">The following sections contain information about the changes in standard functionality for App-V 5.0SP2.</span></span>

### <a href="" id="bkmk-sp2-supported-cfg"></a><span data-ttu-id="69c8d-108">Unterstützung für Windows Server 2012 R2 und Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="69c8d-108">Support for Windows Server 2012 R2 and Windows 8.1</span></span>

<span data-ttu-id="69c8d-109">App-V 5,0 mit Unterstützung für Windows Server 2012 R2 und Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="69c8d-109">App-V 5.0 includes support for Windows Server 2012 R2 and Windows 8.1</span></span>

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> <span data-ttu-id="69c8d-110">App-V 5.0 SP2 unterstützt jetzt die Ordnerumleitung für das Roaming-AppData-Verzeichnis des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="69c8d-110">App-V 5.0SP2 now supports folder redirection for the user’s roaming AppData directory</span></span>

<span data-ttu-id="69c8d-111">App-V 5.0 SP2 unterstützt Roaming-APPDATA (% APPDATA%) Ordnerumleitung.</span><span class="sxs-lookup"><span data-stu-id="69c8d-111">App-V 5.0SP2 supports roaming AppData (%AppData%) folder redirection.</span></span> <span data-ttu-id="69c8d-112">Weitere Informationen finden Sie unter [Planen der Verwendung der Ordnerumleitung mit App-V](planning-to-use-folder-redirection-with-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="69c8d-112">For more information, see the [Planning to Use Folder Redirection with App-V](planning-to-use-folder-redirection-with-app-v.md).</span></span>

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a><span data-ttu-id="69c8d-113">Verbesserungen des Paket Upgrades und ausstehende Aufgaben</span><span class="sxs-lookup"><span data-stu-id="69c8d-113">Package upgrade improvements and pending tasks</span></span>

<span data-ttu-id="69c8d-114">In App-V 5.0 SP2 werden Sie nicht mehr aufgefordert, eine ausgeführte virtuelle Anwendung zu schließen, wenn eine neuere Version des Pakets oder der Verbindungsgruppe veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="69c8d-114">In App-V 5.0SP2, you are no longer prompted to close a running virtual application when a newer version of the package or connection group is published.</span></span> <span data-ttu-id="69c8d-115">Wenn ein Paket oder eine Verbindungsgruppe verwendet wird, wenn Sie versuchen, eine verwandte Aufgabe auszuführen, wird eine Meldung angezeigt, die angibt, dass das Objekt verwendet wird und der Vorgang zu einem späteren Zeitpunkt versucht wird.</span><span class="sxs-lookup"><span data-stu-id="69c8d-115">If a package or connection group is in use when you try to perform a related task, a message displays to indicate that the object is in use, and that the operation will be attempted at a later time.</span></span>

<span data-ttu-id="69c8d-116">Aufgaben, die in einem ausstehenden Status gespeichert wurden, werden gemäß den folgenden Regeln ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="69c8d-116">Tasks that have been placed in a pending state will be performed according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69c8d-117">Art der Hintergrundaufgabe</span><span class="sxs-lookup"><span data-stu-id="69c8d-117">Task type</span></span></th>
<th align="left"><span data-ttu-id="69c8d-118">Anwendbare Regel</span><span class="sxs-lookup"><span data-stu-id="69c8d-118">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69c8d-119">Benutzerbasierte Aufgaben, beispielsweise die Veröffentlichung eines Pakets für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="69c8d-119">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="69c8d-120">Die ausstehende Aufgabe wird ausgeführt, nachdem sich der Benutzer abgemeldet hat und sich dann wieder anmeldet.</span><span class="sxs-lookup"><span data-stu-id="69c8d-120">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69c8d-121">Global basierender Vorgang, beispielsweise Aktivieren einer Verbindungsgruppe Global</span><span class="sxs-lookup"><span data-stu-id="69c8d-121">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="69c8d-122">Die ausstehende Aufgabe wird ausgeführt, wenn der Computer heruntergefahren und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="69c8d-122">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="69c8d-123">Wenn eine Aufgabe in einem ausstehenden Zustand befindet, generiert der App-V-Client auch einen Registrierungsschlüssel für die ausstehende Aufgabe wie folgt:</span><span class="sxs-lookup"><span data-stu-id="69c8d-123">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69c8d-124">Benutzerbasierter oder Global basierter Vorgang</span><span class="sxs-lookup"><span data-stu-id="69c8d-124">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="69c8d-125">Ort, an dem der Registrierungsschlüssel generiert wird</span><span class="sxs-lookup"><span data-stu-id="69c8d-125">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69c8d-126">Benutzerbasierte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="69c8d-126">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="69c8d-127">KEY_CURRENT_USER \software\microsoft\appv\client\pendingtasks</span><span class="sxs-lookup"><span data-stu-id="69c8d-127">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69c8d-128">Global basierte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="69c8d-128">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="69c8d-129">HKEY_LOCAL_MACHINE \software\microsoft\appv\client\pendingtasks</span><span class="sxs-lookup"><span data-stu-id="69c8d-129">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="69c8d-130">Virtualisierung von Microsoft Office 2013 und Microsoft Office 2010 mithilfe von App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="69c8d-130">Virtualizing Microsoft Office 2013 and Microsoft Office 2010 using App-V 5.0</span></span>

<span data-ttu-id="69c8d-131">Verwenden Sie den folgenden Link, um weitere Informationen zu App-V 5,0 unterstützte Microsoft Office-Szenarien zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="69c8d-131">Use the following link for more information about App-V 5.0 supported Microsoft Office scenarios.</span></span>

[<span data-ttu-id="69c8d-132">Virtualisierung von Microsoft Office2013 für Application Virtualization (App-V) 5.0</span><span class="sxs-lookup"><span data-stu-id="69c8d-132">Virtualizing Microsoft Office 2013 for Application Virtualization (App-V) 5.0</span></span>](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

<span data-ttu-id="69c8d-133">**Hinweis**  Dieses Dokument befasst sich mit dem Erstellen eines Microsoft Office 2013-App-V 5,0-Pakets.</span><span class="sxs-lookup"><span data-stu-id="69c8d-133">**Note** This document focuses on creating a Microsoft Office 2013 App-V 5.0 Package.</span></span> <span data-ttu-id="69c8d-134">Sie enthält jedoch auch Informationen zu Szenarien für Microsoft Office 2010 mit App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="69c8d-134">However, it also provides information about scenarios for Microsoft Office 2010 with App-V 5.0.</span></span>

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> <span data-ttu-id="69c8d-135">App-V 5,0-Benutzeroberflächenanwendung für die Client Verwaltung</span><span class="sxs-lookup"><span data-stu-id="69c8d-135">App-V 5.0 Client Management User Interface Application</span></span>

<span data-ttu-id="69c8d-136">In früheren Versionen von App-v 5,0 wurde die Client Verwaltungsbenutzeroberfläche (UI) mit der APP-v 5,0-Clientinstallation bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="69c8d-136">In previous versions of App-V 5.0 the Client Management User Interface (UI) was provided with the App-V 5.0 Client installation.</span></span> <span data-ttu-id="69c8d-137">Mit App-V 5.0 SP2 ist dies nicht mehr der Fall.</span><span class="sxs-lookup"><span data-stu-id="69c8d-137">With App-V 5.0SP2 this is no longer the case.</span></span> <span data-ttu-id="69c8d-138">Administratoren haben jetzt die Möglichkeit, die APP-v 5,0-Client-Benutzeroberfläche als virtuelle Anwendung (unter Verwendung aller unterstützten App-v-Bereitstellungskonfigurationen) oder als installierte Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="69c8d-138">Administrators now have the option to deploy the App-V 5.0 Client UI as a Virtual Application (using all supported App-V deployment configurations) or as an installed application.</span></span>

<span data-ttu-id="69c8d-139">Weitere Informationen finden Sie unter [Microsoft Application Virtualization 5,0 Client-Benutzeroberflächenanwendung](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .</span><span class="sxs-lookup"><span data-stu-id="69c8d-139">For more information see [Microsoft Application Virtualization 5.0 Client UI Application](https://go.microsoft.com/fwlink/p/?LinkId=386345) (https://go.microsoft.com/fwlink/?LinkId=386345).</span></span>

### <span data-ttu-id="69c8d-140">Automatisches Verpacken und Bereitstellen von nebeneinander angeordneten (SxS) Assemblys</span><span class="sxs-lookup"><span data-stu-id="69c8d-140">Side-by-Side (SxS) Assembly Automatic Packaging and Deployment</span></span>

<span data-ttu-id="69c8d-141">App-v 5.0 SP2 erkennt jetzt automatisch parallele (SxS) Assemblys und die Bereitstellung auf dem Computer, auf dem der APP-v 5.0 SP2-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69c8d-141">App-V 5.0SP2 now automatically detects side-by-side (SxS) assemblies, and deployment on the computer running the App-V 5.0SP2 client.</span></span> <span data-ttu-id="69c8d-142">Eine SxS-Assembly besteht in erster Linie aus VC + +-Laufzeitabhängigkeiten oder MSXML.</span><span class="sxs-lookup"><span data-stu-id="69c8d-142">A SxS assembly primarily consists of VC++ run-time dependencies or MSXML.</span></span> <span data-ttu-id="69c8d-143">In früheren Versionen von App-v erforderten virtuelle Anwendungen mit Abhängigkeiten von VC-Laufzeiten, dass diese Abhängigkeiten lokal auf dem Computer ausgeführt werden, auf dem der App-V 5.0 SP2-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69c8d-143">In previous versions of App-V, virtual applications that had dependencies on VC run-times required these dependencies to be locally on the computer running the App-V 5.0SP2 client.</span></span>

<span data-ttu-id="69c8d-144">Die folgenden Funktionen werden jetzt unterstützt:</span><span class="sxs-lookup"><span data-stu-id="69c8d-144">The following functionality is now supported:</span></span>

-   <span data-ttu-id="69c8d-145">Der App-V 5,0-Sequenzer zeichnet die SxS-Assembly automatisch im Paket auf, unabhängig davon, ob die VC-Laufzeit bereits auf dem Computer installiert ist, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69c8d-145">The App-V 5.0 sequencer automatically captures the SxS assembly in the package regardless of whether the VC run-time has already been installed on the computer running the sequencer.</span></span>

-   <span data-ttu-id="69c8d-146">Der App-V 5,0-Client installiert die erforderliche SxS-Assembly automatisch auf dem Computer, auf dem der Client ausgeführt wird, wie dies zum Zeitpunkt der Veröffentlichung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="69c8d-146">The App-V 5.0 client automatically installs the required SxS assembly to the computer running the client as required at publishing time.</span></span>

-   <span data-ttu-id="69c8d-147">Der App-V 5,0-Sequenzer meldet die VC-Laufzeitabhängigkeit mithilfe des Sequencer-Berichterstattungsmechanismus.</span><span class="sxs-lookup"><span data-stu-id="69c8d-147">The App-V 5.0 sequencer reports the VC run-time dependency using the sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="69c8d-148">Mit dem App-V 5,0-Sequenzer können Sie jetzt die VC-Laufzeitabhängigkeit ausschließen, falls die Abhängigkeit bereits auf dem Computer verfügbar ist, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69c8d-148">The App-V 5.0 sequencer now allows you to exclude the VC run-time dependency in the event that the dependency is already available on the computer running the sequencer.</span></span>

### <span data-ttu-id="69c8d-149">Verbesserungen bei der Veröffentlichungsaktualisierung</span><span class="sxs-lookup"><span data-stu-id="69c8d-149">Publishing Refresh Improvements</span></span>

<span data-ttu-id="69c8d-150">App-V 5,0 unterstützt mehrere Features wurden hinzugefügt, um die allgemeine Erfahrung beim Aktualisieren einer Reihe von Anwendungen für einen bestimmten Benutzer zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="69c8d-150">App-V 5.0 supports several features were added to improve the overall experience of refreshing a set of applications for a specific user.</span></span>

<span data-ttu-id="69c8d-151">In der folgenden Liste werden die Verbesserungen der Veröffentlichungsaktualisierung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="69c8d-151">The following list displays the publishing refresh enhancements:</span></span>

<span data-ttu-id="69c8d-152">In der folgenden Liste finden Sie weitere Informationen dazu, wie die Verbesserungen bei der Aktualisierung der Veröffentlichung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="69c8d-152">The following list contains more information about how to enable the new publishing refresh improvements.</span></span>

-   <span data-ttu-id="69c8d-153">**EnablePublishingRefreshUI** – aktiviert die Statusleiste für die Veröffentlichungsaktualisierung für den Computer, auf dem der App-V 5,0-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69c8d-153">**EnablePublishingRefreshUI** - Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span>

-   <span data-ttu-id="69c8d-154">**HideUI** – blendet die Statusleiste der Veröffentlichungsaktualisierung während einer manuellen Synchronisierung aus.</span><span class="sxs-lookup"><span data-stu-id="69c8d-154">**HideUI** - Hides the publishing refresh progress bar during a manual sync.</span></span>

### <span data-ttu-id="69c8d-155">Einstellung für neue Client Konfiguration</span><span class="sxs-lookup"><span data-stu-id="69c8d-155">New Client Configuration Setting</span></span>

<span data-ttu-id="69c8d-156">Die folgende neue Client Konfigurationseinstellung ist in App-V 5,0 SP2 verfügbar:</span><span class="sxs-lookup"><span data-stu-id="69c8d-156">The following new client configuration setting is available with App-V 5.0 SP2:</span></span>

<span data-ttu-id="69c8d-157">**EnableDynamicVirtualization** – ermöglicht unterstützte Shell-Erweiterungen, Browser-helferobjekte und ActiveX-Steuerelemente, die virtualisiert und mit virtuellen Anwendungen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="69c8d-157">**EnableDynamicVirtualization** - Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span>

<span data-ttu-id="69c8d-158">Weitere Informationen finden Sie unter [Informationen zu Client Konfigurationseinstellungen](about-client-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="69c8d-158">For more information, see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span>

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> <span data-ttu-id="69c8d-159">App-V 5,0-Shell-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="69c8d-159">App-V 5.0 Shell extensions</span></span>

<span data-ttu-id="69c8d-160">App-V 5,0 SP2 unterstützt jetzt Shell-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="69c8d-160">App-V 5.0 SP2 now supports shell extensions.</span></span>

<span data-ttu-id="69c8d-161">Weitere Informationen finden Sie im Abschnitt **Unterstützung für Shell-Erweiterungen der APP-v 5.0 SP2** unter [Erstellen und Verwalten von virtualisierten Anwendungen in App-v 5,0](creating-and-managing-app-v-50-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="69c8d-161">For more information see the **App-V 5.0SP2 shell extension support** section of [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

## <a href="" id="---------app-v-5-0-documentation-updates"></a> <span data-ttu-id="69c8d-162">App-V 5,0-Dokumentationsupdates</span><span class="sxs-lookup"><span data-stu-id="69c8d-162">App-V 5.0 documentation updates</span></span>


<span data-ttu-id="69c8d-163">App-V 5,0 SP2 bietet aktualisierte Dokumentation für die folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="69c8d-163">App-V 5.0 SP2 provides updated documentation for the following scenarios:</span></span>

-   [<span data-ttu-id="69c8d-164">Migrieren von einer früheren Version</span><span class="sxs-lookup"><span data-stu-id="69c8d-164">Migrating from a Previous Version</span></span>](migrating-from-a-previous-version-app-v-50.md)

-   [<span data-ttu-id="69c8d-165">Informationen zu App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="69c8d-165">About App-V 5.0</span></span>](about-app-v-50.md)

-   <span data-ttu-id="69c8d-166">[Informationen zu App-V 5,0-Berichterstellung](about-app-v-50-reporting.md) (Abschnitt "häufig gestellte Fragen")</span><span class="sxs-lookup"><span data-stu-id="69c8d-166">[About App-V 5.0 Reporting](about-app-v-50-reporting.md) (frequently asked questions section)</span></span>

## <span data-ttu-id="69c8d-167">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="69c8d-167">How to Get MDOP Technologies</span></span>


<span data-ttu-id="69c8d-168">App-V 5,0 ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="69c8d-168">App-V 5.0 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="69c8d-169">MDOP ist Teil von Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="69c8d-169">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="69c8d-170">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="69c8d-170">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="69c8d-171">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="69c8d-171">Related topics</span></span>


[<span data-ttu-id="69c8d-172">Versionshinweise für App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="69c8d-172">Release Notes for App-V 5.0 SP2</span></span>](release-notes-for-app-v-50-sp2.md)

 

 





