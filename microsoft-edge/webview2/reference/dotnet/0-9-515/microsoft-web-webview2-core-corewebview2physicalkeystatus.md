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
ms.openlocfilehash: bd63bda6b7835ff5edb30b8b1b22f877f4c96e14
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697595"
---
# Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur 

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[IsExtendedKey](#isextendedkey) | Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.
[IsKeyReleased](#iskeyreleased) | Der Übergangszustand.
[IsMenuKeyDown](#ismenukeydown) | Der kontextcode.
[RepeatCount](#repeatcount) | Die Anzahl der Wiederholungen für die aktuelle Nachricht.
[ScanCode](#scancode) | Der Überprüfungscode.
[WasKeyDown](#waskeydown) | Der vorherige Schlüssel Zustand.

Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .

## Member

#### IsExtendedKey 

Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.

> public int [IsExtendedKey](#isextendedkey)

#### IsKeyReleased 

Der Übergangszustand.

> public int [IsKeyReleased](#iskeyreleased)

#### IsMenuKeyDown 

Der kontextcode.

> public int [IsMenuKeyDown](#ismenukeydown)

#### RepeatCount 

Die Anzahl der Wiederholungen für die aktuelle Nachricht.

> public uint [repeatCount](#repeatcount)

#### ScanCode 

Der Überprüfungscode.

> public uint [ScanCode](#scancode)

#### WasKeyDown 

Der vorherige Schlüssel Zustand.

> public int [WasKeyDown](#waskeydown)

