---
description: Verwenden Sie den Anwendungsbereich, um Web-App-Manifeste, Servicemitarbeiter und Dienstmitarbeitercaches zu überprüfen, zu ändern und zu debuggen.
title: Debuggen progressiver Web-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: aea01d25474a030e78ac0eaeaef3954ab7f4539f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398539"
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

# <a name="debug-progressive-web-apps"></a>Debuggen progressiver Web-Apps  

Verwenden Sie **den Anwendungsbereich,** um Web-App-Manifeste, Servicemitarbeiter und Dienstmitarbeitercaches zu überprüfen, zu ändern und zu debuggen.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

In diesem Handbuch werden nur die Progressive Web App-Features des **Anwendungsbereichs** erläutert.  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a>Zusammenfassung  

*   Verwenden Sie den **Manifestbereich,** um Ihr Web-App-Manifest zu überprüfen und Add to Homescreen-Ereignisse auszulösen.  
*   Verwenden Sie **den Bereich Service Workers** für eine ganze Reihe von aufgabenbezogenen Aufgaben, z. B. aufheben der Registrierung oder Aktualisierung eines Diensts, Emulieren von Pushereignissen, Offlinemodus oder Beenden eines Dienstmitarbeiters.  
*   Anzeigen des Dienstarbeitscaches im **Cachespeicherbereich.**  
*   Aufheben der Registrierung eines Dienstmitarbeiters und Löschen aller Speicher und Caches mit einer einzelnen Schaltfläche wählen Sie aus dem **Bereich Speicher löschen** aus.  
    
## <a name="web-app-manifest"></a>Web-App-Manifest  

Wenn Sie möchten, dass Ihre Benutzer Ihre App ihren mobilen Startseiten hinzufügen können, benötigen Sie ein Web-App-Manifest.  Das Manifest definiert, wie die App auf dem Startbildschirm angezeigt wird, wo der Benutzer beim Starten vom Startbildschirm direkt angezeigt werden soll und wie die App beim Start aussieht.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

Nachdem Sie Ihr Manifest eingerichtet haben, können Sie **** den **Manifestbereich** des Anwendungsbereichs verwenden, um es zu überprüfen.  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="Der Manifestbereich" lightbox="../media/manifest-pane.msft.png":::
   Der **Manifestbereich**  
:::image-end:::  

*   Um die Manifestquelle zu sehen, wählen Sie den Link unter **App-Manifestbeschriftung** \( `https://airhorner.com/manifest.json` in der vorherigen Abbildung\).  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   In **den Abschnitten** **Identity und Presentation** werden nur Felder aus der Manifestquelle in einer benutzerfreundlicheren Anzeige angezeigt.  
*   Im **Abschnitt Symbole** werden alle von Ihnen angegebenen Symbole angezeigt.  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a>Service Workers  

Servicemitarbeiter sind eine grundlegende Technologie in der zukünftigen Webplattform.  Dabei handelt es sich um Skripts, die im Hintergrund ausgeführt werden, getrennt von einer Webseite.  Mit den Skripts können Sie auf Features zugreifen, die ohne eine Webseite oder Benutzerinteraktion wie Pushbenachrichtigungen, Hintergrundsynchronisierung und Offlineerfahrungen erforderlich sind.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

Der **Bereich "Service Workers"** im **Bereich "Anwendung"** ist der wichtigste Ort in DevTools zum Überprüfen und Debuggen von Servicemitarbeitern.  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="Der Bereich Service Workers" lightbox="../media/service-workers-pane.msft.png":::
   Der **Bereich "Service Workers"**  
:::image-end:::  

*   Wenn ein Dienstmitarbeiter auf der derzeit geöffneten Seite installiert ist, wird er in diesem Bereich aufgelistet.  In der vorherigen Abbildung ist beispielsweise ein Dienstmitarbeiter für den Bereich `https://weather-pwa-sample.firebaseapp.com` installiert.  
*   Das **Kontrollkästchen Offline** versetzt DevTools in den Offlinemodus.  Dies entspricht dem Offlinemodus, der über **das** Netzwerktool verfügbar ist, oder der Option `Go offline` im [Befehlsmenü][DevtoolsCommandMenuIndex].  
*   Das **Kontrollkästchen Beim Erneutladen** aktualisieren erzwingt, dass der Dienstmitarbeiter bei jeder Seitenlast aktualisiert wird.  
*   Das **Kontrollkästchen Netzwerkumgehung** umgehen umgeht den Dienstmitarbeiter und zwingt den Browser, für angeforderte Ressourcen in das Netzwerk zu wechseln.  
*   Die **Schaltfläche** Aktualisieren führt eine einmalaktualisierung des angegebenen Dienstmitarbeiters durch.  
*   Die **Schaltfläche Push** emuliert eine Pushbenachrichtigung ohne Nutzlast \(auch als **Tickle \)** bekannt.  
*   Die **Schaltfläche Synchronisierung** emuliert ein Hintergrundsynchronisierungsereignis.  
*   Mit **der Schaltfläche** Aufheben der Registrierung wird die Registrierung des angegebenen Dienstmitarbeiters aufgehoben.  Weitere Informationen zum [Aufheben der](#clear-storage) Registrierung eines Dienstmitarbeiters und zum Löschen von Speicher und Zwischenspeichern mit einer einzelnen Schaltfläche finden Sie unter Löschen des Speichers.  
*   Die **Zeile Source** informiert Sie, wann der derzeit ausgeführte Dienstmitarbeiter installiert wurde.  Der Link ist der Name der Quelldatei des Dienstmitarbeiters.  Wenn Sie den Link auswählen, werden Sie an die Quelle des Servicemitarbeiters übermittelt.  
*   In **der Zeile Status** wird der Status des Servicemitarbeiters angezeigt.  Die ID-Nummer neben dem grünen Statusindikator \( in der vorherigen Abbildung\) ist für den `#36` derzeit aktiven Service Worker.  Neben dem Status **** wird eine Startschaltfläche \(wenn der **** Dienstmitarbeiter beendet wird\) oder eine Stoppschaltfläche \(wenn der Dienstmitarbeiter ausgeführt wird\) angezeigt.  Servicemitarbeiter sind so konzipiert, dass sie jederzeit vom Browser angehalten und gestartet werden.  Das explizite Beenden des Dienstmitarbeiters **mithilfe** der Stoppschaltfläche kann dies simulieren.  Das Beenden des Dienstmitarbeiters ist eine hervorragende Möglichkeit, um zu testen, wie sich Ihr Code verhält, wenn der Dienstmitarbeiter wieder hoch startet.  Aufgrund fehlerhafter Annahmen über den dauerhaften globalen Zustand werden häufig Fehler gemeldet.  
*   Die **Zeile Clients** teilt Ihnen den Ursprung mit, auf den der Dienstmitarbeiter begrenzt ist.  Die **Fokusschaltfläche** ist hauptsächlich hilfreich, wenn Sie das Kontrollkästchen Alle **Anzeigen** aktiviert haben.  Wenn dieses Kontrollkästchen aktiviert ist, werden alle registrierten Servicemitarbeiter aufgelistet.  Wenn Sie die **Fokusschaltfläche** neben einem Servicemitarbeiter auswählen, der auf einer anderen Registerkarte ausgeführt wird, konzentriert sich Microsoft Edge auf diese Registerkarte.  
    
Wenn der Dienstmitarbeiter Fehler verursacht, wird eine neue Bezeichnung **namens Errors** angezeigt.  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a>Dienstarbeitscaches  

Der **Bereich Cachespeicher** enthält eine schreibgeschützte Liste der Ressourcen, die mithilfe der Cache-API \(Service Worker\) [zwischengespeichert wurden.][MDNWebCacheAPI]  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="Cachespeicherbereich" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   **Cachespeicherbereich**  
:::image-end:::  

> [!NOTE]
> Wenn Sie zum ersten Mal einen Cache öffnen und eine Ressource hinzufügen, erkennt DevTools die Änderung möglicherweise nicht.  Aktualisieren Sie die Seite, und zeigen Sie den Cache an.  

Wenn sie zwei oder mehr Caches geöffnet haben, werden die Caches im folgenden **Dropdownmenü Cachespeicher** angezeigt.  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="Dropdownliste Cachespeicher" lightbox="../media/cache-pane-cache-storage.msft.png":::
   Dropdownliste **Cachespeicher**  
:::image-end:::  

## <a name="quota-usage"></a>Kontingentverwendung  

Einige Antworten im **Bereich Cachespeicher** werden möglicherweise als "undurchsichtig" gekennzeichnet.  Dies bezieht sich auf eine Antwort, die von einem anderen Ursprung abgerufen wird, z. B. aus einem **CDN** oder einer Remote-API, wenn [CORS][FetchHttpCorsProtocol] nicht aktiviert ist.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Um ein Leck an domänenübergreifenden Informationen zu vermeiden, wird der Größe einer undurchsichtigen Antwort, die zum Berechnen von Speicherkontingentgrenzen verwendet wird \(z. B. ob eine Ausnahme ausgelöst wird\) und von der API gemeldet, ein erheblicher Abstand `QuotaExceeded` `navigator.storage` hinzugefügt.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Die Details dieses Abstands variieren von Browser zu Browser, für **** Microsoft Edge bedeutet dies jedoch, dass die Mindestgröße, die eine einzelne zwischengespeicherte undurchsichtige Antwort zur Gesamtspeichernutzung beiträgt, ca. 7 MB [beträgt.][ChromiumIssues796060#c17]  Denken Sie an den Abstand, wenn Sie bestimmen, wie viele undurchsichtige Antworten Zwischenspeicherung erfordern, da Speicherkontingentbeschränkungen möglicherweise viel früher überschritten werden, als Sie es basierend auf der tatsächlichen Größe der undurchsichtigen Ressourcen sonst erwarten.  

Verwandte Leitfäden:  

*   [Stack Overflow: Welche Einschränkungen gelten für undurchsichtige Antworten?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a>Löschen des Speichers  

Der **Bereich Speicher löschen** ist ein sehr nützliches Feature bei der Entwicklung progressiver Web-Apps.  In diesem Bereich können Sie die Registrierung von Servicemitarbeitern aufheben und alle Caches und Speicher mit einer einzigen Schaltfläche löschen.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit der Microsoft Edge DevTools-Befehlsmenüleiste | Microsoft Docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium Issue 796060: Cache Storage value rises on each refresh when Analytics code is in the html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache – Web-APIs | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stack Overflow: Welche Einschränkungen gelten für undurchsichtige Antworten?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
