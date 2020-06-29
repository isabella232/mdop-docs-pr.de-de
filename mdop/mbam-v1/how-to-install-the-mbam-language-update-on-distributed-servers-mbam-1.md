---
title: So installieren Sie das MBAM-Sprachupdate auf verteilten Servern
description: So installieren Sie das MBAM-Sprachupdate auf verteilten Servern
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811311"
---
# <span data-ttu-id="8566b-103">So installieren Sie das MBAM-Sprachupdate auf verteilten Servern</span><span class="sxs-lookup"><span data-stu-id="8566b-103">How to Install the MBAM Language Update on Distributed Servers</span></span>


<span data-ttu-id="8566b-104">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst vier Serverrollen, die auf einem oder mehreren Computern ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="8566b-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="8566b-105">Allerdings erfordern nur zwei MBAM-Server Features das Update, um die Installation der MBAM 1,0-Sprachversion und der MBAM-Richtlinienvorlage zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8566b-105">However, only two MBAM Server features require the update to support the installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="8566b-106">In Konfigurationen mit den MBAM-Server Features, die auf mehreren Computern installiert sind, müssen nur die folgenden Server Features aktualisiert werden:</span><span class="sxs-lookup"><span data-stu-id="8566b-106">In configurations with the MBAM Server features installed on multiple computers, only the following server features need to be updated:</span></span>

-   <span data-ttu-id="8566b-107">Die MBAM-Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="8566b-107">The MBAM Compliance and Audit Reports</span></span>

-   <span data-ttu-id="8566b-108">Der MBAM-Verwaltungs-und-Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="8566b-108">The MBAM Administration and Monitoring Server</span></span>

<span data-ttu-id="8566b-109">**Wichtig**  Die MBAM-Server Features müssen in dieser Reihenfolge aktualisiert werden: zuerst Konformitäts-und Überwachungsberichte und dann den Server für Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="8566b-109">**Important** The MBAM server features must be updated in this order: Compliance and Audit Reports first, and then the Administration and Monitoring Server.</span></span> <span data-ttu-id="8566b-110">Die MBAM-Gruppenrichtlinienvorlagen können jederzeit ohne Rücksicht auf die Reihenfolge aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8566b-110">The MBAM Group Policy templates can be updated at any time without concern for sequence.</span></span>

 

**<span data-ttu-id="8566b-111">So installieren Sie das MBAM-sprach Update auf der MBAM-Konformitäts-und Überwachungsberichts Server Funktion</span><span class="sxs-lookup"><span data-stu-id="8566b-111">To install the MBAM Language Update on the MBAM Compliance and Audit Report Server feature</span></span>**

1.  <span data-ttu-id="8566b-112">Suchen Sie auf dem Computer, auf dem das Feature MBAM-Konformitäts-und Überwachungsbericht ausgeführt wird, den MBAM-Setup-Assistenten für Sprach Updates (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="8566b-112">On the computer running the MBAM Compliance and Audit Report feature, locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span>

2.  <span data-ttu-id="8566b-113">Führen Sie den Assistenten für Konformitäts-und Überwachungsberichte aus, und schließen Sie dann den Assistenten.</span><span class="sxs-lookup"><span data-stu-id="8566b-113">Complete the wizard for the Compliance and Audit Reports and then close the wizard.</span></span>

**<span data-ttu-id="8566b-114">So installieren Sie das MBAM-sprach Update auf dem MBAM-Server Feature "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="8566b-114">To install the MBAM Language Update on the MBAM Administration and Monitoring Server feature</span></span>**

1.  <span data-ttu-id="8566b-115">Öffnen Sie auf dem Computer, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die IIS-Verwaltungskonsole (Internet Informationsdienste), wechseln Sie zu **Websites**, und schließen Sie dann die Website Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="8566b-115">On the computer that is running the MBAM Administration and Monitoring feature, open the Internet Information Services (IIS) management console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="8566b-116">Wählen Sie aus, um die Bindungen für die MBAM-Website zu bearbeiten, und ändern Sie dann die Bindungen der Website.</span><span class="sxs-lookup"><span data-stu-id="8566b-116">Choose to edit the bindings for the MBAM website, and then modify the bindings of the site.</span></span> <span data-ttu-id="8566b-117">Ändern Sie beispielsweise den Port von 443 in 9443.</span><span class="sxs-lookup"><span data-stu-id="8566b-117">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="8566b-118">Suchen Sie den Setup-Assistenten für MBAM-sprach Updates (MBAMsetup.exe), und führen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8566b-118">Locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span> <span data-ttu-id="8566b-119">Führen Sie den Assistenten für das Feature Verwaltung und Monitoring Server aus, und schließen Sie dann den Assistenten.</span><span class="sxs-lookup"><span data-stu-id="8566b-119">Complete the wizard for the Administration and Monitoring Server feature and then close the wizard.</span></span>

4.  <span data-ttu-id="8566b-120">Nachdem Sie die Server Datenbank aktualisiert haben, öffnen Sie die IIS-Verwaltungskonsole, und überprüfen Sie die Bindungen der Website Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="8566b-120">After you upgrade the server database, open IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="8566b-121">Löschen Sie die alte Bindung, und stellen Sie sicher, dass die verbleibende Bindung den richtigen Hostnamen, das Zertifikat und die Portnummer für die MBAM Enterprise-Konfiguration aufweist.</span><span class="sxs-lookup"><span data-stu-id="8566b-121">Delete the old binding and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="8566b-122">Starten Sie die MBAM-Website neu.</span><span class="sxs-lookup"><span data-stu-id="8566b-122">Restart the MBAM web site.</span></span>

7.  <span data-ttu-id="8566b-123">Testen Sie die Funktionalität der MBAM-Website:</span><span class="sxs-lookup"><span data-stu-id="8566b-123">Test the MBAM web site functionality:</span></span>

    -   <span data-ttu-id="8566b-124">Öffnen Sie die MBAM-Weboberfläche, und stellen Sie sicher, dass Sie einen Wiederherstellungsschlüssel für einen Client abrufen können.</span><span class="sxs-lookup"><span data-stu-id="8566b-124">Open the MBAM web interface and ensure that you can obtain a recovery key for a client.</span></span>

    -   <span data-ttu-id="8566b-125">Erzwingen der Verschlüsselung eines neuen oder manuell entschlüsselten Clientcomputers</span><span class="sxs-lookup"><span data-stu-id="8566b-125">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="8566b-126">**Hinweis**  Der MBAM-Client wird nur geöffnet, wenn er mit der Wiederherstellungs-und Hardware Datenbank kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="8566b-126">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="8566b-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8566b-127">Related topics</span></span>


[<span data-ttu-id="8566b-128">Bereitstellen des Sprachrelease-Updates für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8566b-128">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





