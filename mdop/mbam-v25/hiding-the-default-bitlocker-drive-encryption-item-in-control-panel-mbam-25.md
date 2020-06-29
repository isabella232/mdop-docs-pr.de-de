---
title: Ausblenden der Standard-BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung
description: Ausblenden der Standard-BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809751"
---
# <span data-ttu-id="c0abb-103">Ausblenden der Standard-BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="c0abb-103">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>


<span data-ttu-id="c0abb-104">In diesem Thema wird beschrieben, wie Sie das Control Panel-Element für die **BitLocker-Laufwerkverschlüsselung** ausblenden, das standardmäßig in der Systemsteuerung als Teil des Windows-Betriebssystems angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c0abb-104">This topic describes how to hide the **BitLocker Drive Encryption** Control Panel item, which appears by default on Control Panel as part of the Windows operating system.</span></span>

<span data-ttu-id="c0abb-105">**Hinweis**  Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erstellt ein zusätzliches, benutzerdefiniertes Control Panel-Element mit dem Namen **BitLocker-Verschlüsselungsoptionen**, mit dem Endbenutzer Ihre PIN und Ihr Kennwort verwalten, BitLocker für ein Laufwerk aktivieren und die Verschlüsselung überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="c0abb-105">**Note** Microsoft BitLocker Administration and Monitoring (MBAM) creates an additional, custom Control Panel item, called **BitLocker Encryption Options**, which enables end users to manage their PIN and password, turn on BitLocker for a drive, and check encryption.</span></span>

 

<span data-ttu-id="c0abb-106">Weitere Informationen finden Sie unter [Grundlegendes zu den BitLocker-Verschlüsselungsoptionen und Elementen der BitLocker-Laufwerkverschlüsselung in der System](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) Steuerung:</span><span class="sxs-lookup"><span data-stu-id="c0abb-106">See [Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) to read about:</span></span>

-   <span data-ttu-id="c0abb-107">Unterschiede zwischen der MBAM und den Standardelementen der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="c0abb-107">Differences between the MBAM and the default Control Panel items</span></span>

-   <span data-ttu-id="c0abb-108">Kontextmenü " **BitLocker verwalten** ", das angezeigt wird, wenn Sie in Windows-Explorer mit der rechten Maustaste auf ein Laufwerk klicken</span><span class="sxs-lookup"><span data-stu-id="c0abb-108">**Manage BitLocker** shortcut menu that appears when you right-click a drive in Windows Explorer</span></span>

<span data-ttu-id="c0abb-109">**Wichtig**  Ändern Sie nicht die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten.</span><span class="sxs-lookup"><span data-stu-id="c0abb-109">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node.</span></span> <span data-ttu-id="c0abb-110">In diesem Fall funktioniert MBAM nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c0abb-110">If you do, MBAM will not work correctly.</span></span> <span data-ttu-id="c0abb-111">Wenn Sie die Gruppenrichtlinieneinstellungen im MDOP- **MBAM (BitLocker-Verwaltungsknoten)** konfigurieren, konfiguriert MBAM automatisch die **BitLocker-Laufwerk Verschlüsselungs** Einstellungen für Sie.</span><span class="sxs-lookup"><span data-stu-id="c0abb-111">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="c0abb-112">So blenden Sie das standardmäßige BitLocker-Laufwerk Verschlüsselungselement in der Systemsteuerung aus</span><span class="sxs-lookup"><span data-stu-id="c0abb-112">To hide the default BitLocker Drive Encryption item in Control Panel</span></span>**

1.  <span data-ttu-id="c0abb-113">Navigieren Sie in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder in der erweiterten Gruppenrichtlinienverwaltung zu **Benutzer Konfigurations** &gt; **Richtlinien** für &gt; **Administrative Vorlagen** in der &gt; **System**Steuerung.</span><span class="sxs-lookup"><span data-stu-id="c0abb-113">In the Group Policy Management Console (GPMC) or in Advanced Group Policy Management, browse to **User configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Control Panel**.</span></span>

2.  <span data-ttu-id="c0abb-114">Doppelklicken Sie im **Detail** Bereich auf **angegebene Control Panel-Elemente ausblenden**, und klicken Sie dann auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="c0abb-114">In the **Details** pane, double-click **Hide specified Control Panel items**, and then click **Enabled**.</span></span>

3.  <span data-ttu-id="c0abb-115">Klicken Sie auf **anzeigen**, klicken Sie auf **Hinzufügen**, und geben Sie dann **Microsoft. BitLockerDriveEncryption**ein.</span><span class="sxs-lookup"><span data-stu-id="c0abb-115">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span>



## <span data-ttu-id="c0abb-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c0abb-116">Related topics</span></span>


[<span data-ttu-id="c0abb-117">Grundlegende Informationen zu BitLocker-Verschlüsselungsoptionen und BitLocker-Laufwerkverschlüsselungselementen in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="c0abb-117">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[<span data-ttu-id="c0abb-118">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c0abb-118">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)

 

## <span data-ttu-id="c0abb-119">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="c0abb-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c0abb-120">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="c0abb-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="c0abb-121">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c0abb-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





