---
title: Bereitstellen von DaRT 10 für Administratorcomputer
description: Bereitstellen von DaRT 10 für Administratorcomputer
author: dansimp
ms.assetid: c1981cbe-10f8-41f6-8989-bcc9d57a2aa8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 020ffab3239c5e56b3505f468035cf5007baf9e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804748"
---
# <span data-ttu-id="9cdc7-103">Bereitstellen von DaRT 10 für Administratorcomputer</span><span class="sxs-lookup"><span data-stu-id="9cdc7-103">Deploying DaRT 10 to Administrator Computers</span></span>


<span data-ttu-id="9cdc7-104">Bevor Sie mit der Bereitstellung von Microsoft Diagnostics and Recovery Toolset (Dart) 10 beginnen, überprüfen Sie die Anforderungen für Ihre Umgebung.</span><span class="sxs-lookup"><span data-stu-id="9cdc7-104">Before you begin the deployment of Microsoft Diagnostics and Recovery Toolset (DaRT) 10, review the requirements for your environment.</span></span> <span data-ttu-id="9cdc7-105">Dies umfasst die Hardwareanforderungen für die Installation von DART 10.</span><span class="sxs-lookup"><span data-stu-id="9cdc7-105">This includes the hardware requirements for installing DaRT 10.</span></span> <span data-ttu-id="9cdc7-106">Weitere Informationen zu den Dart-Hardware-und Softwareanforderungen finden Sie unter [unterstützte Dart-Konfigurationen](dart-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="9cdc7-106">For more information about DaRT hardware and software requirements, see [DaRT 10 Supported Configurations](dart-10-supported-configurations.md).</span></span>

<span data-ttu-id="9cdc7-107">Die Themen in diesem Abschnitt können verwendet werden, um die Bereitstellung von Dart in Ihrem Unternehmen basierend auf Ihrer Umgebung und Bereitstellungsstrategie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9cdc7-107">The topics in this section can be used to help you deploy DaRT in your enterprise based on your environment and deployment strategy.</span></span>

## <span data-ttu-id="9cdc7-108">Bereitstellen von DART 10</span><span class="sxs-lookup"><span data-stu-id="9cdc7-108">Deploy DaRT 10</span></span>


<span data-ttu-id="9cdc7-109">Sie können die Windows Installer-Datei für DART verwenden, um Dart auf einem Computer zu installieren, den Sie zum ersten Erstellen des DART-Wiederherstellungs Bilds verwenden, und dann Problembehandlung und Beheben von Endbenutzercomputern.</span><span class="sxs-lookup"><span data-stu-id="9cdc7-109">You can use the Windows Installer file for DaRT to install DaRT on a computer that you will use to first create the DaRT recovery image and then troubleshoot and fix end-user computers.</span></span> <span data-ttu-id="9cdc7-110">Häufig können Sie in einer Organisation auf dem Administratorcomputer nur die DART-Funktionen installieren, die Sie zum Erstellen eines Dart-Wiederherstellungs Bilds benötigen.</span><span class="sxs-lookup"><span data-stu-id="9cdc7-110">Frequently, across an organization, you might install on the administrator computer only the DaRT functionality that you need to create a DaRT recovery image.</span></span> <span data-ttu-id="9cdc7-111">Auf dem Computer eines Helpdesk-Administrators können Sie dann nur die Dart-Funktionalität installieren, die Sie für die Problembehandlung eines Problem Computers benötigen, beispielsweise die Dart-Remote Verbindungsanzeige und den Absturzanalyse-Analyzer.</span><span class="sxs-lookup"><span data-stu-id="9cdc7-111">Then, on a help desk administrator’s computer, you might install only the DaRT functionality that you must have to troubleshoot a problem computer, such as the DaRT Remote Connection Viewer and the Crash Analyzer.</span></span>

<span data-ttu-id="9cdc7-112">Neben der manuellen Ausführung der Windows Installer-Datei zum Installieren von DART können Sie Dart auch an der Eingabeaufforderung installieren, um Enterprise-Software Bereitstellungssysteme wie SystemCenterConfigurationManager2012 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9cdc7-112">In addition to manually running the Windows Installer file to install DaRT, you can also install DaRT at the command prompt to support enterprise software deployment systems such as SystemCenterConfigurationManager2012.</span></span>

[<span data-ttu-id="9cdc7-113">So stellen Sie DaRT 10 bereit</span><span class="sxs-lookup"><span data-stu-id="9cdc7-113">How to Deploy DaRT 10</span></span>](how-to-deploy-dart-10.md)

## <span data-ttu-id="9cdc7-114">Ändern, reparieren oder Entfernen von DART 10</span><span class="sxs-lookup"><span data-stu-id="9cdc7-114">Change, repair, or remove DaRT 10</span></span>


<span data-ttu-id="9cdc7-115">Sie können die Dart-Installation ändern, reparieren oder entfernen, indem Sie auf die Dart-Installationsdatei doppelklicken und dann auf die Schaltfläche klicken, die der Aktion entspricht, die Sie durchführen möchten, oder über die Windows-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="9cdc7-115">You can change, repair, or remove the DaRT installation by double-clicking the DaRT installation file and then clicking the button that corresponds to the action that you want to perform or through the Windows Control Panel.</span></span>

[<span data-ttu-id="9cdc7-116">So ändern, reparieren oder entfernen Sie DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9cdc7-116">How to Change, Repair, or Remove DaRT 10</span></span>](how-to-change-repair-or-remove-dart-10.md)

## <span data-ttu-id="9cdc7-117">So erhalten Sie Dart 10</span><span class="sxs-lookup"><span data-stu-id="9cdc7-117">How to get DaRT 10</span></span>


<span data-ttu-id="9cdc7-118">Informationen zum Abrufen der Dart-Software finden Sie unter [Abrufen von MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="9cdc7-118">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="9cdc7-119">Weitere Ressourcen für die Bereitstellung von DART 10 auf Administrator Computern</span><span class="sxs-lookup"><span data-stu-id="9cdc7-119">Other resources for deploying DaRT 10 to administrator computers</span></span>


[<span data-ttu-id="9cdc7-120">Bereitstellen von DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9cdc7-120">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 





