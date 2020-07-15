---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Controller
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8e0f95f8346f4c4b60b6de2676503b79c743afcb
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880822"
---
# <span data-ttu-id="6d215-104">0.9.515-Interface-ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="6d215-104">0.9.515 - interface ICoreWebView2Controller</span></span> 

> [!NOTE]
> <span data-ttu-id="6d215-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6d215-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="6d215-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6d215-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Controller
  : public IUnknown
```

<span data-ttu-id="6d215-107">Diese Schnittstelle ist der Besitzer des CoreWebView2-Objekts und bietet Unterstützung für die Größenänderung, das ein-und ausblenden, die Fokussierung und andere Funktionen im Zusammenhang mit Fenster und Komposition.</span><span class="sxs-lookup"><span data-stu-id="6d215-107">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="6d215-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6d215-108">Summary</span></span>

 <span data-ttu-id="6d215-109">Member</span><span class="sxs-lookup"><span data-stu-id="6d215-109">Members</span></span>                        | <span data-ttu-id="6d215-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6d215-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6d215-111">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="6d215-111">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="6d215-112">Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-112">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="6d215-113">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-113">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="6d215-114">Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-114">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="6d215-115">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-115">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="6d215-116">Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-116">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="6d215-117">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="6d215-117">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="6d215-118">Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-118">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="6d215-119">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="6d215-119">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="6d215-120">Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-120">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="6d215-121">Schließen</span><span class="sxs-lookup"><span data-stu-id="6d215-121">Close</span></span>](#close) | <span data-ttu-id="6d215-122">Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.</span><span class="sxs-lookup"><span data-stu-id="6d215-122">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="6d215-123">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="6d215-123">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="6d215-124">Die WebView-Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="6d215-124">The webview bounds.</span></span>
[<span data-ttu-id="6d215-125">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="6d215-125">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="6d215-126">Ruft das CoreWebView2 ab, das diesem CoreWebView2Controller zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6d215-126">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>
[<span data-ttu-id="6d215-127">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="6d215-127">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="6d215-128">Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d215-128">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="6d215-129">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="6d215-129">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="6d215-130">Das übergeordnete Fenster, das von der APP bereitgestellt wird, die von dieser WebView zum Rendern von Inhalten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-130">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="6d215-131">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="6d215-131">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="6d215-132">Der Zoomfaktor für die WebView.</span><span class="sxs-lookup"><span data-stu-id="6d215-132">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="6d215-133">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-133">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="6d215-134">Verschieben des Fokus in WebView</span><span class="sxs-lookup"><span data-stu-id="6d215-134">Move focus into WebView.</span></span>
[<span data-ttu-id="6d215-135">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="6d215-135">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="6d215-136">Hierbei handelt es sich um eine Benachrichtigung, die sich von den Grenzen unterscheidet, die WebView das übergeordnete HWND (oder ein Vorgänger) verschoben hat.</span><span class="sxs-lookup"><span data-stu-id="6d215-136">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="6d215-137">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="6d215-137">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="6d215-138">Die Bounds-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d215-138">Set the Bounds property.</span></span>
[<span data-ttu-id="6d215-139">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="6d215-139">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="6d215-140">Festlegen der IsVisible-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d215-140">Set the IsVisible property.</span></span>
[<span data-ttu-id="6d215-141">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="6d215-141">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="6d215-142">Das übergeordnete Fenster für die WebView-Ansicht einrichten</span><span class="sxs-lookup"><span data-stu-id="6d215-142">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="6d215-143">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="6d215-143">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="6d215-144">Festlegen der ZoomFactor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d215-144">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="6d215-145">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="6d215-145">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="6d215-146">Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-146">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="6d215-147">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-147">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="6d215-148">Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-148">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="6d215-149">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-149">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="6d215-150">Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-150">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="6d215-151">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="6d215-151">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="6d215-152">Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-152">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="6d215-153">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="6d215-153">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="6d215-154">Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-154">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="6d215-155">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="6d215-155">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="6d215-156">Gleichzeitiges Aktualisieren von Begrenzungen und ZoomFactor-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d215-156">Update Bounds and ZoomFactor properties at the same time.</span></span>

<span data-ttu-id="6d215-157">Die CoreWebView2Controller besitzt den CoreWebView2, und wenn alle Verweise auf die CoreWebView2Controller verschwindet, wird die WebView geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6d215-157">The CoreWebView2Controller owns the CoreWebView2, and if all references to the CoreWebView2Controller go away, the WebView will be closed.</span></span>

## <span data-ttu-id="6d215-158">Member</span><span class="sxs-lookup"><span data-stu-id="6d215-158">Members</span></span>

#### <span data-ttu-id="6d215-159">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="6d215-159">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="6d215-160">Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-160">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="6d215-161">Public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-161">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6d215-162">AcceleratorKeyPressed wird ausgelöst, wenn eine Zugriffstasten-oder Tastenkombination gedrückt oder freigegeben wird, während die WebView fokussiert ist.</span><span class="sxs-lookup"><span data-stu-id="6d215-162">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="6d215-163">Ein Schlüssel wird in folgenden Fällen als Beschleuniger betrachtet:</span><span class="sxs-lookup"><span data-stu-id="6d215-163">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="6d215-164">STRG oder alt wird derzeit gehalten, oder</span><span class="sxs-lookup"><span data-stu-id="6d215-164">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="6d215-165">die Taste gedrückt wird einem Zeichen nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6d215-165">the pressed key does not map to a character.</span></span> <span data-ttu-id="6d215-166">Einige bestimmte Tasten gelten nie als Beschleuniger, wie etwa die UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="6d215-166">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="6d215-167">Die Escape-Taste wird immer als Beschleuniger angesehen.</span><span class="sxs-lookup"><span data-stu-id="6d215-167">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="6d215-168">Durch automatisch wiederholte Tastenereignisse, die durch das Drücken der Taste nach unten verursacht werden, wird dieses Ereignis ebenfalls ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6d215-168">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="6d215-169">Sie können diese filtern, indem Sie das Ereignis args ' KeyEventLParam oder PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="6d215-169">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="6d215-170">Im Fenstermodus wird dieser Ereignishandler synchron aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6d215-170">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="6d215-171">Bis Sie Handle () für die Ereignis-args aufrufen oder der Ereignishandler zurückgibt, wird der Browserprozess blockiert, und ausgehende prozessübergreifende com-Aufrufe schlagen mit RPC_E_CANTCALLOUT_ININPUTSYNCCALL fehl.</span><span class="sxs-lookup"><span data-stu-id="6d215-171">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="6d215-172">Allerdings funktionieren alle CoreWebView2-API-Methoden.</span><span class="sxs-lookup"><span data-stu-id="6d215-172">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="6d215-173">Im Fenstermodus wird der Ereignishandler asynchron aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6d215-173">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="6d215-174">Eine weitere Eingabe erreicht den Browser erst, wenn der Ereignishandler zurückgegeben oder Handle () aufgerufen wird, der Browserprozess selbst jedoch nicht blockiert wird und ausgehende com-Aufrufe normal funktionieren.</span><span class="sxs-lookup"><span data-stu-id="6d215-174">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="6d215-175">Es wird empfohlen, handle (true) so früh wie möglich aufzurufen, wenn Sie wissen, dass Sie die Zugriffstasten Taste behandeln möchten.</span><span class="sxs-lookup"><span data-stu-id="6d215-175">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_controller->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                COREWEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        COREWEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="6d215-176">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-176">add_GotFocus</span></span> 

<span data-ttu-id="6d215-177">Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-177">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="6d215-178">Public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-178">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6d215-179">GotFocus wird ausgelöst, wenn WebView den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="6d215-179">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="6d215-180">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-180">add_LostFocus</span></span> 

<span data-ttu-id="6d215-181">Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-181">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="6d215-182">Public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-182">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6d215-183">LostFocus wird ausgelöst, wenn WebView den Fokus verloren hat.</span><span class="sxs-lookup"><span data-stu-id="6d215-183">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="6d215-184">In dem Fall, in dem das MoveFocusRequested-Ereignis ausgelöst wird, liegt der Fokus weiterhin auf WebView, wenn das MoveFocusRequested-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-184">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="6d215-185">Der verlorene Fokus wird erst dann ausgelöst, wenn der app-Code oder die Standardaktion des MoveFocusRequested-Ereignisses den Fokus von WebView absetzen.</span><span class="sxs-lookup"><span data-stu-id="6d215-185">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="6d215-186">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="6d215-186">add_MoveFocusRequested</span></span> 

<span data-ttu-id="6d215-187">Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-187">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="6d215-188">Public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-188">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6d215-189">MoveFocusRequested wird ausgelöst, wenn der Benutzer versucht, die Tab-Taste aus der WebView zu ziehen.</span><span class="sxs-lookup"><span data-stu-id="6d215-189">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="6d215-190">Der Fokus der WebView wurde nicht geändert, wenn dieses Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-190">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_controller->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    COREWEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="6d215-191">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="6d215-191">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="6d215-192">Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d215-192">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="6d215-193">Public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-193">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6d215-194">Das Ereignis wird ausgelöst, wenn die ZoomFactor-Eigenschaft des WebView geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-194">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="6d215-195">Das Ereignis konnte ausgelöst werden, weil der Aufrufer die ZoomFactor-Eigenschaft geändert hat, oder weil der Benutzer den Zoom manuell geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6d215-195">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="6d215-196">Wenn Sie vom Aufrufer über die ZoomFactor-Eigenschaft geändert wird, wird der interne Zoomfaktor sofort aktualisiert, und es gibt kein ZoomFactorChanged-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6d215-196">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="6d215-197">WebView ordnet den zuletzt verwendeten Zoomfaktor für jede Website zu.</span><span class="sxs-lookup"><span data-stu-id="6d215-197">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="6d215-198">Daher ist es möglich, dass sich der Zoomfaktor ändert, wenn Sie zu einer anderen Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="6d215-198">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="6d215-199">Wenn sich der Zoomfaktor aufgrund dieser Änderung ändert, wird das ZoomFactorChanged-Ereignis direkt hinter dem ContentLoading-Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6d215-199">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_controller->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Controller* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="6d215-200">Schließen</span><span class="sxs-lookup"><span data-stu-id="6d215-200">Close</span></span> 

<span data-ttu-id="6d215-201">Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.</span><span class="sxs-lookup"><span data-stu-id="6d215-201">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="6d215-202">Public HRESULT [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="6d215-202">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="6d215-203">Beim Bereinigen der Browserinstanz werden die Ressourcen freigegeben, die die WebView-Ansicht auslösen.</span><span class="sxs-lookup"><span data-stu-id="6d215-203">Cleaning up the browser instance will release the resources powering the WebView.</span></span> <span data-ttu-id="6d215-204">Die Browserinstanz wird heruntergefahren, wenn keine anderen Webansichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d215-204">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="6d215-205">Nach dem Aufruf von Close werden alle Methodenaufrufe fehlschlagen, und die Ereignishandler werden nicht mehr ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6d215-205">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="6d215-206">Insbesondere gibt die WebView Ihre Verweise auf die Ereignishandler frei, wenn Close aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-206">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="6d215-207">Close wird implizit aufgerufen, wenn die CoreWebView2Controller den endgültigen Bezug verliert und zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-207">Close is implicitly called when the CoreWebView2Controller loses its final reference and is destructed.</span></span> <span data-ttu-id="6d215-208">Es empfiehlt sich jedoch, explizit Close aufzurufen, um einen zufälligen Zyklus von Verweisen zwischen WebView und app-Code zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6d215-208">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="6d215-209">Insbesondere wenn Sie einen Verweis auf die WebView in einem Ereignishandler aufzeichnen, erstellen Sie einen Referenz Zyklus zwischen WebView und dem Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="6d215-209">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="6d215-210">Durch das Aufrufen von Close wird dieser Zyklus unterbrochen, indem alle Ereignishandler freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6d215-210">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="6d215-211">Um dies zu vermeiden, empfiehlt es sich, sowohl explizit Close für die WebView zu verwenden als auch einen Verweis auf die WebView zu erfassen, um sicherzustellen, dass die WebView ordnungsgemäß bereinigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6d215-211">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_controller)
    {
        m_controller->Close();
        m_controller = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2-idl#createwebview2environmentwithoptions
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instances.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### <span data-ttu-id="6d215-212">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="6d215-212">get_Bounds</span></span> 

<span data-ttu-id="6d215-213">Die WebView-Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="6d215-213">The webview bounds.</span></span>

> <span data-ttu-id="6d215-214">öffentliche HRESULT- [get_Bounds](#get_bounds)(Rect \* bounds)</span><span class="sxs-lookup"><span data-stu-id="6d215-214">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="6d215-215">Begrenzungen sind relativ zum übergeordneten HWND.</span><span class="sxs-lookup"><span data-stu-id="6d215-215">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="6d215-216">Die APP hat zwei Möglichkeiten, um eine WebView-Position zu positionieren:</span><span class="sxs-lookup"><span data-stu-id="6d215-216">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="6d215-217">Erstellen Sie ein untergeordnetes HWND, das das übergeordnete HWND von WebView ist.</span><span class="sxs-lookup"><span data-stu-id="6d215-217">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="6d215-218">Positionieren Sie dieses Fenster, in dem sich die WebView befinden soll.</span><span class="sxs-lookup"><span data-stu-id="6d215-218">Position this window where the WebView should be.</span></span> <span data-ttu-id="6d215-219">Verwenden Sie in diesem Fall (0, 0) für die Bound's obere linke Ecke des Webviews (den Offset).</span><span class="sxs-lookup"><span data-stu-id="6d215-219">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="6d215-220">Verwenden Sie das oberste Fenster der App als übergeordnetes WebView-HWND.</span><span class="sxs-lookup"><span data-stu-id="6d215-220">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="6d215-221">Stellen Sie die Bound's-obere linke Ecke der WebView so ein, dass die WebView in der APP richtig positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="6d215-221">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="6d215-222">Die Werte der Bounds befinden sich im Koordinatenbereich des Hosts.</span><span class="sxs-lookup"><span data-stu-id="6d215-222">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="6d215-223">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="6d215-223">get_CoreWebView2</span></span> 

<span data-ttu-id="6d215-224">Ruft das CoreWebView2 ab, das diesem CoreWebView2Controller zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6d215-224">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>

> <span data-ttu-id="6d215-225">Public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="6d215-225">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="6d215-226">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="6d215-226">get_IsVisible</span></span> 

<span data-ttu-id="6d215-227">Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d215-227">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="6d215-228">öffentliche HRESULT- [get_IsVisible](#get_isvisible)(bool \* isVisible)</span><span class="sxs-lookup"><span data-stu-id="6d215-228">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="6d215-229">Wenn IsVisible auf "false" festgelegt ist, ist die WebView transparent und wird nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="6d215-229">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="6d215-230">Dies wirkt sich jedoch nicht auf das Fenster aus, das die WebView enthält (den HWND-Parameter, der an CreateCoreWebView2Controller übergeben wurde).</span><span class="sxs-lookup"><span data-stu-id="6d215-230">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Controller).</span></span> <span data-ttu-id="6d215-231">Wenn Sie möchten, dass das Fenster ebenfalls ausgeblendet wird, rufen Sie ShowWindow direkt zusätzlich zum Ändern der IsVisible-Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="6d215-231">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="6d215-232">WebView als untergeordnetes Fenster ruft keine Fenster Meldungen ab, wenn das oberste Fenster minimiert oder wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-232">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="6d215-233">Aus Leistungsgründen sollte Entwickler die IsVisible-Eigenschaft der WebView-Eigenschaft auf "false" festlegen, wenn das App-Fenster minimiert wird, und zurück zu "true", wenn das App-Fenster wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-233">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="6d215-234">Das App-Fenster kann dies tun, indem SC_MINIMIZE und SC_RESTORE Befehl beim empfangen WM_SYSCOMMAND Nachricht behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="6d215-234">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_controller->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_controller->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="6d215-235">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="6d215-235">get_ParentWindow</span></span> 

<span data-ttu-id="6d215-236">Das übergeordnete Fenster, das von der APP bereitgestellt wird, die von dieser WebView zum Rendern von Inhalten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-236">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="6d215-237">öffentliche HRESULT- [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="6d215-237">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="6d215-238">Diese API gibt zunächst das Fenster zurück, das an CreateCoreWebView2Controller übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-238">This API initially returns the window passed into CreateCoreWebView2Controller.</span></span>

#### <span data-ttu-id="6d215-239">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="6d215-239">get_ZoomFactor</span></span> 

<span data-ttu-id="6d215-240">Der Zoomfaktor für die WebView.</span><span class="sxs-lookup"><span data-stu-id="6d215-240">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="6d215-241">öffentliche HRESULT- [get_ZoomFactor](#get_zoomfactor)(Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="6d215-241">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="6d215-242">Beachten Sie, dass das Ändern des Zoomfaktors `window.innerWidth/innerHeight` zu einer Änderung des Seitenlayouts führen kann.</span><span class="sxs-lookup"><span data-stu-id="6d215-242">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="6d215-243">Ein Zoomfaktor, der vom Host durch Aufrufen von ZoomFactor angewendet wird, wird zum neuen Standardzoom für die WebView.</span><span class="sxs-lookup"><span data-stu-id="6d215-243">A zoom factor that is applied by the host by calling ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="6d215-244">Dieser Zoomfaktor gilt für alle Navigationselemente und der Zoomfaktor WebView wird zurückgegeben, wenn der Benutzer STRG + 0 drückt.</span><span class="sxs-lookup"><span data-stu-id="6d215-244">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="6d215-245">Wenn der Zoomfaktor vom Benutzer geändert wird (was im App-Empfang ZoomFactorChanged), gilt dieser Zoom nur für die aktuelle Seite.</span><span class="sxs-lookup"><span data-stu-id="6d215-245">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="6d215-246">Der Zoom eines Benutzers, der angewendet wird, ist nur für die aktuelle Seite vorgesehen und wird in einer Navigation zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6d215-246">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="6d215-247">Die Angabe einer ZoomFactor kleiner oder gleich 0 ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6d215-247">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="6d215-248">WebView verfügt auch über einen internen unterstützten Zoomfaktor Bereich.</span><span class="sxs-lookup"><span data-stu-id="6d215-248">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="6d215-249">Wenn sich ein angegebener Zoomfaktor außerhalb dieses Bereichs befindet, wird er normalisiert, sodass er innerhalb des Bereichs liegt, und ein ZoomFactorChanged-Ereignis wird für den tatsächlich angewendeten Zoomfaktor ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6d215-249">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="6d215-250">Wenn diese Bereichs Normalisierung erfolgt, meldet die ZoomFactor-Eigenschaft den Zoomfaktor, der während der vorherigen Änderung der ZoomFactor-Eigenschaft angegeben wird, bis das ZoomFactorChanged-Ereignis empfangen wird, nachdem WebView den normalisierten Zoomfaktor angewendet hat.</span><span class="sxs-lookup"><span data-stu-id="6d215-250">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="6d215-251">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-251">MoveFocus</span></span> 

<span data-ttu-id="6d215-252">Verschieben des Fokus in WebView</span><span class="sxs-lookup"><span data-stu-id="6d215-252">Move focus into WebView.</span></span>

> <span data-ttu-id="6d215-253">öffentliche HRESULT- [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON Grund)</span><span class="sxs-lookup"><span data-stu-id="6d215-253">public HRESULT [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON reason)</span></span>

<span data-ttu-id="6d215-254">WebView erhält den Fokus, und der Fokus wird auf das korrespondierende Element auf der Seite gesetzt, die in der WebView gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-254">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="6d215-255">Aus Programm Gründen wird der Fokus auf das zuvor fokussierte Element oder auf das Standardelement gesetzt, wenn kein zuvor fokussiertes Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6d215-255">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="6d215-256">Aus dem nächsten Grund wird der Fokus auf das erste Element gesetzt.</span><span class="sxs-lookup"><span data-stu-id="6d215-256">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="6d215-257">Aus vorherigen Gründen wird der Fokus auf das letzte Element gesetzt.</span><span class="sxs-lookup"><span data-stu-id="6d215-257">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="6d215-258">WebView kann auch den Fokus über die Benutzerinteraktion erhalten, wie das Klicken in WebView oder die Tab-Taste.</span><span class="sxs-lookup"><span data-stu-id="6d215-258">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="6d215-259">Für die Tab-Taste kann die APP MoveFocus mit der nächsten oder vorherigen aufrufen, um mit Tab und UMSCHALT + TAB auszurichten, wenn Sie beschließt, dass die WebView das nächste Tabbed-Element ist.</span><span class="sxs-lookup"><span data-stu-id="6d215-259">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="6d215-260">Oder die APP kann IsDialogMessage als Teil der Nachrichtenschleife aufrufen, damit die Plattform die Tab-Funktion automatisch verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="6d215-260">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="6d215-261">Die Plattform wird durch alle Fenster mit WS_TABSTOP gedreht.</span><span class="sxs-lookup"><span data-stu-id="6d215-261">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="6d215-262">Wenn die WebView den Fokus von IsDialogMessage erhält, wird der Fokus intern auf das erste oder letzte Element für Tab und UMSCHALT + TAB gesetzt.</span><span class="sxs-lookup"><span data-stu-id="6d215-262">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (size_t i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (size_t i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="6d215-263">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="6d215-263">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="6d215-264">Hierbei handelt es sich um eine Benachrichtigung, die sich von den Grenzen unterscheidet, die WebView das übergeordnete HWND (oder ein Vorgänger) verschoben hat.</span><span class="sxs-lookup"><span data-stu-id="6d215-264">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="6d215-265">Public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span><span class="sxs-lookup"><span data-stu-id="6d215-265">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="6d215-266">Dies ist für die Barrierefreiheit und bestimmte Dialogfelder in WebView erforderlich, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="6d215-266">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 
```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_controller->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="6d215-267">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="6d215-267">put_Bounds</span></span> 

<span data-ttu-id="6d215-268">Die Bounds-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d215-268">Set the Bounds property.</span></span>

> <span data-ttu-id="6d215-269">öffentliche HRESULT- [put_Bounds](#put_bounds)(Rect-Begrenzungen)</span><span class="sxs-lookup"><span data-stu-id="6d215-269">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_controller->put_Bounds(desiredBounds);
    if (m_compositionController)
    {
        POINT webViewOffset = {m_webViewBounds.left, m_webViewBounds.top};

        if (m_dcompDevice)
        {
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetX(float(webViewOffset.x)));
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetY(float(webViewOffset.y)));
            CHECK_FAILURE(m_dcompRootVisual->SetClip(
                {0, 0, float(webViewSize.cx), float(webViewSize.cy)}));
            CHECK_FAILURE(m_dcompDevice->Commit());
        }
        else if (m_wincompHelper)
        {
            m_wincompHelper->UpdateSizeAndPosition(webViewOffset, webViewSize);
        }
    }
}
```

#### <span data-ttu-id="6d215-270">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="6d215-270">put_IsVisible</span></span> 

<span data-ttu-id="6d215-271">Festlegen der IsVisible-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d215-271">Set the IsVisible property.</span></span>

> <span data-ttu-id="6d215-272">öffentliche HRESULT- [put_IsVisible](#put_isvisible)(bool isVisible)</span><span class="sxs-lookup"><span data-stu-id="6d215-272">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_controller->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_controller->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="6d215-273">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="6d215-273">put_ParentWindow</span></span> 

<span data-ttu-id="6d215-274">Das übergeordnete Fenster für die WebView-Ansicht einrichten</span><span class="sxs-lookup"><span data-stu-id="6d215-274">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="6d215-275">Public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="6d215-275">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="6d215-276">Dies bewirkt, dass die WebView das Fenster des neu bereitgestellten Fensters erneut übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6d215-276">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="6d215-277">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="6d215-277">put_ZoomFactor</span></span> 

<span data-ttu-id="6d215-278">Festlegen der ZoomFactor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d215-278">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="6d215-279">öffentliche HRESULT- [put_ZoomFactor](#put_zoomfactor)(Double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="6d215-279">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="6d215-280">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="6d215-280">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="6d215-281">Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-281">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="6d215-282">Public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-282">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6d215-283">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-283">remove_GotFocus</span></span> 

<span data-ttu-id="6d215-284">Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-284">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="6d215-285">Public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-285">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6d215-286">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="6d215-286">remove_LostFocus</span></span> 

<span data-ttu-id="6d215-287">Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-287">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="6d215-288">Public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-288">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6d215-289">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="6d215-289">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="6d215-290">Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-290">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="6d215-291">Public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-291">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6d215-292">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="6d215-292">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="6d215-293">Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d215-293">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="6d215-294">Public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6d215-294">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6d215-295">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="6d215-295">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="6d215-296">Gleichzeitiges Aktualisieren von Begrenzungen und ZoomFactor-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d215-296">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="6d215-297">öffentliche HRESULT- [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(Rect-Begrenzungen, Doppel ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="6d215-297">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds, double zoomFactor)</span></span>

<span data-ttu-id="6d215-298">Dieser Vorgang ist aus der Perspektive des Hosts atomar.</span><span class="sxs-lookup"><span data-stu-id="6d215-298">This operation is atomic from the host's perspective.</span></span> <span data-ttu-id="6d215-299">Nach der Rückgabe von dieser Funktion werden die Bounds-Eigenschaft und die ZoomFactor-Eigenschaft beide aktualisiert, wenn die Funktion erfolgreich ist, oder keine wird aktualisiert, wenn die Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6d215-299">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="6d215-300">Wenn Grenz-und ZoomFactor sowohl auf der gleichen Skala aktualisiert werden (d. h., dass die Begrenzungen und ZoomFactor beide verdoppelt werden), wird der Seite keine Änderung in Window. InnereBreite/InnereHoehe angezeigt, und die WebView rendert den Inhalt mit der neuen Größe und zoomt ohne zwischen Renderings.</span><span class="sxs-lookup"><span data-stu-id="6d215-300">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="6d215-301">Diese Funktion kann auch verwendet werden, um nur eine von ZoomFactor oder Begrenzungen zu aktualisieren, indem der neue Wert für einen und der aktuelle Wert für den anderen übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d215-301">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_controller->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_controller->SetBoundsAndZoomFactor(bounds, scale);
}
```

