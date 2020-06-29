---
title: So richten Sie Skriptaktionen ein
description: So richten Sie Skriptaktionen ein
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804190"
---
# <span data-ttu-id="44231-103">So richten Sie Skriptaktionen ein</span><span class="sxs-lookup"><span data-stu-id="44231-103">How to Set Up Script Actions</span></span>


<span data-ttu-id="44231-104">Der Skript Aktions-Editor ermöglicht es dem Administrator, Aktionen zu erstellen, die während der Einrichtung des MED-V-Arbeitsbereichs durchgeführt werden sollen, sowie die Reihenfolge zu definieren, in der Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="44231-104">The script actions editor allows the administrator to create actions to be performed during MED-V workspace setup, as well as to define the order in which they are performed.</span></span>

<span data-ttu-id="44231-105">Im folgenden finden Sie eine Liste der Aktionen, die dem Domänen Setupskript hinzugefügt werden können:</span><span class="sxs-lookup"><span data-stu-id="44231-105">The following is a list of actions that can be added to the domain setup script:</span></span>

-   <span data-ttu-id="44231-106">**Windows neu starten**– starten Sie Windows neu.</span><span class="sxs-lookup"><span data-stu-id="44231-106">**Restart Windows**—Restart Windows.</span></span>

-   <span data-ttu-id="44231-107">**Beitreten**zu einer Domäne: Fügen Sie bei der Teilnahme an einer Domäne diese Aktion ein, und konfigurieren Sie den Benutzernamen, das Kennwort, den vollqualifizierten Domänennamen, den NetBIOS-Domänennamen und die Organisationseinheit (optional).</span><span class="sxs-lookup"><span data-stu-id="44231-107">**Join Domain**—If joining a domain, include this action and configure the user name, password, fully qualified domain name, NetBIOS domain name, and organization unit (optional).</span></span>

-   <span data-ttu-id="44231-108">**Überprüfen der Konnektivität**– konfigurieren Sie einen Server für die Verbindung, und überprüfen Sie, ob der MED-V-Arbeitsbereich eine Verbindung mit einer Netzwerkressource (wie dem Domänenserver) herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="44231-108">**Check Connectivity**—Configure a server to connect to and verify that the MED-V workspace can connect to a network resource (such as the domain server).</span></span>

-   <span data-ttu-id="44231-109">**Befehlszeile**– konfigurieren Sie ein Skript im MED-V-Arbeitsbereich, und geben Sie eine Befehlszeile mit dem Pfad des Skripts und den Skript Argumenten ein.</span><span class="sxs-lookup"><span data-stu-id="44231-109">**Command Line**—Configure a script in the MED-V workspace, and enter a command line that includes the path of the script and the script arguments.</span></span>

-   <span data-ttu-id="44231-110">**Computer umbenennen**– benennen Sie den virtuellen Computer basierend auf den definierten Einstellungen um.</span><span class="sxs-lookup"><span data-stu-id="44231-110">**Rename Computer**—Rename the virtual machine computer based on the defined settings.</span></span>

-   <span data-ttu-id="44231-111">**Deaktivieren der automatischen Anmeldung**: Deaktivieren Sie die automatische Windows-Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="44231-111">**Disable Auto-Logon**—Disable Windows Auto-Logon.</span></span> <span data-ttu-id="44231-112">Diese Aktion sollte am Ende der Skripts hinzugefügt werden, mit denen der Computer der Domäne hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="44231-112">This action should be added at the end of scripts that add the computer to the domain.</span></span>

## <a href="" id="how-to-set-up-script-actions-"></a><span data-ttu-id="44231-113">So richten Sie Skriptaktionen ein</span><span class="sxs-lookup"><span data-stu-id="44231-113">How to Set Up Script Actions</span></span>


**<span data-ttu-id="44231-114">So richten Sie Skriptaktionen ein</span><span class="sxs-lookup"><span data-stu-id="44231-114">To set up script actions</span></span>**

1.  <span data-ttu-id="44231-115">Klicken Sie auf der Registerkarte **VM-Setup** auf **Skript-Editor**.</span><span class="sxs-lookup"><span data-stu-id="44231-115">On the **VM Setup** tab, click **Script Editor**.</span></span>

2.  <span data-ttu-id="44231-116">Klicken Sie im Dialogfeld **Skriptaktionen** auf **Hinzufügen**, und klicken Sie im Untermenü auf die gewünschten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="44231-116">In the **Script Actions** dialog box, click **Add**, and on the submenu, click the desired actions.</span></span>

3.  <span data-ttu-id="44231-117">Konfigurieren Sie die Aktionen wie in den folgenden Tabellen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="44231-117">Configure the actions as described in the following tables.</span></span>

    <span data-ttu-id="44231-118">**Hinweis** 
     **Computer umbenennen** ist auf der Registerkarte **VM-Einstellungen** konfiguriert. Weitere Informationen finden Sie unter [Konfigurieren von Eigenschaften des VM-Computer namens Musters](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="44231-118">**Note**
**Rename Computer** is configured in the **VM Settings** tab. For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. <span data-ttu-id="44231-119">Legen Sie die Reihenfolge der Aktionen fest, indem Sie eine Aktion auswählen und auf nach **oben** oder **unten**klicken.</span><span class="sxs-lookup"><span data-stu-id="44231-119">Set the order of the actions by selecting an action and clicking **Up** or **Down**.</span></span>

5. <span data-ttu-id="44231-120">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="44231-120">Click **OK**.</span></span>

**<span data-ttu-id="44231-121">Hinweis</span><span class="sxs-lookup"><span data-stu-id="44231-121">Note</span></span>**  
<span data-ttu-id="44231-122">Wenn Sie das Skript für die Join-Domäne ausführen und das Skript funktionieren soll, muss der Benutzer, der sich beim virtuellen Computer des MED-V-Arbeitsbereichs angemeldet hat, über lokale Administratorrechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="44231-122">When running the Join Domain script, for the script to work, the user logged into the MED-V workspace virtual machine must have local administrator rights.</span></span>



**<span data-ttu-id="44231-123">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="44231-123">Note</span></span>**  
<span data-ttu-id="44231-124">Beim Ausführen des Skripts zum Deaktivieren der automatischen Anmeldung wird empfohlen, das für die automatische Anmeldung verwendete lokale Gastkonto zu deaktivieren, sobald die anfängliche Einrichtung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="44231-124">When running the Disable Auto-Logon script, it is recommended to disable the local guest account used for the auto-logon once the initial setup is complete.</span></span>



### <a href="" id="bkmk-joindomainproperties"></a>

**<span data-ttu-id="44231-125">Domäneneigenschaften beitreten</span><span class="sxs-lookup"><span data-stu-id="44231-125">Join Domain Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44231-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44231-126">Property</span></span></th>
<th align="left"><span data-ttu-id="44231-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44231-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-128">Zu verwendende Anmeldeinformationen, wenn Sie den virtuellen Computer zur Domäne hinzugefügt haben</span><span class="sxs-lookup"><span data-stu-id="44231-128">Credentials to use when joining the VM to the domain</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-129">Wählen Sie eine der folgenden Anmeldeinformationen aus, die Sie verwenden können, wenn Sie den virtuellen Computer zur Domäne hinzugefügt haben:</span><span class="sxs-lookup"><span data-stu-id="44231-129">Select one of the following credentials to use when joining the VM to the domain:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="44231-130">Verwenden Sie MED-V-Anmeldeinformationen </strong> – die Anmeldeinformationen für Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="44231-130">Use MED-V credentials</strong>—The end-user credentials.</span></span></p></li>
<li><p><strong><span data-ttu-id="44231-131">Verwenden Sie die folgenden Anmeldeinformationen </strong> – die angegebenen Anmeldeinformationen; geben Sie einen Benutzernamen und ein Kennwort in die entsprechenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="44231-131">Use the following credentials</strong>—The credentials specified; enter a user name and password in the corresponding fields.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="44231-132">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="44231-132">Note</span></span></strong><br/><p><span data-ttu-id="44231-133">Die von Ihnen eingegebenen Anmeldeinformationen sind für alle MED-V Workspace-Benutzer sichtbar.</span><span class="sxs-lookup"><span data-stu-id="44231-133">The credentials you enter are visible to all MED-V workspace users.</span></span> <span data-ttu-id="44231-134">Es wird nicht empfohlen, Domänenadministrator-Anmeldeinformationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="44231-134">It is not recommended to provide domain administrator credentials.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44231-135">Domäne für den Beitritt</span><span class="sxs-lookup"><span data-stu-id="44231-135">Domain to join</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-136">Wählen Sie eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="44231-136">Select one of the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="44231-137">Verwenden Sie den beim Starten des Arbeitsbereichs verwendeten Domänennamen </strong> – nehmen Sie an der Domäne Teil, die vom Endbenutzer beim Anmelden beim MED-V-Client eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="44231-137">Use the domain name utilized in starting the Workspace</strong>—Join the domain entered by the end user when logging into the MED-V client.</span></span></p>
<p><span data-ttu-id="44231-138">Klicken Sie auf <strong> globale Domänenzuordnungstabelle, um die Zuordnung von NetBIOS zu vollqualifizierten Domänennamen zu definieren </strong> .</span><span class="sxs-lookup"><span data-stu-id="44231-138">To define the mapping from NetBIOS to fully qualified domain names, click <strong>Global domain mapping table</strong>.</span></span> <span data-ttu-id="44231-139">Klicken Sie in der Tabelle globale Domänenzuordnung auf <strong> Hinzufügen </strong> , geben Sie einen <strong> NetBIOS-Domänennamen </strong> und einen <strong> vollqualifizierten Domänennamen ein </strong> , und klicken Sie auf <strong> OK </strong> .</span><span class="sxs-lookup"><span data-stu-id="44231-139">In the global domain mapping table, click <strong>Add</strong>, enter a <strong>NetBIOS domain name</strong> and a <strong>Fully qualified domain name</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="44231-140">Verwenden Sie den folgenden Domänennamen </strong> – nehmen Sie an der angegebenen Domäne Teil; geben Sie einen Domänennamen und einen NetBIOS-Domänennamen in die entsprechenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="44231-140">Use the following domain name</strong>—Join the domain specified; enter a domain name and NetBIOS domain name in the corresponding fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-141">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="44231-141">Organization Unit</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-142">Eine Organisationseinheit (OU) kann angegeben werden, um den Computer mit einer bestimmten OU zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="44231-142">An organization unit (OU) may be specified to join the computer to a specific OU.</span></span> <span data-ttu-id="44231-143">Das Format muss einem definierten ou-Namen folgen: OU = &lt; Organisationseinheit &gt; , &lt; Domänen Controller (Beispiels &gt; Weise ou = QATest, DC = Il, DC = MED-V, DC = com).</span><span class="sxs-lookup"><span data-stu-id="44231-143">The format must follow an OU distinguished name: OU=&lt;Organization Unit&gt;,&lt;Domain Controller&gt; (for example, OU=QATest, DC=il, DC=MED-V, DC=com).</span></span></p>
<div class="alert">
<strong><span data-ttu-id="44231-144">Warnung</span><span class="sxs-lookup"><span data-stu-id="44231-144">Warning</span></span></strong><br/><p><span data-ttu-id="44231-145">Es wird nur eine OU für einzelne Ebenen unterstützt, wie im obigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="44231-145">Only a single level OU is supported as is shown in the example above.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**<span data-ttu-id="44231-146">Überprüfen der Verbindungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="44231-146">Check Connectivity Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44231-147">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44231-147">Property</span></span></th>
<th align="left"><span data-ttu-id="44231-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44231-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-149">IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="44231-149">IP Address</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-150">Die IP-Adresse des Servers, mit dem Sie die Verbindung überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="44231-150">The IP Address of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44231-151">Port</span><span class="sxs-lookup"><span data-stu-id="44231-151">Port</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-152">Der Port des Servers, mit dem Sie die Verbindung überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="44231-152">The port of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-153">Timeout</span><span class="sxs-lookup"><span data-stu-id="44231-153">Timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-154">Die Anzahl der Sekunden, die auf eine Antwort gewartet werden muss, bevor ein Timeout eintritt.</span><span class="sxs-lookup"><span data-stu-id="44231-154">The number of seconds to wait for a response before timing out.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**<span data-ttu-id="44231-155">Befehlszeileneigenschaften</span><span class="sxs-lookup"><span data-stu-id="44231-155">Command-Line Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44231-156">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44231-156">Property</span></span></th>
<th align="left"><span data-ttu-id="44231-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44231-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-158">Pfad</span><span class="sxs-lookup"><span data-stu-id="44231-158">Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-159">Der Pfad der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="44231-159">The path of the command line.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44231-160">Argumente</span><span class="sxs-lookup"><span data-stu-id="44231-160">Arguments</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-161">Befehlszeilenargumente</span><span class="sxs-lookup"><span data-stu-id="44231-161">Command-line arguments.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-162">Auf beenden warten</span><span class="sxs-lookup"><span data-stu-id="44231-162">Wait for exit</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-163">Aktivieren Sie das Kontrollkästchen, um auf eine Rückgabe zu warten, bevor Sie mit den Skriptaktionen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="44231-163">Select the check box to wait for a return before continuing with the script actions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44231-164">Fehler bei Fehler</span><span class="sxs-lookup"><span data-stu-id="44231-164">Fail on error</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-165">Aktivieren Sie dieses Kontrollkästchen, wenn die Rückgabe nichts anderes als der angegebene Wert ist.</span><span class="sxs-lookup"><span data-stu-id="44231-165">Select this check box if the return is anything but the value specified.</span></span></p>
<p><span data-ttu-id="44231-166">Geben Sie den Wert ein, der den Befehl als Erfolg kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="44231-166">Enter the value that will indicate the command as a success.</span></span></p>
<p><span data-ttu-id="44231-167">Standard: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="44231-167">Default: <strong>0</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-168">Nur einmal ausführen</span><span class="sxs-lookup"><span data-stu-id="44231-168">Perform only once</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-169">Aktivieren Sie dieses Kontrollkästchen, wenn die Befehlszeile nur einmal ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44231-169">Select this check box to run the command line only once.</span></span> <span data-ttu-id="44231-170">Wenn das Skript fehlschlägt oder abgebrochen wird, wird dieser Befehl nicht erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44231-170">If the script fails or is canceled, this command will not be performed again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44231-171">Diese Befehlszeile führt zu einem Neustart von Windows im Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="44231-171">This command line causes a restart of Windows in the Workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-172">Aktivieren Sie dieses Kontrollkästchen, wenn die Befehlszeile nach Abschluss einen Neustart bewirkt.</span><span class="sxs-lookup"><span data-stu-id="44231-172">Select this check box if the command line causes a restart after completion.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-173">Interaktionen zulassen</span><span class="sxs-lookup"><span data-stu-id="44231-173">Allow interaction</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-174">Aktivieren Sie dieses Kontrollkästchen, wenn für den Befehl Benutzerinteraktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="44231-174">Select this check box if the command will require user interaction.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44231-175">Statusmeldung</span><span class="sxs-lookup"><span data-stu-id="44231-175">Progress message</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-176">Die Meldung, die dem Benutzer angezeigt werden soll, während der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44231-176">Message to be displayed to the user while the command is running.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-177">Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="44231-177">Failure message</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-178">Nachricht, die dem Benutzer angezeigt werden soll, wenn der Befehl fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="44231-178">Message to be displayed to the user if the command fails.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="44231-179">Beim Konfigurieren der Befehlszeilenaktion können verschiedene Variablen verwendet werden, wie in der folgenden Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="44231-179">When configuring the command-line action, several variables can be used as defined in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44231-180">Parameter</span><span class="sxs-lookup"><span data-stu-id="44231-180">Parameter</span></span></th>
<th align="left"><span data-ttu-id="44231-181">Wert</span><span class="sxs-lookup"><span data-stu-id="44231-181">Value</span></span></th>
<th align="left"><span data-ttu-id="44231-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44231-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-183">%MEDVUser%</span><span class="sxs-lookup"><span data-stu-id="44231-183">%MEDVUser%</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-184">Ein authentifizierter Benutzername.</span><span class="sxs-lookup"><span data-stu-id="44231-184">An authenticated user name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-185">MED-V authentifizierter Benutzername.</span><span class="sxs-lookup"><span data-stu-id="44231-185">MED-V authenticated user name.</span></span> <span data-ttu-id="44231-186">Der Benutzername und das Kennwort können im Setupskript für die Teilnahme an einer Domänen-VM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44231-186">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44231-187">%MEDVPassword%</span><span class="sxs-lookup"><span data-stu-id="44231-187">%MEDVPassword%</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-188">Ein authentifiziertes Kennwort.</span><span class="sxs-lookup"><span data-stu-id="44231-188">An authenticated password.</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-189">MED-V-authentifiziertes Kennwort.</span><span class="sxs-lookup"><span data-stu-id="44231-189">MED-V authenticated password.</span></span> <span data-ttu-id="44231-190">Der Benutzername und das Kennwort können im Setupskript für die Teilnahme an einer Domänen-VM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44231-190">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44231-191">%MEDVDomain%</span><span class="sxs-lookup"><span data-stu-id="44231-191">%MEDVDomain%</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-192">Konfigurierte Domäne.</span><span class="sxs-lookup"><span data-stu-id="44231-192">Configured domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-193">Die in der MED-V-Authentifizierung konfigurierte Domäne.</span><span class="sxs-lookup"><span data-stu-id="44231-193">The domain configured in the MED-V authentication.</span></span> <span data-ttu-id="44231-194">Sie kann für das VM-Setupskript verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44231-194">It can be used on the VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44231-195">%DesiredMachineName%</span><span class="sxs-lookup"><span data-stu-id="44231-195">%DesiredMachineName%</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-196">Computer Name</span><span class="sxs-lookup"><span data-stu-id="44231-196">Computer name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="44231-197">Der in der Verwaltungsanwendung konfigurierte eindeutige Computername.</span><span class="sxs-lookup"><span data-stu-id="44231-197">The unique computer name configured in the management application.</span></span> <span data-ttu-id="44231-198">Sie kann im VM-Setupskript verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44231-198">It can be used in the VM setup script.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="44231-199">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="44231-199">Related topics</span></span>


[<span data-ttu-id="44231-200">So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="44231-200">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="44231-201">So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer</span><span class="sxs-lookup"><span data-stu-id="44231-201">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





