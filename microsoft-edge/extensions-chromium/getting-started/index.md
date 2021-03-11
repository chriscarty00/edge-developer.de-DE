---
description: Erfahren Sie mehr über Chromium-Erweiterungen und grundlegende Konzepte zum Erstellen von Erweiterungen.
title: Microsoft Edge-Erweiterungen (Chromium) – Konzepte und Architektur
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge Chromium, Webentwicklung, html, css, javascript, Entwickler, Erweiterungen
ms.openlocfilehash: 05732287bc1a782ed5830d5e7028cf5580f3b605
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397924"
---
# <a name="extension-concepts-and-architecture"></a>Erweiterungen – Konzepte und Architektur  

Dieser Artikel bietet eine kurze Einführung in Konzepte, die Ihnen beim Erstellen einer Erweiterung helfen.  Um Microsoft Edge-Erweiterungen \(Chromium\) besser zu verstehen, lesen Sie die nachstehenden Informationen zur Funktionsweise von Multi-Tab-Browsern.  

## <a name="understand-how-browsers-work"></a>Grundlegendes zur Funktionsweise von Browsern  

Nachfolgend sind hilfreiche Informationen aufgeführt, die Sie vor dem Erstellen Ihrer Erweiterung benötigen.  

1.  Jeder Browsertab ist von jedem anderen Tab isoliert. Jeder Tab wird in einem separaten Thread ausgeführt, der wiederum von anderen Browsertabs und Threads isoliert ist.  
    
    :::image type="complex" source="./media/index-image1-browsertabs.png" alt-text="Ein Thread pro Browsertab" lightbox="./media/index-image1-browsertabs.png":::
       Ein Thread pro Browsertab  
    :::image-end:::  
    
1.  Jeder Tab verarbeitet eine GET-Anforderung.  Jeder Tab verwendet eine URL, um einen einzelnen Datenstrom zu erhalten, bei dem es sich normalerweise um ein HTML-Dokument handelt.  Dieser einzelne Datenstrom oder diese Seite enthält Anweisungen wie JavaScript einschließlich Tags, Bildverweise, CSS-Verweise und vieles mehr.  Alle Ressourcen werden auf diese Tabseite heruntergeladen, und anschließend wird die Seite in dem Tab gerendert.  
1.  Jeder Tab kommuniziert mit einem Remoteserver.  Jeder Tab wird in einer isolierten Umgebung ausgeführt.  Jeder Tab bleibt mit dem Internet verbunden, ist jedoch von anderen Tabs isoliert.  In einem Tab kann JavaScript zur Kommunikation mit einem Server ausgeführt werden.  Der Server ist der Ursprungsserver für die erste GET-Anforderung, die in die URL-Leiste des Tabs eingegeben wurde.  
1.  Im Erweiterungsmodell wird ein anderes Kommunikationsmodell verwendet.  Ähnlich wie bei einer Tabseite wird eine Erweiterung in einem einzelnen Thread ausgeführt, der von anderen Tabseitenthreads isoliert ist.  Ein Tab sendet einzelne GET-Anforderungen an Remoteserver und rendert dann die Seite.  Eine Erweiterung funktioniert jedoch ähnlich wie ein Remoteserver.  Durch das Installieren einer Erweiterung in einem Browser wird ein eigenständiger Webserver im Browser erstellt.  Die Erweiterung ist von allen Tabseiten isoliert.  
    
    :::image type="complex" source="./media/index-image3-upsidedown.png" alt-text="Bei Erweiterungen wird ein anderes Kommunikationsmodell verwendet" lightbox="./media/index-image3-upsidedown.png":::
       Bei Erweiterungen wird ein anderes Kommunikationsmodell verwendet  
    :::image-end:::  
    
## <a name="extension-architecture"></a>Die Architektur von Erweiterungen  

Nachfolgend sind hilfreiche Informationen zur Architektur einer Erweiterung aufgeführt.  

1.  Das Webserver-Bündel der Erweiterung.  Eine Erweiterung ist ein Bündel von Webressourcen.  Die Webressourcen ähneln anderen Ressourcen, die Sie \(der Webentwickler\) auf Webservern veröffentlichen.  Beim Erstellen einer Erweiterung bündeln Sie die Webressourcen in einer ZIP-Datei.  
    
    Die ZIP-Datei enthält HTML-, CSS-, JavaScript- und Bilddateien.  Im Stammverzeichnis der ZIP-Datei ist eine weitere Datei erforderlich.  Bei dieser weiteren Datei handelt es sich um die Manifestdatei mit dem Namen `manifest.json`.  Die Manifestdatei ist die Blaupause Ihrer Erweiterung und umfasst die Version Ihrer Erweiterung, den Titel, die Berechtigungen, die für ihre Ausführung erforderlich sind, und so weiter.  
    
1.  Starten des Erweiterungsservers.  Webserver enthalten Ihr Webbündel.  Ein Browser navigiert zu URLs auf dem Server und lädt die im Browser zu rendernde Datei herunter.  Ein Browser navigiert mithilfe von Zertifikaten, Konfigurationsdateien und so weiter.  Wenn eine `index.html`-Datei angegeben ist, wird die Datei an einem bestimmten Ort auf dem Webserver gespeichert.  
    
    Wenn Sie eine Erweiterung verwenden, gelangt die Tabseite Ihres Browsers mithilfe der Erweiterungslaufzeit zum Webbundle Ihrer Erweiterung.  Die Erweiterungslaufzeit liefert die Dateien aus der URL `extension://{some-long-unique-identifier}/index.html`, wobei `{some-long-unique-identifier}` ein eindeutiger Bezeichner ist, der der Erweiterung bei der Installation zugewiesen wird.  Jede Erweiterung verwendet einen anderen eindeutigen Bezeichner.  Jeder Bezeichner verweist auf das Webbundle, das in Ihrem Browser installiert ist.  
    
1.  Eine Erweiterung kann mit Tab und der Browsersymbolleiste kommunizieren.  Eine Erweiterung kann mit der Symbolleiste Ihres Browsers interagieren.  Jede Erweiterung verwaltet die Ausführung von Tabseiten in separaten Threads, und die DOM-Manipulation auf jeder Tabseite ist isoliert.  Eine Erweiterung verwendet die Erweiterungs-API für die Kommunikation zwischen der Erweiterung und den Tabseiten.  Die Erweiterungs-API bietet zusätzliche Funktionen wie Benachrichtigungsverwaltung, Speicherverwaltung und so weiter.  
    
    Genau wie Webserver wartet eine Erweiterung auf Benachrichtigungen, wenn der Browser geöffnet ist.  Erweiterungen und Tabseiten werden in Threads ausgeführt, die voneinander isoliert sind.  Damit eine Erweiterung mit einer beliebigen Tabseite funktioniert, verwenden Sie die Erweiterungs-API, und legen Sie die Berechtigungen in der Manifestdatei fest.  
    
1.  Eine Erweiterung bietet bei der Installation Opt-In-Berechtigungen.  Sie geben die Erweiterungsberechtigungen in der Datei `manifest.json` an.  Wenn ein Benutzer eine Erweiterung installiert, werden Informationen zu den Berechtigungen angezeigt, die für die Erweiterung erforderlich sind.  Je nach Art der erforderlichen Berechtigung kann die Erweiterung Informationen aus dem Browser extrahieren und verwenden.  
    
## <a name="next-steps"></a>Nächste Schritte  

Informationen zu den ersten Schritte mit Ihrer Erweiterung finden Sie unter [Erstellen eines Lernprogramms zu Erweiterungen][CreateAnExtensionPart1].  

<!-- links -->  

[CreateAnExtensionPart1]: ./part1-simple-extension.md "Erstellen eines Lernprogramms zu Erweiterungen (Teil 1) | Microsoft-Dokumentation"  
