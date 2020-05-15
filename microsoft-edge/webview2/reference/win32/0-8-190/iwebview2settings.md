---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 3c799e97f8e85927e1c11b30be747d7649faeca0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653854"
---
# <span data-ttu-id="6f11f-104">Schnittstellen IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="6f11f-104">interface IWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="6f11f-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="6f11f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="6f11f-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6f11f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="6f11f-107">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="6f11f-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="6f11f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6f11f-108">Summary</span></span>

 <span data-ttu-id="6f11f-109">Member</span><span class="sxs-lookup"><span data-stu-id="6f11f-109">Members</span></span>                        | <span data-ttu-id="6f11f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6f11f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6f11f-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="6f11f-112">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6f11f-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="6f11f-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="6f11f-114">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="6f11f-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="6f11f-116">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f11f-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="6f11f-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="6f11f-118">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="6f11f-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="6f11f-120">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f11f-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="6f11f-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="6f11f-122">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="6f11f-123">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="6f11f-123">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="6f11f-124">Diese Einstellung ist veraltet und gibt immer false zurück.</span><span class="sxs-lookup"><span data-stu-id="6f11f-124">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="6f11f-125">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="6f11f-125">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="6f11f-126">Diese Einstellung ist veraltet und hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="6f11f-126">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="6f11f-127">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-127">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="6f11f-128">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6f11f-128">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="6f11f-129">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-129">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="6f11f-130">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-130">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="6f11f-131">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-131">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="6f11f-132">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6f11f-132">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="6f11f-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="6f11f-134">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-134">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="6f11f-135">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="6f11f-135">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="6f11f-136">Member</span><span class="sxs-lookup"><span data-stu-id="6f11f-136">Members</span></span>

#### <span data-ttu-id="6f11f-137">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-137">get_IsScriptEnabled</span></span> 

<span data-ttu-id="6f11f-138">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6f11f-138">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="6f11f-139">Public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-139">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="6f11f-140">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6f11f-140">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="6f11f-141">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="6f11f-141">It is true by default.</span></span>

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

#### <span data-ttu-id="6f11f-142">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-142">put_IsScriptEnabled</span></span> 

<span data-ttu-id="6f11f-143">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-143">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="6f11f-144">Public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-144">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="6f11f-145">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-145">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="6f11f-146">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f11f-146">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="6f11f-147">Public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-147">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="6f11f-148">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="6f11f-148">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="6f11f-149">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="6f11f-149">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="6f11f-150">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6f11f-150">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="6f11f-151">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="6f11f-151">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="6f11f-152">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="6f11f-152">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="6f11f-153">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-153">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="6f11f-154">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-154">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="6f11f-155">Public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-155">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="6f11f-156">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-156">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="6f11f-157">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f11f-157">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="6f11f-158">Public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-158">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="6f11f-159">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere die in den Funktionen JavaScript-Benachrichtigung, Bestätigung und Eingabeaufforderung angezeigten Funktionen).</span><span class="sxs-lookup"><span data-stu-id="6f11f-159">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="6f11f-160">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6f11f-160">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="6f11f-161">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-161">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="6f11f-162">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-162">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="6f11f-163">Public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-163">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="6f11f-164">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="6f11f-164">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="6f11f-165">Diese Einstellung ist veraltet und gibt immer false zurück.</span><span class="sxs-lookup"><span data-stu-id="6f11f-165">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="6f11f-166">Public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="6f11f-166">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="6f11f-167">Das bedeutet, dass Elemente in der WebView nur die WebView-Begrenzungen ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="6f11f-167">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="6f11f-168">Diese Eigenschaft wird dann vollständig entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f11f-168">This property will then be completely removed.</span></span> <span data-ttu-id="6f11f-169">Bitte hören Sie sich stattdessen das ContainsFullScreenElementChanged-Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="6f11f-169">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="6f11f-170">Steuert, ob Vollbild für Elemente in der WebView zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6f11f-170">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="6f11f-171">Wenn dies zulässig ist, können Webinhalte, wie ein Video Element in der WebView, im Vollbildmodus angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6f11f-171">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="6f11f-172">Wenn dies nicht zulässig ist, füllt ein solches Element die WebView-Begrenzungen aus, wenn das Element den Vollbildmodus anfordert.</span><span class="sxs-lookup"><span data-stu-id="6f11f-172">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="6f11f-173">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="6f11f-173">It is true by default.</span></span>

#### <span data-ttu-id="6f11f-174">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="6f11f-174">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="6f11f-175">Diese Einstellung ist veraltet und hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="6f11f-175">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="6f11f-176">Public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(bool IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="6f11f-176">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="6f11f-177">Bitte hören Sie sich stattdessen das ContainsFullScreenElementChanged-Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="6f11f-177">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="6f11f-178">Festlegen der IsFullscreenAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-178">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="6f11f-179">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-179">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="6f11f-180">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6f11f-180">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="6f11f-181">Public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-181">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="6f11f-182">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="6f11f-182">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="6f11f-183">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="6f11f-183">It is true by default.</span></span>

#### <span data-ttu-id="6f11f-184">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-184">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="6f11f-185">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-185">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="6f11f-186">Public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-186">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="6f11f-187">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-187">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="6f11f-188">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6f11f-188">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="6f11f-189">Public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-189">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="6f11f-190">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="6f11f-190">It is true by default.</span></span>

#### <span data-ttu-id="6f11f-191">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6f11f-191">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="6f11f-192">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f11f-192">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="6f11f-193">Public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6f11f-193">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

