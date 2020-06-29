---
title: Prüfliste für die Installationsnachbereitung von App-V
description: Prüfliste für die Installationsnachbereitung von App-V
author: dansimp
ms.assetid: 74db297e-a744-4287-bcc6-0e096ca8b57a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79728bd2043076b20eb37ba0b1fa6f834a0d94bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808052"
---
# <span data-ttu-id="408f5-103">Prüfliste für die Installationsnachbereitung von App-V</span><span class="sxs-lookup"><span data-stu-id="408f5-103">App-V Postinstallation Checklist</span></span>


<span data-ttu-id="408f5-104">Die folgende Checkliste enthält eine Liste der allgemeinen Elemente, die Sie berücksichtigen sollten, und beschreibt die Schritte, die Sie ausführen sollten, nachdem Sie die Installation des Microsoft Application Virtualization (app-v)-Verwaltungsservers, App-v-Streaming-Servers und des App-v-Desktop Clients abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="408f5-104">The following checklist provides a high-level list of items to consider and outlines the steps you should take after you have completed the installation of the Microsoft Application Virtualization (App-V) Management Server, App-V Streaming Server, and the App-V Desktop Client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="408f5-105">Schritt</span><span class="sxs-lookup"><span data-stu-id="408f5-105">Step</span></span></th>
<th align="left"><span data-ttu-id="408f5-106">Verweis</span><span class="sxs-lookup"><span data-stu-id="408f5-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="408f5-107">Erstellen Sie Firewall-Ausnahmen für den App-V-Verwaltungs Server oder die Streaming Server-Dienste.</span><span class="sxs-lookup"><span data-stu-id="408f5-107">Create firewall exceptions for the App-V Management Server or Streaming Server services.</span></span></p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)"><span data-ttu-id="408f5-108">Konfigurieren der Firewall für App-V Server</span><span class="sxs-lookup"><span data-stu-id="408f5-108">Configuring the Firewall for the App-V Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="408f5-109">Überprüfen Sie, ob das App-V-System ordnungsgemäß funktioniert, indem Sie die Standardanwendung veröffentlichen, streamen und testen.</span><span class="sxs-lookup"><span data-stu-id="408f5-109">Verify that the App-V system is functioning correctly by publishing, streaming, and testing the default application.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)"><span data-ttu-id="408f5-110">So installieren und konfigurieren Sie die Standardanwendung</span><span class="sxs-lookup"><span data-stu-id="408f5-110">How to Install and Configure the Default Application</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="408f5-111">Konfigurieren Sie den App-v-Client so, dass er den App-v-Streamingserver oder einen anderen Server für das Streaming mithilfe der <strong> ApplicationSourceRoot- </strong> , <strong> IconSourceRoot- </strong> und OSDSourceRoot-Einstellungen verwendet <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="408f5-111">Configure the App-V Client to use the App-V Streaming Server or other server for streaming by means of the <strong>ApplicationSourceRoot</strong>, <strong>IconSourceRoot</strong>, and <strong>OSDSourceRoot</strong> settings.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)"><span data-ttu-id="408f5-112">So konfigurieren Sie den Client für den Abruf von Anwendungspaketen</span><span class="sxs-lookup"><span data-stu-id="408f5-112">How to Configure the Client for Application Package Retrieval</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="408f5-113">Sie erfahren, wie Sie die MSI-Dateiversion von sequenzierten Anwendungspaketen für die Offlinebereitstellung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="408f5-113">Understand how to use the .msi file version of sequenced application packages for offline deployment.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)"><span data-ttu-id="408f5-114">So veröffentlichen Sie eine virtuelle Anwendung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="408f5-114">How to Publish a Virtual Application on the Client</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="408f5-115">Optional Konfigurieren Sie die SQL Server-Datenbankspiegelung für die App-V-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="408f5-115">(Optional) Configure SQL Server database mirroring for the App-V database.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)"><span data-ttu-id="408f5-116">So konfigurieren Sie die Unterstützung von Microsoft SQL Server-Spiegelungen für App-V</span><span class="sxs-lookup"><span data-stu-id="408f5-116">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="408f5-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="408f5-117">Related topics</span></span>


[<span data-ttu-id="408f5-118">Bereitstellung und Upgrade von Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="408f5-118">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





