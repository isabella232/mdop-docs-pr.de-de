---
title: Informationen zum Verwenden der Sequencer-Befehlszeile
description: Informationen zum Verwenden der Sequencer-Befehlszeile
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808092"
---
# <span data-ttu-id="9e1e4-103">Informationen zum Verwenden der Sequencer-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="9e1e4-103">About Using the Sequencer Command Line</span></span>


<span data-ttu-id="9e1e4-104">Sie können die Befehlszeile verwenden, um sequenzierte Anwendungspakete zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e1e4-104">You can use the command line to create sequenced application packages.</span></span> <span data-ttu-id="9e1e4-105">Die Verwendung der Befehlszeile zum Erstellen virtueller Anwendungen ist in den folgenden Szenarien hilfreich:</span><span class="sxs-lookup"><span data-stu-id="9e1e4-105">Using the command line to create virtual applications is useful in the following scenarios:</span></span>

-   <span data-ttu-id="9e1e4-106">Sie müssen eine große Anzahl von sequenzierten Anwendungspaketen erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e1e4-106">You need to create a large number of sequenced application packages.</span></span>

-   <span data-ttu-id="9e1e4-107">Sie müssen in regelmäßigen Abständen ein sequenziertes Anwendungspaket erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e1e4-107">You need to create a sequenced application package on a recurring basis.</span></span>

<span data-ttu-id="9e1e4-108">**Wichtig**  Die Sequenzierung an der Eingabeaufforderung ermöglicht nur die standardmäßige Sequenzierung.</span><span class="sxs-lookup"><span data-stu-id="9e1e4-108">**Important** Sequencing at the command prompt allows for default sequencing only.</span></span> <span data-ttu-id="9e1e4-109">Wenn Sie die standardmäßigen Sequenz Parameter ändern müssen, müssen Sie entweder ein sequenziertes Anwendungspaket manuell ändern oder die Anwendung neu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="9e1e4-109">If you need to change default sequencing parameters, you must either manually modify a sequenced application package or re-sequence the application.</span></span>

 

<span data-ttu-id="9e1e4-110">Alle nachfolgenden Änderungen an vorhandenen sequenzierten Anwendungspaketen müssen mithilfe des Sequenz-Assistenten erfolgen.</span><span class="sxs-lookup"><span data-stu-id="9e1e4-110">All subsequent modifications to existing sequenced application packages must be made using the sequencing wizard.</span></span>

## <span data-ttu-id="9e1e4-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9e1e4-111">Prerequisites</span></span>


<span data-ttu-id="9e1e4-112">Um eine Anwendung mithilfe der Eingabeaufforderung zu sequenzieren, müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="9e1e4-112">To sequence an application by using the command prompt, the following conditions must be met:</span></span>

-   <span data-ttu-id="9e1e4-113">Die zu sequenzierte Anwendung darf keine Änderungen oder Problemumgehungen erfordern, die außerhalb des Installationsprogramms oder des Windows Installer-Pakets vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="9e1e4-113">The application that is about to be sequenced must not require changes or workarounds made to it outside the installer or Windows Installer package.</span></span>

-   <span data-ttu-id="9e1e4-114">Vor der Sequenzierung müssen Sie eine Liste der Batchdateien zum Erstellen der sequenzierten Anwendungspakete vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="9e1e4-114">Before sequencing, you must prepare a list of batch files for creating the sequenced application packages.</span></span>

-   <span data-ttu-id="9e1e4-115">Weitere Informationen zu den Befehlszeilenparametern finden Sie unter [Befehlszeilenparameter](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9e1e4-115">Review For more information about the command line parameters, see [Command-Line Parameters](command-line-parameters.md).</span></span>

-   <span data-ttu-id="9e1e4-116">Überprüfen Sie die Fehler, die möglicherweise beim Erstellen eines sequenzierten Anwendungspakets über die Befehlszeile angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e1e4-116">Review the errors that might be displayed when creating a sequenced application package by using the command line.</span></span> <span data-ttu-id="9e1e4-117">Weitere Informationen finden Sie unter diese Fehler finden Sie unter [Befehlszeilenfehler](command-line-errors.md).</span><span class="sxs-lookup"><span data-stu-id="9e1e4-117">For more information, see these errors, see [Command-Line Errors](command-line-errors.md).</span></span>

## <span data-ttu-id="9e1e4-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9e1e4-118">Related topics</span></span>


[<span data-ttu-id="9e1e4-119">So verwalten Sie virtuellen Anwendungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="9e1e4-119">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





