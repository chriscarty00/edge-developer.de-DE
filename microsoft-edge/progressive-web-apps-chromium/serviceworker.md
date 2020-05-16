---
title: Verwenden von Service Mitarbeitern zum Verwalten von Netzwerkanforderungen und Push-Benachrichtigungen
description: Dienstmitarbeiter sind webarbeiter, die dazu beitragen, die Leistung zu verbessern, auf unterschiedliche Netzwerkbedingungen zu reagieren und die Konnektivität mit Ihrer Web-Anwendung zu erhöhen.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 9bf573b668ade351716b69965f653e05857c32ec
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659300"
---
# Verwenden von Service Mitarbeitern zum Verwalten von Netzwerkanforderungen und Push-Benachrichtigungen

Dienstmitarbeiter sind eine spezielle Art von Web-Worker mit der Möglichkeit, mithilfe der API alle Netzwerkanforderungen abzufangen, zu ändern und auf Sie zu reagieren `Fetch` .  Dienstmitarbeiter können auf die `Cache` API und asynchrone clientseitige Datenspeicher zugreifen, beispielsweise `IndexedDB` zum Speichern von Ressourcen.  

## Registrieren eines Dienst Mitarbeiters  

Ähnlich wie andere Web-Worker müssen Service Mitarbeiter in einer separaten Datei vorhanden sein. Sie verweisen auf diese Datei, wenn Sie den Dienstmitarbeiter registrieren, wie im folgenden Codeausschnitt dargestellt.  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

Moderne Browser bieten unterschiedliche Supportstufen für Dienstmitarbeiter. Daher empfiehlt es sich, das vorhanden sein des Objekts zu testen, bevor ein `serviceWorker` Dienstmitarbeiter bezogener Code ausgeführt wird. Im obigen Codeausschnitt wird ein Dienstmitarbeiter mit der Datei registriert, die sich im `serviceworker.min.js` Stammverzeichnis der Website befindet. Stellen Sie sicher, dass die JavaScript-Datei, die ihren Dienstmitarbeiter definiert, im Verzeichnis der obersten Ebene vorhanden ist, das verwaltet werden soll \ (das als Bereich der Dienstmitarbeiter bezeichnet wird).  Im obigen Codeausschnitt wird die Datei im Stammverzeichnis gespeichert, und der Dienstmitarbeiter verwaltet alle Seiten in der Domäne. Wenn die Dienst Arbeitskraft Datei in einem Verzeichnis gespeichert wurde `js` , würde der Bereich des Dienst Arbeitsthreads das `js` Verzeichnis und alle Unterverzeichnisse sein.  Als bewährte Methode sollten Sie die Service Worker-Datei im Stammverzeichnis Ihrer Website platzieren, es sei denn, Sie müssen den Umfang ihrer Dienstmitarbeiter reduzieren.  

## Der Service Worker-Lebenszyklus  

Der Lebenszyklus eines Dienstmitarbeiter besteht aus mehreren Schritten, wobei jeder Schritt ein Ereignis auslöst. Sie können diesen Ereignissen Listener hinzufügen, um Code auszuführen, um eine Aktion auszuführen. Die folgende Liste enthält eine allgemeine Übersicht über den Lebenszyklus und verwandte Ereignisse von Servicemitarbeitern. 

1. Registrieren Sie den Dienstmitarbeiter.  
1.  Der Browser lädt die JavaScript-Datei herunter, installiert den Dienstmitarbeiter und löst das `install` Ereignis aus. Sie können das `install` Ereignis verwenden, um wichtige und langlebige Dateien, wie etwa CSS-Dateien, JavaScript-Dateien, Logo Bilder, Offlineseiten usw., auf Ihrer Website vorab zwischenzuspeichern.  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  Der Dienstmitarbeiter wird aktiviert, wodurch das Ereignis ausgelöst wird `activate` .  Verwenden Sie dieses Ereignis, um veraltete Caches zu bereinigen.  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  Der Dienstmitarbeiter kann ausgeführt werden, wenn die Seite aktualisiert wird, oder wenn der Benutzer zu einer neuen Seite auf der Website navigiert. Wenn Sie den Dienstmitarbeiter ohne Wartezeit ausführen möchten, verwenden Sie die `self.skipWaiting()` Methode während des `install` Ereignisses.  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  Der Dienstmitarbeiter wird nun ausgeführt.     
    
## Verwenden von FETCH in Service Mitarbeitern  

Das Hauptereignis, das Sie in einem Dienstmitarbeiter verwenden, ist das `fetch` Ereignis.  Das `fetch` Ereignis wird jedes Mal ausgeführt, wenn der Browser versucht, auf Inhalte im Bereich der Dienstmitarbeiter zuzugreifen. Der folgende Codeausschnitt zeigt, wie dem FETCH-Ereignis ein Listener hinzugefügt wird.  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

Innerhalb des `fetch` Handlers können Sie steuern, ob eine Anforderung an das Netzwerk wechselt, aus dem Cache abgerufen wird usw.  Der von Ihnen verwendete Ansatz variiert je nach Art der angeforderten Ressource, wie häufig Sie aktualisiert wird, und der anderen Geschäftslogik, die für Ihre Anwendung eindeutig ist.  Hier sind einige Beispiele dafür, was Sie tun können:  

*   Falls verfügbar, geben Sie eine Antwort aus dem Cache zurück, andernfalls Fallback, um die Ressource über das Netzwerk anzufordern.  
*   Abrufen einer Ressource aus dem Netzwerk, Zwischenspeichern einer Kopie und Zurückgeben der Antwort.
*   Zulassen, dass Benutzer eine Einstellung zum Speichern von Daten angeben. 
*   Stellen Sie für bestimmte Bildanforderungen ein Platzhalterbild zur Verfügung.  
*   Direktes Generieren einer Antwort im Dienstmitarbeiter.  

## Pushbenachrichtigungen  

Dienstmitarbeiter können Benachrichtigungen an Benutzer senden. Push-Benachrichtigungen sind hilfreich, wenn Benutzer aufgefordert werden sollen, Ihre Anwendung nach Ablauf einiger Zeit erneut zu aktivieren. Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise und Demo zu Push-Benachrichtigungen][AzurewebsitesWebpushdemo].  

## Weitere Informationen  

Weitere Informationen zu Service Mitarbeitern finden Sie in der folgenden Liste verwandter Themen.  

*   [Offline Arbeiten von PWAs mit Service Mitarbeitern][MDNPwasMakingOfflineServiceWorkers]  
*   [So aktivieren Sie PWAs mit Benachrichtigungen und Push][MDNPwasMakeReengageablesingNotificationsPush]  

<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Web-Push-Benachrichtigungen |  Microsoft Edge-Demos"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Offline Arbeiten von PWAs mit Service Mitarbeitern – PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "So aktivieren Sie PWAs mit Benachrichtigungen und Push-PWAs | MDN"  
