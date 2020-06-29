---
title: Ändern Sie den Port, den der AGPM-Dienst überwacht
description: Ändern Sie den Port, den der AGPM-Dienst überwacht
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808327"
---
# <span data-ttu-id="8d343-103">Ändern Sie den Port, den der AGPM-Dienst überwacht</span><span class="sxs-lookup"><span data-stu-id="8d343-103">Modify the Port on Which the AGPM Service Listens</span></span>


<span data-ttu-id="8d343-104">Der AGPM-Dienst ist ein Windows-Dienst, der als Sicherheitsproxy fungiert und den Clientzugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivierungs-und Produktionsumgebung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8d343-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="8d343-105">Standardmäßig überwacht der AGPM-Dienst Port 4600.</span><span class="sxs-lookup"><span data-stu-id="8d343-105">By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="8d343-106">Sie können diesen Port ändern, indem Sie die erweiterte Archivindexdatei für die Gruppenrichtlinienverwaltung (AGPM) für jedes Archiv ändern.</span><span class="sxs-lookup"><span data-stu-id="8d343-106">You can change this port by modifying the Advanced Group Policy Management (AGPM) archive index file for each archive.</span></span>

<span data-ttu-id="8d343-107">**Hinweis**  Bevor Sie den Port ändern, auf dem der AGPM-Dienst lauscht, wird empfohlen, die AGPM Archive-Indexdatei (gpostate.xml) zu sichern.</span><span class="sxs-lookup"><span data-stu-id="8d343-107">**Note** Before modifying the port on which the AGPM Service listens, it is recommended that you back up the AGPM archive index file (gpostate.xml).</span></span> <span data-ttu-id="8d343-108">Diese Datei befindet sich in dem Ordner, der während der Installation des erweiterten Gruppenrichtlinien-Verwaltungsservers als Archivierungspfad eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8d343-108">This file is located in the folder entered as the archive path during the installation of Advanced Group Policy Management - Server.</span></span> <span data-ttu-id="8d343-109">Standardmäßig ist dieser Speicherort dieser Datei% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml auf dem AGPM-Server.</span><span class="sxs-lookup"><span data-stu-id="8d343-109">By default, this location of this file is %CommonAppData%\\Microsoft\\AGPM\\gpostate.xml on the AGPM Server.</span></span> <span data-ttu-id="8d343-110">Wenn Sie nicht wissen, auf welchem Computer das Archiv gehostet wird, können Sie das Verfahren zum Ändern des Archiv Pfads zum Anzeigen des aktuellen Archiv Pfads ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d343-110">If you do not know which computer hosts the archive, you can follow the procedure for modifying the archive path to display the current archive path.</span></span> <span data-ttu-id="8d343-111">Weitere Informationen finden Sie unter [Ändern des Archiv Pfads](modify-the-archive-path.md).</span><span class="sxs-lookup"><span data-stu-id="8d343-111">For more information, see [Modify the Archive Path](modify-the-archive-path.md).</span></span>

 

<span data-ttu-id="8d343-112">Ein Benutzerkonto mit Zugriff auf den AGPM-Server (der Computer, auf dem der AGPM-Dienst installiert ist) und die Archivindexdatei sind erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8d343-112">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) and the archive index file is required to complete this procedure.</span></span>

**<span data-ttu-id="8d343-113">So ändern Sie den Port, den der AGPM-Dienst überwacht</span><span class="sxs-lookup"><span data-stu-id="8d343-113">To modify the port on which the AGPM Service listens</span></span>**

1.  <span data-ttu-id="8d343-114">Öffnen Sie auf dem Computer, der das Archiv hostet, die Archivindexdatei (gpostate.xml) in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="8d343-114">On the computer hosting the archive, open the archive index file (gpostate.xml) in a text editor.</span></span>

2.  <span data-ttu-id="8d343-115">Suchen Sie in der Datei nach **AGPM: Port = "4600"**.</span><span class="sxs-lookup"><span data-stu-id="8d343-115">In the file, search for **agpm:port="4600"**.</span></span>

3.  <span data-ttu-id="8d343-116">Ersetzen Sie **4600** durch den Port, den der AGPM-Dienst abhören soll; Speichern und schließen Sie dann die Datei.</span><span class="sxs-lookup"><span data-stu-id="8d343-116">Replace **4600** with the port on which the AGPM Service should listen; then, save and close the file.</span></span>

4.  <span data-ttu-id="8d343-117">Starten Sie auf dem AGPM-Server den AGPM-Dienst neu.</span><span class="sxs-lookup"><span data-stu-id="8d343-117">On the AGPM Server, restart the AGPM Service.</span></span> <span data-ttu-id="8d343-118">(Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service.md).)</span><span class="sxs-lookup"><span data-stu-id="8d343-118">(For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).)</span></span>

5.  <span data-ttu-id="8d343-119">Ändern Sie den Port in der AGPM-Server Verbindung für jeden Gruppenrichtlinienadministrator.</span><span class="sxs-lookup"><span data-stu-id="8d343-119">Modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="8d343-120">(Weitere Informationen finden Sie unter [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection.md).)</span><span class="sxs-lookup"><span data-stu-id="8d343-120">(For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).)</span></span>

6.  <span data-ttu-id="8d343-121">Wiederholen Sie diesen Vorgang für jeden Archivierungs-und AGPM-Server.</span><span class="sxs-lookup"><span data-stu-id="8d343-121">Repeat for each archive and AGPM Server.</span></span>

### <span data-ttu-id="8d343-122">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="8d343-122">Additional references</span></span>

-   [<span data-ttu-id="8d343-123">Verwalten des AGPM-Dienstes</span><span class="sxs-lookup"><span data-stu-id="8d343-123">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





