---
title: Konfigurieren der Firewall für App-V Server
description: Konfigurieren der Firewall für App-V Server
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808983"
---
# <span data-ttu-id="aea7d-103">Konfigurieren der Firewall für App-V Server</span><span class="sxs-lookup"><span data-stu-id="aea7d-103">Configuring the Firewall for the App-V Servers</span></span>


<span data-ttu-id="aea7d-104">Nachdem Sie den Microsoft Application Virtualization (App-V)-Verwaltungsserver oder Streamingserver installiert und für die Verwendung des RTSP-oder RTSPS-Protokolls konfiguriert haben, müssen Sie für die APP-v-Programme Firewall-Ausnahmen erstellen.</span><span class="sxs-lookup"><span data-stu-id="aea7d-104">After you install the Microsoft Application Virtualization (App-V) Management Server or Streaming Server and configure it to use the RTSP or RTSPS protocol, you must create firewall exceptions for the App-V programs.</span></span>

## <span data-ttu-id="aea7d-105">Konfigurieren von Firewall-Ausnahmen für Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="aea7d-105">Configuring Firewall Exceptions for Application Virtualization Management Server</span></span>


<span data-ttu-id="aea7d-106">Erstellen Sie eine Firewall-Ausnahme für **sghwdsptr.exe** und **sghwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="aea7d-106">Create a firewall exception for **sghwdsptr.exe** and **sghwsvr.exe**.</span></span> <span data-ttu-id="aea7d-107">Diese Programme finden Sie im Ordner c:\\Programme c:\\Programme\\Microsoft System Center App virt Management Server\\App virt Management Server\\bin auf einem 32-Bit-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="aea7d-107">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="aea7d-108">Wenn Sie eine 64-Bit-Version des Betriebssystems verwenden, befindet sich der Ordner unter c:\\Programme Files (x86) \\Microsoft System Center App virt Management Server\\App virt Management Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="aea7d-108">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.</span></span>

## <span data-ttu-id="aea7d-109">Konfigurieren von Firewall-Ausnahmen für Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="aea7d-109">Configuring Firewall Exceptions for Application Virtualization Streaming Server</span></span>


<span data-ttu-id="aea7d-110">Erstellen Sie eine Firewall-Ausnahme für **sglwdsptr.exe** und **sglwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="aea7d-110">Create a firewall exception for **sglwdsptr.exe** and **sglwsvr.exe**.</span></span> <span data-ttu-id="aea7d-111">Diese Programme finden Sie im Ordner c:\\Programme c:\\Programme\\Microsoft System Center App virt Streaming Server\\App virt-Streaming Server\\bin auf einem 32-Bit-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="aea7d-111">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="aea7d-112">Wenn Sie eine 64-Bit-Betriebssystemversion verwenden, befindet sich der Ordner unter c:\\Programme-Dateien (x86) \\Microsoft System Center-App virt-Streaming Server\\App virt-Streaming Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="aea7d-112">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.</span></span>

## <span data-ttu-id="aea7d-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="aea7d-113">Related topics</span></span>


[<span data-ttu-id="aea7d-114">So konfigurieren Sie Server für die serverbasierte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="aea7d-114">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="aea7d-115">So installieren und konfigurieren Sie die Standardanwendung</span><span class="sxs-lookup"><span data-stu-id="aea7d-115">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)

 

 





