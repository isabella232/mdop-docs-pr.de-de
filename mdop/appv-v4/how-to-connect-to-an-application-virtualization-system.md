---
title: So stellen Sie eine Verbindung mit einem Application Virtualization System her
description: So stellen Sie eine Verbindung mit einem Application Virtualization System her
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807216"
---
# <span data-ttu-id="4bf2a-103">So stellen Sie eine Verbindung mit einem Application Virtualization System her</span><span class="sxs-lookup"><span data-stu-id="4bf2a-103">How to Connect to an Application Virtualization System</span></span>


<span data-ttu-id="4bf2a-104">Sie müssen die Application Virtualization Server-Verwaltungskonsole mit einem Application Virtualization System verbinden, bevor Sie die Verwaltungskonsole zum Verwalten von Anwendungen, Dateitypzuordnungen, Paketen, Anwendungslizenzen, Server Gruppen, Anbieterrichtlinien und Administratoren verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-104">You must connect the Application Virtualization Server Management Console to an Application Virtualization System before you can use the management console to manage applications, file type associations, packages, application licenses, server groups, provider policies and administrators.</span></span> <span data-ttu-id="4bf2a-105">Im folgenden Verfahren werden die Schritte beschrieben, die Sie ausführen müssen, um die Konsole mit einem Application Virtualization System zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-105">The following procedure outlines the steps you must follow to connect the console to an Application Virtualization System.</span></span>

**<span data-ttu-id="4bf2a-106">So stellen Sie eine Verbindung mit einem Application Virtualization System her</span><span class="sxs-lookup"><span data-stu-id="4bf2a-106">To connect to an Application Virtualization System</span></span>**

1. <span data-ttu-id="4bf2a-107">Klicken Sie im **Bereich** Bereich mit der rechten Maustaste auf den Knoten Application Virtualization System, und wählen Sie im Popupmenü die Option mit **Application Virtualization System verbinden** aus.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-107">Right-click the Application Virtualization System node in the **Scope** pane, and select **Connect to Application Virtualization System** from the pop-up menu.</span></span>

   **<span data-ttu-id="4bf2a-108">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4bf2a-108">Note</span></span>**  
   <span data-ttu-id="4bf2a-109">Es gibt drei Komponenten für die Application Virtualization Server-Verwaltung: die Application Virtualization-Verwaltungskonsole, den Verwaltungs-Webdienst und den SQL-Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-109">There are three components to Application Virtualization server management: the Application Virtualization Management Console, the Management Web Service, and the SQL Datastore.</span></span> <span data-ttu-id="4bf2a-110">Wenn diese Komponenten auf verschiedenen physischen Computern verteilt sind, müssen Sie die Sicherheit für die Komponenten für die Kommunikation über das System ordnungsgemäß konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-110">If these components are distributed across different physical machines, you must configure security properly for the components to communicate across the system.</span></span> <span data-ttu-id="4bf2a-111">Weitere Informationen finden Sie in den folgenden Handbüchern und Artikeln:</span><span class="sxs-lookup"><span data-stu-id="4bf2a-111">For more information, see the following manuals and articles:</span></span>

   <span data-ttu-id="4bf2a-112">So [Konfigurieren Sie den Server für die Delegierung als vertrauenswürdig](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span><span class="sxs-lookup"><span data-stu-id="4bf2a-112">[How to Configure the Server to be Trusted for Delegation](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span></span>

   <span data-ttu-id="4bf2a-113">[Leitfaden zur Planung und Bereitstellung für das Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span><span class="sxs-lookup"><span data-stu-id="4bf2a-113">[Planning and Deployment Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span></span>

   <span data-ttu-id="4bf2a-114">[Betriebshandbuch für das Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span><span class="sxs-lookup"><span data-stu-id="4bf2a-114">[Operations Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span></span>

   <span data-ttu-id="4bf2a-115">[Artikel 930472](https://go.microsoft.com/fwlink/?LinkId=114647) in der Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114647)</span><span class="sxs-lookup"><span data-stu-id="4bf2a-115">[Article 930472](https://go.microsoft.com/fwlink/?LinkId=114647) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114647)</span></span>

   <span data-ttu-id="4bf2a-116">[Artikel 930565](https://go.microsoft.com/fwlink/?LinkId=114648) in der Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114648)</span><span class="sxs-lookup"><span data-stu-id="4bf2a-116">[Article 930565](https://go.microsoft.com/fwlink/?LinkId=114648) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114648)</span></span>

     

2. <span data-ttu-id="4bf2a-117">Füllen Sie die Felder im Dialogfeld mit **Application Virtualization System verbinden** aus:</span><span class="sxs-lookup"><span data-stu-id="4bf2a-117">Complete the fields in the **Connect to Application Virtualization System** dialog box:</span></span>

   1. <span data-ttu-id="4bf2a-118">Hostname des **Webdiensts**: Geben Sie den Namen des Application Virtualization Systems ein, mit dem Sie eine Verbindung herstellen möchten, oder geben Sie **localhost** ein, um eine Verbindung mit dem lokalen Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-118">**Web Service Host Name**—Enter the name of the Application Virtualization System to which you want to connect, or enter **localhost** to connect to the local server.</span></span>

   2. <span data-ttu-id="4bf2a-119">**Sichere Verbindung verwenden**– aktivieren Sie dieses Kontrollkästchen, wenn Sie eine Verbindung mit dem Server mit einer sicheren Verbindung herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-119">**Use Secure Connection**—Select this check box if you want to connect to the server with a secure connection.</span></span>

   3. <span data-ttu-id="4bf2a-120">**Port**– geben Sie die Portnummer ein, die Sie für die Verbindung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-120">**Port**—Enter the port number you want to use for the connection.</span></span> <span data-ttu-id="4bf2a-121">**80** ist die standardmäßige Standardportnummer, und **443** ist die Secure-Port-Nummer.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-121">**80** is the default regular port number, and **443** is the secure-port number.</span></span>

   4. <span data-ttu-id="4bf2a-122">**Aktuelles Windows-Konto verwenden**– aktivieren Sie dieses Optionsfeld, um die aktuellen Windows-Kontoanmeldeinformationen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-122">**Use Current Windows Account**—Select this radio button to use the current Windows account credentials.</span></span>

   5. <span data-ttu-id="4bf2a-123">**Windows-Konto angeben**– wählen Sie dieses Optionsfeld aus, wenn Sie eine Verbindung mit dem Server als anderen Benutzer herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-123">**Specify Windows Account**—Select this radio button when you want to connect to the server as a different user.</span></span>

   6. <span data-ttu-id="4bf2a-124">**Name**: Geben Sie den Namen des neuen Benutzers ein, indem Sie entweder das *DOMAIN\\username* -oder das <em> username@Domain-Format verwenden </em> .</span><span class="sxs-lookup"><span data-stu-id="4bf2a-124">**Name**—Enter the name of the new user by using either the *DOMAIN\\username* or the <em>username@domain</em> format.</span></span>

   7. <span data-ttu-id="4bf2a-125">**Kennwort**– geben Sie das Kennwort ein, das dem neuen Benutzer entspricht.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-125">**Password**—Enter the password that corresponds to the new user.</span></span>

3. <span data-ttu-id="4bf2a-126">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bf2a-126">Click **OK**.</span></span>

## <span data-ttu-id="4bf2a-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4bf2a-127">Related topics</span></span>


[<span data-ttu-id="4bf2a-128">So führen Sie Verwaltungsaufgaben in der Application Virtualization Server Management Console durch</span><span class="sxs-lookup"><span data-stu-id="4bf2a-128">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





