---
title: Informationen zu App-V Package Accelerators (App-V 4.6 SP1)
description: Informationen zu App-V Package Accelerators (App-V 4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808168"
---
# <span data-ttu-id="e87b8-103">Informationen zu App-V Package Accelerators (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="e87b8-103">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="e87b8-104">Sie können App-V-Paket Beschleuniger verwenden, um große komplexe Anwendungen automatisch zu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="e87b8-104">You can use App-V Package Accelerators to automatically sequence large, complex applications.</span></span> <span data-ttu-id="e87b8-105">Darüber hinaus müssen Sie beim Anwenden eines App-V-Paket Beschleunigers nicht immer eine Anwendung manuell installieren, um das virtuelle Anwendungspaket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e87b8-105">Additionally, when you apply an App-V Package Accelerator, you are not always required to manually install an application to create the virtual application package.</span></span>

<span data-ttu-id="e87b8-106">**Hinweis**  In einigen Fällen werden Sie aufgefordert, eine Anwendung lokal auf dem Computer zu installieren, auf dem der App-V-Sequencer ausgeführt wird, bevor Sie den Paket Beschleuniger verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e87b8-106">**Note** In some cases, you are prompted to install an application locally to the computer running the App-V Sequencer before you can use the Package Accelerator.</span></span> <span data-ttu-id="e87b8-107">Wenn Sie eine Anwendung installieren müssen, müssen Sie die Anwendung am Standardspeicherort der Anwendung installieren.</span><span class="sxs-lookup"><span data-stu-id="e87b8-107">If you have to install an application, you must install the application to the application’s default location.</span></span> <span data-ttu-id="e87b8-108">Diese Installation wird nicht von App-V Sequencer überwacht.</span><span class="sxs-lookup"><span data-stu-id="e87b8-108">This installation is not monitored by App-V Sequencer.</span></span> <span data-ttu-id="e87b8-109">Wenn der App-V-Paket Beschleuniger erstellt wird, bestimmt der Autor des Paket Beschleunigers, ob eine Anwendung lokal installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e87b8-109">When the App-V Package Accelerator is created, the author of the Package Accelerator determines whether to install an application locally is required.</span></span>

 

<span data-ttu-id="e87b8-110">App-v Sequencer extrahiert die erforderlichen Dateien aus dem App-v-Paket Beschleuniger und zugehörigen Installationsmedien zum Erstellen eines virtuellen Pakets, ohne die Installation der Anwendung überwachen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="e87b8-110">App-V Sequencer extracts the required files from the App-V Package Accelerator and associated installation media to create a virtual package without having to monitor the installation of the application.</span></span>

<span data-ttu-id="e87b8-111">**Wichtig**  Disclaimer: Microsoft Application Virtualization Sequencer gibt Ihnen keine Lizenzrechte für die Softwareanwendung, die Sie zum Erstellen eines Paket Beschleunigers verwenden.</span><span class="sxs-lookup"><span data-stu-id="e87b8-111">**Important** Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="e87b8-112">Sie müssen sich an alle Endnutzer-Lizenzbestimmungen für diese Anwendung halten.</span><span class="sxs-lookup"><span data-stu-id="e87b8-112">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="e87b8-113">Sie müssen sicherstellen, dass die Lizenzbestimmungen der Softwareanwendung es Ihnen ermöglichen, mithilfe von Application Virtualization Sequencer einen Paket Beschleuniger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e87b8-113">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>

 

<span data-ttu-id="e87b8-114">App-V-Paket Beschleuniger und Projektvorlagen unterscheiden sich voneinander.</span><span class="sxs-lookup"><span data-stu-id="e87b8-114">App-V Package Accelerators and project templates differ from each other.</span></span> <span data-ttu-id="e87b8-115">Paket Beschleuniger sind anwendungsspezifisch.</span><span class="sxs-lookup"><span data-stu-id="e87b8-115">Package Accelerators are application-specific.</span></span> <span data-ttu-id="e87b8-116">Projektvorlagen ermöglichen es Benutzern, häufig verwendete Einstellungen zu speichern, die für eine Organisation spezifisch sind, und Sie auf mehrere Anwendungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="e87b8-116">Project templates enable users to save commonly used settings specific to an organization and apply them to multiple applications.</span></span> <span data-ttu-id="e87b8-117">Sie können auch an der Eingabeaufforderung Projektvorlagen erstellen, während Sie im Gegensatz dazu die App-V Sequencer-Konsole zum Erstellen von Paket Beschleunigern verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="e87b8-117">You can also create project templates at the command prompt, while in contrast, you must use the App-V Sequencer console to create Package Accelerators.</span></span> <span data-ttu-id="e87b8-118">Darüber hinaus wird das Erstellen eines Pakets mithilfe eines Paket Beschleunigers und das Anwenden einer Projektvorlage nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e87b8-118">Additionally, creating a package by using a Package Accelerator and applying a project template is not supported.</span></span>

## <span data-ttu-id="e87b8-119">Freigeben von App-V-Paket Beschleunigern</span><span class="sxs-lookup"><span data-stu-id="e87b8-119">Sharing App-V Package Accelerators</span></span>


<span data-ttu-id="e87b8-120">Dieser Abschnitt enthält bewährte Methoden zum Freigeben von Paket Beschleunigern.</span><span class="sxs-lookup"><span data-stu-id="e87b8-120">This section provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="e87b8-121">Wenn Sie die Paket Beschleuniger freigeben möchten, können Informationen wie Computernamen, Benutzerkontoinformationen und Informationen zu den zugehörigen Anwendungen in den Paket Beschleunigern enthalten sein. in der folgenden Liste werden die Methoden beschrieben, die Sie beim Erstellen von Paket Beschleunigern berücksichtigen sollten:</span><span class="sxs-lookup"><span data-stu-id="e87b8-121">If you plan to share Package Accelerators, information such as computer names, user account information, and information about the associated applications might be included in the Package Accelerators.The following list describes methods you should consider when creating Package Accelerators:</span></span>

-   <span data-ttu-id="e87b8-122">**Benutzername**.</span><span class="sxs-lookup"><span data-stu-id="e87b8-122">**User name**.</span></span> <span data-ttu-id="e87b8-123">Wenn Sie sich bei dem Computer anmelden, auf dem App-V Sequencer ausgeführt wird, sollten Sie ein generisches Benutzerkonto verwenden, beispielsweise das integrierte **Administrator** Konto für die Verwaltung des Computers/der Domäne.</span><span class="sxs-lookup"><span data-stu-id="e87b8-123">When you log on to the computer running App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account for administering the computer / domain.</span></span> <span data-ttu-id="e87b8-124">Sie sollten kein Konto verwenden, das auf einem vorhandenen Benutzernamen basiert.</span><span class="sxs-lookup"><span data-stu-id="e87b8-124">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="e87b8-125">**Computer Name**</span><span class="sxs-lookup"><span data-stu-id="e87b8-125">**Computer Name**.</span></span> <span data-ttu-id="e87b8-126">Geben Sie einen allgemeinen, nicht identifizierbaren Namen für den Computer an, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e87b8-126">Specify a general, non-identifying name for the computer running the Sequencer.</span></span>

-   <span data-ttu-id="e87b8-127">**Server-URL**.</span><span class="sxs-lookup"><span data-stu-id="e87b8-127">**Server URL**.</span></span> <span data-ttu-id="e87b8-128">Verwenden Sie in der Sequencer-Konsole auf der Registerkarte **Bereitstellung** die Standardeinstellungen für die Konfigurationsinformationen der Server-URL.</span><span class="sxs-lookup"><span data-stu-id="e87b8-128">In the Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="e87b8-129">**Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="e87b8-129">**Applications**.</span></span> <span data-ttu-id="e87b8-130">Wenn Sie die Liste der Anwendungen, die auf dem Computer installiert waren, auf dem der Sequencer ausgeführt wurde, beim Erstellen des Paket Beschleunigers nicht freigeben möchten, müssen Sie die **appv\_manifest.xml** -Datei löschen.</span><span class="sxs-lookup"><span data-stu-id="e87b8-130">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="e87b8-131">Diese Datei befindet sich im Paketstammverzeichnis des virtuellen Anwendungspakets.</span><span class="sxs-lookup"><span data-stu-id="e87b8-131">This file is located in the package root directory of the virtual application package.</span></span>

<span data-ttu-id="e87b8-132">Darüber hinaus sollten Sie alle Einstellungen oder Konfigurationsdateien überprüfen, die dem virtuellen Anwendungspaket zugeordnet sind, um sicherzustellen, dass die Anwendungen keine persönlichen Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e87b8-132">You should also review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.</span></span>

## <span data-ttu-id="e87b8-133">Sichern von App-V-Paket Beschleunigern</span><span class="sxs-lookup"><span data-stu-id="e87b8-133">Securing App-V Package Accelerators</span></span>


<span data-ttu-id="e87b8-134">Sie können APP-v-Paket Beschleuniger und alle zugehörigen Installationsmedien immer an einem sicheren Ort im Netzwerk speichern, um die APP-v-Paket Beschleuniger und die Installationsdateien vor Manipulationen oder Beschädigungen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="e87b8-134">Always save App-V Package Accelerators and any associated installation media in a secure location on the network to protect the App-V Package Accelerators and the installation files from being tampered with or becoming corrupted.</span></span> <span data-ttu-id="e87b8-135">Da Paket Beschleuniger auch Kennwort-und benutzerspezifische Informationen enthalten können, müssen Sie App-V-Paket Beschleuniger an einem sicheren Speicherort speichern, und Sie müssen den Paket Beschleuniger digital signieren, nachdem Sie ihn erstellt haben, damit der Herausgeber überprüft werden kann, wenn der Paket Beschleuniger angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e87b8-135">Because Package Accelerators can also contain password and user-specific information, you must save App-V Package Accelerators in a secure location, and you must digitally sign the Package Accelerator after you create it so that the publisher can be verified when the Package Accelerator is applied.</span></span> <span data-ttu-id="e87b8-136">Weitere Informationen zu digitalen Signaturen finden Sie unter [Anwendungsrichtlinien für digitale Signatur Methoden für Common Criteria-Sicherheit](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .</span><span class="sxs-lookup"><span data-stu-id="e87b8-136">For more information about digital signatures, see [Application Guidelines on Digital Signature Practices for Common Criteria Security](https://go.microsoft.com/fwlink/?LinkId=204705) (https://go.microsoft.com/fwlink/?LinkId=204705).</span></span>

## <span data-ttu-id="e87b8-137">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e87b8-137">Related topics</span></span>


[<span data-ttu-id="e87b8-138">So erstellen Sie App-V Package Accelerators (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="e87b8-138">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[<span data-ttu-id="e87b8-139">Anwenden eines Paket Beschleunigers zum Erstellen eines virtuellen Anwendungspakets (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="e87b8-139">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





