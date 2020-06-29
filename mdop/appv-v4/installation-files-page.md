---
title: Seite „Installationsdateien“
description: Seite „Installationsdateien“
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806668"
---
# <span data-ttu-id="142fe-103">Seite „Installationsdateien“</span><span class="sxs-lookup"><span data-stu-id="142fe-103">Installation Files Page</span></span>


<span data-ttu-id="142fe-104">Auf der Seite " **Installationsdateien** " können Sie die Installationsdateien angeben, die zum Erstellen des virtuellen Anwendungspakets verwendet wurden, das auf der Seite **"Paket auswählen** " dieses Assistenten angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="142fe-104">Use the **Installation Files** page to specify the installation files that were used to create the virtual application package specified on the **Select Package** page of this wizard.</span></span> <span data-ttu-id="142fe-105">Wenn Sie ein virtuelles Anwendungspaket erstellt haben, das mehrere Anwendungen enthält, sollten Sie alle erforderlichen Installationsdateien in einen einzelnen Ordner auf dem Computer kopieren, auf dem der Microsoft Application Virtualization Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="142fe-105">If you created a virtual application package that contains multiple applications, you should copy all required installation files to a single folder on the computer running the Microsoft Application Virtualization Sequencer.</span></span>

<span data-ttu-id="142fe-106">Diese Seite enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="142fe-106">This page contains the following elements:</span></span>

<a href="" id="original-installation-files"></a>**<span data-ttu-id="142fe-107">Ursprüngliche Installationsdateien</span><span class="sxs-lookup"><span data-stu-id="142fe-107">Original Installation Files</span></span>**  
<span data-ttu-id="142fe-108">Klicken Sie auf **Durchsuchen** , um die Installationsdateien anzugeben, die ursprünglich zum Erstellen des virtuellen Anwendungspakets verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="142fe-108">Click **Browse** to specify the installation files that were originally used to create the virtual application package.</span></span> <span data-ttu-id="142fe-109">Das von Ihnen angegebene übergeordnete Verzeichnis sollte lokal auf dem Computer gespeichert werden, auf dem der Sequencer ausgeführt wird, und muss alle erforderlichen Installationsdateien oder Unterordner enthalten, die die Installationsdateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="142fe-109">The parent directory you specify should be saved locally to the computer running the Sequencer and must contain all required installation files or subfolders that contain the installation files.</span></span> <span data-ttu-id="142fe-110">Die Installationsdateien können im übergeordneten Ordner oder in einem der Unterordner des angegebenen übergeordneten Ordners enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="142fe-110">The installation files can be contained in the parent folder or in any of the subfolders of the specified parent folder.</span></span>

<a href="" id="files-installed-on-local-system"></a>**<span data-ttu-id="142fe-111">Auf dem lokalen System installierte Dateien</span><span class="sxs-lookup"><span data-stu-id="142fe-111">Files installed on local system</span></span>**  
<span data-ttu-id="142fe-112">Klicken Sie auf **Durchsuchen** , um die Installationsdateien anzugeben, die lokal auf dem Computer installiert wurden, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="142fe-112">Click **Browse** to specify the installation files that have been installed locally on the computer running the Sequencer.</span></span> <span data-ttu-id="142fe-113">Sie können diese Option nur auswählen, wenn die Installationsdateien der Anwendung im Standardspeicherort der Anwendung installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="142fe-113">You can only select this option if the application installation files have been installed to the application’s default location.</span></span>

<span data-ttu-id="142fe-114">**Hinweis**  Der von Ihnen bereitgestellte Standard Installationsspeicherort hängt von den folgenden Bedingungen ab:</span><span class="sxs-lookup"><span data-stu-id="142fe-114">**Note** The default installation location you provide depends on the following conditions:</span></span>

 

-   <span data-ttu-id="142fe-115">Der Paketstamm, der beim ursprünglichen Erstellen des Pakets angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="142fe-115">The package root specified when the package was originally created.</span></span>

-   <span data-ttu-id="142fe-116">Der Installationsspeicherort, der beim ursprünglichen Erstellen des Pakets im Windows Installer angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="142fe-116">The installation location specified in the Windows Installer when the package was originally created.</span></span>

-   <span data-ttu-id="142fe-117">Der Standardinstallationspfad der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="142fe-117">The default application installation path.</span></span>

<span data-ttu-id="142fe-118">Wenn beispielsweise der angegebene Paketstamm **Q:\\Office12** ist und während der Installation der Standard Installationsspeicherort von **c:\\Programme Files\\Office12** in **Q:\\Office12**geändert wird, muss der während der Dehydratisierung angegebene Pfad **c:\\Programme Files\\Office 12**sein.</span><span class="sxs-lookup"><span data-stu-id="142fe-118">For example, if the package root specified is **Q:\\Office12** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Office12**, then the path specified during dehydration must be **C:\\Program Files\\Office 12**.</span></span>

<span data-ttu-id="142fe-119">Wenn der angegebene Paketstamm **Q:\\Microsoft** ist und während der Installation der Standard Installationsspeicherort von **c:\\Programme Files\\Office12** in **Q:\\Microsoft\\Office12**geändert wird, muss der während der Dehydratisierung angegebene Pfad **c:\\Programme Dateien**sein.</span><span class="sxs-lookup"><span data-stu-id="142fe-119">If the package root specified is **Q:\\Microsoft** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Microsoft\\Office12**, then the path specified during dehydration must be **C:\\Program Files**.</span></span>

<span data-ttu-id="142fe-120">Wenn Sie ein Paket mithilfe eines Paket Beschleunigers erstellen, wird jede Datei im Paket, beispielsweise **Q:\\Office12\\file.txt** auf dem lokalen Computer gefunden, indem das Paketstamm **Q:\\Office12** durch den Standardspeicherort ersetzt wird, der beim Erstellen des Paket Beschleunigers angegeben wurde, beispielsweise **c:\\Programme Files\\Office12**.</span><span class="sxs-lookup"><span data-stu-id="142fe-120">When you create a package using a package accelerator, each file in the package, for example **Q:\\Office12\\file.txt** is found on the local computer by replacing the package root **Q:\\Office12** with the default location specified when the Package Accelerator was created, for example, **C:\\Program Files\\Office12**.</span></span> <span data-ttu-id="142fe-121">Im vorherigen Beispiel sollte sich die Datei in **c:\\Programme Files\\Office12\\file.txt**befinden.</span><span class="sxs-lookup"><span data-stu-id="142fe-121">In the previous example, the file should be located in **C:\\Program Files\\Office12\\file.txt**.</span></span>

## <span data-ttu-id="142fe-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="142fe-122">Related topics</span></span>


[<span data-ttu-id="142fe-123">Assistent „Package Accelerator erstellen“ (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="142fe-123">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





