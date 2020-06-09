---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b1cf72e967bde8d76ab345e37c1adc090af5d77d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698880"
---
# <span data-ttu-id="60308-104">Microsoft. Web. WebView2. Core. CoreWebView2Settings Klasse</span><span class="sxs-lookup"><span data-stu-id="60308-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

<span data-ttu-id="60308-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="60308-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="60308-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="60308-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="60308-107">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="60308-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="60308-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="60308-108">Summary</span></span>

 <span data-ttu-id="60308-109">Member</span><span class="sxs-lookup"><span data-stu-id="60308-109">Members</span></span>                        | <span data-ttu-id="60308-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="60308-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="60308-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="60308-112">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="60308-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="60308-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="60308-114">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="60308-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="60308-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="60308-116">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="60308-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="60308-117">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="60308-117">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="60308-118">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="60308-118">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="60308-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="60308-120">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="60308-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="60308-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="60308-122">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="60308-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="60308-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="60308-124">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="60308-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="60308-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="60308-126">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="60308-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="60308-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="60308-128">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="60308-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="60308-129">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="60308-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="60308-130">Member</span><span class="sxs-lookup"><span data-stu-id="60308-130">Members</span></span>

#### <span data-ttu-id="60308-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="60308-132">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="60308-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="60308-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="60308-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="60308-134">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60308-134">Defaults to TRUE.</span></span>

#### <span data-ttu-id="60308-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="60308-136">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="60308-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="60308-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="60308-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="60308-138">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="60308-138">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="60308-139">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="60308-139">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="60308-140">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-140">AreDevToolsEnabled</span></span> 

<span data-ttu-id="60308-141">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="60308-141">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="60308-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="60308-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="60308-143">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="60308-143">It is true by default.</span></span>

#### <span data-ttu-id="60308-144">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="60308-144">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="60308-145">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="60308-145">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="60308-146">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="60308-146">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="60308-147">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60308-147">Defaults to TRUE.</span></span>

#### <span data-ttu-id="60308-148">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-148">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="60308-149">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="60308-149">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="60308-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="60308-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="60308-151">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60308-151">Defaults to TRUE.</span></span> <span data-ttu-id="60308-152">Wenn diese Option deaktiviert ist, wird leere Seite angezeigt, wenn ein verwandter Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="60308-152">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="60308-153">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-153">IsScriptEnabled</span></span> 

<span data-ttu-id="60308-154">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="60308-154">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="60308-155">public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="60308-155">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="60308-156">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="60308-156">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="60308-157">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="60308-157">It is true by default.</span></span>

#### <span data-ttu-id="60308-158">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-158">IsStatusBarEnabled</span></span> 

<span data-ttu-id="60308-159">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="60308-159">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="60308-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="60308-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="60308-161">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="60308-161">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="60308-162">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="60308-162">It is true by default.</span></span>

#### <span data-ttu-id="60308-163">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-163">IsWebMessageEnabled</span></span> 

<span data-ttu-id="60308-164">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="60308-164">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="60308-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="60308-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="60308-166">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="60308-166">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="60308-167">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="60308-167">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="60308-168">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="60308-168">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="60308-169">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="60308-169">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="60308-170">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="60308-170">It is true by default.</span></span>

#### <span data-ttu-id="60308-171">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="60308-171">IsZoomControlEnabled</span></span> 

<span data-ttu-id="60308-172">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="60308-172">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="60308-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="60308-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="60308-174">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60308-174">Defaults to TRUE.</span></span> <span data-ttu-id="60308-175">Wenn diese Option deaktiviert ist, kann der Benutzer nicht mehr mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über die ZoomFactor-API eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="60308-175">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

