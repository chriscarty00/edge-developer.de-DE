---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
ms.openlocfilehash: 44fc4f47aa10a7e409ac584cb75b750048056e47
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886527"
---
# Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs Klasse 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Ereignis-args für das WebResourceResponseReceived-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Anforderung](#request) | Web-Ressourcen Anforderungsobjekt
[Antwort](#response) | Webressourcen-Antwortobjekt
[PopulateResponseContentAsync](#populateresponsecontentasync) | Async-Methode, um den Inhaltsdatenstrom der Antwort anzufordern.

## Member

#### Anforderung 

Web-Ressourcen Anforderungsobjekt

> öffentliche HttpRequestMessage- [Anforderung](#request)

Alle Änderungen an diesem Objekt werden ignoriert.

#### Antwort 

Webressourcen-Antwortobjekt

> öffentliche HttpResponseMessage- [Antwort](#response)

Alle Änderungen an diesem Objekt werden ignoriert.

#### PopulateResponseContentAsync 

Async-Methode, um den Inhaltsdatenstrom der Antwort anzufordern.

> Public Async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()

