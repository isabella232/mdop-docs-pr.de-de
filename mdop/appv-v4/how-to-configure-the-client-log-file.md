---
title: So konfigurieren Sie die Clientprotokolldatei
description: So konfigurieren Sie die Clientprotokolldatei
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807251"
---
# <span data-ttu-id="47f06-103">So konfigurieren Sie die Clientprotokolldatei</span><span class="sxs-lookup"><span data-stu-id="47f06-103">How to Configure the Client Log File</span></span>


<span data-ttu-id="47f06-104">Sie können die folgenden Verfahren zum Konfigurieren der Application Virtualization (App-V)-Client Protokolldatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="47f06-104">You can use the following procedures to configure the Application Virtualization (App-V) Client log file.</span></span>

**<span data-ttu-id="47f06-105">So ändern Sie den Speicherort der Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="47f06-105">To change the log file location</span></span>**

-   <span data-ttu-id="47f06-106">Bearbeiten Sie den folgenden Registrierungsschlüsselwert, um den neuen Pfad für die Protokolldatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="47f06-106">Edit the following registry key value to specify the new path for the log file.</span></span> <span data-ttu-id="47f06-107">Nachdem Sie diesen Wert geändert haben, müssen Sie den **sftlist** -Dienst erneut starten.</span><span class="sxs-lookup"><span data-stu-id="47f06-107">You must restart the **sftlist** service after changing this value.</span></span> <span data-ttu-id="47f06-108">Dieser Speicherort kann auch nach der Installation interaktiv geändert werden.</span><span class="sxs-lookup"><span data-stu-id="47f06-108">This location can also be changed interactively after installation.</span></span>

    <span data-ttu-id="47f06-109">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\logfilename</span><span class="sxs-lookup"><span data-stu-id="47f06-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span></span>

**<span data-ttu-id="47f06-110">So ändern Sie die Protokoll Berichterstattungs Ebene</span><span class="sxs-lookup"><span data-stu-id="47f06-110">To change the log reporting level</span></span>**

-   <span data-ttu-id="47f06-111">Standardmäßig enthalten die in das Protokoll geschriebenen Nachrichtentypen alle Ereignisse des Schweregrads 4 (Information) oder höher.</span><span class="sxs-lookup"><span data-stu-id="47f06-111">By default, the type of messages that are written to the log include all events of severity level 4 (Informational) or higher.</span></span> <span data-ttu-id="47f06-112">Der Schweregrad wird im folgenden Schlüsselwert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="47f06-112">The severity level is stored in the following key value.</span></span> <span data-ttu-id="47f06-113">Setzen Sie diesen Schlüsselwert auf 5, um die ausführliche Protokollierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="47f06-113">Set this key value to 5 to enable verbose logging.</span></span> <span data-ttu-id="47f06-114">Verwenden Sie die ausführliche Protokollierung nur für kurze Zeiträume während der Problembehandlung, da Sie eine sehr große Anzahl von Nachrichten generiert und dazu führt, dass das Protokoll schnell gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="47f06-114">Use verbose logging only for short periods during troubleshooting because it will generate a very large volume of messages and cause the log to fill up quickly.</span></span>

    <span data-ttu-id="47f06-115">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\logminseverity</span><span class="sxs-lookup"><span data-stu-id="47f06-115">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span></span>

**<span data-ttu-id="47f06-116">So ändern Sie die Protokollgröße</span><span class="sxs-lookup"><span data-stu-id="47f06-116">To change the log size</span></span>**

-   <span data-ttu-id="47f06-117">In Application Virtualization (App-V) 4,5 wird die Protokollgröße durch den folgenden Registrierungsschlüsselwert gesteuert.</span><span class="sxs-lookup"><span data-stu-id="47f06-117">In Application Virtualization (App-V) 4.5, the log size is controlled by the following registry key value.</span></span> <span data-ttu-id="47f06-118">Dieser Wert ist standardmäßig 256MB und definiert die maximale Größe in MB, auf die das Protokoll anwachsen kann, bevor es zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="47f06-118">This value defaults to 256MB and defines the maximum size, in MB, that the log can grow to before being reset.</span></span>

    <span data-ttu-id="47f06-119">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\logmaxsize</span><span class="sxs-lookup"><span data-stu-id="47f06-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span></span>

    <span data-ttu-id="47f06-120">**Vorsicht**  Dieser Registrierungsschlüsselwert muss auf einen Wert größer als 0 (null) gesetzt werden, um sicherzustellen, dass die Protokolldatei zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="47f06-120">**Caution** This registry key value must be set to a value greater than zero to ensure the log file does get reset.</span></span>

     

**<span data-ttu-id="47f06-121">So ändern Sie die Anzahl von Sicherungskopien</span><span class="sxs-lookup"><span data-stu-id="47f06-121">To change the number of backup copies</span></span>**

-   <span data-ttu-id="47f06-122">Wenn die Protokolldatei die maximale Größe erreicht, wird ein Reset erzwungen, wenn der nächste Schreibvorgang in das Protokoll erfolgt.</span><span class="sxs-lookup"><span data-stu-id="47f06-122">When the log file reaches the maximum size, a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="47f06-123">Bei einem Reset wird eine neue Protokolldatei erstellt, und die alte Datei wird als Sicherung umbenannt.</span><span class="sxs-lookup"><span data-stu-id="47f06-123">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span> <span data-ttu-id="47f06-124">Mit der folgenden Registrierungseinstellung wird die Anzahl von Sicherungskopien der Protokolldatei gesteuert, die beim Zurücksetzen der Datei aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="47f06-124">The following registry setting controls the number of backup copies of the log file that are kept when the file is reset.</span></span> <span data-ttu-id="47f06-125">Der Standardwert ist 4.</span><span class="sxs-lookup"><span data-stu-id="47f06-125">The default value is 4.</span></span>

    <span data-ttu-id="47f06-126">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\logrollovercount</span><span class="sxs-lookup"><span data-stu-id="47f06-126">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span></span>

    <span data-ttu-id="47f06-127">Das Format der Namen der Sicherungsprotokolldatei lautet: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** und basiert auf der Zeit zum Zurücksetzen, in UTC (Universal Coordinated Time).</span><span class="sxs-lookup"><span data-stu-id="47f06-127">The format of the backup log file names is: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** and is based on the reset time, in Universal Coordinated Time (UTC).</span></span> <span data-ttu-id="47f06-128">In der folgenden Tabelle sind die beim Erstellen der Dateinamen und deren Beschreibungen verwendeten Symbole aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="47f06-128">The following table lists the symbols used in creating the file names and their descriptions.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="47f06-129">Symbol</span><span class="sxs-lookup"><span data-stu-id="47f06-129">Symbol</span></span></th>
    <th align="left"><span data-ttu-id="47f06-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47f06-130">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="47f06-131">JJJJ</span><span class="sxs-lookup"><span data-stu-id="47f06-131">YYYY</span></span></p></td>
    <td align="left"><p><span data-ttu-id="47f06-132">vierstellige Jahreszahl</span><span class="sxs-lookup"><span data-stu-id="47f06-132">4-digit year</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="47f06-133">MM</span><span class="sxs-lookup"><span data-stu-id="47f06-133">MM</span></span></p></td>
    <td align="left"><p><span data-ttu-id="47f06-134">zweistelliger Monat (01 – 12)</span><span class="sxs-lookup"><span data-stu-id="47f06-134">2-digit month (01–12)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="47f06-135">DD</span><span class="sxs-lookup"><span data-stu-id="47f06-135">DD</span></span></p></td>
    <td align="left"><p><span data-ttu-id="47f06-136">zweistelliger Tag des Monats (01 – 31)</span><span class="sxs-lookup"><span data-stu-id="47f06-136">2-digit day of the month (01–31)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="47f06-137">hh</span><span class="sxs-lookup"><span data-stu-id="47f06-137">hh</span></span></p></td>
    <td align="left"><p><span data-ttu-id="47f06-138">Stunde (00 – 23)</span><span class="sxs-lookup"><span data-stu-id="47f06-138">hour (00–23)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="47f06-139">mm</span><span class="sxs-lookup"><span data-stu-id="47f06-139">mm</span></span></p></td>
    <td align="left"><p><span data-ttu-id="47f06-140">Minuten (00 – 59)</span><span class="sxs-lookup"><span data-stu-id="47f06-140">minutes (00–59)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="47f06-141">ss</span><span class="sxs-lookup"><span data-stu-id="47f06-141">ss</span></span></p></td>
    <td align="left"><p><span data-ttu-id="47f06-142">Sekunden (00 – 59)</span><span class="sxs-lookup"><span data-stu-id="47f06-142">seconds (00–59)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="47f06-143">uuu</span><span class="sxs-lookup"><span data-stu-id="47f06-143">uuu</span></span></p></td>
    <td align="left"><p><span data-ttu-id="47f06-144">Millisekunden (000 – 999)</span><span class="sxs-lookup"><span data-stu-id="47f06-144">milliseconds (000–999)</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="47f06-145">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="47f06-145">Related topics</span></span>


[<span data-ttu-id="47f06-146">So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="47f06-146">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





