---
title: Verwalten von MBAM 1.0-Funktionen
description: Verwalten von MBAM 1.0-Funktionen
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808626"
---
# <span data-ttu-id="d196e-103">Verwalten von MBAM 1.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d196e-103">Administering MBAM 1.0 Features</span></span>


<span data-ttu-id="d196e-104">Nachdem Sie alle erforderlichen MBAM-Planung und-Bereitstellung (Microsoft BitLocker-Verwaltung und-Überwachung) abgeschlossen haben, können Sie MBAM konfigurieren und verwenden, um die BitLocker-Unternehmens-Verschlüsselung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d196e-104">After you complete all necessary Microsoft BitLocker Administration and Monitoring (MBAM) planning and deployment, you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="d196e-105">Die Informationen in diesem Abschnitt beschreiben die täglichen Aufgaben der MBAM-funktionsvorgänge nach der Installation.</span><span class="sxs-lookup"><span data-stu-id="d196e-105">The information in this section describes post-installation day-to-day MBAM feature operations tasks.</span></span>

## <span data-ttu-id="d196e-106">Verwalten von MBAM-Administrator Rollen</span><span class="sxs-lookup"><span data-stu-id="d196e-106">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="d196e-107">Nachdem das MBAM-Setup für alle Server Features abgeschlossen ist, müssen Administrator Benutzern Zugriff auf diese Server Features gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="d196e-107">After MBAM Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="d196e-108">Als bewährte Methode sollten Administratoren, die die MBAM-Server Features verwalten oder verwenden, Active Directory-Sicherheitsgruppen zugewiesen werden, und diese Gruppen sollten der entsprechenden administrativen lokalen Gruppe MBAM hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d196e-108">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="d196e-109">So verwalten Sie MBAM-Administratorrollen</span><span class="sxs-lookup"><span data-stu-id="d196e-109">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-1.md)

## <span data-ttu-id="d196e-110">Verwalten der Hardware Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="d196e-110">Manage Hardware Compatibility</span></span>


<span data-ttu-id="d196e-111">Das MBAM-Hardware Kompatibilitätsfeature kann Ihnen dabei helfen, sicherzustellen, dass nur die von Ihnen als unterstützende BitLocker angegebene Computer Hardware verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="d196e-111">The MBAM Hardware Compatibility feature can help you to ensure that only the computer hardware that you specify as supporting BitLocker will be encrypted.</span></span> <span data-ttu-id="d196e-112">Wenn dieses Feature aktiviert ist, werden in Bit \ _admmontla nur Computer verschlüsselt, die als kompatibel gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="d196e-112">When this feature is turned on, bit\_admmontla will encrypt only computers that are marked as Compatible.</span></span>

<span data-ttu-id="d196e-113">**Wichtig**  Wenn dieses Feature deaktiviert ist, werden alle Computer, auf denen die MBAM-Richtlinie bereitgestellt wird, verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="d196e-113">**Important** When this feature is turned off, all computers where the MBAM policy is deployed will be encrypted.</span></span>

 

<span data-ttu-id="d196e-114">MBAM kann Informationen über die Marke und das Modell von Clientcomputern sammeln, wenn Sie die Gruppenrichtlinie "Hardware Kompatibilitätsüberprüfung zulassen" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d196e-114">MBAM can collect information on both the make and model of client computers if you deploy the “Allow Hardware Compatibility Checking” Group Policy.</span></span> <span data-ttu-id="d196e-115">Wenn Sie diese Richtlinie konfigurieren, meldet der MBAM-Agent dem MBAM-Server die Informationen zum Erstellen und modellieren des Computers, wenn der MBAM-Client auf einem Clientcomputer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d196e-115">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

[<span data-ttu-id="d196e-116">So verwalten Sie Hardwarekompatibilität</span><span class="sxs-lookup"><span data-stu-id="d196e-116">How to Manage Hardware Compatibility</span></span>](how-to-manage-hardware-compatibility-mbam-1.md)

[<span data-ttu-id="d196e-117">So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer</span><span class="sxs-lookup"><span data-stu-id="d196e-117">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## <span data-ttu-id="d196e-118">Verwalten von BitLocker-Verschlüsselungs Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="d196e-118">Manage BitLocker encryption exemptions</span></span>


<span data-ttu-id="d196e-119">MBAM kann zwei Arten von Ausnahmen von der BitLocker-Verschlüsselung gewähren: Computer Befreiung und Benutzer Befreiung.</span><span class="sxs-lookup"><span data-stu-id="d196e-119">MBAM can grant two forms of exemption from BitLocker encryption: computer exemption and user exemption.</span></span> <span data-ttu-id="d196e-120">Die Computer Befreiung wird in der Regel verwendet, wenn ein Unternehmen über Computer verfügt, die nicht verschlüsselt werden müssen, beispielsweise Computer, die in Entwicklungs-oder Testversionen verwendet werden, oder ältere Computer, die BitLocker nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d196e-120">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="d196e-121">In einigen Fällen kann die örtliche Gesetzgebung auch verlangen, dass bestimmte Computer nicht verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="d196e-121">In some cases, local law may also require that certain computers are not encrypted.</span></span> <span data-ttu-id="d196e-122">Sie können auch festlegen, dass Benutzer, die Ihre Laufwerke nicht benötigen oder verschlüsselt werden sollen, davon ausgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="d196e-122">You may also choose to exempt users who do not need or want their drives encrypted.</span></span>

[<span data-ttu-id="d196e-123">So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Computer</span><span class="sxs-lookup"><span data-stu-id="d196e-123">How to Manage Computer BitLocker Encryption Exemptions</span></span>](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## <span data-ttu-id="d196e-124">Verwalten von MBAM-Client-BitLocker-Verschlüsselungsoptionen mithilfe der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="d196e-124">Manage MBAM Client BitLocker Encryption Options by using the Control Panel</span></span>


<span data-ttu-id="d196e-125">Wenn Sie über ein Gruppenrichtlinienobjekt (Group Policy Objects, GPO) aktiviert ist, wird unter **System und Sicherheit**ein benutzerdefiniertes MBAM-Control Panel mit dem Namen BitLocker-Verschlüsselungsoptionen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d196e-125">If enabled through a Group Policy Objects (GPO), a custom MBAM control panel that is named BitLocker Encryption Options will be available under **System and Security**.</span></span> <span data-ttu-id="d196e-126">Dieses angepasste Control Panel ersetzt die standardmäßige Windows BitLocker-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="d196e-126">This customized control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="d196e-127">Das MBAM Control Panel ermöglicht Ihnen, verschlüsselte Laufwerke (behoben und abnehmbar) zu entsperren, und hilft Ihnen auch bei der Verwaltung Ihrer PIN oder Ihres Kennworts.</span><span class="sxs-lookup"><span data-stu-id="d196e-127">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span>

[<span data-ttu-id="d196e-128">So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="d196e-128">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## <span data-ttu-id="d196e-129">Weitere Ressourcen für die Verwaltung von MBAM-Features</span><span class="sxs-lookup"><span data-stu-id="d196e-129">Other resources for Administering MBAM features</span></span>


[<span data-ttu-id="d196e-130">Vorgänge für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d196e-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





