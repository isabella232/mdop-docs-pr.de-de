---
title: So ändern Sie die Cachegröße und Laufwerkbuchstabenangabe
description: So ändern Sie die Cachegröße und Laufwerkbuchstabenangabe
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807347"
---
# <span data-ttu-id="ca839-103">So ändern Sie die Cachegröße und Laufwerkbuchstabenangabe</span><span class="sxs-lookup"><span data-stu-id="ca839-103">How to Change the Cache Size and the Drive Letter Designation</span></span>


<span data-ttu-id="ca839-104">Sie können die Größe des Caches und die Bezeichnung des Laufwerkbuchstabens direkt aus dem **Application Virtualization** -Knoten in der Application Virtualization Client Management Console ändern.</span><span class="sxs-lookup"><span data-stu-id="ca839-104">You can change the cache size and drive letter designation directly from the **Application Virtualization** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="ca839-105">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ca839-105">Note</span></span>**  
<span data-ttu-id="ca839-106">Nachdem die Cachegröße eingestellt wurde, kann Sie nicht verkleinert werden.</span><span class="sxs-lookup"><span data-stu-id="ca839-106">After the cache size has been set, it cannot be made smaller.</span></span>



**<span data-ttu-id="ca839-107">So ändern Sie die Größe des Caches</span><span class="sxs-lookup"><span data-stu-id="ca839-107">To change the cache size</span></span>**

1.  <span data-ttu-id="ca839-108">Klicken Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** , und wählen Sie im Popupmenü **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="ca839-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ca839-109">Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Datei System** aus.</span><span class="sxs-lookup"><span data-stu-id="ca839-109">Select the **File System** tab on the **Properties** dialog box.</span></span> <span data-ttu-id="ca839-110">Klicken Sie im Abschnitt **Client Cache-Konfigurationseinstellungen** auf eines der folgenden Optionsfelder, um auszuwählen, wie der Cachespeicher verwaltet werden soll:</span><span class="sxs-lookup"><span data-stu-id="ca839-110">In the **Client Cache Configuration Settings** section, click one of the following radio buttons to choose how to manage the cache space:</span></span>

    **<span data-ttu-id="ca839-111">Wichtig</span><span class="sxs-lookup"><span data-stu-id="ca839-111">Important</span></span>**  
    <span data-ttu-id="ca839-112">Wenn Sie die Einstellung Speicher **Platz für freien Speicherplatz verwenden** auswählen, wird mit dem eingegebenen Wert die Cachegröße auf die Gesamtgröße des Datenträgers abzüglich der von Ihnen eingegebenen Schwellenwert Nummer für freien Speicherplatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca839-112">If you select the **Use free disk space threshold** setting, the value you enter will set the cache size to the total disk size minus the free disk space threshold number you entered.</span></span> <span data-ttu-id="ca839-113">Wenn Sie dann zur Verwendung der Einstellung **Maximale Cachegröße verwenden** wiederherstellen möchten, müssen Sie eine größere Zahl als die vorhandene Cachegröße angeben.</span><span class="sxs-lookup"><span data-stu-id="ca839-113">If you then want revert to using the **Use maximum cache size** setting, you must specify a larger number than the existing cache size.</span></span> <span data-ttu-id="ca839-114">Andernfalls wird der Fehler "neue Größe muss größer sein als die vorhandene Cachegröße" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ca839-114">Otherwise, the error “New size must be larger than the existing cache size” will appear.</span></span>



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. <span data-ttu-id="ca839-115">Klicken Sie auf **OK** oder auf über **nehmen** , um die Einstellung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ca839-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="ca839-116">So ändern Sie die Bezeichnung des Laufwerkbuchstabens</span><span class="sxs-lookup"><span data-stu-id="ca839-116">To change the drive letter designation</span></span>**

1.  <span data-ttu-id="ca839-117">Klicken Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** , und wählen Sie im Popupmenü **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="ca839-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ca839-118">Wählen Sie auf der Registerkarte **Datei System** im Dialogfeld **Eigenschaften** im Feld **zu verwendender Antrieb** in der Dropdownliste der verfügbaren Laufwerkbuchstaben den gewünschten Laufwerkbuchstaben aus.</span><span class="sxs-lookup"><span data-stu-id="ca839-118">On the **File System** tab in the **Properties** dialog box, in the **Drive to use** field, select the desired drive letter from the drop-down list of available drive letters.</span></span> <span data-ttu-id="ca839-119">Diese Einstellung wird wirksam, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ca839-119">This setting becomes effective when the computer is rebooted.</span></span>

3.  <span data-ttu-id="ca839-120">Klicken Sie auf **OK** oder auf über **nehmen** , um die Einstellung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ca839-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="ca839-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ca839-121">Related topics</span></span>


[<span data-ttu-id="ca839-122">So konfigurieren Sie den Client in der Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="ca839-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









