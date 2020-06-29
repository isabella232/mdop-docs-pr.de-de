---
title: Anwenden von Hotfixes auf MBAM 2,5 SP1
description: Anwenden von Hotfixes auf MBAM 2,5 SP1
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810405"
---
# <span data-ttu-id="b8685-103">Anwenden von Hotfixes auf MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="b8685-103">Applying hotfixes on MBAM 2.5 SP1</span></span>
<span data-ttu-id="b8685-104">In diesem Thema wird das Verfahren zum Anwenden der Hotfixes für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) Server 2,5 SP1 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b8685-104">This topic describes the process for applying the hotfixes for Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>

### <span data-ttu-id="b8685-105">Bevor Sie beginnen, laden Sie den neuesten Hotfix für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) Server 2,5 SP1 herunter.</span><span class="sxs-lookup"><span data-stu-id="b8685-105">Before you begin, download the latest hotfix of Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>
[<span data-ttu-id="b8685-106">Desktop Optimierungspaket</span><span class="sxs-lookup"><span data-stu-id="b8685-106">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> <span data-ttu-id="b8685-107">Weitere Informationen zu den Hotfix-Versionen finden Sie im [MBAM-Versions Diagramm](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span><span class="sxs-lookup"><span data-stu-id="b8685-107">For more information about the hotfix releases, see the [MBAM version chart](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span></span>

#### <span data-ttu-id="b8685-108">Schritte zum Aktualisieren des MBAM-Servers für die vorhandene MBAM-Umgebung</span><span class="sxs-lookup"><span data-stu-id="b8685-108">Steps to update the MBAM Server for existing MBAM environment</span></span> 
1. <span data-ttu-id="b8685-109">Entfernen Sie MBAM Server-Feature (Öffnen Sie dazu das MBAM Server-Konfigurations Tool, und wählen Sie dann Features entfernen) aus.</span><span class="sxs-lookup"><span data-stu-id="b8685-109">Remove MBAM server feature (do this by opening the MBAM Server Configuration Tool, then selecting Remove Features).</span></span>
2. <span data-ttu-id="b8685-110">Entfernen von MDOP-MBAM aus der Systemsteuerung | Programme und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="b8685-110">Remove MDOP MBAM from Control Panel | Programs and Features.</span></span>
3. <span data-ttu-id="b8685-111">Installieren Sie MBAM 2,5 SP1 RTM-Server Komponenten.</span><span class="sxs-lookup"><span data-stu-id="b8685-111">Install MBAM 2.5 SP1 RTM server components.</span></span>
4. <span data-ttu-id="b8685-112">Installieren Sie das neueste MBAM 2,5 SP1-Hotfix-Rollup.</span><span class="sxs-lookup"><span data-stu-id="b8685-112">Install lastest MBAM 2.5 SP1 hotfix rollup.</span></span>
5. <span data-ttu-id="b8685-113">Konfigurieren Sie MBAM-Features mithilfe von MBAM Server Configurator.</span><span class="sxs-lookup"><span data-stu-id="b8685-113">Configure MBAM features using MBAM Server Configurator.</span></span>

#### <span data-ttu-id="b8685-114">Schritte zum Installieren des neuen MBAM 2,5 SP1-Server Hotfixes</span><span class="sxs-lookup"><span data-stu-id="b8685-114">Steps to install the new MBAM 2.5 SP1 server hotfix</span></span>
<span data-ttu-id="b8685-115">Weitere Informationen finden Sie im Dokument für die [Installation von neuen Servern](deploying-the-mbam-25-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="b8685-115">Refer to the document for [new server installation](deploying-the-mbam-25-server-infrastructure.md).</span></span>
