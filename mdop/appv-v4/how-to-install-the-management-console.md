---
title: So installieren Sie die Verwaltungskonsole
description: So installieren Sie die Verwaltungskonsole
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807052"
---
# <span data-ttu-id="4c4f4-103">So installieren Sie die Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="4c4f4-103">How to Install the Management Console</span></span>


<span data-ttu-id="4c4f4-104">Sie können das folgende Verfahren zum Installieren der Application Virtualization-Verwaltungskonsole auf einem Zielcomputer im Netzwerk verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-104">You can use the following procedure to install the Application Virtualization Management Console on a target computer on the network.</span></span> <span data-ttu-id="4c4f4-105">Sie müssen ein Netzwerkkonto verwenden, das über Administratorrechte auf dem Zielcomputer verfügt.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-105">You must use a network account that has administrator privileges on the target computer.</span></span> <span data-ttu-id="4c4f4-106">Sie können die Konsole zum Konfigurieren und Verwalten der Application Virtualization System-Plattform verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-106">You can use the console to configure and manage the Application Virtualization System Platform.</span></span>

<span data-ttu-id="4c4f4-107">Bevor Sie diese Schritte ausführen können, müssen Sie den Application Virtualization Management Web Service auf diesem oder einem anderen Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-107">Before you can complete this procedure, you must install the Application Virtualization Management Web Service on this or a different computer.</span></span> <span data-ttu-id="4c4f4-108">Mit dem Verwaltungs-Web-Service können Sie auf den Datenspeicher und den Domänencontroller zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-108">The Management Web Service allows you to access the data store and the domain controller.</span></span> <span data-ttu-id="4c4f4-109">Weitere Informationen zum Installieren des Webdiensts finden Sie unter so wird es [gemacht: Installieren des Verwaltungs-Webdiensts](how-to-install-the-management-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="4c4f4-109">For more information about installing the Web service, see [How to Install the Management Web Service](how-to-install-the-management-web-service.md).</span></span>

**<span data-ttu-id="4c4f4-110">So installieren Sie die Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="4c4f4-110">To install the Management Console</span></span>**

1.  <span data-ttu-id="4c4f4-111">Vergewissern Sie sich, dass auf dem Zielcomputer keine vorherigen Versionen der Verwaltungskonsole installiert sind.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-111">Verify that no previous versions of the Management Console are installed on the target computer.</span></span>

2.  <span data-ttu-id="4c4f4-112">Navigieren Sie zum Speicherort des Application Virtualization System-Setupprogramms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-112">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="4c4f4-113">Klicken Sie auf der **Seite Willkommen**auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-113">On the **Welcome Page**, click **Next**.</span></span>

4.  <span data-ttu-id="4c4f4-114">Wählen Sie auf der Seite **Lizenzvertrag** die Option **Ich akzeptiere die Lizenzbedingungen**aus, um den Lizenzvertrag anzunehmen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-114">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="4c4f4-115">Geben Sie auf der Seite **Registrierungsinformationen** den **Benutzernamen** und die **Organisations** Informationen an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-115">On the **Registration Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

6.  <span data-ttu-id="4c4f4-116">Klicken Sie auf der Seite **Setuptyp** auf **Benutzerdefiniert** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-116">On the **Setup Type** page, click **Custom** and then click **Next**.</span></span>

7.  <span data-ttu-id="4c4f4-117">Deaktivieren Sie auf der Seite **benutzerdefinierte Einrichtung** die Option Alle Komponenten des Application Virtualization System-Ausnahme **Management Console**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-117">On the **Custom Setup** page, deselect all Application Virtualization System components except **Management Console**, and then click **Next**.</span></span>

    <span data-ttu-id="4c4f4-118">**Hinweis**  Wenn eine Komponente bereits auf dem Computer installiert ist, wird Sie automatisch deinstalliert, indem Sie Sie auf dem Bildschirm "benutzerdefiniertes Setup" aufheben.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-118">**Note** If a component is already installed on the computer, by deselecting it on the Custom Setup screen, it will automatically be uninstalled.</span></span>

     

8.  <span data-ttu-id="4c4f4-119">Klicken Sie auf dem Bildschirm **bereit zum Ändern des Programms** auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-119">On the **Ready to Modify the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="4c4f4-120">**Hinweis**  Wenn es sich um die erste Komponente handelt, die Sie installieren, wird die Seite " **bereit zum Installieren des Programms** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-120">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="4c4f4-121">Klicken Sie auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-121">To start the installation, click **Install**.</span></span>

     

9.  <span data-ttu-id="4c4f4-122">Klicken Sie im Bildschirm **Installationsassistent abgeschlossen** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-122">On the **Installation Wizard Completed** screen, click **Finish**.</span></span> <span data-ttu-id="4c4f4-123">Klicken Sie auf **OK** , um den Computer neu zu starten und die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-123">Click **Okay** to restart the computer and complete the installation.</span></span>

10. <span data-ttu-id="4c4f4-124">Doppelklicken Sie in der Windows-Systemsteuerung auf **Verwaltungs Tools** , und klicken Sie dann auf **Application Virtualization Management Console** , um die Verwaltungskonsole anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-124">In the Windows Control Panel, double-click **Administrative Tools** and then click **Application Virtualization Management Console** to display the Management Console.</span></span>

11. <span data-ttu-id="4c4f4-125">Klicken Sie auf das Symbol **verbinden** , oder klicken Sie mit der rechten Maustaste auf den Container **Application Virtualization Systems** , und klicken Sie dann auf **mit Application Virtualization System verbinden**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-125">Click the **Connect** icon, or right-click the **Application Virtualization Systems** container, and then click **Connect to Application Virtualization System**.</span></span>

12. <span data-ttu-id="4c4f4-126">Geben Sie auf dem Bildschirm mit **Application Virtualization System verbinden** den Hostnamen und den Port des Management Web Service-Computers ein, ändern Sie bei Bedarf die Sicherheitsinformationen und Anmeldeinformationen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-126">On the **Connect to Application Virtualization System** screen, enter the host name and port of the Management Web Service computer, change the security information and login credentials if necessary, and then click **OK**.</span></span>

13. <span data-ttu-id="4c4f4-127">Nachdem Sie eine Verbindung mit dem Management Web Service-Computer hergestellt haben, klicken Sie im Menü **Konsole** auf **Datei** , und klicken Sie dann auf **Beenden**.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-127">After connecting to the Management Web Service computer, click **File** on the **Console** menu, and then click **Exit**.</span></span> <span data-ttu-id="4c4f4-128">Klicken Sie auf **Ja** , um die Konsoleneinstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-128">Click **Yes** to save console settings.</span></span>

## <span data-ttu-id="4c4f4-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4c4f4-129">Related topics</span></span>


[<span data-ttu-id="4c4f4-130">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="4c4f4-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





