---
title: So stellen Sie den MBAM-Client über eine Befehlszeile bereit
description: So stellen Sie den MBAM-Client über eine Befehlszeile bereit
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810585"
---
# <span data-ttu-id="536c1-103">So stellen Sie den MBAM-Client über eine Befehlszeile bereit</span><span class="sxs-lookup"><span data-stu-id="536c1-103">How to Deploy the MBAM Client by Using a Command Line</span></span>


<span data-ttu-id="536c1-104">Sie können eine Befehlszeile zum Bereitstellen der Microsoft BitLocker-Client Software für die Verwaltung und Überwachung (MBAM) verwenden.</span><span class="sxs-lookup"><span data-stu-id="536c1-104">You can use a command line to deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software.</span></span>

## <span data-ttu-id="536c1-105">Befehlszeile zum Bereitstellen der MBAM-Client Software</span><span class="sxs-lookup"><span data-stu-id="536c1-105">Command Line to deploy the MBAM Client software</span></span>


<span data-ttu-id="536c1-106">Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um den Endbenutzer-Lizenzvertrag beim Bereitstellen der MBAM-Client Software automatisch zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="536c1-106">Type the following command at the command prompt to automatically accept the end user license agreement when deploying the MBAM Client software.</span></span>

**<span data-ttu-id="536c1-107">MBAMClientSetup.exe/acceptEula = ja</span><span class="sxs-lookup"><span data-stu-id="536c1-107">MBAMClientSetup.exe /acceptEula=Yes</span></span>**

<span data-ttu-id="536c1-108">**Hinweis**  Die Befehlszeilenoptionen **/Ju** und **/JM** werden nicht unterstützt und können nicht zum Installieren der MBAM-Client Software verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="536c1-108">**Note** The **/ju** and **/jm** command-line options are not supported and cannot be used to install the MBAM Client software.</span></span>

 

<span data-ttu-id="536c1-109">Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um das MSP zu extrahieren und zu installieren:</span><span class="sxs-lookup"><span data-stu-id="536c1-109">Type the following command at the command prompt to extract and install the MSP:</span></span>

**<span data-ttu-id="536c1-110">MBAMClientSetup.exe/Extract- &lt; Pfad zum Extrahieren von MSI &gt; /acceptEula = Yes</span><span class="sxs-lookup"><span data-stu-id="536c1-110">MBAMClientSetup.exe /extract &lt;path to extract MSI&gt; /acceptEula=Yes</span></span>**

<span data-ttu-id="536c1-111">Installieren Sie dann die MSI-Installation im Hintergrund, indem Sie den folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="536c1-111">Then, install the MSI silently by running the following command:</span></span>

**<span data-ttu-id="536c1-112">msiexec/i- &lt; Pfad zu extrahierten MSI- &gt; /qb ALLUSERS = 1 REBOOT = ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="536c1-112">msiexec /i &lt;path to extracted MSI&gt; /qb ALLUSERS=1 REBOOT=ReallySuppress</span></span>**

<span data-ttu-id="536c1-113">**Hinweis**  Ab MBAM 2,5 SP1 ist eine separate MSI-Version nicht mehr im MBAM-Produkt enthalten.</span><span class="sxs-lookup"><span data-stu-id="536c1-113">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="536c1-114">Sie können jedoch die MSI-Datei aus der ausführbaren Datei (. exe) extrahieren, die im Lieferumfang des Produkts enthalten ist, nachdem Sie den EULA angenommen haben.</span><span class="sxs-lookup"><span data-stu-id="536c1-114">However, you can extract the MSI from the executable file (.exe) that is included with the product, after accepting the EULA.</span></span>

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a><span data-ttu-id="536c1-115">Optin \ _FOR \ _MICROSOFT \ _UPDATES = 1 Befehlszeilenoption</span><span class="sxs-lookup"><span data-stu-id="536c1-115">OPTIN\_FOR\_MICROSOFT\_UPDATES=1 command-line option</span></span>


<span data-ttu-id="536c1-116">Sie können bei der Clientsoftwareinstallation optional die Befehlszeilenoption angeben `OPTIN_FOR_MICROSOFT_UPDATES=1` , um Microsoft-Updates auf Clientcomputern automatisch zu installieren.</span><span class="sxs-lookup"><span data-stu-id="536c1-116">You can optionally specify the command-line option `OPTIN_FOR_MICROSOFT_UPDATES=1` during the Client software installation to automatically install Microsoft Updates on client computers.</span></span> <span data-ttu-id="536c1-117">Wenn Sie diese Option angeben, wird Microsoft Update automatisch gestartet, und Sie suchen nach verfügbaren Updates, die nach Abschluss der Client Software Installation installiert werden.</span><span class="sxs-lookup"><span data-stu-id="536c1-117">Specifying this option makes Microsoft Update automatically start and search for available updates to install after the Client software installation finishes.</span></span>

<span data-ttu-id="536c1-118">Sie können diese Befehlszeilenoption mit einer der folgenden Installationsmethoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="536c1-118">You can use this command-line option with either of the following installation methods.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="536c1-119">Installieren der MBAM-Client Software mithilfe von</span><span class="sxs-lookup"><span data-stu-id="536c1-119">Install the MBAM Client software by using</span></span></th>
<th align="left"><span data-ttu-id="536c1-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="536c1-120">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="536c1-121">MBAMClientSetup.exe</span><span class="sxs-lookup"><span data-stu-id="536c1-121">MBAMClientSetup.exe</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="536c1-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="536c1-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="536c1-123">msiexec/i MBAMClient.msi</span><span class="sxs-lookup"><span data-stu-id="536c1-123">msiexec /i MBAMClient.msi</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="536c1-124">msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="536c1-124">msiexec /i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="536c1-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="536c1-125">Related topics</span></span>


[<span data-ttu-id="536c1-126">Bereitstellen des MBAM 2.5-Clients</span><span class="sxs-lookup"><span data-stu-id="536c1-126">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="536c1-127">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="536c1-127">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="536c1-128">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="536c1-128">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="536c1-129">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="536c1-129">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




