---
description: Prozessmodell
title: Prozessmodell
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8548308896815266fbd1e150da979b56cfb268e2
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895565"
---
# Prozessmodell  

WebView2 verwendet das gleiche Prozessmodell wie der Microsoft Edge-Browser.  Weitere Informationen zum Browser-Prozessmodell finden Sie unter [Browser Architektur – Innenansicht des modernen Webbrowsers][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]. 

Ein Browserprozess ist mit den Renderer-Prozessen und anderen Dienstprogrammen verknüpft, wie in diesem Artikel beschrieben.  Darüber hinaus gibt es im Fall von WebView2 eine Host-APP, die mithilfe von WebView2 Prozesse anfordert.  

:::image type="complex" source="../media/process-model-1.png" alt-text="Prozess 1" lightbox="../media/process-model-1.png":::
   Prozess 1  
:::image-end:::  

Ein Browserprozess wird pro benutzerdatenordner in einer Benutzersitzung angegeben, die einem beliebigen WebView2-Prozess dient, der den benutzerdatenordner angibt.  Dies bedeutet, dass ein Browserprozess möglicherweise mehrere anfordernde Prozesse bedient und ein anfordernder Prozess möglicherweise mehrere Browserprozesse verwendet.  

:::image type="complex" source="../media/process-model-2.png" alt-text="Prozess 2" lightbox="../media/process-model-2.png":::
   Prozess 2  
:::image-end:::  

Ein Browserprozess verfügt über eine Reihe zugeordneter Renderer-Prozesse.  Die Browserprozesse werden nach Bedarf erstellt, um potenziell mehrere Frames in verschiedenen Instanzen von WebView2 zu bedienen.  Die Anzahl der Renderer-Prozesse variiert basierend auf dem Feature "Website Isolierungs Browser" und der Anzahl der unterschiedlichen getrennten Ursprünge, die in zugeordneten Instanzen von WebView2 gerendert werden.  Das Feature "Website Isolierungs Browser" wird im vorherigen Inhalt beschrieben.  

Der `CoreWebView2Environment` stellt einen benutzerdatenordner und einen Browserprozess dar.  Der entspricht `CoreWebView2` nicht direkt einem Satz von Prozessen, da verschiedene Renderer-Prozesse von einem WebView2-Element abhängig von der Standort Isolierung wie zuvor beschrieben verwendet werden.  

Sie können in diesen Browser-und Renderer-Prozessen mit dem `ProcessFailed` Ereignis von `CoreWebView2` .  

Sie können zugeordnete Browser-und Renderer-Prozesse mithilfe der `Close` Methode von sicher Herunterfahren `CoreWebView2Controller` .  

Um das Fenster des Task-Managers des Browsers über das **devtools** -Fenster einer WebView2-Instanz zu öffnen, können Sie `Shift` + `Escape` auf der Titelleiste des devtools-Fensters auswählen oder darauf zeigen, das Kontextmenü öffnen \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie aus `Browser task manager` .  Alle Prozesse, die dem Browserprozess ihrer WebView2 zugeordnet sind, werden einschließlich der zugehörigen Zwecke angezeigt.  

<!-- links -->  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Browser Architektur – Einblick in den modernen Webbrowser (Teil 1)"  
