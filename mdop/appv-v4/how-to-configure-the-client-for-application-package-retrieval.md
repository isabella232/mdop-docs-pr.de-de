---
title: So konfigurieren Sie den Client für den Abruf von Anwendungspaketen
description: So konfigurieren Sie den Client für den Abruf von Anwendungspaketen
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807263"
---
# <span data-ttu-id="dde23-103">So konfigurieren Sie den Client für den Abruf von Anwendungspaketen</span><span class="sxs-lookup"><span data-stu-id="dde23-103">How to Configure the Client for Application Package Retrieval</span></span>


<span data-ttu-id="dde23-104">Wenn der Client mit einem Application Virtualization (App-V)-Verwaltungsserver als Veröffentlichungsserver konfiguriert ist, ruft der Clientstandard mäßig beim nächsten Veröffentlichungs Aktualisierungszyklus vom Server die Open Software Descriptor (OSD)-und Paket Manifestdateien für jedes Paket ab, das der Benutzer für die Verwendung autorisiert hat.</span><span class="sxs-lookup"><span data-stu-id="dde23-104">When the client is configured with an Application Virtualization (App-V) Management Server as its publishing server, by default at the next publishing refresh cycle, the client retrieves from the server the Open Software Descriptor (OSD) and package manifest files for each package that the user is authorized to use.</span></span> <span data-ttu-id="dde23-105">Der Client verwendet die in diesen Dateien definierten Paketquellinformationen, um zu bestimmen, wo die Paketinhalte, Symbole und Dateitypzuordnungen zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="dde23-105">The client uses the package source information that is defined in these files to determine where to find the package content, icons, and file type associations.</span></span>

<span data-ttu-id="dde23-106">Wenn der Client den Paketinhalt (SFT-Datei) von einem lokalen app-v-Streamingserver oder einer anderen alternativen Quelle wie einem Webserver oder Dateiserver anstatt vom APP-v-Verwaltungsserver abrufen soll, können Sie den ApplicationSourceRoot-Registrierungsschlüsselwert auf dem Computer so konfigurieren, dass er auf die lokale Inhaltsfreigabe auf dem anderen Server verweist.</span><span class="sxs-lookup"><span data-stu-id="dde23-106">If you want the client to obtain the package content (SFT file) from a local App-V Streaming Server or other alternate source such as a Web server or file server, instead of from the App-V Management Server, you can configure the ApplicationSourceRoot registry key value on the computer to point to the local content share on the other server.</span></span> <span data-ttu-id="dde23-107">Die OSD-Datei definiert weiterhin den ursprünglichen Quellpfad für den Paketinhalt.</span><span class="sxs-lookup"><span data-stu-id="dde23-107">The OSD file still defines the original source path for the package content.</span></span> <span data-ttu-id="dde23-108">Der Client verwendet jedoch den Wert der ApplicationSourceRoot-Einstellung anstelle des Servers und der Freigabe, die im Inhaltspfad in der OSD-Datei angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="dde23-108">However the client uses the value of the ApplicationSourceRoot setting in place of the server and share that are specified in the content path in the OSD file.</span></span> <span data-ttu-id="dde23-109">Dadurch wird der Client umgeleitet, um den Inhalt vom anderen Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dde23-109">This redirects the client to retrieve the content from the other server.</span></span>

<span data-ttu-id="dde23-110">Sie können auch die Registrierungsschlüsselwerte für OSDSourceRoot und IconSourceRoot konfigurieren, wenn Sie diese Einstellungen in der Paket Manifestdatei oder in den von einem Veröffentlichungsserver gesendeten Pfaden überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="dde23-110">You can also configure the OSDSourceRoot and IconSourceRoot registry key values if you want to override those settings in the package manifest file or in the paths sent by a publishing server.</span></span> <span data-ttu-id="dde23-111">OSDSourceRoot gibt einen Quellspeicherort für das Abrufen von OSD-Dateien für ein Anwendungspaket während der Veröffentlichung an.</span><span class="sxs-lookup"><span data-stu-id="dde23-111">The OSDSourceRoot specifies a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="dde23-112">Der IconSourceRoot gibt einen Quellspeicherort für den Symbol Abruf für ein Anwendungspaket während der Veröffentlichung an.</span><span class="sxs-lookup"><span data-stu-id="dde23-112">The IconSourceRoot specifies a source location for icon retrieval for an application package during publication.</span></span>

**<span data-ttu-id="dde23-113">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="dde23-113">Note</span></span>**  
-   <span data-ttu-id="dde23-114">Die IconSourceRoot-und OSDSourceRoot-Einstellungen setzen die Werte in der Paket Manifestdatei außer Kraft, wenn Sie also versuchen, ein Paket mithilfe der Windows Installer-Datei Methode (MSI) bereitzustellen, werden auch die Werte in der Paket Manifestdatei überschrieben, die in dieser MSI-Datei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="dde23-114">The IconSourceRoot and OSDSourceRoot settings override the values in the package manifest file, so if you try to deploy a package by using the Windows Installer (.msi) file method, it will also override the values in the package manifest file that is contained within that .msi file.</span></span>

-   <span data-ttu-id="dde23-115">Während der Veröffentlichungs-und http (S)-Streaming-Vorgänge verwenden App-V 4,5 SP1-Clients die Proxyservereinstellungen, die in Internet Explorer auf dem Computer des Benutzers konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="dde23-115">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>



**<span data-ttu-id="dde23-116">So konfigurieren Sie den ApplicationSourceRoot-Registrierungsschlüsselwert</span><span class="sxs-lookup"><span data-stu-id="dde23-116">To configure the ApplicationSourceRoot registry key value</span></span>**

-   <span data-ttu-id="dde23-117">Konfigurieren Sie den ApplicationSourceRoot im folgenden Registrierungsschlüsselwert mit einem UNC-Pfad oder einer URL:</span><span class="sxs-lookup"><span data-stu-id="dde23-117">Configure the ApplicationSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="dde23-118">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\applicationsourceroot</span><span class="sxs-lookup"><span data-stu-id="dde23-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span></span>

    <span data-ttu-id="dde23-119">Das richtige Format für den UNC-Pfad (Universal Naming Convention) ist **\\\\computername\\sharefolder\\\ [Folder \] \ [\ \ \]**, wobei **Folder** optional ist.</span><span class="sxs-lookup"><span data-stu-id="dde23-119">The correct format for the Universal Naming Convention (UNC) path is **\\\\computername\\sharefolder\\\[folder\]\[\\\]**, where **folder** is optional.</span></span> <span data-ttu-id="dde23-120">Bei **Computer** Name kann es sich um einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder eine IP-Adresse handeln, und **sharefolder** kann ein Laufwerkbuchstabe sein.</span><span class="sxs-lookup"><span data-stu-id="dde23-120">The **computername** can be a Fully Qualified Domain Name (FQDN) or an IP address, and **sharefolder** can be a drive letter.</span></span> <span data-ttu-id="dde23-121">Es wird nur der **\\\\computername\\sharedfolder** -oder Laufwerkbuchstaben Bereich des OSD-Pfads ersetzt.</span><span class="sxs-lookup"><span data-stu-id="dde23-121">Only the **\\\\computername\\sharedfolder** or drive letter portion of the OSD path is replaced.</span></span>

    <span data-ttu-id="dde23-122">Das richtige Format für den URL-Pfad ist **Protocol://Servername: \ [Port \] \ [/path\] \ [/\]**, wobei **Port** und **path** optional sind.</span><span class="sxs-lookup"><span data-stu-id="dde23-122">The correct format for the URL path is **protocol://servername:\[port\]\[/path\]\[/\]**, where **port** and **path** are optional.</span></span> <span data-ttu-id="dde23-123">Wenn **Port** nicht angegeben wird, wird der Standardport für das Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="dde23-123">If **port** is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="dde23-124">Nur der Abschnitt **Protocol://Server: Port** der OSD-URL wird ersetzt.</span><span class="sxs-lookup"><span data-stu-id="dde23-124">Only the **protocol://server:port** portion of the OSD URL is replaced.</span></span>

    **<span data-ttu-id="dde23-125">Wichtig</span><span class="sxs-lookup"><span data-stu-id="dde23-125">Important</span></span>**  
    <span data-ttu-id="dde23-126">Umgebungsvariablen werden in der ApplicationSourceRoot-Definition nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dde23-126">Environment variables are not supported in the ApplicationSourceRoot definition.</span></span>



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**<span data-ttu-id="dde23-127">So konfigurieren Sie den OSDSourceRoot-Wert</span><span class="sxs-lookup"><span data-stu-id="dde23-127">To configure the OSDSourceRoot value</span></span>**

-   <span data-ttu-id="dde23-128">Konfigurieren Sie den OSDSourceRoot im folgenden Registrierungsschlüsselwert mit einem UNC-Pfad oder einer URL:</span><span class="sxs-lookup"><span data-stu-id="dde23-128">Configure the OSDSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="dde23-129">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\osdsourceroot</span><span class="sxs-lookup"><span data-stu-id="dde23-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span></span>

    <span data-ttu-id="dde23-130">Zulässige Formate für die OSDSourceRoot sind UNC-Pfade und-URLs, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="dde23-130">Acceptable formats for the OSDSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="dde23-131">**\\\\computername\\sharefolder\\resource** oder **\\\\computername\\content** oder \*\* &lt; Laufwerk &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="dde23-131">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="dde23-132">**http://computername/productivity/** oder**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="dde23-132">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

**<span data-ttu-id="dde23-133">So konfigurieren Sie den IconSourceRoot-Wert</span><span class="sxs-lookup"><span data-stu-id="dde23-133">To configure the IconSourceRoot value</span></span>**

-   <span data-ttu-id="dde23-134">Konfigurieren Sie den IconSourceRoot im folgenden Registrierungsschlüsselwert mit einem UNC-Pfad oder einer URL:</span><span class="sxs-lookup"><span data-stu-id="dde23-134">Configure the IconSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="dde23-135">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\iconsourceroot</span><span class="sxs-lookup"><span data-stu-id="dde23-135">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span></span>

    <span data-ttu-id="dde23-136">Zulässige Formate für die IconSourceRoot sind UNC-Pfade und-URLs, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="dde23-136">Acceptable formats for the IconSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="dde23-137">**\\\\computername\\sharefolder\\resource** oder **\\\\computername\\content** oder \*\* &lt; Laufwerk &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="dde23-137">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="dde23-138">**http://computername/productivity/** oder**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="dde23-138">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

## <span data-ttu-id="dde23-139">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dde23-139">Related topics</span></span>


[<span data-ttu-id="dde23-140">So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="dde23-140">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









