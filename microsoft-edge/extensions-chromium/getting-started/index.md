---
description: Erfahren Sie mehr über Chromium-Erweiterungen und kernige Konzepte zum Erstellen von Erweiterungen.
title: Microsoft Edge (Chromium) Extensions Konzepte und Architektur
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, web development, html, css, javascript, developer, extensions
ms.openlocfilehash: 05732287bc1a782ed5830d5e7028cf5580f3b605
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397924"
---
# <a name="extension-concepts-and-architecture"></a>Erweiterungskonzepte und -architektur  

Dieser Artikel enthält eine kurze Einführung in Konzepte, mit deren Hilfe Sie eine Erweiterung erstellen können.  Um Microsoft Edge \(Chromium\) -Erweiterungen zu verstehen, folgen Sie, um zu verstehen, wie Multi-Tab-Browser funktionieren.  

## <a name="understand-how-browsers-work"></a>Verstehen der Funktionsweise von Browsern  

Die folgende Liste enthält hilfreiche Informationen, die Sie vor dem Erstellen Ihrer Erweiterung verstehen können.  

1.  Jede Browserregisterkarte ist von jeder anderen Registerkarte isoliert.  Jede Registerkarte wird in einem separaten Thread ausgeführt, der von anderen Browserregisterkarten und Threads isoliert ist.  
    
    :::image type="complex" source="./media/index-image1-browsertabs.png" alt-text="Ein Thread pro Browserregisterkarte" lightbox="./media/index-image1-browsertabs.png":::
       Ein Thread pro Browserregisterkarte  
    :::image-end:::  
    
1.  Jede Registerkarte verarbeitet eine GET-Anforderung.  Jede Registerkarte verwendet eine URL, um einen einzelnen Datenstrom zu erhalten, bei dem es sich normalerweise um ein HTML-Dokument handelt.  Dieser einzelne Datenstrom oder diese Seite enthält Anweisungen wie JavaScript einschließlich Tags, Bildverweise, CSS-Verweise und vieles mehr.  Alle Ressourcen werden auf diese Registerkartenseite heruntergeladen, und dann wird die Seite auf der Registerkarte gerendert.  
1.  Die Kommunikation erfolgt zwischen jeder Registerkarte und einem Remoteserver.  Jede Registerkarte wird in einer isolierten Umgebung ausgeführt.  Jede Registerkarte ist weiterhin mit dem Internet verbunden, jede ist jedoch von anderen Registerkarten isoliert.  Auf einer Registerkarte kann JavaScript ausgeführt werden, um mit einem Server zu kommunizieren.  Der Server ist der Ursprungsserver für die erste GET-Anforderung, die in die URL-Leiste der Registerkarte eingegeben wurde.  
1.  Das Erweiterungsmodell verwendet ein anderes Kommunikationsmodell.  Ähnlich wie bei einer Registerkartenseite wird eine Erweiterung in einem einzelnen Thread ausgeführt, der von anderen Registerkartenseitenthreads isoliert ist.  Eine Registerkarte sendet einzelne GET-Anforderungen an Remoteserver und rendert dann die Seite.  Eine Erweiterung funktioniert jedoch ähnlich wie ein Remoteserver.  Durch das Installieren einer Erweiterung in einem Browser wird ein eigenständiger Webserver im Browser erstellt.  Die Erweiterung ist von allen Registerkartenseiten isoliert.  
    
    :::image type="complex" source="./media/index-image3-upsidedown.png" alt-text="Erweiterungen verwenden ein anderes Kommunikationsmodell" lightbox="./media/index-image3-upsidedown.png":::
       Erweiterungen verwenden ein anderes Kommunikationsmodell  
    :::image-end:::  
    
## <a name="extension-architecture"></a>Architektur der Erweiterung  

In der folgenden Liste sind hilfreiche Informationen zur Architektur einer Erweiterung aufgeführt.  

1.  Das Erweiterungswebserverbündel.  Eine Erweiterung ist ein Bündel von Webressourcen.  Die Webressourcen ähneln anderen Ressourcen, die Sie \(der Webentwickler\) auf Webservern veröffentlichen.  Beim Erstellen einer Erweiterung bündeln Sie die Webressourcen in einer ZIP-Datei.  
    
    Die ZIP-Datei enthält HTML-, CSS-, JavaScript- und Bilddateien.  Im Stammverzeichnis der ZIP-Datei ist eine weitere Datei erforderlich.  Die andere Datei ist die Manifestdatei mit dem Namen `manifest.json` .  Die Manifestdatei ist der Blueprint Ihrer Erweiterung und enthält die Version Ihrer Erweiterung, den Titel, die berechtigungen, die für die Ausführung der Erweiterung erforderlich sind, und so weiter.  
    
1.  Starten des Erweiterungsservers.  Webserver enthalten Ihr Webbundepaket.  Ein Browser navigiert zu URLs auf dem Server und lädt die Datei zum Rendern im Browser herunter.  Ein Browser navigiert mithilfe von Zertifikaten, Konfigurationsdateien und so weiter.  Wenn eine Datei angegeben wird, wird die Datei an einem bestimmten `index.html` Speicherort auf dem Webserver gespeichert.  
    
    Wenn Sie eine Erweiterung verwenden, wird die Registerkartenseite Ihres Browsers mithilfe der Erweiterungslaufzeit zum Webbunde ihrer Erweiterung angezeigt.  Die Erweiterungslaufzeit dient den Dateien aus der URL , wobei ein eindeutiger Bezeichner ist, der der Erweiterung bei `extension://{some-long-unique-identifier}/index.html` `{some-long-unique-identifier}` der Installation zugewiesen ist.  Jede Erweiterung verwendet einen anderen eindeutigen Bezeichner.  Jeder Bezeichner verweist auf das Webbundepaket, das in Ihrem Browser installiert ist.  
    
1.  Eine Erweiterung kann mit Registerkarten und der Browsersymbolleiste kommunizieren.  Eine Erweiterung kann mit der Symbolleiste Ihres Browsers interagieren.  Jede Erweiterung verwaltet die Ausführung von Registerkartenseiten in separaten Threads, und die DOM-Manipulation auf jeder Registerkartenseite ist isoliert.  Eine Erweiterung verwendet die Extensions-API, um zwischen der Erweiterung und den Registerkartenseiten zu kommunizieren.  Die Extensions-API bietet zusätzliche Funktionen, die Benachrichtigungsverwaltung, Speicherverwaltung und so weiter umfassen.  
    
    Genau wie Webserver wartet eine Erweiterung auf Benachrichtigungen, wenn der Browser geöffnet ist.  Eine Erweiterungs- und Registerkartenseiten werden in Threads ausgeführt, die voneinander isoliert sind.  Um zu ermöglichen, dass eine Erweiterung mit einer beliebigen Registerkartenseite funktioniert, verwenden Sie die Extensions-API, und legen Sie die Berechtigungen in der Manifestdatei.  
    
1.  Eine Erweiterung bietet bei der Installation Opt-In-Berechtigungen.  Sie geben die Erweiterungsberechtigungen in der Datei `manifest.json` an.  Wenn ein Benutzer eine Erweiterung installiert, werden Informationen zu den berechtigungen angezeigt, die für die Erweiterung erforderlich sind.  Basierend auf der Art der erforderlichen Berechtigung kann die Erweiterung Informationen aus dem Browser extrahieren und verwenden.  
    
## <a name="next-steps"></a>Nächste Schritte  

Informationen zu den ersten Schritte mit Ihrer Erweiterung finden Sie unter [Erstellen eines Erweiterungs-Lernprogramms][CreateAnExtensionPart1].  

<!-- links -->  

[CreateAnExtensionPart1]: ./part1-simple-extension.md "Erstellen eines Erweiterungs-Lernprogramms – Teil 1 | Microsoft Docs"  
