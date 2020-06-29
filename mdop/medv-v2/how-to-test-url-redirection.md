---
title: So testen Sie die URL-Umleitung
description: So testen Sie die URL-Umleitung
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810561"
---
# <span data-ttu-id="7e720-103">So testen Sie die URL-Umleitung</span><span class="sxs-lookup"><span data-stu-id="7e720-103">How to Test URL Redirection</span></span>


<span data-ttu-id="7e720-104">Nachdem Ihr Test der erstmaligen Einrichtung abgeschlossen wurde, können Sie überprüfen, ob die URL-Umleitungsfunktion wie erwartet funktioniert, indem Sie die folgenden Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e720-104">After your test of first time setup finishes, you can verify that the URL redirection functionality is working as expected by performing the following tasks.</span></span>

<span data-ttu-id="7e720-105">**Wichtig**  Der MED-V-Host-Agent muss ausgeführt werden, damit die URL-Umleitung ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7e720-105">**Important** The MED-V Host Agent must be running for URL redirection to function correctly.</span></span>

<a href="" id="bkmk-urlredir"></a>**<span data-ttu-id="7e720-106">So testen Sie die URL-Umleitung</span><span class="sxs-lookup"><span data-stu-id="7e720-106">To test URL Redirection</span></span>**

1.  <span data-ttu-id="7e720-107">Öffnen Sie einen Internet Explorer-Browser auf dem Hostcomputer, und geben Sie eine URL ein, die Sie für die Umleitung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="7e720-107">Open an Internet Explorer browser in the host computer and enter a URL that you specified for redirection.</span></span>

2.  <span data-ttu-id="7e720-108">Überprüfen Sie, ob die Webseite auf dem virtuellen Gastcomputer in Internet Explorer geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7e720-108">Verify that the webpage is opened in Internet Explorer on the guest virtual machine.</span></span>

3.  <span data-ttu-id="7e720-109">Wiederholen Sie diesen Vorgang für jede URL, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="7e720-109">Repeat this process for each URL that you want to test.</span></span>

**<span data-ttu-id="7e720-110">So testen Sie, ob eine URL hinzugefügt oder entfernt werden kann</span><span class="sxs-lookup"><span data-stu-id="7e720-110">To test that a URL can be added or removed</span></span>**

1.  <span data-ttu-id="7e720-111">Hinzufügen oder Entfernen einer URL aus dem MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="7e720-111">Add or remove a URL from the MED-V workspace.</span></span>

    <span data-ttu-id="7e720-112">Informationen zum Hinzufügen und Entfernen von URLs für die Umleitung in einem Med-v-Arbeitsbereich finden Sie unter [Verwalten der Med-v-URL-Umleitung](manage-med-v-url-redirection.md).</span><span class="sxs-lookup"><span data-stu-id="7e720-112">For information about how to add and remove URLs for redirection on a MED-V workspace, see [Manage MED-V URL Redirection](manage-med-v-url-redirection.md).</span></span>

2.  <span data-ttu-id="7e720-113">Wenn Sie der Umleitungsliste eine URL hinzugefügt haben, wiederholen Sie die Schritte in [, um die URL-Umleitung zu testen](#bkmk-urlredir) , um zu überprüfen, ob die neue URL wie beabsichtigt umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7e720-113">If you added a URL to the redirection list, repeat the steps in [To Test URL Redirection](#bkmk-urlredir) to verify that the new URL redirects as intended.</span></span>

3.  <span data-ttu-id="7e720-114">Wenn Sie eine URL aus der Umleitungsliste entfernt haben, überprüfen Sie, ob Sie entfernt wurde, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="7e720-114">If you removed a URL from the redirection list, verify that it is removed by following these steps:</span></span>

    1.  <span data-ttu-id="7e720-115">Öffnen Sie einen Internet Explorer-Browser auf dem Hostcomputer, und geben Sie die URL ein, die Sie aus der Umleitungsliste entfernt haben.</span><span class="sxs-lookup"><span data-stu-id="7e720-115">Open an Internet Explorer browser in the host computer and enter the URL that you removed from the redirection list.</span></span>

    2.  <span data-ttu-id="7e720-116">Überprüfen Sie, ob die Webseite in Internet Explorer auf dem Hostcomputer und nicht auf dem virtuellen Gastcomputer geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="7e720-116">Verify that the webpage is opened in Internet Explorer on the host computer instead of on the guest virtual machine.</span></span>

        <span data-ttu-id="7e720-117">**Hinweis**  Es kann einige Sekunden dauern, bis die URL-Umleitungs Änderungen stattfinden.</span><span class="sxs-lookup"><span data-stu-id="7e720-117">**Note** It can take several seconds for the URL redirection changes to take place.</span></span>

<span data-ttu-id="7e720-118">**Hinweis**  Wenn bei der Überprüfung Ihrer URL-Umleitungseinstellungen Probleme auftreten, lesen Sie [Problembehandlung bei Vorgängen](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="7e720-118">**Note** If you encounter any problems when verifying your URL redirection settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="7e720-119">Nachdem Sie das Testen der URL-Umleitung in Ihrem MED-V-Arbeitsbereich abgeschlossen haben, können Sie andere Konfigurationen testen, um zu überprüfen, ob Sie wie beabsichtigt funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7e720-119">After you have completed testing URL redirection in your MED-V workspace, you can test other configurations to verify that they function as intended.</span></span>

<span data-ttu-id="7e720-120">Nachdem Sie das Testen des Med-v-Arbeitsbereichs Pakets abgeschlossen haben und überprüft haben, dass es wie beabsichtigt funktioniert, können Sie den Med-v-Arbeitsbereich für Ihr Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7e720-120">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="7e720-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7e720-121">Related topics</span></span>

[<span data-ttu-id="7e720-122">So testen Sie die Anwendungsveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="7e720-122">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="7e720-123">So überprüfen Sie erstmalige Einstellungen für das Setup</span><span class="sxs-lookup"><span data-stu-id="7e720-123">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="7e720-124">Bereitstellen des MED-V-Arbeitsbereichspakets</span><span class="sxs-lookup"><span data-stu-id="7e720-124">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





