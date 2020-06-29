---
title: So konfigurieren Sie das Verhalten von Verknüpfungen und Dateitypzuordnungen
description: So konfigurieren Sie das Verhalten von Verknüpfungen und Dateitypzuordnungen
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807296"
---
# <span data-ttu-id="22ca8-103">So konfigurieren Sie das Verhalten von Verknüpfungen und Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="22ca8-103">How to Configure Shortcut and File Type Association Behavior</span></span>


<span data-ttu-id="22ca8-104">Die Veröffentlichungsrichtlinie für die Verknüpfungs-und Dateitypzuordnung (FTA) wird von der Veröffentlichungs-XML-Datei definiert und gesteuert, die von einem Veröffentlichungsserver während eines Veröffentlichungs Aktualisierungsvorgangs an Clients gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="22ca8-104">Shortcut and File Type Association (FTA) publishing policy is defined and controlled by the publishing XML file, which is sent to clients by a publishing server during a publishing refresh operation.</span></span> <span data-ttu-id="22ca8-105">Wenn der Client diese Informationen erhält, werden alle neu veröffentlichten Daten zu Anwendungen wie den Symbolen und Freihandelsabkommen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="22ca8-105">When the client receives this information, it adds any newly published data about applications such as the icons and FTAs.</span></span> <span data-ttu-id="22ca8-106">Anschließend werden alle veralteten Veröffentlichungsdaten entfernt.</span><span class="sxs-lookup"><span data-stu-id="22ca8-106">Then, it removes any outdated publishing data.</span></span>

<span data-ttu-id="22ca8-107">In App-V Version 4,6 wurden zwei Registrierungsschlüsselwerte definiert, damit Administratoren dieses Verhalten steuern können.</span><span class="sxs-lookup"><span data-stu-id="22ca8-107">In App-V version 4.6, two registry key values have been defined to enable administrators to control this behavior.</span></span> <span data-ttu-id="22ca8-108">Standardmäßig werden Tastenkombinationen, die lokal mithilfe der Clientkonsole erstellt werden, nun beibehalten.</span><span class="sxs-lookup"><span data-stu-id="22ca8-108">By default, shortcuts that are created locally by using the client console are now retained.</span></span>

## <span data-ttu-id="22ca8-109">So ändern Sie das Verhalten von Tastenkombinationen und FTA</span><span class="sxs-lookup"><span data-stu-id="22ca8-109">How to Change Shortcut and FTA Behavior</span></span>


<span data-ttu-id="22ca8-110">Für den Registrierungsschlüssel "Clientkonfiguration", "FileTypePolicy" und "ShortcutPolicy", wurden zwei neue DWORD-Registrierungswerte definiert.</span><span class="sxs-lookup"><span data-stu-id="22ca8-110">Two new DWORD registry values have been defined for the client Configuration registry key, “FileTypePolicy” and “ShortcutPolicy”.</span></span> <span data-ttu-id="22ca8-111">Diese DWORD-Registrierungswerte sind standardmäßig nicht vorhanden, können aber manuell hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="22ca8-111">These DWORD registry values are not present by default, but they can be added manually.</span></span> <span data-ttu-id="22ca8-112">Der Registrierungsschlüssel für die Konfiguration befindet sich unter HKEY \ _LOCAL \ _MACHINE \\software\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="22ca8-112">The Configuration registry key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span></span>

<span data-ttu-id="22ca8-113">Es gibt vier Richtlinienwerte, die in der folgenden Tabelle definiert sind, und diese gelten für beide Registrierungsschlüsselwerte.</span><span class="sxs-lookup"><span data-stu-id="22ca8-113">There are four policy values defined in the following table and these apply to both registry key values.</span></span> <span data-ttu-id="22ca8-114">Die folgende Liste zeigt die numerischen Werte für die Registrierungseinstellungen und das Verhalten, das auf Dateitypen oder Tastenkombinationen bei einem Veröffentlichungs Aktualisierungsvorgang angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="22ca8-114">The following list shows the numeric values for the registry settings, and the behavior applied to file types or shortcuts on a publishing refresh operation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22ca8-115">Name</span><span class="sxs-lookup"><span data-stu-id="22ca8-115">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ca8-116">Typ</span><span class="sxs-lookup"><span data-stu-id="22ca8-116">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ca8-117">Daten (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="22ca8-117">Data (Examples)</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ca8-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22ca8-118">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22ca8-119">FileTypePolicy</span><span class="sxs-lookup"><span data-stu-id="22ca8-119">FileTypePolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ca8-120">DWORD</span><span class="sxs-lookup"><span data-stu-id="22ca8-120">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ca8-121">Standard = 0x2 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="22ca8-121">Default=0x2 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ca8-122">(0x0) – "ClientOnly" – entfernen Sie alle vorhandenen Elemente aus derselben Veröffentlichungs Informationsquelle, und behalten Sie nur Elemente bei, die lokal hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="22ca8-122">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items that are added locally</span></span></p>
<p><span data-ttu-id="22ca8-123">(0x1) – "ServerOnly" – entfernen Sie alle veralteten Elemente aus derselben Veröffentlichungs Informationsquelle sowie alle Elemente, die lokal hinzugefügt wurden, und fügen Sie die neuen Elemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="22ca8-123">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items that are added locally, and add the new items</span></span></p>
<p><span data-ttu-id="22ca8-124">(0x2) – "ClientAndServer" – entfernen Sie alle veralteten Elemente aus derselben Veröffentlichungs Informationsquelle, halten Sie die Elemente lokal hinzugefügt, und fügen Sie die neuen Elemente hinzu (Standard, wenn Sie für App-V 4,6 nicht vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="22ca8-124">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present for App-V 4.6)</span></span></p>
<p><span data-ttu-id="22ca8-125">(0x3) – "NoChange" – nehmen Sie keine Änderungen an Dateitypen oder Tastenkombinationen vor.</span><span class="sxs-lookup"><span data-stu-id="22ca8-125">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22ca8-126">ShortcutPolicy</span><span class="sxs-lookup"><span data-stu-id="22ca8-126">ShortcutPolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ca8-127">DWORD</span><span class="sxs-lookup"><span data-stu-id="22ca8-127">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ca8-128">Standard = 0x2</span><span class="sxs-lookup"><span data-stu-id="22ca8-128">Default=0x2</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ca8-129">(0x0) – "ClientOnly" – entfernen Sie alle vorhandenen Elemente aus derselben Veröffentlichungs Informationsquelle, und behalten Sie nur lokal hinzugefügte Elemente bei.</span><span class="sxs-lookup"><span data-stu-id="22ca8-129">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items added locally</span></span></p>
<p><span data-ttu-id="22ca8-130">(0x1) – "ServerOnly" – entfernen Sie alle veralteten Elemente aus derselben Veröffentlichungs Informationsquelle und alle Elemente, die lokal hinzugefügt wurden, und fügen Sie die neuen Elemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="22ca8-130">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items added locally, and add the new items</span></span></p>
<p><span data-ttu-id="22ca8-131">(0x2) – "ClientAndServer" – entfernt alle veralteten Elemente aus derselben Veröffentlichungs Informationsquelle, behält Elemente lokal hinzu und fügt die neuen Elemente hinzu (Standard, wenn nicht vorhanden).</span><span class="sxs-lookup"><span data-stu-id="22ca8-131">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present)</span></span></p>
<p><span data-ttu-id="22ca8-132">(0x3) – "NoChange" – nehmen Sie keine Änderungen an Dateitypen oder Tastenkombinationen vor.</span><span class="sxs-lookup"><span data-stu-id="22ca8-132">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="22ca8-133">**Hinweis**  Die Textwerte beziehen sich auf die Werte für die XML-Attribute in der Veröffentlichungs-XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="22ca8-133">**Note** The text values refer to the values for the XML attributes in the publishing XML file.</span></span><span data-ttu-id="22ca8-134">Sie können diese Werte manuell einstellen, wenn Sie eine benutzerdefinierte HTTP-Veröffentlichungslösung implementiert haben.</span><span class="sxs-lookup"><span data-stu-id="22ca8-134"> You can set these values manually if you have implemented a custom HTTP publishing solution.</span></span>

 

 

 





