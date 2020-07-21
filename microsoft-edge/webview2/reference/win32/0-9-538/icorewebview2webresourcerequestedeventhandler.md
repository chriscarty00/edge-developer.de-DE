---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 3cdafae6480a3bf6e3a5bf96f7e7fba1ae8cc77c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884519"
---
# Schnittstellen ICoreWebView2WebResourceRequestedEventHandler 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

Wird ausgelöst, wenn eine URL-Anforderung (über Netzwerk, Datei usw.) in der WebView für einen Ressourcenkontext Filter und eine in AddWebResourceRequestedFilter angegebene URL für die Webressource erstellt wird.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.

Der Host kann die Anforderung anzeigen und ändern oder eine Antwort in einem ähnlichen Muster wie http bereitstellen, in diesem Fall ist die Anforderung sofort abgeschlossen. Dieser enthält möglicherweise keine Anforderungs Kopfzeilen, die vom Netzwerkstapel hinzugefügt werden, wie Autorisierungs Kopfzeilen.

## Member

#### Invoke 

Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.

> Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) * Sender; [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) * args)

