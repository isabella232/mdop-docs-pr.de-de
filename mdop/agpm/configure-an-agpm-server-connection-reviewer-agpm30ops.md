---
title: Konfigurieren einer AGPM-Server-Verbindung
description: Konfigurieren einer AGPM-Server-Verbindung
author: dansimp
ms.assetid: ae78dc74-111d-4509-b0a6-e8b8b451c22a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 50968d8b1b1eb5d464c6dbdb251354a9dc691d62
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807735"
---
# <span data-ttu-id="e1a6c-103">Konfigurieren einer AGPM-Server-Verbindung</span><span class="sxs-lookup"><span data-stu-id="e1a6c-103">Configure an AGPM Server Connection</span></span>


<span data-ttu-id="e1a6c-104">Wenn Sie sicherstellen möchten, dass Sie mit dem richtigen zentralen Archiv verbunden sind, überprüfen Sie die Konfiguration der AGPM-Server Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e1a6c-104">To ensure that you are connected to the correct central archive, review the configuration of the AGPM Server connection.</span></span> <span data-ttu-id="e1a6c-105">Wenn ein AGPM-Administrator (Vollzugriff) für Sie keine AGPM-Server Verbindung konfiguriert hat, müssen Sie ihn manuell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e1a6c-105">If an AGPM Administrator (Full Control) has not configured an AGPM Server connection for you, then you must manually configure it.</span></span>

**<span data-ttu-id="e1a6c-106">So wählen Sie einen AGPM-Server aus</span><span class="sxs-lookup"><span data-stu-id="e1a6c-106">To select an AGPM Server</span></span>**

1.  <span data-ttu-id="e1a6c-107">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="e1a6c-107">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e1a6c-108">Klicken Sie im Detailbereich auf die Registerkarte **AGPM-Server** :</span><span class="sxs-lookup"><span data-stu-id="e1a6c-108">In the details pane, click the **AGPM Server** tab:</span></span>

    -   <span data-ttu-id="e1a6c-109">Wenn die Optionen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, wurden Sie von einem AGPM-Administrator zentral konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e1a6c-109">If the options on the **AGPM Server** tab are unavailable, they have been centrally configured by an AGPM Administrator.</span></span>

    -   <span data-ttu-id="e1a6c-110">Wenn die Optionen auf der Registerkarte **AGPM-Server** verfügbar sind, geben Sie den vollqualifizierten Computernamen für den AGPM-Server (beispielsweise Server.contoso.com) und den Port ein, den der AGPM-Dienst überwacht (standardmäßig Port 4600).</span><span class="sxs-lookup"><span data-stu-id="e1a6c-110">If the options on the **AGPM Server** tab are available, type the fully-qualified computer name for the AGPM Server (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span> <span data-ttu-id="e1a6c-111">Klicken Sie auf über **nehmen**, und klicken Sie dann zum bestätigen auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="e1a6c-111">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="e1a6c-112">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="e1a6c-112">Additional considerations</span></span>

-   <span data-ttu-id="e1a6c-113">Die ausgewählten AGPM-Server legen fest, welche GPOs auf der Registerkarte **Inhalt** angezeigt werden und an welchem Speicherort die Einstellungen für die **Domänen Delegierungs** Einstellungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1a6c-113">The AGPM Servers selected determine which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="e1a6c-114">Wenn Sie nicht zentral über die administrative Vorlage verwaltet werden, muss jeder Gruppenrichtlinienadministrator diese Einstellung so konfigurieren, dass er auf den AGPM-Server für die Domäne verweist.</span><span class="sxs-lookup"><span data-stu-id="e1a6c-114">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

### <span data-ttu-id="e1a6c-115">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="e1a6c-115">Additional references</span></span>

-   [<span data-ttu-id="e1a6c-116">Durchführen von Editor-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="e1a6c-116">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="e1a6c-117">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="e1a6c-117">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="e1a6c-118">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="e1a6c-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





