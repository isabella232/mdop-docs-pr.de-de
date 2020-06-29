---
title: So stellen Sie den App-V 5.1-Server bereit
description: So stellen Sie den App-V 5.1-Server bereit
author: dansimp
ms.assetid: 4729beda-b98f-481b-ae74-ad71c59b1d69
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a367be7db4cea1835124657dbdfa3375474228e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805498"
---
# <span data-ttu-id="dd804-103">So stellen Sie den App-V 5.1-Server bereit</span><span class="sxs-lookup"><span data-stu-id="dd804-103">How to Deploy the App-V 5.1 Server</span></span>


<span data-ttu-id="dd804-104">Gehen Sie wie folgt vor, um den Microsoft Application Virtualization (App-V) 5,1-Server zu installieren.</span><span class="sxs-lookup"><span data-stu-id="dd804-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 server.</span></span> <span data-ttu-id="dd804-105">Informationen zum Bereitstellen des App-v 5,1-Servers finden Sie unter [Informationen zu app-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).</span><span class="sxs-lookup"><span data-stu-id="dd804-105">For information about deploying the App-V 5.1 Server, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51).</span></span>

**<span data-ttu-id="dd804-106">Bevor Sie beginnen:</span><span class="sxs-lookup"><span data-stu-id="dd804-106">Before you start:</span></span>**

-   <span data-ttu-id="dd804-107">Stellen Sie sicher, dass Sie die erforderliche Software installiert haben.</span><span class="sxs-lookup"><span data-stu-id="dd804-107">Ensure that you’ve installed prerequisite software.</span></span> <span data-ttu-id="dd804-108">Weitere Informationen finden Sie unter [App-V 5,1-Voraussetzungen](app-v-51-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="dd804-108">See [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

-   <span data-ttu-id="dd804-109">Lesen Sie den Abschnitt Server der [Sicherheitsüberlegungen zu App-V 5,1](app-v-51-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="dd804-109">Review the server section of [App-V 5.1 Security Considerations](app-v-51-security-considerations.md).</span></span>

-   <span data-ttu-id="dd804-110">Geben Sie einen Port an, in dem die einzelnen Komponenten gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="dd804-110">Specify a port where each component will be hosted.</span></span>

-   <span data-ttu-id="dd804-111">Fügen Sie Firewallregeln hinzu, damit eingehende Anforderungen auf die angegebenen Ports zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="dd804-111">Add firewall rules to allow incoming requests to access the specified ports.</span></span>

-   <span data-ttu-id="dd804-112">Wenn Sie anstelle des Windows Installers SQL-Skripts verwenden, um die Verwaltungsdatenbank oder die Berichtsdatenbank einzurichten, müssen Sie die SQL-Skripts ausführen, bevor Sie den Verwaltungsserver oder den Berichtsserver installieren.</span><span class="sxs-lookup"><span data-stu-id="dd804-112">If you use SQL scripts, instead of the Windows Installer, to set up the Management database or Reporting database, you must run the SQL scripts before installing the Management Server or Reporting Server.</span></span> <span data-ttu-id="dd804-113">Weitere Informationen finden Sie unter [Bereitstellen der App-V-Datenbanken mithilfe von SQL-Skripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span><span class="sxs-lookup"><span data-stu-id="dd804-113">See [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span></span>

**<span data-ttu-id="dd804-114">So installieren Sie den App-V 5,1-Server</span><span class="sxs-lookup"><span data-stu-id="dd804-114">To install the App-V 5.1 server</span></span>**

1. <span data-ttu-id="dd804-115">Kopieren Sie die App-V 5,1 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="dd804-115">Copy the App-V 5.1 server installation files to the computer on which you want to install it.</span></span>

2. <span data-ttu-id="dd804-116">Starten Sie die App-V 5,1 Server-Installation, indem Sie mit der rechten Maustaste klicken und **appv\_server\_setup.exe** als Administrator ausführen, und klicken Sie dann auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="dd804-116">Start the App-V 5.1 server installation by right-clicking and running **appv\_server\_setup.exe** as an administrator, and then click **Install**.</span></span>

3. <span data-ttu-id="dd804-117">Überprüfen und akzeptieren Sie die Lizenzbestimmungen, und wählen Sie aus, ob Microsoft Updates aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd804-117">Review and accept the license terms, and choose whether to enable Microsoft updates.</span></span>

4. <span data-ttu-id="dd804-118">Wählen Sie auf der Seite **Featureauswahl** alle der folgenden Komponenten aus.</span><span class="sxs-lookup"><span data-stu-id="dd804-118">On the **Feature Selection** page, select all of the following components.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="dd804-119">Komponente</span><span class="sxs-lookup"><span data-stu-id="dd804-119">Component</span></span></th>
   <th align="left"><span data-ttu-id="dd804-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd804-120">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="dd804-121">Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="dd804-121">Management server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dd804-122">Bietet allgemeine Verwaltungsfunktionen für die App-V-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="dd804-122">Provides overall management functionality for the App-V infrastructure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="dd804-123">Verwaltungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="dd804-123">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dd804-124">Vereinfacht die Bereitstellung von Datenbanken für die App-V-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="dd804-124">Facilitates database predeployments for App-V management.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="dd804-125">Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="dd804-125">Publishing server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dd804-126">Bietet Hosting-und Streamingfunktionen für virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="dd804-126">Provides hosting and streaming functionality for virtual applications.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="dd804-127">Berichtsserver</span><span class="sxs-lookup"><span data-stu-id="dd804-127">Reporting server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dd804-128">Bietet App-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="dd804-128">Provides App-V 5.1 reporting services.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="dd804-129">Berichtsdatenbank</span><span class="sxs-lookup"><span data-stu-id="dd804-129">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dd804-130">Vereinfacht die Bereitstellung von Datenbanken für die App-V-Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="dd804-130">Facilitates database predeployments for App-V reporting.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

5. <span data-ttu-id="dd804-131">Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, an dem die ausgewählten Komponenten installiert werden sollen, oder ändern Sie den Speicherort, indem Sie einen neuen Pfad in der **Installationsstandort** Zeile eingeben.</span><span class="sxs-lookup"><span data-stu-id="dd804-131">On the **Installation Location** page, accept the default location where the selected components will be installed, or change the location by typing a new path on the **Installation Location** line.</span></span>

6. <span data-ttu-id="dd804-132">Konfigurieren Sie auf der Seite erste **neue Verwaltungsdatenbank erstellen** die **Microsoft SQL Server-Instanz** und die **Verwaltungs Server-Datenbank** , indem Sie die entsprechende Option unten auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd804-132">On the initial **Create New Management Database** page, configure the **Microsoft SQL Server instance** and **Management Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="dd804-133">Methode</span><span class="sxs-lookup"><span data-stu-id="dd804-133">Method</span></span></th>
   <th align="left"><span data-ttu-id="dd804-134">Was Sie tun müssen</span><span class="sxs-lookup"><span data-stu-id="dd804-134">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="dd804-135">Sie verwenden eine benutzerdefinierte Microsoft SQL Server-Instanz.</span><span class="sxs-lookup"><span data-stu-id="dd804-135">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dd804-136">Wählen Sie <strong> die benutzerdefinierte Instanz verwenden aus </strong> , und geben Sie den Namen der Instanz ein.</span><span class="sxs-lookup"><span data-stu-id="dd804-136">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="dd804-137">Verwenden Sie das Format <strong> instanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="dd804-137">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="dd804-138">Der angenommene Installationsspeicherort ist der lokale Computer.</span><span class="sxs-lookup"><span data-stu-id="dd804-138">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="dd804-139">Nicht unterstützt: ein Servername unter Verwendung <strong> der </strong> &lt; starken &gt; Instanz von Format Servername </strong> .</span><span class="sxs-lookup"><span data-stu-id="dd804-139">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="dd804-140">Sie verwenden einen benutzerdefinierten Datenbanknamen.</span><span class="sxs-lookup"><span data-stu-id="dd804-140">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dd804-141">Wählen Sie <strong> benutzerdefinierte Konfiguration aus </strong> , und geben Sie den Datenbanknamen ein.</span><span class="sxs-lookup"><span data-stu-id="dd804-141">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="dd804-142">Der Datenbankname muss eindeutig sein, oder die Installation schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="dd804-142">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="dd804-143">Übernehmen Sie auf der Seite **Konfigurieren** den Standardwert **diesen lokalen Computer verwenden**.</span><span class="sxs-lookup"><span data-stu-id="dd804-143">On the **Configure** page, accept the default value **Use this local computer**.</span></span>

   **<span data-ttu-id="dd804-144">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="dd804-144">Note</span></span>**  
   <span data-ttu-id="dd804-145">Wenn Sie den Verwaltungsserver und die Verwaltungsdatenbank nebeneinander installieren, stehen einige Optionen auf dieser Seite nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dd804-145">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="dd804-146">In diesem Fall sind die entsprechenden Optionen standardmäßig aktiviert und können nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dd804-146">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

8. <span data-ttu-id="dd804-147">Konfigurieren Sie auf der ersten Seite zum **Erstellen einer neuen Berichtsdatenbank** die **Microsoft SQL Server-Instanz** und die **Berichtsserver-Datenbank** , indem Sie die entsprechende Option unten auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd804-147">On the initial **Create New Reporting Database** page, configure the **Microsoft SQL Server instance** and **Reporting Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="dd804-148">Methode</span><span class="sxs-lookup"><span data-stu-id="dd804-148">Method</span></span></th>
   <th align="left"><span data-ttu-id="dd804-149">Was Sie tun müssen</span><span class="sxs-lookup"><span data-stu-id="dd804-149">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="dd804-150">Sie verwenden eine benutzerdefinierte Microsoft SQL Server-Instanz.</span><span class="sxs-lookup"><span data-stu-id="dd804-150">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dd804-151">Wählen Sie <strong> die benutzerdefinierte Instanz verwenden aus </strong> , und geben Sie den Namen der Instanz ein.</span><span class="sxs-lookup"><span data-stu-id="dd804-151">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="dd804-152">Verwenden Sie das Format <strong> instanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="dd804-152">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="dd804-153">Der angenommene Installationsspeicherort ist der lokale Computer.</span><span class="sxs-lookup"><span data-stu-id="dd804-153">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="dd804-154">Nicht unterstützt: ein Servername unter Verwendung <strong> der </strong> &lt; starken &gt; Instanz von Format Servername </strong> .</span><span class="sxs-lookup"><span data-stu-id="dd804-154">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="dd804-155">Sie verwenden einen benutzerdefinierten Datenbanknamen.</span><span class="sxs-lookup"><span data-stu-id="dd804-155">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dd804-156">Wählen Sie <strong> benutzerdefinierte Konfiguration aus </strong> , und geben Sie den Datenbanknamen ein.</span><span class="sxs-lookup"><span data-stu-id="dd804-156">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="dd804-157">Der Datenbankname muss eindeutig sein, oder die Installation schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="dd804-157">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

9. <span data-ttu-id="dd804-158">Übernehmen Sie auf der Seite **configure** den Standardwert: **verwenden Sie diesen lokalen Computer**.</span><span class="sxs-lookup"><span data-stu-id="dd804-158">On the **Configure** page, accept the default value: **Use this local computer**.</span></span>

   **<span data-ttu-id="dd804-159">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="dd804-159">Note</span></span>**  
   <span data-ttu-id="dd804-160">Wenn Sie den Verwaltungsserver und die Verwaltungsdatenbank nebeneinander installieren, stehen einige Optionen auf dieser Seite nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dd804-160">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="dd804-161">In diesem Fall sind die entsprechenden Optionen standardmäßig aktiviert und können nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dd804-161">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

10. <span data-ttu-id="dd804-162">Geben Sie auf der Seite **configure** (Management Server Configuration) Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="dd804-162">On the **Configure** (Management Server Configuration) page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="dd804-163">Zu konfigurierendes Element</span><span class="sxs-lookup"><span data-stu-id="dd804-163">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="dd804-164">Beschreibung und Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd804-164">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="dd804-165">Geben Sie die Anzeigengruppe mit den entsprechenden Berechtigungen zum Verwalten der App-V-Umgebung ein.</span><span class="sxs-lookup"><span data-stu-id="dd804-165">Type the AD group with sufficient permissions to manage the App-V environment.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="dd804-166">Beispiel: MYDOMAIN\myuser</span><span class="sxs-lookup"><span data-stu-id="dd804-166">Example: MyDomain\MyUser</span></span></p>
    <p><span data-ttu-id="dd804-167">Nach der Installation können Sie weitere Benutzer oder Gruppen mithilfe der Verwaltungskonsole hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dd804-167">After installation, you can add additional users or groups by using the Management console.</span></span> <span data-ttu-id="dd804-168">Globale Sicherheitsgruppen und Active Directory-Domänendienste (AD DS)-Verteilergruppen werden jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd804-168">However, global security groups and Active Directory Domain Services (AD DS) distribution groups are not supported.</span></span> <span data-ttu-id="dd804-169"><strong> </strong> <strong> Zum Ausführen dieser Aktion müssen Sie eine lokale Domäne oder universelle </strong> Gruppen verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd804-169">You must use <strong>Domain local</strong> or <strong>Universal</strong> groups are required to perform this action.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="dd804-170">Website Name </strong> : Geben Sie den benutzerdefinierten Namen an, der zum Ausführen des Veröffentlichungs Diensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd804-170">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="dd804-171">Wenn Sie keinen benutzerdefinierten Namen haben, nehmen Sie keine Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="dd804-171">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="dd804-172">Portbindung </strong> : Geben Sie eine eindeutige Portnummer an, die von App-V verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd804-172">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="dd804-173">Beispiel: <strong> 12345</span><span class="sxs-lookup"><span data-stu-id="dd804-173">Example: <strong>12345</span></span></strong></p>
    <p><span data-ttu-id="dd804-174">Stellen Sie sicher, dass der angegebene Port nicht von einer anderen Website verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd804-174">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

11. <span data-ttu-id="dd804-175">Geben Sie auf der Seite **Konfigurieren** der **Veröffentlichungs Server Konfiguration** Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="dd804-175">On the **Configure** **Publishing Server Configuration** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="dd804-176">Zu konfigurierendes Element</span><span class="sxs-lookup"><span data-stu-id="dd804-176">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="dd804-177">Beschreibung und Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd804-177">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="dd804-178">Geben Sie die URL für den Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="dd804-178">Specify the URL for the management service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="dd804-179">Beispiel<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span><span class="sxs-lookup"><span data-stu-id="dd804-179">Example: <a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span></span></a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="dd804-180">Website Name </strong> : Geben Sie den benutzerdefinierten Namen an, der zum Ausführen des Veröffentlichungs Diensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd804-180">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="dd804-181">Wenn Sie keinen benutzerdefinierten Namen haben, nehmen Sie keine Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="dd804-181">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="dd804-182">Portbindung </strong> : Geben Sie eine eindeutige Portnummer an, die von App-V verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd804-182">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="dd804-183">Beispiel: 54321</span><span class="sxs-lookup"><span data-stu-id="dd804-183">Example: 54321</span></span></p>
    <p><span data-ttu-id="dd804-184">Stellen Sie sicher, dass der angegebene Port nicht von einer anderen Website verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd804-184">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

12. <span data-ttu-id="dd804-185">Geben Sie auf der Seite **Reporting Server** Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="dd804-185">On the **Reporting Server** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="dd804-186">Zu konfigurierendes Element</span><span class="sxs-lookup"><span data-stu-id="dd804-186">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="dd804-187">Beschreibung und Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd804-187">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="dd804-188">Website Name </strong> : Geben Sie den benutzerdefinierten Namen an, der zum Ausführen des Berichts Diensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd804-188">Website name</strong>: Specify the custom name that will be used to run the Reporting Service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="dd804-189">Wenn Sie keinen benutzerdefinierten Namen haben, nehmen Sie keine Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="dd804-189">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="dd804-190">Portbindung </strong> : Geben Sie eine eindeutige Portnummer an, die von App-V verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd804-190">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="dd804-191">Beispiel: 55555</span><span class="sxs-lookup"><span data-stu-id="dd804-191">Example: 55555</span></span></p>
    <p><span data-ttu-id="dd804-192">Stellen Sie sicher, dass der angegebene Port nicht von einer anderen Website verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd804-192">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

13. <span data-ttu-id="dd804-193">Um die Installation zu starten, klicken Sie auf der Seite **Ready** auf **Installieren** , und klicken Sie dann auf der Seite **Fertig** auf **Schließen** .</span><span class="sxs-lookup"><span data-stu-id="dd804-193">To start the installation, click **Install** on the **Ready** page, and then click **Close** on the **Finished** page.</span></span>

14. <span data-ttu-id="dd804-194">Um zu überprüfen, ob das Setup erfolgreich abgeschlossen wurde, öffnen Sie einen Webbrowser, und geben Sie die folgende URL ein:</span><span class="sxs-lookup"><span data-stu-id="dd804-194">To verify that the setup completed successfully, open a web browser, and type the following URL:</span></span>

    <span data-ttu-id="dd804-195">**http:// &lt; Verwaltungsservercomputer Name &gt; : &lt; Verwaltungsdienst-Portnummer &gt; /Console.html**.</span><span class="sxs-lookup"><span data-stu-id="dd804-195">**http://&lt;Management server machine name&gt;:&lt;Management service port number&gt;/Console.html**.</span></span>

    <span data-ttu-id="dd804-196">Beispiel: **http://localhost:12345/console.html** .</span><span class="sxs-lookup"><span data-stu-id="dd804-196">Example: **http://localhost:12345/console.html**.</span></span> <span data-ttu-id="dd804-197">Wenn die Installation erfolgreich war, wird die App-V-Verwaltungskonsole ohne Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd804-197">If the installation succeeded, the App-V Management console is displayed with no errors.</span></span>

    <span data-ttu-id="dd804-198">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="dd804-198">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="dd804-199">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="dd804-199">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="dd804-200">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="dd804-200">Got an App-V issue?</span></span>** <span data-ttu-id="dd804-201">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="dd804-201">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="dd804-202">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dd804-202">Related topics</span></span>


[<span data-ttu-id="dd804-203">Bereitstellen von App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="dd804-203">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="dd804-204">So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste</span><span class="sxs-lookup"><span data-stu-id="dd804-204">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[<span data-ttu-id="dd804-205">So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer</span><span class="sxs-lookup"><span data-stu-id="dd804-205">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[<span data-ttu-id="dd804-206">So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit</span><span class="sxs-lookup"><span data-stu-id="dd804-206">How to Deploy the App-V 5.1 Server Using a Script</span></span>](how-to-deploy-the-app-v-51-server-using-a-script.md)

 

 





