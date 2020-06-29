---
title: So verwalten Sie virtuelle Anwendungen manuell
description: So verwalten Sie virtuelle Anwendungen manuell
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806976"
---
# <span data-ttu-id="176ea-103">So verwalten Sie virtuelle Anwendungen manuell</span><span class="sxs-lookup"><span data-stu-id="176ea-103">How to Manage Virtual Applications Manually</span></span>


<span data-ttu-id="176ea-104">Sie können die Clientverwaltungskonsole Application Virtualization (app-v) verwenden, um virtuelle Anwendungen im App-v-Desktop Client oder auf dem App-v-Client für Remote Desktop Dienste (vormals Terminal Dienste) zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="176ea-104">You can use the Application Virtualization (App-V) Client Management Console to manage virtual applications in the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="176ea-105">App-V-Administratoren können die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="176ea-105">App-V administrators can use perform the following tasks:</span></span>

## <span data-ttu-id="176ea-106">Laden oder Entladen einer App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-106">How to Load or Unload an App-V Application</span></span>


<span data-ttu-id="176ea-107">Mit den folgenden Verfahren können Sie eine Anwendung direkt aus dem Cache im Bereich **Ergebnisse** des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole laden oder entladen.</span><span class="sxs-lookup"><span data-stu-id="176ea-107">You can use the following procedures to load or unload an application from the cache, directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="176ea-108">Wenn Sie diesen Knoten auswählen, wird im **Ergebnis** Bereich eine Liste der Anwendungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="176ea-108">When you select this node, the **Results** pane displays a list of applications.</span></span>

<span data-ttu-id="176ea-109">**Hinweis**  Beim Laden oder Entladen eines Pakets werden alle Anwendungen im Paket in den Cache geladen oder daraus entfernt.</span><span class="sxs-lookup"><span data-stu-id="176ea-109">**Note** When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span> <span data-ttu-id="176ea-110">Wenn Sie beim Laden eines Pakets nicht genügend Speicherplatz im Cache haben, um die Anwendungen zu laden, müssen Sie die Cachegröße erhöhen.</span><span class="sxs-lookup"><span data-stu-id="176ea-110">When loading a package, if you do not have adequate space in cache to load the applications, increase your cache size.</span></span> <span data-ttu-id="176ea-111">Weitere Informationen zur Cachegröße finden Sie unter [Ändern der Cachegröße und der Laufwerkbuchstaben Bezeichnung](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span><span class="sxs-lookup"><span data-stu-id="176ea-111">For more information about cache size, see [How to Change the Cache Size and the Drive Letter Designation](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span></span>

 

**<span data-ttu-id="176ea-112">So laden Sie eine App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-112">To load an App-V application</span></span>**

1.  <span data-ttu-id="176ea-113">Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **Laden** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-113">Move the cursor to the **Results** pane, right-click the desired application, and select **Load** from the pop-up menu.</span></span>

2.  <span data-ttu-id="176ea-114">Die Anwendung wird automatisch geladen.</span><span class="sxs-lookup"><span data-stu-id="176ea-114">The application is automatically loaded.</span></span> <span data-ttu-id="176ea-115">Der Fortschritt wird in der Spalte mit der Bezeichnung **Paket Status**nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="176ea-115">The progress is tracked in the column labeled **Package Status**.</span></span> <span data-ttu-id="176ea-116">Sie müssen die Ansicht aktualisieren, um festzustellen, ob die Auslastung abgeschlossen ist, oder um den Fortschritt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="176ea-116">You must refresh the view to see that the load is complete or to see the progress.</span></span>

**<span data-ttu-id="176ea-117">So entladen Sie eine App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-117">To unload an App-V application</span></span>**

1.  <span data-ttu-id="176ea-118">Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **entladen** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-118">Move the cursor to the **Results** pane, right-click the desired application, and select **Unload** from the pop-up menu.</span></span>

2.  <span data-ttu-id="176ea-119">Die Anwendung wird automatisch entladen, und die Spalte **Paket Status** wird aktualisiert, um die Änderung wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="176ea-119">The application is automatically unloaded, and the **Package Status** column is updated to reflect the change.</span></span>

## <span data-ttu-id="176ea-120">So löschen Sie eine App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-120">How to clear an App-V application</span></span>


<span data-ttu-id="176ea-121">Sie können eine Anwendung aus der Konsole direkt aus dem Bereich " **Ergebnisse** " des **Anwendungs** Knotens in der Application Virtualization Client Management Console löschen.</span><span class="sxs-lookup"><span data-stu-id="176ea-121">You can clear an application from the console directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="176ea-122">Wenn Sie eine Anwendung löschen, entfernt das System die Einstellungen, Verknüpfungen und Dateitypzuordnungen, die der Anwendung entsprechen, und entfernt die Anwendung auch aus der Liste der Anwendungen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="176ea-122">When you clear an application, the system removes the settings, shortcuts, and file type associations that correspond to the application and also removes the application from the user’s list of applications.</span></span>

<span data-ttu-id="176ea-123">**Hinweis**  Wenn Sie eine Anwendung von der Konsole löschen, können Sie diese Anwendung nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="176ea-123">**Note** When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="176ea-124">Die Anwendung verbleibt jedoch im Cache und steht weiterhin anderen Benutzern im gleichen System zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="176ea-124">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="176ea-125">Nach einer Veröffentlichungsaktualisierung werden die gelöschten Anwendungen wieder zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="176ea-125">After a publishing refresh, the cleared applications will again become available to you.</span></span> <span data-ttu-id="176ea-126">Wenn in einem Paket mehrere Anwendungen vorhanden sind, werden die Einstellungen des Benutzers erst entfernt, wenn alle Anwendungen gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="176ea-126">If there are multiple applications in a package, the user's settings are not removed until all of the applications are cleared.</span></span>

 

**<span data-ttu-id="176ea-127">So löschen Sie eine Anwendung über die Konsole</span><span class="sxs-lookup"><span data-stu-id="176ea-127">To clear an application from the console</span></span>**

1.  <span data-ttu-id="176ea-128">Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü die Option **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-128">Move the cursor to the **Results** pane, right-click the desired application, and select **Clear** from the pop-up menu.</span></span>

2.  <span data-ttu-id="176ea-129">Klicken Sie bei der Bestätigungsaufforderung auf **Ja** , um die Anwendung zu entfernen, oder auf **Nein** , um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="176ea-129">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="176ea-130">Reparieren einer App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-130">How to Repair an App-V application</span></span>


<span data-ttu-id="176ea-131">Wenn Sie eine ausgewählte Anwendung reparieren möchten, können Sie das folgende Verfahren direkt im Bereich " **Ergebnisse** " des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="176ea-131">To repair a selected application, you can perform the following procedure directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="176ea-132">Wenn Sie eine Anwendung reparieren, werden alle benutzerdefinierten Benutzereinstellungen entfernt und die Standardeinstellungen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="176ea-132">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="176ea-133">Mit dieser Aktion werden keine Verknüpfungen oder Dateitypzuordnungen geändert oder gelöscht, und die Anwendung wird nicht aus dem Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="176ea-133">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

**<span data-ttu-id="176ea-134">So reparieren Sie eine App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-134">To repair an App-V application</span></span>**

1.  <span data-ttu-id="176ea-135">Bewegen Sie den Cursor in den Bereich **Ergebnisse** .</span><span class="sxs-lookup"><span data-stu-id="176ea-135">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="176ea-136">Klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie dann im Popupmenü **Reparieren** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-136">Right-click the desired application, and select **Repair** from the pop-up menu.</span></span>

3.  <span data-ttu-id="176ea-137">Klicken Sie bei der Bestätigungsaufforderung auf **Ja** , um die Anwendung zu reparieren, oder auf **Nein** , um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="176ea-137">At the confirmation prompt, click **Yes** to repair the application or **No** to cancel.</span></span>

## <span data-ttu-id="176ea-138">Importieren einer App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-138">How to import an App-V application</span></span>


<span data-ttu-id="176ea-139">Mit dem folgenden Verfahren können Sie eine Anwendung direkt aus dem Bereich **Ergebnisse** des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole in den Cache importieren.</span><span class="sxs-lookup"><span data-stu-id="176ea-139">You can use the following procedure to import an application into the cache directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="176ea-140">So importieren Sie eine App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-140">To import an App-V application</span></span>**

1.  <span data-ttu-id="176ea-141">Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-141">Move the cursor to the **Results** pane, right-click the desired application, and select **Import** from the pop-up menu.</span></span>

2.  <span data-ttu-id="176ea-142">Navigieren Sie im Fenster **Durchsuchen** zum Speicherort der Paketdatei für die gewünschte Anwendung, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="176ea-142">From the **Browse** window, navigate to the location of the package file for the desired application, and then click **OK**.</span></span>

    <span data-ttu-id="176ea-143">**Hinweis**  Wenn Sie bereits einen Such Pfad für den Import konfiguriert haben oder sich die SFT-Datei im gleichen Pfad wie der letzte erfolgreiche Import befindet, ist Schritt 2 nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="176ea-143">**Note** If you have already configured an import search path or if the SFT file is in the same path as the last successful import, step 2 is not required.</span></span>

     

## <span data-ttu-id="176ea-144">Sperren oder Entsperren einer App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-144">How to lock or unlock an App-V application</span></span>


<span data-ttu-id="176ea-145">Mit den folgenden Verfahren können Sie alle Anwendungen im Application Virtualization Desktop Client-Cache oder im Client für Remote Desktop Dienste (ehemals Terminal Dienste) sperren oder entsperren.</span><span class="sxs-lookup"><span data-stu-id="176ea-145">You can use the following procedures to lock or unlock any application in the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services (formerly Terminal Services) cache.</span></span> <span data-ttu-id="176ea-146">Eine gesperrte Anwendung kann nicht aus dem Cache entfernt werden, um Platz für neue Anwendungen zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="176ea-146">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="176ea-147">Um eine gesperrte Anwendung aus dem Application Virtualization Desktop Client-Cache oder dem Client für Remote Desktop Dienste-Cache zu entfernen, müssen Sie Sie zuerst entsperren.</span><span class="sxs-lookup"><span data-stu-id="176ea-147">To remove a locked application from the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services cache, you must first unlock it.</span></span>

**<span data-ttu-id="176ea-148">So sperren Sie eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-148">To lock an application</span></span>**

1.  <span data-ttu-id="176ea-149">Bewegen Sie den Cursor in den Bereich **Ergebnisse** .</span><span class="sxs-lookup"><span data-stu-id="176ea-149">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="176ea-150">Klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü die Option **Sperren** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-150">Right-click the desired application, and select **Lock** from the pop-up menu.</span></span> <span data-ttu-id="176ea-151">Die ausgewählte Anwendung ist im Cache gesperrt.</span><span class="sxs-lookup"><span data-stu-id="176ea-151">The selected application is locked in the cache.</span></span>

**<span data-ttu-id="176ea-152">So entsperren Sie eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-152">To unlock an application</span></span>**

1.  <span data-ttu-id="176ea-153">Bewegen Sie den Cursor in den Bereich **Ergebnisse** .</span><span class="sxs-lookup"><span data-stu-id="176ea-153">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="176ea-154">Klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **entsperren** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-154">Right-click the desired application, and select **Unlock** from the pop-up menu.</span></span> <span data-ttu-id="176ea-155">Die ausgewählte Anwendung wird im Cache freigegeben und kann entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="176ea-155">The selected application is unlocked in the cache and can be removed.</span></span>

## <span data-ttu-id="176ea-156">So löschen Sie eine App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-156">How to delete an App-V application</span></span>


<span data-ttu-id="176ea-157">Wenn Sie den **Anwendungs** Knoten in der Application Virtualization Client Management Console auswählen, wird im **Ergebnis** Bereich eine Liste der Anwendungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="176ea-157">When you select the **Application** node in the Application Virtualization Client Management Console, the **Results** pane displays a list of applications.</span></span> <span data-ttu-id="176ea-158">Sie können das folgende Verfahren verwenden, um eine Anwendung aus dem **Ergebnis** Bereich zu löschen, wodurch auch die Anwendung aus dem Cache entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="176ea-158">You can use the following procedure to delete an application from the **Results** pane, which also removes the application from the cache.</span></span>

<span data-ttu-id="176ea-159">**Hinweis**  Wenn Sie eine Anwendung löschen, steht die ausgewählte Anwendung nicht mehr für alle Benutzer dieses Clients zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="176ea-159">**Note** When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="176ea-160">Verknüpfungen und Dateitypzuordnungen werden ausgeblendet, und die Anwendung wird aus dem Cache gelöscht.</span><span class="sxs-lookup"><span data-stu-id="176ea-160">Shortcuts and file type associations are hidden, and the application is deleted from cache.</span></span> <span data-ttu-id="176ea-161">Wenn sich eine andere Anwendung jedoch auf Daten in den Dateisystem-Cachedaten für die ausgewählte Anwendung bezieht, werden diese Elemente nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="176ea-161">However, if another application refers to data in the file system cache data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="176ea-162">Nach einer Veröffentlichungsaktualisierung werden die gelöschten Anwendungen wieder zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="176ea-162">After a publishing refresh, the deleted applications will again become available to you.</span></span>

 

**<span data-ttu-id="176ea-163">So löschen Sie eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-163">To delete an application</span></span>**

1.  <span data-ttu-id="176ea-164">Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-164">Move the cursor to the **Results** pane, right-click the desired application, and select **Delete** from the pop-up menu.</span></span>

2.  <span data-ttu-id="176ea-165">Klicken Sie bei der Bestätigungsaufforderung auf **Ja** , um die Anwendung zu entfernen, oder auf **Nein** , um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="176ea-165">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="176ea-166">So ändern Sie ein App-V-Anwendungssymbol</span><span class="sxs-lookup"><span data-stu-id="176ea-166">How to change an App-V application icon</span></span>


<span data-ttu-id="176ea-167">Mit dem folgenden Verfahren können Sie ein Symbol, das der ausgewählten Anwendung zugeordnet ist, direkt aus dem Bereich **Ergebnisse** des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole ändern.</span><span class="sxs-lookup"><span data-stu-id="176ea-167">You can use the following procedure to change an icon associated with the selected application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="176ea-168">So ändern Sie ein Anwendungssymbol</span><span class="sxs-lookup"><span data-stu-id="176ea-168">To change an application icon</span></span>**

1.  <span data-ttu-id="176ea-169">Bewegen Sie den Cursor in den Bereich **Ergebnisse** , und klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="176ea-169">Move the cursor to the **Results** pane, and right-click the desired application.</span></span>

2.  <span data-ttu-id="176ea-170">Wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-170">Select **Properties**.</span></span>

3.  <span data-ttu-id="176ea-171">Klicken Sie auf der Registerkarte **Allgemein** auf **Symbol ändern**.</span><span class="sxs-lookup"><span data-stu-id="176ea-171">On the **General** tab, click **Change Icon**.</span></span>

4.  <span data-ttu-id="176ea-172">Wählen Sie das gewünschte Symbol aus, oder navigieren Sie zu einem anderen Speicherort, um das Symbol auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="176ea-172">Select the desired icon, or browse to another location to select the icon.</span></span> <span data-ttu-id="176ea-173">Nachdem Sie das Symbol ausgewählt haben, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="176ea-173">After you've selected the icon, click **OK**.</span></span> <span data-ttu-id="176ea-174">Das Symbol "neu" wird im **Ergebnis** Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="176ea-174">The new icon appears in the **Results** pane.</span></span>

## <span data-ttu-id="176ea-175">So wird es gemacht: Hinzufügen einer App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-175">How to add an App-V application</span></span>


<span data-ttu-id="176ea-176">Mit dem folgenden Verfahren können Sie eine Anwendung direkt aus dem Bereich **Ergebnisse** des **Anwendungs** Knotens in der Application Virtualization Client Management Console hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="176ea-176">You can use the following procedure to add an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="176ea-177">So fügen Sie eine Anwendung hinzu</span><span class="sxs-lookup"><span data-stu-id="176ea-177">To add an application</span></span>**

1.  <span data-ttu-id="176ea-178">Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste, und wählen Sie im Popupmenü die Option **neue Anwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-178">In the **Results** pane, right-click and select **New Application** from the pop-up menu.</span></span>

2.  <span data-ttu-id="176ea-179">Auf der Seite des Assistenten können Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="176ea-179">On the wizard page, you can perform the following tasks:</span></span>

    1.  <span data-ttu-id="176ea-180">**Symbol "ändern"**– zeigt einen Standardbrowser für Windows-Symbole an.</span><span class="sxs-lookup"><span data-stu-id="176ea-180">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="176ea-181">Navigieren Sie zu dem gewünschten Symbol, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-181">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="176ea-182">**OSD**-Dateipfad oder-URL: Geben Sie einen lokalen absoluten Pfad, einen vollständigen UNC-Pfad (freigegebene Datei oder ein Verzeichnis in einem Netzwerk) oder eine HTTP-URL ein.</span><span class="sxs-lookup"><span data-stu-id="176ea-182">**OSD File Path or URL**—Enter a local absolute path, a full UNC path (shared file or directory on a network), or an HTTP URL.</span></span>

    3.  <span data-ttu-id="176ea-183">**(Schaltfläche "Durchsuchen")**– zeigt das Windows-Standarddialogfeld " **Datei öffnen** " an.</span><span class="sxs-lookup"><span data-stu-id="176ea-183">**(OSD browse button)**—Displays the standard Windows **Open File** dialog box.</span></span> <span data-ttu-id="176ea-184">Navigieren Sie zu der gewünschten Datei.</span><span class="sxs-lookup"><span data-stu-id="176ea-184">Browse to find the desired file.</span></span>

3.  <span data-ttu-id="176ea-185">Klicken Sie auf **Fertig stellen** , um die Anwendung dem **Ergebnis** Bereich hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="176ea-185">Click **Finish** to add the application to the **Results** pane.</span></span>

## <span data-ttu-id="176ea-186">Veröffentlichen einer App-V-Anwendungsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="176ea-186">How to publish an App-V application shortcut</span></span>


<span data-ttu-id="176ea-187">Mit dem folgenden Verfahren können Sie Verknüpfungen zu einer Anwendung direkt im **Ergebnis** Bereich des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="176ea-187">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="176ea-188">So veröffentlichen Sie Anwendungsverknüpfungen</span><span class="sxs-lookup"><span data-stu-id="176ea-188">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="176ea-189">Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü die Option **neue Verknüpfung** aus, um den Assistenten für neue Tastenkombinationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="176ea-189">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="176ea-190">Wählen Sie auf der ersten Seite des Assistenten für neue Tastenkombinationen ein Symbol aus, und geben Sie einen Namen für die Verknüpfung an.</span><span class="sxs-lookup"><span data-stu-id="176ea-190">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="176ea-191">**Symbol "ändern"**– zeigt einen Standardbrowser für Windows-Symbole an.</span><span class="sxs-lookup"><span data-stu-id="176ea-191">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="176ea-192">Navigieren Sie zu dem gewünschten Symbol, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-192">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="176ea-193">**Verknüpfungs Titel**– geben Sie den Namen ein, dem Sie die Tastenkombination zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="176ea-193">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="176ea-194">In diesem Feld wird standardmäßig der vorhandene Name und die Version der Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="176ea-194">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="176ea-195">Ermitteln Sie auf der zweiten Seite des Assistenten den Speicherort der veröffentlichten Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="176ea-195">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="176ea-196">**Desktop**: Aktivieren Sie dieses Kontrollkästchen, um die Verknüpfung auf dem Desktop zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="176ea-196">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="176ea-197">**Die Schnellstartleiste**– aktivieren Sie dieses Kontrollkästchen, um die Verknüpfung auf der Schnellstartleiste zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="176ea-197">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="176ea-198">**Das Menü "Senden an"**: Aktivieren Sie dieses Kontrollkästchen, um die Verknüpfung im Menü **Senden an** zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="176ea-198">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="176ea-199">**Programme im Menü "Start"**– Wenn Sie das Kontrollkästchen **"Start"** aktivieren, wird dieses Feld aktiviert.</span><span class="sxs-lookup"><span data-stu-id="176ea-199">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="176ea-200">Lassen Sie dieses Feld leer, um die Verknüpfung direkt im Stammverzeichnis des Ordners Programme zu veröffentlichen, oder geben Sie einen Ordnernamen oder eine Hierarchie ein, beispielsweise "meine \ _Computer \\office-Anwendungen".</span><span class="sxs-lookup"><span data-stu-id="176ea-200">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="176ea-201">Auf diese Weise erstellte Tastenkombinationen stehen nur für den aktuellen Benutzer zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="176ea-201">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="176ea-202">**Ein anderer Speicherort** und die Schaltfläche " **Durchsuchen** " – Wenn Sie das Kontrollkästchen " **anderer Speicherort** " aktivieren, wird dieses Feld aktiviert.</span><span class="sxs-lookup"><span data-stu-id="176ea-202">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="176ea-203">Geben Sie einen beliebigen gültigen Speicherort auf dem Computer oder einen beliebigen verfügbaren UNC-Pfad (freigegebene Datei oder Verzeichnis in einem Netzwerk) ein.</span><span class="sxs-lookup"><span data-stu-id="176ea-203">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="176ea-204">Die Schaltfläche " **Durchsuchen** " zeigt das Dialogfeld "Windows-Standard **Datei öffnen** " an.</span><span class="sxs-lookup"><span data-stu-id="176ea-204">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="176ea-205">Geben Sie auf der dritten Seite des Assistenten die gewünschten Befehlszeilenparameter ein.</span><span class="sxs-lookup"><span data-stu-id="176ea-205">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="176ea-206">Klicken Sie auf **Fertig stellen** , um die Verknüpfungen zu veröffentlichen und zum Bereich **Ergebnisse** zu beenden.</span><span class="sxs-lookup"><span data-stu-id="176ea-206">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="176ea-207">Hinzufügen einer Dateitypzuordnung für eine App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-207">How to add a file type association for an App-V application</span></span>


<span data-ttu-id="176ea-208">Mit dem folgenden Verfahren können Sie mithilfe des Knotens **Dateitypzuordnungen** in der Application Virtualization Client-Verwaltungskonsole eine Dateitypzuordnung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="176ea-208">You can use the following procedure to add a file type association, using the **File Type Associations** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="176ea-209">So fügen Sie eine Dateitypzuordnung hinzu</span><span class="sxs-lookup"><span data-stu-id="176ea-209">To add a file type association</span></span>**

1.  <span data-ttu-id="176ea-210">Klicken Sie mit der rechten Maustaste auf den Knoten **Dateitypzuordnungen** , und wählen Sie im Popupmenü die Option **neue Zuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-210">Right-click the **File Type Associations** node, and select **New Association** from the pop-up menu.</span></span>

2.  <span data-ttu-id="176ea-211">Führen Sie den ersten Schritt des Dialogfelds aus, indem Sie die folgenden Informationen ausfüllen, und klicken Sie dann auf **weiter**:</span><span class="sxs-lookup"><span data-stu-id="176ea-211">Complete the first step of the dialog box by completing the following information, and then click **Next**:</span></span>

    1.  <span data-ttu-id="176ea-212">**Erweiterung**– geben Sie eine neue Dateinamenerweiterung ein.</span><span class="sxs-lookup"><span data-stu-id="176ea-212">**Extension**—Enter a new file name extension.</span></span> <span data-ttu-id="176ea-213">Dieses Feld ist standardmäßig leer.</span><span class="sxs-lookup"><span data-stu-id="176ea-213">This field is blank by default.</span></span>

    2.  <span data-ttu-id="176ea-214">**Erstellen eines neuen Dateityps mit dieser Beschreibung**– wählen Sie dieses Optionsfeld aus, um eine neue Dateitypen Beschreibung in das aktive Feld einzugeben.</span><span class="sxs-lookup"><span data-stu-id="176ea-214">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="176ea-215">Diese Schaltfläche ist standardmäßig aktiviert, und das aktive Feld ist leer.</span><span class="sxs-lookup"><span data-stu-id="176ea-215">This button is selected by default, and the active field is blank.</span></span>

    3.  <span data-ttu-id="176ea-216">**Diesen Dateityp auf alle Benutzer anwenden**– aktivieren Sie dieses Kontrollkästchen, wenn diese Zuordnung für alle Benutzer Global sein soll.</span><span class="sxs-lookup"><span data-stu-id="176ea-216">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="176ea-217">Standardmäßig ist dieses Kontrollkästchen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="176ea-217">By default, this box is cleared.</span></span>

    4.  <span data-ttu-id="176ea-218">**Diese Erweiterung mit einem vorhandenen Dateityp verknüpfen**– aktivieren Sie dieses Optionsfeld, um die Erweiterung einem vorhandenen Dateityp zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="176ea-218">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="176ea-219">Suchen Sie in der Dropdownliste einen Dateityp aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-219">Pick a file type from the drop-down list.</span></span> <span data-ttu-id="176ea-220">Wenn Sie diese Option auswählen, wird " **weiter** " in " **Fertig stellen**" geändert.</span><span class="sxs-lookup"><span data-stu-id="176ea-220">When you choose this option, **Next** is changed to **Finish**.</span></span>

3.  <span data-ttu-id="176ea-221">Führen Sie den zweiten Schritt des Dialogfelds aus, indem Sie die folgenden Informationen ausfüllen, und klicken Sie dann auf **Fertig stellen** , um zur Client Verwaltungskonsole zurückzukehren:</span><span class="sxs-lookup"><span data-stu-id="176ea-221">Complete the second step of the dialog box by completing the following information, and then click **Finish** to return to the Client Management Console:</span></span>

    1.  <span data-ttu-id="176ea-222">**Symbol "ändern**" – klicken Sie auf diese Schaltfläche, um das Anwendungssymbol zu ändern.</span><span class="sxs-lookup"><span data-stu-id="176ea-222">**Change Icon**—Click this button to change the application icon.</span></span> <span data-ttu-id="176ea-223">Wählen Sie eines der verfügbaren Symbole aus, oder navigieren Sie zu einem neuen Speicherort, und wählen Sie ein Symbol aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-223">Select one of the available icons, or browse to a new location and select an icon.</span></span>

    2.  <span data-ttu-id="176ea-224">**Öffnen von Dateien mit der ausgewählten Anwendung**– aktivieren Sie dieses Optionsfeld, um die Datei mit einer vorhandenen Anwendung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="176ea-224">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="176ea-225">Wählen Sie in der Dropdownliste der verfügbaren Anwendungen eine Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-225">Choose an application from the drop-down list of available applications.</span></span>

    3.  <span data-ttu-id="176ea-226">**Öffnen einer Datei mit der in dieser OSD-Datei beschriebenen Zuordnung**– aktivieren Sie dieses Optionsfeld, um eine OSD-Datei (Open Software Descriptor) anzugeben, die die zum Öffnen der Datei verwendete Anwendung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="176ea-226">**Open file with the association described in this OSD file**—Select this radio button to specify an Open Software Descriptor (OSD) file that determines the application used to open the file.</span></span> <span data-ttu-id="176ea-227">Verwenden Sie die Schaltfläche Durchsuchen, um einen vorhandenen Speicherort auszuwählen, oder geben Sie einen Pfad oder eine HTTP-formatierte URL in dieses Feld ein.</span><span class="sxs-lookup"><span data-stu-id="176ea-227">Use the browse button to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

## <span data-ttu-id="176ea-228">So löschen Sie eine Dateitypzuordnung für eine App-V-Anwendung</span><span class="sxs-lookup"><span data-stu-id="176ea-228">How to delete a file type association for an App-V application</span></span>


<span data-ttu-id="176ea-229">Sie können das folgende Verfahren verwenden, um eine Dateitypzuordnung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="176ea-229">You can use the following procedure to delete a file type association.</span></span> <span data-ttu-id="176ea-230">Der Knoten " **Dateitypzuordnungen** " befindet sich eine Ebene unterhalb des Knotens " **Application Virtualization** " im **Bereich** Bereich.</span><span class="sxs-lookup"><span data-stu-id="176ea-230">The **File Type Associations** node is one level below the **Application Virtualization** node in the **Scope** pane.</span></span> <span data-ttu-id="176ea-231">Wenn Sie diesen Knoten auswählen, wird im **Ergebnis** Bereich eine Liste der Dateitypzuordnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="176ea-231">When you select this node, the **Results** pane displays a list of file type associations.</span></span>

**<span data-ttu-id="176ea-232">So entfernen Sie eine Dateitypzuordnung</span><span class="sxs-lookup"><span data-stu-id="176ea-232">To remove a file type association</span></span>**

1.  <span data-ttu-id="176ea-233">Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste auf die Erweiterung der Dateitypen Zuordnung, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="176ea-233">In the **Results** pane, right-click the extension of the file type association you want to delete.</span></span>

2.  <span data-ttu-id="176ea-234">Wählen Sie im Popupmenü **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="176ea-234">Select **Delete** from the pop-up menu.</span></span>

3.  <span data-ttu-id="176ea-235">Klicken Sie auf **Ja** , um die Zuordnung zu löschen, oder klicken Sie auf **Nein** , um zum **Ergebnis** Bereich zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="176ea-235">Click **Yes** to delete the association, or click **No** to return to the **Results** pane.</span></span>

## <span data-ttu-id="176ea-236">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="176ea-236">Related topics</span></span>


[<span data-ttu-id="176ea-237">Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="176ea-237">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





