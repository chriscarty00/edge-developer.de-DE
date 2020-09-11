---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012041"
---
# Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse Klasse 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Inhalt](#content) | HTTP-Antwortinhalt als Stream.
[Header](#headers) | Überschriebene HTTP-Antwortheader.
[ReasonPhrase](#reasonphrase) | Der HTTP-Antwort Grund Ausdruck.
[Statuscode](#statuscode) | Der HTTP-Antwortstatuscode.

## Member

#### Inhalt 

HTTP-Antwortinhalt als Stream.

> [Inhalte](#content) öffentlicher Datenströme

Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist. Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern. NULL bedeutet keine Inhaltsdaten. IStream-Semantik wird angewendet (geben Sie S_OK ein, um Anrufe zu lesen, bis alle Daten erschöpft sind).

#### Header 

Überschriebene HTTP-Antwortheader.

> öffentliche [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) - [Header](#headers)

#### ReasonPhrase 

Der HTTP-Antwort Grund Ausdruck.

> public String [ReasonPhrase](#reasonphrase)

#### Statuscode 

Der HTTP-Antwortstatuscode.

> public int [Statuscode](#statuscode)

