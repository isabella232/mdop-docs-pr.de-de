---
title: Übersicht über Application Virtualization
description: Übersicht über Application Virtualization
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806556"
---
# <span data-ttu-id="1b1b4-103">Übersicht über Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="1b1b4-103">Overview of Application Virtualization</span></span>


<span data-ttu-id="1b1b4-104">Microsoft Application Virtualization (App-V) kann Anwendungen für Endbenutzercomputer verfügbar machen, ohne die Anwendungen direkt auf diesen Computern installieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-104">Microsoft Application Virtualization (App-V) can make applications available to end user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="1b1b4-105">Dies wird durch einen Prozess ermöglicht, der als *Sequenzierung der Anwendung*bezeichnet wird, wodurch jede Anwendung in ihrer eigenen, eigenständigen virtuellen Umgebung auf dem Clientcomputer ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-105">This is made possible through a process known as *sequencing the application*, which enables each application to run in its own self-contained virtual environment on the client computer.</span></span> <span data-ttu-id="1b1b4-106">Die sequenzierten Anwendungen sind voneinander isoliert.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-106">The sequenced applications are isolated from each other.</span></span> <span data-ttu-id="1b1b4-107">Dadurch werden Anwendungskonflikte beseitigt, die Anwendungen können jedoch weiterhin mit dem Clientcomputer interagieren.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-107">This eliminates application conflicts, but the applications can still interact with the client computer.</span></span>

<span data-ttu-id="1b1b4-108">Der App-V-Client ist das Feature, mit dem Endbenutzer mit den Anwendungen interagieren können, nachdem Sie auf dem Computer veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-108">The App-V client is the feature that lets the end user interact with the applications after they have been published to the computer.</span></span> <span data-ttu-id="1b1b4-109">Der Client verwaltet die virtuelle Umgebung, in der die virtualisierten Anwendungen auf jedem Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-109">The client manages the virtual environment in which the virtualized applications run on each computer.</span></span> <span data-ttu-id="1b1b4-110">Nachdem der Client auf einem Computer installiert wurde, müssen die Anwendungen dem Computer über einen als " *Publishing*" bezeichneten Prozess zur Verfügung gestellt werden, mit dem der Endbenutzer die virtuellen Anwendungen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-110">After the client has been installed on a computer, the applications must be made available to the computer through a process known as *publishing*, which enables the end user to run the virtual applications.</span></span> <span data-ttu-id="1b1b4-111">Beim Veröffentlichungsprozess werden die Symbole und Verknüpfungen der virtuellen Anwendung auf den Computer kopiert – normalerweise auf dem Windows-Desktop oder im **Startmenü** – und auch die Zuordnungsinformationen für die Paketdefinition und die Dateitypen werden auf den Computer kopiert.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-111">The publishing process copies the virtual application icons and shortcuts to the computer—typically on the Windows desktop or on the **Start** menu—and also copies the package definition and file type association information to the computer.</span></span> <span data-ttu-id="1b1b4-112">Durch die Veröffentlichung wird der Inhalt des Anwendungspakets auch dem Computer des Endbenutzers zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-112">Publishing also makes the application package content available to the end user’s computer.</span></span>

<span data-ttu-id="1b1b4-113">Der Inhalt des virtuellen Anwendungspakets kann auf einen oder mehrere Application Virtualization-Server kopiert werden, damit er bei Bedarf auf die Clients gestreamt und lokal zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-113">The virtual application package content can be copied onto one or more Application Virtualization servers so that it can be streamed down to the clients on demand and cached locally.</span></span> <span data-ttu-id="1b1b4-114">Dateiserver und Webserver können auch als Streamingserver verwendet werden, oder der Inhalt kann direkt auf den Computer des Endbenutzers kopiert werden – beispielsweise, wenn Sie ein elektronisches Softwareverteilungssystem wie Microsoft Endpoint Configuration Manager verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-114">File servers and Web servers can also be used as streaming servers, or the content can be copied directly to the end user’s computer—for example, if you are using an electronic software distribution system, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="1b1b4-115">Bei einer Multi-Server-Implementierung erfordert die Beibehaltung des Paketinhalts und die Aktualität auf allen Streaming-Servern eine umfassende Paketverwaltungslösung.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-115">In a multi-server implementation, maintaining the package content and keeping it up to date on all the streaming servers requires a comprehensive package management solution.</span></span> <span data-ttu-id="1b1b4-116">Je nach Größe Ihrer Organisation müssen Sie möglicherweise viele virtuelle Anwendungen für Endbenutzer verfügbar machen, die sich auf der ganzen Welt befinden.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-116">Depending on the size of your organization, you might need to have many virtual applications available to end users located all over the world.</span></span> <span data-ttu-id="1b1b4-117">Die Verwaltung der Pakete, um sicherzustellen, dass die entsprechenden Anwendungen allen Benutzern zur Verfügung stehen, wenn Sie Zugriff darauf benötigen, ist daher eine wichtige Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-117">Managing the packages to ensure that the appropriate applications are available to all users where and when they need access to them is therefore an important requirement.</span></span>

## <span data-ttu-id="1b1b4-118">Features des Microsoft Application Virtualization-Systems</span><span class="sxs-lookup"><span data-stu-id="1b1b4-118">Microsoft Application Virtualization System Features</span></span>


<span data-ttu-id="1b1b4-119">In der folgenden Tabelle werden die primären Features des Microsoft Application Virtualization-Verwaltungssystems beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-119">The following table describes the primary features of the Microsoft Application Virtualization Management System.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1b1b4-120">Feature</span><span class="sxs-lookup"><span data-stu-id="1b1b4-120">Feature</span></span></th>
<th align="left"><span data-ttu-id="1b1b4-121">Funktion</span><span class="sxs-lookup"><span data-stu-id="1b1b4-121">Function</span></span></th>
<th align="left"><span data-ttu-id="1b1b4-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1b1b4-122">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1b1b4-123">Microsoft Application Virtualization-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="1b1b4-123">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-124">Verantwortlich für das Streaming des Paketinhalts und die Veröffentlichung der Verknüpfungen und Dateitypzuordnungen zum Application Virtualization Client.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-124">Responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-125">Der Application Virtualization-Verwaltungs Server unterstützt das aktive Upgrade, die Lizenzverwaltung und eine Datenbank, die für die Berichterstellung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-125">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1b1b4-126">Inhalts </strong> Ordner</span><span class="sxs-lookup"><span data-stu-id="1b1b4-126">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-127">Gibt den Speicherort der Application Virtualization-Pakete für Streaming an.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-127">Indicates the location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-128">Dieser Ordner kann sich auf einer Freigabe auf dem Application Virtualization-Verwaltungs Server befinden.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-128">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1b1b4-129">Microsoft Application Virtualization-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="1b1b4-129">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-130">Diese Konsole ist ein MMC 3,0-Snap-in-Verwaltungstool, das für die Microsoft Application Virtualization Server-Verwaltung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-130">This console is an MMC 3.0 snap-in management tool used for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-131">Dieses Tool kann auf dem Microsoft Application Virtualization Server oder auf einer separaten Workstation mit Microsoft Management Console (MMC) 3.0 und Microsoft installiert werden. NETFramework 2,0 installiert.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-131">This tool can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has Microsoft Management Console (MMC)3.0 and Microsoft .NETFramework 2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1b1b4-132">Microsoft Application Virtualization Management Web Service</span><span class="sxs-lookup"><span data-stu-id="1b1b4-132">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-133">Verantwortlich für die Übermittlung von Lese-und Schreibanforderungen an den Application Virtualization-Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-133">Responsible for communicating any read and write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-134">Der Verwaltungs-Web-Service kann auf dem Microsoft Application Virtualization Management Server oder auf einem separaten Computer installiert werden, auf dem Microsoft Internet Information Services (IIS) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-134">The Management Web Service can be installed on the Microsoft Application Virtualization Management server or on a separate computer that has Microsoft Internet Information Services (IIS) installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1b1b4-135">Microsoft Application Virtualization-Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="1b1b4-135">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-136">Die App-V SQL Server-Datenbank, die für das Speichern aller Informationen im Zusammenhang mit der Application Virtualization-Infrastruktur verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-136">The App-V SQL Server database responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-137">Diese Informationen umfassen alle Anwendungsdatensätze, Anwendungszuordnungen und welche Gruppen für die Verwaltung der Application Virtualization-Umgebung verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-137">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1b1b4-138">Microsoft Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="1b1b4-138">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-139">Verantwortlich für das Hosten der Application Virtualization-Pakete für das Streaming an Clients in einer Zweigstelle, wobei der Link zurück zum Application Virtualization Management Server als WAN-Verbindung (Wide Area Networks) gilt.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-139">Responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a wide area networks (WAN) connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-140">Dieser Server enthält nur Streamingfunktionen und stellt weder die Application Virtualization Management Console noch den Application Virtualization Management Web Service bereit.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-140">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1b1b4-141">Microsoft Application Virtualization-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="1b1b4-141">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-142">Der Sequencer wird verwendet, um die Installation von Anwendungen zur Erstellung virtueller Anwendungspakete zu überwachen und zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-142">The sequencer is used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-143">Die Ausgabe besteht aus den Symbolen der Anwendung, einer OSD-Datei, die Paketdefinitionsinformationen enthält, einer Paket Manifestdatei und der SFT-Datei, die die Inhaltsdateien des Anwendungsprogramms enthält.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-143">The output consists of the application’s icons, an .osd file that contains package definition information, a package manifest file, and the .sft file that contains the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1b1b4-144">Microsoft Application Virtualization-Client</span><span class="sxs-lookup"><span data-stu-id="1b1b4-144">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-145">Der Application Virtualization-Desktop Client und der Application Virtualization-Client für Remote Desktop Dienste bieten und verwalten die virtuelle Umgebung für virtualisierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-145">The Application Virtualization Desktop Client and the Application Virtualization Client for Remote Desktop Services provide and manage the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b1b4-146">Der Microsoft Application Virtualization-Client verwaltet das Paketstreaming in den Zwischenspeicher, Veröffentlichungsaktualisierung, Transport und alle Interaktionen mit den Application Virtualization-Servern.</span><span class="sxs-lookup"><span data-stu-id="1b1b4-146">The Microsoft Application Virtualization client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





