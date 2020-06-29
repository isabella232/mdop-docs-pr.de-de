---
title: So konfigurieren Sie die Vorabbereitstellung von Images
description: So konfigurieren Sie die Vorabbereitstellung von Images
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811737"
---
# <span data-ttu-id="89658-103">So konfigurieren Sie die Vorabbereitstellung von Images</span><span class="sxs-lookup"><span data-stu-id="89658-103">How to Configure Image Pre-staging</span></span>


<span data-ttu-id="89658-104">**Hinweis**  Bild-Pre-Staging ist nur für den anfänglichen Bild Download hilfreich.</span><span class="sxs-lookup"><span data-stu-id="89658-104">**Note** Image pre-staging is useful only for the initial image download.</span></span> <span data-ttu-id="89658-105">Es wird für die Bildaktualisierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89658-105">It is not supported for image update.</span></span>

 

## <span data-ttu-id="89658-106">So konfigurieren Sie die Vorabbereitstellung von Images</span><span class="sxs-lookup"><span data-stu-id="89658-106">How to Configure Image Pre-staging</span></span>


**<span data-ttu-id="89658-107">So konfigurieren Sie das Pre-Staging von Bildern</span><span class="sxs-lookup"><span data-stu-id="89658-107">To configure image pre-staging</span></span>**

1.  <span data-ttu-id="89658-108">Erstellen Sie auf dem Clientcomputer unter dem Bildspeicher Verzeichnis einen Ordner für das Pre-Staging-Bild, und nennen Sie es *MED-V-Bilder*.</span><span class="sxs-lookup"><span data-stu-id="89658-108">On the client computer, under the image store directory, create a folder for the pre-staging image, and name it *MED-V Images*.</span></span>

    <span data-ttu-id="89658-109">**Hinweis**  Dieser Ordner muss als *MED-V-Bilder*bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="89658-109">**Note** This folder must be called *MED-V Images*.</span></span>

     

2.  <span data-ttu-id="89658-110">Erstellen Sie im Ordner MED-V Images einen Unterordner, und geben Sie ihm den Namen *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="89658-110">Inside the MED-V Images folder, create a subfolder and name it *PrestagedImages*.</span></span>

    <span data-ttu-id="89658-111">**Hinweis**  Dieser Ordner muss *PrestagedImages*genannt werden.</span><span class="sxs-lookup"><span data-stu-id="89658-111">**Note** This folder must be called *PrestagedImages*.</span></span>

     

3.  <span data-ttu-id="89658-112">Um Zugriffsteuerungslisten (ACL)-Sicherheit auf den *MED-V Images-* Ordner anzuwenden, legen Sie die folgende ACL:</span><span class="sxs-lookup"><span data-stu-id="89658-112">To apply Access Control Lists (ACL) security to the *MED-V Images* folder, set the following ACL:</span></span>

    **<span data-ttu-id="89658-113">NT AUTHORITY\\Authenticated-Benutzer: (OI) (CI) (spezieller Zugriff:)</span><span class="sxs-lookup"><span data-stu-id="89658-113">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 <span data-ttu-id="89658-114">Datei \ _APPEND \ _data</span><span class="sxs-lookup"><span data-stu-id="89658-114">FILE\_APPEND\_DATA</span></span>**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **<span data-ttu-id="89658-115">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="89658-115">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="89658-116">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="89658-116">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="89658-117">**Hinweis**  Es wird empfohlen, ACL-Sicherheit auf den *MED-V Images-* Ordner anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="89658-117">**Note** It is recommended to apply ACL security to the *MED-V Images* folder.</span></span>

     

4.  <span data-ttu-id="89658-118">Wenn Sie ACL-Sicherheit auf den *PrestagedImages* -Ordner anwenden möchten, legen Sie die folgende ACL ab:</span><span class="sxs-lookup"><span data-stu-id="89658-118">To apply ACL security to the *PrestagedImages* folder, set the following ACL:</span></span>

    **<span data-ttu-id="89658-119">NT AUTHORITY\\Authenticated-Benutzer: (OI) (CI) (spezieller Zugriff:)</span><span class="sxs-lookup"><span data-stu-id="89658-119">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

    **<span data-ttu-id="89658-120">Lesen \ _CONTROL</span><span class="sxs-lookup"><span data-stu-id="89658-120">READ\_CONTROL</span></span>**

    **<span data-ttu-id="89658-121">Synchronisieren</span><span class="sxs-lookup"><span data-stu-id="89658-121">SYNCHRONIZE</span></span>**

    **<span data-ttu-id="89658-122">Datei \ _GENERIC \ _READ</span><span class="sxs-lookup"><span data-stu-id="89658-122">FILE\_GENERIC\_READ</span></span>**

    **<span data-ttu-id="89658-123">Datei \ _READ \ _data</span><span class="sxs-lookup"><span data-stu-id="89658-123">FILE\_READ\_DATA</span></span>**

    **<span data-ttu-id="89658-124">Datei \ _READ \ _EA</span><span class="sxs-lookup"><span data-stu-id="89658-124">FILE\_READ\_EA</span></span>**

    **<span data-ttu-id="89658-125">Datei \ _READ \ _ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="89658-125">FILE\_READ\_ATTRIBUTES</span></span>**

    **<span data-ttu-id="89658-126">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="89658-126">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="89658-127">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="89658-127">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="89658-128">**Hinweis**  Es wird empfohlen, ACL-Sicherheit auf den *PrestagedImages* -Ordner anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="89658-128">**Note** It is recommended to apply ACL security to the *PrestagedImages* folder.</span></span>

     

5.  <span data-ttu-id="89658-129">Drücken Sie die Bilddateien (CKM und Index Dateien) in den *PrestagedImages* -Ordner.</span><span class="sxs-lookup"><span data-stu-id="89658-129">Push the image files (CKM and INDEX files) to the *PrestagedImages* folder.</span></span>

    <span data-ttu-id="89658-130">**Hinweis**  Nachdem die Bilddateien in den Ordner "Pre-stage" verschoben wurden, empfiehlt es sich, eine Datenintegritätsprüfung durchzuführen und die Dateien schreibgeschützt zu markieren.</span><span class="sxs-lookup"><span data-stu-id="89658-130">**Note** After the image files have been pushed to the pre-stage folder, it is recommended to run a data integrity check and to mark the files as read-only.</span></span>

     

6.  <span data-ttu-id="89658-131">Fügen Sie den folgenden Parameter in die MED-V-Clientinstallation ein: *Client.MSI VMSFOLDER = "C:\\MED-V-Bilder"*.</span><span class="sxs-lookup"><span data-stu-id="89658-131">Include the following parameter in the MED-V client installation: *Client.MSI VMSFOLDER=”C:\\MED-V Images”*.</span></span>

## <span data-ttu-id="89658-132">Aktualisieren des Standorts vor der Phase</span><span class="sxs-lookup"><span data-stu-id="89658-132">How to Update the Pre-stage Location</span></span>


**<span data-ttu-id="89658-133">So aktualisieren Sie den Standort vor der Phase</span><span class="sxs-lookup"><span data-stu-id="89658-133">To update the pre-stage location</span></span>**

1.  <span data-ttu-id="89658-134">Der Registrierungsschlüssel, *PrestagedImagesPath*, verweist auf die Standardbild Position.</span><span class="sxs-lookup"><span data-stu-id="89658-134">The registry key, *PrestagedImagesPath*, points to the default image location.</span></span> <span data-ttu-id="89658-135">Die Datei befindet sich im folgenden Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="89658-135">It is located in the following directory:</span></span>

    -   <span data-ttu-id="89658-136">Auf einem x86-</span><span class="sxs-lookup"><span data-stu-id="89658-136">On an x86 -</span></span> `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   <span data-ttu-id="89658-137">Auf einem x64-</span><span class="sxs-lookup"><span data-stu-id="89658-137">On an x64 -</span></span> `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  <span data-ttu-id="89658-138">Wenn sich das Bild an einem anderen Speicherort befindet, ändern Sie den Pfad.</span><span class="sxs-lookup"><span data-stu-id="89658-138">If the image is in a different location, change the path.</span></span>

 

 





