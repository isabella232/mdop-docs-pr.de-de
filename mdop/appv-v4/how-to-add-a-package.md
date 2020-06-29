---
title: So fügen Sie ein Paket hinzu
description: So fügen Sie ein Paket hinzu
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808731"
---
# <span data-ttu-id="e36f0-103">So fügen Sie ein Paket hinzu</span><span class="sxs-lookup"><span data-stu-id="e36f0-103">How to Add a Package</span></span>


<span data-ttu-id="e36f0-104">Sie können ein Paket aus der Application Virtualization Server-Verwaltungskonsole wie folgt hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="e36f0-104">You can add a package from the Application Virtualization Server Management Console in the following ways:</span></span>

-   <span data-ttu-id="e36f0-105">Importieren Sie eine Anwendung, die das Paket automatisch im Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="e36f0-105">Import an application, which creates the package automatically in the process.</span></span>

-   <span data-ttu-id="e36f0-106">Manuelles Hinzufügen eines Pakets</span><span class="sxs-lookup"><span data-stu-id="e36f0-106">Add a package manually.</span></span>

<span data-ttu-id="e36f0-107">Es wird empfohlen, dass Sie Anwendungen importieren, anstatt Sie manuell hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e36f0-107">It is recommended that you import applications instead of adding them manually.</span></span> <span data-ttu-id="e36f0-108">Weitere Informationen zum Importieren von Anwendungen finden Sie unter [so wird es gemacht: Importieren einer Anwendung](how-to-import-an-applicationserver.md).</span><span class="sxs-lookup"><span data-stu-id="e36f0-108">For more information about importing applications, see [How to Import an Application](how-to-import-an-applicationserver.md).</span></span>

**<span data-ttu-id="e36f0-109">So fügen Sie ein Paket manuell hinzu</span><span class="sxs-lookup"><span data-stu-id="e36f0-109">To add a package manually</span></span>**

1.  <span data-ttu-id="e36f0-110">Klicken Sie in der Application Virtualization Server-Verwaltungskonsole im linken Bereich mit der rechten Maustaste auf den Knoten **Pakete** , und wählen Sie **neues Paket**aus.</span><span class="sxs-lookup"><span data-stu-id="e36f0-110">In the Application Virtualization Server Management Console, right-click the **Packages** node in the left pane and choose **New Package**.</span></span>

2.  <span data-ttu-id="e36f0-111">Geben Sie im Dialogfeld **neues Paket** einen Namen in das Feld **Paketname** ein.</span><span class="sxs-lookup"><span data-stu-id="e36f0-111">In the **New Package** dialog box, type a name in the **Package Name** field.</span></span>

3.  <span data-ttu-id="e36f0-112">Suchen oder geben Sie im Feld **Vollständiger Pfad für Paketdatei** einen Pfadnamen ein.</span><span class="sxs-lookup"><span data-stu-id="e36f0-112">Browse for or type a path name in the **Full path for package file** field.</span></span> <span data-ttu-id="e36f0-113">Hierbei muss es sich um eine SFT-Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="e36f0-113">This must be an SFT file.</span></span>

    <span data-ttu-id="e36f0-114">**Hinweis**  Wenn Sie die SFT-Datei durchsuchen, ersetzen Sie den lokalen Pfad (wie c:\\Programme Files\\User\ _Apps \\virtual\ _App \ _Server \\content) durch den statischen Hostnamen oder die IP-Adresse des Servers.</span><span class="sxs-lookup"><span data-stu-id="e36f0-114">**Note** If you browse to the SFT file, replace the local path (such as C:\\Program Files\\User\_Apps\\Virtual\_App\_Server\\content) with the server's static host name or IP address.</span></span> <span data-ttu-id="e36f0-115">Bei Verwendung der Variablen *% SFT \ _SOFTGRIDSERVER%* ist die Konfiguration pro Clientcomputer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e36f0-115">Using the variable *%SFT\_SOFTGRIDSERVER%* requires per-client computer configuration.</span></span>

    <span data-ttu-id="e36f0-116">In Dialogfeldern, die auf virtuelle Anwendungsserver verweisen, müssen Sie einen Netzwerkspeicherort verwenden, beispielsweise den statischen Hostnamen oder die IP-Adresse des Servers, auf den Ihre Benutzer zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="e36f0-116">In dialog boxes that refer to Virtual Application Servers, you must use a network location, such as the server's static host name or IP address, that your users can access.</span></span> <span data-ttu-id="e36f0-117">Die OSD-Datei (Open Software Descriptor) der Anwendung kann die Platzhaltervariable *% SFT \ _SOFTGRIDSERER%* durch den statischen Hostnamen oder die IP-Adresse des Servers ersetzen.</span><span class="sxs-lookup"><span data-stu-id="e36f0-117">The application's Open Software Descriptor (OSD) file can replace the placeholder variable *%SFT\_SOFTGRIDSERER%* with the server's static host name or IP address.</span></span> <span data-ttu-id="e36f0-118">Wenn Sie die Platzhaltervariable beibehalten, müssen Sie diese Variable auf jedem Clientcomputer, der auf diesen Server zugreifen soll, festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e36f0-118">If you leave the placeholder variable, you must set this variable on each client computer that will access that server.</span></span> <span data-ttu-id="e36f0-119">Setzen Sie einen Benutzer oder eine System Variable auf jedem Computer für SFT \ _SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="e36f0-119">Set a User or System variable on each computer for SFT\_SOFTGRIDSERVER.</span></span> <span data-ttu-id="e36f0-120">Der Variablenwert muss der statische Hostname oder die IP-Adresse des Servers sein.</span><span class="sxs-lookup"><span data-stu-id="e36f0-120">The variable value must be the server's static host name or IP address.</span></span> <span data-ttu-id="e36f0-121">Wenn Sie eine Variable festzulegen, beenden Sie die Client Sitzung, melden Sie sich bei Microsoft Windows ab und wieder an, und starten Sie die Sitzung auf jedem Computer neu, auf dem eine Sitzung ausgeführt wurde und für die die Variable festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="e36f0-121">If you set a variable, exit the Client session, log out of and back into Microsoft Windows, and then restart the session on each computer that had a session running and had the variable set.</span></span>

     

4.  <span data-ttu-id="e36f0-122">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="e36f0-122">Click **Next**.</span></span>

5.  <span data-ttu-id="e36f0-123">Im Dialogfeld " **Zusammenfassung** " wird der Speicherort der Datei angezeigt, und Sie werden aufgefordert, die Datei an den Speicherort zu kopieren, wenn dies noch nicht geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="e36f0-123">The **Summary** dialog box shows the file location and prompts you to copy the file to the location if you have not already done so.</span></span> <span data-ttu-id="e36f0-124">Klicken Sie auf **Fertig stellen** , nachdem Sie die Informationen überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="e36f0-124">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="e36f0-125">**Hinweis**  Wenn Sie Anwendungen auf einem Remoteserver verwalten, geben Sie im nächsten Dialogfeld nur den Pfad der Datei relativ zum Inhaltsstamm des Servers ein.</span><span class="sxs-lookup"><span data-stu-id="e36f0-125">**Note** If you are managing applications on a remote server, in the next dialog box, type only the path of the file relative to the server's content root.</span></span>

     

## <span data-ttu-id="e36f0-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e36f0-126">Related topics</span></span>


[<span data-ttu-id="e36f0-127">So importieren Sie eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="e36f0-127">How to Import an Application</span></span>](how-to-import-an-applicationserver.md)

[<span data-ttu-id="e36f0-128">So verwalten Sie die Pakete in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="e36f0-128">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





