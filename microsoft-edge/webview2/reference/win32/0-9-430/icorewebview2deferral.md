---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: bf6ce187168223b7e108aff7abf1bee5adea05a6
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884267"
---
# 0.9.430-Interface-ICoreWebView2Deferral 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
  : public IUnknown
```

Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Complete](#complete) | Schließt das zugeordnete verzögerte Ereignis ab.

## Member

#### Complete 

Schließt das zugeordnete verzögerte Ereignis ab.

> Public HRESULT [Complete](#complete)()

Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.

