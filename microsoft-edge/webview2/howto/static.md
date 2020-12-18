---
description: Hier erfahren Sie, wie Sie die WebView2-Loader-Bibliothek statisch verknüpfen.
title: So verknüpfen Sie die WebView2-Ladeprogramm Bibliothek statisch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 397c226eb958d1e656fb0ecb6dd8f1e2fe300746
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230929"
---
# Statische Verknüpfung der WebView2-Loader-Bibliothek  

Möglicherweise möchten Sie Ihre Anwendung mit einer einzelnen ausführbaren Datei anstelle eines Pakets von vielen Dateien verteilen. Wenn Sie eine einzelne ausführbare Datei erstellen oder die Größe Ihres Pakets verkleinern möchten, sollten Sie die WebView2Loader-Dateien statisch verknüpfen. Das WebView2-SDK enthält eine Headerdatei `WebView2Loader.dll` und die `IDL` Datei. `WebView2Loader.dll` ist eine kleine Komponente, die apps dabei hilft, die WebView2-Runtime oder nicht-stable-Kanäle von Microsoft Edge auf dem Gerät zu finden.  

Führen Sie die folgenden Schritte aus, wenn Sie keine apps senden möchten `WebView2Loader.dll` .  

1.  Öffnen `.vcxproj` Sie die Projektdatei für Ihre APP in einem Text-Editor wie Visual Studio-Code.  
    
    > [!NOTE]
    > Die `.vcproj` Projektdatei kann eine versteckte Datei sein, was bedeutet, dass Sie in Visual Studio nicht angezeigt wird.  Verwenden Sie die Befehlszeile, um ausgeblendete Dateien zu suchen.  
    
1.  Suchen Sie den Abschnitt im Code, in den Sie die WebView2 NuGet-Paket Zieldateien einbeziehen.  Die Position im Code ist in der folgenden Abbildung hervorgehoben.  

    :::image type="complex" source="./media/inserthere.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/inserthere.png":::
       Codeausschnitt für Projektdateien   
    :::image-end:::  
  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn dort ein, wo er `Microsoft.Web.WebView2.targets` enthalten ist.  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Eingefügter Codeausschnitt" lightbox="./media/staticlib.png":::
       Eingefügter Codeausschnitt  
    :::image-end:::  
    
1.  Bearbeiten Sie die zusätzlichen Abhängigkeiten der Buildkonfiguration für Ihre APP.  Suchen Sie zunächst alle `<AdditionalDependencies>` Kategorien. Fügen Sie für jede `version.lib` eine weitere Abhängigkeit zu jeder anderen Buildkonfiguration in der Datei hinzu `.vcxproj` .  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Hinzufügen von Version. lib zu ItemDefinitionGroups verfügen" lightbox="./media/versionlib.png":::
       Hinzufügen `version.lib` zu `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > Das WebView2-Team zielt darauf ab, das Hinzufügen der zusätzlichen Abhängigkeit in zukünftigen Versionen zu automatisieren.  
    
1. Kompilieren Sie Ihre APP, und führen Sie Sie aus.

### Kontakt mit dem WebView2-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### Weitere Informationen  

*   Um mit der Verwendung von WebView2 zu beginnen, navigieren Sie zu [WebView2 Anleitungen für erste Schritte][Webview2MainGettingStarted].  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samples] auf GitHub.
*   Ausführlichere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].
*   Wenn Sie weitere Informationen zu WebView2 möchten, navigieren Sie zu [WebView2-Ressourcen][Webview2MainNextSteps].

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Was ist neu? -JavaScript-Debugger für Visual Studio-Code – Microsoft/vscode-js – Debuggen | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen – Visual Studio-Code – Debugger für Microsoft Edge – Microsoft/vscode-Edge-debug2 | GitHub"  
