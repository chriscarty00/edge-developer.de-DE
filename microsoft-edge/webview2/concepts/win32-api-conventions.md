---
description: Win32 C++ WebView2-API-Konventionen
title: Win32 C++ WebView2-API-Konventionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6c596b038e871caa5a364991351636f51ef7d685
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010684"
---
# <span data-ttu-id="6cd53-104">Win32 C++ WebView2-API-Konventionen</span><span class="sxs-lookup"><span data-stu-id="6cd53-104">Win32 C++ WebView2 API conventions</span></span>  

## <span data-ttu-id="6cd53-105">Async-Methoden</span><span class="sxs-lookup"><span data-stu-id="6cd53-105">Async Methods</span></span>  

<span data-ttu-id="6cd53-106">Asynchrone Methoden in der WebView2 Win32 C++-API verwenden eine Delegate-Schnittstelle, um Ihnen einen Rückruf zu senden, um anzugeben, wann die Async-Methode abgeschlossen wurde, den Erfolgs-oder Fehlercode und für einige das Ergebnis der asynchronen Methode.</span><span class="sxs-lookup"><span data-stu-id="6cd53-106">Asynchronous methods in the WebView2 Win32 C++ API use a delegate interface to callback to you to indicate when the async method has completed, the success or failure code, and for some, the result of the asynchronous method.</span></span>  <span data-ttu-id="6cd53-107">Der letzte Parameter für alle asynchronen Methoden ist ein Zeiger auf eine Delegat-Schnittstelle, von der Sie eine Implementierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6cd53-107">The final parameter for all asynchronous methods is a pointer to a delegate interface of which you provide an implementation.</span></span>  

<span data-ttu-id="6cd53-108">Die Delegat-Schnittstelle verfügt über eine einzelne `Invoke` Methode, die als erster Parameter eine `HRESULT` des Erfolgs-oder Fehlercodes akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="6cd53-108">The delegate interface has a single `Invoke` method that takes as a first parameter an `HRESULT` of the success or failure code.</span></span>  <span data-ttu-id="6cd53-109">Darüber hinaus gibt es möglicherweise einen zweiten Parameter, der das Ergebnis der Methode ist, wenn die Methode ein Ergebnis hat.</span><span class="sxs-lookup"><span data-stu-id="6cd53-109">Additionally there may be a second parameter that is the result of the method if the method has a result.</span></span>  <span data-ttu-id="6cd53-110">Beispielsweise nimmt die [ICoreWebView2:: CapturePreview] [Webview2ReferenceWin3209538Icorewebview2CapturePreview]-Methode als letzten Parameter einen `ICoreWebView2CapturePreviewCompletedHandler` Zeiger ein.</span><span class="sxs-lookup"><span data-stu-id="6cd53-110">For example, the [ICoreWebView2::CapturePreview][Webview2ReferenceWin3209538Icorewebview2CapturePreview] method takes as the final parameter an `ICoreWebView2CapturePreviewCompletedHandler` pointer.</span></span>  <span data-ttu-id="6cd53-111">Um eine `CapturePreview` Methoden Anforderung zu senden, geben Sie eine Instanz des `ICoreWebView2CapturePreviewCompletedHandler` Zeigers an, den Sie implementieren.</span><span class="sxs-lookup"><span data-stu-id="6cd53-111">To send a `CapturePreview` method request, you provide an instance of the `ICoreWebView2CapturePreviewCompletedHandler` pointer that you implement.</span></span>  <span data-ttu-id="6cd53-112">Im folgenden Codeausschnitt wird eine Methode zum Implementieren verwendet.</span><span class="sxs-lookup"><span data-stu-id="6cd53-112">The following code snippet uses one method to implement.</span></span>  

```cpp
HRESULT Invoke(HRESULT result)
```  

<span data-ttu-id="6cd53-113">Sie implementieren die `Invoke` Methode und `CoreWebView2` fordern Ihre `Invoke` Methode an, wenn die `CapturePreview` Anforderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6cd53-113">You implement the `Invoke` method and `CoreWebView2` requests your `Invoke` method when `CapturePreview` request completes.</span></span>  <span data-ttu-id="6cd53-114">Der Single `HRESULT` -Parameter beschreibt den Erfolgs-oder Fehlercode der `CapturePreview` Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6cd53-114">The single parameter is the `HRESULT` describing the success or failure code of the `CapturePreview` request.</span></span>  

<span data-ttu-id="6cd53-115">Oder für `ICoreWebView2::ExecuteScript` , stellen Sie eine Instanz von zur Verfügung, die über `ICoreWebView2ExecuteScriptCompletedHandler` eine `Invoke` Methode verfügt, die Ihnen den Erfolgs-oder Fehlercode der Anforderung sowie den zweiten Parameter bereitstellt, bei dem es sich um die `ExecuteScript` `resultObjectAsJson` JSON des Ergebnisses der Ausführung des Skripts handelt.</span><span class="sxs-lookup"><span data-stu-id="6cd53-115">Or for `ICoreWebView2::ExecuteScript`, you provide an instance of `ICoreWebView2ExecuteScriptCompletedHandler` which has an `Invoke` method that provides you with the success or failure code of the `ExecuteScript` request as well as the second parameter `resultObjectAsJson` which is the JSON of the result of running the script.</span></span>  

<span data-ttu-id="6cd53-116">Sie können die `CompleteHandler` Stell Vertretungs Schnittstellen manuell implementieren, oder Sie können die [WRL-Rückruffunktion][CppCxWrlCallbackFunction]verwenden.</span><span class="sxs-lookup"><span data-stu-id="6cd53-116">You may manually implement the `CompleteHandler` delegate interfaces, or you may use the [WRL Callback function][CppCxWrlCallbackFunction].</span></span>  <span data-ttu-id="6cd53-117">Die Rückruffunktion wird im folgenden WebView2-Codeausschnitt verwendet.</span><span class="sxs-lookup"><span data-stu-id="6cd53-117">The Callback function is used throughout the following WebView2 code snippet.</span></span>  

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

## <span data-ttu-id="6cd53-118">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="6cd53-118">Events</span></span>  

<span data-ttu-id="6cd53-119">Ereignisse in der WebView2 Win32 C++-API verwenden das `add_EventName` und `remove_EventName` -Methodenpaar, um Ereignisse zu abonnieren und abzubestellen.</span><span class="sxs-lookup"><span data-stu-id="6cd53-119">Events in the WebView2 Win32 C++ API use the `add_EventName` and `remove_EventName` method pair to subscribe and unsubscribe from events.</span></span>  <span data-ttu-id="6cd53-120">Die `add_EventName` Methode verwendet eine Ereignishandler-Delegat Schnittstelle und gibt einen `EventRegistrationToken` als out-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="6cd53-120">The `add_EventName` method takes an event handler delegate interface and gives back an `EventRegistrationToken` as an out parameter.</span></span>  <span data-ttu-id="6cd53-121">Die `remove_EventName` Methode verwendet ein `EventRegistrationToken` -und-Abonnement für das entsprechende Ereignisabonnement.</span><span class="sxs-lookup"><span data-stu-id="6cd53-121">The `remove_EventName` method takes an `EventRegistrationToken` and unsubscribes the corresponding event subscription.</span></span>  

<span data-ttu-id="6cd53-122">Ereignishandler-Delegat-Schnittstellen funktionieren sehr ähnlich wie die von der Async-Methode abgeschlossenen Handler-Delegat Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="6cd53-122">Event handler delegate interfaces work very similarly to the async method completed handler delegate interfaces.</span></span>  <span data-ttu-id="6cd53-123">Sie implementieren die Ereignishandler-Delegat Schnittstelle und `CoreWebView2` senden einen Rückruf, wenn das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="6cd53-123">You implement the event handler delegate interface and `CoreWebView2` sends a callback whenever the event fires.</span></span>  <span data-ttu-id="6cd53-124">Jede Schnittstelle für einen Ereignishandler-Delegat verfügt über eine einzelne `Invoke` Methode, die über einen Sender-Parameter gefolgt von einem Event args-Parameter verfügt.</span><span class="sxs-lookup"><span data-stu-id="6cd53-124">Every event handler delegate interface has a single `Invoke` method that has a sender parameter followed by an event args parameter.</span></span>  <span data-ttu-id="6cd53-125">Der Absender ist die Instanz des Objekts, für das Sie Ereignisse abonniert haben.</span><span class="sxs-lookup"><span data-stu-id="6cd53-125">The sender is the instance of the object on which you subscribed for events.</span></span>  <span data-ttu-id="6cd53-126">Der Ereignis-args-Parameter ist eine Schnittstelle, die Informationen zum aktuell ausgelösten Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="6cd53-126">The event args parameter is an interface that contains information about the currently firing event.</span></span>  

<span data-ttu-id="6cd53-127">Das `NavigationCompleted` Ereignis on weist Beispiels `ICoreWebView2` Weise das `ICoreWebView2::add_NavigationCompleted` und `ICoreWebView2::remove_NavigationCompleted` -Methodenpaar auf.</span><span class="sxs-lookup"><span data-stu-id="6cd53-127">For instance the `NavigationCompleted` event on `ICoreWebView2` has the `ICoreWebView2::add_NavigationCompleted` and `ICoreWebView2::remove_NavigationCompleted` method pair.</span></span>  <span data-ttu-id="6cd53-128">Wenn Sie Add anfordern, geben Sie eine Instanz an `ICoreWebView2NavigationCompletedEventHandler` , in der Sie zuvor die Methode implementiert haben `Invoke` .</span><span class="sxs-lookup"><span data-stu-id="6cd53-128">When you request add you provide an instance of `ICoreWebView2NavigationCompletedEventHandler` in which you previously implemented `Invoke` method.</span></span>  <span data-ttu-id="6cd53-129">Wenn das `NavigationCompleted` Ereignis ausgelöst wird, `Invoke` wird die Methode angefordert.</span><span class="sxs-lookup"><span data-stu-id="6cd53-129">When the `NavigationCompleted` event fires, your `Invoke` method is requested.</span></span>  <span data-ttu-id="6cd53-130">Der erste Parameter ist das `ICoreWebView2` Auslösen des `NavigationCompleted` Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="6cd53-130">The first parameter is the `ICoreWebView2` which is firing the `NavigationCompleted` event.</span></span>  <span data-ttu-id="6cd53-131">Der zweite Parameter ist der `ICoreWebView2NavigationCompletedEventArgs` , der Informationen darüber enthält, ob die Navigation erfolgreich abgeschlossen wurde usw.</span><span class="sxs-lookup"><span data-stu-id="6cd53-131">The second parameter is the `ICoreWebView2NavigationCompletedEventArgs` which contains information about if the navigation completed successfully and so on.</span></span>  

<span data-ttu-id="6cd53-132">Ähnlich wie bei der durch die Async-Methode abgeschlossenen Handler-Delegat-Schnittstelle können Sie Sie direkt selbst implementieren, oder Sie können die WRL-Rückruffunktion verwenden, die im folgenden WebView2-Codeausschnitt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cd53-132">Similarly to the async method completed handler delegate interface you are able to implement it yourself directly, or you may use the WRL Callback function that is used in the following WebView2 code snippet.</span></span>  

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

## <span data-ttu-id="6cd53-133">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="6cd53-133">Strings</span></span>  

<span data-ttu-id="6cd53-134">Zeichenfolgenparameter sind `LPWSTR` NULL-terminierte Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="6cd53-134">String out parameters are `LPWSTR` null-terminated strings.</span></span>  <span data-ttu-id="6cd53-135">Der Anforderer ordnet die Zeichenfolge mithilfe von `CoTaskMemAlloc` .</span><span class="sxs-lookup"><span data-stu-id="6cd53-135">The requester allocates the string using `CoTaskMemAlloc`.</span></span>  <span data-ttu-id="6cd53-136">Der Besitz wird an den anfordernden übertragen, und es ist Aufgabe des anfordernden, den Speicher mit zu befreien `CoTaskMemFree` .</span><span class="sxs-lookup"><span data-stu-id="6cd53-136">Ownership is transferred to the requester and it is up to the requester to free the memory using `CoTaskMemFree`.</span></span>  

<span data-ttu-id="6cd53-137">Zeichenfolge in Parametern sind `LPCWSTR` NULL-terminierte Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="6cd53-137">String in parameters are `LPCWSTR` null-terminated strings.</span></span>  <span data-ttu-id="6cd53-138">Der Anforderer stellt sicher, dass die Zeichenfolge für die Dauer der synchronen Funktionsanforderung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6cd53-138">The requester ensures the string is valid for the duration of the synchronous function request.</span></span>  <span data-ttu-id="6cd53-139">Wenn der Empfänger diesen Wert bis zu einem gewissen Punkt beibehalten muss, nachdem die Funktionsanforderung abgeschlossen ist, muss der Empfänger eine zugeordnete Kopie des Zeichenfolgenwerts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="6cd53-139">If the receiver must retain that value to some point after the function request completes, the receiver must allocate an associated copy of the string value.</span></span>  

## <span data-ttu-id="6cd53-140">URI-und JSON-Analyse</span><span class="sxs-lookup"><span data-stu-id="6cd53-140">URI and JSON parsing</span></span>  

<span data-ttu-id="6cd53-141">Verschiedene Methoden stellen URIs und JSON als Zeichenfolgen bereit oder akzeptieren Sie.</span><span class="sxs-lookup"><span data-stu-id="6cd53-141">Various methods provide or accept URIs and JSON as strings.</span></span>  <span data-ttu-id="6cd53-142">Verwenden Sie bitte Ihre eigene bevorzugte Bibliothek, um die Zeichenfolgen zu analysieren und zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6cd53-142">Please use your own preferred library for parsing and generating the strings.</span></span>  

<span data-ttu-id="6cd53-143">Wenn WinRT für Ihre app verfügbar ist, können Sie die `RuntimeClass_Windows_Data_Json_JsonObject` Methoden und verwenden, `IJsonObjectStatics` um JSON-Zeichenfolgen oder `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` Methoden zum Analysieren und Erstellen von URIs zu analysieren oder zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="6cd53-143">If WinRT is available for your app, you may use the `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` methods to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` methods to parse and produce URIs.</span></span>  <span data-ttu-id="6cd53-144">Beide Methoden funktionieren in Win32-apps.</span><span class="sxs-lookup"><span data-stu-id="6cd53-144">Both of methods work in Win32 apps.</span></span>  

<span data-ttu-id="6cd53-145">Wenn Sie `IUri` URIs verwenden und `CreateUri` analysieren, sollten Sie die folgenden URI-Erstellungs Flags verwenden, damit `CreateUri` das Verhalten der URI-Analyse in der WebView genauer entspricht.</span><span class="sxs-lookup"><span data-stu-id="6cd53-145">If you use `IUri` and `CreateUri` to parse URIs, you may want to use the following URI creation flags to have `CreateUri` behavior more closely match the URI parsing in the WebView.</span></span>  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin3209622Icorewebview2CapturePreview]: ../reference/win32/0-9-622/icorewebview2.md#capturepreview "CapturePreview-Interface-ICoreWebView2 | Microsoft docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Callback-Funktion (WRL) | Microsoft docs"  
