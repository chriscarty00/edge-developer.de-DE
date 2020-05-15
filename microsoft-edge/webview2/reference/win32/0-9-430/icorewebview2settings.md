---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 79f6e2712cab6d18025bd49ab0e7ceba01495d65
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654098"
---
# <span data-ttu-id="6a9c3-104">Schnittstellen ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="6a9c3-104">interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="6a9c3-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6a9c3-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6a9c3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="6a9c3-107">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="6a9c3-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6a9c3-108">Summary</span></span>

 <span data-ttu-id="6a9c3-109">Member</span><span class="sxs-lookup"><span data-stu-id="6a9c3-109">Members</span></span>                        | <span data-ttu-id="6a9c3-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6a9c3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a9c3-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="6a9c3-112">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="6a9c3-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="6a9c3-114">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="6a9c3-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="6a9c3-116">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="6a9c3-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="6a9c3-118">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="6a9c3-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="6a9c3-120">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="6a9c3-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="6a9c3-122">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="6a9c3-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="6a9c3-124">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="6a9c3-125">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-125">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="6a9c3-126">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-126">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="6a9c3-127">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-127">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="6a9c3-128">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-128">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="6a9c3-129">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-129">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="6a9c3-130">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-130">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="6a9c3-131">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-131">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="6a9c3-132">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="6a9c3-133">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-133">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="6a9c3-134">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-134">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="6a9c3-135">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="6a9c3-135">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="6a9c3-136">Die AreRemoteObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Remoteobjekten über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-136">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="6a9c3-137">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="6a9c3-137">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="6a9c3-138">Festlegen der AreRemoteObjectsAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-138">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="6a9c3-139">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-139">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="6a9c3-140">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-140">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="6a9c3-141">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-141">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="6a9c3-142">Festlegen der IsZoomControlEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-142">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="6a9c3-143">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-143">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="6a9c3-144">Member</span><span class="sxs-lookup"><span data-stu-id="6a9c3-144">Members</span></span>

#### <span data-ttu-id="6a9c3-145">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-145">get_IsScriptEnabled</span></span> 

<span data-ttu-id="6a9c3-146">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-146">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="6a9c3-147">Public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-147">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="6a9c3-148">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-148">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="6a9c3-149">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-149">It is true by default.</span></span>

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

#### <span data-ttu-id="6a9c3-150">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-150">put_IsScriptEnabled</span></span> 

<span data-ttu-id="6a9c3-151">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-151">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="6a9c3-152">Public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-152">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="6a9c3-153">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-153">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="6a9c3-154">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-154">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="6a9c3-155">Public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-155">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="6a9c3-156">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="6a9c3-156">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="6a9c3-157">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="6a9c3-157">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="6a9c3-158">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-158">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="6a9c3-159">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-159">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="6a9c3-160">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-160">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="6a9c3-161">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-161">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="6a9c3-162">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-162">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="6a9c3-163">Public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-163">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="6a9c3-164">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-164">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="6a9c3-165">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-165">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="6a9c3-166">Public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-166">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="6a9c3-167">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="6a9c3-167">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="6a9c3-168">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-168">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="6a9c3-169">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-169">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="6a9c3-170">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-170">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="6a9c3-171">Public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-171">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="6a9c3-172">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-172">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="6a9c3-173">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-173">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="6a9c3-174">Public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-174">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="6a9c3-175">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-175">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="6a9c3-176">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-176">It is true by default.</span></span>

#### <span data-ttu-id="6a9c3-177">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-177">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="6a9c3-178">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-178">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="6a9c3-179">Public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-179">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="6a9c3-180">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-180">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="6a9c3-181">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-181">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="6a9c3-182">Public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-182">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="6a9c3-183">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-183">It is true by default.</span></span>

#### <span data-ttu-id="6a9c3-184">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-184">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="6a9c3-185">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-185">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="6a9c3-186">Public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-186">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="6a9c3-187">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-187">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="6a9c3-188">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-188">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="6a9c3-189">öffentliche HRESULT- [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-189">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="6a9c3-190">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-190">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="6a9c3-191">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-191">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="6a9c3-192">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-192">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="6a9c3-193">öffentliche HRESULT- [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-193">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="6a9c3-194">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="6a9c3-194">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="6a9c3-195">Die AreRemoteObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Remoteobjekten über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-195">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="6a9c3-196">öffentliche HRESULT- [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(bool \* zulässig)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-196">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="6a9c3-197">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-197">Defaults to TRUE.</span></span>

```cpp
            BOOL allowRemoteObjects;
            CHECK_FAILURE(m_settings->get_AreRemoteObjectsAllowed(&allowRemoteObjects));
            if (allowRemoteObjects)
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to remote objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to remote objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="6a9c3-198">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="6a9c3-198">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="6a9c3-199">Festlegen der AreRemoteObjectsAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-199">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="6a9c3-200">öffentliche HRESULT- [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(bool Allowed)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-200">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="6a9c3-201">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-201">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="6a9c3-202">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-202">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="6a9c3-203">öffentliche HRESULT- [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-203">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="6a9c3-204">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-204">Defaults to TRUE.</span></span> <span data-ttu-id="6a9c3-205">Wenn diese Option deaktiviert ist, kann der Benutzer nicht mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über put_ZoomFactor-API eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6a9c3-205">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control is disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control is enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="6a9c3-206">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="6a9c3-206">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="6a9c3-207">Festlegen der IsZoomControlEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a9c3-207">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="6a9c3-208">öffentliche HRESULT- [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="6a9c3-208">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

