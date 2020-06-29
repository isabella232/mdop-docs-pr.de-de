---
title: Bereitstellen von DaRT 8.0 für Administratorcomputer
description: Bereitstellen von DaRT 8.0 für Administratorcomputer
author: dansimp
ms.assetid: f918ead8-742e-464a-8bf6-1fcedde66cae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0ab001f612f2257ecbd77c39319cc99c17d36197
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810366"
---
# <span data-ttu-id="c0482-103">Bereitstellen von DaRT 8.0 für Administratorcomputer</span><span class="sxs-lookup"><span data-stu-id="c0482-103">Deploying DaRT 8.0 to Administrator Computers</span></span>


<span data-ttu-id="c0482-104">Bevor Sie mit der Bereitstellung von Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 beginnen, überprüfen Sie die Anforderungen für Ihre Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c0482-104">Before you begin the deployment of Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, review the requirements for your environment.</span></span> <span data-ttu-id="c0482-105">Dies umfasst die Hardwareanforderungen für die Installation von Dart 8,0.</span><span class="sxs-lookup"><span data-stu-id="c0482-105">This includes the hardware requirements for installing DaRT 8.0.</span></span> <span data-ttu-id="c0482-106">Weitere Informationen zu DART-Hardware-und Softwareanforderungen finden Sie unter [unterstützte Dart 8,0-Konfigurationen](dart-80-supported-configurations-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="c0482-106">For more information about DaRT hardware and software requirements, see [DaRT 8.0 Supported Configurations](dart-80-supported-configurations-dart-8.md).</span></span>

<span data-ttu-id="c0482-107">Die Themen in diesem Abschnitt können verwendet werden, um die Bereitstellung von Dart in Ihrem Unternehmen basierend auf Ihrer Umgebung und Bereitstellungsstrategie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c0482-107">The topics in this section can be used to help you deploy DaRT in your enterprise based on your environment and deployment strategy.</span></span>

## <span data-ttu-id="c0482-108">Bereitstellen von Dart 8,0</span><span class="sxs-lookup"><span data-stu-id="c0482-108">Deploy DaRT 8.0</span></span>


<span data-ttu-id="c0482-109">Sie können die Windows Installer-Datei für DART verwenden, um Dart auf einem Computer zu installieren, den Sie zum ersten Erstellen des DART-Wiederherstellungs Bilds verwenden, und dann Problembehandlung und Beheben von Endbenutzercomputern.</span><span class="sxs-lookup"><span data-stu-id="c0482-109">You can use the Windows Installer file for DaRT to install DaRT on a computer that you will use to first create the DaRT recovery image and then troubleshoot and fix end-user computers.</span></span> <span data-ttu-id="c0482-110">Häufig können Sie in einer Organisation auf dem Administratorcomputer nur die DART-Funktionen installieren, die Sie zum Erstellen eines Dart-Wiederherstellungs Bilds benötigen.</span><span class="sxs-lookup"><span data-stu-id="c0482-110">Frequently, across an organization, you might install on the administrator computer only the DaRT functionality that you need to create a DaRT recovery image.</span></span> <span data-ttu-id="c0482-111">Auf dem Computer eines Helpdesk-Administrators können Sie dann nur die Dart-Funktionalität installieren, die Sie für die Problembehandlung eines Problem Computers benötigen, beispielsweise die Dart-Remote Verbindungsanzeige und den Absturzanalyse-Analyzer.</span><span class="sxs-lookup"><span data-stu-id="c0482-111">Then, on a help desk administrator’s computer, you might install only the DaRT functionality that you must have to troubleshoot a problem computer, such as the DaRT Remote Connection Viewer and the Crash Analyzer.</span></span>

<span data-ttu-id="c0482-112">Neben der manuellen Ausführung der Windows Installer-Datei zum Installieren von DART können Sie Dart auch an der Eingabeaufforderung installieren, um Enterprise-Software Bereitstellungssysteme wie SystemCenterConfigurationManager2012 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c0482-112">In addition to manually running the Windows Installer file to install DaRT, you can also install DaRT at the command prompt to support enterprise software deployment systems such as SystemCenterConfigurationManager2012.</span></span>

[<span data-ttu-id="c0482-113">So stellen Sie DaRT 8.0 bereit</span><span class="sxs-lookup"><span data-stu-id="c0482-113">How to Deploy DaRT 8.0</span></span>](how-to-deploy-dart-80-dart-8.md)

## <span data-ttu-id="c0482-114">Ändern, reparieren oder Entfernen von Dart 8,0</span><span class="sxs-lookup"><span data-stu-id="c0482-114">Change, repair, or remove DaRT 8.0</span></span>


<span data-ttu-id="c0482-115">Sie können die Dart-Installation ändern, reparieren oder entfernen, indem Sie auf die Dart-Installationsdatei doppelklicken und dann auf die Schaltfläche klicken, die der Aktion entspricht, die Sie durchführen möchten, oder über die Windows-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="c0482-115">You can change, repair, or remove the DaRT installation by double-clicking the DaRT installation file and then clicking the button that corresponds to the action that you want to perform or through the Windows Control Panel.</span></span>

[<span data-ttu-id="c0482-116">So ändern, reparieren oder entfernen Sie DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="c0482-116">How to Change, Repair, or Remove DaRT 8.0</span></span>](how-to-change-repair-or-remove-dart-80-dart-8.md)

## <span data-ttu-id="c0482-117">So erhalten Sie Dart 8,0</span><span class="sxs-lookup"><span data-stu-id="c0482-117">How to get DaRT 8.0</span></span>


<span data-ttu-id="c0482-118">Informationen zum Abrufen der Dart-Software finden Sie unter [Abrufen von MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="c0482-118">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="c0482-119">Weitere Ressourcen für die Bereitstellung von Dart 8,0 auf Administrator Computern</span><span class="sxs-lookup"><span data-stu-id="c0482-119">Other resources for deploying the DaRT 8.0 to administrator computers</span></span>


[<span data-ttu-id="c0482-120">Bereitstellen von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="c0482-120">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





