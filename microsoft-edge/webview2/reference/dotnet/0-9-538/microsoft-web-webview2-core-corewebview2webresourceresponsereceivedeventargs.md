---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
ms.openlocfilehash: a8c988fdfee72ed22e74886b440819d7a9d6fe24
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010510"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

