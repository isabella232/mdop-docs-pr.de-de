---
title: Konfigurieren von Management oder Streaming Server für die sichere Kommunikation nach der Installation
description: Konfigurieren von Management oder Streaming Server für die sichere Kommunikation nach der Installation
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809019"
---
# <span data-ttu-id="59bc9-103">Konfigurieren von Management oder Streaming Server für die sichere Kommunikation nach der Installation</span><span class="sxs-lookup"><span data-stu-id="59bc9-103">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>


<span data-ttu-id="59bc9-104">Wenn das richtige Zertifikat vor der Installation des App-v-Verwaltungsservers oder des App-v-Streaming-Servers nicht bereitgestellt wurde, kann App-v nach der ersten Installation für erhöhte Sicherheit konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="59bc9-104">If the proper certificate was not provisioned before the installation of the App-V Management Server or the App-V Streaming Server, App-V can be configured for enhanced security after the initial installation.</span></span> <span data-ttu-id="59bc9-105">Sie können den App-v-Verwaltungs Server über die APP-v-Verwaltungskonsole konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="59bc9-105">You can configure the App-V Management Server through the App-V Management Console.</span></span> <span data-ttu-id="59bc9-106">Der App-V-Streamingserver wird jedoch über die Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="59bc9-106">However, the App-V Streaming Server is managed through the registry.</span></span> <span data-ttu-id="59bc9-107">In beiden Fällen muss das Zertifikat die richtige *Erweiterte Schlüsselverwendung* (EKU) für die Server Authentifizierung enthalten, und der Netzwerkdienst muss über Lesezugriff auf den privaten Schlüssel verfügen.</span><span class="sxs-lookup"><span data-stu-id="59bc9-107">In either case, the certificate must include the proper *extended key usage* (EKU) for Server authentication and the Network Service must have read access to the private key.</span></span>

## <span data-ttu-id="59bc9-108">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="59bc9-108">In This Section</span></span>


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[<span data-ttu-id="59bc9-109">So konfigurieren Sie Management Server Security-Nachinstallation</span><span class="sxs-lookup"><span data-stu-id="59bc9-109">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)  
<span data-ttu-id="59bc9-110">Bietet eine Prozedur, die nach der Installation mithilfe der APP-v-Verwaltungskonsole durchgeführt werden kann, um das Zertifikat hinzuzufügen und den App-v-Verwaltungs Server für erhöhte Sicherheit zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="59bc9-110">Provides a procedure that can be performed post-installation, using the App-V Management Console, to add the certificate and configure the App-V Management Server for enhanced security.</span></span>

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[<span data-ttu-id="59bc9-111">So konfigurieren Sie die Streaming Server Security-Nachinstallation</span><span class="sxs-lookup"><span data-stu-id="59bc9-111">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)  
<span data-ttu-id="59bc9-112">Bietet eine Prozedur, die nach der Installation durchgeführt werden kann, um das Zertifikat hinzuzufügen und den App-V-Streamingserver für erhöhte Sicherheit zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="59bc9-112">Provides a procedure that can be performed post-installation, to add the certificate and configure the App-V Streaming Server for enhanced security.</span></span>

<a href="" id="troubleshooting-certificate-permission-issues"></a>[<span data-ttu-id="59bc9-113">Behandeln von Problemen mit Zertifikatberechtigungen</span><span class="sxs-lookup"><span data-stu-id="59bc9-113">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)  
<span data-ttu-id="59bc9-114">Bietet Anleitungen zur Problembehandlung, wenn der private Schlüssel nicht mit der richtigen ACL für den Netzwerkdienst konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="59bc9-114">Provides troubleshooting guidance for when the private key has not been configured with the proper ACL for the Network Service.</span></span>

 

 





