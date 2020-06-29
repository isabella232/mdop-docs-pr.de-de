---
title: So ändern Sie die Größe des Dateisystemcaches
description: So ändern Sie die Größe des Dateisystemcaches
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807332"
---
# <span data-ttu-id="4089a-103">So ändern Sie die Größe des Dateisystemcaches</span><span class="sxs-lookup"><span data-stu-id="4089a-103">How to Change the Size of the FileSystem Cache</span></span>


<span data-ttu-id="4089a-104">Sie können die Größe des Dateisystemcaches über die Befehlszeile ändern.</span><span class="sxs-lookup"><span data-stu-id="4089a-104">You can change the size of the FileSystem cache by using the command line.</span></span> <span data-ttu-id="4089a-105">Für diese Aktion ist ein vollständiges Zurücksetzen des Caches erforderlich, und es sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4089a-105">This action requires a complete reset of the cache, and it requires administrative rights.</span></span>

**<span data-ttu-id="4089a-106">So ändern Sie die Größe des Dateisystemcaches</span><span class="sxs-lookup"><span data-stu-id="4089a-106">To change the size of the FileSystem cache</span></span>**

1.  <span data-ttu-id="4089a-107">Setzen Sie den folgenden Registrierungswert auf 0 (null):</span><span class="sxs-lookup"><span data-stu-id="4089a-107">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="4089a-108">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\state</span><span class="sxs-lookup"><span data-stu-id="4089a-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="4089a-109">Setzen Sie den folgenden Registrierungswert auf die maximale Cachegröße in MB, die für die Speicherung der Pakete erforderlich ist, beispielsweise 8192 MB:</span><span class="sxs-lookup"><span data-stu-id="4089a-109">Set the following registry value to the maximum cache size, in MB, that is necessary to hold the packages—for example, 8192 MB:</span></span>

    <span data-ttu-id="4089a-110">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\filesize</span><span class="sxs-lookup"><span data-stu-id="4089a-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span></span>

3.  <span data-ttu-id="4089a-111">Starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="4089a-111">Restart the computer.</span></span>

## <span data-ttu-id="4089a-112">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4089a-112">Related topics</span></span>


[<span data-ttu-id="4089a-113">So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="4089a-113">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





