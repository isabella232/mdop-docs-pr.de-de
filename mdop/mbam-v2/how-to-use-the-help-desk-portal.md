---
title: So verwenden Sie das Helpdeskportal
description: So verwenden Sie das Helpdeskportal
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811689"
---
# So verwenden Sie das Helpdeskportal


Die Website "MBAM-Verwaltung und-Überwachung", auch als Helpdesk-Portal bezeichnet, ist eine Verwaltungsschnittstelle zur BitLocker-Laufwerkverschlüsselung, die als Teil der Microsoft BitLocker-Verwaltungs-und-Überwachungsserver-Infrastruktur (MBAM) installiert wird. In den folgenden Abschnitten wird beschrieben, wie Sie diese Website verwenden können, um Berichte zu überprüfen, die Laufwerke der Endbenutzer wiederherzustellen und das TPMs der Endbenutzer zu verwalten.

## <a href="" id="bkmk-reports"></a>Berichte


MBAM sammelt Informationen von Active Directory und Clientcomputern, wodurch Sie verschiedene Berichte ausführen können, um die BitLocker-Nutzung und-Kompatibilität zu überwachen. Über den Abschnitt **Berichte** der Websiteverwaltung und Überwachung können Sie Berichte zu Unternehmenskonformität, einzelnen Computern und wichtigen Wiederherstellungsaktivitäten erstellen. Eine Beschreibung der einzelnen Berichte finden Sie unter [Grundlegendes zu MBAM-Berichten](understanding-mbam-reports-mbam-2.md).

**So greifen Sie auf Berichte zu**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur Website MBAM-Verwaltung und-Überwachung.

2.  Wählen Sie im linken Bereich **Berichte** aus.

3.  Wählen Sie in der oberen Menüleiste den zu generierenden Berichtstyp aus. Wenn Sie Berichte speichern möchten, klicken Sie auf der Menüleiste Berichte auf die Schaltfläche **exportieren** .

Weitere Informationen zum Ausführen von MBAM-Berichten finden Sie unter [so](how-to-generate-mbam-reports-mbam-2.md)wird es gemacht: Erstellen von MBAM-Berichten.

## <a href="" id="bkmk-drirec"></a>Laufwerk Wiederherstellung


Das **Laufwerk Wiederherstellungs** Feature der Verwaltungs-und Überwachungs Website ermöglicht Benutzern mit bestimmten Administratorrollen (beispielsweise Helpdesk-Benutzern) den Zugriff auf Wiederherstellungsschlüssel Daten, die vom MBAM-Client erfasst wurden. Diese Daten können verwendet werden, um auf ein durch BitLocker geschütztes Laufwerk zuzugreifen, wenn BitLocker in den Wiederherstellungsmodus wechselt. Anweisungen zum Wiederherstellen eines Laufwerks, das sich im Wiederherstellungsmodus befindet, finden Sie unter [Wiederherstellen eines Laufwerks im Wiederherstellungsmodus](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).

Sie können auch Laufwerke wiederherstellen, die verschoben wurden oder die beschädigt sind:

-   [So stellen Sie ein verschobenes Laufwerk wieder her](how-to-recover-a-moved-drive-mbam-2.md)

-   [So stellen Sie ein beschädigtes Laufwerk wieder her](how-to-recover-a-corrupted-drive-mbam-2.md)

Weitere Informationen zum Wiederherstellen eines durch BitLocker geschützten Laufwerks finden Sie unter [Durchführen der BitLocker-Verwaltung mit MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).

## <a href="" id="bkmk-manatpm"></a>TPM verwalten


Das Feature "TPM verwalten" der Website "Verwaltung und Überwachung" bietet Benutzern mit bestimmten Administratorrollen (beispielsweise "MBAM Helpdesk-Benutzer") Zugriff auf TPM-Daten, die vom MBAM-Client erfasst wurden. Bei einer TPM-Sperrung kann ein Administrator die Websiteverwaltung und Überwachung verwenden, um die erforderliche Kennwortdatei abzurufen, um das TPM zu entsperren. Anweisungen zum Zurücksetzen eines TPMs nach einer TPM-Sperrung finden Sie unter [Zurücksetzen einer TPM-Sperrung](how-to-reset-a-tpm-lockout-mbam-2.md).

## <a href="" id="bkmk-helpdesk"></a> MBAM Help Desk-Aufgaben


Sie können die Websiteverwaltung und Überwachung für viele administrative Aufgaben verwenden, beispielsweise für die Verwaltung von BitLocker-geschützter Hardware, das Recovery von Laufwerken und das Ausführen von Berichten. Standardmäßig ist die URL für die Websiteverwaltung und Überwachung http:// &lt; *MBAMAdministrationServername* &gt; , Sie können Sie aber während des Installationsvorgangs anpassen.

**Hinweis**  Für den Zugriff auf die verschiedenen Features, die auf der Websiteverwaltung und Überwachung angeboten werden, müssen Sie über die entsprechenden Rollen verfügen, die Ihrem Benutzerkonto zugeordnet sind. Weitere Informationen zum Grundlegendes zu Benutzerrollen finden Sie unter [Verwalten von MBAM-Administrator Rollen](how-to-manage-mbam-administrator-roles-mbam-2.md).

 

Verwenden Sie die folgenden Links, um Informationen zu den Aufgaben zu finden, die Sie mithilfe der Websiteverwaltung und Überwachung ausführen können:

-   [So setzen Sie eine TPM-Sperre zurück](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [So stellen Sie ein verschobenes Laufwerk wieder her](how-to-recover-a-moved-drive-mbam-2.md)

-   [So stellen Sie ein beschädigtes Laufwerk wieder her](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





