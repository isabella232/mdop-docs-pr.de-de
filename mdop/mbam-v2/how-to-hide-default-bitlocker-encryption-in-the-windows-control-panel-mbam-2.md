---
title: So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus
description: So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810342"
---
# <span data-ttu-id="40e4c-103">So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus</span><span class="sxs-lookup"><span data-stu-id="40e4c-103">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>


<span data-ttu-id="40e4c-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) bietet ein angepasstes Control Panel für Microsoft BitLocker-Verwaltung und-Überwachung von Clientcomputern, so genannte BitLocker-Verschlüsselungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="40e4c-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for Microsoft BitLocker Administration and Monitoring client computers, called BitLocker Encryption Options.</span></span> <span data-ttu-id="40e4c-105">Dieses angepasste Control Panel kann die standardmäßige Windows BitLocker-Systemsteuerung ersetzen, die als BitLocker-Laufwerkverschlüsselung bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="40e4c-105">This customized control panel can replace the default Windows BitLocker control panel, which is called BitLocker Drive Encryption.</span></span> <span data-ttu-id="40e4c-106">Das angepasste Control Panel, das sich in der Systemsteuerung unter System und Sicherheit befindet, ermöglicht Benutzern, Ihre PIN und Kennwörter zu verwalten sowie Laufwerke zu entsperren, und blendet die Benutzeroberfläche aus, mit der Administratoren ein Laufwerk entschlüsseln oder die BitLocker-Laufwerkverschlüsselung anhalten oder fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="40e4c-106">The customized control panel, which is in Control Panel under System and Security, enables users to manage their PIN and passwords and to unlock drives, and hides the interface that enables administrators to decrypt a drive or to suspend or resume BitLocker drive encryption.</span></span>

**<span data-ttu-id="40e4c-107">So blenden Sie die standardmäßige BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung aus</span><span class="sxs-lookup"><span data-stu-id="40e4c-107">To hide default BitLocker drive encryption in Windows Control Panel</span></span>**

1.  <span data-ttu-id="40e4c-108">Navigieren Sie in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC), der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) oder dem Editor für lokale Gruppenrichtlinien auf dem BitLocker-Computer für Gruppenrichtlinien zur **Benutzerkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="40e4c-108">In the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer, browse to **User configuration**.</span></span>

2.  <span data-ttu-id="40e4c-109">Klicken Sie als nächstes auf **Richtlinien**, wählen Sie **Administrative Vorlagen**aus, und klicken Sie dann auf **System**Steuerung.</span><span class="sxs-lookup"><span data-stu-id="40e4c-109">Next, click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="40e4c-110">Doppelklicken Sie im **Detail** Bereich auf **angegebene Control Panel-Elemente ausblenden** , und wählen Sie dann **aktiviert**aus.</span><span class="sxs-lookup"><span data-stu-id="40e4c-110">Double-click **Hide specified Control Panel items** in the **Details** pane, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="40e4c-111">Klicken Sie auf **anzeigen**, klicken Sie auf **Hinzufügen**, und geben Sie dann **Microsoft. BitLockerDriveEncryption**ein.</span><span class="sxs-lookup"><span data-stu-id="40e4c-111">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span> <span data-ttu-id="40e4c-112">Mit dieser Richtlinie wird das standardmäßige Windows BitLocker-Verwaltungstool aus der Windows-Systemsteuerung ausgeblendet, und der Benutzer kann in der Systemsteuerung das aktualisierte MBAM BitLocker-Verschlüsselungsoptionen-Tool unter System und Sicherheit öffnen.</span><span class="sxs-lookup"><span data-stu-id="40e4c-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and, in Control Panel, lets the user open the updated MBAM BitLocker Encryption Options tool under System and Security.</span></span>

## <span data-ttu-id="40e4c-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="40e4c-113">Related topics</span></span>


[<span data-ttu-id="40e4c-114">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="40e4c-114">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





