---
title: Protokolldateien für Application Virtualization Sequencer
description: Protokolldateien für Application Virtualization Sequencer
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806619"
---
# <span data-ttu-id="919ef-103">Protokolldateien für Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="919ef-103">Log Files for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="919ef-104">Die Protokolldateien für den Application Virtualization (App-V)-Sequenzer liefern detaillierte Informationen zu Sequenz Anwendungen und können hilfreich sein, wenn Sie die Funktionalität überprüfen oder Probleme behandeln.</span><span class="sxs-lookup"><span data-stu-id="919ef-104">The log files for the Application Virtualization (App-V) Sequencer provide detailed information about sequencing applications, and they can be helpful when you are verifying functionality or when you are troubleshooting issues.</span></span>

<span data-ttu-id="919ef-105">Die folgende Tabelle enthält Informationen zu den Protokolldateien und ihren Standardspeicherorten, die bei Verwendung des Sequencers erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="919ef-105">The following table provides information about the log files and their default locations, which are created when using the Sequencer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="919ef-106">Name der Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="919ef-106">Log File Name</span></span></th>
<th align="left"><span data-ttu-id="919ef-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="919ef-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="919ef-108">sft-seq-log.txt</span><span class="sxs-lookup"><span data-stu-id="919ef-108">sft-seq-log.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="919ef-109">Enthält allgemeine Informationen zur Sequenzierung einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="919ef-109">Provides general information about sequencing an application.</span></span> <span data-ttu-id="919ef-110">Verwenden Sie dieses Protokoll als Ausgangspunkt für die Problembehandlung von Sequencer-Fehlern.</span><span class="sxs-lookup"><span data-stu-id="919ef-110">Use this log as a starting point for troubleshooting Sequencer errors.</span></span></p>
<p><span data-ttu-id="919ef-111">Speicherort der Protokolldatei: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="919ef-111">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="919ef-112">[Vorlage-Tokenwert] App-v 4.6-Protokolldateispeicherort: <em> %windir%\Programme\Gemeinsame Dateien\Microsoft Application Virtualization Sequencer\Logs </em> [Vorlagen Tokenwert]</span><span class="sxs-lookup"><span data-stu-id="919ef-112">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="919ef-113">sftbt.txt</span><span class="sxs-lookup"><span data-stu-id="919ef-113">sftbt.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="919ef-114">Enthält Informationen zu Computerneustart Aufgaben, die während des simulierten Neustarts des Sequencers auftreten.</span><span class="sxs-lookup"><span data-stu-id="919ef-114">Provides information about computer restart tasks that occur during the Sequencer’s simulated restart.</span></span></p>
<p><span data-ttu-id="919ef-115">Speicherort der Protokolldatei: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="919ef-115">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="919ef-116">[Vorlage-Tokenwert] App-v 4.6-Protokolldateispeicherort: <em> %windir%\Programme\Gemeinsame Dateien\Microsoft Application Virtualization Sequencer\Logs </em> [Vorlagen Tokenwert]</span><span class="sxs-lookup"><span data-stu-id="919ef-116">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="919ef-117">SftCallBack.txt</span><span class="sxs-lookup"><span data-stu-id="919ef-117">SftCallBack.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="919ef-118">Bietet allgemeine Informationen zu Prozessen, die während der Sequenzierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="919ef-118">Provides general information about processes used during sequencing.</span></span></p>
<p><span data-ttu-id="919ef-119">Speicherort der Protokolldatei: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="919ef-119">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="919ef-120">[Vorlage-Tokenwert] App-v 4.6-Protokolldateispeicherort: <em> %windir%\Programme\Gemeinsame Dateien\Microsoft Application Virtualization Sequencer\Logs </em> [Vorlagen Tokenwert]</span><span class="sxs-lookup"><span data-stu-id="919ef-120">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="919ef-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="919ef-121">Related topics</span></span>


[<span data-ttu-id="919ef-122">Referenz zu Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="919ef-122">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

 

 





