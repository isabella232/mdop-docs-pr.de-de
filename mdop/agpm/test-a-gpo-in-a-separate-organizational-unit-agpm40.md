---
title: Testen eines Gruppenrichtlinienobjekts in einer separaten Organisationseinheit
description: Testen eines Gruppenrichtlinienobjekts in einer separaten Organisationseinheit
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807435"
---
# <span data-ttu-id="e4862-103">Testen eines Gruppenrichtlinienobjekts in einer separaten Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="e4862-103">Test a GPO in a Separate Organizational Unit</span></span>


<span data-ttu-id="e4862-104">Wenn Sie eine Testorganisationseinheit (Organizational Unit, OU) zum Testen von Gruppenrichtlinienobjekten (GPOs) innerhalb der gleichen Domäne vor der Bereitstellung in der Produktionsumgebung verwenden, müssen Sie über die erforderlichen Berechtigungen für den Zugriff auf die Testorganisationseinheit verfügen.</span><span class="sxs-lookup"><span data-stu-id="e4862-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) within the same domain before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="e4862-105">Die Verwendung einer Test-ou ist optional.</span><span class="sxs-lookup"><span data-stu-id="e4862-105">Using a test OU is optional.</span></span>

**<span data-ttu-id="e4862-106">So verwenden Sie eine Testorganisationseinheit</span><span class="sxs-lookup"><span data-stu-id="e4862-106">To use a test OU</span></span>**

1.  <span data-ttu-id="e4862-107">Obwohl Sie das Gruppenrichtlinienobjekt zur Bearbeitung ausgecheckt haben, klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten.</span><span class="sxs-lookup"><span data-stu-id="e4862-107">Although you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="e4862-108">Klicken Sie auf die ausgecheckte Kopie des zu testenden Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="e4862-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="e4862-109">Dem Namen wird **\ [AGPM \]** vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="e4862-109">The name will be preceded by **\[AGPM\]**.</span></span> <span data-ttu-id="e4862-110">(Wenn Sie nicht aufgeführt ist, klicken Sie auf **Aktion**und dann auf **Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="e4862-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="e4862-111">Sortieren Sie die Namen alphabetisch, und **\ [AGPM \]** GPOs werden in der Regel oben in der Liste angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="e4862-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="e4862-112">Ziehen Sie das Gruppenrichtlinienobjekt in die OU Test.</span><span class="sxs-lookup"><span data-stu-id="e4862-112">Drag the GPO to the test OU.</span></span>

4.  <span data-ttu-id="e4862-113">Klicken Sie im Dialogfeld, in dem Sie gefragt werden, ob Sie einen Link zu einem GPO in der Testorganisationseinheit erstellen möchten, auf **OK** .</span><span class="sxs-lookup"><span data-stu-id="e4862-113">Click **OK** in the dialog box that asks whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="e4862-114">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="e4862-114">Additional considerations</span></span>

-   <span data-ttu-id="e4862-115">Nach Abschluss der Prüfung löscht das Einchecken des Gruppenrichtlinienobjekts automatisch den Link zu der ausgecheckten Kopie des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="e4862-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="e4862-116">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="e4862-116">Additional references</span></span>

-   [<span data-ttu-id="e4862-117">Verwenden einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="e4862-117">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





