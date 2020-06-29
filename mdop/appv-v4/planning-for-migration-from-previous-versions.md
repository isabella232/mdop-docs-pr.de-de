---
title: Planen der Migration von früheren Versionen
description: Planen der Migration von früheren Versionen
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806503"
---
# <span data-ttu-id="db257-103">Planen der Migration von früheren Versionen</span><span class="sxs-lookup"><span data-stu-id="db257-103">Planning for Migration from Previous Versions</span></span>


<span data-ttu-id="db257-104">Bevor Sie versuchen, auf Microsoft Application Virtualization 4.5 oder höhere Versionen zu aktualisieren, muss jede Version vor 4.1 auf Version 4.1 aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="db257-104">Before attempting to upgrade to Microsoft Application Virtualization4.5 or later versions, any version prior to4.1 must be upgraded to version4.1.</span></span> <span data-ttu-id="db257-105">Sie sollten zunächst planen, Ihre Clients zu aktualisieren und dann die Server Komponenten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="db257-105">You should plan to upgrade your clients first, and then upgrade the server components.</span></span> <span data-ttu-id="db257-106">Clients, die auf 4.5 aktualisiert wurden, arbeiten weiterhin mit Application Virtualization-Servern, die noch nicht aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="db257-106">Clients that have been upgraded to4.5 will continue to work with Application Virtualization servers that have not yet been upgraded.</span></span> <span data-ttu-id="db257-107">Frühere Versionen des Clients werden auf Servern, die auf 4.5 aktualisiert wurden, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db257-107">Earlier versions of the client are not supported on servers that have been upgraded to4.5.</span></span> <span data-ttu-id="db257-108">Weitere Informationen zum Aktualisieren der Systemkomponenten finden Sie unter [Überlegungen zur Implementierung und zum Upgrade von Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="db257-108">For more information about upgrading the system components, see [Application Virtualization Deployment and Upgrade Considerations](application-virtualization-deployment-and-upgrade-considerations.md).</span></span>

<span data-ttu-id="db257-109">Zur Sicherstellungeiner erfolgreichen Migration sollten die Komponenten des Application Virtualization-Systems in der folgenden Reihenfolge aktualisiert werden:</span><span class="sxs-lookup"><span data-stu-id="db257-109">To help ensure a successful migration, the Application Virtualization system components should be upgraded in the following order:</span></span>

1.  **<span data-ttu-id="db257-110">Microsoft Application Virtualization-Clients.</span><span class="sxs-lookup"><span data-stu-id="db257-110">Microsoft Application Virtualization Clients.</span></span>** <span data-ttu-id="db257-111">Eine Schritt-für-Schritt-Anleitung finden Sie unter [Aktualisieren des Application Virtualization-Clients](how-to-upgrade-the-application-virtualization-client.md).</span><span class="sxs-lookup"><span data-stu-id="db257-111">For step-by-step upgrade instructions, see [How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).</span></span>

2.  **<span data-ttu-id="db257-112">Microsoft Application Virtualization-Server und-Datenbank</span><span class="sxs-lookup"><span data-stu-id="db257-112">Microsoft Application Virtualization Servers and Database.</span></span>** <span data-ttu-id="db257-113">Eine schrittweise Anleitung zum Upgrade finden Sie unter [Aktualisieren der Server und System Komponenten](how-to-upgrade-the-servers-and-system-components.md).</span><span class="sxs-lookup"><span data-stu-id="db257-113">For step-by-step upgrade instructions, see [How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md).</span></span>

    <span data-ttu-id="db257-114">**Hinweis**  Wenn Sie über mehr als einen Serverfreigabe Zugriff auf die Application Virtualization-Datenbank verfügen, müssen alle diese Server offline geschaltet werden, während die Datenbank aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="db257-114">**Note** If you have more than one server sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="db257-115">Sie sollten ihre normalen Geschäftsmethoden für das Datenbankupgrade befolgen, es empfiehlt sich jedoch, das Datenbankupgrade mithilfe einer Sicherungskopie der Datenbank zuerst auf einem Testserver zu testen.</span><span class="sxs-lookup"><span data-stu-id="db257-115">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="db257-116">Wählen Sie dann einen der Server für das erste Upgrade aus, um das Datenbankschema zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="db257-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="db257-117">Nachdem die Produktionsdatenbank erfolgreich aktualisiert wurde, können Sie die anderen Server aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="db257-117">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

     

3.  **<span data-ttu-id="db257-118">Microsoft Application Virtualization Management Web Service.</span><span class="sxs-lookup"><span data-stu-id="db257-118">Microsoft Application Virtualization Management Web Service.</span></span>** <span data-ttu-id="db257-119">Dieser Schritt gilt nur, wenn sich der Verwaltungs-Web-Service auf einem separaten Server befindet, was erfordert, dass Sie das Serverinstallationsprogramm auf diesem separaten Server ausführen, um den Webdienst zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="db257-119">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Web service.</span></span> <span data-ttu-id="db257-120">Andernfalls führt der vorherige Server Upgrade-Schritt automatisch zu einem Upgrade des Verwaltungs-Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="db257-120">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span>

4.  **<span data-ttu-id="db257-121">Microsoft Application Virtualization-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="db257-121">Microsoft Application Virtualization Management Console.</span></span>** <span data-ttu-id="db257-122">Dieser Schritt gilt nur, wenn sich die Verwaltungskonsole auf einem separaten Computer befindet, was erfordert, dass Sie das Serverinstallationsprogramm auf diesem separaten Computer ausführen, um die Konsole zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="db257-122">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="db257-123">Andernfalls wird der vorherige Server Aktualisierungsschritt die Verwaltungskonsole aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="db257-123">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span>

5.  **<span data-ttu-id="db257-124">Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="db257-124">Microsoft Application Virtualization Sequencer.</span></span>** <span data-ttu-id="db257-125">Schritt-für-Schritt-Anleitungen finden Sie unter so wird es [gemacht: Installieren des Application Virtualization Sequencers](how-to-install-the-application-virtualization-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="db257-125">For step-by-step instructions, see [How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span></span> <span data-ttu-id="db257-126">Alle virtuellen Anwendungspakete, die in Version 4.2 sequenziert sind, müssen nicht für die Verwendung mit Version 4.5 neu sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="db257-126">Any virtual application packages sequenced in version4.2 will not have to be re-sequenced for use with version4.5.</span></span> <span data-ttu-id="db257-127">Sie sollten jedoch das Upgrade der virtuellen Pakete auf das Microsoft Application Virtualization 4.5-Format erwägen, wenn Sie standardmäßige Zugriffssteuerungslisten (Access Control Lists, ACLs) anwenden oder eine Windows Installer-Datei generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="db257-127">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization4.5 format if you would like to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="db257-128">Dies ist ein einfacher Vorgang und erfordert nur, dass das vorhandene virtuelle Anwendungspaket mit dem 4.5-Sequenzer geöffnet und gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="db257-128">This is a simple process and requires only that the existing virtual application package be opened and saved with the4.5 Sequencer.</span></span> <span data-ttu-id="db257-129">Dies kann mithilfe der Befehlszeilenschnittstelle Application Virtualization Sequencer automatisiert werden.</span><span class="sxs-lookup"><span data-stu-id="db257-129">This can be automated by using the Application Virtualization Sequencer command-line interface.</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="db257-130">Unterstützung für App-v 4.6-Client Pakete</span><span class="sxs-lookup"><span data-stu-id="db257-130">App-V4.6 Client Package Support</span></span>


<span data-ttu-id="db257-131">Sie können Pakete bereitstellen, die in früheren Versionen von App-v für App-v 4.6-Clients erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="db257-131">You can deploy packages created in previous versions of App-V to App-V4.6 Clients.</span></span> <span data-ttu-id="db257-132">Sie müssen jedoch die zugehörige **OSD** -Datei so ändern, dass Sie die entsprechenden Informationen zum Betriebssystem und zur Chiparchitektur enthält.</span><span class="sxs-lookup"><span data-stu-id="db257-132">However, you must modify the associated **.osd** file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="db257-133">Verwenden Sie die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="db257-133">Use the following values.</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db257-134">Betriebssystem Wert</span><span class="sxs-lookup"><span data-stu-id="db257-134">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db257-135">&lt;BS-Wert = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-135">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db257-136">&lt;BS-Wert = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-136">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db257-137">&lt;BS-Wert = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-137">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db257-138">&lt;BS-Wert = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-138">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db257-139">&lt;BS-Wert = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-139">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db257-140">&lt;BS-Wert = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-140">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db257-141">&lt;BS-Wert = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-141">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db257-142">&lt;BS-Wert = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-142">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db257-143">&lt;BS-Wert = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-143">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db257-144">&lt;BS-Wert = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-144">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db257-145">&lt;BS-Wert = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="db257-145">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="db257-146">Wenn Sie ein neu erstelltes 32-Bit-Paket ausführen möchten, müssen Sie die Anwendung auf einem Computer mit einem 32-Bit-Betriebssystem mit dem App-v 4.6 Sequencer abgleichen.</span><span class="sxs-lookup"><span data-stu-id="db257-146">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V4.6 Sequencer installed.</span></span> <span data-ttu-id="db257-147">Nachdem Sie die Anwendung sequenziert haben, wählen Sie in der Sequencer-Konsole die Registerkarte **Bereitstellung** aus, und geben Sie dann die gewünschte Betriebssystem-und Chiparchitektur an.</span><span class="sxs-lookup"><span data-stu-id="db257-147">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="db257-148">**Wichtig**  Anwendungen, die auf einem Computer mit einem 64-Bit-Betriebssystem sequenziert sind, müssen auf Computern bereitgestellt werden, auf denen ein 64-Bit-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db257-148">**Important** Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="db257-149">Neue 32-Bit-Pakete, die mit dem App-v 4.6-Sequenzer erstellt wurden, werden auf Computern, auf denen der APP-v 4,5-Client ausgeführt wird, nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db257-149">New 32-bit packages created by using the App-V4.6 Sequencer will not run on computers running the App-V 4.5 Client.</span></span>

 

<span data-ttu-id="db257-150">Wenn Sie neue 64-Bit-Pakete auf dem App-v 4.6-Client ausführen möchten, müssen Sie die Anwendung auf einem Computer mit dem App-v 4.6-Sequenzer abgleichen, auf dem ein 64-Bit-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db257-150">To run new 64-bit packages on the App-V4.6 Client, you must sequence the application on a computer running the App-V4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="db257-151">Nachdem Sie die Anwendung sequenziert haben, wählen Sie in der Sequencer-Konsole die Registerkarte **Bereitstellung** aus, und geben Sie dann die gewünschte Betriebssystem-und Chiparchitektur an.</span><span class="sxs-lookup"><span data-stu-id="db257-151">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="db257-152">In der folgenden Tabelle wird aufgeführt, welche Clientversionen Pakete ausführen, die mit den verschiedenen Versionen des Sequencers erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="db257-152">The following table lists which client versions will run packages created by using the various versions of the Sequencer.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="db257-153">Sequenziert mithilfe des App-V 4,2-Sequenzers</span><span class="sxs-lookup"><span data-stu-id="db257-153">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="db257-154">Sequenziert mithilfe des App-V 4,5-Sequenzers</span><span class="sxs-lookup"><span data-stu-id="db257-154">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="db257-155">Sequenziert mithilfe des 32-Bit-App-V 4,6-Sequenzers</span><span class="sxs-lookup"><span data-stu-id="db257-155">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="db257-156">Sequenziert mithilfe des 64-Bit-App-V 4,6-Sequenzers</span><span class="sxs-lookup"><span data-stu-id="db257-156">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="db257-157">Sequenziert mithilfe der 32-Bit-App-V 4,6 SP1-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="db257-157">Sequenced by using the 32-bit App-V 4.6 SP1 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="db257-158">Sequenziert mithilfe der 64-Bit-App-V 4,6 SP1-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="db257-158">Sequenced by using the 64-bit App-V 4.6 SP1 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db257-159">4,2-Client</span><span class="sxs-lookup"><span data-stu-id="db257-159">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-160">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-160">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-161">Nein</span><span class="sxs-lookup"><span data-stu-id="db257-161">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-162">Nein</span><span class="sxs-lookup"><span data-stu-id="db257-162">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-163">Nein</span><span class="sxs-lookup"><span data-stu-id="db257-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-164">Nein</span><span class="sxs-lookup"><span data-stu-id="db257-164">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-165">Nein</span><span class="sxs-lookup"><span data-stu-id="db257-165">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db257-166">4,5-Client ¹</span><span class="sxs-lookup"><span data-stu-id="db257-166">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-167">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-167">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-168">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-168">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-169">Nein</span><span class="sxs-lookup"><span data-stu-id="db257-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-170">Nein</span><span class="sxs-lookup"><span data-stu-id="db257-170">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-171">Nein</span><span class="sxs-lookup"><span data-stu-id="db257-171">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-172">Nein</span><span class="sxs-lookup"><span data-stu-id="db257-172">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db257-173">4,6-Client (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="db257-173">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-174">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-174">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-175">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-175">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-176">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-176">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-177">Nein.</span><span class="sxs-lookup"><span data-stu-id="db257-177">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-178">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-179">Nein.</span><span class="sxs-lookup"><span data-stu-id="db257-179">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db257-180">4,6-Client (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="db257-180">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-181">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-182">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-182">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-183">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-184">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-185">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-185">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-186">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db257-187">4,6 SP1-Client</span><span class="sxs-lookup"><span data-stu-id="db257-187">4.6 SP1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-188">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-189">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-190">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-191">Nein.</span><span class="sxs-lookup"><span data-stu-id="db257-191">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-192">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-192">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-193">Nein.</span><span class="sxs-lookup"><span data-stu-id="db257-193">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db257-194">4,6 SP1-Client (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="db257-194">4.6 SP1 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-195">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-196">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-197">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-197">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-198">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-199">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-199">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db257-200">Ja</span><span class="sxs-lookup"><span data-stu-id="db257-200">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="db257-201">¹ gilt für alle Versionen des App-v 4.5-Clients, einschließlich APP-v 4.5, App-v 4.5 CU1 und App-v 4.5 SP1.</span><span class="sxs-lookup"><span data-stu-id="db257-201">¹Applies to all versions of the App-V4.5 Client, including App-V4.5, App-V4.5CU1 and App-V4.5 SP1.</span></span>

## <span data-ttu-id="db257-202">Weitere Überlegungen zur Migration</span><span class="sxs-lookup"><span data-stu-id="db257-202">Additional Migration Considerations</span></span>


<span data-ttu-id="db257-203">Eines der Features des App-v 4.5-Sequenzers ist die Möglichkeit, Windows Installer-Dateien (MSI) als Kontrollpunkte für die Interoperabilität des virtuellen Anwendungspakets mit ESD-Systemen (Electronic Software Distribution) wie Microsoft Endpoint Configuration Manager zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="db257-203">One of the features of the App-V4.5 Sequencer is the ability to create Windows Installer files (.msi) as control points for virtual application package interoperability with electronic software distribution (ESD) systems such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="db257-204">Frühere Windows Installer-Dateien, die mit dem MSI-Tool für Application Virtualization erstellt wurden, die auf einem App-v 4.1-oder 4.2-Client installiert wurden und anschließend auf 4.5 aktualisiert wurden, funktionieren weiterhin, auch wenn Sie nicht auf dem 4.5-Client installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="db257-204">Previous Windows Installer files created with the .msi tool for Application Virtualization that were installed on a App-V4.1 or4.2 Client that is subsequently upgraded to4.5 continue to work, although they cannot be installed on the4.5 Client.</span></span> <span data-ttu-id="db257-205">Sie können jedoch nur dann entfernt oder aktualisiert werden, wenn Sie im 4.5-Sequenzer aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="db257-205">However, they cannot be removed or upgraded unless they are upgraded in the4.5 Sequencer.</span></span> <span data-ttu-id="db257-206">Das ursprüngliche virtuelle Anwendungspaket vor 4,5 muss im 4.5-Sequenzer geöffnet und dann als Windows Installer-Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="db257-206">The original pre-4.5 virtual application package would need to be opened in the4.5 Sequencer and then saved as a Windows Installer File.</span></span>

<span data-ttu-id="db257-207">**Hinweis**  Wenn der APP-v 4.2-Client bereits auf 4.5 aktualisiert wurde, ist es möglich, das Skript als Problemumgehung zu verwenden, um die 4.2-Pakete auf 4.5-Clients beizubehalten und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="db257-207">**Note** If the App-V4.2 Client has already been upgraded to4.5, it is possible to use script as a workaround to preserve the4.2 packages on4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="db257-208">Dieses Skript muss zwei Dateien, msvcp71.dll und msvcr71.dll, in den App-V-Installationsordner kopieren und die folgenden Registrierungsschlüsselwerte unter dem Registrierungsschlüssel \ [HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\] einrichten:</span><span class="sxs-lookup"><span data-stu-id="db257-208">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key \[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

<span data-ttu-id="db257-209">"Clientversion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="db257-209">"ClientVersion"="4.2.1.20"</span></span>

<span data-ttu-id="db257-210">"GlobalDataDirectory" = "C:\\\\Documents und Settings\\\\All Users\\\\Documents\\\\" (ein Global beschreibbarer Speicherort)</span><span class="sxs-lookup"><span data-stu-id="db257-210">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>

 

<span data-ttu-id="db257-211">Windows Installer-Dateien, die vom APP-v 4,5-Sequenzer generiert werden, zeigen die Fehlermeldung "dieses Paket erfordert Microsoft Application Virtualization Client 4,5 oder höher" an, wenn Sie versuchen, Sie auf einem App-v 4,6-Client auszuführen.</span><span class="sxs-lookup"><span data-stu-id="db257-211">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when you try to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="db257-212">Öffnen Sie das alte Paket entweder mit dem App-v 4,5 SP1-Sequenzer oder dem App-v 4,6-Sequenzer, und generieren Sie eine neue MSI-Version für das Paket.</span><span class="sxs-lookup"><span data-stu-id="db257-212">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi for the package.</span></span>

<span data-ttu-id="db257-213">Alle 4,2 Berichte, die erstellt und gespeichert wurden, werden überschrieben, wenn der Server auf 4.5 aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="db257-213">Any4.2 reports that were created and saved will be overwritten when the server is upgraded to4.5.</span></span> <span data-ttu-id="db257-214">Wenn Sie diese Berichte behalten möchten, müssen Sie eine Sicherungskopie der "SftMMC. MSC-Datei speichern, die sich im Ordner SoftGrid-Verwaltungskonsole auf dem Server befindet, und diese Kopie verwenden, um das neue" SftMMC. msc zu ersetzen, das während des Upgrades installiert ist.</span><span class="sxs-lookup"><span data-stu-id="db257-214">If you need to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

<span data-ttu-id="db257-215">Weitere Informationen zum Upgrade von vorherigen Versionen finden Sie unter [Upgrade auf Microsoft Application Virtualization 4,5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="db257-215">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <span data-ttu-id="db257-216">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="db257-216">Related topics</span></span>


[<span data-ttu-id="db257-217">Planen der Bereitstellung von Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="db257-217">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





