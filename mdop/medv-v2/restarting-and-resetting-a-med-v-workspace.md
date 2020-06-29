---
title: Neu starten und das Zurücksetzen eines MED-V-Arbeitsbereichs
description: Neu starten und das Zurücksetzen eines MED-V-Arbeitsbereichs
author: dansimp
ms.assetid: a959cdb3-a727-47c7-967e-e58f224e74de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48a644c2ed1668f87eb6e1a78521e780e8b783dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811146"
---
# <span data-ttu-id="d401e-103">Neu starten und das Zurücksetzen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d401e-103">Restarting and Resetting a MED-V Workspace</span></span>


<span data-ttu-id="d401e-104">Bei der Problembehandlung kann es manchmal notwendig sein, den MED-V-Arbeitsbereich neu zu starten oder zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d401e-104">During troubleshooting, you may sometimes find it necessary to restart or reset the MED-V workspace.</span></span> <span data-ttu-id="d401e-105">Der Neustart des MED-V-Arbeitsbereichs entspricht im Grunde dem Neustart eines physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="d401e-105">Restarting the MED-V workspace is basically the same as restarting a physical computer.</span></span> <span data-ttu-id="d401e-106">Beim Zurücksetzen des MED-V-Arbeitsbereichs wird die erstmalige Einrichtung erneut durchlaufen, und alle Daten, die auf dem virtuellen Computer gespeichert sind, werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d401e-106">Resetting the MED-V workspace reruns first time setup and deletes all data that is stored in the virtual machine.</span></span> <span data-ttu-id="d401e-107">Da alle gespeicherten Daten gelöscht werden, sollten Sie in der Regel nur den Med-v-Arbeitsbereich zurücksetzen, um die schwerwiegendsten Probleme bei der Problembehandlung zu beheben, oder um einen zuvor funktionierenden Med-v-Arbeitsbereich wieder in einen Arbeitszustand zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d401e-107">Because all stored data is deleted, you typically should only reset the MED-V workspace to resolve the most serious troubleshooting issues, or to restore a previously working MED-V workspace back to a working state.</span></span>

<span data-ttu-id="d401e-108">Informationen zum Öffnen des Med-v-Administrations-Toolkits finden Sie unter [Problembehandlung bei Med-v mit dem Administrations-Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="d401e-108">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

**<span data-ttu-id="d401e-109">Einen MED-V-Arbeitsbereich neu starten</span><span class="sxs-lookup"><span data-stu-id="d401e-109">Restarting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="d401e-110">Klicken Sie im Fenster **Med-v-Administrations-Toolkit** auf **Med-v Workspace neu starten**.</span><span class="sxs-lookup"><span data-stu-id="d401e-110">On the **MED-V Administration Toolkit** window, click **Restart MED-V Workspace**.</span></span> <span data-ttu-id="d401e-111">Ein Dialogfenster wird geöffnet, in dem Sie bestätigen müssen, dass Sie den MED-V-Arbeitsbereich neu starten möchten.</span><span class="sxs-lookup"><span data-stu-id="d401e-111">A dialog window opens in which you must confirm that you want to restart the MED-V workspace.</span></span>

2.  <span data-ttu-id="d401e-112">Klicken Sie auf **neu starten**.</span><span class="sxs-lookup"><span data-stu-id="d401e-112">Click **Restart**.</span></span>

    <span data-ttu-id="d401e-113">Veröffentlichte Anwendungen, die geöffnete oder umgeleitete Websites sind, werden geschlossen, wenn der MED-V-Arbeitsbereich neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d401e-113">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace restarts.</span></span>

**<span data-ttu-id="d401e-114">Zurücksetzen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d401e-114">Resetting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="d401e-115">Klicken Sie im Fenster **Med-v Administration Toolkit** auf **Med-v Workspace zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="d401e-115">On the **MED-V Administration Toolkit** window, click **Reset MED-V Workspace**.</span></span> <span data-ttu-id="d401e-116">Ein Dialogfenster wird geöffnet, in dem Sie bestätigen müssen, dass Sie den MED-V-Arbeitsbereich zurücksetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="d401e-116">A dialog window opens in which you must confirm that you want to reset the MED-V workspace.</span></span>

    <span data-ttu-id="d401e-117">**Warnung**  Wenn Sie den MED-V-Arbeitsbereich zurücksetzen, wird das erstmalige Setup erneut ausgeführt, und die ursprüngliche virtuelle Festplatte wird neu geladen.</span><span class="sxs-lookup"><span data-stu-id="d401e-117">**Warning** Resetting the MED-V workspace causes first time setup to run again, and thus reloads the original virtual hard disk.</span></span> <span data-ttu-id="d401e-118">Alle Daten, die im MED-V-Arbeitsbereich seit der ersten Ausführung von Setup gespeichert sind, werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d401e-118">All data that is stored in the MED-V workspace since first time setup was originally run will be deleted.</span></span>

     

2.  <span data-ttu-id="d401e-119">Klicken Sie auf **Zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="d401e-119">Click **Reset**.</span></span>

    <span data-ttu-id="d401e-120">Veröffentlichte Anwendungen, die geöffnete oder umgeleitete Websites sind, werden geschlossen, wenn der MED-V-Arbeitsbereich zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d401e-120">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace resets.</span></span>

## <span data-ttu-id="d401e-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d401e-121">Related topics</span></span>


[<span data-ttu-id="d401e-122">Anzeigen und Konfigurieren von MED-V-Protokollen</span><span class="sxs-lookup"><span data-stu-id="d401e-122">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)

[<span data-ttu-id="d401e-123">Anzeigen von MED-V-Arbeitsbereichskonfigurationen</span><span class="sxs-lookup"><span data-stu-id="d401e-123">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





