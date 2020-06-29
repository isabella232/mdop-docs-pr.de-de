---
title: MED-V-TrimTransfer-Technologie
description: MED-V-TrimTransfer-Technologie
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811605"
---
# <span data-ttu-id="35183-103">MED-V-TrimTransfer-Technologie</span><span class="sxs-lookup"><span data-stu-id="35183-103">MED-V Trim Transfer Technology</span></span>


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


<span data-ttu-id="35183-104">Die Med-v Advanced Trim Transfer-Deduplizierungs-Technologie beschleunigt den Download von anfänglichen und aktualisierten virtuellen Computerbildern über das LAN oder WAN, wodurch die Netzwerkbandbreite verringert wird, die für den Transport eines virtuellen Computers mit einem Med-v-Arbeitsbereich an mehrere Endbenutzer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="35183-104">The MED-V advanced Trim Transfer de-duplication technology accelerates the download of initial and updated virtual machine images over the LAN or WAN, thereby reducing the network bandwidth needed to transport a MED-V workspace virtual machine to multiple end users.</span></span>

<span data-ttu-id="35183-105">Diese bahnbrechende Technologie verwendet vorhandene lokale Daten, um das Bild des virtuellen Computers zu erstellen, und nutzt dabei die Tatsache, dass in vielen Fällen ein Großteil des virtuellen Computers (beispielsweise System-und Anwendungsdateien) auf dem Datenträger des Endbenutzers bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="35183-105">This breakthrough technology uses existing local data to build the virtual machine image, leveraging the fact that in many cases, much of the virtual machine (for example, system and application files) already exists on the end user's disk.</span></span> <span data-ttu-id="35183-106">Wenn beispielsweise ein virtueller Computer, der WindowsXP enthält, an einen Client mit einer lokalen Kopie von WindowsXP übermittelt wird, entfernt MED-V automatisch die redundanten WindowsXP-Elemente aus der Übertragung.</span><span class="sxs-lookup"><span data-stu-id="35183-106">For example, if a virtual machine containing WindowsXP is delivered to a client running a local copy of WindowsXP, MED-V will automatically remove the redundant WindowsXP elements from the transfer.</span></span> <span data-ttu-id="35183-107">Um einen gültigen und funktionsfähigen Arbeitsbereich zu gewährleisten, überprüft der MED-V-Client die Integrität lokaler Daten vor der Verwendung kryptografisch, und gewährleistet, dass die lokalen Datenblöcke absolut identisch mit denen im Bild des gewünschten virtuellen Computers sind.</span><span class="sxs-lookup"><span data-stu-id="35183-107">To ensure a valid and functional workspace, the MED-V client cryptographically verifies the integrity of local data before it is utilized, guaranteeing that the local blocks of data are absolutely bit-by-bit identical to those in the desired virtual machine image.</span></span> <span data-ttu-id="35183-108">Blöcke, die nicht übereinstimmen, werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="35183-108">Blocks that do not match are not used.</span></span>

<span data-ttu-id="35183-109">Der Prozess ist bandbreiteneffizient und transparent, und Übertragungen werden im Hintergrund ausgeführt, wobei ungenutzte Netzwerk-und CPU-Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35183-109">The process is bandwidth-efficient and transparent, and transfers run in the background, utilizing unused network and CPU resources.</span></span>

<span data-ttu-id="35183-110">Beim Aktualisieren auf eine neue Bildversion (beispielsweise wenn Administratoren eine neue Anwendung oder einen neuen Patch verteilen möchten) werden nur die geänderten Elemente ("Deltas") heruntergeladen, und nicht die gesamte virtuelle Maschine, wodurch die erforderliche Netzwerkbandbreite und die erforderliche Lieferzeit erheblich reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="35183-110">When updating to a new image version (for example, when administrators want to distribute a new application or patch), only the elements that have changed ("deltas") are downloaded, and not the entire virtual machine, significantly reducing the required network bandwidth and delivery time.</span></span>

<span data-ttu-id="35183-111">Sie können konfigurieren, welche Ordner auf dem Host als Teil des Trim-Übertragungsprotokolls basierend auf dem Hostbetriebssystem indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="35183-111">You can configure which folders are indexed on the host as part of the Trim Transfer protocol, based on the host operating system.</span></span> <span data-ttu-id="35183-112">Diese Einstellungen werden in der *ClientSettings.xml* -Datei konfiguriert, die im Ordner **Servers\\Configuration Server\\** zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="35183-112">These settings are configured in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="35183-113">Bei der Anwendung neuer Einstellungen muss der Dienst neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="35183-113">When applying new settings, the service must be restarted.</span></span>

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





