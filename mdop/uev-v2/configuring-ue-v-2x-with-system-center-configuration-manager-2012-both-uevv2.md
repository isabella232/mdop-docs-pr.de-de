---
title: Konfigurieren von UE-V 2. x mit System Center Configuration Manager 2012
description: Konfigurieren von UE-V 2. x mit System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810537"
---
# <span data-ttu-id="b00b8-103">Konfigurieren von UE-V 2. x mit System Center Configuration Manager 2012</span><span class="sxs-lookup"><span data-stu-id="b00b8-103">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>


<span data-ttu-id="b00b8-104">Nachdem Sie die Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 oder 2,1 SP1 und die erforderlichen Features installiert haben, muss UE-v konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="b00b8-104">After you install Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 and their required features, UE-V must be configured.</span></span> <span data-ttu-id="b00b8-105">Das UE-v-Konfigurationspaket bietet Administratoren die Möglichkeit, das Feature "Konformitäts Einstellungen" von System Center Configuration Manager 2012 SP1 oder höher zu verwenden, um konsistente Konfigurationen auf Websites anzuwenden, auf denen UE-v und Configuration Manager installiert sind.</span><span class="sxs-lookup"><span data-stu-id="b00b8-105">The UE-V Configuration Pack provides a way for administrators to use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

## <span data-ttu-id="b00b8-106">Unterstützte Features des UE-V-Konfigurationspakets</span><span class="sxs-lookup"><span data-stu-id="b00b8-106">UE-V Configuration Pack supported features</span></span>


<span data-ttu-id="b00b8-107">Das UE-V-Konfigurationspaket enthält Tools, mit denen Sie die folgenden Aufgaben ausführen können:</span><span class="sxs-lookup"><span data-stu-id="b00b8-107">The UE-V Configuration Pack includes tools to perform the following tasks:</span></span>

-   <span data-ttu-id="b00b8-108">Erstellen oder Aktualisieren von Basislinien für die Verteilung von Standort Vorlagen für UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b00b8-108">Create or update UE-V settings location template distribution baselines.</span></span>

    -   <span data-ttu-id="b00b8-109">Definieren von UE-V-Vorlagen für die Registrierung oder Nichtregistrierung</span><span class="sxs-lookup"><span data-stu-id="b00b8-109">Define UE-V templates to be registered or unregistered</span></span>

    -   <span data-ttu-id="b00b8-110">Aktualisieren von Konfigurationselementen und Basisplänen für UE-V-Vorlagen, wenn Vorlagen hinzugefügt oder aktualisiert werden</span><span class="sxs-lookup"><span data-stu-id="b00b8-110">Update UE-V template configuration items and baselines as templates are added or updated</span></span>

    -   <span data-ttu-id="b00b8-111">Verteilen und Registrieren von UE-V-Vorlagen mithilfe der standardmäßigen Konfigurationselement Bereinigung</span><span class="sxs-lookup"><span data-stu-id="b00b8-111">Distribute and register UE-V templates using standard Configuration Item remediation</span></span>

-   <span data-ttu-id="b00b8-112">Erstellen oder aktualisieren Sie ein UE-V-Agent-Richtlinien Konfigurationselement, um diese Einstellungen festzulegen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b00b8-112">Create or update a UE-V Agent policy configuration item to set or clear these settings.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b00b8-113">Maximale Paketgröße</span><span class="sxs-lookup"><span data-stu-id="b00b8-113">Max package size</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-114">Aktivieren/Deaktivieren der Windows-App-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="b00b8-114">Enable/disable Windows app sync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-115">Auf Synchronisierung beim Anwendungsstart warten</span><span class="sxs-lookup"><span data-stu-id="b00b8-115">Wait for sync on application start</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b00b8-116">Festlegen der Import Verzögerung</span><span class="sxs-lookup"><span data-stu-id="b00b8-116">Setting import delay</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-117">Synchronisieren nicht aufgelisteter Windows-apps</span><span class="sxs-lookup"><span data-stu-id="b00b8-117">Sync unlisted Windows apps</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-118">Auf die Synchronisierung bei der Anmeldung warten</span><span class="sxs-lookup"><span data-stu-id="b00b8-118">Wait for sync on logon</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b00b8-119">Benachrichtigung zum Importieren von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b00b8-119">Settings import notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-120">IT-Kontakt-URL</span><span class="sxs-lookup"><span data-stu-id="b00b8-120">IT contact URL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-121">Auf Synchronisierungs Timeout warten</span><span class="sxs-lookup"><span data-stu-id="b00b8-121">Wait for sync timeout</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b00b8-122">Speicherpfad für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b00b8-122">Settings storage path</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-123">Sie wenden sich an einen beschreibenden Text</span><span class="sxs-lookup"><span data-stu-id="b00b8-123">IT contact descriptive text</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-124">Katalogpfad für Einstellungs Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b00b8-124">Settings template catalog path</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b00b8-125">Synchronisierungs Aktivierung</span><span class="sxs-lookup"><span data-stu-id="b00b8-125">Sync enablement</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-126">Taskleistensymbol aktiviert</span><span class="sxs-lookup"><span data-stu-id="b00b8-126">Tray icon enabled</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-127">Starten/Beenden des UE-V-Agent-Diensts</span><span class="sxs-lookup"><span data-stu-id="b00b8-127">Start/Stop UE-V agent service</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b00b8-128">Sync-Methode</span><span class="sxs-lookup"><span data-stu-id="b00b8-128">Sync method</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-129">Benachrichtigung zur ersten Verwendung</span><span class="sxs-lookup"><span data-stu-id="b00b8-129">First use notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b00b8-130">Definieren, welche Windows-apps Roaming-Einstellungen durchführen</span><span class="sxs-lookup"><span data-stu-id="b00b8-130">Define which Windows apps will roam settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b00b8-131">Synchronisierungs Timeout</span><span class="sxs-lookup"><span data-stu-id="b00b8-131">Sync timeout</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="b00b8-132">Überprüfen Sie die Kompatibilität, indem Sie bestätigen, dass UE-V ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b00b8-132">Verify compliance by confirming that UE-V is running.</span></span>

## <span data-ttu-id="b00b8-133">Generieren eines UE-V-Agentenrichtlinien-Konfigurationselements</span><span class="sxs-lookup"><span data-stu-id="b00b8-133">Generate a UE-V Agent Policy Configuration Item</span></span>


<span data-ttu-id="b00b8-134">Alle UE-V-Agentenrichtlinien und-Konfigurationen werden über ein einzelnes Konfigurationselement verteilt, das mit dem UevAgentPolicyGenerator.exe-Tool generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b00b8-134">All UE-V Agent policy and configuration is distributed through a single configuration item that is generated using the UevAgentPolicyGenerator.exe tool.</span></span> <span data-ttu-id="b00b8-135">Dieses Tool liest die gewünschte Konfiguration aus einer XML-Konfigurationsdatei und erstellt eine CI, die die Einstellungen für Ermittlung und Behebung enthält, die erforderlich sind, um den Computer in die Konformität zu bringen.</span><span class="sxs-lookup"><span data-stu-id="b00b8-135">This tool reads the desired configuration from an XML configuration file and creates a CI containing the discovery and remediation settings needed to bring the machine into compliance.</span></span>

<span data-ttu-id="b00b8-136">Die CAB-Datei für das UE-V-Agent-Richtlinien Konfigurationselement wird mithilfe des Befehlszeilentools UevTemplateBaselineGenerator.exe erstellt, das die folgenden Parameter aufweist:</span><span class="sxs-lookup"><span data-stu-id="b00b8-136">The UE-V Agent policy configuration item CAB file is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="b00b8-137">Website-Website &lt; Code&gt;</span><span class="sxs-lookup"><span data-stu-id="b00b8-137">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="b00b8-138">Richtlinien &lt; Name &gt; -Name optional: standardmäßig "UE-V-Agent-Richtlinie", wenn nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="b00b8-138">PolicyName &lt;name&gt; Optional: Defaults to “UE-V Agent Policy” if not present</span></span>

-   <span data-ttu-id="b00b8-139">PolicyDescription &lt; Beschreibung &gt; Optional: eine Beschreibung wird bereitgestellt, wenn Sie nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b00b8-139">PolicyDescription &lt;description&gt; Optional: A description is provided if not present</span></span>

-   <span data-ttu-id="b00b8-140">CabFilePath &lt; Vollständiger Pfad zum Konfigurationselement. CAB-Datei&gt;</span><span class="sxs-lookup"><span data-stu-id="b00b8-140">CabFilePath &lt;full path to configuration item .CAB file&gt;</span></span>

-   <span data-ttu-id="b00b8-141">Konfigurations &lt; Datei, vollständiger Pfad zur XML-Konfigurationsdatei für Agents&gt;</span><span class="sxs-lookup"><span data-stu-id="b00b8-141">ConfigurationFile &lt;full path to agent configuration XML file&gt;</span></span>

<span data-ttu-id="b00b8-142">**Hinweis**  Es kann erforderlich sein, die PowerShell-Ausführungsrichtlinie so zu ändern, dass diese Skripts in Ihrer Umgebung ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="b00b8-142">**Note** It might be necessary to change the PowerShell execution policy to allow these scripts to run in your environment.</span></span> <span data-ttu-id="b00b8-143">Führen Sie die folgenden Schritte in der Configuration Manager-Konsole aus:</span><span class="sxs-lookup"><span data-stu-id="b00b8-143">Perform these steps in the Configuration Manager console:</span></span>

1.  <span data-ttu-id="b00b8-144">Auswählen von Einstellungen für den \*\*Administrations &gt; Client &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="b00b8-144">Select **Administration &gt; Client Settings &gt; Properties**</span></span>

2.  <span data-ttu-id="b00b8-145">Setzen Sie auf der Registerkarte **Benutzer-Agent** die **PowerShell-Ausführungsrichtlinie** auf **Bypass**</span><span class="sxs-lookup"><span data-stu-id="b00b8-145">In the **User Agent** tab, set the **PowerShell Execution Policy** to **Bypass**</span></span>

<a href="" id="create"></a>**<span data-ttu-id="b00b8-146">Erstellen des ersten UE-V-Richtlinien Konfigurationselements</span><span class="sxs-lookup"><span data-stu-id="b00b8-146">Create the First UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="b00b8-147">Kopieren Sie die Konfigurationsdatei für die Standardeinstellungen aus dem Installationsverzeichnis des UE-V config Packs an einen Speicherort, der für Ihre ConfigMgr-Verwaltungskonsole sichtbar ist:</span><span class="sxs-lookup"><span data-stu-id="b00b8-147">Copy the default settings configuration file from the UE-V Config Pack installation directory to a location visible to your ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    <span data-ttu-id="b00b8-148">Die Standardkonfigurationsdatei enthält fünf Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="b00b8-148">The default configuration file contains five sections:</span></span>

    <a href="" id="computer-policy"></a>**<span data-ttu-id="b00b8-149">Computer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b00b8-149">Computer Policy</span></span>**  
    <span data-ttu-id="b00b8-150">Alle UE-V-Einstellungen auf Computerebene.</span><span class="sxs-lookup"><span data-stu-id="b00b8-150">All UE-V machine level settings.</span></span> <span data-ttu-id="b00b8-151">Das DesiredState-Attribut kann</span><span class="sxs-lookup"><span data-stu-id="b00b8-151">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="b00b8-152">So **eingestellt** , dass der Wert in der Registrierung zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="b00b8-152">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="b00b8-153">**Löschen** , um die Einstellung zu entfernen</span><span class="sxs-lookup"><span data-stu-id="b00b8-153">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="b00b8-154">**Nicht verwaltet** , damit das Konfigurationselement in seinem aktuellen Zustand bleibt</span><span class="sxs-lookup"><span data-stu-id="b00b8-154">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="b00b8-155">Entfernen Sie keine Zeilen aus diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="b00b8-155">Do not remove lines from this section.</span></span> <span data-ttu-id="b00b8-156">Legen Sie die DesiredState stattdessen auf "nicht verwaltet", wenn Sie nicht möchten, dass der Configuration Manager aktuelle oder Standardwerte ändert.</span><span class="sxs-lookup"><span data-stu-id="b00b8-156">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="currentcomputeruserpolicy"></a>**<span data-ttu-id="b00b8-157">CurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="b00b8-157">CurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="b00b8-158">Alle UE-V-Einstellungen auf Benutzerebene</span><span class="sxs-lookup"><span data-stu-id="b00b8-158">All UE-V user level settings.</span></span> <span data-ttu-id="b00b8-159">Diese Einträge überschreiben die Computereinstellungen für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b00b8-159">These entries override the machine settings for a user.</span></span> <span data-ttu-id="b00b8-160">Das DesiredState-Attribut kann</span><span class="sxs-lookup"><span data-stu-id="b00b8-160">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="b00b8-161">So **eingestellt** , dass der Wert in der Registrierung zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="b00b8-161">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="b00b8-162">**Löschen** , um die Einstellung zu entfernen</span><span class="sxs-lookup"><span data-stu-id="b00b8-162">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="b00b8-163">**Nicht verwaltet** , damit das Konfigurationselement in seinem aktuellen Zustand bleibt</span><span class="sxs-lookup"><span data-stu-id="b00b8-163">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="b00b8-164">Entfernen Sie keine Zeilen aus diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="b00b8-164">Do not remove lines from this section.</span></span> <span data-ttu-id="b00b8-165">Legen Sie die DesiredState stattdessen auf "nicht verwaltet", wenn Sie nicht möchten, dass der Configuration Manager aktuelle oder Standardwerte ändert.</span><span class="sxs-lookup"><span data-stu-id="b00b8-165">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="services"></a>**<span data-ttu-id="b00b8-166">Dienste</span><span class="sxs-lookup"><span data-stu-id="b00b8-166">Services</span></span>**  
    <span data-ttu-id="b00b8-167">Einträge in diesem Abschnitt Steuern des Dienstvorgangs.</span><span class="sxs-lookup"><span data-stu-id="b00b8-167">Entries in this section control service operation.</span></span> <span data-ttu-id="b00b8-168">Die Standardkonfigurationsdatei enthält einen einzelnen Eintrag für die UevAgentService-Datei.</span><span class="sxs-lookup"><span data-stu-id="b00b8-168">The default configuration file contains a single entry for the UevAgentService.</span></span> <span data-ttu-id="b00b8-169">Das DesiredState-Attribut kann auf **Running** oder **Stopped**eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b00b8-169">The DesiredState attribute can be set to **Running** or **Stopped**.</span></span>

    <a href="" id="windows8appscomputerpolicy"></a>**<span data-ttu-id="b00b8-170">Windows8AppsComputerPolicy</span><span class="sxs-lookup"><span data-stu-id="b00b8-170">Windows8AppsComputerPolicy</span></span>**  
    <span data-ttu-id="b00b8-171">Alle Synchronisierungseinstellungen für Windows-App auf Computerebene.</span><span class="sxs-lookup"><span data-stu-id="b00b8-171">All machine level Windows app synchronization settings.</span></span> <span data-ttu-id="b00b8-172">Jedem in diesem Abschnitt aufgelisteten PackageFamilyName kann eine DesiredState von zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b00b8-172">Each PackageFamilyName listed in this section can be assigned a DesiredState of</span></span>

    -   <span data-ttu-id="b00b8-173">**Aktiviert** , um die Einstellungen zu durchlaufen</span><span class="sxs-lookup"><span data-stu-id="b00b8-173">**Enabled** to have settings roam</span></span>

    -   <span data-ttu-id="b00b8-174">**Deaktiviert** , um zu verhindern, dass Roaming-Einstellungen durchlaufen werden</span><span class="sxs-lookup"><span data-stu-id="b00b8-174">**Disabled** to prevent settings from roaming</span></span>

    -   <span data-ttu-id="b00b8-175">**Gelöscht** , damit der Eintrag aus dem UE-V-Steuerelement entfernt wird</span><span class="sxs-lookup"><span data-stu-id="b00b8-175">**Cleared** to have the entry removed from UE-V control</span></span>

    <span data-ttu-id="b00b8-176">In diesem Abschnitt können zusätzliche Zeilen basierend auf der Liste der installierten Windows-apps hinzugefügt werden, die mit dem PowerShell-Cmdlet GetAppxPackage angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="b00b8-176">Additional lines can be added to this section based on the list of installed Windows apps that can be viewed using the PowerShell cmdlet GetAppxPackage.</span></span>

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**<span data-ttu-id="b00b8-177">Windows8AppsCurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="b00b8-177">Windows8AppsCurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="b00b8-178">Identisch mit dem Windows8AppsComputerPolicy mit Einstellungen, die die Computereinstellungen für einen einzelnen Benutzer außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="b00b8-178">Identical to the Windows8AppsComputerPolicy with settings that override machine settings for an individual user.</span></span>

2.  <span data-ttu-id="b00b8-179">Bearbeiten Sie die Konfigurationsdatei, indem Sie die Felder für den gewünschten Zustand und die Werte ändern.</span><span class="sxs-lookup"><span data-stu-id="b00b8-179">Edit the configuration file by changing the desired state and value fields.</span></span>

3.  <span data-ttu-id="b00b8-180">Führen Sie diesen Befehl auf einem Computer aus, auf dem die ConfigMgr-Verwaltungskonsole ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="b00b8-180">Run this command on a machine running the ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  <span data-ttu-id="b00b8-181">Importieren der CAB-Datei mithilfe der ConfigMgr-Konsole oder des PowerShell-Import-CMConfigurationItem</span><span class="sxs-lookup"><span data-stu-id="b00b8-181">Import the CAB file using ConfigMgr console or PowerShell Import-CMConfigurationItem</span></span>

**<span data-ttu-id="b00b8-182">Aktualisieren eines UE-V-Richtlinien Konfigurationselements</span><span class="sxs-lookup"><span data-stu-id="b00b8-182">Update a UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="b00b8-183">Bearbeiten Sie die Konfigurationsdatei, indem Sie die Felder für den gewünschten Zustand und die Werte ändern.</span><span class="sxs-lookup"><span data-stu-id="b00b8-183">Edit the configuration file by changing the desired state and value fields.</span></span>

2.  <span data-ttu-id="b00b8-184">Führen Sie den Befehl aus Schritt 3 in [Erstellen des ersten UE-V-Richtlinien Konfigurationselements](#create)aus.</span><span class="sxs-lookup"><span data-stu-id="b00b8-184">Run the command from Step 3 in [Create the First UE-V Policy Configuration Item](#create).</span></span> <span data-ttu-id="b00b8-185">Wenn Sie den Namen mit dem Parameter PolicyName geändert haben, stellen Sie sicher, dass Sie denselben Namen eingeben.</span><span class="sxs-lookup"><span data-stu-id="b00b8-185">If you changed the name with the PolicyName parameter, make sure you enter the same name.</span></span>

3.  <span data-ttu-id="b00b8-186">Importieren Sie die CAB-Datei erneut.</span><span class="sxs-lookup"><span data-stu-id="b00b8-186">Reimport the CAB file.</span></span> <span data-ttu-id="b00b8-187">Die Version in ConfigMgr wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b00b8-187">The version in ConfigMgr will be updated.</span></span>

## <span data-ttu-id="b00b8-188">Erstellen einer UE-V-Vorlagen Basislinie</span><span class="sxs-lookup"><span data-stu-id="b00b8-188">Generate a UE-V Template Baseline</span></span>
<span data-ttu-id="b00b8-189">UE-V-Vorlagen werden mithilfe einer Baseline verteilt, die mehrere Konfigurationselemente enthält.</span><span class="sxs-lookup"><span data-stu-id="b00b8-189">UE-V templates are distributed using a baseline containing multiple configuration items.</span></span> <span data-ttu-id="b00b8-190">Jedes Konfigurationselement enthält die Ermittlungs-und Korrekturskripts, die zum Installieren einer UE-V-Vorlage erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b00b8-190">Each configuration item contains the discovery and remediation scripts needed to install one UE-V template.</span></span> <span data-ttu-id="b00b8-191">Die tatsächliche UE-V-Vorlage wird in das Behebungs Skript für die Verteilung unter Verwendung der Standardfunktionalität für Konfigurationselemente eingebettet.</span><span class="sxs-lookup"><span data-stu-id="b00b8-191">The actual UE-V template is embedded within the remediation script for distribution using standard Configuration Item functionality.</span></span>

<span data-ttu-id="b00b8-192">Der Basisplan der UE-V-Vorlage wird mithilfe des Befehlszeilentools UevTemplateBaselineGenerator.exe erstellt, das die folgenden Parameter aufweist:</span><span class="sxs-lookup"><span data-stu-id="b00b8-192">The UE-V template baseline is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="b00b8-193">Website-Website &lt; Code&gt;</span><span class="sxs-lookup"><span data-stu-id="b00b8-193">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="b00b8-194">Baselinename &lt; &gt; -Name (optional: standardmäßig "UE-V-Vorlagen Verteilungs Basisplan", wenn nicht vorhanden)</span><span class="sxs-lookup"><span data-stu-id="b00b8-194">BaselineName &lt;name&gt; (Optional: defaults to “UE-V Template Distribution Baseline” if not present)</span></span>

-   <span data-ttu-id="b00b8-195">BaselineDescription &lt; Beschreibung &gt; (optional: eine Beschreibung wird bereitgestellt, wenn nicht vorhanden)</span><span class="sxs-lookup"><span data-stu-id="b00b8-195">BaselineDescription &lt;description&gt; (Optional: a description is provided if not present)</span></span>

-   <span data-ttu-id="b00b8-196">TemplateFolder &lt; UE-V-Vorlagenordner&gt;</span><span class="sxs-lookup"><span data-stu-id="b00b8-196">TemplateFolder &lt;UE-V template folder&gt;</span></span>

-   <span data-ttu-id="b00b8-197">Registrieren einer durch &lt; Kommas getrennten Vorlagendatei Liste&gt;</span><span class="sxs-lookup"><span data-stu-id="b00b8-197">Register &lt;comma separated template file list&gt;</span></span>

-   <span data-ttu-id="b00b8-198">Aufheben der Registrierung der Liste der durch &lt; Kommas getrennten Vorlagen&gt;</span><span class="sxs-lookup"><span data-stu-id="b00b8-198">Unregister &lt;comma separated template list&gt;</span></span>

-   <span data-ttu-id="b00b8-199">CabFilePath &lt; Vollständiger Pfad zur zu Generier-Baseline-CAB-Datei&gt;</span><span class="sxs-lookup"><span data-stu-id="b00b8-199">CabFilePath &lt;Full path to baseline CAB file to generate&gt;</span></span>

<span data-ttu-id="b00b8-200">Das Ergebnis ist eine Baseline-CAB-Datei, die in Configuration Manager importiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b00b8-200">The result is a baseline CAB file that is ready for import into Configuration Manager.</span></span> <span data-ttu-id="b00b8-201">Wenn Sie zu einem späteren Zeitpunkt eine Vorlage aktualisieren oder hinzufügen, können Sie den Befehl mit dem gleichen Basisplan erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="b00b8-201">If at a future date, you update or add a template, you can rerun the command using the same baseline name.</span></span> <span data-ttu-id="b00b8-202">Beim Importieren der CAB-Version werden die geänderten Vorlagen in CI-Versionsupdates angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b00b8-202">Importing the CAB results in CI version updates on the changed templates.</span></span>

### <a href="" id="create2"></a><span data-ttu-id="b00b8-203">Erstellen des ersten Basisplans für die UE-V-Vorlage</span><span class="sxs-lookup"><span data-stu-id="b00b8-203">Create the First UE-V Template Baseline</span></span>

1.  <span data-ttu-id="b00b8-204">Erstellen Sie einen "Master"-Satz von UE-V-Vorlagen in einem stabilen Ordnerspeicherort, der auf dem Computer sichtbar ist, auf dem Ihre ConfigMgr-Verwaltungskonsole ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b00b8-204">Create a “master” set of UE-V templates in a stable folder location visible to the machine running your ConfigMgr Admin Console.</span></span> <span data-ttu-id="b00b8-205">Wenn Vorlagen hinzugefügt oder aktualisiert werden, wird dieser Ordner für die Verteilung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b00b8-205">As templates are added or updated, this folder is where they are pulled for distribution.</span></span> <span data-ttu-id="b00b8-206">Die erste Liste der Vorlagen kann von einem Computer kopiert werden, auf dem UE-V installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b00b8-206">The initial list of templates can be copied from a machine with UE-V installed.</span></span> <span data-ttu-id="b00b8-207">Der Standardspeicherort für Vorlagen ist c:\\Programme c:\\Programme\\Microsoft-Benutzeroberfläche Virtualization\\Templates.</span><span class="sxs-lookup"><span data-stu-id="b00b8-207">The default template location is C:\\Program Files\\Microsoft User Experience Virtualization\\Templates.</span></span>

2.  <span data-ttu-id="b00b8-208">Erstellen Sie eine text.bat-Datei, in der Sie den Befehl Vorlagen Generator hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="b00b8-208">Create a text.bat file where you can add the template generator command.</span></span> <span data-ttu-id="b00b8-209">Dies ist optional, bewirkt aber eine einfachere Regenerierung, wenn Sie die Befehlsparameter speichern.</span><span class="sxs-lookup"><span data-stu-id="b00b8-209">This is optional, but will make regeneration simpler if you save the command parameters.</span></span>

3.  <span data-ttu-id="b00b8-210">Fügen Sie der bat-Datei den Befehl und die Parameter hinzu, die den Basisplan generieren soll.</span><span class="sxs-lookup"><span data-stu-id="b00b8-210">Add the command and parameters to the .bat file that will generate the baseline.</span></span> <span data-ttu-id="b00b8-211">Im folgenden Beispiel wird ein Basisplan erstellt, der Notepad und Calculator verteilt:</span><span class="sxs-lookup"><span data-stu-id="b00b8-211">The following example creates a baseline that distributes Notepad and Calculator:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  <span data-ttu-id="b00b8-212">Führen Sie die bat-Datei aus, um UevTemplateBaseline.cab bereit für den Import in Configuration Manager zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b00b8-212">Run the .bat file to create UevTemplateBaseline.cab ready for import into Configuration Manager.</span></span>

### <span data-ttu-id="b00b8-213">Aktualisieren einer UE-V-Vorlagen Basislinie</span><span class="sxs-lookup"><span data-stu-id="b00b8-213">Update a UE-V Template Baseline</span></span>

<span data-ttu-id="b00b8-214">Der Vorlagen Generator verwendet die Vorlagenversion, um zu ermitteln, ob eine Vorlage aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b00b8-214">The template generator uses the template version to determine if a template should be updated.</span></span> <span data-ttu-id="b00b8-215">Wenn Sie eine Vorlage ändern und die Version aktualisieren, vergleicht der Baseline-Generator die Vorlage im Masterordner mit der Vorlage, die in der CI auf dem ConfigMgr-Server enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b00b8-215">If you make a template change and update the version, the baseline generator compares the template in your master folder with the template contained in the CI on the ConfigMgr server.</span></span> <span data-ttu-id="b00b8-216">Wenn ein Unterschied gefunden wird, werden die generierten Baseline-und modified-CI-Versionen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b00b8-216">If a difference is found, the generated baseline and modified CI versions are updated.</span></span>

<span data-ttu-id="b00b8-217">Wenn Sie eine neue Notizblock Vorlage verteilen möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="b00b8-217">To distribute a new Notepad template, you would perform these steps:</span></span>

1.  <span data-ttu-id="b00b8-218">Aktualisieren Sie die Vorlage und die Vorlagenversion, die sich im &lt; Version- &gt; Element der Vorlage befindet.</span><span class="sxs-lookup"><span data-stu-id="b00b8-218">Update the template and template version located in the &lt;Version&gt; element of the template.</span></span>

2.  <span data-ttu-id="b00b8-219">Kopieren Sie die Vorlage in das Mastervorlagen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b00b8-219">Copy the template to your master template directory.</span></span>

3.  <span data-ttu-id="b00b8-220">Führen Sie den Befehl in der bat-Datei aus, die Sie in Schritt 3 unter [Erstellen der ersten UE-V-Vorlagen Basislinie](#create2)erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b00b8-220">Run the command in the .bat file that you created in Step 3 in [Create the First UE-V Template Baseline](#create2).</span></span>

4.  <span data-ttu-id="b00b8-221">Importieren Sie die generierte CAB-Datei mithilfe der Konsole oder PowerShell-Import-CMBaseline in ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="b00b8-221">Import the generated CAB file into ConfigMgr using the console or PowerShell Import-CMBaseline.</span></span>

## <span data-ttu-id="b00b8-222">Abrufen des UE-V-Konfigurationspakets</span><span class="sxs-lookup"><span data-stu-id="b00b8-222">Get the UE-V Configuration Pack</span></span>


<span data-ttu-id="b00b8-223">Das UE-V-Konfigurationspaket für Configuration Manager 2012 SP1 oder höher kann [hier](https://go.microsoft.com/fwlink/?LinkId=317263)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="b00b8-223">The UE-V Configuration Pack for Configuration Manager 2012 SP1 or later can be downloaded [here](https://go.microsoft.com/fwlink/?LinkId=317263).</span></span>






## <span data-ttu-id="b00b8-224">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b00b8-224">Related topics</span></span>


[<span data-ttu-id="b00b8-225">Verwalten von Konfigurationen für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="b00b8-225">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





