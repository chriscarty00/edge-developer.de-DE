---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 280fe2d970d78bf1ea7a79b21f5081510ee27053
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878771"
---
# Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur 

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

