---
title: So konfigurieren Sie den Server, damit ihm für Delegierungszwecke vertraut wird
description: So konfigurieren Sie den Server, damit ihm für Delegierungszwecke vertraut wird
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807231"
---
# <span data-ttu-id="beb68-103">So konfigurieren Sie den Server, damit ihm für Delegierungszwecke vertraut wird</span><span class="sxs-lookup"><span data-stu-id="beb68-103">How to Configure the Server to be Trusted for Delegation</span></span>


<span data-ttu-id="beb68-104">Wenn Sie die Microsoft Application Virtualization (App-V)-Verwaltungs Server Software installieren, können Sie Sie mithilfe einer verteilten Systemarchitektur installieren.</span><span class="sxs-lookup"><span data-stu-id="beb68-104">When you install the Microsoft Application Virtualization (App-V) Management Server software, you can choose to install it by using a distributed system architecture.</span></span> <span data-ttu-id="beb68-105">Wenn Sie die Konsole, den Verwaltungs-Webdienst und die Datenbank auf unterschiedlichen Computern installieren, müssen Sie den IIS-Server (Internet Information Services) so konfigurieren, dass er für die Delegierung als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="beb68-105">If you install the console, the Management Web Service, and the database on different computers, you must configure the Internet Information Services (IIS) server to be trusted for delegation.</span></span> <span data-ttu-id="beb68-106">Dies ist erforderlich, da der Verwaltungs-Webdienst versucht, eine Verbindung mit dem App-v-Datenspeicher mithilfe der Anmeldeinformationen des App-v-Administrators herzustellen, der die Konsole verwendet.</span><span class="sxs-lookup"><span data-stu-id="beb68-106">This is necessary because the Management Web Service will attempt to connect to the App-V data store by using the credentials of the App-V administrator who is using the console.</span></span> <span data-ttu-id="beb68-107">Der Datenbankserver, auf dem der Datenspeicher installiert ist, akzeptiert die Anmeldeinformationen des Administrators nicht vom IIS-Server, es sei denn, der IIS-Server ist für die Delegierung als vertrauenswürdig eingestuft, und der Verwaltungs-Webdienst kann keine Verbindung mit dem App-V-Datenspeicher herstellen.</span><span class="sxs-lookup"><span data-stu-id="beb68-107">The database server on which the data store is installed will not accept the administrator’s credentials from the IIS server unless the IIS server is configured to be trusted for delegation, and so the Management Web Service will not be able to connect to the App-V data store.</span></span>

<span data-ttu-id="beb68-108">**Hinweis**  Wenn Sie die App-V Management Server-Software auf einem einzelnen Server installieren und den Datenspeicher auf einem separaten Server platzieren, gibt es eine Situation, in der Sie den Server weiterhin als vertrauenswürdig für die Delegierung konfigurieren müssen, obwohl sich der Verwaltungs-Webservice und die Verwaltungskonsole auf demselben Server befinden.</span><span class="sxs-lookup"><span data-stu-id="beb68-108">**Note** If you install the App-V Management Server software on a single server and place the data store on a separate server, there is one situation in which you must still configure the server to be trusted for delegation even though the Management Web Service and Management Console are on the same server.</span></span> <span data-ttu-id="beb68-109">Diese Situation tritt auf, wenn Sie eine Verbindung mit dem Verwaltungs-Webdienst in der Konsole herstellen müssen, indem Sie die Option **Alternative Anmeldeinformationen verwenden verwenden** .</span><span class="sxs-lookup"><span data-stu-id="beb68-109">This situation occurs if you need to connect to the Management Web Service in the console by using the **Use Alternate Credentials** option.</span></span>

 

<span data-ttu-id="beb68-110">Die Art der Delegierung, die Sie verwenden können, hängt von der Domänenfunktionsebene ab, die Sie in Ihrer Infrastruktur für Active Directory-Domänendienste (Adds) konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="beb68-110">The type of delegation that you can use depends on the Domain Functional Level that you have configured in your Active Directory Domain Services (ADDS) infrastructure.</span></span> <span data-ttu-id="beb68-111">In der folgenden Tabelle sind die Delegierungs Typen aufgeführt, die für die einzelnen Domänenfunktionsebenen für App-V konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="beb68-111">The following table lists the types of delegation that can be configured for each Domain Functional Level for App-V.</span></span> <span data-ttu-id="beb68-112">Eine detaillierte Anleitung finden Sie in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="beb68-112">Detailed instructions follow the table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="beb68-113">Domänenfunktionsebene</span><span class="sxs-lookup"><span data-stu-id="beb68-113">Domain Functional Level</span></span></th>
<th align="left"><span data-ttu-id="beb68-114">Verfügbare Delegierungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="beb68-114">Delegation Levels Available</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="beb68-115">Windows 2000 Native</span><span class="sxs-lookup"><span data-stu-id="beb68-115">Windows 2000 native</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="beb68-116">Keine Delegierung (Standard)</span><span class="sxs-lookup"><span data-stu-id="beb68-116">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="beb68-117">Nicht eingeschränkte Delegierung</span><span class="sxs-lookup"><span data-stu-id="beb68-117">Unconstrained delegation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="beb68-118">Windows Server 2003, Windows Server 2008 oder Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="beb68-118">Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="beb68-119">Keine Delegierung (Standard)</span><span class="sxs-lookup"><span data-stu-id="beb68-119">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="beb68-120">Uneingeschränkte Delegierung ¹</span><span class="sxs-lookup"><span data-stu-id="beb68-120">Unconstrained delegation¹</span></span></p></li>
<li><p><span data-ttu-id="beb68-121">Beschränkte Delegierung (nur Kerberos-Protokolle verwenden)</span><span class="sxs-lookup"><span data-stu-id="beb68-121">Constrained delegation (Use Kerberos Only Protocols)</span></span></p></li>
<li><p><span data-ttu-id="beb68-122">Beschränkte Delegierung (Verwenden eines beliebigen Authentifizierungsprotokolls) ¹</span><span class="sxs-lookup"><span data-stu-id="beb68-122">Constrained delegation (Use any authentication protocol) ¹</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="beb68-123">¹ nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="beb68-123">¹ Not recommended.</span></span>

## <span data-ttu-id="beb68-124">So konfigurieren Sie eine uneingeschränkte Delegierung, wenn die Domänenfunktionsebene Windows 2000 native ist</span><span class="sxs-lookup"><span data-stu-id="beb68-124">To configure unconstrained delegation when the Domain Functional Level is Windows 2000 native</span></span>


<span data-ttu-id="beb68-125">Führen Sie auf dem Domänencontroller für die Domäne Ihres Webservers die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="beb68-125">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="beb68-126">Klicken Sie auf **Start**, **Verwaltungs Tools**und dann auf **Active Directory-Benutzer und-Computer**.</span><span class="sxs-lookup"><span data-stu-id="beb68-126">Click **Start**, **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="beb68-127">Erweitern Sie Domäne, und erweitern Sie dann den Ordner Computer.</span><span class="sxs-lookup"><span data-stu-id="beb68-127">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="beb68-128">Klicken Sie im rechten Bereich mit der rechten Maustaste auf den Computernamen für den Webserver, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="beb68-128">In the right pane, right-click the computer name for the Web server, and then click **Properties**.</span></span>

4.  <span data-ttu-id="beb68-129">Stellen Sie auf der Registerkarte **Allgemein** sicher, dass das Kontrollkästchen **Computer für Delegierungszwecke vertrauen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="beb68-129">On the **General** tab, ensure that the **Trust computer for delegation** check box is selected.</span></span>

5.  <span data-ttu-id="beb68-130">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="beb68-130">Click **OK**.</span></span>

## <span data-ttu-id="beb68-131">So konfigurieren Sie eine uneingeschränkte Delegierung, wenn es sich bei der Domänenfunktionsebene um Windows Server 2003, Windows Server 2008 oder Windows Server 2008 R2 handelt</span><span class="sxs-lookup"><span data-stu-id="beb68-131">To configure unconstrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="beb68-132">Führen Sie auf dem Domänencontroller für die Domäne Ihres Webservers die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="beb68-132">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="beb68-133">Klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Active Directory-Benutzer und-Computer**.</span><span class="sxs-lookup"><span data-stu-id="beb68-133">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="beb68-134">Erweitern Sie Domäne, und erweitern Sie den Ordner Computer.</span><span class="sxs-lookup"><span data-stu-id="beb68-134">Expand domain, and expand the Computers folder.</span></span>

3.  <span data-ttu-id="beb68-135">Klicken Sie im rechten Bereich mit der rechten Maustaste auf den Computernamen für den Webserver, wählen Sie **Eigenschaften**aus, und klicken Sie dann auf die Registerkarte **Delegierung** .</span><span class="sxs-lookup"><span data-stu-id="beb68-135">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="beb68-136">Klicken Sie auf **diesen Computer für die Delegierung an einen beliebigen Dienst Vertrauen (nur Kerberos)**.</span><span class="sxs-lookup"><span data-stu-id="beb68-136">Click to select **Trust this computer for delegation to any service (Kerberos only)**.</span></span>

5.  <span data-ttu-id="beb68-137">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="beb68-137">Click **OK**.</span></span>

## <span data-ttu-id="beb68-138">So konfigurieren Sie eine begrenzte Delegierung, wenn die Domänenfunktionsebene Windows Server 2003, Windows Server 2008 oder Windows Server 2008 R2 ist</span><span class="sxs-lookup"><span data-stu-id="beb68-138">To configure constrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="beb68-139">Führen Sie auf dem Domänencontroller für die Domäne Ihres Webservers die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="beb68-139">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="beb68-140">Klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Active Directory-Benutzer und-Computer**.</span><span class="sxs-lookup"><span data-stu-id="beb68-140">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="beb68-141">Erweitern Sie Domäne, und erweitern Sie dann den Ordner Computer.</span><span class="sxs-lookup"><span data-stu-id="beb68-141">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="beb68-142">Klicken Sie im rechten Bereich mit der rechten Maustaste auf den Computernamen für den Webserver, wählen Sie **Eigenschaften**aus, und klicken Sie dann auf die Registerkarte **Delegierung** .</span><span class="sxs-lookup"><span data-stu-id="beb68-142">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="beb68-143">Klicken Sie auf **diesen Computer für Delegierung nur an angegebene Dienste vertrauen**.</span><span class="sxs-lookup"><span data-stu-id="beb68-143">Click to select **Trust this computer for delegation to specified services only**.</span></span>

5.  <span data-ttu-id="beb68-144">Stellen Sie sicher, dass **nur Kerberos verwenden** ausgewählt ist, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="beb68-144">Ensure that **Use Kerberos only** is selected, and then click **OK**.</span></span>

6.  <span data-ttu-id="beb68-145">Klicken Sie auf die Schaltfläche **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="beb68-145">Click the **Add** button.</span></span> <span data-ttu-id="beb68-146">Klicken Sie im Dialogfeld **Dienste hinzufügen** auf **Benutzer oder Computer**, und navigieren Sie dann zu dem Namen des Microsoft SQL Server, auf dem sich der App-V-Datenspeicher befindet, oder geben Sie ihn ein, um die Anmeldeinformationen des Benutzers aus IIS zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="beb68-146">In the **Add Services** dialog box, click **Users or Computers**, and then browse to or type the name of the Microsoft SQL server that has the App-V data store and is to receive the users credentials from IIS.</span></span> <span data-ttu-id="beb68-147">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="beb68-147">Click **OK**.</span></span>

7.  <span data-ttu-id="beb68-148">Wählen Sie in der Liste **verfügbare Dienste** den MSSQLSvc-Dienst aus, der die Portnummer auflistet, für die der Microsoft SQL Server Verbindungen für die App-V-Datenbank akzeptiert (der Standardport ist 1433).</span><span class="sxs-lookup"><span data-stu-id="beb68-148">In the **Available Services** list, select the MSSQLSvc service that lists port number on which the Microsoft SQL Server is accepting connections for the App-V database (the default port is 1433).</span></span> <span data-ttu-id="beb68-149">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="beb68-149">Click **OK**.</span></span>

### <span data-ttu-id="beb68-150">Zusätzliche Schritte zum Konfigurieren von IIS 7 für eine begrenzte Delegierung</span><span class="sxs-lookup"><span data-stu-id="beb68-150">Additional steps to configure IIS 7 for constrained delegation</span></span>

<span data-ttu-id="beb68-151">Wenn Sie den Verwaltungs-Webdienst auf einem IIS 7-Server ausführen, müssen Sie die folgenden Schritte ausführen, um die IIS 7- *useAppPoolCredentials* -Variable auf "true" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="beb68-151">If you are running the Management Web Service on an IIS 7 server, you must complete the following steps to set the IIS 7 *useAppPoolCredentials* variable to True.</span></span>

1.  <span data-ttu-id="beb68-152">Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="beb68-152">Open an elevated Command Prompt window.</span></span> <span data-ttu-id="beb68-153">Klicken Sie zum Öffnen eines Eingabeaufforderungsfensters mit erhöhten Rechten auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie mit der rechten Maustaste auf **Eingabeaufforderung**, und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="beb68-153">To open an elevated Command Prompt window, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="beb68-154">Navigieren zu%windir%\\system32\\inetsrv.</span><span class="sxs-lookup"><span data-stu-id="beb68-154">Navigate to %windir%\\system32\\inetsrv.</span></span>

3.  <span data-ttu-id="beb68-155">Geben Sie **appcmd.exe Satz config-section: System. Webserver/Security/Authentication/WindowsAuthentication-useAppPoolCredentials: true**ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="beb68-155">Type **appcmd.exe set config -section:system.webServer/security/authentication/windowsAuthentication -useAppPoolCredentials:true**, and then press ENTER.</span></span>

 

 





