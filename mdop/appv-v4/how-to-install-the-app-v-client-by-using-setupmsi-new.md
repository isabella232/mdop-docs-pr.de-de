---
title: So installieren Sie App-V-Client mit Setup.msi
description: So installieren Sie App-V-Client mit Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807064"
---
# <span data-ttu-id="cbbdf-103">So installieren Sie App-V-Client mit Setup.msi</span><span class="sxs-lookup"><span data-stu-id="cbbdf-103">How to Install the App-V Client by Using Setup.msi</span></span>


<span data-ttu-id="cbbdf-104">In diesem Thema wird beschrieben, wie Sie den App-V-Client mit dem setup.msi-Programm installieren.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-104">This topic describes how to install the App-V client by using the setup.msi program.</span></span> <span data-ttu-id="cbbdf-105">Bevor Sie den App-V-Client mit dem setup.msi-Programm installieren, müssen Sie zunächst ermitteln, ob eine erforderliche Software installiert werden muss, und Sie müssen Sie installieren.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-105">Before you install the App-V client using the setup.msi program, you must first determine if any prerequisite software must be installed, and then you must install it.</span></span> <span data-ttu-id="cbbdf-106">Informationen zum Installieren der erforderlichen Software finden Sie im Abschnitt [Installieren der erforderlichen Software](#prereq-sw) in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-106">To install the prerequisite software, see the [Installing Prerequisite Software](#prereq-sw) section of this topic.</span></span> <span data-ttu-id="cbbdf-107">Informationen zum Installieren der Client Software finden Sie unter [Installieren des App-V-Clients im Abschnitt Setup.msi Programm](#msi-setup) in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-107">To install the client software, see the [Installing the App-V Client Using the Setup.msi Program](#msi-setup) section of this topic.</span></span>

## <a href="" id="prereq-sw"></a><span data-ttu-id="cbbdf-108">Installieren der erforderlichen Software</span><span class="sxs-lookup"><span data-stu-id="cbbdf-108">Installing Prerequisite Software</span></span>


<span data-ttu-id="cbbdf-109">Mit den folgenden Verfahren können Sie die erforderliche Software installieren.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-109">You can use the following procedures to install the prerequisite software.</span></span> <span data-ttu-id="cbbdf-110">Sie können eine Befehlsdatei erstellen und die Befehle an der Eingabeaufforderung ausführen, oder Sie können eine Skriptsprache wie VBScript oder Windows PowerShell verwenden, um die Befehle auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-110">You can create a command file and run the commands from the command prompt, or you can use a scripting language such as VBScript or Windows PowerShell to run the commands.</span></span>

<span data-ttu-id="cbbdf-111">**Hinweis**  Für x86-und x64-Versionen des App-V-Clients sind die x86-Versionen der folgenden Software erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-111">**Note** The x86 versions of the following software are required for both x86 and x64 versions of the App-V client.</span></span>

 

**<span data-ttu-id="cbbdf-112">So installieren Sie Microsoft VisualC + + 2005SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="cbbdf-112">To install Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>**

1. <span data-ttu-id="cbbdf-113">Laden Sie das [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)-](https://go.microsoft.com/fwlink/?LinkId=119961) Softwarepaket aus dem Microsoft Download Center ( <https://go.microsoft.com/fwlink/?LinkId=119961> ) herunter.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-113">Download the [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) software package from the Microsoft Download Center (<https://go.microsoft.com/fwlink/?LinkId=119961>).</span></span> <span data-ttu-id="cbbdf-114">\ [Vorlagen Tokenwert \] für Version 4,5 SP2 und höher des App-V-Clients laden Sie vcredist\_x86.exe aus dem [Microsoft Visual C++ 2005 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=169360) verteilbaren Paket ATL-Sicherheits Update herunter ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [Vorlagen Tokenwert \]</span><span class="sxs-lookup"><span data-stu-id="cbbdf-114">\[Template Token Value\] For version 4.5 SP2 and later of the App-V client, download vcredist\_x86.exe from [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360) (https://go.microsoft.com/fwlink/?LinkId=169360).\[Template Token Value\]</span></span>

2. <span data-ttu-id="cbbdf-115">Verwenden Sie zum unbeaufsichtigten installieren die Befehlszeilenoption "/q" mit vcredist\_x86.exe, beispielsweise **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-115">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

3. <span data-ttu-id="cbbdf-116">Wenn Sie die Software mithilfe der vcredist\_x86.msi-Datei installieren möchten, verwenden Sie die Befehlszeilenoption "/c/t: &lt; fullpathtofolder &gt; ", um die Dateien vcredist.msi und vcredis1.cab aus vcredist\_x86.exe in einen temporären Ordner zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-116">To install the software by using the vcredist\_x86.msi file, use the command-line option “/C /T:&lt;fullpathtofolder&gt;” to extract the files vcredist.msi and vcredis1.cab from vcredist\_x86.exe to a temporary folder.</span></span> <span data-ttu-id="cbbdf-117">Verwenden Sie zum unbeaufsichtigten installieren die Befehlszeilenoption/quiet – beispielsweise **msiexec/i vcredist.msi** /quiet.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-117">To install silently, use the command-line option /quiet—for example, **msiexec /i vcredist.msi** /quiet.</span></span>

### <span data-ttu-id="cbbdf-118">So installieren Sie Microsoft VisualC + + 2008SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="cbbdf-118">To install Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

<span data-ttu-id="cbbdf-119">**Wichtig**  Für Version 4.6 und höher des App-V-Clients müssen Sie auch das ATL-Sicherheits Update "Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package" installieren.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-119">**Important** For version4.6 and later of the App-V client, you must also install the Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update.</span></span>

 

****

1.  <span data-ttu-id="cbbdf-120">Laden Sie das [Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=150700) -Softwarepaket aus dem Microsoft Download Center ( https://go.microsoft.com/fwlink/?LinkId=150700) .</span><span class="sxs-lookup"><span data-stu-id="cbbdf-120">Download the [Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=150700) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=150700).</span></span>

2.  <span data-ttu-id="cbbdf-121">Verwenden Sie zum unbeaufsichtigten installieren die Befehlszeilenoption "/q" mit vcredist\_x86.exe, beispielsweise **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-121">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

### <span data-ttu-id="cbbdf-122">So installieren Sie Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="cbbdf-122">To install Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

****

1.  <span data-ttu-id="cbbdf-123">Herunterladen des [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) -Softwarepakets aus dem Microsoft Download Center ( https://go.microsoft.com/fwlink/?LinkId=63266) .</span><span class="sxs-lookup"><span data-stu-id="cbbdf-123">Download the [Microsoft Core XML Services (MSXML)6.0SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=63266).</span></span>

2.  <span data-ttu-id="cbbdf-124">Verwenden Sie zum unbeaufsichtigten installieren die Befehlszeilenoption/quiet, beispielsweise **msiexec/i msxml6\_x86.msi/quiet**.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-124">To install silently, use the command-line option /quiet—for example, **msiexec /i msxml6\_x86.msi /quiet**.</span></span>

### <span data-ttu-id="cbbdf-125">So installieren Sie die Microsoft-Anwendungsfehler Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="cbbdf-125">To install Microsoft Application Error Reporting</span></span>

<span data-ttu-id="cbbdf-126">Wenn Sie die Microsoft-Anwendungsfehler Berichterstattung installieren, müssen Sie den *AppGUID* -Parameter verwenden, um den App-V-Produktcode anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-126">When installing Microsoft Application Error Reporting, you must use the *APPGUID* parameter to specify the App-V product code.</span></span> <span data-ttu-id="cbbdf-127">Der Produktcode ist für jeden App-V-Clienttyp und jede Version eindeutig.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-127">The product code is unique for each App-V client type and version.</span></span> <span data-ttu-id="cbbdf-128">Wählen Sie den richtigen Produktcode aus der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-128">Select the correct product code from the following table.</span></span>

<span data-ttu-id="cbbdf-129">**Wichtig**  Für App-v 4.6 SP2 und höher müssen Sie die Microsoft-Anwendungsfehler Berichterstattung (dw20shared.msi) nicht mehr installieren.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-129">**Important** For App-V4.6SP2 and later, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="cbbdf-130">App-V verwendet jetzt die Microsoft-Fehlerberichterstattung.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-130">App-V now uses Microsoft Error Reporting.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cbbdf-131">Version</span><span class="sxs-lookup"><span data-stu-id="cbbdf-131">Version</span></span></th>
<th align="left"><span data-ttu-id="cbbdf-132">Produkt Code für den Desktop Client</span><span class="sxs-lookup"><span data-stu-id="cbbdf-132">Product Code for Desktop Client</span></span></th>
<th align="left"><span data-ttu-id="cbbdf-133">Produkt Code für Client für Remote Desktop Dienste</span><span class="sxs-lookup"><span data-stu-id="cbbdf-133">Product Code for Client for Remote Desktop Services</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbdf-134">App-V 4,5 CU1</span><span class="sxs-lookup"><span data-stu-id="cbbdf-134">App-V 4.5 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span><span class="sxs-lookup"><span data-stu-id="cbbdf-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span><span class="sxs-lookup"><span data-stu-id="cbbdf-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbdf-137">App-V 4,5 SP1</span><span class="sxs-lookup"><span data-stu-id="cbbdf-137">App-V 4.5 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-138">93468B43-C19D-44F9-8BCC-114076DB0443</span><span class="sxs-lookup"><span data-stu-id="cbbdf-138">93468B43-C19D-44F9-8BCC-114076DB0443</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span><span class="sxs-lookup"><span data-stu-id="cbbdf-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbdf-140">App-V 4,5 SP2</span><span class="sxs-lookup"><span data-stu-id="cbbdf-140">App-V 4.5 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span><span class="sxs-lookup"><span data-stu-id="cbbdf-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span><span class="sxs-lookup"><span data-stu-id="cbbdf-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbdf-143">App-V 4,6 x86</span><span class="sxs-lookup"><span data-stu-id="cbbdf-143">App-V 4.6 x86</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span><span class="sxs-lookup"><span data-stu-id="cbbdf-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-145">439FAC21-B423-41D4-8126-54F9FCB70039</span><span class="sxs-lookup"><span data-stu-id="cbbdf-145">439FAC21-B423-41D4-8126-54F9FCB70039</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbdf-146">App-V 4,6 x64</span><span class="sxs-lookup"><span data-stu-id="cbbdf-146">App-V 4.6 x64</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span><span class="sxs-lookup"><span data-stu-id="cbbdf-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span><span class="sxs-lookup"><span data-stu-id="cbbdf-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbdf-149">App-V 4,6 x86 ¹</span><span class="sxs-lookup"><span data-stu-id="cbbdf-149">App-V 4.6 x86 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span><span class="sxs-lookup"><span data-stu-id="cbbdf-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-151">9915D911-CC73-4122-AF4F-564F89454655</span><span class="sxs-lookup"><span data-stu-id="cbbdf-151">9915D911-CC73-4122-AF4F-564F89454655</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbdf-152">App-V 4,6 x64 ¹</span><span class="sxs-lookup"><span data-stu-id="cbbdf-152">App-V 4.6 x64 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span><span class="sxs-lookup"><span data-stu-id="cbbdf-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span><span class="sxs-lookup"><span data-stu-id="cbbdf-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbdf-155">App-V 4,6 x86 SP1</span><span class="sxs-lookup"><span data-stu-id="cbbdf-155">App-V 4.6 x86 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span><span class="sxs-lookup"><span data-stu-id="cbbdf-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-157">1354855A-2298-4C73-9022-EF0686C65991</span><span class="sxs-lookup"><span data-stu-id="cbbdf-157">1354855A-2298-4C73-9022-EF0686C65991</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbdf-158">App-V 4,6 x64 SP1</span><span class="sxs-lookup"><span data-stu-id="cbbdf-158">App-V 4.6 x64 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span><span class="sxs-lookup"><span data-stu-id="cbbdf-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbdf-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span><span class="sxs-lookup"><span data-stu-id="cbbdf-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="cbbdf-161">¹ App-V "Sprachen"-Version.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-161">¹App-V “Languages” release.</span></span>

<span data-ttu-id="cbbdf-162">**Hinweis**  Wenn Sie den Produktcode finden müssen, können Sie den Orca.exe-Datenbankeditor oder ein ähnliches Tool verwenden, um Windows Installer-Dateien zu untersuchen, um den Wert der *ProductCode* -Eigenschaft zu finden.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-162">**Note** If you need to find the product code, you can use the Orca.exe database editor or a similar tool to examine Windows Installer files to find the value of the *ProductCode* property.</span></span> <span data-ttu-id="cbbdf-163">Weitere Informationen zum Verwenden von Orca.exe finden Sie unter [Windows Installer-Entwicklungs Tools](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .</span><span class="sxs-lookup"><span data-stu-id="cbbdf-163">For more information about using Orca.exe, see [Windows Installer Development Tools](https://go.microsoft.com/fwlink/?LinkId=150008) (https://go.microsoft.com/fwlink/?LinkId=150008).</span></span>

 

****

1.  <span data-ttu-id="cbbdf-164">Suchen Sie das Installationsprogramm für die Microsoft-Anwendungsfehler Berichterstattung dw20shared.msi, das im Ordner **Support\\Watson** auf dem Veröffentlichungsmedium zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-164">Locate the Microsoft Application Error Reporting install program, dw20shared.msi, which can be found in the **Support\\Watson** folder on the release media.</span></span>

2.  <span data-ttu-id="cbbdf-165">Führen Sie den folgenden Befehl aus, um die Software zu installieren:</span><span class="sxs-lookup"><span data-stu-id="cbbdf-165">To install the software, run the following command:</span></span>

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a><span data-ttu-id="cbbdf-166">Installieren des App-V-Clients mithilfe des Setup.msi-Programms</span><span class="sxs-lookup"><span data-stu-id="cbbdf-166">Installing the App-V Client by Using the Setup.msi Program</span></span>


<span data-ttu-id="cbbdf-167">Gehen Sie wie folgt vor, um den App-V-Client zu installieren.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-167">Use the following procedure to install the App-V client.</span></span> <span data-ttu-id="cbbdf-168">Stellen Sie sicher, dass alle erforderlichen Softwarekomponenten installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-168">Ensure that any necessary prerequisite software has been installed.</span></span> <span data-ttu-id="cbbdf-169">\ [Vorlagen Tokenwert \] für Version 4.6 und höher des App-V-Clients überprüft das setup.msi-Programm das System, und wenn die erforderliche Software nicht installiert ist, wird eine Fehlermeldung mit dem Hinweis angezeigt, dass die Installation nicht fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-169">\[Template Token Value\] For version4.6 and later of the App-V client, the setup.msi program checks the system and if prerequisite software is not installed, it generates an error message indicating that installation cannot continue.</span></span> <span data-ttu-id="cbbdf-170">\ [Vorlage-Tokenwert \]</span><span class="sxs-lookup"><span data-stu-id="cbbdf-170">\[Template Token Value\]</span></span>

**<span data-ttu-id="cbbdf-171">So installieren Sie den Application Virtualization-Client mithilfe von Setup.msi</span><span class="sxs-lookup"><span data-stu-id="cbbdf-171">To install the Application Virtualization Client by Using Setup.msi</span></span>**

1.  <span data-ttu-id="cbbdf-172">Stellen Sie sicher, dass Sie mit einem Konto angemeldet sind, das über Administratorrechte auf dem Computer verfügt.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-172">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="cbbdf-173">Öffnen Sie ein Eingabeaufforderungsfenster, indem Sie erhöhte Rechte verwenden, und ändern Sie dann das Verzeichnis in den Ordner, in dem die Setupdateien enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-173">Open a Command Prompt window by using elevated rights, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="cbbdf-174">Wenn Sie Version 4.6 oder eine neuere Version des App-V-Clients installieren, müssen Sie das richtige Installationsprogramm für das Betriebssystem des Computers, 32-Bit oder 64-Bit verwenden.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-174">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="cbbdf-175">Bei der Installation tritt ein Fehler auf, und es wird eine Fehlermeldung angezeigt, wenn Sie das falsche Installationsprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-175">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="cbbdf-176">Geben Sie die Befehlszeichenfolge für den Installationsbefehl an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-176">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="cbbdf-177">Alternativ können Sie eine Befehlsdatei erstellen und diese über die Eingabeaufforderung ausführen.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-177">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="cbbdf-178">Sie können auch eine Skriptsprache wie VBScript oder Windows PowerShell verwenden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-178">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="cbbdf-179">Das folgende Befehlszeilenbeispiel zeigt, wie setup.msi mit einer Reihe optionaler Parameter verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-179">The following command-line example shows how setup.msi can be used with a number of optional parameters.</span></span> <span data-ttu-id="cbbdf-180">Weitere Informationen zu diesen Parametern finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cbbdf-180">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="cbbdf-181">msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "Production System" SWIPUBSVRTYPE = "http/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "SWIGLOBALDATA =" D:\\AppVirt\\Global "SWIUSERDATA =" ^% LocalAppData ^%\\Windows\\Application Virtualization Client "SWIFSDRIVE =" S "/q</span><span class="sxs-lookup"><span data-stu-id="cbbdf-181">msiexec.exe /i "setup.msi" SWICACHESIZE="10240" SWIPUBSVRDISPLAY="Production System" SWIPUBSVRTYPE="HTTP /secure" SWIPUBSVRHOST="PRODSYS" SWIPUBSVRPORT="443" SWIPUBSVRPATH="/AppVirt/appsntype.xml" SWIPUBSVRREFRESH="on" SWIGLOBALDATA="D:\\AppVirt\\Global" SWIUSERDATA="^% LOCALAPPDATA^%\\Windows\\Application Virtualization Client" SWIFSDRIVE="S" /q</span></span>**

    **<span data-ttu-id="cbbdf-182">Wichtig</span><span class="sxs-lookup"><span data-stu-id="cbbdf-182">Important</span></span>**  
    -   <span data-ttu-id="cbbdf-183">Der Windows Installer-Schalter "**/q**" wird verwendet, um dies zu einer unbeaufsichtigten Installation zu machen.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-183">The Windows Installer switch "**/q**" is used to make this a silent installation.</span></span>

    -   <span data-ttu-id="cbbdf-184">Dem "" " **%** -Zeichen in"**% HOMEDRIVE%**"muss das Escapezeichen" "vorangestellt werden **^** .</span><span class="sxs-lookup"><span data-stu-id="cbbdf-184">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="cbbdf-185">Andernfalls legt die Windows-Befehlsshell den Wert auf den Wert des Benutzers fest, der die Installation ausführt.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-185">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="cbbdf-186">Um die Installationsprotokollierung zu aktivieren, verwenden Sie den msiexec-Schalter **/l\ \* v filename. log**.</span><span class="sxs-lookup"><span data-stu-id="cbbdf-186">To turn on installation logging, use the msiexec switch **/l\*v filename.log**.</span></span>

     

## <span data-ttu-id="cbbdf-187">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="cbbdf-187">Related topics</span></span>


[<span data-ttu-id="cbbdf-188">So installieren Sie den Client über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="cbbdf-188">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





