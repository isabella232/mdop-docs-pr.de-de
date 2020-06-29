---
title: So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung
description: So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804616"
---
# <span data-ttu-id="ac6e7-103">So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="ac6e7-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="ac6e7-104">Eine Microsoft BitLocker-Verwaltungs-und Überwachungsanwendung (MBAM), die so genannten BitLocker-Verschlüsselungsoptionen, ist unter **System und Sicherheit** verfügbar, wenn der MBAM-Client installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the MBAM Client is installed.</span></span> <span data-ttu-id="ac6e7-105">Diese angepasste MBAM-Systemsteuerung ersetzt die standardmäßige Windows BitLocker-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-105">This customized MBAM control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="ac6e7-106">Das MBAM Control Panel ermöglicht Ihnen, verschlüsselte Laufwerke (behoben und abnehmbar) zu entsperren, und hilft Ihnen auch bei der Verwaltung Ihrer PIN oder Ihres Kennworts.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-106">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span> <span data-ttu-id="ac6e7-107">Weitere Informationen zum Aktivieren der MBAM-Systemsteuerung finden Sie unter [Ausblenden der BitLocker-Standardverschlüsselung in der Windows-System](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)Steuerung.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-107">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in The Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span></span>

<span data-ttu-id="ac6e7-108">**Hinweis**  Für den BitLocker-Client befinden sich die Administrator-und Betriebsprotokoll Dateien in der Ereignisanzeige unter **Anwendungs-und Dienstprotokolle**  /  **Microsoft**  /  **Windows**-  /  **BitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-108">**Note** For the BitLocker client, the Admin and Operational log files are located in Event Viewer, under **Application and Services Logs** / **Microsoft** / **Windows** / **BitLockerManagement**.</span></span>

 

**<span data-ttu-id="ac6e7-109">So verwenden Sie die MBAM-Client-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="ac6e7-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="ac6e7-110">Um die BitLocker-Verschlüsselungsoptionen zu öffnen, klicken Sie auf **Start**, und wählen Sie **System**Steuerung aus.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-110">To open BitLocker Encryption Options, click **Start**, and then select **Control Panel**.</span></span> <span data-ttu-id="ac6e7-111">Wenn **die Systemsteuerung geöffnet** wird, wählen Sie **System und Sicherheit**aus.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="ac6e7-112">Doppelklicken Sie auf **BitLocker-Verschlüsselungsoptionen** , um die angepasste MBAM-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="ac6e7-113">Es wird eine Liste aller Festplatten auf dem Computer und deren Verschlüsselungsstatus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-113">You will see a list of all the hard disk drives on the computer and their encryption status.</span></span> <span data-ttu-id="ac6e7-114">Außerdem wird eine Option zum Verwalten Ihrer PIN oder Kennwörter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-114">You will also see an option to manage your PIN or passwords.</span></span>

3.  <span data-ttu-id="ac6e7-115">Verwenden Sie die Liste der Festplattenlaufwerke auf dem Computer, um den Verschlüsselungsstatus zu überprüfen, ein Laufwerk zu entsperren oder eine Ausnahme für den BitLocker-Schutz zu fordern, wenn die Richtlinien für Benutzer-und Computer Ausnahmen bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-115">Use the list of hard disk drives on the computer to verify the encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

4.  <span data-ttu-id="ac6e7-116">Nicht Administratoren können Pins oder Kennwörter mithilfe der Systemsteuerung für BitLocker-Verschlüsselungsoptionen verwalten.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-116">Non-administrators can use the BitLocker Encryption Options control panel to manage PINs or passwords.</span></span> <span data-ttu-id="ac6e7-117">Ein Benutzer kann " **Pin verwalten** " auswählen und dann sowohl eine aktuelle PIN als auch eine neue PIN eingeben.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-117">A user can select **Manage PIN,** and then enter both a current PIN and a new PIN.</span></span> <span data-ttu-id="ac6e7-118">Benutzer können auch Ihre neue PIN bestätigen.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-118">Users can also confirm their new PIN.</span></span> <span data-ttu-id="ac6e7-119">Mit der Funktion " **Pin aktualisieren** " wird die PIN auf das neue zurückgesetzt, das der Benutzer auswählt.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-119">The **Update PIN** function will reset the PIN to the new one that the user selects.</span></span>

5.  <span data-ttu-id="ac6e7-120">Wenn Sie Ihr Kennwort verwalten möchten, wählen Sie **Laufwerk entsperren** und geben Sie Ihr aktuelles Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-120">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="ac6e7-121">Sobald das Laufwerk entriegelt ist, wählen Sie **Kennwort zurücksetzen** aus, um Ihr aktuelles Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ac6e7-121">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="ac6e7-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ac6e7-122">Related topics</span></span>


[<span data-ttu-id="ac6e7-123">Verwalten von MBAM 1.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ac6e7-123">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





