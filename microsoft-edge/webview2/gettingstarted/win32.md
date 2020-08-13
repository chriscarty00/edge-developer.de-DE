---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Erste Schritte mit WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ec5144f911d5bf00f141d1e8e53718154f1cbb24
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926484"
---
# <span data-ttu-id="83674-104">Erste Schritte mit WebView2 (Entwicklervorschau)</span><span class="sxs-lookup"><span data-stu-id="83674-104">Getting started with WebView2 (developer preview)</span></span>  

<span data-ttu-id="83674-105">Der folgende Inhalt führt Sie durch die häufig verwendeten Funktionen von [WebView2 (Developer Preview)][Webview2Index] und stellt einen Ausgangspunkt zum Erstellen Ihrer ersten WebView2-App bereit.</span><span class="sxs-lookup"><span data-stu-id="83674-105">The following content walks you through the commonly used functionalities of [WebView2 (developer preview)][Webview2Index] and provides a starting  point for creating your first WebView2 app.</span></span>  <span data-ttu-id="83674-106">Weitere Informationen zu einzelnen WebView2-APIs finden Sie unter [API-Referenz][Webview2ReferenceWin3209538].</span><span class="sxs-lookup"><span data-stu-id="83674-106">For more information about individual WebView2 APIs, see [API reference][Webview2ReferenceWin3209538].</span></span>  

## <span data-ttu-id="83674-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="83674-107">Prerequisites</span></span>  

*   <span data-ttu-id="83674-108">[Microsoft Edge (Chrom)][MicrosoftedgeinsiderDownload] ist auf unterstützten Betriebssystemen installiert \ (derzeit Windows 10, Windows 8,1 und Windows 7).</span><span class="sxs-lookup"><span data-stu-id="83674-108">[Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="83674-109">Das WebView-Team empfiehlt die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="83674-109">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="83674-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 oder höher mit installierter C++-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="83674-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  

## <span data-ttu-id="83674-111">Schritt 1 – Erstellen einer Win32-App für ein einzelnes Fenster</span><span class="sxs-lookup"><span data-stu-id="83674-111">Step 1 - Create a single window win32 app</span></span>  

<span data-ttu-id="83674-112">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="83674-112">Start with a basic desktop project containing a single main window.</span></span>  <span data-ttu-id="83674-113">Um die exemplarische Vorgehensweise besser zu fokussieren, verwenden Sie den geänderten Beispielcode aus [Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows-Desktop Anwendung (C++)][CppWindowsWalkthroughCreatingDesktopApplication] für Ihre Beispiel-app.</span><span class="sxs-lookup"><span data-stu-id="83674-113">To better focus the walkthrough, you are using modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="83674-114">Informationen zum Herunterladen des geänderten Beispiels und erste Schritte finden Sie unter [WebView2-Beispiele][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="83674-114">To download the modified sample and get started, see [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

<span data-ttu-id="83674-115">Öffnen Sie in Visual Studio `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="83674-115">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  <span data-ttu-id="83674-116">Wenn Sie eine ältere Version von Visual Studio verwenden, zeigen Sie mit der Maus auf das **WebView2GettingStarted** -Projekt, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="83674-116">If you are using an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and select **Properties**.</span></span>  <span data-ttu-id="83674-117">Ändern Sie unter **Konfigurationseigenschaften**  >  **Allgemein**die **Windows SDK-Version** und das **Platform-Toolset** , um das Win10-SDK und das Visual Studio-Toolset \ (vs Toolset \) zu verwenden, das Ihnen zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="83674-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset \(VS toolset\) available to you.</span></span>  

:::image type="complex" source="../media/tool-version.png" alt-text="Tool Version":::
   <span data-ttu-id="83674-119">Tool Version</span><span class="sxs-lookup"><span data-stu-id="83674-119">Tool version</span></span>  
:::image-end:::  

<span data-ttu-id="83674-120">In Visual Studio werden möglicherweise Fehler aufgrund fehlender WebView2-Headerdatei angezeigt, die nach Abschluss von Schritt 2 verschwinden sollten.</span><span class="sxs-lookup"><span data-stu-id="83674-120">Visual Studio may show some errors due to missing WebView2 header file, which should go away after Step 2 is completed.</span></span>  

## <span data-ttu-id="83674-121">Schritt 2 – Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="83674-121">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="83674-122">Fügen Sie das WebView2-SDK in das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="83674-122">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="83674-123">Für die Entwicklervorschau können Sie das Win32-SDK mithilfe von Nuget installieren.</span><span class="sxs-lookup"><span data-stu-id="83674-123">For the developer preview, you may install the Win32 SDK using Nuget.</span></span>  

1.  <span data-ttu-id="83674-124">Zeigen Sie mit der Maus auf das Projekt, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Nuget-Pakete verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="83674-124">Hover on the project, open the contextual menu \(right-click\), and select **Manage Nuget Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Verwalten von Nuget-Paketen":::
       <span data-ttu-id="83674-126">Verwalten von Nuget-Paketen</span><span class="sxs-lookup"><span data-stu-id="83674-126">Manage Nuget packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="83674-127">Installieren Sie die Windows-Implementierungs Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="83674-127">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="83674-128">Geben Sie `Microsoft.Windows.ImplementationLibrary` in der Suchleiste **Microsoft. Windows. ImplementationLibrary** aus den Ergebnissen ein, und wählen Sie im rechten Fenster **Installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="83674-128">Enter `Microsoft.Windows.ImplementationLibrary` in the search bar, select **Microsoft.Windows.ImplementationLibrary** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="83674-129">Nuget downloadet das SDK auf Ihren Computer.</span><span class="sxs-lookup"><span data-stu-id="83674-129">Nuget downloads the SDK to your machine.</span></span>  
        
        > [!NOTE] 
        > <span data-ttu-id="83674-130">Die [Windows-Implementierungs Bibliothek][GithubMicrosoftWilMain] und die [Windows-Runtime-C++-Vorlagenbibliothek][CppCxWrlTemplateLibraryVS2019] sind optional und wurden hinzugefügt, um die Arbeit mit com für das Beispiel zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="83674-130">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and were added to make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows-Implementierungs Bibliothek":::
           <span data-ttu-id="83674-132">Windows-Implementierungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="83674-132">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="83674-133">Installieren Sie das WebView2-SDK.</span><span class="sxs-lookup"><span data-stu-id="83674-133">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="83674-134">Geben Sie `Microsoft.Web.WebView2` in der Suchleiste **Microsoft. Web. WebView2** aus den Ergebnissen ein, und wählen Sie im rechten Fenster **Installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="83674-134">Enter `Microsoft.Web.WebView2` in the search bar, select **Microsoft.Web.WebView2** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="83674-135">Nuget downloadet das SDK auf Ihren Computer.</span><span class="sxs-lookup"><span data-stu-id="83674-135">Nuget downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="Nuget":::
           <span data-ttu-id="83674-137">Nuget</span><span class="sxs-lookup"><span data-stu-id="83674-137">Nuget</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="83674-138">Fügen Sie WebView2-Kopfzeile zu Ihrem Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="83674-138">Add WebView2 header to your project.</span></span>  
    :::row:::
       :::column span="1":::
          <span data-ttu-id="83674-139">Öffnen `HelloWebView.cpp` , kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` nach der letzten `#include` Zeile ein.</span><span class="sxs-lookup"><span data-stu-id="83674-139">Open `HelloWebView.cpp`, copy the following code snippet and paste into `HelloWebView.cpp` after last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="83674-140">Der Abschnitt include sollte ähnlich wie der folgende Codeausschnitt aussehen.</span><span class="sxs-lookup"><span data-stu-id="83674-140">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="83674-141">Sie sind für die Verwendung und Erstellung von WebView2-APIs eingestellt.</span><span class="sxs-lookup"><span data-stu-id="83674-141">You are all set to use and build against the WebView2 API.</span></span>  

### <span data-ttu-id="83674-142">Erstellen der leeren Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="83674-142">Build your empty sample app</span></span>  

<span data-ttu-id="83674-143">Drücken Sie `F5` , um die Beispiel-APP zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="83674-143">Press `F5` to build and run the sample app.</span></span>  <span data-ttu-id="83674-144">Es sollte eine App angezeigt werden, die ein leeres Fenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="83674-144">You should see an app displaying an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Leere App":::
   <span data-ttu-id="83674-146">Leere App</span><span class="sxs-lookup"><span data-stu-id="83674-146">Empty app</span></span>  
:::image-end:::  

## <span data-ttu-id="83674-147">Schritt 3 – Erstellen einer einzelnen WebView im übergeordneten Fenster</span><span class="sxs-lookup"><span data-stu-id="83674-147">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="83674-148">Fügen Sie dem Hauptfenster eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="83674-148">Add a WebView to the main window.</span></span>  <span data-ttu-id="83674-149">Verwenden Sie die `CreateCoreWebView2Environment` Methode zum Einrichten der Umgebung, und suchen Sie den Microsoft Edge \ (Chrom \)-Browser, der das Steuerelement steuert.</span><span class="sxs-lookup"><span data-stu-id="83674-149">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="83674-150">Sie können die Methode auch verwenden, `CreateCoreWebView2EnvironmentWithOptions` Wenn Sie den Browser Speicherort, den Benutzerordner, die Browser Kennzeichnung usw. angeben möchten, anstatt die Standardeinstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="83674-150">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="83674-151">Nach Abschluss der `CreateCoreWebView2Environment` Methode können Sie die `ICoreWebView2Environment::CreateCoreWebView2Controller` Methode innerhalb des `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` Rückrufs ausführen und die Methode ausführen, `ICoreWebView2Controller::get_CoreWebView2` um die zugeordnete WebView abzurufen.</span><span class="sxs-lookup"><span data-stu-id="83674-151">Upon the completion of the `CreateCoreWebView2Environment` method, you are able to run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="83674-152">Legen Sie im Rückruf einige zusätzliche Einstellungen an, ändern Sie die Größe der WebView, um 100% des übergeordneten Fensters zu übernehmen, und navigieren Sie zu Bing.</span><span class="sxs-lookup"><span data-stu-id="83674-152">In the callback, set a few additional settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="83674-153">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` nach der `// <-- WebView2 sample code starts here -->` Notiz und vor der `// <-- WebView2 sample code ends here -->` Notiz ein.</span><span class="sxs-lookup"><span data-stu-id="83674-153">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` note and before the `// <-- WebView2 sample code ends here -->` note.</span></span>  

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


### <span data-ttu-id="83674-154">Erstellen einer Bing-Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="83674-154">Build your Bing sample app</span></span>  

<span data-ttu-id="83674-155">Drücken Sie `F5` , um die APP zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="83674-155">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="83674-156">Nun wird ein WebView-Fenster mit der Bing-Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83674-156">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Bing-Fenster":::
   <span data-ttu-id="83674-158">Bing-Fenster</span><span class="sxs-lookup"><span data-stu-id="83674-158">Bing window</span></span>  
:::image-end:::  

## <span data-ttu-id="83674-159">Schritt 4 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="83674-159">Step 4 - Navigation events</span></span>  

<span data-ttu-id="83674-160">Das WebView-Team hat bereits die Navigation zur URL unter Verwendung der `ICoreWebView2::Navigate` Methode im letzten Schritt abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="83674-160">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="83674-161">Während der Navigation löst WebView eine Abfolge von Ereignissen aus, an die der Host möglicherweise lauscht.</span><span class="sxs-lookup"><span data-stu-id="83674-161">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

<span data-ttu-id="83674-162">Weitere Informationen finden Sie unter [Navigationsereignisse][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="83674-162">For more information, see [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   <span data-ttu-id="83674-164">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="83674-164">Navigation events</span></span>  
:::image-end:::  

<span data-ttu-id="83674-165">In Fehlerfällen können eines oder mehrere der folgenden Ereignisse auftreten, je nachdem, ob die Navigation auf einer Fehlerseite fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="83674-165">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

<span data-ttu-id="83674-166">Im Fall einer HTTP-Umleitung gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="83674-166">In case of an HTTP redirect, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="83674-167">Als Beispiel für die Verwendung der Ereignisse registrieren Sie einen Handler für das `NavigationStarting` Ereignis, um nicht-HTTPS-Anforderungen abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="83674-167">As an example of utilizing the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="83674-168">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in ein `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="83674-168">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="83674-169">Jetzt wird die APP nicht zu allen nicht-HTTPS-Websites navigiert.</span><span class="sxs-lookup"><span data-stu-id="83674-169">Now the app is not navigating to any non-https sites.</span></span>  <span data-ttu-id="83674-170">Sie können einen ähnlichen Mechanismus verwenden, um andere Aufgaben auszuführen, wie etwa das Einschränken der Navigation in ihrer eigenen Domäne.</span><span class="sxs-lookup"><span data-stu-id="83674-170">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <span data-ttu-id="83674-171">Schritt 5 – Skripting</span><span class="sxs-lookup"><span data-stu-id="83674-171">Step 5 - Scripting</span></span>  

<span data-ttu-id="83674-172">Die Host-App kann auch JavaScript in WebView einfügen.</span><span class="sxs-lookup"><span data-stu-id="83674-172">The hosting app may also inject JavaScript into WebView.</span></span>  <span data-ttu-id="83674-173">Sie können mit der Aufgabe WebView beliebiges JavaScript ausführen oder Initialisierungsskripts hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="83674-173">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="83674-174">Hinzugefügte Initialisierungsskripts gelten für alle zukünftigen Dokument-und untergeordneten Frame-Navigationselemente auf oberster Ebene, bis Sie entfernt werden, und werden nach dem Erstellen des globalen Objekts und vor dem Ausführen anderer Skripts ausgeführt, die im HTML-Dokument enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="83674-174">Added initialization scripts apply to all future top level document and child frame navigation until removed, and run after the global object has been created and before any other script included by the HTML document is run.</span></span>  

<span data-ttu-id="83674-175">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in ein `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="83674-175">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="83674-176">WebView sollte das Objekt nun immer fixieren `Object` und das Seiten Dokument einmal zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="83674-176">Now WebView should always freezes the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="83674-177">Die Skript Injektions-APIs \ (und einige andere WebView2-APIs \) sind asynchron, Sie sollten Rückrufe verwenden, wenn Code in einer bestimmten Reihenfolge ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="83674-177">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <span data-ttu-id="83674-178">Schritt 6 – Kommunikation zwischen Host-und Webinhalten</span><span class="sxs-lookup"><span data-stu-id="83674-178">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="83674-179">Der Host und der Webinhalt können über die Methode auch miteinander kommunizieren `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="83674-179">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="83674-180">Die Webinhalte, die in einer WebView ausgeführt werden, können über die Methode an den Host gesendet werden `window.chrome.webview.postMessage` , und die Nachricht wird von jedem registrierten `ICoreWebView2WebMessageReceivedEventHandler` Ereignishandler auf dem Host verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="83674-180">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="83674-181">Ebenso kann der Host den Webinhalt über oder die `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` Methode Nachrichten, die von Handlern abgefangen wird, die vom Listener hinzugefügt werden `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="83674-181">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="83674-182">Mithilfe des Kommunikationsmechanismus können Webinhalte systemeigene Funktionen verwenden, indem Sie Nachrichten übergeben, um den Host zu bitten, systemeigene APIs aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="83674-182">The communication mechanism allows the web content to utilize native capabilities by passing messages to ask the host to call native APIs.</span></span>  

<span data-ttu-id="83674-183">Als Beispiel, um den Mechanismus zu verstehen, treten die folgenden Schritte auf, wenn Sie versuchen, die Dokument-URL in WebView zu drucken.</span><span class="sxs-lookup"><span data-stu-id="83674-183">As an example to understand the mechanism, the following steps occur when you try printing out the document URL in WebView.</span></span>  

1.  <span data-ttu-id="83674-184">Der Host registriert einen Handler, um die empfangene Nachricht zurück an den Webinhalt zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="83674-184">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="83674-185">Der Host injiziert einem Webinhalt ein Skript, das einen Handler registriert, um eine Nachricht vom Host zu drucken.</span><span class="sxs-lookup"><span data-stu-id="83674-185">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="83674-186">Der Host injiziert einem Webinhalt ein Skript, das die URL an den Host sendet.</span><span class="sxs-lookup"><span data-stu-id="83674-186">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="83674-187">Der Handler des Hosts wird ausgelöst und gibt die Nachricht \ (die URL \) an den Webinhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="83674-187">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="83674-188">Der Handler des Webinhalts wird ausgelöst, und die Nachricht wird vom Host \ (der URL \) gedruckt.</span><span class="sxs-lookup"><span data-stu-id="83674-188">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  

<span data-ttu-id="83674-189">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in ein `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="83674-189">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>    

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

### <span data-ttu-id="83674-190">Erstellen einer Beispiel-App für die Show-URL</span><span class="sxs-lookup"><span data-stu-id="83674-190">Build your show URL sample app</span></span>  

<span data-ttu-id="83674-191">Drücken Sie `F5` , um die APP zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="83674-191">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="83674-192">Sie sollten die URL in einem Popupfenster sehen, bevor Sie zu einer Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="83674-192">You should see the URL in a pop-up window prior to navigating to a page.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="URL anzeigen":::
   <span data-ttu-id="83674-194">URL anzeigen</span><span class="sxs-lookup"><span data-stu-id="83674-194">Show url</span></span>  
:::image-end:::  

<span data-ttu-id="83674-195">Herzlichen Glückwunsch, Sie haben soeben Ihre erste WebView2-App erstellt!</span><span class="sxs-lookup"><span data-stu-id="83674-195">Congratulations, you just built your first WebView2 app!</span></span>  

## <span data-ttu-id="83674-196">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="83674-196">Next steps</span></span>  

<span data-ttu-id="83674-197">Viele der WebView2-Funktionen, die auf dieser Seite nicht behandelt werden, im folgenden Abschnitt wurden zusätzliche Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="83674-197">Many of the WebView2 functionalities that are not covered on this page, the following section provided additional resources.</span></span>  

### <span data-ttu-id="83674-198">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83674-198">See also</span></span>  

*   <span data-ttu-id="83674-199">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter Beispiel für die [WebView2-API][GithubMicrosoftedgeWebview2samplesApisample].</span><span class="sxs-lookup"><span data-stu-id="83674-199">For a comprehensive example of WebView2 capabilities, see [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="83674-200">Eine Beispielanwendung, die mit WebView2 erstellt wurde, finden Sie unter [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="83674-200">For a sample application built using WebView2, see [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="83674-201">Ausführliche Informationen zur WebView2-API finden Sie unter [API-Referenz][Webview2ReferenceWin3209538].</span><span class="sxs-lookup"><span data-stu-id="83674-201">For detailed information about the WebView2 API, see [API reference][Webview2ReferenceWin3209538].</span></span>  

## <span data-ttu-id="83674-202">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="83674-202">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft docs"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019 "Windows-Runtime C++-Vorlagenbibliothek (WRL) | Microsoft docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019 "Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows-Desktop Anwendung (C++) | Microsoft docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser-MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "WebView2-API-Beispiel-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Windows-Implementierungs Bibliotheken (Wil) – Microsoft/Wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
