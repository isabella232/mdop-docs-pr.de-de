---
title: Konfigurieren von IIS für sicheres Streaming
description: Konfigurieren von IIS für sicheres Streaming
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809022"
---
# <span data-ttu-id="a6c46-103">Konfigurieren von IIS für sicheres Streaming</span><span class="sxs-lookup"><span data-stu-id="a6c46-103">Configuring IIS for Secure Streaming</span></span>


<span data-ttu-id="a6c46-104">Mit der Veröffentlichung von Microsoft Application Virtualization (app-v), Version 4,5, können Sie http und HTTPS als Protokolle für das Streaming von Anwendungspaketen für die APP-v-Clients verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6c46-104">With the release of Microsoft Application Virtualization (App-V) version 4.5, you can use HTTP and HTTPS as protocols for streaming application packages to the App-V clients.</span></span> <span data-ttu-id="a6c46-105">Mit dieser Option können Organisationen die zusätzliche Skalierbarkeit nutzen, die IIS in der Regel bietet.</span><span class="sxs-lookup"><span data-stu-id="a6c46-105">This option enables organizations to leverage the additional scalability that IIS typically offers.</span></span> <span data-ttu-id="a6c46-106">Wenn Sie IIS als Streamingserver verwenden, können Sie die Kommunikation zwischen dem Client und dem Server mithilfe von HTTPS anstelle von http sichern.</span><span class="sxs-lookup"><span data-stu-id="a6c46-106">When you use IIS as a streaming server, you can help secure the communications between the client and server by using HTTPS instead of HTTP.</span></span>

<span data-ttu-id="a6c46-107">**Hinweis**  Wenn Sie Anwendungen von einem Dateiserver streamen möchten, sollten Sie die Sicherheit der Kommunikation zu den Anwendungspaketen verbessern.</span><span class="sxs-lookup"><span data-stu-id="a6c46-107">**Note** If you want to stream applications from a file server, you should enhance the security of the communications to the application packages.</span></span> <span data-ttu-id="a6c46-108">Dies kann mit IPSec erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="a6c46-108">This can be achieved using IPsec.</span></span> <span data-ttu-id="a6c46-109">Weitere Informationen finden Sie in den folgenden Themen in der TechNet-Bibliothek:</span><span class="sxs-lookup"><span data-stu-id="a6c46-109">For more information see the following topics in the TechNet Library:</span></span>

-   <span data-ttu-id="a6c46-110">Für Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="a6c46-110">For Windows Server2003,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133226>

-   <span data-ttu-id="a6c46-111">Für Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6c46-111">For Windows Server 2008,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## <span data-ttu-id="a6c46-112">MIME-Typen</span><span class="sxs-lookup"><span data-stu-id="a6c46-112">MIME Types</span></span>


<span data-ttu-id="a6c46-113">Wenn Sie IIS zum Streamen virtueller Anwendungen mit http oder HTTPS verwenden, um App-V zu unterstützen, müssen die folgenden MIME-Typen dem IIS-Server hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="a6c46-113">When you use IIS to stream virtual applications with HTTP or HTTPS, to support App-V, the following MIME types must be added to the IIS server:</span></span>

-   <span data-ttu-id="a6c46-114">. OSD = txt</span><span class="sxs-lookup"><span data-stu-id="a6c46-114">.OSD=TXT</span></span>

-   <span data-ttu-id="a6c46-115">. SFT = Binär</span><span class="sxs-lookup"><span data-stu-id="a6c46-115">.SFT=Binary</span></span>

<span data-ttu-id="a6c46-116">Verwenden Sie die folgenden KB-Artikel als Leitfaden für das Hinzufügen von MIME-Typen:</span><span class="sxs-lookup"><span data-stu-id="a6c46-116">Use the following KB articles as guidance for adding MIME types:</span></span>

<span data-ttu-id="a6c46-117">IIS 6,0:</span><span class="sxs-lookup"><span data-stu-id="a6c46-117">IIS 6.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151973>

<span data-ttu-id="a6c46-118">IIS 7,0:</span><span class="sxs-lookup"><span data-stu-id="a6c46-118">IIS 7.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151977>

## <span data-ttu-id="a6c46-119">Kerberos-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a6c46-119">Kerberos Authentication</span></span>


<span data-ttu-id="a6c46-120">Wenn Sie die http-oder HTTPS-und Kerberos-Authentifizierung zum Streamen von ICO-, OSD-oder SFT-Dateien verwenden, verbessern Sie die Sicherheit Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a6c46-120">When you use HTTP or HTTPS and Kerberos authentication to stream ICO, OSD, or SFT files, you are enhancing the security of your environment.</span></span> <span data-ttu-id="a6c46-121">Damit IIS die Kerberos-Authentifizierung unterstützt, müssen Sie jedoch einen richtigen Dienstprinzipalnamen (Service Principal Name, SPN) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a6c46-121">However, for IIS to support Kerberos authentication, you must configure a proper Service Principal Name (SPN).</span></span> <span data-ttu-id="a6c46-122">Das `setspn.exe` Tool ist für Windows Server2003 über die Support Tools auf der Installations-CD verfügbar und in Windows Server2008 integriert.</span><span class="sxs-lookup"><span data-stu-id="a6c46-122">The `setspn.exe` tool is available for Windows Server2003 from the Support Tools on the installation CD and is built-in to Windows Server2008.</span></span>

<span data-ttu-id="a6c46-123">Führen Sie zum Erstellen eines SPN an `setspn.exe` einer Eingabeaufforderung aus, während Sie als Mitglied von Domänenadministratoren angemeldet sind – beispielsweise `setspn.exe –A HTTP/FQDN of Server ServerName` .</span><span class="sxs-lookup"><span data-stu-id="a6c46-123">To create an SPN, run `setspn.exe` from a command prompt while logged in as a member of Domain Administrators—for example, `setspn.exe –A HTTP/FQDN of Server ServerName`.</span></span>

## <span data-ttu-id="a6c46-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a6c46-124">Related topics</span></span>


[<span data-ttu-id="a6c46-125">Konfigurieren von Management oder Streaming Server für die sichere Kommunikation nach der Installation</span><span class="sxs-lookup"><span data-stu-id="a6c46-125">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





