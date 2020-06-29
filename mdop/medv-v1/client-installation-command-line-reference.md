---
title: Befehlszeilenreferenz für die Clientinstallation
description: Befehlszeilenreferenz für die Clientinstallation
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811929"
---
# <span data-ttu-id="91402-103">Befehlszeilenreferenz für die Clientinstallation</span><span class="sxs-lookup"><span data-stu-id="91402-103">Client Installation Command Line Reference</span></span>


**<span data-ttu-id="91402-104">So installieren Sie MED-V über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="91402-104">To install MED-V from the command line</span></span>**

1.  <span data-ttu-id="91402-105">Führen Sie in der Befehlszeile das MED-V. MSI-Paket aus, gefolgt von einem der optionalen Parameter, die in der folgenden Tabelle beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="91402-105">From the command line, run the MED-V .msi package followed by any of the optional parameters described in the following table.</span></span>

2.  <span data-ttu-id="91402-106">Das MED-V. MSI-Paket heißt *MED-V\_x.msi*, wobei *x* die Versionsnummer ist.</span><span class="sxs-lookup"><span data-stu-id="91402-106">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="91402-107">Beispiel: *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="91402-107">For example, *MED-V\_1.0.65.msi*.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="91402-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="91402-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="91402-109">Wert</span><span class="sxs-lookup"><span data-stu-id="91402-109">Value</span></span></th>
<th align="left"><span data-ttu-id="91402-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91402-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91402-111">/Quiet</span><span class="sxs-lookup"><span data-stu-id="91402-111">/quiet</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="91402-112">Unbeaufsichtigte Installation</span><span class="sxs-lookup"><span data-stu-id="91402-112">Silent installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91402-113">/log &lt; Vollständiger Pfad zur Protokolldatei&gt;</span><span class="sxs-lookup"><span data-stu-id="91402-113">/log &lt;full path to log file&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="91402-114">Der vollständige Pfad zur Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="91402-114">The full path to the log file.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91402-115">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="91402-115">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="91402-116">Der vollständige Pfad zum Installationsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="91402-116">The full path to the installation directory.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91402-117">VMSFOLDER</span><span class="sxs-lookup"><span data-stu-id="91402-117">VMSFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="91402-118">Der vollständige Pfad zum Ordner "virtueller Computer".</span><span class="sxs-lookup"><span data-stu-id="91402-118">The full path to the virtual machine folder.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91402-119">INSTALL_ADMIN_TOOLS</span><span class="sxs-lookup"><span data-stu-id="91402-119">INSTALL_ADMIN_TOOLS</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="91402-120">1.0</span><span class="sxs-lookup"><span data-stu-id="91402-120">1,0</span></span></strong></p>
<p><span data-ttu-id="91402-121">Standard: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="91402-121">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91402-122">Installiert MED-V-Verwaltungstools.</span><span class="sxs-lookup"><span data-stu-id="91402-122">Installs MED-V administration tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91402-123">START_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="91402-123">START_AUTOMATICALLY</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="91402-124">1.0</span><span class="sxs-lookup"><span data-stu-id="91402-124">1,0</span></span></strong></p>
<p><span data-ttu-id="91402-125">Standard: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="91402-125">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91402-126">Startet den MED-V-Client automatisch jedes Mal, wenn sich der Benutzer bei Windows anmeldet.</span><span class="sxs-lookup"><span data-stu-id="91402-126">Automatically starts MED-V client every time the user logs on to Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91402-127">SERVER_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="91402-127">SERVER_ADDRESS</span></span></p></td>
<td align="left"><p><span data-ttu-id="91402-128">Hostname oder IP</span><span class="sxs-lookup"><span data-stu-id="91402-128">host name or IP</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91402-129">SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="91402-129">SERVER_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="91402-130">Anschluss</span><span class="sxs-lookup"><span data-stu-id="91402-130">port</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91402-131">SERVER_SSL</span><span class="sxs-lookup"><span data-stu-id="91402-131">SERVER_SSL</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="91402-132">1.0</span><span class="sxs-lookup"><span data-stu-id="91402-132">1,0</span></span></strong></p>
<p><span data-ttu-id="91402-133">für <strong> https </strong> oder <strong> http</span><span class="sxs-lookup"><span data-stu-id="91402-133">for <strong>https</strong> or <strong>http</span></span></strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91402-134">START_MEDV</span><span class="sxs-lookup"><span data-stu-id="91402-134">START_MEDV</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="91402-135">1.0</span><span class="sxs-lookup"><span data-stu-id="91402-135">1,0</span></span></strong></p>
<p><span data-ttu-id="91402-136">Standard: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="91402-136">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91402-137">Startet Med-v nach Abschluss der Med-v-Installation.</span><span class="sxs-lookup"><span data-stu-id="91402-137">Starts MED-V at the completion of the MED-V installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="91402-138">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="91402-138">Note</span></span></strong><br/><p><span data-ttu-id="91402-139">Es wird empfohlen, START_MEDV = 0 zu setzen, falls MED-V vom System installiert wird.</span><span class="sxs-lookup"><span data-stu-id="91402-139">It is recommended to set START_MEDV=0 in case MED-V is installed by the system.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91402-140">DESKTOP_SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="91402-140">DESKTOP_SHORTCUT</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="91402-141">1.0</span><span class="sxs-lookup"><span data-stu-id="91402-141">1,0</span></span></strong></p>
<p><span data-ttu-id="91402-142">Standard: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="91402-142">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91402-143">Erstellt eine Verknüpfung auf dem Desktop, auf der der MED-V-Client gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="91402-143">Creates a shortcut on the desktop, which starts MED-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91402-144">MINIMAL_RAM_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="91402-144">MINIMAL_RAM_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="91402-145">RAM in MB</span><span class="sxs-lookup"><span data-stu-id="91402-145">RAM in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="91402-146">Überprüfen Sie bei der Installation von MED-V, ob der Computer über die Mindestgröße des angegebenen Arbeitsspeichers verfügt.</span><span class="sxs-lookup"><span data-stu-id="91402-146">When installing MED-V, checks whether the computer has the minimum amount of RAM specified.</span></span> <span data-ttu-id="91402-147">Wenn dies nicht der Fall ist, wird die Installation abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="91402-147">If not, installation is aborted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91402-148">SKIP_OS_CHECK</span><span class="sxs-lookup"><span data-stu-id="91402-148">SKIP_OS_CHECK</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="91402-149">1.0</span><span class="sxs-lookup"><span data-stu-id="91402-149">1,0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91402-150">Unterdrückt die Validierung des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="91402-150">Omits the operating system validation.</span></span></p></td>
</tr>
</tbody>
</table>











