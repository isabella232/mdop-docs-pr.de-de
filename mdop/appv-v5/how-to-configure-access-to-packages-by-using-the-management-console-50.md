---
title: So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete
description: So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete
author: dansimp
ms.assetid: 8f4c91e4-f4e6-48cf-aa94-6085a054e8f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e1f5b51b118dc7b783a4a550e19fd39a61a0ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805714"
---
# <span data-ttu-id="89871-103">So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete</span><span class="sxs-lookup"><span data-stu-id="89871-103">How to Configure Access to Packages by Using the Management Console</span></span>


<span data-ttu-id="89871-104">Bevor Sie ein virtualisiertes App-V 5,0-Paket bereitstellen, müssen Sie die Active Directory-Domänendienste (AD DS)-Sicherheitsgruppen konfigurieren, die für den Zugriff auf und die Ausführung der Anwendungen zugelassen sind.</span><span class="sxs-lookup"><span data-stu-id="89871-104">Before you deploy an App-V 5.0 virtualized package, you must configure the Active Directory Domain Services (AD DS) security groups that will be allowed to access and run the applications.</span></span> <span data-ttu-id="89871-105">Die Sicherheitsgruppen enthalten möglicherweise Computer oder Benutzer.</span><span class="sxs-lookup"><span data-stu-id="89871-105">The security groups may contain computers or users.</span></span> <span data-ttu-id="89871-106">Wenn Sie ein Paket zu einer Computergruppe berechtigen, wird das Paket Global auf allen Computern in der Gruppe veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="89871-106">Entitling a package to a computer group publishes the package globally to all computers in the group.</span></span>

<span data-ttu-id="89871-107">Gehen Sie wie folgt vor, um den Zugriff auf virtualisierte Pakete zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="89871-107">Use the following procedure to configure access to virtualized packages.</span></span>

**<span data-ttu-id="89871-108">So gewähren Sie Zugriff auf ein App-V 5,0-Paket</span><span class="sxs-lookup"><span data-stu-id="89871-108">To grant access to an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="89871-109">Suchen Sie das Paket, das Sie konfigurieren möchten:</span><span class="sxs-lookup"><span data-stu-id="89871-109">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="89871-110">Öffnen Sie die App-V 5,0-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="89871-110">Open the App-V 5.0 Management console.</span></span>

    2.  <span data-ttu-id="89871-111">Klicken Sie zum Anzeigen der Seite **anzeigen Zugriff** mit der rechten Maustaste auf das zu konfigurierbare Paket, und wählen Sie **Active Directory-Zugriff bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="89871-111">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="89871-112">Alternativ können Sie das Paket auswählen und im Bereich **anzeigen Zugriff** auf **Bearbeiten** klicken.</span><span class="sxs-lookup"><span data-stu-id="89871-112">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="89871-113">Bereitstelleneiner Sicherheitsgruppe für das Paket:</span><span class="sxs-lookup"><span data-stu-id="89871-113">Provision a security group for the package:</span></span>

    1.  <span data-ttu-id="89871-114">Wechseln Sie zur Seite **gültige Active Directory-Namen und Grant-Zugriff suchen** .</span><span class="sxs-lookup"><span data-stu-id="89871-114">Go to the **FIND VALID ACTIVE DIRECTORY NAMES AND GRANT ACCESS** page.</span></span>

    2.  <span data-ttu-id="89871-115">**mydomain**  \\  **groupname**Geben Sie den Namen oder einen Teil des Namens eines Active Directory-Gruppenobjekts ein, und klicken Sie auf **überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="89871-115">Using the format **mydomain** \\ **groupname**, type the name or part of the name of an Active Directory group object, and click **Check**.</span></span>

        <span data-ttu-id="89871-116">**Hinweis**  Stellen Sie sicher, dass Sie einen zugehörigen Domänennamen für die Gruppe angeben, nach der Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="89871-116">**Note** Ensure that you provide an associated domain name for the group that you are searching for.</span></span>

         

3.  <span data-ttu-id="89871-117">Wenn Sie dem Paketzugriff gewähren möchten, wählen Sie die gewünschte Gruppe aus, und klicken Sie auf **Zugriff gewähren**.</span><span class="sxs-lookup"><span data-stu-id="89871-117">To grant access to the package, select the desired group and click **Grant Access**.</span></span> <span data-ttu-id="89871-118">Die neu hinzugefügte Gruppe wird im Bereich " **anzeigen Entitäten mit Access** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89871-118">The newly added group is displayed in the **AD ENTITIES WITH ACCESS** pane.</span></span>

4.  

    <span data-ttu-id="89871-119">Wenn Sie die Standardkonfigurationseinstellungen übernehmen und die Seite **anzeigen Zugriff** schließen möchten, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="89871-119">To accept the default configuration settings and close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="89871-120">Wenn Sie Konfigurationen für eine bestimmte Gruppe anpassen möchten, klicken Sie auf die Dropdownliste **zugewiesene Konfigurationen** , und wählen Sie **Benutzerdefiniert**aus.</span><span class="sxs-lookup"><span data-stu-id="89871-120">To customize configurations for a specific group, click the **ASSIGNED CONFIGURATIONS** drop-down and select **Custom**.</span></span> <span data-ttu-id="89871-121">Klicken Sie zum Konfigurieren der benutzerdefinierten Konfigurationen auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="89871-121">To configure the custom configurations, click **EDIT**.</span></span> <span data-ttu-id="89871-122">Nachdem Sie Access gewährt haben, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="89871-122">After you grant access, click **Close**.</span></span>

**<span data-ttu-id="89871-123">So entfernen Sie den Zugriff auf ein App-V 5,0-Paket</span><span class="sxs-lookup"><span data-stu-id="89871-123">To remove access to an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="89871-124">Suchen Sie das Paket, das Sie konfigurieren möchten:</span><span class="sxs-lookup"><span data-stu-id="89871-124">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="89871-125">Öffnen Sie die App-V 5,0-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="89871-125">Open the App-V 5.0 Management console.</span></span>

    2.  <span data-ttu-id="89871-126">Klicken Sie zum Anzeigen der Seite **anzeigen Zugriff** mit der rechten Maustaste auf das zu konfigurierbare Paket, und wählen Sie **Active Directory-Zugriff bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="89871-126">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="89871-127">Alternativ können Sie das Paket auswählen und im Bereich **anzeigen Zugriff** auf **Bearbeiten** klicken.</span><span class="sxs-lookup"><span data-stu-id="89871-127">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="89871-128">Wählen Sie die Gruppe aus, die Sie entfernen möchten, und klicken Sie auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="89871-128">Select the group you want to remove, and click **DELETE**.</span></span>

3.  <span data-ttu-id="89871-129">Klicken Sie auf **Schließen**, um die Seite **anzeigen Zugriff** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="89871-129">To close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="89871-130">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="89871-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="89871-131">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="89871-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="89871-132">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="89871-132">Got an App-V issue?</span></span>** <span data-ttu-id="89871-133">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="89871-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="89871-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="89871-134">Related topics</span></span>


[<span data-ttu-id="89871-135">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89871-135">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





