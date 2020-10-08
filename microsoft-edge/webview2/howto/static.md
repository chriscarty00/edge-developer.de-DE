---
description: Hier erfahren Sie, wie Sie die WebView2-Loader-Bibliothek statisch verknüpfen.
title: So verknüpfen Sie die WebView2-Ladeprogramm Bibliothek statisch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b7e0ec70cb00f318d4eb67254f37fcec79a5fcf6
ms.sourcegitcommit: 903524ab85321ade278facd741d6487e8cabe33f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100307"
---
# So verknüpfen Sie die WebView2-Ladeprogramm Bibliothek statisch  

## Kontext  

Was ist der WebView2Loader.dll?  

*   Das WebView2-SDK enthält eine Headerdatei `WebView2Loader.dll.` und die `IDL` Datei. `WebView2Loader.dll` ist eine kleine Komponente, die apps bei der Suche nach der WebView2-Runtime (oder nicht stabilen Microsoft Edge-Kanälen) auf dem Gerät unterstützt.  

Führen Sie die folgenden Schritte aus, wenn apps, die über eine einzige Laufzeit verfügen und keine senden möchten `WebView2Loader.dll` , die folgenden Schritte **Ausführen** .  

## Verfahren  

1.  Öffnen `.vcxproj` Sie die Projektdatei für Ihre APP in einem Text-Editor wie Visual Studio-Code.  
    
    > [!NOTE]
    > Die `.vcproj` Projektdatei kann eine versteckte Datei sein, was bedeutet, dass Sie in Visual Studio nicht angezeigt wird.  Verwenden Sie die Befehlszeile, um eine versteckte Datei zu suchen.  
    
1.  Suchen Sie den Abschnitt im Code, in den Sie die WebView2 NuGet-Paket Zieldateien einbeziehen.  Die Position im Code ist in der folgenden Abbildung hervorgehoben.  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/inserthere.png"::: 
       Codeausschnitt für Projektdateien  
    :::image-end:::  
    
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn überall im `Microsoft.Web.WebView2.targets` Lieferumfang ein.  

    > [!NOTE]
    > Fügen Sie den Codebeispiels Weise nach dem folgenden Codeblock ein.  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/staticlib.png"::: 
       Eingefügter Codeausschnitt  
    :::image-end:::  
    
1.  Bearbeiten Sie die zusätzlichen Abhängigkeiten der Buildkonfiguration für Ihre APP.  Suchen Sie zunächst alle `<AdditionalDependencies>` Kategorien.  
1.  Fügen Sie `version.lib` jeder anderen Buildkonfiguration in der `.vcxproj` Datei für Ihre APP eine zusätzliche Abhängigkeit hinzu.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/versionlib.png"::: 
       Hinzufügen `version.lib` zu `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > Das WebView2-Team zielt darauf ab, den zusätzlichen Abhängigkeits Schritt in zukünftigen Versionen zu automatisieren.  
    
Kompilieren und Bereitstellen Ihrer APP  Erfolgreich.  

## Weitere Informationen  

*   Um mit der Verwendung von WebView2 zu beginnen, navigieren Sie zu [WebView2 Anleitungen für erste Schritte][Webview2MainGettingStarted].  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samples] auf GitHub.
*   Ausführlichere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].
*   Wenn Sie weitere Informationen zu WebView2 möchten, navigieren Sie zu [WebView2-Ressourcen][Webview2MainNextSteps].

## Kontakt mit dem WebView2-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions Klasse | Microsoft docs"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Was ist neu? -JavaScript-Debugger für Visual Studio-Code – Microsoft/vscode-js – Debuggen | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen – Visual Studio-Code – Debugger für Microsoft Edge – Microsoft/vscode-Edge-debug2 | GitHub"  
