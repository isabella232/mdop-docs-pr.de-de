---
title: So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer
description: So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812139"
---
# So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer


Ein Computernamens Muster für virtuelle Computer kann sowohl für revertible als auch für persistente MED-V-Arbeitsbereiche zugewiesen werden.

-   Revertible – Administratoren können jeder Revertible Med-v Workspace-Instanz einen eindeutigen Namen zuweisen, um zwischen mehreren Computern unterscheiden zu können, die denselben Med-v-Arbeitsbereich verwenden.

-   Persistent – in einem persistenten MED-V-Arbeitsbereich können Administratoren einen Computer so einrichten, dass er während eines Setupskripts umbenannt wird.

## Zuweisen eines Computername-Musters für einen virtuellen Computer zu einem Revertible MED-V-Arbeitsbereich


**So weisen Sie einem revertible MED-V-Arbeitsbereich ein Computernamens Muster eines virtuellen Computers zu**

1.  Klicken Sie auf den revertible MED-V-Arbeitsbereich, den Sie konfigurieren möchten.

2.  Aktivieren Sie im Abschnitt **Revertible VM Setup** das Kontrollkästchen **VM auf der Grundlage des Computernamens Musters umbenennen** .

3.  Geben Sie im Abschnitt **VM-Computer Namensmuster** das Muster ein, das für die Benennung von Bildern virtueller Computer verwendet werden soll, und verwenden Sie die folgenden Optionen:

    -   **Konstant**– geben Sie freien Text ein, der auf allen Computern mit dem MED-V-Arbeitsbereich konstant ist.

    -   **Variabel**– geben Sie eine Variable ein, indem Sie auf **Variable einfügen**klicken, und wählen Sie eine der folgenden Optionen aus:

        -   **Benutzername**

        -   **Domänenname**

        -   **Hostname**

        -   **Name des Arbeitsbereichs**

        -   **Name des virtuellen Computers**

        Die ausgewählte Variable ist spezifisch für den Computer, der den MED-V-Arbeitsbereich verwendet. Wenn beispielsweise der **Domänenname** ausgewählt ist, enthält der eindeutige Name für jeden Computer den Domänennamen des Computers.

    -   **Zufällige Zeichen**: Geben Sie "\ #" für jedes zufällige Zeichen ein, das in das Muster aufgenommen werden soll. Jeder Computer, der den MED-V-Arbeitsbereich verwendet, hat ein Suffix der angegebenen Länge, das willkürlich generiert wird.

    **Hinweis:**  
    Der Computername hat eine Grenze von 15 Zeichen. Wenn das Muster die Grenze überschreitet, wird es abgeschnitten.



4.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

    **Hinweis:**  
    Ein revertible VM-Computernamens Muster kann nur zugewiesen werden, wenn **der VM-Name auf der Grundlage der Computernamens Muster** (im Abschnitt **revertible VM-Setup** ) umbenannt wird.



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## Zuweisen eines Computer namens Musters für einen virtuellen Computer zu einem persistenten MED-V-Arbeitsbereich


**So weisen Sie einem persistenten MED-V-Arbeitsbereich ein Computernamens Muster eines virtuellen Computers zu**

1.  Klicken Sie auf den persistenten MED-V-Arbeitsbereich, den Sie konfigurieren möchten.

2.  Klicken Sie im Abschnitt **persistent VM Setup** auf **Skript-Editor**.

3.  Klicken Sie im Dialogfeld **Skriptaktionen** auf **Hinzufügen**, und klicken Sie im Untermenü auf **Computer umbenennen**.

4.  Klicken Sie auf **OK** , um das Dialogfeld **Skriptaktionen** zu schließen.

5.  Geben Sie auf der Registerkarte **VM-Setup** im Abschnitt **VM-Computer Namensmuster** das Muster ein, das zum Umbenennen des Computers verwendet werden soll, indem Sie Folgendes verwenden:

    -   **Konstant**– geben Sie kostenlosen Text ein, der in den Computernamen aufgenommen werden soll.

    -   **Variabel**– geben Sie eine Variable ein, indem Sie auf **Variable einfügen**klicken, und wählen Sie eine der folgenden Optionen aus:

        -   **Benutzername**

        -   **Domänenname**

        -   **Hostname**

        -   **Name des Arbeitsbereichs**

        -   **Name des virtuellen Computers**

        Die ausgewählte Variable ist spezifisch für den Computer, der umbenannt wird. Wenn beispielsweise **Domänenname** ausgewählt ist, enthält der Computername den Domänennamen des Computers.

    -   **Zufällige Zeichen**: Geben Sie "\ #" für jedes zufällige Zeichen ein, das in das Muster aufgenommen werden soll. Auf dem Computer wird ein Suffix der angegebenen Länge angegeben, das nach dem Zufallsprinzip generiert wird.

    **Hinweis:**  
    Der Computername hat eine Grenze von 15 Zeichen. Wenn das Muster die Grenze überschreitet, wird es abgeschnitten.



6.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

    **Hinweis:**  
    Der Computer wird nur dann umbenannt, wenn er im Dialogfeld **Skriptaktionen** als Aktion eingestellt ist. Ausführliche Informationen finden Sie unter [so wird es gemacht: Einrichten von Skriptaktionen](how-to-set-up-script-actions.md).



## Verwandte Themen


[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

[Erstellen eines MED-V-Arbeitsbereichs](creating-a-med-v-workspacemedv-10-sp1.md)

[So richten Sie Skriptaktionen ein](how-to-set-up-script-actions.md)

[Beispiele für VM-Konfigurationen](examples-of-virtual-machine-configurationsv2.md)









