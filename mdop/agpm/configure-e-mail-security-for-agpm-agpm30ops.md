---
title: Konfigurieren von E-Mail-Sicherheit für AGPM
description: Konfigurieren von E-Mail-Sicherheit für AGPM
author: dansimp
ms.assetid: 4850ed8e-a1c6-43f0-95c5-853aa66a94ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3694662fd0ed81edacd16cf55ac9760b1be2ba97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807727"
---
# Konfigurieren von E-Mail-Sicherheit für AGPM


E-Mail-Benachrichtigungen, die aufgrund von Aktionen in Advanced Group Policy Management (AGPM) gesendet wurden, werden standardmäßig nicht verschlüsselt und über den SMTP-Port 25 gesendet. Sie können die e-Mail-Sicherheit für AGPM jedoch mithilfe von Registrierungseinstellungen konfigurieren, um anzugeben, ob SSL-Verschlüsselung (Secure Sockets Layer) und welcher SMTP-Port verwendet werden soll.

Durch Verschlüsseln von AGPM-e-Mail-Benachrichtigungen können Sie die Personen, die vertrauliche Informationen über die Sicherheit Ihrer Organisation offen legen, besser schützen. Das Verschlüsseln von e-Mail-Benachrichtigungen wird empfohlen, wenn Sie über Remote-e-Mail-Server weitergeleitet werden und möglicherweise durch einige Konformitätsrichtlinien erforderlich sind.

**Vorsicht**  Durch unsachgemäßes Bearbeiten der Registrierung kann Ihr System schwer beschädigt werden. Bevor Sie Änderungen an der Registrierung vornehmen, sollten Sie alle wichtigen Daten auf dem Computer sichern.

 

Ein Benutzerkonto, das über die Rolle AGPM-Administrator (Vollzugriff) verfügt, das Benutzerkonto der genehmigenden Person, die das in diesen Verfahren verwendete Gruppenrichtlinienobjekt (Group Policy Object, GPO) erstellt hat, oder ein Benutzerkonto, das über die erforderlichen Berechtigungen in AGPM verfügt, ist erforderlich, um diese Verfahren auszuführen. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So konfigurieren Sie die e-Mail-Sicherheit für AGPM mithilfe von Gruppenrichtlinieneinstellungen**

1.  Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle AGPM-Server angewendet wird, für die Sie die e-Mail-Sicherheit konfigurieren möchten. (Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo-agpm30ops.md).)

2.  Erweitern Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** die Ordner **Computer Konfiguration**, **Einstellungen**, **Windows-Einstellungen**und **Registrierung** .

3.  Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf **Registrierung**, zeigen Sie auf **neu**, klicken Sie auf **Sammlungselement**, und geben Sie **AGPM-e-Mail-Sicherheit**ein.

4.  Erstellen Sie ein Registrierungs Einstellungselement, um die Verschlüsselung zu aktivieren:

    1.  Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf **AGPM-e-Mail-Sicherheit**, zeigen Sie auf **neu**, und klicken Sie dann auf **Registrierungselement**.

    2.  Wählen Sie im Dialogfeld **neue Registrierungseigenschaften** die Aktion **Aktualisieren** aus.

    3.  Wählen **Hive**Sie für Hive **HKEY \ _LOCAL \ _MACHINE**aus.

    4.  Geben Sie für **Schlüsselpfad** **SOFTWARE\\Microsoft\\AGPM**.

    5.  Geben Sie für **Wertname** **EncryptSmtp**.

    6.  Wählen Sie unter **Werttyp**die Option **reg \ _DWORD**aus.

    7.  Wählen Sie für **Base**die Option **Decimal**aus, und geben Sie für **Wertdaten den Wert** **1 ein** , um die SSL-Verschlüsselung zu verwenden, oder **0** , damit e-Mails ohne Verschlüsselung gesendet werden können. Standardmäßig werden e-Mail-Nachrichten ohne Verschlüsselung gesendet.

    8.  Klicken Sie auf **OK**.

5.  Erstellen Sie ein Registrierungs Einstellungselement, um den SMTP-Port anzugeben:

    1.  Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf **AGPM-e-Mail-Sicherheit**, zeigen Sie auf **neu**, und klicken Sie dann auf **Registrierungselement**.

    2.  Wählen Sie im Dialogfeld **neue Registrierungseigenschaften** die Aktion **Aktualisieren** aus.

    3.  Wählen **Hive**Sie für Hive **HKEY \ _LOCAL \ _MACHINE**aus.

    4.  Geben Sie im Dialogfeld **Schlüsselpfad** den Namen **SOFTWARE\\Microsoft\\AGPM**ein.

    5.  Geben Sie für **Wertname** **SmtpPort**.

    6.  Wählen Sie unter **Werttyp**die Option **reg \ _DWORD**aus.

    7.  Wählen Sie für **Base**den Wert **Decimal**aus, und geben Sie für **Wertdaten**eine Portnummer für den SMTP-Port ein. Standardmäßig ist der SMTP-Port Port 25, wenn die Verschlüsselung nicht aktiviert ist, oder Port 587, wenn die SSL-Verschlüsselung aktiviert ist.

    8.  Klicken Sie auf **OK**.

6.  Schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** , und aktivieren Sie das Gruppenrichtlinienobjekt, und stellen Sie es bereit. Weitere Informationen finden Sie unter [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm30ops.md).

### Weitere Überlegungen

-   Sie müssen in der Lage sein, ein GPO zu bearbeiten und bereitzustellen, um Registrierungseinstellungen mithilfe von Gruppenrichtlinieneinstellungen zu konfigurieren. Weitere Informationen finden Sie unter [Bearbeiten eines GPO](editing-a-gpo-agpm30ops.md) und [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm30ops.md) .

### Weitere Verweise

-   [Konfigurieren von Advanced Group Policy Management](configuring-advanced-group-policy-management.md)

 

 





