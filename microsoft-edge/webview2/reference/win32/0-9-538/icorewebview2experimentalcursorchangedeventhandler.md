---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b44bd47f5352179abcc06ef5fd5b8f613bde455e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698815"
---
# Schnittstellen ICoreWebView2ExperimentalCursorChangedEventHandler 

> [!NOTE]
> Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

Der Aufrufer implementiert diese Schnittstelle, um Cursor Ereignisse zu empfangen.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.

Verwenden Sie die Cursor-Eigenschaft, um den neuen Cursor abzurufen.

## Member

#### Invoke 

Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.

> Public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) * Sender; IUnknown * args)

Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.

