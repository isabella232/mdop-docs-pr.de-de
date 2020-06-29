---
title: So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole
description: So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812082"
---
# <span data-ttu-id="ecc5f-103">So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="ecc5f-103">How to Install MED-V Client and MED-V Management Console</span></span>


<span data-ttu-id="ecc5f-104">Die folgenden MED-V-Komponenten sind im Client. MSI-Paket enthalten:</span><span class="sxs-lookup"><span data-stu-id="ecc5f-104">The following MED-V components are included in the client .msi package:</span></span>

-   <span data-ttu-id="ecc5f-105">Med-v-Client – die Med-v-Software, die auf Clientcomputern für die Ausführung von Med-v-Arbeitsbereichen installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-105">MED-V client—The MED-V software that must be installed on client computers for running MED-V workspaces.</span></span>

-   <span data-ttu-id="ecc5f-106">Med-v-Verwaltungskonsole – das Verwaltungstool, das Administratoren verwenden können, um Bilder, Med-v-Arbeitsbereiche und Richtlinien zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-106">MED-V management console—The administrative tool that administrators can use to create and maintain images, MED-V workspaces, and policies.</span></span>

<span data-ttu-id="ecc5f-107">Die Med-v-Verwaltungskonsole und der Med-v-Client sind beide aus dem Med-v-Client. MSI-Paket installiert.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-107">The MED-V management console and the MED-V client are both installed from the MED-V client .msi package.</span></span> <span data-ttu-id="ecc5f-108">Der Med-v-Client kann jedoch unabhängig von der Med-v-Verwaltungskonsole installiert werden, indem das Kontrollkästchen **Installieren der Med-v-Verwaltungsanwendung** während der Installation deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-108">The MED-V client, however, can be installed independently without the MED-V management console by clearing the **Install the MED-V Management application** check box during installation.</span></span>

**<span data-ttu-id="ecc5f-109">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ecc5f-109">Note</span></span>**  
<span data-ttu-id="ecc5f-110">Der Med-v-Client und die Med-v-Verwaltungskonsole können nur auf Computern unter Windows 7, Windows Vista und Windows XP installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-110">The MED-V client and MED-V management console can only be installed on Windows 7-, Windows Vista-, and Windows XP-based computers.</span></span> <span data-ttu-id="ecc5f-111">Sie können nicht auf Serverprodukten installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-111">They cannot be installed on server products.</span></span>



**<span data-ttu-id="ecc5f-112">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ecc5f-112">Note</span></span>**  
<span data-ttu-id="ecc5f-113">Installieren Sie den MED-V-Client nicht mit dem Befehl Windows **runas** .</span><span class="sxs-lookup"><span data-stu-id="ecc5f-113">Do not install the MED-V client using the Windows **runas** command.</span></span>



**<span data-ttu-id="ecc5f-114">So installieren Sie den MED-V-Client</span><span class="sxs-lookup"><span data-stu-id="ecc5f-114">To install the MED-V client</span></span>**

1.  <span data-ttu-id="ecc5f-115">Melden Sie sich als Benutzer mit lokalen Administratorrechten auf dem lokalen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-115">Log in as a user with local administrator rights on the local computer.</span></span>

2.  <span data-ttu-id="ecc5f-116">Führen Sie das MED-V. MSI-Paket aus.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-116">Run the MED-V .msi package.</span></span>

    <span data-ttu-id="ecc5f-117">Das MED-V. MSI-Paket heißt *MED-V\_x.msi*, wobei *x* die Versionsnummer ist.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-117">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="ecc5f-118">Beispiel: *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-118">For example, *MED-V\_1.0.65.msi*.</span></span>

3.  <span data-ttu-id="ecc5f-119">Wenn der **Begrüßungs** Bildschirm des InstallShield-Assistenten angezeigt wird, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-119">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

4.  <span data-ttu-id="ecc5f-120">Lesen Sie auf dem Bildschirm **Lizenzvertrag** den Lizenzvertrag, klicken Sie auf **Ich stimme den Bedingungen des Lizenzvertrags**zu, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-120">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and click **Next**.</span></span>

    <span data-ttu-id="ecc5f-121">Der Bildschirm **Zielordner** wird angezeigt, und der Standardinstallationsordner wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-121">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="ecc5f-122">Der Standardinstallationsordner ist das Verzeichnis, in dem das Betriebssystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-122">The default installation folder is the directory where the operating system is installed.</span></span>

    -   <span data-ttu-id="ecc5f-123">Wenn Sie den Ordner ändern möchten, in dem MED-V installiert werden soll, klicken Sie auf **ändern**, und navigieren Sie zu einem vorhandenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-123">To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.</span></span>

5.  <span data-ttu-id="ecc5f-124">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-124">Click **Next**.</span></span>

6.  <span data-ttu-id="ecc5f-125">Konfigurieren Sie auf dem Bildschirm **Med-v-Einstellungen** die Med-v-Installation wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ecc5f-125">On the **MED-V Settings** screen, configure the MED-V installation as follows:</span></span>

    -   <span data-ttu-id="ecc5f-126">Aktivieren Sie das Kontrollkästchen **MED-V-Verwaltungsanwendung installieren** , um die Verwaltungskomponente in die Installation einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-126">Select the **Install the MED-V management application** check box to include the management component in the installation.</span></span>

        **<span data-ttu-id="ecc5f-127">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ecc5f-127">Note</span></span>**  
        <span data-ttu-id="ecc5f-128">Administratoren von Unternehmens Desktop-Virtualisierung sollten die MED-V-Verwaltungsanwendung installieren.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-128">Enterprise Desktop Virtualization administrators should install the MED-V management application.</span></span> <span data-ttu-id="ecc5f-129">Diese Anwendung ist für die Konfiguration von Desktop Bildern und MED-V-Arbeitsbereichen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-129">This application is required for configuring desktop images and MED-V workspaces.</span></span>



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. <span data-ttu-id="ecc5f-130">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-130">Click **Next**.</span></span>

8. <span data-ttu-id="ecc5f-131">Klicken Sie auf dem Bildschirm **bereit zum Installieren des Programms** auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-131">On the **Ready to Install the Program** screen, click **Install**.</span></span>

   <span data-ttu-id="ecc5f-132">Die MED-V-Clientinstallation wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-132">The MED-V client installation starts.</span></span> <span data-ttu-id="ecc5f-133">Dies kann mehrere Minuten dauern, und auf dem Bildschirm wird möglicherweise kein Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-133">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="ecc5f-134">Während der Installation werden mehrere Status Bildschirme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-134">During installation, several progress screens appear.</span></span> <span data-ttu-id="ecc5f-135">Wenn eine Meldung angezeigt wird, folgen Sie den Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-135">If a message appears, follow the instructions provided.</span></span>

   <span data-ttu-id="ecc5f-136">Nach erfolgreicher Installation wird der Bildschirm **InstallShield-Assistent abgeschlossen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-136">Upon successful installation, the **InstallShield Wizard Completed** screen appears.</span></span>

9. <span data-ttu-id="ecc5f-137">Klicken Sie auf **Fertig stellen** , um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-137">Click **Finish** to close the wizard.</span></span>

## <span data-ttu-id="ecc5f-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ecc5f-138">Related topics</span></span>


[<span data-ttu-id="ecc5f-139">Unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="ecc5f-139">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="ecc5f-140">Installations- und Aktualisierungsprüflisten</span><span class="sxs-lookup"><span data-stu-id="ecc5f-140">Installation and Upgrade Checklists</span></span>](installation-and-upgrade-checklists.md)









