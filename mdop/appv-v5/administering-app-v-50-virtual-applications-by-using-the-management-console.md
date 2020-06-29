---
title: Verwalten von mit App-V 5.0 virtualisierten Anwendungen mithilfe der Verwaltungskonsole
description: Verwalten von mit App-V 5.0 virtualisierten Anwendungen mithilfe der Verwaltungskonsole
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806050"
---
# <span data-ttu-id="fe7f4-103">Verwalten von mit App-V 5.0 virtualisierten Anwendungen mithilfe der Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="fe7f4-103">Administering App-V 5.0 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="fe7f4-104">Verwenden Sie den Microsoft Application Virtualization (App-V) 5,0-Verwaltungsserver, um Pakete, Verbindungsgruppen und den Paketzugriff in Ihrer Umgebung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-104">Use the Microsoft Application Virtualization (App-V) 5.0 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="fe7f4-105">Der Server veröffentlicht Anwendungssymbole, Verknüpfungen und Dateitypzuordnungen auf autorisierten Computern, auf denen der App-V 5,0-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="fe7f4-106">Mindestens ein Verwaltungsserver gibt in der Regel einen gemeinsamen Datenspeicher für Konfigurations-und Paketinformationen frei.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="fe7f4-107">Der Verwaltungsserver verwendet Active Directory-Domänendienste (AD DS)-Gruppen, um die Benutzerautorisierung zu verwalten und SQL Server zum Verwalten der Datenbank und des Datenspeichers zu installieren.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="fe7f4-108">Da die Verwaltungsserver Anwendungen bei Bedarf an Endbenutzer streamen, eignen sich diese Server ideal für Systemkonfigurationen mit zuverlässigen LANs mit hoher Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="fe7f4-109">Der Verwaltungsserver besteht aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="fe7f4-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="fe7f4-110">Verwaltungsserver – verwenden Sie den Verwaltungsserver, um Pakete und Verbindungsgruppen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="fe7f4-111">Publishing Server – verwenden Sie den Veröffentlichungsserver zum Bereitstellen von Paketen auf Computern, auf denen der App-V 5,0-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.0 client.</span></span>

-   <span data-ttu-id="fe7f4-112">Verwaltungsdatenbank – verwenden Sie die Verwaltungsdatenbank, um den Paketzugriff zu verwalten und die Synchronisierung des Servers mit dem Verwaltungsserver zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="fe7f4-113">Verwaltungskonsolen Aufgaben</span><span class="sxs-lookup"><span data-stu-id="fe7f4-113">Management Console tasks</span></span>


<span data-ttu-id="fe7f4-114">Die häufigsten Aufgaben, die Sie mit der App-V 5,0-Verwaltungskonsole ausführen können, sind:</span><span class="sxs-lookup"><span data-stu-id="fe7f4-114">The most common tasks that you can perform with the App-V 5.0 Management console are:</span></span>

-   [<span data-ttu-id="fe7f4-115">So stellen Sie eine Verbindung mit der Verwaltungskonsole her</span><span class="sxs-lookup"><span data-stu-id="fe7f4-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-beta.md)

-   [<span data-ttu-id="fe7f4-116">So fügen Sie mithilfe der Verwaltungskonsole Pakete hinzu oder aktualisieren sie</span><span class="sxs-lookup"><span data-stu-id="fe7f4-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [<span data-ttu-id="fe7f4-117">So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete</span><span class="sxs-lookup"><span data-stu-id="fe7f4-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [<span data-ttu-id="fe7f4-118">So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket</span><span class="sxs-lookup"><span data-stu-id="fe7f4-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [<span data-ttu-id="fe7f4-119">So löschen Sie ein Paket in der Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="fe7f4-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-beta.md)

-   [<span data-ttu-id="fe7f4-120">So fügen Sie mithilfe der Verwaltungskonsole einen Administrator hinzu oder entfernen einen Administrator</span><span class="sxs-lookup"><span data-stu-id="fe7f4-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [<span data-ttu-id="fe7f4-121">So registrieren Sie mithilfe der Verwaltungskonsole einen Veröffentlichungsserver oder heben die Registrierung eines Veröffentlichungsservers auf</span><span class="sxs-lookup"><span data-stu-id="fe7f4-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [<span data-ttu-id="fe7f4-122">So erstellen Sie mithilfe der App-V 5.0-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="fe7f4-122">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [<span data-ttu-id="fe7f4-123">So übertragen Sie mithilfe der Verwaltungskonsole Zugriff und Konfigurationen auf eine andere Version eines Pakets</span><span class="sxs-lookup"><span data-stu-id="fe7f4-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [<span data-ttu-id="fe7f4-124">So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an</span><span class="sxs-lookup"><span data-stu-id="fe7f4-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [<span data-ttu-id="fe7f4-125">Konfigurieren von Anwendungen und Standard-Erweiterungen für virtuelle Anwendungen in der Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="fe7f4-125">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

<span data-ttu-id="fe7f4-126">Die Hauptelemente der App-V 5,0-Verwaltungskonsole sind:</span><span class="sxs-lookup"><span data-stu-id="fe7f4-126">The main elements of the App-V 5.0 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fe7f4-127">Registerkarte "Verwaltungskonsole"</span><span class="sxs-lookup"><span data-stu-id="fe7f4-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="fe7f4-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe7f4-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe7f4-129">Übersicht</span><span class="sxs-lookup"><span data-stu-id="fe7f4-129">Overview</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><strong><span data-ttu-id="fe7f4-130">App-v Sequencer </strong> - Wählen Sie diese Option aus, um allgemeine Informationen zur Verwendung des App-v 5,0-Sequenzers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-130">App-V Sequencer</strong> - Select this option to review general information about using the App-V 5.0 sequencer.</span></span></p></li>
<li><p><strong><span data-ttu-id="fe7f4-131">Bibliothek für Anwendungspakete </strong> – Wählen Sie diese Option aus, um die <strong> </strong> Seite Pakete der Verwaltungskonsole zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-131">Application Packages Library</strong> – Select this option to open the <strong>PACKAGES</strong> page of the Management Console.</span></span> <span data-ttu-id="fe7f4-132">Auf dieser Seite können Sie die Pakete überprüfen, die dem Server hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-132">Use this page to review packages that have been added to the server.</span></span> <span data-ttu-id="fe7f4-133">Sie können auch die Verbindungsgruppen verwalten sowie Pakete hinzufügen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-133">You can also manage the connection groups, as well as add or upgrade packages.</span></span></p></li>
<li><p><strong><span data-ttu-id="fe7f4-134">Server </strong> – Wählen Sie diese Option aus, um die <strong> </strong> Seite Server der Verwaltungskonsole zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-134">SERVERS</strong> – Select this option to open the <strong>SERVERS</strong> page of the Management Console.</span></span> <span data-ttu-id="fe7f4-135">Auf dieser Seite können Sie die Liste der Server überprüfen, die bei ihrer App-V 5,0-Infrastruktur registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-135">Use this page to review the list of servers that have been registered with your App-V 5.0 infrastructure.</span></span></p></li>
<li><p><strong><span data-ttu-id="fe7f4-136">Clients </strong> – Wählen Sie diese Option aus, um allgemeine Informationen zu App-V 5,0-Clients zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-136">CLIENTS</strong> – Select this option to review general information about App-V 5.0 clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe7f4-137">Registerkarte "Pakete"</span><span class="sxs-lookup"><span data-stu-id="fe7f4-137">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe7f4-138">Verwenden <strong> Sie die </strong> Registerkarte Pakete, um Pakete hinzuzufügen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-138">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span> <span data-ttu-id="fe7f4-139">Sie können Verbindungsgruppen auch verwalten, indem Sie auf <strong> Verbindungsgruppen klicken </strong> .</span><span class="sxs-lookup"><span data-stu-id="fe7f4-139">You can also manage connection groups by clicking <strong>CONNECTION GROUPS</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe7f4-140">Server (Registerkarte)</span><span class="sxs-lookup"><span data-stu-id="fe7f4-140">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe7f4-141">Verwenden Sie <strong> die </strong> Registerkarte Server, um einen neuen Server zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-141">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe7f4-142">Registerkarte "Administratoren"</span><span class="sxs-lookup"><span data-stu-id="fe7f4-142">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe7f4-143">Verwenden Sie <strong> die </strong> Registerkarte Administratoren, um Administratoren in ihrer App-V 5,0-Umgebung zu registrieren, hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fe7f4-143">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.0 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a><span data-ttu-id="fe7f4-144">Weitere Ressourcen für diese App-V 5,0-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="fe7f4-144">Other resources for this App-V 5.0 deployment</span></span>


-   [<span data-ttu-id="fe7f4-145">Microsoft Application Virtualization 5,0-Administrator Handbuch</span><span class="sxs-lookup"><span data-stu-id="fe7f4-145">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="fe7f4-146">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="fe7f4-146">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





