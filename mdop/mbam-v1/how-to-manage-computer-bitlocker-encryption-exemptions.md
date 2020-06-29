---
title: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Computer
description: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Computer
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811299"
---
# <span data-ttu-id="d1120-103">So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Computer</span><span class="sxs-lookup"><span data-stu-id="d1120-103">How to Manage Computer BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="d1120-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann verwendet werden, um bestimmte Computer vom BitLocker-Schutz zu befreien.</span><span class="sxs-lookup"><span data-stu-id="d1120-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to exempt certain computers from BitLocker protection.</span></span> <span data-ttu-id="d1120-105">Beispielsweise kann eine Organisation beschließen, die BitLocker-Ausnahmeregelung auf Computer-für-Computer-Basis zu steuern.</span><span class="sxs-lookup"><span data-stu-id="d1120-105">For example, an organization may decide to control BitLocker exemption on a computer-by-computer basis.</span></span>

<span data-ttu-id="d1120-106">Wenn Sie einen Computer von der BitLocker-Verschlüsselung ausschließen möchten, müssen Sie den Computer zu einer Sicherheitsgruppe in ActiveDirectoryDomainServices hinzufügen, um alle computerbasierten BitLocker-Schutzregeln zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="d1120-106">To exempt a computer from BitLocker encryption, you must add the computer to a security group in ActiveDirectoryDomainServices in order to bypass any computer-based BitLocker protection rules.</span></span>

<span data-ttu-id="d1120-107">**Hinweis**  Wenn der Computer bereits mit BitLocker geschützt ist, hat die Richtlinie für den Computer Ausschluss keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="d1120-107">**Note** If the computer is already BitLocker-protected, the computer exemption policy has no effect.</span></span>

 

**<span data-ttu-id="d1120-108">So nehmen Sie einen Computer von der BitLocker-Verschlüsselung frei</span><span class="sxs-lookup"><span data-stu-id="d1120-108">To exempt a computer from BitLocker encryption</span></span>**

1.  <span data-ttu-id="d1120-109">Fügen Sie in ActiveDirectoryDomainServices das Computerkonto hinzu, das für eine Sicherheitsgruppe freigestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1120-109">Add the computer account that you want to be exempted to a security group in ActiveDirectoryDomainServices.</span></span> <span data-ttu-id="d1120-110">Auf diese Weise können Sie alle computerbasierten BitLocker-Schutzregeln umgehen.</span><span class="sxs-lookup"><span data-stu-id="d1120-110">This allows you to bypass any computer-based BitLocker protection rules.</span></span>

2.  <span data-ttu-id="d1120-111">Erstellen Sie ein Gruppenrichtlinienobjekt mithilfe der MBAM-Gruppenrichtlinienvorlage, und ordnen Sie dann das Gruppenrichtlinienobjekt der Active Directory-Gruppe zu, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="d1120-111">Create a Group Policy Object by using the MBAM Group Policy template, then associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="d1120-112">Weitere Informationen zum Erstellen der erforderlichen Gruppenrichtlinienobjekte finden Sie unter [Bereitstellen von MBAM 1,0-Gruppenrichtlinienobjekten](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d1120-112">For more information about creating the necessary Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

3.  <span data-ttu-id="d1120-113">Wenn ein ausgenommener Computer gestartet wird, überprüft der MBAM-Client die Einstellungen für die Computer Freistellungs Richtlinie und unterbricht den Schutz, je nachdem, ob der Computer Bestandteil der BitLocker-Ausnahme Sicherheitsgruppe ist.</span><span class="sxs-lookup"><span data-stu-id="d1120-113">When an exempted computer starts, the MBAM client checks the Computer Exemption Policy setting and suspends protection based on whether the computer is part of the BitLocker exemption security group.</span></span>

## <span data-ttu-id="d1120-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d1120-114">Related topics</span></span>


[<span data-ttu-id="d1120-115">Verwalten von MBAM 1.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d1120-115">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





