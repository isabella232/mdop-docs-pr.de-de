---
title: So erstellen Sie das Stammverzeichnis des Pakets
description: So erstellen Sie das Stammverzeichnis des Pakets
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807183"
---
# <span data-ttu-id="eb575-103">So erstellen Sie das Stammverzeichnis des Pakets</span><span class="sxs-lookup"><span data-stu-id="eb575-103">How to Create the Package Root Directory</span></span>


<span data-ttu-id="eb575-104">Das Paketstammverzeichnis ist das Verzeichnis auf dem Computer, auf dem der App-V-Sequencer ausgeführt wird, in dem Dateien für die sequenzierte Anwendung installiert sind.</span><span class="sxs-lookup"><span data-stu-id="eb575-104">The package root directory is the directory on the computer running the App-V Sequencer where files for the sequenced application are installed.</span></span> <span data-ttu-id="eb575-105">Dieses Verzeichnis ist auch virtuell auf dem Computer vorhanden, auf den eine sequenzierte Anwendung gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="eb575-105">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span> <span data-ttu-id="eb575-106">Sie sollten das Paketstammverzeichnis erstellen, bevor Sie die Installation einer neuen Anwendung überwachen.</span><span class="sxs-lookup"><span data-stu-id="eb575-106">You should create the package root directory before you monitor the installation of a new application.</span></span>

<span data-ttu-id="eb575-107">Nachdem Sie das Paketstammverzeichnis erstellt haben, können Sie mit der Sequenzierung von Anwendungen beginnen.</span><span class="sxs-lookup"><span data-stu-id="eb575-107">After you have created the package root directory, you can begin sequencing applications.</span></span> <span data-ttu-id="eb575-108">Weitere Informationen zum Sequenzieren einer neuen Anwendung finden Sie unter [so wird es gemacht: Installieren des Sequencers](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="eb575-108">For more information about sequencing a new application, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

**<span data-ttu-id="eb575-109">So erstellen Sie das Paketstammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="eb575-109">To create the package root directory</span></span>**

1.  <span data-ttu-id="eb575-110">Zum Erstellen des Paketstammverzeichnisses ordnen Sie auf dem Computer, auf dem der App-V-Sequencer ausgeführt wird, das Q:\\-Laufwerk dem angegebenen Netzwerkspeicherort zu.</span><span class="sxs-lookup"><span data-stu-id="eb575-110">To create the package root directory, on the computer running the App-V Sequencer, map the Q:\\ drive to the specified network location.</span></span> <span data-ttu-id="eb575-111">Der von Ihnen angegebene Speicherort sollte über genügend Speicherplatz verfügen, um die Anwendung zu speichern, die Sie sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="eb575-111">The location you specify should have sufficient space to save the application you are sequencing.</span></span>

2.  <span data-ttu-id="eb575-112">Wenn Sie ein Verzeichnis erstellen möchten, das Sie für eine neue virtuelle Anwendung verwenden können, erstellen Sie einen Ordner auf dem Q:\\-Laufwerk, und weisen Sie ihm einen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="eb575-112">To create a directory that you can use for a new virtual application, create a folder on the Q:\\ drive and assign it a name.</span></span>

    <span data-ttu-id="eb575-113">**Wichtig**  Der Name, den Sie virtuellen Anwendungsdateien zuweisen, die im Paketstammverzeichnis gespeichert werden, sollte das 8,3-Benennungsformat verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb575-113">**Important** The name you assign to virtual application files that will be saved in the package root directory should use the 8.3 naming format.</span></span> <span data-ttu-id="eb575-114">Die Dateinamen dürfen nicht mehr als 8 Zeichen mit einer Dateinamenerweiterung mit drei Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="eb575-114">The file names should be no longer than 8 characters with a three-character file name extension.</span></span>

     

## <span data-ttu-id="eb575-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="eb575-115">Related topics</span></span>


[<span data-ttu-id="eb575-116">Aufgaben für den Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="eb575-116">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





