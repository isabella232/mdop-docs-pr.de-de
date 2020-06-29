---
title: So sequenzieren Sie ein neues Anwendungspaket über die Befehlszeile
description: So sequenzieren Sie ein neues Anwendungspaket über die Befehlszeile
author: dansimp
ms.assetid: de72912b-d9e7-45b5-a601-12528f1a4cac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2dd638a7e4765cedbf1d8050626fb8cc54b2ce8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806803"
---
# <span data-ttu-id="a8a92-103">So sequenzieren Sie ein neues Anwendungspaket über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="a8a92-103">How to Sequence a New Application Package Using the Command Line</span></span>


<span data-ttu-id="a8a92-104">Sie können eine Befehlszeile verwenden, um eine neue Anwendung zu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="a8a92-104">You can use a command line to sequence a new application.</span></span> <span data-ttu-id="a8a92-105">Die Verwendung einer Befehlszeile ist hilfreich, wenn Sie eine große Anzahl von virtuellen Anwendungen erstellen müssen oder wenn Sie sequenzierte Anwendungen regelmäßig erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="a8a92-105">Using a command line is useful when you have to create a large number of virtual applications or when you need to create sequenced applications on a recurring basis.</span></span>

**<span data-ttu-id="a8a92-106">Wichtig</span><span class="sxs-lookup"><span data-stu-id="a8a92-106">Important</span></span>**  
<span data-ttu-id="a8a92-107">Die Befehlszeilen-Sequenzierung ermöglicht nur die standardmäßige Sequenzierung.</span><span class="sxs-lookup"><span data-stu-id="a8a92-107">Command-line sequencing allows for default sequencing only.</span></span> <span data-ttu-id="a8a92-108">Wenn Sie die Standardinstallationseinstellungen für die von Ihnen sequenzierte Anwendung ändern müssen, müssen Sie entweder die virtuelle Anwendung manuell ändern oder die virtuelle Anwendung mithilfe von Application Virtualization (App-V) Sequencer aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a8a92-108">If you need to change default installation settings for the application you are sequencing, you must either manually modify the virtual application or update the virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="a8a92-109">Weitere Informationen zum Aktualisieren einer virtuellen Anwendung mithilfe von App-V Sequencer finden Sie unter [Aktualisieren einer vorhandenen virtuellen Anwendung](how-to-upgrade-an-existing-virtual-application.md).</span><span class="sxs-lookup"><span data-stu-id="a8a92-109">For more information about updating a virtual application by using the App-V Sequencer, see [How to Upgrade an Existing Virtual Application](how-to-upgrade-an-existing-virtual-application.md).</span></span>



<span data-ttu-id="a8a92-110">Gehen Sie wie folgt vor, um eine virtuelle Anwendung mithilfe der Befehlszeile zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8a92-110">Use the following procedure to create a virtual application by using the command line.</span></span>

**<span data-ttu-id="a8a92-111">So Sequenzieren Sie eine Anwendung mithilfe der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="a8a92-111">To sequence an application by using the command line</span></span>**

1.  <span data-ttu-id="a8a92-112">Öffnen Sie auf dem Computer, auf dem der App-V-Sequencer ausgeführt wird, die Eingabeaufforderung, indem Sie **Start**, **Ausführen**und dann **cmd**eingeben.</span><span class="sxs-lookup"><span data-stu-id="a8a92-112">On the computer that is running the App-V Sequencer, open the command prompt by selecting **Start**, **Run**, and then type **cmd**.</span></span> <span data-ttu-id="a8a92-113">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8a92-113">Click **OK**.</span></span>

2.  <span data-ttu-id="a8a92-114">Verwenden Sie die Eingabeaufforderung, um den Speicherort anzugeben, an dem der App-V-Sequencer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a8a92-114">Use the command prompt to specify the location of where the App-V Sequencer is installed.</span></span> <span data-ttu-id="a8a92-115">Geben Sie beispielsweise an der Eingabeaufforderung Folgendes ein: **CD c:\\Programme c:\\Programme\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="a8a92-115">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="a8a92-116">Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, und ersetzen Sie den Text in Anführungszeichen durch ihre Werte:</span><span class="sxs-lookup"><span data-stu-id="a8a92-116">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="a8a92-117">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="a8a92-117">Note</span></span>**  
    <span data-ttu-id="a8a92-118">Sie können zusätzliche Parameter mithilfe der Befehlszeile angeben, abhängig von der Komplexität der Anwendung, die Sie sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="a8a92-118">You can specify additional parameters by using the command line, depending on the complexity of the application you are sequencing.</span></span> <span data-ttu-id="a8a92-119">Eine vollständige Liste der Parameter, die für die Verwendung mit dem App-V-Sequenzer verfügbar sind, finden Sie unter [Befehlszeile für Application Virtualization Sequencer](application-virtualization-sequencer-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="a8a92-119">For a complete list of parameters that are available for use with the App-V Sequencer, see [Application Virtualization Sequencer Command Line](application-virtualization-sequencer-command-line.md).</span></span>



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
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specifies the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="a8a92-120">Drücken **Sie die Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="a8a92-120">Press **Enter**.</span></span>

## <span data-ttu-id="a8a92-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a8a92-121">Related topics</span></span>


[<span data-ttu-id="a8a92-122">So verwalten Sie virtuellen Anwendungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="a8a92-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









