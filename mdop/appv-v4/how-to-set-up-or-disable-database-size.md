---
title: So richten Sie die Datenbankgröße ein oder deaktivieren Sie sie
description: So richten Sie die Datenbankgröße ein oder deaktivieren Sie sie
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806756"
---
# <span data-ttu-id="a994e-103">So richten Sie die Datenbankgröße ein oder deaktivieren Sie sie</span><span class="sxs-lookup"><span data-stu-id="a994e-103">How to Set Up or Disable Database Size</span></span>


<span data-ttu-id="a994e-104">Mit den folgenden Verfahren können Sie in der Application Virtualization Server-Verwaltungskonsole die Größe (in MB) der Application Virtualization System-Nutzung angeben, die in der Datenbank gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a994e-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the size (in MB) of Application Virtualization System usage that you want to store in the database.</span></span>

<span data-ttu-id="a994e-105">Wenn die Größe der gespeicherten Daten 95% (das höchst Wasserzeichen) des angegebenen Grenzwerts erreicht, löscht das System 10% der Nutzungsdaten, wobei 85% der Daten übrig sind.</span><span class="sxs-lookup"><span data-stu-id="a994e-105">When the size of the stored data reaches 95% (the high watermark) of the specified limit, the system will delete 10% of the usage data, leaving 85% of the data.</span></span> <span data-ttu-id="a994e-106">Paket-und Anwendungs Nutzungsdaten werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a994e-106">Package and application usage data will be deleted.</span></span> <span data-ttu-id="a994e-107">Wenn die Datenbank groß genug ist und sich dem hohen Wasserzeichen nähert, wird eine Warnmeldung an das SQL Server-Protokoll gesendet, um Sie darüber zu informieren, dass dieser Grenzwert erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="a994e-107">When the database grows large enough and approaches the high watermark, a warning message is sent to the SQL Server log to inform you that this limit has been reached.</span></span> <span data-ttu-id="a994e-108">Diese Warnung ist erforderlich, da sich die Bereinigungsaktion auf die Ausgabe der Berichte auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="a994e-108">This warning is necessary because the cleanup action can affect the output of the reports.</span></span> <span data-ttu-id="a994e-109">Darüber hinaus können Sie entscheiden, ob Sie die maximale Datenbankgröße erhöhen, die Anzahl der Monate für die Aufbewahrung der Nutzungsdaten verringern oder den Protokolliergrad reduzieren müssen.</span><span class="sxs-lookup"><span data-stu-id="a994e-109">It will also help you decide whether you need to increase the maximum database size, reduce the number of months of usage data to be kept, or turn down the logging level.</span></span>

<span data-ttu-id="a994e-110">**Hinweis**  Die Optionen " **keine Größe begrenzen** " und " **alle Verwendung beibehalten** " werden bereitgestellt, damit Sie die Verwendungsberichterstattung und die Datenbankbereinigung deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="a994e-110">**Note** The **No Size Limit** and **Keep All Usage** options are provided so that you can disable usage reporting and database cleanup.</span></span> <span data-ttu-id="a994e-111">Durch Auswahl dieser Elemente wird auch das Datenbanktransaktionsprotokoll bereinigt.</span><span class="sxs-lookup"><span data-stu-id="a994e-111">Selecting these items will clean up the database transaction log as well.</span></span> <span data-ttu-id="a994e-112">(Alle übernommenen Microsoft SQL Server-Transaktionen werden aus dem Datenbankprotokoll entfernt.)</span><span class="sxs-lookup"><span data-stu-id="a994e-112">(All committed Microsoft SQL Server transactions will be removed from the database log.)</span></span>

 

**<span data-ttu-id="a994e-113">So richten Sie die Datenbankgröße ein</span><span class="sxs-lookup"><span data-stu-id="a994e-113">To set up database size</span></span>**

1.  <span data-ttu-id="a994e-114">Klicken Sie im linken Bereich mit der rechten Maustaste auf den Knoten Application Virtualization System, und wählen Sie **Systemoptionen**aus.</span><span class="sxs-lookup"><span data-stu-id="a994e-114">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="a994e-115">Wählen Sie die Registerkarte **Datenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="a994e-115">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="a994e-116">Aktivieren Sie das Optionsfeld **maximale Datenbankgröße (MB)** oder **keine Größenbeschränkung** .</span><span class="sxs-lookup"><span data-stu-id="a994e-116">Select the **Maximum Database Size (MB)** or **No Size Limit** radio button.</span></span>

4.  <span data-ttu-id="a994e-117">Wenn Sie sich entscheiden, eine Datenbankgröße anzugeben, empfehlen bewährte Methoden, eine Zahl zwischen 512 und 4096 MB einzugeben.</span><span class="sxs-lookup"><span data-stu-id="a994e-117">If you choose to specify a database size, best practices recommend that you enter a number between 512 and 4096 MB.</span></span> <span data-ttu-id="a994e-118">Die Standardgröße ist 1024 MB, und wenn Sie die Datenbankgröße erhöhen müssen, ist der Maximalwert, den Sie eingeben können, 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="a994e-118">The default size is 1024 MB and if you need to increase the database size, the maximum value you can enter is 2,147,483,647.</span></span> <span data-ttu-id="a994e-119">Wenn Sie **keine Größenbeschränkung**auswählen, wird die Datenbank so lange vergrößert, bis Sie den Grenzwert für die Datenträgergröße erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="a994e-119">If you select **No Size Limit**, the database will grow until it reaches the disk size limit.</span></span>

5.  <span data-ttu-id="a994e-120">Klicken Sie auf über **nehmen** oder **OK**.</span><span class="sxs-lookup"><span data-stu-id="a994e-120">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="a994e-121">So deaktivieren Sie die Größenbeschränkungen für Datenbanken</span><span class="sxs-lookup"><span data-stu-id="a994e-121">To disable database size limits</span></span>**

1.  <span data-ttu-id="a994e-122">Klicken Sie im **Bereich** Bereich mit der rechten Maustaste auf den Knoten Application Virtualization System, und wählen Sie **Systemoptionen**aus.</span><span class="sxs-lookup"><span data-stu-id="a994e-122">Right-click the Application Virtualization System node in the **Scope** pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="a994e-123">Wählen Sie die Registerkarte **Datenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="a994e-123">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="a994e-124">Wählen Sie die Optionsfelder **keine Größenbeschränkung** und **alle Verwendung beibehalten** aus.</span><span class="sxs-lookup"><span data-stu-id="a994e-124">Select the **No Size Limit** and **Keep All Usage** radio buttons.</span></span>

4.  <span data-ttu-id="a994e-125">Klicken Sie auf über **nehmen** oder **OK**.</span><span class="sxs-lookup"><span data-stu-id="a994e-125">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="a994e-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a994e-126">Related topics</span></span>


[<span data-ttu-id="a994e-127">So passen Sie ein Application Virtualization System in der Server Management Console an</span><span class="sxs-lookup"><span data-stu-id="a994e-127">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="a994e-128">So richten Sie die Verwendungsberichterstellung ein oder deaktivieren Sie sie</span><span class="sxs-lookup"><span data-stu-id="a994e-128">How to Set Up or Disable Usage Reporting</span></span>](how-to-set-up-or-disable-usage-reporting.md)

 

 





