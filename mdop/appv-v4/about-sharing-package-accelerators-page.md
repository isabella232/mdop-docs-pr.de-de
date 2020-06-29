---
title: Seite „Informationen zur Package Accelerator-Freigabe“
description: Seite „Informationen zur Package Accelerator-Freigabe“
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808128"
---
# <span data-ttu-id="3a7ee-103">Seite „Informationen zur Package Accelerator-Freigabe“</span><span class="sxs-lookup"><span data-stu-id="3a7ee-103">About Sharing Package Accelerators Page</span></span>


<span data-ttu-id="3a7ee-104">Die folgenden Informationen enthalten bewährte Methoden zum Freigeben von Paket Beschleunigern.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-104">This following information provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="3a7ee-105">Wenn Sie die Paket Beschleunigerdateien freigeben möchten, können Informationen wie Computernamen, Benutzerkontoinformationen und Informationen zu den in den Transformationen enthaltenen Anwendungen in der Paket Beschleunigerdatei enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-105">If you plan to share Package Accelerators files, information such as computer names, user account information, and information about applications included in the transforms might be included in the Package Accelerators file.</span></span> <span data-ttu-id="3a7ee-106">Überprüfen Sie alle Einstellungen oder Konfigurationsdateien, die dem virtuellen Anwendungspaket zugeordnet sind, um sicherzustellen, dass die Anwendungen keine persönlichen Informationen enthalten. Diese Seite enthält die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-106">You should review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.This page contains the following elements.</span></span>

-   <span data-ttu-id="3a7ee-107">**Benutzername**.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-107">**Username**.</span></span> <span data-ttu-id="3a7ee-108">Wenn Sie sich bei dem Computer anmelden, auf dem Microsoft App-V Sequencer ausgeführt wird, sollten Sie ein generisches Benutzerkonto verwenden, beispielsweise das integrierte **Administrator** Konto.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-108">When you log on to the computer running the Microsoft App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account.</span></span> <span data-ttu-id="3a7ee-109">Sie sollten kein Konto verwenden, das auf einem vorhandenen Benutzernamen basiert.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-109">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="3a7ee-110">**Computer Name**</span><span class="sxs-lookup"><span data-stu-id="3a7ee-110">**Computer Name**.</span></span> <span data-ttu-id="3a7ee-111">Geben Sie einen allgemeinen, nicht identifizierbaren Namen des Computers an, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-111">Specify a general, non-identifying name of the computer running the Sequencer.</span></span>

-   <span data-ttu-id="3a7ee-112">**Server-URL**.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-112">**Server URL**.</span></span> <span data-ttu-id="3a7ee-113">Verwenden Sie in der App-V Sequencer-Konsole auf der Registerkarte **Bereitstellung** die Standardeinstellungen für die Konfigurationsinformationen der Server-URL.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-113">In the App-V Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="3a7ee-114">**Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-114">**Applications**.</span></span> <span data-ttu-id="3a7ee-115">Wenn Sie die Liste der Anwendungen, die auf dem Computer installiert waren, auf dem der Sequencer ausgeführt wurde, beim Erstellen des Paket Beschleunigers nicht freigeben möchten, müssen Sie die **appv\_manifest.xml** -Datei löschen.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-115">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="3a7ee-116">Diese Datei befindet sich im Paketstammverzeichnis des virtuellen Anwendungspakets.</span><span class="sxs-lookup"><span data-stu-id="3a7ee-116">This file is located in the package root directory of the virtual application package.</span></span>

## <span data-ttu-id="3a7ee-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3a7ee-117">Related topics</span></span>


[<span data-ttu-id="3a7ee-118">Assistent „Package Accelerator erstellen“ (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="3a7ee-118">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

[<span data-ttu-id="3a7ee-119">Informationen zu App-V Package Accelerators (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="3a7ee-119">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





