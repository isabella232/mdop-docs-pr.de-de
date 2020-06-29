---
title: So erstellen Sie mithilfe der App-V 5.0-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei
description: So erstellen Sie mithilfe der App-V 5.0-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805645"
---
# <span data-ttu-id="3453b-103">So erstellen Sie mithilfe der App-V 5.0-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="3453b-103">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>


<span data-ttu-id="3453b-104">Sie können eine dynamische Konfiguration verwenden, um ein App-V 5,0-Paket für einen bestimmten Benutzer anzupassen.</span><span class="sxs-lookup"><span data-stu-id="3453b-104">You can use a dynamic configuration to customize an App-V 5.0 package for a specific user.</span></span> <span data-ttu-id="3453b-105">Sie müssen jedoch zuerst die Dynamic User Configuration-Datei (XML) oder die dynamische Bereitstellungs Konfigurationsdatei erstellen, bevor Sie die Dateien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="3453b-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="3453b-106">Die Erstellung der Datei ist eine erweiterte manuelle Operation.</span><span class="sxs-lookup"><span data-stu-id="3453b-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="3453b-107">Allgemeine Informationen zu Dynamic User-Konfigurationsdateien finden Sie unter Informationen [zur dynamischen App-V 5,0-Konfiguration](about-app-v-50-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="3453b-107">For general information about dynamic user configuration files, see, [About App-V 5.0 Dynamic Configuration](about-app-v-50-dynamic-configuration.md).</span></span>

<span data-ttu-id="3453b-108">Gehen Sie wie folgt vor, um mithilfe der App-V 5,0-Verwaltungskonsole eine Dynamic User-Konfigurationsdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3453b-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.0 Management console.</span></span>

**<span data-ttu-id="3453b-109">So erstellen Sie eine Dynamic User-Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="3453b-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="3453b-110">Klicken Sie mit der rechten Maustaste auf den Namen des Pakets, das Sie anzeigen möchten, und wählen Sie **Active Directory-Zugriff bearbeiten** aus, um die Konfiguration anzuzeigen, die einer bestimmten Benutzergruppe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3453b-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="3453b-111">Alternativ können Sie das Paket auswählen und auf **Bearbeiten**klicken.</span><span class="sxs-lookup"><span data-stu-id="3453b-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="3453b-112">Wählen Sie mithilfe der Liste der **anzeigen Entitäten mit Access**die Anzeigengruppe aus, die Sie anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="3453b-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="3453b-113">Wählen Sie in der Dropdownliste **Benutzerdefiniert** aus, wenn Sie noch nicht ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="3453b-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="3453b-114">Der Link " **Bearbeiten** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3453b-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="3453b-115">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="3453b-115">Click **Edit**.</span></span> <span data-ttu-id="3453b-116">Die der Anzeigengruppe zugewiesene dynamische Benutzerkonfiguration wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3453b-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="3453b-117">Klicken Sie auf **erweitert**, und klicken Sie dann auf **Konfiguration exportieren**.</span><span class="sxs-lookup"><span data-stu-id="3453b-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="3453b-118">Geben Sie einen Dateinamen ein, und klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="3453b-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="3453b-119">Nun können Sie die Datei bearbeiten, um ein Paket für einen Benutzer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3453b-119">Now you can edit the file to configure a package for a user.</span></span>

    <span data-ttu-id="3453b-120">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="3453b-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="3453b-121">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="3453b-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="3453b-122">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="3453b-122">Got an App-V issue?</span></span>** <span data-ttu-id="3453b-123">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="3453b-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="3453b-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3453b-124">Related topics</span></span>


[<span data-ttu-id="3453b-125">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3453b-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





