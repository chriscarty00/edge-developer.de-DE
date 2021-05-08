---
description: Erste Schritte mit WebView2 für Win32-Apps
title: Erste Schritte mit WebView2 für Win32-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 073a92bf10a7ead85ac91bff54b5fc405c7d577c
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535996"
---
# <a name="get-started-with-webview2"></a><span data-ttu-id="edffe-104">Erste Schritte mit WebView2</span><span class="sxs-lookup"><span data-stu-id="edffe-104">Get started with WebView2</span></span>  

<span data-ttu-id="edffe-105">Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="edffe-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="edffe-106">Weitere Informationen zu einzelnen WebView2-APIs finden Sie unter [API-Referenz][Webview2ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="edffe-106">For more information about individual WebView2 APIs, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="edffe-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="edffe-107">Prerequisites</span></span>  

<span data-ttu-id="edffe-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="edffe-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="edffe-109">[WebView2 Runtime][Webview2Installer] oder Microsoft Edge [(Chromium)][MicrosoftedgeinsiderDownload] nicht stabile Kanal, der auf dem unterstützten Betriebssystem \(derzeit Windows 10, Windows 8.1 und Windows 7\ installiert ist).</span><span class="sxs-lookup"><span data-stu-id="edffe-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="edffe-110">Das WebView-Team empfiehlt die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="edffe-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="edffe-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 oder höher mit installierter C++-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="edffe-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  
    
## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="edffe-112">Schritt 1 : Erstellen einer App mit einem Fenster</span><span class="sxs-lookup"><span data-stu-id="edffe-112">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="edffe-113">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="edffe-113">Start with a basic desktop project that contains a single main window.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="edffe-114">Um die exemplarische Vorgehensweise besser zu fokussieren, verwenden Sie geänderten Beispielcode aus [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] für Ihre Beispiel-App.</span><span class="sxs-lookup"><span data-stu-id="edffe-114">To better focus the walkthrough, use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="edffe-115">Um das geänderte Beispiel herunterzuladen und zu beginnen, navigieren Sie zu [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="edffe-115">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

1.  <span data-ttu-id="edffe-116">Öffnen Visual Studio in der Datei `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="edffe-116">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  
    <span data-ttu-id="edffe-117">Wenn Sie eine ältere Version von Visual Studio verwenden, zeigen Sie auf das **WebView2GettingStarted-Projekt,** öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Eigenschaften aus.**</span><span class="sxs-lookup"><span data-stu-id="edffe-117">If you use an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and choose **Properties**.</span></span>  <span data-ttu-id="edffe-118">Ändern **Sie unter**Konfigurationseigenschaften allgemein Windows SDK Version und Platform  >  \*\*\*\* **Toolset,** um das Win10 SDK und Visual Studio toolset zu verwenden, das Ihnen zur Verfügung steht. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="edffe-118">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset available to you.</span></span>  
    
:::image type="complex" source="../media/tool-version.png" alt-text="Toolversion" lightbox="../media/tool-version.png":::
   <span data-ttu-id="edffe-120">Toolversion</span><span class="sxs-lookup"><span data-stu-id="edffe-120">Tool version</span></span>  
:::image-end:::      

<span data-ttu-id="edffe-121">Visual Studio können Fehler angezeigt werden, da in Ihrem Projekt die WebView2-Headerdatei fehlt.</span><span class="sxs-lookup"><span data-stu-id="edffe-121">Visual Studio may display errors, because your project is missing the WebView2 header file.</span></span>  <span data-ttu-id="edffe-122">Die Fehler sollten nach [Schritt 2 behoben werden.](#step-2---install-webview2-sdk)</span><span class="sxs-lookup"><span data-stu-id="edffe-122">The errors should be fixed after [Step 2](#step-2---install-webview2-sdk).</span></span>  

## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="edffe-123">Schritt 2 : Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="edffe-123">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="edffe-124">Fügen Sie dem Projekt das WebView2 SDK hinzu.</span><span class="sxs-lookup"><span data-stu-id="edffe-124">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="edffe-125">Verwenden NuGet, um das Win32 SDK zu installieren.</span><span class="sxs-lookup"><span data-stu-id="edffe-125">Use NuGet to install the Win32 SDK.</span></span>  

1.  <span data-ttu-id="edffe-126">Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Verwalten NuGet Pakete aus.**</span><span class="sxs-lookup"><span data-stu-id="edffe-126">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="NuGet-Pakete verwalten" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="edffe-128">NuGet-Pakete verwalten</span><span class="sxs-lookup"><span data-stu-id="edffe-128">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="edffe-129">Installieren Sie Windows Implementierungsbibliothek.</span><span class="sxs-lookup"><span data-stu-id="edffe-129">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="edffe-130">Geben Sie in der Suchleiste `Microsoft.Windows.ImplementationLibrary` > **Microsoft.Windows. ImplementationLibrary**.</span><span class="sxs-lookup"><span data-stu-id="edffe-130">In the search bar, type `Microsoft.Windows.ImplementationLibrary` > choose **Microsoft.Windows.ImplementationLibrary**.</span></span>  
    1.  <span data-ttu-id="edffe-131">Wählen Sie im rechten Fenster Installieren **aus.**</span><span class="sxs-lookup"><span data-stu-id="edffe-131">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="edffe-132">NuGet lädt die Bibliothek auf Ihren Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="edffe-132">NuGet downloads the library to your machine.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="edffe-133">Die [Windows Implementierungsbibliothek][GithubMicrosoftWilMain] [und Windows Runtime C++-Vorlagenbibliothek][CppCxWrlTemplateLibraryVS2019] sind optional und erleichtern das Arbeiten mit COM für das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="edffe-133">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows Implementierungsbibliothek" lightbox="../media/wil.png":::
           <span data-ttu-id="edffe-135">Windows Implementierungsbibliothek</span><span class="sxs-lookup"><span data-stu-id="edffe-135">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="edffe-136">Installieren Sie das WebView2 SDK.</span><span class="sxs-lookup"><span data-stu-id="edffe-136">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="edffe-137">Geben Sie in der Suchleiste `Microsoft.Web.WebView2` > Wählen Sie **Microsoft.Web.WebView2 aus.**</span><span class="sxs-lookup"><span data-stu-id="edffe-137">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    1.  <span data-ttu-id="edffe-138">Wählen Sie im rechten Fenster Installieren **aus.**</span><span class="sxs-lookup"><span data-stu-id="edffe-138">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="edffe-139">NuGet das SDK auf Ihren Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="edffe-139">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Paket-Manager" lightbox="../media/nuget.png":::
           <span data-ttu-id="edffe-141">NuGet Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="edffe-141">NuGet Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="edffe-142">Fügen Sie Ihrem Projekt WebView2-Header hinzu.</span><span class="sxs-lookup"><span data-stu-id="edffe-142">Add WebView2 header to your project.</span></span>  
    
    :::row:::
       :::column span="1":::
          <span data-ttu-id="edffe-143">Kopieren Sie `HelloWebView.cpp` in der Datei den folgenden Codeausschnitt, und fügen Sie ihn nach der letzten Zeile `#include` ein.</span><span class="sxs-lookup"><span data-stu-id="edffe-143">In the `HelloWebView.cpp` file, copy the following code snippet and paste it after the last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="edffe-144">Der Include-Abschnitt sollte dem folgenden Codeausschnitt ähnlich aussehen.</span><span class="sxs-lookup"><span data-stu-id="edffe-144">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="edffe-145">Bereit für die Verwendung und Erstellung für die WebView2-API.</span><span class="sxs-lookup"><span data-stu-id="edffe-145">Ready to use and build against the WebView2 API.</span></span>  

### <a name="build-your-empty-sample-app"></a><span data-ttu-id="edffe-146">Erstellen Einer leeren Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="edffe-146">Build your empty sample app</span></span>  

<span data-ttu-id="edffe-147">Wählen Sie aus, um die Beispiel-App zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="edffe-147">To build and run the sample app, select `F5`.</span></span>  <span data-ttu-id="edffe-148">Ihre App zeigt ein leeres Fenster an.</span><span class="sxs-lookup"><span data-stu-id="edffe-148">Your app displays an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Leere App" lightbox="../media/empty-app.png":::
   <span data-ttu-id="edffe-150">Leere App</span><span class="sxs-lookup"><span data-stu-id="edffe-150">Empty app</span></span>  
:::image-end:::    

## <a name="step-3---create-a-single-webview-within-the-parent-window"></a><span data-ttu-id="edffe-151">Schritt 3: Erstellen einer einzelnen WebView im übergeordneten Fenster</span><span class="sxs-lookup"><span data-stu-id="edffe-151">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="edffe-152">Fügen Sie dem Hauptfenster eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="edffe-152">Add a WebView to the main window.</span></span>  

<span data-ttu-id="edffe-153">Verwenden Sie die -Methode, um die Umgebung zu einrichten und den Microsoft Edge \(Chromium\)-Browser zu finden, der das `CreateCoreWebView2Environment` Steuerelement unterstützt.</span><span class="sxs-lookup"><span data-stu-id="edffe-153">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="edffe-154">Sie können die Methode auch verwenden, wenn Sie browser location, user folder, browser flags und so weiter angeben möchten, anstatt die `CreateCoreWebView2EnvironmentWithOptions` Standardeinstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="edffe-154">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="edffe-155">Führen Sie nach Abschluss der Methode die Methode im Rückruf aus, und führen Sie die `CreateCoreWebView2Environment` -Methode aus, `ICoreWebView2Environment::CreateCoreWebView2Controller` um die `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` zugeordnete WebView zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="edffe-155">Upon the completion of the `CreateCoreWebView2Environment` method, run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="edffe-156">Legen Sie im Rückruf einige weitere Einstellungen ein, ändern Sie die Größe der WebView auf 100 % des übergeordneten Fensters, und navigieren Sie zu Bing.</span><span class="sxs-lookup"><span data-stu-id="edffe-156">In the callback, set a few more settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="edffe-157">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` nach dem Kommentar und vor dem Kommentar `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` ein.</span><span class="sxs-lookup"><span data-stu-id="edffe-157">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` comment and before the `// <-- WebView2 sample code ends here -->` comment.</span></span>  

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

### <a name="build-your-bing-sample-app"></a><span data-ttu-id="edffe-158">Erstellen Bing Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="edffe-158">Build your Bing sample app</span></span>  

<span data-ttu-id="edffe-159">Wählen Sie zum Erstellen und Ausführen der App `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="edffe-159">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="edffe-160">Jetzt haben Sie ein WebView-Fenster, in dem die Bing angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="edffe-160">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Bing fenster" lightbox="../media/bing-window.png":::
   <span data-ttu-id="edffe-162">Bing fenster</span><span class="sxs-lookup"><span data-stu-id="edffe-162">Bing window</span></span>  
:::image-end:::    

## <a name="step-4---navigation-events"></a><span data-ttu-id="edffe-163">Schritt 4 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="edffe-163">Step 4 - Navigation events</span></span>  

<span data-ttu-id="edffe-164">Das WebView-Team hat bereits im letzten Schritt die Navigation zu URL mithilfe der `ICoreWebView2::Navigate` -Methode behandelt.</span><span class="sxs-lookup"><span data-stu-id="edffe-164">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="edffe-165">Während der Navigation gibt WebView eine Abfolge von Ereignissen aus, auf die der Host lauschen kann.</span><span class="sxs-lookup"><span data-stu-id="edffe-165">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   
    
<span data-ttu-id="edffe-166">Weitere Informationen finden Sie unter [Navigationsereignisse][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="edffe-166">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="edffe-168">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="edffe-168">Navigation events</span></span>  
:::image-end:::    

<span data-ttu-id="edffe-169">In Fehlerfällen kann eines oder mehrere der folgenden Ereignisse auftreten, je nachdem, ob die Navigation zu einer Fehlerwebseite fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="edffe-169">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`
    
> [!NOTE]
> <span data-ttu-id="edffe-170">Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="edffe-170">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="edffe-171">Registrieren Sie als Beispiel für die Verwendung der Ereignisse einen Handler für das Ereignis, `NavigationStarting` um alle Nicht-https-Anforderungen abbricht.</span><span class="sxs-lookup"><span data-stu-id="edffe-171">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="edffe-172">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` ein.</span><span class="sxs-lookup"><span data-stu-id="edffe-172">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="edffe-173">Jetzt navigiert die App nicht zu nicht https-Websites.</span><span class="sxs-lookup"><span data-stu-id="edffe-173">Now the app does not navigate to any non-https sites.</span></span>  <span data-ttu-id="edffe-174">Sie können einen ähnlichen Mechanismus verwenden, um andere Aufgaben auszuführen, z. B. die Beschränkung der Navigation auf innerhalb Ihrer eigenen Domäne.</span><span class="sxs-lookup"><span data-stu-id="edffe-174">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <a name="step-5---scripting"></a><span data-ttu-id="edffe-175">Schritt 5 – Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="edffe-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="edffe-176">Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.</span><span class="sxs-lookup"><span data-stu-id="edffe-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="edffe-177">Sie können WebView zum Ausführen beliebiger JavaScript- oder Initialisierungsskripts aufgaben.</span><span class="sxs-lookup"><span data-stu-id="edffe-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="edffe-178">Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="edffe-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="edffe-179">Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="edffe-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="edffe-180">Führen Sie es nach der Erstellung des globalen Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="edffe-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="edffe-181">Führen Sie es aus, bevor ein anderes Skript ausgeführt wird, das im HTML-Dokument enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="edffe-181">Run it before any other script included in the HTML document is run.</span></span>  
    
<span data-ttu-id="edffe-182">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` ein.</span><span class="sxs-lookup"><span data-stu-id="edffe-182">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="edffe-183">Jetzt sollte WebView das Objekt immer fixieren `Object` und das Seitendokument einmal zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="edffe-183">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="edffe-184">Die Skriptinjektions-APIs \(und einige andere WebView2-APIs\) sind asynchron. Sie sollten Rückrufe verwenden, wenn Code in einer bestimmten Reihenfolge ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="edffe-184">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <a name="step-6---communication-between-host-and-web-content"></a><span data-ttu-id="edffe-185">Schritt 6 – Kommunikation zwischen Host- und Webinhalten</span><span class="sxs-lookup"><span data-stu-id="edffe-185">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="edffe-186">Der Host und der Webinhalt können auch über die Methode miteinander `postMessage` kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="edffe-186">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="edffe-187">Der in einer WebView ausgeführte Webinhalt kann über die -Methode an den Host gesendet werden, und die Nachricht wird von allen registrierten Ereignishandlern auf `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` dem Host verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="edffe-187">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="edffe-188">Ebenso kann der Host den Webinhalt über oder die -Methode senden, die von Handlern erfasst wird, die vom `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` Listener hinzugefügt `window.chrome.webview.addEventListener` wurden.</span><span class="sxs-lookup"><span data-stu-id="edffe-188">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="edffe-189">Der Kommunikationsmechanismus ermöglicht es dem Webinhalt, systemeigene Funktionen zu verwenden, indem Nachrichten übergeben werden, um den Host zum Ausführen systemeigener APIs zu bitten.</span><span class="sxs-lookup"><span data-stu-id="edffe-189">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="edffe-190">Um den Mechanismus zu verstehen, führen Sie die folgenden Schritte aus, wenn Sie versuchen, die Dokument-URL in WebView auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="edffe-190">As an example to understand the mechanism, the following steps occur when you try to output the document URL in WebView.</span></span>  

1.  <span data-ttu-id="edffe-191">Der Host registriert einen Handler, um empfangene Nachrichten an den Webinhalt zurückzukehren</span><span class="sxs-lookup"><span data-stu-id="edffe-191">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="edffe-192">Der Host injiziert ein Skript in den Webinhalt, der einen Handler zum Drucken von Nachrichten vom Host registriert</span><span class="sxs-lookup"><span data-stu-id="edffe-192">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="edffe-193">Der Host injiziert ein Skript in den Webinhalt, der die URL auf dem Host veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="edffe-193">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="edffe-194">Der Handler des Hosts wird ausgelöst und gibt die Nachricht \(die URL\) an den Webinhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="edffe-194">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="edffe-195">Der Handler des Webinhalts wird ausgelöst und druckt die Nachricht vom Host \(die URL\)</span><span class="sxs-lookup"><span data-stu-id="edffe-195">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  
    
<span data-ttu-id="edffe-196">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` ein.</span><span class="sxs-lookup"><span data-stu-id="edffe-196">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

### <a name="build-your-display-url-sample-app"></a><span data-ttu-id="edffe-197">Erstellen Der Beispiel-App für die Anzeige-URL</span><span class="sxs-lookup"><span data-stu-id="edffe-197">Build your display URL sample app</span></span>  

<span data-ttu-id="edffe-198">Wählen Sie zum Erstellen und Ausführen der App `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="edffe-198">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="edffe-199">Die URL wird in einem Popupfenster angezeigt, bevor sie zu einer Webseite navigiert.</span><span class="sxs-lookup"><span data-stu-id="edffe-199">The URL appears in a pop-up window before navigating to a webpage.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Anzeige-URL" lightbox="../media/show-url.png":::
   <span data-ttu-id="edffe-201">Anzeige-URL</span><span class="sxs-lookup"><span data-stu-id="edffe-201">Display url</span></span>  
:::image-end:::    

<span data-ttu-id="edffe-202">Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="edffe-202">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="edffe-203">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="edffe-203">Next steps</span></span>  

<span data-ttu-id="edffe-204">Weitere WebView2-Funktionen, die in diesem Artikel nicht behandelt werden, finden Sie in den folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="edffe-204">For additional WebView2 functionality that isn't covered in this article, review the following resources.</span></span>  

*   <span data-ttu-id="edffe-205">Weitere Informationen zum Erstellen von WebView2-Anwendungen finden Sie unter Bewährte Methoden für [die WebView2-Entwicklung.][WV2BestPractices]</span><span class="sxs-lookup"><span data-stu-id="edffe-205">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="edffe-206">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2-API-Beispiel][GithubMicrosoftedgeWebview2samplesApisample].</span><span class="sxs-lookup"><span data-stu-id="edffe-206">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="edffe-207">Navigieren Sie zu [WebView2Browser,][GithubMicrosoftedgeWebview2browser]um eine mit WebView2 erstellte Beispiel-App zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="edffe-207">For a sample app built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="edffe-208">Ausführliche Informationen zur WebView2-API finden Sie unter [API-Referenz][Webview2ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="edffe-208">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="edffe-209">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="edffe-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Bewährte Methoden für die WebView2-| Microsoft Docs"  
[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-| Microsoft Edge Entwickler"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++-Referenz | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Windows Runtime C++ Template Library (WRL) | Microsoft Docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Walkthrough: Create a traditional Windows Desktop application (C++) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser – MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Windows Implementierungsbibliotheken (WIL) – microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer"  
