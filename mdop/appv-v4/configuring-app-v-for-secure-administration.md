---
title: Konfigurieren von App-V für die sichere Verwaltung
description: Konfigurieren von App-V für die sichere Verwaltung
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809034"
---
# <span data-ttu-id="bb927-103">Konfigurieren von App-V für die sichere Verwaltung</span><span class="sxs-lookup"><span data-stu-id="bb927-103">Configuring App-V for Secure Administration</span></span>


<span data-ttu-id="bb927-104">In einer Umgebung, in der es wichtig ist, administrative Vorgänge zu sichern, ermöglicht App-v die sichere Kommunikation zwischen dem App-v-Webverwaltungs Dienst und der APP-v-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="bb927-104">In an environment where securing administrative operations is important, App-V allows for secure communication between the App-V Web Management Service and the App-V Management Console.</span></span> <span data-ttu-id="bb927-105">Da es sich bei dem Verwaltungsdienst um eine webbasierte Anwendung handelt, muss die App-V-Verwaltungs Server Anwendung auf dem Webserver gesichert werden, der den Verwaltungsdienst hostet.</span><span class="sxs-lookup"><span data-stu-id="bb927-105">Because the Management Service is a Web-based application, it requires securing the App-V Management Server application on the Web server that hosts the Management Service.</span></span> <span data-ttu-id="bb927-106">Wie in der folgenden Abbildung dargestellt, umfasst dieser Prozess die Verwendung von HTTPS für die Kommunikation und die Konfiguration des IIS-Servers, um nur die integrierte Windows-Authentifizierung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bb927-106">As shown in the following illustration, this process includes using HTTPS for communication and configuring the IIS server to allow only Windows Integrated Authentication.</span></span>

![App-v Web Service-Netzwerkkonfiguration](images/appvmgmtwebservice.gif)

<span data-ttu-id="bb927-108">Der App-V-Webverwaltungs Dienst wird als webbasierte Anwendung unter IIS installiert.</span><span class="sxs-lookup"><span data-stu-id="bb927-108">The App-V Web Management Service is installed as a Web-based application on IIS.</span></span> <span data-ttu-id="bb927-109">Damit der Webverwaltungs Dienst sichere (SSL-) Verbindungen zwischen der APP-v-Verwaltungskonsole und dem Webverwaltungs Dienst unterstützt, müssen Sie den IIS-Server konfigurieren, auf dem der Webverwaltungs Dienst installiert ist, und die APP-v-Verwaltungskonsole konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bb927-109">For the Web Management Service to support secure (SSL) connections between the App-V Management Console and the Web Management Service, you will need to configure the IIS server where the Web Management Service is installed and configure the App-V Management Console.</span></span>

## <span data-ttu-id="bb927-110">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="bb927-110">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[<span data-ttu-id="bb927-111">Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service</span><span class="sxs-lookup"><span data-stu-id="bb927-111">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)  
<span data-ttu-id="bb927-112">Bietet hilfreiche Informationen zum Konfigurieren von Zertifikaten zur Unterstützung von SSL-basierten Verbindungen, um die Kommunikation für den App-V Web Management Service zu sichern.</span><span class="sxs-lookup"><span data-stu-id="bb927-112">Provides helpful information about configuring certificates to support SSL-based connections, to help secure communication for the App-V Web Management Service.</span></span>

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[<span data-ttu-id="bb927-113">So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung</span><span class="sxs-lookup"><span data-stu-id="bb927-113">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
<span data-ttu-id="bb927-114">Bietet eine schrittweise Anleitung zum Herstellen einer Verbindung mit einem App-V-Webverwaltungs Dienst mithilfe einer sicheren Verbindung.</span><span class="sxs-lookup"><span data-stu-id="bb927-114">Provides a step-by-step procedure for connecting to an App-V Web Management Service by using a secure connection.</span></span>

 

 





