---
description: Threadingmodell
title: Threadingmodell
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 61e3b7fc8d25e2a1ce9c60fb84f5f39ba43f281b
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013737"
---
# Threadingmodell 

Das WebView2-Steuerelement basiert auf dem [Component-Objektmodell (com)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) und muss auf einem [Single Threaded Apartments (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) -Thread ausgeführt werden.

## Thread Sicherheit  

Der WebView2 muss in einem UI-Thread erstellt werden.  Insbesondere ein Thread mit einer Nachrichten Pumpe.  Alle Rückrufe treten für diesen Thread auf, und Anforderungen an die WebView2 müssen in diesem Thread ausgeführt werden.  Es ist nicht sicher, die WebView2 aus einem anderen Thread zu verwenden.  

Die einzige Ausnahme ist die `Content` Eigenschaft von `CoreWebView2WebResourceRequest` .  Der `Content` Eigenschaftendaten Strom wird aus einem Hintergrundthread gelesen.  Der Datenstrom sollte agil sein oder aus einem background-STA erstellt werden, um die Auswirkungen auf die Leistung des UI-Threads zu verhindern.  

## Reentranz  

Rückrufe, einschließlich Ereignishandlern und Vervollständigungs Handlern, werden seriell ausgeführt.  Wenn Sie einen Ereignishandler ausführen und eine Nachrichtenschleife beginnen, können keine anderen Ereignishandler oder Abschluss Rückrufe auf eine Art und Weise gestartet werden.  

## Verzögerungen  

Einige WebView2-Ereignisse lesen Werte, die für Ihre Ereignisargumente festgesetzt sind, oder führen nach Abschluss des Ereignishandlers eine Aktion aus.  Wenn Sie auch einen asynchronen Vorgang wie einen Ereignishandler ausführen müssen, können Sie die `GetDeferral` Methode für die Ereignisargumente der zugeordneten Ereignisse verwenden.  Das zurückgegebene verzögerte Objekt stellt sicher, dass der Ereignishandler erst dann als abgeschlossen betrachtet wird, wenn die `Complete` Methode von `Deferral` angefordert wird.  

Beispielsweise können Sie das Ereignis verwenden `NewWindowRequested` , um eine `CoreWebView2` Verbindung als untergeordnetes Fenster bereitzustellen, wenn der Ereignishandler abgeschlossen ist.  Wenn Sie das jedoch asynchron erstellen müssen `CoreWebView2` , fordern Sie die `GetDeferral` Methode für die `NewWindowRequestedEventArgs` .  Nachdem Sie den asynchronen erstellt haben `CoreWebView2` und die `NewWindow` Eigenschaft für die-Eigenschaft festlegen `NewWindowRequestedEventArgs` , wird die Anforderung `Complete` für das `Deferral` Objekt mithilfe der Methode zurückgegeben `GetDeferral` .  

<!-- links -->  
