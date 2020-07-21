---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 10694292c7943f87753ae87f6129655b27f425f3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885142"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

