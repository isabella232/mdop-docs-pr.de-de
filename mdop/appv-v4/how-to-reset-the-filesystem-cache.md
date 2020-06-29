---
title: So setzen Sie den Dateisystemcache zurück
description: So setzen Sie den Dateisystemcache zurück
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806816"
---
# <span data-ttu-id="7606b-103">So setzen Sie den Dateisystemcache zurück</span><span class="sxs-lookup"><span data-stu-id="7606b-103">How to Reset the FileSystem Cache</span></span>


<span data-ttu-id="7606b-104">Das Zurücksetzen des Dateisystemcaches sollte in der Regel nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="7606b-104">Resetting the FileSystem cache is not something that should usually be necessary.</span></span> <span data-ttu-id="7606b-105">Wenn Sie den Dateisystemcache allerdings, vielleicht zur Problembehandlung, vollständig zurücksetzen müssen, können Sie das folgende Verfahren verwenden.</span><span class="sxs-lookup"><span data-stu-id="7606b-105">However if you need to completely reset the FileSystem cache, perhaps for troubleshooting purposes, you can use the following procedure.</span></span> <span data-ttu-id="7606b-106">Zum Ausführen dieser Aktion sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7606b-106">Administrative rights are required to perform this action.</span></span>

**<span data-ttu-id="7606b-107">So setzen Sie den Dateisystemcache zurück</span><span class="sxs-lookup"><span data-stu-id="7606b-107">To reset the FileSystem cache</span></span>**

1.  <span data-ttu-id="7606b-108">Setzen Sie den folgenden Registrierungswert auf 0 (null):</span><span class="sxs-lookup"><span data-stu-id="7606b-108">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="7606b-109">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\state</span><span class="sxs-lookup"><span data-stu-id="7606b-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="7606b-110">Starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="7606b-110">Restart the computer.</span></span>

## <span data-ttu-id="7606b-111">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7606b-111">Related topics</span></span>


[<span data-ttu-id="7606b-112">So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="7606b-112">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





