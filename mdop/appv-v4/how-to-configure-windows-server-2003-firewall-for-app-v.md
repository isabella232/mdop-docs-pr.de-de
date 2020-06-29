---
title: So konfigurieren Sie Windows Server 2003 Firewall für App-V
description: So konfigurieren Sie Windows Server 2003 Firewall für App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807223"
---
# <span data-ttu-id="452da-103">So konfigurieren Sie Windows Server 2003 Firewall für App-V</span><span class="sxs-lookup"><span data-stu-id="452da-103">How to Configure Windows Server 2003 Firewall for App-V</span></span>


<span data-ttu-id="452da-104">Gehen Sie wie folgt vor, um die Windows Server 2003-Firewall für App-V zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="452da-104">Use the following procedure to configure the WindowsServer 2003 firewall for App-V.</span></span>

**<span data-ttu-id="452da-105">So konfigurieren Sie die Windows Server 2003-Firewall für App-V</span><span class="sxs-lookup"><span data-stu-id="452da-105">To configure WindowsServer 2003 firewall for App-V</span></span>**

1.  <span data-ttu-id="452da-106">Öffnen Sie in der **System**Steuerung die **Windows-Firewall**.</span><span class="sxs-lookup"><span data-stu-id="452da-106">In **Control Panel**, open the **Windows Firewall**.</span></span>

    <span data-ttu-id="452da-107">**Hinweis**  Wenn der Server nicht so konfiguriert ist, dass der Firewalldienst vor diesem Schritt ausgeführt wird, werden Sie aufgefordert, den Firewalldienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="452da-107">**Note** If the server has not been configured to run the firewall service before this step, you will be prompted to start the firewall service.</span></span>

     

2.  <span data-ttu-id="452da-108">Wenn ICO-und OSD-Dateien über SMB veröffentlicht werden, stellen Sie sicher, dass die **Datei-und Druckerfreigabe** auf der Registerkarte **Ausnahmen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="452da-108">If ICO and OSD files are published through SMB, ensure that **File and Printer Sharing** is enabled on the **Exceptions** tab.</span></span>

    <span data-ttu-id="452da-109">**Hinweis**  Wenn ICO-und OSD-Dateien über HTTP/HTTPS auf dem Verwaltungs Server veröffentlicht werden, müssen Sie möglicherweise eine Ausnahme für http oder HTTPS hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="452da-109">**Note** If ICO and OSD files are published through HTTP/HTTPS on the Management Server, you might need to add an exception for HTTP or HTTPS.</span></span> <span data-ttu-id="452da-110">Wenn der IIS-Server, der die ICO-und OSD-Dateien hostet, auf einem Computer gehostet wird, der vom Verwaltungsserver getrennt ist, müssen Sie die Ausnahme diesem Computer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="452da-110">If the IIS server hosting the ICO and OSD files is hosted on a computer separate from the Management Server, you need to add the exception to that computer.</span></span> <span data-ttu-id="452da-111">Um die Leistung zu maximieren, sollten Sie die ICO-und OSD-Dateien auf einem separaten Server vom Verwaltungsserver hosten.</span><span class="sxs-lookup"><span data-stu-id="452da-111">To maximize performance, it is recommended that you host the ICO and OSD files on a separate server from the Management Server.</span></span>

     

3.  <span data-ttu-id="452da-112">Fügen Sie eine Programmausnahme für hinzu `sghwdsptr.exe` , die die ausführbare Verwaltungs Server-Dienstdatei ist.</span><span class="sxs-lookup"><span data-stu-id="452da-112">Add a program exception for `sghwdsptr.exe`, which is the Management Server service executable.</span></span> <span data-ttu-id="452da-113">Der Standardpfad zu dieser ausführbaren Datei ist `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="452da-113">The default path to this executable is `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

    <span data-ttu-id="452da-114">**Hinweis**  Wenn der Verwaltungs Server RTSP für die Kommunikation verwendet, müssen Sie auch eine Programmausnahme für hinzufügen `sghwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="452da-114">**Note** If the Management Server uses RTSP for communication, you must also add a program exception for `sghwsvr.exe`.</span></span>

    <span data-ttu-id="452da-115">Der App-V Streaming-Server erfordert eine Programmausnahme `sglwdsptr.exe` für die RTSPS-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="452da-115">The App-V Streaming Server requires a program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="452da-116">Der App-V-Streamingserver, der RTSP für die Kommunikation verwendet, erfordert auch eine Programmausnahme für `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="452da-116">The App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

     

4.  <span data-ttu-id="452da-117">Stellen Sie sicher, dass der richtige Bereich für jede Ausnahme konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="452da-117">Ensure that the proper scope is configured for each exception.</span></span> <span data-ttu-id="452da-118">Um das Risiko zu verringern, entfernen Sie jeden Computer, und begrenzen Sie die IP-Adressen, auf die der Server antwortet.</span><span class="sxs-lookup"><span data-stu-id="452da-118">To reduce risk, remove any computer and strictly limit the IP addresses to which the server will respond.</span></span>

## <span data-ttu-id="452da-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="452da-119">Related topics</span></span>


[<span data-ttu-id="452da-120">So konfigurieren Sie Windows Server 2008 Firewall für App-V</span><span class="sxs-lookup"><span data-stu-id="452da-120">How to Configure Windows Server 2008 Firewall for App-V</span></span>](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





