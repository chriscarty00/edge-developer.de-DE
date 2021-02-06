---
description: Navigation
title: Navigation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/05/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: ac15b9f32a29c64bbdc2a7886fa654a2d71a5453
ms.sourcegitcommit: 4cea8cf99b5f12db9d2daba99bbf48f3ccc537fe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314797"
---
# Navigationsereignisse  

Die normale Abfolge von Navigationsereignissen ist `NavigationStarting` , , und dann `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .  Die folgenden Ereignisse beschreiben den Status von WebView2 während jeder Navigation.  

| Sequence | Ereignisname | Details |  
|:--- |:--- |:--- |  
| 1 | `NavigationStarting`  |  WebView2 beginnt zu navigieren, und die Navigation führt zu einer Netzwerkanforderung.  Der Host kann die Anforderung während des Ereignisses disallowen.  |  
| 2 | `SourceChanged`  |  Die Quelle von WebView2 ändert sich in eine neue URL.  Das Ereignis kann durch eine Navigation verursacht werden, die keine Netzwerkanforderung verursacht, z. B. eine Fragmentnavigation.  |  
| 3 | `HistoryChanged`  |  Der Verlauf von WebView2 wird als Ergebnis der Navigation aktualisiert.  |  
| 4 | `ContentLoading`  |  WebView2 beginnt mit dem Laden von Inhalten für die neue Seite.  |  
| 5 | `NavigationCompleted`  |  WebView2 schließt das Laden von Inhalten auf der neuen Seite ab.  |  

Verfolgen `navigations` Sie jedes neue Dokument mithilfe der Navigations-ID \( `NavigationId` \).  Die `NavigationId` WebView ändert sich jedes Mal, wenn eine erfolgreiche Navigation zu einem neuen Dokument besteht.

:::image type="complex" source="../media/navigation-graph.png" alt-text="Die Microsoft Edge WebView2-Navigationsereignisse" lightbox="../media/navigation-graph.png":::
   Die Microsoft Edge WebView2-Navigationsereignisse  
:::image-end:::  

> [!NOTE]
> Die vorherige Abbildung stellt Navigationsereignisse mit derselben `NavigationId` Eigenschaft für das entsprechende Ereignis arg dar.  

 `Navigations` Ereignisse mit unterschiedlichen `NavigationId` Ereignisinstanzen überlappen können.  Wenn Sie beispielsweise eine Navigation starten, müssen Sie auf das zugehörige Ereignis `NavigationStarting` warten.  Wenn Sie dann eine andere Navigation starten, sollte das Ereignis für die erste Navigation gefolgt vom Ereignis für die zweite Navigation angezeigt werden, gefolgt vom Ereignis für die erste Navigation und dann von allen anderen geeigneten Navigationsereignissen für die zweite `NavigationStarting` `NavigationStarting` `NavigationCompleted` Navigation.  
 
 In Fehlerfällen kann es je nachdem, ob die Navigation zu einer Fehlerseite fortgesetzt wird, ein Ereignis sein oder `ContentLoading` nicht.  
 
 Im Fall einer HTTP-Umleitung gibt es mehrere Ereignisse in einer Zeile, bei denen nachfolgende Ereignis-Args den Eigenschaftensatz `NavigationStarting` `IsRedirect` haben, dies bleibt jedoch `NavigationId` gleich.  
 
 Dasselbe Dokument, z. B. das Navigieren zu einem Fragment, führt nicht zu dem Ereignis `navigations` und erhöht nicht das `NavigationStarting` `NavigationId` .  

Verwenden Sie zum Überwachen oder Abbrechen innerhalb von Unterframes in der WebView die Ereignisse und die Ereignisse, die genau wie die entsprechenden Ereignisse, die keine Frames sind, `navigations` `FrameNavigationStarting` `FrameNavigationCompleted` agieren.  

<!-- links -->  
