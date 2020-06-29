---
title: So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus
description: So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810597"
---
# <span data-ttu-id="6abe1-103">So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus</span><span class="sxs-lookup"><span data-stu-id="6abe1-103">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>


<span data-ttu-id="6abe1-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) bietet ein angepasstes Control Panel für MBAM-Clientcomputer mit dem Namen "BitLocker-Verschlüsselungsoptionen".</span><span class="sxs-lookup"><span data-stu-id="6abe1-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for MBAM client computers that is named called BitLocker Encryption Options.</span></span> <span data-ttu-id="6abe1-105">Dieses angepasste Control Panel kann die standardmäßige Windows BitLocker-Systemsteuerung mit dem Namen BitLocker Drive Encryption ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6abe1-105">This customized control panel can replace the default Windows BitLocker control panel that is named BitLocker Drive Encryption.</span></span> <span data-ttu-id="6abe1-106">Mit der Systemsteuerung für BitLocker-Verschlüsselungsoptionen, die sich unter System und Sicherheit in der Windows-Systemsteuerung befindet, können Benutzer Ihre PIN und Kennwörter verwalten, Laufwerke entsperren und die Oberfläche ausblenden, mit der Administratoren ein Laufwerk entschlüsseln oder die BitLocker-Verschlüsselung anhalten oder fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="6abe1-106">The BitLocker Encryption Options control panel, located under System and Security in the Windows control panel, enables users to manage their PIN and passwords, unlock drives, and hides the interface that allows administrators to decrypt a drive or to suspend or resume BitLocker encryption.</span></span>

**<span data-ttu-id="6abe1-107">So blenden Sie die BitLocker-Standardverschlüsselung in der Windows-Systemsteuerung aus</span><span class="sxs-lookup"><span data-stu-id="6abe1-107">To hide default BitLocker Encryption in the Windows Control Panel</span></span>**

1.  <span data-ttu-id="6abe1-108">Navigieren Sie mithilfe der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC), der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) oder des Editors für lokale Gruppenrichtlinien auf dem BitLocker-Gruppenrichtlinien Computer zu **Benutzerkonfiguration** .</span><span class="sxs-lookup"><span data-stu-id="6abe1-108">Browse to **User configuration** by using the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer.</span></span>

2.  <span data-ttu-id="6abe1-109">Klicken Sie auf **Richtlinien**, wählen Sie **Administrative Vorlagen**aus, und klicken Sie dann auf **System**Steuerung.</span><span class="sxs-lookup"><span data-stu-id="6abe1-109">Click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="6abe1-110">Doppelklicken Sie im **Detail** Bereich auf **angegebene Control Panel-Elemente ausblenden**, und wählen Sie dann **aktiviert**aus.</span><span class="sxs-lookup"><span data-stu-id="6abe1-110">In the **Details** pane, double-click **Hide specified Control Panel items**, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="6abe1-111">Klicken Sie auf **anzeigen**, **Klicken Sie auf hinzufügen...**, und geben Sie dann Microsoft. BitLockerDriveEncryption ein.</span><span class="sxs-lookup"><span data-stu-id="6abe1-111">Click **Show**, **click Add…**, and then type Microsoft.BitLockerDriveEncryption.</span></span> <span data-ttu-id="6abe1-112">Mit dieser Richtlinie wird das standardmäßige Windows BitLocker-Verwaltungstool aus der Windows-Systemsteuerung ausgeblendet, und der Benutzer kann das aktualisierte MBAM BitLocker-Verschlüsselungsoptionen Tool in der Windows-Systemsteuerung öffnen.</span><span class="sxs-lookup"><span data-stu-id="6abe1-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and allows the user to open the updated MBAM BitLocker Encryption Options tool from the Windows Control Panel.</span></span>

## <span data-ttu-id="6abe1-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6abe1-113">Related topics</span></span>


[<span data-ttu-id="6abe1-114">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="6abe1-114">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





