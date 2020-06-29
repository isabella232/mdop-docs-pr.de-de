---
title: So verwalten Sie Hardwarekompatibilität
description: So verwalten Sie Hardwarekompatibilität
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804637"
---
# <span data-ttu-id="a1395-103">So verwalten Sie Hardwarekompatibilität</span><span class="sxs-lookup"><span data-stu-id="a1395-103">How to Manage Hardware Compatibility</span></span>


<span data-ttu-id="a1395-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann Informationen zum Hersteller und Modell von Clientcomputern sammeln, nachdem Sie die Gruppenrichtlinie Hardware Kompatibilitätsüberprüfung zulassen bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="a1395-104">Microsoft BitLocker Administration and Monitoring (MBAM) can collect information about the manufacturer and model of client computers after you deploy the Allow Hardware Compatibility Checking Group Policy.</span></span> <span data-ttu-id="a1395-105">Wenn Sie diese Richtlinie konfigurieren, meldet der MBAM-Agent dem MBAM-Server die Informationen zum Erstellen und modellieren des Computers, wenn der MBAM-Client auf einem Clientcomputer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a1395-105">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

<span data-ttu-id="a1395-106">Das Hardware Kompatibilitätsfeature ist hilfreich, wenn Ihre Organisation über ältere Computer Hardware oder Computer verfügt, die TPM-Chips (Trusted Platform Module) nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a1395-106">The Hardware Compatibility feature is helpful when your organization has older computer hardware or computers that do not support Trusted Platform Module (TPM) chips.</span></span> <span data-ttu-id="a1395-107">In diesen Fällen können Sie das Hardware Kompatibilitätsfeature verwenden, um sicherzustellen, dass die BitLocker-Verschlüsselung nur auf Computermodelle angewendet wird, die Sie unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a1395-107">In these cases, you can use the Hardware Compatibility feature to ensure that BitLocker encryption is applied only to computer models that support it.</span></span> <span data-ttu-id="a1395-108">Wenn alle Computer in Ihrer Organisation BitLocker unterstützen, müssen Sie das Hardware Kompatibilitätsfeature nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1395-108">If all computers in your organization will support BitLocker, you do not have to use the Hardware Compatibility feature.</span></span>

<span data-ttu-id="a1395-109">**Hinweis**  Standardmäßig ist das MBAM-Hardware Kompatibilitätsfeature nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a1395-109">**Note** By default, MBAM Hardware Compatibility feature is not enabled.</span></span> <span data-ttu-id="a1395-110">Um Sie zu aktivieren, wählen Sie das **Hardware Kompatibilitäts** Feature während der Installation unter dem **Server Feature Verwaltung und Überwachung** aus.</span><span class="sxs-lookup"><span data-stu-id="a1395-110">To enable it, select the **Hardware Compatibility** feature under the **Administration and Monitoring Server** feature during setup.</span></span> <span data-ttu-id="a1395-111">Weitere Informationen zum Einrichten und Konfigurieren der Hardware Kompatibilität finden Sie unter [Bereitstellen der MBAM 1,0-Server Infrastruktur](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="a1395-111">For more information about how to set up and configure Hardware Compatibility, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

<span data-ttu-id="a1395-112">Das Hardware Kompatibilitätsfeature funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a1395-112">The Hardware Compatibility feature works in the following way.</span></span>

****

1.  <span data-ttu-id="a1395-113">Der MBAM-Client-Agent ermittelt grundlegende Computer Informationen wie Hersteller, Modell, BIOS Maker, BIOS-Version, TPM-Hersteller und TPM-Version und übergibt diese Informationen an den MBAM-Server.</span><span class="sxs-lookup"><span data-stu-id="a1395-113">The MBAM client agent discovers basic computer information such as manufacturer, model, BIOS maker, BIOS version, TPM maker, and TPM version, and then passes this information to the MBAM server.</span></span>

2.  <span data-ttu-id="a1395-114">Der MBAM-Server generiert eine Liste der Clientcomputer Marken und-Modelle, mit denen Sie zwischen denjenigen unterscheiden können, die BitLocker unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="a1395-114">The MBAM server generates a list of client computer makes and models to enable you to differentiate between those that can or cannot support BitLocker</span></span>

3.  <span data-ttu-id="a1395-115">Die im Unternehmen bereitgestellten MBAM-Client-Agents aktualisieren diese Liste automatisch mit allen neuen Computermarken und-Modellen, die mit einem **unbekannten**Zustand gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a1395-115">The MBAM client agents that are deployed in the enterprise automatically update this list with all new computer makes and models that are discovered with a state of **Unknown**.</span></span> <span data-ttu-id="a1395-116">Ein Administrator kann dann die MBAM-Verwaltungswebsite zum Ändern von Listeneinträgen verwenden, um einen bestimmten Computer als **kompatibel** oder **inkompatibel**festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a1395-116">An administrator can then use the MBAM administration website to change list entries to specify a particular computer make and model as **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="a1395-117">Bevor der MBAM-Client-Agent mit der Verschlüsselung eines Laufwerks beginnt, überprüft der Agent zuerst die BitLocker-Verschlüsselungs Kompatibilität der Hardware, auf der er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1395-117">Before the MBAM client agent begins encrypting a drive, the agent first verifies the BitLocker encryption compatibility of the hardware it is running on.</span></span>

    -   <span data-ttu-id="a1395-118">Wenn die Hardware als kompatibel markiert ist, wird der BitLocker-Verschlüsselungsprozess gestartet.</span><span class="sxs-lookup"><span data-stu-id="a1395-118">If the hardware is marked as compatible, the BitLocker encryption process starts.</span></span> <span data-ttu-id="a1395-119">MBAM wird auch den Hardware Kompatibilitätsstatus des Computers einmal pro Tag erneut überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a1395-119">MBAM will also recheck the hardware compatibility status of the computer one time per day.</span></span>

    -   <span data-ttu-id="a1395-120">Wenn die Hardware als nicht kompatibel gekennzeichnet ist, protokolliert der Agent ein Ereignis und übergibt den Status "Hardware ausgenommen" als Teil der Konformitäts Berichterstattung.</span><span class="sxs-lookup"><span data-stu-id="a1395-120">If the hardware is marked as incompatible, the agent logs an event and passes a “hardware exempted” state as part of compliance reporting.</span></span> <span data-ttu-id="a1395-121">Der Agent überprüft alle sieben Tage, ob der Status in "kompatibel" geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a1395-121">The agent checks every seven days to see whether the state has changed to “compatible.”</span></span>

    -   <span data-ttu-id="a1395-122">Wenn die Hardware als unbekannt markiert ist, wird der BitLocker-Verschlüsselungsprozess nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="a1395-122">If the hardware is marked as unknown, the BitLocker encryption process will not begin.</span></span> <span data-ttu-id="a1395-123">Der MBAM-Client-Agent überprüft den Hardware Kompatibilitätsstatus des Computers einmal pro Tag erneut.</span><span class="sxs-lookup"><span data-stu-id="a1395-123">The MBAM client agent will recheck the hardware compatibility status of the computer one time per day.</span></span>

<span data-ttu-id="a1395-124">**Warnung**  Wenn der MBAM-Client-Agent versucht, einen Computer zu verschlüsseln, der die BitLocker-Laufwerkverschlüsselung nicht unterstützt, besteht die Möglichkeit, dass der Computer beschädigt wird.</span><span class="sxs-lookup"><span data-stu-id="a1395-124">**Warning** If the MBAM client agent tries to encrypt a computer that does not support BitLocker drive encryption, there is a possibility that the computer will become corrupted.</span></span> <span data-ttu-id="a1395-125">Stellen Sie sicher, dass das Hardware Kompatibilitätsfeature richtig konfiguriert ist, wenn Ihre Organisation über eine ältere Hardware verfügt, die BitLocker nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a1395-125">Ensure that the hardware compatibility feature is correctly configured when your organization has older hardware that does not support BitLocker.</span></span>

 

**<span data-ttu-id="a1395-126">So verwalten Sie die Hardwarekompatibilität</span><span class="sxs-lookup"><span data-stu-id="a1395-126">To manage hardware compatibility</span></span>**

1.  <span data-ttu-id="a1395-127">Öffnen Sie einen Webbrowser, und navigieren Sie zur Website Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="a1395-127">Open a web browser and navigate to the Microsoft BitLocker Administration and Monitoring website.</span></span> <span data-ttu-id="a1395-128">Wählen Sie in der linken Menüleiste **Hardware** aus.</span><span class="sxs-lookup"><span data-stu-id="a1395-128">Select **Hardware** in the left menu bar.</span></span>

2.  <span data-ttu-id="a1395-129">Klicken Sie im rechten Bereich auf **Erweiterte Suche**und dann auf Filtern, um eine Liste aller Computermodelle anzuzeigen, die einen **Funktions** Status **unbekannt**aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a1395-129">On the right pane, click **Advanced Search**, and then filter to display a list of all computer models that have a **Capability** status of **Unknown**.</span></span> <span data-ttu-id="a1395-130">Eine Liste der Computermodelle, die den Suchkriterien entsprechen, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a1395-130">A list of computer models matching the search criteria is displayed.</span></span> <span data-ttu-id="a1395-131">Administratoren können auf dieser Seite neue Computertypen hinzufügen, bearbeiten oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="a1395-131">Administrators can add, edit, or remove new computer types from this page.</span></span>

3.  <span data-ttu-id="a1395-132">Überprüfen Sie jede unbekannte Hardwarekonfiguration, um zu ermitteln, ob die Konfiguration auf **kompatibel** oder nicht **kompatibel**festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1395-132">Review each unknown hardware configuration to determine whether the configuration should be set to **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="a1395-133">Wählen Sie eine oder mehrere Zeilen aus, und klicken Sie dann entweder auf **kompatibel festlegen** oder auf nicht **kompatibel** festlegen, um die BitLocker-Kompatibilität entsprechend den ausgewählten Computermodellen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a1395-133">Select one or more rows, and then click either **Set Compatible** or **Set Incompatible** to set the BitLocker compatibility, as appropriate, for the selected computer models.</span></span> <span data-ttu-id="a1395-134">Wenn Sie auf **kompatibel**festzulegen, versucht BitLocker, die Richtlinien für die Laufwerkverschlüsselung auf Computern zu erzwingen, die dem unterstützten Modell entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a1395-134">If set to **Compatible**, BitLocker tries to enforce drive encryption policy on computers that match the supported model.</span></span> <span data-ttu-id="a1395-135">Wenn Sie auf **inkompatibel**festzulegen, wird von BitLocker keine Laufwerk Verschlüsselungsrichtlinie auf diesen Computern erzwungen.</span><span class="sxs-lookup"><span data-stu-id="a1395-135">If set to **Incompatible**, BitLocker will not enforce drive encryption policy on those computers.</span></span>

    <span data-ttu-id="a1395-136">**Hinweis**  Nachdem Sie ein Computermodell als kompatibel festgesetzt haben, kann es mehr als vierundzwanzig Stunden dauern, bis der MBAM-Client die BitLocker-Verschlüsselung auf den Computern beginnt, die diesem Hardwaremodell entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a1395-136">**Note** After you set a computer model as compatible, it can take more than twenty-four hours for the MBAM Client to begin BitLocker encryption on the computers matching that hardware model.</span></span>

     

5.  <span data-ttu-id="a1395-137">Administratoren sollten die Hardwarekompatibilitätsliste regelmäßig überwachen, um neue Modelle zu überprüfen, die vom MBAM-Agent erkannt werden, und dann Ihre Kompatibilitätseinstellung auf **kompatibel** oder **inkompatibel** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a1395-137">Administrators should regularly monitor the hardware compatibility list to review new models that are discovered by the MBAM agent, and then update their compatibility setting to **Compatible** or **Incompatible** as appropriate.</span></span>

## <span data-ttu-id="a1395-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a1395-138">Related topics</span></span>


[<span data-ttu-id="a1395-139">Verwalten von MBAM 1.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a1395-139">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





