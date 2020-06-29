---
title: App-V 4.6 SP1 – Versionshinweise
description: App-V 4.6 SP1 – Versionshinweise
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808067"
---
# <span data-ttu-id="9cc5d-103">App-V 4.6 SP1 – Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="9cc5d-103">App-V 4.6 SP1 Release Notes</span></span>


<span data-ttu-id="9cc5d-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="9cc5d-105">**Wichtig**  Lesen Sie diese Versionshinweise gründlich, bevor Sie das Microsoft Application Virtualization (App-V)-Verwaltungs System installieren.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-105">**Important** Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="9cc5d-106">Diese Anmerkungen zu dieser Version enthalten Informationen, die Ihnen bei der erfolgreichen Installation von Application Virtualization (App-V) 4.6 SP1 helfen.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="9cc5d-107">Dieses Dokument enthält Informationen, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="9cc5d-108">Wenn es einen Unterschied zwischen diesen Anmerkungen zu dieser Version und einer anderen App-V-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span>

 

## <span data-ttu-id="9cc5d-109">Schutz vor Sicherheitsrisiken und Viren</span><span class="sxs-lookup"><span data-stu-id="9cc5d-109">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="9cc5d-110">Zum Schutz vor Sicherheitsrisiken und Viren ist es wichtig, die neuesten verfügbaren Sicherheitsupdates für jede neue Software zu installieren, die installiert wird.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-110">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="9cc5d-111">Weitere Informationen finden Sie auf der [Microsoft-Sicherheitswebsite](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="9cc5d-111">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="9cc5d-112">Bekannte Probleme mit Application Virtualization 4.6 SP1</span><span class="sxs-lookup"><span data-stu-id="9cc5d-112">Known Issues with Application Virtualization4.6 SP1</span></span>


<span data-ttu-id="9cc5d-113">In diesem Abschnitt finden Sie die neuesten Informationen zu Problemen mit Microsoft Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-113">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="9cc5d-114">Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-114">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="9cc5d-115">Wenn dies möglich ist, werden diese Probleme in späteren Versionen behoben.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-115">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="9cc5d-116">Der Pfad von sprt geht verloren, wenn er nicht in Schrägstrich (/) endet.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-116">Path from SPRT is lost if it does not end in forward slash ( / )</span></span>

<span data-ttu-id="9cc5d-117">Wenn der Pfad in einem href-Objekt in einer Projektvorlage nicht mit einem Schrägstrich ( **/** ) endet, enthält die generierte href den Pfad nicht.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-117">When the path in an HREF in a project template does not end with a forward slash (**/**), the generated HREF does not include the path.</span></span> <span data-ttu-id="9cc5d-118">Dies tritt auf, wenn der Benutzer die **sprt-** Datei manuell bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-118">This occurs when the user manually manipulates the **.sprt** file.</span></span> <span data-ttu-id="9cc5d-119">Wenn Sie den Sequencer verwenden, wird nach dem Pfad immer der Schrägstrich () hinzugefügt **/** .</span><span class="sxs-lookup"><span data-stu-id="9cc5d-119">If you use the sequencer it always adds the forward slash (**/**) after the path.</span></span>

<span data-ttu-id="9cc5d-120">Problemumgehung stellen Sie sicher, dass die href einen nachgestellten Schrägstrich () aufweist **/** .</span><span class="sxs-lookup"><span data-stu-id="9cc5d-120">WORKAROUND Make sure that the HREF has a trailing forward slash (**/**).</span></span>

### <span data-ttu-id="9cc5d-121">Der Name des Benutzerordners entspricht nicht dem Paketnamen.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-121">User folder name do not correspond to the package name</span></span>

<span data-ttu-id="9cc5d-122">Ordner, die Benutzer-und Global. pkg-Dateien enthalten, enthalten nicht mehr den Paketnamen.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-122">Folders that contain user and global .pkg files no longer include the package name.</span></span> <span data-ttu-id="9cc5d-123">Zuvor verwendete der App-V-Client den Paketstamm Ordner 8,3 Short Name als Teil des Ordner namens.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-123">Previously, the App-V client used to use the package root folder 8.3 short name as part of the folder name.</span></span> <span data-ttu-id="9cc5d-124">So können Sie Sie ganz einfach erkennen.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-124">This lets you easily identify it.</span></span> <span data-ttu-id="9cc5d-125">Wenn Sie den App-V 4,6 SP1-Sequenzer verwenden, sind die kurz Namen des Paketstamm Ordners 8,3 nun zufällige Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-125">When you use the App-V 4.6 SP1 sequencer, the package root folder 8.3 short names are now random strings.</span></span> <span data-ttu-id="9cc5d-126">Dadurch ist es schwierig, die Ordner zu identifizieren, die die **pkg** -Dateien des Pakets auf dem Computer enthalten, auf dem der App-V-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-126">This makes it difficult to identify the folders that contain the package’s **.pkg** files on the computer that is running the App-V client.</span></span>

<span data-ttu-id="9cc5d-127">Problemumgehung verwenden Sie eine der folgenden Methoden, um diese Paketordner leichter zu erkennen:</span><span class="sxs-lookup"><span data-stu-id="9cc5d-127">WORKAROUND Use one of the following methods to more easily identify these package folders:</span></span>

1.  <span data-ttu-id="9cc5d-128">Wenn Sie das Paket mithilfe des Sequencers erstellen, geben Sie einen Ordnernamen an, der der 8,3-Benennungskonvention für den primären Anwendungsordner entspricht.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-128">When you create the package by using the Sequencer, specify a folder name that follows the 8.3 naming convention for the primary application folder.</span></span> <span data-ttu-id="9cc5d-129">Dieser Name wird dann als Teil des benutzerordnernamens verwendet, wie dies in App-V 4,6 der Fall war.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-129">This name will then be used as part of the user folder name as was the case in App-V 4.6.</span></span>

2.  <span data-ttu-id="9cc5d-130">Die SPRJ-Datei enthält jetzt ein Tag, in dem die Zeichenfolge angezeigt wird, die als Anfang des benutzerordnernamens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-130">The .sprj file now contains a tag that displays the string that is used as the beginning of the user folder name.</span></span> <span data-ttu-id="9cc5d-131">Sie können das **Shortname** -Element des **PACKAGEROOTFOLDER** -Elements verwenden, um den Namen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-131">You can use the **SHORTNAME** element of the **PACKAGEROOTFOLDER** element to determine the name.</span></span>

### <span data-ttu-id="9cc5d-132">Ausführen von App-V 4,6 SP1 auf Computern mit mehr als 64 Prozessoren</span><span class="sxs-lookup"><span data-stu-id="9cc5d-132">Running App-V 4.6 SP1 on computers that have more than 64 processors</span></span>

<span data-ttu-id="9cc5d-133">Wenn Sie App-v 4,6 SP1 auf Computern ausführen, auf denen mehr als 64-Prozessoren installiert sind, schlägt der APP-v-Client fehl.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-133">When you run App-V 4.6 SP1 on computers that have more than 64 processors installed, the App-V client fails.</span></span>

<span data-ttu-id="9cc5d-134">Problemumgehung keine.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-134">WORKAROUND None.</span></span> <span data-ttu-id="9cc5d-135">Diese Konfiguration wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-135">This configuration is not supported.</span></span> <span data-ttu-id="9cc5d-136">Sie müssen App-V 4,6 SP1on-Computer ausführen, die weniger als 64-Prozessoren aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-136">You must run App-V 4.6 SP1on computers that have fewer than 64 processors.</span></span>

### <span data-ttu-id="9cc5d-137">Application Virtualization 4,6 SP1-Update wird nicht in allen Gebietsschemas angeboten, die Microsoft Update verwenden</span><span class="sxs-lookup"><span data-stu-id="9cc5d-137">Application Virtualization 4.6 SP1 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="9cc5d-138">Wenn Sie Microsoft Update verwenden, steht das Update für App-V 4,6 SP1 für die folgenden Sprachgebietsschemas nicht zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="9cc5d-138">When you use Microsoft Update, the update for App-V 4.6 SP1 is not available for the following language locales:</span></span>

-   <span data-ttu-id="9cc5d-139">Kasachisch</span><span class="sxs-lookup"><span data-stu-id="9cc5d-139">Kazakh</span></span>

-   <span data-ttu-id="9cc5d-140">Hindi</span><span class="sxs-lookup"><span data-stu-id="9cc5d-140">Hindi</span></span>

-   <span data-ttu-id="9cc5d-141">Serbisch-Kyrillisch</span><span class="sxs-lookup"><span data-stu-id="9cc5d-141">Serbian-Cyrillic</span></span>

<span data-ttu-id="9cc5d-142">PROBLEMUMGEHUNG Wenn Sie Microsoft Windows Server Update Services (WSUS) verwenden, verwenden Sie die englische Version des Updates, oder laden Sie das Update aus dem Microsoft Update-Katalog herunter.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-142">WORKAROUND If you are using Microsoft Windows Server Update Services (WSUS) use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

### <span data-ttu-id="9cc5d-143">Nach dem Erweitern des übergeordneten Pakets können Sie ein Plug-in nicht mit nebeneinander angeordneten Komponenten Sequenzen</span><span class="sxs-lookup"><span data-stu-id="9cc5d-143">After expanding the parent package, you cannot sequence a plug-in with side by side components</span></span>

<span data-ttu-id="9cc5d-144">Wenn Sie ein übergeordnetes Paket erweitern **Tools**, indem Sie  /  in der App-V Sequencer-Konsole Tools**zum Erweitern des Pakets in lokales System** verwenden und ein Plug-in mit parallelen Komponenten Sequenzen, wird ein Installationsfehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-144">When you expand a parent package by using **Tools** / **Expand Package to Local System** in the App-V Sequencer console and you sequence a plug-in with side by side components, an installation error is returned.</span></span> <span data-ttu-id="9cc5d-145">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9cc5d-145">For example:</span></span>

-   **<span data-ttu-id="9cc5d-146">HRESULT 0x80073712</span><span class="sxs-lookup"><span data-stu-id="9cc5d-146">HRESULT 0x80073712</span></span>**

<span data-ttu-id="9cc5d-147">Dies wird verursacht, wenn der Sequencer die parallele Komponente in die Registrierung schreibt, aber den Wert für den folgenden Registrierungsschlüssel nicht löscht:</span><span class="sxs-lookup"><span data-stu-id="9cc5d-147">This is caused when the sequencer writes the side-by-side component to the registry but does not clear the value for the following registry key:</span></span>

<span data-ttu-id="9cc5d-148">HKEY \ _LOCAL \ _MACHINE \\components\\storedirty</span><span class="sxs-lookup"><span data-stu-id="9cc5d-148">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="9cc5d-149">Problemumgehung nachdem Sie das übergeordnete Paket auf dem Computer, auf dem der Sequencer ausgeführt wird, erweitert haben, müssen Sie den Wert für den folgenden Registrierungsschlüssel löschen:</span><span class="sxs-lookup"><span data-stu-id="9cc5d-149">WORKAROUND After expanding the parent package on the computer that is running the sequencer, you have to delete the value for the following registry key:</span></span>

<span data-ttu-id="9cc5d-150">HKEY \ _LOCAL \ _MACHINE \\components\\storedirty</span><span class="sxs-lookup"><span data-stu-id="9cc5d-150">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="9cc5d-151">Nachdem Sie den Wert gelöscht haben, müssen Sie das Plug-in sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-151">After you have deleted the value, sequence the plug-in.</span></span>

### <span data-ttu-id="9cc5d-152">Anmerkungen zu dieser Version Copyright-Informationen</span><span class="sxs-lookup"><span data-stu-id="9cc5d-152">Release Notes Copyright Information</span></span>

<span data-ttu-id="9cc5d-153">Dieses Dokument wird "as-is" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-153">This document is provided “as-is”.</span></span> <span data-ttu-id="9cc5d-154">Informationen und Ansichten, die in diesem Dokument ausgedrückt werden, wie URL und andere Verweise auf Internet Websites, können sich ohne Vorankündigung ändern.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-154">Information and views expressed in this document, such as URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="9cc5d-155">Das Risiko der Nutzung dieser Informationen liegt beim Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-155">You bear the risk of using it.</span></span>

<span data-ttu-id="9cc5d-156">Einige hier dargestellte Beispiele werden nur zur Illustration bereitgestellt und sind fiktiv.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="9cc5d-157">Es ist keine wirkliche Zuordnung oder Verbindung vorgesehen oder sollte abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="9cc5d-158">Dieses Dokument stellt Ihnen keinerlei Rechte am geistigen Eigentum eines beliebigen Microsoft-Produkts zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="9cc5d-159">Dieses Dokument darf für interne Referenzzwecke kopiert und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-159">You may copy and use this document for your internal, reference purposes.</span></span> <span data-ttu-id="9cc5d-160">Sie können dieses Dokument für Ihre internen, Referenzzwecke ändern.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-160">You may modify this document for your internal, reference purposes.</span></span>



<span data-ttu-id="9cc5d-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server und Windows Vista sind Marken der Microsoft-Unternehmensgruppe.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="9cc5d-162">Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.</span><span class="sxs-lookup"><span data-stu-id="9cc5d-162">All other trademarks are property of their respective owners.</span></span>

 

 





