---
title: So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung
description: So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810957"
---
# <span data-ttu-id="4d6ac-103">So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="4d6ac-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="4d6ac-104">Eine Microsoft BitLocker-Verwaltungs-und Überwachungsanwendung (MBAM), die so genannten BitLocker-Verschlüsselungsoptionen, wird unter **System und Sicherheit** verfügbar sein, wenn der Microsoft BitLocker-Verwaltungs-und-Überwachungs Client installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the Microsoft BitLocker Administration and Monitoring Client is installed.</span></span> <span data-ttu-id="4d6ac-105">Dieses benutzerdefinierte MBAM Control Panel ist ein zusätzliches Control Panel.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-105">This custom MBAM control panel is an additional control panel.</span></span> <span data-ttu-id="4d6ac-106">Die standardmäßige Windows BitLocker-Systemsteuerung wird nicht ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-106">It does not replace the default Windows BitLocker control panel.</span></span> <span data-ttu-id="4d6ac-107">Über das MBAM-Control Panel können verschlüsselte fest-und Wechseldatenträger freigegeben und auch Ihre PIN oder Ihr Kennwort verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-107">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span> <span data-ttu-id="4d6ac-108">Weitere Informationen zum Aktivieren der MBAM-Systemsteuerung finden Sie unter [Ausblenden der BitLocker-Standardverschlüsselung in der Windows-System](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)Steuerung.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-108">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in the Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span></span>

**<span data-ttu-id="4d6ac-109">So verwenden Sie die MBAM-Client-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="4d6ac-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="4d6ac-110">Klicken Sie zum Öffnen der BitLocker-Verschlüsselungsoptionen auf **Start** und dann auf **System**Steuerung.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-110">To open BitLocker Encryption Options, click **Start** and then select **Control Panel**.</span></span> <span data-ttu-id="4d6ac-111">Wenn **die Systemsteuerung geöffnet** wird, wählen Sie **System und Sicherheit**aus.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="4d6ac-112">Doppelklicken Sie auf **BitLocker-Verschlüsselungsoptionen** , um die angepasste MBAM-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="4d6ac-113">Es wird eine Liste aller Festplatten auf dem Computer und deren Verschlüsselungsstatus sowie eine Option zum Verwalten Ihrer PIN oder Kennwörter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-113">You will see a list of all the hard disk drives on the computer and their encryption status, in addition to an option to manage your PIN or passwords.</span></span>

    <span data-ttu-id="4d6ac-114">Die Liste der Festplattenlaufwerke auf dem Computer kann zum Überprüfen des Verschlüsselungsstatus, Entsperren eines Laufwerks oder zum Anfordern einer Ausnahme für den BitLocker-Schutz verwendet werden, wenn die Ausnahmerichtlinien für Benutzer und Computer bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-114">The list of hard disk drives on the computer can be used to verify encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

    <span data-ttu-id="4d6ac-115">Mit der Systemsteuerung für BitLocker-Verschlüsselungsoptionen können auch Benutzer ohne Administratorrechte Ihre PIN oder Kennwörter verwalten.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-115">The BitLocker Encryption Options control panel also allows for non-administrator users to manage their PIN or passwords.</span></span> <span data-ttu-id="4d6ac-116">Durch Auswahl von " **Pin verwalten**" werden die Benutzer aufgefordert, sowohl eine aktuelle PIN als auch eine neue PIN einzugeben (zusätzlich zur Bestätigung der neuen PIN).</span><span class="sxs-lookup"><span data-stu-id="4d6ac-116">By selecting **Manage PIN**, users are prompted to enter both a current PIN and a new PIN (in addition to confirming the new PIN).</span></span> <span data-ttu-id="4d6ac-117">Wenn Sie die Option " **Pin aktualisieren** " auswählen, wird die PIN auf das neue Kennwort zurückgesetzt, das die Benutzer ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-117">Selecting **Update PIN** will reset the PIN to the new one that the users selected.</span></span>

    <span data-ttu-id="4d6ac-118">Wenn Sie Ihr Kennwort verwalten möchten, wählen Sie **Laufwerk entsperren** und geben Sie Ihr aktuelles Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-118">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="4d6ac-119">Sobald das Laufwerk entriegelt ist, wählen Sie **Kennwort zurücksetzen** aus, um Ihr aktuelles Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4d6ac-119">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="4d6ac-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4d6ac-120">Related topics</span></span>


[<span data-ttu-id="4d6ac-121">Verwalten von MBAM 2.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="4d6ac-121">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





