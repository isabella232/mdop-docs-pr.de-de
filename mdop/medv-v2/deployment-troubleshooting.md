---
title: Problembehandlung bei der Bereitstellung
description: Problembehandlung bei der Bereitstellung
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809631"
---
# <span data-ttu-id="134c4-103">Problembehandlung bei der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="134c4-103">Deployment Troubleshooting</span></span>


<span data-ttu-id="134c4-104">Dieses Thema enthält Informationen, die Sie bei der Behandlung von Bereitstellungsproblemen in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 unterstützen.</span><span class="sxs-lookup"><span data-stu-id="134c4-104">This topic includes information to help you troubleshoot deployment issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="134c4-105">Behandeln von Problemen bei der MED-V-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="134c4-105">Troubleshooting Issues in MED-V Deployment</span></span>


<span data-ttu-id="134c4-106">Das folgende Problem kann auftreten, wenn Sie MED-V bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="134c4-106">The following issue might occur when you deploy MED-V.</span></span> <span data-ttu-id="134c4-107">Die Lösung hilft bei der Behebung dieses Problems.</span><span class="sxs-lookup"><span data-stu-id="134c4-107">The solution helps troubleshoot this issue.</span></span>

**<span data-ttu-id="134c4-108">Probleme treten auf, wenn Sie nur MED-V für den aktuellen Benutzer installieren.</span><span class="sxs-lookup"><span data-stu-id="134c4-108">Problems Occur if Installing MED-V for Current User Only.</span></span>** <span data-ttu-id="134c4-109">Med-v unterstützt nur die Installation des Med-v-Arbeitsbereichs Pakets, des Med-v-Host-Agents und des Med-v-Arbeitsbereichs für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="134c4-109">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="134c4-110">Die Installation für den aktuellen Benutzer verursacht nur Fehler bei der Installation der Komponenten und beim Einrichten des MED-V-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="134c4-110">Installing for the current user only causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>

**<span data-ttu-id="134c4-111">Lösung</span><span class="sxs-lookup"><span data-stu-id="134c4-111">Solution</span></span>**

<span data-ttu-id="134c4-112">Verwenden Sie bei der Installation der MED-V-Komponenten niemals die Option **ALLUSERS = ""** .</span><span class="sxs-lookup"><span data-stu-id="134c4-112">Never use the option **ALLUSERS=””** when installing the MED-V components.</span></span>

**<span data-ttu-id="134c4-113">Für MED-V ist eine exklusive Verwendung des Virtualisierungs-Stacks erforderlich.</span><span class="sxs-lookup"><span data-stu-id="134c4-113">MED-V Requires Exclusive Use of the Virtualization Stack.</span></span>** <span data-ttu-id="134c4-114">Auf einem Computer kann jeweils nur ein Virtualisierungs-Stack ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="134c4-114">Only one virtualization stack can be run at a time on a computer.</span></span> <span data-ttu-id="134c4-115">Windows Virtual PC muss den virtuellen Stapel verwenden, und MED-V ist von Windows Virtual PC abhängig.</span><span class="sxs-lookup"><span data-stu-id="134c4-115">Windows Virtual PC must use the virtual stack, and MED-V depends on Windows Virtual PC.</span></span> <span data-ttu-id="134c4-116">Wenn Sie also versuchen, Med-v bereitzustellen oder zu verwenden, wenn andere Anwendungen ausgeführt werden, die den virtuellen Stapel verwenden, kann Med-v nicht ausgeführt oder erfolgreich installiert werden.</span><span class="sxs-lookup"><span data-stu-id="134c4-116">Therefore, if you try to deploy or use MED-V when other applications are running that use the virtual stack, MED-V cannot run or be successfully installed.</span></span>

**<span data-ttu-id="134c4-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="134c4-117">Solution</span></span>**

<span data-ttu-id="134c4-118">Schließen Sie alle Anwendungen, die ausgeführt werden, die den Virtualisierungs-Stack verwenden, bevor Sie MED-V installieren oder ausführen.</span><span class="sxs-lookup"><span data-stu-id="134c4-118">Close any application that is running that uses the virtualization stack before you install or run MED-V.</span></span>

**<span data-ttu-id="134c4-119">Verknüpfungen bleiben nach der Deinstallation erhalten.</span><span class="sxs-lookup"><span data-stu-id="134c4-119">Shortcuts Remain after Uninstall.</span></span>** <span data-ttu-id="134c4-120">Standardmäßig werden beim Deinstallieren von MED-V Verknüpfungen im **Startmenü** des Endbenutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="134c4-120">By default, when you uninstall MED-V, shortcuts in the end user’s **Start** menu are removed.</span></span> <span data-ttu-id="134c4-121">In bestimmten Situationen wie beispielsweise für Endbenutzer, die Server gespeicherte Profile ausführen, bleiben Verknüpfungen zu den veröffentlichten MED-V-Anwendungen im **Startmenü** des Endbenutzers erhalten.</span><span class="sxs-lookup"><span data-stu-id="134c4-121">However, in certain situations, such as for end users who are running roaming profiles, shortcuts to MED-V published applications remain in the end user’s **Start** menu.</span></span>

**<span data-ttu-id="134c4-122">Lösung</span><span class="sxs-lookup"><span data-stu-id="134c4-122">Solution</span></span>**

<span data-ttu-id="134c4-123">Wenn Sie die restlichen Verknüpfungen im **Startmenü** manuell löschen möchten, klicken Sie mit der rechten Maustaste auf die Verknüpfungen, und klicken Sie dann auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="134c4-123">To manually delete the remaining shortcuts on the **Start** menu, right-click the shortcuts, and then click **Remove**.</span></span>

**<span data-ttu-id="134c4-124">Deaktivieren Sie die Gruppenrichtlinieneinstellung für Anmeldenachrichten im MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="134c4-124">Disable Logon Message Group Policy Setting in the MED-V Workspace.</span></span>** <span data-ttu-id="134c4-125">Wenn die Windows XP-Anmeldenachricht im Med-v-Arbeitsbereich aktiviert ist, muss sich der Endbenutzer jedes Mal anmelden, wenn er eine virtuelle Med-v-Anwendung öffnen möchte.</span><span class="sxs-lookup"><span data-stu-id="134c4-125">If the Windows XP logon message is enabled in the MED-V workspace, the end user must log on every time they want to open a MED-V virtual application.</span></span> <span data-ttu-id="134c4-126">Dadurch entsteht eine schlechte Benutzererfahrung.</span><span class="sxs-lookup"><span data-stu-id="134c4-126">This creates a poor user experience.</span></span>

**<span data-ttu-id="134c4-127">Lösung</span><span class="sxs-lookup"><span data-stu-id="134c4-127">Solution</span></span>**

<span data-ttu-id="134c4-128">Deaktivieren Sie die folgenden Gruppenrichtlinieneinstellungen auf dem MED-V-virtuellen Computer:</span><span class="sxs-lookup"><span data-stu-id="134c4-128">Disable the following Group Policy settings in the MED-V virtual machine:</span></span>

**<span data-ttu-id="134c4-129">Interaktive Anmeldung: Nachricht für Benutzer, die sich anmelden wollen</span><span class="sxs-lookup"><span data-stu-id="134c4-129">Interactive logon: Message text for users attempting to log on</span></span>**

**<span data-ttu-id="134c4-130">Interaktive Anmeldung: Nachrichtentitel für Benutzer, die sich anmelden wollen</span><span class="sxs-lookup"><span data-stu-id="134c4-130">Interactive logon: Message title for users attempting to log on</span></span>**

## <span data-ttu-id="134c4-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="134c4-131">Related topics</span></span>


[<span data-ttu-id="134c4-132">Problembehandlung bei Vorgängen</span><span class="sxs-lookup"><span data-stu-id="134c4-132">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

 

 





