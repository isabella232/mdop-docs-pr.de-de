---
title: Liste auszuschließender Anwendungen für virtuelle Windows-PCs
description: Liste auszuschließender Anwendungen für virtuelle Windows-PCs
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810108"
---
# <span data-ttu-id="38a06-103">Liste auszuschließender Anwendungen für virtuelle Windows-PCs</span><span class="sxs-lookup"><span data-stu-id="38a06-103">Windows Virtual PC Application Exclude List</span></span>


<span data-ttu-id="38a06-104">In einigen Fällen möchten Sie möglicherweise nicht, dass im MED-V-Arbeitsbereich installierte Anwendungen im **Startmenü** des Hostcomputers veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="38a06-104">In some instances, you might not want applications that are installed in the MED-V workspace to be published to the host computer **Start** menu.</span></span> <span data-ttu-id="38a06-105">Sie können die Veröffentlichung dieser Anwendungen aufheben, indem Sie die Anweisungen unter Veröffentlichen und Aufheben der [Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)befolgen.</span><span class="sxs-lookup"><span data-stu-id="38a06-105">You can unpublish these applications by following the instructions at [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span> <span data-ttu-id="38a06-106">Wenn das Programm allerdings immer automatisch aktualisiert wird, wird es möglicherweise auch automatisch erneut veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="38a06-106">However, if the program ever automatically updates, it might also be automatically republished.</span></span> <span data-ttu-id="38a06-107">Dies führt dazu, dass Sie die Veröffentlichung der Anwendung erneut aufheben müssen.</span><span class="sxs-lookup"><span data-stu-id="38a06-107">This causes you to have to unpublish the application again.</span></span>

<span data-ttu-id="38a06-108">Windows Virtual PC enthält ein Feature, das als "Ausschlussliste" bezeichnet wird, mit der Sie bestimmte installierte Anwendungen angeben können, die nicht **im Startmenü des Hosts veröffentlicht** werden sollen.</span><span class="sxs-lookup"><span data-stu-id="38a06-108">Windows Virtual PC includes a feature known as the "Exclude List" that lets you specify certain installed applications that you do not want published to the host **Start** menu.</span></span> <span data-ttu-id="38a06-109">Die "Ausschlussliste" befindet sich in der gastregistrierung im HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList-Schlüssel und listet die Anwendungen auf, die nicht im **Start** Menü des Hosts veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="38a06-109">The "Exclude List" is located in the guest registry in the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList key and lists those applications that are not published to the host **Start** menu.</span></span> <span data-ttu-id="38a06-110">Sie können sich die "Ausschlussliste" als permanente Aufhebung der Veröffentlichung der angegebenen Anwendungen vorstellen, da automatische Updates für die aufgelisteten Anwendungen nicht dazu führen, dass Sie automatisch erneut veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="38a06-110">You can think of the “Exclude List” as permanently unpublishing the specified applications because any automatic updates to the applications that are listed will not cause them to be automatically republished.</span></span>

## <span data-ttu-id="38a06-111">Verwalten von Anwendungen mithilfe der Ausschlussliste in Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="38a06-111">Managing Applications by Using the Exclude List in Windows Virtual PC</span></span>


****

1.  <span data-ttu-id="38a06-112">Öffnen Sie den Arbeitsbereich MED-V im Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="38a06-112">Open the MED-V workspace in full screen.</span></span>

    <span data-ttu-id="38a06-113">Informationen zum Öffnen des Med-v-Arbeitsbereichs im Vollbildmodus mithilfe des Med-v-Administrations-Toolkits finden Sie unter [Anzeigen von Med-v-Arbeitsbereichskonfigurationen](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span><span class="sxs-lookup"><span data-stu-id="38a06-113">For information about opening the MED-V workspace in full-screen mode by using the MED-V Administration Toolkit, see [Viewing MED-V Workspace Configurations](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span></span> <span data-ttu-id="38a06-114">Sie können Sie aber auch manuell im Vollbildmodus öffnen, indem Sie auf **Start**, dann auf **Alle Programme**, auf **Windows Virtual PC**, auf **Windows Virtual PC**und dann auf den MED-V-Arbeitsbereich doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="38a06-114">Or you can manually open it in full screen by clicking **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, and then double-click the MED-V workspace.</span></span>

2.  <span data-ttu-id="38a06-115">Öffnen Sie im Windows Virtual PC-Fenster des MED-V Workspace den Registrierungs-Editor.</span><span class="sxs-lookup"><span data-stu-id="38a06-115">In the MED-V workspace Windows Virtual PC window, open Registry Editor.</span></span>

    <span data-ttu-id="38a06-116">Klicken Sie auf **Start**, klicken Sie auf **Ausführen**, und geben Sie dann regedit ein.</span><span class="sxs-lookup"><span data-stu-id="38a06-116">Click **Start**, click **Run**, and then type regedit.</span></span> <span data-ttu-id="38a06-117">Klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="38a06-117">Then click **OK**.</span></span>

3.  <span data-ttu-id="38a06-118">Suchen Sie im Registrierungs-Editor den Registrierungsschlüssel HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="38a06-118">In Registry Editor, locate the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList registry key.</span></span>

4.  <span data-ttu-id="38a06-119">Erstellen Sie einen neuen Registrierungswert für die installierte Anwendung, die nicht im **Startmenü** des Hostcomputers veröffentlicht werden soll.</span><span class="sxs-lookup"><span data-stu-id="38a06-119">Create a new registry value for the installed application that you do not want published to the host computer **Start** menu.</span></span> <span data-ttu-id="38a06-120">Wenn Sie beispielsweise die Veröffentlichung des automatisch veröffentlichten Programms Microsoft Silverlight aufheben möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="38a06-120">For example, if you want to unpublish the automatically published program Microsoft Silverlight, follow these steps:</span></span>

    1.  <span data-ttu-id="38a06-121">Klicken Sie mit hervorgehobenem VPCVAppExcludeList-Registrierungsschlüssel auf **Bearbeiten**, klicken Sie auf **neu**, und klicken Sie dann auf **Zeichenfolgenwert**.</span><span class="sxs-lookup"><span data-stu-id="38a06-121">With the VPCVAppExcludeList registry key highlighted, click **Edit**, click **New**, and then click **String Value**.</span></span>

    2.  <span data-ttu-id="38a06-122">Geben Sie den Namen für den neuen Registrierungswert ein.</span><span class="sxs-lookup"><span data-stu-id="38a06-122">Enter the name for the new registry value.</span></span> <span data-ttu-id="38a06-123">Für Microsoft Silverlight können Sie beispielsweise sllauncher.exe eingeben.</span><span class="sxs-lookup"><span data-stu-id="38a06-123">For example, for Microsoft Silverlight, you might enter sllauncher.exe.</span></span>

    3.  <span data-ttu-id="38a06-124">Doppelklicken Sie auf den neuen Registrierungswert, und geben Sie die Wertdaten ein.</span><span class="sxs-lookup"><span data-stu-id="38a06-124">Double-click the new registry value and enter the value data.</span></span>

        <span data-ttu-id="38a06-125">Die Wertdaten sind der vollständige Pfad für den Befehl, dessen Veröffentlichung Sie aufheben möchten.</span><span class="sxs-lookup"><span data-stu-id="38a06-125">The value data is the full path for the command that you want to unpublish.</span></span> <span data-ttu-id="38a06-126">Sie können den vollständigen Pfad finden, indem Sie mit der rechten Maustaste auf die Verknüpfung im **Startmenü** für die Anwendung klicken, die nicht veröffentlicht werden soll, und dann auf **Eigenschaften**klicken.</span><span class="sxs-lookup"><span data-stu-id="38a06-126">You can find the full path by right-clicking on the shortcut on the **Start** menu for the application that you do not want published and then clicking **Properties**.</span></span> <span data-ttu-id="38a06-127">Der vollständige Pfad wird auf der Registerkarte **Verknüpfung** unter **Ziel**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38a06-127">The full path is listed in the **Shortcut** tab under **Target**.</span></span>

        <span data-ttu-id="38a06-128">Für das Programm Microsoft Silverlight kann der vollständige Pfad beispielsweise "c:\\Programme c:\\Programme\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe" sein.</span><span class="sxs-lookup"><span data-stu-id="38a06-128">For example, for the program Microsoft Silverlight, the full path might be "C:\\Program Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."</span></span>

        <span data-ttu-id="38a06-129">**Wichtig**  Falls zutreffend, entfernen Sie die Anführungszeichen aus dem vollständigen Pfad, wenn Sie Sie in das Datenfeld "Wert" eingeben.</span><span class="sxs-lookup"><span data-stu-id="38a06-129">**Important** If applicable, remove the quotation marks from the full path when you enter it into the value data field.</span></span>

         

5.  <span data-ttu-id="38a06-130">Schließen Sie den Registrierungs-Editor, und starten Sie den virtuellen Computer mit dem MED-V Workspace neu.</span><span class="sxs-lookup"><span data-stu-id="38a06-130">Close Registry Editor and restart the MED-V workspace virtual machine.</span></span>

    <span data-ttu-id="38a06-131">Die Anwendung ist weiterhin im MED-V-Arbeitsbereich installiert, wird aber jetzt aus dem **Startmenü** des Hostcomputers entfernt.</span><span class="sxs-lookup"><span data-stu-id="38a06-131">The application is still installed in the MED-V workspace but is now removed from the host computer **Start** menu.</span></span>

<span data-ttu-id="38a06-132">Sie können auch eine ausgeschlossene Anwendung im **Startmenü** des Hosts erneut veröffentlichen, indem Sie den entsprechenden Wert aus dem VPCVAppExcludeList-Schlüssel löschen.</span><span class="sxs-lookup"><span data-stu-id="38a06-132">You can also republish an excluded application to the host **Start** menu by deleting the corresponding value from the VPCVAppExcludeList key.</span></span> <span data-ttu-id="38a06-133">Wenn Sie beispielsweise Microsoft Silverlight erneut veröffentlichen möchten, klicken Sie mit der rechten Maustaste auf den Registrierungswert sllauncher.exe, und wählen Sie **Löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="38a06-133">For example, to republish Microsoft Silverlight, right-click the registry value sllauncher.exe and select **Delete**.</span></span>

## <span data-ttu-id="38a06-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="38a06-134">Related topics</span></span>


[<span data-ttu-id="38a06-135">Technische Referenz für MED-V</span><span class="sxs-lookup"><span data-stu-id="38a06-135">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

[<span data-ttu-id="38a06-136">Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="38a06-136">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





