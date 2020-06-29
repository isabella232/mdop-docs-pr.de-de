---
title: So richten Sie regelmäßige Veröffentlichungsaktualisierungen ein
description: So richten Sie regelmäßige Veröffentlichungsaktualisierungen ein
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806752"
---
# <span data-ttu-id="9a672-103">So richten Sie regelmäßige Veröffentlichungsaktualisierungen ein</span><span class="sxs-lookup"><span data-stu-id="9a672-103">How to Set Up Periodic Publishing Refresh</span></span>


<span data-ttu-id="9a672-104">Mit dem folgenden Verfahren können Sie den Client so konfigurieren, dass die Veröffentlichungsinformationen in regelmäßigen Abständen von den App-V-Servern aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9a672-104">You can use the following procedure to configure the client to periodically refresh the publishing information from the App-V servers.</span></span> <span data-ttu-id="9a672-105">Nachdem der Client konfiguriert wurde, ist der Aktualisierungsvorgang automatisch.</span><span class="sxs-lookup"><span data-stu-id="9a672-105">After the client is configured, the refresh operation is automatic.</span></span> <span data-ttu-id="9a672-106">Mit diesen Einstellungen werden die Standardeinstellungen für den Client so konfiguriert, dass alle Benutzer auf diesem Computer dieselben Einstellungen sehen.</span><span class="sxs-lookup"><span data-stu-id="9a672-106">These settings configure the default settings for the client so that all users on this computer will see the same settings.</span></span>

<span data-ttu-id="9a672-107">**Hinweis**  Nachdem Sie diese Schritte ausgeführt haben, werden die Veröffentlichungsinformationen gemäß den neuen Einstellungen nach der ersten Aktualisierung bei der Anmeldung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9a672-107">**Note** After you have performed this procedure, the publishing information will be refreshed according to the new settings after the first refresh at login.</span></span> <span data-ttu-id="9a672-108">Wenn diese erste Aktualisierung erfolgt, kann der Server je nach Konfiguration die Computereinstellungen mit unterschiedlichen Einstellungen außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="9a672-108">When this first refresh occurs, the server might override the computer settings with different settings, depending on how it is configured.</span></span> <span data-ttu-id="9a672-109">Auf der Registerkarte " **Aktualisieren** " im Dialogfeld " **Eigenschaften** " werden die lokal konfigurierten Clientcomputereinstellungen sowie alle Einstellungen angezeigt, die möglicherweise vom Veröffentlichungsserver für den Benutzer konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="9a672-109">The **Refresh** tab in the **Properties** dialog box shows the locally configured client computer settings and any settings that might have been configured for the user by the publishing server.</span></span>

 

**<span data-ttu-id="9a672-110">So aktualisieren Sie die Veröffentlichungsinformationen in regelmäßigen Abständen von den Application Virtualization-Servern</span><span class="sxs-lookup"><span data-stu-id="9a672-110">To periodically refresh the publishing information from the Application Virtualization Servers</span></span>**

1.  <span data-ttu-id="9a672-111">Klicken Sie **im Bereich Bereich** auf **Veröffentlichungsserver** .</span><span class="sxs-lookup"><span data-stu-id="9a672-111">Click **Publishing Servers** in the **Scope** pane.</span></span>

2.  <span data-ttu-id="9a672-112">Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste auf den gewünschten Server, und wählen Sie im Popup-Menü **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="9a672-112">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up-menu.</span></span>

3.  <span data-ttu-id="9a672-113">Aktivieren Sie im Dialogfeld **Eigenschaften** auf der Registerkarte **Aktualisieren** das Kontrollkästchen **Konfiguration aktualisieren alle** , und geben Sie eine Zahl ein, die die Häufigkeit im Feld darstellt.</span><span class="sxs-lookup"><span data-stu-id="9a672-113">In the **Properties** dialog box, on the **Refresh** tab, select the **Refresh configuration every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="9a672-114">Wählen Sie dann im Dropdownmenü die Option **Minuten**, **Stunden**und **Tage** aus.</span><span class="sxs-lookup"><span data-stu-id="9a672-114">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span>

    <span data-ttu-id="9a672-115">**Hinweis**  Diese Einstellung bewirkt, dass der Client die Veröffentlichungsinformationen jedes Mal aktualisiert, wenn der konfigurierte Zeitraum abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="9a672-115">**Note** This setting will cause the client to refresh publishing information every time the configured period elapses.</span></span> <span data-ttu-id="9a672-116">Wenn der Benutzer nicht angemeldet ist, wenn es Zeit ist, eine Aktualisierung durchführen zu lassen, wird die Aktualisierung durchgeführt, wenn sich der Benutzer beim nächsten Mal anmeldet.</span><span class="sxs-lookup"><span data-stu-id="9a672-116">If the user is not logged in when it's time to do a refresh, the refresh will take place when the user next logs in.</span></span> <span data-ttu-id="9a672-117">Der Timer wird dann für den nächsten Zeitraum erneut gestartet.</span><span class="sxs-lookup"><span data-stu-id="9a672-117">The timer is then started again for the next period.</span></span>

     

4.  <span data-ttu-id="9a672-118">Klicken Sie auf über **nehmen** , um die Konfiguration zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9a672-118">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="9a672-119">Wenn Sie die Konfiguration des Servers abgeschlossen haben, klicken Sie auf **OK** , um das Dialogfeld zu schließen und zur Application Virtualization Client Management Console zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="9a672-119">When you finish configuring the server, click **OK** to exit the dialog box and return to the Application Virtualization Client Management Console.</span></span>

## <span data-ttu-id="9a672-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9a672-120">Related topics</span></span>


[<span data-ttu-id="9a672-121">So konfigurieren Sie den Client in der Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="9a672-121">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





