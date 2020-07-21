---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 649506b28e0ecdbff33b44bbd8010ddb3d2a66b0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885800"
---
# <span data-ttu-id="9e5e4-104">0.8.355-Interface-IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="9e5e4-104">0.8.355 - interface IWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="9e5e4-105">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="9e5e4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9e5e4-106">Summary</span></span>

 <span data-ttu-id="9e5e4-107">Member</span><span class="sxs-lookup"><span data-stu-id="9e5e4-107">Members</span></span>                        | <span data-ttu-id="9e5e4-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9e5e4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e5e4-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="9e5e4-110">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="9e5e4-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="9e5e4-112">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="9e5e4-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="9e5e4-114">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="9e5e4-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="9e5e4-116">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="9e5e4-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="9e5e4-118">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="9e5e4-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="9e5e4-120">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="9e5e4-121">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="9e5e4-121">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="9e5e4-122">Diese Einstellung ist veraltet und gibt immer false zurück.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-122">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="9e5e4-123">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="9e5e4-123">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="9e5e4-124">Diese Einstellung ist veraltet und hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-124">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="9e5e4-125">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-125">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="9e5e4-126">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="9e5e4-127">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-127">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="9e5e4-128">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-128">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="9e5e4-129">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-129">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="9e5e4-130">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-130">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="9e5e4-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="9e5e4-132">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-132">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="9e5e4-133">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-133">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="9e5e4-134">Member</span><span class="sxs-lookup"><span data-stu-id="9e5e4-134">Members</span></span>

#### <span data-ttu-id="9e5e4-135">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-135">get_IsScriptEnabled</span></span> 

<span data-ttu-id="9e5e4-136">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-136">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="9e5e4-137">Public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-137">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="9e5e4-138">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-138">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="9e5e4-139">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-139">It is true by default.</span></span>

```cpp
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
```

#### <span data-ttu-id="9e5e4-140">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-140">put_IsScriptEnabled</span></span> 

<span data-ttu-id="9e5e4-141">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-141">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="9e5e4-142">Public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-142">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="9e5e4-143">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-143">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="9e5e4-144">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-144">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="9e5e4-145">Public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-145">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="9e5e4-146">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="9e5e4-146">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="9e5e4-147">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="9e5e4-147">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="9e5e4-148">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-148">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="9e5e4-149">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-149">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="9e5e4-150">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-150">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="9e5e4-151">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-151">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="9e5e4-152">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-152">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="9e5e4-153">Public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-153">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="9e5e4-154">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-154">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="9e5e4-155">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-155">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="9e5e4-156">Public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-156">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="9e5e4-157">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere die in den Funktionen JavaScript-Benachrichtigung, Bestätigung und Eingabeaufforderung angezeigten Funktionen).</span><span class="sxs-lookup"><span data-stu-id="9e5e4-157">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="9e5e4-158">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-158">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="9e5e4-159">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-159">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="9e5e4-160">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-160">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="9e5e4-161">Public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-161">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="9e5e4-162">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="9e5e4-162">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="9e5e4-163">Diese Einstellung ist veraltet und gibt immer false zurück.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-163">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="9e5e4-164">Public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-164">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="9e5e4-165">Das bedeutet, dass Elemente in der WebView nur die WebView-Begrenzungen ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-165">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="9e5e4-166">Diese Eigenschaft wird dann vollständig entfernt.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-166">This property will then be completely removed.</span></span> <span data-ttu-id="9e5e4-167">Bitte hören Sie sich stattdessen das ContainsFullScreenElementChanged-Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-167">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="9e5e4-168">Steuert, ob Vollbild für Elemente in der WebView zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-168">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="9e5e4-169">Wenn dies zulässig ist, können Webinhalte, wie ein Video Element in der WebView, im Vollbildmodus angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-169">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="9e5e4-170">Wenn dies nicht zulässig ist, füllt ein solches Element die WebView-Begrenzungen aus, wenn das Element den Vollbildmodus anfordert.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-170">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="9e5e4-171">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-171">It is true by default.</span></span>

#### <span data-ttu-id="9e5e4-172">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="9e5e4-172">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="9e5e4-173">Diese Einstellung ist veraltet und hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-173">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="9e5e4-174">Public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(bool IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-174">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="9e5e4-175">Bitte hören Sie sich stattdessen das ContainsFullScreenElementChanged-Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-175">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="9e5e4-176">Festlegen der IsFullscreenAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-176">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="9e5e4-177">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-177">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="9e5e4-178">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-178">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="9e5e4-179">Public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-179">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="9e5e4-180">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-180">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="9e5e4-181">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-181">It is true by default.</span></span>

#### <span data-ttu-id="9e5e4-182">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-182">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="9e5e4-183">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-183">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="9e5e4-184">Public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-184">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="9e5e4-185">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-185">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="9e5e4-186">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-186">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="9e5e4-187">Public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-187">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="9e5e4-188">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="9e5e4-188">It is true by default.</span></span>

#### <span data-ttu-id="9e5e4-189">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e5e4-189">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="9e5e4-190">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e5e4-190">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="9e5e4-191">Public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="9e5e4-191">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

