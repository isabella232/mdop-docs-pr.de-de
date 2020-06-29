---
title: Planen der Betriebssystemkompatibilität der Anwendung
description: Planen der Betriebssystemkompatibilität der Anwendung
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811173"
---
# <span data-ttu-id="0ef61-103">Planen der Betriebssystemkompatibilität der Anwendung</span><span class="sxs-lookup"><span data-stu-id="0ef61-103">Planning for Application Operating System Compatibility</span></span>


<span data-ttu-id="0ef61-104">In diesem Thema wird erläutert, wie Kompatibilitätsprobleme mit Anwendungs Betriebssystemen behoben werden können, und es wird erläutert, wie Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 als Lösung für Ihre Organisation funktioniert.</span><span class="sxs-lookup"><span data-stu-id="0ef61-104">This topic helps determine how to resolve application operating system compatibility issues, and discusses how Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 works as a solution for your organization.</span></span>

<span data-ttu-id="0ef61-105">In diesem Thema werden die geschäftlichen Anforderungen für med-v erläutert und der Vergleich zwischen Med-v und Windows XP-Modus und Microsoft Application Virtualization (app-v) beschrieben:</span><span class="sxs-lookup"><span data-stu-id="0ef61-105">This topic discusses the business requirements for MED-V and compares MED-V to Windows XP Mode and Microsoft Application Virtualization (App-V):</span></span>

-   [<span data-ttu-id="0ef61-106">Geschäftsanforderungen für MED-V</span><span class="sxs-lookup"><span data-stu-id="0ef61-106">Business Requirements for MED-V</span></span>](#bkmk-whenmedv)

-   [<span data-ttu-id="0ef61-107">Vorteile von MED-V versus Windows XP-Modus</span><span class="sxs-lookup"><span data-stu-id="0ef61-107">Benefits of MED-V versus Windows XP Mode</span></span>](#bkmk-medvvsxp)

-   [<span data-ttu-id="0ef61-108">Vorteile von Med-v versus App-v</span><span class="sxs-lookup"><span data-stu-id="0ef61-108">Benefits of MED-V versus App-V</span></span>](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a><span data-ttu-id="0ef61-109">Geschäftsanforderungen für MED-V</span><span class="sxs-lookup"><span data-stu-id="0ef61-109">Business Requirements for MED-V</span></span>


<span data-ttu-id="0ef61-110">Wenn die IT-Abteilung Ihres Unternehmens feststellt, ob ein Upgrade auf Windows 7 durchgeführt werden soll, muss Sie auf Ihre Branchenanwendungen und webbasierten Branchenanwendungen achten, um sicherzustellen, dass diese unter dem neuen Betriebssystem ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="0ef61-110">When your company’s IT department is determining whether to upgrade to Windows 7, it must pay attention to its line-of-business applications and web-based line-of-business applications to make certain that these can run on the new operating system.</span></span> <span data-ttu-id="0ef61-111">Häufig wurden diese Anwendungen und URLs erstellt, um speziell mit einer älteren Version von Windows oder Internet Explorer zu arbeiten, und Probleme können auftreten, wenn Sie versuchen, Sie im neuen Betriebssystem zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ef61-111">Often, these applications and URLs were created to work specifically with an older version of Windows or Internet Explorer, and problems can occur when trying to use them in the new operating system.</span></span> <span data-ttu-id="0ef61-112">Microsoft bietet viele verschiedene Methoden zur Behandlung der verschiedenen Kompatibilitätsprobleme, die beim Upgrade auftreten können, beispielsweise das Application Compatibility Toolkit (Act) und der Windows 7-Programmkompatibilitäts-Assistent.</span><span class="sxs-lookup"><span data-stu-id="0ef61-112">Microsoft offers many different methods for handling the various compatibility issues that can occur when you upgrade, such as the Application Compatibility Toolkit (ACT) and the Windows 7 Program Compatibility Assistant.</span></span> <span data-ttu-id="0ef61-113">Auch nachdem alle Anwendungen auf Kompatibilität getestet wurden und Korrekturen festgelegt wurden, funktionieren einige Anwendungen unter Windows 7 immer noch nicht richtig oder sind zu kostspielig, um Sie zu beheben.</span><span class="sxs-lookup"><span data-stu-id="0ef61-113">But even after all applications have been tested for compatibility and fixes have been determined, some applications still do not work correctly on Windows 7 or are too costly to resolve.</span></span>

<span data-ttu-id="0ef61-114">Mithilfe von MED-V können Sie diese Legacyanwendungen über eine Windows Virtual PC-Umgebung ausführen, auf der Windows XP ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef61-114">By using MED-V, you can run these legacy applications through a Windows Virtual PC environment that is running Windows XP.</span></span> <span data-ttu-id="0ef61-115">Da Sie diese problemanwendungen nicht mehr vor dem Upgrade auf dem neuen Betriebssystem testen und überprüfen müssen, ist die Migration zu Windows 7 viel reibungsloser und schneller.</span><span class="sxs-lookup"><span data-stu-id="0ef61-115">Because you no longer have to test and validate these problem applications on the new operating system before upgrading, your migration to Windows 7 is much smoother and quicker.</span></span>

### <span data-ttu-id="0ef61-116">Verwenden der MED-V-Checkliste</span><span class="sxs-lookup"><span data-stu-id="0ef61-116">Using MED-V Checklist</span></span>

<span data-ttu-id="0ef61-117">Bedenken Sie MED-V, wenn eines der folgenden Szenarien auf Sie zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef61-117">Consider MED-V if any of the following scenarios apply to you:</span></span>

-   <span data-ttu-id="0ef61-118">Sie eine große Organisation sind (beispielsweise 500-Benutzer und mehr), über einen Enterprise-Vertrag mit Microsoft verfügen und planen, ein Upgrade auf Windows 7 durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="0ef61-118">You are a large organization (for example, 500 users and more), have an Enterprise Agreement with Microsoft, and plan to upgrade to Windows 7.</span></span>

-   <span data-ttu-id="0ef61-119">Sie haben Ihre Branchenanwendungen getestet und einige gefunden, die mit Windows 7 nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="0ef61-119">You have tested your line-of-business applications and have found some that are incompatible with Windows 7.</span></span>

-   <span data-ttu-id="0ef61-120">Sie haben die Kompatibilitätsprobleme für einige dieser problemanwendungen behoben, indem Sie die Anwendung aktualisieren oder ein von Microsoft bereitgestelltes Shim verwenden, beispielsweise das Application Compatibility Toolkit (Act), aber Kompatibilitätsprobleme bleiben für einige Anwendungen bestehen.</span><span class="sxs-lookup"><span data-stu-id="0ef61-120">You have resolved the compatibility issues for some of these problem applications by upgrading the application or by using a Microsoft-provided shim, such as the Application Compatibility Toolkit (ACT), but compatibility issues remain for some applications.</span></span>

-   <span data-ttu-id="0ef61-121">Sie haben App-v als eine Option für die Bereitstellung der nicht kompatiblen Anwendungen betrachtet und festgestellt, dass Sie auch nach der Implementierung von App-v weiterhin Kompatibilitätsprobleme mit dem Anwendungs Betriebssystem haben, die Sie berücksichtigen müssen.</span><span class="sxs-lookup"><span data-stu-id="0ef61-121">You have considered App-V as an option for delivering the incompatible applications and have concluded that even after you implement App-V, you still have application operating system compatibility issues that you must address.</span></span>

-   <span data-ttu-id="0ef61-122">Sie haben den Windows XP-Modus als Lösung betrachtet und festgestellt, dass es sich nicht um eine effiziente Option handelt, weil:</span><span class="sxs-lookup"><span data-stu-id="0ef61-122">You have considered Windows XP Mode as a solution and have determined that it is not an efficient option because:</span></span>

    -   <span data-ttu-id="0ef61-123">Sie möchten in der Lage sein, virtuelle Bilder, die die problemanwendungen enthalten, für alle Endbenutzer gleichzeitig bereitzustellen, anstatt einzeln, und die virtuellen Bilder automatisch der Domäne hinzugefügt zu haben.</span><span class="sxs-lookup"><span data-stu-id="0ef61-123">You want to be able to deploy virtual images that contain the problem applications to all end users at the same time, instead of individually, and have the virtual images automatically joined to the domain.</span></span>

    -   <span data-ttu-id="0ef61-124">Sie haben entschieden, dass es weitaus kostengünstiger ist, diese Legacyanwendungen (die praktisch geliefert werden) zu verwalten und die Windows Virtual PC-Einstellungen von einem zentralen Speicherort aus zu steuern, anstatt auf dem Desktop jedes Endbenutzers.</span><span class="sxs-lookup"><span data-stu-id="0ef61-124">You have decided it is much more cost effective to manage these legacy applications (that are delivered virtually) and control the Windows Virtual PC settings from a centralized location instead of on each end user’s desktop.</span></span>

    -   <span data-ttu-id="0ef61-125">Sie möchten in der Lage sein, die virtuellen Computer in Scale anstatt pro Desktop zu aktualisieren und zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0ef61-125">You want to be able to update and support the virtual machines in scale instead of per desktop.</span></span>

    -   <span data-ttu-id="0ef61-126">Sie möchten, dass URLs, die in einer älteren Version von Internet Explorer besser ausgeführt werden, auf die virtuellen Computer umleiten und die URL-Umleitung später einfach verwalten können.</span><span class="sxs-lookup"><span data-stu-id="0ef61-126">You want the ability to redirect URLs that run better on an older version of Internet Explorer to the virtual machines and to easily manage URL redirection later.</span></span>

-   <span data-ttu-id="0ef61-127">Sie haben festgestellt, dass es kostengünstiger und hilfreich wäre, so schnell wie möglich auf Windows 7 zu aktualisieren, und haben beschlossen, die Lösung ihrer verbleibenden Anwendungskompatibilitätsprobleme bis zu einem späteren Zeitpunkt zu verschieben, da Sie wissen, dass Sie über eine Lösung in MED-V verfügen.</span><span class="sxs-lookup"><span data-stu-id="0ef61-127">You have determined that it would be more cost effective and helpful to upgrade to Windows 7 as soon as possible and have decided to postpone resolving your remaining application compatibility issues until a later date, knowing that you have a solution available in MED-V.</span></span>

## <a href="" id="bkmk-medvvsxp"></a> <span data-ttu-id="0ef61-128">Vorteile von MED-V versus Windows XP-Modus</span><span class="sxs-lookup"><span data-stu-id="0ef61-128">Benefits of MED-V versus Windows XP Mode</span></span>


<span data-ttu-id="0ef61-129">Mit Windows Virtual PC für Windows 7 können Sie unterschiedliche Versionen eines Betriebssystems gleichzeitig auf einem einzigen Gerät ausführen und sind in Windows 7 Professional Edition und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0ef61-129">Windows Virtual PC for Windows 7 lets you run different versions of an operating system at the same time on a single device and is included in Windows 7 Professional Edition and higher.</span></span>

<span data-ttu-id="0ef61-130">Die Funktionalität von Windows XP-Modus nutzt Windows Virtual PC, indem ein vorkonfiguriertes Windows XP-Abbild bereitgestellt wird, mit dem Sie eine virtuelle Windows XP-Umgebung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="0ef61-130">Windows XP Mode functionality takes advantage of Windows Virtual PC by providing a preconfigured Windows XP image that lets you create a virtual Windows XP environment.</span></span> <span data-ttu-id="0ef61-131">In dieser virtuellen Umgebung können Sie Anwendungen manuell installieren, die mit Windows 7 nicht kompatibel sind und von Ihrem Desktop aus über den Windows Virtual PC nahtlos ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0ef61-131">In this virtual environment, you can manually install applications that are incompatible with Windows 7 and that run seamlessly from your desktop through Windows Virtual PC.</span></span>

**<span data-ttu-id="0ef61-132">Mithilfe des Windows XP-Modus können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="0ef61-132">By using Windows XP Mode, you can do the following:</span></span>**

-   <span data-ttu-id="0ef61-133">Ausführen von Anwendungen, die mit Windows XP kompatibel sind, in einem virtuellen Computer, der in Windows Virtual PC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef61-133">Run applications that are compatible with Windows XP inside a virtual machine that runs in Windows Virtual PC.</span></span>

-   <span data-ttu-id="0ef61-134">Veröffentlichen Sie diese Anwendungen im Desktop-oder Programmmenü des Hosts.</span><span class="sxs-lookup"><span data-stu-id="0ef61-134">Publish these applications to the host’s desktop or Program menu.</span></span>

<span data-ttu-id="0ef61-135">Wenn Sie diese virtuellen Computer im Rahmen einer Unternehmens Migration zu Windows 7 im großen Maßstab bereitstellen möchten, müssen Sie in der Lage sein, die virtuellen Computer schnell bereitzustellen, effizient bereitzustellen und anzupassen, Ihre Einstellungen zu steuern und Sie einfach zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0ef61-135">When you want to deliver these virtual machines on a large scale as part of an enterprise migration to Windows 7, you must be able to deploy the virtual machines quickly, provision, and customize them efficiently, control their settings, and support them easily.</span></span>

<span data-ttu-id="0ef61-136">MED-V baut auf dem Windows XP-Modus auf, um unternehmensweite Anwendungskompatibilität zu bieten.</span><span class="sxs-lookup"><span data-stu-id="0ef61-136">MED-V builds upon Windows XP Mode to deliver enterprise-wide application compatibility.</span></span> <span data-ttu-id="0ef61-137">Während sich der Windows XP-Modus auf die Bereitstellung virtueller Anwendungsfunktionen für Einzelpersonen und kleine Unternehmen ausrichtet, ermöglicht MED-V die Bereitstellung von vorkonfigurierten Windows XP-Images in großem Umfang im gesamten Unternehmensnetzwerk.</span><span class="sxs-lookup"><span data-stu-id="0ef61-137">Whereas Windows XP mode is limited to providing virtual application functionality to individuals and small businesses, MED-V allows for large-scale deployments of preconfigured Windows XP images throughout your corporate network.</span></span> <span data-ttu-id="0ef61-138">Es bietet Ihnen eine Unternehmens bereite Verwaltungslösung für die Konfiguration, Bereitstellung und Wartung dieser virtuellen MED-V-Arbeitsbereiche.</span><span class="sxs-lookup"><span data-stu-id="0ef61-138">It gives you an enterprise-ready management solution for the configuration, deployment, and maintenance of these virtual MED-V workspaces.</span></span> <span data-ttu-id="0ef61-139">MED-V bietet enterpriseadministrators außerdem eine Reihe von Richtlinien zur Steuerung der Bild Verwendung.</span><span class="sxs-lookup"><span data-stu-id="0ef61-139">MED-V also gives enterpriseadministrators a set of policies to control image use.</span></span> <span data-ttu-id="0ef61-140">Dies beinhaltet, welche Benutzer Zugriff auf welche spezifischen Anwendungen innerhalb dieser Bilder haben werden.</span><span class="sxs-lookup"><span data-stu-id="0ef61-140">This includes which users will have access to which specific applications within these images.</span></span>

**<span data-ttu-id="0ef61-141">Mithilfe von MED-V können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="0ef61-141">By using MED-V, you can do the following:</span></span>**

-   <span data-ttu-id="0ef61-142">Aktualisieren Sie auf Ihr neues Betriebssystem, ohne jede inkompatible Anwendung und URL testen und beheben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="0ef61-142">Upgrade to your new operating system without having to test and resolve every incompatible application and URL.</span></span>

-   <span data-ttu-id="0ef61-143">Stellen Sie virtuelle Windows XP-Bilder bereit, die automatisch mit der Domäne verbunden und pro Benutzer angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="0ef61-143">Deploy virtual Windows XP images that are automatically domain-joined and customized per user.</span></span>

-   <span data-ttu-id="0ef61-144">Bereitstellen von Anwendungen und URL-Umleitungsinformationen für Benutzer</span><span class="sxs-lookup"><span data-stu-id="0ef61-144">Provision applications and URL redirection information to users.</span></span>

-   <span data-ttu-id="0ef61-145">Steuern der Windows Virtual PC-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0ef61-145">Control the Windows Virtual PC settings.</span></span>

-   <span data-ttu-id="0ef61-146">Verwalten und unterstützen von Endpunkten durch Überwachung und Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="0ef61-146">Maintain and support endpoints through monitoring and troubleshooting.</span></span>

-   <span data-ttu-id="0ef61-147">Stellen Sie sicher, dass die Gastcomputer gepatcht werden, auch wenn Sie in einem angehalten-Zustand sind.</span><span class="sxs-lookup"><span data-stu-id="0ef61-147">Ensure that guest computers are patched, even if in a suspended state.</span></span>

-   <span data-ttu-id="0ef61-148">Automatisieren Sie die Erstellung virtueller Computer pro Benutzer und die Sysprep-Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="0ef61-148">Automate per-user virtual machine creation and sysprep initialization.</span></span>

-   <span data-ttu-id="0ef61-149">Einfache Diagnose von Problemen auf den Host-und Gastcomputern</span><span class="sxs-lookup"><span data-stu-id="0ef61-149">Easily diagnose issues on the host and guest computers.</span></span>

-   <span data-ttu-id="0ef61-150">Nahtloses Verwalten von Gastcomputern, die über den Windows Virtual PC-NAT-Modus verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="0ef61-150">Seamlessly manage guest computers that are connected through Windows Virtual PC NAT mode.</span></span>

## <a href="" id="bkmk-medvvsappv"></a><span data-ttu-id="0ef61-151">Vorteile von Med-v versus App-v</span><span class="sxs-lookup"><span data-stu-id="0ef61-151">Benefits of MED-V versus App-V</span></span>


<span data-ttu-id="0ef61-152">Med-v und App-v sind zwei sehr unterschiedliche Technologien, die problemlos zusammenarbeiten können, um Kompatibilitätsprobleme mit dem Anwendungs Betriebssystem zu lösen.</span><span class="sxs-lookup"><span data-stu-id="0ef61-152">MED-V and App-V are two very different technologies that can easily work together to solve your application operating system compatibility issues.</span></span> <span data-ttu-id="0ef61-153">Mithilfe von App-V erstellen Sie für jede Anwendung ein individualisiertes Paket, das jeweils getrennt von den anderen Anwendungen aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef61-153">By using App-V, you create an individualized package for each application, each of which is then kept separate from the others.</span></span> <span data-ttu-id="0ef61-154">Jede virtuelle Anwendung kann dann sofort an den Endbenutzer übermittelt werden, was sehr hilfreich für eine Windows 7-Bereitstellungsstrategie ist.</span><span class="sxs-lookup"><span data-stu-id="0ef61-154">Each virtual application can then be immediately delivered to the end user, which is very useful for a Windows 7 deployment strategy.</span></span>

<span data-ttu-id="0ef61-155">MED-V behandelt Anwendungen nicht einzeln.</span><span class="sxs-lookup"><span data-stu-id="0ef61-155">MED-V does not handle applications individually.</span></span> <span data-ttu-id="0ef61-156">Stattdessen wird eine weitere Instanz von Windows XP auf dem Desktop erstellt, auf dem Windows 7 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef61-156">Instead, it creates an additional instance of Windows XP on the same desktop that is running Windows 7.</span></span> <span data-ttu-id="0ef61-157">Sie können in diesem virtuellen Bild so viele Anwendungen wie nötig installieren und das Bild genauso wie jeden anderen Desktop in Ihrer Organisation verwalten.</span><span class="sxs-lookup"><span data-stu-id="0ef61-157">You can install as many applications as necessary into this virtual image and manage the image just as you would any other desktop in your organization.</span></span>

<span data-ttu-id="0ef61-158">Darüber hinaus können Sie Med-v zusammen mit App-v verwenden, damit virtuelle Anwendungen, die über APP-v sequenziert sind, mithilfe von Med-v installiert, veröffentlicht und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="0ef61-158">In addition, you can use MED-V together with App-V so that virtual applications that are sequenced through App-V are installed, published, and managed by using MED-V.</span></span>

## <span data-ttu-id="0ef61-159">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0ef61-159">Related topics</span></span>


[<span data-ttu-id="0ef61-160">Definieren und Planen der MED-V-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="0ef61-160">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

 

 





