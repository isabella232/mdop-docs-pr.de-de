---
title: Konfigurieren eines virtuellen Windows-PC-Images für MED-V
description: Konfigurieren eines virtuellen Windows-PC-Images für MED-V
author: dansimp
ms.assetid: d87a0df8-9e08-4d1e-bfb0-9dc3cebf0d28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 340754b33576651c8ba89c85f369c48c0a0ab957
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811983"
---
# Konfigurieren eines virtuellen Windows-PC-Images für MED-V


Nachdem Sie alle Elemente installiert haben, die Sie in Ihr Med-v-Abbild aufnehmen möchten, können Sie das Bild für die Verwendung in Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 konfigurieren. Die Themen in diesem Abschnitt enthalten Anleitungen für die Konfiguration Ihres Med-v-Abbilds, um das erstmalige Setup auszuführen, bevor Sie Ihr Med-v-Arbeitsbereichs Paket erstellen.

Bei der erstmaligen Einrichtung wird der MED-V-Arbeitsbereich für einen Endbenutzer vorbereitet. Der Prozess erstellt einen virtuellen Computer aus dem Bild, das im MED-V-Arbeitsbereich verpackt ist, und führt dann Windows Mini-Setup auf dem virtuellen Computer aus. Dazu gehören sowohl die Ausführung von benutzerdefinierten Setupskripts als auch die Anwendung zur erstmaligen Einrichtung des Setups, FtsCompletion.exe.

Führen Sie die folgenden Schritte aus, um Ihr MED-V-Abbild für die Ausführung der erstmaligen Einrichtung zu konfigurieren:

1. Optional können Sie die virtuelle Festplatte (VHD) komprimieren, um leeren Speicherplatz freizugeben und die Größe der VHD zu verringern, bevor Sie mit dem Konfigurieren des Windows Virtual PC-Bilds fortfahren. Weitere Informationen finden Sie unter [Komprimieren der virtuellen MED-V-Festplatte](compacting-the-med-v-virtual-hard-disk.md).

2. Passen Sie den Setupvorgang für den virtuellen Computer an.

3. Versiegeln Sie das MED-V-Bild mithilfe von Sysprep.

   **Anpassen des Setup Prozesses für den virtuellen Computer**

4. Im Rahmen der Vorbereitung Ihres Bilds zur Verwendung mit MED-V können Sie verschiedene Einstellungen auf dem virtuellen Computer konfigurieren, wie beispielsweise die Angabe der Einstellungen für die Ausführung von Windows Update. Geben Sie vor dem Erstellen des MED-V Workspace-Pakets alle erforderlichen Einstellungen für den virtuellen Computer an.

5. Bevor Sie das MED-V Workspace-Paket erstellen, empfehlen wir, die Wiederherstellungspunkte auf dem virtuellen Computer zu deaktivieren, um zu verhindern, dass der differenzierende Datenträger unbegrenzt wächst. Weitere Informationen finden Sie unter [so wird es gemacht: deaktivieren und Aktivieren der System Wiederherstellung unter Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

   **Hinweis:**  
   Sie können Ihre Datei "Sysprep. inf" so einrichten, dass Wiederherstellungspunkte deaktiviert werden, wenn die erstmalige Einrichtung ausgeführt wird. Ein Beispiel für das Festlegen dieses GUIRunOnce-Schlüssels finden Sie im Beispiel für die Datei "Sysprep. inf" weiter unten in diesem Abschnitt.



6. Konfigurieren Sie den Setupvorgang so, dass die Mini Installation statt der standardmäßigen Windows-Willkommensseite ausgeführt wird. Sie müssen entweder das Sysprep-Tool mithilfe des **-Mini-** Schalters ausführen oder das Kontrollkästchen **MiniSetup** auf der grafischen Benutzeroberfläche aktivieren. Weitere Informationen finden Sie unter [versiegeln des Bilds mit Sysprep](#bkmk-seal).

   **Aufrufen der Abschluss Datei für das erstmalige Setup**

   1.  Eine ausführbare Datei mit dem Namen FtsCompletion.exe ist Teil der Installation des MED-V-Gast-Agents. Standardmäßig befindet Sie sich auf dem Systemlaufwerk Ihres MED-V-Images unter **Programmdateien – Microsoft Enterprise-Desktop-Virtualisierung**.

       **Wichtig**  
       Als letzten Schritt beim erstmaligen Einrichtungsvorgang müssen Sie dieses ausführbare Programm ausführen. Der Benutzer, für den das ausführbare Programm aufgerufen wird, muss ein Mitglied der lokalen Administratorgruppe des Gasts sein.



   2.  Sie können entscheiden, wie Sie dieses ausführbare Programm aufrufen möchten, beispielsweise über ein Skript, das mit dem MED-V-Arbeitsbereich bereitgestellt wird. Sie können diese ausführbare Datei als letzte Zeile der Datei "Sysprep. inf" aufrufen. Ein Beispiel für das Aufrufen dieses ausführbaren Programms in der Datei "Sysprep. inf" finden Sie in der Beispieldatei weiter unten in diesem Abschnitt.

Nachdem Sie die Anpassung Ihres MED-V-Bilds abgeschlossen haben, können Sie das Bild mithilfe von sysprep versiegeln.

<a href="" id="bkmk-seal"></a>**Abdichten des MED-V-Bilds mithilfe von Sysprep**

1.  Das System Vorbereitungstool (Sysprep) ist eine Technologie, die Sie verwenden können, um bildbasierte Installationen im gesamten Netzwerk mit minimalem Eingriff durch einen Administrator oder IT-Experten durchzuführen.

2.  In einer Med-v-Umgebung können Sie Sysprep verwenden, um jedem Med-v-Arbeitsbereich beim ersten Starten eindeutige Sicherheits-IDs (SID) und andere Einstellungen zuzuweisen.

    **Hinweis:**  
    Weitere Informationen zum Verwenden von Sysprep finden Sie unter [Technische Referenz zu Sysprep](https://go.microsoft.com/fwlink/?LinkId=195930) ( https://go.microsoft.com/fwlink/?LinkId=195930) .



~~~
**Caution**  
When you use non-ASCII characters in the Sysprep.inf file, you must save the file by using the encoding appropriate for the characters entered. Windows XP expects the Sysprep.inf file to be encoded by using the code page for the language that you are targeting.

You must also make sure that the System Locale of the computers to which the MED-V workspace is deployed is set to handle the language specific characters that might be present in the Sysprep.inf file. To change the settings for the System Locale, follow these steps:

1.  To open Region and Language, click **Start**, click **Control Panel**, and then click **Region and Language**.

2.  Click the **Administrative** tab, and then click **Change System Locale** under **Language for non-Unicode programs**.

    If you are prompted for an administrator password or confirmation, type the administrator password or provide confirmation.

3.  Select your preferred language and then click **OK**.



**To configure Sysprep on the MED-V Guest Computer**

1.  Create a folder named *Sysprep* in the root of the MED-V image system drive.

2.  Download the deploy.cab file. For more information, see [Windows XP Service Pack 3 Deployment Tools](https://go.microsoft.com/fwlink/?LinkId=195928) From the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195928).

3.  From the deploy.cab file, copy or extract the Setupmgr.exe, Sysprep.exe, and Setupcl.exe files to the Sysprep folder.

4.  In the Sysprep folder, run **Setup Manager** (Setupmgr.exe) to create a Sysprep.inf answer file.

    Or, you can create this file manually or use your company’s existing file. For more information, see [How to use the Sysprep tool to automate successful deployment of Windows XP](https://go.microsoft.com/fwlink/?LinkId=195929) (https://go.microsoft.com/fwlink/?LinkId=195929).

5.  Follow the **Setup Manager** wizard.

    **Important**  
    You must configure the MED-V guest to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.



    **Caution**  
    When you configure a proxy account for joining virtual machines to the domain, know that it is possible for an end user to obtain the proxy account credentials. Take all the necessary security precautions to minimize risk, such as limiting account user rights. For more information about security concerns when you configure a Windows Virtual PC image for MED-V, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).



    If end users must provide information during the first time setup process based on the parameters specified in the Sysprep.inf file, you must also specify that first time setup is run in **Attended** mode when you are creating your MED-V workspace package. If no information will be required from the end user, you can specify that first time setup is run in **Unattended** mode when you are creating your MED-V workspace package. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode. This requires that you provide all of the required settings information as you continue through the **Setup Manager** wizard.

    **Caution**  
    If you have set a local policy or registry entry to include a service level agreement (SLA) in your image (VHD), you must specify that first time setup is run in **Attended** mode or first time setup will fail. Or, a MED-V best practice is to enforce the SLA through Group Policy later so that the SLA is displayed to the end user after first time setup is finished.



    **Note**  
    You can configure the MED-V workspace to set certain Sysprep.inf settings based on the configuration of the host and the identity of the end user. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).



6.  Seal the MED-V image.

    **Important**  
    We recommend that you make a backup copy of the MED-V image before sealing it.



    After you have completed all the steps in the **Setup Manager** wizard, you are ready to run Sysprep to seal the MED-V image.

**To run Sysprep**

1.  Run the System Preparation Tool (Sysprep.exe) from the *Sysprep* folder that you created when you configured Sysprep in the MED-V virtual machine.

2.  In the warning message box that appears, click **OK**.

3.  In the **Options** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes. Also, make sure that the **Shutdown mode** box is set to **Shut down**.

4.  Click **Reseal**. This removes identity information and clears event logs to prepare for first time setup.

5.  If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and then change the selections.

6.  Click **OK** to complete the system preparation process.

After you have run Sysprep on your MED-V image, the virtual machine shuts down and is ready for use in creating a MED-V workspace.
~~~

## Beispiel


Im folgenden finden Sie ein Beispiel für eine Sysprep. inf-Datei.

``` syntax
;SetupMgrTag
[GuiUnattended]
    EncryptedAdminPassword=NO
    TimeZone=10
    OEMDuplicatorstring="MED_V v2 Host"
    AdminPassword="administrator"
    AutoLogon=Yes
    AutoLogonCount=1
    OEMSkipRegional=1
    OemSkipWelcome=1

[UserData]
    ProductKey=
    FullName="MED-V User"
    OrgName="Contoso"
    ComputerName=*

[Identification]
    JoinDomain=domain.corp.contoso.com
    DomainAdmin=UserName
    DomainAdminPassword=Password

[Networking]
    InstallDefaultComponents=Yes

[Branding]
    BrandIEUsingUnattended=Yes

[Proxy]
    Proxy_Enable=0
    Use_Same_Proxy=0

[Unattended]
    InstallFilesPath=C:\sysprep\i386
    TargetPath=\WINDOWS
    UpdateServerProfileDirectory=1
    OemSkipEula=Yes

[RegionalSettings]
    LanguageGroup=1
    Language=00000409

[GuiRunOnce]
    Command0="wmic /namespace:\\root\default path SystemRestore call Disable %SystemDrive%\"
    Command1="c:\Program Files\Microsoft Enterprise Desktop Virtualization\FtsCompletion.exe"

[sysprepcleanup]
```

## Verwandte Themen


[Erstellen eines MED-V-Arbeitsbereichspakets](create-a-med-v-workspace-package.md)

[Vorbereiten eines MED-V-Images](prepare-a-med-v-image.md)









