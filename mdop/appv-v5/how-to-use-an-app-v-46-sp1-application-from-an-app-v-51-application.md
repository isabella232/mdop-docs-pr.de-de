---
title: Verwenden einer APP-v 4,6-Anwendung aus einer APP-v 5,1-Anwendung
description: Verwenden einer APP-v 4,6-Anwendung aus einer APP-v 5,1-Anwendung
author: dansimp
ms.assetid: 909b4391-762b-4988-b0cf-32b67f1fcf0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: c0d308dcae33b02c089c101ffcd5041b2e665f59
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805126"
---
# <span data-ttu-id="e4fc2-103">Verwenden einer APP-v 4,6-Anwendung aus einer APP-v 5,1-Anwendung</span><span class="sxs-lookup"><span data-stu-id="e4fc2-103">How to Use an App-V 4.6 Application From an App-V 5.1 Application</span></span>

<span data-ttu-id="e4fc2-104">*Hinweis:*\* App-V 4,6 hat den Mainstream-Support verlassen.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="e4fc2-105">Das folgende gilt für ein App-V 4,6 SP3-Paket.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-105">The following applies to an App-V 4.6 SP3 package.</span></span>

<span data-ttu-id="e4fc2-106">Gehen Sie wie folgt vor, um eine APP-v 4.6-Anwendung mit App-v 5,1-Anwendungen auf einem eigenständigen Client auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-106">Use the following procedure to run an App-V4.6 application with App-V 5.1 applications on a standalone client.</span></span>

<span data-ttu-id="e4fc2-107">**Hinweis**  Bei diesem Verfahren wird davon ausgegangen, dass Sie die neueste Version von App-V 4,6 ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-107">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>

**<span data-ttu-id="e4fc2-108">So führen Sie Anwendungen auf einem eigenständigen Client aus</span><span class="sxs-lookup"><span data-stu-id="e4fc2-108">To run applications on a standalone client</span></span>**

1.  <span data-ttu-id="e4fc2-109">Wählen Sie in Ihrer Umgebung zwei Anwendungen aus, die von einander geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-109">Select two applications in your environment that can be opened from one another.</span></span> <span data-ttu-id="e4fc2-110">Beispiel: Microsoft Outlook und Adobe Acrobat Reader.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-110">For example, Microsoft Outlook and Adobe Acrobat Reader.</span></span> <span data-ttu-id="e4fc2-111">Sie können auf eine mit Adobe Acrobat erstellte e-Mail-Anlage zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-111">You can access an email attachment created using Adobe Acrobat.</span></span>

2.  <span data-ttu-id="e4fc2-112">Konvertieren Sie die Pakete, oder erstellen Sie ein neues Paket für eine der Anwendungen mit dem App-V 5,1-Format.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-112">Convert the packages, or create a new package for either of the applications using the App-V 5.1 format.</span></span> <span data-ttu-id="e4fc2-113">Weitere Informationen zum Konvertieren von Paketen finden Sie unter [Migrieren von Erweiterungspunkten aus einem App-v 4,6-Paket zu einem konvertierten App-v 5,1-Paket für alle Benutzer auf einem bestimmten Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md) oder zum [Migrieren von Erweiterungspunkten aus einem App-v 4,6-Paket zu app-v 5,1 für einen bestimmten Benutzer](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="e4fc2-113">For more information about converting packages see, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md) or [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span></span>

3.  <span data-ttu-id="e4fc2-114">Hinzufügen und Bereitstellen des Pakets mithilfe der App-V 5,1-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-114">Add and provision the package using the App-V 5.1 management console.</span></span> <span data-ttu-id="e4fc2-115">Weitere Informationen zum Hinzufügen und Bereitstellen von Paketen finden Sie unter [Hinzufügen oder Aktualisieren von Paketen mithilfe der Verwaltungskonsole](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) und [Konfigurieren des Zugriffs auf Pakete mithilfe der Verwaltungskonsole](how-to-configure-access-to-packages-by-using-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="e4fc2-115">For more information adding and provisioning packages see, [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) and [How to Configure Access to Packages by Using the Management Console](how-to-configure-access-to-packages-by-using-the-management-console-51.md).</span></span>

4.  <span data-ttu-id="e4fc2-116">Die konvertierte Anwendung wird jetzt mit App-V 5,1 ausgeführt, und Sie können eine Anwendung von der anderen öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-116">The converted application now runs using App-V 5.1 and you can open one application from the other.</span></span> <span data-ttu-id="e4fc2-117">Wenn Sie beispielsweise ein Microsoft Office-Paket in ein App-v 5,1-Paket konvertiert haben und Adobe Acrobat weiterhin als App-v 4.6-Paket ausgeführt wird, können Sie eine Adobe Acrobat Reader-Anlage mit Microsoft Outlook öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-117">For example, if you converted a Microsoft Office package to an App-V 5.1 package and Adobe Acrobat is still running as an App-V4.6 package, you can open an Adobe Acrobat Reader attachment using Microsoft Outlook.</span></span>

    <span data-ttu-id="e4fc2-118">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="e4fc2-118">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="e4fc2-119">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="e4fc2-119">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="e4fc2-120">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="e4fc2-120">Got an App-V issue?</span></span>** <span data-ttu-id="e4fc2-121">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="e4fc2-121">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="e4fc2-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e4fc2-122">Related topics</span></span>


[<span data-ttu-id="e4fc2-123">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e4fc2-123">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





