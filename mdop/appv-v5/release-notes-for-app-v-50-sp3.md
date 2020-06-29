---
title: Versionshinweise für App-V 5.0 SP3
description: Versionshinweise für App-V 5.0 SP3
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804892"
---
# <span data-ttu-id="df14d-103">Versionshinweise für App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="df14d-103">Release Notes for App-V 5.0 SP3</span></span>


<span data-ttu-id="df14d-104">Im folgenden sind bekannte Probleme in Microsoft Application Virtualization (App-V) 5,0 SP3 zu finden.</span><span class="sxs-lookup"><span data-stu-id="df14d-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.0 SP3.</span></span>

## <span data-ttu-id="df14d-105">Server Dateien können nach einer neuen App-V 5,0 SP3-Server Installation nicht gelöscht werden</span><span class="sxs-lookup"><span data-stu-id="df14d-105">Server files fail to get deleted after a new App-V 5.0 SP3 Server installation</span></span>


<span data-ttu-id="df14d-106">Wenn Sie den App-v 5,0 SP1-Server deinstallieren und dann den App-v 5,0 SP3-Server installieren, schlägt die Installation fehl, und die falsche Version des Verwaltungsservers ist installiert.</span><span class="sxs-lookup"><span data-stu-id="df14d-106">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.0 SP3 Server, the installation fails and the wrong version of the Management server is installed.</span></span> <span data-ttu-id="df14d-107">Die folgenden Fehler werden angezeigt:</span><span class="sxs-lookup"><span data-stu-id="df14d-107">The following errors are displayed:</span></span>

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

<span data-ttu-id="df14d-108">Das Problem tritt auf, weil die Server Dateien nicht gelöscht werden, wenn Sie App-v 5,0 SP1 deinstallieren, sodass der Installationsvorgang für die APP-v 5,0 SP3 irrtümlicherweise ein Upgrade statt einer neuen Installation durchführt.</span><span class="sxs-lookup"><span data-stu-id="df14d-108">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the App-V 5.0 SP3 installation process erroneously does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="df14d-109">**Problemumgehung**: Löschen Sie den folgenden Registrierungsschlüssel, bevor Sie mit der Installation von App-V 5,0 SP3 beginnen:</span><span class="sxs-lookup"><span data-stu-id="df14d-109">**Workaround**: Delete the following registry key before you start installing App-V 5.0 SP3:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## <span data-ttu-id="df14d-110">Abfragen von AD DS können dazu führen, dass einige Anwendungen falsch funktionieren</span><span class="sxs-lookup"><span data-stu-id="df14d-110">Querying AD DS can cause some applications to work incorrectly</span></span>


<span data-ttu-id="df14d-111">Wenn Sie aktualisierte Pakete erhalten, indem Sie die Active Directory-Domänendienste nach aktualisierten Gruppenmitgliedschaften Abfragen, kann dies dazu führen, dass einige Anwendungen falsch funktionieren, wenn die Anwendungen vom Zugriffstoken des Benutzers abhängen.</span><span class="sxs-lookup"><span data-stu-id="df14d-111">When you receive updated packages by querying Active Directory Domain Services for updated group memberships, it can cause some applications to work incorrectly if the applications depend on the user’s access token.</span></span> <span data-ttu-id="df14d-112">Darüber hinaus können häufige Gruppen Mitgliedschafts Abfragen dazu führen, dass der Domänencontroller überlastet wird.</span><span class="sxs-lookup"><span data-stu-id="df14d-112">In addition, frequent group membership queries can cause the domain controller to overload.</span></span> <span data-ttu-id="df14d-113">Weitere Informationen zu Benutzerzugriffstoken finden Sie unter [Zugriffstoken](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span><span class="sxs-lookup"><span data-stu-id="df14d-113">For more information about user access tokens, see [Access Tokens](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span></span>

<span data-ttu-id="df14d-114">**Problemumgehung**: warten Sie, bis sich der Benutzer abmeldet und dann wieder anmeldet, bevor Sie eine Abfrage nach aktualisierten Gruppenmitgliedschaften durchführen.</span><span class="sxs-lookup"><span data-stu-id="df14d-114">**Workaround**: Wait until the user logs off and then logs back on before you query for updated group memberships.</span></span> <span data-ttu-id="df14d-115">Verwenden Sie nicht den Registrierungsschlüssel, der im [Hotfix-Paket 2 für Microsoft Application Virtualization 5,0 Service Pack 1](https://support.microsoft.com/kb/2897087)beschrieben ist, um nach aktualisierten Gruppenmitgliedschaften zu suchen.</span><span class="sxs-lookup"><span data-stu-id="df14d-115">Do not use the registry key, described in [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://support.microsoft.com/kb/2897087), to query for updated group memberships.</span></span>






## <span data-ttu-id="df14d-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="df14d-116">Related topics</span></span>


[<span data-ttu-id="df14d-117">Informationen zu App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="df14d-117">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

 

 





