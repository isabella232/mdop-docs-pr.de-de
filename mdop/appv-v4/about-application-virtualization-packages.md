---
title: Informationen zu Application Virtualization-Paketen
description: Informationen zu Application Virtualization-Paketen
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808164"
---
# <span data-ttu-id="6985d-103">Informationen zu Application Virtualization-Paketen</span><span class="sxs-lookup"><span data-stu-id="6985d-103">About Application Virtualization Packages</span></span>


<span data-ttu-id="6985d-104">In Application Virtualization ist ein *Paket* die Ausgabe des Sequenz Prozesses.</span><span class="sxs-lookup"><span data-stu-id="6985d-104">In Application Virtualization, a *package* is the output of the sequencing process.</span></span> <span data-ttu-id="6985d-105">Sie verwenden Pakete, wenn Sie zuerst Anwendungen auf Ihren Servern bereitstellen und Anwendungen mit einer neuen Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6985d-105">You use packages when you first deploy applications on your servers and when you upgrade applications with a new version.</span></span> <span data-ttu-id="6985d-106">Mit Paketen können Sie virtuelle Anwendungsversionen auf Ihren Application Virtualization Management-Servern steuern.</span><span class="sxs-lookup"><span data-stu-id="6985d-106">Packages enable you to control virtual application versions on your Application Virtualization Management Servers.</span></span> <span data-ttu-id="6985d-107">Ein einzelnes Paket kann mindestens eine Anwendung enthalten.</span><span class="sxs-lookup"><span data-stu-id="6985d-107">A single package can contain one or more applications.</span></span> <span data-ttu-id="6985d-108">Jedes Anwendungspaket enthält eine Reihe von Dateien als eigenständige Einheit.</span><span class="sxs-lookup"><span data-stu-id="6985d-108">Each application package contains a set of files as a self-contained unit.</span></span>

## <span data-ttu-id="6985d-109">Verwalten von Paketen</span><span class="sxs-lookup"><span data-stu-id="6985d-109">Managing Packages</span></span>


<span data-ttu-id="6985d-110">Nachdem der Sequencer ein Paket aus einer oder mehreren Anwendungen als Teil des Prozesses erstellt hat, können Sie die vom Sequencer generierten Dateien auf einen Application Virtualization Management-Server kopieren und für das Streaming verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="6985d-110">After the Sequencer creates a package of one or more applications as part of its process, you can copy the Sequencer-generated files to a Application Virtualization Management Server and make them available for streaming.</span></span>

<span data-ttu-id="6985d-111">Verfügbare Pakete werden unter dem Container **Pakete** im linken Bereich der Application Virtualization-Verwaltungskonsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6985d-111">Available packages appear under the **Packages** container in the left pane of the Application Virtualization Management Console.</span></span> <span data-ttu-id="6985d-112">Wenn Sie eine Anwendung mit einer Sequencer Project-Datei (SPRJ) oder einer Open Software Descriptor-Datei (OSD) importieren, wird im Container **Pakete** ein verwandter Eintrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6985d-112">When you import an application with a Sequencer Project (SPRJ) file or an Open Software Descriptor (OSD) file, a related entry appears in the **Packages** container.</span></span> <span data-ttu-id="6985d-113">In der Application Virtualization Server-Verwaltungskonsole können Sie Pakete und Versionen davon bereitstellen, aktualisieren oder löschen.</span><span class="sxs-lookup"><span data-stu-id="6985d-113">From the Application Virtualization Server Management Console, you can then deploy, upgrade, or delete packages and versions of them.</span></span>

<span data-ttu-id="6985d-114">Jede virtuelle Anwendung verfügt über ein zugeordnetes Paket.</span><span class="sxs-lookup"><span data-stu-id="6985d-114">Each virtual application has an associated package.</span></span> <span data-ttu-id="6985d-115">Dieses Paket enthält die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="6985d-115">This package includes the following files:</span></span>

-   <span data-ttu-id="6985d-116">SFT – die Datei, die die Anwendung an Clients streamt.</span><span class="sxs-lookup"><span data-stu-id="6985d-116">SFT—The file that streams the application to clients.</span></span>

-   <span data-ttu-id="6985d-117">OSD – die Open Software Descriptor-Datei enthält die Informationen, die zum Suchen und Starten der Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6985d-117">OSD—The Open Software Descriptor file contains the information needed to find and launch the application.</span></span>

-   <span data-ttu-id="6985d-118">ICO – die Symboldatei, die die Anwendung visuell in Benutzeroberflächen und Tastenkombinationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="6985d-118">ICO—The icon file that visually represents the application in user interfaces and shortcuts.</span></span>

-   <span data-ttu-id="6985d-119">SPRJ – die Projektdatei des Sequencers.</span><span class="sxs-lookup"><span data-stu-id="6985d-119">SPRJ—The Sequencer Project file.</span></span>

<span data-ttu-id="6985d-120">Wenn Sie die SPRJ-Datei importieren, stehen standardmäßig alle sequenzierten Anwendungen für die Bereitstellung zur Verfügung, die Anwendungen sind jedoch nicht für Streaming aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6985d-120">When you import the SPRJ file, all sequenced applications are available for deployment, by default, but the applications are not enabled for streaming.</span></span> <span data-ttu-id="6985d-121">Sie können auswählen, ob alle oder einige der Anwendungen im Paket gestreamt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6985d-121">You can choose to stream all or some of the applications in the package.</span></span> <span data-ttu-id="6985d-122">Wenn Sie beispielsweise Microsoft Office sequenziert und importiert haben, können Sie auswählen, dass einige Anwendungen nicht bereitgestellt werden sollen, beispielsweise den Assistenten zum Speichern meiner Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="6985d-122">For example, if you sequenced and imported Microsoft Office, you can choose not to deploy some applications, such as the Save My Settings Wizard.</span></span> <span data-ttu-id="6985d-123">Klicken Sie in diesem Fall mit der rechten Maustaste auf jede Anwendung, die Sie bereitstellen möchten, wählen Sie **Eigenschaften**aus, und stellen Sie sicher, dass das Feld **aktiviert** (leer) deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6985d-123">In this case, right-click each application you want to deploy, choose **Properties**, and make sure that the **Enabled** box is cleared (blank).</span></span> <span data-ttu-id="6985d-124">Nur die Anwendungen mit **aktiviertem aktivierten** Feld werden auf Clientcomputer gestreamt.</span><span class="sxs-lookup"><span data-stu-id="6985d-124">Only the applications with the **Enabled** box selected will stream to client computers.</span></span>

<span data-ttu-id="6985d-125">Nachdem Sie ein Paket neu sequenziert und eine neue SFT-Datei für das Streaming erstellt haben, können Sie das alte Paket schnell und einfach über die Application Virtualization Server-Verwaltungskonsole aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6985d-125">After you resequence a package and produce a new SFT file for streaming, you can upgrade the old package quickly and easily through the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="6985d-126">Das einzige operationelle Szenario, in dem Sie den Knoten **Pakete** verwenden müssen, ist, wenn Sie eine neue Version (SFT-Datei) für das Paket einführen.</span><span class="sxs-lookup"><span data-stu-id="6985d-126">The only operational scenario that requires you to use the **Packages** node is when you introduce a new version (SFT file) for the package.</span></span> <span data-ttu-id="6985d-127">Wenn Sie Anwendungen importieren, Anwendungen Zugriff und Lizenzen zuweisen usw., verfolgt das Application Virtualization System diese Informationen auf Paketebene.</span><span class="sxs-lookup"><span data-stu-id="6985d-127">Whenever you import applications, assign access and licenses to applications, and so on, the Application Virtualization System tracks this information at the package level.</span></span> <span data-ttu-id="6985d-128">Das bedeutet, dass Sie dem Benutzer die Berechtigung erteilen, eine Anwendung im gleichen Paket auszuführen, wenn Sie einen Benutzer zur Verwendung einer Anwendung autorisieren.</span><span class="sxs-lookup"><span data-stu-id="6985d-128">This means that when you authorize a user to use an application, you are giving the user permission to run any application in the same package.</span></span>

### <span data-ttu-id="6985d-129">Paket Version</span><span class="sxs-lookup"><span data-stu-id="6985d-129">Package Version</span></span>

<span data-ttu-id="6985d-130">Eine Paketversion wird durch eine bestimmte SFT-Datei dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6985d-130">A package version is represented by a specific SFT file.</span></span> <span data-ttu-id="6985d-131">Wenn Sie ein Paket aktualisieren (ein Update auf eine Anwendung anwenden oder einem Paket eine Anwendung hinzufügen), erstellen Sie eine neue SFT-Datei.</span><span class="sxs-lookup"><span data-stu-id="6985d-131">When you upgrade a package (apply an update to an application or add an application to a package), you generate a new SFT file.</span></span> <span data-ttu-id="6985d-132">Jedes Mal, wenn Sie eine neue SFT-Datei erstellen, erstellen Sie eine neue Paketversion.</span><span class="sxs-lookup"><span data-stu-id="6985d-132">Each time you create a new SFT file, you are creating a new package version.</span></span>

<span data-ttu-id="6985d-133">Wenn Sie Anwendungen über die Application Virtualization Server-Verwaltungskonsole importieren, erstellt die Software automatisch ein Paket und eine Paketversion, wenn Sie noch nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6985d-133">When you import applications through the Application Virtualization Server Management Console, the software automatically creates a package and a package version if they do not already exist.</span></span>

## <span data-ttu-id="6985d-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6985d-134">Related topics</span></span>


[<span data-ttu-id="6985d-135">Informationen zu Application Virtualization-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6985d-135">About Application Virtualization Applications</span></span>](about-application-virtualization-applications.md)

[<span data-ttu-id="6985d-136">Informationen zur Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="6985d-136">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="6985d-137">So verwalten Sie die Pakete in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="6985d-137">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





