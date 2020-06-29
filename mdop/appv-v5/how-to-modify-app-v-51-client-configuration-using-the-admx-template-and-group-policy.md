---
title: Ändern der App-V 5.1-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie
description: Ändern der App-V 5.1-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie
author: dansimp
ms.assetid: 0d9cf13a-b29c-4c87-a776-15fea34027dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 18363b4fb904d995862ac30634be1350c972d918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805267"
---
# <span data-ttu-id="2b6d9-103">Ändern der App-V 5.1-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="2b6d9-103">How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy</span></span>


<span data-ttu-id="2b6d9-104">Verwenden Sie die Microsoft Application Virtualization (app-v) 5,1 ADMX-Vorlage, um App-v 5,1-Clienteinstellungen mithilfe der ADMX-Vorlage und der Gruppenrichtlinie zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-104">Use the Microsoft Application Virtualization (App-V) 5.1 ADMX template to configure App-V 5.1 client settings using the ADMX Template and Group Policy.</span></span>

**<span data-ttu-id="2b6d9-105">So ändern Sie die App-V 5,1-Clientkonfiguration mithilfe von Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="2b6d9-105">To modify App-V 5.1 client configuration using Group Policy</span></span>**

1.  <span data-ttu-id="2b6d9-106">Wenn Sie die APP-v 5,1-Clientkonfiguration ändern möchten, suchen Sie die **ADMXTemplate** -Dateien, die in App-v 5,1 zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-106">To modify the App-V 5.1 client configuration, locate the **ADMXTemplate** files that are available with App-V 5.1.</span></span>

    <span data-ttu-id="2b6d9-107">**Hinweis**  Verwenden Sie den folgenden Link zum Herunterladen der App-V 5,1 **ADMX-Vorlagen**: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .</span><span class="sxs-lookup"><span data-stu-id="2b6d9-107">**Note** Use the following link to download the App-V 5.1 **ADMX Templates**: <https://go.microsoft.com/fwlink/p/?LinkId=393941>.</span></span>

     

2.  <span data-ttu-id="2b6d9-108">Kopieren Sie die Datei "template **. ADMX** " auf dem Computer, auf dem Sie Gruppenrichtlinien verwalten, in der Regel dem Domänencontroller, in das folgende Verzeichnis: \*\* &lt; Installationslaufwerk &gt; \ \ Windows \ \ PolicyDefinitions\*\*.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-108">On the computer where you manage group Policy, typically the domain controller, copy the template **.admx** file to the following directory: **&lt;Installation Drive&gt; \\ Windows \\ PolicyDefinitions**.</span></span>

    <span data-ttu-id="2b6d9-109">Kopieren Sie dann auf demselben Computer die **ADML** -Datei in das folgende Verzeichnis: \*\* &lt; InstallationDrive &gt; \ \ Windows \ \ PolicyDefinitions \ \ en-US\*\*.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-109">Next, on the same computer, copy the **.adml** file to the following directory: **&lt;InstallationDrive&gt; \\ Windows \\ PolicyDefinitions \\ en-US**.</span></span>

3.  <span data-ttu-id="2b6d9-110">Nachdem Sie die Dateien kopiert haben, öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole, um die Richtlinien zu ändern, die ihren App-v 5,1-Clients zugeordnet sind, navigieren Sie zu den **Computer Konfigurations**  /  **Richtlinien**  /  **Administrative Vorlagen**  /  **System**  /  **App-V**.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-110">After you have copied the files open the Group Policy Management Console, to modify the policies associated with your App-V 5.1 clients browse to **Computer Configuration** / **Policies** / **Administrative Templates** / **System** / **App-V**.</span></span>

    <span data-ttu-id="2b6d9-111">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="2b6d9-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2b6d9-112">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2b6d9-113">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="2b6d9-113">Got an App-V issue?</span></span>** <span data-ttu-id="2b6d9-114">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2b6d9-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2b6d9-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2b6d9-115">Related topics</span></span>


[<span data-ttu-id="2b6d9-116">Bereitstellen von App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2b6d9-116">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="2b6d9-117">Informationen über Clientkonfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="2b6d9-117">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

 

 





