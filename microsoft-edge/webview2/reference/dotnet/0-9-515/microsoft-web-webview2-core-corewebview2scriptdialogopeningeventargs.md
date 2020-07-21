---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 4e7cd20b982d829be6d304eea1f3f60759cc503f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884855"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Ereignis-args für das ScriptDialogOpening-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[DefaultText](#defaulttext) | Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.
[Art](#kind) | Das Dialogfeld "JavaScript-Art"
[Meldung](#message) | Die Meldung des Dialogfelds.
[ResultText](#resulttext) | Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.
[URI](#uri) | Der URI der Seite, die das Dialogfeld angefordert hat.
[Annehmen](#accept) | Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.
[GetDeferral](#getdeferral) | Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.

## Member

#### DefaultText 

Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.

> public String [DefaultText](#defaulttext)

Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.

#### Art 

Das Dialogfeld "JavaScript-Art"

> öffentliche CoreWebView2ScriptDialogKind- [Art](#kind)

Akzeptieren, bestätigen, auffordern oder beforeunload.

#### Meldung 

Die Meldung des Dialogfelds.

> [Nachricht](#message) für öffentliche Zeichenfolge

Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.

#### ResultText 

Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.

> public String [ResultText](#resulttext)

Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert. Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.

#### URI 

Der URI der Seite, die das Dialogfeld angefordert hat.

> öffentlicher Zeichenfolgen- [URI](#uri)

#### Annehmen 

Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.

> public void [Accept](#accept)()

Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird. Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.

#### GetDeferral 

Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.

> Public CoreWebView2Deferral [getstundungal](#getdeferral)()

Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.

