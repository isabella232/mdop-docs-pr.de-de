---
title: So erstellen Sie mithilfe der App-V 5.1-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei an
description: So erstellen Sie mithilfe der App-V 5.1-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei an
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805642"
---
# <span data-ttu-id="4d1cc-103">So erstellen Sie mithilfe der App-V 5.1-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei an</span><span class="sxs-lookup"><span data-stu-id="4d1cc-103">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>


<span data-ttu-id="4d1cc-104">Sie können eine dynamische Konfiguration verwenden, um ein App-V 5,1-Paket für einen bestimmten Benutzer anzupassen.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-104">You can use a dynamic configuration to customize an App-V 5.1 package for a specific user.</span></span> <span data-ttu-id="4d1cc-105">Sie müssen jedoch zuerst die Dynamic User Configuration-Datei (XML) oder die dynamische Bereitstellungs Konfigurationsdatei erstellen, bevor Sie die Dateien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="4d1cc-106">Die Erstellung der Datei ist eine erweiterte manuelle Operation.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="4d1cc-107">Allgemeine Informationen zu Dynamic User-Konfigurationsdateien finden Sie unter Informationen [zur dynamischen App-V 5,1-Konfiguration](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="4d1cc-107">For general information about dynamic user configuration files, see, [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

<span data-ttu-id="4d1cc-108">Gehen Sie wie folgt vor, um mithilfe der App-V 5,1-Verwaltungskonsole eine Dynamic User-Konfigurationsdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.1 Management console.</span></span>

**<span data-ttu-id="4d1cc-109">So erstellen Sie eine Dynamic User-Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="4d1cc-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="4d1cc-110">Klicken Sie mit der rechten Maustaste auf den Namen des Pakets, das Sie anzeigen möchten, und wählen Sie **Active Directory-Zugriff bearbeiten** aus, um die Konfiguration anzuzeigen, die einer bestimmten Benutzergruppe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="4d1cc-111">Alternativ können Sie das Paket auswählen und auf **Bearbeiten**klicken.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="4d1cc-112">Wählen Sie mithilfe der Liste der **anzeigen Entitäten mit Access**die Anzeigengruppe aus, die Sie anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="4d1cc-113">Wählen Sie in der Dropdownliste **Benutzerdefiniert** aus, wenn Sie noch nicht ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="4d1cc-114">Der Link " **Bearbeiten** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="4d1cc-115">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-115">Click **Edit**.</span></span> <span data-ttu-id="4d1cc-116">Die der Anzeigengruppe zugewiesene dynamische Benutzerkonfiguration wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="4d1cc-117">Klicken Sie auf **erweitert**, und klicken Sie dann auf **Konfiguration exportieren**.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="4d1cc-118">Geben Sie einen Dateinamen ein, und klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="4d1cc-119">Nun können Sie die Datei bearbeiten, um ein Paket für einen Benutzer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-119">Now you can edit the file to configure a package for a user.</span></span>

    **<span data-ttu-id="4d1cc-120">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4d1cc-120">Note</span></span>**  
    <span data-ttu-id="4d1cc-121">Wenn Sie eine Konfiguration exportieren möchten, während Sie unter Windows Server ausgeführt wird, müssen Sie "IE Enhanced Security Configuration" deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-121">To export a configuration while running on Windows Server, you must disable "IE Enhanced Security Configuration".</span></span> <span data-ttu-id="4d1cc-122">Wenn diese Option aktiviert ist und auf Downloads blockieren eingestellt ist, können Sie nichts vom App-V-Server herunterladen.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-122">If this is enabled and set to block downloads, you cannot download anything from the App-V Server.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="4d1cc-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4d1cc-123">Related topics</span></span>


[<span data-ttu-id="4d1cc-124">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4d1cc-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









