---
title: So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu
description: So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807860"
---
# <span data-ttu-id="b01ae-103">So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu</span><span class="sxs-lookup"><span data-stu-id="b01ae-103">How to Assign the Proper Credentials for Windows XP</span></span>


<span data-ttu-id="b01ae-104">Gehen Sie wie folgt vor, um den App-V-Desktop Client für korrekte WindowsXP-Anmeldeinformationen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b01ae-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsXP credentials.</span></span>

<span data-ttu-id="b01ae-105">**Hinweis**  Nach Abschluss dieses Verfahrens kann der nicht der Domäne beige tretene Client eine Veröffentlichungsaktualisierung durchführen, ohne mit einer Domäne verbunden zu sein.</span><span class="sxs-lookup"><span data-stu-id="b01ae-105">**Note** After finishing this procedure, the non-domain joined client can perform a publishing refresh without being joined to a domain.</span></span>

 

**<span data-ttu-id="b01ae-106">So weisen Sie die richtigen Anmeldeinformationen für App-V-Clients mit WindowsXP zu</span><span class="sxs-lookup"><span data-stu-id="b01ae-106">To assign the proper credentials for App-V clients running WindowsXP</span></span>**

1.  <span data-ttu-id="b01ae-107">Öffnen Sie mit Administratorrechten auf dem App-V-Client, auf dem WindowsXP ausgeführt wird, die Systemsteuerung für **Benutzerkonten** (klassisches Control Panel).</span><span class="sxs-lookup"><span data-stu-id="b01ae-107">With administrator privileges on the App-V Client running WindowsXP, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="b01ae-108">Klicken Sie auf die **Registerkarte Erweitert**, und wählen Sie dann **Kennwörter verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="b01ae-108">Click the **Advanced Tab**, and select **Manage Passwords**.</span></span>

3.  <span data-ttu-id="b01ae-109">Klicken Sie auf dem Bildschirm **Gespeicherte Benutzernamen und Kennwörter** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="b01ae-109">On the **Stored User Names and Passwords** screen, click **Add**.</span></span>

4.  <span data-ttu-id="b01ae-110">Füllen Sie auf dem Bildschirm **Anmeldeinformationen Eigenschaften** die folgenden Felder mit Informationen aus der App-V-Infrastruktur aus:</span><span class="sxs-lookup"><span data-stu-id="b01ae-110">On the **Logon Information Properties** screen, fill out the following fields with information from the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="b01ae-111">**Server:** Name des externen Namens des Veröffentlichungsservers.</span><span class="sxs-lookup"><span data-stu-id="b01ae-111">**Server:** Name of publishing server external name.</span></span>

    2.  <span data-ttu-id="b01ae-112">**Benutzername:** Benutzername für externen Benutzer im Formular Domain\\username.</span><span class="sxs-lookup"><span data-stu-id="b01ae-112">**User name:** User name for external user in the form Domain\\username.</span></span>

    3.  <span data-ttu-id="b01ae-113">**Kennwort:** Das Kennwort für das Benutzerkonto, das in das Feld " **Benutzername** " eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b01ae-113">**Password:** Password for the user account entered in the **User name** field.</span></span>

5.  <span data-ttu-id="b01ae-114">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b01ae-114">Click **OK**.</span></span> <span data-ttu-id="b01ae-115">Die Anmeldeinformationen werden auf dem Client gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b01ae-115">The credentials will be stored on the client.</span></span>

## <span data-ttu-id="b01ae-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b01ae-116">Related topics</span></span>


[<span data-ttu-id="b01ae-117">In die Domäne eingebundene und keiner Domäne beigetretene Clients</span><span class="sxs-lookup"><span data-stu-id="b01ae-117">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="b01ae-118">So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu</span><span class="sxs-lookup"><span data-stu-id="b01ae-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





