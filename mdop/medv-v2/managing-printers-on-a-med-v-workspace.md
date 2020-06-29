---
title: Verwalten von Druckern in einem MED-V-Arbeitsbereich
description: Verwalten von Druckern in einem MED-V-Arbeitsbereich
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811563"
---
# <span data-ttu-id="5db2b-103">Verwalten von Druckern in einem MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="5db2b-103">Managing Printers on a MED-V Workspace</span></span>


<span data-ttu-id="5db2b-104">In Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 bietet die Druckerumleitung Endbenutzern eine konsistente Druckfunktionalität zwischen dem virtuellen Med-v-Computer und dem Hostcomputer.</span><span class="sxs-lookup"><span data-stu-id="5db2b-104">In Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, printer redirection provides end users with a consistent printing experience between the MED-V virtual machine and the host computer.</span></span>

<span data-ttu-id="5db2b-105">Dieses Thema enthält Informationen zum Verwalten des Druckvorgangs in einem MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5db2b-105">This topic provides information about how to manage printing in a MED-V workspace.</span></span>

## <span data-ttu-id="5db2b-106">Verwalten von Druckern in MED-V-Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="5db2b-106">Managing Printers in MED-V Workspaces</span></span>


<span data-ttu-id="5db2b-107">In den meisten Fällen verarbeitet MED-V die Druckerumleitung automatisch.</span><span class="sxs-lookup"><span data-stu-id="5db2b-107">In most cases, MED-V handles printer redirection automatically.</span></span> <span data-ttu-id="5db2b-108">Nach Abschluss der erstmaligen Einrichtung identifiziert Med-v alle auf dem Host installierten Netzwerkdrucker, ruft die entsprechenden Treiber vom Netzwerkdruckserver ab und installiert die entsprechenden Treiber im Med-v-Arbeitsbereich, wenn Sie gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="5db2b-108">After first time setup finishes, MED-V identifies all network printers installed on the host, retrieves the corresponding drivers from the network print server, and if found, installs the relevant drivers in the MED-V workspace.</span></span> <span data-ttu-id="5db2b-109">Nachdem alle Treiber gefunden und installiert wurden, startet Med-v den Med-v-Arbeitsbereich neu.</span><span class="sxs-lookup"><span data-stu-id="5db2b-109">After all drivers are found and installed, MED-V reboots the MED-V workspace.</span></span> <span data-ttu-id="5db2b-110">Erst nachdem der MED-V-Arbeitsbereich neu gestartet wurde, sind die Host Drucker vorhanden und für den Gast verfügbar, in der Regel in wenigen Minuten.</span><span class="sxs-lookup"><span data-stu-id="5db2b-110">Only after the MED-V workspace restarts, the host printers are present and available on the guest, typically in a few minutes.</span></span>

<span data-ttu-id="5db2b-111">**Hinweis**  Wenn Anwendungen im MED-V-Arbeitsbereich ausgeführt werden, wird der Endbenutzer aufgefordert, den Neustart fortzusetzen oder zu einem späteren Zeitpunkt zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5db2b-111">**Note** If applications are running on the MED-V workspace, the end user is prompted to let the restart continue or postpone it until later.</span></span> <span data-ttu-id="5db2b-112">Wenn keine Anwendungen ausgeführt werden, ist der Neustart automatisch und wird dem Endbenutzer nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5db2b-112">If no applications are running, the restart is automatic and not shown to the end user.</span></span>

 

<span data-ttu-id="5db2b-113">Jedes Mal, wenn MED-V neu gestartet wird, überprüft es, ob neue Drucker auf dem Host installiert sind, und ruft, falls gefunden, die entsprechenden Treiber vom Netzwerkdruckserver ab und installiert Sie auf dem Gast.</span><span class="sxs-lookup"><span data-stu-id="5db2b-113">Every time MED-V is re-started, it checks whether any new printers are installed on the host and, if found, retrieves the corresponding drivers from the network print server and installs them on the guest.</span></span> <span data-ttu-id="5db2b-114">Med-v startet den Med-v-Arbeitsbereich so neu, wie wenn die erstmalige Einrichtung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5db2b-114">MED-V then restarts the MED-V workspace just as when first time setup was completed.</span></span>

<span data-ttu-id="5db2b-115">**Wichtig**  Nachdem die relevanten Treiber auf dem Gast installiert wurden, werden die Drucker erst nach dem Neustart auf dem Gast sichtbar.</span><span class="sxs-lookup"><span data-stu-id="5db2b-115">**Important** After the relevant drivers are installed on the guest, the printers only become visible on the guest after the restart occurs.</span></span>

 

<span data-ttu-id="5db2b-116">Wenn ein Treiber zu einem beliebigen Zeitpunkt nicht gefunden oder installiert werden kann, muss er manuell auf dem Gast installiert sein, damit der Netzwerkdrucker für den Endbenutzer zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="5db2b-116">If at any time a driver cannot be located or installed, it must be manually installed on the guest for the network printer to be available to the end user.</span></span>

<span data-ttu-id="5db2b-117">Die folgende Liste enthält einige zusätzliche Anleitungen:</span><span class="sxs-lookup"><span data-stu-id="5db2b-117">The following list offers some additional guidance:</span></span>

<span data-ttu-id="5db2b-118">In **MED-V werden nur Netzwerkdrucker verwaltet**.</span><span class="sxs-lookup"><span data-stu-id="5db2b-118">**MED-V only manages network printers**.</span></span> <span data-ttu-id="5db2b-119">Treiber für Drucker, die lokal auf dem Host installiert sind, werden auf dem Gast nicht automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="5db2b-119">Drivers for printers that are installed locally on the host are not automatically installed on the guest.</span></span>

<span data-ttu-id="5db2b-120">**In MED-V werden nur Druckertreiber installiert, wenn Sie auf dem Druckserver gefunden**werden.</span><span class="sxs-lookup"><span data-stu-id="5db2b-120">**MED-V only installs printer drivers if found on the print server**.</span></span> <span data-ttu-id="5db2b-121">Wenn Sie nicht gefunden werden, müssen die Druckertreiber manuell installiert werden.</span><span class="sxs-lookup"><span data-stu-id="5db2b-121">If not found, printer drivers must be manually installed.</span></span>

<span data-ttu-id="5db2b-122">**Drucker, die manuell auf dem Gast installiert sind, sind für den Host nicht zugänglich**.</span><span class="sxs-lookup"><span data-stu-id="5db2b-122">**Printers manually installed on the guest are not accessible to the host**.</span></span> <span data-ttu-id="5db2b-123">Standardmäßig unterstützt MED-V nur die Druckerumleitung vom Gast zum Host.</span><span class="sxs-lookup"><span data-stu-id="5db2b-123">By default, MED-V only supports printer redirection from the guest to the host.</span></span>

<span data-ttu-id="5db2b-124">**Warnung**  Wenn ein Drucker manuell auf dem Gast installiert ist und der Drucker später auf dem Host installiert ist, ist das Ergebnis, dass der Drucker zwei Mal im Gast installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5db2b-124">**Warning** If a printer is manually installed on the guest, and the same printer is later installed on the host, the result is that the printer is installed two times in the guest.</span></span> <span data-ttu-id="5db2b-125">Um dieses Problem zu vermeiden, empfiehlt es sich, die Druckerumleitung nur auf eine Art und Weise zu verwalten: entweder deaktivieren Sie die Umleitung, und installieren Sie Drucker manuell auf dem Gast, oder aktivieren Sie die Umleitung, und installieren Sie Drucker nicht manuell auf dem Gast.</span><span class="sxs-lookup"><span data-stu-id="5db2b-125">To avoid this situation, a MED-V best practice is to manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

 

## <span data-ttu-id="5db2b-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5db2b-126">Related topics</span></span>


[<span data-ttu-id="5db2b-127">Verwalten von MED-V-Arbeitsbereichseinstellungen</span><span class="sxs-lookup"><span data-stu-id="5db2b-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





