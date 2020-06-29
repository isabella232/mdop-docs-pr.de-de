---
title: Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service
description: Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809025"
---
# <span data-ttu-id="c854d-103">Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service</span><span class="sxs-lookup"><span data-stu-id="c854d-103">Configuring Certificates to Support the App-V Web Management Service</span></span>


<span data-ttu-id="c854d-104">Der App-V-Webverwaltungs Dienst muss so konfiguriert sein, dass SSL-basierte Verbindungen unterstützt werden, um die Kommunikation zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="c854d-104">The App-V Web Management Service must be configured to support SSL-based connections to help secure the communication.</span></span> <span data-ttu-id="c854d-105">Dieser Vorgang setzt voraus, dass der Webserver oder der Computer, auf dem der Verwaltungsdienst installiert ist, über ein Zertifikat verfügt, das für den Dienst oder Computer ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c854d-105">This process requires that the Web server or computer on which the Management Service is installed has a certificate issued to the service or computer.</span></span>

<span data-ttu-id="c854d-106">Die folgenden Szenarien veranschaulichen, wie Sie ein Zertifikat für diesen Zweck erhalten:</span><span class="sxs-lookup"><span data-stu-id="c854d-106">The following scenarios illustrate how to obtain a certificate for this purpose:</span></span>

1.  <span data-ttu-id="c854d-107">Die Infrastruktur des Unternehmens verfügt bereits über eine Public Key-Infrastruktur (PKI), die automatisch Zertifikate für Computer ausgibt.</span><span class="sxs-lookup"><span data-stu-id="c854d-107">The company infrastructure already has a public key infrastructure (PKI) in place that automatically issues certificates to computers.</span></span>

2.  <span data-ttu-id="c854d-108">Die Infrastruktur des Unternehmens verfügt bereits über eine PKI, die jedoch nicht automatisch Zertifikate für Computer ausstellt.</span><span class="sxs-lookup"><span data-stu-id="c854d-108">The company infrastructure already has a PKI in place, although it does not automatically issue certificates to computers.</span></span>

3.  <span data-ttu-id="c854d-109">In der Unternehmensinfrastruktur ist keine PKI vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c854d-109">The company infrastructure has no PKI in place.</span></span>

<span data-ttu-id="c854d-110">In jedem der vorhergehenden Szenarien ist die Methode zum Abrufen eines Zertifikats anders, das Endergebnis ist jedoch identisch.</span><span class="sxs-lookup"><span data-stu-id="c854d-110">In each of the preceding scenarios, the method for obtaining a certificate is different, but the end result is the same.</span></span> <span data-ttu-id="c854d-111">Der Administrator muss der IIS-Standardwebsite ein Zertifikat zuweisen und den App-V Web-Verwaltungsdienst so konfigurieren, dass eine sichere Kommunikation erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c854d-111">The administrator must assign a certificate to the IIS Default Web Site and configure the App-V Web Management Service to require secure communications.</span></span>

<span data-ttu-id="c854d-112">**Wichtig**  Der Name des Zertifikats muss dem Namen des Servers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c854d-112">**Important** The name of the certificate must match the name of the server.</span></span> <span data-ttu-id="c854d-113">Es empfiehlt sich, vollständig qualifizierte Domänennamen (FQDNs) für den allgemeinen Namen des Zertifikats zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c854d-113">It is a best practice to use fully qualified domain names (FQDNs) for the common name of the certificate.</span></span>

 

<span data-ttu-id="c854d-114">App-V kann IIS-Server verwenden, um unterschiedliche Infrastrukturkonfigurationen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c854d-114">App-V can use IIS servers to support different infrastructure configurations.</span></span> <span data-ttu-id="c854d-115">Weitere Informationen zum Konfigurieren von IIS-Servern zur Unterstützung von HTTPS finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151972> .</span><span class="sxs-lookup"><span data-stu-id="c854d-115">For more information about configuring IIS servers to support HTTPS, see <https://go.microsoft.com/fwlink/?LinkId=151972>.</span></span>

## <span data-ttu-id="c854d-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c854d-116">Related topics</span></span>


[<span data-ttu-id="c854d-117">So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung</span><span class="sxs-lookup"><span data-stu-id="c854d-117">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





