---
title: So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile
description: So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806899"
---
# <span data-ttu-id="44cd4-103">So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="44cd4-103">How to Open a Sequenced Application Using the Command Line</span></span>


<span data-ttu-id="44cd4-104">Sie können virtuelle Anwendungspakete über die Befehlszeile öffnen.</span><span class="sxs-lookup"><span data-stu-id="44cd4-104">You can open virtual application packages using the command line.</span></span> <span data-ttu-id="44cd4-105">Sie müssen die **cmd** -Eingabeaufforderung als Administrator ausführen.</span><span class="sxs-lookup"><span data-stu-id="44cd4-105">You must run the **cmd** prompt as an administrator.</span></span>

<span data-ttu-id="44cd4-106">Gehen Sie wie folgt vor, um sequenzierte Anwendungspakete über die Befehlszeile zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="44cd4-106">Use the following procedure to open sequenced application packages using the command line</span></span>

**<span data-ttu-id="44cd4-107">So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="44cd4-107">To open a sequenced application using the command line</span></span>**

1.  <span data-ttu-id="44cd4-108">Um die Eingabeaufforderung zu öffnen, klicken Sie auf **Start**, wählen Sie **Ausführen**aus, geben Sie **cmd**ein, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="44cd4-108">To open the command prompt, click **Start**, and select **Run**, type **cmd**, and click **OK**.</span></span>

2.  <span data-ttu-id="44cd4-109">Geben Sie an der Eingabeaufforderung **cd\\** ein, und geben Sie den Pfad zu dem Verzeichnis an, in dem der Sequencer installiert ist, und drücken Sie dann die **EINGABETASTE.**</span><span class="sxs-lookup"><span data-stu-id="44cd4-109">At a command prompt, type **cd\\** and specify the path to the directory where the Sequencer is installed and then press **Enter.**</span></span>

3.  <span data-ttu-id="44cd4-110">Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, und ersetzen Sie den kursiv formatierten Text durch ihre Werte:</span><span class="sxs-lookup"><span data-stu-id="44cd4-110">At the command prompt, type the following command, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="44cd4-111">SFTSequencer/Open:*"gibt die zu öffnende SPRJ-Datei an"*</span><span class="sxs-lookup"><span data-stu-id="44cd4-111">SFTSequencer /OPEN:*”specifies the .sprj file to open"*</span></span>

    <span data-ttu-id="44cd4-112">Drücken **Sie die Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="44cd4-112">Press **Enter**.</span></span>

4.  <span data-ttu-id="44cd4-113">Sie können auch die folgenden optionalen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="44cd4-113">You can also specify the following optional parameters.</span></span> <span data-ttu-id="44cd4-114">Geben Sie an der Eingabeaufforderung die folgenden Befehle ein, und ersetzen Sie den kursiv formatierten Text durch ihre Werte:</span><span class="sxs-lookup"><span data-stu-id="44cd4-114">At the command prompt, type the following commands, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="44cd4-115">/PackageName: "*gibt den Paketnamen an"*</span><span class="sxs-lookup"><span data-stu-id="44cd4-115">/PACKAGENAME:"*specifies the package name"*</span></span>

    <span data-ttu-id="44cd4-116">/MSI – gibt an, dass ein zugeordneter Microsoft Windows Installer generiert wird.</span><span class="sxs-lookup"><span data-stu-id="44cd4-116">/MSI - specifies generating an associated Microsoft Windows Installer.</span></span>

    <span data-ttu-id="44cd4-117">/COMPRESS – gibt an, ob das Paket komprimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="44cd4-117">/COMPRESS – specifies if the package will be compressed.</span></span> <span data-ttu-id="44cd4-118">Standardmäßig werden Pakete nicht komprimiert.</span><span class="sxs-lookup"><span data-stu-id="44cd4-118">By default, packages are not compressed.</span></span>

    <span data-ttu-id="44cd4-119">Drücken **Sie die Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="44cd4-119">Press **Enter**.</span></span>

    <span data-ttu-id="44cd4-120">**Hinweis**  Wenn das Installationsprogramm oder das Windows Installer-Paket über eine grafische Benutzeroberfläche verfügt, wird es angezeigt, nachdem Sie die Befehlszeilenparameter angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="44cd4-120">**Note** If the installer or Windows Installer package has a graphical user interface, it will be displayed after you specify the command-line parameters.</span></span>

     

## <span data-ttu-id="44cd4-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="44cd4-121">Related topics</span></span>


[<span data-ttu-id="44cd4-122">So verwalten Sie virtuellen Anwendungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="44cd4-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





