---
title: So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung
description: So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807080"
---
# <span data-ttu-id="0614b-103">So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung</span><span class="sxs-lookup"><span data-stu-id="0614b-103">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>


<span data-ttu-id="0614b-104">Die Standardinstallation der App-V-Verwaltungskonsole umfasst Unterstützung für die sichere Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="0614b-104">The default installation of the App-V Management Console includes support for secure communications.</span></span> <span data-ttu-id="0614b-105">Jede Verwaltungskonsole wird für einzelne Verbindungen konfiguriert, wenn die Konsole zum ersten Mal gestartet wird oder wenn eine Verbindung mit einem zusätzlichen App-V Web Management-Dienst hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0614b-105">Each Management Console is configured on a per-connection basis when the console is started for the first time or when connecting to an additional App-V Web Management Service.</span></span> <span data-ttu-id="0614b-106">Die Standardkonfiguration verwendet SSL über TCP-Port 443.</span><span class="sxs-lookup"><span data-stu-id="0614b-106">The default configuration uses SSL over TCP port 443.</span></span> <span data-ttu-id="0614b-107">Sie können die Portnummer ändern, wenn die Portnummer auf dem Server geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0614b-107">You can change the port number if the port number was modified on the server.</span></span> <span data-ttu-id="0614b-108">Mithilfe der folgenden Vorgehensweise können Sie eine Verbindung mit einem App-V Web Management-Dienst mithilfe einer sicheren Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="0614b-108">You can use the following procedure to connect to an App-V Web Management Service by using a secure connection.</span></span>

**<span data-ttu-id="0614b-109">Herstellen einer Verbindung zu einem App-V-Verwaltungsdienst mithilfe einer SSL-Verbindung</span><span class="sxs-lookup"><span data-stu-id="0614b-109">How to Connect to an App-V Management Service by Using an SSL Connection</span></span>**

1.  <span data-ttu-id="0614b-110">Starten Sie die Application Virtualization-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="0614b-110">Start the Application Virtualization Management Console.</span></span>

2.  <span data-ttu-id="0614b-111">Klicken Sie im Bereich Aktionen der Konsole auf **Verbindung konfigurieren** .</span><span class="sxs-lookup"><span data-stu-id="0614b-111">Click **Configure Connection** in the actions pane of the console.</span></span>

3.  <span data-ttu-id="0614b-112">Geben Sie den **Hostnamen des Webdiensts**ein, und stellen Sie sicher, dass **sichere Verbindung verwenden** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="0614b-112">Type the **Web Service Host Name**, and ensure that **Use Secure Connection** is selected.</span></span>

    <span data-ttu-id="0614b-113">**Wichtig**  Der im Hostnamen des Webdiensts angegebene Name muss mit dem allgemeinen Namen im Zertifikat übereinstimmen, oder die Verbindung schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="0614b-113">**Important** The name provided in the Web Service Host Name must match the common name on the certificate, or the connection will fail.</span></span>

     

4.  <span data-ttu-id="0614b-114">Wählen Sie die entsprechenden Anmeldeinformationen aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="0614b-114">Select the appropriate login credentials, and click **OK**.</span></span>

## <span data-ttu-id="0614b-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0614b-115">Related topics</span></span>


[<span data-ttu-id="0614b-116">Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service</span><span class="sxs-lookup"><span data-stu-id="0614b-116">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





