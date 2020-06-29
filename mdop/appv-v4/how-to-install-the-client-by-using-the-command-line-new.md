---
title: So installieren Sie den Client über die Befehlszeile
description: So installieren Sie den Client über die Befehlszeile
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807060"
---
# <span data-ttu-id="c74ce-103">So installieren Sie den Client über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="c74ce-103">How to Install the Client by Using the Command Line</span></span>


<span data-ttu-id="c74ce-104">Die Themen in diesem Abschnitt enthalten Verfahren zum Installieren des Application Virtualization (app-v)-Desktop Clients oder des App-v-Clients für Remote Desktop Dienste (ehemals Terminal Dienste) mithilfe von setup.exe oder setup.msi.</span><span class="sxs-lookup"><span data-stu-id="c74ce-104">The topics in this section include procedures to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span> <span data-ttu-id="c74ce-105">Zum Ausführen eines der Setupprogramme sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c74ce-105">Administrative rights are required to run either setup program.</span></span>

<span data-ttu-id="c74ce-106">Sie können optionale Befehlszeilenparameter verwenden, um während der Installation bestimmte Konfigurationseinstellungen auf den App-V-Client anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="c74ce-106">You can use optional command-line parameters to apply specific configuration settings to the App-V client during the installation.</span></span> <span data-ttu-id="c74ce-107">Weitere Informationen zum Verwenden von Parametern finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c74ce-107">For more information about using parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span> <span data-ttu-id="c74ce-108">Wenn Sie die Registrierungseinstellungen auf einen Computer angewendet haben, bevor Sie einen Client bereitstellen, beispielsweise mithilfe von Gruppenrichtlinien, werden diese Einstellungen beibehalten, und es werden alle zusätzlichen Befehlszeilenparameter angewendet.</span><span class="sxs-lookup"><span data-stu-id="c74ce-108">If you have applied registry settings to a computer before deploying a client—for example, by using Group Policy—these settings are retained and any additional command line parameters are applied.</span></span> <span data-ttu-id="c74ce-109">Mit Befehlszeilenparametern werden alle vorhandenen Werte für die gleiche Einstellung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c74ce-109">Command line parameter values will replace any existing value for the same setting.</span></span>

<span data-ttu-id="c74ce-110">**Hinweis**  Wenn Sie den App-V-Client zur Verwendung mit einem schreibgeschützten Cache installieren, beispielsweise bei einer VDI-Server Implementierung, müssen Sie den *AUTOLOADTARGET* -Parameter auf None setzen, um zu verhindern, dass der Client versucht, Anwendungen zu aktualisieren, wenn der Cache schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="c74ce-110">**Note** When you install the App-V client to use with a read-only cache, for example with a VDI server implementation, you must set the *AUTOLOADTARGET* parameter to NONE to prevent the client from trying to update applications when the cache is read-only.</span></span>

 

<span data-ttu-id="c74ce-111">Weitere Informationen zum Festlegen dieser Parameterwerte nach der Installation finden Sie unter [Konfigurieren der Einstellungen der App-V-Client Registrierung über die Befehlszeile](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) im Operations Handbuch für Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="c74ce-111">For more information about setting these parameter values after installation, see [How to Configure the App-V Client Registry Settings by Using the Command Line](https://go.microsoft.com/fwlink/?LinkId=169355) (https://go.microsoft.com/fwlink/?LinkId=169355) in the Application Virtualization (App-V) Operations Guide.</span></span>

<span data-ttu-id="c74ce-112">**Hinweis**  Wenn eine Konfigurationseinstellung auf dem Computer des Benutzers vom Client Installationspfad abhängt, beachten Sie, dass der Application Virtualization (App-V) 4.5-Client seine Installationsdateien in einen anderen Ordner als in früheren Versionen kopiert.</span><span class="sxs-lookup"><span data-stu-id="c74ce-112">**Note** If a configuration setting on the user’s computer depends on the client installation path, note that the Application Virtualization (App-V)4.5 client copies its installation files to a different folder than previous versions did.</span></span> <span data-ttu-id="c74ce-113">Standardmäßig werden durch eine neue Installation des App-v 4.5-Clients die Installationsdateien in den \\Program c:\\Programme\\Microsoft Application Virtualization Client-Ordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="c74ce-113">By default, a new installation of the App-V4.5 client will copy its installation files to the \\Program Files\\Microsoft Application Virtualization Client folder.</span></span> <span data-ttu-id="c74ce-114">Wenn eine frühere Version des Clients bereits installiert ist, führt das Ausführen des App-V 4,5-Clientinstallationsprogramms zu einem Upgrade des vorhandenen Clients mithilfe des vorhandenen Installationsordners.</span><span class="sxs-lookup"><span data-stu-id="c74ce-114">If an earlier version of the client is already installed, running the App-V 4.5 client installer will perform an upgrade of the existing client using the existing installation folder.</span></span>

 

<span data-ttu-id="c74ce-115">\ [Vorlage-Tokenwert \]</span><span class="sxs-lookup"><span data-stu-id="c74ce-115">\[Template Token Value\]</span></span>

<span data-ttu-id="c74ce-116">**Hinweis**  Bei App-v, Version 4.6 und höher, wenn der APP-v-Client installiert ist, wird SFTLDR.DLL in das Windows\\system32-Verzeichnis kopiert.</span><span class="sxs-lookup"><span data-stu-id="c74ce-116">**Note** For App-V version4.6 and later, when the App-V client is installed, SFTLDR.DLL is copied to the Windows\\system32 directory.</span></span> <span data-ttu-id="c74ce-117">Wenn der App-V-Client auf einem 64-Bit-System installiert ist, wird SFTLDR\_WOW64.DLL in das Windows\\SysWOW64-Verzeichnis kopiert.</span><span class="sxs-lookup"><span data-stu-id="c74ce-117">If the App-V client is installed on a 64-bit system, SFTLDR\_WOW64.DLL is copied to the Windows\\SysWOW64 directory.</span></span>

 

<span data-ttu-id="c74ce-118">\ [Vorlage-Tokenwert \]</span><span class="sxs-lookup"><span data-stu-id="c74ce-118">\[Template Token Value\]</span></span>

## <span data-ttu-id="c74ce-119">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="c74ce-119">In This Section</span></span>


<span data-ttu-id="c74ce-120">In den folgenden Themen wird beschrieben, wie Sie entweder den Application Virtualization (app-v)-Desktop Client oder den App-v-Client für Remote Desktop Dienste (ehemals Terminal Dienste) mithilfe von setup.exe oder setup.msi installieren.</span><span class="sxs-lookup"><span data-stu-id="c74ce-120">The following topics describe how to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[<span data-ttu-id="c74ce-121">So installieren Sie den App-V-Client mithilfe von Setup.exe</span><span class="sxs-lookup"><span data-stu-id="c74ce-121">How to Install the App-V Client by Using Setup.exe</span></span>](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
<span data-ttu-id="c74ce-122">Bietet eine schrittweise Anleitung zum Installieren des App-V-Clients mithilfe des setup.exe-Programms.</span><span class="sxs-lookup"><span data-stu-id="c74ce-122">Provides a step-by-step procedure for installing the App-V client by using the setup.exe program.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[<span data-ttu-id="c74ce-123">So installieren Sie App-V-Client mit Setup.msi</span><span class="sxs-lookup"><span data-stu-id="c74ce-123">How to Install the App-V Client by Using Setup.msi</span></span>](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
<span data-ttu-id="c74ce-124">Bietet Schritt-für-Schritt-Verfahren zum Installieren aller erforderlichen Software und auch des App-V-Clients mithilfe des setup.msi-Programms.</span><span class="sxs-lookup"><span data-stu-id="c74ce-124">Provides step-by-step procedures for installing any prerequisite software and also the App-V client by using the setup.msi program.</span></span>

## <span data-ttu-id="c74ce-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c74ce-125">Related topics</span></span>


[<span data-ttu-id="c74ce-126">Befehlszeilenparameter von Application Virtualization Client Installer</span><span class="sxs-lookup"><span data-stu-id="c74ce-126">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="c74ce-127">So installieren Sie Application Virtualization Client manuell</span><span class="sxs-lookup"><span data-stu-id="c74ce-127">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="c74ce-128">So veröffentlichen Sie eine virtuelle Anwendung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="c74ce-128">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="c74ce-129">So deinstallieren Sie App-V Client</span><span class="sxs-lookup"><span data-stu-id="c74ce-129">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





