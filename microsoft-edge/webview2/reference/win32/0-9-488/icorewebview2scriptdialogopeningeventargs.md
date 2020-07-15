---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a0372e9319a3dd260092b8bc96c693976b7f1fec
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880320"
---
# 0.9.515-Interface-ICoreWebView2ScriptDialogOpeningEventArgs 

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Ereignis-args für das ScriptDialogOpening-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Annehmen](#accept) | Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.
[get_DefaultText](#get_defaulttext) | Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.
[get_Kind](#get_kind) | Das Dialogfeld "JavaScript-Art"
[get_Message](#get_message) | Die Meldung des Dialogfelds.
[get_ResultText](#get_resulttext) | Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.
[get_Uri](#get_uri) | Der URI der Seite, die das Dialogfeld angefordert hat.
[GetDeferral](#getdeferral) | Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.
[put_ResultText](#put_resulttext) | Festlegen der ResultText-Eigenschaft

## Member

#### Annehmen 

Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.

> öffentliche HRESULT- [Annahme](#accept)()

Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird. Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.

#### get_DefaultText 

Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.

> Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR * DefaultText)

Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.

#### get_Kind 

Das Dialogfeld "JavaScript-Art"

> öffentliche HRESULT- [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND * Art)

Akzeptieren, bestätigen, auffordern oder beforeunload.

#### get_Message 

Die Meldung des Dialogfelds.

> öffentliche HRESULT- [get_Message](#get_message)(LPWSTR *-Meldung)

Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.

#### get_ResultText 

Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.

> Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR * ResultText)

Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert. Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.

#### get_Uri 

Der URI der Seite, die das Dialogfeld angefordert hat.

> Public HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### GetDeferral 

Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.

> öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * Stundung)

Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.

#### put_ResultText 

Festlegen der ResultText-Eigenschaft

> Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)

