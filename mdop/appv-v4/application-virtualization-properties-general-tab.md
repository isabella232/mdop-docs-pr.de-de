---
title: Registerkarte ' Allgemeine Eigenschaften von Application Virtualization '
description: Registerkarte ' Allgemeine Eigenschaften von Application Virtualization '
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808007"
---
# <span data-ttu-id="065fc-103">Application Virtualization-Eigenschaften: Registerkarte "Allgemein"</span><span class="sxs-lookup"><span data-stu-id="065fc-103">Application Virtualization Properties: General Tab</span></span>


<span data-ttu-id="065fc-104">Verwenden Sie die Registerkarte **Allgemein** im Dialogfeld **Eigenschaften von Application Virtualization** , um Protokolleinstellungen und Datenspeicherorte zu ändern.</span><span class="sxs-lookup"><span data-stu-id="065fc-104">Use the **General** tab of the **Application Virtualization Properties** dialog box to modify log settings and data locations.</span></span>

<span data-ttu-id="065fc-105">Diese Registerkarte enthält die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="065fc-105">This tab contains the following elements.</span></span>

<a href="" id="log-level"></a>**<span data-ttu-id="065fc-106">Protokollebene</span><span class="sxs-lookup"><span data-stu-id="065fc-106">Log Level</span></span>**  
<span data-ttu-id="065fc-107">Wählen Sie die Ebene in der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="065fc-107">Select the level from the drop-down list.</span></span> <span data-ttu-id="065fc-108">Die Standardebene ist " **Informationen**".</span><span class="sxs-lookup"><span data-stu-id="065fc-108">The default level is **Information**.</span></span>

<a href="" id="reset-log"></a>**<span data-ttu-id="065fc-109">Protokoll zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="065fc-109">Reset Log</span></span>**  
<span data-ttu-id="065fc-110">Klicken Sie auf diese Schaltfläche, um die aktuelle Protokolldatei zu sichern und sofort eine neue Protokolldatei zu starten.</span><span class="sxs-lookup"><span data-stu-id="065fc-110">Click this button to back up the current log file and immediately start a new log file.</span></span>

<a href="" id="location"></a>**<span data-ttu-id="065fc-111">Pfad</span><span class="sxs-lookup"><span data-stu-id="065fc-111">Location</span></span>**  
<span data-ttu-id="065fc-112">Geben Sie den Speicherort ein, an dem die Protokolldatei sftlog.txt gespeichert werden soll, oder navigieren Sie zu ihm.</span><span class="sxs-lookup"><span data-stu-id="065fc-112">Enter or browse to the location where you want to save the log file sftlog.txt.</span></span> <span data-ttu-id="065fc-113">Die Standardspeicherorte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="065fc-113">The default locations are as follows:</span></span>

-   <span data-ttu-id="065fc-114">Für WindowsXP, Windows Server2003 –*c:\\Dokumente und Einstellungen\\All Users\\Application Data\\Microsoft\\Application-Virtualisierungs-Client*</span><span class="sxs-lookup"><span data-stu-id="065fc-114">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="065fc-115">Für Windows Vista, Windows 7, Windows Server2008 –*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span><span class="sxs-lookup"><span data-stu-id="065fc-115">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="system-log-level"></a>**<span data-ttu-id="065fc-116">System Protokollebene</span><span class="sxs-lookup"><span data-stu-id="065fc-116">System Log Level</span></span>**  
<span data-ttu-id="065fc-117">Wählen Sie die Ebene in der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="065fc-117">Select the level from the drop-down list.</span></span> <span data-ttu-id="065fc-118">Die Standardstufe ist **Warning**.</span><span class="sxs-lookup"><span data-stu-id="065fc-118">The default level is **Warning**.</span></span>

<span data-ttu-id="065fc-119">**Hinweis**  Die Einstellung **Systemprotokollebene** steuert die Ebene der Nachrichten, die an das Systemereignisprotokoll gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="065fc-119">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="065fc-120">Die protokollierten Nachrichten sind identisch mit den Nachrichten, die im Clientereignisprotokoll protokolliert werden, aber Sie werden an einem anderen Speicherort gespeichert, der nicht die Speicherplatzeinschränkungen des Clientereignisprotokolls aufweist.</span><span class="sxs-lookup"><span data-stu-id="065fc-120">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location that does not have the space limitations of the client event log.</span></span> <span data-ttu-id="065fc-121">Da das Systemereignisprotokoll keine Speicherplatzeinschränkungen aufweist, eignet es sich hervorragend für Situationen, in denen eine ausführliche Protokollierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="065fc-121">Because the system event log does not have space limitations, it is ideally suited for situations where verbose logging is necessary.</span></span>

 

<a href="" id="global-data-directory"></a>**<span data-ttu-id="065fc-122">Globales Datenverzeichnis</span><span class="sxs-lookup"><span data-stu-id="065fc-122">Global Data Directory</span></span>**  
<span data-ttu-id="065fc-123">Geben Sie den Speicherort des Verzeichnisses der Protokolldatei ein, oder suchen Sie nach ihm.</span><span class="sxs-lookup"><span data-stu-id="065fc-123">Enter or browse to the location of the directory of the log file.</span></span> <span data-ttu-id="065fc-124">Die Standardspeicherorte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="065fc-124">The default locations are as follows:</span></span>

-   <span data-ttu-id="065fc-125">Für WindowsXP, Windows Server2003 –*c:\\Dokumente und Einstellungen\\All Users\\Application Data\\Microsoft\\Application-Virtualisierungs-Client*</span><span class="sxs-lookup"><span data-stu-id="065fc-125">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="065fc-126">Für Windows Vista, Windows 7, Windows Server2008 –*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span><span class="sxs-lookup"><span data-stu-id="065fc-126">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="user-data-directory"></a>**<span data-ttu-id="065fc-127">Benutzerdatenverzeichnis</span><span class="sxs-lookup"><span data-stu-id="065fc-127">User Data Directory</span></span>**  
<span data-ttu-id="065fc-128">Geben Sie den Speicherort des Verzeichnisses ein, in dem benutzerspezifische Daten gespeichert sind, oder suchen Sie nach ihm.</span><span class="sxs-lookup"><span data-stu-id="065fc-128">Enter or browse to the location of the directory where user-specific data is stored.</span></span> <span data-ttu-id="065fc-129">Der Standardwert ist% APPDATA%.</span><span class="sxs-lookup"><span data-stu-id="065fc-129">The default is %APPDATA%.</span></span> <span data-ttu-id="065fc-130">Dieser Pfad muss eine gültige Umgebungsvariable auf dem Clientcomputer sein.</span><span class="sxs-lookup"><span data-stu-id="065fc-130">This path must be a valid environment variable on the client computer.</span></span>

## <span data-ttu-id="065fc-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="065fc-131">Related topics</span></span>


[<span data-ttu-id="065fc-132">Client Management Console: Application Virtualization-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="065fc-132">Client Management Console: Application Virtualization Properties</span></span>](client-management-console-application-virtualization-properties.md)

 

 





