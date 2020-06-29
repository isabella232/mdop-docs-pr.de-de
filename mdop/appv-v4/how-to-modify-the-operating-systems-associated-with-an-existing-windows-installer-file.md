---
title: So ändern Sie die Betriebssysteme, die mit einer vorhandenen Windows Installer-Datei verknüpft sind
description: So ändern Sie die Betriebssysteme, die mit einer vorhandenen Windows Installer-Datei verknüpft sind
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806912"
---
# <span data-ttu-id="622ff-103">So ändern Sie die Betriebssysteme, die mit einer vorhandenen Windows Installer-Datei verknüpft sind</span><span class="sxs-lookup"><span data-stu-id="622ff-103">How to Modify the Operating Systems Associated With an Existing Windows Installer File</span></span>


<span data-ttu-id="622ff-104">Gehen Sie wie folgt vor, um die Betriebssystemversionen zu ändern, die einer vorhandenen Windows Installer-Datei (**MSI**) zugeordnet sind, die mithilfe von App-V Sequencer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="622ff-104">Use the following procedure to modify the operating system versions associated with an existing Windows Installer (**MSI**) file that was created by using the App-V Sequencer.</span></span>

**<span data-ttu-id="622ff-105">So ändern Sie die Betriebssysteme einer vorhandenen Windows Installer-Datei</span><span class="sxs-lookup"><span data-stu-id="622ff-105">To modify the operating systems of an existing Windows Installer file</span></span>**

1.  <span data-ttu-id="622ff-106">Installieren Sie den App-V-Sequencer auf einem Computer in Ihrer Umgebung, auf dem nur das Betriebssystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="622ff-106">Install the App-V Sequencer on a computer in your environment that has only the operating system installed.</span></span> <span data-ttu-id="622ff-107">Alternativ können Sie den Sequencer auf einem Computer mit einer virtuellen Umgebung installieren – beispielsweise Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="622ff-107">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="622ff-108">Diese Methode ist hilfreich, da es einfacher ist, eine saubere Sequenz Umgebung beizubehalten, die Sie mit minimaler zusätzlicher Konfiguration wieder verwenden können.</span><span class="sxs-lookup"><span data-stu-id="622ff-108">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span> <span data-ttu-id="622ff-109">Weitere Informationen zum Installieren des App-V-Sequencers finden Sie unter so wird es [gemacht: Installieren des Sequencers](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="622ff-109">For more information about installing the App-V Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

2.  <span data-ttu-id="622ff-110">Kopieren Sie das gesamte virtuelle Anwendungspaket, das die Windows Installer-Datei enthält, die Sie ändern möchten, auf den Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="622ff-110">Copy the entire virtual application package that contains the Windows Installer file you want to modify to the computer running the Sequencer.</span></span>

3.  <span data-ttu-id="622ff-111">Wenn Sie die Windows Installer-Datei ändern möchten, öffnen Sie die Sequencer-Konsole, wählen Sie **Paket**  /  **Öffnen**aus, und navigieren Sie dann zu dem Speicherort, an dem das mit der Windows Installer-Datei verknüpfte virtuelle Anwendungspaket gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="622ff-111">To modify the Windows Installer file, open the Sequencer console, select **Package** / **Open**, and then browse to the location where the virtual application package associated with the Windows Installer file is saved.</span></span>

4.  <span data-ttu-id="622ff-112">Zum Hinzufügen oder Entfernen von Betriebssystemen wählen Sie die Registerkarte **Bereitstellung** in der Sequencer-Konsole aus.</span><span class="sxs-lookup"><span data-stu-id="622ff-112">To add or remove operating systems, select the **Deployment** tab in the Sequencer console.</span></span> <span data-ttu-id="622ff-113">Wenn Sie zusätzliche Betriebssysteme angeben möchten, die der Windows Installer-Datei zugeordnet werden sollen, wählen Sie das gewünschte Betriebssystem aus, und klicken Sie dann auf den Pfeil, der auf das **ausgewählte** Betriebssystem Listen-Steuerelement zeigt.</span><span class="sxs-lookup"><span data-stu-id="622ff-113">To specify additional operating systems that will be associated with the Windows Installer file, select the desired operating system, and then click the arrow that points to the **Selected** operating system list control.</span></span>

    <span data-ttu-id="622ff-114">Wenn Sie eine Betriebssystem Zuordnung entfernen möchten, wählen Sie das zu entfernende Betriebssystem aus, und klicken Sie dann auf den Pfeil, der auf das **Verfügbare** Betriebssystem Listen-Steuerelement zeigt.</span><span class="sxs-lookup"><span data-stu-id="622ff-114">To remove an operating system association, select the operating system you want to remove, and then click the arrow that points to the **Available** operating system list control.</span></span>

5.  <span data-ttu-id="622ff-115">Zum Erstellen eines neuen Windows Installers, der dem virtuellen Anwendungspaket zugeordnet wird, wählen Sie **Microsoft Windows Installer (MSI)-Paket generieren**aus.</span><span class="sxs-lookup"><span data-stu-id="622ff-115">To create a new Windows Installer that will be associated with the virtual application package, select **Generate Microsoft Windows Installer (MSI) Package**.</span></span> <span data-ttu-id="622ff-116">Sie können auch Tools zum **Tools**  /  **Erstellen von MSI**auswählen.</span><span class="sxs-lookup"><span data-stu-id="622ff-116">Alternatively, you can select **Tools** / **Create MSI**.</span></span>

    <span data-ttu-id="622ff-117">**Hinweis**  Wenn Sie **Tools** / **Create MSI** auswählen, um eine neue Windows Installer-Datei zu erstellen, können Sie **Schritt 6** dieses Verfahrens überspringen.</span><span class="sxs-lookup"><span data-stu-id="622ff-117">**Note** If you select **Tools** / **Create MSI** to create a new Windows Installer file, you can skip **Step 6** of this procedure.</span></span>

     

6.  <span data-ttu-id="622ff-118">Zum Speichern des virtuellen Anwendungspakets wählen Sie **Paket**  /  **Speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="622ff-118">To save the virtual application package, select **Package** / **Save**.</span></span>

## <span data-ttu-id="622ff-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="622ff-119">Related topics</span></span>


[<span data-ttu-id="622ff-120">Aufgaben für den Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="622ff-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





