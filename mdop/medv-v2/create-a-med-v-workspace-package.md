---
title: Erstellen eines MED-V-Arbeitsbereichspakets
description: Erstellen eines MED-V-Arbeitsbereichspakets
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809850"
---
# <span data-ttu-id="b8202-103">Erstellen eines MED-V-Arbeitsbereichspakets</span><span class="sxs-lookup"><span data-stu-id="b8202-103">Create a MED-V Workspace Package</span></span>


<span data-ttu-id="b8202-104">Ein Med-v-Arbeitsbereich ist die Windows XP-Desktopumgebung, in der Endbenutzer mit dem virtuellen Computer interagieren, der von Med-v bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-104">A MED-V workspace is the Windows XP desktop environment where end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="b8202-105">Der Administrator erstellt und passt den MED-V-Arbeitsbereich an.</span><span class="sxs-lookup"><span data-stu-id="b8202-105">The administrator creates and customizes the MED-V workspace.</span></span> <span data-ttu-id="b8202-106">Der Arbeitsbereich besteht aus einem Bild und der Gruppenrichtlinie, die die Regeln und Funktionen des MED-V-Arbeitsbereichs definiert.</span><span class="sxs-lookup"><span data-stu-id="b8202-106">The workspace consists of an image and the Group Policy that defines the rules and functionality of the MED-V workspace.</span></span>

<span data-ttu-id="b8202-107">Sie können mehrere MED-V-Arbeitsbereiche erstellen, die jeweils mit eigener Konfiguration, Einstellungen und Regeln angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="b8202-107">You can create multiple MED-V workspaces, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="b8202-108">Jedem MED-V-Arbeitsbereich können Benutzer, Gruppen oder mehrere Benutzer oder Gruppen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b8202-108">A user, group, or multiple users or groups can be associated with each MED-V workspace.</span></span> <span data-ttu-id="b8202-109">Durch die Anpassung wird dieser MED-V-Arbeitsbereich nur für diesen Benutzer oder diese Gruppe zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="b8202-109">The customization makes that MED-V workspace available only for that user or group.</span></span>

<span data-ttu-id="b8202-110">Verwenden Sie den **Med-v Workspace-Paketer** zum Erstellen von Med-v-Arbeitsbereichen.</span><span class="sxs-lookup"><span data-stu-id="b8202-110">Use the **MED-V Workspace Packager** to create MED-V workspaces.</span></span> <span data-ttu-id="b8202-111">Der **MED-V Workspace-Paketer** ist in zwei Hauptabschnitte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="b8202-111">The **MED-V Workspace Packager** is divided into two main sections:</span></span>

-   <span data-ttu-id="b8202-112">Ein Hauptbereich mit drei Schaltflächen, die Sie zum Erstellen und Verwalten von MED-V-Arbeitsbereichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8202-112">A main panel that includes three buttons that you use to create and manage MED-V workspaces.</span></span> <span data-ttu-id="b8202-113">Mit der Schaltfläche " **Med-v Workspace-Paket erstellen** " wird der Assistent zum Erstellen eines **Med-v-Arbeitsbereichs Pakets** geöffnet, mit dem Sie Ihre Med-v-Arbeitsbereiche erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8202-113">The **Create a MED-V Workspace Package** button opens the **Create MED-V Workspace Package Wizard** that you use to create your MED-V workspaces.</span></span>

-   <span data-ttu-id="b8202-114">Ein **Hilfe Center** auf der rechten Seite des Fensters, in dem Sie Informationen und Anleitungen zum Erstellen, testen und Verwalten Ihrer MED-V-Arbeitsbereiche finden.</span><span class="sxs-lookup"><span data-stu-id="b8202-114">A **Help Center** on the right-hand side of the window that provides information and guidance to help you create, test, and manage your MED-V workspaces.</span></span>

**<span data-ttu-id="b8202-115">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b8202-115">Important</span></span>**  
<span data-ttu-id="b8202-116">Bevor Sie den **MED-V-Arbeitsbereichs-Packager**verwenden können, müssen Sie zuerst sicherstellen, dass die Windows PowerShell-Ausführungsrichtlinie auf Unrestricted festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="b8202-116">Before you can use the **MED-V Workspace Packager**, you must first make sure that the Windows PowerShell execution policy is set to Unrestricted.</span></span>

`Set-ExecutionPolicy Unrestricted`

<span data-ttu-id="b8202-117">Darüber hinaus muss die San-Richtlinie für den Computer, auf dem der **MED-V Workspace-Paketer** ausgeführt wird, auf "Online alle" eingestellt sein.</span><span class="sxs-lookup"><span data-stu-id="b8202-117">In addition, the SAN policy for the computer on which the **MED-V Workspace Packager** is run must be set to “Online All”.</span></span> <span data-ttu-id="b8202-118">Führen Sie die folgenden Befehle an einer Eingabeaufforderung mit Administratorrechten aus, um die Einstellung der San-Richtlinie zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="b8202-118">To check the setting of the SAN policy, run the following commands at a command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

<span data-ttu-id="b8202-119">Wenn dies erforderlich ist, ändern Sie die San-Richtlinie in "Online alle", indem Sie an der Eingabeaufforderung die folgenden Befehle mit Administratoranmeldeinformationen eingeben:</span><span class="sxs-lookup"><span data-stu-id="b8202-119">If it is necessary, change the SAN policy to "Online All" by typing the following commands at the command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**<span data-ttu-id="b8202-120">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b8202-120">Important</span></span>**  
<span data-ttu-id="b8202-121">Wenn die automatische datenträgerverschlüsselungssoftware auf dem Computer installiert ist, den Sie zum Bereitstellen der virtuellen Festplatte und zum Erstellen des MED-V-Arbeitsbereichs Pakets verwenden, müssen Sie die Software vor dem Start deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b8202-121">If automatic disk encryption software is installed on the computer that you use to mount the virtual hard disk and build the MED-V workspace package, you must disable the software before you start.</span></span> <span data-ttu-id="b8202-122">Andernfalls können Sie den MED-V-Arbeitsbereich nicht auf einem anderen Computer verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8202-122">Otherwise, you cannot use the MED-V workspace on any other computer.</span></span>



<span data-ttu-id="b8202-123">Die hier bereitgestellten Informationen können Ihnen beim Erstellen Ihres MED-V Workspace-Bereitstellungspakets helfen.</span><span class="sxs-lookup"><span data-stu-id="b8202-123">The information we provide here can help you create your MED-V workspace deployment package.</span></span>

## <a href="" id="bkmk-prereq"></a><span data-ttu-id="b8202-124">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="b8202-124">Prerequisites</span></span>


<span data-ttu-id="b8202-125">Bevor Sie mit dem Erstellen Ihres MED-V Workspace-Bereitstellungspakets beginnen, stellen Sie sicher, dass Sie Zugriff auf die folgenden Elemente haben:</span><span class="sxs-lookup"><span data-stu-id="b8202-125">Before you start to build your MED-V workspace deployment package, verify that you have access to the following items:</span></span>

-   **<span data-ttu-id="b8202-126">Ein vorbereitetes Windows XP-Abbild</span><span class="sxs-lookup"><span data-stu-id="b8202-126">A prepared Windows XP image</span></span>**

    <span data-ttu-id="b8202-127">Weitere Informationen zum Erstellen eines Windows XP-Images zur Verwendung mit Med-v finden Sie unter [Vorbereiten eines Med-v-Abbilds](prepare-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="b8202-127">For more information about how to create a Windows XP image for use with MED-V, see [Prepare a MED-V Image](prepare-a-med-v-image.md).</span></span>

-   **<span data-ttu-id="b8202-128">Eine Textdatei oder Liste, die URL-Umleitungsinformationen enthält</span><span class="sxs-lookup"><span data-stu-id="b8202-128">A text file or list that contains URL redirection information</span></span>**

    <span data-ttu-id="b8202-129">Ihre URL-Umleitungs Textdatei oder-Liste enthält die URLs, die Sie vom Hostcomputer zu Internet Explorer im MED-V-Arbeitsbereich weiterleiten möchten.</span><span class="sxs-lookup"><span data-stu-id="b8202-129">Your URL redirection text file or list contains those URLs that you want redirected from the host computer to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="b8202-130">Wenn Sie den Verpackungs-Assistenten zum Erstellen Ihres MED-V-Arbeitsbereichs verwenden, können Sie diese Umleitungsinformationen importieren, eingeben oder kopieren und als einen der Schritte im Paketerstellungsprozess einfügen.</span><span class="sxs-lookup"><span data-stu-id="b8202-130">When you are using the packaging wizard to create your MED-V workspace, you import, type, or copy and paste this redirection information as one of the steps in the package creation process.</span></span>

    **<span data-ttu-id="b8202-131">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8202-131">Note</span></span>**  
    <span data-ttu-id="b8202-132">Die URL-Umleitung in MED-V unterstützt nur die Protokolle http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b8202-132">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="b8202-133">MED-V bietet keine Unterstützung für FTP oder andere Protokolle.</span><span class="sxs-lookup"><span data-stu-id="b8202-133">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## <span data-ttu-id="b8202-134">Verpacken eines Med-v-Arbeitsbereichs für eine andere Sprache als die Sprache des Med-v-Arbeitsbereichs-Paket Computers</span><span class="sxs-lookup"><span data-stu-id="b8202-134">Packaging a MED-V Workspace for a Language Other than the Language of the MED-V Workspace Packager Computer</span></span>


<span data-ttu-id="b8202-135">Standardmäßig unterstützt der MED-V-Arbeitsbereich Zeichen sowohl in der Sprache des Computers als auch in Englisch.</span><span class="sxs-lookup"><span data-stu-id="b8202-135">By default, the MED-V workspace supports characters in both the language of the computer and in English.</span></span> <span data-ttu-id="b8202-136">Wenn Sie einen Med-v-Arbeitsbereich für eine Sprache erstellen möchten, die nicht auf dem Computer installiert ist, geben Sie **-Loc \ [Gebietsschema \]** im PowerShell-Skript (. ps1) nach dem Med-v-Arbeitsbereichsnamen ein.</span><span class="sxs-lookup"><span data-stu-id="b8202-136">To create a MED-V workspace for a language other than the one installed on the computer, specify **-loc \[locale\]** in the PowerShell script (.ps1) after the MED-V workspace name.</span></span>

<span data-ttu-id="b8202-137">Wenn Sie ein Med-v-Arbeitsbereichs Paket in einer anderen Sprache als der Standardsprache des Med-v Workspace-Paket Computers erstellen möchten, generieren Sie ein Skript in der Standardsprache, indem Sie den Med-v-Arbeitsbereichs-Paketdienst ausführen und dann das Ausgabeskript nach Bedarf für Ihr Gebietsschema ändern.</span><span class="sxs-lookup"><span data-stu-id="b8202-137">To create a MED-V workspace package in a language other than the default language of the MED-V Workspace Packager computer, generate a script in the default language by running the MED-V Workspace Packager and then modifying the output script as required for your locale.</span></span> <span data-ttu-id="b8202-138">Das Skript befindet sich im MED-V Workspace-Ausgabeverzeichnis, das während der Verpackung angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b8202-138">The script is located in the MED-V workspace output directory that was specified during packaging.</span></span> <span data-ttu-id="b8202-139">Die Namen der Gebietsschemaeinstellungen befinden sich auf der. BXL-Dateien im folgenden Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="b8202-139">The names of the locale settings are on the .WXL files in the following directory:</span></span>

<span data-ttu-id="b8202-140">C:\\Programme c:\\Programme\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.medv.Administration.Commands.WorkspacePackager\\locale</span><span class="sxs-lookup"><span data-stu-id="b8202-140">C:\\Program Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span></span>

## <span data-ttu-id="b8202-141">Erstellen eines MED-V-Arbeitsbereichs Pakets</span><span class="sxs-lookup"><span data-stu-id="b8202-141">Creating a MED-V Workspace Package</span></span>


<span data-ttu-id="b8202-142">Führen Sie die folgenden Schritte aus, um ein MED-V-Arbeitsbereichs Paket zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="b8202-142">To create a MED-V workspace package, follow these steps:</span></span>

****

1.  <span data-ttu-id="b8202-143">Klicken Sie zum Öffnen des **Med-v Workspace-Pakets**auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **Med-v Workspace Packager**.</span><span class="sxs-lookup"><span data-stu-id="b8202-143">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="b8202-144">Klicken Sie im Hauptbereich des **Med-v Workspace-Pakets** auf **Med-v Workspace-Paket erstellen**.</span><span class="sxs-lookup"><span data-stu-id="b8202-144">On the **MED-V Workspace Packager** main panel, click **Create a MED-V Workspace Package**.</span></span>

    <span data-ttu-id="b8202-145">Der Med-v- **Assistent zum Erstellen eines Med-v-Arbeitsbereichs Pakets** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8202-145">The MED-V **Create MED-V Workspace Package Wizard** appears.</span></span> <span data-ttu-id="b8202-146">Der Assistent besteht aus den folgenden Seiten:</span><span class="sxs-lookup"><span data-stu-id="b8202-146">The wizard consists of the following pages:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b8202-147">Paketinformationen</span><span class="sxs-lookup"><span data-stu-id="b8202-147">Package Information</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b8202-148">Geben Sie einen Namen für den Med-v-Arbeitsbereich an, und wählen Sie einen Ordner aus, in dem die Med-v Workspace-Paketdateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b8202-148">Specify a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="b8202-149">Windows XP-Abbild auswählen</span><span class="sxs-lookup"><span data-stu-id="b8202-149">Select Windows XP Image</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b8202-150">Geben Sie Ihr vorbereitetes Windows XP Virtual PC-Abbild an.</span><span class="sxs-lookup"><span data-stu-id="b8202-150">Specify your prepared Windows XP Virtual PC image.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b8202-151">Erstmaliges Einrichten</span><span class="sxs-lookup"><span data-stu-id="b8202-151">First Time Setup</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b8202-152">Geben Sie den Setupprozess an, dem MED-V bei der erstmaligen Einrichtung folgt.</span><span class="sxs-lookup"><span data-stu-id="b8202-152">Specify the setup process that MED-V follows during first time setup.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="b8202-153">MED-V-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="b8202-153">MED-V Messages</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b8202-154">Geben Sie die Nachrichten und die optionale URL für Hilfeinformationen an, die der Endbenutzer während der erstmaligen Einrichtung sieht.</span><span class="sxs-lookup"><span data-stu-id="b8202-154">Specify the messages and optional URL for Help information that the end user sees during first time setup.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b8202-155">Benennen von Computern</span><span class="sxs-lookup"><span data-stu-id="b8202-155">Naming Computers</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b8202-156">Geben Sie an, wie der virtuelle MED-V-Computer benannt wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-156">Specify how the MED-V virtual machine is named.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="b8202-157">Kopieren von Einstellungen vom Host</span><span class="sxs-lookup"><span data-stu-id="b8202-157">Copy Settings from Host</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b8202-158">Geben Sie an, wie die Einstellungen für den MED-V-Arbeitsbereich definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8202-158">Specify how the settings for the MED-V workspace are defined.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b8202-159">Start und Netzwerk</span><span class="sxs-lookup"><span data-stu-id="b8202-159">Startup and Networking</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b8202-160">Geben Sie die Einstellungen für den Start des MED-V Workspace, der Netzwerk-und der Benutzeranmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="b8202-160">Specify the settings for starting the MED-V workspace, networking, and user credentials.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="b8202-161">Web-Umleitung</span><span class="sxs-lookup"><span data-stu-id="b8202-161">Web Redirection</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b8202-162">Geben Sie eine Textdatei oder eine Liste der URLs an, die Sie im MED-V-Arbeitsbereich an Internet Explorer weitergeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b8202-162">Specify a text file or a list of the URLs you want redirected to Internet Explorer in the MED-V workspace.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b8202-163">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b8202-163">Summary</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b8202-164">Überprüfen Sie Ihre Med-v Workspace-Einstellungen, und beginnen Sie mit dem Erstellen Ihres Med-v Workspace-Bereitstellungspakets.</span><span class="sxs-lookup"><span data-stu-id="b8202-164">Verify your MED-V workspace settings and start to build your MED-V workspace deployment package.</span></span></p></td>
    </tr>
    </tbody>
    </table>



3.  <span data-ttu-id="b8202-165">Geben Sie auf der Seite **Paketinformationen** einen Namen für den Med-v-Arbeitsbereich ein, und wählen Sie einen Ordner aus, in dem die Med-v-Arbeitsbereichs Paketdateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b8202-165">On the **Package Information** page, enter a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span>

    **<span data-ttu-id="b8202-166">Warnung</span><span class="sxs-lookup"><span data-stu-id="b8202-166">Warning</span></span>**  
    <span data-ttu-id="b8202-167">Sie müssen den MED-V-Arbeitsbereich benennen und einen Ordner angeben, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="b8202-167">You must name the MED-V workspace and specify a folder to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

4. <span data-ttu-id="b8202-168">Geben Sie auf der Seite **Windows XP-Abbild auswählen** den Speicherort Ihres vorbereiteten MED-V Windows XP Virtual PC-Bilds an (VHD-Datei).</span><span class="sxs-lookup"><span data-stu-id="b8202-168">On the **Select Windows XP Image** page, specify the location of your prepared MED-V Windows XP Virtual PC image (.vhd file).</span></span>

   **<span data-ttu-id="b8202-169">Warnung</span><span class="sxs-lookup"><span data-stu-id="b8202-169">Warning</span></span>**  
   <span data-ttu-id="b8202-170">Sie müssen ein Windows XP VHD-Abbild angeben, um fortfahren zu können.</span><span class="sxs-lookup"><span data-stu-id="b8202-170">You must specify a Windows XP VHD image to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

5. <span data-ttu-id="b8202-171">Wählen Sie auf der Seite für die **erstmalige Einrichtung** aus, ob die erstmalige Einrichtung ausgeführt werden soll, während Sie besucht oder unbeaufsichtigt sind, und ob Sie den MED-V-Arbeitsbereich separat verwenden oder von allen Endbenutzern auf einem freigegebenen Computer verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b8202-171">On the **First Time Setup** page, select whether you want first time setup to run while attended or unattended and whether you want the MED-V workspace used separately or used by all end users on a shared computer.</span></span>

   <span data-ttu-id="b8202-172">Wenn Sie die **unbeaufsichtigte Installation ohne Benachrichtigung**auswählen, wird der Endbenutzer nicht informiert, bevor das erstmalige Setup ausgeführt wird und der virtuelle Computer dem Endbenutzer während der erstmaligen Einrichtung nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-172">If you select **Unattended setup, without any notification**, the end user is not informed before first time setup is run and the virtual machine is not shown to the end user during first time setup.</span></span> <span data-ttu-id="b8202-173">Darüber hinaus ist die Seite **MED-V-Nachrichten** des Assistenten ausgeblendet, da keine Nachrichten erforderlich sind, wenn die erstmalige Einrichtung in einem vollständig unbeaufsichtigten Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-173">In addition, the **MED-V Messages** page of the wizard is hidden because no messages are required if first time setup runs in a completely unattended mode.</span></span>

   <span data-ttu-id="b8202-174">Wenn Sie die Option **unbeaufsichtigtes Setup auswählen, aber Endbenutzer Benachrichtigen, bevor das erstmalige Setup beginnt**, wird der Endbenutzer informiert, bevor die erstmalige Einrichtung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-174">If you select **Unattended setup, but notify end users before first time setup begins**, the end user is informed before first time setup is run.</span></span> <span data-ttu-id="b8202-175">Bei der erstmaligen Einrichtung wird der virtuelle Computer dem Endbenutzer jedoch nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8202-175">However, the virtual machine is not shown to the end user during first time setup.</span></span>

   <span data-ttu-id="b8202-176">Wählen Sie **beaufsichtigte Einrichtung** aus, wenn der Endbenutzer während der erstmaligen Einrichtung Informationen eingeben muss.</span><span class="sxs-lookup"><span data-stu-id="b8202-176">Select **Attended setup** if the end user must enter information during first time setup.</span></span>

   <span data-ttu-id="b8202-177">Das Standardverhalten ist die **unbeaufsichtigte Installation, aber die Endbenutzer werden benachrichtigt, bevor das erstmalige Setup beginnt**.</span><span class="sxs-lookup"><span data-stu-id="b8202-177">The default behavior is **Unattended setup, but notify end users before first time setup begins**.</span></span>

   **<span data-ttu-id="b8202-178">Achtung</span><span class="sxs-lookup"><span data-stu-id="b8202-178">Caution</span></span>**  
   <span data-ttu-id="b8202-179">Wenn Sie die Datei "Sysprep. inf" erstellt haben, damit für das Mini Setup eine Benutzereingabe erforderlich ist, müssen Sie " **beaufsichtigte Einrichtung** " auswählen oder während der erstmaligen Einrichtung Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="b8202-179">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, you must select **Attended setup** or problems might occur during first time setup.</span></span>



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. <span data-ttu-id="b8202-180">Geben Sie auf der Seite **MED-V-Nachrichten** die folgenden Nachrichten an, die der Endbenutzer während der erstmaligen Einrichtung sieht:</span><span class="sxs-lookup"><span data-stu-id="b8202-180">On the **MED-V Messages** page, specify the following messages that the end user sees during first time setup:</span></span>

   -   <span data-ttu-id="b8202-181">Die Meldung, die der Endbenutzer beim Starten der erstmaligen Einrichtung sieht.</span><span class="sxs-lookup"><span data-stu-id="b8202-181">The message that the end user sees when first time setup starts.</span></span>

   -   <span data-ttu-id="b8202-182">Die Meldung, die der Endbenutzer sieht, wenn die erstmalige Einrichtung fehlschlägt oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b8202-182">The message that the end user sees if first time setup fails or an error occurs.</span></span>

   **<span data-ttu-id="b8202-183">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8202-183">Note</span></span>**  
   <span data-ttu-id="b8202-184">Die Seite **MED-V-Nachrichten** des Assistenten wird ausgeblendet, wenn Sie die **unbeaufsichtigte Installation ohne Benachrichtigung** auf der Seite zum **erstmaligen Einrichten** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="b8202-184">The **MED-V Messages** page of the wizard is hidden if you selected **Unattended setup, without any notification** on the **First Time Setup** page.</span></span>



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. <span data-ttu-id="b8202-185">Auf der Seite **Naming Computers** können Sie angeben, ob die Computerbenennung von MED-V oder von einem Systemverwaltungstool wie Sysprep verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-185">On the **Naming Computers** page, you can specify whether computer naming is managed by MED-V or by a system management tool, such as Sysprep.</span></span> <span data-ttu-id="b8202-186">Standardmäßig wird die Computer Namensgebung von einem Systemverwaltungstool verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b8202-186">The default is that computer naming is managed by a system management tool.</span></span>

   <span data-ttu-id="b8202-187">Wenn Sie angeben, dass die Computerbenennung von MED-V verwaltet wird, wählen Sie in der Dropdownliste eine vordefinierte computernaming Convention (Maske) aus.</span><span class="sxs-lookup"><span data-stu-id="b8202-187">If you specify that computer naming is managed by MED-V, select a predefined computer naming convention (mask) from the drop-down list.</span></span> <span data-ttu-id="b8202-188">Eine Vorschau eines Beispiel Computernamens wird angezeigt, die auf dem Computer basiert, den Sie zum Erstellen des MED-V-Arbeitsbereichs Pakets verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8202-188">A preview of a sample computer name appears that is based on the computer that you are using to build the MED-V workspace package.</span></span>

   <span data-ttu-id="b8202-189">Wenn Sie eine der benutzerdefinierten Benennungskonventionen auswählen, sind die Felder, die Sie angeben können, auf die folgenden Zeichen limitiert:</span><span class="sxs-lookup"><span data-stu-id="b8202-189">If you select one of the custom naming conventions, the fields you can specify are limited to the following characters:</span></span>

   -   <span data-ttu-id="b8202-190">Die Felder "Präfix" und "Suffix" sind auf die Zeichen a-z, a-z, 0-9 und die Sonderzeichen limitiert!</span><span class="sxs-lookup"><span data-stu-id="b8202-190">The prefix and suffix fields are limited to the characters A-Z, a-z, 0-9, and the special characters !</span></span> <span data-ttu-id="b8202-191">@ \ # $% ^ & ()-\ _ ' {}.</span><span class="sxs-lookup"><span data-stu-id="b8202-191">@ \# $ % ^ & ( ) - \_ ' { } .</span></span> <span data-ttu-id="b8202-192">und ~.</span><span class="sxs-lookup"><span data-stu-id="b8202-192">and ~.</span></span>

   -   <span data-ttu-id="b8202-193">Die Felder Hostname und username sind auf die Ziffern 0 bis 9 limitiert.</span><span class="sxs-lookup"><span data-stu-id="b8202-193">The hostname and username fields are limited to the digits 0 through 9.</span></span>

   **<span data-ttu-id="b8202-194">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b8202-194">Important</span></span>**  
   <span data-ttu-id="b8202-195">Computer Namen müssen eindeutig sein und auf maximal 15 Zeichen limitiert sein.</span><span class="sxs-lookup"><span data-stu-id="b8202-195">Computer names must be unique and are limited to a maximum of 15 characters.</span></span> <span data-ttu-id="b8202-196">Wenn Sie sich für Ihre Computer Benennungsmethode entscheiden, sollten Sie die Endbenutzer in Frage stellen, die über mehrere Computer verfügen oder einen Computer freigeben, und vermeiden Sie die Verwendung von Computernamens Masken, die zu einer Kollision im Netzwerk führen können.</span><span class="sxs-lookup"><span data-stu-id="b8202-196">When you decide on your computer naming method, consider end users who have multiple computers or that share a computer, and avoid using computer name masks that could cause a collision on the network.</span></span>



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. <span data-ttu-id="b8202-197">Auf der Seite **Einstellungen von Host kopieren** können Sie die folgenden Einstellungen auswählen, um anzugeben, wie der MED-V-Arbeitsbereich konfiguriert werden soll:</span><span class="sxs-lookup"><span data-stu-id="b8202-197">On the **Copy Settings from Host** page, you can select the following settings to specify how the MED-V workspace is configured:</span></span>

   **<span data-ttu-id="b8202-198">Achtung</span><span class="sxs-lookup"><span data-stu-id="b8202-198">Caution</span></span>**  
   <span data-ttu-id="b8202-199">Die Einstellungen, die Sie auf dieser Seite angeben, die vom Hostcomputer in den MED-V-Arbeitsbereich kopiert werden, überschreiben die in der Antwortdatei "Sysprep. inf" angegebenen.</span><span class="sxs-lookup"><span data-stu-id="b8202-199">The settings that you specify on this page that are copied from the host computer to the MED-V workspace override those specified in the Sysprep.inf answer file.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. <span data-ttu-id="b8202-200">Auf der Seite **Start und Netzwerk** können Sie das Standardverhalten für die folgenden Einstellungen ändern:</span><span class="sxs-lookup"><span data-stu-id="b8202-200">On the **Startup and Networking** page, you can change the default behavior for the following settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b8202-201">Starten des MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="b8202-201">Start MED-V workspace</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b8202-202">Wählen Sie aus, ob der Med-v-Arbeitsbereich bei der Benutzeranmeldung bei der ersten Verwendung gestartet oder der Endbenutzer entscheiden soll, wann der Med-v-Arbeitsbereich gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-202">Choose whether to start the MED-V workspace at user logon, at first use, or to let the end user decide when the MED-V workspace starts.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="b8202-203">Der Arbeitsbereich Med-v beginnt auf eine von zwei Arten: entweder beim Anmelden des Endbenutzers oder beim ersten Starten einer Aktion, für die Med-v erforderlich ist, beispielsweise das Öffnen einer veröffentlichten Anwendung oder das Eingeben einer URL, die eine Umleitung erfordert.</span><span class="sxs-lookup"><span data-stu-id="b8202-203">The MED-V workspace starts in one of two ways: either when the end user logs on or when they first start an action that requires MED-V, such as opening a published application or entering a URL that requires redirection.</span></span></p>
   <p><span data-ttu-id="b8202-204">Sie können diese Einstellung für den Endbenutzer definieren oder zulassen, dass der Endbenutzer steuert, wie MED-V gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-204">You can either define this setting for the end user or let the end user control how MED-V starts.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b8202-205">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8202-205">Note</span></span></strong><br/><p><span data-ttu-id="b8202-206">Wenn Sie angeben, dass der Endbenutzer entscheidet, besteht das Standardverhalten darin, dass der MED-V-Arbeitsbereich bei der Anmeldung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-206">If you specify that the end user decides, the default behavior they experience is that the MED-V workspace starts when they log on.</span></span> <span data-ttu-id="b8202-207">Sie können die Standardeinstellung ändern, indem Sie mit der rechten Maustaste auf das Med-v-Symbol im Infobereich klicken und dann <strong> Med-v-Benutzereinstellungen auswählen </strong> .</span><span class="sxs-lookup"><span data-stu-id="b8202-207">They can change the default by right-clicking the MED-V icon in the notification area and selecting <strong>MED-V User Settings</strong>.</span></span> <span data-ttu-id="b8202-208">Wenn Sie diese Einstellung für den Endbenutzer definieren, können Sie nicht ändern, wie MED-V gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-208">If you define this setting for the end user, they cannot change how MED-V starts.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b8202-209">Networking</span><span class="sxs-lookup"><span data-stu-id="b8202-209">Networking</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b8202-210">Wählen <strong> Sie </strong> <strong> </strong> für Ihre Netzwerkeinstellung freigegeben oder überbrückt aus.</span><span class="sxs-lookup"><span data-stu-id="b8202-210">Select <strong>Shared</strong> or <strong>Bridged</strong> for your networking setting.</span></span> <span data-ttu-id="b8202-211">Der Standardwert ist <strong> Shared </strong> .</span><span class="sxs-lookup"><span data-stu-id="b8202-211">The default is <strong>Shared</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong><span data-ttu-id="b8202-212">Shared </strong> - der MED-V Workspace verwendet die Netzwerkadressübersetzung (Network Address Translation, NAT), um die IP-Adresse des Host-&#39;für ausgehenden Datenverkehr freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b8202-212">Shared</strong> - The MED-V workspace uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p>
   <p><strong><span data-ttu-id="b8202-213">Überbrückt </strong> - der MED-V-Arbeitsbereich verfügt über eine eigene Netzwerkadresse, die in der Regel über DHCP abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b8202-213">Bridged</strong> - The MED-V workspace has its own network address, typically obtained through DHCP.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b8202-214">Speichern von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="b8202-214">Store credentials</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b8202-215">Wählen Sie aus, ob die Endbenutzeranmeldeinformationen gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b8202-215">Choose whether you want to store the end user credentials.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="b8202-216">Das Standardverhalten ist, dass die Speicherung von Anmeldeinformationen deaktiviert ist, damit der Endbenutzer bei jeder Anmeldung authentifiziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b8202-216">The default behavior is that credential storing is disabled so that the end user must be authenticated every time that they log on.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b8202-217">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b8202-217">Important</span></span></strong><br/><p><span data-ttu-id="b8202-218">Auch wenn die Zwischenspeicherung der Anmeldeinformationen des Endbenutzers die beste Benutzererfahrung bietet, sollten Sie sich mit den damit verbundenen Risiken vertraut machen.</span><span class="sxs-lookup"><span data-stu-id="b8202-218">Even though caching the end user’s credentials provides the best user experience, you should be aware of the risks involved.</span></span></p>
   <p><span data-ttu-id="b8202-219">Die Domänenanmeldeinformationen des Endbenutzers werden in einem reversiblen Format im Windows-Anmelde Informations-Manager gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b8202-219">The end user’s domain credential is stored in a reversible format in the Windows Credential Manager.</span></span> <span data-ttu-id="b8202-220">Daher kann ein Angreifer ein Programm schreiben, das das Kennwort abruft und Zugriff auf die Anmeldeinformationen des Benutzers erhält.</span><span class="sxs-lookup"><span data-stu-id="b8202-220">As a result, an attacker could write a program that retrieves the password and could gain access to the user’s credentials.</span></span> <span data-ttu-id="b8202-221">Sie können dieses Risiko nur verringern, indem Sie die Speicherung von Anmeldeinformationen des Endbenutzers deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b8202-221">You can only lessen this risk by disabling the storing of end-user credentials.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. <span data-ttu-id="b8202-222">Auf der Seite " **webumleitung** " können Sie eine Liste der URLs eingeben, einfügen oder importieren, die im MED-V-Arbeitsbereich an Internet Explorer umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b8202-222">On the **Web Redirection** page, you can enter, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="b8202-223">Weitere Informationen zum Konfigurieren der URL-Umleitungsinformationen finden Sie unter [Voraussetzungen](#bkmk-prereq).</span><span class="sxs-lookup"><span data-stu-id="b8202-223">For more information about how to configure your URL redirection information, see [Prerequisites](#bkmk-prereq).</span></span>

   <span data-ttu-id="b8202-224">Sie können auch angeben, wie Internet Explorer im MED-V-Arbeitsbereich für Endbenutzer konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="b8202-224">You can also specify how Internet Explorer in the MED-V workspace is configured for end users.</span></span> <span data-ttu-id="b8202-225">Standardmäßig ist die Sicherheitsstufe Internet Zone auf hoch festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b8202-225">By default, the Internet zone security level is set to High.</span></span> <span data-ttu-id="b8202-226">Darüber hinaus werden bestimmte Standardbrowserfunktionen wie die Adressleiste entfernt.</span><span class="sxs-lookup"><span data-stu-id="b8202-226">Also, certain default browsing capabilities, such as the address bar, are removed.</span></span> <span data-ttu-id="b8202-227">Diese Standardkonfiguration von Internet Explorer im MED-V-Arbeitsbereich bietet eine sicherere Browserumgebung für Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="b8202-227">This default configuration of Internet Explorer in the MED-V workspace provides a more secure browsing environment for end users.</span></span>

   **<span data-ttu-id="b8202-228">Achtung</span><span class="sxs-lookup"><span data-stu-id="b8202-228">Caution</span></span>**  
   <span data-ttu-id="b8202-229">Wenn Sie die Standardeinstellungen ändern, können Sie Internet Explorer im MED-V-Arbeitsbereich anpassen.</span><span class="sxs-lookup"><span data-stu-id="b8202-229">By changing the default settings, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="b8202-230">Beachten Sie jedoch, dass Sie die Sicherheitsrisiken, die in älteren Versionen von Internet Explorer vorhanden sind, wenn Sie die Standardeinstellungen so ändern, dass Sie nicht so sicher sind, für Ihre Organisation verfügbar machen können.</span><span class="sxs-lookup"><span data-stu-id="b8202-230">However, realize that if you change the default settings so as to make them less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span> <span data-ttu-id="b8202-231">Weitere Informationen finden Sie unter [bewährte Methoden für die Sicherheit von MED-V-Vorgängen](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="b8202-231">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>



~~~
After you have finished, click **Next**.
~~~

11. <span data-ttu-id="b8202-232">Auf der **Zusammenfassungs** Seite können Sie die Verpackungs Einstellungen für diesen MED-V-Arbeitsbereich überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b8202-232">On the **Summary** page, you can review the packaging settings for this MED-V workspace.</span></span> <span data-ttu-id="b8202-233">Wenn Sie Einstellungen ändern möchten, klicken Sie auf die Schaltfläche **zurück** , um zur entsprechenden Seite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b8202-233">If you want to change any settings, click the **Previous** button to return to the relevant page.</span></span> <span data-ttu-id="b8202-234">Nachdem Sie die Überprüfung der Einstellungen vorgenommen haben, klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="b8202-234">After you have finished reviewing the settings, click **Create**.</span></span>

   <span data-ttu-id="b8202-235">Die Seite **Fertigstellung** des **Assistenten zum Erstellen von MED-V Workspace-Paketen** wird geöffnet, um den Fortschritt der Paketerstellung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b8202-235">The **Completion** page of the **Create MED-V Workspace Package Wizard** opens to show the progress of the package creation.</span></span>

   **<span data-ttu-id="b8202-236">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8202-236">Note</span></span>**  
   <span data-ttu-id="b8202-237">Je nach Größe der festgelegten Festplatte kann es einige Minuten dauern, bis der Prozess des MED-V-Arbeitsbereichs Pakets abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b8202-237">The MED-V workspace package creation process might take several minutes to complete, depending on the size of the VHD specified.</span></span>



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. <span data-ttu-id="b8202-238">Klicken Sie auf **Schließen** , um den Verpackungs-Assistenten zu schließen und zum **MED-V Workspace-Paketer**zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b8202-238">Click **Close** to close the packaging wizard and return to the **MED-V Workspace Packager**.</span></span>

<span data-ttu-id="b8202-239">Ihr MED-V Workspace-Paket kann jetzt vor der Bereitstellung getestet werden.</span><span class="sxs-lookup"><span data-stu-id="b8202-239">Your MED-V workspace package is now ready for testing before deployment.</span></span>

## <span data-ttu-id="b8202-240">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b8202-240">Related topics</span></span>


[<span data-ttu-id="b8202-241">Konfigurieren von erweiterten Einstellungen mit Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8202-241">Configuring Advanced Settings by Using Windows PowerShell</span></span>](configuring-advanced-settings-by-using-windows-powershell.md)

[<span data-ttu-id="b8202-242">Testen des MED-V-Arbeitsbereichspakets</span><span class="sxs-lookup"><span data-stu-id="b8202-242">Testing the MED-V Workspace Package</span></span>](testing-the-med-v-workspace-package.md)

[<span data-ttu-id="b8202-243">Vorbereiten eines MED-V-Images</span><span class="sxs-lookup"><span data-stu-id="b8202-243">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)









