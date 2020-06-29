---
title: Elemente der OSD-Datei
description: Elemente der OSD-Datei
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806575"
---
# <span data-ttu-id="f199f-103">Elemente der OSD-Datei</span><span class="sxs-lookup"><span data-stu-id="f199f-103">OSD File Elements</span></span>


<span data-ttu-id="f199f-104">Das Sequencer-Installationsverzeichnis enthält eine XML-Schemadatei, **Softricity. xsd**, die die gültige Struktur einer Open Software Descriptor-Datei (OSD) definiert.</span><span class="sxs-lookup"><span data-stu-id="f199f-104">The Sequencer installation directory contains an XML schema file, **Softricity.xsd**, which defines the valid structure of an Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="f199f-105">Im folgenden finden Sie einige der häufiger verwendeten OSD-Elemente.</span><span class="sxs-lookup"><span data-stu-id="f199f-105">Following are some of the more frequently used OSD elements.</span></span>

<a href="" id="softpkg"></a><span data-ttu-id="f199f-106">SOFTPKG</span><span class="sxs-lookup"><span data-stu-id="f199f-106">SOFTPKG</span></span>  
<span data-ttu-id="f199f-107">Das Stammelement der OSD-Datei, die alle Elemente enthält, die das Softwarepaket definieren.</span><span class="sxs-lookup"><span data-stu-id="f199f-107">The root element of the OSD file containing all elements defining the software package.</span></span>

<a href="" id="codebase"></a><span data-ttu-id="f199f-108">CodeBase</span><span class="sxs-lookup"><span data-stu-id="f199f-108">CODEBASE</span></span>  
<span data-ttu-id="f199f-109">Informationen zur SFT-Datei für dieses Paket, einschließlich der Attribute href, filename und GUID.</span><span class="sxs-lookup"><span data-stu-id="f199f-109">Information about the .sft file for this package, including the HREF, FILENAME, and GUID attributes.</span></span> <span data-ttu-id="f199f-110">Sie können das href-Attribut bearbeiten, wenn Sie den Verteilungspunkt dieses bestimmten Pakets ändern.</span><span class="sxs-lookup"><span data-stu-id="f199f-110">You can edit the HREF attribute if you change the distribution point of this particular package.</span></span>

<a href="" id="os"></a><span data-ttu-id="f199f-111">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="f199f-111">OS</span></span>  
<span data-ttu-id="f199f-112">Definiert, auf welchen Betriebssystemen diese Anwendung basierend auf Werten ausgeführt werden kann, die anfangs im Sequenz-Assistenten festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="f199f-112">Defines on what operating systems this application can run based on values that are initially set in the Sequencing Wizard.</span></span> <span data-ttu-id="f199f-113">Dieser Wert kann nur die Werte enthalten, die in **Softricity. xsd**definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f199f-113">This value can contain only the values defined in **Softricity.xsd**.</span></span>

<a href="" id="local-interaction-allowed"></a><span data-ttu-id="f199f-114">lokal \ _INTERACTION \ _ALLOWED</span><span class="sxs-lookup"><span data-stu-id="f199f-114">LOCAL\_INTERACTION\_ALLOWED</span></span>  
<span data-ttu-id="f199f-115">Auf true festgelegt, ermöglicht dies die Erstellung benannter Objekte (Ereignisse, Mutexe, Semaphoren, Dateizuordnungen und Mailslots) und COM-Objekte im globalen Namespace, anstatt innerhalb einer bestimmten virtuellen Umgebung isoliert zu werden, wodurch virtuellen Anwendungen die Interaktion mit den Anwendungen des Hostbetriebssystems ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="f199f-115">Set to TRUE, this enables creation of named objects (events, mutexes, semaphores, file mappings, and mailslots) and COM objects in the global namespace rather than isolated inside a particular virtual environment, which allows virtual applications to interact with the host operating system's applications.</span></span>

<span data-ttu-id="f199f-116">Beispiel: &lt; SOFTPKG- &gt; &lt; Implementierung&gt;</span><span class="sxs-lookup"><span data-stu-id="f199f-116">Example:&lt;SOFTPKG&gt;&lt;IMPLEMENTATION&gt;</span></span>

<span data-ttu-id="f199f-117">&lt;VIRTUALENV- &gt; &lt; Richtlinien&gt;</span><span class="sxs-lookup"><span data-stu-id="f199f-117">&lt;VIRTUALENV&gt;&lt;POLICIES&gt;</span></span>

<span data-ttu-id="f199f-118">&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; true</span><span class="sxs-lookup"><span data-stu-id="f199f-118">&lt;LOCAL\_INTERACTION\_ALLOWED&gt;TRUE</span></span>

<span data-ttu-id="f199f-119">&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;</span><span class="sxs-lookup"><span data-stu-id="f199f-119">&lt;/LOCAL\_INTERACTION\_ALLOWED&gt;</span></span>

<span data-ttu-id="f199f-120">&lt;/Policies &gt; &lt; /VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="f199f-120">&lt;/POLICIES&gt;&lt;/VIRTUALENV&gt;</span></span>

<span data-ttu-id="f199f-121">&lt;/Implementation &gt; &lt; /SOFTPKG&gt;</span><span class="sxs-lookup"><span data-stu-id="f199f-121">&lt;/IMPLEMENTATION&gt;&lt;/SOFTPKG&gt;</span></span>

<a href="" id="dependencies"></a><span data-ttu-id="f199f-122">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="f199f-122">DEPENDENCIES</span></span>  
<span data-ttu-id="f199f-123">Definiert die dynamische Suite-Komposition (Abhängigkeiten von anderen Paketen) mithilfe eines CodeBase-Tags aus einem anderen Paket.</span><span class="sxs-lookup"><span data-stu-id="f199f-123">Defines Dynamic Suite Composition (dependencies on other packages) by using a CODEBASE tag from another package.</span></span>

<span data-ttu-id="f199f-124">Beispiel: &lt; Abhängigkeiten &gt; &lt; CodeBase href = "RTSPS://Server/Package.SFT" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" sysguarddatei = "pkg. 1 \ \ osguard. CP" size = "6572748" Mandatory = "falsch"/ &gt; &lt; /Dependencies&gt;</span><span class="sxs-lookup"><span data-stu-id="f199f-124">Example:&lt;DEPENDENCIES&gt;&lt;CODEBASE HREF="rtsps://server/package.sft" GUID="7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE="pkg.1\\osguard.cp" SIZE="6572748" MANDATORY="FALSE"/&gt;&lt;/DEPENDENCIES&gt;</span></span>

<a href="" id="package-name"></a><span data-ttu-id="f199f-125">Paket Name</span><span class="sxs-lookup"><span data-stu-id="f199f-125">PACKAGE NAME</span></span>  
<span data-ttu-id="f199f-126">Ein allgemeiner Name für das Paket, das in die **Paket Informations** Seite des Sequenz-Assistenten eingegeben wurde, mit der Sie einen einzelnen Namen für eine sequenzierte Anwendung mit mehreren Anwendungen angeben können.</span><span class="sxs-lookup"><span data-stu-id="f199f-126">A common name for the package entered into the Sequencing Wizard **Package Information** page, which enables you to specify a single name used for a sequenced application containing multiple applications.</span></span>

<a href="" id="title"></a><span data-ttu-id="f199f-127">Titel</span><span class="sxs-lookup"><span data-stu-id="f199f-127">TITLE</span></span>  
<span data-ttu-id="f199f-128">Optionaler beschreibender Name der Anwendung, die Sie sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="f199f-128">Optional descriptive name of the application you are sequencing.</span></span>

<a href="" id="abstract"></a><span data-ttu-id="f199f-129">Abstrakt</span><span class="sxs-lookup"><span data-stu-id="f199f-129">ABSTRACT</span></span>  
<span data-ttu-id="f199f-130">Kurzbeschreibung des Softwarepakets, das im Feld " **Kommentare** " auf der **Paket Informations** Seite des Sequenz-Assistenten eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f199f-130">Short description of the software package entered in the **Comments** field in the Sequencing Wizard **Package Information** page.</span></span> <span data-ttu-id="f199f-131">Es empfiehlt sich, Informationen wie das Betriebssystem und die Service Pack-Ebene der Sequencer-Workstation, die Sequencer-Version und den Namen des Sequenzierungs Ingenieurs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f199f-131">A best practice is to specify information such as the operating system and service-pack level of the Sequencer workstation, Sequencer version, and the sequencing engineer’s name.</span></span>

<a href="" id="script"></a><span data-ttu-id="f199f-132">Skript</span><span class="sxs-lookup"><span data-stu-id="f199f-132">SCRIPT</span></span>  
<span data-ttu-id="f199f-133">Definiert bestimmte Skriptereignisse, die beim Starten, Herunterfahren oder Streaming auftreten können.</span><span class="sxs-lookup"><span data-stu-id="f199f-133">Defines specific scripted events to occur during startup, shutdown, or streaming.</span></span>

<a href="" id="mgmt-shortcutlist"></a><span data-ttu-id="f199f-134">Mgmt \ _SHORTCUTLIST</span><span class="sxs-lookup"><span data-stu-id="f199f-134">MGMT\_SHORTCUTLIST</span></span>  
<span data-ttu-id="f199f-135">Liste aller im Assistenten definierten Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="f199f-135">List of all shortcuts defined in the wizard.</span></span>

<a href="" id="mgmt-fileassociations"></a><span data-ttu-id="f199f-136">Mgmt \ _FILEASSOCIATIONS</span><span class="sxs-lookup"><span data-stu-id="f199f-136">MGMT\_FILEASSOCIATIONS</span></span>  
<span data-ttu-id="f199f-137">Liste der im Assistenten angegebenen Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="f199f-137">List of the file types specified in the wizard.</span></span>

## <span data-ttu-id="f199f-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f199f-138">Related topics</span></span>


[<span data-ttu-id="f199f-139">Informationen zur Registerkarte „OSD“</span><span class="sxs-lookup"><span data-stu-id="f199f-139">About the OSD Tab</span></span>](about-the-osd-tab.md)

 

 





