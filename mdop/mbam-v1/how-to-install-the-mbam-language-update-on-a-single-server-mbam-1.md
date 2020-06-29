---
title: So installieren Sie das MBAM-Sprachupdate auf einem einzelnen Server
description: So installieren Sie das MBAM-Sprachupdate auf einem einzelnen Server
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810744"
---
# <span data-ttu-id="54b45-103">So installieren Sie das MBAM-Sprachupdate auf einem einzelnen Server</span><span class="sxs-lookup"><span data-stu-id="54b45-103">How to Install the MBAM Language Update on a Single Server</span></span>


<span data-ttu-id="54b45-104">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst vier Serverrollen, die auf einem oder mehreren Computern ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="54b45-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="54b45-105">Allerdings erfordern nur zwei MBAM-Server Features das Update, um die Installation der MBAM 1,0-Sprachversion und der MBAM-Richtlinienvorlage zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="54b45-105">However, only two MBAM Server features require the update to support installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="54b45-106">Führen Sie die in diesem Thema beschriebenen Schritte aus, um alle drei erforderlichen MBAM-Features zu aktualisieren, die auf einem Computer installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="54b45-106">To update all three of the required MBAM features to be installed on one computer, perform the steps described in this topic.</span></span>

**<span data-ttu-id="54b45-107">So installieren Sie das MBAM-sprach Update auf einem einzelnen Server</span><span class="sxs-lookup"><span data-stu-id="54b45-107">To install the MBAM language update on a single server</span></span>**

1.  <span data-ttu-id="54b45-108">Öffnen Sie die Internet Informationsdienste (IIS)-Verwaltungskonsole, wechseln Sie zu **Websites**, und schließen Sie dann die Website für die Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="54b45-108">Open the Internet Information Services (IIS) Management Console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="54b45-109">Bearbeiten Sie die Bindungen für die MBAM-Website, und ändern Sie dann temporär die Bindungen der Website.</span><span class="sxs-lookup"><span data-stu-id="54b45-109">Edit the bindings for the MBAM website, and then temporarily modify the bindings of the site.</span></span> <span data-ttu-id="54b45-110">Ändern Sie beispielsweise den Port von 443 in 9443.</span><span class="sxs-lookup"><span data-stu-id="54b45-110">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="54b45-111">Suchen Sie den MBAM-Setup-Assistenten (MBAMsetup.exe), und führen Sie ihn aus, und wählen Sie die folgenden drei Features aus:</span><span class="sxs-lookup"><span data-stu-id="54b45-111">Locate and run the MBAM setup wizard (MBAMsetup.exe) and select the following three features:</span></span>

    1.  <span data-ttu-id="54b45-112">Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="54b45-112">Compliance and Audit Reports</span></span>

    2.  <span data-ttu-id="54b45-113">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="54b45-113">Administration and Monitoring Server</span></span>

    3.  <span data-ttu-id="54b45-114">Vorlagen für Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="54b45-114">Group Policy Templates</span></span>

    <span data-ttu-id="54b45-115">**Wichtig**  Die MBAM-Server Features müssen in der folgenden Reihenfolge aktualisiert werden: zuerst Konformitäts-und Überwachungsberichte, dann Administration und Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="54b45-115">**Important** The MBAM server features must be updated in the following order: Compliance and Audit Reports first, then Administration and Monitoring Server.</span></span> <span data-ttu-id="54b45-116">Die Gruppenrichtlinienvorlagen können jederzeit ohne Rücksicht auf die Reihenfolge aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="54b45-116">The Group Policy templates can be updated at any time without concern for sequence.</span></span>

     

4.  <span data-ttu-id="54b45-117">Nachdem Sie die Server Datenbank aktualisiert haben, öffnen Sie die IIS-Verwaltungskonsole, und überprüfen Sie die Bindungen der Website Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="54b45-117">After you upgrade the server database, open the IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="54b45-118">Löschen Sie eine der Bindungen, und stellen Sie sicher, dass die verbleibende Bindung den richtigen Hostnamen, das Zertifikat und die Portnummer für die MBAM Enterprise-Konfiguration aufweist.</span><span class="sxs-lookup"><span data-stu-id="54b45-118">Delete one of the bindings and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="54b45-119">Starten Sie die MBAM-Website neu.</span><span class="sxs-lookup"><span data-stu-id="54b45-119">Restart the MBAM website.</span></span>

7.  <span data-ttu-id="54b45-120">Testen Sie die Funktionalität der MBAM-Website:</span><span class="sxs-lookup"><span data-stu-id="54b45-120">Test the MBAM website functionality:</span></span>

    -   <span data-ttu-id="54b45-121">Öffnen Sie die MBAM-Weboberfläche, und stellen Sie sicher, dass Sie einen Wiederherstellungsschlüssel für einen Client abrufen können.</span><span class="sxs-lookup"><span data-stu-id="54b45-121">Open the MBAM web interface and ensure you can fetch a recovery key for a client.</span></span>

    -   <span data-ttu-id="54b45-122">Erzwingen der Verschlüsselung eines neuen oder manuell entschlüsselten Clientcomputers</span><span class="sxs-lookup"><span data-stu-id="54b45-122">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="54b45-123">**Hinweis**  Der MBAM-Client wird nur geöffnet, wenn er mit der Wiederherstellungs-und Hardware Datenbank kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="54b45-123">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="54b45-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="54b45-124">Related topics</span></span>


[<span data-ttu-id="54b45-125">Bereitstellen des Sprachrelease-Updates für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="54b45-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





