---
title: Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei
description: Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei
author: dansimp
ms.assetid: 0bc5e7d8-9747-4da6-a1b3-38d8f27ba121
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 272f597974e96efa0c742fecfe9488a4899fc695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809811"
---
# <span data-ttu-id="5e6d9-103">Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei</span><span class="sxs-lookup"><span data-stu-id="5e6d9-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="5e6d9-104">Damit die Clientcomputer BitLocker-Kompatibilitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die SMS \ _def. MOF-Datei erstellen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="5e6d9-105">Wenn Sie SystemCenter2012 ConfigurationManager verwenden, müssen Sie die Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="5e6d9-106">Erstellen Sie die Datei auf der Website der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-106">Create the file on the top-tier site.</span></span> <span data-ttu-id="5e6d9-107">Die Änderungen werden auf die anderen Websites in Ihrer Infrastruktur repliziert.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-107">The changes will be replicated to the other sites in your infrastructure.</span></span>

<span data-ttu-id="5e6d9-108">In Configuration Manager 2007 ist die Datei bereits vorhanden, sodass Sie Sie nur bearbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-108">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> **<span data-ttu-id="5e6d9-109">Überschreiben Sie die vorhandene Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-109">Do not overwrite the existing file.</span></span>**

<span data-ttu-id="5e6d9-110">Führen Sie in den folgenden Abschnitten die Anweisungen aus, die der von Ihnen verwendeten Version von Configuration Manager entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-110">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="5e6d9-111">So erstellen Sie die SMS \ _def. MOF-Datei für SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="5e6d9-111">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="5e6d9-112">Navigieren Sie auf dem Configuration Manager-Server zu dem Speicherort, an dem Sie die SMS \ _def. MOF-Datei erstellen müssen, beispielsweise den Desktop.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-112">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="5e6d9-113">Erstellen Sie eine Textdatei mit dem Namen **SMS \ _def. MOF** , und kopieren Sie den folgenden Code, um die Datei mit den folgenden SMS \ _def. MOF-MBAM-Klassen zu füllen:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-113">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="5e6d9-114">Importieren Sie die **SMS \ _def. MOF-** Datei, indem Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-114">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="5e6d9-115">Öffnen Sie die **SystemCenter2012 ConfigurationManager-Konsole** , und wählen Sie die Registerkarte **Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-115">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="5e6d9-116">Wählen Sie auf der Registerkarte **Verwaltung** die Option **Client Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-116">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="5e6d9-117">Klicken Sie mit der rechten Maustaste auf **Standard Client Einstellungen**, und wählen Sie dann **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-117">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="5e6d9-118">Wählen Sie im Fenster **Standardeinstellungen** den Eintrag **Hardware Inventory**aus.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-118">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="5e6d9-119">Klicken Sie auf **Klassen einrichten**, und klicken Sie dann auf **importieren**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-119">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="5e6d9-120">Wählen Sie im daraufhin geöffneten Browser Ihre **MOF** -Datei aus, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-120">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="5e6d9-121">Das Fenster " **Zusammenfassung importieren** " wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-121">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="5e6d9-122">Stellen Sie im Fenster **Zusammenfassung importieren** sicher, dass die Option zum Importieren von Hardwareinventurklassen und Kurseinstellungen ausgewählt ist, und klicken Sie dann auf **importieren**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-122">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="5e6d9-123">Klicken Sie im Fenster **Hardware Inventurklassen** und im Fenster **Standardeinstellungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-123">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="5e6d9-124">Aktivieren Sie die **Win32-_Tpm** Klasse wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-124">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="5e6d9-125">Öffnen Sie die **SystemCenter2012 ConfigurationManager-Konsole** , und wählen Sie die Registerkarte **Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-125">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="5e6d9-126">Wählen Sie auf der Registerkarte **Verwaltung** die Option **Client Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-126">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="5e6d9-127">Klicken Sie mit der rechten Maustaste auf **Standard Client Einstellungen**, und wählen Sie dann **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-127">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="5e6d9-128">Wählen Sie im Fenster **Standardeinstellungen** den Eintrag **Hardware Inventory**aus.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-128">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="5e6d9-129">Klicken Sie auf **Klassen einstellen**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-129">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="5e6d9-130">Scrollen Sie im Hauptfenster nach unten, und wählen Sie dann die TPM-Klasse **(Win32 \ _Tpm)** aus.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-130">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="5e6d9-131">Stellen Sie sicher, dass unter **TPM**die **SpecVersion** -Eigenschaft ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-131">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="5e6d9-132">Klicken Sie im Fenster **Hardware Inventurklassen** und im Fenster **Standardeinstellungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-132">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="5e6d9-133">So bearbeiten Sie die SMS \ _def. MOF-Datei für Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="5e6d9-133">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="5e6d9-134">Navigieren Sie auf dem Configuration Manager-Server zum Speicherort der **SMS \ _def. MOF** -Datei:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-134">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="5e6d9-135">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="5e6d9-135">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="5e6d9-136">Bei einer Standardinstallation ist der Installationspfad% Drive% \\Program Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-136">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="5e6d9-137">Kopieren Sie den folgenden Code, und fügen Sie ihn dann an **SMS \ _def. MOF** -Datei an, um der Datei die folgenden erforderlichen MBAM-Klassen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-137">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=32|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=64|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy_64: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="5e6d9-138">Ändern Sie die **Win32-_Tpm** Klasse wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-138">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="5e6d9-139">Setzen Sie **SMS \ _REPORT** in den Klassenattributen auf **true** .</span><span class="sxs-lookup"><span data-stu-id="5e6d9-139">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="5e6d9-140">Stellen Sie im **SpecVersion** -Eigenschaftenattribut **SMS \ _REPORT** auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-140">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

    <span data-ttu-id="5e6d9-141">Sie **haben einen Vorschlag für MBAM**?</span><span class="sxs-lookup"><span data-stu-id="5e6d9-141">**Got a suggestion for MBAM**?</span></span> <span data-ttu-id="5e6d9-142">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-142">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> <span data-ttu-id="5e6d9-143">**Haben Sie ein MBAM Problem**?</span><span class="sxs-lookup"><span data-stu-id="5e6d9-143">**Got a MBAM issue**?</span></span> <span data-ttu-id="5e6d9-144">Verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5e6d9-144">Use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="5e6d9-145">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5e6d9-145">Related topics</span></span>


[<span data-ttu-id="5e6d9-146">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</span><span class="sxs-lookup"><span data-stu-id="5e6d9-146">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)

[<span data-ttu-id="5e6d9-147">Bearbeiten der Datei „Configuration.mof“</span><span class="sxs-lookup"><span data-stu-id="5e6d9-147">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

[<span data-ttu-id="5e6d9-148">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="5e6d9-148">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

 

 
## <span data-ttu-id="5e6d9-149">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="5e6d9-149">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5e6d9-150">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-150">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5e6d9-151">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5e6d9-151">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




