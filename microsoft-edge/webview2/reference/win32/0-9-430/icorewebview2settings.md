---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 70ccef9e99b3649ceca49b736570ba416cf73ebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883987"
---
# <span data-ttu-id="04bb6-104">0.9.430-Interface-ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="04bb6-104">0.9.430 - interface ICoreWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="04bb6-105">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="04bb6-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="04bb6-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="04bb6-106">Summary</span></span>

 <span data-ttu-id="04bb6-107">Member</span><span class="sxs-lookup"><span data-stu-id="04bb6-107">Members</span></span>                        | <span data-ttu-id="04bb6-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="04bb6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="04bb6-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="04bb6-110">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="04bb6-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="04bb6-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="04bb6-112">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="04bb6-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="04bb6-114">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="04bb6-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="04bb6-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="04bb6-116">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="04bb6-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="04bb6-118">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="04bb6-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="04bb6-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="04bb6-120">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="04bb6-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="04bb6-122">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="04bb6-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="04bb6-123">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-123">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="04bb6-124">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-124">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="04bb6-125">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-125">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="04bb6-126">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="04bb6-126">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="04bb6-127">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-127">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="04bb6-128">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-128">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="04bb6-129">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-129">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="04bb6-130">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="04bb6-130">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="04bb6-131">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-131">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="04bb6-132">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-132">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="04bb6-133">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="04bb6-133">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="04bb6-134">Die AreRemoteObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Remoteobjekten über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="04bb6-134">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="04bb6-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="04bb6-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="04bb6-136">Festlegen der AreRemoteObjectsAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="04bb6-137">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-137">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="04bb6-138">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="04bb6-138">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="04bb6-139">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-139">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="04bb6-140">Festlegen der IsZoomControlEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-140">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="04bb6-141">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="04bb6-141">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="04bb6-142">Member</span><span class="sxs-lookup"><span data-stu-id="04bb6-142">Members</span></span>

#### <span data-ttu-id="04bb6-143">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-143">get_IsScriptEnabled</span></span> 

<span data-ttu-id="04bb6-144">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="04bb6-144">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="04bb6-145">Public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-145">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="04bb6-146">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="04bb6-146">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="04bb6-147">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="04bb6-147">It is true by default.</span></span>

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

#### <span data-ttu-id="04bb6-148">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-148">put_IsScriptEnabled</span></span> 

<span data-ttu-id="04bb6-149">Festlegen der IsScriptEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-149">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="04bb6-150">Public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-150">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="04bb6-151">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-151">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="04bb6-152">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="04bb6-152">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="04bb6-153">Public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-153">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="04bb6-154">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="04bb6-154">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="04bb6-155">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="04bb6-155">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="04bb6-156">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="04bb6-156">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="04bb6-157">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="04bb6-157">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="04bb6-158">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="04bb6-158">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="04bb6-159">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-159">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="04bb6-160">Festlegen der IsWebMessageEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-160">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="04bb6-161">Public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-161">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="04bb6-162">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-162">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="04bb6-163">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="04bb6-163">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="04bb6-164">Public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-164">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="04bb6-165">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="04bb6-165">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="04bb6-166">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="04bb6-166">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="04bb6-167">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-167">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="04bb6-168">Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-168">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="04bb6-169">Public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-169">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="04bb6-170">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-170">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="04bb6-171">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="04bb6-171">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="04bb6-172">Public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-172">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="04bb6-173">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="04bb6-173">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="04bb6-174">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="04bb6-174">It is true by default.</span></span>

#### <span data-ttu-id="04bb6-175">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-175">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="04bb6-176">Festlegen der IsStatusBarEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-176">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="04bb6-177">Public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-177">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="04bb6-178">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-178">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="04bb6-179">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="04bb6-179">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="04bb6-180">Public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-180">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="04bb6-181">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="04bb6-181">It is true by default.</span></span>

#### <span data-ttu-id="04bb6-182">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-182">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="04bb6-183">Festlegen der AreDevToolsEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-183">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="04bb6-184">Public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-184">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="04bb6-185">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-185">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="04bb6-186">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="04bb6-186">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="04bb6-187">öffentliche HRESULT- [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-187">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="04bb6-188">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04bb6-188">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="04bb6-189">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-189">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="04bb6-190">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-190">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="04bb6-191">öffentliche HRESULT- [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-191">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="04bb6-192">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="04bb6-192">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="04bb6-193">Die AreRemoteObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Remoteobjekten über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="04bb6-193">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="04bb6-194">öffentliche HRESULT- [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(bool \* zulässig)</span><span class="sxs-lookup"><span data-stu-id="04bb6-194">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="04bb6-195">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04bb6-195">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="04bb6-196">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="04bb6-196">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="04bb6-197">Festlegen der AreRemoteObjectsAllowed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-197">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="04bb6-198">öffentliche HRESULT- [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(bool Allowed)</span><span class="sxs-lookup"><span data-stu-id="04bb6-198">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="04bb6-199">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-199">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="04bb6-200">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="04bb6-200">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="04bb6-201">öffentliche HRESULT- [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-201">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="04bb6-202">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04bb6-202">Defaults to TRUE.</span></span> <span data-ttu-id="04bb6-203">Wenn diese Option deaktiviert ist, kann der Benutzer nicht mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über put_ZoomFactor-API eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="04bb6-203">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

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

#### <span data-ttu-id="04bb6-204">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="04bb6-204">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="04bb6-205">Festlegen der IsZoomControlEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04bb6-205">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="04bb6-206">öffentliche HRESULT- [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="04bb6-206">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

