---
title: Bereitstellen von MBAM mit dem Konfigurations-Manager
description: Bereitstellen von MBAM mit dem Konfigurations-Manager
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809964"
---
# <span data-ttu-id="81e2c-103">Bereitstellen von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="81e2c-103">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="81e2c-104">In den folgenden Verfahren wird beschrieben, wie Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit Microsoft System Center Configuration Manager 2007 oder MicrosoftSystemCenter2012 ConfigurationManager durch usingthe Empfohlene Konfiguration bereitstellen, die unter [Erste Schritte bei der Verwendung von MBAM mit Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="81e2c-104">The following procedures describe how to deploy Microsoft BitLocker Administration and Monitoring (MBAM) with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager by usingthe recommended configuration, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="81e2c-105">Die empfohlene Konfiguration besteht darin, die Verwaltungs-und Überwachungsfeatures auf einem oder mehreren Microsoft BitLocker-Verwaltungs-und-Überwachungs Servern zu installieren und Microsoft System Center Configuration Manager 2007 oder MicrosoftSystemCenter2012 ConfigurationManager auf einem separaten Server zu installieren.</span><span class="sxs-lookup"><span data-stu-id="81e2c-105">The recommended configuration is to install the Administration and Monitoring features on one or more Microsoft BitLocker Administration and Monitoring servers, and install Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager on a separate server.</span></span>

<span data-ttu-id="81e2c-106">Bevor Sie mit der Installation beginnen, stellen Sie sicher, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen für die Installation von MBAM mit Configuration Manager erfüllt haben, indem Sie [Planen zum Bereitstellen von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md)überprüfen.</span><span class="sxs-lookup"><span data-stu-id="81e2c-106">Before you start the installation, ensure that you have met the prerequisites and hardware and software requirements for installing MBAM with Configuration Manager by reviewing [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="81e2c-107">Wenn Sie MBAM mit der Configuration Manager-Topologie erneut installieren müssen, müssen Sie zuerst bestimmte Configuration Manager-Objekte entfernen.</span><span class="sxs-lookup"><span data-stu-id="81e2c-107">If you ever have to reinstall MBAM with the Configuration Manager topology, you will need to remove certain Configuration Manager objects first.</span></span> <span data-ttu-id="81e2c-108">Lesen Sie den [Knowledge Base-Artikel](https://go.microsoft.com/fwlink/?LinkId=286306) , um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="81e2c-108">Read the [Knowledge Base article](https://go.microsoft.com/fwlink/?LinkId=286306) for more information.</span></span>

<span data-ttu-id="81e2c-109">Die Schritte zum Installieren von MBAM mit Configuration Manager sind in die folgenden Kategorien unterteilt.</span><span class="sxs-lookup"><span data-stu-id="81e2c-109">The steps to install MBAM with Configuration Manager are grouped into the following categories.</span></span> <span data-ttu-id="81e2c-110">Führen Sie die Schritte für jede Kategorie aus, um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="81e2c-110">Complete the steps for each category to complete the installation.</span></span>

## <span data-ttu-id="81e2c-111">So erstellen oder bearbeiten Sie MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="81e2c-111">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="81e2c-112">Damit die Clientcomputer BitLocker-Konformitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die Datei " **Configuration. MOF** " Bearbeiten und entweder die SMS \ _def. MOF-Datei bearbeiten oder erstellen, je nachdem, welche Version von Configuration Manager Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="81e2c-112">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the **Configuration.mof** file, and either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

[<span data-ttu-id="81e2c-113">So erstellen oder bearbeiten Sie MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="81e2c-113">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

## <span data-ttu-id="81e2c-114">So installieren Sie MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="81e2c-114">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="81e2c-115">In diesem Abschnitt finden Sie eine schrittweise Anleitung zum Installieren der folgenden Schritte: MBAM auf dem Configuration Manager-Server; die Wiederherstellungs-und Überwachungsdatenbanken auf dem Daten Bank Server; und die Verwaltungs-und Überwachungsserver Features auf dem Verwaltungs-und Überwachungsserver.</span><span class="sxs-lookup"><span data-stu-id="81e2c-115">This section provides steps about how to install the following: MBAM on the Configuration Manager Server; the Recovery and Audit Databases on the Database Server; and the Administration and Monitoring Server features on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="81e2c-116">So installieren Sie MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="81e2c-116">How to Install MBAM with Configuration Manager</span></span>](how-to-install-mbam-with-configuration-manager.md)

## <span data-ttu-id="81e2c-117">Überprüfen der MBAM Server-Feature-Installation auf dem Configuration Manager-Server</span><span class="sxs-lookup"><span data-stu-id="81e2c-117">How to Validate the MBAM Server Feature Installation on the Configuration Manager Server</span></span>


<span data-ttu-id="81e2c-118">Wenn die Microsoft BitLocker-Administrator-und-überwachungsinstallation abgeschlossen ist, überprüfen Sie, ob die Installation alle erforderlichen MBAM-Features erfolgreich eingerichtet hat, die für den Configuration Manager-Server erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="81e2c-118">When the Microsoft BitLocker Administration and Monitoring installation is complete, validate that the installation has successfully set up all the necessary MBAM features required for the Configuration Manager Server.</span></span>

[<span data-ttu-id="81e2c-119">So überprüfen Sie die MBAM-Installation mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="81e2c-119">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## <span data-ttu-id="81e2c-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="81e2c-120">Related topics</span></span>


[<span data-ttu-id="81e2c-121">Verwenden von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="81e2c-121">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





