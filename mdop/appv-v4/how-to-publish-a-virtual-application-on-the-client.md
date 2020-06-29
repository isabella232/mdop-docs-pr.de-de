---
title: So veröffentlichen Sie eine virtuelle Anwendung auf dem Client
description: So veröffentlichen Sie eine virtuelle Anwendung auf dem Client
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806880"
---
# <span data-ttu-id="3b18b-103">So veröffentlichen Sie eine virtuelle Anwendung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="3b18b-103">How to Publish a Virtual Application on the Client</span></span>


<span data-ttu-id="3b18b-104">Wenn Sie Application Virtualization mithilfe eines elektronischen Softwareverteilungssystems bereitstellen, können Sie eines der folgenden Verfahren zum Veröffentlichen eines Anwendungspakets für Ihre Benutzer verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b18b-104">When you deploy Application Virtualization by using an electronic software distribution system, you can use one of the following procedures to publish an application package to your users.</span></span>

**<span data-ttu-id="3b18b-105">So veröffentlichen Sie ein Paket mit einer eigenständigen Windows Installer-Datei</span><span class="sxs-lookup"><span data-stu-id="3b18b-105">To publish a package using a stand-alone Windows Installer file</span></span>**

1.  <span data-ttu-id="3b18b-106">Der Client sollte mit dem *RequireAuthorizationIfCached* -Parameter auf 0 (null) festgelegten installiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b18b-106">The client should be installed with the *REQUIREAUTHORIZATIONIFCACHED* parameter set to 0 (zero).</span></span> <span data-ttu-id="3b18b-107">Weitere Informationen zum Festlegen dieses Parameters finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="3b18b-107">For more information about setting this parameter, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md)</span></span>

2.  <span data-ttu-id="3b18b-108">Kopieren Sie die Windows Installer-Datei und die SFT-Datei in denselben Ordner auf dem Zielcomputer.</span><span class="sxs-lookup"><span data-stu-id="3b18b-108">Copy the Windows Installer file and the SFT file to same folder on the target computer.</span></span>

3.  <span data-ttu-id="3b18b-109">Führen Sie den folgenden Befehl auf dem Computer aus:</span><span class="sxs-lookup"><span data-stu-id="3b18b-109">Run the following command on the computer:</span></span>

    `Msiexec.exe /I "packagename.msi" /q`

**<span data-ttu-id="3b18b-110">So veröffentlichen Sie ein Paket mit Windows Installer und dem Paketmanifest</span><span class="sxs-lookup"><span data-stu-id="3b18b-110">To publish a package using Windows Installer and the package manifest</span></span>**

1.  <span data-ttu-id="3b18b-111">Kopieren Sie die Windows Installer-Datei auf den Zielcomputer und die SFT-Datei auf die Inhaltsfreigabe auf dem Streamingserver.</span><span class="sxs-lookup"><span data-stu-id="3b18b-111">Copy the Windows Installer file to the target computer and the SFT file to the CONTENT share on the streaming server.</span></span>

2.  <span data-ttu-id="3b18b-112">Führen Sie den folgenden Befehl auf dem Computer der einzelnen Benutzer aus:</span><span class="sxs-lookup"><span data-stu-id="3b18b-112">Run the following command on each user’s computer:</span></span>

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    <span data-ttu-id="3b18b-113">**Wichtig**  Bei OVERRIDEURL müssen alle umgekehrten Schrägstriche mit einem vorangehenden umgekehrten Schrägstrich maskiert werden, oder der OVERRIDEURL-Pfad wird nicht richtig analysiert.</span><span class="sxs-lookup"><span data-stu-id="3b18b-113">**Important** For OVERRIDEURL all backslash characters must be escaped using a preceding backslash, or the OVERRIDEURL path will not be parsed correctly.</span></span> <span data-ttu-id="3b18b-114">Außerdem müssen Eigenschaften und Werte als Großbuchstaben eingegeben werden, es sei denn, der Wert ist ein Pfad zu einer Datei.</span><span class="sxs-lookup"><span data-stu-id="3b18b-114">Also, properties and values must be entered as uppercase except where the value is a path to a file.</span></span>

     

**<span data-ttu-id="3b18b-115">So veröffentlichen Sie ein Paket mit SFTMIME</span><span class="sxs-lookup"><span data-stu-id="3b18b-115">To publish a package using SFTMIME</span></span>**

-   <span data-ttu-id="3b18b-116">Führen Sie den folgenden Befehl auf dem Computer des Benutzers aus, um ein Beispiel für das Veröffentlichen einer Anwendung für alle Benutzer auf einem Computer zu finden:</span><span class="sxs-lookup"><span data-stu-id="3b18b-116">For an example of how to publish an application for all users on a computer, run the following command on the user’s computer:</span></span>

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    <span data-ttu-id="3b18b-117">Weitere Informationen zu diesen und anderen SFTMIME-Befehlen finden Sie unter [Befehlsreferenz für SFTMIME](sftmime--command-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3b18b-117">For additional details about these and other SFTMIME commands, see [SFTMIME Command Reference](sftmime--command-reference.md).</span></span>

## <span data-ttu-id="3b18b-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3b18b-118">Related topics</span></span>


[<span data-ttu-id="3b18b-119">Bestimmen der Veröffentlichungsmethode</span><span class="sxs-lookup"><span data-stu-id="3b18b-119">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="3b18b-120">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="3b18b-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="3b18b-121">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="3b18b-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

[<span data-ttu-id="3b18b-122">Szenario für die eigenständige Bereitstellung für Application Virtualization Clients</span><span class="sxs-lookup"><span data-stu-id="3b18b-122">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





