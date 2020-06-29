---
title: So installieren Sie die Server und Systemkomponenten
description: So installieren Sie die Server und Systemkomponenten
author: dansimp
ms.assetid: c6f5fef0-522a-4ef1-8585-05b292d0289b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ceb5b8376189aee7631229dca912140e454536b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807028"
---
# <span data-ttu-id="3a4be-103">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="3a4be-103">How to Install the Servers and System Components</span></span>


<span data-ttu-id="3a4be-104">Bevor Sie Anwendungen für Benutzer bereitstellen können, müssen Sie die Microsoft Application Virtualization Platform-Komponenten installieren.</span><span class="sxs-lookup"><span data-stu-id="3a4be-104">Before you can deliver applications to users, you must install the Microsoft Application Virtualization Platform components.</span></span> <span data-ttu-id="3a4be-105">Die Themen in diesem Abschnitt enthalten die Informationen, die zum Installieren der Application Virtualization-Server und der anderen Application Virtualization System-Komponenten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3a4be-105">The topics in this section provide the information required to install the Application Virtualization Servers and the other Application Virtualization System components.</span></span>

<span data-ttu-id="3a4be-106">**Hinweis**  Die Verfahren in diesem Abschnitt führen Sie durch eine angepasste Installation, in der Sie Komponenten auswählen und auswählen, die auf separaten Computern installiert werden sollen, wie in einer Produktionsumgebung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="3a4be-106">**Note** The procedures in this section take you through a customized installation, where you pick and choose components to install on separate computers, as recommended in a production environment.</span></span> <span data-ttu-id="3a4be-107">Allerdings können Ihre Betriebsverfahren einen anderen Ansatz diktieren, und während des Installationsvorgangs möchten Sie möglicherweise Komponenten zusammen gruppieren.</span><span class="sxs-lookup"><span data-stu-id="3a4be-107">However, your operating procedures might dictate a different approach, and during the installation process you might want to group components together.</span></span> <span data-ttu-id="3a4be-108">Unabhängig davon, wo Sie die Komponenten installieren, können Sie Sie in beliebiger Reihenfolge installieren.</span><span class="sxs-lookup"><span data-stu-id="3a4be-108">Regardless of where you install the components, you can install them in any order.</span></span>

 

## <span data-ttu-id="3a4be-109">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="3a4be-109">In This Section</span></span>


<a href="" id="how-to-install-application-virtualization-management-server"></a>[<span data-ttu-id="3a4be-110">So installieren Sie Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="3a4be-110">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)  
<span data-ttu-id="3a4be-111">Bietet eine schrittweise Anleitung zum Installieren des Application Virtualization Management Servers und zur Zuweisung an die entsprechende Servergruppe.</span><span class="sxs-lookup"><span data-stu-id="3a4be-111">Provides a step-by-step procedure for installing the Application Virtualization Management Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-application-virtualization-streaming-server"></a>[<span data-ttu-id="3a4be-112">So installieren Sie die Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="3a4be-112">How to Install the Application Virtualization Streaming Server</span></span>](how-to-install-the-application-virtualization-streaming-server.md)  
<span data-ttu-id="3a4be-113">Enthält ein schrittweises Verfahren zum Installieren des Application Virtualization Streaming Servers und zur Zuweisung an die entsprechende Servergruppe.</span><span class="sxs-lookup"><span data-stu-id="3a4be-113">Provides a step-by-step procedure for installing the Application Virtualization Streaming Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-management-web-service"></a>[<span data-ttu-id="3a4be-114">So installieren Sie Management Web Service</span><span class="sxs-lookup"><span data-stu-id="3a4be-114">How to Install the Management Web Service</span></span>](how-to-install-the-management-web-service.md)  
<span data-ttu-id="3a4be-115">Bietet eine schrittweise Anleitung zum Installieren des Application Virtualization Management-Webdiensts auf einem Zielcomputer in Ihrem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3a4be-115">Provides a step-by-step procedure for installing the Application Virtualization Management Web Service on a target computer on your network.</span></span>

<a href="" id="how-to-install-the-management-console"></a>[<span data-ttu-id="3a4be-116">So installieren Sie die Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="3a4be-116">How to Install the Management Console</span></span>](how-to-install-the-management-console.md)  
<span data-ttu-id="3a4be-117">Bietet eine schrittweise Anleitung zum Installieren der Application Virtualization Management Console auf einem Zielcomputer in Ihrem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3a4be-117">Provides a step-by-step procedure for installing the Application Virtualization Management Console on a target computer on your network.</span></span>

<a href="" id="how-to-install-a-database"></a>[<span data-ttu-id="3a4be-118">So installieren Sie eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="3a4be-118">How to Install a Database</span></span>](how-to-install-a-database.md)  
<span data-ttu-id="3a4be-119">Bietet eine schrittweise Anleitung zum Installieren einer Datenbank für Ihre serverbasierte Bereitstellung von Application Virtualization, wenn noch keine Datenbank verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3a4be-119">Provides a step-by-step procedure for installing a database for your server-based deployment of Application Virtualization, if a database is not already available.</span></span>

<a href="" id="how-to-remove-the-application-virtualization-system-components"></a>[<span data-ttu-id="3a4be-120">So entfernen Sie die Application Virtualization System-Komponenten</span><span class="sxs-lookup"><span data-stu-id="3a4be-120">How to Remove the Application Virtualization System Components</span></span>](how-to-remove-the-application-virtualization-system-components.md)  
<span data-ttu-id="3a4be-121">Bietet Schritt-für-Schritt-Verfahren zum Entfernen aller oder ausgewählter Application Virtualization Software-Komponenten von einem Zielcomputer.</span><span class="sxs-lookup"><span data-stu-id="3a4be-121">Provides step-by-step procedures to remove all or selected Application Virtualization software components from a target computer.</span></span>

## <span data-ttu-id="3a4be-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3a4be-122">Related topics</span></span>


[<span data-ttu-id="3a4be-123">Übersicht über Application Virtualization Server-basierte Szenarien</span><span class="sxs-lookup"><span data-stu-id="3a4be-123">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="3a4be-124">So konfigurieren Sie Server für die serverbasierte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3a4be-124">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="3a4be-125">So aktualisieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="3a4be-125">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)

 

 





