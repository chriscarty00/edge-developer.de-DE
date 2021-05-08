---
description: Microsoft Edge (Chromium) und Visual Studio Code
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, vs code, visual studio code, debugger, webhint
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230691"
---
# Visual Studio Code – Übersicht  

[Visual Studio Code][VisualStudioCodeDocs] ist ein einfacher, aber leistungsstarker Quellcode-Editor.  [Visual Studio Code][VisualStudioCodeDocs] ist für Windows, Linux und macOS verfügbar.  Es umfasst integrierte Unterstützung für JavaScript, TypeScript und Node.js, daher ist es ein großartiges Tool für Webentwickler, bevor Sie es anpassen.  Wenn Sie es noch nicht verwenden, laden Sie [Visual Studio Code][VisualstudioCode].  

## Erweiterungen  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Um eine der unten hervorgehobenen Erweiterungen zu erwerben, navigieren Sie zu Erweiterungen \(wählen Sie `Ctrl` + `Shift` + `X` unter Windows/Linux oder `Command` + `Shift` + `X` unter macOS\) in Visual Studio Code.  

Suchen Sie im Marketplace nach der spezifischen Erweiterung, und wählen Sie **Installieren aus.**  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Installieren des Debuggers für Microsoft Edge Visual Studio Code Erweiterung" lightbox="./media/vscode-debugger-install.png":::
   Installieren des **Debuggers für Microsoft Edge** Visual Studio Code Erweiterung  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Debugger für Microsoft Edge Visual Studio Code Erweiterung" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         **Debugger für Microsoft Edge** Visual Studio Code Erweiterung  
      :::image-end:::  
      [Debugger für Microsoft Edge](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Tools für Visual Studio Code Visual Studio Code Erweiterung" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension  
      :::image-end:::  
      [Microsoft Edge Tools für Visual Studio Code](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="webhint Visual Studio Code Erweiterung" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **webhint** Visual Studio Code Erweiterung  
      :::image-end:::  
      [Webhint](#webhint)  
   :::column-end:::
:::row-end:::  

## Debugger für Microsoft Edge  

Debugger for [Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debuggen Sie Ihren Front-End-JavaScript-Code Zeile für Zeile, und sehen Sie anweisungen direkt aus `console.log()` [Visual Studio Code][VisualstudioCode].  
      
Mithilfe des Debuggertools können Sie sowohl Microsoft Edge \(EdgeHTML\) als auch Microsoft Edge \(Chromium\) starten oder anfügen.  Eine exemplarische Vorgehensweise zum Debuggen Microsoft Edge von Visual Studio Code und Beispielkonfigurationen finden Sie unter `launch.json` [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].  Wählen Sie die folgende Abbildung aus, um die Erweiterung in Aktion zu sehen.  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Debugger für Edge-Visual Studio Code in Aktion" lightbox="./media/debugger-for-edge.gif":::
   **Debugger für Microsoft Edge** Visual Studio Code erweiterung in Aktion  
:::image-end:::  

## Microsoft Edge Tools für Visual Studio Code

Verwenden Sie [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code das **Element-Tool** des Microsoft Edge in Visual Studio Code.  Verwenden Sie es für die folgenden Aktionen.  

*   Fügen Sie eine Instanz an, oder starten Sie eine Instanz Microsoft Edge.  
*   Zeigt die Laufzeit-HTML-Struktur an.  
*   Aktualisieren Sie das Layout.  
*   Behebung von Formatierungsproblemen.  
    
Weitere Informationen finden Sie unter [Microsoft Edge Tools for Visual Studio Code Visual Studio Code Extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Tools für Visual Studio Code Visual Studio Code erweiterung in Aktion" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Microsoft Edge tools for Visual Studio Code** Visual Studio Code extension in action  
:::image-end:::  

## Webhint  
      
Verwenden [Sie webhint][WebhintMain], ein anpassbares Lintingtool, um die folgenden Funktionen Ihrer Website zu verbessern.  

*   Barrierefreiheit
*   Leistung
*   Browserübergreifende Kompatibilität
*   PWA Kompatibilität
*   Sicherheit

Der Code wird auf Codierungsmethoden und häufige Fehler überprüft. Das webhint-Open-Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS Foundation][OpenjsFoundation].  Das Microsoft Edge-Team arbeitet weiterhin zusammen mit Webentwicklern in der Community am Webhint mit.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Screenshot der Webhint-Visual Studio Code-Erweiterung" lightbox="./media/webhint-extension.png":::
   Screenshot der **Webhint-Visual Studio Code-Erweiterung**  
:::image-end:::  
      
Identifizieren und beheben Sie Probleme auf Ihrer Website, indem Sie die [Webhint-Erweiterung für Visual Studio Code.][VisualstudioMarketplaceWebhint]  Hinweise untersuchen HTML, CSS, JavaScript, TypeScript und vieles mehr.  Hinweise werden als Inline unterstreicht angezeigt und im Bereich **Probleme zusammengefasst.**  
      
Weitere Informationen finden Sie unter [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Debugger Für Microsoft Edge Visual Studio Code Erweiterung | Microsoft Docs"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools für Visual Studio Code Erweiterung | Microsoft Docs"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio Code Extension | Microsoft Docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio Code"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
