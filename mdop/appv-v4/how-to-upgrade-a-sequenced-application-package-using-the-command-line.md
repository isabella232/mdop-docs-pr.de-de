---
title: So aktualisieren Sie ein sequenziertes Anwendungspaket über die Befehlszeile
description: So aktualisieren Sie ein sequenziertes Anwendungspaket über die Befehlszeile
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806727"
---
# <span data-ttu-id="4eebf-103">So aktualisieren Sie ein sequenziertes Anwendungspaket über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="4eebf-103">How to Upgrade a Sequenced Application Package Using the Command Line</span></span>


<span data-ttu-id="4eebf-104">Gehen Sie wie folgt vor, um eine virtuelle Anwendung mithilfe einer Befehlszeile zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4eebf-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span> <span data-ttu-id="4eebf-105">Wenn Sie ein vorhandenes virtuelles Anwendungspaket über die Befehlszeile aktualisieren, wird die ursprüngliche Version der SFT-Datei gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4eebf-105">When you upgrade an existing virtual application package by using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="4eebf-106">Sie sollten die zugehörige SFT-Datei sichern, bevor Sie das Paket über die Befehlszeile aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4eebf-106">You should back up the associated .sft file before upgrading the package by using the command line.</span></span>

**<span data-ttu-id="4eebf-107">So aktualisieren Sie eine virtuelle Anwendung</span><span class="sxs-lookup"><span data-stu-id="4eebf-107">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="4eebf-108">Klicken Sie auf dem Computer, auf dem Application Virtualization (App-V) Sequencer ausgeführt wird, zum Öffnen der Eingabeaufforderung auf **Start**, **Ausführen**und geben Sie **cmd**ein.</span><span class="sxs-lookup"><span data-stu-id="4eebf-108">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="4eebf-109">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4eebf-109">Click **OK**.</span></span>

2.  <span data-ttu-id="4eebf-110">Geben Sie an der Eingabeaufforderung den Ort an, an dem der App-V-Sequencer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4eebf-110">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="4eebf-111">Geben Sie beispielsweise an der Eingabeaufforderung Folgendes ein: **CD c:\\Programme c:\\Programme\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="4eebf-111">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="4eebf-112">Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, und ersetzen Sie den Text in Anführungszeichen durch ihre Werte:</span><span class="sxs-lookup"><span data-stu-id="4eebf-112">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="4eebf-113">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4eebf-113">Note</span></span>**  
    <span data-ttu-id="4eebf-114">Sie können zusätzliche Parameter über die Befehlszeile angeben, abhängig von der Komplexität der Anwendung, die Sie aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4eebf-114">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="4eebf-115">Eine vollständige Liste der Parameter, die für die Verwendung mit dem App-V-Sequenzer verfügbar sind, finden Sie unter [Befehlszeilenparameter](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4eebf-115">For a complete list of parameters that are available for use with the App-V Sequencer, see [Command-Line Parameters](command-line-parameters.md).</span></span>



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="4eebf-116">Drücken **Sie die Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="4eebf-116">Press **Enter**.</span></span>

## <span data-ttu-id="4eebf-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4eebf-117">Related topics</span></span>


[<span data-ttu-id="4eebf-118">So verwalten Sie virtuellen Anwendungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="4eebf-118">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









