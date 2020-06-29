---
title: Informationen zum Sequenzierungsphasen
description: Informationen zum Sequenzierungsphasen
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808132"
---
# <span data-ttu-id="fc132-103">Informationen zum Sequenzierungsphasen</span><span class="sxs-lookup"><span data-stu-id="fc132-103">About Sequencing Phases</span></span>


<span data-ttu-id="fc132-104">Sequenzierung ist der Vorgang, mit dem Sie ein sequenziertes Anwendungspaket mithilfe von Microsoft Application Virtualization (App-V) Sequencer erstellen.</span><span class="sxs-lookup"><span data-stu-id="fc132-104">Sequencing is the process by which you create a sequenced application package by using the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="fc132-105">Während der Sequenzierung überwacht und zeichnet der Sequencer alle Installations-und Einrichtungsprozesse für eine Anwendung auf und erstellt die folgenden Dateien: ico, OSD, SFT und SPRJ.</span><span class="sxs-lookup"><span data-stu-id="fc132-105">During sequencing, the Sequencer monitors and records all installation and setup processes for an application and creates the following files: ICO, OSD, SFT, and SPRJ.</span></span> <span data-ttu-id="fc132-106">Diese Dateien enthalten alle erforderlichen Informationen zu einer Anwendung und ermöglichen die Ausführung dieser Anwendung in einer virtuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="fc132-106">These files contain all the necessary information about an application, and they allow that application to run in a virtual environment.</span></span>

<span data-ttu-id="fc132-107">Die vier Phasen zur Sequenzierung einer Anwendung und zum Erstellen eines virtuellen Anwendungspakets sind Installation, Start, Anpassung und speichern.</span><span class="sxs-lookup"><span data-stu-id="fc132-107">The four phases to sequencing an application and creating a virtual application package are installation, launch, customization, and save.</span></span> <span data-ttu-id="fc132-108">In der folgenden Liste finden Sie Informationen zu den einzelnen Phasen:</span><span class="sxs-lookup"><span data-stu-id="fc132-108">The following list provides information about each of the phases:</span></span>

1.  <span data-ttu-id="fc132-109">**Installationsphase**: Sie geben während der Installationsphase den Paketnamen und einen optionalen zugehörigen Kommentar an, der dem Paket zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="fc132-109">**Installation phase**—During the installation phase, you specify the package name and an optional associated comment that will be associated with the package.</span></span> <span data-ttu-id="fc132-110">In dieser Phase können Sie auch erweiterte Überwachungsoptionen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fc132-110">You can also configure advanced monitoring options during this phase.</span></span> <span data-ttu-id="fc132-111">Zu den erweiterten Überwachungsoptionen zählen die Angabe der Blockgröße und die Frage, ob automatische Updates während der Überwachung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc132-111">Advanced monitoring options include specifying the block size and whether you will install automatic updates during monitoring.</span></span> <span data-ttu-id="fc132-112">Der Sequencer zeichnet alle erforderlichen Informationen und Konfigurationen auf, die zum Erstellen eines virtuellen Anwendungspakets und der zugehörigen Datei-und Registrierungseinstellungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fc132-112">The sequencer records all necessary information and configurations required to create a virtual application package and the associated file and registry settings.</span></span>

    <span data-ttu-id="fc132-113">**Wichtig**  Wenn Sie die erweiterten Optionen anzeigen möchten, wählen Sie auf der Seite **Paketinformationen** die Option **erweiterte Überwachungsoptionen anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="fc132-113">**Important** To view the advanced options select **Show Advanced Monitoring Options** on the **Package Information** page.</span></span>

     

2.  <span data-ttu-id="fc132-114">**Startphase**: Sie können während der Startphase alle erforderlichen Dateizuordnungen und Sicherheitsbeschreibungen angeben, die mit dem Paket konfiguriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc132-114">**Launch phase**—During the launch phase, you can specify any required file associations and security descriptors that should be configured with the package.</span></span> <span data-ttu-id="fc132-115">Sie sollten die Anwendung so oft wie erforderlich öffnen, um die Funktionalität und Stabilität der Anwendung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="fc132-115">You should open the application as many times as necessary to ensure application functionality and stability.</span></span>

3.  <span data-ttu-id="fc132-116">**Anpassungsphase**: Sie können das Paket während der Anpassungsphase mithilfe der zugehörigen OSD-Dateien konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fc132-116">**Customization phase**—During the customization phase, you can configure your package by using the associated .osd files.</span></span> <span data-ttu-id="fc132-117">Sie können angeben, ob zugeordnete Skripts innerhalb oder außerhalb der virtuellen Umgebung ausgeführt werden sollen, zusätzliche Aktionen angeben, die ausgeführt werden sollen, angeben, wie zugeordnete Skripts (synchron oder asynchron) ausgeführt werden sollen, und zusätzliche Skripts angeben, die im Benutzerkontext ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc132-117">You can specify whether any associated scripts should run inside or outside of the virtual environment, specify additional actions that should be performed, specify how associated scripts run (synchronously or asynchronously), and specify any additional scripts that should be run under the user context.</span></span>

4.  <span data-ttu-id="fc132-118">**Phase speichern**– während der speicherphase werden alle erforderlichen Dateien für das virtuelle Anwendungspaket erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc132-118">**Save phase**—During the save phase, all required files for the virtual application package are created.</span></span> <span data-ttu-id="fc132-119">Die erstellten Dateien sind SPRJ, SFT, OSD, ICO, XML-Manifest und die Windows Installer-Datei (MSI).</span><span class="sxs-lookup"><span data-stu-id="fc132-119">The files created are .sprj, .sft, .osd, .ico, .xml manifest, and the Windows installer (.msi) file.</span></span>

## <span data-ttu-id="fc132-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="fc132-120">Related topics</span></span>


[<span data-ttu-id="fc132-121">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="fc132-121">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





