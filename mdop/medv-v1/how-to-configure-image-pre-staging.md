---
title: So konfigurieren Sie die Vorabbereitstellung von Images
description: So konfigurieren Sie die Vorabbereitstellung von Images
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811737"
---
# So konfigurieren Sie die Vorabbereitstellung von Images


**Hinweis**  Bild-Pre-Staging ist nur für den anfänglichen Bild Download hilfreich. Es wird für die Bildaktualisierung nicht unterstützt.

 

## So konfigurieren Sie die Vorabbereitstellung von Images


**So konfigurieren Sie das Pre-Staging von Bildern**

1.  Erstellen Sie auf dem Clientcomputer unter dem Bildspeicher Verzeichnis einen Ordner für das Pre-Staging-Bild, und nennen Sie es *MED-V-Bilder*.

    **Hinweis**  Dieser Ordner muss als *MED-V-Bilder*bezeichnet werden.

     

2.  Erstellen Sie im Ordner MED-V Images einen Unterordner, und geben Sie ihm den Namen *PrestagedImages*.

    **Hinweis**  Dieser Ordner muss *PrestagedImages*genannt werden.

     

3.  Um Zugriffsteuerungslisten (ACL)-Sicherheit auf den *MED-V Images-* Ordner anzuwenden, legen Sie die folgende ACL:

    **NT AUTHORITY\\Authenticated-Benutzer: (OI) (CI) (spezieller Zugriff:)**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 Datei \ _APPEND \ _data**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Hinweis**  Es wird empfohlen, ACL-Sicherheit auf den *MED-V Images-* Ordner anzuwenden.

     

4.  Wenn Sie ACL-Sicherheit auf den *PrestagedImages* -Ordner anwenden möchten, legen Sie die folgende ACL ab:

    **NT AUTHORITY\\Authenticated-Benutzer: (OI) (CI) (spezieller Zugriff:)**

    **Lesen \ _CONTROL**

    **Synchronisieren**

    **Datei \ _GENERIC \ _READ**

    **Datei \ _READ \ _data**

    **Datei \ _READ \ _EA**

    **Datei \ _READ \ _ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Hinweis**  Es wird empfohlen, ACL-Sicherheit auf den *PrestagedImages* -Ordner anzuwenden.

     

5.  Drücken Sie die Bilddateien (CKM und Index Dateien) in den *PrestagedImages* -Ordner.

    **Hinweis**  Nachdem die Bilddateien in den Ordner "Pre-stage" verschoben wurden, empfiehlt es sich, eine Datenintegritätsprüfung durchzuführen und die Dateien schreibgeschützt zu markieren.

     

6.  Fügen Sie den folgenden Parameter in die MED-V-Clientinstallation ein: *Client.MSI VMSFOLDER = "C:\\MED-V-Bilder"*.

## Aktualisieren des Standorts vor der Phase


**So aktualisieren Sie den Standort vor der Phase**

1.  Der Registrierungsschlüssel, *PrestagedImagesPath*, verweist auf die Standardbild Position. Die Datei befindet sich im folgenden Verzeichnis:

    -   Auf einem x86- `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   Auf einem x64- `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  Wenn sich das Bild an einem anderen Speicherort befindet, ändern Sie den Pfad.

 

 





