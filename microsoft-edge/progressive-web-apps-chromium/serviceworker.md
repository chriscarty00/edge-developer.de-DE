---
title: Verwalten von Netzwerkanforderungen und Pushbenachrichtigungen mithilfe von Service Workers
description: Service Workers sind Web Workers, die dazu beitragen, die Leistung zu verbessern, auf unterschiedliche Netzwerkbedingungen zu reagieren und die Konnektivität mit Ihrer Webanwendung zu erhöhen.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 314acbbd5a2f423c274f92e815b2be4329ace9b8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399134"
---
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a>Verwalten von Netzwerkanforderungen und Pushbenachrichtigungen mithilfe von Service Workers

Service Workers sind ein spezieller Typ von Web Worker mit der Möglichkeit, alle Netzwerkanforderungen mithilfe der API abzufangen, zu ändern und auf diese zu `Fetch` reagieren.  Service Workers kann auf die API und asynchrone clientseitige Datenspeicher zugreifen, z. B. `Cache` , um Ressourcen zu `IndexedDB` speichern.  

## <a name="registering-a-service-worker"></a>Registrieren eines Dienstmitarbeiters  

Ähnlich wie andere Web Workers müssen Service Workers in einer separaten Datei vorhanden sein. Sie verweisen bei der Registrierung des Service Worker auf diese Datei, wie im folgenden Codeausschnitt gezeigt.  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

Moderne Browser bieten unterschiedliche Unterstützungsebenen für Service Workers. Daher ist es eine bewährte Methode, das Vorhandensein des Objekts zu testen, bevor Sie service `serviceWorker` workerbezogenen Code ausführen. Im obigen Codeausschnitt wird ein Service Worker mithilfe der Datei registriert, die sich `serviceworker.min.js` im Stammverzeichnis der Website befindet. Stellen Sie sicher, dass die JavaScript-Datei, die Ihren Dienstarbeitsmitarbeiter definiert, in dem Verzeichnis auf höchster Ebene vorhanden ist, das sie verwalten soll \(das als Bereich des Dienstarbeitsmitarbeiters\ bezeichnet wird).  Im vorherigen Codeausschnitt wird die Datei im Stammverzeichnis gespeichert, und der Service Worker verwaltet alle Seiten in der Domäne. Wenn die Dienstarbeitsdatei in einem Verzeichnis gespeichert wurde, würde der Bereich des Dienstarbeitsmitarbeiters das Verzeichnis und `js` `js` alle Unterverzeichnisse sein.  Als bewährte Methode sollten Sie die Dienstarbeitsdatei im Stammverzeichnis Ihrer Website platzieren, es sei denn, Sie müssen den Umfang Ihres Dienstmitarbeiters reduzieren.  

## <a name="the-service-worker-lifecycle"></a>Der Service Worker-Lebenszyklus  

Der Lebenszyklus eines Service Worker besteht aus mehreren Schritten, bei der jeder Schritt ein Ereignis auslöst. Sie können diesen Ereignissen Listener hinzufügen, um Code zum Ausführen einer Aktion ausführen zu können. Die folgende Liste enthält eine übersichtsbezogene Ansicht des Lebenszyklus und der zugehörigen Ereignisse von Servicemitarbeitern. 

1.  Registrieren Sie den Service Worker.  
1.  Der Browser lädt die JavaScript-Datei herunter, installiert den Service Worker und löst das Ereignis `install` aus. Sie können das Ereignis verwenden, um wichtige und langlebige Dateien wie `install` CSS-Dateien, JavaScript-Dateien, Logobilder, Offlineseiten und so weiter von Ihrer Website vorab zwischenspeichern.  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  Der Dienstmitarbeiter wird aktiviert, wodurch das Ereignis ausgelöst `activate` wird.  Verwenden Sie dieses Ereignis, um veraltete Caches zu bereinigen.  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  Der Dienstmitarbeiter kann ausgeführt werden, wenn die Seite aktualisiert wird oder wenn der Benutzer zu einer neuen Seite auf der Website navigiert. Wenn Sie den Service Worker ohne Wartezeit ausführen möchten, verwenden Sie die `self.skipWaiting()` -Methode während des `install` Ereignisses.  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  Der Dienstmitarbeiter wird jetzt ausgeführt.     
    
## <a name="using-fetch-in-service-workers"></a>Verwenden des Abrufs in Service Workers  

Das Hauptereignis, das Sie in einem Service Worker verwenden, ist das `fetch` Ereignis.  Das Ereignis wird jedes Mal ausgeführt, wenn der Browser versucht, auf `fetch` Inhalte im Bereich des Service Workers zu zugreifen. Der folgende Codeausschnitt zeigt, wie Sie dem Fetch-Ereignis einen Listener hinzufügen.  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

Innerhalb des Handlers können Sie steuern, ob eine Anforderung an das Netzwerk geht, aus dem Cache zurückgeht `fetch` und so weiter.  Der von Ihnen verwendete Ansatz variiert je nach Art der angeforderten Ressource, der Anzahl der Aktualisierungen und der anderen geschäftsbezogenen Logik, die für Ihre Anwendung eindeutig ist.  Im Folgenden finden Sie einige Beispiele dafür, was Sie tun können:  

*   Wenn verfügbar, geben Sie eine Antwort aus dem Cache zurück, andernfalls fallback, um die Ressource über das Netzwerk an anforderung.  
*   Rufen Sie eine Ressource aus dem Netzwerk ab, speichern Sie eine Kopie zwischen, und geben Sie die Antwort zurück.
*   Zulassen, dass Benutzer eine Einstellung zum Speichern von Daten angeben. 
*   Geben Sie ein Platzhalterbild für bestimmte Bildanforderungen an.  
*   Generieren Sie eine Antwort direkt im Service Worker.  
    
## <a name="push-notifications"></a>Pushbenachrichtigungen  

Servicemitarbeiter können Benachrichtigungen per Push an Benutzer senden. Pushbenachrichtigungen sind hilfreich, um Benutzer zum erneuten Interagieren mit Ihrer Anwendung nach einiger Zeit aufforderen. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise und Demo zu [Pushbenachrichtigungen.][AzurewebsitesWebpushdemo]  

## <a name="see-also"></a>Weitere Informationen  

Weitere Informationen zu Service Workers finden Sie in der folgenden Liste verwandter Themen.  

*   [Offlinebetrieb von PWAs mit Servicemitarbeitern][MDNPwasMakingOfflineServiceWorkers]  
*   [So können Sie PWAs mithilfe von Benachrichtigungen und Push wieder aktivieren][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Web-Pushbenachrichtigungen |  Microsoft Edge Demos"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Offlinebetrieb von PWAs mit Servicemitarbeitern – PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "So können Sie PWAs mithilfe von Benachrichtigungen und Push wieder aktivieren – PWAs | MDN"  
