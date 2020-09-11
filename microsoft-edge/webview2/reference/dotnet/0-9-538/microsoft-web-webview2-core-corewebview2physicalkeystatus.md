---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 17ed4a578234a056a7e6ff347829a12e39fa93bd
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010922"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur 

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

