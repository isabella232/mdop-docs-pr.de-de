---
title: So deinstallieren Sie App-V Client
description: So deinstallieren Sie App-V Client
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806740"
---
# <span data-ttu-id="c15e0-103">So deinstallieren Sie App-V Client</span><span class="sxs-lookup"><span data-stu-id="c15e0-103">How to Uninstall the App-V Client</span></span>


<span data-ttu-id="c15e0-104">Gehen Sie wie folgt vor, um den Application Virtualization-Client auf dem Computer zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="c15e0-104">Use the following procedure to uninstall the Application Virtualization Client from the computer.</span></span>

**<span data-ttu-id="c15e0-105">So deinstallieren Sie den Application Virtualization-Desktop Client</span><span class="sxs-lookup"><span data-stu-id="c15e0-105">To uninstall the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="c15e0-106">Doppelklicken Sie in der Systemsteuerung auf **Software** (oder in Windows Vista, **Programme und Funktionen**), und doppelklicken Sie dann auf **Microsoft Application Virtualization Desktop Client**.</span><span class="sxs-lookup"><span data-stu-id="c15e0-106">In Control Panel, double-click **Add or Remove Programs** (or in Windows Vista, **Programs and Features**), and then double-click **Microsoft Application Virtualization Desktop Client**.</span></span>

2.  <span data-ttu-id="c15e0-107">Klicken Sie im daraufhin angezeigten Dialogfeld auf **Ja** , um den Deinstallationsvorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c15e0-107">In the dialog box that appears, click **Yes** to continue with the uninstall process.</span></span>

    <span data-ttu-id="c15e0-108">**Wichtig**  Der Deinstallationsprozess kann nicht abgebrochen oder unterbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="c15e0-108">**Important** The uninstall process cannot be canceled or interrupted.</span></span>

     

3.  <span data-ttu-id="c15e0-109">Wenn eine Meldung angezeigt wird, die besagt, dass die Microsoft Application Virtualization Client Tray-Anwendung geschlossen werden muss, bevor Sie fortfahren, klicken Sie mit der rechten Maustaste auf das App-V-Symbol im Infobereich, und wählen Sie **Beenden** aus, um die Anwendung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c15e0-109">When a message stating that the Microsoft Application Virtualization Client Tray application must be closed before continuing appears, right-click the App-V icon in the notification area and select **Exit** to close the application.</span></span> <span data-ttu-id="c15e0-110">Klicken Sie dann auf wieder **holen** , um den Deinstallationsvorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c15e0-110">Then click **Retry** to continue with the uninstall process.</span></span>

    <span data-ttu-id="c15e0-111">**Wichtig**  Möglicherweise wird eine Meldung angezeigt, die besagt, dass eine oder mehrere virtuelle Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c15e0-111">**Important** You might see a message stating that one or more virtual applications are in use.</span></span> <span data-ttu-id="c15e0-112">Schließen Sie alle geöffneten Anwendungen, und speichern Sie Ihre Daten, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="c15e0-112">Close any open applications and save your data before you continue.</span></span> <span data-ttu-id="c15e0-113">Klicken Sie dann auf **OK** , um den Deinstallationsvorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c15e0-113">Then click **OK** to continue with the uninstall process.</span></span>

     

4.  <span data-ttu-id="c15e0-114">Eine Fortschrittsleiste zeigt die verbleibende Zeit an.</span><span class="sxs-lookup"><span data-stu-id="c15e0-114">A progress bar shows the time remaining.</span></span> <span data-ttu-id="c15e0-115">Wenn dieser Schritt abgeschlossen ist, müssen Sie den Computer neu starten, damit alle zugehörigen Treiber beendet werden können, um den Deinstallationsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c15e0-115">When this step finishes, you must restart the computer so that all associated drivers can be stopped to complete the uninstall process.</span></span>

    <span data-ttu-id="c15e0-116">**Hinweis**  Die folgenden Registrierungsschlüssel bleiben nach Abschluss des Deinstallationsvorgangs erhalten:</span><span class="sxs-lookup"><span data-stu-id="c15e0-116">**Note** The following registry keys remain after the uninstall process is complete:</span></span>

    -   <span data-ttu-id="c15e0-117">HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid</span><span class="sxs-lookup"><span data-stu-id="c15e0-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span></span>

    -   <span data-ttu-id="c15e0-118">HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5</span><span class="sxs-lookup"><span data-stu-id="c15e0-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span></span>

    -   <span data-ttu-id="c15e0-119">HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\systemguard "Client" = DWORD: 00000000</span><span class="sxs-lookup"><span data-stu-id="c15e0-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard"Client"=dword:00000000</span></span>

    -   <span data-ttu-id="c15e0-120">HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\systemguard\\seckey</span><span class="sxs-lookup"><span data-stu-id="c15e0-120">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span></span>

     

## <span data-ttu-id="c15e0-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c15e0-121">Related topics</span></span>


[<span data-ttu-id="c15e0-122">So installieren Sie den Client über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="c15e0-122">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="c15e0-123">So installieren Sie Application Virtualization Client manuell</span><span class="sxs-lookup"><span data-stu-id="c15e0-123">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="c15e0-124">So veröffentlichen Sie eine virtuelle Anwendung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="c15e0-124">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





