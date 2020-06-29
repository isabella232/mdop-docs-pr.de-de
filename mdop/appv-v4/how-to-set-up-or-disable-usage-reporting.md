---
title: So richten Sie die Verwendungsberichterstellung ein oder deaktivieren Sie sie
description: So richten Sie die Verwendungsberichterstellung ein oder deaktivieren Sie sie
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806751"
---
# <span data-ttu-id="84092-103">So richten Sie die Verwendungsberichterstellung ein oder deaktivieren Sie sie</span><span class="sxs-lookup"><span data-stu-id="84092-103">How to Set Up or Disable Usage Reporting</span></span>


<span data-ttu-id="84092-104">Sie können die folgenden Verfahren in der Application Virtualization Server-Verwaltungskonsole verwenden, um die Dauer (in Monaten) der Nutzungsinformationen für Application Virtualization System anzugeben, die Sie in der Datenbank speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="84092-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the duration (in months) of Application Virtualization System usage information you want to store in the database.</span></span>

<span data-ttu-id="84092-105">**Hinweis**  Zum Speichern von Nutzungsinformationen müssen Sie auf der Registerkarte **Anbieter Pipeline** das Kontrollkästchen **Verwendungsinformationen protokollieren** aktivieren. Wenn Sie diese Registerkarte anzeigen möchten, klicken Sie im Ergebnisbereich **Anbieterrichtlinien** mit der rechten Maustaste auf die Anbieterrichtlinie, und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="84092-105">**Note** To store usage information, you must select the **Log Usage Information** check box on the **Provider Pipeline** tab. To display this tab, right-click the provider policy in the **Provider Policies Results** pane and select **Properties**.</span></span>

 

**<span data-ttu-id="84092-106">So richten Sie Verwendungsberichte ein</span><span class="sxs-lookup"><span data-stu-id="84092-106">To set up usage reporting</span></span>**

1.  <span data-ttu-id="84092-107">Klicken Sie im linken Bereich mit der rechten Maustaste auf den Knoten Application Virtualization System, und wählen Sie **Systemoptionen**aus.</span><span class="sxs-lookup"><span data-stu-id="84092-107">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="84092-108">Wählen Sie die Registerkarte **Datenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="84092-108">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="84092-109">Aktivieren Sie das Optionsfeld **Nutzung für (Monate)** oder **alle Verwendung** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="84092-109">Select the **Keep Usage For (Months)** or **Keep All Usage** radio button.</span></span>

4.  <span data-ttu-id="84092-110">Wenn Sie die Nutzungsdauer in Monaten angeben möchten, geben Sie eine Zahl von 1 bis 120 ein (Standardwert ist 6 Monate).</span><span class="sxs-lookup"><span data-stu-id="84092-110">If you choose to specify usage duration in months, enter a number from 1 to 120 (default value is 6 months).</span></span> <span data-ttu-id="84092-111">Wenn Sie **alle Verwendung beibehalten**auswählen, wird die Datenbank so lange vergrößert, bis Sie die angegebene Größenbeschränkung erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="84092-111">If you select **Keep All Usage**, the database will grow until it reaches the specified size limit.</span></span>

5.  <span data-ttu-id="84092-112">Klicken Sie auf über **nehmen** oder **OK**.</span><span class="sxs-lookup"><span data-stu-id="84092-112">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="84092-113">So deaktivieren Sie die Verwendungsberichterstattung</span><span class="sxs-lookup"><span data-stu-id="84092-113">To disable usage reporting</span></span>**

1.  <span data-ttu-id="84092-114">Klicken Sie auf den Knoten **Anbieterrichtlinien** .</span><span class="sxs-lookup"><span data-stu-id="84092-114">Click the **Provider Policies** node.</span></span>

2.  <span data-ttu-id="84092-115">Klicken Sie mit der rechten Maustaste auf **Anbieterrichtlinie** , und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="84092-115">Right-click **Provider Policy** and select **Properties**.</span></span>

3.  <span data-ttu-id="84092-116">Wählen Sie die Registerkarte **Anbieter Pipeline** aus.</span><span class="sxs-lookup"><span data-stu-id="84092-116">Select the **Provider Pipeline** tab.</span></span>

4.  <span data-ttu-id="84092-117">Deaktivieren Sie das Kontrollkästchen **Verwendungsinformationen protokollieren** .</span><span class="sxs-lookup"><span data-stu-id="84092-117">Clear the **Log Usage Information** check box.</span></span>

5.  <span data-ttu-id="84092-118">Klicken Sie auf über **nehmen** oder **OK**.</span><span class="sxs-lookup"><span data-stu-id="84092-118">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="84092-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="84092-119">Related topics</span></span>


[<span data-ttu-id="84092-120">So passen Sie ein Application Virtualization System in der Server Management Console an</span><span class="sxs-lookup"><span data-stu-id="84092-120">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="84092-121">So richten Sie die Datenbankgröße ein oder deaktivieren Sie sie</span><span class="sxs-lookup"><span data-stu-id="84092-121">How to Set Up or Disable Database Size</span></span>](how-to-set-up-or-disable-database-size.md)

 

 





