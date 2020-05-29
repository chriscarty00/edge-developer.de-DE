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
# <span data-ttu-id="4613f-104">Erste Schritte mit WebView2 (Entwicklervorschau)</span><span class="sxs-lookup"><span data-stu-id="4613f-104">Getting Started with WebView2 (developer preview)</span></span>

<span data-ttu-id="4613f-105">In dieser exemplarischen Vorgehensweise werden die häufig verwendeten Funktionen von [WebView2 (Developer Preview)](https://aka.ms/webview) erläutert, und Sie erhalten den Einstieg in die Erstellung Ihrer ersten WebView2-app.</span><span class="sxs-lookup"><span data-stu-id="4613f-105">This walkthrough goes over the commonly used functionalities of [WebView2 (developer preview)](https://aka.ms/webview) and gets you started on creating your first WebView2 app.</span></span> <span data-ttu-id="4613f-106">Besuchen Sie die [API-Referenz](../reference/win32/0-9-488-reference-webview2.md) , um mehr über einzelne APIs zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="4613f-106">Visit [API reference](../reference/win32/0-9-488-reference-webview2.md) to learn more about individual APIs.</span></span>  

## <span data-ttu-id="4613f-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4613f-107">Prerequisites</span></span>

* <span data-ttu-id="4613f-108">[Microsoft Edge (Chrom)](https://www.microsoftedgeinsider.com/download/) auf dem unterstützten Betriebssystem installiert (derzeit Windows 10, Windows 8,1 und Windows 7).</span><span class="sxs-lookup"><span data-stu-id="4613f-108">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) installed on supported OS (currently Windows 10, Windows 8.1, and Windows 7).</span></span> <span data-ttu-id="4613f-109">**Wir empfehlen die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0**.</span><span class="sxs-lookup"><span data-stu-id="4613f-109">**We recommend using the Canary channel and the minimum required version is 82.0.488.0**.</span></span>
* <span data-ttu-id="4613f-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 oder höher mit installierter C++-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="4613f-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 or later with C++ support installed.</span></span>

## <span data-ttu-id="4613f-111">Schritt 1 – Erstellen einer Win32-App für ein einzelnes Fenster</span><span class="sxs-lookup"><span data-stu-id="4613f-111">Step 1 - Create a single window win32 app</span></span>

<span data-ttu-id="4613f-112">Wir beginnen mit einem einfachen Desktopprojekt, in dem sich ein einzelnes Hauptfenster befindet.</span><span class="sxs-lookup"><span data-stu-id="4613f-112">We will start with a basic desktop project containing a single main window.</span></span> <span data-ttu-id="4613f-113">Da dies nicht der Hauptschwerpunkt dieser exemplarischen Vorgehensweise ist, verwenden wir einfach geänderter Beispielcode aus [Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows-Desktop Anwendung (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="4613f-113">As this is not the main focus of this walkthrough, we will simply use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span> <span data-ttu-id="4613f-114">[Laden](https://aka.ms/HelloWebView) Sie das geänderte Beispiel herunter, um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="4613f-114">[Download](https://aka.ms/HelloWebView) the modified sample to get started.</span></span>

<span data-ttu-id="4613f-115">Öffnen Sie **WebView2GettingStarted. sln** in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4613f-115">Open **WebView2GettingStarted.sln** in Visual Studio.</span></span> <span data-ttu-id="4613f-116">Wenn Sie eine ältere Version von Visual Studio verwenden, klicken Sie mit der rechten Maustaste auf das **WebView2GettingStarted** -Projekt, und klicken Sie auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="4613f-116">If you are using an older version of Visual Studio, right click on the **WebView2GettingStarted** project and click **Properties**.</span></span> <span data-ttu-id="4613f-117">Ändern Sie unter **Konfigurationseigenschaften**  >  **Allgemein**die **Windows SDK-Version** und das **Platform-Toolset** , um das Win10 SDK und das vs-Toolset zu verwenden, das Ihnen zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="4613f-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and VS toolset available to you.</span></span>

![Tool-Version](../media/tool-version.png)

<span data-ttu-id="4613f-119">In Visual Studio werden möglicherweise einige Fehler aufgrund fehlender WebView2-Headerdatei angezeigt, die nach Abschluss des Schritts 2 verschwinden sollten.</span><span class="sxs-lookup"><span data-stu-id="4613f-119">Visual Studio may show some errors due to missing WebView2 header file, which should go away once Step 2 is completed.</span></span>

## <span data-ttu-id="4613f-120">Schritt 2 – Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="4613f-120">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="4613f-121">Nun fügen wir das WebView2-SDK in das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="4613f-121">Now let's add the WebView2 SDK into the project.</span></span> <span data-ttu-id="4613f-122">Für die Entwicklervorschau können Sie das Win32 SDK über Nuget installieren.</span><span class="sxs-lookup"><span data-stu-id="4613f-122">For the developer preview, you can install the Win32 SDK via Nuget.</span></span>

1. <span data-ttu-id="4613f-123">Klicken Sie mit der rechten Maustaste auf das Projekt, und klicken Sie auf **Nuget Pakete verwalten**.</span><span class="sxs-lookup"><span data-stu-id="4613f-123">Right click the project and click **Manage Nuget Packages**.</span></span>

    ![Manage-nuget-Pakete](../media/manage-nuget-packages.png)

2. <span data-ttu-id="4613f-125">Geben Sie in der Suchleiste **Microsoft. Windows. ImplementationLibrary** ein, klicken Sie auf der Seite Ergebnisse auf **Microsoft. Windows. ImplementationLibrary** , und klicken Sie im rechten Fenster auf **Installieren** , und installieren Sie das neueste SDK.</span><span class="sxs-lookup"><span data-stu-id="4613f-125">Enter **Microsoft.Windows.ImplementationLibrary** in the search bar, click **Microsoft.Windows.ImplementationLibrary** from the results, and click **Install** inthe right hand side window and install the latest SDK.</span></span> <span data-ttu-id="4613f-126">Nuget wird das SDK auf Ihren Computer herunterladen.</span><span class="sxs-lookup"><span data-stu-id="4613f-126">Nuget will download the SDK to your machine.</span></span> <span data-ttu-id="4613f-127">Während wir die [Windows-Implementierungs Bibliothek](https://github.com/Microsoft/wil) und die [Windows-Runtime-C++-Vorlagenbibliothek](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) verwenden, um die Arbeit mit com in dieser exemplarischen Vorgehensweise zu vereinfachen, sind Sie völlig optional.</span><span class="sxs-lookup"><span data-stu-id="4613f-127">While we use [Windows Implementation Library](https://github.com/Microsoft/wil) and [Windows Runtime C++ Template Library](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) to make working with COM easier in this walkthrough, they are completely optional.</span></span>

    ![Wil](../media/wil.png)

3. <span data-ttu-id="4613f-129">Geben Sie in der Suchleiste **Microsoft. Web. WebView2** ein, klicken Sie auf der Seite Ergebnisse auf **Microsoft. Web. WebView2** , und klicken Sie im rechten Fenster auf **Installieren** , und installieren Sie das neueste SDK.</span><span class="sxs-lookup"><span data-stu-id="4613f-129">Enter **Microsoft.Web.WebView2** in the search bar, click **Microsoft.Web.WebView2** from the results, and click **Install** in the right hand side window and install the latest SDK.</span></span> <span data-ttu-id="4613f-130">Nuget wird das SDK auf Ihren Computer herunterladen.</span><span class="sxs-lookup"><span data-stu-id="4613f-130">Nuget will download the SDK to your machine.</span></span>

    ![nuget](../media/nuget.png)

4. <span data-ttu-id="4613f-132">Fügen Sie den WebView2-Header ein.</span><span class="sxs-lookup"><span data-stu-id="4613f-132">Include the WebView2 header.</span></span> <span data-ttu-id="4613f-133">Fügen Sie in **HelloWebView. cpp** `#include "WebView2.h"` unterhalb der Zeilen von `#include` s ein.</span><span class="sxs-lookup"><span data-stu-id="4613f-133">In **HelloWebView.cpp**, add `#include "WebView2.h"` below the lines of `#include`s.</span></span>

    ```cpp
    ...
    #include <wrl.h>
    #include <wil/com.h>
    // include WebView2 header
    #include "WebView2.h"
    ```

<span data-ttu-id="4613f-134">Sie sind für die Verwendung und Erstellung von WebView2-APIs eingestellt.</span><span class="sxs-lookup"><span data-stu-id="4613f-134">You are all set to use and build against the WebView2 API.</span></span> <span data-ttu-id="4613f-135">Drücken Sie F5, um die Beispiel-APP zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4613f-135">Press F5 to build and run the sample app.</span></span> <span data-ttu-id="4613f-136">Es sollte eine App angezeigt werden, die ein leeres Fenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="4613f-136">You should see an app displaying an empty window.</span></span>

![Empty-App](../media/empty-app.png)

## <span data-ttu-id="4613f-138">Schritt 3 – Erstellen einer einzelnen WebView im übergeordneten Fenster</span><span class="sxs-lookup"><span data-stu-id="4613f-138">Step 3 - Create a single WebView within the parent window</span></span>

<span data-ttu-id="4613f-139">Nun fügen wir dem Hauptfenster eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="4613f-139">Now let's add a WebView to the main window.</span></span> <span data-ttu-id="4613f-140">Wir werden `CreateCoreWebView2Environment` zum Einrichten der Umgebung und suchen des Microsoft Edge-Browsers (Chrom), der das Steuerelement steuert, verwendet.</span><span class="sxs-lookup"><span data-stu-id="4613f-140">We'll use `CreateCoreWebView2Environment` to set up the environment and locate the Microsoft Edge (Chromium) browser powering the control.</span></span> <span data-ttu-id="4613f-141">Sie können auch verwenden, `CreateCoreWebView2EnvironmentWithOptions` Wenn Sie Browser Speicherort, Benutzerordner, Browser-Flags usw. angeben möchten, anstatt die Standardeinstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4613f-141">You can also use `CreateCoreWebView2EnvironmentWithOptions` if you want to specify browser location, user folder, browser flags, etc., instead of using the default setting.</span></span> <span data-ttu-id="4613f-142">Nach Abschluss des `CreateCoreWebView2Environment` Vorgangs können Sie `ICoreWebView2Environment::CreateCoreWebView2Controller` innerhalb des `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` Rückrufs anrufen und `ICoreWebView2Controller::get_CoreWebView2` den zugehörigen WebView abrufen.</span><span class="sxs-lookup"><span data-stu-id="4613f-142">Upon the completion of `CreateCoreWebView2Environment`, you'll be able to call `ICoreWebView2Environment::CreateCoreWebView2Controller` inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and call `ICoreWebView2Controller::get_CoreWebView2` to get the associated WebView.</span></span>

<span data-ttu-id="4613f-143">Im Rückruf können Sie auch einige Einstellungen festlegen, die Größe der WebView ändern, um 100% des übergeordneten Fensters zu übernehmen, und zu Bing navigieren.</span><span class="sxs-lookup"><span data-stu-id="4613f-143">In the callback, let's also set a few settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>

<span data-ttu-id="4613f-144">Kopieren Sie den folgenden Code in **HelloWebView. cpp** zwischen `// <-- WebView2 sample code starts here -->` und `// <-- WebView2 sample code ends here -->` .</span><span class="sxs-lookup"><span data-stu-id="4613f-144">Copy the following code to **HelloWebView.cpp** between `// <-- WebView2 sample code starts here -->` and `// <-- WebView2 sample code ends here -->`.</span></span>

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

<span data-ttu-id="4613f-145">Drücken Sie F5, um die App zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4613f-145">Press F5 to build and run the app.</span></span> <span data-ttu-id="4613f-146">Sie haben jetzt ein WebView-Fenster, in dem Bing angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4613f-146">Now you have a WebView window displaying Bing.</span></span>

![Bing-Fenster](../media/bing-window.png)

## <span data-ttu-id="4613f-148">Schritt 4 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="4613f-148">Step 4 - Navigation events</span></span>

<span data-ttu-id="4613f-149">Im letzten Schritt haben wir bereits über die Navigation zur URL verdeckt `ICoreWebView2::Navigate` .</span><span class="sxs-lookup"><span data-stu-id="4613f-149">We already covered navigating to URL using `ICoreWebView2::Navigate` in the last step.</span></span> <span data-ttu-id="4613f-150">Während der Navigation löst WebView eine Abfolge von Ereignissen aus, die der Host abhören kann –,,, `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` und dann `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="4613f-150">During navigation, WebView fires a sequence of events that the host can listen to - `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span> <span data-ttu-id="4613f-151">Klicken Sie [hier](../reference/win32/0-9-488/ICoreWebView2.md#navigation-events) , um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4613f-151">Click [here](../reference/win32/0-9-488/ICoreWebView2.md#navigation-events) to learn more.</span></span>

![Navigationsereignisse](../media/navigation-events.png)

<span data-ttu-id="4613f-153">In Fehlerfällen kann es vorkommen, dass es `SourceChanged` sich `ContentLoading` `HistoryChanged` um eine Fehlerseite handelt oder nicht, oder ob es sich um ein Ereignis (e) handelt.</span><span class="sxs-lookup"><span data-stu-id="4613f-153">In error cases there may or may not be `SourceChanged`, `ContentLoading`, or `HistoryChanged` event(s) depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="4613f-154">Im Fall einer HTTP-Umleitung werden mehrere `NavigationStarting` Ereignisse in einer Zeile vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4613f-154">In case of an HTTP redirect, there will be multiple `NavigationStarting` events in a row.</span></span>

<span data-ttu-id="4613f-155">Als Beispiel für die Verwendung dieser Ereignisse registrieren wir einen Handler, `NavigationStarting` um nicht-HTTPS-Anforderungen abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="4613f-155">As an example of utilizing those events, let's register a handler for `NavigationStarting` to cancel any non-https requests.</span></span> <span data-ttu-id="4613f-156">Kopieren Sie den folgenden Code unten in **HelloWebView. cpp** `// Step 4 - Navigation events` .</span><span class="sxs-lookup"><span data-stu-id="4613f-156">Copy the following code to **HelloWebView.cpp** below `// Step 4 - Navigation events`.</span></span>

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

<span data-ttu-id="4613f-157">Nun wird die APP nicht zu allen nicht-HTTPS-Websites navigieren.</span><span class="sxs-lookup"><span data-stu-id="4613f-157">Now the app will not navigate to any non-https sites.</span></span> <span data-ttu-id="4613f-158">Sie können einen ähnlichen Mechanismus verwenden, um andere Aufgaben auszuführen, wie etwa das Einschränken der Navigation in ihrer eigenen Domäne.</span><span class="sxs-lookup"><span data-stu-id="4613f-158">You can use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>

## <span data-ttu-id="4613f-159">Schritt 5 – Skripting</span><span class="sxs-lookup"><span data-stu-id="4613f-159">Step 5 - Scripting</span></span>

<span data-ttu-id="4613f-160">Die Host-App kann auch JavaScript in WebView einfügen.</span><span class="sxs-lookup"><span data-stu-id="4613f-160">The hosting app can also inject JavaScript into WebView.</span></span> <span data-ttu-id="4613f-161">Sie können mit der Aufgabe WebView beliebiges JavaScript ausführen oder Initialisierungsskripts hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4613f-161">You can task WebView to execute arbitrary JavaScript or add initialization scripts.</span></span> <span data-ttu-id="4613f-162">Hinzugefügte Initialisierungsskripts gelten für alle zukünftigen Dokument-und untergeordneten Frame-Navigationselemente auf oberster Ebene, bis Sie entfernt werden, und führen Sie nach dem Erstellen des globalen Objekts und vor dem Ausführen anderer Skripts, die im HTML-Dokument enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4613f-162">Added initialization scripts apply to all future top level document and child frame navigation until removed, and run after the global object has been created and before any other script included by the HTML document is executed.</span></span>

<span data-ttu-id="4613f-163">Kopieren Sie den folgenden Code unten `// Step 5 - Scripting` .</span><span class="sxs-lookup"><span data-stu-id="4613f-163">Copy the following code below `// Step 5 - Scripting`.</span></span>

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

<span data-ttu-id="4613f-164">Jetzt fixiert WebView das Objekt Objekt immer und gibt das Seiten Dokument einmal zurück.</span><span class="sxs-lookup"><span data-stu-id="4613f-164">Now WebView will always freeze the Object object and return the page document once.</span></span>

**<span data-ttu-id="4613f-165">Beachten Sie, dass diese Skript Injektions-APIs (und einige andere WebView2-APIs) asynchron sind, sollten Sie Rückrufe verwenden, wenn Code in einer bestimmten Reihenfolge ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4613f-165">Note that these script injection APIs (and some other WebView2 APIs) are asynchronous, you should use callbacks if code is to be executed in a particular order.</span></span>**

## <span data-ttu-id="4613f-166">Schritt 6 – Kommunikation zwischen Host-und Webinhalten</span><span class="sxs-lookup"><span data-stu-id="4613f-166">Step 6 - Communication between host and web content</span></span>

<span data-ttu-id="4613f-167">Der Host und die Webinhalte können auch miteinander kommunizieren `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="4613f-167">The host and the web content can also communicate with each other through `postMessage`.</span></span> <span data-ttu-id="4613f-168">Die Webinhalte, die in einer WebView ausgeführt werden, können über den Host bereitgestellt `window.chrome.webview.postMessage` werden, und die Nachricht wird von allen `ICoreWebView2WebMessageReceivedEventHandler` auf dem Host registrierten Computern verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4613f-168">The web content running within a WebView can post to the host through `window.chrome.webview.postMessage`, and the message would be handled by any registered `ICoreWebView2WebMessageReceivedEventHandler` on the host.</span></span> <span data-ttu-id="4613f-169">Ebenso kann der Host die Webinhalte über `ICoreWebView2::PostWebMessageAsString` oder `ICoreWebView2::PostWebMessageAsJSON` , die von Handlern hinzugefügt wurden, Nachrichten `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="4613f-169">Likewise, the host can message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON`, which would be caught by handlers added from `window.chrome.webview.addEventListener`.</span></span> <span data-ttu-id="4613f-170">Mithilfe des Kommunikationsmechanismus können Webinhalte systemeigene Funktionen verwenden, indem Sie Nachrichten übergeben, um den Host zu bitten, systemeigene APIs aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4613f-170">The communication mechanism allows the web content to utilize native capabilities by passing messages to ask the host to call native APIs.</span></span>

<span data-ttu-id="4613f-171">Als Beispiel, um den Mechanismus zu verstehen, versuchen wir, die Dokument-URL in WebView mit einem kleinen Umweg zu drucken.</span><span class="sxs-lookup"><span data-stu-id="4613f-171">As an example to understand the mechanism, let's try printing out the document URL in WebView with a little detour,</span></span>

1. <span data-ttu-id="4613f-172">der Host registriert einen Handler, um die empfangene Nachricht zurück an den Webinhalt zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="4613f-172">the host registers a handler to return received message back to the web content</span></span>
2. <span data-ttu-id="4613f-173">der Host injiziert einem Webinhalt ein Skript, das einen Handler registriert, um eine Nachricht vom Host zu drucken.</span><span class="sxs-lookup"><span data-stu-id="4613f-173">the host injects a script to the web content that registers a handler to print message from the host</span></span>
3. <span data-ttu-id="4613f-174">der Host injiziert einem Webinhalt ein Skript, das die URL an den Host sendet.</span><span class="sxs-lookup"><span data-stu-id="4613f-174">the host injects a script to the web content that posts the URL to the host</span></span>
4. <span data-ttu-id="4613f-175">der Handler des Hosts wird ausgelöst und gibt die Nachricht (die URL) an die Webinhalte zurück.</span><span class="sxs-lookup"><span data-stu-id="4613f-175">the host's handler is triggered and returns the message (the URL) to the web content</span></span>
5. <span data-ttu-id="4613f-176">der Handler des Webinhalts wird ausgelöst und die Nachricht des Hosts (die URL) gedruckt.</span><span class="sxs-lookup"><span data-stu-id="4613f-176">the web content's handler is triggered and prints the host's message (the URL)</span></span>

<span data-ttu-id="4613f-177">Kopieren Sie den folgenden Code unten `// Step 6 - Communication between host and web content` :</span><span class="sxs-lookup"><span data-stu-id="4613f-177">Copy the following code below `// Step 6 - Communication between host and web content`,</span></span>

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

<span data-ttu-id="4613f-178">Drücken Sie F5, um die App zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4613f-178">Press F5 to build and run the app.</span></span> <span data-ttu-id="4613f-179">Es werden nun URLs angezeigt, bevor Sie zu Seiten navigieren.</span><span class="sxs-lookup"><span data-stu-id="4613f-179">It will now show URLs before navigating to pages.</span></span>

![anzeigen-URL](../media/show-url.png)

<span data-ttu-id="4613f-181">Herzlichen Glückwunsch, Sie haben soeben Ihre erste WebView2-App erstellt!</span><span class="sxs-lookup"><span data-stu-id="4613f-181">Congratulations, you've just built your first WebView2 app!</span></span>

## <span data-ttu-id="4613f-182">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="4613f-182">Next Steps</span></span>

<span data-ttu-id="4613f-183">Es gibt viele WebView2-Funktionen, die in dieser exemplarischen Vorgehensweise nicht behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="4613f-183">There are plenty of WebView2 functionalities that are not covered in this walkthrough.</span></span>

<span data-ttu-id="4613f-184">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="4613f-184">To learn more:</span></span>

* <span data-ttu-id="4613f-185">Checkout [-WebView2-API-Beispiel](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) für ein umfassendes Beispiel für WebView2's-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="4613f-185">Checkout [WebView2 API Sample](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) for a comprehensive example of WebView2's capabilities.</span></span>
* <span data-ttu-id="4613f-186">Auschecken [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) einer mit WebView2 erstellten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4613f-186">Checkout [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) an application built using WebView2.</span></span>
* <span data-ttu-id="4613f-187">Detaillierte Informationen zu unserer API finden Sie unter [API-Referenz](../reference/win32/0-9-488-reference-webview2.md) .</span><span class="sxs-lookup"><span data-stu-id="4613f-187">Please explore [API reference](../reference/win32/0-9-488-reference-webview2.md) for detailed information about our API.</span></span>  

## <span data-ttu-id="4613f-188">Kontakt mit dem WebView2-Team</span><span class="sxs-lookup"><span data-stu-id="4613f-188">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="4613f-189">Helfen Sie uns, ein reicheres WebView2-Erlebnis zu schaffen, indem Sie Ihr Feedback austauschen!</span><span class="sxs-lookup"><span data-stu-id="4613f-189">Help us build a richer WebView2 experience by sharing your feedback!</span></span> <span data-ttu-id="4613f-190">Besuchen Sie unser [Feedback-Repo](https://aka.ms/webviewfeedback) , um Funktionsanforderungen oder Fehlerberichte einzureichen oder nach bekannten Problemen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4613f-190">Visit our [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>
