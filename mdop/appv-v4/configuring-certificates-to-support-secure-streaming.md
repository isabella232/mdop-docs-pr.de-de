---
title: Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming
description: Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809028"
---
# <span data-ttu-id="2351b-103">Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming</span><span class="sxs-lookup"><span data-stu-id="2351b-103">Configuring Certificates to Support Secure Streaming</span></span>


<span data-ttu-id="2351b-104">Standardmäßig wird der App-V-Dienst unter dem Netzwerkdienstkonto ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2351b-104">By default, the App-V service runs under the Network Service account.</span></span> <span data-ttu-id="2351b-105">Sie können jedoch ein Dienstkonto in den Active Directory-Domänendiensten erstellen und das Netzwerkdienstkonto durch das Active Directory-Domänenkonto ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2351b-105">However, you can create a service account in Active Directory Domain Services and replace the Network Service account with the Active Directory Domain account.</span></span>

<span data-ttu-id="2351b-106">Der Sicherheitskontext, in dem der Dienst ausgeführt wird, ist für die Konfiguration der erweiterten sicheren Kommunikation wichtig.</span><span class="sxs-lookup"><span data-stu-id="2351b-106">The security context under which the service runs is important for configuring enhanced secure communications.</span></span> <span data-ttu-id="2351b-107">Dieser Sicherheitskontext muss über Leseberechtigungen für den privaten Zertifikatschlüssel verfügen.</span><span class="sxs-lookup"><span data-stu-id="2351b-107">This security context must have read permissions for the certificate private key.</span></span> <span data-ttu-id="2351b-108">Wenn eine PKCS \ #10 *Certificate Signing Request* (CSR) für den App-V-Server generiert wird, wird der Windows *Cryptographic Service Provider* aufgerufen und ein privater Schlüssel generiert.</span><span class="sxs-lookup"><span data-stu-id="2351b-108">When a PKCS\#10 *Certificate Signing Request* (CSR) is generated for the App-V server, the Windows *Cryptographic Service Provider* is called and a private key is generated.</span></span> <span data-ttu-id="2351b-109">Der private Schlüssel ist mit den Berechtigungen geschützt, die nur den System-und Administrator Konten zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="2351b-109">The private key is secured with permissions given to the System and Administrator accounts only.</span></span>

<span data-ttu-id="2351b-110">Sie müssen die Zugriffssteuerungslisten (ACLs) für den privaten Schlüssel ändern, damit der App-V-Verwaltungs-oder Streamingserver auf den privaten Schlüssel zugreifen kann, der für eine erfolgreiche TLS-gesicherte Kommunikation erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2351b-110">You must modify the access control lists (ACLs) on the private key to let the App-V Management or Streaming Server access the private key required for successful TLS secured communication.</span></span>

## <span data-ttu-id="2351b-111">Abrufen und Installieren eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="2351b-111">Obtaining and Installing a Certificate</span></span>


<span data-ttu-id="2351b-112">Die Szenarien für das Abrufen und Installieren eines Zertifikats für App-V lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2351b-112">The scenarios for obtaining and installing a certificate for App-V are as follows:</span></span>

-   <span data-ttu-id="2351b-113">Interne Public Key-Infrastruktur (PKI).</span><span class="sxs-lookup"><span data-stu-id="2351b-113">Internal public key infrastructure (PKI).</span></span>

-   <span data-ttu-id="2351b-114">Zertifizierungsstelle (ca) eines Drittanbieters für Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="2351b-114">Third-party certificate issuing certification authority (CA).</span></span>

    <span data-ttu-id="2351b-115">**Hinweis**  Wenn Sie ein Zertifikat von einer Drittanbieter-Zertifizierungsstelle anfordern müssen, befolgen Sie die auf der Website der Zertifizierungsstelle verfügbare Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2351b-115">**Note** If you need to obtain a certificate from a third-party CA, follow the documentation available on that CA’s Web site.</span></span>

     

<span data-ttu-id="2351b-116">Wenn eine PKI-Infrastruktur bereitgestellt wurde, konsultieren Sie die PKI-Administratoren, um ein Zertifikat zu erwerben, das die in diesem Thema beschriebenen Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="2351b-116">If a PKI infrastructure has been deployed, consult with the PKI administrators to acquire a certificate that complies with the requirements described in this topic.</span></span> <span data-ttu-id="2351b-117">Wenn keine PKI-Infrastruktur verfügbar ist, verwenden Sie eine Drittanbieter-Zertifizierungsstelle, um ein gültiges Zertifikat zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2351b-117">If a PKI infrastructure is not available, use a third-party CA to obtain a valid certificate.</span></span>

<span data-ttu-id="2351b-118">Eine Schritt-für-Schritt-Anleitung zum Abrufen und Installieren eines Zertifikats finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151969> .</span><span class="sxs-lookup"><span data-stu-id="2351b-118">For step-by-step guidance for obtaining and installing a certificate, see <https://go.microsoft.com/fwlink/?LinkId=151969>.</span></span>

## <span data-ttu-id="2351b-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2351b-119">Related topics</span></span>


<span data-ttu-id="2351b-120">Konfigurieren von Zertifikaten zur Unterstützung von sicheres Streaming so [Ändern Sie die Berechtigungen privater Schlüssel zur Unterstützung des Verwaltungsservers oder des Streaming Servers](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span><span class="sxs-lookup"><span data-stu-id="2351b-120">Configuring Certificates to Support Secure Streaming [How to Modify Private Key Permissions to Support Management Server or Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span></span>

 

 





