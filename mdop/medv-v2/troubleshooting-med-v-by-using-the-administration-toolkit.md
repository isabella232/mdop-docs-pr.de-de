---
title: Problembehandlung von MED-V mit dem Verwaltungstoolkit
description: Problembehandlung von MED-V mit dem Verwaltungstoolkit
author: dansimp
ms.assetid: 6c096a1c-b9ce-4ec7-8dfd-5286e3b9a617
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1eaa493e5603e8a1275a6ff5f189739b168f319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811116"
---
# <span data-ttu-id="97d4e-103">Problembehandlung von MED-V mit dem Verwaltungstoolkit</span><span class="sxs-lookup"><span data-stu-id="97d4e-103">Troubleshooting MED-V by Using the Administration Toolkit</span></span>


<span data-ttu-id="97d4e-104">Verwenden Sie das Med-v-Administrations-Toolkit, um bestimmte Probleme in einem Med-v-Arbeitsbereich zu beheben.</span><span class="sxs-lookup"><span data-stu-id="97d4e-104">Use the MED-V Administration Toolkit to troubleshoot certain problems in a MED-V workspace.</span></span> <span data-ttu-id="97d4e-105">Mit dem Med-v-Administrations-Toolkit können Sie auf Ereignisprotokolle zugreifen und diese konfigurieren, den Med-v-Arbeitsbereich neu starten oder Zurücksetzen sowie die veröffentlichten Anwendungen und umgeleiteten Webadressen im Med-v-Arbeitsbereich anzeigen.</span><span class="sxs-lookup"><span data-stu-id="97d4e-105">The MED-V Administration Toolkit lets you access and configure event logs, restart or reset the MED-V workspace, and view the published applications and redirected web addresses in the MED-V workspace.</span></span> <span data-ttu-id="97d4e-106">Sie können auch das Med-v-Administrations-Toolkit verwenden, um den virtuellen Med-v Workspace-Computer im Vollbildmodus zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="97d4e-106">You can also use the MED-V Administration Toolkit to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="97d4e-107">So öffnen Sie das MED-V-Administrations-Toolkit</span><span class="sxs-lookup"><span data-stu-id="97d4e-107">To Open the MED-V Administration Toolkit</span></span>


<span data-ttu-id="97d4e-108">Führen Sie die folgenden Schritte aus, um das MED-V-Administrations-Toolkit zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="97d4e-108">Perform the following steps to open the MED-V Administration Toolkit:</span></span>

1.  <span data-ttu-id="97d4e-109">Öffnen Sie ein Eingabeaufforderungsfenster auf dem Hostcomputer, der den MED-V-Arbeitsbereich enthält, bei dem Sie die Problembehandlung ausführen.</span><span class="sxs-lookup"><span data-stu-id="97d4e-109">On the host computer that contains the MED-V workspace you are troubleshooting, open a Command Prompt window.</span></span>

2.  <span data-ttu-id="97d4e-110">Navigieren Sie zu%SystemDrive%\\Program c:\\Programme\\Microsoft Enterprise-Desktop-Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="97d4e-110">Browse to %systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization.</span></span>

3.  <span data-ttu-id="97d4e-111">Geben Sie an der Eingabeaufforderung **MedvHost/Toolkit**.</span><span class="sxs-lookup"><span data-stu-id="97d4e-111">At the command prompt, type **MedvHost /toolkit**.</span></span>

<span data-ttu-id="97d4e-112">Nachdem das Med-v-Administrations-Toolkit geöffnet wurde, können Sie das Toolkit verwenden, um Probleme im Med-v-Arbeitsbereich zu beheben, die während der Problembehandlung gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="97d4e-112">After the MED-V Administration Toolkit opens, you can use the toolkit to help resolve issues in the MED-V workspace found during troubleshooting.</span></span>

## <span data-ttu-id="97d4e-113">Inhalt dieses Abschnitts:</span><span class="sxs-lookup"><span data-stu-id="97d4e-113">In this Section</span></span>


<a href="" id="viewing-and-configuring-med-v-logs"></a>[<span data-ttu-id="97d4e-114">Anzeigen und Konfigurieren von MED-V-Protokollen</span><span class="sxs-lookup"><span data-stu-id="97d4e-114">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)  
<span data-ttu-id="97d4e-115">Beschreibt, wie Sie das Med-v-Administrations-Toolkit zum Sammeln und Verwalten von Med-v-Ereignisprotokollen auf dem Hostcomputer und dem virtuellen Gastcomputer verwenden.</span><span class="sxs-lookup"><span data-stu-id="97d4e-115">Describes how to use the MED-V Administration Toolkit to collect and manage MED-V event logs in the host computer and the guest virtual machine.</span></span>

<a href="" id="restarting-and-resetting-a-med-v-workspace"></a>[<span data-ttu-id="97d4e-116">Neu starten und das Zurücksetzen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="97d4e-116">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)  
<span data-ttu-id="97d4e-117">Beschreibt, wie Sie Med-v-Arbeitsbereiche mithilfe des Med-v-Administrations-Toolkits neu starten und zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="97d4e-117">Describes how to restart and reset MED-V workspaces by using the MED-V Administration Toolkit.</span></span>

<a href="" id="viewing-med-v-workspace-configurations"></a>[<span data-ttu-id="97d4e-118">Anzeigen von MED-V-Arbeitsbereichskonfigurationen</span><span class="sxs-lookup"><span data-stu-id="97d4e-118">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)  
<span data-ttu-id="97d4e-119">Es wird beschrieben, wie Sie das Med-v-Administrations-Toolkit verwenden, um veröffentlichte Anwendungen und umgeleitete Webadressen in einem Med-v-Arbeitsbereich anzuzeigen und zu erfahren, wie Sie den virtuellen Computer mit dem Med-v-Arbeitsbereich im Vollbildmodus öffnen.</span><span class="sxs-lookup"><span data-stu-id="97d4e-119">Describes how to use the MED-V Administration Toolkit to view the published applications and redirected web addresses in a MED-V workspace and how to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="97d4e-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="97d4e-120">Related topics</span></span>


[<span data-ttu-id="97d4e-121">MED-V-Ereignisprotokollmeldungen</span><span class="sxs-lookup"><span data-stu-id="97d4e-121">MED-V Event Log Messages</span></span>](med-v-event-log-messages.md)

[<span data-ttu-id="97d4e-122">Problembehandlung für MED-V</span><span class="sxs-lookup"><span data-stu-id="97d4e-122">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





