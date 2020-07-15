---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2Settings
ms.openlocfilehash: 24a1e06be83fbb5c510c455e80c52b7165dabcde
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879590"
---
# <span data-ttu-id="07f5b-104">Schnittstellen ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="07f5b-104">interface ICoreWebView2Settings</span></span> 

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="07f5b-105">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="07f5b-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="07f5b-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="07f5b-106">Summary</span></span>

 <span data-ttu-id="07f5b-107">Member</span><span class="sxs-lookup"><span data-stu-id="07f5b-107">Members</span></span>                        | <span data-ttu-id="07f5b-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="07f5b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="07f5b-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="07f5b-110">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="07f5b-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="07f5b-111">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-111">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="07f5b-112">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="07f5b-112">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="07f5b-113">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-113">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="07f5b-114">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="07f5b-114">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="07f5b-115">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="07f5b-115">get_AreHostObjectsAllowed</span></span>](#get_arehostobjectsallowed) | <span data-ttu-id="07f5b-116">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="07f5b-116">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="07f5b-117">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-117">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="07f5b-118">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="07f5b-118">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="07f5b-119">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-119">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="07f5b-120">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="07f5b-120">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="07f5b-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="07f5b-122">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="07f5b-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="07f5b-123">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-123">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="07f5b-124">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="07f5b-124">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="07f5b-125">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-125">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="07f5b-126">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="07f5b-126">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="07f5b-127">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-127">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="07f5b-128">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-128">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="07f5b-129">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-129">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="07f5b-130">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-130">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="07f5b-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="07f5b-132">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-132">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="07f5b-133">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="07f5b-133">put_AreHostObjectsAllowed</span></span>](#put_arehostobjectsallowed) | <span data-ttu-id="07f5b-134">Festlegen der AreHostObjectsAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-134">Set the AreHostObjectsAllowed property.</span></span>
[<span data-ttu-id="07f5b-135">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-135">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="07f5b-136">Festlegen der IsBuiltInErrorPageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-136">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="07f5b-137">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-137">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="07f5b-138">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-138">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="07f5b-139">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-139">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="07f5b-140">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-140">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="07f5b-141">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-141">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="07f5b-142">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-142">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="07f5b-143">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-143">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="07f5b-144">Festlegen der IsZoomControlEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-144">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="07f5b-145">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="07f5b-145">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="07f5b-146">Member</span><span class="sxs-lookup"><span data-stu-id="07f5b-146">Members</span></span>

#### <span data-ttu-id="07f5b-147">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-147">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="07f5b-148">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="07f5b-148">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="07f5b-149">öffentliche HRESULT- [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-149">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="07f5b-150">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07f5b-150">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="07f5b-151">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-151">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="07f5b-152">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="07f5b-152">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="07f5b-153">Public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-153">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="07f5b-154">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="07f5b-154">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="07f5b-155">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="07f5b-155">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="07f5b-156">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-156">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="07f5b-157">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="07f5b-157">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="07f5b-158">Public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-158">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="07f5b-159">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="07f5b-159">It is true by default.</span></span>

#### <span data-ttu-id="07f5b-160">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="07f5b-160">get_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="07f5b-161">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="07f5b-161">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="07f5b-162">öffentliche HRESULT- [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(bool \* zulässig)</span><span class="sxs-lookup"><span data-stu-id="07f5b-162">public HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="07f5b-163">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07f5b-163">Defaults to TRUE.</span></span>

```cpp
            BOOL allowHostObjects;
            CHECK_FAILURE(m_settings->get_AreHostObjectsAllowed(&allowHostObjects));
            if (allowHostObjects)
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to host objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to host objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="07f5b-164">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-164">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="07f5b-165">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="07f5b-165">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="07f5b-166">öffentliche HRESULT- [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-166">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="07f5b-167">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07f5b-167">Defaults to TRUE.</span></span> <span data-ttu-id="07f5b-168">Wenn diese Option deaktiviert ist, wird leere Seite angezeigt, wenn ein verwandter Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="07f5b-168">When disabled, blank page will be shown when related error happens.</span></span>

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

#### <span data-ttu-id="07f5b-169">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-169">get_IsScriptEnabled</span></span> 

<span data-ttu-id="07f5b-170">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="07f5b-170">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="07f5b-171">Public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-171">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="07f5b-172">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="07f5b-172">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="07f5b-173">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="07f5b-173">It is true by default.</span></span>

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

#### <span data-ttu-id="07f5b-174">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-174">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="07f5b-175">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="07f5b-175">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="07f5b-176">Public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-176">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="07f5b-177">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="07f5b-177">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="07f5b-178">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="07f5b-178">It is true by default.</span></span>

#### <span data-ttu-id="07f5b-179">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-179">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="07f5b-180">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="07f5b-180">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="07f5b-181">Public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-181">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="07f5b-182">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="07f5b-182">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="07f5b-183">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="07f5b-183">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="07f5b-184">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="07f5b-184">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="07f5b-185">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="07f5b-185">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="07f5b-186">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="07f5b-186">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="07f5b-187">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-187">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="07f5b-188">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="07f5b-188">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="07f5b-189">öffentliche HRESULT- [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-189">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="07f5b-190">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07f5b-190">Defaults to TRUE.</span></span> <span data-ttu-id="07f5b-191">Wenn diese Option deaktiviert ist, kann der Benutzer nicht mehr mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über die ZoomFactor-API eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="07f5b-191">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

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

#### <span data-ttu-id="07f5b-192">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-192">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="07f5b-193">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-193">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="07f5b-194">öffentliche HRESULT- [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-194">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="07f5b-195">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-195">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="07f5b-196">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-196">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="07f5b-197">Public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-197">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="07f5b-198">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-198">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="07f5b-199">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-199">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="07f5b-200">Public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-200">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="07f5b-201">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="07f5b-201">put_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="07f5b-202">Festlegen der AreHostObjectsAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-202">Set the AreHostObjectsAllowed property.</span></span>

> <span data-ttu-id="07f5b-203">öffentliche HRESULT- [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)(bool Allowed)</span><span class="sxs-lookup"><span data-stu-id="07f5b-203">public HRESULT [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="07f5b-204">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-204">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="07f5b-205">Festlegen der IsBuiltInErrorPageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-205">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="07f5b-206">öffentliche HRESULT- [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-206">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="07f5b-207">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-207">put_IsScriptEnabled</span></span> 

<span data-ttu-id="07f5b-208">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-208">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="07f5b-209">Public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-209">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="07f5b-210">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-210">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="07f5b-211">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-211">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="07f5b-212">Public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-212">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="07f5b-213">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-213">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="07f5b-214">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-214">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="07f5b-215">Public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-215">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="07f5b-216">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="07f5b-216">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="07f5b-217">Festlegen der IsZoomControlEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07f5b-217">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="07f5b-218">öffentliche HRESULT- [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="07f5b-218">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

