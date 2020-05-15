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
ms.openlocfilehash: ef2eb16f6ba0186494400e6190d316ea503f9f16
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654035"
---
# Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Ereignis-args für das AcceleratorKeyPressed-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Handled](#handled) | Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.
[KeyEventKind](#keyeventkind) | Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.
[KeyEventLParam](#keyeventlparam) | Der lParam-Wert, der die Fenstermeldung begleitet hat.
[PhysicalKeyStatus](#physicalkeystatus) | Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.
[VirtualKey](#virtualkey) | Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.

## Member

#### Handled 

Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.

> öffentliche bool- [Behandlung](#handled)

Wenn die Handled-Eigenschaft auf true festgelegt ist, wird dadurch verhindert, dass die WebView die Standardaktion für diese Zugriffstaste ausführt. Andernfalls führt WebView die Standardaktion für die Zugriffstasten Taste aus.

#### KeyEventKind 

Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.

> öffentliche [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) - [KeyEventKind](#keyeventkind)

#### KeyEventLParam 

Der lParam-Wert, der die Fenstermeldung begleitet hat.

> public int [KeyEventLParam](#keyeventlparam)

Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.

#### PhysicalKeyStatus 

Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.

> öffentliche [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) - [PhysicalKeyStatus](#physicalkeystatus)

#### VirtualKey 

Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.

> public uint [VirtualKey](#virtualkey)

Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A". Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.

