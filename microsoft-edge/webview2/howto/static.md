---
description: Erfahren Sie, wie Sie die WebView2-Ladebibliothek statisch verknüpfen.
title: So verknüpfen Sie die WebView2-Ladebibliothek statisch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 397c226eb958d1e656fb0ecb6dd8f1e2fe300746
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536476"
---
# <a name="statically-link-the-webview2-loader-library"></a>Statische Verknüpfung der WebView2-Ladebibliothek  

Möglicherweise möchten Sie Ihre Anwendung mit einer einzelnen ausführbaren Datei anstelle eines Pakets mit vielen Dateien verteilen. Um eine einzelne ausführbare Datei zu erstellen oder die Größe Ihres Pakets zu reduzieren, sollten Sie die WebView2Loader-Dateien statisch verknüpfen. Das WebView2 SDK enthält eine Headerdatei `WebView2Loader.dll` und die `IDL` Datei. `WebView2Loader.dll` ist eine kleine Komponente, die Apps dabei hilft, die WebView2-Runtime oder nicht stabile Kanäle der Microsoft Edge auf dem Gerät zu finden.  

Führen Sie die folgenden Schritte für Apps aus, die keines versenden `WebView2Loader.dll` möchten.  

1.  Öffnen Sie die Projektdatei für Ihre App in einem Texteditor, z. `.vcxproj` B. Visual Studio Code.  
    
    > [!NOTE]
    > Die `.vcproj` Projektdatei kann eine ausgeblendete Datei sein, d. h. sie wird nicht in der Visual Studio.  Verwenden Sie die Befehlszeile, um nach ausgeblendeten Dateien zu suchen.  
    
1.  Suchen Sie den Abschnitt im Code, in den Sie die WebView2-NuGet Packzieldateien eingeben.  Die Position im Code wird in der folgenden Abbildung hervorgehoben.  

    :::image type="complex" source="./media/inserthere.png" alt-text="Project Codeausschnitt für Dateien" lightbox="./media/inserthere.png":::
       Project Codeausschnitt für Dateien   
    :::image-end:::  
  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn dort ein, wo `Microsoft.Web.WebView2.targets` der enthalten ist.  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Eingefügter Codeausschnitt" lightbox="./media/staticlib.png":::
       Eingefügter Codeausschnitt  
    :::image-end:::  
    
1.  Bearbeiten Sie die zusätzlichen Abhängigkeiten der Buildkonfiguration für Ihre App.  Suchen Sie zunächst alle `<AdditionalDependencies>` Tags. Fügen Sie jeweils als zusätzliche Abhängigkeit zu `version.lib` jeder anderen Buildkonfiguration in der Datei `.vcxproj` hinzu.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Hinzufügen von version.lib zu ItemDefinitionGroups" lightbox="./media/versionlib.png":::
       Hinzufügen `version.lib` zu `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > Das WebView2-Team möchte das Hinzufügen der zusätzlichen Abhängigkeit in zukünftigen Versionen automatisieren.  
    
1. Kompilieren und Ausführen Der App.

### <a name="getting-in-touch-with-the-webview2-team"></a>Kontakt mit dem WebView2-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### <a name="see-also"></a>Weitere Informationen  

*   Navigieren Sie zu [WebView2 Getting Started Guides,][Webview2MainGettingStarted]um mit WebView2 zu beginnen.  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.
*   Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2MainNextSteps].

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Was ist neu? - JavaScript-Debugger für Visual Studio Code - microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chromium) WebView-Anwendungen - Visual Studio Code - Debugger für Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
