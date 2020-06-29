---
title: So erstellen Sie ein zeitlich begrenztes Wiederherstellungsabbild
description: So erstellen Sie ein zeitlich begrenztes Wiederherstellungsabbild
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804373"
---
# <span data-ttu-id="68788-103">So erstellen Sie ein zeitlich begrenztes Wiederherstellungsabbild</span><span class="sxs-lookup"><span data-stu-id="68788-103">How to Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="68788-104">Sie können ein DART-Wiederherstellungsbild erstellen, das nur für eine bestimmte Anzahl von Tagen nach der Generierung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="68788-104">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="68788-105">Dazu müssen Sie den **Dart-Wiederherstellungsbild-Assistenten** an einer Eingabeaufforderung ausführen und die Anzahl der Tage angeben.</span><span class="sxs-lookup"><span data-stu-id="68788-105">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

**<span data-ttu-id="68788-106">So erstellen Sie ein Wiederherstellungsbild mit einem Zeitlimit</span><span class="sxs-lookup"><span data-stu-id="68788-106">To create a recovery image that has a time limit</span></span>**

1.  <span data-ttu-id="68788-107">Öffnen Sie eine Eingabeaufforderung mit Administratoranmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="68788-107">Open a Command Prompt with administrator credentials.</span></span>

2.  <span data-ttu-id="68788-108">Ändern Sie das Verzeichnis in den Speicherort des ERDC.exe-Programms.</span><span class="sxs-lookup"><span data-stu-id="68788-108">Change the directory to the location of the ERDC.exe program.</span></span>

3.  <span data-ttu-id="68788-109">Führen Sie mit der folgenden Syntax den **Dart-Wiederherstellungsbild-Assistenten**aus.</span><span class="sxs-lookup"><span data-stu-id="68788-109">Using the following syntax, run the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="68788-110">*NumberOfDays* ist eine positive ganze Zahl, die die Anzahl der Tage darstellt, für die das DART-Wiederherstellungsbild verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="68788-110">*NumberOfDays* is a positive integer that represents the number of days that the DaRT recovery image will be usable.</span></span>

    ``` syntax
    ERDC /e NumberOfDays
    ```

## <span data-ttu-id="68788-111">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="68788-111">Related topics</span></span>


[<span data-ttu-id="68788-112">Erstellen des DaRT 7.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="68788-112">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





