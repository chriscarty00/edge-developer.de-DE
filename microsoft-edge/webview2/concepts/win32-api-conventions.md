---
description: Win32 C++ WebView2-API-Konventionen
title: Win32 C++ WebView2-API-Konventionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: b47e53a4846d4bb662ae108c6445a6c2a615722a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470858"
---
# <a name="win32-c-webview2-api-conventions"></a><span data-ttu-id="abb52-104">Win32 C++ WebView2-API-Konventionen</span><span class="sxs-lookup"><span data-stu-id="abb52-104">Win32 C++ WebView2 API conventions</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="abb52-105">Unterstützte Plattformen:</span><span class="sxs-lookup"><span data-stu-id="abb52-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="abb52-106">Win32</span><span class="sxs-lookup"><span data-stu-id="abb52-106">Win32</span></span>
   :::column-end:::
:::row-end:::  

## <a name="prerequisites"></a><span data-ttu-id="abb52-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="abb52-107">Prerequisites</span></span>  

*   <span data-ttu-id="abb52-108">Erfahrung mit der Win32-API</span><span class="sxs-lookup"><span data-stu-id="abb52-108">Experience using Win32 API</span></span>  

## <a name="async-methods"></a><span data-ttu-id="abb52-109">Async-Methoden</span><span class="sxs-lookup"><span data-stu-id="abb52-109">Async methods</span></span>  

<span data-ttu-id="abb52-110">Asynchrone Methoden in der WebView2 Win32 C++-API verwenden eine Stellvertretungsschnittstelle, um Sie aus den folgenden Gründen zu kontaktieren.</span><span class="sxs-lookup"><span data-stu-id="abb52-110">Asynchronous methods in the WebView2 Win32 C++ API use a delegate interface to contact you for the following reasons.</span></span>  

*   <span data-ttu-id="abb52-111">Die async-Methode wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="abb52-111">The async method has completed.</span></span>  
*   <span data-ttu-id="abb52-112">Der Erfolgs- oder Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="abb52-112">The success or failure code.</span></span>  
*   <span data-ttu-id="abb52-113">Das Ergebnis der asynchronen Methode.</span><span class="sxs-lookup"><span data-stu-id="abb52-113">The result of the asynchronous method.</span></span>  

<span data-ttu-id="abb52-114">Der letzte Parameter für alle asynchronen Methoden ist ein Zeiger auf eine Stellvertretungsschnittstelle, von der Sie eine Implementierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="abb52-114">The final parameter for all asynchronous methods is a pointer to a delegate interface of which you provide an implementation.</span></span>  

<span data-ttu-id="abb52-115">Die Stellvertretungsschnittstelle verfügt über eine einzelne Methode, die als erster Parameter einen des Erfolgs- oder `Invoke` `HRESULT` Fehlercodes verwendet.</span><span class="sxs-lookup"><span data-stu-id="abb52-115">The delegate interface has a single `Invoke` method that takes as a first parameter an `HRESULT` of the success or failure code.</span></span>  <span data-ttu-id="abb52-116">Darüber hinaus gibt es möglicherweise einen zweiten Parameter, der das Ergebnis der Methode ist, wenn die Methode ein Ergebnis hat.</span><span class="sxs-lookup"><span data-stu-id="abb52-116">Additionally, there may be a second parameter that is the result of the method if the method has a result.</span></span>  <span data-ttu-id="abb52-117">Beispielsweise verwendet die [ICoreWebView2::CapturePreview-Methode][Webview2ReferenceWin32Icorewebview2CapturePreview] als letzter Parameter einen `ICoreWebView2CapturePreviewCompletedHandler` Zeiger.</span><span class="sxs-lookup"><span data-stu-id="abb52-117">For example, the [ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] method takes as the final parameter an `ICoreWebView2CapturePreviewCompletedHandler` pointer.</span></span>  <span data-ttu-id="abb52-118">Zum Senden einer Methodenanforderung geben Sie eine Instanz des Zeigers an, `CapturePreview` `ICoreWebView2CapturePreviewCompletedHandler` den Sie implementieren.</span><span class="sxs-lookup"><span data-stu-id="abb52-118">To send a `CapturePreview` method request, you provide an instance of the `ICoreWebView2CapturePreviewCompletedHandler` pointer that you implement.</span></span>  <span data-ttu-id="abb52-119">Im folgenden Codeausschnitt wird eine Methode zum Implementieren verwendet.</span><span class="sxs-lookup"><span data-stu-id="abb52-119">The following code snippet uses one method to implement.</span></span>  

```cpp
HRESULT Invoke(HRESULT result)
```  

<span data-ttu-id="abb52-120">Sie implementieren die `Invoke` Methode und fordern ihre Methode `CoreWebView2` `Invoke` an, wenn die Anforderung abgeschlossen `CapturePreview` ist.</span><span class="sxs-lookup"><span data-stu-id="abb52-120">You implement the `Invoke` method and `CoreWebView2` requests your `Invoke` method when `CapturePreview` request completes.</span></span>  <span data-ttu-id="abb52-121">Der einzelne Parameter ist die Beschreibung des Erfolgs- oder `HRESULT` Fehlercodes der `CapturePreview` Anforderung.</span><span class="sxs-lookup"><span data-stu-id="abb52-121">The single parameter is the `HRESULT` describing the success or failure code of the `CapturePreview` request.</span></span>  

<span data-ttu-id="abb52-122">Alternativ stellen Sie für eine Instanz mit einer Methode zur Verfügung, die Ihnen den Erfolgs- oder `ICoreWebView2::ExecuteScript` `Invoke` Fehlercode der Anforderung `ExecuteScript` zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="abb52-122">Alternately, for `ICoreWebView2::ExecuteScript`, you provide an instance that has an `Invoke` method that provides you with the success or failure code of the `ExecuteScript` request.</span></span>  <span data-ttu-id="abb52-123">Geben Sie außerdem den zweiten Parameter an, der das JSON des Ergebnisses der Ausführung des Skripts ist.</span><span class="sxs-lookup"><span data-stu-id="abb52-123">Also provide the second parameter that is the JSON of the result of running the script.</span></span>  

<span data-ttu-id="abb52-124">Sie können die Stellvertretungsschnittstellen manuell implementieren oder die `CompleteHandler` [Rückruffunktion (Callback Function, WRL) verwenden.][CppCxWrlCallbackFunction]</span><span class="sxs-lookup"><span data-stu-id="abb52-124">You may manually implement the `CompleteHandler` delegate interfaces, or you may use the [Callback function (WRL)][CppCxWrlCallbackFunction].</span></span>  <span data-ttu-id="abb52-125">Die [Rückruffunktion (Callback Function, WRL)][CppCxWrlCallbackFunction] wird im folgenden WebView2-Codeausschnitt verwendet.</span><span class="sxs-lookup"><span data-stu-id="abb52-125">The [Callback function (WRL)][CppCxWrlCallbackFunction] is used throughout the following WebView2 code snippet.</span></span>  

```cpp
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```  

## <a name="events"></a><span data-ttu-id="abb52-126">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="abb52-126">Events</span></span>  

<span data-ttu-id="abb52-127">Ereignisse in der WebView2 Win32 C++-API verwenden das `add_EventName` and-Methodenpaar, um Ereignisse zu abonnieren und `remove_EventName` zu kündigen.</span><span class="sxs-lookup"><span data-stu-id="abb52-127">Events in the WebView2 Win32 C++ API use the `add_EventName` and `remove_EventName` method pair to subscribe and unsubscribe from events.</span></span>  <span data-ttu-id="abb52-128">Die `add_EventName` Methode verwendet eine Ereignishandlerdelegiertenschnittstelle und gibt ein Token als `EventRegistrationToken` Ausgabeparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="abb52-128">The `add_EventName` method takes an event handler delegate interface and gives back an `EventRegistrationToken` token as an output parameter.</span></span>  <span data-ttu-id="abb52-129">Die `remove_EventName` Methode verwendet ein Token und `EventRegistrationToken` kündigen das entsprechende Ereignisabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="abb52-129">The `remove_EventName` method takes an `EventRegistrationToken` token and unsubscribes the corresponding event subscription.</span></span>  

<span data-ttu-id="abb52-130">Ereignishandlerdelegiertenschnittstellen funktionieren ähnlich wie die abgeschlossenen Handlerdelegiertenschnittstellen der async-Methode.</span><span class="sxs-lookup"><span data-stu-id="abb52-130">Event handler delegate interfaces work similarly to the async method completed handler delegate interfaces.</span></span>  <span data-ttu-id="abb52-131">Sie implementieren die Stellvertretungsschnittstelle des Ereignishandlers und `CoreWebView2` senden einen Rückruf, wenn das Ereignis ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abb52-131">You implement the event handler delegate interface and `CoreWebView2` sends a callback whenever the event runs.</span></span>  <span data-ttu-id="abb52-132">Jede Ereignishandlerdelegiertenschnittstelle verfügt über eine einzelne Methode, die über einen Sender-Parameter gefolgt von `Invoke` einem Ereignis-args-Parameter verfügt.</span><span class="sxs-lookup"><span data-stu-id="abb52-132">Every event handler delegate interface has a single `Invoke` method that has a sender parameter followed by an event args parameter.</span></span>  <span data-ttu-id="abb52-133">Der Absender ist die Instanz des Objekts, für das Sie Ereignisse abonniert haben.</span><span class="sxs-lookup"><span data-stu-id="abb52-133">The sender is the instance of the object on which you subscribed for events.</span></span>  <span data-ttu-id="abb52-134">Der Ereignis-args-Parameter ist eine Schnittstelle, die Informationen zum aktuell abfeuernden Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="abb52-134">The event args parameter is an interface that contains information about the currently firing event.</span></span>  

<span data-ttu-id="abb52-135">Das Ereignis on `NavigationCompleted` hat z. `ICoreWebView2` B. das `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` Und-Methodenpaar.</span><span class="sxs-lookup"><span data-stu-id="abb52-135">For instance, the `NavigationCompleted` event on `ICoreWebView2` has the `ICoreWebView2::add_NavigationCompleted` and `ICoreWebView2::remove_NavigationCompleted` method pair.</span></span>  <span data-ttu-id="abb52-136">Wenn Sie eine Anforderung senden, stellen Sie eine Instanz zur Verfügung, `ICoreWebView2NavigationCompletedEventHandler` in der Sie zuvor eine Methode implementiert `Invoke` haben.</span><span class="sxs-lookup"><span data-stu-id="abb52-136">When you send a request, you provide an instance of `ICoreWebView2NavigationCompletedEventHandler` in which you previously implemented `Invoke` method.</span></span>  <span data-ttu-id="abb52-137">Wenn das `NavigationCompleted` Ereignis ausgeführt wird, wird `Invoke` Ihre Methode angefordert.</span><span class="sxs-lookup"><span data-stu-id="abb52-137">When the `NavigationCompleted` event runs, your `Invoke` method is requested.</span></span>  <span data-ttu-id="abb52-138">Der erste Parameter führt das Ereignis `NavigationCompleted` aus.</span><span class="sxs-lookup"><span data-stu-id="abb52-138">The first parameter runs the `NavigationCompleted` event.</span></span>  <span data-ttu-id="abb52-139">Der zweite Parameter enthält Informationen dazu, ob die Navigation erfolgreich abgeschlossen wurde und so weiter.</span><span class="sxs-lookup"><span data-stu-id="abb52-139">The second parameter contains information about if the navigation completed successfully and so on.</span></span>  

<span data-ttu-id="abb52-140">Verwenden Sie ähnlich wie bei der async-Methode abgeschlossene Handlerdelegiertenschnittstelle eine der folgenden Aktionen, um sie zu einrichten.</span><span class="sxs-lookup"><span data-stu-id="abb52-140">Similar to the async method completed handler delegate interface, use one of the following actions to set it up.</span></span>  

*   <span data-ttu-id="abb52-141">Implementieren Sie es direkt.</span><span class="sxs-lookup"><span data-stu-id="abb52-141">Implement it directly.</span></span>  
*   <span data-ttu-id="abb52-142">Verwenden Sie [die Rückruffunktion (Callback Function, WRL),][CppCxWrlCallbackFunction] die im folgenden WebView2-Codeausschnitt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="abb52-142">Use the [Callback function (WRL)][CppCxWrlCallbackFunction] function that is used in the following WebView2 code snippet.</span></span>  

<!-- todo:  what is async method completed handler delegate interface?  Is there a shorter name for it?  -->  

```cpp
// Register a handler for the NavigationCompleted event.
// Check whether the navigation succeeded, and if not, do something.
// Also update the Cancel buttons.
CHECK_FAILURE(m_webView->add_NavigationCompleted(
    Callback<ICoreWebView2NavigationCompletedEventHandler>(
        [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
            -> HRESULT {
            BOOL success;
            CHECK_FAILURE(args->get_IsSuccess(&success));
            if (!success)
            {
                COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                {
                    // Do something here if you want to handle a specific error case.
                    // In most cases it is not necessary, because the WebView
                    // displays an error page automatically.
                }
            }
            m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
            m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
            return S_OK;
        })
        .Get(),
    &m_navigationCompletedToken));
```  

## <a name="strings"></a><span data-ttu-id="abb52-143">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="abb52-143">Strings</span></span>  

<span data-ttu-id="abb52-144">Zeichenfolgenausgabeparameter sind `LPWSTR` zeichenfolgenent terminierte Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="abb52-144">String output parameters are `LPWSTR` null-terminated strings.</span></span>  <span data-ttu-id="abb52-145">Der Anfordernde stellt die Zeichenfolge mithilfe von `CoTaskMemAlloc` zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="abb52-145">The requester provides the string using `CoTaskMemAlloc`.</span></span>  <span data-ttu-id="abb52-146">Der Besitz wird an den Anantrager übertragen, und es liegt an dem Anantrager, den Arbeitsspeicher mithilfe von frei zu `CoTaskMemFree` stellen.</span><span class="sxs-lookup"><span data-stu-id="abb52-146">Ownership is transferred to the requester and it is up to the requester to free the memory using `CoTaskMemFree`.</span></span>  

<span data-ttu-id="abb52-147">Zeichenfolgeneingabeparameter sind `LPCWSTR` zeichenfolgenend beendete Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="abb52-147">String input parameters are `LPCWSTR` null-terminated strings.</span></span>  <span data-ttu-id="abb52-148">Der Anser stellt sicher, dass die Zeichenfolge für die Dauer der synchronen Funktionsanforderung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="abb52-148">The requester ensures the string is valid for the duration of the synchronous function request.</span></span>  <span data-ttu-id="abb52-149">Wenn der Empfänger den Wert bis zu einem bestimmten Punkt speichern muss, nachdem die Funktionsanforderung abgeschlossen ist, muss der Empfänger eine zugeordnete Kopie des Zeichenfolgenwerts angeben.</span><span class="sxs-lookup"><span data-stu-id="abb52-149">If the receiver must store the value to some point after the function request completes, the receiver must give an associated copy of the string value.</span></span>  

## <a name="uri-and-json-parsing"></a><span data-ttu-id="abb52-150">URI- und JSON-Analyse</span><span class="sxs-lookup"><span data-stu-id="abb52-150">URI and JSON parsing</span></span>  

<span data-ttu-id="abb52-151">Verschiedene Methoden bieten oder akzeptieren URIs und JSON als Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="abb52-151">Various methods provide or accept URIs and JSON as strings.</span></span>  <span data-ttu-id="abb52-152">Verwenden Sie Ihre bevorzugte Bibliothek zum Analysen und Generieren der Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="abb52-152">Use your preferred library for parsing and generating the strings.</span></span>  

<span data-ttu-id="abb52-153">Wenn WinRT für Ihre App verfügbar ist, können Sie die und-Methoden verwenden, um JSON-Zeichenfolgen oder -Methoden zu analysieren oder zu erstellen, um `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` URIs zu analysieren und zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="abb52-153">If WinRT is available for your app, you may use the `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` methods to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` methods to parse and produce URIs.</span></span>  <span data-ttu-id="abb52-154">Beide Methoden funktionieren in Win32-Apps.</span><span class="sxs-lookup"><span data-stu-id="abb52-154">Both of methods work in Win32 apps.</span></span>  

<span data-ttu-id="abb52-155">Wenn Sie URIs verwenden und analysieren, sollten Sie die folgenden `IUri` `CreateUri` URI-Erstellungsflags verwenden, um das Verhalten besser mit der `CreateUri` URI-Analyse in der WebView zu übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="abb52-155">If you use `IUri` and `CreateUri` to parse URIs, you may want to use the following URI creation flags to have `CreateUri` behavior more closely match the URI parsing in the WebView.</span></span>  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

## <a name="see-also"></a><span data-ttu-id="abb52-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="abb52-156">See also</span></span>  

*   <span data-ttu-id="abb52-157">Um mit der Verwendung von WebView2 Win32 C/C++ zu beginnen, navigieren Sie zu [Erste Schritte mit WebView2][Webview2IndexGettingStarted]-Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="abb52-157">To get started using WebView2 Win32 C/C++, navigate to [Getting started with WebView2][Webview2IndexGettingStarted] guides.</span></span>  
*   <span data-ttu-id="abb52-158">Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="abb52-158">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="abb52-159">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="abb52-159">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2GettingstartedWin32]: ../gettingstarted/win32.md "Erste Schritte mit WebView2 | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview – Schnittstelle ICoreWebView2 | Microsoft Docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Rückruffunktion (Callback Function, WRL) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2-Klasse | Microsoft Docs"  
