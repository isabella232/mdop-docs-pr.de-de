---
title: So stellen Sie einen MED-V-Arbeitsbereich in ein Windows 7-Image bereit
description: So stellen Sie einen MED-V-Arbeitsbereich in ein Windows 7-Image bereit
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812262"
---
# <span data-ttu-id="672eb-103">So stellen Sie einen MED-V-Arbeitsbereich in ein Windows 7-Image bereit</span><span class="sxs-lookup"><span data-stu-id="672eb-103">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>


<span data-ttu-id="672eb-104">Sie können alle MED-V-Komponenten in einem Windows 7-Abbild installieren, das Sie in Ihrem Unternehmen genauso wie bei jeder neuen Installation von Windows 7 verteilen.</span><span class="sxs-lookup"><span data-stu-id="672eb-104">You can install all the MED-V components into a Windows 7 image that you distribute throughout your enterprise just as you would any new installation of Windows 7.</span></span> <span data-ttu-id="672eb-105">Der Endbenutzer beendet dann die Installation des Med-v-Arbeitsbereichs, indem er auf eine **Start** Menü Verknüpfung klickt, die Sie zum Starten von Med-v konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="672eb-105">The end user then finishes the installation of the MED-V workspace by clicking a **Start** menu shortcut that you configure to start MED-V.</span></span> <span data-ttu-id="672eb-106">Das erstmalige Setup wird gestartet, und der Endbenutzer befolgt die Anweisungen, um die Konfiguration abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="672eb-106">First time setup starts and the end user follows the instructions to complete the configuration.</span></span>

<span data-ttu-id="672eb-107">Der folgende Abschnitt enthält Informationen und Anweisungen, die Ihnen bei der Bereitstellung des MED-V-Arbeitsbereichs in Ihrem Unternehmen helfen, indem Sie ein Windows 7-Abbild verwenden.</span><span class="sxs-lookup"><span data-stu-id="672eb-107">The following section provides information and instructions to help you deploy the MED-V workspace throughout your enterprise by using a Windows 7 image.</span></span>

**<span data-ttu-id="672eb-108">So stellen Sie einen MED-V-Arbeitsbereich in einem Windows 7-Abbild bereit</span><span class="sxs-lookup"><span data-stu-id="672eb-108">To deploy a MED-V workspace in a Windows 7 image</span></span>**

1.  <span data-ttu-id="672eb-109">Erstellen Sie ein Standardbild von Windows 7.</span><span class="sxs-lookup"><span data-stu-id="672eb-109">Create a standard image of Windows 7.</span></span> <span data-ttu-id="672eb-110">Weitere Informationen finden Sie unter [Erstellen eines Standard Abbilds von Windows 7: Schritt-für-Schritt-Anleitung](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .</span><span class="sxs-lookup"><span data-stu-id="672eb-110">For more information, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=204843) (https://go.microsoft.com/fwlink/?LinkId=204843).</span></span>

2.  <span data-ttu-id="672eb-111">Installieren Sie im Windows 7-Abbild Windows Virtual PC und die Windows Virtual PC-Updates.</span><span class="sxs-lookup"><span data-stu-id="672eb-111">In the Windows 7 image, install Windows Virtual PC and the Windows Virtual PC updates.</span></span> <span data-ttu-id="672eb-112">Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.</span><span class="sxs-lookup"><span data-stu-id="672eb-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

3.  <span data-ttu-id="672eb-113">Installieren Sie den Med-v-Host-Agent mithilfe der Installationsdatei Med-v \ _HostAgent \ _setup.</span><span class="sxs-lookup"><span data-stu-id="672eb-113">Install the MED-V Host Agent by using the MED-V\_HostAgent\_Setup installation file.</span></span> <span data-ttu-id="672eb-114">Weitere Informationen finden Sie unter [Manuelles Installieren des MED-V-Host-Agents](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="672eb-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    <span data-ttu-id="672eb-115">**Warnung**  Internet Explorer muss geschlossen werden, bevor Sie den MED-V-Host-Agent installieren, andernfalls können Konflikte später bei der URL-Umleitung auftreten.</span><span class="sxs-lookup"><span data-stu-id="672eb-115">**Warning** Internet Explorer must be closed before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="672eb-116">Sie können dies auch tun, indem Sie während einer Verteilung einen Neustart des Computers angeben.</span><span class="sxs-lookup"><span data-stu-id="672eb-116">You can also do this by specifying a computer restart during a distribution.</span></span>

     

4.  <span data-ttu-id="672eb-117">Kopieren Sie die MED-V Workspace-Paketdateien in das Windows 7-Abbild.</span><span class="sxs-lookup"><span data-stu-id="672eb-117">Copy the MED-V workspace package files to the Windows 7 image.</span></span> <span data-ttu-id="672eb-118">Die Med-v Workspace-Paketdateien sind das Med-v Workspace-Installationsprogramm, die medv-Datei und setup.exe Datei, die Sie mithilfe des **Med-v-Arbeitsbereichs-Packagers**erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="672eb-118">The MED-V workspace package files are the MED-V workspace installer, .medv file, and setup.exe file that you created by using the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="672eb-119">**Wichtig**  Die medv-und die setup.exe-Datei müssen sich im gleichen Ordner wie das MED-V Workspace-Installationsprogramm befinden.</span><span class="sxs-lookup"><span data-stu-id="672eb-119">**Important** The .medv and setup.exe file must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="672eb-120">Installieren Sie dann den MED-V-Arbeitsbereich, indem Sie setup.exe ausführen.</span><span class="sxs-lookup"><span data-stu-id="672eb-120">Then, install the MED-V workspace by running setup.exe.</span></span>

     

5.  <span data-ttu-id="672eb-121">Konfigurieren Sie eine Verknüpfung im Menü " **Start** ", um die Installation des MED-V-Arbeitsbereichs Pakets zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="672eb-121">Configure a shortcut on the **Start** menu to open the MED-V workspace package installation.</span></span>

    <span data-ttu-id="672eb-122">Erstellen Sie eine Verknüpfung im **Startmenü** mit der setup.exe-Datei, über die der Endbenutzer eine MED-V-Installation nach Bedarf starten kann.</span><span class="sxs-lookup"><span data-stu-id="672eb-122">Create a **Start** menu shortcut to the setup.exe file that lets the end user start a MED-V installation as required.</span></span>

6.  <span data-ttu-id="672eb-123">Verteilen Sie das Windows 7-Abbild mithilfe des standardmäßigen Bild Bereitstellungsprozesses Ihres Unternehmens an Computer in Ihrem Unternehmen, für die MED-V erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="672eb-123">By using your company’s standard image deployment process, distribute the Windows 7 image to computers in your enterprise that require MED-V.</span></span>

<span data-ttu-id="672eb-124">Wenn der Endbenutzer auf eine im Med-v-Arbeitsbereich veröffentlichte Anwendung zugreifen muss, kann er auf die Verknüpfung **Start** Menü klicken, um den Med-v-Arbeitsbereich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="672eb-124">When the end user has to access an application published in the MED-V workspace, they can click the **Start** menu shortcut to install the MED-V workspace.</span></span> <span data-ttu-id="672eb-125">Dadurch wird automatisch die erstmalige Einrichtung gestartet und die Konfiguration von MED-V abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="672eb-125">This automatically starts first time setup and completes the configuration of MED-V.</span></span> <span data-ttu-id="672eb-126">Nach Abschluss der erstmaligen Einrichtung kann der Endbenutzer im **Startmenü** auf die MED-V-Anwendungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="672eb-126">After first time setup is complete, the end user can access the MED-V applications on the **Start** menu.</span></span>

## <span data-ttu-id="672eb-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="672eb-127">Related topics</span></span>


[<span data-ttu-id="672eb-128">Übersicht über die Bereitstellung von MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="672eb-128">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="672eb-129">So stellen Sie einen MED-V-Arbeitsbereich über eines elektronischen Softwareverteilungssystem bereit</span><span class="sxs-lookup"><span data-stu-id="672eb-129">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





