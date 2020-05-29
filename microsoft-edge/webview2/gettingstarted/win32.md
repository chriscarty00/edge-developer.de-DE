---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Microsoft Edge WebView 2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 0ab152e52b5e5d89cf493ff525ce53d9ab174e6d
ms.sourcegitcommit: 799fe63d961a37ada455bb36ef3ef0d8076e70bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "10685680"
---
# Erste Schritte mit WebView2 (Entwicklervorschau)

In dieser exemplarischen Vorgehensweise werden die häufig verwendeten Funktionen von [WebView2 (Developer Preview)](https://aka.ms/webview) erläutert, und Sie erhalten den Einstieg in die Erstellung Ihrer ersten WebView2-app. Besuchen Sie die [API-Referenz](../reference/win32/0-9-488-reference-webview2.md) , um mehr über einzelne APIs zu erfahren.  

## Voraussetzungen

* [Microsoft Edge (Chrom)](https://www.microsoftedgeinsider.com/download/) auf dem unterstützten Betriebssystem installiert (derzeit Windows 10, Windows 8,1 und Windows 7). **Wir empfehlen die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0**.
* [Visual Studio](https://visualstudio.microsoft.com/) 2015 oder höher mit installierter C++-Unterstützung.

## Schritt 1 – Erstellen einer Win32-App für ein einzelnes Fenster

Wir beginnen mit einem einfachen Desktopprojekt, in dem sich ein einzelnes Hauptfenster befindet. Da dies nicht der Hauptschwerpunkt dieser exemplarischen Vorgehensweise ist, verwenden wir einfach geänderter Beispielcode aus [Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows-Desktop Anwendung (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019). [Laden](https://aka.ms/HelloWebView) Sie das geänderte Beispiel herunter, um zu beginnen.

Öffnen Sie **WebView2GettingStarted. sln** in Visual Studio. Wenn Sie eine ältere Version von Visual Studio verwenden, klicken Sie mit der rechten Maustaste auf das **WebView2GettingStarted** -Projekt, und klicken Sie auf **Eigenschaften**. Ändern Sie unter **Konfigurationseigenschaften**  >  **Allgemein**die **Windows SDK-Version** und das **Platform-Toolset** , um das Win10 SDK und das vs-Toolset zu verwenden, das Ihnen zur Verfügung steht.

![Tool-Version](../media/tool-version.png)

In Visual Studio werden möglicherweise einige Fehler aufgrund fehlender WebView2-Headerdatei angezeigt, die nach Abschluss des Schritts 2 verschwinden sollten.

## Schritt 2 – Installieren des WebView2 SDK

Nun fügen wir das WebView2-SDK in das Projekt ein. Für die Entwicklervorschau können Sie das Win32 SDK über Nuget installieren.

1. Klicken Sie mit der rechten Maustaste auf das Projekt, und klicken Sie auf **Nuget Pakete verwalten**.

    ![Manage-nuget-Pakete](../media/manage-nuget-packages.png)

2. Geben Sie in der Suchleiste **Microsoft. Windows. ImplementationLibrary** ein, klicken Sie auf der Seite Ergebnisse auf **Microsoft. Windows. ImplementationLibrary** , und klicken Sie im rechten Fenster auf **Installieren** , und installieren Sie das neueste SDK. Nuget wird das SDK auf Ihren Computer herunterladen. Während wir die [Windows-Implementierungs Bibliothek](https://github.com/Microsoft/wil) und die [Windows-Runtime-C++-Vorlagenbibliothek](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) verwenden, um die Arbeit mit com in dieser exemplarischen Vorgehensweise zu vereinfachen, sind Sie völlig optional.

    ![Wil](../media/wil.png)

3. Geben Sie in der Suchleiste **Microsoft. Web. WebView2** ein, klicken Sie auf der Seite Ergebnisse auf **Microsoft. Web. WebView2** , und klicken Sie im rechten Fenster auf **Installieren** , und installieren Sie das neueste SDK. Nuget wird das SDK auf Ihren Computer herunterladen.

    ![nuget](../media/nuget.png)

4. Fügen Sie den WebView2-Header ein. Fügen Sie in **HelloWebView. cpp** `#include "WebView2.h"` unterhalb der Zeilen von `#include` s ein.

    ```cpp
    ...
    #include <wrl.h>
    #include <wil/com.h>
    // include WebView2 header
    #include "WebView2.h"
    ```

Sie sind für die Verwendung und Erstellung von WebView2-APIs eingestellt. Drücken Sie F5, um die Beispiel-APP zu erstellen und auszuführen. Es sollte eine App angezeigt werden, die ein leeres Fenster anzeigt.

![Empty-App](../media/empty-app.png)

## Schritt 3 – Erstellen einer einzelnen WebView im übergeordneten Fenster

Nun fügen wir dem Hauptfenster eine WebView hinzu. Wir werden `CreateCoreWebView2Environment` zum Einrichten der Umgebung und suchen des Microsoft Edge-Browsers (Chrom), der das Steuerelement steuert, verwendet. Sie können auch verwenden, `CreateCoreWebView2EnvironmentWithOptions` Wenn Sie Browser Speicherort, Benutzerordner, Browser-Flags usw. angeben möchten, anstatt die Standardeinstellung zu verwenden. Nach Abschluss des `CreateCoreWebView2Environment` Vorgangs können Sie `ICoreWebView2Environment::CreateCoreWebView2Controller` innerhalb des `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` Rückrufs anrufen und `ICoreWebView2Controller::get_CoreWebView2` den zugehörigen WebView abrufen.

Im Rückruf können Sie auch einige Einstellungen festlegen, die Größe der WebView ändern, um 100% des übergeordneten Fensters zu übernehmen, und zu Bing navigieren.

Kopieren Sie den folgenden Code in **HelloWebView. cpp** zwischen `// <-- WebView2 sample code starts here -->` und `// <-- WebView2 sample code ends here -->` .

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {

            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }

                // Add a few settings for the webview
                // this is a redundant demo step as they are the default settings values
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);

                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);

                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");

                // Step 4 - Navigation events


                // Step 5 - Scripting


                // Step 6 - Communication between host and web content


                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```

Drücken Sie F5, um die App zu erstellen und auszuführen. Sie haben jetzt ein WebView-Fenster, in dem Bing angezeigt wird.

![Bing-Fenster](../media/bing-window.png)

## Schritt 4 – Navigationsereignisse

Im letzten Schritt haben wir bereits über die Navigation zur URL verdeckt `ICoreWebView2::Navigate` . Während der Navigation löst WebView eine Abfolge von Ereignissen aus, die der Host abhören kann –,,, `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` und dann `NavigationCompleted` . Klicken Sie [hier](../reference/win32/0-9-488/ICoreWebView2.md#navigation-events) , um weitere Informationen zu erhalten.

![Navigationsereignisse](../media/navigation-events.png)

In Fehlerfällen kann es vorkommen, dass es `SourceChanged` sich `ContentLoading` `HistoryChanged` um eine Fehlerseite handelt oder nicht, oder ob es sich um ein Ereignis (e) handelt. Im Fall einer HTTP-Umleitung werden mehrere `NavigationStarting` Ereignisse in einer Zeile vorhanden sein.

Als Beispiel für die Verwendung dieser Ereignisse registrieren wir einen Handler, `NavigationStarting` um nicht-HTTPS-Anforderungen abzubrechen. Kopieren Sie den folgenden Code unten in **HelloWebView. cpp** `// Step 4 - Navigation events` .

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```

Nun wird die APP nicht zu allen nicht-HTTPS-Websites navigieren. Sie können einen ähnlichen Mechanismus verwenden, um andere Aufgaben auszuführen, wie etwa das Einschränken der Navigation in ihrer eigenen Domäne.

## Schritt 5 – Skripting

Die Host-App kann auch JavaScript in WebView einfügen. Sie können mit der Aufgabe WebView beliebiges JavaScript ausführen oder Initialisierungsskripts hinzufügen. Hinzugefügte Initialisierungsskripts gelten für alle zukünftigen Dokument-und untergeordneten Frame-Navigationselemente auf oberster Ebene, bis Sie entfernt werden, und führen Sie nach dem Erstellen des globalen Objekts und vor dem Ausführen anderer Skripts, die im HTML-Dokument enthalten sind.

Kopieren Sie den folgenden Code unten `// Step 5 - Scripting` .

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```

Jetzt fixiert WebView das Objekt Objekt immer und gibt das Seiten Dokument einmal zurück.

**Beachten Sie, dass diese Skript Injektions-APIs (und einige andere WebView2-APIs) asynchron sind, sollten Sie Rückrufe verwenden, wenn Code in einer bestimmten Reihenfolge ausgeführt werden soll.**

## Schritt 6 – Kommunikation zwischen Host-und Webinhalten

Der Host und die Webinhalte können auch miteinander kommunizieren `postMessage` . Die Webinhalte, die in einer WebView ausgeführt werden, können über den Host bereitgestellt `window.chrome.webview.postMessage` werden, und die Nachricht wird von allen `ICoreWebView2WebMessageReceivedEventHandler` auf dem Host registrierten Computern verarbeitet. Ebenso kann der Host die Webinhalte über `ICoreWebView2::PostWebMessageAsString` oder `ICoreWebView2::PostWebMessageAsJSON` , die von Handlern hinzugefügt wurden, Nachrichten `window.chrome.webview.addEventListener` . Mithilfe des Kommunikationsmechanismus können Webinhalte systemeigene Funktionen verwenden, indem Sie Nachrichten übergeben, um den Host zu bitten, systemeigene APIs aufzurufen.

Als Beispiel, um den Mechanismus zu verstehen, versuchen wir, die Dokument-URL in WebView mit einem kleinen Umweg zu drucken.

1. der Host registriert einen Handler, um die empfangene Nachricht zurück an den Webinhalt zurückzugeben
2. der Host injiziert einem Webinhalt ein Skript, das einen Handler registriert, um eine Nachricht vom Host zu drucken.
3. der Host injiziert einem Webinhalt ein Skript, das die URL an den Host sendet.
4. der Handler des Hosts wird ausgelöst und gibt die Nachricht (die URL) an die Webinhalte zurück.
5. der Handler des Webinhalts wird ausgelöst und die Nachricht des Hosts (die URL) gedruckt.

Kopieren Sie den folgenden Code unten `// Step 6 - Communication between host and web content` :

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```

Drücken Sie F5, um die App zu erstellen und auszuführen. Es werden nun URLs angezeigt, bevor Sie zu Seiten navigieren.

![anzeigen-URL](../media/show-url.png)

Herzlichen Glückwunsch, Sie haben soeben Ihre erste WebView2-App erstellt!

## Nächste Schritte

Es gibt viele WebView2-Funktionen, die in dieser exemplarischen Vorgehensweise nicht behandelt werden.

Weitere Informationen finden Sie unter:

* Checkout [-WebView2-API-Beispiel](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) für ein umfassendes Beispiel für WebView2's-Funktionen.
* Auschecken [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) einer mit WebView2 erstellten Anwendung.
* Detaillierte Informationen zu unserer API finden Sie unter [API-Referenz](../reference/win32/0-9-488-reference-webview2.md) .  

## Kontakt mit dem WebView2-Team  

Helfen Sie uns, ein reicheres WebView2-Erlebnis zu schaffen, indem Sie Ihr Feedback austauschen! Besuchen Sie unser [Feedback-Repo](https://aka.ms/webviewfeedback) , um Funktionsanforderungen oder Fehlerberichte einzureichen oder nach bekannten Problemen zu suchen.
