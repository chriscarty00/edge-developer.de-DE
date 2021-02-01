---
description: Erste Schritte mit WebView2 für WinForms-Apps
title: Erste Schritte mit WebView2 für WinForms-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, Webview2, WebView, Webview, winforms apps, winforms, edge, CoreWebView2, browser control, edge html, getting started, .NET, windows forms
ms.openlocfilehash: 45a3b59733a57975e373df2e21258198645be2d4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306166"
---
# Erste Schritte mit WebView2 in Windows Forms

In diesem Artikel beginnen Sie mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Wichtigsten Features von [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]  Weitere Informationen zu einzelnen APIs finden Sie in der [API-Referenz.][DotnetApiMicrosoftWebWebview2Winforms]  

## Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.  

*   [WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen \(derzeit Windows 10, Windows 8.1 und Windows 7\ installiert ist).  
    
    > [!NOTE]
    > Das WebView-Team empfiehlt die Verwendung des Canarykanals, und die mindestens erforderliche Version ist 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 oder höher.  
    
> [!NOTE]
> WebView2 unterstützt derzeit keine .NET 5- und .NET Core-Designer.

## Schritt 1: Erstellen einer App mit einem Fenster

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  

1.  Wählen Visual Studio **"Windows Forms .NET Framework App**  >  **Next" aus.**
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Neues Projekt" lightbox="./media/winforms-newproject.png":::
       Neues Projekt  
    :::image-end:::
    
1.  Geben Sie Werte für **den Projektnamen und** den **Speicherort ein.**  Wählen **Sie .NET Framework 4.6.2** oder höher aus.  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Projekt starten" lightbox="./media/winforms-startproj.png":::
       Projekt starten  
    :::image-end:::
    
1.  Um Ihr Projekt zu erstellen, wählen Sie **"Erstellen"** aus.
    
## Schritt 2: Installieren des WebView2 SDK

Verwenden Sie NuGet, um dem Projekt das WebView2 SDK hinzuzufügen.  

1.  Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **NuGet-Pakete verwalten... aus.**  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Verwalten von NuGet-Paketen":::
       Verwalten von NuGet-Paketen
    :::image-end:::
    
1.  Geben Sie in der Suchleiste > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2 aus.**  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       NuGet  
    :::image-end:::
    
    Beginnen Sie mit der Entwicklung von Apps mithilfe der WebView2-API.  Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Das ausgeführte Projekt zeigt ein leeres Fenster an.  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Leere App" lightbox="./media/winforms-emptyapp.png":::
       Leere App  
    :::image-end:::
    
## Schritt 3: Erstellen einer einzelnen WebView  

Fügen Sie Ihrer App eine WebView hinzu.  

1.  Öffnen Sie **den Windows Forms Designer.**  
1.  Suchen Sie in der **Toolbox**nach **WebView2.**  
    
    > [!NOTE]
    > Wenn Sie Visual Studio 2017 verwenden, wird **WebView2** standardmäßig nicht in der **Toolbox angezeigt.**  Um das Verhalten zu aktivieren, **wählen**Sie tools Options General > die Einstellung "Toolbox automatisch  >  ****  >  **** auffüllen" auf **** `True` .  
    
    Drag and drop the **WebView2** control into the Windows Forms App.
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Toolbox mit WebView2":::
       Toolbox mit WebView2
    :::image-end:::  

1.  Legen Sie die `(Name)`-Eigenschaft auf `webView` fest.
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Eigenschaften des WebView2-Steuerelements":::
       Eigenschaften des WebView2-Steuerelements
    :::image-end:::

1.  Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.  Legen Sie die `Source`-Eigenschaft auf `https://www.microsoft.com` fest.  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Die Eigenschaft Source des WebView2-Steuerelements":::
       Die **Eigenschaft "Source"** des WebView2-Steuerelements
    :::image-end:::  

Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Stellen Sie sicher, dass Ihr WebView2-Steuerelement angezeigt [https://www.microsoft.com][|::ref1::|Main] wird.

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   hello webview  
:::image-end:::  

> [!NOTE]
> Wenn Sie an einem Monitor mit hohem DPI arbeiten, müssen Sie Ihre [Windows Forms-App][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]möglicherweise für die Unterstützung hoher DPI konfigurieren.  

## Schritt 4: Behandeln von Ereignissen für die Fenstergröße

Fügen Sie ein paar weitere Steuerelemente zu Ihren Windows Forms aus der Toolbox hinzu, und behandeln Sie die Ereignisse für die Fenstergröße entsprechend.

1.  Öffnen Sie **im Windows Forms Designer**die **Toolbox**
1.  Ziehen Sie ein **TextBox-Objekt per** Drag and Drop in die Windows Forms App.  Geben Sie **auf der Registerkarte "Eigenschaften"** den Namen **"TextBox" ein.** `addressBar`
1.  Drag and drop a **Button** into the Windows Forms App.  Ändern Sie den Text in der **Schaltfläche,** `Go!` und benennen Sie die **Schaltfläche** auf der `goButton` Registerkarte **"Eigenschaften".**

    Die App sollte wie das folgende Bild im Designer aussehen.
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="Designer" lightbox="./media/winforms-designer.png":::
       Designer  
    :::image-end:::  

1.  Definieren Sie in der Datei, dass die Steuerelemente bei der Größenänderung des `Form1.cs` `Form_Resize` App-Fensters weiterhin verwendet werden.

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```

Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Stellen Sie sicher, dass die App ähnlich wie im folgenden Screenshot angezeigt wird.

:::image type="complex" source="./media/winforms-app.png" alt-text="App" lightbox="./media/winforms-app.png":::
   App  
:::image-end:::

## Schritt 5: Navigation

Fügen Sie die Möglichkeit hinzu, Benutzern das Ändern der URL zu ermöglichen, die das WebView2-Steuerelement anzeigt, indem Sie der App eine Adressleiste hinzufügen.

1.  Fügen Sie in der Datei den folgenden Codeausschnitt oben ein, um den `Form1.cs` `CoreWebView2` Namespace hinzuzufügen.  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  Doppelklicken Sie **im Windows Forms Designer**auf die Schaltfläche, um die Methode in der Datei zu `Go!` `goButton_Click` `Form1.cs` erstellen.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in die Funktion ein.  Nun navigiert die Funktion in der WebAnsicht zu `goButton_Click` der URL, die in der Adressleiste eingegeben wurde.

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **"Los" aus.**  Geben Sie z. `https://www.bing.com` B. .  Stellen Sie sicher, dass das WebView2-Steuerelement zur URL navigiert.  

> [!NOTE]
> Stellen Sie sicher, dass in der Adressleiste eine vollständige URL eingegeben ist.  Ein `ArgumentException` wird ausgelöst, wenn die URL nicht mit oder `http://` `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   bing.com  
:::image-end:::

## Schritt 6: Navigationsereignisse  

Während der Webseitennavigation löst das WebView2-Steuerelement Ereignisse aus.  Die App, die WebView2-Steuerelemente hostet, lauscht auf die folgenden Ereignisse.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Navigieren Sie zu [Navigationsereignissen, um weitere Informationen zu erhalten.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   Navigationsereignisse
:::image-end:::

Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und sind möglicherweise von der Navigation zu einer Fehlerwebseite abhängig.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.  

Um die Verwendung dieser Ereignisse zu veranschaulichen, registrieren Sie zunächst einen Handler, der alle Anforderungen abbricht, die HTTPS `NavigationStarting` nicht verwenden.  

Aktualisieren Sie in der Datei den Konstruktor so, dass er mit dem `Form1.cs` folgenden Codeausschnitt übereinstimmen kann, und fügen Sie die Funktion `EnsureHttps` hinzu.  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```

Im Konstruktor wird EnsureHttps als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.  

Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Stellen Sie sicher, dass die WebView beim Navigieren zu einer HTTP-Website unverändert bleibt.  Die WebView navigiert jedoch zu HTTPS-Websites.

## Schritt 7: Skripterstellung  

Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.  You may task WebView to run arbitrary JavaScript or add initialization scripts.  Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.  Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.  

*   Führen Sie es nach der Erstellung des globalen Objekts aus.  
*   Führen Sie es aus, bevor ein anderes Im HTML-Dokument enthaltenes Skript ausgeführt wird.  

Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.  Ändern Sie die Funktion, um ein Skript in den Webinhalt zu injizieren, `EnsureHttps` der die [ExecuteScriptAsync-Methode][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] verwendet.  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Stellen Sie sicher, dass die App eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die https nicht verwendet.  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   https  
:::image-end:::

## Schritt 8: Kommunikation zwischen Host- und Webinhalt  

Host- und Webinhalte können für `postMessage` die Kommunikation miteinander wie folgt verwendet werden:  

*   Webinhalte in einem WebView2-Steuerelement können zum Veröffentlichen `window.chrome.webview.postMessage` einer Nachricht an den Host verwendet werden.  Der Host verarbeitet die Nachricht mit allen auf dem `WebMessageReceived` Host registrierten Nachrichten.  
*   Hostet Nachrichten an Webinhalte in einem WebView2-Steuerelement mithilfe oder `CoreWebView2.PostWebMessageAsString` `CoreWebView2.PostWebMessageAsJSON` .  Diese Nachrichten werden von Handlern erfasst, die zu hinzugefügt `window.chrome.webview.addEventListener` wurden.  

Der Kommunikationsmechanismus übergibt Nachrichten von Webinhalten mithilfe systemeigener Funktionen an den Host.  

Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, zeigt es die URL in der Adressleiste an und benachrichtigt den Benutzer über die im WebView2-Steuerelement angezeigte URL.  

1.  Aktualisieren Sie in der Datei den Konstruktor, und erstellen Sie eine `Form1.cs` `InitializeAsync` Funktion, die mit dem folgenden Codeausschnitt übereinstimmen soll.  Die `InitializeAsync` Funktion wartet auf [EnsureCoreWebView2Async,][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] da die Initialisierung `CoreWebView2` asynchron ist.  

    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

1.  Registrieren `CoreWebView2` Sie nach der Initialisierung einen Ereignishandler, um auf zu `WebMessageReceived` reagieren.  Aktualisieren und `Form1.cs` fügen Sie in der Datei mithilfe des folgenden `InitializeAsync` `UpdateAddressBar` Codeausschnitts hinzu.  

    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }

    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  

1.  Damit WebView die Webnachricht sendet und darauf antwortet, wird nach der Initialisierung ein Skript in den `CoreWebView2` Webinhalt eingef?nkt, um:  

    1.  Senden Sie die URL mithilfe von `postMessage` .
    1.  Registrieren Sie einen Ereignishandler, um eine vom Host gesendete Nachricht zu drucken.  

Aktualisieren Sie `Form1.cs` in der Datei so, dass sie mit `InitializeAsync` dem folgenden Codeausschnitt übereinstimmen.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Wählen Sie zum Erstellen und Ausführen der App die Option `F5` aus.  Jetzt zeigt die Adressleiste den URI im WebView2-Steuerelement an.  Wenn Sie erfolgreich zu einer neuen URL navigieren, wird der Benutzer außerdem von WebView über die url benachrichtigt, die in der WebView angezeigt wird.  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Endgültige App" lightbox="./media/winforms-finalapp.png":::
   Endgültige App  
:::image-end:::

Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.  

## Nächste Schritte  

Um weitere Informationen zu WebView2 zu erhalten, navigieren Sie zu den folgenden Ressourcen.  

### Weitere Informationen  

*   Ein umfassendes Beispiel der WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Weitere Informationen zu WebView2 finden Sie unter ["WebView2-Ressourcen".][Webview2IndexNextSteps]  
*   Ausführliche Informationen zur WebView2-API finden Sie in der [API-Referenz.][DotnetApiMicrosoftWebWebview2WinformsWebview2]  

## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft.Web.WebView2.WinForms Namespace-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "WebView2-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "WebView2.EnsureCoreWebView2Async(CoreWebView2Environment)-Methode | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String)-Methode | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Konfigurieren der Windows Forms-App für hohe DPI-Unterstützung – Unterstützung für hohe DPI in Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2| Microsoft Edge Developer"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
