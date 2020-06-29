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
# Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei


Damit die Clientcomputer BitLocker-Kompatibilitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die SMS \ _def. MOF-Datei erstellen oder bearbeiten.

Wenn Sie SystemCenter2012 ConfigurationManager verwenden, müssen Sie die Datei erstellen. Erstellen Sie die Datei auf der Website der obersten Ebene. Die Änderungen werden auf die anderen Websites in Ihrer Infrastruktur repliziert.

In Configuration Manager 2007 ist die Datei bereits vorhanden, sodass Sie Sie nur bearbeiten müssen. **Überschreiben Sie die vorhandene Datei nicht.**

Führen Sie in den folgenden Abschnitten die Anweisungen aus, die der von Ihnen verwendeten Version von Configuration Manager entsprechen.

**So erstellen Sie die SMS \ _def. MOF-Datei für SystemCenter2012 ConfigurationManager**

1.  Navigieren Sie auf dem Configuration Manager-Server zu dem Speicherort, an dem Sie die SMS \ _def. MOF-Datei erstellen müssen, beispielsweise den Desktop.

2.  Erstellen Sie eine Textdatei mit dem Namen **SMS \ _def. MOF** , und kopieren Sie den folgenden Code, um die Datei mit den folgenden SMS \ _def. MOF-MBAM-Klassen zu füllen:

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

3.  Importieren Sie die **SMS \ _def. MOF-** Datei, indem Sie wie folgt vorgehen:

    1.  Öffnen Sie die **SystemCenter2012 ConfigurationManager-Konsole** , und wählen Sie die Registerkarte **Verwaltung** aus.

    2.  Wählen Sie auf der Registerkarte **Verwaltung** die Option **Client Einstellungen**aus.

    3.  Klicken Sie mit der rechten Maustaste auf **Standard Client Einstellungen**, und wählen Sie dann **Eigenschaften**aus.

    4.  Wählen Sie im Fenster **Standardeinstellungen** den Eintrag **Hardware Inventory**aus.

    5.  Klicken Sie auf **Klassen einrichten**, und klicken Sie dann auf **importieren**.

    6.  Wählen Sie im daraufhin geöffneten Browser Ihre **MOF** -Datei aus, und klicken Sie dann auf **Öffnen**. Das Fenster " **Zusammenfassung importieren** " wird geöffnet.

    7.  Stellen Sie im Fenster **Zusammenfassung importieren** sicher, dass die Option zum Importieren von Hardwareinventurklassen und Kurseinstellungen ausgewählt ist, und klicken Sie dann auf **importieren**.

    8.  Klicken Sie im Fenster **Hardware Inventurklassen** und im Fenster **Standardeinstellungen** auf **OK**.

4.  Aktivieren Sie die **Win32-_Tpm** Klasse wie folgt:

    1.  Öffnen Sie die **SystemCenter2012 ConfigurationManager-Konsole** , und wählen Sie die Registerkarte **Verwaltung** aus.

    2.  Wählen Sie auf der Registerkarte **Verwaltung** die Option **Client Einstellungen**aus.

    3.  Klicken Sie mit der rechten Maustaste auf **Standard Client Einstellungen**, und wählen Sie dann **Eigenschaften**aus.

    4.  Wählen Sie im Fenster **Standardeinstellungen** den Eintrag **Hardware Inventory**aus.

    5.  Klicken Sie auf **Klassen einstellen**.

    6.  Scrollen Sie im Hauptfenster nach unten, und wählen Sie dann die TPM-Klasse **(Win32 \ _Tpm)** aus.

    7.  Stellen Sie sicher, dass unter **TPM**die **SpecVersion** -Eigenschaft ausgewählt ist.

    8.  Klicken Sie im Fenster **Hardware Inventurklassen** und im Fenster **Standardeinstellungen** auf **OK**.

**So bearbeiten Sie die SMS \ _def. MOF-Datei für Configuration Manager 2007**

1.  Navigieren Sie auf dem Configuration Manager-Server zum Speicherort der **SMS \ _def. MOF** -Datei:

    &lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv\\

    Bei einer Standardinstallation ist der Installationspfad% Drive% \\Program Files (x86) \\Microsoft Configuration Manager.

2.  Kopieren Sie den folgenden Code, und fügen Sie ihn dann an **SMS \ _def. MOF** -Datei an, um der Datei die folgenden erforderlichen MBAM-Klassen hinzuzufügen:

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

3.  Ändern Sie die **Win32-_Tpm** Klasse wie folgt:

    -   Setzen Sie **SMS \ _REPORT** in den Klassenattributen auf **true** .

    -   Stellen Sie im **SpecVersion** -Eigenschaftenattribut **SMS \ _REPORT** auf **true** fest.

    Sie **haben einen Vorschlag für MBAM**? [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. **Haben Sie ein MBAM Problem**? Verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Verwandte Themen


[MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)

[Bearbeiten der Datei „Configuration.mof“](edit-the-configurationmof-file-mbam-25.md)

[MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

 

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




