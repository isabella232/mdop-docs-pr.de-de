---
title: So aktualisieren Sie eine virtuelle Anwendung über die Befehlszeile
description: So aktualisieren Sie eine virtuelle Anwendung über die Befehlszeile
author: dansimp
ms.assetid: 83c97767-6ea1-42aa-b411-ccc9fa61cf81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8612deb31a1692dd85cfee88ca4b18cbc5ac2ab2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806716"
---
# <span data-ttu-id="3affe-103">So aktualisieren Sie eine virtuelle Anwendung über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="3affe-103">How to Upgrade a Virtual Application by Using the Command Line</span></span>


<span data-ttu-id="3affe-104">Gehen Sie wie folgt vor, um eine virtuelle Anwendung mithilfe einer Befehlszeile zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3affe-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span>

**<span data-ttu-id="3affe-105">So aktualisieren Sie eine virtuelle Anwendung</span><span class="sxs-lookup"><span data-stu-id="3affe-105">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="3affe-106">Klicken Sie auf dem Computer, auf dem Application Virtualization (App-V) Sequencer ausgeführt wird, zum Öffnen der Eingabeaufforderung auf **Start**, **Ausführen**und geben Sie **cmd**ein.</span><span class="sxs-lookup"><span data-stu-id="3affe-106">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="3affe-107">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3affe-107">Click **OK**.</span></span>

2.  <span data-ttu-id="3affe-108">Geben Sie an der Eingabeaufforderung den Ort an, an dem der App-V-Sequencer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3affe-108">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="3affe-109">Geben Sie beispielsweise an der Eingabeaufforderung Folgendes ein: **CD c:\\Programme c:\\Programme\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="3affe-109">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="3affe-110">Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, und ersetzen Sie den Text in Anführungszeichen durch ihre Werte:</span><span class="sxs-lookup"><span data-stu-id="3affe-110">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="3affe-111">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3affe-111">Note</span></span>**  
    <span data-ttu-id="3affe-112">Sie können zusätzliche Parameter über die Befehlszeile angeben, abhängig von der Komplexität der Anwendung, die Sie aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3affe-112">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="3affe-113">Eine vollständige Liste der Parameter, die für die Verwendung mit dem App-V-Sequenzer verfügbar sind, finden Sie unter [Befehlszeilenparameter für Sequencer](sequencer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3affe-113">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



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



4. <span data-ttu-id="3affe-114">Drücken **Sie die Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="3affe-114">Press **Enter**.</span></span>

## <span data-ttu-id="3affe-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3affe-115">Related topics</span></span>


[<span data-ttu-id="3affe-116">Erstellen oder Aktualisieren virtueller Anwendungen mit dem App-V-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="3affe-116">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="3affe-117">Sequencer-Befehlszeilenfehlercodes</span><span class="sxs-lookup"><span data-stu-id="3affe-117">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="3affe-118">Sequencer Befehlszeilenparameter</span><span class="sxs-lookup"><span data-stu-id="3affe-118">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









