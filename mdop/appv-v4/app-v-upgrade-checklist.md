---
title: Upgrade-Prüfliste für App-V
description: Upgrade-Prüfliste für App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808027"
---
# <span data-ttu-id="198c4-103">Upgrade-Prüfliste für App-V</span><span class="sxs-lookup"><span data-stu-id="198c4-103">App-V Upgrade Checklist</span></span>


<span data-ttu-id="198c4-104">Bevor Sie versuchen, auf Microsoft Application Virtualization (app-v) 4,5 oder höhere Versionen zu aktualisieren, muss jede frühere Version als App-v 4,1 auf App-v 4,1 aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="198c4-104">Before trying to upgrade to Microsoft Application Virtualization (App-V) 4.5 or later versions, any version earlier than App-V 4.1 must be upgraded to App-V 4.1.</span></span> <span data-ttu-id="198c4-105">Sie sollten zunächst planen, Clients zu aktualisieren und dann die Server Komponenten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="198c4-105">You should plan to upgrade clients first, and then upgrade the server components.</span></span> <span data-ttu-id="198c4-106">App-v-Clients, die auf App-v 4,5 aktualisiert wurden, arbeiten weiterhin mit App-v-Servern, die noch nicht aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="198c4-106">App-V clients that have been upgraded to App-V 4.5 continue to work with App-V servers that have not yet been upgraded.</span></span> <span data-ttu-id="198c4-107">Frühere Versionen des Clients werden auf Servern, die auf App-V 4,5 aktualisiert wurden, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="198c4-107">Earlier versions of the client are not supported on servers that have been upgraded to App-V 4.5.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="198c4-108">Schritt</span><span class="sxs-lookup"><span data-stu-id="198c4-108">Step</span></span></th>
<th align="left"><span data-ttu-id="198c4-109">Verweis</span><span class="sxs-lookup"><span data-stu-id="198c4-109">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-110">Aktualisieren Sie die App-V-Clients.</span><span class="sxs-lookup"><span data-stu-id="198c4-110">Upgrade the App-V clients.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)"><span data-ttu-id="198c4-111">So aktualisieren Sie Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="198c4-111">How to Upgrade the Application Virtualization Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="198c4-112">Aktualisieren Sie die App-V-Server und-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="198c4-112">Upgrade the App-V servers and database.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="198c4-113">Wichtig</span><span class="sxs-lookup"><span data-stu-id="198c4-113">Important</span></span></strong><br/><p><span data-ttu-id="198c4-114">Wenn Sie über mehr als einen Serverfreigabe Zugriff auf die App-V-Datenbank verfügen, müssen alle diese Server offline geschaltet werden, während die Datenbank aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="198c4-114">If you have more than one server sharing access to the App-V database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="198c4-115">Sie sollten ihre normalen Geschäftsmethoden für die Datenbankaktualisierung befolgen, aber wir empfehlen, dass Sie das Datenbankupgrade mithilfe einer Sicherungskopie der Datenbank zuerst auf einem Testserver testen.</span><span class="sxs-lookup"><span data-stu-id="198c4-115">You should follow your regular business practices for the database upgrade, but we recommend that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="198c4-116">Wählen Sie dann einen der Server für das erste Upgrade aus, um das Datenbankschema zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="198c4-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="198c4-117">Nachdem die Produktionsdatenbank erfolgreich aktualisiert wurde, können Sie die App-V-Software auf den anderen Servern aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="198c4-117">After the production database has been successfully upgraded, you can upgrade the App-V software on the other servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="198c4-118">So aktualisieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="198c4-118">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-119">Aktualisieren des App-V-Verwaltungs-Webdiensts</span><span class="sxs-lookup"><span data-stu-id="198c4-119">Upgrade the App-V Management Web Service.</span></span></p>
<p><span data-ttu-id="198c4-120">Dieser Schritt gilt nur, wenn sich der Verwaltungs-Web-Service auf einem separaten Server befindet, was erfordert, dass Sie das Serverinstallationsprogramm auf diesem separaten Server ausführen, um den Verwaltungs-Webservice zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="198c4-120">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Management Web service.</span></span> <span data-ttu-id="198c4-121">Andernfalls führt der vorherige Server Upgrade-Schritt automatisch zu einem Upgrade des Verwaltungs-Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="198c4-121">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="198c4-122">So aktualisieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="198c4-122">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="198c4-123">Aktualisieren Sie die App-V-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="198c4-123">Upgrade the App-V Management Console.</span></span></p>
<p><span data-ttu-id="198c4-124">Dieser Schritt gilt nur, wenn sich die Verwaltungskonsole auf einem separaten Computer befindet, was erfordert, dass Sie das Serverinstallationsprogramm auf diesem separaten Computer ausführen, um die Konsole zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="198c4-124">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="198c4-125">Andernfalls wird der vorherige Server Aktualisierungsschritt die Verwaltungskonsole aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="198c4-125">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="198c4-126">So aktualisieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="198c4-126">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-127">Aktualisieren Sie den App-V-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="198c4-127">Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)"><span data-ttu-id="198c4-128">So aktualisieren Sie Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="198c4-128">How to Upgrade the Application Virtualization Sequencer</span></span></a></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="198c4-129">Weitere Überlegungen zu Upgrades</span><span class="sxs-lookup"><span data-stu-id="198c4-129">Additional Upgrade Considerations</span></span>


-   <span data-ttu-id="198c4-130">Alle virtuellen Anwendungspakete, die in Version 4,2 sequenziert sind, müssen für die Verwendung mit Version 4,5 nicht erneut sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="198c4-130">Any virtual application packages sequenced in version 4.2 will not have to be sequenced again for use with version 4.5.</span></span> <span data-ttu-id="198c4-131">Sie sollten jedoch erwägen, die virtuellen Pakete auf das Microsoft Application Virtualization 4,5-Format zu aktualisieren, wenn Sie standardmäßige Zugriffssteuerungslisten verwenden oder eine Windows Installer-Datei generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="198c4-131">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization 4.5 format if you want to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="198c4-132">Dies ist ein einfacher Vorgang und erfordert nur, dass das vorhandene virtuelle Anwendungspaket mit dem App-V 4,5-Sequenzer geöffnet und gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="198c4-132">This is a simple process and requires only that the existing virtual application package be opened and saved with the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="198c4-133">Dies kann mithilfe der Befehlszeilenschnittstelle für die APP-VSequencer automatisiert werden.</span><span class="sxs-lookup"><span data-stu-id="198c4-133">This can be automated by using the App-VSequencer command-line interface.</span></span> <span data-ttu-id="198c4-134">Weitere Informationen finden Sie unter [erstellen oder Aktualisieren virtueller Anwendungen mit dem App-V-Sequenzer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md) .</span><span class="sxs-lookup"><span data-stu-id="198c4-134">For more information, see [How to Create or Upgrade Virtual Applications Using the App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span></span>

-   <span data-ttu-id="198c4-135">Eines der Features des 4,5-Sequenzers ist die Möglichkeit zum Erstellen von Windows Installer-Dateien (MSI) als Kontrollpunkte für die Interoperabilität des virtuellen Anwendungspakets mit ESD-Systemen (Electronic Software Distribution) wie Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="198c4-135">One of the features of the 4.5 Sequencer is the ability to create Windows Installer (.msi) files as control points for virtual application package interoperability with electronic software distribution (ESD) systems, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="198c4-136">Frühere Windows Installer-Dateien, die mit dem MSI-Tool für Application Virtualization erstellt wurden, die auf einem App-v 4,1-oder 4,2-Client installiert wurden und anschließend auf App-v 4,5 aktualisiert wurden, funktionieren weiterhin, auch wenn Sie nicht auf dem App-v 4,5-Client installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="198c4-136">Previous Windows Installer files created with the MSI tool for Application Virtualization that were installed on a App-V 4.1 or 4.2 client that is subsequently upgraded to App-V 4.5 will continue to work, although they cannot be installed on the App-V 4.5 client.</span></span> <span data-ttu-id="198c4-137">Sie können jedoch nur dann entfernt oder aktualisiert werden, wenn Sie im App-V 4,5-Sequenzer aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="198c4-137">However, they cannot be removed or upgraded unless they are upgraded in the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="198c4-138">Das ursprüngliche App-v-Paket, das älter als 4,5 ist, muss im App-v 4,5-Sequenzer geöffnet und dann als Windows Installer-Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="198c4-138">The original App-V package earlier than 4.5 has to be opened in the App-V 4.5 Sequencer and then saved as a Windows Installer File.</span></span>

    **<span data-ttu-id="198c4-139">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="198c4-139">Note</span></span>**  
    <span data-ttu-id="198c4-140">Wenn der APP-v 4,2-Client bereits auf App-v 4,5 aktualisiert wurde, ist es möglich, eine Problemumgehung zu erstellen, um die Version 4,2-Pakete auf Version 4,5-Clients beizubehalten und deren Verwaltung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="198c4-140">If the App-V 4.2 Client has already been upgraded to App-V 4.5, it is possible to script a workaround to preserve the version 4.2 packages on version 4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="198c4-141">Dieses Skript muss zwei Dateien, msvcp71.dll und msvcr71.dll, in den App-V-Installationsordner kopieren und die folgenden Registrierungsschlüsselwerte unter dem Registrierungsschlüssel einrichten: \ [HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\]:</span><span class="sxs-lookup"><span data-stu-id="198c4-141">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key:\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

    <span data-ttu-id="198c4-142">"Clientversion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="198c4-142">"ClientVersion"="4.2.1.20"</span></span>

    <span data-ttu-id="198c4-143">"GlobalDataDirectory" = "C:\\\\Documents und Settings\\\\All Users\\\\Documents\\\\" (ein Global beschreibbarer Speicherort)</span><span class="sxs-lookup"><span data-stu-id="198c4-143">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>



-   <span data-ttu-id="198c4-144">Windows Installer-Dateien, die vom APP-v 4,5-Sequenzer generiert werden, zeigen die Fehlermeldung "dieses Paket erfordert Microsoft Application Virtualization Client 4,5 oder höher" an, wenn Sie versuchen, Sie auf einem App-v 4,6-Client auszuführen.</span><span class="sxs-lookup"><span data-stu-id="198c4-144">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when trying to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="198c4-145">Öffnen Sie das alte Paket entweder mit dem App-v 4,5 SP1-Sequenzer oder dem App-v 4,6-Sequenzer, und generieren Sie eine neue MSI-Datei für das Paket.</span><span class="sxs-lookup"><span data-stu-id="198c4-145">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi file for the package.</span></span>

-   <span data-ttu-id="198c4-146">Alle Berichte der Version 4,2, die erstellt und gespeichert wurden, werden überschrieben, wenn der Server auf Version 4,5 aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="198c4-146">Any version 4.2 reports that were created and saved will be overwritten when the server is upgraded to version 4.5.</span></span> <span data-ttu-id="198c4-147">Wenn Sie diese Berichte behalten müssen, müssen Sie eine Sicherungskopie der "SftMMC. MSC-Datei speichern, die sich im Ordner SoftGrid-Verwaltungskonsole auf dem Server befindet, und diese Kopie verwenden, um das neue" SftMMC. msc zu ersetzen, das während des Upgrades installiert ist.</span><span class="sxs-lookup"><span data-stu-id="198c4-147">If you have to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

-   <span data-ttu-id="198c4-148">Weitere Informationen zum Upgrade von vorherigen Versionen finden Sie unter [Upgrade auf Microsoft Application Virtualization 4,5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="198c4-148">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="198c4-149">Unterstützung für App-V 4,6-Client Pakete</span><span class="sxs-lookup"><span data-stu-id="198c4-149">App-V 4.6 Client Package Support</span></span>


<span data-ttu-id="198c4-150">Sie können Pakete bereitstellen, die in früheren Versionen von App-v für App-v 4,6-Clients erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="198c4-150">You can deploy packages created in previous versions of App-V to App-V 4.6 clients.</span></span> <span data-ttu-id="198c4-151">Sie müssen jedoch die zugehörige OSD-Datei so ändern, dass Sie die entsprechenden Informationen zum Betriebssystem und zur Chiparchitektur enthält.</span><span class="sxs-lookup"><span data-stu-id="198c4-151">However, you must modify the associated .osd file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="198c4-152">Die folgenden Werte können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="198c4-152">The following values can be used:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="198c4-153">Betriebssystem Wert</span><span class="sxs-lookup"><span data-stu-id="198c4-153">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-154">&lt;BS-Wert = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-154">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="198c4-155">&lt;BS-Wert = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-155">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-156">&lt;BS-Wert = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-156">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="198c4-157">&lt;BS-Wert = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-157">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-158">&lt;BS-Wert = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-158">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="198c4-159">&lt;BS-Wert = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-159">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-160">&lt;BS-Wert = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-160">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="198c4-161">&lt;BS-Wert = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-161">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-162">&lt;BS-Wert = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-162">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="198c4-163">&lt;BS-Wert = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-163">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-164">&lt;BS-Wert = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="198c4-164">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="198c4-165">Wenn Sie ein neu erstelltes 32-Bit-Paket ausführen möchten, müssen Sie die Anwendung auf einem Computer abgleichen, auf dem ein 32-Bit-Betriebssystem ausgeführt wird, wobei der App-V 4,6-Sequencer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="198c4-165">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V 4.6 Sequencer installed.</span></span> <span data-ttu-id="198c4-166">Nachdem Sie die Anwendung sequenziert haben, klicken Sie in der Sequencer-Konsole auf die Registerkarte **Bereitstellung** , und geben Sie dann die entsprechende Betriebssystem-und Chiparchitektur nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="198c4-166">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

**<span data-ttu-id="198c4-167">Wichtig</span><span class="sxs-lookup"><span data-stu-id="198c4-167">Important</span></span>**  
<span data-ttu-id="198c4-168">Anwendungen, die auf einem Computer mit einem 64-Bit-Betriebssystem sequenziert sind, müssen auf Computern bereitgestellt werden, auf denen ein 64-Bit-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="198c4-168">Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="198c4-169">Neue 32-Bit-Pakete, die mit dem App-v 4,6-Sequenzer erstellt wurden, werden auf Computern, auf denen der APP-v 4,5-Client ausgeführt wird, nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="198c4-169">New 32-bit packages created by using the App-V 4.6 Sequencer do not run on computers running the App-V 4.5 client.</span></span>



<span data-ttu-id="198c4-170">Wenn Sie neue 64-Bit-Pakete auf dem App-v 4,6-Client ausführen möchten, müssen Sie die Anwendung auf einem Computer mit dem App-v 4,6-Sequenzer abgleichen, auf dem ein 64-Bit-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="198c4-170">To run new 64-bit packages on the App-V 4.6 Client, you must sequence the application on a computer running the App-V 4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="198c4-171">Nachdem Sie die Anwendung sequenziert haben, klicken Sie in der Sequencer-Konsole auf die Registerkarte **Bereitstellung** , und geben Sie dann die gewünschte Betriebssystem-und Chiparchitektur an.</span><span class="sxs-lookup"><span data-stu-id="198c4-171">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab, and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="198c4-172">In der folgenden Tabelle wird aufgeführt, welche Clientversionen Pakete ausführen, die mit den verschiedenen Versionen des Sequencers erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="198c4-172">The following table lists which client versions will run packages created by using the various versions of the sequencer.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="198c4-173">Sequenziert mithilfe des App-V 4,2-Sequenzers</span><span class="sxs-lookup"><span data-stu-id="198c4-173">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="198c4-174">Sequenziert mithilfe des App-V 4,5-Sequenzers</span><span class="sxs-lookup"><span data-stu-id="198c4-174">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="198c4-175">Sequenziert mithilfe des 32-Bit-App-V 4,6-Sequenzers</span><span class="sxs-lookup"><span data-stu-id="198c4-175">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="198c4-176">Sequenziert mithilfe des 64-Bit-App-V 4,6-Sequenzers</span><span class="sxs-lookup"><span data-stu-id="198c4-176">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-177">4,2-Client</span><span class="sxs-lookup"><span data-stu-id="198c4-177">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-178">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-179">Nein</span><span class="sxs-lookup"><span data-stu-id="198c4-179">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-180">Nein</span><span class="sxs-lookup"><span data-stu-id="198c4-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-181">Nein</span><span class="sxs-lookup"><span data-stu-id="198c4-181">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="198c4-182">4,5-Client ¹</span><span class="sxs-lookup"><span data-stu-id="198c4-182">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-183">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-184">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-185">Nein</span><span class="sxs-lookup"><span data-stu-id="198c4-185">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-186">Nein</span><span class="sxs-lookup"><span data-stu-id="198c4-186">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="198c4-187">4,6-Client (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="198c4-187">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-188">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-189">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-190">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-191">Nein.</span><span class="sxs-lookup"><span data-stu-id="198c4-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="198c4-192">4,6-Client (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="198c4-192">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-193">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-194">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-194">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-195">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="198c4-196">Ja</span><span class="sxs-lookup"><span data-stu-id="198c4-196">Yes</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="198c4-197">¹ gilt für alle Versionen des App-v 4,5-Clients, einschließlich APP-v 4,5, App-v 4,5 CU1 und App-v 4,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="198c4-197">¹Applies to all versions of the App-V 4.5 client, including App-V 4.5, App-V 4.5 CU1, and App-V 4.5 SP1.</span></span>









