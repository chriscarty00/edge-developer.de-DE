---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: eecf4dd59d12c30667defd4e078e8624718bde26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884589"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

