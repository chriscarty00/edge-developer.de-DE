---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalCompositionController
ms.openlocfilehash: d651133162520e4a967d13de6f585fe3ac02e830
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886465"
---
# <span data-ttu-id="1fd58-104">Schnittstellen ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="1fd58-104">interface ICoreWebView2ExperimentalCompositionController</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

<span data-ttu-id="1fd58-105">Diese Schnittstelle ist eine Erweiterung der [ICoreWebView2Controller](icorewebview2controller.md) -Schnittstelle, um visuelles Hosting zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1fd58-105">This interface is an extension of the [ICoreWebView2Controller](icorewebview2controller.md) interface to support visual hosting.</span></span>

## <span data-ttu-id="1fd58-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1fd58-106">Summary</span></span>

 <span data-ttu-id="1fd58-107">Member</span><span class="sxs-lookup"><span data-stu-id="1fd58-107">Members</span></span>                        | <span data-ttu-id="1fd58-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1fd58-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1fd58-109">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="1fd58-109">add_CursorChanged</span></span>](#add_cursorchanged) | <span data-ttu-id="1fd58-110">Fügen Sie einen Ereignishandler für das Cursor Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="1fd58-110">Add an event handler for the CursorChanged event.</span></span>
[<span data-ttu-id="1fd58-111">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="1fd58-111">CreateCoreWebView2PointerInfoFromPointerId</span></span>](#createcorewebview2pointerinfofrompointerid) | <span data-ttu-id="1fd58-112">Eine Hilfsfunktion zum Konvertieren einer vom System empfangenen Zeiger-Nr in eine [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="1fd58-112">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="1fd58-113">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="1fd58-113">get_Cursor</span></span>](#get_cursor) | <span data-ttu-id="1fd58-114">Der aktuelle Cursor, der von WebView als vorgesehen erachtet wird.</span><span class="sxs-lookup"><span data-stu-id="1fd58-114">The current cursor that WebView thinks it should be.</span></span>
[<span data-ttu-id="1fd58-115">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="1fd58-115">get_RootVisualTarget</span></span>](#get_rootvisualtarget) | <span data-ttu-id="1fd58-116">Die RootVisualTarget ist ein visuelles Element in der visuellen Struktur der Host-app.</span><span class="sxs-lookup"><span data-stu-id="1fd58-116">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>
[<span data-ttu-id="1fd58-117">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="1fd58-117">get_UIAProvider</span></span>](#get_uiaprovider) | <span data-ttu-id="1fd58-118">Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die WebView zurück.</span><span class="sxs-lookup"><span data-stu-id="1fd58-118">Returns the UI Automation Provider for the WebView.</span></span>
[<span data-ttu-id="1fd58-119">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="1fd58-119">put_RootVisualTarget</span></span>](#put_rootvisualtarget) | <span data-ttu-id="1fd58-120">Festlegen der RootVisualTarget-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1fd58-120">Set the RootVisualTarget property.</span></span>
[<span data-ttu-id="1fd58-121">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="1fd58-121">remove_CursorChanged</span></span>](#remove_cursorchanged) | <span data-ttu-id="1fd58-122">Entfernen Sie einen Ereignishandler, der zuvor mit add_CursorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1fd58-122">Remove an event handler previously added with add_CursorChanged.</span></span>
[<span data-ttu-id="1fd58-123">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="1fd58-123">SendMouseInput</span></span>](#sendmouseinput) | <span data-ttu-id="1fd58-124">Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL oder COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL ist, gibt mouseData den Umfang der Mausradbewegung an.</span><span class="sxs-lookup"><span data-stu-id="1fd58-124">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>
[<span data-ttu-id="1fd58-125">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="1fd58-125">SendPointerInput</span></span>](#sendpointerinput) | <span data-ttu-id="1fd58-126">SendPointerInput akzeptiert Fingereingabe-oder Stiftzeiger Eingaben von Typen, die in COREWEBVIEW2_POINTER_EVENT_KIND definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1fd58-126">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>
[<span data-ttu-id="1fd58-127">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="1fd58-127">COREWEBVIEW2_MATRIX_4X4</span></span>](#corewebview2_matrix_4x4) | <span data-ttu-id="1fd58-128">Matrix, die eine 3D-Transformation darstellt.</span><span class="sxs-lookup"><span data-stu-id="1fd58-128">Matrix that represents a 3D transform.</span></span>
[<span data-ttu-id="1fd58-129">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="1fd58-129">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span>](#corewebview2_mouse_event_kind) | <span data-ttu-id="1fd58-130">Maus Ereignistyp, der von SendMouseInput verwendet wird, um den Typ des Mausereignisses zu übermitteln, das an WebView gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fd58-130">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>
[<span data-ttu-id="1fd58-131">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="1fd58-131">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span>](#corewebview2_mouse_event_virtual_keys) | <span data-ttu-id="1fd58-132">Virtuelle Mausereignis Tasten, die einem COREWEBVIEW2_MOUSE_EVENT_KIND für SendMouseInput zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1fd58-132">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>
[<span data-ttu-id="1fd58-133">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="1fd58-133">COREWEBVIEW2_POINTER_EVENT_KIND</span></span>](#corewebview2_pointer_event_kind) | <span data-ttu-id="1fd58-134">Zeiger Ereignistyp, der von SendPointerInput verwendet wird, um den Typ des Zeiger Ereignisses zu vermitteln, das an WebView gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fd58-134">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

<span data-ttu-id="1fd58-135">Ein Objekt, das die ICoreWebView2ExperimentalCompositionController-Schnittstelle implementiert, implementiert auch [ICoreWebView2Controller](icorewebview2controller.md).</span><span class="sxs-lookup"><span data-stu-id="1fd58-135">An object implementing the ICoreWebView2ExperimentalCompositionController interface will also implement [ICoreWebView2Controller](icorewebview2controller.md).</span></span> <span data-ttu-id="1fd58-136">Anrufern wird erwartet, dass Sie [ICoreWebView2Controller](icorewebview2controller.md) für die Größenänderung, Sichtbarkeit, Fokus usw. verwenden, und verwenden Sie dann ICoreWebView2ExperimentalCompositionController, um eine Verbindung mit einer Kompositionsstruktur herzustellen und die Eingabe für die WebView bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1fd58-136">Callers are expected to use [ICoreWebView2Controller](icorewebview2controller.md) for resizing, visibility, focus, and so on, and then use ICoreWebView2ExperimentalCompositionController to connect to a composition tree and provide input meant for the WebView.</span></span>

## <span data-ttu-id="1fd58-137">Member</span><span class="sxs-lookup"><span data-stu-id="1fd58-137">Members</span></span>

#### <span data-ttu-id="1fd58-138">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="1fd58-138">add_CursorChanged</span></span> 

<span data-ttu-id="1fd58-139">Fügen Sie einen Ereignishandler für das Cursor Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="1fd58-139">Add an event handler for the CursorChanged event.</span></span>

> <span data-ttu-id="1fd58-140">Public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="1fd58-140">public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="1fd58-141">Das Ereignis wird ausgelöst, wenn WebView glaubt, dass der Cursor geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fd58-141">The event fires when WebView thinks the cursor should be changed.</span></span> <span data-ttu-id="1fd58-142">Wenn beispielsweise der Mauszeiger aktuell der Standardcursor ist, aber dann über Text verschoben wird, kann er versuchen, zum IBeam-Cursor zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="1fd58-142">For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.</span></span>

<span data-ttu-id="1fd58-143">Es wird erwartet, dass der Entwickler COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE Nachrichten (zusätzlich zu COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE Nachrichten) über die SendMouseInput-API sendet.</span><span class="sxs-lookup"><span data-stu-id="1fd58-143">It is expected for the developer to send COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE messages (in addition to COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE messages) through the SendMouseInput API.</span></span> <span data-ttu-id="1fd58-144">Dadurch wird sichergestellt, dass sich die Maus tatsächlich in der WebView befindet, die Cursor Ereignisse sendet.</span><span class="sxs-lookup"><span data-stu-id="1fd58-144">This is to ensure that the mouse is actually within the WebView that sends out CursorChanged events.</span></span>

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

#### <span data-ttu-id="1fd58-145">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="1fd58-145">CreateCoreWebView2PointerInfoFromPointerId</span></span> 

<span data-ttu-id="1fd58-146">Eine Hilfsfunktion zum Konvertieren einer vom System empfangenen Zeiger-Nr in eine [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="1fd58-146">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="1fd58-147">öffentliche HRESULT- [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint-Zeiger-Nr., HWND-ParentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="1fd58-147">public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(UINT pointerId, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="1fd58-148">ParentWindow ist das HWND, das die WebView enthält.</span><span class="sxs-lookup"><span data-stu-id="1fd58-148">parentWindow is the HWND that contains the webview.</span></span> <span data-ttu-id="1fd58-149">Dies kann ein beliebiges HWND in der HWND-Struktur sein, das die WebView enthält.</span><span class="sxs-lookup"><span data-stu-id="1fd58-149">This can be any HWND in the hwnd tree that contains the webview.</span></span> <span data-ttu-id="1fd58-150">Die COREWEBVIEW2_MATRIX_4X4 ist die Transformation aus diesem HWND in die WebView.</span><span class="sxs-lookup"><span data-stu-id="1fd58-150">The COREWEBVIEW2_MATRIX_4X4 is the transform from that HWND to the webview.</span></span> <span data-ttu-id="1fd58-151">Der zurückgegebene [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) wird in SendPointerInfo verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fd58-151">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) is used in SendPointerInfo.</span></span> <span data-ttu-id="1fd58-152">Der Zeigertyp muss entweder Stift oder Fingereingabe sein, oder die Funktion schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="1fd58-152">The pointer type must be either pen or touch or the function will fail.</span></span>


#### <span data-ttu-id="1fd58-153">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="1fd58-153">get_Cursor</span></span> 

<span data-ttu-id="1fd58-154">Der aktuelle Cursor, der von WebView als vorgesehen erachtet wird.</span><span class="sxs-lookup"><span data-stu-id="1fd58-154">The current cursor that WebView thinks it should be.</span></span>

> <span data-ttu-id="1fd58-155">öffentliche HRESULT- [get_Cursor](#get_cursor)(HCURSOR \* Cursor)</span><span class="sxs-lookup"><span data-stu-id="1fd58-155">public HRESULT [get_Cursor](#get_cursor)(HCURSOR \* cursor)</span></span>

<span data-ttu-id="1fd58-156">Der Cursor sollte in WM_SETCURSOR durch:: SetCursor festzulegen oder für das entsprechende übergeordnete/Ancestor-HWND des Webviews über:: SetClassLongPtr festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1fd58-156">The cursor should be set in WM_SETCURSOR through ::SetCursor or set on the corresponding parent/ancestor HWND of the WebView through ::SetClassLongPtr.</span></span> <span data-ttu-id="1fd58-157">Die HCURSOR kann freigegeben werden, damit CopyCursor/DestroyCursor empfohlen wird, ihre eigene Kopie beizubehalten, wenn Sie mehr als das sofortige Festlegen des Cursors tun.</span><span class="sxs-lookup"><span data-stu-id="1fd58-157">The HCURSOR can be freed so CopyCursor/DestroyCursor is recommended to keep your own copy if you are doing more than immediately setting the cursor.</span></span>

#### <span data-ttu-id="1fd58-158">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="1fd58-158">get_RootVisualTarget</span></span> 

<span data-ttu-id="1fd58-159">Die RootVisualTarget ist ein visuelles Element in der visuellen Struktur der Host-app.</span><span class="sxs-lookup"><span data-stu-id="1fd58-159">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>

> <span data-ttu-id="1fd58-160">öffentliche HRESULT- [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \* \*-Ziel)</span><span class="sxs-lookup"><span data-stu-id="1fd58-160">public HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \*\* target)</span></span>

<span data-ttu-id="1fd58-161">In diesem visuellen Element wird die WebView-Struktur mit der visuellen Struktur verbunden.</span><span class="sxs-lookup"><span data-stu-id="1fd58-161">This visual is where the WebView will connect its visual tree.</span></span> <span data-ttu-id="1fd58-162">Die APP verwendet dieses visuelle Element, um die WebView in der APP zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="1fd58-162">The app uses this visual to position the WebView within the app.</span></span> <span data-ttu-id="1fd58-163">Die APP muss weiterhin die Bounds-Eigenschaft verwenden, um die Größe von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1fd58-163">The app still needs to use the Bounds property to size the WebView.</span></span> <span data-ttu-id="1fd58-164">Die RootVisualTarget-Eigenschaft kann ein IDCompositionVisual oder ein Windows:: UI:: Composition:: ContainerVisual sein.</span><span class="sxs-lookup"><span data-stu-id="1fd58-164">The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual.</span></span> <span data-ttu-id="1fd58-165">WebView verbindet die visuelle Struktur mit dem bereitgestellten visuellen Element, bevor es vom Eigenschaftensetter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1fd58-165">WebView will connect its visual tree to the provided visual before returning from the property setter.</span></span> <span data-ttu-id="1fd58-166">Die APP muss auf Ihrem Gerät einen Commit für die RootVisualTarget-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="1fd58-166">The app needs to commit on its device setting the RootVisualTarget property.</span></span> <span data-ttu-id="1fd58-167">Die RootVisualTarget-Eigenschaft unterstützt die Einstellung auf nullptr, um die WebView aus der visuellen Struktur der APP zu trennen.</span><span class="sxs-lookup"><span data-stu-id="1fd58-167">The RootVisualTarget property supports being set to nullptr to disconnect the WebView from the app's visual tree.</span></span> 
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

#### <span data-ttu-id="1fd58-168">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="1fd58-168">get_UIAProvider</span></span> 

<span data-ttu-id="1fd58-169">Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die WebView zurück.</span><span class="sxs-lookup"><span data-stu-id="1fd58-169">Returns the UI Automation Provider for the WebView.</span></span>

> <span data-ttu-id="1fd58-170">öffentliche HRESULT- [get_UIAProvider](#get_uiaprovider)(IUnknown \* \*-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="1fd58-170">public HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \*\* provider)</span></span>

#### <span data-ttu-id="1fd58-171">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="1fd58-171">put_RootVisualTarget</span></span> 

<span data-ttu-id="1fd58-172">Festlegen der RootVisualTarget-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1fd58-172">Set the RootVisualTarget property.</span></span>

> <span data-ttu-id="1fd58-173">öffentliche HRESULT- [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \*-Ziel)</span><span class="sxs-lookup"><span data-stu-id="1fd58-173">public HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \* target)</span></span>

#### <span data-ttu-id="1fd58-174">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="1fd58-174">remove_CursorChanged</span></span> 

<span data-ttu-id="1fd58-175">Entfernen Sie einen Ereignishandler, der zuvor mit add_CursorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1fd58-175">Remove an event handler previously added with add_CursorChanged.</span></span>

> <span data-ttu-id="1fd58-176">Public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="1fd58-176">public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="1fd58-177">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="1fd58-177">SendMouseInput</span></span> 

<span data-ttu-id="1fd58-178">Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL oder COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL ist, gibt mouseData den Umfang der Mausradbewegung an.</span><span class="sxs-lookup"><span data-stu-id="1fd58-178">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>

> <span data-ttu-id="1fd58-179">Public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UInt32 mouseData, Point Point)</span><span class="sxs-lookup"><span data-stu-id="1fd58-179">public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, POINT point)</span></span>

<span data-ttu-id="1fd58-180">Ein positiver Wert gibt an, dass das Rad nach vorne gedreht wurde, vom Benutzer entfernt; ein negativer Wert gibt an, dass das Rad nach hinten gedreht wurde, in Richtung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1fd58-180">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span> <span data-ttu-id="1fd58-181">Ein Mausrad Klick ist als WHEEL_DELTA definiert, was 120 ist.</span><span class="sxs-lookup"><span data-stu-id="1fd58-181">One wheel click is defined as WHEEL_DELTA, which is 120.</span></span> <span data-ttu-id="1fd58-182">Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN oder COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP ist, gibt mouseData an, welche X-Schaltflächen gedrückt oder freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="1fd58-182">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN, or COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, then mouseData specifies which X buttons were pressed or released.</span></span> <span data-ttu-id="1fd58-183">Dieser Wert sollte 1 sein, wenn die erste x-Taste gedrückt/freigegeben wird, und 2, wenn die zweite x-Taste gedrückt/freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1fd58-183">This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released.</span></span> <span data-ttu-id="1fd58-184">Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE ist, sollten virtualKeys, mouseData und Point alle NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1fd58-184">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, then virtualKeys, mouseData, and point should all be zero.</span></span> <span data-ttu-id="1fd58-185">Wenn eventKind ein beliebiger anderer Wert ist, sollte mouseData NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1fd58-185">If eventKind is any other value, then mouseData should be zero.</span></span> <span data-ttu-id="1fd58-186">Point wird im Client Koordinatensystem der WebView erwartet.</span><span class="sxs-lookup"><span data-stu-id="1fd58-186">Point is expected to be in the client coordinate space of the WebView.</span></span> <span data-ttu-id="1fd58-187">Zum nachvollziehen von Mausereignissen, die in der WebView beginnen und potenziell außerhalb der WebView-und Hostanwendung verschoben werden können, wird der Aufruf von SetCapture und ReleaseCapture empfohlen.</span><span class="sxs-lookup"><span data-stu-id="1fd58-187">To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended.</span></span> <span data-ttu-id="1fd58-188">Wenn Sie Hover-Popups schließen möchten, empfiehlt es sich auch, COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE Nachrichten zu senden.</span><span class="sxs-lookup"><span data-stu-id="1fd58-188">To dismiss hover popups, it is also recommended to send COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE messages.</span></span> 
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

#### <span data-ttu-id="1fd58-189">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="1fd58-189">SendPointerInput</span></span> 

<span data-ttu-id="1fd58-190">SendPointerInput akzeptiert Fingereingabe-oder Stiftzeiger Eingaben von Typen, die in COREWEBVIEW2_POINTER_EVENT_KIND definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1fd58-190">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>

> <span data-ttu-id="1fd58-191">Public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="1fd58-191">public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) eventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span></span>

<span data-ttu-id="1fd58-192">Alle zeigereingaben aus dem System müssen zuerst in eine [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="1fd58-192">Any pointer input from the system must be converted into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) first.</span></span>

#### <span data-ttu-id="1fd58-193">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="1fd58-193">COREWEBVIEW2_MATRIX_4X4</span></span> 

<span data-ttu-id="1fd58-194">Matrix, die eine 3D-Transformation darstellt.</span><span class="sxs-lookup"><span data-stu-id="1fd58-194">Matrix that represents a 3D transform.</span></span>

> <span data-ttu-id="1fd58-195">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span><span class="sxs-lookup"><span data-stu-id="1fd58-195">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span></span>

<span data-ttu-id="1fd58-196">Diese Transformation wird verwendet, um korrekte Koordinaten beim Aufrufen von CreateCoreWebView2PointerInfoFromPointerId zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1fd58-196">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span> <span data-ttu-id="1fd58-197">Dies entspricht einer D2D1_MATRIX_4X4_F</span><span class="sxs-lookup"><span data-stu-id="1fd58-197">This is equivalent to a D2D1_MATRIX_4X4_F</span></span>

#### <span data-ttu-id="1fd58-198">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="1fd58-198">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span> 

<span data-ttu-id="1fd58-199">Maus Ereignistyp, der von SendMouseInput verwendet wird, um den Typ des Mausereignisses zu übermitteln, das an WebView gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fd58-199">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>

> <span data-ttu-id="1fd58-200">Enum- [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span><span class="sxs-lookup"><span data-stu-id="1fd58-200">enum [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span></span>

 <span data-ttu-id="1fd58-201">Werte</span><span class="sxs-lookup"><span data-stu-id="1fd58-201">Values</span></span>                         | <span data-ttu-id="1fd58-202">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1fd58-202">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="1fd58-203">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span><span class="sxs-lookup"><span data-stu-id="1fd58-203">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span></span>            | <span data-ttu-id="1fd58-204">Mausrad Scroll-Ereignis, WM_MOUSEHWHEEL</span><span class="sxs-lookup"><span data-stu-id="1fd58-204">Mouse horizontal wheel scroll event, WM_MOUSEHWHEEL.</span></span>
<span data-ttu-id="1fd58-205">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="1fd58-205">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="1fd58-206">Klicken Sie mit der linken Maustaste auf das Mausereignis, WM_LBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="1fd58-206">Left button double click mouse event, WM_LBUTTONDBLCLK.</span></span>
<span data-ttu-id="1fd58-207">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="1fd58-207">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span></span>            | <span data-ttu-id="1fd58-208">Linke Maustaste-Maustaste-Ereignis, WM_LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="1fd58-208">Left button down mouse event, WM_LBUTTONDOWN.</span></span>
<span data-ttu-id="1fd58-209">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="1fd58-209">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span></span>            | <span data-ttu-id="1fd58-210">Linke Maustaste, Mausereignis, WM_LBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="1fd58-210">Left button up mouse event, WM_LBUTTONUP.</span></span>
<span data-ttu-id="1fd58-211">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="1fd58-211">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="1fd58-212">Maus-Leave-Ereignis, WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="1fd58-212">Mouse leave event, WM_MOUSELEAVE.</span></span>
<span data-ttu-id="1fd58-213">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="1fd58-213">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="1fd58-214">Klicken Sie auf die mittlere Schaltfläche, und klicken Sie auf Mausereignis WM_MBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="1fd58-214">Middle button double click mouse event, WM_MBUTTONDBLCLK.</span></span>
<span data-ttu-id="1fd58-215">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="1fd58-215">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span></span>            | <span data-ttu-id="1fd58-216">Klicken Sie auf der mittleren Maustaste auf das Mausereignis, WM_MBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="1fd58-216">Middle button down mouse event, WM_MBUTTONDOWN.</span></span>
<span data-ttu-id="1fd58-217">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="1fd58-217">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span></span>            | <span data-ttu-id="1fd58-218">Mittlere Maustaste auf Mausereignis, WM_MBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="1fd58-218">Middle button up mouse event, WM_MBUTTONUP.</span></span>
<span data-ttu-id="1fd58-219">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span><span class="sxs-lookup"><span data-stu-id="1fd58-219">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span></span>            | <span data-ttu-id="1fd58-220">Maus Bewegungs Ereignis, WM_MOUSEMOVE.</span><span class="sxs-lookup"><span data-stu-id="1fd58-220">Mouse move event, WM_MOUSEMOVE.</span></span>
<span data-ttu-id="1fd58-221">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="1fd58-221">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="1fd58-222">Klicken Sie mit der rechten Maustaste auf Mausereignis, WM_RBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="1fd58-222">Right button double click mouse event, WM_RBUTTONDBLCLK.</span></span>
<span data-ttu-id="1fd58-223">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="1fd58-223">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span></span>            | <span data-ttu-id="1fd58-224">Klicken Sie mit der rechten Maustaste auf das Mausereignis, WM_RBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="1fd58-224">Right button down mouse event, WM_RBUTTONDOWN.</span></span>
<span data-ttu-id="1fd58-225">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="1fd58-225">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span></span>            | <span data-ttu-id="1fd58-226">Klicken Sie mit der rechten Maustaste auf das Mausereignis, WM_RBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="1fd58-226">Right button up mouse event, WM_RBUTTONUP.</span></span>
<span data-ttu-id="1fd58-227">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span><span class="sxs-lookup"><span data-stu-id="1fd58-227">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span></span>            | <span data-ttu-id="1fd58-228">Mausrad Scroll-Ereignis, WM_MOUSEWHEEL.</span><span class="sxs-lookup"><span data-stu-id="1fd58-228">Mouse wheel scroll event, WM_MOUSEWHEEL.</span></span>
<span data-ttu-id="1fd58-229">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="1fd58-229">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="1fd58-230">Erste oder zweite X-Taste Doppelklick-Mausereignis, WM_XBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="1fd58-230">First or second X button double click mouse event, WM_XBUTTONDBLCLK.</span></span>
<span data-ttu-id="1fd58-231">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="1fd58-231">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span></span>            | <span data-ttu-id="1fd58-232">Erstes oder zweites X-Schaltflächen-Mausereignis, WM_XBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="1fd58-232">First or second X button down mouse event, WM_XBUTTONDOWN.</span></span>
<span data-ttu-id="1fd58-233">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="1fd58-233">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span></span>            | <span data-ttu-id="1fd58-234">Erstes oder zweites X-Schaltflächen-Mausereignis, WM_XBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="1fd58-234">First or second X button up mouse event, WM_XBUTTONUP.</span></span>

<span data-ttu-id="1fd58-235">Die Werte dieser Enumeration sind an die übereinstimmenden WM_ \*-Fenster Meldungen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="1fd58-235">The values of this enum align with the matching WM_\* window messages.</span></span>

#### <span data-ttu-id="1fd58-236">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="1fd58-236">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span> 

<span data-ttu-id="1fd58-237">Virtuelle Mausereignis Tasten, die einem COREWEBVIEW2_MOUSE_EVENT_KIND für SendMouseInput zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1fd58-237">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>

> <span data-ttu-id="1fd58-238">Enum- [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span><span class="sxs-lookup"><span data-stu-id="1fd58-238">enum [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span></span>

 <span data-ttu-id="1fd58-239">Werte</span><span class="sxs-lookup"><span data-stu-id="1fd58-239">Values</span></span>                         | <span data-ttu-id="1fd58-240">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1fd58-240">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="1fd58-241">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span><span class="sxs-lookup"><span data-stu-id="1fd58-241">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span></span>            | <span data-ttu-id="1fd58-242">Keine weiteren Tasten gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1fd58-242">No additional keys pressed.</span></span>
<span data-ttu-id="1fd58-243">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="1fd58-243">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span></span>            | <span data-ttu-id="1fd58-244">Linke Maustaste gedrückt, MK_LBUTTON.</span><span class="sxs-lookup"><span data-stu-id="1fd58-244">Left mouse button is down, MK_LBUTTON.</span></span>
<span data-ttu-id="1fd58-245">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="1fd58-245">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span></span>            | <span data-ttu-id="1fd58-246">Klicken Sie mit der rechten Maustaste auf die MK_RBUTTON.</span><span class="sxs-lookup"><span data-stu-id="1fd58-246">Right mouse button is down, MK_RBUTTON.</span></span>
<span data-ttu-id="1fd58-247">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span><span class="sxs-lookup"><span data-stu-id="1fd58-247">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span></span>            | <span data-ttu-id="1fd58-248">Die UMSCHALTTASTE ist MK_SHIFT.</span><span class="sxs-lookup"><span data-stu-id="1fd58-248">SHIFT key is down, MK_SHIFT.</span></span>
<span data-ttu-id="1fd58-249">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span><span class="sxs-lookup"><span data-stu-id="1fd58-249">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span></span>            | <span data-ttu-id="1fd58-250">Die STRG-Taste ist MK_CONTROL.</span><span class="sxs-lookup"><span data-stu-id="1fd58-250">CTRL key is down, MK_CONTROL.</span></span>
<span data-ttu-id="1fd58-251">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span><span class="sxs-lookup"><span data-stu-id="1fd58-251">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span></span>            | <span data-ttu-id="1fd58-252">Mittlere Maustaste gedrückt, MK_MBUTTON.</span><span class="sxs-lookup"><span data-stu-id="1fd58-252">Middle mouse button is down, MK_MBUTTON.</span></span>
<span data-ttu-id="1fd58-253">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span><span class="sxs-lookup"><span data-stu-id="1fd58-253">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span></span>            | <span data-ttu-id="1fd58-254">Die erste X-Taste ist unten, MK_XBUTTON1.</span><span class="sxs-lookup"><span data-stu-id="1fd58-254">First X button is down, MK_XBUTTON1.</span></span>
<span data-ttu-id="1fd58-255">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span><span class="sxs-lookup"><span data-stu-id="1fd58-255">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span></span>            | <span data-ttu-id="1fd58-256">Die zweite X-Taste ist unten, MK_XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="1fd58-256">Second X button is down, MK_XBUTTON2.</span></span>

<span data-ttu-id="1fd58-257">Diese Werte können in ein Bitflags-Flag kombiniert werden, wenn mehr als eine virtuelle Taste für das Ereignis gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="1fd58-257">These values can be combined into a bit flag if more than one virtual key is pressed for the event.</span></span> <span data-ttu-id="1fd58-258">Die Werte dieser Enumeration werden an die übereinstimmenden MK_ \*-Maustasten angeglichen.</span><span class="sxs-lookup"><span data-stu-id="1fd58-258">The values of this enum align with the matching MK_\* mouse keys.</span></span>

#### <span data-ttu-id="1fd58-259">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="1fd58-259">COREWEBVIEW2_POINTER_EVENT_KIND</span></span> 

<span data-ttu-id="1fd58-260">Zeiger Ereignistyp, der von SendPointerInput verwendet wird, um den Typ des Zeiger Ereignisses zu vermitteln, das an WebView gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fd58-260">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

> <span data-ttu-id="1fd58-261">Enum- [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span><span class="sxs-lookup"><span data-stu-id="1fd58-261">enum [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span></span>

 <span data-ttu-id="1fd58-262">Werte</span><span class="sxs-lookup"><span data-stu-id="1fd58-262">Values</span></span>                         | <span data-ttu-id="1fd58-263">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1fd58-263">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="1fd58-264">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="1fd58-264">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span></span>            | <span data-ttu-id="1fd58-265">Entspricht WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="1fd58-265">Corresponds to WM_POINTERACTIVATE.</span></span>
<span data-ttu-id="1fd58-266">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span><span class="sxs-lookup"><span data-stu-id="1fd58-266">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span></span>            | <span data-ttu-id="1fd58-267">Entspricht WM_POINTERDOWN.</span><span class="sxs-lookup"><span data-stu-id="1fd58-267">Corresponds to WM_POINTERDOWN.</span></span>
<span data-ttu-id="1fd58-268">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span><span class="sxs-lookup"><span data-stu-id="1fd58-268">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span></span>            | <span data-ttu-id="1fd58-269">Entspricht WM_POINTERENTER.</span><span class="sxs-lookup"><span data-stu-id="1fd58-269">Corresponds to WM_POINTERENTER.</span></span>
<span data-ttu-id="1fd58-270">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="1fd58-270">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="1fd58-271">Entspricht WM_POINTERLEAVE.</span><span class="sxs-lookup"><span data-stu-id="1fd58-271">Corresponds to WM_POINTERLEAVE.</span></span>
<span data-ttu-id="1fd58-272">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span><span class="sxs-lookup"><span data-stu-id="1fd58-272">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span></span>            | <span data-ttu-id="1fd58-273">Entspricht WM_POINTERUP.</span><span class="sxs-lookup"><span data-stu-id="1fd58-273">Corresponds to WM_POINTERUP.</span></span>
<span data-ttu-id="1fd58-274">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span><span class="sxs-lookup"><span data-stu-id="1fd58-274">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span></span>            | <span data-ttu-id="1fd58-275">Entspricht WM_POINTERUPDATE.</span><span class="sxs-lookup"><span data-stu-id="1fd58-275">Corresponds to WM_POINTERUPDATE.</span></span>

<span data-ttu-id="1fd58-276">Die Werte dieser Enumeration sind an die übereinstimmenden WM_POINTER \*-Fenster Meldungen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="1fd58-276">The values of this enum align with the matching WM_POINTER\* window messages.</span></span>

