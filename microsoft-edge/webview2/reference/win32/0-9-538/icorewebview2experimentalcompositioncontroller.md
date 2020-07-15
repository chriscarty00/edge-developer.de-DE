---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalCompositionController
ms.openlocfilehash: e2b16cfd9095d43eb01d7e6233da2857c12a04ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880031"
---
# <span data-ttu-id="494da-104">Schnittstellen ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="494da-104">interface ICoreWebView2ExperimentalCompositionController</span></span> 

> [!NOTE]
> <span data-ttu-id="494da-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="494da-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

<span data-ttu-id="494da-106">Diese Schnittstelle ist eine Erweiterung der ICoreWebView2Controller-Schnittstelle, um visuelles Hosting zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="494da-106">This interface is an extension of the ICoreWebView2Controller interface to support visual hosting.</span></span>

## <span data-ttu-id="494da-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="494da-107">Summary</span></span>

 <span data-ttu-id="494da-108">Member</span><span class="sxs-lookup"><span data-stu-id="494da-108">Members</span></span>                        | <span data-ttu-id="494da-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="494da-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="494da-110">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="494da-110">add_CursorChanged</span></span>](#add_cursorchanged) | <span data-ttu-id="494da-111">Fügen Sie einen Ereignishandler für das Cursor Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="494da-111">Add an event handler for the CursorChanged event.</span></span>
[<span data-ttu-id="494da-112">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="494da-112">CreateCoreWebView2PointerInfoFromPointerId</span></span>](#createcorewebview2pointerinfofrompointerid) | <span data-ttu-id="494da-113">Eine Hilfsfunktion zum Konvertieren einer vom System empfangenen Zeiger-Nr in eine [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="494da-113">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="494da-114">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="494da-114">get_Cursor</span></span>](#get_cursor) | <span data-ttu-id="494da-115">Der aktuelle Cursor, der von WebView als vorgesehen erachtet wird.</span><span class="sxs-lookup"><span data-stu-id="494da-115">The current cursor that WebView thinks it should be.</span></span>
[<span data-ttu-id="494da-116">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="494da-116">get_RootVisualTarget</span></span>](#get_rootvisualtarget) | <span data-ttu-id="494da-117">Die RootVisualTarget ist ein visuelles Element in der visuellen Struktur der Host-app.</span><span class="sxs-lookup"><span data-stu-id="494da-117">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>
[<span data-ttu-id="494da-118">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="494da-118">get_UIAProvider</span></span>](#get_uiaprovider) | <span data-ttu-id="494da-119">Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die WebView zurück.</span><span class="sxs-lookup"><span data-stu-id="494da-119">Returns the UI Automation Provider for the WebView.</span></span>
[<span data-ttu-id="494da-120">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="494da-120">put_RootVisualTarget</span></span>](#put_rootvisualtarget) | <span data-ttu-id="494da-121">Festlegen der RootVisualTarget-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="494da-121">Set the RootVisualTarget property.</span></span>
[<span data-ttu-id="494da-122">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="494da-122">remove_CursorChanged</span></span>](#remove_cursorchanged) | <span data-ttu-id="494da-123">Entfernen Sie einen Ereignishandler, der zuvor mit add_CursorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="494da-123">Remove an event handler previously added with add_CursorChanged.</span></span>
[<span data-ttu-id="494da-124">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="494da-124">SendMouseInput</span></span>](#sendmouseinput) | <span data-ttu-id="494da-125">Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL oder COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL ist, gibt mouseData den Umfang der Mausradbewegung an.</span><span class="sxs-lookup"><span data-stu-id="494da-125">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>
[<span data-ttu-id="494da-126">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="494da-126">SendPointerInput</span></span>](#sendpointerinput) | <span data-ttu-id="494da-127">SendPointerInput akzeptiert Fingereingabe-oder Stiftzeiger Eingaben von Typen, die in COREWEBVIEW2_POINTER_EVENT_KIND definiert sind.</span><span class="sxs-lookup"><span data-stu-id="494da-127">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>
[<span data-ttu-id="494da-128">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="494da-128">COREWEBVIEW2_MATRIX_4X4</span></span>](#corewebview2_matrix_4x4) | <span data-ttu-id="494da-129">Matrix, die eine 3D-Transformation darstellt.</span><span class="sxs-lookup"><span data-stu-id="494da-129">Matrix that represents a 3D transform.</span></span>
[<span data-ttu-id="494da-130">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="494da-130">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span>](#corewebview2_mouse_event_kind) | <span data-ttu-id="494da-131">Maus Ereignistyp, der von SendMouseInput verwendet wird, um den Typ des Mausereignisses zu übermitteln, das an WebView gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="494da-131">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>
[<span data-ttu-id="494da-132">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="494da-132">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span>](#corewebview2_mouse_event_virtual_keys) | <span data-ttu-id="494da-133">Virtuelle Mausereignis Tasten, die einem COREWEBVIEW2_MOUSE_EVENT_KIND für SendMouseInput zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="494da-133">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>
[<span data-ttu-id="494da-134">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="494da-134">COREWEBVIEW2_POINTER_EVENT_KIND</span></span>](#corewebview2_pointer_event_kind) | <span data-ttu-id="494da-135">Zeiger Ereignistyp, der von SendPointerInput verwendet wird, um den Typ des Zeiger Ereignisses zu vermitteln, das an WebView gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="494da-135">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

<span data-ttu-id="494da-136">Ein Objekt, das die ICoreWebView2ExperimentalCompositionController-Schnittstelle implementiert, implementiert auch ICoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="494da-136">An object implementing the ICoreWebView2ExperimentalCompositionController interface will also implement ICoreWebView2Controller.</span></span> <span data-ttu-id="494da-137">Anrufern wird erwartet, dass Sie ICoreWebView2Controller für die Größenänderung, Sichtbarkeit, Fokus usw. verwenden, und verwenden Sie dann ICoreWebView2ExperimentalCompositionController, um eine Verbindung mit einer Kompositionsstruktur herzustellen und die Eingabe für die WebView bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="494da-137">Callers are expected to use ICoreWebView2Controller for resizing, visibility, focus, and so on, and then use ICoreWebView2ExperimentalCompositionController to connect to a composition tree and provide input meant for the WebView.</span></span>

## <span data-ttu-id="494da-138">Member</span><span class="sxs-lookup"><span data-stu-id="494da-138">Members</span></span>

#### <span data-ttu-id="494da-139">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="494da-139">add_CursorChanged</span></span> 

<span data-ttu-id="494da-140">Fügen Sie einen Ereignishandler für das Cursor Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="494da-140">Add an event handler for the CursorChanged event.</span></span>

> <span data-ttu-id="494da-141">Public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="494da-141">public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="494da-142">Das Ereignis wird ausgelöst, wenn WebView glaubt, dass der Cursor geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="494da-142">The event fires when WebView thinks the cursor should be changed.</span></span> <span data-ttu-id="494da-143">Wenn beispielsweise der Mauszeiger aktuell der Standardcursor ist, aber dann über Text verschoben wird, kann er versuchen, zum IBeam-Cursor zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="494da-143">For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.</span></span>

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender,
                       IUnknown* args) -> HRESULT {
                    HCURSOR cursor;
                    CHECK_FAILURE(sender->get_Cursor(&cursor));
                    SetClassLongPtr(m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                    return S_OK;
                })
                .Get(),
            &m_cursorChangedToken));
```

#### <span data-ttu-id="494da-144">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="494da-144">CreateCoreWebView2PointerInfoFromPointerId</span></span> 

<span data-ttu-id="494da-145">Eine Hilfsfunktion zum Konvertieren einer vom System empfangenen Zeiger-Nr in eine [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="494da-145">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="494da-146">öffentliche HRESULT- [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint-Zeiger-Nr., HWND-ParentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="494da-146">public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(UINT pointerId, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="494da-147">ParentWindow ist das HWND, das die WebView enthält.</span><span class="sxs-lookup"><span data-stu-id="494da-147">parentWindow is the HWND that contains the webview.</span></span> <span data-ttu-id="494da-148">Dies kann ein beliebiges HWND in der HWND-Struktur sein, das die WebView enthält.</span><span class="sxs-lookup"><span data-stu-id="494da-148">This can be any HWND in the hwnd tree that contains the webview.</span></span> <span data-ttu-id="494da-149">Die COREWEBVIEW2_MATRIX_4X4 ist die Transformation aus diesem HWND in die WebView.</span><span class="sxs-lookup"><span data-stu-id="494da-149">The COREWEBVIEW2_MATRIX_4X4 is the transform from that HWND to the webview.</span></span> <span data-ttu-id="494da-150">Der zurückgegebene [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) wird in SendPointerInfo verwendet.</span><span class="sxs-lookup"><span data-stu-id="494da-150">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) is used in SendPointerInfo.</span></span> <span data-ttu-id="494da-151">Der Zeigertyp muss entweder Stift oder Fingereingabe sein, oder die Funktion schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="494da-151">The pointer type must be either pen or touch or the function will fail.</span></span>



#### <span data-ttu-id="494da-152">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="494da-152">get_Cursor</span></span> 

<span data-ttu-id="494da-153">Der aktuelle Cursor, der von WebView als vorgesehen erachtet wird.</span><span class="sxs-lookup"><span data-stu-id="494da-153">The current cursor that WebView thinks it should be.</span></span>

> <span data-ttu-id="494da-154">öffentliche HRESULT- [get_Cursor](#get_cursor)(HCURSOR \* Cursor)</span><span class="sxs-lookup"><span data-stu-id="494da-154">public HRESULT [get_Cursor](#get_cursor)(HCURSOR \* cursor)</span></span>

<span data-ttu-id="494da-155">Der Cursor sollte in WM_SETCURSOR durch:: SetCursor festzulegen oder für das entsprechende übergeordnete/Ancestor-HWND des Webviews über:: SetClassLongPtr festzulegen.</span><span class="sxs-lookup"><span data-stu-id="494da-155">The cursor should be set in WM_SETCURSOR through ::SetCursor or set on the corresponding parent/ancestor HWND of the WebView through ::SetClassLongPtr.</span></span> <span data-ttu-id="494da-156">Die HCURSOR kann freigegeben werden, damit CopyCursor/DestroyCursor empfohlen wird, ihre eigene Kopie beizubehalten, wenn Sie mehr als das sofortige Festlegen des Cursors tun.</span><span class="sxs-lookup"><span data-stu-id="494da-156">The HCURSOR can be freed so CopyCursor/DestroyCursor is recommended to keep your own copy if you are doing more than immediately setting the cursor.</span></span>

#### <span data-ttu-id="494da-157">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="494da-157">get_RootVisualTarget</span></span> 

<span data-ttu-id="494da-158">Die RootVisualTarget ist ein visuelles Element in der visuellen Struktur der Host-app.</span><span class="sxs-lookup"><span data-stu-id="494da-158">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>

> <span data-ttu-id="494da-159">öffentliche HRESULT- [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \* \*-Ziel)</span><span class="sxs-lookup"><span data-stu-id="494da-159">public HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \*\* target)</span></span>

<span data-ttu-id="494da-160">In diesem visuellen Element wird die WebView-Struktur mit der visuellen Struktur verbunden.</span><span class="sxs-lookup"><span data-stu-id="494da-160">This visual is where the WebView will connect its visual tree.</span></span> <span data-ttu-id="494da-161">Die APP verwendet dieses visuelle Element, um die WebView in der APP zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="494da-161">The app uses this visual to position the WebView within the app.</span></span> <span data-ttu-id="494da-162">Die APP muss weiterhin die Bounds-Eigenschaft verwenden, um die Größe von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="494da-162">The app still needs to use the Bounds property to size the WebView.</span></span> <span data-ttu-id="494da-163">Die RootVisualTarget-Eigenschaft kann ein IDCompositionVisual oder ein Windows:: UI:: Composition:: ContainerVisual sein.</span><span class="sxs-lookup"><span data-stu-id="494da-163">The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual.</span></span> <span data-ttu-id="494da-164">WebView verbindet die visuelle Struktur mit dem bereitgestellten visuellen Element, bevor es vom Eigenschaftensetter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="494da-164">WebView will connect its visual tree to the provided visual before returning from the property setter.</span></span> <span data-ttu-id="494da-165">Die APP muss auf Ihrem Gerät einen Commit für die RootVisualTarget-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="494da-165">The app needs to commit on its device setting the RootVisualTarget property.</span></span> <span data-ttu-id="494da-166">Die RootVisualTarget-Eigenschaft unterstützt die Einstellung auf nullptr, um die WebView aus der visuellen Struktur der APP zu trennen.</span><span class="sxs-lookup"><span data-stu-id="494da-166">The RootVisualTarget property supports being set to nullptr to disconnect the WebView from the app's visual tree.</span></span> 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            CHECK_FAILURE(m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            CHECK_FAILURE(m_dcompDevice->Commit());
```

```cpp
// Create host app visual that the WebView will connect to.
//   - Create a IDCompositionTarget for the host window
//   - Create a visual and set that as the IDCompositionTarget's root
//   - Create another visual and add that to the IDCompositionTarget's root.
//     This visual will be the visual root for the WebView.
void ViewComponent::BuildDCompTreeUsingVisual()
{
    CHECK_FAILURE_BOOL(m_dcompDevice != nullptr);

    if (m_dcompWebViewVisual == nullptr)
    {
        CHECK_FAILURE(m_dcompDevice->CreateTargetForHwnd(
            m_appWindow->GetMainWindow(), TRUE, &m_dcompHwndTarget));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompRootVisual));
        CHECK_FAILURE(m_dcompHwndTarget->SetRoot(m_dcompRootVisual.get()));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompWebViewVisual));
        CHECK_FAILURE(m_dcompRootVisual->AddVisual(m_dcompWebViewVisual.get(), TRUE, nullptr));
    }
}
```

#### <span data-ttu-id="494da-167">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="494da-167">get_UIAProvider</span></span> 

<span data-ttu-id="494da-168">Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die WebView zurück.</span><span class="sxs-lookup"><span data-stu-id="494da-168">Returns the UI Automation Provider for the WebView.</span></span>

> <span data-ttu-id="494da-169">öffentliche HRESULT- [get_UIAProvider](#get_uiaprovider)(IUnknown \* \*-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="494da-169">public HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \*\* provider)</span></span>

#### <span data-ttu-id="494da-170">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="494da-170">put_RootVisualTarget</span></span> 

<span data-ttu-id="494da-171">Festlegen der RootVisualTarget-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="494da-171">Set the RootVisualTarget property.</span></span>

> <span data-ttu-id="494da-172">öffentliche HRESULT- [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \*-Ziel)</span><span class="sxs-lookup"><span data-stu-id="494da-172">public HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \* target)</span></span>

#### <span data-ttu-id="494da-173">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="494da-173">remove_CursorChanged</span></span> 

<span data-ttu-id="494da-174">Entfernen Sie einen Ereignishandler, der zuvor mit add_CursorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="494da-174">Remove an event handler previously added with add_CursorChanged.</span></span>

> <span data-ttu-id="494da-175">Public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="494da-175">public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="494da-176">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="494da-176">SendMouseInput</span></span> 

<span data-ttu-id="494da-177">Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL oder COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL ist, gibt mouseData den Umfang der Mausradbewegung an.</span><span class="sxs-lookup"><span data-stu-id="494da-177">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>

> <span data-ttu-id="494da-178">Public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UInt32 mouseData, Point Point)</span><span class="sxs-lookup"><span data-stu-id="494da-178">public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, POINT point)</span></span>

<span data-ttu-id="494da-179">Ein positiver Wert gibt an, dass das Rad nach vorne gedreht wurde, vom Benutzer entfernt; ein negativer Wert gibt an, dass das Rad nach hinten gedreht wurde, in Richtung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="494da-179">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span> <span data-ttu-id="494da-180">Ein Mausrad Klick ist als WHEEL_DELTA definiert, was 120 ist.</span><span class="sxs-lookup"><span data-stu-id="494da-180">One wheel click is defined as WHEEL_DELTA, which is 120.</span></span> <span data-ttu-id="494da-181">Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN oder COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP ist, gibt mouseData an, welche X-Schaltflächen gedrückt oder freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="494da-181">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN, or COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, then mouseData specifies which X buttons were pressed or released.</span></span> <span data-ttu-id="494da-182">Dieser Wert sollte 1 sein, wenn die erste x-Taste gedrückt/freigegeben wird, und 2, wenn die zweite x-Taste gedrückt/freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="494da-182">This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released.</span></span> <span data-ttu-id="494da-183">Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE ist, sollten virtualKeys, mouseData und Point alle NULL sein.</span><span class="sxs-lookup"><span data-stu-id="494da-183">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, then virtualKeys, mouseData, and point should all be zero.</span></span> <span data-ttu-id="494da-184">Wenn eventKind ein beliebiger anderer Wert ist, sollte mouseData NULL sein.</span><span class="sxs-lookup"><span data-stu-id="494da-184">If eventKind is any other value, then mouseData should be zero.</span></span> <span data-ttu-id="494da-185">Point wird im Client Koordinatensystem der WebView erwartet.</span><span class="sxs-lookup"><span data-stu-id="494da-185">Point is expected to be in the client coordinate space of the WebView.</span></span> <span data-ttu-id="494da-186">Zum nachvollziehen von Mausereignissen, die in der WebView beginnen und potenziell außerhalb der WebView-und Hostanwendung verschoben werden können, wird der Aufruf von SetCapture und ReleaseCapture empfohlen.</span><span class="sxs-lookup"><span data-stu-id="494da-186">To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended.</span></span> <span data-ttu-id="494da-187">Wenn Sie Hover-Popups schließen möchten, empfiehlt es sich auch, WM_MOUSELEAVE Nachrichten zu senden.</span><span class="sxs-lookup"><span data-stu-id="494da-187">To dismiss hover popups, it is also recommended to send WM_MOUSELEAVE messages.</span></span> 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
    if (m_dcompDevice || m_wincompHelper)
    {
        POINT point;
        POINTSTOPOINT(point, lParam);
        if (message == WM_MOUSEWHEEL || message == WM_MOUSEHWHEEL)
        {
            // Mouse wheel messages are delivered in screen coordinates.
            // SendMouseInput expects client coordinates for the WebView, so convert
            // the point from screen to client.
            ::ScreenToClient(m_appWindow->GetMainWindow(), &point);
        }
        // Send the message to the WebView if the mouse location is inside the
        // bounds of the WebView, if the message is telling the WebView the
        // mouse has left the client area, or if we are currently capturing
        // mouse events.
        bool isMouseInWebView = PtInRect(&m_webViewBounds, point);
        if (isMouseInWebView || message == WM_MOUSELEAVE || m_isCapturingMouse)
        {
            DWORD mouseData = 0;

            switch (message)
            {
            case WM_MOUSEWHEEL:
            case WM_MOUSEHWHEEL:
                mouseData = GET_WHEEL_DELTA_WPARAM(wParam);
                break;
            case WM_XBUTTONDBLCLK:
            case WM_XBUTTONDOWN:
            case WM_XBUTTONUP:
                mouseData = GET_XBUTTON_WPARAM(wParam);
                break;
            case WM_MOUSEMOVE:
                if (!m_isTrackingMouse)
                {
                    // WebView needs to know when the mouse leaves the client area
                    // so that it can dismiss hover popups. TrackMouseEvent will
                    // provide a notification when the mouse leaves the client area.
                    TrackMouseEvents(TME_LEAVE);
                    m_isTrackingMouse = true;
                }
                break;
            case WM_MOUSELEAVE:
                m_isTrackingMouse = false;
                break;
            }

            // We need to capture the mouse in case the user drags the
            // mouse outside of the window bounds and we still need to send
            // mouse messages to the WebView process. This is useful for
            // scenarios like dragging the scroll bar or panning a map.
            // This is very similar to the Pointer Message case where a
            // press started inside of the WebView.
            if (message == WM_LBUTTONDOWN || message == WM_MBUTTONDOWN ||
                message == WM_RBUTTONDOWN || message == WM_XBUTTONDOWN)
            {
                if (isMouseInWebView && ::GetCapture() != m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = true;
                    ::SetCapture(m_appWindow->GetMainWindow());
                }
            }
            else if (message == WM_LBUTTONUP || message == WM_MBUTTONUP ||
                message == WM_RBUTTONUP || message == WM_XBUTTONUP)
            {
                if (::GetCapture() == m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = false;
                    ::ReleaseCapture();
                }
            }

            // Adjust the point from app client coordinates to webview client coordinates.
            // WM_MOUSELEAVE messages don't have a point, so don't adjust the point.
            if (message != WM_MOUSELEAVE)
            {
                point.x -= m_webViewBounds.left;
                point.y -= m_webViewBounds.top;
            }

            CHECK_FAILURE(m_compositionController->SendMouseInput(
                static_cast<COREWEBVIEW2_MOUSE_EVENT_KIND>(message),
                static_cast<COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS>(GET_KEYSTATE_WPARAM(wParam)),
                mouseData, point));
            return true;
        }
        else if (message == WM_MOUSEMOVE && m_isTrackingMouse)
        {
            // When the mouse moves outside of the WebView, but still inside the app
            // turn off mouse tracking and send the WebView a leave event.
            m_isTrackingMouse = false;
            TrackMouseEvents(TME_LEAVE | TME_CANCEL);
            OnMouseMessage(WM_MOUSELEAVE, 0, 0);
        }
    }
    return false;
}
```

#### <span data-ttu-id="494da-188">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="494da-188">SendPointerInput</span></span> 

<span data-ttu-id="494da-189">SendPointerInput akzeptiert Fingereingabe-oder Stiftzeiger Eingaben von Typen, die in COREWEBVIEW2_POINTER_EVENT_KIND definiert sind.</span><span class="sxs-lookup"><span data-stu-id="494da-189">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>

> <span data-ttu-id="494da-190">Public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="494da-190">public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) eventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span></span>

<span data-ttu-id="494da-191">Alle zeigereingaben aus dem System müssen zuerst in eine [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="494da-191">Any pointer input from the system must be converted into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) first.</span></span>

#### <span data-ttu-id="494da-192">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="494da-192">COREWEBVIEW2_MATRIX_4X4</span></span> 

<span data-ttu-id="494da-193">Matrix, die eine 3D-Transformation darstellt.</span><span class="sxs-lookup"><span data-stu-id="494da-193">Matrix that represents a 3D transform.</span></span>

> <span data-ttu-id="494da-194">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span><span class="sxs-lookup"><span data-stu-id="494da-194">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span></span>

<span data-ttu-id="494da-195">Diese Transformation wird verwendet, um korrekte Koordinaten beim Aufrufen von CreateCoreWebView2PointerInfoFromPointerId zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="494da-195">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span> <span data-ttu-id="494da-196">Dies entspricht einer D2D1_MATRIX_4X4_F</span><span class="sxs-lookup"><span data-stu-id="494da-196">This is equivalent to a D2D1_MATRIX_4X4_F</span></span>

#### <span data-ttu-id="494da-197">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="494da-197">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span> 

<span data-ttu-id="494da-198">Maus Ereignistyp, der von SendMouseInput verwendet wird, um den Typ des Mausereignisses zu übermitteln, das an WebView gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="494da-198">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>

> <span data-ttu-id="494da-199">Enum- [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span><span class="sxs-lookup"><span data-stu-id="494da-199">enum [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span></span>

 <span data-ttu-id="494da-200">Werte</span><span class="sxs-lookup"><span data-stu-id="494da-200">Values</span></span>                         | <span data-ttu-id="494da-201">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="494da-201">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="494da-202">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span><span class="sxs-lookup"><span data-stu-id="494da-202">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span></span>            | <span data-ttu-id="494da-203">Mausrad Scroll-Ereignis, WM_MOUSEHWHEEL</span><span class="sxs-lookup"><span data-stu-id="494da-203">Mouse horizontal wheel scroll event, WM_MOUSEHWHEEL.</span></span>
<span data-ttu-id="494da-204">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="494da-204">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="494da-205">Klicken Sie mit der linken Maustaste auf das Mausereignis, WM_LBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="494da-205">Left button double click mouse event, WM_LBUTTONDBLCLK.</span></span>
<span data-ttu-id="494da-206">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="494da-206">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span></span>            | <span data-ttu-id="494da-207">Linke Maustaste-Maustaste-Ereignis, WM_LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="494da-207">Left button down mouse event, WM_LBUTTONDOWN.</span></span>
<span data-ttu-id="494da-208">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="494da-208">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span></span>            | <span data-ttu-id="494da-209">Linke Maustaste, Mausereignis, WM_LBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="494da-209">Left button up mouse event, WM_LBUTTONUP.</span></span>
<span data-ttu-id="494da-210">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="494da-210">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="494da-211">Maus-Leave-Ereignis, WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="494da-211">Mouse leave event, WM_MOUSELEAVE.</span></span>
<span data-ttu-id="494da-212">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="494da-212">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="494da-213">Klicken Sie auf die mittlere Schaltfläche, und klicken Sie auf Mausereignis WM_MBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="494da-213">Middle button double click mouse event, WM_MBUTTONDBLCLK.</span></span>
<span data-ttu-id="494da-214">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="494da-214">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span></span>            | <span data-ttu-id="494da-215">Klicken Sie auf der mittleren Maustaste auf das Mausereignis, WM_MBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="494da-215">Middle button down mouse event, WM_MBUTTONDOWN.</span></span>
<span data-ttu-id="494da-216">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="494da-216">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span></span>            | <span data-ttu-id="494da-217">Mittlere Maustaste auf Mausereignis, WM_MBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="494da-217">Middle button up mouse event, WM_MBUTTONUP.</span></span>
<span data-ttu-id="494da-218">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span><span class="sxs-lookup"><span data-stu-id="494da-218">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span></span>            | <span data-ttu-id="494da-219">Maus Bewegungs Ereignis, WM_MOUSEMOVE.</span><span class="sxs-lookup"><span data-stu-id="494da-219">Mouse move event, WM_MOUSEMOVE.</span></span>
<span data-ttu-id="494da-220">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="494da-220">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="494da-221">Klicken Sie mit der rechten Maustaste auf Mausereignis, WM_RBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="494da-221">Right button double click mouse event, WM_RBUTTONDBLCLK.</span></span>
<span data-ttu-id="494da-222">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="494da-222">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span></span>            | <span data-ttu-id="494da-223">Klicken Sie mit der rechten Maustaste auf das Mausereignis, WM_RBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="494da-223">Right button down mouse event, WM_RBUTTONDOWN.</span></span>
<span data-ttu-id="494da-224">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="494da-224">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span></span>            | <span data-ttu-id="494da-225">Klicken Sie mit der rechten Maustaste auf das Mausereignis, WM_RBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="494da-225">Right button up mouse event, WM_RBUTTONUP.</span></span>
<span data-ttu-id="494da-226">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span><span class="sxs-lookup"><span data-stu-id="494da-226">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span></span>            | <span data-ttu-id="494da-227">Mausrad Scroll-Ereignis, WM_MOUSEWHEEL.</span><span class="sxs-lookup"><span data-stu-id="494da-227">Mouse wheel scroll event, WM_MOUSEWHEEL.</span></span>
<span data-ttu-id="494da-228">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="494da-228">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="494da-229">Erste oder zweite X-Taste Doppelklick-Mausereignis, WM_XBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="494da-229">First or second X button double click mouse event, WM_XBUTTONDBLCLK.</span></span>
<span data-ttu-id="494da-230">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="494da-230">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span></span>            | <span data-ttu-id="494da-231">Erstes oder zweites X-Schaltflächen-Mausereignis, WM_XBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="494da-231">First or second X button down mouse event, WM_XBUTTONDOWN.</span></span>
<span data-ttu-id="494da-232">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="494da-232">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span></span>            | <span data-ttu-id="494da-233">Erstes oder zweites X-Schaltflächen-Mausereignis, WM_XBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="494da-233">First or second X button up mouse event, WM_XBUTTONUP.</span></span>

<span data-ttu-id="494da-234">Die Werte dieser Enumeration sind an die übereinstimmenden WM_ \*-Fenster Meldungen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="494da-234">The values of this enum align with the matching WM_\* window messages.</span></span>

#### <span data-ttu-id="494da-235">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="494da-235">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span> 

<span data-ttu-id="494da-236">Virtuelle Mausereignis Tasten, die einem COREWEBVIEW2_MOUSE_EVENT_KIND für SendMouseInput zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="494da-236">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>

> <span data-ttu-id="494da-237">Enum- [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span><span class="sxs-lookup"><span data-stu-id="494da-237">enum [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span></span>

 <span data-ttu-id="494da-238">Werte</span><span class="sxs-lookup"><span data-stu-id="494da-238">Values</span></span>                         | <span data-ttu-id="494da-239">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="494da-239">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="494da-240">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span><span class="sxs-lookup"><span data-stu-id="494da-240">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span></span>            | <span data-ttu-id="494da-241">Keine weiteren Tasten gedrückt.</span><span class="sxs-lookup"><span data-stu-id="494da-241">No additional keys pressed.</span></span>
<span data-ttu-id="494da-242">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="494da-242">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span></span>            | <span data-ttu-id="494da-243">Linke Maustaste gedrückt, MK_LBUTTON.</span><span class="sxs-lookup"><span data-stu-id="494da-243">Left mouse button is down, MK_LBUTTON.</span></span>
<span data-ttu-id="494da-244">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="494da-244">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span></span>            | <span data-ttu-id="494da-245">Klicken Sie mit der rechten Maustaste auf die MK_RBUTTON.</span><span class="sxs-lookup"><span data-stu-id="494da-245">Right mouse button is down, MK_RBUTTON.</span></span>
<span data-ttu-id="494da-246">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span><span class="sxs-lookup"><span data-stu-id="494da-246">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span></span>            | <span data-ttu-id="494da-247">Die UMSCHALTTASTE ist MK_SHIFT.</span><span class="sxs-lookup"><span data-stu-id="494da-247">SHIFT key is down, MK_SHIFT.</span></span>
<span data-ttu-id="494da-248">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span><span class="sxs-lookup"><span data-stu-id="494da-248">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span></span>            | <span data-ttu-id="494da-249">Die STRG-Taste ist MK_CONTROL.</span><span class="sxs-lookup"><span data-stu-id="494da-249">CTRL key is down, MK_CONTROL.</span></span>
<span data-ttu-id="494da-250">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span><span class="sxs-lookup"><span data-stu-id="494da-250">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span></span>            | <span data-ttu-id="494da-251">Mittlere Maustaste gedrückt, MK_MBUTTON.</span><span class="sxs-lookup"><span data-stu-id="494da-251">Middle mouse button is down, MK_MBUTTON.</span></span>
<span data-ttu-id="494da-252">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span><span class="sxs-lookup"><span data-stu-id="494da-252">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span></span>            | <span data-ttu-id="494da-253">Die erste X-Taste ist unten, MK_XBUTTON1.</span><span class="sxs-lookup"><span data-stu-id="494da-253">First X button is down, MK_XBUTTON1.</span></span>
<span data-ttu-id="494da-254">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span><span class="sxs-lookup"><span data-stu-id="494da-254">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span></span>            | <span data-ttu-id="494da-255">Die zweite X-Taste ist unten, MK_XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="494da-255">Second X button is down, MK_XBUTTON2.</span></span>

<span data-ttu-id="494da-256">Diese Werte können in ein Bitflags-Flag kombiniert werden, wenn mehr als eine virtuelle Taste für das Ereignis gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="494da-256">These values can be combined into a bit flag if more than one virtual key is pressed for the event.</span></span> <span data-ttu-id="494da-257">Die Werte dieser Enumeration werden an die übereinstimmenden MK_ \*-Maustasten angeglichen.</span><span class="sxs-lookup"><span data-stu-id="494da-257">The values of this enum align with the matching MK_\* mouse keys.</span></span>

#### <span data-ttu-id="494da-258">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="494da-258">COREWEBVIEW2_POINTER_EVENT_KIND</span></span> 

<span data-ttu-id="494da-259">Zeiger Ereignistyp, der von SendPointerInput verwendet wird, um den Typ des Zeiger Ereignisses zu vermitteln, das an WebView gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="494da-259">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

> <span data-ttu-id="494da-260">Enum- [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span><span class="sxs-lookup"><span data-stu-id="494da-260">enum [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span></span>

 <span data-ttu-id="494da-261">Werte</span><span class="sxs-lookup"><span data-stu-id="494da-261">Values</span></span>                         | <span data-ttu-id="494da-262">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="494da-262">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="494da-263">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="494da-263">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span></span>            | <span data-ttu-id="494da-264">Entspricht WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="494da-264">Corresponds to WM_POINTERACTIVATE.</span></span>
<span data-ttu-id="494da-265">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span><span class="sxs-lookup"><span data-stu-id="494da-265">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span></span>            | <span data-ttu-id="494da-266">Entspricht WM_POINTERDOWN.</span><span class="sxs-lookup"><span data-stu-id="494da-266">Corresponds to WM_POINTERDOWN.</span></span>
<span data-ttu-id="494da-267">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span><span class="sxs-lookup"><span data-stu-id="494da-267">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span></span>            | <span data-ttu-id="494da-268">Entspricht WM_POINTERENTER.</span><span class="sxs-lookup"><span data-stu-id="494da-268">Corresponds to WM_POINTERENTER.</span></span>
<span data-ttu-id="494da-269">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="494da-269">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="494da-270">Entspricht WM_POINTERLEAVE.</span><span class="sxs-lookup"><span data-stu-id="494da-270">Corresponds to WM_POINTERLEAVE.</span></span>
<span data-ttu-id="494da-271">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span><span class="sxs-lookup"><span data-stu-id="494da-271">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span></span>            | <span data-ttu-id="494da-272">Entspricht WM_POINTERUP.</span><span class="sxs-lookup"><span data-stu-id="494da-272">Corresponds to WM_POINTERUP.</span></span>
<span data-ttu-id="494da-273">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span><span class="sxs-lookup"><span data-stu-id="494da-273">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span></span>            | <span data-ttu-id="494da-274">Entspricht WM_POINTERUPDATE.</span><span class="sxs-lookup"><span data-stu-id="494da-274">Corresponds to WM_POINTERUPDATE.</span></span>

<span data-ttu-id="494da-275">Die Werte dieser Enumeration sind an die übereinstimmenden WM_POINTER \*-Fenster Meldungen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="494da-275">The values of this enum align with the matching WM_POINTER\* window messages.</span></span>

