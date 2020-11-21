---
description: Microsoft Edge (Chrom) und Visual Studio-Code
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Debugger, webhint
ms.openlocfilehash: 0d13c6eb9411f89e3a681176ade0caf8d59d46d8
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182740"
---
# Visual Studio Code  

[Visual Studio-Code][VisualStudioCodeDocs] ist ein leichter, aber leistungsstarker Quellcode-Editor.  [Visual Studio-Code][VisualStudioCodeDocs] steht für Windows, Linux und macOS zur Verfügung.  Es enthält integrierte Unterstützung für JavaScript, Maschinen-und Node.js, daher ist es ein hervorragendes Tool für Web-Entwickler, bevor Sie es anpassen.  Wenn Sie Sie noch nicht verwenden, laden Sie [Visual Studio-Code][VisualstudioCode]herunter.  

## Extensions  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Wenn Sie eine der unten hervorgehobenen Erweiterungen erwerben möchten, navigieren Sie in Visual Studio-Code zu Erweiterungen \ (Wählen Sie `Ctrl` + `Shift` + `X` unter Windows/Linux oder `Command` + `Shift` + `X` unter macOS \) aus.  

Durchsuchen Sie den Marktplatz nach der jeweiligen Erweiterung, und wählen Sie **Installieren**aus.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Installieren des Debuggers für Microsoft Edge Visual Studio-Code Erweiterung" lightbox="./media/vscode-debugger-install.png":::
   Installieren des **Debuggers für Microsoft Edge** Visual Studio-Code Erweiterung  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Debugger für Microsoft Edge Visual Studio-Code Erweiterung" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         **Debugger für Microsoft Edge** Visual Studio-Code Erweiterung  
      :::image-end:::  
      [Debugger für Microsoft Edge](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Tools für Visual Studio Code Visual Studio-Code Erweiterung" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Microsoft Edge Tools für Visual Studio-Code** Visual Studio-Code Erweiterung  
      :::image-end:::  
      [Microsoft Edge Tools für Visual Studio-Code](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="webhint Visual Studio-Code Erweiterung" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **webhint** Visual Studio-Code Erweiterung  
      :::image-end:::  
      [Webhint](#webhint)  
   :::column-end:::
:::row-end:::  

## Debugger für Microsoft Edge  

Mit der [Debugger für Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio-Code Erweiterung können Sie den Front-End-JavaScript-Code Zeile für Zeile Debuggen und `console.log()` Anweisungen direkt aus [Visual Studio-Code][VisualstudioCode]anzeigen.  
      
Mit dem Debugger-Tool können Sie sowohl Microsoft Edge \ (EdgeHTML \) als auch Microsoft Edge \ (Chrom \) starten oder anfügen.  Eine exemplarische Vorgehensweise zum Debuggen von Microsoft Edge in Visual Studio-Code und Beispiel `launch.json` Konfigurationen finden Sie unter [Debugger für Microsoft Edge Visual Studio-Code Erweiterung][VisualStudioCodeDebuggerEdge].  Wählen Sie die folgende Abbildung aus, um die Erweiterung in Aktion anzuzeigen.  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Debugger für Edge Visual Studio-Code Erweiterung in Aktion" lightbox="./media/debugger-for-edge.gif":::
   **Debugger für Microsoft Edge** Visual Studio-Code Erweiterung in Aktion  
:::image-end:::  

## Microsoft Edge Tools für Visual Studio-Code

Verwenden Sie die Code Erweiterung [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio, und verwenden Sie das Tool **Elemente** des Microsoft Edge-Browsers in Visual Studio-Code.  Verwenden Sie es für die folgenden Aktionen.  

*   Anfügen an eine Instanz oder Starten einer Instanz von Microsoft Edge  
*   Anzeigen der HTML-Laufzeitstruktur  
*   Aktualisieren Sie das Layout.  
*   Beheben von Formatierungsproblemen  
    
Weitere Informationen finden Sie unter [Microsoft Edge Tools for Visual Studio Code Visual Studio Code Extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Tools for Visual Studio Code Visual Studio-Code Erweiterung in Aktion" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Microsoft Edge Tools für Visual Studio-Code** Visual Studio-Code Erweiterung in Aktion  
:::image-end:::  

## Webhint  
      
Verwenden Sie [webhint][WebhintMain], ein anpassbares linting-Tool, um die folgende Funktionalität Ihrer Website zu verbessern.  

*   Bedienungshilfen
*   Leistung
*   Browserübergreifende Kompatibilität
*   PWA-Kompatibilität
*   Sicherheit

Sie überprüft Ihren Code auf Codierungsmethoden und häufige Fehler. Das webhint Open-Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS-Foundation][OpenjsFoundation].  Das Microsoft Edge-Team trägt weiterhin zu webhint neben Webentwicklern in der Community bei.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Screenshot der webhint Visual Studio-Code Erweiterung" lightbox="./media/webhint-extension.png":::
   Screenshot der **webhint** Visual Studio-Code Erweiterung  
:::image-end:::  
      
Identifizieren und beheben Sie Probleme in Ihrer Website, indem Sie die [webhint-Erweiterung für Visual Studio-Code][VisualstudioMarketplaceWebhint]hinzufügen.  Hinweise untersuchen HTML, CSS, JavaScript, Manuskript und vieles mehr.  Hinweise werden als Inline Unterstriche angezeigt und im **Problem** Bereich zusammengefasst.  
      
Weitere Informationen finden Sie unter [Verwenden von webhint in Visual Studio-Code][VisualStudioCodeWebhint].  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Debugger für Microsoft Edge Visual Studio-Code Erweiterung | Microsoft docs"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge-devtools für Visual Studio-Code Erweiterung | Microsoft docs"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio-Code Erweiterung | Microsoft docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio-Code"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio-Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
