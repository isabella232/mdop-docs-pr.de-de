---
title: Verwalten von mit App-V 5.1 virtualisierten Anwendungen mithilfe der Verwaltungskonsole
description: Verwalten von mit App-V 5.1 virtualisierten Anwendungen mithilfe der Verwaltungskonsole
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806047"
---
# <span data-ttu-id="6db66-103">Verwalten von mit App-V 5.1 virtualisierten Anwendungen mithilfe der Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="6db66-103">Administering App-V 5.1 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="6db66-104">Verwenden Sie den Microsoft Application Virtualization (App-V) 5,1-Verwaltungsserver, um Pakete, Verbindungsgruppen und den Paketzugriff in Ihrer Umgebung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6db66-104">Use the Microsoft Application Virtualization (App-V) 5.1 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="6db66-105">Der Server veröffentlicht Anwendungssymbole, Verknüpfungen und Dateitypzuordnungen auf autorisierten Computern, auf denen der App-V 5,1-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6db66-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="6db66-106">Mindestens ein Verwaltungsserver gibt in der Regel einen gemeinsamen Datenspeicher für Konfigurations-und Paketinformationen frei.</span><span class="sxs-lookup"><span data-stu-id="6db66-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="6db66-107">Der Verwaltungsserver verwendet Active Directory-Domänendienste (AD DS)-Gruppen, um die Benutzerautorisierung zu verwalten und SQL Server zum Verwalten der Datenbank und des Datenspeichers zu installieren.</span><span class="sxs-lookup"><span data-stu-id="6db66-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="6db66-108">Da die Verwaltungsserver Anwendungen bei Bedarf an Endbenutzer streamen, eignen sich diese Server ideal für Systemkonfigurationen mit zuverlässigen LANs mit hoher Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="6db66-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="6db66-109">Der Verwaltungsserver besteht aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="6db66-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="6db66-110">Verwaltungsserver – verwenden Sie den Verwaltungsserver, um Pakete und Verbindungsgruppen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6db66-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="6db66-111">Publishing Server – verwenden Sie den Veröffentlichungsserver zum Bereitstellen von Paketen auf Computern, auf denen der App-V 5,1-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6db66-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.1 client.</span></span>

-   <span data-ttu-id="6db66-112">Verwaltungsdatenbank – verwenden Sie die Verwaltungsdatenbank, um den Paketzugriff zu verwalten und die Synchronisierung des Servers mit dem Verwaltungsserver zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6db66-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="6db66-113">Verwaltungskonsolen Aufgaben</span><span class="sxs-lookup"><span data-stu-id="6db66-113">Management Console tasks</span></span>


<span data-ttu-id="6db66-114">Die häufigsten Aufgaben, die Sie mit der App-V 5,1-Verwaltungskonsole ausführen können, sind:</span><span class="sxs-lookup"><span data-stu-id="6db66-114">The most common tasks that you can perform with the App-V 5.1 Management console are:</span></span>

-   [<span data-ttu-id="6db66-115">So stellen Sie eine Verbindung mit der Verwaltungskonsole her</span><span class="sxs-lookup"><span data-stu-id="6db66-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-51.md)

-   [<span data-ttu-id="6db66-116">So fügen Sie mithilfe der Verwaltungskonsole Pakete hinzu oder aktualisieren sie</span><span class="sxs-lookup"><span data-stu-id="6db66-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [<span data-ttu-id="6db66-117">So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete</span><span class="sxs-lookup"><span data-stu-id="6db66-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [<span data-ttu-id="6db66-118">So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket</span><span class="sxs-lookup"><span data-stu-id="6db66-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [<span data-ttu-id="6db66-119">So löschen Sie ein Paket in der Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="6db66-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-51.md)

-   [<span data-ttu-id="6db66-120">So fügen Sie mithilfe der Verwaltungskonsole einen Administrator hinzu oder entfernen einen Administrator</span><span class="sxs-lookup"><span data-stu-id="6db66-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [<span data-ttu-id="6db66-121">So registrieren Sie mithilfe der Verwaltungskonsole einen Veröffentlichungsserver oder heben die Registrierung eines Veröffentlichungsservers auf</span><span class="sxs-lookup"><span data-stu-id="6db66-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [<span data-ttu-id="6db66-122">So erstellen Sie mithilfe der App-V 5.1-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei an</span><span class="sxs-lookup"><span data-stu-id="6db66-122">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [<span data-ttu-id="6db66-123">So übertragen Sie mithilfe der Verwaltungskonsole Zugriff und Konfigurationen auf eine andere Version eines Pakets</span><span class="sxs-lookup"><span data-stu-id="6db66-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [<span data-ttu-id="6db66-124">So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an</span><span class="sxs-lookup"><span data-stu-id="6db66-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [<span data-ttu-id="6db66-125">So zeigen Sie mithilfe der Verwaltungskonsole Anwendungen und virtuelle Standardanwendungserweiterungen an und konfigurieren sie</span><span class="sxs-lookup"><span data-stu-id="6db66-125">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

<span data-ttu-id="6db66-126">Die Hauptelemente der App-V 5,1-Verwaltungskonsole sind:</span><span class="sxs-lookup"><span data-stu-id="6db66-126">The main elements of the App-V 5.1 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6db66-127">Registerkarte "Verwaltungskonsole"</span><span class="sxs-lookup"><span data-stu-id="6db66-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="6db66-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6db66-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6db66-129">Registerkarte "Pakete"</span><span class="sxs-lookup"><span data-stu-id="6db66-129">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6db66-130">Verwenden <strong> Sie die </strong> Registerkarte Pakete, um Pakete hinzuzufügen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6db66-130">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6db66-131">Registerkarte "Verbindungsgruppen"</span><span class="sxs-lookup"><span data-stu-id="6db66-131">Connection Groups tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6db66-132">Verwenden Sie die <strong> </strong> Registerkarte Verbindungsgruppen, um Verbindungsgruppen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6db66-132">Use the <strong>CONNECTION GROUPS</strong> tab to manage connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6db66-133">Server (Registerkarte)</span><span class="sxs-lookup"><span data-stu-id="6db66-133">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6db66-134">Verwenden Sie <strong> die </strong> Registerkarte Server, um einen neuen Server zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="6db66-134">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6db66-135">Registerkarte "Administratoren"</span><span class="sxs-lookup"><span data-stu-id="6db66-135">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6db66-136">Verwenden Sie <strong> die </strong> Registerkarte Administratoren, um Administratoren in ihrer App-V 5,1-Umgebung zu registrieren, hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6db66-136">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.1 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6db66-137">**Wichtig**  JavaScript muss im Browser aktiviert sein, über den die Webverwaltungs Konsole geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="6db66-137">**Important** JavaScript must be enabled on the browser that opens the Web Management Console.</span></span>

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a><span data-ttu-id="6db66-138">Weitere Ressourcen für diese App-V 5,1-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="6db66-138">Other resources for this App-V 5.1 deployment</span></span>


-   [<span data-ttu-id="6db66-139">Microsoft Application Virtualization 5,1-Administrator Handbuch</span><span class="sxs-lookup"><span data-stu-id="6db66-139">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="6db66-140">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="6db66-140">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





