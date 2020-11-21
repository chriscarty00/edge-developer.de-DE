---
description: Leitfaden für erste Schritte mit WebView2 für WinForms-apps
title: Erste Schritte mit WebView2 für WinForms-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinForms-apps, WinForms, Edge, CoreWebView2, Browser Control, Edge HTML, erste Schritte, erste Schritte, .net, Windows Forms
ms.openlocfilehash: f4768c38f293d1931e625136ea7068a61176541e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182388"
---
# Erste Schritte mit WebView2 in Windows Forms

In diesem Artikel erfahren Sie, wie Sie Ihre erste WebView2-app erstellen und Informationen zu den Hauptfeatures von [WebView2](/microsoft-edge/webview2/index)erhalten.  Weitere Informationen zu einzelnen APIs finden Sie unter [API-Referenz](/dotnet/api/microsoft.web.webview2.winforms).  

## Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installiert haben, bevor Sie fortfahren:  

* [WebView2-Runtime][Webview2Installer] oder ein [nicht stabiler Microsoft Edge (Chrom) Canary-Kanal](https://www.microsoftedgeinsider.com/download) , der unter Windows 10, Windows 8,1 oder Windows 7 installiert ist. 
* [Visual Studio](https://visualstudio.microsoft.com) 2017 oder höher

> [!NOTE]
> WebView2 unterstützt derzeit keine .net 5-und .net Core-Designer.

## Schritt 1 – Erstellen einer einzelnen Fenster Anwendung

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  

1. Öffnen Sie **Visual Studio.**

1. Wählen Sie **Windows Forms .NET Framework-App** aus, und wählen Sie dann **weiter**aus.

    ![NewProject](./media/winforms-newproject.png)

1. Geben Sie Werte für **Projektname** und **Speicherort**ein.  Wählen Sie **.NET Framework 4.6.2** oder höher aus.  

    ![startproject](./media/winforms-startproj.png)

1. Wählen Sie **Erstellen** aus, um Ihr Projekt zu erstellen.

## Schritt 2 – Installieren des WebView2 SDK

Als Nächstes fügen Sie das WebView2-SDK mit NuGet zum Projekt hinzu.

1. Öffnen Sie das Kontextmenü im Projekt \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **NuGet-Pakete verwalten**aus.  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Verwalten von NuGet-Paketen":::
       Verwalten von NuGet-Paketen :::image-end:::

1. Geben Sie `Microsoft.Web.WebView2` in die Suchleiste ein.  Wählen Sie in den Suchergebnissen **Microsoft. Web. WebView2** aus.  

    ![nuget](./media/installnuget.png)

Mit der WebView2-API können Sie nun mit der Entwicklung von Anwendungen beginnen.  Wählen Sie aus `F5` , um das Projekt zu erstellen und auszuführen.  Im laufenden Projekt wird ein leeres Fenster angezeigt.  

![emptyApp](./media/winforms-emptyApp.png)

## Schritt 3 – Erstellen einer einzelnen WebView  

Fügen Sie Ihrer Anwendung als nächstes eine WebView hinzu.  

1. Öffnen Sie den **Windows Forms-Designer**.  
1. Suchen Sie in der **Toolbox**nach **WebView2** . Ziehen Sie das **WebView2** -Steuerelement in die Windows Forms-APP, und legen Sie es ab.
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Toolbox mit Anzeige von WebView2":::
       Toolbox mit Anzeige von WebView2 :::image-end:::  

1. Ändern Sie die `Name`-Eigenschaft in `webView`.
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Eigenschaften des WebView2-Steuerelements":::
       Eigenschaften des WebView2-Steuerelements :::image-end:::

1. Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird. Setzen Sie die Source-Eigenschaft auf <https://www.microsoft.com>
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Die Source-Eigenschaft des WebView2-Steuerelements":::
       Die Source-Eigenschaft des WebView2-Steuerelements :::image-end:::

Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.  Vergewissern Sie sich, dass Ihr WebView2-Steuerelement angezeigt wird [https://www.microsoft.com](https://www.microsoft.com) .

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> Wenn Sie mit einem HD-Monitor arbeiten, müssen Sie möglicherweise [Ihre Windows Forms-App für die Unterstützung mit höherer dpi-Auflösung konfigurieren](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).

## Schritt 4: Behandeln von Fenstergrößen Ereignissen

Fügen Sie Ihren Windows Forms einige weitere Steuerelemente aus der Toolbox hinzu, und behandeln Sie die Ereignisse für die Fenstergröße entsprechend.

1. Öffnen der **Toolbox** im **Windows Forms-Designer**
1. Ziehen Sie ein **Textfeld** in die Windows Forms-APP, und legen Sie es ab. Benennen Sie das **Textfeld** `addressBar` auf der **Registerkarte Eigenschaften**.
1. Ziehen Sie eine **Schaltfläche** in die Windows Forms-APP, und legen Sie Sie ab. Ändern Sie den Text in der **Schaltfläche** , `Go!` und benennen Sie die **Schaltfläche** auf `goButton` der **Registerkarte Eigenschaften**.

    Die APP sollte im Designer wie in der folgenden Abbildung aussehen.
    
    ![-Designer](./media/winforms-designer.png)

1. In **Form1.cs** definieren `Form_Resize` , um die Steuerelemente beizubehalten, wenn die Größe des App-Fensters geändert wird.

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

Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.  Vergewissern Sie sich, dass die APP ähnlich wie der folgende Screenshot angezeigt wird.

![App](./media/winforms-app.png)

## Schritt 5 – Navigation

Hinzufügen der Möglichkeit, dass Benutzer die vom WebView2-Steuerelement angezeigte URL ändern können, indem Sie der App eine Adressleiste hinzufügen.

1. `Form1.cs`Fügen Sie den `CoreWebView2` Namespace hinzu, indem Sie den folgenden Codeausschnitt oben auf Einfügen `Form1.cs` .  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. Doppelklicken Sie im **Windows Forms-Designer**auf die `Go!` Schaltfläche, um die `goButton_Click` Methode in zu erstellen `Form1.cs` . Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in die Funktion ein. Nun `goButton_Click` navigiert die Funktion in der WebView zu der URL, die in der Adressleiste eingegeben wurde.

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.  Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **dann gehe**zu aus.  Geben Sie beispielsweise ein `https://www.bing.com` .  Überprüfen Sie, ob das WebView2-Steuerelement zur URL navigiert.  

> [!NOTE]
> Stellen Sie sicher, dass in der Adressleiste eine vollständige URL eingegeben wurde. Eine `ArgumentException` wird ausgelöst, wenn die URL nicht mit gestartet wird `http://` oder `https://`

![bing](./media/winforms-bing.png)

## Schritt 6 – Navigationsereignisse  

Während der Webseiten Navigation löst das WebView2-Steuerelementereignisse aus. Die Anwendung, die WebView2-Steuerelemente hostet, überwacht die folgenden Ereignisse.  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

Weitere Informationen finden Sie unter [Navigationsereignisse](../concepts/navigation-events.md).  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   Navigationsereignisse
:::image-end:::

Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und können von der Navigation zu einer Fehlerseite abhängen.  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

Wenn eine HTTP-Umleitung vorhanden ist, gibt es mehrere `NavigationStarting` Ereignisse.  

Um zu veranschaulichen, wie diese Ereignisse verwendet werden, müssen Sie zunächst einen Handler registrieren, der `NavigationStarting` alle Anforderungen abbricht, die kein HTTPS verwenden.  

`Form1.cs`Ändern Sie in den Konstruktor wie unten dargestellt, und fügen Sie die `EnsureHttps` Funktion hinzu.  

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

Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen. Vergewissern Sie sich, dass die WebView-Ansicht beim Navigieren zu einer HTTP-Website unverändert bleibt. Die WebView wird jedoch zu HTTPS-Websites navigieren.

## Schritt 7 – Skripting  

Sie können Host-Anwendungen verwenden, um JavaScript-Code zur Laufzeit in WebView2-Steuerelemente einzufügen.  Das eingefügte JavaScript gilt für alle neuen Dokumente auf oberster Ebene und für alle untergeordneten Frames, bis das JavaScript entfernt wurde.  Das eingefügte JavaScript wird nach der Erstellung des globalen Objekts und vor den Skripts, die im HTML-Dokument enthalten sind, ausgeführt.  

Sie können Skripting verwenden, um den Benutzer zu benachrichtigen, wenn Sie zu einer nicht-HTTPS-Website navigieren.  Ändern `EnsureHttps` Sie die Funktion so, dass Sie mit der [ExecuteScriptAsync]() -Methode Skripts in den Webinhalt einfügt.  

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

Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.  Vergewissern Sie sich, dass die Anwendung eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die nicht HTTPS verwendet.  

![https](./media/winforms-https.png)

## Schritt 8 – Kommunikation zwischen Host-und Webinhalten  

Die Host-und Webinhalte können mithilfe der folgenden Informationen miteinander kommunizieren `postMessage` :  

* Webinhalte in einem WebView2-Steuerelement senden möglicherweise eine Nachricht mithilfe von an den Host `window.chrome.webview.postMessage` .  Der Host verarbeitet die Nachricht mit einem `WebMessageReceived` auf dem Host registrierten Namen.  
* Hosts Posten Nachrichten an Webinhalte in einem WebView2-Steuerelement mit `CoreWebView2.PostWebMessageAsString` oder `CoreWebView2.PostWebMessageAsJSON` .  Diese Nachrichten werden von Handlern abgefangen, denen Sie hinzugefügt wurden `window.chrome.webview.addEventListener` .  

Mit diesem Kommunikationsmechanismus können Webinhalte Nachrichten mithilfe von systemeigenen Funktionen an den Host weiterleiten.  

Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, wird die URL in der Adressleiste angezeigt, und der Benutzer wird benachrichtigt, dass die URL im WebView2-Steuerelement angezeigt wird.  

1. Aktualisieren Sie in **Form1.cs**den Konstruktor, und erstellen Sie eine `InitializeAsync` Funktion, wie im folgenden Codeausschnitt dargestellt.  Die `InitializeAsync` Funktion wartet [EnsureCoreWebView2Async]() auf, da die Initialisierung von `CoreWebView2` asynchron ist.  

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

1. Nachdem **CoreWebView2** initialisiert wurde, registrieren Sie einen Ereignishandler, auf den Sie Antworten können `WebMessageReceived` .  In `Form1.cs` , aktualisieren `InitializeAsync` und hinzufügen `UpdateAddressBar` mithilfe des folgenden Codeausschnitts.  

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

1. Damit die WebView die Webnachricht senden und beantworten kann, wird nach der `CoreWebView2` Initialisierung der Host ein Skript in den Webinhalt eingefügt, um:  

    1. Senden Sie die URL an den Host mit `postMessage` .
    1. Registrieren Sie einen Ereignishandler, um eine vom Host gesendete Nachricht zu drucken.  

In `Form1.cs` , aktualisieren Sie, `InitializeAsync` wie im folgenden Codeausschnitt dargestellt.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Wählen Sie aus `F5` , um die APP zu erstellen und auszuführen.  Vergewissern Sie sich, dass auf der Adressleiste die URL der Website angezeigt wird, die in der WebView angezeigt wird. Wenn Sie erfolgreich zu einer neuen URL navigieren, benachrichtigt die WebView den Benutzer auch über die URL, die in der WebView angezeigt wird.  

![finalapp](./media/winforms-finalapp.png)

Herzlichen Glückwunsch, Sie haben ihre erste WebView2-App erstellt!  

## Nächste Schritte 

Navigieren Sie zu den folgenden Ressourcen, um weitere Informationen zu WebView2 zu erfahren.

* Das [WebView2Samples Repo](https://github.com/MicrosoftEdge/WebView2Samples) bietet ein umfassendes Beispiel für WebView2's-Funktionen.
* Die [API-Referenz](/dotnet/api/microsoft.web.webview2.winforms.webview2) für detailliertere Informationen zu unseren APIs.
* [WebView2-Ressourcen](../index.md#next-steps).


## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-Installationsprogramm" 
