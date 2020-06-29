---
title: So verwenden Sie Dynamic Suite Composition
description: So verwenden Sie Dynamic Suite Composition
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806699"
---
# <span data-ttu-id="3acba-103">So verwenden Sie Dynamic Suite Composition</span><span class="sxs-lookup"><span data-stu-id="3acba-103">How To Use Dynamic Suite Composition</span></span>


<span data-ttu-id="3acba-104">Mit der Dynamic Suite-Komposition in Application Virtualization können Sie eine Anwendung als von einer anderen Anwendung abhängig definieren, beispielsweise von Middleware oder einem Plug-in.</span><span class="sxs-lookup"><span data-stu-id="3acba-104">Dynamic Suite Composition in Application Virtualization enables you to define an application as being dependent on another application, such as middleware or a plug-in.</span></span> <span data-ttu-id="3acba-105">Dadurch kann die Anwendung mit der Middleware oder dem Plug-in in der virtuellen Umgebung interagieren, wobei dies in der Regel verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="3acba-105">This enables the application to interact with the middleware or plug-in in the virtual environment, where typically this is prevented.</span></span> <span data-ttu-id="3acba-106">Dies ist hilfreich, da ein sekundäres Anwendungspaket mit mehreren anderen Anwendungen verwendet werden kann, die als *primäre Anwendungen*bezeichnet werden, sodass jede primäre Anwendung auf dasselbe sekundäre Paket verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="3acba-106">This is useful because a secondary application package can be used with several other applications, referred to as the *primary applications*, which enables each primary application to reference the same secondary package.</span></span>

<span data-ttu-id="3acba-107">Sie können die Dynamic Suite-Komposition verwenden, wenn Sie Anwendungen sequenzieren, die von Plug-ins wie ActiveX-Steuerelementen oder Anwendungen abhängen, die von Middleware wie OLE DB oder Java Runtime Environment (JRE) abhängen.</span><span class="sxs-lookup"><span data-stu-id="3acba-107">You can use Dynamic Suite Composition when you sequence applications that depend on plug-ins such as ActiveX controls or for applications that depend on middleware such as OLE DB or the Java Runtime Environment (JRE).</span></span> <span data-ttu-id="3acba-108">Wenn für jede Anwendung, die diese abhängigen Komponenten verwendet hat, sequenzielle Sequenzierung erforderlich war, einschließlich der Komponenten, müssten Updates für diese Komponenten eine erneute Sequenzierung aller primären Anwendungen erfordern.</span><span class="sxs-lookup"><span data-stu-id="3acba-108">If each application that used these dependent components required sequencing, including the components, updates to those components would require re-sequencing all the primary applications.</span></span> <span data-ttu-id="3acba-109">Wenn Sie die primären Anwendungen ohne die Komponenten sequenzieren und dann die Middleware oder das Plug-in als sekundäres Paket sequenzieren, muss nur das sekundäre Paket aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3acba-109">If you sequence the primary applications without the components and then sequence the middleware or plug-in as a secondary package, then only the secondary package must be updated.</span></span>

<span data-ttu-id="3acba-110">Ein Vorteil dieses Ansatzes besteht darin, dass die Größe der primären Pakete verringert wird.</span><span class="sxs-lookup"><span data-stu-id="3acba-110">One advantage of this approach is that it reduces the size of the primary packages.</span></span> <span data-ttu-id="3acba-111">Ein weiterer Vorteil besteht darin, dass Sie die Zugriffsberechtigungen für sekundäre Anwendungen besser steuern können.</span><span class="sxs-lookup"><span data-stu-id="3acba-111">Another advantage is that it provides you with better control of access permissions on the secondary applications.</span></span> <span data-ttu-id="3acba-112">Beachten Sie, dass die sekundäre Anwendung in regelmäßigen Abständen gestreamt werden kann und nicht vollständig zwischengespeichert werden muss, um ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="3acba-112">Note that the secondary application can be streamed in the regular way and does not have to be fully cached to run.</span></span>

<span data-ttu-id="3acba-113">Ein primäres Paket kann mehr als ein sekundäres Paket aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3acba-113">A primary package can have more than one secondary package.</span></span> <span data-ttu-id="3acba-114">Es wird jedoch nur eine Abhängigkeitsstufe unterstützt, sodass Sie ein sekundäres Paket nicht als abhängig von einem anderen sekundären Paket definieren können.</span><span class="sxs-lookup"><span data-stu-id="3acba-114">However, only one level of dependency is supported, so you cannot define a secondary package as dependent on another secondary package.</span></span> <span data-ttu-id="3acba-115">Auch die sekundäre Anwendung kann nur Middleware oder ein Plug-in sein und kann kein weiteres vollständiges Softwareprodukt sein.</span><span class="sxs-lookup"><span data-stu-id="3acba-115">Also the secondary application can only be middleware or a plug-in and cannot be another full software product.</span></span>

<span data-ttu-id="3acba-116">Wenn Sie beabsichtigen, mehrere primäre Anwendungen von einem einzelnen Middleware-Produkt abhängig zu machen, stellen Sie sicher, dass Sie diese Konfiguration testen, um die potenziellen Auswirkungen auf die Systemleistung zu ermitteln, bevor Sie Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3acba-116">If you plan to make several primary applications dependent on a single middleware product, make sure that you test this configuration to determine the potential effect on system performance before you deploy it.</span></span>

<span data-ttu-id="3acba-117">**Wichtig**  Paketabhängigkeiten können als obligatorisch für eine primäre Anwendung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3acba-117">**Important** Package dependencies can be specified as mandatory for a primary application.</span></span> <span data-ttu-id="3acba-118">Wenn ein sekundäres Paket als obligatorisch gekennzeichnet ist und während des Ladens nicht zugegriffen werden kann, tritt beim Laden des sekundären Pakets ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3acba-118">If a secondary package is flagged as mandatory and it cannot be accessed for some reason during loading, the load of the secondary package will fail.</span></span> <span data-ttu-id="3acba-119">Außerdem schlägt die primäre Anwendung fehl, wenn der Benutzer versucht, Sie zu starten.</span><span class="sxs-lookup"><span data-stu-id="3acba-119">Also, the primary application will fail when the user tries to start it.</span></span>

 

<span data-ttu-id="3acba-120">Sie können die folgenden Verfahren zum Erstellen eines sekundären Pakets für ein Plug-in oder eine Middleware-Komponente verwenden, und dann können Sie das letzte Verfahren verwenden, um die Abhängigkeit in der OSD-Datei des sekundären Pakets zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3acba-120">You can use the following procedures to create a secondary package, for either a plug-in or a middleware component, and then you can use the final procedure to define the dependency in the OSD file of the secondary package.</span></span>

**<span data-ttu-id="3acba-121">So erstellen Sie ein sekundäres Paket für ein Plug-in mithilfe der Dynamic Suite-Komposition</span><span class="sxs-lookup"><span data-stu-id="3acba-121">To create a secondary package for a plug-in by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="3acba-122">Installieren Sie Application Virtualization Sequencer auf einem Sequenzcomputer, der mit einem sauberen Bild eingerichtet ist, und speichern Sie den Computerzustand.</span><span class="sxs-lookup"><span data-stu-id="3acba-122">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="3acba-123">Sequenzieren Sie die primäre Anwendung, und speichern Sie das Paket im Inhaltsordner auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="3acba-123">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

3.  <span data-ttu-id="3acba-124">Wiederherstellen des Sequenz Computers in seinem gespeicherten Zustand aus Schritt 1.</span><span class="sxs-lookup"><span data-stu-id="3acba-124">Restore the sequencing computer to its saved state from step 1.</span></span>

4.  <span data-ttu-id="3acba-125">Installieren und konfigurieren Sie die primäre Anwendung lokal auf dem Sequenzcomputer.</span><span class="sxs-lookup"><span data-stu-id="3acba-125">Install and configure the primary application locally on the sequencing computer.</span></span>

    <span data-ttu-id="3acba-126">**Wichtig**  Sie müssen einen neuen Paketstamm für das sekundäre Paket angeben.</span><span class="sxs-lookup"><span data-stu-id="3acba-126">**Important** You must specify a new package root for the secondary package.</span></span>

     

5.  <span data-ttu-id="3acba-127">Starten Sie die Sequencer-Überwachungsphase.</span><span class="sxs-lookup"><span data-stu-id="3acba-127">Start the sequencer monitoring phase.</span></span>

6.  <span data-ttu-id="3acba-128">Installieren Sie das Plug-in auf dem Sequenzcomputer, und konfigurieren Sie es nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="3acba-128">Install the plug-in on the sequencing computer and configure it as needed.</span></span>

7.  <span data-ttu-id="3acba-129">Öffnen Sie die primäre Anwendung, und stellen Sie sicher, dass das Plug-in ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3acba-129">Open the primary application, and confirm that the plug-in is working correctly.</span></span>

8.  <span data-ttu-id="3acba-130">Erstellen Sie in der Sequencer-Konsole eine Dummy-Anwendung zur Darstellung des sekundären Pakets, das das Plug-in enthalten soll, und wählen Sie ein Symbol aus.</span><span class="sxs-lookup"><span data-stu-id="3acba-130">In the sequencer console, create a dummy application to represent the secondary package that will contain the plug-in and select an icon.</span></span>

9.  <span data-ttu-id="3acba-131">Speichern Sie das Paket im Inhaltsordner auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="3acba-131">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="3acba-132">**Hinweis**  Um die Verwaltung sekundärer Pakete zu unterstützen, wird empfohlen, dass der Paketname den Begriff "sekundäres Paket" enthält, um hervorzuheben, dass es sich um ein Paket handelt, das nicht als eigenständige Anwendung verwendet werden kann, beispielsweise **\ [Plug in Name \]-sekundäres Paket**.</span><span class="sxs-lookup"><span data-stu-id="3acba-132">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Plug In Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="3acba-133">So erstellen Sie ein sekundäres Paket für Middleware mithilfe der Dynamic Suite-Komposition</span><span class="sxs-lookup"><span data-stu-id="3acba-133">To create a secondary package for middleware by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="3acba-134">Installieren Sie Application Virtualization Sequencer auf einem Sequenzcomputer, der mit einem sauberen Bild eingerichtet ist, und speichern Sie den Computerzustand.</span><span class="sxs-lookup"><span data-stu-id="3acba-134">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="3acba-135">Installieren Sie die Middleware lokal auf dem Sequenzcomputer, und konfigurieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="3acba-135">Install the middleware locally on the sequencing computer, and configure it.</span></span>

3.  <span data-ttu-id="3acba-136">Sequenzieren Sie die primäre Anwendung, und speichern Sie das Paket im Inhaltsordner auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="3acba-136">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

4.  <span data-ttu-id="3acba-137">Wiederherstellen des Sequenz Computers in seinem gespeicherten Zustand aus Schritt 1.</span><span class="sxs-lookup"><span data-stu-id="3acba-137">Restore the sequencing computer to its saved state from step 1.</span></span>

5.  <span data-ttu-id="3acba-138">Starten Sie den Sequencer, um ein neues Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3acba-138">Start the sequencer to create a new package.</span></span>

6.  <span data-ttu-id="3acba-139">Starten Sie die Sequencer-Überwachungsphase.</span><span class="sxs-lookup"><span data-stu-id="3acba-139">Start the sequencer monitoring phase.</span></span>

7.  <span data-ttu-id="3acba-140">Installieren Sie die Middleware-Anwendung auf dem Sequenzcomputer, und konfigurieren Sie Sie wie in einer typischen Installation.</span><span class="sxs-lookup"><span data-stu-id="3acba-140">Install the middleware application on the sequencing computer, and configure it as in a typical installation.</span></span>

8.  <span data-ttu-id="3acba-141">Durchführen des Sequenz Prozesses</span><span class="sxs-lookup"><span data-stu-id="3acba-141">Complete the sequencing process.</span></span>

9.  <span data-ttu-id="3acba-142">Speichern Sie das Paket im Inhaltsordner auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="3acba-142">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="3acba-143">**Hinweis**  Um die Verwaltung sekundärer Pakete zu unterstützen, wird empfohlen, dass der Paketname den Begriff "sekundäres Paket" enthält, um hervorzuheben, dass es sich um ein Paket handelt, das nicht als eigenständige Anwendung verwendet werden kann, beispielsweise " **\ [Middleware Name \]"-sekundäres Paket**.</span><span class="sxs-lookup"><span data-stu-id="3acba-143">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Middleware Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="3acba-144">So definieren Sie die Abhängigkeit im primären Paket</span><span class="sxs-lookup"><span data-stu-id="3acba-144">To define the dependency in the primary package</span></span>**

1. <span data-ttu-id="3acba-145">Öffnen Sie auf dem Server die OSD-Datei des sekundären Pakets zur Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="3acba-145">On the server, open the OSD file of the secondary package for editing.</span></span> <span data-ttu-id="3acba-146">(Es empfiehlt sich, einen XML-Editor zu verwenden, um Änderungen an der OSD-Datei vorzunehmen; Sie können jedoch auch Notepad als Alternative verwenden.)</span><span class="sxs-lookup"><span data-stu-id="3acba-146">(It is a good idea to use an XML editor to make changes to the OSD file; however, you can use Notepad as an alternative.)</span></span>

2. <span data-ttu-id="3acba-147">Kopieren Sie die **CODEBASE-HREF** -Zeile aus der Datei.</span><span class="sxs-lookup"><span data-stu-id="3acba-147">Copy the **CODEBASE HREF** line from that file.</span></span>

3. <span data-ttu-id="3acba-148">Öffnen Sie die OSD-Datei des primären Pakets zur Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="3acba-148">Open the OSD file of the primary package for editing.</span></span>

4. <span data-ttu-id="3acba-149">Fügen Sie das Tag <strong> &lt; Dependencies &gt; </strong> nach dem Schließen des \*\* &lt; /ENVLIST &gt; \*\* -Tags am Ende des \*\* &lt; VIRTUALENV &gt; \*\* -Abschnitts direkt vor dem \*\* &lt; &gt; /VIRTUALENV\*\* -Tag ein.</span><span class="sxs-lookup"><span data-stu-id="3acba-149">Insert the <strong>&lt;DEPENDENCIES&gt;</strong>tag after the close of **&lt;/ENVLIST&gt;** tag at the end of the **&lt;VIRTUALENV&gt;** section just before the **&lt;/VIRTUALENV&gt;** tag.</span></span>

5. <span data-ttu-id="3acba-150">Fügen Sie die **CODEBASE-HREF** -Zeile aus dem sekundären Paket nach dem soeben erstellten \*\* &lt; Dependencies &gt; \*\* -Tag ein.</span><span class="sxs-lookup"><span data-stu-id="3acba-150">Paste the **CODEBASE HREF** line from the secondary package after the **&lt;DEPENDENCIES&gt;** tag you just created.</span></span>

6. <span data-ttu-id="3acba-151">Wenn das sekundäre Paket ein obligatorisches Paket ist, was bedeutet, dass es gestartet werden muss, bevor das primäre Paket gestartet wird, fügen Sie die Eigenschaft **Mandatory = "true"** innerhalb des **CodeBase** -Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="3acba-151">If the secondary package is a mandatory package, which means that it must be started before the primary package is started, add the **MANDATORY=”TRUE”** property inside the **CODEBASE** tag.</span></span> <span data-ttu-id="3acba-152">Wenn dies nicht zwingend erforderlich ist, kann die Eigenschaft ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="3acba-152">If it is not mandatory, the property can be omitted.</span></span>

7. <span data-ttu-id="3acba-153">Schließen Sie das \*\* &lt; Dependencies &gt; \*\* -Tag, indem Sie Folgendes einfügen:</span><span class="sxs-lookup"><span data-stu-id="3acba-153">Close the **&lt;DEPENDENCIES&gt;** tag by inserting the following:</span></span>

   **<span data-ttu-id="3acba-154">&lt;/DEPENDENCIES&gt;</span><span class="sxs-lookup"><span data-stu-id="3acba-154">&lt;/DEPENDENCIES&gt;</span></span>**

8. <span data-ttu-id="3acba-155">Überprüfen Sie die Änderungen, die Sie an der OSD-Datei vorgenommen haben, und speichern Sie die Datei, und schließen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="3acba-155">Review the changes that you made to the OSD file, and then save and close the file.</span></span> <span data-ttu-id="3acba-156">Im folgenden Beispiel wird gezeigt, wie der hinzugefügte Abschnitt angezeigt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="3acba-156">The following example shows how the added section should appear.</span></span> <span data-ttu-id="3acba-157">Die hier gezeigten Tag-Werte sind beispielsweise nur.</span><span class="sxs-lookup"><span data-stu-id="3acba-157">The tag values shown here are for example only.</span></span>

   **<span data-ttu-id="3acba-158">&lt;VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="3acba-158">&lt;VIRTUALENV&gt;</span></span>**

        **&lt;ENVLIST&gt;**

   **<span data-ttu-id="3acba-159">…</span><span class="sxs-lookup"><span data-stu-id="3acba-159">…</span></span>**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **<span data-ttu-id="3acba-160">&lt;/VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="3acba-160">&lt;/VIRTUALENV&gt;</span></span>**

9. <span data-ttu-id="3acba-161">Wenn das sekundäre Paket Einträge im \*\* &lt; ENVLIST &gt; \*\* -Abschnitt der OSD-Datei enthält, müssen Sie diese Einträge in denselben Abschnitt im primären Paket kopieren.</span><span class="sxs-lookup"><span data-stu-id="3acba-161">If the secondary package has any entries in the **&lt;ENVLIST&gt;** section of the OSD file, you must copy those entries to the same section in the primary package.</span></span>

## <span data-ttu-id="3acba-162">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3acba-162">Related topics</span></span>


[<span data-ttu-id="3acba-163">Erstellen oder Aktualisieren virtueller Anwendungen mit dem App-V-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="3acba-163">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





