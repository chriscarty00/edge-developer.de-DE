---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Settings
ms.openlocfilehash: 7ce831c3259aaede687a5f5bdf3e2a78fc9700a3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010838"
---
# <span data-ttu-id="00295-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Settings Klasse</span><span class="sxs-lookup"><span data-stu-id="00295-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="00295-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="00295-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="00295-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="00295-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="00295-107">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="00295-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="00295-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="00295-108">Summary</span></span>

 <span data-ttu-id="00295-109">Member</span><span class="sxs-lookup"><span data-stu-id="00295-109">Members</span></span>                        | <span data-ttu-id="00295-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="00295-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="00295-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="00295-112">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="00295-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="00295-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="00295-114">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="00295-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="00295-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="00295-116">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="00295-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="00295-117">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="00295-117">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="00295-118">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="00295-118">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="00295-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="00295-120">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="00295-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="00295-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="00295-122">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="00295-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="00295-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="00295-124">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="00295-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="00295-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="00295-126">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="00295-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="00295-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="00295-128">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="00295-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="00295-129">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="00295-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="00295-130">Member</span><span class="sxs-lookup"><span data-stu-id="00295-130">Members</span></span>

#### <span data-ttu-id="00295-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="00295-132">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="00295-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="00295-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="00295-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="00295-134">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00295-134">Defaults to TRUE.</span></span>

#### <span data-ttu-id="00295-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="00295-136">AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="00295-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="00295-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="00295-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="00295-138">Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="00295-138">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="00295-139">Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="00295-139">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="00295-140">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-140">AreDevToolsEnabled</span></span> 

<span data-ttu-id="00295-141">AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="00295-141">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="00295-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="00295-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="00295-143">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="00295-143">It is true by default.</span></span>

#### <span data-ttu-id="00295-144">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="00295-144">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="00295-145">Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="00295-145">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="00295-146">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="00295-146">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="00295-147">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00295-147">Defaults to TRUE.</span></span>

#### <span data-ttu-id="00295-148">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-148">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="00295-149">Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="00295-149">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="00295-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="00295-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="00295-151">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00295-151">Defaults to TRUE.</span></span> <span data-ttu-id="00295-152">Wenn diese Option deaktiviert ist, wird leere Seite angezeigt, wenn ein verwandter Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="00295-152">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="00295-153">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-153">IsScriptEnabled</span></span> 

<span data-ttu-id="00295-154">Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="00295-154">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="00295-155">public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="00295-155">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="00295-156">Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="00295-156">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="00295-157">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="00295-157">It is true by default.</span></span>

#### <span data-ttu-id="00295-158">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-158">IsStatusBarEnabled</span></span> 

<span data-ttu-id="00295-159">IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="00295-159">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="00295-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="00295-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="00295-161">Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="00295-161">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="00295-162">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="00295-162">It is true by default.</span></span>

#### <span data-ttu-id="00295-163">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-163">IsWebMessageEnabled</span></span> 

<span data-ttu-id="00295-164">Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="00295-164">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="00295-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="00295-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="00295-166">Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="00295-166">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="00295-167">Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="00295-167">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="00295-168">Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="00295-168">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="00295-169">Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen.</span><span class="sxs-lookup"><span data-stu-id="00295-169">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="00295-170">Standardmäßig ist dies der Fall.</span><span class="sxs-lookup"><span data-stu-id="00295-170">It is true by default.</span></span>

#### <span data-ttu-id="00295-171">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="00295-171">IsZoomControlEnabled</span></span> 

<span data-ttu-id="00295-172">Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="00295-172">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="00295-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="00295-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="00295-174">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00295-174">Defaults to TRUE.</span></span> <span data-ttu-id="00295-175">Wenn diese Option deaktiviert ist, kann der Benutzer nicht mehr mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über die ZoomFactor-API eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="00295-175">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

