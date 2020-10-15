---
description: Informationen zur Verwendung von JavaScript in komplexen Szenarien in WebView2-apps
title: Verwenden von JavaScript in WebView2-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: f6e59acb0c4bf8ad5357aba87e0359d3b103ed63
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119066"
---
# Verwenden von JavaScript in WebView für erweiterte Szenarien  

Durch die Verwendung von JavaScript in WebView2-Steuerelementen können Sie systemeigene apps an Ihre Anforderungen anpassen.  In diesem Artikel wird erläutert, wie Sie JavaScript in WebView2 verwenden, und es wird erläutert, wie Sie mithilfe der erweiterten WebView2-Features und-Funktionen entwickeln können.  

## Vorbemerkungen  

In diesem Artikel wird davon ausgegangen, dass Sie bereits über ein funktionierendes Projekt verfügen.  Wenn Sie nicht über ein Projekt verfügen und folgen möchten, navigieren Sie zum [WebView2-Leitfaden für erste Schritte][Webview2GettingstartedWpf].  

## Grundlegende WebView2-Funktionen  

Verwenden Sie die folgenden Funktionen, um mit der Einbettung von JavaScript in Ihre WebView-APP zu beginnen.  

| API  | Beschreibung  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpf09515MicrosoftWebExecutescriptasync] | Führen Sie JavaScript in einem WebView-Steuerelement aus. Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum Lernprogramm "erste Schritte". |
| [OnDocumentCreatedAsync][Webview2ReferenceWin3209538Icorewebview2Addscripttoexecuteondocumentcreated] | Wird ausgeführt, wenn das Dokumentobjektmodell \ (DOM \) erstellt wird. |
      
## Szenario: Ausführen einer dedizierten Skriptdatei  

Greifen Sie in diesem Abschnitt auf eine dedizierte JavaScript-Datei über Ihr WebView2-Steuerelement zu.  

> [!NOTE]
> Obwohl das Schreiben von JavaScript Inline für schnelle JavaScript-Befehle effizient sein kann, verlieren Sie JavaScript-Farbdesigns und die Zeilenformatierung, wodurch große Codeabschnitte in Visual Studio schwierig zu schreiben sind.  

Um das Problem zu beheben, erstellen Sie eine separate JavaScript-Datei mit Ihrem Code, und übergeben Sie dann mithilfe der Parameter einen Verweis auf diese Datei `ExecuteScriptAsync` .  

1.  Erstellen Sie eine `.js` Datei in Ihrem Projekt, und fügen Sie den JavaScript-Code hinzu, den Sie ausführen möchten.  Erstellen Sie beispielsweise eine Datei mit dem Namen `script.js` .  
1.  Konvertieren Sie die JavaScript-Datei in eine Zeichenfolge, die übergeben wird `ExecuteScriptAsync` .  
    1.  Wenn Sie Ihre JavaScript-Datei in eine Zeichenfolge konvertieren möchten, kopieren Sie den folgenden Codeausschnitt.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  Fügen Sie den Code in ein `MainWindow.xaml.cs` .  
1.  Übergeben Sie die Textvariable mit `ExecuteScriptAsync` .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## Szenario: Entfernen von Drag & Drop-Funktionen  

Verwenden Sie in diesem Abschnitt JavaScript, um die Drag & Drop-Funktion aus Ihrem WebView2-Steuerelement zu entfernen.  

Erkunden Sie zunächst die aktuelle Drag & Drop-Funktion.  

1.  Erstellen `.txt` Sie eine Datei, um Sie zu ziehen und abzulegen.  Erstellen Sie beispielsweise eine Datei mit dem Namen, `contoso.txt` und fügen Sie Text hinzu.  
1.  Führen Sie das Projekt aus.  
1.  Ziehen Sie die `contoso.txt` Datei auf das WebView-Steuerelement, und legen Sie Sie ab.  Es wird ein neues Fenster geöffnet, das das Ergebnis des Codes in Ihrem Beispielprojekt ist.  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Ergebnis beim Ziehen und Ablegen von contoso.txt" lightbox="./media/dragtext.png":::
       Ergebnis beim Ziehen und Ablegen von contoso.txt  
    :::image-end:::  

Fügen Sie jetzt Code hinzu, um die Drag & Drop-Funktion aus dem WebView2-Steuerelement zu entfernen.  

1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in ein `MainWindow.xaml.cs` .   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  Führen Sie das Projekt aus.  
1.  Ziehen und ablegen versuchen `contoso.txt` .  Vergewissern Sie sich, dass Sie nicht in der Lage sind, Drag & Drop zu ziehen.  

## Szenario: Entfernen des Kontextmenüs  

Entfernen Sie in diesem Abschnitt das Standardkontextmenü aus Ihrem WebView2-Steuerelement.  

Erkunden Sie zunächst die aktuelle Kontextmenü Funktionalität.  

1.  Führen Sie das Projekt aus.  
1.  Zeigen Sie auf das WebView2-Steuerelement, und öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \).  Das Kontextmenü zeigt die Standardauswahl an.  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Ergebnis beim Ziehen und Ablegen von contoso.txt" lightbox="./media/contextmenu.png":::
       Das Kontextmenü mit den Standardoptionen  
    :::image-end:::  
    
Fügen Sie nun Code hinzu, um die Kontextmenü Funktionalität des WebView2-Steuerelements zu entfernen.  

1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in ein `MainWindow.xaml.cs` .    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  Führen Sie den Code erneut aus.  Vergewissern Sie sich, dass Sie nicht in der Lage sind, ein Kontextmenü zu öffnen \ (Klicken Sie mit der rechten Maustaste auf \).  
   
## Weitere Informationen  

*   Weitere Informationen zu den ersten Schritten mit WebView2 finden Sie unter [Erste Schritte mit WebView2][Webview2MainGettingStarted].  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samples] Repo auf GitHub.  
*   Detaillierte Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].  
*   Wenn Sie weitere Informationen zu WebView2 möchten, navigieren Sie zu [WebView2-Ressourcen][Webview2MainNextSteps].  

## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  


[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft docs"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2ReferenceWin3209538Icorewebview2Addscripttoexecuteondocumentcreated]: ../reference/win32/0-9-538/icorewebview2.md#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated-0.9.579-Interface ICoreWebView2 | Microsoft docs"  
[Webview2ReferenceWpf09515MicrosoftWebExecutescriptasync]: ../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync "ExecuteScriptAsync-Microsoft. Web. WebView2. WPF. WebView2 Klasse | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  
