---
description: Dieser Leitfaden enthält eine Übersicht über die Grundlagen und Tools von PWA für das Erstellen von progressiven Web-Apps unter Windows.
title: Erste Schritte mit Progressive Web-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, PWABuilder, Web-Manifest, Service Worker, Push
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a76399616ab7645b82242b94dd4757b73b37f60
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233572"
---
# Erste Schritte mit Progressive Web-Apps  

Progressive Web-Apps \(PWAs \) sind einfach Webanwendungen, die mit systemeigenen App-ähnlichen Features auf unterstützenden Plattformen und Browser Modulen, wie Start-from-Homescreen-Installation, Offline-Unterstützung und Push-Benachrichtigungen, [zunehmend verbessert][WikiProgressiveEnhancement] werden.  Unter Windows 10 mit dem Microsoft Edge \(EdgeHTML \)-Modul genießen PWAs den zusätzlichen Vorteil, dass Sie unabhängig vom Browserfenster als [universelle Windows-Plattform][WindowsUwpGetStartedWhat] -apps ausgeführt werden.  

Dieser Leitfaden bietet Ihnen einen Überblick über die Grundlagen von PWA, indem Sie eine einfache `localhost` Web-App als PWA mit Microsoft Visual Studio und einigen PWA Builder-Dienstprogrammen erstellen.  Das fertige Produkt funktioniert ähnlich in jedem Browser, der PWAs unterstützt.  

> [!TIP]
> Wenn Sie eine vorhandene Website schnell in eine PWA-Datei konvertieren und für Windows 10 und andere APP-Plattformen verpacken möchten, überprüfen Sie den [PWA-Generator][PwaBuilder].  

## Voraussetzungen  

Sie können PWAs mit jeder Webentwicklungs-IDE erstellen.  Im folgenden finden Sie nur die Voraussetzungen für diesen Leitfaden, der Sie durch die Unterstützung von PWA-Tools im Windows Developer-Ökosystem führt.  

*   Laden Sie die \(Free \) [Visual Studio Community 2017][VisualStudioDownloads].  Sie können auch die Editionen Professional, Enterprise oder [Preview][VisualStudioPreview] verwenden.  Wählen Sie im Visual Studio-Installationsprogramm die folgenden Arbeitsauslastungen aus.  
    
    *   **Entwicklung der universellen Windows-Plattform**  
    *   **Node.js Entwicklung**  

## Einrichten einer einfachen Web-App  

Verwenden Sie aus Gründen der Einfachheit die Visual Studio [Node.js-und Express-App][VisualStudioNodeJsTutorial] -Vorlage, um `localhost` Web-App zu erstellen, die eine `index.html` Seite bedient.  Stellen Sie sich dies als Platzhalter für die überzeugend umfassende Web-App vor, die Sie als PWA entwickeln.  

1.  Starten Sie Visual Studio, und starten Sie ein neues Projekt.  
    *   **Datei**  >  **Neu**  >  **Project...**  
    *   `Ctrl`+`Shift`+`N`  
1.  Wählen Sie unter **JavaScript**die Option **Basic Node.js Express 4-Anwendung**aus.  Geben Sie den Namen und den Speicherort ein, und wählen Sie **OK**aus.  
    
    ![Auswählen der Projektvorlage "Node.js Express 4" in Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  Nachdem das neue Projekt geladen wurde, wählen Sie **Build** \( `Ctrl` + `Shift` + `B` \) aus, und starten Sie das **Debuggen** `F5` .  Überprüfen Sie, ob die `index.html` Datei beim Durchsuchen geladen wird `http://localhost:1337` .  
    
    ![Ausführen der neuen Website auf localhost][ImageVsNodejsExpressIndex]  

## Umwandeln Ihrer APP in eine PWA  

Jetzt ist es an der Zeit, die Grund [Legenden PWA-Anforderungen][PwaEdgehtmlIndexRequirements] für Ihre Web-App zu *vernetzen: ein Web App-Manifest*, *https* und *Dienstmitarbeiter*.  

### Web App-Manifest  

Bei einem [Web App-Manifest][MDNWebAppManifest] handelt es sich um eine JSON-Metadatendatei, die Ihre APP beschreibt, einschließlich Name, Autor, Eintrags Seiten-URL und einem oder mehreren Symbolen.  Da es sich um ein [standardbasiertes Schema][W3cWebAppManifest]handelt, müssen Sie nur ein einzelnes Web App-Manifest für die PWA-Datei bereitstellen, die Sie auf einer beliebigen Plattform-, Betriebssystem-und Gerätekombination installieren, die PWAs unterstützt.  Im Windows-Ökosystem signalisiert Ihr Web App-Manifest dem Bing Web-Indexer, dass Ihre PWA ein Kandidat für die automatische Inklusion in den [Microsoft Store][PwaEdgehtmlMicrosoftStore]ist, wo Sie fast 700 Millionen aktive monatliche Benutzer als Windows 10-App erreichen kann.  

Wenn es sich um eine vorhandene Live Website handelt, können Sie ein Web App-Manifest mit dem [PWA-Generator][PwaBuilder]generieren.  Da es sich immer noch um ein unveröffentlichtes Projekt handelt, kopieren Sie ein Beispiel Manifest.  

1.  Klicken Sie im Visual Studio- *Projektmappen-Explorer*mit der rechten Maustaste auf den *öffentlichen* Ordner, und wählen Sie neue Datei **Hinzufügen**  >  **...** aus, wobei Sie `manifest.json` den Namen des Elements angeben.  
1.  Kopieren Sie `manifest.json` den folgenden Code in der Datei.  

    ```json
    {
        "dir": "ltr",
        "lang": "en-us",
        "name": "My Sample PWA",
        "scope": "/",
        "display": "browser",
        "start_url": "https://PLACEHOLDER-FOR-PWA-URL",
        "short_name": "SamplePWA",
        "theme_color": "transparent",
        "description": "A sample PWA for testing purposes",
        "orientation": "any",
        "background_color": "transparent",
        "related_applications": [],
        "prefer_related_applications": false,
        "icons": []
    }
    ```  
    
    In einer echten PWA besteht der nächste Schritt darin, *Namen*, *start_url*, *SHORT_NAME*, *Beschreibung*und *Symbole* anzupassen \(im nächsten Schritt werden die Symbole behandelt).  
    
    Weitere Informationen zu den verschiedenen Mitglieds Werten und zugehörigen Zwecken finden Sie im [Web App-Manifest-][MDNWebAppManifest] Referenz.  
    
1.  Als nächstes füllen Sie das leere `icons` Array mit tatsächlichen Bildpfaden mithilfe des PWA Builder App-Bild Generators aus.  
    
    1.  Laden Sie dieses [Beispiel 512x512 PWA-Bild][ImagePwa]mithilfe eines Webbrowsers herunter.  
    1.  Wechseln Sie zum [Bild Generator][PwaBuilderAppImageGenerator]der PWA Builder-APP, und wählen Sie das Bild aus, das `pwa.png` Sie gerade als **Eingabebild** gespeichert haben, und wählen Sie dann die Schaltfläche **herunterladen** aus.  
    1.  **Öffnen** und **extrahieren** Sie die ZIP-Datei.  
    1.  Klicken Sie im Visual Studio-Projektmappen-Explorer mit der rechten Maustaste auf den `public` Ordner, und öffnen Sie den **Ordner im Datei-Explorer**.  Erstellen Sie einen **neuen Ordner** mit dem Namen `images` .  
    1.  Kopieren Sie alle Plattformordner \( `android` ,, usw `chrome` `windows10` . \) aus dem extrahierten zip in den `images` Ordner, und schließen Sie das Fenster "Datei-Explorer".  Fügen Sie die Ordner Ihrem Visual Studio-Projekt hinzu (Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf `images` Ordner, und wählen Sie vorhandenen Ordner **Hinzufügen**  >  **...** für jeden der Ordner \) aus.  
    1.  Öffnen Sie die Datei aus dem extrahierten ZIP-Datei (mit Visual Studio oder einem beliebigen Editor) `icons.json` , und kopieren `"icons": [...]` Sie das Array in die `manifest.json` Datei Ihres Projekts.  

1.  Nun müssen Sie Ihr Web App-Manifest mit Ihrer APP verknüpfen.  Öffnen `layout.pug` Sie die Datei \(in `views` Ordner \) für die Bearbeitung, und fügen Sie diese Zeile direkt hinter dem Stylesheet-Link hinzu.  \(Es handelt sich einfach um die Kurzform für den Knoten [Mops][PugAttributes] für `<link rel='manifest' href='/manifest.json'>` \).  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
Mit all dem, was an Ort und Stelle ist, dient Ihre Web-App nun einer Manifesten und Homescreen-fähigen APP-Ikone!  Führen Sie Ihre APP aus `F5` , und laden Sie das Manifest ein.  

![Web App-Manifest wird von localhost geladen][ImageVsNodejsExpressManifest]  

Und eines ihrer Symbole.  

![Square71x71Logo-App-Logo wird von localhost geladen][ImageVsNodejsExpressIcon]  

Wenn Sie die APP Live veröffentlichen \(mit einem tatsächlichen `start_url` \), wird Sie von der Bing-Suchmaschine nun als Kandidat für [das automatische Verpacken und die Übermittlung an den Microsoft Store][PwaEdgehtmlMicrosoftStore] als installierbare Windows 10-App bezeichnet.  Stellen Sie sicher, dass Ihre manifest.json [-Datei die Qualitäts Signale für Progressive Web-Apps][WindowsBlogsPwaEdge] enthält, für die Bing Scans einschließlich der folgenden Elemente umfasst.   

*   `name`  
*   `description`  
*   Mindestens ein Symbol 512px quadratisch oder größer \(um sicherzustellen, dass eine Bildquelle mit einer genügenden Auflösung für die automatische Generierung des Begrüßungsbildschirms Ihrer APP, des Store-Eintrags, der Kachel Abbildung usw. angezeigt wird).  

Darüber hinaus können Sie [https](#https), [Servicemitarbeiter](#service-workers)und die [Microsoft Store-Richtlinien][LegalWindowsAgrementsMicrosoftStorePolicies]einhalten.  

### HTTPS  

[Dienstmitarbeiter][MDNServiceWorkerApi] und andere wichtige PWA-Technologien, die mit Servicemitarbeitern arbeiten, wie etwa die [Cache][MDNCache]-, [Push][MDNPushApi]-und [Hintergrund-Synchronisierungs][MDNSyncManager] -APIs, funktionieren nur über sichere Verbindungen, was [https][WikiHttps] für Live-Websites oder `localhost` für Debugging-Zwecke bedeutet.  

Wenn Sie [diese Web-App als Live Website veröffentlichen][VisualStudioNodejsTutorialPublishAzureAppService] \(beispielsweisedurch Einrichten eines [Azure Free-Kontos][AzureCreateFreeAccount]\), müssen Sie sicherstellen, dass Ihr Server für HTTPS konfiguriert ist.  Wenn Sie den [Microsoft Azure-App-Dienst][AzureWebApps] zum Hosten Ihrer Website verwenden, wird diese standardmäßig über HTTPS bereitgestellt.  

Für dieses Handbuch verwenden Sie weiterhin die Verwendung `http://localhost` als Platzhalter für eine Live-Website, die für Sie bereitgestellt wird `https://` .  

### Service Workers  

Service Mitarbeiter sind die Schlüsseltechnologien hinter PWAs. Dienstmitarbeiter fungieren als Proxy zwischen PWA und dem Netzwerk, damit Ihre Website als installierte systemeigene App fungieren kann, die Offlineszenarien bedient, auf Server-Push-Benachrichtigungen reagiert und Hintergrundaufgaben ausführt.  Service Mitarbeiter erschließen auch neue Leistungs Strategien.  Sie müssen keine vollständige Web-App implementieren, um den Service Worker-Cache für optimierte Seiten Ladeleistung für Ihre Website zu verwenden.  

Dienstmitarbeiter sind ereignisgesteuerte Hintergrund Threads, die von JavaScript-Dateien ausgeführt werden, die zusammen mit den regulären Skripts, die Ihre Web-App antreiben, bereitgestellt werden.  Da Dienstmitarbeiter nicht auf dem Hauptbenutzeroberflächen Thread ausgeführt werden, verfügen Dienstmitarbeiter nicht über DOM-Zugriff, obwohl der [UI-Thread][MDNWorkerPrototypePostMessage] und ein [Worker-Thread][MDNDedicatedWorkerGlobalScopePostMessage] mithilfe von `postMessage()` und `onmessage` Ereignishandlern kommunizieren können.  

Sie ordnen eine Dienstmitarbeiter Ihrer APP zu, indem Sie Sie auf dem URL-Ursprung ihrer Website registrieren \(oder einem angegebenen Pfad darin \).  Nach der Registrierung wird die Service Worker-Datei dann auf dem Benutzer Computer heruntergeladen, installiert und aktiviert.  Weitere Informationen finden Sie im MDN Web docs-Handbuch mit einer umfassenden Anleitung zur [Verwendung von Servicemitarbeitern][MDNUsingServiceWorkers] und einer detaillierten [Service Worker-API][MDNServiceWorkerApi] -Referenz.  

Verwenden Sie für dieses Lernprogramm das Worker-Skript für Offline Seiten Dienst in [PWA Builder][PwaBuilderServiceWorker].  Beginnen Sie, indem Sie das Skript mit mehr Funktionalität entsprechend Ihren Leistungsanforderungen, Netzwerkbandbreite usw. anpassen.  Überprüfen Sie das von Mozilla bereitgestellte [Service Worker Cookbook][ServiceWorkerCookbook]  für eine Reihe nützlicher Ideen für die Zwischenspeicherung von Dienstmitarbeiter.  

1.  Öffnen Sie [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] den \(Standard \) **Offline Page** Service Worker, und klicken Sie auf die Schaltfläche **Dienstmitarbeiter herunterladen** .  
1.  Öffnen Sie den Ordner "Download", und kopieren Sie die beiden folgenden Dateien:  

    *   ServiceWorker1\pwabuilder-sw-register.js  
    *   ServiceWorker1\pwabuilder-sw.js  
    
    Speichern Sie die Dateien im `public` Ordner Ihres Visual Studio Web App-Projekts.  \(In Visual Studio können Sie den `Ctrl` + `O` Datei-Explorer in Ihrem Projekt öffnen und zu dem `public` Ordner navigieren \).  
    
    Öffnen Sie im Projektmappen-Explorer die `public/pwabuilder-sw.js` Datei, und ändern Sie den Wert von in `offlineFallbackPage` `offline.html` .  
    
    ```javascript
    const offlineFallbackPage = "offline.html";
    ```
    
    Es lohnt sich, den Code in diesen beiden Dateien zu überprüfen, um zu erfahren, wie ein Dienstmitarbeiter registriert wird, der eine bestimmte Seite zwischenspeichert \( `offline.html` \), und wenn ein Netzwerkabruf fehlschlägt.  Als Nächstes erstellen Sie eine einfache `offline.html` Seite als Platzhalter für die Offlinefunktionen Ihrer APP.  
    
1.  Öffnen Sie im Projektmappen-Explorer die `views/layout.pug` Datei, und fügen Sie die folgende Zeile unter Ihren Link-Tags hinzu.  
    
    ```html
    script(src='/pwabuilder-sw-register.js' type='module')
    ```  
    
    Ihre Website lädt und führt Ihr Registrierungsskript für Dienstmitarbeiter aus.  
    
1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf den `public` Ordner, und wählen Sie ****  >  **neue Datei**hinzufügen aus.  Benennen Sie `offline.html` die Datei, und fügen Sie einen `<title>` und einige Textinhalte hinzu, beispielsweise den folgenden Code.  
    
    ```html
    <!DOCTYPE html>
    
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Offline mode</title>
    </head>
    <body>
        You are now offline.
    </body>
    </html>
    ```  
    
    An diesem Punkt sollte Ihr `public` Ordner über drei neue Dateien verfügen.  
    
    ![Dateien, die dem öffentlichen Ordner der Projektmappe hinzugefügt wurden][ImageVsNodejsExpressPublic]  
    
1.  Öffnen Sie im Projektmappen-Explorer die `routes\index.js` Datei, und fügen Sie den folgenden Code direkt vor dem letzten Befehl \( `module.exports = router;` \) hinzu.  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    Dadurch wird Ihre APP angewiesen, die `offline.html` Datei zu bedienen \(wenn Ihr Dienstmitarbeiter Sie für den Offlinecache abruft \).  
    
1.  Testen Sie Ihre PWA!  Erstellen Sie \( `Ctrl` + `Shift` + `B` \), und führen `F5` Sie \(\) Ihre Web-App aus, um Microsoft Edge zu starten und Ihre Seite zu öffnen `localhost` .  Führen Sie dann die folgenden Schritte aus.  
    
    1.  Öffnen Sie die Edge **** `Ctrl` + `Shift` + `J` -devtools-Konsole, und überprüfen Sie, ob der Dienstmitarbeiter registriert wurde.  
    1.  Erweitern Sie im **Debugger** -Panel das **Service Worker** -Steuerelement, und klicken Sie auf ihren Ursprung.  Überprüfen Sie in der **Übersicht der Dienstmitarbeiter**, ob Ihr Dienstmitarbeiter aktiviert ist und ausgeführt wird.  
        
        ![Übersicht über den Edge devtools Service Worker][ImageDevtoolsSwOverview]  
        
    1.  Erweitern Sie das **Cache** -Steuerelement, und überprüfen Sie, ob die `offline.html` Seite zwischengespeichert ist.  
        
        ![Edge devtools Service Worker-Cache][ImageDevtoolsSwCache]  
        
1.  Zeit, ihre PWA als offline-app zu testen!  Beenden Sie in Visual Studio das **Debuggen** \( `Shift` + `F5` \) Ihre Web-App, und öffnen Sie dann Microsoft Edge \(oder aktualisieren \) an die localhost-Adresse Ihrer Website.  Es sollte nun die `offline.html` Seite laden (Dank ihres Service-Worker-und Offline-Caches \)!  
    
    ![offline.html http://localhost:1337 in Microsoft Edge geladen][ImageOfflineHtml]  

## Hinzufügen von Push-Benachrichtigungen  

Machen Sie Ihre PWA-App-ähnlicher, indem Sie clientseitige Unterstützung für Push-Benachrichtigungen hinzufügen, indem Sie die [Push-API][MDNPushApi] verwenden, um einen Messagingdienst zu abonnieren, und die [Benachrichtigungs-API][MDNNotificationsApi] , um beim Empfang einer Nachricht eine Popupnachricht anzuzeigen.  Wie bei Service Mitarbeitern sind dies standardbasierte APIs, die browserübergreifend funktionieren, sodass Sie den Code nur einmal schreiben müssen, damit er überall funktioniert, PWAs unterstützt werden.  Verwenden Sie auf der Serverseite die Open-Source-Bibliothek [Web-Push][NPMWebPush] , um die Unterschiede bei der Bereitstellung von Push-Nachrichten in verschiedenen Browsern zu behandeln.  

Im folgenden wird das Push Rich-Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] von Mozilla angepasst, das für eine Reihe anderer nützlicher Web-Push-und Service-Worker-Rezepte interessant ist.  

### Schritt 1: Installieren der NPM Web-Push-Bibliothek  

Klicken Sie im Visual Studio-Projektmappen-Explorer mit der rechten Maustaste auf das Projekt, und **Öffnen Sie Node.js interaktives Fenster**.  Geben Sie den folgenden Code ein.  

```javascript
.npm install web-push
```  

Dadurch wird die [Web-Push-][NPMWebPush] Bibliothek installiert.  Öffnen Sie dann Ihre `index.js` Datei, und fügen Sie die folgende Zeile oben in der Datei nach den anderen Anforderungs Anweisungen hinzu.  

```javascript
var webpush = require('web-push');
```  

### Schritt 2: Generieren von VAPID-Schlüsseln für Ihren Server  

Als nächstes müssen Sie VAPID \(freiwillige Application Server Identification \)-Schlüssel für Ihren Server generieren, um Push-Nachrichten an den PWA-Client zu senden.  Sie müssen dies nur einmal tun \(das heißt, Ihr Server erfordert nur ein einzelnes Paar VAPID-Schlüssel \).  Geben Sie im interaktiven Node.js Fenster den folgenden Code ein.  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

Die Ausgabe sollte zu einem JSON-Objekt führen, das einen öffentlichen und einen privaten Schlüssel enthält, die Sie in Ihre Serverlogik kopieren.  

`index.js`Fügen Sie in der Datei unmittelbar vor der letzten \( `module.exports = router` \)-Zeile den folgenden Code hinzu.  

```javascript
const vapidKeys = {
    publicKey: '',
    privateKey: ''
};

webpush.setVapidDetails(
    'mailto:pwa@example.com',
    vapidKeys.publicKey,
    vapidKeys.privateKey
);
```  

Kopieren `publicKey` Sie die `privateKey` soeben generierten und-Werte.  Gerne können `mailto` Sie auch die Adresse anpassen \(obwohl dies nicht erforderlich ist, um dieses Beispiel auszuführen \).  

Der [Mozilla Services Engineering-Blog][MozillaServicesSendingVapidWebPushNotificationsPush] hat einen netten Explainer auf VAPID und webpush, wenn Sie an den Details darüber interessiert sind, wie es hinter den Kulissen funktioniert.  

### Schritt 3 – behandeln von Push-bezogenen Server Anforderungen  

Richten Sie nun Routen für die Verarbeitung von Push-bezogenen Anforderungen vom PWA-Client ein, einschließlich der Bereitstellung des öffentlichen VAPID-Schlüssels und der Registrierung des Clients für den Empfang von Pushs.  

In einem realen Szenario stammt eine Push-Benachrichtigung wahrscheinlich von einem Ereignis in ihrer Serverlogik.  Um die Dinge hier zu vereinfachen, müssen Sie der PWA-Startseite eine Schaltfläche " **Push-Benachrichtigung** " hinzufügen, um Pushs von unserem Server zu generieren, und einen `/sendNotification` Endpunkt \(Server Route \) für die Verarbeitung dieser Anforderungen.  

`index.js`Fügen Sie in Ihrer Datei unmittelbar nach dem VAPID-Initialisierungscode, den Sie in [Schritt 2] [#Step-2---generieren-VAPID-Schlüssel-für-Server] hinzugefügt haben, die folgenden Routen an.  

```javascript
router.get('/vapidPublicKey', function (req, res) {
    res.send(vapidKeys.publicKey);
});

router.post('/register', function (req, res) {
    // A real world application stores the subscription info.
    res.sendStatus(201);
});

router.post('/sendNotification', function (req, res) {
    const subscription = req.body.subscription;
    const payload = 'payload';
    const options = null;
    
    webpush.sendNotification(subscription, payload, options)
        .then(function () {
            res.sendStatus(201);
        })
        .catch(function (error) {
            res.sendStatus(500);
            console.log(error);
        });
});
```  

Mit dem serverseitigen Code in Kraft, in Push-Benachrichtigungen auf dem PWA-Client.  

### Schritt 4 – Abonnieren von Push-Benachrichtigungen  

Als Teil ihrer Rolle als PWA-Netzwerk Proxys behandeln Dienstmitarbeiter Push-Ereignisse und Popup Benachrichtigungs Interaktionen.  Wie bei der ersten Einrichtung von \(oder der Registrierung \) eines Dienst Mitarbeiters, erfolgt die Anmeldung der PWA to Server-Push-Benachrichtigungen im Hauptbenutzeroberflächen Thread der PWA und erfordert eine Netzwerkverbindung.  Für das Abonnieren von Push-Benachrichtigungen ist eine Active Service Worker-Registrierung erforderlich, daher müssen Sie zuerst überprüfen, ob Ihr Dienstmitarbeiter installiert und aktiv ist, bevor Sie versuchen, ihn für Push-Benachrichtigungen zu abonnieren.  

Bevor ein neues Pushabonnement erstellt wird, überprüfen Sie, ob der Benutzer die PWA-Berechtigung zum Empfangen von Benachrichtigungen gewährt hat.  Wenn dies nicht der Fall ist, wird der Benutzer vom Browser zur Genehmigung aufgefordert.  Wenn die Berechtigung verweigert wird, wird die Anforderung `registration.pushManager.subscribe` ausgelöst `DOMException` , sodass Sie Sie behandeln müssen.  Weitere Informationen zur Berechtigungsverwaltung finden Sie unter [Push-Benachrichtigungen in Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

Fügen Sie in der `pwabuilder-sw-register.js` Datei den folgenden Code ein.  

```javascript
// Subscribe this PWA to push notifications from the server
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(async function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                // Otherwise subscribe with the server public key
                const response = await fetch('./vapidPublicKey');
                const vapidPublicKey = await response.text();
                const convertedVapidKey = urlBase64ToUint8Array(vapidPublicKey);
                
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: convertedVapidKey
                });
            });
    }).then(function (subscription) {
        // Send the subscription details to the server
        fetch('./register', {
            method: 'post',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({
                subscription: subscription
            }),
        });
        
        // Create a button to mimic server pushes for testing purposes
        var button = document.createElement('input');
        button.type = 'button';
        button.id = 'notify';
        button.value = 'Send Notification';
        document.body.appendChild(button);
        document.getElementById('notify').addEventListener('click', function () {
            fetch('./sendNotification', {
                method: 'post',
                headers: {
                    'Content-type': 'application/json'
                },
                body: JSON.stringify({
                    subscription: subscription
                }),
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

Lesen Sie die MDN-Dokumentation auf der [pushmanager][MDNPushManager] -Oberfläche und in den NPM-Dokumenten in der [Web-Push-][NPMWebPushUsage] Bibliothek, um weitere Informationen zur Funktionsweise der APIs und verschiedene verwandte Optionen zu finden.  

### Schritt 5 – Einrichten von Push-und notificationclick-Ereignishandlern  

Bei der Einrichtung des Push-Abonnements erfolgt der Rest der Arbeit im Dienstmitarbeiter.  Zunächst müssen Sie einen Handler für vom Server gesendete Push-Ereignisse einrichten und mit einer Popupbenachrichtigung Antworten \(wenn die Berechtigung erteilt wurde \), die die pushdaten-Nutzlast anzeigt.  Als Nächstes fügen Sie einen Click-Handler für den Toast hinzu, um die Benachrichtigung zu schließen und durch eine Liste der derzeit geöffneten Fenster zu sortieren, um die beabsichtigte PWA-Clientseite zu öffnen, zu fokussieren oder zu öffnen und zu fokussieren.  

Fügen Sie in der `pwabuilder-sw.js` Datei die folgenden Handler ein.  

```javascript
//Respond to a server push with a user notification
self.addEventListener('push', function (event) {
    if ("granted" === Notification.permission) {
        var payload = event.data ? event.data.text() : 'no payload';
        const promiseChain = self.registration.showNotification('Sample PWA', {
            body: payload,
            icon: 'images/windows10/Square44x44Logo.scale-100.png'
        });
        //Ensure the toast notification is displayed before exiting this function
        event.waitUntil(promiseChain);
    }
});
    
//Respond to the user clicking the toast notification
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current is already open and focuses it
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

### Schritt 6 – probieren Sie es aus  

Zeit zum Testen von Push-Benachrichtigungen in ihrer PWA!  

1.  Führen `F5` Sie im Browser \(\) PWA aus.  Da Sie den Service Worker-Code \( `pwabuilder-sw.js` \) geändert haben, müssen Sie den devtools-Debugger \( `F12` \) im **Service Worker** -Übersichts Panel öffnen und die Registrierung der Dienstmitarbeiter **aufheben** und \( `F5` \) die Seite neu laden, um Sie erneut zu registrieren \(oder klicken Sie auf **Aktualisieren**\).  In einem Produktionsszenario überprüft der Browser regelmäßig, ob Updates für Dienstmitarbeiter vorhanden sind, und installiert die Updates im Hintergrund.  Sie sollten Sie hier für sofortige Ergebnisse zwingen.  
    
    Wenn Ihr Servicemitarbeiter aktiviert und versucht, ihre PWA-Benachrichtigung für Push-Benachrichtigungen zu abonnieren, wird unten auf der Seite ein Dialogfeld "Berechtigung" angezeigt.  
    
    ![Dialogfeld ' Berechtigung ' zum Aktivieren von Benachrichtigungen][ImageNotificationPermission]  
    
    Wählen Sie **Ja** aus, um Popupbenachrichtigungen für Ihre PWA zu aktivieren.  
    
1.  Wählen Sie im Bereich Service Worker Overview die Schaltfläche  **drücken** aus.  Es sollte eine Popupbenachrichtigung mit der Nutzlast \(hart codierte "Test Push Message from devtools" \) angezeigt werden.  
    
    ![Pushen einer Benachrichtigung von devtools][ImageDevtoolsPush]  
    
1.  Wählen Sie als nächstes die Schaltfläche " **Benachrichtigung senden** " auf der Startseite Ihrer PWA aus.  Dieses Mal wird ein Toast mit der Nutzlast Ihres Servers angezeigt.  
    
    ![Pushen einer Benachrichtigung vom PWA-Server][ImagePwaPush]  
    
    Wenn Sie nicht auf \(oder aktivieren \) einer Popupbenachrichtigung klicken, wird diese nach einigen Sekunden geschlossen und in Ihrem Windows-Wartungs Center in die Warteschlange gestellt.  
    
    ![Benachrichtigungen im Windows-Wartungs Center][ImageWindowsActionCenter]  
    
    Sie haben die Grundlagen von PWA-Push-Benachrichtigungen.  In einer echten App werden die nächsten Schritte auf eine Weise implementiert, um Pushabonnements zu verwalten und zu speichern sowie Nutzdaten, die über das Netzwerk gesendet werden, ordnungsgemäß zu [verschlüsseln][NPMWebPushEncrypt] .  
    
## Vertiefung  

Dieser Leitfaden zeigt die grundlegende Anatomie einer progressiven Web-App und Microsoft PWA-Entwicklungstools, einschließlich Visual Studio, PWA Builder und Edge-devtools.  

Natürlich gibt es noch viel mehr, was dazu führt, dass [eine tolle PWA][PwaEdgehtmlIndexRequirements] über das hinausgeht, was Sie hier lesen, einschließlich des reaktionsfähigen Designs, der Deep-Linking-Funktion, der [browserübergreifenden Tests][BrowserStackTestEdgeBrowser] und anderer [bewährter Methoden][Webhint] \(ganz zu schweigen von Ihrer APP-Funktionalität! \), doch dieser Leitfaden hat Ihnen hoffentlich eine fundierte Einführung in die Grundlagen von  Wenn Sie weitere Fragen zur PWA-Entwicklung mit Windows oder Visual Studio haben, geben Sie bitte einen Kommentar ab!  

Sehen Sie sich die anderen PWA-Leitfäden an, um zu erfahren, wie Sie die Kundenbindung erhöhen und eine nahtlosere, Betriebssystem integrierte App-Umgebung bereitstellen können.  

*   [Anpassen von Windows][PwaEdgehtmlWindowsFeatures] Mithilfe der einfachen Feature-Erkennung können Sie Ihre PWA für Windows 10-Kunden schrittweise über Native Windows-Runtime \(WinRT \)-APIs verbessern, beispielsweise für die Anpassung der kachelbenachrichtigungen für Windows- **Startmenü** und für die Taskleiste Jumplists und \(nach Berechtigung), die mit Benutzer Ressourcen wie Fotos, Musik und Kalender arbeiten.  
*   [PWAs im Microsoft Store][PwaEdgehtmlMicrosoftStore].  Erfahren Sie mehr über die Vorteile der App Store-Verteilung und wie Sie Ihre PWA übermitteln.  

## Weitere Informationen  

*   [Progressive Web-Apps auf MDN Web docs][MDNProgressiveWebApps] – exzellenter Leitfaden für Progressive Web-Apps.  
*   [Progressive Web-Apps auf Web. dev][WebDevProgressiveWebApps] – exzellenter Leitfaden für Progressive Web-Apps.  
*   [Progressive Web-Apps rockt][ProgressiveWebApps] – zeigt Beispiele für PWAs in der realen Welt.  
*   [Hacker-Nachrichten Leser als Progressive Web-Apps][HackerNewsProgressiveWebApps] – vergleicht unterschiedliche Frameworks und Leistungsmuster für die Implementierung einer Stichprobe \(Hacker Newsreader \) PWA.  

<!-- image links -->  

[ImageDevtoolsPush]: ./media/devtools-push.png  
[ImageDevtoolsSwCache]: ./media/devtools-cache.png  
[ImageDevtoolsSwOverview]: ./media/devtools-sw-overview.png  
[ImageNotificationPermission]: ./media/notification-permission.png  
[ImageOfflineHtml]: ./media/offline-html.png  
[ImagePwa]: ./media/pwa.png  
[ImagePwaPush]: ./media/pwa-push.png  
[ImageVsNodejsExpressIcon]: ./media/vs-nodejs-express-icon.png  
[ImageVsNodejsExpressIndex]: ./media/vs-nodejs-express-index.png  
[ImageVsNodejsExpressManifest]: ./media/vs-nodejs-express-manifest.png  
[ImageVsNodejsExpressPublic]: ./media/vs-nodejs-express-public.png  
[ImageVsNodejsExpressTemplate]: ./media/vs-nodejs-express-template.png  
[ImageWindowsActionCenter]: ./media/windows-action-center.png  

<!-- links -->  

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Anforderungen – Progressive Web-Apps \(EdgeHTML \) unter Windows | Microsoft docs"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Progressive Web-Apps \(EdgeHTML \) im Microsoft Store | Microsoft docs"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps/windows-features.md "Anpassen ihrer PWA \(EdgeHTML \) für Windows | Microsoft docs"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Microsoft Store-Richtlinien | Microsoft docs"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Lernprogramm: Erstellen einer Node.js-und Express-app in Visual Studio | Microsoft docs"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Veröffentlichen im Azure-App-Dienst – erstellen einer Node.js-und Express-app in Visual Studio | Microsoft docs"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "Was ist eine universelle Windows-Plattform \(UWP \)-app?  | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Erstellen eines Azure Free-Kontos | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web-Apps | Microsoft Azure"  

<!--[DeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote/ "page not found"  -->  

[WindowsBlogsPwaEdge]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#4UOdrDJj3124VIkc.97 "Willkommene Progressive Web-Apps für Microsoft Edge und Windows 10 | Windows-Blogs"  
[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Web-Benachrichtigungen in Microsoft Edge | Windows-Blogs"  

[VisualStudioDownloads]: https://www.visualstudio.com/downloads "Downloads | Visual Studio"  
[VisualStudioFree]: https://visualstudio.microsoft.com/free-developer-offers "﻿Kostenlose Entwickler Software & Services | Visual Studio"  
[VisualStudioPreview]: https://www.visualstudio.com/vs/preview "Visual Studio Preview"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "﻿Kostenlose Tests für Microsoft Edge-Browser unter Windows 10 | BrowserStack"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Hacker-Nachrichten Leser als Progressive Web-Apps"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope. PostMessage \(\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Progressive Web-Apps \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "Pushmanager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "Synchronisierungs-Manager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Verwenden von Service Mitarbeitern | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifest | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker. Prototype. PostMessage \(\) | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Senden von VAPID identifizierten webpush-Benachrichtigungen über den Push-Dienst von Mozilla | Mozilla-Dienste"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Push | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Verwendung-Web-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Progressive Web-Apps"  

[PugAttributes]: https://pugjs.org/language/attributes.html "Attribute | Mops"  

[PwaBuilder]: https://www.pwabuilder.com "PWA-Generator"  
[PwaBuilderAppImageGenerator]: https://www.pwabuilder.com/imageGenerator "App-Bild Generator"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Dienstmitarbeiter | PWA-Generator"  

[ServiceWorkerCookbook]: https://serviceworke.rs "ServiceWorker Cookbook"  
[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich-Demo | ServiceWorker Cookbook"  

[W3cWebAppManifest]: https://www.w3.org/TR/appmanifest "Web App-Manifest | W3C"  

[Webhint]: https://sonarwhal.com "webhint, das Hinweis Modul für bewährte Webmethoden" 
 
[MDNWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Verwenden von Web Workern" 

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Progressive Web-Apps | Web. dev"  

[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS | Wikipedia"  
[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Progressive Verbesserung | Wikipedia"  
