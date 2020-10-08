---
description: Microsoft Edge (Chrom) und Visual Studio-Code
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Debugger, webhint
ms.openlocfilehash: e178612d9db8ce3223bb5158c4557675d3314e15
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695881"
---
# Visual Studio Code  

[Visual Studio-Code][VisualStudioCodeDocs] ist ein leichter, aber leistungsstarker Quellcode-Editor, der auf dem Desktop ausgeführt wird und für Windows, macOS und Linux verfügbar ist.  Es bietet integrierte Unterstützung für JavaScript, Maschinen-und Node.js und ist daher ein tolles Tool für Web-Entwickler direkt aus der Box!  Wenn Sie Sie noch nicht verwenden, laden Sie [Visual Studio-Code][VisualstudioCode]herunter.  

## Extensions  

<!--Todo: We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Wenn Sie eine der unten hervorgehobenen Erweiterungen erwerben möchten, navigieren Sie in vs-Code zu Erweiterungen \ ( `Ctrl` + `Shift` + `X` unter Windows oder `Command` + `Shift` + `X` unter macOS).  

Durchsuchen Sie den Marktplatz nach der jeweiligen Erweiterung, und wählen Sie **Installieren**aus.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Installieren des Debuggers für Microsoft Edge vs Code Extension":::
   Installieren des Debuggers für Microsoft Edge vs Code Extension  
:::image-end:::  

:::row:::
   :::column span="1":::
      ### Debugger für Microsoft Edge  

      Debuggen Sie mit dem [Debugger für Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] vs Code Extension ihren Front-End-JavaScript-Code Zeile für Zeile, und lesen Sie `console.log()` Anweisungen direkt aus [Visual Studio-Code][VisualstudioCode]!  
      
      Mit dem Debugger-Tool können Sie sowohl Microsoft Edge \ (EdgeHTML \) als auch Microsoft Edge \ (Chrom \) starten oder anfügen.  Eine exemplarische Vorgehensweise zum Debuggen von Microsoft Edge aus vs-Code und Beispiel `launch.json` Konfigurationen finden Sie unter [Debugger für Microsoft Edge vs Code Extension][VscodeDebuggerEdge].  Wählen Sie die folgende Abbildung aus, um die Erweiterung in Aktion anzuzeigen.  

      :::image type="content" source="./media/debugger-for-edge.png" alt-text="Installieren des Debuggers für Microsoft Edge vs Code Extension" lightbox="./media/debugger-for-edge.gif":::  
   :::column-end:::
   :::column span="1":::
      ### Elemente für Microsoft Edge  
      
      Mit den [Elementen für Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] vs Code Extension verwenden Sie das Tool Elemente des Microsoft Edge-Browsers in Visual Studio-Code.  Durch Starten oder Anfügen wird das elementtool mit einer Instanz von Microsoft Edge verbunden, zeigt die HTML-Laufzeitstruktur an und ermöglicht Ihnen, das Layout zu ändern oder Formatierungsprobleme zu beheben.  
      
      Weitere Informationen finden Sie unter [Elemente für Microsoft Edge vs Code Extension][VscodeElementsEdge].  Wählen Sie die folgende Abbildung aus, um die Erweiterung in Aktion anzuzeigen.  
      
      :::image type="content" source="./media/elements-for-edge.png" alt-text="Installieren des Debuggers für Microsoft Edge vs Code Extension" lightbox="./media/elements-for-edge.gif":::  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      ### Webhint
      
      Verwenden Sie [webhint][WebhintMain], ein anpassbares linting-Tool, um die Barrierefreiheit, die Leistung, die browserübergreifende Kompatibilität, die PWA-Kompatibilität und die Sicherheit Ihrer Website zu verbessern.  Sie überprüft Ihren Code auf bewährte Methoden und häufige Fehler. Das webhint Open-Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS-Foundation][OpenjsFoundation].  Das Microsoft Edge-Team trägt weiterhin zu webhint neben Webentwicklern in der Community bei.  <!--Select the following image to see the extension in action.  -->  
      
      :::image type="content" source="./media/webhint-extension.png" alt-text="Installieren des Debuggers für Microsoft Edge vs Code Extension" lightbox="./media/webhint-extension.png":::  
      
      Identifizieren und beheben Sie Probleme in HTML, CSS, JavaScript, Manuskript und mehr, indem Sie die [webhint-Erweiterung für vs-Code][VisualstudioMarketplaceWebhint]hinzufügen.  Hinweise werden als Inline Unterstriche angezeigt und im **Problem** Bereich zusammengefasst.  
      
      Weitere Informationen finden Sie unter [so wird es gemacht: Verwenden von webhint in Visual Studio-Code][VscodeWebhint].  
   :::column-end:::
   :::column span="1":::
      <!--Empty to retain grid  -->  
   :::column-end:::
:::row-end:::

<!-- image links -->  

<!--links -->  

[VscodeDebuggerEdge]: ./debugger-for-edge.md "Debugger für Microsoft Edge vs Code Extension | Microsoft docs"  
[VscodeElementsEdge]: ./elements-for-edge.md "Elemente für Microsoft Edge vs Code Extension | Microsoft docs"  
[VscodeWebhint]: ./webhint.md "Webhint vs-Code Erweiterung | Microsoft docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio-Code"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elemente für Microsoft Edge (Chrom) | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
