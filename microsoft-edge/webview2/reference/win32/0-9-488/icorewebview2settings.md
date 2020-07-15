---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a996660bb667ca0e556326e0bf2b71c15b9344c2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880332"
---
# <span data-ttu-id="22d86-104">0.9.515-Interface-ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="22d86-104">0.9.515 - interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="22d86-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="22d86-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="22d86-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="22d86-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="22d86-107">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="22d86-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="22d86-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="22d86-108">Summary</span></span>

 <span data-ttu-id="22d86-109">Member</span><span class="sxs-lookup"><span data-stu-id="22d86-109">Members</span></span>                        | <span data-ttu-id="22d86-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="22d86-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="22d86-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="22d86-112">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="22d86-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="22d86-113">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-113">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="22d86-114">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="22d86-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="22d86-115">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-115">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="22d86-116">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="22d86-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="22d86-117">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="22d86-117">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="22d86-118">Die AreRemoteObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="22d86-118">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="22d86-119">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-119">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="22d86-120">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="22d86-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="22d86-121">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-121">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="22d86-122">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="22d86-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="22d86-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="22d86-124">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="22d86-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="22d86-125">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-125">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="22d86-126">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="22d86-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="22d86-127">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-127">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="22d86-128">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="22d86-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="22d86-129">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-129">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="22d86-130">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-130">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="22d86-131">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-131">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="22d86-132">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-132">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="22d86-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="22d86-134">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-134">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="22d86-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="22d86-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="22d86-136">Festlegen der AreRemoteObjectsAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="22d86-137">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-137">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="22d86-138">Festlegen der IsBuiltInErrorPageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-138">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="22d86-139">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-139">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="22d86-140">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-140">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="22d86-141">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-141">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="22d86-142">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-142">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="22d86-143">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-143">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="22d86-144">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-144">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="22d86-145">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-145">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="22d86-146">Festlegen der IsZoomControlEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-146">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="22d86-147">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="22d86-147">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="22d86-148">Member</span><span class="sxs-lookup"><span data-stu-id="22d86-148">Members</span></span>

#### <span data-ttu-id="22d86-149">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-149">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="22d86-150">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="22d86-150">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="22d86-151">öffentliche HRESULT- [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-151">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="22d86-152">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22d86-152">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="22d86-153">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-153">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="22d86-154">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="22d86-154">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="22d86-155">Public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-155">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="22d86-156">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="22d86-156">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="22d86-157">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22d86-157">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="22d86-158">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-158">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="22d86-159">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="22d86-159">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="22d86-160">Public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-160">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="22d86-161">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="22d86-161">It is true by default.</span></span>

#### <span data-ttu-id="22d86-162">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="22d86-162">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="22d86-163">Die AreRemoteObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="22d86-163">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="22d86-164">öffentliche HRESULT- [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(bool \* zulässig)</span><span class="sxs-lookup"><span data-stu-id="22d86-164">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="22d86-165">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22d86-165">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="22d86-166">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-166">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="22d86-167">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="22d86-167">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="22d86-168">öffentliche HRESULT- [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-168">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="22d86-169">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22d86-169">Defaults to TRUE.</span></span> <span data-ttu-id="22d86-170">Wenn diese Option deaktiviert ist, wird leere Seite angezeigt, wenn ein verwandter Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="22d86-170">When disabled, blank page will be shown when related error happens.</span></span>

```cpp
            BOOL enabled;
            CHECK_FAILURE(m_settings->get_IsBuiltInErrorPageEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(FALSE));
                MessageBox(
                    nullptr, L"Built-in error page will be disabled for future navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(TRUE));
                MessageBox(
                    nullptr, L"Built-in error page will be enabled for future navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="22d86-171">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-171">get_IsScriptEnabled</span></span> 

<span data-ttu-id="22d86-172">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="22d86-172">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="22d86-173">Public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-173">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="22d86-174">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="22d86-174">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="22d86-175">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="22d86-175">It is true by default.</span></span>

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

#### <span data-ttu-id="22d86-176">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-176">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="22d86-177">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="22d86-177">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="22d86-178">Public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-178">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="22d86-179">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="22d86-179">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="22d86-180">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="22d86-180">It is true by default.</span></span>

#### <span data-ttu-id="22d86-181">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-181">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="22d86-182">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="22d86-182">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="22d86-183">Public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-183">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="22d86-184">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="22d86-184">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="22d86-185">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="22d86-185">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="22d86-186">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="22d86-186">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="22d86-187">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="22d86-187">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="22d86-188">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="22d86-188">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="22d86-189">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-189">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="22d86-190">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="22d86-190">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="22d86-191">öffentliche HRESULT- [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-191">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="22d86-192">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22d86-192">Defaults to TRUE.</span></span> <span data-ttu-id="22d86-193">Wenn diese Option deaktiviert ist, kann der Benutzer nicht mehr mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über die ZoomFactor-API eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="22d86-193">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control will be disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control will be enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="22d86-194">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-194">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="22d86-195">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-195">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="22d86-196">öffentliche HRESULT- [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-196">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="22d86-197">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-197">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="22d86-198">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-198">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="22d86-199">Public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-199">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="22d86-200">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-200">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="22d86-201">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-201">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="22d86-202">Public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-202">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="22d86-203">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="22d86-203">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="22d86-204">Festlegen der AreRemoteObjectsAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-204">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="22d86-205">öffentliche HRESULT- [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(bool Allowed)</span><span class="sxs-lookup"><span data-stu-id="22d86-205">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="22d86-206">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-206">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="22d86-207">Festlegen der IsBuiltInErrorPageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-207">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="22d86-208">öffentliche HRESULT- [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-208">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="22d86-209">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-209">put_IsScriptEnabled</span></span> 

<span data-ttu-id="22d86-210">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-210">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="22d86-211">Public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-211">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="22d86-212">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-212">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="22d86-213">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-213">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="22d86-214">Public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-214">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="22d86-215">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-215">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="22d86-216">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-216">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="22d86-217">Public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-217">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="22d86-218">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="22d86-218">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="22d86-219">Festlegen der IsZoomControlEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d86-219">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="22d86-220">öffentliche HRESULT- [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="22d86-220">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

