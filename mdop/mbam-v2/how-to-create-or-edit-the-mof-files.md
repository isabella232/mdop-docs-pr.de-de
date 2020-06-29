---
title: So erstellen oder bearbeiten Sie MOF-Dateien
description: So erstellen oder bearbeiten Sie MOF-Dateien
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811086"
---
# <span data-ttu-id="7ad68-103">So erstellen oder bearbeiten Sie MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="7ad68-103">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="7ad68-104">Bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit Configuration Manager installieren, müssen Sie die Datei "Configuration. mof" bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-104">Before you install Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, you need to edit the Configuration.mof file.</span></span> <span data-ttu-id="7ad68-105">Je nachdem, welche Version von Configuration Manager Sie verwenden, müssen Sie auch die SMS \ _def. MOF-Datei bearbeiten oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-105">You also need to either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

## <span data-ttu-id="7ad68-106">Bearbeiten der Datei „Configuration.mof“</span><span class="sxs-lookup"><span data-stu-id="7ad68-106">Edit the Configuration.mof File</span></span>


<span data-ttu-id="7ad68-107">Damit die Clientcomputer BitLocker-Kompatibilitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die Datei "Configuration. mof" für Microsoft System Center Configuration Manager 2007 und SystemCenter2012 ConfigurationManager bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-107">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file for Microsoft System Center Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span>

[<span data-ttu-id="7ad68-108">Bearbeiten der Datei „Configuration.mof“</span><span class="sxs-lookup"><span data-stu-id="7ad68-108">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="7ad68-109">Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei</span><span class="sxs-lookup"><span data-stu-id="7ad68-109">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="7ad68-110">Damit die Clientcomputer BitLocker-Kompatibilitätsdetails in den MBAM-Configuration Manager-Berichten melden können, müssen Sie die SMS \ _def. MOF-Datei erstellen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-110">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="7ad68-111">In Configuration Manager 2007 ist die Datei bereits vorhanden, daher müssen Sie die vorhandene Datei bearbeiten, aber nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="7ad68-111">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span> <span data-ttu-id="7ad68-112">Wenn Sie SystemCenter2012 ConfigurationManager verwenden, müssen Sie die Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-112">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

[<span data-ttu-id="7ad68-113">Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei</span><span class="sxs-lookup"><span data-stu-id="7ad68-113">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file.md)

## <span data-ttu-id="7ad68-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7ad68-114">Related topics</span></span>


[<span data-ttu-id="7ad68-115">Bereitstellen von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="7ad68-115">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





