---
title: Behandeln von Problemen mit Zertifikatberechtigungen
description: Behandeln von Problemen mit Zertifikatberechtigungen
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806215"
---
# <span data-ttu-id="017c9-103">Behandeln von Problemen mit Zertifikatberechtigungen</span><span class="sxs-lookup"><span data-stu-id="017c9-103">Troubleshooting Certificate Permission Issues</span></span>


<span data-ttu-id="017c9-104">Wenn der private Schlüssel nach der Installation von App-v 4.5 nicht mit der richtigen Zugriffssteuerungsliste für den Netzwerkdienst konfiguriert wurde, wird ein Ereignis im NT-Ereignisprotokoll protokolliert, und es wird ein Eintrag in der `Sft-server.log` Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="017c9-104">After the installation of App-V4.5, if the private key has not been configured with the proper ACL for the Network Service, an event is logged in the NT Event Log and an entry is placed in the `Sft-server.log` file.</span></span>

## <span data-ttu-id="017c9-105">Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="017c9-105">Error Messages</span></span>


### <span data-ttu-id="017c9-106">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="017c9-106">Windows Server2003</span></span>

<span data-ttu-id="017c9-107">Ereignis-ID-36870 – es ist ein schwerwiegender Fehler beim Zugriff auf den privaten Schlüssel des SSL-Serveranmeldeinformationen aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="017c9-107">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="017c9-108">Der vom kryptografischen Modul zurückgegebene Fehlercode lautet 0x80090016.</span><span class="sxs-lookup"><span data-stu-id="017c9-108">The error code returned from the cryptographic module is 0x80090016.</span></span>

### <span data-ttu-id="017c9-109">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="017c9-109">Windows Server2008</span></span>

<span data-ttu-id="017c9-110">Ereignis-ID-36870 – es ist ein schwerwiegender Fehler beim Zugriff auf den privaten Schlüssel des SSL-Serveranmeldeinformationen aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="017c9-110">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="017c9-111">Der vom kryptografischen Modul zurückgegebene Fehlercode lautet 0x8009030d.</span><span class="sxs-lookup"><span data-stu-id="017c9-111">The error code returned from the cryptographic module is 0x8009030d.</span></span>

## <span data-ttu-id="017c9-112">SFT-Server. log</span><span class="sxs-lookup"><span data-stu-id="017c9-112">Sft-server.log</span></span>


<span data-ttu-id="017c9-113">Die folgende Fehlermeldung befindet sich in der `sft-server.log` Datei im `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="017c9-113">The following error is placed in the `sft-server.log` file located in the `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` directory:</span></span>

<span data-ttu-id="017c9-114">Das Zertifikat konnte nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="017c9-114">Certificate could not be loaded.</span></span> <span data-ttu-id="017c9-115">Fehlercode \ [-2146893043 \].</span><span class="sxs-lookup"><span data-stu-id="017c9-115">Error code \[-2146893043\].</span></span> <span data-ttu-id="017c9-116">Stellen Sie sicher, dass das Netzwerkdienstkonto über den richtigen Zugriff auf das Zertifikat und die zugehörige private Schlüsseldatei verfügt.</span><span class="sxs-lookup"><span data-stu-id="017c9-116">Make sure that the Network Service account has proper access to the certificate and its corresponding private key file.</span></span>

 

 





