---
description: Dieser Leitfaden enthält eine Übersicht über die Grundlagen und Tools von PWA für das Erstellen von progressiven Web-Apps unter Windows.
title: Erste Schritte mit Progressive Web-Apps (Chrom)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, PWABuilder, Web-Manifest, Service Worker, Push
ms.openlocfilehash: a9a0cad2d771e52b783053e36f0f23dec5d8e70c
ms.sourcegitcommit: 515522959f517e194f93a27f5d360690600edd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894710"
---
# Erste Schritte mit Progressive Web-Apps (Chrom)  

Progressive Web-Apps \ (PWAs \) sind Web-Apps, die mit App-ähnlichen Features wie Installation, Offline-Unterstützung und Push-Benachrichtigungen [schrittweise verbessert][WikiProgressiveEnhancement] werden.  Sie können auch Ihre PWA für App-Stores, einschließlich des Microsoft Store, sowie Google Play, Mac App Store und vieles mehr verpacken.  Der Microsoft Store ist der in Windows 10 integrierte kommerzielle App Store.  

Das folgende Handbuch bietet Ihnen einen Überblick über die Grundlagen von PWA, indem Sie eine einfache Web-App erstellen und diese als PWA erweitern.  Das fertige Projekt funktioniert in modernen Browsern.  

> [!TIP]
> Sie können [PWABuilder][PwaBuilder] verwenden, um eine neue PWA zu erstellen, Ihre vorhandene PWA zu erweitern oder Ihre PWA für App-Stores zu verpacken.  

## Voraussetzungen  

*   Verwenden Sie [vs-Code][VisualstudioCodeMain] zum Bearbeiten Ihres PWA-Quellcodes.  
*   Verwenden Sie [Node.js][NodejsMain] als lokalen Webserver.  

## Einrichten einer einfachen Web-App  

Wenn Sie eine leere Web-App erstellen möchten, führen Sie die Schritte im [Knoten Express-App-Generator][ExpressjsApplicationGenerator]aus, und benennen Sie Ihre APP `MySamplePwa` .  

Führen Sie in der Eingabeaufforderung die folgenden Befehle aus.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Die Befehle erstellen eine leere Web-App und installieren alle Abhängigkeiten.  

Sie haben jetzt eine einfache, funktionelle Web-App.  Führen Sie den folgenden Befehl aus, um ihn zu starten.  

```shell
npm start
```  

Navigieren Sie nun zu `http://localhost:3000` ihrer neuen Web-App, um Sie anzuzeigen.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ausführen ihrer neuen PWA auf localhost":::
   Ausführen ihrer neuen PWA auf localhost
:::image-end:::

## Erste Schritte beim Erstellen einer PWA  

Nachdem Sie nun über eine einfache Web App verfügen, können Sie Sie als PWA erweitern, indem Sie die drei Anforderungen für PWAs hinzufügen.<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [Https](#step-1---use-https), ein [Web App-Manifest](#step-2---create-a-web-app-manifest)und ein [Dienstmitarbeiter](#step-3---add-a-service-worker).  

### Schritt 1 – Verwenden von HTTPS  

Wichtige Teile der PWA-Plattform, wie [Dienstmitarbeiter][MDNServiceWorkerApi], erfordern die Verwendung von HTTPS.  Wenn Ihre PWA live geschaltet wird, müssen Sie Sie in einer HTTPS-URL veröffentlichen.  

Zu Debugging-Zwecken ermöglicht Microsoft Edge auch `http://localhost` die Verwendung der PWA-APIs.  

Wenn Sie [Ihre Web-App als Live Website veröffentlichen][VisualStudioNodejsTutorialPublishAzureAppService] \ (beispielsweisedurch Einrichten eines [Azure Free-Kontos][AzureCreateFreeAccount]\), müssen Sie sicherstellen, dass Ihr Server für HTTPS konfiguriert ist.  Wenn Sie den [Microsoft Azure-App-Dienst][AzureWebApps] zum Hosten Ihrer Website verwenden, wird diese standardmäßig über HTTPS bereitgestellt.  

Das folgende Handbuch wird `http://localhost` zum Erstellen ihrer PWA-Anwendung verwendet.  

### Schritt 2: Erstellen eines Web App-Manifests  

Bei einem [Web App-Manifest][MDNWebAppManifest] handelt es sich um eine JSON-Datei, die Metadaten zu ihrer app enthält, wie Name, Beschreibung, Symbole und vieles mehr.  

So fügen Sie ein App-Manifest zur Web-App hinzu:  

1.  **Klicken Sie**im vs-Code auf  >  **Ordner öffnen** , und wählen Sie das Verzeichnis aus, das `MySamplePwa` Sie zuvor erstellt haben.  
1.  Drücken Sie, `Ctrl` + `N` um eine neue Datei zu erstellen, und fügen Sie den folgenden Codeausschnitt ein.  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  Speichern Sie die Datei als `/MySamplePwa/public/manifest.json` .  
1.  Fügen Sie ein 512x512-App-Symbolbild mit dem Namen hinzu `icon512.png` `/MySamplePwa/public/images` .  Sie können das [Beispielbild][ImagePwa] für Testzwecke verwenden.  
1.  Öffnen Sie im vs-Code, `/public/index.html` und fügen Sie den folgenden Code Ausschnitt innerhalb des `<head>` Tags hinzu.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Schritt 3: Hinzufügen eines Dienst Mitarbeiters  

Dienstmitarbeiter sind die Schlüsseltechnologie hinter PWAs und ermöglichen Szenarien wie offline Support, erweiterte Zwischenspeicherung und Ausführen von Hintergrundaufgaben, die zuvor auf systemeigene apps reduziert wurden.  

Dienstmitarbeiter sind Hintergrundaufgaben, die Netzwerkanforderungen aus Ihrer Web-App abfangen.  Sie führen Aufgaben aus, auch wenn Ihre PWA nicht ausgeführt wird, beispielsweise das Servieren von angeforderten Ressourcen aus einem Cache, Senden von Push-Benachrichtigungen, Ausführen von Hintergrund-FETCH-Aufgaben, Badges-Symbolen usw.  Dienstmitarbeiter werden in einer speziellen JavaScript-Datei definiert.  Weitere Informationen finden Sie unter [Verwenden von Servicemitarbeitern][MDNUsingServiceWorkers] und [Service Worker-API][MDNServiceWorkerApi].  

Um einen Dienstmitarbeiter in Ihrem Projekt zu erstellen, verwenden Sie das **Cache-First-Netzwerkdienst-Worker-** Rezept aus dem [PWA-Generator][PwaBuilderServiceWorker].  

1.  Navigieren Sie zu [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], wählen Sie den **Cache-First-Netzwerk** Dienstmitarbeiter aus, und klicken Sie auf die Schaltfläche **herunterladen** .  Die heruntergeladene Datei enthält die folgenden Dateien:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  Kopieren Sie die heruntergeladenen Dateien `public` in den Ordner in Ihrem Web App-Projekt.  
    
1.  Öffnen Sie im vs-Code `/public/index.html` den folgenden Codeausschnitt, und fügen Sie ihn in das `<head>` Tag ein.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Ihre Web-App verfügt nun über einen Dienstmitarbeiter, der die Cache-First-Strategie verwendet, die Ressourcen wie Bilder, JS, CSS und HTML zuerst aus dem Cache abruft und nach Bedarf zurück zum Netzwerk fällt.  

Führen Sie die folgenden Schritte aus, um zu überprüfen, ob Ihre Dienstmitarbeiter ausgeführt werden.  

1.  Navigieren Sie mithilfe von zu Ihrer Web-App `http://localhost:3000` .  Wenn Ihre Web-App nicht verfügbar ist, führen Sie den folgenden Befehl aus.   
    
    ```shell
    npm start
    ```
    
1.  Wählen Sie in Microsoft Edge aus, `F12` um den Microsoft Edge-devtools zu öffnen.  Wählen Sie **Anwendung**und dann **Servicemitarbeiter** aus, um die Servicemitarbeiter anzuzeigen.  Wenn der Dienstmitarbeiter nicht angezeigt wird, müssen Sie möglicherweise die Seite aktualisieren.  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Übersicht über den Microsoft Edge devtools Service Worker":::
       Übersicht über den Microsoft Edge devtools Service Worker
    :::image-end:::
    
1.  Zeigen Sie den Service Worker-Cache an, indem Sie den **Cachespeicher** erweitern und **pwabuilder-precache**auswählen.  Sie sollten alle Ressourcen sehen, die vom Dienstmitarbeiter zwischengespeichert wurden, wie etwa das App-Symbol, App-Manifest, CSS-und JavaScript-Dateien.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Service Worker-Cache in Microsoft Edge devtools":::
       Service Worker-Cache in Microsoft Edge devtools (F12)
    :::image-end:::
    
1.  Testen Sie Ihre PWA als offline-app.  Klicken Sie in Microsoft Edge devtools \ ( `F12` \) auf **Netzwerk** , und ändern Sie dann den **Online** Status in **Offline**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Festlegen der APP auf den Offlinemodus in Microsoft Edge devtools":::
       Festlegen der APP auf den Offlinemodus in Microsoft Edge devtools
    :::image-end:::
    
1.  Aktualisieren Sie Ihre APP, und Sie sollten Sie offline arbeiten sehen, indem Sie die Ressourcen ihrer App aus dem Cache servieren.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA, die offline ausgeführt wird":::
       PWA, die offline ausgeführt wird
    :::image-end:::
    
## Hinzufügen von Push-Benachrichtigungen zu ihrer PWA  

Sie können PWAs erstellen, die Push-Benachrichtigungen unterstützen, indem Sie die folgenden Aufgaben ausführen.  

1.  Abonnieren eines Messagingdiensts mithilfe der [Push-API][MDNPushApi]  
1.  Anzeigen von Popupmeldungen, wenn eine Nachricht vom Dienst mithilfe der [Benachrichtigungs-API][MDNNotificationsApi] empfangen wird  

Wie bei Service Mitarbeitern sind dies standardbasierte APIs, die in Browsern funktionieren, sodass Sie den Code nur einmal schreiben müssen, damit er überall funktioniert, wo PWAs unterstützt werden.  Weitere Informationen zum Übermitteln von Push-Nachrichten an verschiedene Browser auf dem Server finden Sie in der [Web-Push][NPMWebPush] -Open-Source-Bibliothek.  

Die folgenden Schritte wurden von der Push Rich-Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] , die von Mozilla bereitgestellt wurde, mit einer Reihe anderer nützlicher Web Push-und Service-Worker-Rezepte angepasst.  

### Schritt 1: Generieren von VAPID-Schlüsseln  

Push-Benachrichtigungen erfordern VAPID \ (freiwillige Application Server Identification \)-Schlüssel, um Push-Nachrichten an den PWA-Client zu senden.  Es stehen mehrere VAPID-Schlüsselgeneratoren online zur Verfügung \ (beispielsweise [vapidkeys.com][VapidkeysMain]\).  Nach der Generierung sollten Sie ein JSON-Objekt mit einem öffentlichen und einem privaten Schlüssel abrufen.  Speichern Sie die Schlüssel für die nachfolgenden Schritte im folgenden Lernprogramm.  Informationen dazu, wie VAPID und webpush funktionieren, finden Sie unter [Senden von VAPID identifizierten webpush-Benachrichtigungen über den Push-Dienst von Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].  

### Schritt 2 – abonnieren von Push-Benachrichtigungen  

Dienstmitarbeiter behandeln Push-Ereignisse und Popup Benachrichtigungs Interaktionen in ihrer PWA.  Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind, um die PWA to Server-Push-Benachrichtigungen zu abonnieren.  

*   Ihre PWA ist installiert, aktiv und registriert  
*   Ihr Code, der die Abonnement Aufgabe ausführt, befindet sich im Hauptbenutzeroberflächen Thread der PWA  
*   Sie verfügen über Netzwerkkonnektivität  

Bevor ein neues Push-Abonnement erstellt wird, überprüft Microsoft Edge, ob der Benutzer die PWA-Berechtigung zum Empfangen von Benachrichtigungen gewährt hat.  Wenn dies nicht der Fall ist, wird der Benutzer vom Browser zur Genehmigung aufgefordert.  Wenn die Berechtigung verweigert wird, wird die Anforderung zum Auslösen `registration.pushManager.subscribe` einer `DOMException` , die verarbeitet werden muss, ausgelöst.  Weitere Informationen zur Berechtigungsverwaltung finden Sie unter [Push-Benachrichtigungen in Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

Fügen Sie in `pwabuilder-sw-register.js` der Datei den folgenden Codeausschnitt an.  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
                });
            });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

Weitere Informationen finden Sie unter [pushmanager][MDNPushManager] und [Web-Push][NPMWebPushUsage].  

### Schritt 3 – überwachen von Push-Benachrichtigungen  

Nachdem nun ein Abonnement in ihrer PWA eingerichtet wurde, fügen Sie dem Dienstmitarbeiter Handler hinzu, um auf Push-Ereignisse zu reagieren \ (vom Server gesendet \), um Popupbenachrichtigungen mit den Daten einer empfangenen Nachricht anzuzeigen.  Sie müssen einen Click-Handler hinzufügen, um die folgenden Aufgaben auszuführen.  
*   Schließen der Popupbenachrichtigung  
*   Öffnen, fokussieren oder öffnen und fokussieren offener Fenster  
*   Öffnen und fokussieren eines neuen Fensters, um eine PWA-Clientseite anzuzeigen  

`pwabuilder-sw.js`Fügen Sie in der Datei die folgenden Handler hinzu.  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current notification is already open and focuses it.
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### Schritt 4 – probieren Sie es aus  

Führen Sie die folgenden Schritte aus, um Push-Benachrichtigungen in ihrer PWA zu testen.  

1.  Navigieren Sie zu ihrer PWA unter `http://localhost:3000` .  Wenn Ihr Dienstmitarbeiter ihre PWA-Benachrichtigung für Push-Benachrichtigungen aktiviert und versucht, Sie zu abonnieren, werden Sie von Microsoft Edge dazu aufgefordert, zulassen, dass Ihre PWA-Benachrichtigungen angezeigt werden.  Wählen Sie **zulassen**aus.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Dialogfeld ' Berechtigung ' zum Aktivieren von Benachrichtigungen":::
       Dialogfeld ' Berechtigung ' zum Aktivieren von Benachrichtigungen
    :::image-end:::
    
    
1.  Simulieren Sie eine serverseitige Push-Benachrichtigung.  Wenn Ihre PWA `http://localhost:3000` in Ihrem Browser geöffnet ist, wählen Sie aus, `F12` um die devtools zu öffnen.  Wählen Sie **Application**  >  **Service Worker**  >  **Push** aus, um eine Test-Push-Benachrichtigung an Ihre PWA zu senden.  Es sollte eine Push-Benachrichtigung in der Nähe der Taskleiste angezeigt werden.  
    
    :::image type="complex" source="./media/devtools-push.png" alt-text="Pushen einer Benachrichtigung von devtools":::
       Pushen einer Benachrichtigung von devtools
    :::image-end:::
     
    Wenn Sie keine Popupbenachrichtigung \ (oder Activate \) auswählen, wird Sie nach einigen Sekunden geschlossen und in Ihrem Windows-Wartungs Center in der Warteschlange.  
    
    :::image type="complex" source="./media/windows-action-center.png" alt-text="Benachrichtigungen im Windows-Wartungs Center":::
       Benachrichtigungen im Windows-Wartungs Center
    :::image-end:::
    
    
## Nächste Schritte  

Im folgenden finden Sie eine Liste weiterer Aufgaben, die Sie beim Erstellen von PWAs in der realen Welt kennenlernen sollten:  

*  Verwalten und Speichern von Pushabonnement-Abonnements  
*  [Verschlüsseln][NPMWebPushEncrypt] von Nutzdaten  
*  Dynamisches Design  
*  Deep-Linking  
*  [Browserübergreifende Tests][BrowserStackTestEdgeBrowser]  
*  Implementieren bewährter Methoden wie [webhint][Webhint]  

## Weitere Informationen  

*   [Progressive Web-Apps auf MDN Web docs][MDNProgressiveWebApps].  
*   [Progressive Web-Apps auf Web. dev][WebDevProgressiveWebApps].  
*   [Hacker-Nachrichten Leser als Progressive Web-Apps][HackerNewsProgressiveWebApps] – vergleicht unterschiedliche Frameworks und Leistungsmuster für die Implementierung einer Stichprobe \ (Hacker Newsreader \) PWA.  

<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Bereitstelleneiner Node.js-App für Azure mit vs-Code | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Erstellen eines Azure Free-Kontos | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web-Apps | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Web-Benachrichtigungen in Microsoft Edge | Windows-Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio-Code"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "﻿Kostenlose Tests für Microsoft Edge-Browser unter Windows 10 | BrowserStack"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Express-Anwendungsgenerator | Express" 

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Hacker-Nachrichten Leser als Progressive Web-Apps"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Progressive Web-Apps \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "Pushmanager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Verwenden von Service Mitarbeitern | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifest | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Senden von VAPID identifizierten webpush-Benachrichtigungen über den Push-Dienst von Mozilla | Mozilla-Dienste"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Push | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Verwendung-Web-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Progressive Web-Apps"  

[PwaBuilder]: https://www.pwabuilder.com "PWA-Generator"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Dienstmitarbeiter | PWA-Generator"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich-Demo | ServiceWorker Cookbook"  

[VapidkeysMain]: https://vapidkeys.com "Secure VAPID-Schlüssel Generator | VapidKeys" 

[Webhint]: https://sonarwhal.com "webhint, das Hinweis Modul für bewährte Webmethoden"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Progressive Web-Apps | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Progressive Verbesserung | Wikipedia"  
