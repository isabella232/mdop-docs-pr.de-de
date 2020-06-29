---
title: So installieren Sie den App-V-Client mithilfe von Setup.exe
description: So installieren Sie den App-V-Client mithilfe von Setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807067"
---
# <span data-ttu-id="18605-103">So installieren Sie den App-V-Client mithilfe von Setup.exe</span><span class="sxs-lookup"><span data-stu-id="18605-103">How to Install the App-V Client by Using Setup.exe</span></span>


<span data-ttu-id="18605-104">In diesem Thema wird beschrieben, wie Sie den App-V-Client mit dem setup.exe-Programm installieren.</span><span class="sxs-lookup"><span data-stu-id="18605-104">This topic describes how to install the App-V client by using the setup.exe program.</span></span> <span data-ttu-id="18605-105">Wenn Sie den App-V-Client mit dem setup.exe-Programm installieren, ermittelt das Installationsprogramm, welche erforderliche Software erforderlich ist, und installiert sie automatisch, bevor der Client installiert wird.</span><span class="sxs-lookup"><span data-stu-id="18605-105">When you install the App-V client using the setup.exe program, the installer determines which prerequisite software is needed and installs it automatically before it installs the client.</span></span>

**<span data-ttu-id="18605-106">So installieren Sie den Application Virtualization-Client mithilfe von Setup.exe</span><span class="sxs-lookup"><span data-stu-id="18605-106">To install the Application Virtualization Client by Using Setup.exe</span></span>**

1.  <span data-ttu-id="18605-107">Stellen Sie sicher, dass Sie mit einem Konto angemeldet sind, das über Administratorrechte auf dem Computer verfügt.</span><span class="sxs-lookup"><span data-stu-id="18605-107">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="18605-108">Öffnen Sie ein Eingabeaufforderungsfenster, und ändern Sie das Verzeichnis in den Ordner, in dem die Setupdateien enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="18605-108">Open a Command Prompt window, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="18605-109">Wenn Sie Version 4.6 oder eine neuere Version des App-V-Clients installieren, müssen Sie das richtige Installationsprogramm für das Betriebssystem des Computers, 32-Bit oder 64-Bit verwenden.</span><span class="sxs-lookup"><span data-stu-id="18605-109">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="18605-110">Bei der Installation tritt ein Fehler auf, und es wird eine Fehlermeldung angezeigt, wenn Sie das falsche Installationsprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="18605-110">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="18605-111">Geben Sie die Befehlszeichenfolge für den Installationsbefehl an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="18605-111">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="18605-112">Alternativ können Sie eine Befehlsdatei erstellen und diese über die Eingabeaufforderung ausführen.</span><span class="sxs-lookup"><span data-stu-id="18605-112">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="18605-113">Sie können auch eine Skriptsprache wie VBScript oder Windows PowerShell verwenden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="18605-113">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="18605-114">Das folgende Befehlszeilenbeispiel zeigt, wie setup.exe mit einer Reihe optionaler Parameter verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18605-114">The following command-line example shows how setup.exe can be used with a number of optional parameters.</span></span> <span data-ttu-id="18605-115">Weitere Informationen zu diesen Parametern finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="18605-115">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="18605-116">"setup.exe"/s/v "/qn SWICACHESIZE = \ \" 10240 \ \ "SWIPUBSVRDISPLAY = \ \" Production System\\ "SWIPUBSVRTYPE = \ \" http/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \ \" ^% LocalAppData ^%\\Windows\\Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""</span><span class="sxs-lookup"><span data-stu-id="18605-116">"setup.exe" /s /v"/qn SWICACHESIZE=\\"10240\\" SWIPUBSVRDISPLAY=\\"Production System\\" SWIPUBSVRTYPE=\\"HTTP /secure\\" SWIPUBSVRHOST=\\"PRODSYS\\" SWIPUBSVRPORT=\\"443\\" SWIPUBSVRPATH=\\"/AppVirt/appsntype.xml\\" SWIPUBSVRREFRESH=\\"on\\" SWIGLOBALDATA=\\"D:\\AppVirt\\Global\\" SWIUSERDATA=\\"^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\" SWIFSDRIVE=\\"Q\\""</span></span>**

    **<span data-ttu-id="18605-117">Wichtig</span><span class="sxs-lookup"><span data-stu-id="18605-117">Important</span></span>**  
    -   <span data-ttu-id="18605-118">Die Anführungszeichen, die im Abschnitt "**/v**" angezeigt werden, müssen als Sonderzeichen behandelt und mit einem vorangehenden "" eingegeben werden **\\** .</span><span class="sxs-lookup"><span data-stu-id="18605-118">The quotation marks that appear in the "**/v**" section must be treated as special characters and entered with a preceding "**\\**".</span></span> <span data-ttu-id="18605-119">Die Anführungszeichen sind nur erforderlich, wenn der Wert ein Leerzeichen enthält. aus Gründen der Konsistenz werden jedoch alle Instanzen im vorherigen Beispiel als Anführungszeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18605-119">The quotation marks are required only when the value contains a space; however, for consistency, all the instances in the preceding example are shown as having quotation marks.</span></span>

    -   <span data-ttu-id="18605-120">Dem "" " **%** -Zeichen in"**% HOMEDRIVE%**"muss das Escapezeichen" "vorangestellt werden **^** .</span><span class="sxs-lookup"><span data-stu-id="18605-120">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="18605-121">Andernfalls legt die Windows-Befehlsshell den Wert auf den Wert des Benutzers fest, der die Installation ausführt.</span><span class="sxs-lookup"><span data-stu-id="18605-121">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="18605-122">Die **InstallShield** -Schalter **/s** und **/QN** sind erforderlich, um eine unbeaufsichtigte Installation zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="18605-122">The **InstallShield** switches **/s** and **/qn** are needed to make this a silent install.</span></span> <span data-ttu-id="18605-123">Der **/QN** -Schalter muss dem **/v** -Schalter folgen, getrennt durch ein Anführungszeichen ohne dazwischen liegende Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="18605-123">The **/qn** switch must follow the **/v** switch, separated by only a quote character with no intervening spaces.</span></span>

    -   <span data-ttu-id="18605-124">Der im **SWIGLOBALDATA** -Wert angegebene Ordner muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="18605-124">The folder specified in the **SWIGLOBALDATA** value must already exist.</span></span>

     

5.  <span data-ttu-id="18605-125">Wenn die Installation abgeschlossen ist, empfehlen wir, dass Sie einen Microsoft Update-Scan ausführen, um sicherzustellen, dass die neuesten Updates installiert sind.</span><span class="sxs-lookup"><span data-stu-id="18605-125">When the installation is complete, we recommend that you run a Microsoft Update scan to ensure the latest updates are installed.</span></span>

## <span data-ttu-id="18605-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="18605-126">Related topics</span></span>


[<span data-ttu-id="18605-127">So installieren Sie den Client über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="18605-127">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





