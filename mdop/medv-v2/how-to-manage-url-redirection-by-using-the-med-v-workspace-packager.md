---
title: So verwalten Sie URL-Umleitungen mit dem Arbeitsbereichs-Packager für MED-V
description: So verwalten Sie URL-Umleitungen mit dem Arbeitsbereichs-Packager für MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810783"
---
# <span data-ttu-id="17863-103">So verwalten Sie URL-Umleitungen mit dem Arbeitsbereichs-Packager für MED-V</span><span class="sxs-lookup"><span data-stu-id="17863-103">How to Manage URL Redirection by Using the MED-V Workspace Packager</span></span>


<span data-ttu-id="17863-104">Sie können den Med-v-Arbeitsbereichs Paketdienst verwenden, um die URL-Umleitung im Med-v-Arbeitsbereich zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="17863-104">You can use the MED-V Workspace Packager to manage URL redirection in the MED-V workspace.</span></span>

**<span data-ttu-id="17863-105">So verwalten Sie die Umleitung von Webadressen in einem MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="17863-105">To manage web address redirection in a MED-V workspace</span></span>**

1.  <span data-ttu-id="17863-106">Klicken Sie zum Öffnen des **Med-v Workspace-Pakets**auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **Med-v Workspace Packager**.</span><span class="sxs-lookup"><span data-stu-id="17863-106">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="17863-107">Klicken Sie im Hauptbereich des **MED-V Workspace-Pakets** auf **Web-Umleitung verwalten**.</span><span class="sxs-lookup"><span data-stu-id="17863-107">On the **MED-V Workspace Packager** main panel, click **Manage Web Redirection**.</span></span>

3.  <span data-ttu-id="17863-108">Im Fenster **Web-Umleitung verwalten** können Sie eine Liste der URLs eingeben, einfügen oder importieren, die im MED-V-Arbeitsbereich an Internet Explorer umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="17863-108">In the **Manage Web Redirection** window, you can type, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span>

    **<span data-ttu-id="17863-109">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="17863-109">Note</span></span>**  
    <span data-ttu-id="17863-110">Die URL-Umleitung in MED-V unterstützt nur die Protokolle http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="17863-110">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="17863-111">MED-V bietet keine Unterstützung für FTP oder andere Protokolle.</span><span class="sxs-lookup"><span data-stu-id="17863-111">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. <span data-ttu-id="17863-112">Klicken Sie auf **Speichern unter...**</span><span class="sxs-lookup"><span data-stu-id="17863-112">Click **Save as…**</span></span> <span data-ttu-id="17863-113">, um die aktualisierten URL-Umleitungs Dateien im angegebenen Ordner zu speichern.</span><span class="sxs-lookup"><span data-stu-id="17863-113">to save the updated URL redirection files in the specified folder.</span></span> <span data-ttu-id="17863-114">MED-V erstellt eine Registrierungsdatei, die die aktualisierten URL-Umleitungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="17863-114">MED-V creates a registry file that contains the updated URL redirection information.</span></span> <span data-ttu-id="17863-115">Bereitstellen des aktualisierten Registrierungsschlüssels mithilfe von Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="17863-115">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="17863-116">Weitere Informationen zum Verwenden von Gruppenrichtlinien finden Sie unter [Gruppenrichtlinien-Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="17863-116">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

   <span data-ttu-id="17863-117">Med-v erstellt auch ein Windows PowerShell-Skript im angegebenen Ordner, das Sie zum erneuten Erstellen des aktualisierten MED-V-Arbeitsbereichs Pakets verwenden können.</span><span class="sxs-lookup"><span data-stu-id="17863-117">MED-V also creates a Windows PowerShell script in the specified folder that you can use to re-create the updated MED-V workspace package.</span></span>

## <span data-ttu-id="17863-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="17863-118">Related topics</span></span>


[<span data-ttu-id="17863-119">So fügen Sie URL-Umleitungsinformationen in einem bereitgestellten MED-V-Arbeitsbereich hinzu bzw. entfernen Sie sie</span><span class="sxs-lookup"><span data-stu-id="17863-119">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[<span data-ttu-id="17863-120">Verwalten von MED-V-URL-Umleitungen</span><span class="sxs-lookup"><span data-stu-id="17863-120">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)









