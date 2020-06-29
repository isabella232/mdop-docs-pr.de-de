---
title: So installieren Sie Management Web Service
description: So installieren Sie Management Web Service
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807043"
---
# <span data-ttu-id="c562f-103">So installieren Sie Management Web Service</span><span class="sxs-lookup"><span data-stu-id="c562f-103">How to Install the Management Web Service</span></span>


<span data-ttu-id="c562f-104">Gehen Sie wie folgt vor, um den Application Virtualization Management Web Service auf einem Zielcomputer im Netzwerk zu installieren, wobei ein Anmeldekonto über lokale Administratorrechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="c562f-104">Use the following procedure to install the Application Virtualization Management Web Service on a target computer on the network, with a logon account having local administrative privileges.</span></span> <span data-ttu-id="c562f-105">Auch wenn dies nicht erforderlich ist, empfehlen wir, diese Komponente auf dem Webserver zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c562f-105">Although it is not required, we recommended that you install this component on your Web server.</span></span>

**<span data-ttu-id="c562f-106">So installieren Sie den Verwaltungs-Web-Service</span><span class="sxs-lookup"><span data-stu-id="c562f-106">To install the Management Web Service</span></span>**

1.  <span data-ttu-id="c562f-107">Vergewissern Sie sich, dass auf dem Zielcomputer keine vorherigen Versionen des Application Virtualization-Webdiensts installiert sind.</span><span class="sxs-lookup"><span data-stu-id="c562f-107">Verify that no previous versions of the Application Virtualization Web Service are installed on your target computer.</span></span>

2.  <span data-ttu-id="c562f-108">Navigieren Sie zum Speicherort des Application Virtualization System-Setupprogramms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="c562f-108">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="c562f-109">Klicken Sie nach dem Öffnen des Installations-Assistenten auf der Seite **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c562f-109">After the Installation Wizard opens, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="c562f-110">Wählen Sie auf der Seite **Lizenzvertrag** die Option **Ich akzeptiere die Lizenzbedingungen**aus, um den Lizenzvertrag anzunehmen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c562f-110">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="c562f-111">Geben Sie auf der Seite **Registrierungsinformationen** den **Benutzernamen** und die Organisationsinformationen an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c562f-111">On the **Registration Information** page, specify the **User Name** and organization information, and then click **Next**.</span></span>

6.  <span data-ttu-id="c562f-112">Klicken Sie auf der Seite **Setuptyp** auf **Benutzerdefiniert**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c562f-112">On the **Setup Type** page, click **Custom**, and then click **Next**.</span></span>

    <span data-ttu-id="c562f-113">**Hinweis**  Wenn es sich nicht um die erste Komponente handelt, die Sie auf diesem Computer installiert haben, wird die Seite **Programmwartung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c562f-113">**Note** If this is not the first component you installed on this computer, the **Program Maintenance** page is displayed.</span></span> <span data-ttu-id="c562f-114">Klicken Sie auf der Seite **Programmwartung** auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="c562f-114">On the **Program Maintenance** page, click **Modify**.</span></span>

     

7.  <span data-ttu-id="c562f-115">Deaktivieren Sie auf der Seite **Benutzerdefiniertes Setup** alle Application Virtualization System-Komponenten mit Ausnahme des **App virt-Verwaltungsdiensts**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c562f-115">On the **Custom Setup** page, clear all Application Virtualization System components except **App Virt Management Service**, and then click **Next**.</span></span>

    <span data-ttu-id="c562f-116">**Hinweis**  Wenn eine Komponente bereits auf dem Computer installiert ist, können Sie Sie automatisch deinstallieren, indem Sie Sie auf der **benutzerdefinierten Setup** Seite löschen.</span><span class="sxs-lookup"><span data-stu-id="c562f-116">**Note** If a component is already installed on the computer, by clearing it on the **Custom Setup** page, you will automatically uninstall it.</span></span>

     

8.  <span data-ttu-id="c562f-117">Klicken Sie auf der Seite **Daten Bank Server** auf **Verbindung mit verfügbarer Datenbank herstellen**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c562f-117">On the **Database Server** page, click **Connect to available database**, and then click **Next**.</span></span>

    <span data-ttu-id="c562f-118">**Hinweis**  In einer Produktionsumgebung geht Microsoft davon aus, dass Sie eine Verbindung mit einer vorhandenen Datenbank herstellen.</span><span class="sxs-lookup"><span data-stu-id="c562f-118">**Note** In a production environment, Microsoft assumes that you will connect to an existing database.</span></span> <span data-ttu-id="c562f-119">Wenn Sie eine Datenbank installieren möchten, lesen Sie [so wird es gemacht: Installieren einer Datenbank](how-to-install-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="c562f-119">If you want to install a database, see [How to Install a Database](how-to-install-a-database.md).</span></span> <span data-ttu-id="c562f-120">Nachdem Sie die Datenbank installiert haben, fahren Sie mit Schritt 13 fort.</span><span class="sxs-lookup"><span data-stu-id="c562f-120">After installing the database, continue with step 13.</span></span>

     

9.  <span data-ttu-id="c562f-121">Wählen Sie auf der Seite **Daten Bank** Servertyp einen Datenbanktyp aus der Liste aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c562f-121">On the **Database Server Type** page, select a database type from the list, and then click **Next**.</span></span>

10. <span data-ttu-id="c562f-122">Wählen Sie auf der Seite **Speicherort des Datenbankservers** in der Liste der verfügbaren Server einen Datenbankserver aus, oder fügen Sie einen Server hinzu, indem Sie das Kontrollkästchen **folgenden Hostnamen verwenden** und Informationen in die Felder **Server Name** und **Port Nummer** eingeben und dann auf **weiter**klicken.</span><span class="sxs-lookup"><span data-stu-id="c562f-122">On the **Database Server Location** page, select a database server from the list of available servers or add a server by selecting the **Use the following host name** check box and entering information in the **Server Name** and **Port Number** boxes, and then click **Next**.</span></span>

11. <span data-ttu-id="c562f-123">Wählen Sie auf der Seite **Datenbank auswählen** die gewünschte Datenbank aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c562f-123">On the **Select Database** page, select the database you want, and then click **Next**.</span></span>

12. <span data-ttu-id="c562f-124">Geben Sie auf der Seite **Datenbankbenutzer Konfiguration** die Anmeldeinformationen ein, die der Verwaltungs-Webdienst für den Zugriff auf den Datenspeicher verwenden wird, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c562f-124">On the **Database User Configuration** page, enter the credentials that the Management Web Service will use to access the data store, and then click **Next**.</span></span>

13. <span data-ttu-id="c562f-125">Klicken Sie auf der Seite **bereit zum Ändern des Programms** auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="c562f-125">On the **Ready to Modify the Program** page, click **Install**.</span></span>

    <span data-ttu-id="c562f-126">**Hinweis**  Wenn es sich um die erste Komponente handelt, die Sie installieren, wird die Seite " **bereit zum Installieren des Programms** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c562f-126">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="c562f-127">Klicken Sie auf der Seite auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="c562f-127">On the page, click **Install**.</span></span>

     

14. <span data-ttu-id="c562f-128">Klicken Sie auf der Seite **fertig gestellt des Installations-Assistenten** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="c562f-128">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

## <span data-ttu-id="c562f-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c562f-129">Related topics</span></span>


[<span data-ttu-id="c562f-130">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="c562f-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





