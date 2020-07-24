---
description: Navigation
title: Navigation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895578"
---
# Navigationsereignisse  

Die normale Abfolge von Navigations Ereignissen ist,,, `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` und dann `NavigationCompleted` .  Die folgenden Ereignisse beschreiben den Zustand von WebView2 während jeder Navigation.  

| Sequenz | Ereignisname | Details |  
|:--- |:--- |:--- |  
| 1 | `NavigationStarting`  |  WebView2 beginnt zu navigieren, und die Navigation führt zu einer Netzwerkanforderung.  Der Host kann die Anforderung während des Ereignisses nicht zulassen.  |  
| 2 | `SourceChanged`  |  Die Quelle von WebView2 Änderungen an einer neuen URL.  Das Ereignis kann durch eine Navigation entstehen, die keine Netzwerkanforderung wie eine Fragment-Navigation verursacht.  |  
| 3 | `HistoryChanged`  |  Das Protokoll der WebView2-Updates als Ergebnis der Navigation.  |  
| 4 | `ContentLoading`  |  WebView startet das Laden von Inhalten für die neue Seite.  |  
| 5 | `NavigationCompleted`  |  WebView2 vervollständigt das Laden von Inhalten auf der neuen Seite.  |  

`navigations`Nachvollziehen jedes neuen Dokuments mithilfe der Navigations-ID \ ( `NavigationId` \).  Die `NavigationId` von WebView ändert sich jedes Mal, wenn eine erfolgreiche Navigation zu einem neuen Dokument vorliegt.

:::image type="complex" source="../media/navigation-graph.png" alt-text="Navigationsereignisse für Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   Navigationsereignisse für Microsoft Edge WebView2  
:::image-end:::  

> [!NOTE]
> Die vorherige Abbildung stellt Navigationsereignisse mit der gleichen `NavigationId` Eigenschaft für das jeweilige Ereignis arg dar.  

 `Navigations` Ereignisse mit unterschiedlichen `NavigationId` Ereignisinstanzen können sich überlappen.  Wenn Sie beispielsweise eine Navigation starten, müssen Sie auf das zugehörige Ereignis warten `NavigationStarting` .  Wenn Sie dann eine andere Navigation starten, sollten Sie das `NavigationStarting` Ereignis für die erste Navigation, gefolgt vom `NavigationStarting` Ereignis für die zweite Navigate, gefolgt vom `NavigationCompleted` Ereignis für die erste Navigation und dann alle restlichen geeigneten Navigationsereignisse für die zweite Navigation sehen.  
 
 In Fehlerfällen kann es sich um ein Ereignis handeln `ContentLoading` , das davon abhängt, ob die Navigation auf einer Fehlerseite fortgesetzt wird.  
 
 Im Fall einer HTTP-Umleitung gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile, bei denen nachfolgende Ereignisargumente die `IsRedirect` Eigenschaft festzulegen, jedoch `NavigationId` bleibt die gleiche.  
 
 Dasselbe Dokument `navigations` , beispielsweise das Navigieren zu einem Fragment, führt nicht zu dem `NavigationStarting` Ereignis und erhöht nicht das `NavigationId` .  

Zum Überwachen oder Abbrechen `navigations` innerhalb von unter Frames in der WebView verwenden Sie das `FrameNavigationStarting` und die Ereignisse, die `FrameNavigationCompleted` wie die entsprechenden nicht-Frame-Entsprechungs Ereignisse fungieren.  

<!-- links -->  
