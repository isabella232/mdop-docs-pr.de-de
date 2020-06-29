---
title: So konfigurieren Sie den Client für den unterbrochenen Betriebsmodus
description: So konfigurieren Sie den Client für den unterbrochenen Betriebsmodus
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807259"
---
# <span data-ttu-id="ed329-103">So konfigurieren Sie den Client für den unterbrochenen Betriebsmodus</span><span class="sxs-lookup"><span data-stu-id="ed329-103">How to Configure the Client for Disconnected Operation Mode</span></span>


<span data-ttu-id="ed329-104">Der Modus für getrennte Vorgänge ermöglicht es dem Application Virtualization (app-v)-Desktop Client oder dem Application Virtualization (app-v)-Client für Remote Desktop Dienste (ehemals Terminal Dienste), Anwendungen auszuführen, die im Dateisystemcache des Clients gespeichert sind, wenn der Client keine Verbindung mit dem App-v-Verwaltungs Server herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="ed329-104">The disconnected operation mode enables the Application Virtualization (App-V) Desktop Client or the Application Virtualization (App-V) Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client cannot connect to the App-V Management Server.</span></span>

<span data-ttu-id="ed329-105">**Wichtig**  In einer großen Organisation, in der mehrere Remote Desktop-Sitzungshost Server (ehemals Terminal Server) in einer Farm zur Unterstützung vieler Benutzer verknüpft sind, stellt die Verwendung eines einzelnen App-V-Verwaltungsservers zur Unterstützung der Farm einen einzelnen Fehlerpunkt dar.</span><span class="sxs-lookup"><span data-stu-id="ed329-105">**Important** In a large organization where multiple Remote Desktop Session Host (RD°Session Host) servers (formerly Terminal Servers) are linked in a farm to support many users, using a single App-V Management Server to support the farm represents a single point of failure.</span></span> <span data-ttu-id="ed329-106">Wenn Sie eine höhere Verfügbarkeit für die Unterstützung der RDSession-Host Farm bereitstellen möchten, sollten Sie zwei oder mehr App-V-Verwaltungsserver zur Verwendung derselben Datenbank verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="ed329-106">To provide high availability to support the RDSession Host farm, consider linking two or more App-V Management Servers to use the same database.</span></span>

 

**<span data-ttu-id="ed329-107">So aktivieren Sie den Modus für unterbrochenen Betrieb</span><span class="sxs-lookup"><span data-stu-id="ed329-107">To enable disconnected operation mode</span></span>**

-   <span data-ttu-id="ed329-108">Setzen Sie den folgenden Registrierungsschlüsselwert auf "1", um den unterbrochenen Betriebsmodus zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="ed329-108">Set the following registry key value equal to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="ed329-109">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\allowdisconnectedoperation</span><span class="sxs-lookup"><span data-stu-id="ed329-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

**<span data-ttu-id="ed329-110">So setzen Sie ein Zeitlimit für die Verwendung des getrennten Betriebsmodus</span><span class="sxs-lookup"><span data-stu-id="ed329-110">To set a time limit on disconnected operation mode use</span></span>**

1.  <span data-ttu-id="ed329-111">Setzen Sie den folgenden Registrierungsschlüsselwert auf 1:</span><span class="sxs-lookup"><span data-stu-id="ed329-111">Set the following registry key value to 1:</span></span>

    <span data-ttu-id="ed329-112">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\limitdisconnectedoperation</span><span class="sxs-lookup"><span data-stu-id="ed329-112">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

2.  <span data-ttu-id="ed329-113">Setzen Sie den folgenden Registrierungsschlüsselwert auf die Anzahl der Minuten, die Sie den unterbrochenen Betriebsmodus einschränken möchten.</span><span class="sxs-lookup"><span data-stu-id="ed329-113">Set the following registry key value to the number of minutes you want to limit disconnected operation mode.</span></span> <span data-ttu-id="ed329-114">Der gültige Wertebereich ist 1 – 999999.</span><span class="sxs-lookup"><span data-stu-id="ed329-114">The valid range of values is 1–999999.</span></span> <span data-ttu-id="ed329-115">Der Standardwert ist 90 Tage oder 129.600 Minuten.</span><span class="sxs-lookup"><span data-stu-id="ed329-115">The default value is 90 days or 129,600 minutes.</span></span>

    <span data-ttu-id="ed329-116">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\dotimeoutminutes</span><span class="sxs-lookup"><span data-stu-id="ed329-116">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span></span>

**<span data-ttu-id="ed329-117">So konfigurieren Sie den Client für Remote Desktop Dienste für den unterbrochenen Betriebsmodus</span><span class="sxs-lookup"><span data-stu-id="ed329-117">To configure the Client for Remote Desktop Services for disconnected operation mode</span></span>**

1.  <span data-ttu-id="ed329-118">Stellen Sie den folgenden Registrierungsschlüsselwert auf 1 ein, um den unterbrochenen Betriebsmodus zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="ed329-118">Set the following registry key value to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="ed329-119">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\allowdisconnectedoperation</span><span class="sxs-lookup"><span data-stu-id="ed329-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

2.  <span data-ttu-id="ed329-120">Setzen Sie den folgenden Registrierungsschlüsselwert auf 0 (null), um die unbegrenzte Verwendung des unterbrochenen Betriebsmodus zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="ed329-120">Set the following registry key value to 0 (zero) to allow unlimited use of disconnected operation mode:</span></span>

    <span data-ttu-id="ed329-121">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\limitdisconnectedoperation</span><span class="sxs-lookup"><span data-stu-id="ed329-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

3.  <span data-ttu-id="ed329-122">Stellen Sie sicher, dass alle Pakete in den Cache geladen sind, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ed329-122">Ensure that all packages are preloaded into the cache to improve performance.</span></span>

## <span data-ttu-id="ed329-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ed329-123">Related topics</span></span>


[<span data-ttu-id="ed329-124">Unterbrochener Betriebsmodus</span><span class="sxs-lookup"><span data-stu-id="ed329-124">Disconnected Operation Mode</span></span>](disconnected-operation-mode.md)

[<span data-ttu-id="ed329-125">So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="ed329-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





