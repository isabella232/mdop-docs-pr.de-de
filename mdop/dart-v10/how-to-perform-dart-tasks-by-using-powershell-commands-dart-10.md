---
title: So führen Sie DaRT-Aufgaben mithilfe von PowerShell-Befehlen durch
description: So führen Sie DaRT-Aufgaben mithilfe von PowerShell-Befehlen durch
author: dansimp
ms.assetid: f5a5c5f9-d667-4c85-9e82-7baf0b2aec6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fdf167ca81281da4e04dae10e34bad6122ec05aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809451"
---
# <span data-ttu-id="3a846-103">So führen Sie DaRT-Aufgaben mithilfe von PowerShell-Befehlen durch</span><span class="sxs-lookup"><span data-stu-id="3a846-103">How to Perform DaRT Tasks by Using PowerShell Commands</span></span>


<span data-ttu-id="3a846-104">Microsoft Diagnostics and Recovery Toolset (Dart) 10 enthält den folgenden Satz von Windows PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="3a846-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 10 provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="3a846-105">Administratoren können diese PowerShell-Cmdlets verwenden, um verschiedene Dart 10-Serveraufgaben über die Eingabeaufforderung und nicht über den Dart-Wiederherstellungsbild-Assistenten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3a846-105">Administrators can use these PowerShell cmdlets to perform various DaRT 10 server tasks from the command prompt rather than from the DaRT Recovery Image wizard.</span></span>

## <span data-ttu-id="3a846-106">So verwalten Sie Dart mithilfe von PowerShell-Befehlen</span><span class="sxs-lookup"><span data-stu-id="3a846-106">To administer DaRT by using PowerShell commands</span></span>


<span data-ttu-id="3a846-107">Verwenden Sie die hier beschriebenen PowerShell-Cmdlets, um Dart zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3a846-107">Use the PowerShell cmdlets described here to administer DaRT.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3a846-108">Name</span><span class="sxs-lookup"><span data-stu-id="3a846-108">Name</span></span></th>
<th align="left"><span data-ttu-id="3a846-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a846-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3a846-110">Kopieren-DartImage</span><span class="sxs-lookup"><span data-stu-id="3a846-110">Copy-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3a846-111">Brennt eine ISO auf eine CD, DVD oder ein USB-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3a846-111">Burns an ISO to a CD, DVD, or USB drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3a846-112">Export-DartImage</span><span class="sxs-lookup"><span data-stu-id="3a846-112">Export-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3a846-113">Ermöglicht die Konvertierung der Quell-WIM-Datei, die ein DART-Bild enthält, in eine ISO-Datei.</span><span class="sxs-lookup"><span data-stu-id="3a846-113">Allows the source WIM file, which contains a DaRT image, to be converted into an ISO file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3a846-114">Neu – DartConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a846-114">New-DartConfiguration</span></span></p></td>
<td align="left"><p><span data-ttu-id="3a846-115">Erstellt ein DART-Konfigurationsobjekt, das zum Anwenden eines Dart-Toolsets auf ein Windows-Abbild erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3a846-115">Creates a DaRT configuration object that is needed to apply a DaRT toolset to a Windows Image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3a846-116">Satz-DartImage</span><span class="sxs-lookup"><span data-stu-id="3a846-116">Set-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3a846-117">Wendet ein DartConfiguration-Objekt auf ein bereitgestelltes Windows-Abbild an.</span><span class="sxs-lookup"><span data-stu-id="3a846-117">Applies a DartConfiguration object to a mounted Windows Image.</span></span> <span data-ttu-id="3a846-118">Dies umfasst das Hinzufügen aller Dateien, Konfigurationen und Paketabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="3a846-118">This includes adding all files, configuration, and package dependencies.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3a846-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3a846-119">Related topics</span></span>


[<span data-ttu-id="3a846-120">Verwalten von DaRT 10 mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="3a846-120">Administering DaRT 10 Using PowerShell</span></span>](administering-dart-10-using-powershell.md)

 

 





