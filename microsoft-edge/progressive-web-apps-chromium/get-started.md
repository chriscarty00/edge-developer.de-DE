---
description: Dieser Leitfaden enthält eine Übersicht über die Grundlagen und Tools von PWA für das Erstellen von Progressive Web-Apps (Chrom) unter Windows.
title: Erste Schritte mit Progressive Web-Apps (Chrom)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, PWABuilder, Web-Manifest, Service Worker, Push
ms.openlocfilehash: 7ad13f98f54c52891681d7591b21503c9d5825ff
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231223"
---
# Erste Schritte mit Progressive Web-Apps (Chrom)  

Progressive Web-Apps \ (PWAs \) sind Web-Apps, die [schrittweise verbessert][WikiProgressiveEnhancement]werden.  Zu den fortschrittlichen Erweiterungen gehören App-ähnliche Features wie Installation, Offline Support und Push-Benachrichtigungen.  Sie können auch Ihre PWA für App-Stores verpacken.  Zu den möglichen App Stores gehören der Microsoft Store, Google Play, Mac App Store und vieles mehr.  Der Microsoft Store ist der in Windows 10 integrierte kommerzielle App Store.  

Das folgende Handbuch bietet Ihnen einen Überblick über die Grundlagen von PWA, indem Sie eine einfache Web-App erstellen und diese als PWA erweitern.  Das fertige Projekt funktioniert in modernen Browsern.  

> [!TIP]
> Sie können [PWABuilder][PwaBuilder] verwenden, um eine neue PWA zu erstellen, Ihre vorhandene PWA zu erweitern oder Ihre PWA für App-Stores zu verpacken.  

## Voraussetzungen  

*   Verwenden Sie [Visual Studio-Code][VisualstudioCodeMain] zum Bearbeiten Ihres PWA-Quellcodes.  
*   Verwenden Sie [Node.js][NodejsMain] als lokalen Webserver.  
    
## Erstellen einer einfachen Web-App  

Wenn Sie eine leere Web-App erstellen möchten, führen Sie die Schritte im [Knoten Express-App-Generator][ExpressjsApplicationGenerator]aus, und benennen Sie Ihre APP `MySamplePwa` .  

Führen Sie in der Eingabeaufforderung die folgenden Befehle aus.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Die Befehle erstellen eine leere Web-App und installieren alle Abhängigkeiten.  

Sie verfügen jetzt über eine einfache, funktionelle Web-App.  Führen Sie den folgenden Befehl aus, um die Web-App zu starten.  

```shell
npm start
```  

Navigieren Sie nun zu `http://localhost:3000` ihrer neuen Web-App, um Sie anzuzeigen.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ausführen ihrer neuen PWA auf localhost" lightbox="./media/vs-nodejs-express-index.png":::
   Ausführen ihrer neuen PWA auf localhost
:::image-end:::

## Erste Schritte beim Erstellen einer PWA  

Nachdem Sie nun über eine einfache Web App verfügen, können Sie Sie als PWA erweitern, indem Sie die drei Anforderungen für PWAs hinzufügen.<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [Https](#step-1---use-https), ein [Web App-Manifest](#step-2---create-a-web-app-manifest)und ein [Dienstmitarbeiter](#step-3---add-a-service-worker).  

### Schritt 1 – Verwenden von HTTPS  

Wichtige Teile der PWA-Plattform, wie [Dienstmitarbeiter][MDNServiceWorkerApi], erfordern die Verwendung von HTTPS.  Wenn Ihre PWA live geschaltet wird, müssen Sie Sie in einer HTTPS-URL veröffentlichen.  

Zu Debugging-Zwecken ermöglicht Microsoft Edge auch `http://localhost` die Verwendung der PWA-APIs.  

[Veröffentlichen Sie Ihre Web-App als Live-Website][VisualStudioNodejsTutorialPublishAzureAppService], stellen Sie sicher, dass Ihr Server für HTTPS konfiguriert ist.  So können Sie beispielsweise ein [Azure Free-Konto][AzureCreateFreeAccount]erstellen.  Hosten Sie Ihre Website im [Microsoft Azure-App-Dienst][AzureWebApps] , und Sie wird standardmäßig über HTTPS bereitgestellt.  

Das folgende Handbuch wird `http://localhost` zum Erstellen ihrer PWA-Anwendung verwendet.  

### Schritt 2: Erstellen eines Web App-Manifests  

Bei einem [Web App-Manifest][MDNWebAppManifest] handelt es sich um eine JSON-Datei, die Metadaten zu ihrer app enthält, wie Name, Beschreibung, Symbole und vieles mehr.  

So fügen Sie ein App-Manifest zur Web-App hinzu:  

1.  Wählen Sie im Visual Studio-Code **Datei**  >  **Ordner öffnen** aus, und wählen Sie das Verzeichnis aus, das `MySamplePwa` Sie zuvor erstellt haben.  
1.  Wählen Sie aus, `Ctrl` + `N` um eine neue Datei zu erstellen, und fügen Sie den folgenden Codeausschnitt ein.  
    
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
1.  Öffnen Sie in Visual Studio-Code, `/public/index.html` und fügen Sie den folgenden Code Ausschnitt innerhalb des `<head>` Tags hinzu.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Schritt 3: Hinzufügen eines Dienst Mitarbeiters  

Dienstmitarbeiter sind die Schlüsseltechnologie hinter PWAs und ermöglichen Szenarien wie offline Support, erweiterte Zwischenspeicherung und Ausführen von Hintergrundaufgaben, die zuvor auf systemeigene apps reduziert wurden.  

Dienstmitarbeiter sind Hintergrundaufgaben, die Netzwerkanforderungen aus Ihrer Web-App abfangen.  Dienstmitarbeiter versuchen, Aufgaben abzuschließen, selbst wenn Ihre PWA nicht ausgeführt wird.  Aufgaben umfassen die folgenden Aktionen:  

*   Servieren von angeforderten Ressourcen aus einem Cache  
*   Senden von Pushbenachrichtigungen  
*   Ausführen von Hintergrund Abruf Aufgaben  
*   Badges-Symbole  
*   und vieles mehr  
    
Dienstmitarbeiter werden in einer speziellen JavaScript-Datei definiert.  Weitere Informationen finden Sie unter [Verwenden von Dienst Mitarbeitern][MDNUsingServiceWorkers] und [Service Worker-API][MDNServiceWorkerApi].  

Um einen Dienstmitarbeiter in Ihrem Projekt zu erstellen, verwenden Sie das **Cache-First-Netzwerkdienst-Worker-** Rezept aus dem [PWA-Generator][PwaBuilderServiceWorker].  

1.  Navigieren Sie zu [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], wählen Sie den **Cache-First-Netzwerk** Dienstmitarbeiter aus, und klicken Sie auf die Schaltfläche **herunterladen** .  Die heruntergeladene Datei enthält die folgenden Dateien:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  Kopieren Sie die heruntergeladenen Dateien `public` in den Ordner in Ihrem Web App-Projekt.  
1.  Öffnen Sie in Visual Studio-Code `/public/index.html` den folgenden Codeausschnitt, und fügen Sie ihn in das `<head>` Tag ein.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Ihre Web-App verfügt nun über einen Dienstmitarbeiter, der die Cache-First-Strategie verwendet.  Der neue Dienstmitarbeiter ruft zunächst Ressourcen aus dem Cache und nur nach Bedarf aus dem Netzwerk ab.  Zu den zwischengespeicherten Ressourcen gehören Bilder, JavaScript, CSS und HTML.

Führen Sie die folgenden Schritte aus, um zu überprüfen, ob Ihre Dienstmitarbeiter ausgeführt werden.  

1.  Navigieren Sie mithilfe von zu Ihrer Web-App `http://localhost:3000` .  Wenn Ihre Web-App nicht verfügbar ist, führen Sie den folgenden Befehl aus.   
    
    ```shell
    npm start
    ```
    
1.  Wählen Sie in Microsoft Edge aus, `F12` um den Microsoft Edge-devtools zu öffnen.  Wählen Sie **Anwendung**und dann **Servicemitarbeiter** aus, um die Servicemitarbeiter anzuzeigen.  Wenn der Dienstmitarbeiter nicht angezeigt wird, aktualisieren Sie die Seite.  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Übersicht über den Microsoft Edge devtools Service Worker" lightbox="./media/devtools-sw-overview.png":::
       Übersicht über den Microsoft Edge devtools Service Worker
    :::image-end:::
    
1.  Zeigen Sie den Service Worker-Cache an, indem Sie den **Cachespeicher** erweitern und **pwabuilder-precache**auswählen.  Alle vom Dienstmitarbeiter zwischengespeicherten Ressourcen sollten angezeigt werden.  Zu den vom Dienstmitarbeiter zwischengespeicherten Ressourcen gehören das App-Symbol, das App-Manifest, CSS-und JavaScript-Dateien.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Service Worker-Cache in Microsoft Edge devtools" lightbox="./media/devtools-cache.png":::
       Service Worker-Cache in Microsoft Edge devtools (F12)
    :::image-end:::
    
1.  Testen Sie Ihre PWA als offline-app.  Klicken Sie in Microsoft Edge devtools \ ( `F12` \) auf **Netzwerk** , und ändern Sie dann den **Online** Status in **Offline**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Festlegen der APP auf den Offlinemodus in Microsoft Edge devtools" lightbox="./media/devtools-offline.png":::
       Festlegen der APP auf den Offlinemodus in Microsoft Edge devtools
    :::image-end:::
    
1.  Aktualisieren Sie Ihre APP, und es sollte den Offline Mechanismus anzeigen, um die Ressourcen ihrer App aus dem Cache zu bedienen.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA, die offline ausgeführt wird" lightbox="./media/vs-nodejs-express-index.png":::
       PWA, die offline ausgeführt wird
    :::image-end:::
    
## Hinzufügen von Push-Benachrichtigungen zu ihrer PWA  

Sie können PWAs erstellen, die Push-Benachrichtigungen unterstützen, indem Sie die folgenden Aufgaben ausführen.  

1.  Abonnieren eines Messagingdiensts mithilfe der [Push-API][MDNPushApi]  
1.  Anzeigen einer Popupnachricht, wenn eine Nachricht vom Dienst mithilfe der [Benachrichtigungs-API][MDNNotificationsApi] empfangen wird  
    
Genau wie bei Service Mitarbeitern sind die Push-Benachrichtigungs-APIs standardbasierte APIs.  Die Push-Benachrichtigungs-APIs funktionieren in Browsern, sodass Ihr Code überall funktionieren kann, wenn PWAs unterstützt werden.  Weitere Informationen zum Bereitstellen von Push-Nachrichten an verschiedene Browser auf dem Server finden Sie unter [Web-Push][NPMWebPush].  

Die folgenden Schritte wurden von der Push Rich-Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] , die von Mozilla bereitgestellt wurde, mit einer Reihe anderer nützlicher Web Push-und Service-Worker-Rezepte angepasst.  

### Schritt 1: Generieren von VAPID-Schlüsseln  

Push-Benachrichtigungen erfordern VAPID \ (freiwillige Application Server Identification \)-Schlüssel, um Push-Nachrichten an den PWA-Client zu senden.  Es stehen mehrere VAPID-Schlüsselgeneratoren online zur Verfügung \ (beispielsweise [vapidkeys.com][VapidkeysMain]\).  Nach der Generierung sollten Sie ein JSON-Objekt mit einem öffentlichen und einem privaten Schlüssel abrufen.  Speichern Sie die Schlüssel für spätere Schritte im folgenden Lernprogramm.  Informationen zu VAPID und webpush finden Sie unter [Senden von VAPID identifizierten webpush-Benachrichtigungen mit dem Mozilla Push-Dienst][MozillaServicesSendingVapidWebPushNotificationsPush].  

### Schritt 2 – abonnieren von Push-Benachrichtigungen  

Dienstmitarbeiter behandeln Push-Ereignisse und Popup Benachrichtigungs Interaktionen in ihrer PWA.  Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind, um die PWA to Server-Push-Benachrichtigungen zu abonnieren.  

*   Ihre PWA ist installiert, aktiv und registriert  
*   Der Code zum Abschließen der Abonnement Aufgabe befindet sich im Hauptbenutzeroberflächen Thread der PWA  
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

Wenn Sie weitere Informationen wünschen, navigieren Sie zu [pushmanager][MDNPushManager] und [Web-Push][NPMWebPushUsage].  

### Schritt 3 – überwachen von Push-Benachrichtigungen  

Nachdem ein Abonnement in ihrer PWA erstellt wurde, fügen Sie dem Dienstmitarbeiter Handler hinzu, um auf Push-Ereignisse zu reagieren.  Das Push-Ereignis wird vom Server gesendet, um Popupbenachrichtigungen anzuzeigen.  Popupbenachrichtigungen zeigen Daten für eine empfangene Nachricht an.  Wenn Sie die folgenden Aufgaben ausführen möchten, müssen Sie einen Click-Handler hinzufügen.  

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
    
    // This attempts to display the current notification if it is already open and then focuses on it.
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

Führen Sie die folgenden Schritte aus, um Push-Benachrichtigungen für Ihre PWA zu testen.  

1.  Navigieren Sie zu ihrer PWA unter `http://localhost:3000` .  Wenn Ihr Dienstmitarbeiter ihre PWA-Benachrichtigung für Push-Benachrichtigungen aktiviert und versucht, Sie zu abonnieren, werden Sie von Microsoft Edge dazu aufgefordert, zulassen, dass Ihre PWA-Benachrichtigungen angezeigt werden.  Wählen Sie **zulassen**aus.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Dialogfeld ' Berechtigung ' zum Aktivieren von Benachrichtigungen" lightbox="./media/notification-permission.png":::
       Dialogfeld ' Berechtigung ' zum Aktivieren von Benachrichtigungen
    :::image-end:::
    
1.  Simulieren Sie eine serverseitige Push-Benachrichtigung.  Wenn Ihre PWA `http://localhost:3000` in Ihrem Browser geöffnet ist, wählen Sie aus, `F12` um die devtools zu öffnen.  Wählen Sie **Application**  >  **Service Worker**  >  **Push** aus, um eine Test-Push-Benachrichtigung an Ihre PWA zu senden.  
    
    :::row:::
       :::column span="":::
          Eine Push-Benachrichtigung sollte in der Nähe der Taskleiste angezeigt werden.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Pushen einer Benachrichtigung von devtools" lightbox="./media/devtools-push.png":::
             Pushen einer Benachrichtigung von devtools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Wenn Sie keine Popupbenachrichtigung \ (oder aktivieren \) auswählen, wird das System nach einigen Sekunden automatisch geschlossen und in Ihrem Windows-Wartungs Center in die Warteschlange eingereiht.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Benachrichtigungen im Windows-Wartungs Center" lightbox="./media/windows-action-center.png":::
             Benachrichtigungen im Windows-Wartungs Center :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## Nächste Schritte  

Die folgenden Schritte umfassen zusätzliche Aufgaben, mit denen Sie den Aufbau von PWAs in der realen Welt verstehen können.  

*   Verwalten und Speichern von Pushabonnement-Abonnements  
*   [Verschlüsseln][NPMWebPushEncrypt] von Nutzdaten  
*   Dynamisches Design  
*   Deep-Linking  
*   [Browserübergreifende Tests][BrowserStackTestEdgeBrowser]  
*   Implementieren von Validierungs-und Testmethoden wie [webhint][Webhint]  
    
## Weitere Informationen  

*   [Progressive Web-Apps auf MDN Web docs][MDNProgressiveWebApps]  
*   [Progressive Web-Apps auf Web. dev][WebDevProgressiveWebApps]  
*   [Hacker-Nachrichten Leser als Progressive Web-Apps][HackerNewsProgressiveWebApps] – vergleicht unterschiedliche Frameworks und Leistungsmuster für die Implementierung einer Stichprobe \ (Hacker Newsreader \) PWA.  
*   [Mythos Zerschlagung PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Eine progressive Roadmap für Ihre Progressive Web-App][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Offline Beiträge mit progressiven Web-Apps][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Wetten im Web][JoretegBlogBettingWeb]  
*   [Benennen von progressiven Web-Apps][Fberriman20170626NamingProgressiveWebApps]  
*   [Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Bereitstelleneiner Node.js-App für Azure mit Visual Studio-Code | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Erstellen eines Azure Free-Kontos | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web-Apps | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Web-Benachrichtigungen in Microsoft Edge | Windows-Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "﻿Kostenlose Tests für Microsoft Edge-Browser unter Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Eine progressive Roadmap für Ihre Progressive Web-App"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Mythos Zerschlagung PWAs – die neue Edge-Edition"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Express-Anwendungsgenerator | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Benennen von progressiven Web-Apps"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Hacker-Nachrichten Leser als Progressive Web-Apps"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Wetten im Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Progressive Web-Apps \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "Pushmanager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Verwenden von Service Mitarbeitern | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifest | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Offline Beiträge mit progressiven Web-Apps"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Senden von VAPID identifizierten webpush-Benachrichtigungen über den Push-Dienst von Mozilla | Mozilla-Dienste"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Push | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Verwendung-Web-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Progressive Web-Apps"  

[PwaBuilder]: https://www.pwabuilder.com "PWA-Generator"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Dienstmitarbeiter | PWA-Generator"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich-Demo | ServiceWorker Cookbook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 3)"  

[VapidkeysMain]: https://vapidkeys.com "Secure VAPID-Schlüssel Generator | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Progressive Web-Apps | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Progressive Verbesserung | Wikipedia"  
