---
title: Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei
description: Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei
author: dansimp
ms.assetid: d1747e43-484e-4031-a63b-6342fe588aa2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/04/2017
ms.openlocfilehash: 15f1d1a1c19cb9b19b7d83534e035d5410720ce9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810000"
---
# <span data-ttu-id="d1369-103">Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei</span><span class="sxs-lookup"><span data-stu-id="d1369-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="d1369-104">Damit die Clientcomputer BitLocker-Kompatibilitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die SMS \ _def. MOF-Datei erstellen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d1369-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="d1369-105">Wenn Sie SystemCenter2012 ConfigurationManager verwenden, müssen Sie die Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1369-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

<span data-ttu-id="d1369-106">In Configuration Manager 2007 ist die Datei bereits vorhanden, sodass Sie Sie nur bearbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="d1369-106">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> <span data-ttu-id="d1369-107">Über **schreiben Sie die vorhandene Datei nicht**.</span><span class="sxs-lookup"><span data-stu-id="d1369-107">**Do not overwrite the existing file**.</span></span>

<span data-ttu-id="d1369-108">Führen Sie in den folgenden Abschnitten die Anweisungen aus, die der von Ihnen verwendeten Version von Configuration Manager entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d1369-108">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="d1369-109">So erstellen Sie die SMS \ _def. MOF-Datei für SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="d1369-109">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="d1369-110">Navigieren Sie auf dem Configuration Manager-Server zu dem Speicherort, an dem Sie die SMS \ _def. MOF-Datei erstellen müssen, beispielsweise den Desktop.</span><span class="sxs-lookup"><span data-stu-id="d1369-110">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="d1369-111">Erstellen Sie eine Textdatei mit dem Namen **SMS \ _def. MOF** , und kopieren Sie den folgenden Code, um die Datei mit den folgenden SMS \ _def. MOF-MBAM-Klassen zu füllen:</span><span class="sxs-lookup"><span data-stu-id="d1369-111">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

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

        //MBAM agent fields
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

3.  <span data-ttu-id="d1369-112">Importieren Sie die **SMS \ _def. MOF-** Datei, indem Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="d1369-112">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="d1369-113">Öffnen Sie die **SystemCenter2012 ConfigurationManager-Konsole** , und wählen Sie die Registerkarte **Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="d1369-113">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="d1369-114">Wählen Sie auf der Registerkarte **Verwaltung** die Option **Client Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="d1369-114">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="d1369-115">Klicken Sie mit der rechten Maustaste auf **Standard Client Einstellungen**, und wählen Sie dann **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="d1369-115">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="d1369-116">Wählen Sie im Fenster **Standardeinstellungen** den Eintrag **Hardware Inventory**aus.</span><span class="sxs-lookup"><span data-stu-id="d1369-116">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="d1369-117">Klicken Sie auf **Klassen einrichten**, und klicken Sie dann auf **importieren**.</span><span class="sxs-lookup"><span data-stu-id="d1369-117">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="d1369-118">Wählen Sie im daraufhin geöffneten Browser Ihre **MOF** -Datei aus, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="d1369-118">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="d1369-119">Das Fenster " **Zusammenfassung importieren** " wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d1369-119">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="d1369-120">Stellen Sie im Fenster **Zusammenfassung importieren** sicher, dass die Option zum Importieren von Hardwareinventurklassen und Kurseinstellungen ausgewählt ist, und klicken Sie dann auf **importieren**.</span><span class="sxs-lookup"><span data-stu-id="d1369-120">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="d1369-121">Klicken Sie im Fenster **Hardware Inventurklassen** und im Fenster **Standardeinstellungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1369-121">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="d1369-122">Aktivieren Sie die **Win32-_Tpm** Klasse wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d1369-122">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="d1369-123">Öffnen Sie die **SystemCenter2012 ConfigurationManager-Konsole** , und wählen Sie die Registerkarte **Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="d1369-123">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="d1369-124">Wählen Sie auf der Registerkarte **Verwaltung** die Option **Client Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="d1369-124">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="d1369-125">Klicken Sie mit der rechten Maustaste auf **Standard Client Einstellungen**, und wählen Sie dann **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="d1369-125">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="d1369-126">Wählen Sie im Fenster **Standardeinstellungen** den Eintrag **Hardware Inventory**aus.</span><span class="sxs-lookup"><span data-stu-id="d1369-126">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="d1369-127">Klicken Sie auf **Klassen einstellen**.</span><span class="sxs-lookup"><span data-stu-id="d1369-127">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="d1369-128">Scrollen Sie im Hauptfenster nach unten, und wählen Sie dann die TPM-Klasse **(Win32 \ _Tpm)** aus.</span><span class="sxs-lookup"><span data-stu-id="d1369-128">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="d1369-129">Stellen Sie sicher, dass unter **TPM**die **SpecVersion** -Eigenschaft ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d1369-129">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="d1369-130">Klicken Sie im Fenster **Hardware Inventurklassen** und im Fenster **Standardeinstellungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1369-130">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="d1369-131">So bearbeiten Sie die SMS \ _def. MOF-Datei für Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="d1369-131">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="d1369-132">Navigieren Sie auf dem Configuration Manager-Server zum Speicherort der **SMS \ _def. MOF** -Datei:</span><span class="sxs-lookup"><span data-stu-id="d1369-132">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="d1369-133">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="d1369-133">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="d1369-134">Bei einer Standardinstallation ist der Installationspfad% Drive% \\Program Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1369-134">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="d1369-135">Kopieren Sie den folgenden Code, und fügen Sie ihn dann an **SMS \ _def. MOF** -Datei an, um der Datei die folgenden erforderlichen MBAM-Klassen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="d1369-135">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

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

3.  <span data-ttu-id="d1369-136">Ändern Sie die **Win32-_Tpm** Klasse wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d1369-136">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="d1369-137">Setzen Sie **SMS \ _REPORT** in den Klassenattributen auf **true** .</span><span class="sxs-lookup"><span data-stu-id="d1369-137">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="d1369-138">Stellen Sie im **SpecVersion** -Eigenschaftenattribut **SMS \ _REPORT** auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="d1369-138">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

## <span data-ttu-id="d1369-139">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d1369-139">Related topics</span></span>


[<span data-ttu-id="d1369-140">So erstellen oder bearbeiten Sie MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="d1369-140">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

[<span data-ttu-id="d1369-141">Bereitstellen von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="d1369-141">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





