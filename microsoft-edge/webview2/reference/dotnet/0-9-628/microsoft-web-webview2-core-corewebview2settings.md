---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Settings
ms.openlocfilehash: 87b78956c29dac74bd023556a8c495222d248e9f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012051"
---
# <span data-ttu-id="ba002-104">Microsoft. Web. WebView2. Core. CoreWebView2Settings Klasse</span><span class="sxs-lookup"><span data-stu-id="ba002-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

<span data-ttu-id="ba002-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ba002-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ba002-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="ba002-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ba002-107">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="ba002-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="ba002-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ba002-108">Summary</span></span>

 <span data-ttu-id="ba002-109">Member</span><span class="sxs-lookup"><span data-stu-id="ba002-109">Members</span></span>                        | <span data-ttu-id="ba002-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ba002-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ba002-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="ba002-112">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ba002-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>
[<span data-ttu-id="ba002-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="ba002-114">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba002-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="ba002-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="ba002-116">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ba002-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="ba002-117">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ba002-117">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="ba002-118">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba002-118">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>
[<span data-ttu-id="ba002-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="ba002-120">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ba002-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="ba002-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="ba002-122">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ba002-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="ba002-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="ba002-124">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ba002-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="ba002-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="ba002-126">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba002-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="ba002-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="ba002-128">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="ba002-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="ba002-129">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="ba002-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="ba002-130">Member</span><span class="sxs-lookup"><span data-stu-id="ba002-130">Members</span></span>

#### <span data-ttu-id="ba002-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="ba002-132">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ba002-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>

> <span data-ttu-id="ba002-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="ba002-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="ba002-134">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="ba002-134">It is true by default.</span></span>

#### <span data-ttu-id="ba002-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="ba002-136">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba002-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="ba002-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="ba002-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="ba002-138">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="ba002-138">If set to false, then WebView won't render the default JavaScript dialog box (Specifically those shown by the JavaScript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="ba002-139">Wenn Sie auf "true" festgelegt ist, kann auch das ScriptDialogOpening-Ereignis abonniert werden, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ba002-139">If set to true, one can also subscribe to ScriptDialogOpening event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span> <span data-ttu-id="ba002-140">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="ba002-140">It is true by default.</span></span>

#### <span data-ttu-id="ba002-141">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-141">AreDevToolsEnabled</span></span> 

<span data-ttu-id="ba002-142">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ba002-142">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="ba002-143">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="ba002-143">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="ba002-144">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="ba002-144">It is true by default.</span></span>

#### <span data-ttu-id="ba002-145">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ba002-145">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="ba002-146">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba002-146">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>

> <span data-ttu-id="ba002-147">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="ba002-147">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="ba002-148">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="ba002-148">It is true by default.</span></span>

#### <span data-ttu-id="ba002-149">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-149">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="ba002-150">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ba002-150">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="ba002-151">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="ba002-151">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="ba002-152">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="ba002-152">It is true by default.</span></span> <span data-ttu-id="ba002-153">Wenn diese Option deaktiviert ist, wird leere Seite angezeigt, wenn ein verwandter Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="ba002-153">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="ba002-154">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-154">IsScriptEnabled</span></span> 

<span data-ttu-id="ba002-155">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ba002-155">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="ba002-156">public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="ba002-156">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="ba002-157">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ba002-157">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="ba002-158">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="ba002-158">It is true by default.</span></span>

#### <span data-ttu-id="ba002-159">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-159">IsStatusBarEnabled</span></span> 

<span data-ttu-id="ba002-160">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ba002-160">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="ba002-161">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="ba002-161">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="ba002-162">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="ba002-162">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="ba002-163">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="ba002-163">It is true by default.</span></span>

#### <span data-ttu-id="ba002-164">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-164">IsWebMessageEnabled</span></span> 

<span data-ttu-id="ba002-165">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba002-165">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="ba002-166">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="ba002-166">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="ba002-167">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="ba002-167">If set to true, communication from the host to the WebView's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="ba002-168">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und das WebMessageReceived-Ereignis zulässig (Einzelheiten finden Sie in der WebMessageReceived-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="ba002-168">Communication from the WebView's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the WebMessageReceived event (see WebMessageReceived documentation for details).</span></span> <span data-ttu-id="ba002-169">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ba002-169">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="ba002-170">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="ba002-170">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="ba002-171">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="ba002-171">It is true by default.</span></span>

#### <span data-ttu-id="ba002-172">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ba002-172">IsZoomControlEnabled</span></span> 

<span data-ttu-id="ba002-173">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="ba002-173">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="ba002-174">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="ba002-174">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="ba002-175">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="ba002-175">It is true by default.</span></span> <span data-ttu-id="ba002-176">Wenn diese Option deaktiviert ist, kann der Benutzer nicht mehr mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über die ZoomFactor-API eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ba002-176">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

