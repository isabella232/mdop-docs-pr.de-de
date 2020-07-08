---
title: So ändern Sie die Cachegröße des Servers
description: So ändern Sie die Cachegröße des Servers
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807343"
---
# So ändern Sie die Cachegröße des Servers


Mit dem folgenden Verfahren können Sie die Cachegröße für jeden Server direkt in der Application Virtualization Server-Verwaltungskonsole ändern.

**Hinweis**  Zwar können Sie die Cachegröße ändern, es wird jedoch empfohlen, die Cachegröße auf die Standardwerte festzulegen, es sei denn, Sie müssen die Größe speziell für die Konfiguration ändern.

 

**So ändern Sie die Größe des Server Caches**

1.  Klicken Sie im linken Bereich auf den Knoten **Servergruppen** , um die Liste der Servergruppen zu erweitern.

2.  Doppelklicken Sie im **Ergebnis** Bereich auf die gewünschte Servergruppe, um die Liste der Server in der Gruppe anzuzeigen.

3.  Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste auf den gewünschten Server, und wählen Sie **Eigenschaften**aus.

4.  Wählen Sie die Registerkarte **erweitert** aus.

5.  Geben Sie im Feld **Maximale Speicherzuteilung** für den Server Cache einen Wert ein, und geben Sie einen Wert für die Schwellenwert Warnstufe im Feld Warnungs **Speicherzuteilung** ein.

6.  Geben Sie einen Wert in das Feld **Maximale Block Größe** ein. Diese Zahl muss größer oder gleich der maximalen Blockgröße des größten Pakets sein, das vom Server gestreamt wird.

7.  Klicken Sie auf **OK**.

## Verwandte Themen


[So ändern Sie den Server-Port](how-to-change-the-server-port.md)

[So verwalten Sie Server in der Server Management Console](how-to-manage-servers-in-the-server-management-console.md)

 

 





