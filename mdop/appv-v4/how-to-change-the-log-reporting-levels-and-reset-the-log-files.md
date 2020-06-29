---
title: So ändern Sie die Protokollberichtsebenen und setzen die Protokolldateien zurück
description: So ändern Sie die Protokollberichtsebenen und setzen die Protokolldateien zurück
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807351"
---
# <span data-ttu-id="dc620-103">So ändern Sie die Protokollberichtsebenen und setzen die Protokolldateien zurück</span><span class="sxs-lookup"><span data-stu-id="dc620-103">How to Change the Log Reporting Levels and Reset the Log Files</span></span>


<span data-ttu-id="dc620-104">Mit dem folgenden Verfahren können Sie die Protokoll Berichterstattungs Ebene über den Knoten **Application Virtualization** in der Application Virtualization-Verwaltungskonsole ändern.</span><span class="sxs-lookup"><span data-stu-id="dc620-104">You can use the following procedure to change the log reporting level from the **Application Virtualization** node in the Application Virtualization Management Console.</span></span> <span data-ttu-id="dc620-105">Wenn die Protokolldatei die maximale Größe erreicht (Standard ist 256 MB), wird ein Reset erzwungen, wenn der nächste Schreibvorgang in das Protokoll erfolgt.</span><span class="sxs-lookup"><span data-stu-id="dc620-105">When the log file reaches the maximum size (default is 256 MB), a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="dc620-106">Bei einem Reset wird eine neue Protokolldatei erstellt, und die alte Datei wird als Sicherung umbenannt.</span><span class="sxs-lookup"><span data-stu-id="dc620-106">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span>

**<span data-ttu-id="dc620-107">So ändern Sie die Protokoll Berichterstattungs Ebene</span><span class="sxs-lookup"><span data-stu-id="dc620-107">To change the log reporting level</span></span>**

1.  <span data-ttu-id="dc620-108">Klicken Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** , und wählen Sie im Popupmenü **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="dc620-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="dc620-109">Wählen Sie auf der Registerkarte **Allgemein** im Dialogfeld **Eigenschaften** in der Dropdownliste **Protokollebene** die gewünschte Protokollebene aus.</span><span class="sxs-lookup"><span data-stu-id="dc620-109">On the **General** tab in the **Properties** dialog box, from the **Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="dc620-110">**Hinweis**  Wenn Sie " **verbose** " als Protokollierungsstufe auswählen, werden die Protokolldateien sehr schnell vergrößert.</span><span class="sxs-lookup"><span data-stu-id="dc620-110">**Note** If you choose **Verbose** as the logging level, the log files will grow large very quickly.</span></span> <span data-ttu-id="dc620-111">Dies kann die Clientleistung hemmen, daher empfiehlt es sich, diese Protokollebene nur zum Diagnostizieren spezifischer Probleme zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc620-111">This might inhibit client performance, so best practice is to use this log level only for diagnosing specific problems.</span></span>

     

3.  <span data-ttu-id="dc620-112">Wählen Sie auf der Registerkarte **Allgemein** im Dialogfeld **Eigenschaften** in der Dropdownliste **System Protokollebene** die gewünschte Protokollebene aus.</span><span class="sxs-lookup"><span data-stu-id="dc620-112">On the **General** tab in the **Properties** dialog box, from the **System Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="dc620-113">**Hinweis**  Die Einstellung **Systemprotokollebene** steuert die Ebene der Nachrichten, die an das Systemereignisprotokoll gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc620-113">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="dc620-114">Die protokollierten Nachrichten sind identisch mit den Nachrichten, die im Clientereignisprotokoll protokolliert werden, aber an einem anderen Speicherort gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="dc620-114">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location.</span></span>

     

4.  <span data-ttu-id="dc620-115">Klicken Sie auf **OK** oder auf über **nehmen** , um die Einstellung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="dc620-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="dc620-116">So setzen Sie die Protokolldatei zurück</span><span class="sxs-lookup"><span data-stu-id="dc620-116">To reset the log file</span></span>**

1.  <span data-ttu-id="dc620-117">Klicken Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** , und wählen Sie im Popupmenü **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="dc620-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="dc620-118">Klicken Sie im Dialogfeld **Eigenschaften** auf der Registerkarte **Allgemein** auf **Protokoll zurücksetzen** , um die aktuelle Protokolldatei zu sichern und sofort eine neue Protokolldatei zu starten.</span><span class="sxs-lookup"><span data-stu-id="dc620-118">On the **General** tab in the **Properties** dialog box, click **Reset Log** to back up the current log file and immediately start a new log file.</span></span> <span data-ttu-id="dc620-119">Die Sicherungsprotokolldateien werden im gleichen Ordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dc620-119">The backup log files are stored in the same folder.</span></span>

3.  <span data-ttu-id="dc620-120">Klicken Sie auf **OK** oder auf über **nehmen** , um die Einstellung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="dc620-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="dc620-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dc620-121">Related topics</span></span>


[<span data-ttu-id="dc620-122">So konfigurieren Sie den Client in der Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="dc620-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[<span data-ttu-id="dc620-123">Benutzerzugriffsberechtigungen in Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="dc620-123">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





