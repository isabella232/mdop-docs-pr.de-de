---
title: So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu
description: So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808713"
---
# <span data-ttu-id="54690-103">So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu</span><span class="sxs-lookup"><span data-stu-id="54690-103">How to Assign the Proper Credentials for Windows Vista</span></span>


<span data-ttu-id="54690-104">Gehen Sie wie folgt vor, um den App-V-Desktop Client für korrekte Windows Vista-Anmeldeinformationen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="54690-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsVista credentials.</span></span>

<span data-ttu-id="54690-105">**Hinweis**  Dieses Verfahren muss auf jedem Computer ohne Domäne abgeschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="54690-105">**Note** This procedure must be completed on each non-domain joined computer.</span></span> <span data-ttu-id="54690-106">Je nach der Anzahl der nicht an die Domäne angeschlossenen Computer in Ihrer Umgebung kann dies eine sehr mühsame Operation sein.</span><span class="sxs-lookup"><span data-stu-id="54690-106">Depending on the number of non-domain joined computers in your environment, this could be a very tedious operation.</span></span> <span data-ttu-id="54690-107">Sie können Skripts und die Befehlszeilenschnittstelle für den Anmelde Informations-Manager verwenden, um Administratoren bei der Automatisierung dieses Prozesses zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="54690-107">You can use scripts and the command-line interface for Credential Manager to help administrators automate this process.</span></span>

 

**<span data-ttu-id="54690-108">So weisen Sie die richtigen Anmeldeinformationen für App-V-Clients mit Windows Vista zu</span><span class="sxs-lookup"><span data-stu-id="54690-108">To assign the proper credentials for App-V clients running Windows Vista</span></span>**

1.  <span data-ttu-id="54690-109">Öffnen Sie mit Administratorrechten auf dem App-V-Desktop Client unter Windows Vista die Systemsteuerung für **Benutzerkonten** (klassisches Control Panel).</span><span class="sxs-lookup"><span data-stu-id="54690-109">With administrator privileges on the App-V Desktop Client running Windows Vista, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="54690-110">Wählen Sie im Bereich links Aufgaben die Option **Netzwerkkennwörter** aus **Benutzerkonten** verwalten aus.</span><span class="sxs-lookup"><span data-stu-id="54690-110">Select **Manage your network passwords** from **User Accounts** in the left tasks pane.</span></span>

3.  <span data-ttu-id="54690-111">Wählen Sie auf dem Bildschirm **Gespeicherte Benutzernamen und Kennwörter** die Option **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="54690-111">Select **Add** on the **Stored User Names and Passwords** screen.</span></span>

4.  <span data-ttu-id="54690-112">Geben Sie auf dem Bildschirm **Eigenschaften der gespeicherten Anmelde** Informationen die Informationen für die App-V-Infrastruktur an:</span><span class="sxs-lookup"><span data-stu-id="54690-112">On the **Stored Credential Properties** screen, provide the information for the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="54690-113">**Melden Sie sich bei an:** Externer Name des Veröffentlichungsservers.</span><span class="sxs-lookup"><span data-stu-id="54690-113">**Log on to:** External name of the publishing server.</span></span>

    2.  <span data-ttu-id="54690-114">**Benutzername:** Benutzername für den externen Benutzer im Formular Domain\\Username.</span><span class="sxs-lookup"><span data-stu-id="54690-114">**User name:** User name for the external user in the form Domain\\Username.</span></span>

    3.  <span data-ttu-id="54690-115">**Kennwort:** Das Kennwort für das Benutzerkonto, das in das Feld " **Benutzername** " eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="54690-115">**Password:** Password for the user account entered in the **User name** field.</span></span>

    4.  <span data-ttu-id="54690-116">Geben Sie den **Anmeldeinformationstyp** ausgewählt, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="54690-116">Leave **Credential Type** selected, and click **OK**.</span></span>

5.  <span data-ttu-id="54690-117">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="54690-117">Click **Close**.</span></span> <span data-ttu-id="54690-118">Die Anmeldeinformationen werden im Anmeldeinformationsspeicher für die ordnungsgemäße Authentifizierung in der App-V-Infrastruktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="54690-118">The credentials are stored in the credential store for proper authentication to the App-V infrastructure.</span></span>

## <span data-ttu-id="54690-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="54690-119">Related topics</span></span>


[<span data-ttu-id="54690-120">In die Domäne eingebundene und keiner Domäne beigetretene Clients</span><span class="sxs-lookup"><span data-stu-id="54690-120">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="54690-121">So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu</span><span class="sxs-lookup"><span data-stu-id="54690-121">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





