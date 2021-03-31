---
description: Leitfaden für erste Schritte mit WebView2 für Win32-Apps
title: Erste Schritte mit WebView2 für Win32-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 19bc0c5600ebd072ad9a6aa61d2a965e999865ce
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306159"
---
# <span data-ttu-id="d486a-104">Erste Schritte mit WebView2</span><span class="sxs-lookup"><span data-stu-id="d486a-104">Getting started with WebView2</span></span>  

<span data-ttu-id="d486a-105">In diesem Artikel erfahren Sie, wie Sie Ihre erste WebView2-App erstellen, und erfahren Sie mehr über die Wichtigsten Features [von WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]</span><span class="sxs-lookup"><span data-stu-id="d486a-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="d486a-106">Weitere Informationen zu einzelnen WebView2-APIs finden Sie in der [API-Referenz.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="d486a-106">For more information about individual WebView2 APIs, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="d486a-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d486a-107">Prerequisites</span></span>  

<span data-ttu-id="d486a-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="d486a-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="d486a-109">[WebView2 Runtime][Webview2Installer] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen \(derzeit Windows 10, Windows 8.1 und Windows 7\ installiert ist).</span><span class="sxs-lookup"><span data-stu-id="d486a-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d486a-110">Das WebView-Team empfiehlt die Verwendung des Canarykanals, und die mindestens erforderliche Version ist 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="d486a-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="d486a-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 oder höher mit installierter C++-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="d486a-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  
    
## <span data-ttu-id="d486a-112">Schritt 1: Erstellen einer App mit einem Fenster</span><span class="sxs-lookup"><span data-stu-id="d486a-112">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="d486a-113">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="d486a-113">Start with a basic desktop project that contains a single main window.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="d486a-114">Um die exemplarische Vorgehensweise besser zu fokussieren, verwenden Sie geänderten Beispielcode aus ["Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app".</span><span class="sxs-lookup"><span data-stu-id="d486a-114">To better focus the walkthrough, use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="d486a-115">Um das geänderte Beispiel herunterzuladen und zu beginnen, navigieren Sie zu [WebView2-Beispiele.][GithubMicrosoftedgeWebview2samplesGettingStartedGuide]</span><span class="sxs-lookup"><span data-stu-id="d486a-115">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

1.  <span data-ttu-id="d486a-116">Öffnen Visual Studio in der Datei `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="d486a-116">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  
    <span data-ttu-id="d486a-117">Wenn Sie eine ältere Version von Visual Studio verwenden, zeigen Sie auf das **WebView2GettingStarted-Projekt,** öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="d486a-117">If you use an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and choose **Properties**.</span></span>  <span data-ttu-id="d486a-118">Ändern **Sie unter**"Allgemeine Konfigurationseigenschaften" die Windows  >   **SDK-Version** und das **Plattformtoolset** so, dass sie das Win10 SDK und Visual Studio toolset verwenden, das Ihnen zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="d486a-118">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset available to you.</span></span>  

:::image type="complex" source="../media/tool-version.png" alt-text="Toolversion" lightbox="../media/tool-version.png":::
   <span data-ttu-id="d486a-120">Toolversion</span><span class="sxs-lookup"><span data-stu-id="d486a-120">Tool version</span></span>  
:::image-end:::  

<span data-ttu-id="d486a-121">Visual Studio werden möglicherweise Fehler angezeigt, da in Ihrem Projekt die WebView2-Headerdatei fehlt.</span><span class="sxs-lookup"><span data-stu-id="d486a-121">Visual Studio may display errors, because your project is missing the WebView2 header file.</span></span>  <span data-ttu-id="d486a-122">Die Fehler sollten nach Schritt [2 behoben werden.](#step-2---install-webview2-sdk)</span><span class="sxs-lookup"><span data-stu-id="d486a-122">The errors should be fixed after [Step 2](#step-2---install-webview2-sdk).</span></span>  

## <span data-ttu-id="d486a-123">Schritt 2: Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="d486a-123">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="d486a-124">Fügen Sie dem Projekt das WebView2 SDK hinzu.</span><span class="sxs-lookup"><span data-stu-id="d486a-124">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="d486a-125">Verwenden Sie NuGet, um das Win32 SDK zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d486a-125">Use NuGet to install the Win32 SDK.</span></span>  

1.  <span data-ttu-id="d486a-126">Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **"NuGet-Pakete verwalten" aus.**</span><span class="sxs-lookup"><span data-stu-id="d486a-126">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="NuGet-Pakete verwalten" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="d486a-128">NuGet-Pakete verwalten</span><span class="sxs-lookup"><span data-stu-id="d486a-128">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d486a-129">Installieren Sie die Windows-Implementierungsbibliothek.</span><span class="sxs-lookup"><span data-stu-id="d486a-129">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="d486a-130">Geben Sie in der Suchleiste > `Microsoft.Windows.ImplementationLibrary` **Microsoft.Windows.ImplementationLibrary aus.**</span><span class="sxs-lookup"><span data-stu-id="d486a-130">In the search bar, type `Microsoft.Windows.ImplementationLibrary` > choose **Microsoft.Windows.ImplementationLibrary**.</span></span>  
    1.  <span data-ttu-id="d486a-131">Wählen Sie im rechten Fenster "Installieren" **aus.**</span><span class="sxs-lookup"><span data-stu-id="d486a-131">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="d486a-132">NuGet lädt die Bibliothek auf Ihren Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="d486a-132">NuGet downloads the library to your machine.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="d486a-133">Die [#A0 und][GithubMicrosoftWilMain] [die C++-Vorlagenbibliothek][CppCxWrlTemplateLibraryVS2019] für #A1 sind optional und erleichtern das Arbeiten mit COM für das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d486a-133">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows-Implementierungsbibliothek" lightbox="../media/wil.png":::
           <span data-ttu-id="d486a-135">Windows-Implementierungsbibliothek</span><span class="sxs-lookup"><span data-stu-id="d486a-135">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="d486a-136">Installieren Sie das WebView2 SDK.</span><span class="sxs-lookup"><span data-stu-id="d486a-136">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="d486a-137">Geben Sie in der Suchleiste > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2 aus.**</span><span class="sxs-lookup"><span data-stu-id="d486a-137">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    1.  <span data-ttu-id="d486a-138">Wählen Sie im rechten Fenster "Installieren" **aus.**</span><span class="sxs-lookup"><span data-stu-id="d486a-138">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="d486a-139">NuGet lädt das SDK auf Ihren Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="d486a-139">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Paket-Manager" lightbox="../media/nuget.png":::
           <span data-ttu-id="d486a-141">NuGet Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="d486a-141">NuGet Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="d486a-142">Fügen Sie Ihrem Projekt die WebView2-Kopfzeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="d486a-142">Add WebView2 header to your project.</span></span>  
    :::row:::
       :::column span="1":::
          <span data-ttu-id="d486a-143">Kopieren Sie `HelloWebView.cpp` in der Datei den folgenden Codeausschnitt, und fügen Sie ihn nach der letzten Zeile `#include` ein.</span><span class="sxs-lookup"><span data-stu-id="d486a-143">In the `HelloWebView.cpp` file, copy the following code snippet and paste it after the last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="d486a-144">Der Abschnitt "Include" sollte ähnlich wie der folgende Codeausschnitt aussehen.</span><span class="sxs-lookup"><span data-stu-id="d486a-144">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="d486a-145">Bereit zur Verwendung und Erstellung für die WebView2-API.</span><span class="sxs-lookup"><span data-stu-id="d486a-145">Ready to use and build against the WebView2 API.</span></span>  

### <span data-ttu-id="d486a-146">Erstellen Einer leeren Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="d486a-146">Build your empty sample app</span></span>  

<span data-ttu-id="d486a-147">Wählen Sie zum Erstellen und Ausführen der Beispiel-App die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="d486a-147">To build and run the sample app, select `F5`.</span></span>  <span data-ttu-id="d486a-148">Ihre App zeigt ein leeres Fenster an.</span><span class="sxs-lookup"><span data-stu-id="d486a-148">Your app displays an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Leere App" lightbox="../media/empty-app.png":::
   <span data-ttu-id="d486a-150">Leere App</span><span class="sxs-lookup"><span data-stu-id="d486a-150">Empty app</span></span>  
:::image-end:::  

## <span data-ttu-id="d486a-151">Schritt 3: Erstellen einer einzelnen WebView im übergeordneten Fenster</span><span class="sxs-lookup"><span data-stu-id="d486a-151">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="d486a-152">Fügen Sie dem Hauptfenster eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="d486a-152">Add a WebView to the main window.</span></span>  

 <span data-ttu-id="d486a-153">Verwenden Sie die Methode, um die Umgebung einrichten und `CreateCoreWebView2Environment` den Microsoft Edge \(Chromium\)-Browser zu suchen, der das Steuerelement unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d486a-153">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="d486a-154">Sie können die Methode auch verwenden, wenn Sie browserspeicherort, Benutzerordner, Browserflags und so weiter angeben möchten, anstatt die `CreateCoreWebView2EnvironmentWithOptions` Standardeinstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d486a-154">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="d486a-155">Führen Sie nach Abschluss der Methode die Methode innerhalb des Rückrufs aus, und führen Sie die Methode aus, um `CreateCoreWebView2Environment` `ICoreWebView2Environment::CreateCoreWebView2Controller` die `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` zugeordnete WebView zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d486a-155">Upon the completion of the `CreateCoreWebView2Environment` method, run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="d486a-156">Legen Sie im Rückruf ein paar weitere Einstellungen, ändern Sie die Größe der WebView, um 100 % des übergeordneten Fensters zu übernehmen, und navigieren Sie zu Bing.</span><span class="sxs-lookup"><span data-stu-id="d486a-156">In the callback, set a few more settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="d486a-157">Kopieren Sie den folgenden Codeausschnitt, und fügen `HelloWebView.cpp` Sie ihn nach dem Kommentar und vor dem Kommentar `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` ein.</span><span class="sxs-lookup"><span data-stu-id="d486a-157">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` comment and before the `// <-- WebView2 sample code ends here -->` comment.</span></span>  

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
                // The demo step is redundant since the values are the default settings
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

### <span data-ttu-id="d486a-158">Erstellen Ihrer Bing-Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="d486a-158">Build your Bing sample app</span></span>  

<span data-ttu-id="d486a-159">Wählen Sie zum Erstellen und Ausführen der App die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="d486a-159">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="d486a-160">Jetzt haben Sie ein WebView-Fenster, in dem die Seite Bing angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d486a-160">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Fenster "Bing"" lightbox="../media/bing-window.png":::
   <span data-ttu-id="d486a-162">Fenster "Bing"</span><span class="sxs-lookup"><span data-stu-id="d486a-162">Bing window</span></span>  
:::image-end:::  

## <span data-ttu-id="d486a-163">Schritt 4: Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="d486a-163">Step 4 - Navigation events</span></span>  

<span data-ttu-id="d486a-164">Das WebView-Team hat bereits das Navigieren zu URL mithilfe der `ICoreWebView2::Navigate` Methode im letzten Schritt behandelt.</span><span class="sxs-lookup"><span data-stu-id="d486a-164">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="d486a-165">Während der Navigation wird von WebView eine Abfolge von Ereignissen ausgeführt, auf die der Host möglicherweise lauscht.</span><span class="sxs-lookup"><span data-stu-id="d486a-165">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

<span data-ttu-id="d486a-166">Navigieren Sie zu [Navigationsereignissen, um weitere Informationen zu erhalten.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="d486a-166">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="d486a-168">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="d486a-168">Navigation events</span></span>  
:::image-end:::  

<span data-ttu-id="d486a-169">In Fehlerfällen kann eines oder mehrere der folgenden Ereignisse auftreten, je nachdem, ob die Navigation zu einer Fehlerwebseite fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d486a-169">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

> [!NOTE]
> <span data-ttu-id="d486a-170">Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="d486a-170">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="d486a-171">Registrieren Sie als Beispiel für die Verwendung der Ereignisse einen Handler für das Ereignis, um `NavigationStarting` alle Nicht-https-Anforderungen abbricht.</span><span class="sxs-lookup"><span data-stu-id="d486a-171">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="d486a-172">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` ein.</span><span class="sxs-lookup"><span data-stu-id="d486a-172">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="d486a-173">Jetzt navigiert die App nicht zu nicht https-Websites.</span><span class="sxs-lookup"><span data-stu-id="d486a-173">Now the app does not navigate to any non-https sites.</span></span>  <span data-ttu-id="d486a-174">Sie können einen ähnlichen Mechanismus verwenden, um andere Aufgaben auszuführen, z. B. das Einschränken der Navigation auf Ihre eigene Domäne.</span><span class="sxs-lookup"><span data-stu-id="d486a-174">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <span data-ttu-id="d486a-175">Schritt 5: Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="d486a-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="d486a-176">Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.</span><span class="sxs-lookup"><span data-stu-id="d486a-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="d486a-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span><span class="sxs-lookup"><span data-stu-id="d486a-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="d486a-178">Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d486a-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="d486a-179">Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d486a-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="d486a-180">Führen Sie es nach der Erstellung des globalen Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="d486a-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="d486a-181">Führen Sie es aus, bevor ein anderes Im HTML-Dokument enthaltenes Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d486a-181">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="d486a-182">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` ein.</span><span class="sxs-lookup"><span data-stu-id="d486a-182">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="d486a-183">Jetzt sollte WebView das Objekt immer fixieren `Object` und das Seitendokument einmal zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d486a-183">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="d486a-184">Die Skripteinführungs-APIs \(und einige andere WebView2-APIs\) sind asynchron. Sie sollten Rückrufe verwenden, wenn Code in einer bestimmten Reihenfolge ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d486a-184">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <span data-ttu-id="d486a-185">Schritt 6: Kommunikation zwischen Host- und Webinhalt</span><span class="sxs-lookup"><span data-stu-id="d486a-185">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="d486a-186">Der Host und der Webinhalt können auch über die Methode miteinander `postMessage` kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d486a-186">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="d486a-187">Der Webinhalt, der in einer WebView ausgeführt wird, kann über die Methode an den Host gesendet werden, und die Nachricht wird von einem registrierten Ereignishandler auf dem `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` Host verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d486a-187">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="d486a-188">Ebenso kann der Host den Webinhalt über oder die Methode senden, die von Handlern erfasst wird, die `ICoreWebView2::PostWebMessageAsString` vom Listener hinzugefügt `ICoreWebView2::PostWebMessageAsJSON` `window.chrome.webview.addEventListener` wurden.</span><span class="sxs-lookup"><span data-stu-id="d486a-188">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="d486a-189">Der Kommunikationsmechanismus ermöglicht es den Webinhalten, systemeigene Funktionen zu verwenden, indem Nachrichten übergeben werden, um den Host zur Ausführung systemeigener APIs zu bitten.</span><span class="sxs-lookup"><span data-stu-id="d486a-189">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="d486a-190">Um den Mechanismus zu verstehen, führen Sie die folgenden Schritte aus, wenn Sie versuchen, die Dokument-URL in WebView ausausgabe.</span><span class="sxs-lookup"><span data-stu-id="d486a-190">As an example to understand the mechanism, the following steps occur when you try to output the document URL in WebView.</span></span>  

1.  <span data-ttu-id="d486a-191">Der Host registriert einen Handler, um empfangene Nachrichten zurück an den Webinhalt zurück zu senden.</span><span class="sxs-lookup"><span data-stu-id="d486a-191">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="d486a-192">Der Host injiziert ein Skript in den Webinhalt, das einen Handler zum Drucken von Nachrichten vom Host registriert.</span><span class="sxs-lookup"><span data-stu-id="d486a-192">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="d486a-193">Der Host injiziert ein Skript in den Webinhalt, der die URL auf dem Host veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d486a-193">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="d486a-194">Der Handler des Hosts wird ausgelöst und gibt die Nachricht \(die URL\) an den Webinhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="d486a-194">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="d486a-195">Der Handler des Webinhalts wird ausgelöst und druckt die Nachricht vom Host \(die URL\)</span><span class="sxs-lookup"><span data-stu-id="d486a-195">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  

<span data-ttu-id="d486a-196">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` ein.</span><span class="sxs-lookup"><span data-stu-id="d486a-196">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

### <span data-ttu-id="d486a-197">Erstellen Der Beispiel-App für die Anzeige-URL</span><span class="sxs-lookup"><span data-stu-id="d486a-197">Build your display URL sample app</span></span>  

<span data-ttu-id="d486a-198">Wählen Sie zum Erstellen und Ausführen der App die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="d486a-198">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="d486a-199">Die URL wird in einem Popupfenster angezeigt, bevor sie zu einer Webseite navigiert.</span><span class="sxs-lookup"><span data-stu-id="d486a-199">The URL appears in a pop-up window before navigating to a webpage.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Anzeige-URL" lightbox="../media/show-url.png":::
   <span data-ttu-id="d486a-201">Anzeige-URL</span><span class="sxs-lookup"><span data-stu-id="d486a-201">Display url</span></span>  
:::image-end:::  

<span data-ttu-id="d486a-202">Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="d486a-202">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="d486a-203">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d486a-203">Next steps</span></span>  

<span data-ttu-id="d486a-204">Viele der WebView2-Funktionen werden in diesem Artikel nicht behandelt, der folgende Abschnitt enthält weitere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="d486a-204">Many of the WebView2 functionalities are not covered on this article, the following section provides more resources.</span></span>  

### <span data-ttu-id="d486a-205">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d486a-205">See also</span></span>  

*   <span data-ttu-id="d486a-206">Ein umfassendes Beispiel der WebView2-Funktionen finden Sie im [WebView2-API-Beispiel.][GithubMicrosoftedgeWebview2samplesApisample]</span><span class="sxs-lookup"><span data-stu-id="d486a-206">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="d486a-207">For a sample app built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="d486a-207">For a sample app built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="d486a-208">Ausführliche Informationen zur WebView2-API finden Sie in der [API-Referenz.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="d486a-208">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="d486a-209">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="d486a-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2-| Microsoft Edge Developer"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++-Referenz | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Windows Runtime C++ Template Library (WRL) | Microsoft Docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Walkthrough: Create a traditional Windows Desktop application (C++) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser – MicrosoftEdge/WebView2Browser-| GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback-| GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples-| GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Windows Implementation Libraries (WIL) – microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer"  
