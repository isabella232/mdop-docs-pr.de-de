---
title: So fügen Sie URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich hinzu bzw. entfernen Sie sie
description: So fügen Sie URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich hinzu bzw. entfernen Sie sie
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811758"
---
# <span data-ttu-id="c6649-103">So fügen Sie URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich hinzu bzw. entfernen Sie sie</span><span class="sxs-lookup"><span data-stu-id="c6649-103">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>


<span data-ttu-id="c6649-104">Zum Bearbeiten von URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich empfehlen wir, die Systemregistrierung mithilfe von Gruppenrichtlinien zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c6649-104">To edit URL redirection information in a deployed MED-V workspace, we recommend that you update the system registry by using Group Policy.</span></span> <span data-ttu-id="c6649-105">Obwohl wir dies nicht empfehlen, können Sie den MED-V-Arbeitsbereich auch mit den aktualisierten URL-Umleitungsinformationen neu erstellen und erneut bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c6649-105">Although we do not recommend it, you can also rebuild and redeploy the MED-V workspace with the updated URL redirection information.</span></span>

<span data-ttu-id="c6649-106">Der Registrierungsschlüssel befindet sich normalerweise unter:</span><span class="sxs-lookup"><span data-stu-id="c6649-106">The registry key is usually located at:</span></span>

<span data-ttu-id="c6649-107">Computer\\HKEY\ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\userexperience</span><span class="sxs-lookup"><span data-stu-id="c6649-107">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="c6649-108">Der folgende mehrteilige Zeichenfolgenwert muss vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="c6649-108">The following multi-string value must be present:</span></span> `RedirectUrls`

<span data-ttu-id="c6649-109">Die Wertdaten für `RedirectUrls` ist eine Liste aller URLs, die Sie bei der Erstellung des Med-v-Arbeitsbereichs Pakets mithilfe des **Med-v-Arbeitsbereichs Pakets**für die Umleitung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="c6649-109">The value data for `RedirectUrls` is a list of all of the URLs that you specified for redirection when you built the MED-V workspace package by using the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="c6649-110">Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="c6649-110">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="c6649-111">Sie können URL-Umleitungsinformationen hinzufügen und entfernen, indem Sie eine der folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="c6649-111">You can add and remove URL redirection information by performing one of the following tasks:</span></span>

-   [<span data-ttu-id="c6649-112">Bearbeiten des Registrierungsschlüssels für die URL-Umleitung und Bereitstellen mithilfe von Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="c6649-112">Edit the URL Redirection Registry Key and Deploy Using Group Policy</span></span>](#bkmk-editreg)

-   [<span data-ttu-id="c6649-113">Bearbeiten der Textdatei für die URL-Umleitung und erneutes Erstellen des MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c6649-113">Edit the URL Redirection Text File and Rebuild the MED-V Workspace</span></span>](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**<span data-ttu-id="c6649-114">So aktualisieren Sie URL-Umleitungsinformationen mithilfe von Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="c6649-114">To update URL Redirection information by using Group Policy</span></span>**

1.  <span data-ttu-id="c6649-115">Bearbeiten Sie den Namen des Registrierungsschlüssel-mehrteiligen Zeichenfolgenwerts `RedirectUrls` .</span><span class="sxs-lookup"><span data-stu-id="c6649-115">Edit the registry key multi-string value that is named `RedirectUrls`.</span></span> <span data-ttu-id="c6649-116">Dieser Wert befindet sich normalerweise unter:</span><span class="sxs-lookup"><span data-stu-id="c6649-116">This value is typically located at:</span></span>

    <span data-ttu-id="c6649-117">Computer\\HKEY\ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\userexperience</span><span class="sxs-lookup"><span data-stu-id="c6649-117">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

    <span data-ttu-id="c6649-118">Wenn Sie dem Registrierungsschlüssel URLs hinzufügen, geben Sie diese pro Zeile ein, wie es beim Aufbau des MED-V-Arbeitsbereichs Pakets erforderlich war.</span><span class="sxs-lookup"><span data-stu-id="c6649-118">If you are adding URLs to the registry key, enter them one per line, as was required when you built the MED-V workspace package.</span></span> <span data-ttu-id="c6649-119">Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="c6649-119">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

2.  <span data-ttu-id="c6649-120">Bereitstellen des aktualisierten Registrierungsschlüssels mithilfe von Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="c6649-120">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="c6649-121">Weitere Informationen zum Verwenden von Gruppenrichtlinien finden Sie unter [Gruppenrichtlinien-Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="c6649-121">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

<span data-ttu-id="c6649-122">**Hinweis**  Diese Methode zum Bearbeiten von URL-Umleitungsinformationen ist ein bewährtes MED-V-Verfahren.</span><span class="sxs-lookup"><span data-stu-id="c6649-122">**Note** This method of editing URL redirection information is a MED-V best practice.</span></span>

 

<a href="" id="bkmk-edittext"></a>**<span data-ttu-id="c6649-123">So erstellen Sie den MED-V-Arbeitsbereich mithilfe einer aktualisierten URL-Textdatei neu</span><span class="sxs-lookup"><span data-stu-id="c6649-123">To rebuild the MED-V workspace by using an updated URL text file</span></span>**

-   <span data-ttu-id="c6649-124">Eine weitere Methode zum Hinzufügen und Entfernen von URLs aus der Umleitungsliste besteht darin, die URL-Umleitungs Text Datei zu aktualisieren und dann zum Erstellen eines neuen MED-V-Arbeitsbereichs zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6649-124">Another method of adding and removing URLs from the redirection list is to update the URL redirection text file and then use it to build a new MED-V workspace.</span></span> <span data-ttu-id="c6649-125">Anschließend können Sie den MED-V-Arbeitsbereich wie zuvor mithilfe Ihres Standard Bereitstellungsprozesses wie einem ESD-System erneut bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c6649-125">You can then redeploy the MED-V workspace as before, by using your standard process of deployment, such as an ESD system.</span></span>

    <span data-ttu-id="c6649-126">**Wichtig**  Diese Methode zur Bearbeitung von URL-Umleitungsinformationen wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="c6649-126">**Important** We do not recommend this method of editing URL redirection information.</span></span> <span data-ttu-id="c6649-127">Darüber hinaus muss die erstmalige Einrichtung erneut ausgeführt werden, und alle auf dem virtuellen Computer gespeicherten Daten gehen verloren, wenn Sie den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c6649-127">In addition, any time that you redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="c6649-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c6649-128">Related topics</span></span>


[<span data-ttu-id="c6649-129">So testen Sie die URL-Umleitung</span><span class="sxs-lookup"><span data-stu-id="c6649-129">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="c6649-130">Verwalten von Anwendungen, die in MED-V-Arbeitsbereichen bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="c6649-130">Managing Applications Deployed to MED-V Workspaces</span></span>](managing-applications-deployed-to-med-v-workspaces.md)

[<span data-ttu-id="c6649-131">Erstellen eines MED-V-Arbeitsbereichspakets</span><span class="sxs-lookup"><span data-stu-id="c6649-131">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

 

 





