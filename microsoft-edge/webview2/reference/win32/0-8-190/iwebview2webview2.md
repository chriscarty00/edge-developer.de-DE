---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 64dac6c56576b618cbdc84da2c8fcbcd0e41028f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884736"
---
# 0.8.355-Interface-IWebView2WebView2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView2
  : public IUnknown
```

Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Stop](#stop) | Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.

Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert. Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.

## Member

#### Stop 

Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.

> öffentlicher HRESULT- [Stopp](#stop)()

