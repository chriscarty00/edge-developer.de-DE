---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 793dbde462e25ae0bfe0dc0bc475cc49e7237fb2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654006"
---
# Schnittstellen ICoreWebView2CapturePreviewCompletedHandler 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

Der Aufrufer implementiert diese Methode, um das Ergebnis der CapturePreview-Methode zu empfangen.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.

Das Ergebnis wird in den Stream geschrieben, der im CapturePreview-Methodenaufruf bereitgestellt wird.

## Member

#### Invoke 

Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.

> Public HRESULT [Invoke](#invoke)(HRESULT-Ergebnis)

