---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Debuggen von WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 386bc237257be0ade8c48bc1c737b0151a882719
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659700"
---
# Debuggen bei der Entwicklung mit WebView2-Steuerelementen  

Das Ziel des Microsoft Edge WebView2-Steuerelements ist die Kombination der besten Features der Web-und nativen Anwendungsentwicklung sowie der Entwicklertools.  In diesem Artikel werden die verschiedenen Tools erläutert, die bei der Entwicklung mit WebView2-Steuerelementen zu verwenden sind.  

## Microsoft Edge DevTools  

Verwenden Sie die [Microsoft Edge (Chrom)-Entwickler Tools](/microsoft-edge/devtools-guide-chromium) zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise wie bei Verwendung von Microsoft Edge.  Um das devtools zu öffnen, setzen Sie den Fokus auf das WebView-Fenster, und verwenden Sie dann eine der folgenden Optionen.  
*   Wählen Sie aus `F12` .  
*   Wählen Sie aus `Ctrl` + `Shift` + `I` .  
*   Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) > auswählen `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!NOTE]
> Wenn Sie die Anwendung in Visual Studio debuggen, wobei der systemeigene Debugger angefügt ist, `F12` kann die Auswahl den systemeigenen Debugger anstelle der Entwickler Tools auslösen.  Verwenden Sie `Ctrl` + `Shift` + `I` das Kontextmenü, oder klicken Sie mit der rechten Maustaste auf \), um diese Situation zu vermeiden.  

## Visual Studio  

Verwenden Sie den Skriptdebugger in Visual Studio 2019, Version 16,4 Preview 2 oder höher, um Ihr Skript in Visual Studio zu debuggen.  Überprüfen Sie, ob die Komponente **JavaScript-Diagnose** in der **Desktop Entwicklung mit C++** -Arbeitsauslastung installiert ist.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Visual Studio-JavaScript-Diagnose":::
   Visual Studio-JavaScript-Diagnose  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Zum Aktivieren des WebView2-Skript Debuggens öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \) in Ihrem Projekt, > **Eigenschaften**auswählen.  Wählen Sie unter **Konfigurationseigenschaften**die Option **Debuggen**aus.  Wählen Sie in der Eigenschaft **Debuggertyp** in der Liste der Optionen **JavaScript (WebView2)** aus. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Visual Studio-JavaScript-Debugger":::
   Visual Studio-JavaScript-Debugger  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## Visual Studio Code  

Sie können Visual Studio-Code verwenden, um Skripts zu debuggen, die in WebView2-Steuerelementen ausgeführt werden.  Weitere Informationen finden Sie unter [Microsoft Edge (Chrom) WebView-Anwendungen](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).  

<!--todo:  add See also heading  -->  

## Kontakt mit dem Microsoft Edge WebView-Team  

Helfen Sie beim Aufbau einer reicheren WebView2-Erfahrung, indem Sie Ihr Feedback freigeben.  Besuchen Sie das [Feedback-Repo](https://aka.ms/webviewfeedback) , um Funktionsanforderungen oder Fehlerberichte einzureichen.  
