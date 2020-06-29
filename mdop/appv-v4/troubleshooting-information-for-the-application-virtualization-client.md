---
title: Informationen zur Problembehandlung für Application Virtualization Client
description: Informationen zur Problembehandlung für Application Virtualization Client
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806208"
---
# <span data-ttu-id="5f0f5-103">Informationen zur Problembehandlung für Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="5f0f5-103">Troubleshooting Information for the Application Virtualization Client</span></span>


<span data-ttu-id="5f0f5-104">Dieses Thema enthält Informationen, die Sie zur Behebung verschiedener Probleme auf dem Application Virtualization (App-V)-Client verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Client.</span></span>

## <span data-ttu-id="5f0f5-105">Die Veröffentlichungsaktualisierung ist sehr langsam</span><span class="sxs-lookup"><span data-stu-id="5f0f5-105">Publishing Refresh Is Very Slow</span></span>


<span data-ttu-id="5f0f5-106">Wenn die Veröffentlichungsaktualisierung auf einem bestimmten Computer viel länger als erwartet dauert und der Client für die Verwendung der **IconSourceRoot** -Einstellung konfiguriert ist, ermitteln Sie, ob **IconSourceRoot** eine ungültige URL enthält.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-106">If publishing refresh on a specific computer takes much longer than expected and if the client is configured to use the **IconSourceRoot** setting, determine whether **IconSourceRoot** contains a nonvalid URL.</span></span> <span data-ttu-id="5f0f5-107">Eine nicht gültige URL führt zu sehr langen Verzögerungen während der Veröffentlichungsaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-107">A nonvalid URL will cause very long delays during publishing refresh.</span></span>

## <span data-ttu-id="5f0f5-108">Benutzer können keine Verbindung mit dem Server herstellen und in den Modus für getrennte Vorgänge wechseln</span><span class="sxs-lookup"><span data-stu-id="5f0f5-108">Users Cannot Connect to the Server and Go into Disconnected Operations Mode</span></span>


<span data-ttu-id="5f0f5-109">Wenn Sie einen App-V-Verwaltungs Server verwenden, der mit dem RTSPS-Protokoll konfiguriert ist, können Sie ermitteln, ob das auf dem Server verwendete Zertifikat gültig ist, wenn die Benutzer keine Verbindung herstellen können und Sie in den Modus für getrennte Vorgänge wechseln.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-109">When you are using an App-V Management Server configured with the RTSPS protocol, if the users are unable to connect and they go into disconnected operations mode, determine whether the certificate that is being used on the server is valid.</span></span> <span data-ttu-id="5f0f5-110">Ein nicht gültiges Zertifikat verhindert, dass Benutzer eine Verbindung herstellen können, und führt dazu, dass Sie in den Modus für getrennte Vorgänge wechseln.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-110">A nonvalid certificate will prevent users from connecting and will cause them to go into disconnected operations mode.</span></span>

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a><span data-ttu-id="5f0f5-111">Benutzer verlangsamen die Leistung, wenn Anwendungen nicht vollständig zwischengespeichert werden</span><span class="sxs-lookup"><span data-stu-id="5f0f5-111">Users Experience Slow Performance When Applications Are Not Fully Cached</span></span>


<span data-ttu-id="5f0f5-112">Wenn Anwendungen nicht vollständig zwischengespeichert werden, kann es vorkommen, dass Benutzer beim Starten oder verwenden der Anwendung gelegentlich vorübergehende langsame oder zeitweilige Leistung erfahren.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-112">When applications are not fully cached, users might occasionally experience temporary slow or intermittent performance when they start or use the application.</span></span> <span data-ttu-id="5f0f5-113">Dies kann mehrere mögliche Gründe haben, beispielsweise, wenn der App-V-Client gerade eine Anwendung automatisch lädt oder wenn eine außer Sequenz-Anforderung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-113">There are several possible reasons this can occur—for example, when the App-V Client is in the process of auto-loading an application or when an Out Of Sequence request is being processed.</span></span> <span data-ttu-id="5f0f5-114">Wenn die Anwendungen vollständig zwischengespeichert sind, treten diese Probleme nicht mehr auf.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-114">When the applications are fully cached, these problems will no longer occur.</span></span>

## <a href="" id="error-displayed-after-an-update-is-removed-"></a><span data-ttu-id="5f0f5-115">Fehler angezeigt, nachdem eine Aktualisierung entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="5f0f5-115">Error Displayed After an Update Is Removed</span></span>


<span data-ttu-id="5f0f5-116">Sie müssen das richtige Windows Installer 3,1-Befehls Format verwenden, um ein Update vom App-V-Client wie folgt zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="5f0f5-116">You must use the correct Windows Installer 3.1 command format to remove an update from the App-V Client, as follows:</span></span>

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

<span data-ttu-id="5f0f5-117">Die Verwendung des älteren Befehlsformats `msiexec /package <GUID> /uninstall <GUID>` führt zu einem Fehler 6003 "Application Virtualization Client konnte nicht gestartet werden".</span><span class="sxs-lookup"><span data-stu-id="5f0f5-117">Using the older command format `msiexec /package <GUID> /uninstall <GUID>` will cause error 6003 "Application Virtualization client could not be started".</span></span>

## <span data-ttu-id="5f0f5-118">Fehler Code 0A-0000E01E tritt auf, wenn Sie versuchen, eine Anwendung zu starten</span><span class="sxs-lookup"><span data-stu-id="5f0f5-118">Error Code 0A-0000E01E Occurs When You Try to Start an Application</span></span>


<span data-ttu-id="5f0f5-119">Fehlercode 0A-0000E01E gibt an, dass das sequenzierte Anwendungspaket möglicherweise beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-119">Error code 0A-0000E01E indicates that the sequenced application package might be corrupt.</span></span> <span data-ttu-id="5f0f5-120">Die Lösung ist die Neusequenzierung des Pakets.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-120">The solution is to resequence the package.</span></span>

## <span data-ttu-id="5f0f5-121">Benutzer können nicht auf Dateien zugreifen, die Sie auf dem Laufwerk "f:" erstellt haben</span><span class="sxs-lookup"><span data-stu-id="5f0f5-121">Users Cannot Access Files They Have Created on the Q: Drive</span></span>


<span data-ttu-id="5f0f5-122">Wenn Benutzer Dateien auf dem Laufwerk **Q:** speichern, können Sie Sie nicht abrufen, da Sie keine Lese Rechte für das Laufwerk besitzen.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-122">If users save files to the **Q:** drive, they cannot retrieve them because they do not have read rights to the drive.</span></span> <span data-ttu-id="5f0f5-123">Benutzer sollten Dateien nicht auf dem Laufwerk **Q:** speichern.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-123">Users should not save files to the **Q:** drive.</span></span>

## <span data-ttu-id="5f0f5-124">Der Benutzer wird mit einem 1D1-Fehler aufgefordert</span><span class="sxs-lookup"><span data-stu-id="5f0f5-124">User Is Prompted with a 1D1 Error</span></span>


<span data-ttu-id="5f0f5-125">Wenn die Datei-Streaming-URL fälschlicherweise in der OSD-Datei (Open Software Descriptor) festgesetzt ist, gibt der App-V-Client einen 1D1-Fehler zurück, anstatt einen Fehler "Datei nicht gefunden" zu finden.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-125">When the file streaming URL is incorrectly set in the Open Software Descriptor (OSD) file, the App-V Client returns a 1d1 error instead of a “file not found” error.</span></span> <span data-ttu-id="5f0f5-126">Dieser Fehler zeigt an, dass der Anwendungsstart fehlgeschlagen ist und der Benutzer in den Modus für getrennte Vorgänge gezwungen wurde.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-126">This error indicates that the application start failed and the user has been forced into disconnected operations mode.</span></span> <span data-ttu-id="5f0f5-127">Korrigieren Sie die Datei-Streaming-URL.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-127">Correct the file streaming URL.</span></span>

## <span data-ttu-id="5f0f5-128">Mit einigen Anwendungen verknüpfte falsche Symbole</span><span class="sxs-lookup"><span data-stu-id="5f0f5-128">Incorrect Icons Associated with Some Applications</span></span>


<span data-ttu-id="5f0f5-129">Wenn ein Symbol in einem Veröffentlichungsvorgang verwendet werden soll, ermittelt der App-V-Client zunächst, ob bereits eine zwischengespeicherte Kopie des Symbols vorhanden ist, indem im Symbolcache nach einem Element gesucht wird, dessen ursprünglicher Quellpfad dem Pfad des Symbols entspricht, das dem Veröffentlichungsvorgang zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-129">When an icon is to be used in a publishing operation, the App-V Client first determines whether it already has a cached copy of the icon, by looking in the icon cache for an item whose original source path matches the path of the icon given to the publishing operation.</span></span> <span data-ttu-id="5f0f5-130">Wenn der App-V-Client eine Übereinstimmung findet, wird das bereits zwischengespeicherte Symbol verwendet. Andernfalls wird das neue Symbol in den Cache heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-130">If the App-V Client finds a match, it will use the already-cached icon; otherwise, it will download the new icon into the cache.</span></span> <span data-ttu-id="5f0f5-131">Wenn es sich bei dem Pfad zu dem Symbol um ein Scratch-Verzeichnis handelt oder wenn es für neue Symbole oder Pakete wieder verwendet wird, kann das Nachschlagen im Cache das falsche Symbol aus einem vorherigen Vorgang auswählen.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-131">If the path to the icon is a scratch directory or if it gets reused for new icons or packages, the lookup in the cache might pick the wrong icon from a previous operation.</span></span>

## <span data-ttu-id="5f0f5-132">Benutzer werden beim Starten einer Anwendung zur Eingabe von Anmeldeinformationen aufgefordert</span><span class="sxs-lookup"><span data-stu-id="5f0f5-132">Users Are Prompted for Credentials When Starting an Application</span></span>


<span data-ttu-id="5f0f5-133">Wenn ein Benutzer versucht, eine virtuelle Anwendung zu starten, auf die der System Administrator eingeschränkten Zugriff hat, wird der Benutzer möglicherweise zur Eingabe von Anmeldeinformationen aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-133">If a user attempts to start a virtual application to which the system administrator has restricted access, the user might be prompted to enter credentials.</span></span> <span data-ttu-id="5f0f5-134">Der Benutzer sollte den Benutzernamen und das Kennwort für ein Konto eingeben, das über die Berechtigung zum Starten der Anwendung verfügt, und dann die EINGABETASTE drücken.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-134">The user should type the user name and password for an account that has permission to launch the application and then press ENTER.</span></span>

## <span data-ttu-id="5f0f5-135">Die Veröffentlichungsaktualisierung schlägt nach dem Upgrade des App-V-Clients auf Version 4,5 fehl</span><span class="sxs-lookup"><span data-stu-id="5f0f5-135">Publishing Refresh Fails After Upgrading the App-V Client to Version 4.5</span></span>


<span data-ttu-id="5f0f5-136">Wenn das Benutzerdatenverzeichnis zuvor an einem nicht standardmäßigen Speicherort (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*username*%) gespeichert wurde, finden Benutzer, die nicht über Administratorrechte auf dem Computer verfügen, die Veröffentlichungsaktualisierung nach dem Upgrade des App-V-Clients fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-136">If the user data directory was previously placed in a non-standard location (%*AllUsersProfile*%\\Documents\\SoftGrid Client\\Users\\%*username*%), users who do not have administrator privileges on the computer will find that publishing refresh fails after the App-V Client is upgraded.</span></span> <span data-ttu-id="5f0f5-137">Während des Upgrades werden das globale App-V-Client-Datenverzeichnis und alle zugehörigen Unterverzeichnisse mit eingeschränkten Zugriffsrechten für Administratoren konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-137">During the upgrade, the App-V Client global data directory and all its subdirectories are configured with restricted access rights for administrators only.</span></span> <span data-ttu-id="5f0f5-138">Sie können dieses Problem vermeiden, indem Sie das Benutzerdatenverzeichnis vor dem Upgrade ändern, sodass es sich nicht um ein Unterverzeichnis des globalen Datenverzeichnisses handelt.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-138">You can avoid this problem by changing the user data directory before upgrading so that it is not a subdirectory of the global data directory.</span></span>

## <span data-ttu-id="5f0f5-139">Neustart nach Installationsfehler erforderlich</span><span class="sxs-lookup"><span data-stu-id="5f0f5-139">Reboot Required After Install Failure</span></span>


<span data-ttu-id="5f0f5-140">Wenn die Clientinstallation aus irgendeinem Grund fehlschlägt und bei nachfolgenden versuchen, den Client zu installieren, ebenfalls fehlschlägt, überprüfen Sie das Windows Installer-Protokoll, um festzustellen, ob ein Fehler "sftplay Fehler, Fehler = 1072" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-140">If the client install fails for any reason and if subsequent attempts to install the client also fail, check the Windows Installer log to see whether it shows an error “sftplay failed, error=1072”.</span></span> <span data-ttu-id="5f0f5-141">Wenn dies der Fall ist, starten Sie den Computer neu, bevor Sie versuchen, den Client erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-141">If so, restart the computer before trying to install the client again.</span></span>

## <span data-ttu-id="5f0f5-142">Reparieren einer beschädigten virtuellen Anwendung</span><span class="sxs-lookup"><span data-stu-id="5f0f5-142">Repairing a Corrupted Virtual Application</span></span>


<span data-ttu-id="5f0f5-143">Wenn ein virtuelles Anwendungspaket, das mit einer MSI-Datei (Windows Installer-Paket) installiert wurde, beschädigt wird, installieren Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-143">If for any reason a virtual application package installed using a Windows Installer Package (MSI) file becomes corrupted, reinstall the package.</span></span> <span data-ttu-id="5f0f5-144">Mit der im Windows Installer verfügbaren Funktion reparieren werden die Benutzer-Volumes nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-144">The Repair function available in the Windows Installer will not update the user volumes.</span></span>

## <span data-ttu-id="5f0f5-145">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5f0f5-145">Related topics</span></span>


[<span data-ttu-id="5f0f5-146">Application Virtualization Client-Referenz</span><span class="sxs-lookup"><span data-stu-id="5f0f5-146">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)

 

 





