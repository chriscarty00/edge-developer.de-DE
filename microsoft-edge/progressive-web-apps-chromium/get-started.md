---
description: In diesem Handbuch erhalten Sie eine Übersicht über die Grundlagen und Tools von PWA zum Erstellen von Progressive Web Apps (Chromium) unter Windows.
title: Erste Schritte mit Progressive Web Apps (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/16/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: progressive Web-Apps, PWA, Edge, Windows, PWABuilder, Webmanifest, Service worker, Push
ms.openlocfilehash: 3023c38790185ca6989f4a487928abc79b1d5a2c
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480195"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a>Erste Schritte mit Progressive Web Apps (Chromium)  

Progressive Web Apps \(PWAs\) sind Web-Apps, die [schrittweise erweitert werden.][WikiProgressiveEnhancement]  Die progressiven Verbesserungen umfassen app- like Features, z. B. Installation, Offlineunterstützung und Pushbenachrichtigungen.  Sie können ihre PWA auch für App-Stores packen.  Zu den möglichen App-Stores gehören der Microsoft Store, Google Play, der Mac App Store und vieles mehr.  Der Microsoft Store ist der kommerzielle App Store in Windows 10.  

Im folgenden Handbuch erhalten Sie eine Übersicht über die Grundlagen von PWA, indem Sie eine einfache Web-App erstellen und als PWA erweitern.  Das fertige Projekt funktioniert in modernen Browsern.  

> [!TIP]
> Sie können [PWABuilder verwenden,][PwaBuilder] um eine neue PWA zu erstellen, Ihre vorhandene PWA zu verbessern oder Ihre PWA für App-Stores zu packen.  

## <a name="prerequisites"></a>Voraussetzungen  

*   Verwenden [Visual Studio Code zum][VisualstudioCodeMain] Bearbeiten des PWA-Quellcodes.  
*   Verwenden [Node.js][NodejsMain] als lokaler Webserver.  
    
## <a name="create-a-basic-web-app"></a>Erstellen einer einfachen Web-App  

Führen Sie zum Erstellen einer leeren Web-App die Schritte unter [Node Express App Generator aus,][ExpressjsApplicationGenerator]und nennen Sie Ihre App `MySamplePwa` .  

Führen Sie in der Eingabeaufforderung die folgenden Befehle aus.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Die Befehle erstellen eine leere Web-App und installieren abhängigkeiten.  

Sie haben jetzt eine einfache, funktionale Web-App.  Führen Sie den folgenden Befehl aus, um Ihre Web-App zu starten.  

```shell
npm start
```  

Navigieren Sie nun, `http://localhost:3000` um Ihre neue Web-App zu sehen.  

:::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="Ausführen des neuen PWA auf localhost" lightbox="./media/visual-studio-nodejs-express-index.png":::
   Ausführen des neuen PWA auf localhost  
:::image-end:::  

## <a name="get-started-building-a-pwa"></a>Erste Schritte beim Erstellen einer PWA  

Da Sie nun über eine einfache Web-App verfügen, erweitern Sie sie als PWA, indem Sie die drei Anforderungen für PWAs hinzufügen.<!--[3 requirements for PWAs][ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]-->: [HTTPS](#step-1---use-https), [ein Web-App-Manifest](#step-2---create-a-web-app-manifest)und ein [Service Worker](#step-3---add-a-service-worker).  

### <a name="step-1---use-https"></a>Schritt 1 : Verwenden von HTTPS  

Wichtige Teile der PWA-Plattform, z. B. [Service Workers,][MDNServiceWorkerApi]erfordern die Verwendung von HTTPS.  Wenn Ihr PWA live geht, müssen Sie es in einer HTTPS-URL veröffentlichen.  

Zum Debuggen ermöglicht Microsoft Edge auch `http://localhost` die Verwendung der PWA-APIs.  

[Veröffentlichen Sie Ihre Web-App als Livewebsite,][VisualStudioNodejsTutorialPublishAzureAppService]stellen Sie jedoch sicher, dass Ihr Server für HTTPS konfiguriert ist.  Sie können beispielsweise ein kostenloses [Azure-Konto erstellen.][AzureCreateFreeAccount]  Hosten Sie Ihre Website im [Microsoft Azure App Service,][AzureWebApps] und sie wird standardmäßig über HTTPS bereitgestellt.  

Verwenden Sie die folgende Anleitung, `http://localhost` um Ihre PWA zu erstellen.  

### <a name="step-2---create-a-web-app-manifest"></a>Schritt 2 : Erstellen eines Web-App-Manifests  

Ein [Web App-Manifest][MDNWebAppManifest] ist eine JSON-Datei, die Metadaten zu Ihrer App enthält, z. B. Name, Beschreibung, Symbole und vieles mehr.  

So fügen Sie der Web-App ein App-Manifest hinzu:  

1.  Wählen Visual Studio Code die Option **Datei**öffnen Ordner  >  **aus,** und wählen Sie das `MySamplePwa` Verzeichnis aus, das Sie zuvor erstellt haben.  
1.  Wählen `Ctrl` + `N` Sie diese Option aus, um eine neue Datei zu erstellen, und fügen Sie den folgenden Codeausschnitt ein.  
    
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
    
1.  Speichern Sie die Datei unter `/MySamplePwa/public/manifest.json` .  
1.  Fügen Sie ein 512x512-App-Symbolbild mit dem Namen `icon512.png` zu `/MySamplePwa/public/images` hinzu.  Sie können das [Beispielbild zu](./media/progressive-web-app.png) Testzwecken verwenden.  
1.  Öffnen Visual Studio `/public/index.html` Code, und fügen Sie den folgenden Codeausschnitt innerhalb des Tags `<head>` hinzu.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a>Schritt 3 : Hinzufügen eines Dienstmitarbeiters  

Servicemitarbeiter sind die Schlüsseltechnologie für PWAs und ermöglichen Szenarien wie Offlineunterstützung, erweiterte Zwischenspeicherung und Ausführen von Hintergrundaufgaben, die zuvor auf systemeigene Apps beschränkt waren.  

Servicemitarbeiter sind Hintergrundaufgaben, die Netzwerkanforderungen von Ihrer Web-App abfangen.  Service workers attempt to complete tasks, even when your PWA is not running.  Zu den Aufgaben gehören die folgenden Aktionen.  

*   Serving requested resources from a cache  
*   Senden von Pushbenachrichtigungen  
*   Ausführen von Aufgaben zum Abrufen von Hintergrundinformationen  
*   Ungültige Symbole  
*   und mehr  
    
Dienstmitarbeiter werden in einer speziellen JavaScript-Datei definiert.  Weitere Informationen finden Sie unter [Using Service Workers][MDNUsingServiceWorkers] and Service Worker [API][MDNServiceWorkerApi].  

Verwenden Sie zum Erstellen eines Dienstmitarbeiters in Ihrem Projekt das **Rezept cache-first network** service worker von [PWA Builder][PwaBuilderServiceWorker].  

1.  Navigieren Sie [zu pwabuilder.com/serviceworker,][PwaBuilderServiceWorker]wählen Sie **den Cache-First-Netzwerkdienstmitarbeiter** aus, und wählen Sie die **Schaltfläche Herunterladen** aus.  Die heruntergeladene Datei enthält die folgenden Dateien:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  Kopieren Sie die heruntergeladenen Dateien `public` in den Ordner in Ihrem Web-App-Projekt.  
1.  Öffnen Visual Studio Code, und fügen Sie den `/public/index.html` folgenden Codeausschnitt innerhalb des Tags `<head>` hinzu.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Ihre Web-App verfügt jetzt über einen Dienstmitarbeiter, der die Cache-First-Strategie verwendet.  Der neue Dienstmitarbeiter ruft ressourcen zuerst aus dem Cache und nur bei Bedarf aus dem Netzwerk ab.  Zwischengespeicherte Ressourcen umfassen Bilder, JavaScript, CSS und HTML.

Verwenden Sie die folgenden Schritte, um zu bestätigen, dass Ihr Dienstmitarbeiter ausgeführt wird.  

1.  Navigieren Sie zu Ihrer Web-App mithilfe `http://localhost:3000` von .  Wenn Ihre Web-App nicht verfügbar ist, führen Sie den folgenden Befehl aus.   
    
    ```shell
    npm start
    ```
    
1.  Wählen Sie in Microsoft Edge aus, `F12` um die Microsoft Edge DevTools zu öffnen.  Wählen **Sie Anwendung**und dann Service Workers **aus,** um die Servicemitarbeiter anzeigen zu können.  Wenn der Dienstmitarbeiter nicht angezeigt wird, aktualisieren Sie die Seite.  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Übersicht über Microsoft Edge DevTools Service Worker" lightbox="./media/devtools-sw-overview.png":::
       Übersicht über Microsoft Edge DevTools Service Worker  
    :::image-end:::  
    
1.  Zeigen Sie den Dienstarbeitscache an, indem Sie **Cachespeicher erweitern,** und wählen Sie **pwabuilder-precache aus.**  Alle vom Dienstmitarbeiter zwischengespeicherten Ressourcen sollten angezeigt werden.  Zu den ressourcen, die vom Dienstmitarbeiter zwischengespeichert werden, gehören das App-Symbol, das App-Manifest, css und die JavaScript-Dateien.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Dienstarbeitscache in Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       Dienstarbeitscache in Microsoft Edge DevTools \(F12\)  
    :::image-end:::  
    
1.  Testen Sie PWA als Offline-App.  Wählen Sie in Microsoft Edge DevTools \( \) Netzwerk aus, und ändern Sie dann `F12` den **Onlinestatus** in **Offline**. ****  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Festlegen des Offlinemodus der App in Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       Festlegen des Offlinemodus der App in Microsoft Edge DevTools  
    :::image-end:::  
    
1.  Aktualisieren Sie Ihre App, und sie sollte den Offlinemechanismus für die Verwendung der Ressourcen Ihrer App aus dem Cache anzeigen.  
    
    :::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="Offline ausgeführter PWA" lightbox="./media/visual-studio-nodejs-express-index.png":::
       Offline ausgeführter PWA  
    :::image-end:::  
    
## <a name="add-push-notifications-to-your-pwa"></a>Hinzufügen von Pushbenachrichtigungen zu Ihrem PWA  

Sie können PWAs erstellen, die Pushbenachrichtigungen unterstützen, indem Sie die folgenden Aufgaben ausführen.  

1.  Abonnieren eines Messagingdiensts mithilfe der [Push-API][MDNPushApi]  
1.  Anzeigen einer Popupnachricht beim Empfangen einer Nachricht vom Dienst mithilfe der [Benachrichtigungs-API][MDNNotificationsApi]  
    
Genau wie bei Service Workers sind die Pushbenachrichtigungs-APIs standardbasierte APIs.  Die Pushbenachrichtigungs-APIs funktionieren browserübergreifend, daher sollte Ihr Code überall funktionieren, wo PWAs unterstützt werden.  Weitere Informationen zum Senden von Pushnachrichten an verschiedene Browser auf Ihrem Server finden Sie unter [Web-Push][NPMWebPush].  

Die folgenden Schritte wurden aus dem Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] von Mozilla angepasst, das eine Reihe anderer nützlicher Web-Push- und Servicearbeitsrezepte bietet.  

### <a name="step-1---generate-vapid-keys"></a>Schritt 1 : Generieren von VAPID-Schlüsseln  

Pushbenachrichtigungen erfordern VAPID \(Voluntary Application Server Identification\)-Schlüssel, um Pushnachrichten an den PWA-Client zu senden.  Es sind mehrere VAPID-Schlüsselgeneratoren online verfügbar \(z. B. [vapidkeys.com][VapidkeysMain]\).  Nach der Generierung sollten Sie ein JSON-Objekt mit einem öffentlichen und einem privaten Schlüssel erhalten.  Speichern Sie die Schlüssel für spätere Schritte im folgenden Lernprogramm.  Weitere Informationen zu VAPID und WebPush finden Sie unter Senden von VAPID identifizierten [WebPush-Benachrichtigungen mithilfe des Mozilla-Pushdiensts.][MozillaServicesSendingVapidWebPushNotificationsPush]  

### <a name="step-2---subscribe-to-push-notifications"></a>Schritt 2 – Abonnieren von Pushbenachrichtigungen  

Servicemitarbeiter verarbeiten Pushereignisse und Popupbenachrichtigungsinteraktionen in Ihrem PWA.  Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind, um die PWA auf Server-Pushbenachrichtigungen zu abonnieren.  

*   Ihr PWA ist installiert, aktiv und registriert  
*   Ihr Code zum Abschließen der Abonnementaufgabe befindet sich im Hauptbenutzeroberflächenthread des PWA  
*   Sie verfügen über Netzwerkkonnektivität  
    
Bevor ein neues Pushabonnement erstellt wird, überprüft Microsoft Edge, ob der Benutzer die PWA-Berechtigung zum Empfangen von Benachrichtigungen erteilt hat.  Andern falls nicht, wird der Benutzer vom Browser zur Berechtigung aufgefordert.  Wenn die Berechtigung verweigert wird, wird von der Anforderung ein `registration.pushManager.subscribe` `DOMException` ausgelöst, der verarbeitet werden muss.  Weitere Informationen zur Berechtigungsverwaltung finden Sie unter [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

Fügen Sie `pwabuilder-sw-register.js` in Ihrer Datei den folgenden Codeausschnitt an.  

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

Weitere Informationen finden Sie unter [PushManager][MDNPushManager] und [Web-Push.][NPMWebPushUsage]  

### <a name="step-3---listen-for-push-notifications"></a>Schritt 3 – Abhören auf Pushbenachrichtigungen  

Nachdem ein Abonnement in Ihrem PWA erstellt wurde, fügen Sie dem Dienstmitarbeiter Handler hinzu, um auf Pushereignisse zu reagieren.  Das Pushereignis wird vom Server gesendet, um Popupbenachrichtigungen anzuzeigen.  Popupbenachrichtigungen zeigen Daten für eine empfangene Nachricht an.  Zum Ausführen der folgenden Aufgaben müssen Sie einen Handler `click` hinzufügen.  

*   Schließen der Popupbenachrichtigung  
*   Öffnen, Fokussieren oder Öffnen und Fokussieren von geöffneten Fenstern  
*   Öffnen und Fokussieren eines neuen Fensters zum Anzeigen einer PWA-Clientseite  
    
Fügen Sie `pwabuilder-sw.js` in Ihrer Datei die folgenden Handler hinzu.  

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

### <a name="step-4---try-it-out"></a>Schritt 4 – Ausprobieren  

Führen Sie die folgenden Schritte aus, um Pushbenachrichtigungen für Ihre PWA zu testen.  

1.  Navigieren Sie zu Ihrem PWA unter `http://localhost:3000` .  Wenn Ihr Servicemitarbeiter aktiviert wird und versucht, Ihre PWA für Pushbenachrichtigungen zu abonnieren, fordert Microsoft Edge Sie auf, Ihrem PWA das Anzeigen von Benachrichtigungen zu erlauben.  Wählen Sie **Zulassen**aus.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Berechtigungsdialogfeld zum Aktivieren von Benachrichtigungen" lightbox="./media/notification-permission.png":::
       Berechtigungsdialogfeld zum Aktivieren von Benachrichtigungen  
    :::image-end:::  
    
1.  Simulieren sie eine serverseitige Pushbenachrichtigung.  Wenn Ihr PWA `http://localhost:3000` in Ihrem Browser geöffnet ist, wählen Sie `F12` aus, um die DevTools zu öffnen.  Wählen **Sie Application**Service  >  **Worker**Push  >  **aus,** um eine Test-Pushbenachrichtigung an Ihre PWA zu senden.  
    
    :::row:::
       :::column span="":::
          Eine Pushbenachrichtigung sollte in der Nähe der Taskleiste angezeigt werden.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Pushen einer Benachrichtigung von DevTools" lightbox="./media/devtools-push.png":::
             Pushen einer Benachrichtigung von DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Wenn Sie keine Popupbenachrichtigung \(oder aktivieren\) auswählen, wird sie nach einigen Sekunden automatisch vom System geschlossen und im Windows Action Center in eine Warteschlange eingereiht.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Benachrichtigungen im Windows Action Center" lightbox="./media/windows-action-center.png":::
             Benachrichtigungen im Windows Action Center  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a>Nächste Schritte  

Die folgenden Schritte umfassen zusätzliche Aufgaben, mit deren Hilfe Sie das Erstellen von echten PWAs verstehen können.  

*   Verwalten und Speichern von Pushabonnements  
*   [Verschlüsseln von][NPMWebPushEncrypt] Nutzlastdaten  
*   Dynamisches Design  
*   Tiefenverknüpfung  
*   [Browserübergreifende Tests][BrowserStackTestEdgeBrowser]  
*   Implementieren von Validierungs- und Testmethoden wie [Webhint][Webhint]  
    
## <a name="see-also"></a>Weitere Informationen  

*   [Progressive Web Apps in MDN-Web-Dokumenten][MDNProgressiveWebApps]  
*   [Progressive Web Apps auf web.dev][WebDevProgressiveWebApps]  
*   [Hacker News-Leser als Progressive Web Apps][HackerNewsProgressiveWebApps] – Vergleicht verschiedene Frameworks und Leistungsmuster für die Implementierung eines Beispiels \(Hacker News Reader\) PWA.  
*   [Legendenbusting PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Eine progressive Roadmap für Ihre Progressive Web App][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Offline-POSTs mit progressiven Web-Apps][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Wetten im Web][JoretegBlogBettingWeb]  
*   [Benennung progressiver Web-Apps][Fberriman20170626NamingProgressiveWebApps]  
*   [Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  

<!-- links -->  

<!--[ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]: /archive/microsoft-edge/legacy/developer/progressive-web-apps/index#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Bereitstellen einer Node.js in Azure mit Visual Studio Code | Microsoft Docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Erstellen von kostenlosen Azure-| Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web Apps | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Webbenachrichtigungen in Microsoft Edge | Windows-Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Kostenlose Microsoft Edge-Browsertests unter Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Eine progressive Roadmap für Ihre Progressive Web App"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Legendenbusting PWAs – Die neue Edge Edition"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Expressanwendungsgenerator | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Benennung progressiver Web-Apps"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Hacker News-Leser als Progressive Web Apps"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Wetten im Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API-| MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Progressive Web apps \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API-| MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager-| MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Dienstarbeits-API-| MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Verwenden von Service Workers | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App Manifest | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Offline-POSTs mit progressiven Web-Apps"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Senden von VON VAPID identifizierten WebPush-Benachrichtigungen über mozillas Pushdienst-| Mozilla Services"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Push-| npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) – Web-Push-| NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Verwendung – Web-Push-| NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Progressive Web Apps"  

[PwaBuilder]: https://www.pwabuilder.com "PWA Builder"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Service Worker | PWA Builder"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | ServiceWorker Cookbook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 3)"  

[VapidkeysMain]: https://vapidkeys.com "Secure VAPID Key Generator | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Progressive Web Apps | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Progressive | Wikipedia"  
