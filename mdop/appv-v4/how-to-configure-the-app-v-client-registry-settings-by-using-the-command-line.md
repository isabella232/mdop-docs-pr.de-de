---
title: So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile
description: So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807291"
---
# <span data-ttu-id="760d4-103">So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="760d4-103">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>


<span data-ttu-id="760d4-104">Nachdem der Application Virtualization (App-V)-Client während der Installation über die Befehlszeile bereitgestellt und konfiguriert wurde, ist es möglicherweise erforderlich, eine oder mehrere Clientkonfigurationseinstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="760d4-104">After the Application Virtualization (App-V) Client has been deployed and configured during the installation by using the command line, it might be necessary to change one or more client configuration settings.</span></span> <span data-ttu-id="760d4-105">Dies erfolgt durch Bearbeiten der entsprechenden Registrierungsschlüssel mithilfe einer der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="760d4-105">This is accomplished by editing the appropriate registry keys, using one of the following methods:</span></span>

-   <span data-ttu-id="760d4-106">Direktes Verwenden des Registrierungs-Editors</span><span class="sxs-lookup"><span data-stu-id="760d4-106">Using the Registry Editor directly</span></span>

-   <span data-ttu-id="760d4-107">Verwenden einer REG-Datei</span><span class="sxs-lookup"><span data-stu-id="760d4-107">Using a .reg file</span></span>

-   <span data-ttu-id="760d4-108">Verwenden einer Skriptsprache wie VBScript oder Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="760d4-108">Using a scripting language such as VBScript or Windows PowerShell</span></span>

<span data-ttu-id="760d4-109">Es gibt auch eine ADM-Vorlage, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="760d4-109">There is also an ADM template that you can use.</span></span> <span data-ttu-id="760d4-110">Weitere Informationen zur ADM-Vorlage finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=121835> .</span><span class="sxs-lookup"><span data-stu-id="760d4-110">For more information about the ADM template, see <https://go.microsoft.com/fwlink/?LinkId=121835>.</span></span>

<span data-ttu-id="760d4-111">**Vorsicht**  Verwenden Sie beim Bearbeiten der Registrierung Vorsicht, da Fehler den Computer in einem unbrauchbaren Zustand belassen können.</span><span class="sxs-lookup"><span data-stu-id="760d4-111">**Caution** Use care when you edit the registry because errors can leave the computer in an unusable state.</span></span> <span data-ttu-id="760d4-112">Befolgen Sie unbedingt Ihre Standard Geschäftsmethoden, die sich auf Registrierungsänderungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="760d4-112">Be sure to follow your standard business practices that relate to registry edits.</span></span> <span data-ttu-id="760d4-113">Testen Sie alle vorgeschlagenen Änderungen in einer Testumgebung gründlich, bevor Sie Sie auf Produktionscomputern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="760d4-113">Thoroughly test all proposed changes in a test environment before you deploy them to production computers.</span></span>

 

## <span data-ttu-id="760d4-114">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="760d4-114">In This Section</span></span>


<span data-ttu-id="760d4-115">**Wichtig**  Auf einem 64-Bit-Computer finden Sie die in den folgenden Abschnitten beschriebenen Schlüssel und Werte unter HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\client.</span><span class="sxs-lookup"><span data-stu-id="760d4-115">**Important** On a 64-bit computer, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[<span data-ttu-id="760d4-116">So setzen Sie den Dateisystemcache zurück</span><span class="sxs-lookup"><span data-stu-id="760d4-116">How to Reset the FileSystem Cache</span></span>](how-to-reset-the-filesystem-cache.md)  
<span data-ttu-id="760d4-117">Enthält die Informationen, die erforderlich sind, um den Dateisystemcache zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="760d4-117">Provides the information that is required to reset the FileSystem cache.</span></span>

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[<span data-ttu-id="760d4-118">So ändern Sie die Größe des Dateisystemcaches</span><span class="sxs-lookup"><span data-stu-id="760d4-118">How to Change the Size of the FileSystem Cache</span></span>](how-to-change-the-size-of-the-filesystem-cache.md)  
<span data-ttu-id="760d4-119">Erläutert, wie Sie die Größe des Caches ändern können.</span><span class="sxs-lookup"><span data-stu-id="760d4-119">Explains how you can change the size of the cache.</span></span>

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[<span data-ttu-id="760d4-120">So verwenden Sie das Verwaltungsfeature für den Cachespeicher</span><span class="sxs-lookup"><span data-stu-id="760d4-120">How to Use the Cache Space Management Feature</span></span>](how-to-use-the-cache-space-management-feature.md)  
<span data-ttu-id="760d4-121">Beschreibt, wie Sie das Feature für die Cachespeicherverwaltung konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="760d4-121">Describes how you can configure the cache space management feature.</span></span>

<a href="" id="how-to-configure-the-client-log-file"></a>[<span data-ttu-id="760d4-122">So konfigurieren Sie die Clientprotokolldatei</span><span class="sxs-lookup"><span data-stu-id="760d4-122">How to Configure the Client Log File</span></span>](how-to-configure-the-client-log-file.md)  
<span data-ttu-id="760d4-123">Beschreibt die verschiedenen Registrierungsschlüsselwerte, die die Clientprotokolldatei steuern, und wie Sie Sie ändern können.</span><span class="sxs-lookup"><span data-stu-id="760d4-123">Describes the various registry key values that control the client log file and how you can change them.</span></span>

<a href="" id="how-to-configure-user-permissions"></a>[<span data-ttu-id="760d4-124">So konfigurieren Sie Benutzerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="760d4-124">How to Configure User Permissions</span></span>](how-to-configure-user-permissions.md)  
<span data-ttu-id="760d4-125">Identifiziert den Registrierungsschlüssel, der die Benutzerberechtigungen steuert, und gibt Beispiele dafür, wie Sie einige Berechtigungen ändern können.</span><span class="sxs-lookup"><span data-stu-id="760d4-125">Identifies the registry key that controls the user permissions and gives examples of how you can change some permissions.</span></span>

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[<span data-ttu-id="760d4-126">So konfigurieren Sie den Client für den Abruf von Anwendungspaketen</span><span class="sxs-lookup"><span data-stu-id="760d4-126">How to Configure the Client for Application Package Retrieval</span></span>](how-to-configure-the-client-for-application-package-retrieval.md)  
<span data-ttu-id="760d4-127">Es wird erläutert, wie Sie den Client so konfigurieren, dass Paketinhalte, Symbole und Dateitypzuordnungen aus unterschiedlichen Quellen abgerufen werden, und es werden mehrere Beispiele für das richtige Pfadformat bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="760d4-127">Explains how to configure the client to retrieve package content, icons, and file type associations from different sources, and provides several examples of the correct path format.</span></span>

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[<span data-ttu-id="760d4-128">So konfigurieren Sie den Client für den unterbrochenen Betriebsmodus</span><span class="sxs-lookup"><span data-stu-id="760d4-128">How to Configure the Client for Disconnected Operation Mode</span></span>](how-to-configure-the-client-for-disconnected-operation-mode.md)  
<span data-ttu-id="760d4-129">Enthält Informationen zum Konfigurieren der verschiedenen Einstellungen, die mit dem Modus für getrennte Vorgänge verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="760d4-129">Provides information about how to configure the various settings associated with disconnected operations mode.</span></span>

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[<span data-ttu-id="760d4-130">So konfigurieren Sie das Verhalten von Verknüpfungen und Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="760d4-130">How to Configure Shortcut and File Type Association Behavior</span></span>](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
<span data-ttu-id="760d4-131">Beschreibt die Registrierungsschlüsselwerte, die Tastenkombinationen und Dateitypzuordnungen im App-V-Client steuern, und enthält Details zur Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="760d4-131">Describes the registry key values that control shortcuts and file type associations in the App-V client, and provides details on how to configure them.</span></span>

## <span data-ttu-id="760d4-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="760d4-132">Related topics</span></span>


[<span data-ttu-id="760d4-133">Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="760d4-133">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





