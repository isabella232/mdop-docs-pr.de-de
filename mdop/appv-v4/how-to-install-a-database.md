---
title: So installieren Sie eine Datenbank
description: So installieren Sie eine Datenbank
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807083"
---
# <span data-ttu-id="1cdfc-103">So installieren Sie eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="1cdfc-103">How to Install a Database</span></span>


<span data-ttu-id="1cdfc-104">Mit dem folgenden Verfahren können Sie eine Datenbank für Ihre serverbasierte Bereitstellung von Application Virtualization installieren, wenn noch keine Datenbank verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-104">You can use the following procedure to install a database for your server-based deployment of Application Virtualization if a database is not already available.</span></span> <span data-ttu-id="1cdfc-105">In einer Produktionsumgebung stellen Sie normalerweise eine Verbindung mit einer vorhandenen Datenbank her.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-105">Typically, in a production environment, you will connect to an existing database.</span></span>

<span data-ttu-id="1cdfc-106">**Wichtig**  Um die Datenbank zu installieren, müssen Sie ein Netzwerkkonto mit den entsprechenden Berechtigungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-106">**Important** To install the database, you must use a network account with the appropriate permissions.</span></span> <span data-ttu-id="1cdfc-107">Wenn Ihre Organisation erfordert, dass nur Datenbankadministratoren Datenbankaktualisierungen erstellen und durchführen können, stehen Skripts zur Verfügung, mit denen diese Aufgabe ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-107">If your organization requires that only database administrators are allowed to create and conduct database upgrades, scripts are available that allow this task to be performed.</span></span>

 

**<span data-ttu-id="1cdfc-108">So installieren Sie eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="1cdfc-108">To install a database</span></span>**

1.  <span data-ttu-id="1cdfc-109">Navigieren Sie zum Speicherort des Application Virtualization System-Setupprogramms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-109">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

2.  <span data-ttu-id="1cdfc-110">Klicken Sie auf der **Seite Willkommen**auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-110">On the **Welcome Page**, click **Next**.</span></span>

3.  <span data-ttu-id="1cdfc-111">Wählen Sie auf der Seite **Lizenzvertrag** die Option **Ich akzeptiere die Lizenzbedingungen**aus, um den Lizenzvertrag anzunehmen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-111">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and click **Next**.</span></span>

4.  <span data-ttu-id="1cdfc-112">Geben Sie auf der Seite **Registrierungsinformationen** den **Benutzernamen** und die **Organisations** Informationen an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-112">On the **Registering Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

5.  <span data-ttu-id="1cdfc-113">Wählen Sie auf der Seite **Setuptyp** die Option **Benutzerdefiniert** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-113">On the **Setup Type** page, select **Custom** and then click **Next**.</span></span>

6.  <span data-ttu-id="1cdfc-114">Deaktivieren Sie auf der Seite **Benutzerdefiniertes Setup** alle Application Virtualization System-Komponenten außer **Application Virtualization Server**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-114">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    <span data-ttu-id="1cdfc-115">**Hinweis**  Wenn eine Komponente bereits auf dem Computer installiert ist, wird Sie im **benutzerdefinierten Setup** -Bildschirm automatisch deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-115">**Note** If a component is already installed on the computer, by deselecting it on the **Custom Setup** screen it will automatically be uninstalled.</span></span>

     

7.  <span data-ttu-id="1cdfc-116">Geben Sie auf der Seite **Daten Bank Server** die Kennwörter ein, weisen Sie einen Installationspfad zu, speichern Sie die Informationen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-116">On the **Database Server** page, type the passwords, assign an installation path, save the information, and click **Next**.</span></span>

8.  <span data-ttu-id="1cdfc-117">Wählen Sie einen Namen für die Datenbank aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-117">Select a name for the database, and then click **Next**.</span></span>

    <span data-ttu-id="1cdfc-118">**Hinweis**  Wenn bei dem Versuch, diesen Schritt abzuschließen, Fehler 25109 angezeigt wird, haben Sie die erforderlichen Berechtigungen zum Installieren der Datenbank falsch eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-118">**Note** If error 25109 is displayed when you try to complete this step, you have incorrectly set up the permissions necessary to install the database.</span></span> <span data-ttu-id="1cdfc-119">Weitere Informationen zum Einrichten der erforderlichen SQL-Berechtigungen finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=132144> .</span><span class="sxs-lookup"><span data-stu-id="1cdfc-119">For details on setting up the necessary SQL permissions, please see <https://go.microsoft.com/fwlink/?LinkId=132144>.</span></span>

     

9.  <span data-ttu-id="1cdfc-120">Geben Sie auf dem Bildschirm **Verzeichnis Server** einen Domänennamen und die Anmeldeinformationen ein, die von Application Virtualization Server und dem Verwaltungs-Webdienst für den Zugriff auf Ihren Domänencontroller verwendet werden, speichern Sie diese Informationen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-120">On the **Directory Server** screen, enter a domain name and credentials that Application Virtualization Servers and the Management Web Service will use to access your domain controller, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="1cdfc-121">**Hinweis**  Bei der Installation wird standardmäßig die Domäne des aktuellen Computers verwendet.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-121">**Note** The installation will default to the domain of the current computer.</span></span>

     

10. <span data-ttu-id="1cdfc-122">Geben Sie auf der Seite **Administratorgruppe** den Namen einer Gruppe ein, die über Administratorrechte verfügen soll, speichern Sie diese Informationen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-122">On the **Administrator Group** page, enter the name of a group that will have Administrator privileges, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="1cdfc-123">**Hinweis**  Sie können auch die ersten Zeichen des Namens einer Gruppe eingeben, die über Administratorrechte verfügen, klicken Sie auf **weiter**, und wählen Sie auf der Seite **Administrator Gruppe auswählen** die Gruppe aus der resultierenden Liste aus.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-123">**Note** You can also enter the first few characters of the name of a group that will have Administration privileges, click **Next**, and on the **Select Administrator Group** screen, select the group from the resulting list.</span></span> <span data-ttu-id="1cdfc-124">Speichern Sie diese Informationen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-124">Then save this information and click **Next**.</span></span>

     

11. <span data-ttu-id="1cdfc-125">Geben Sie auf der Seite **Standardanbietergruppe** den vollständigen Namen einer Gruppe ein, die den Zugriff auf Anwendungen steuern soll, speichern Sie diese Informationen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-125">On the **Default Provider Group** page, enter the complete name of a group that will control access to applications, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="1cdfc-126">**Hinweis**  Sie können auch die ersten Zeichen des Namens einer Gruppe eingeben, die den Zugriff auf Anwendungen steuern soll, klicken Sie auf **weiter**, und wählen Sie auf dem Bildschirm **Standardanbietergruppe auswählen** die Gruppe in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-126">**Note** You can also enter the first few characters of the name of a group that will control access to applications, click **Next**, and on the **Select Default Provider Group** screen, select the group in the list.</span></span> <span data-ttu-id="1cdfc-127">Speichern Sie diese Informationen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-127">Then save this information and click **Next**.</span></span>

     

12. <span data-ttu-id="1cdfc-128">Klicken Sie auf der Seite **abgeschlossen des Installations-Assistenten** auf **Fertig stellen**, um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-128">On the **Installation Wizard Completed** page, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="1cdfc-129">**Wichtig**  Es kann einige Minuten dauern, bis die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-129">**Important** The installation can take a few minutes to finish.</span></span> <span data-ttu-id="1cdfc-130">Über dem Windows-Desktop-Benachrichtigungsbereich blinkt eine Statusmeldung, die angibt, ob die Installation erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1cdfc-130">A status message will flash above the Windows desktop notification area, indicating whether the installation succeeded.</span></span>

     

## <span data-ttu-id="1cdfc-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1cdfc-131">Related topics</span></span>


[<span data-ttu-id="1cdfc-132">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="1cdfc-132">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





