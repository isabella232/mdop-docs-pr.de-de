---
title: So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server
description: So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806943"
---
# <span data-ttu-id="022ac-103">So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server</span><span class="sxs-lookup"><span data-stu-id="022ac-103">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>


<span data-ttu-id="022ac-104">Um eine sicherere App-V-Installation zu unterstützen, können Sie die folgenden Verfahren verwenden, um private Schlüssel in Windows Server2003 oder Windows Server2008 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="022ac-104">To support a more secure App-V installation, you can use the following procedures to modify private keys in either Windows Server2003 or Windows Server2008.</span></span> <span data-ttu-id="022ac-105">Wenn Sie die Berechtigungen für den privaten Schlüssel ändern möchten, können Sie das Windows Server2003 Resource Kit-Tool verwenden `WinHttpCertCfg.exe` .</span><span class="sxs-lookup"><span data-stu-id="022ac-105">To modify the permissions of the private key, you can use the Windows Server2003 Resource Kit tool `WinHttpCertCfg.exe`.</span></span>

<span data-ttu-id="022ac-106">Für Windows Server2003 erfordert das Verfahren, dass ein Zertifikat, das die in diesem Dokument aufgeführten Voraussetzungen erfüllt, auf dem Computer installiert ist, auf dem Sie das App-V-Verwaltungs-oder Streamingserver installieren werden.</span><span class="sxs-lookup"><span data-stu-id="022ac-106">For Windows Server2003, the procedure requires that a certificate that meets the prerequisites listed in this document is installed on the computer or computers on which you will install the App-V Management or Streaming Server.</span></span> <span data-ttu-id="022ac-107">Weitere Informationen zur Verwendung des `WinHttpCertCfg.exe` Tools finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151981> .</span><span class="sxs-lookup"><span data-stu-id="022ac-107">Additional information about using the `WinHttpCertCfg.exe` tool is available at <https://go.microsoft.com/fwlink/?LinkId=151981>.</span></span>

<span data-ttu-id="022ac-108">In Windows Server2008 ist der Vorgang zum Ändern der ACLs für den privaten Schlüssel wesentlich einfacher.</span><span class="sxs-lookup"><span data-stu-id="022ac-108">In Windows Server2008, the process of changing the ACLs on the private key is much simpler.</span></span> <span data-ttu-id="022ac-109">Die Benutzeroberfläche des Zertifikats kann zum Verwalten von Berechtigungen für den privaten Schlüssel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="022ac-109">The certificate’s user interface can be used to manage private key permissions.</span></span>

<span data-ttu-id="022ac-110">**Hinweis**  Der Standardsicherheitskontext ist Netzwerkdienst; Stattdessen kann jedoch ein Domänenkonto verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="022ac-110">**Note** The default security context is Network Service; however, a domain account can be used instead.</span></span>

 

**<span data-ttu-id="022ac-111">So verwalten Sie private Schlüssel in Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="022ac-111">To manage private keys in Windows Server2003</span></span>**

1.  <span data-ttu-id="022ac-112">Geben Sie auf dem Computer, der zum App-V-Verwaltungs-oder Streamingserver wird, in der Eingabeaufforderung den folgenden Befehl ein, um die aktuellen Berechtigungen aufzulisten, die einem bestimmten Zertifikat zugewiesen sind:</span><span class="sxs-lookup"><span data-stu-id="022ac-112">On the computer that will become the App-V Management or Streaming Server, type the following command in a command prompt to list the current permissions assigned to a specific certificate:</span></span>

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  <span data-ttu-id="022ac-113">Ändern Sie bei Bedarf die Berechtigungen des Zertifikats, um Lesezugriff auf den Sicherheitskontext zur Verfügung zu stellen, der für den Verwaltungs-oder Streamingdienst verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="022ac-113">If necessary, modify the permissions of the certificate to provide read access to the security context that will be used for Management or Streaming Service:</span></span>

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  <span data-ttu-id="022ac-114">Überprüfen Sie, ob der Sicherheitskontext ordnungsgemäß hinzugefügt wurde, indem Sie die Berechtigungen für das Zertifikat auflisten:</span><span class="sxs-lookup"><span data-stu-id="022ac-114">Verify that the security context was properly added by listing the permissions on the certificate:</span></span>

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**<span data-ttu-id="022ac-115">So verwalten Sie private Schlüssel in Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="022ac-115">To manage private keys in Windows Server2008</span></span>**

1.  <span data-ttu-id="022ac-116">Erstellen Sie eine Microsoft Management Console (MMC) mit dem *Zertifikate* -Snap-in, das auf den Zertifikatspeicher des *lokalen Computers* ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="022ac-116">Create a Microsoft Management Console (MMC) with the *Certificates* snap-in that targets the *Local Machine* certificate store.</span></span>

2.  <span data-ttu-id="022ac-117">Erweitern Sie die MMC, und wählen Sie **private Schlüssel verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="022ac-117">Expand the MMC and select **Manage Private Keys**.</span></span>

3.  <span data-ttu-id="022ac-118">Fügen Sie auf der Registerkarte **Sicherheit** das **Netzwerkdienst** Konto mit **Lese** Zugriff hinzu.</span><span class="sxs-lookup"><span data-stu-id="022ac-118">On the **Security** tab, add the **Network Service** account with **Read** access.</span></span>

## <span data-ttu-id="022ac-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="022ac-119">Related topics</span></span>


[<span data-ttu-id="022ac-120">Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server</span><span class="sxs-lookup"><span data-stu-id="022ac-120">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[<span data-ttu-id="022ac-121">Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming</span><span class="sxs-lookup"><span data-stu-id="022ac-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

 

 





