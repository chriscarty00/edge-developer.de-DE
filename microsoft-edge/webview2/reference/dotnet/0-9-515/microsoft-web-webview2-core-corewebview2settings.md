---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 519ef71db87d49aaf5a8a80970ff0cda61dfebbf
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653803"
---
# <span data-ttu-id="782e6-104">Microsoft. Web. WebView2. Core. CoreWebView2Settings Klasse</span><span class="sxs-lookup"><span data-stu-id="782e6-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

<span data-ttu-id="782e6-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="782e6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="782e6-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="782e6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="782e6-107">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="782e6-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="782e6-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="782e6-108">Summary</span></span>

 <span data-ttu-id="782e6-109">Member</span><span class="sxs-lookup"><span data-stu-id="782e6-109">Members</span></span>                        | <span data-ttu-id="782e6-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="782e6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="782e6-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="782e6-112">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="782e6-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="782e6-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="782e6-114">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="782e6-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="782e6-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="782e6-116">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="782e6-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="782e6-117">AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="782e6-117">AreRemoteObjectsAllowed</span></span>](#areremoteobjectsallowed) | <span data-ttu-id="782e6-118">Die AreRemoteObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Remoteobjekten über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="782e6-118">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="782e6-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="782e6-120">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="782e6-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="782e6-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="782e6-122">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="782e6-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="782e6-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="782e6-124">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="782e6-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="782e6-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="782e6-126">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="782e6-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="782e6-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="782e6-128">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="782e6-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="782e6-129">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="782e6-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="782e6-130">Member</span><span class="sxs-lookup"><span data-stu-id="782e6-130">Members</span></span>

#### <span data-ttu-id="782e6-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="782e6-132">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="782e6-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="782e6-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="782e6-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="782e6-134">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="782e6-134">Defaults to TRUE.</span></span>

#### <span data-ttu-id="782e6-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="782e6-136">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="782e6-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="782e6-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="782e6-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="782e6-138">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="782e6-138">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="782e6-139">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="782e6-139">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="782e6-140">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-140">AreDevToolsEnabled</span></span> 

<span data-ttu-id="782e6-141">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="782e6-141">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="782e6-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="782e6-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="782e6-143">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="782e6-143">It is true by default.</span></span>

#### <span data-ttu-id="782e6-144">AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="782e6-144">AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="782e6-145">Die AreRemoteObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Remoteobjekten über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="782e6-145">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="782e6-146">public bool [AreRemoteObjectsAllowed](#areremoteobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="782e6-146">public bool [AreRemoteObjectsAllowed](#areremoteobjectsallowed)</span></span>

<span data-ttu-id="782e6-147">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="782e6-147">Defaults to TRUE.</span></span>

#### <span data-ttu-id="782e6-148">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-148">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="782e6-149">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="782e6-149">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="782e6-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="782e6-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="782e6-151">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="782e6-151">Defaults to TRUE.</span></span> <span data-ttu-id="782e6-152">Wenn diese Option deaktiviert ist, wird leere Seite angezeigt, wenn ein verwandter Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="782e6-152">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="782e6-153">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-153">IsScriptEnabled</span></span> 

<span data-ttu-id="782e6-154">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="782e6-154">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="782e6-155">public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="782e6-155">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="782e6-156">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="782e6-156">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="782e6-157">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="782e6-157">It is true by default.</span></span>

#### <span data-ttu-id="782e6-158">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-158">IsStatusBarEnabled</span></span> 

<span data-ttu-id="782e6-159">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="782e6-159">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="782e6-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="782e6-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="782e6-161">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="782e6-161">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="782e6-162">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="782e6-162">It is true by default.</span></span>

#### <span data-ttu-id="782e6-163">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-163">IsWebMessageEnabled</span></span> 

<span data-ttu-id="782e6-164">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="782e6-164">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="782e6-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="782e6-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="782e6-166">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="782e6-166">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="782e6-167">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="782e6-167">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="782e6-168">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="782e6-168">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="782e6-169">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="782e6-169">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="782e6-170">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="782e6-170">It is true by default.</span></span>

#### <span data-ttu-id="782e6-171">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="782e6-171">IsZoomControlEnabled</span></span> 

<span data-ttu-id="782e6-172">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="782e6-172">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="782e6-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="782e6-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="782e6-174">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="782e6-174">Defaults to TRUE.</span></span> <span data-ttu-id="782e6-175">Wenn diese Option deaktiviert ist, kann der Benutzer nicht mehr mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über die ZoomFactor-API eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="782e6-175">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

