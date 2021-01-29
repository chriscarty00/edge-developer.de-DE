---
description: Verwenden Sie den Anwendungs Panel, um Web App-Manifeste, Dienstmitarbeiter und Service Worker-Caches zu prüfen, zu ändern und zu debuggen.
title: Debuggen von progressiven Web-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 79edf4b04c85db33e89d18ec1832138a61f4f884
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233600"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# Debuggen von progressiven Web-Apps  

Verwenden Sie den **Anwendungs** Panel, um Web App-Manifeste, Dienstmitarbeiter und Service Worker-Caches zu prüfen, zu ändern und zu debuggen.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

In diesem Leitfaden werden nur die fortschrittlichen Web App-Features des **Anwendungs** Panels erläutert.  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### Zusammenfassung  

*   Verwenden Sie den Bereich **Manifest** , um das Web App-Manifest zu überprüfen und auf Homescreen-Ereignisse hinzufügen zu starten.  
*   Verwenden Sie den Bereich " **Dienstmitarbeiter** " für eine ganze Reihe von Dienstmitarbeiter bezogenen Aufgaben, wie das Aufheben der Registrierung oder Aktualisierung eines Diensts, das Emulieren von Push-Ereignissen, das offline schalten oder Beenden eines Dienst Mitarbeiters.  
*   Zeigen Sie den Service Worker-Cache im **Cachespeicher** Bereich an.  
*   Heben Sie die Registrierung eines Dienstmitarbeiter auf, und löschen Sie alle Speicher und Caches mit einem einzigen Mausklick aus dem Bereich " **Speicher löschen** ".  
    
## Web App-Manifest  

Wenn Sie möchten, dass Ihre Benutzer Ihre APP ihren mobilen Homescreens hinzufügen können, benötigen Sie ein Web App-Manifest.  Das Manifest definiert, wie die APP auf dem Homescreen angezeigt wird, wo der Benutzer beim Start von Homescreen weitergeleitet wird und wie die APP beim Start aussieht.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

Nachdem Sie Ihr Manifest eingerichtet haben, können Sie es über den Bereich **Manifest** des **Anwendungs** Bereichs überprüfen.  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/manifest-pane.msft.png":::
   Bereich ' **Manifest** '  
:::image-end:::  

*   Wenn Sie sich die Manifest-Quelle ansehen möchten, klicken Sie auf den Link unter **App-Manifest** -Beschriftung \ ( `https://airhorner.com/manifest.json` in der vorhergehenden Abbildung).  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   In den Abschnitten **Identität** und **Präsentation** werden nur Felder aus der Manifestdatei in einer benutzerfreundlicheren Anzeige angezeigt.  
*   Im Abschnitt "Symbole" werden alle von Ihnen angegebenen **Symbole** angezeigt.  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## Service Workers  

Service Mitarbeiter sind eine grundlegende Technologie in der zukünftigen Web-Plattform.  Dabei handelt es sich um Skripts, die der Browser im Hintergrund ausführt, und zwar unabhängig von einer Webseite.  Diese Skripts ermöglichen Ihnen den Zugriff auf Features, die keine Webseite oder Benutzerinteraktion benötigen, wie Push-Benachrichtigungen, Hintergrundsynchronisierung und Offline-Erlebnisse.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

Der Bereich " **Dienstmitarbeiter** " im Bereich " **Anwendung** " ist der wichtigste Ort in devtools zum Überprüfen und Debuggen von Dienst Mitarbeitern.  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="Der Bereich Dienstmitarbeiter" lightbox="../media/service-workers-pane.msft.png":::
   Der Bereich " **Dienstmitarbeiter** "  
:::image-end:::  

*   Wenn ein Dienstmitarbeiter auf der aktuell geöffneten Seite installiert ist, wird er in diesem Bereich aufgelistet.  In der vorherigen Abbildung ist beispielsweise ein Dienstmitarbeiter für den Bereich von installiert `https://weather-pwa-sample.firebaseapp.com` .  
*   Mit dem Kontrollkästchen **Offline** wird devtools in den Offlinemodus versetzt.  Dies entspricht dem Offlinemodus, der über das **Netzwerk** Panel zur Verfügung steht, oder die `Go offline` Option im [Menübefehl][DevtoolsCommandMenuIndex].  
*   Das Kontrollkästchen " **beim erneuten Laden aktualisieren** " zwingt den Dienstmitarbeiter, bei jeder Seitenauslastung zu aktualisieren.  
*   Das Kontrollkästchen " **für Netzwerk umgehen** " umgeht den Dienstmitarbeiter und zwingt den Browser, für angeforderte Ressourcen zum Netzwerk zu wechseln.  
*   Die Schaltfläche " **Aktualisieren** " führt eine einmalige Aktualisierung der angegebenen Dienstmitarbeiter aus.  
*   Die Schaltfläche " **Push** " emuliert eine Push-Benachrichtigung ohne Nutzlast \ (auch bekannt als " **Tickle**\").  
*   Die Schaltfläche " **Synchronisieren** " emuliert ein Hintergrund Synchronisierungsereignis.  
*   Mit der Schaltfläche zum **aufheben** der Registrierung wird der angegebene Dienstmitarbeiter aufgehoben.  Schauen Sie sich das Kontrollkästchen [Speicher löschen](#clear-storage) an, um eine Möglichkeit zum Aufheben der Registrierung eines Dienstmitarbeiter und zum Löschen von Speicher und Zwischenspeichern mit einem einzigen Mausklick zu finden.  
*   Die **Quell** Zeile zeigt an, wann der aktuell ausgeführte Dienstmitarbeiter installiert wurde.  Bei dem Link handelt es sich um den Namen der Quelldatei des Dienst Mitarbeiters.  Wenn Sie auf den Link klicken, werden Sie an die Quelle des Dienst Mitarbeiters gesendet.  
*   In der **Status** Zeile wird der Status der Dienstmitarbeiter angezeigt.  Die ID-Nummer neben dem grünen Statusindikator \ ( `#36` in der vorherigen Abbildung \) ist für den aktuell aktiven Dienstmitarbeiter.  Neben dem Status wird die Schaltfläche **Start** \ (wenn der Dienstmitarbeiter angehalten wird) oder eine Schaltfläche " **Beenden** " \ (wenn der Dienstmitarbeiter ausgeführt wird) angezeigt.  Dienstmitarbeiter sind so konzipiert, dass Sie jederzeit angehalten und vom Browser gestartet werden können.  Das explizite beenden Ihrer Dienstmitarbeiter mithilfe der Schaltfläche " **Beenden** " kann dies simulieren.  Das Beenden Ihrer Dienstmitarbeiter stellt eine hervorragende Möglichkeit dar, zu testen, wie sich der Code verhält, wenn der Dienstmitarbeiter wieder startet.  Sie zeigt häufig Fehler aufgrund fehlerhafter Annahmen über den persistenten globalen Zustand.  
*   Die Zeile " **Clients** " gibt den Ursprung an, auf den sich der Dienstmitarbeiter beläuft.  Die Schaltfläche " **Fokus** " ist meist hilfreich, wenn Sie das Kontrollkästchen " **Alle anzeigen** " aktiviert haben.  Wenn dieses Kontrollkästchen aktiviert ist, werden alle registrierten Dienstmitarbeiter aufgelistet.  Wenn Sie auf die Schaltfläche **Fokus** neben einem Dienstmitarbeiter klicken, der auf einer anderen Registerkarte ausgeführt wird, konzentriert sich Microsoft Edge auf die Registerkarte.  
    
Wenn der Dienstmitarbeiter Fehler verursacht, wird eine neue Bezeichnung mit dem Namen **Fehler** angezeigt.  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## Dienst Worker-Caches  

Der Bereich **Cache-Speicher** bietet eine schreibgeschützte Liste der Ressourcen, die mit der [Cache-API][MDNWebCacheAPI]\ (Service Worker \) zwischengespeichert wurden.  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="Der Cache Speicherbereich" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   Der **Cache Speicher** Bereich  
:::image-end:::  

> [!NOTE]
> Wenn Sie zum ersten Mal einen Cache öffnen und ihm eine Ressource hinzufügen, erkennt devtools die Änderung möglicherweise nicht.  Laden Sie die Seite neu, und Sie sollten den Cache sehen.  

Wenn zwei oder mehr Caches geöffnet sind, werden Sie unter der Dropdownliste **Cachespeicher** aufgelistet.  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="Die Dropdownliste Cache Speicher" lightbox="../media/cache-pane-cache-storage.msft.png":::
   Die Dropdownliste " **Cache Speicher** "  
:::image-end:::  

## Kontingent Verwendung  

Einige Antworten innerhalb des **Cache Speicher** Bereichs werden möglicherweise als "undurchsichtig" gekennzeichnet.  Dies bezieht sich auf eine Antwort, die von einem anderen Ursprung abgerufen wurde, wie etwa von einem **CDN** oder einer Remote-API, wenn [CORS][FetchHttpCorsProtocol] nicht aktiviert ist.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Um das Auslaufen von domänenübergreifenden Informationen zu vermeiden, wird die Größe einer undurchsichtigen Antwort, die für die Berechnung von Speicherkontingent Grenzwerten verwendet wird, erheblich erweitert (beispielsweise, ob eine `QuotaExceeded` Ausnahme ausgelöst wird \) und von der `navigator.storage` API gemeldet.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Die Details dieses Textabstands variieren von Browser zu Browser, aber für Microsoft Edge bedeutet dies, dass die **Mindestgröße** , die eine einzelne zwischengespeicherte undurchsichtige Antwort zur allgemeinen Speichernutzung beiträgt, [ungefähr 7 Megabyte][ChromiumIssues796060#c17]beträgt.  Beachten Sie Folgendes, wenn Sie ermitteln möchten, wie viele undurchsichtige Antworten Sie zwischenspeichern möchten, da Sie die Speicherkontingent Einschränkungen auf einfache Weise überschreiten können, die auf der tatsächlichen Größe der opaken Ressourcen basiert.  

Verwandte Leitfäden:  

*   [Stapelüberlauf: Welche Einschränkungen gelten für undurchsichtige Antworten?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## Speicher löschen  

Der Bereich " **Speicher löschen** " ist eine sehr nützliche Funktion, wenn Sie Progressive Web-Apps entwickeln.  In diesem Bereich können Sie die Registrierung von Dienst Mitarbeitern aufheben und alle Caches und den Speicher mit einem einzigen Klick auf die Schaltfläche Löschen.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chrom Problem 796060: der Cache Speicherwert steigt bei jeder Aktualisierung, wenn sich der Analysecode im HTML-Code befindet"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache-Web-APIs | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stapelüberlauf: Welche Einschränkungen gelten für undurchsichtige Antworten?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
