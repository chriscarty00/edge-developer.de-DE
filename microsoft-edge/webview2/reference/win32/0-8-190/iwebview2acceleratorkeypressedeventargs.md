---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 885ad6b161fbde6721e1812735ab50d7e0c3e8d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885052"
---
# 0.8.355-Interface-IWebView2AcceleratorKeyPressedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Ereignis-args für das AcceleratorKeyPressed-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_KeyEventType](#get_keyeventtype) | Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.
[get_VirtualKey](#get_virtualkey) | Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.
[get_KeyEventLParam](#get_keyeventlparam) | Der lParam-Wert, der die Fenstermeldung begleitet hat.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.
[Behandeln](#handle) | Durch diesen Aufruf kann der Browserprozess fortgesetzt werden.

## Member

#### get_KeyEventType 

Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.

> Public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE * keyeventtype)

Hierbei handelt es sich um einen WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN oder WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.

#### get_VirtualKey 

Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.

> Public HRESULT [get_VirtualKey](#get_virtualkey)(uint * VirtualKey)

Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A". Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.

#### get_KeyEventLParam 

Der lParam-Wert, der die Fenstermeldung begleitet hat.

> Public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int * LPARAM)

Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.

#### get_PhysicalKeyStatus 

Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.

> Public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### Behandeln 

Durch diesen Aufruf kann der Browserprozess fortgesetzt werden.

> öffentliches HRESULT- [handle](#handle)(bool Handled)

Durch das Übergeben von true wird verhindert, dass der Browser die Standardaktion für diese Zugriffstaste ausführt. Wenn der Ereignishandler ohne Aufrufen des [Handles ()](#handle)zurückgibt, entspricht dies dem aufrufenden handle (false). Das Aufrufen des [Handles ()](#handle) , nachdem es bereits aufgerufen wurde oder der Ereignishandler zurückgegeben wurde, bewirkt nichts.

