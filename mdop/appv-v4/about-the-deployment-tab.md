---
title: Informationen zur Registerkarte „Bereitstellung“
description: Informationen zur Registerkarte „Bereitstellung“
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808116"
---
# <span data-ttu-id="3e4ce-103">Informationen zur Registerkarte „Bereitstellung“</span><span class="sxs-lookup"><span data-stu-id="3e4ce-103">About the Deployment Tab</span></span>


<span data-ttu-id="3e4ce-104">Verwenden Sie die Registerkarte **Bereitstellung** in der Application Virtualization Sequencer Console, um die Informationen für eine Anwendung zu ändern, die Sie gerade abgleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-104">Use the **Deployment** tab in the Application Virtualization Sequencer Console to change the information for an application you are about to sequence.</span></span> <span data-ttu-id="3e4ce-105">Diese Registerkarte enthält die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-105">This tab contains the following elements.</span></span>

## <span data-ttu-id="3e4ce-106">Server-URL</span><span class="sxs-lookup"><span data-stu-id="3e4ce-106">Server URL</span></span>


<span data-ttu-id="3e4ce-107">Verwenden Sie die **Server-URL** -Steuerelemente, um die Konfigurationseinstellungen für den virtuellen Anwendungsserver anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-107">Use the **Server URL** controls to specify the virtual application server configuration settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e4ce-108">Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3e4ce-108">Control</span></span></th>
<th align="left"><span data-ttu-id="3e4ce-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e4ce-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3e4ce-110">Protokoll</span><span class="sxs-lookup"><span data-stu-id="3e4ce-110">Protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3e4ce-111">Ermöglicht Ihnen, das Protokoll auszuwählen, das das sequenzierte Anwendungspaket von einem virtuellen Anwendungsserver zu einem Application Virtualization-Desktop Client streamen soll.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-111">Enables you to select the protocol that will stream the sequenced application package from a virtual application server to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="3e4ce-112">Die folgenden Protokolle stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="3e4ce-112">The following protocols are available:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="3e4ce-113">RTSP </strong> – der Standardwert gibt an, dass das Echt Zeit Streaming-Protokoll den Austausch von Virtualisierungs fähigen Anwendungen steuert.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-113">RTSP</strong>—The default, it specifies that the Real-Time Streaming Protocol controls the exchange of virtualization-enabled applications.</span></span></p></li>
<li><p><strong><span data-ttu-id="3e4ce-114">RTSPS </strong> – gibt an, dass das Echt Zeit Streaming-Protokoll mit Transport Schicht Sicherheit den Austausch eines sequenzierten Anwendungspakets steuert.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-114">RTSPS</strong>—Specifies that the Real-Time Streaming Protocol with Transport Layer Security controls the exchange of a sequenced application package.</span></span></p></li>
<li><p><strong><span data-ttu-id="3e4ce-115">Datei </strong> : gibt an, dass die sequenzierte Anwendung von einer Dateifreigabe gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-115">File</strong>—Specifies that the sequenced application will be streamed from a file share.</span></span></p></li>
<li><p><strong><span data-ttu-id="3e4ce-116">HTTPS </strong> : gibt an, dass das sichere Hypertext-Transport Protokoll den Austausch eines Pakets steuert.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-116">HTTPS</strong>—Specifies that Secure Hypertext Transport Protocol controls the exchange of a package.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3e4ce-117">Hostname</span><span class="sxs-lookup"><span data-stu-id="3e4ce-117">Hostname</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3e4ce-118">Ermöglicht Ihnen, den virtuellen Anwendungsserver oder das Load Balancer vor einer Gruppe virtueller Anwendungsserver auszuwählen, die das Softwarepaket an einen Application Virtualization Desktop-Client streamen.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-118">Enables you to select the virtual application server or the load balancer in front of a group of virtual application servers that will stream the software package to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="3e4ce-119">Sie müssen dieses Element zum Erstellen eines sequenzierten Anwendungspakets ausfüllen, doch können Sie von der Standardumgebungsvariable% SFT_SOFTGRIDSERVER% auf den tatsächlichen Hostnamen oder die IP-Adresse eines virtuellen Anwendungsservers umstellen.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-119">You must complete this item to create a sequenced application package, but you can change from the default %SFT_SOFTGRIDSERVER% environment variable to the actual hostname or IP address of a virtual application server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3e4ce-120">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3e4ce-120">Note</span></span></strong><br/><p><span data-ttu-id="3e4ce-121">Wenn Sie keine statischen Hostnamen oder IP-Adressen angeben, müssen Sie auf jedem Application Virtualization-Desktop Client eine Umgebungsvariable mit dem Namen SFT_SOFTGRIDSERVER einrichten.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-121">If you choose not to specify a static hostname or IP address, on each Application Virtualization Desktop Client you must set up an environment variable called SFT_SOFTGRIDSERVER.</span></span> <span data-ttu-id="3e4ce-122">Der Wert muss der Hostname oder die IP-Adresse des Virtual Application Servers oder Load Balancer sein, bei dem es sich um die Quelle der Anwendungen dieses Client&#39;s handelt.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-122">Its value must be the hostname or IP address of the virtual application server or load balancer that is this client&#39;s source of applications.</span></span> <span data-ttu-id="3e4ce-123">Sie sollten diese Umgebungsvariable zu einer Systemvariablen anstatt zu einer Benutzervariablen machen.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-123">You should make this environment variable a system variable rather than a user variable.</span></span> <span data-ttu-id="3e4ce-124">Jede Application Virtualization Desktop Client-Sitzung, die während der Zuweisung dieser Variable auf diesem Computer ausgeführt wird, muss geschlossen und dann geöffnet werden, damit die wieder aufgenommene Sitzung über die neue Anwendungsquelle informiert wird.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-124">Any Application Virtualization Desktop Client session that is running on this computer during your assignment of this variable must be closed and then opened so that the resumed session will be aware of its new application source.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3e4ce-125">Port</span><span class="sxs-lookup"><span data-stu-id="3e4ce-125">Port</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3e4ce-126">Ermöglicht es Ihnen, den Port anzugeben, auf dem der Virtual Application Server oder das Load Balancer auf eine Application Virtualization Desktop Client&#39;s-Anforderung für das Paket lauscht.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-126">Enables you to specify the port on which the virtual application server or the load balancer will listen for an Application Virtualization Desktop Client&#39;s request for the package.</span></span> <span data-ttu-id="3e4ce-127">Diese Informationen sind zum Erstellen eines Pakets erforderlich, können aber geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-127">This information is required to create a package, but you can change it.</span></span> <span data-ttu-id="3e4ce-128">Der Standardport ist 554.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-128">The default port is 554.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3e4ce-129">Pfad</span><span class="sxs-lookup"><span data-stu-id="3e4ce-129">Path</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3e4ce-130">Ermöglicht es Ihnen, den relativen Pfad auf dem virtuellen Anwendungsserver anzugeben, in dem das Softwarepaket gespeichert ist und von dem es gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-130">Enables you to specify the relative path on the virtual application server where the software package is stored and from which it will be streamed.</span></span> <span data-ttu-id="3e4ce-131">Diese Informationen sind erforderlich, um ein Paket zu erstellen, wenn die SFT-Datei in einem Unterverzeichnis des Inhalts gespeichert werden soll. Andernfalls sind diese Informationen nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-131">This information is required to create a package if the SFT file will be stored in a subdirectory of CONTENT; otherwise, this information is not required.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3e4ce-132">Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="3e4ce-132">Operating Systems</span></span>


<span data-ttu-id="3e4ce-133">Verwenden Sie die Steuerelemente für **Betriebssysteme** , um die Betriebssystemanforderungen der Anwendung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-133">Use the **Operating Systems** controls to specify the application's operating system requirements.</span></span> <span data-ttu-id="3e4ce-134">Wenn ein Application Virtualization Desktop-Client keines der ausgewählten Betriebssysteme unterstützt, wird die Anwendung nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-134">If an Application Virtualization Desktop Client cannot support any of the selected operating systems, the application will not start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e4ce-135">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3e4ce-135">Controls</span></span></th>
<th align="left"><span data-ttu-id="3e4ce-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e4ce-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3e4ce-137">Verfügbare Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="3e4ce-137">Available Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3e4ce-138">Zeigt eine Liste der Betriebssysteme an, die die Anwendungen im Paket unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-138">Displays a list of operating systems that can support the applications in the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3e4ce-139">Ausgewählte Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="3e4ce-139">Selected Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3e4ce-140">Zeigt eine Liste der ausgewählten Betriebssysteme an, die die Anwendungen im Paket unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-140">Displays a list of selected operating systems that support the applications in the package.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3e4ce-141">Ausgabeoptionen</span><span class="sxs-lookup"><span data-stu-id="3e4ce-141">Output Options</span></span>


<span data-ttu-id="3e4ce-142">Verwenden Sie die Steuerelemente für **Ausgabeoptionen** , um die Ausgabeoptionen für die Anwendung anzugeben, die installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-142">Use the **Output Options** controls to specify the output options for the application to be installed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e4ce-143">Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3e4ce-143">Control</span></span></th>
<th align="left"><span data-ttu-id="3e4ce-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e4ce-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3e4ce-145">Komprimierungsalgorithmus</span><span class="sxs-lookup"><span data-stu-id="3e4ce-145">Compression Algorithm</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3e4ce-146">Hiermit wählen Sie die Methode zum Komprimieren der SFT-Datei für das Streaming in einem Netzwerk aus.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-146">Use to select the method for compressing the SFT file for streaming across a network.</span></span> <span data-ttu-id="3e4ce-147">Wählen Sie eine der folgenden Komprimierungsmethoden aus:</span><span class="sxs-lookup"><span data-stu-id="3e4ce-147">Select one of the following compression methods:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="3e4ce-148">Komprimiert </strong> : gibt an, dass die SFT-Datei im zlib-Format komprimiert werden soll <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="3e4ce-148">Compressed</strong>—Specifies that the SFT file be compressed in the <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)">ZLIB</a> format.</span></span></p></li>
<li><p><strong><span data-ttu-id="3e4ce-149">Nicht komprimiert </strong> – Standard; gibt an, dass die SFT-Datei nicht komprimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-149">Not Compressed</strong>—The default; specifies that the SFT file not be compressed.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3e4ce-150">Erzwingen von Sicherheitsbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="3e4ce-150">Enforce Security Descriptors</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3e4ce-151">Wählen Sie diese Option aus, um Sicherheitsbeschreibungen der Anwendungen im Paket zu erzwingen, nachdem Sie für den Client bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-151">Select to enforce security descriptors of the applications in the package after it is deployed to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3e4ce-152">Generieren des Microsoft Windows Installer-Pakets (MSI)</span><span class="sxs-lookup"><span data-stu-id="3e4ce-152">Generate Microsoft Windows Installer (MSI) Package</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3e4ce-153">Wählen Sie aus, ob Sie ein sequenziertes Anwendungspaket mit dem Windows Installer installieren oder bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-153">Select to install or deploy a sequenced application package with the Windows Installer.</span></span> <span data-ttu-id="3e4ce-154">Wenn Sie mit dem Sequencer Änderungen vorgenommen haben, werden die Änderungen nicht in die Windows Installer-Datei übernommen.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-154">If you have made any changes using the sequencer the changes will not be included with the Windows Installer file.</span></span> <span data-ttu-id="3e4ce-155">Die Windows Installer-Datei wird immer unter Verwendung der auf der Festplatte gespeicherten SFT-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="3e4ce-155">The Windows Installer file will always be created using the .sft file saved on the hard disk.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3e4ce-156">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3e4ce-156">Related topics</span></span>


[<span data-ttu-id="3e4ce-157">So ändern Sie die Bereitstellungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e4ce-157">How to Change Deployment Properties</span></span>](how-to-change-deployment-properties.md)

[<span data-ttu-id="3e4ce-158">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="3e4ce-158">Sequencer Console</span></span>](sequencer-console.md)









