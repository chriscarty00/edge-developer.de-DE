---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6adc494c63d0bd7adc2fd578fcb877e0bf75307f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879366"
---
# <span data-ttu-id="c0fd4-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Settings Klasse</span><span class="sxs-lookup"><span data-stu-id="c0fd4-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

> [!NOTE]
> <span data-ttu-id="c0fd4-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c0fd4-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="c0fd4-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="c0fd4-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c0fd4-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c0fd4-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="c0fd4-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c0fd4-109">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-109">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="c0fd4-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c0fd4-110">Summary</span></span>

 <span data-ttu-id="c0fd4-111">Member</span><span class="sxs-lookup"><span data-stu-id="c0fd4-111">Members</span></span>                        | <span data-ttu-id="c0fd4-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c0fd4-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0fd4-113">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-113">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="c0fd4-114">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-114">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="c0fd4-115">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-115">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="c0fd4-116">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-116">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="c0fd4-117">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-117">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="c0fd4-118">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-118">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="c0fd4-119">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c0fd4-119">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="c0fd4-120">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-120">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="c0fd4-121">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-121">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="c0fd4-122">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-122">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="c0fd4-123">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-123">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="c0fd4-124">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-124">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="c0fd4-125">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-125">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="c0fd4-126">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="c0fd4-127">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-127">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="c0fd4-128">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-128">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="c0fd4-129">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-129">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="c0fd4-130">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-130">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="c0fd4-131">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-131">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="c0fd4-132">Member</span><span class="sxs-lookup"><span data-stu-id="c0fd4-132">Members</span></span>

#### <span data-ttu-id="c0fd4-133">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-133">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="c0fd4-134">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-134">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="c0fd4-135">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="c0fd4-135">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="c0fd4-136">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-136">Defaults to TRUE.</span></span>

#### <span data-ttu-id="c0fd4-137">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-137">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="c0fd4-138">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-138">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="c0fd4-139">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="c0fd4-139">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="c0fd4-140">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="c0fd4-140">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="c0fd4-141">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-141">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="c0fd4-142">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-142">AreDevToolsEnabled</span></span> 

<span data-ttu-id="c0fd4-143">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-143">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="c0fd4-144">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="c0fd4-144">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="c0fd4-145">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-145">It is true by default.</span></span>

#### <span data-ttu-id="c0fd4-146">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c0fd4-146">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="c0fd4-147">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-147">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="c0fd4-148">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="c0fd4-148">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="c0fd4-149">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-149">Defaults to TRUE.</span></span>

#### <span data-ttu-id="c0fd4-150">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-150">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="c0fd4-151">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-151">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="c0fd4-152">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="c0fd4-152">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="c0fd4-153">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-153">Defaults to TRUE.</span></span> <span data-ttu-id="c0fd4-154">Wenn diese Option deaktiviert ist, wird leere Seite angezeigt, wenn ein verwandter Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-154">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="c0fd4-155">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-155">IsScriptEnabled</span></span> 

<span data-ttu-id="c0fd4-156">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-156">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="c0fd4-157">public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="c0fd4-157">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="c0fd4-158">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-158">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="c0fd4-159">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-159">It is true by default.</span></span>

#### <span data-ttu-id="c0fd4-160">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-160">IsStatusBarEnabled</span></span> 

<span data-ttu-id="c0fd4-161">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-161">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="c0fd4-162">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="c0fd4-162">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="c0fd4-163">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-163">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="c0fd4-164">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-164">It is true by default.</span></span>

#### <span data-ttu-id="c0fd4-165">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-165">IsWebMessageEnabled</span></span> 

<span data-ttu-id="c0fd4-166">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-166">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="c0fd4-167">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="c0fd4-167">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="c0fd4-168">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="c0fd4-168">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="c0fd4-169">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="c0fd4-169">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="c0fd4-170">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-170">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="c0fd4-171">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-171">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="c0fd4-172">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-172">It is true by default.</span></span>

#### <span data-ttu-id="c0fd4-173">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c0fd4-173">IsZoomControlEnabled</span></span> 

<span data-ttu-id="c0fd4-174">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-174">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="c0fd4-175">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="c0fd4-175">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="c0fd4-176">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-176">Defaults to TRUE.</span></span> <span data-ttu-id="c0fd4-177">Wenn diese Option deaktiviert ist, kann der Benutzer nicht mehr mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über die ZoomFactor-API eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-177">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

