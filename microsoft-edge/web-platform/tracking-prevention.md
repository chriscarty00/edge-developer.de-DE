---
description: Diese Seite enthält Eine Dokumentation zum Feature Microsoft Edge (Chromium) zur Nachverfolgung
title: Tracking Prevention in Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, tracking prevention, trackers, cookies, storage, ad blocking, tracker blocking, tracking protection
ms.openlocfilehash: 66356ab7ddaa56e46e74560d72b510ba63f7d70a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399288"
---
# <a name="tracking-prevention-in-microsoft-edge-chromium"></a>Tracking Prevention in Microsoft Edge (Chromium)  

Das Feature zur Nachverfolgungsverhütung in Microsoft Edge schützt Benutzer vor der Onlineverfolgung, indem die Möglichkeit von Trackern eingeschränkt wird, auf browserbasierten Speicher sowie auf das Netzwerk zu zugreifen.  Es wurde so erstellt, [][MicrosoftEdgeBrowserPrivacyPromise] dass Microsoft Edge Datenschutzversprechen des Browsers eingehalten wird, während gleichzeitig sichergestellt wird, dass standardmäßig keine Auswirkungen auf die Websitekompatibilität oder die wirtschaftliche Lebensfähigkeit des Webs entstehen.  

Microsoft Edge bietet Benutzern derzeit drei Ebenen der Nachverfolgungsverhütung, die durch Navigieren zu ausgewählt `edge://settings/privacy` werden.  

![Drei Einstellungen für die Nachverfolgungsverhütung][ImageThreeSettingsTrackingPrevention]  

1.  **Basic** – Die am wenigsten restriktive Ebene der Nachverfolgungsverhütung, die für Benutzer gedacht ist, die personalisierte Werbung genießen und keine Bedenken haben, im Web nachverfolgt zu werden.  Basic schützt Benutzer nur vor bösartigen Trackern wie Fingerabdrücken und Kryptominern.  
1.  **Balanced (Standard)** – Die Standardstufe der Nachverfolgungsverhütung, die für Benutzer entwickelt wurde, die weniger gruselige Anzeigen anzeigen möchten, die ihnen während des Browsens im Web folgen.  Balanced zielt darauf ab, Tracker von Websites zu blockieren, mit deren Zugriff Benutzer niemals interagieren, und gleichzeitig das Risiko von Kompatibilitätsproblemen im Web zu minimieren.  
1.  **Strict** – Die restriktivste Stufe der Nachverfolgungsverhütung, die für Benutzer entwickelt wurde, die mit der Kompatibilität von Websites in Ordnung sind, um maximalen Datenschutz zu gewährleisten.  

Das Feature zur Nachverfolgungsverhütung in Microsoft Edge besteht aus drei Hauptkomponenten, die zusammenarbeiten, um zu bestimmen, ob eine bestimmte Ressource von einer Website als Tracker klassifiziert und blockiert werden soll.  Die Komponenten sind wie folgt:  

1.  **Klassifizierung** – Die Art Microsoft Edge bestimmt, ob eine URL zu einem Tracker gehört.  
1.  **Erzwingung** – Die Aktionen zum Schutz Microsoft Edge benutzer vor URLs, die als Tracker klassifiziert sind.  
1.  **Gegenmaßnahmen** – Die bereitgestellten Mechanismen, um sicherzustellen, dass von Benutzern angegebene Favoritenwebsites weiterhin funktionieren und gleichzeitig einen starken Standardschutz bieten.  

Jede der Komponenten wird auf dieser Seite untersucht und ausführlich erläutert.  

## <a name="classification"></a>Klassifizierung  

Die erste Komponente des Features zur Nachverfolgungsverhütung in Microsoft Edge ist die Klassifizierung.  Um Onlinetracker zu klassifizieren und in Kategorien einzuteilen, verwendet Microsoft Edge [die Schutzlisten zum][|::ref1::|Main] Trennen der Open [Source-Nachverfolgung.][GitHubDisconnectMeTrackingProtection]  Die Listen werden über die Komponente "Vertrauensschutzlisten" übermittelt, die unter angezeigt werden `edge://components` kann.  Nach dem Herunterladen werden die Listen auf dem Datenträger gespeichert, auf dem Sie bestimmen können, ob/wie eine bestimmte URL klassifiziert wird.  

Um zu ermitteln, ob eine URL vom Klassifizierungssystem in Microsoft Edge als Nachverfolgung betrachtet wird, wird eine Reihe von Hostnamen überprüft, beginnend mit einer genauen Übereinstimmung und anschließend mit der Überprüfung auf Teil übereinstimmungen auf bis zu vier Bezeichnungen außerhalb der Domäne auf oberster Ebene.  

> **Beispiel**:  
> 
> URL: `https://a.subdomain.of.a.known.tracker.test/some/path`  
> 
> Getestete Hostnamen:  
> 
> *   `a.subdomain.of.a.known.tracker.test`  
> *   `of.a.known.tracker.test`  
> *   `a.known.tracker.test`  
> *   `known.tracker.test`  
> *   `tracker.test`  

Wenn einer dieser Hostnamen mit einem [][|::ref2::|Main] Hostnamen in den Disconnect-Listen [übereinstimmen,][GitHubDisconnectMeTrackingProtection]wird Microsoft Edge mit der Auswertung von Erzwingungsaktionen fortgesetzt, um zu verhindern, dass Benutzer nachverfolgt werden.  

## <a name="enforcement"></a>Erzwingung  

Um Schutz vor Nachverfolgungsaktionen im Web zu bieten, Microsoft Edge zwei Erzwingungsaktionen gegen klassifizierte Tracker:

*   **Speicherzugriff einschränken:** Wenn eine bekannte Nachverfolgungsressource versucht, auf einen Webspeicher zu zugreifen, auf den daten über den Benutzer gespeichert werden können, wird Microsoft Edge zugriff blockiert.  Dies umfasst das Einschränken der Möglichkeit für diesen Tracker, Cookies zu erhalten oder zu setzen, sowie den Zugriff auf Speicher-APIs wie `IndexedDB` und `localStorage` .  
*   Blockieren von Ressourcenlasten **:** Wenn eine bekannte Nachverfolgungsressource auf einer Website geladen wird, blockiert Microsoft Edge diese Last möglicherweise, bevor die Anforderung das Netzwerk erreicht, je nachdem, wie sich die Auslastung auf die Kompatibilität auswirken und die Einstellung zur Nachverfolgungsverhütung festgelegt wurde, die ein Benutzer festgelegt hat.  Blockierte Lasten können Überwachungsskripts, Pixel, iframes und vieles mehr umfassen.  Dadurch wird verhindert, dass potenziell Daten an die Nachverfolgungsdomäne gesendet werden, und die Ladezeiten und die Seitenleistung können sogar als Nebeneffekt verbessert werden.  

Ein Benutzer kann das Flyoutsymbol für Seiteninformationen auf der linken Seite der Adressleiste auswählen, um herauszufinden, welche Tracker auf einer bestimmten Seite blockiert wurden: 

![Blockierte Tracker im Flyout für Seiteninformationen][ImageBlockedTrackersPageInfoFlyout]  

Wie die Erzwingungen angewendet werden, hängt davon ab, welche Stufe der Nachverfolgungsverhütung der Benutzer ausgewählt hat und welche Gegenmaßnahmen gelten können.  

## <a name="mitigations"></a>Gegenmaßnahmen  

Um sicherzustellen, dass die Webkompatibilität so weit wie möglich erhalten bleibt, Microsoft Edge drei Gegenmaßnahmen zum Ausgleich der Durchsetzung in bestimmten Situationen.  Dies sind [die Risikominderung für Org-Beziehungen,](#org-relationship-mitigation) [die Risikominderung für Org Engagement](#org-engagement-mitigation)und die [CompatExceptions-Liste.](#the-compatexceptions-list)  

Bevor Sie sich mit den Gegenmaßnahmen abm nnen, lohnt es sich, kurz das Konzept einer "Organisation" oder "Org" zu definieren.  [Disconnect][|::ref3::|Main] verwaltet auch eine Liste namens [entities.js,][GitHubDisconnectMeTrackingProtectionEntitiesJson] in der Gruppen von URLs definiert werden, die sich im Besitz derselben übergeordneten Organisation/desselben Unternehmens befinden.  Das Feature zur Nachverfolgungsverhütung in [](#org-relationship-mitigation) Microsoft Edge verwendet diese [](#org-engagement-mitigation) Liste sowohl in der Risikominderung der Organisationsbeziehung als auch in der Risikominderung für Organisationsengagement, um das Auftreten von Kompatibilitätsproblemen zu minimieren, die durch die Nachverfolgung von Verhinderungen verursacht werden, die organisationsübergreifende Anforderungen betreffen.  

### <a name="org-relationship-mitigation"></a>Risikominderung für Organisationsbeziehungen  

Mehrere beliebte Websites verwalten websites und Content Delivery Networks \(CDNs\), um statische Ressourcen und Inhalte für diese Websites zu verwenden.  Um sicherzustellen, dass diese Arten von Szenarien nicht von der Nachverfolgungsverhütung betroffen sind, entkoppelt Microsoft Edge eine Website von der Nachverfolgungsverhütung, wenn die Website Anforderungen von Drittanbietern an andere Websites stellt, die derselben übergeordneten Organisation gehören \(wie in der Trennliste [entities.jsin][GitHubDisconnectMeTrackingProtectionEntitiesJson]der Liste \ definiert).  Dies wird am besten durch ein Beispiel veranschaulicht.  

> **Beispiel:**
> 
> Eine Organisation namens Org1 besitzt die Domänen und , wie in der Liste trennen `org1.test` `org1-cdn.test` entities.js[definiert.][GitHubDisconnectMeTrackingProtectionEntitiesJson]  Imagine, die als Tracker klassifiziert sind und in der Regel durchsetzungsversprechend für die Nachverfolgung `org1-cdn.test` angewendet würden.  Wenn ein Benutzer besucht und die Website versucht, eine Ressource aus zu laden, führt Microsoft Edge keine Erzwingungsaktionen gegen Anforderungen an, an die sie vorgenommen werden, obwohl es sich nicht um eine URL eines `https://org1.test` `https://org1-cdn.test` Erstbenutzers `org1-cdn.test` handelt.  Wenn jedoch eine andere URL, die nicht Teil der Organisation Org1 ist, versucht, dieselbe Ressource zu laden, wird die Anforderung erzwingt, da sie nicht Teil derselben Organisation ist.  
> 
> Auch wenn dadurch die Verfolgung von Durchsetzungsmaßnahmen für Websites, die derselben Organisation angehören, entspannt wird, ist es unwahrscheinlich, dass dies ein hohes Datenschutzrisiko mit sich bringt, da solche Organisationen in der Lage sind, zu bestimmen, auf welche Websites/Ressourcen Sie zugegriffen haben, sowie interne `https://org1.test` `https://org1-cdn.test` Back-End-Daten.  

### <a name="org-engagement-mitigation"></a>Risikominderung für Organisationsengagement  

Die Risikominderung für das Engagement der Organisation wurde erstellt, um die durch die Nachverfolgung der Verhinderung verbundenen Kompatibilitätsrisiken zu minimieren, indem sichergestellt wurde, dass Websites im Besitz von Organisationen, mit denen Benutzer ausreichend interagieren, weiterhin wie erwartet im Gesamten Web funktionieren.  Die Websitebindung [][ChromiumDesignDocsSiteEngagement] wird verwendet, um die Erzwingung zu lockern, wenn ein Benutzer eine fortlaufende Beziehung \(derzeit definiert durch eine Websitebindungsnote von 4,1 oder höher\) mit einer bestimmten Website eingerichtet hat.  Dies wird auch hier am besten durch ein Beispiel veranschaulicht:

> **Beispiel:**
> 
> Eine Organisation namens Social Org besitzt die Domänen `social.example` und `social-videos.example` .
> 
> Benutzer gelten als eine Beziehung zu Social Org, wenn sie eine Websitebindungsnote von 4,1 oder höher mit einer der Domänen eingerichtet haben, die im Besitz von Social Org sind.
> 
> Wenn eine andere Website , Inhalte von Drittanbietern \(z. B. ein eingebettetes Video von \) aus einer der Domänen enthält, die im Besitz von Social Org sind, die normalerweise durch die Verfolgung von Durchsetzungen der Verhinderung eingeschränkt würden, ist die Website von der Verfolgung von Erzwingungen der Verhinderung ausgenommen, solange die Bewertung des Websiteengagements des Benutzers mit Domänen, die im Besitz von Social Org sind, über dem Schwellenwert beibehalten `https://content-embedder.example` `social-videos.example` wird.
> 
> Wenn eine Website nicht zu einer Organisation gehört, muss ein Benutzer eine Standortverlobungsnote von 4,1 oder höher direkt damit festlegen, bevor speicherzugriffs-/ressourcenlastblöcke, die durch die Nachverfolgungsverhinddung auferlegt werden, gelockert werden.

Die Risikominderung für Organisationsengagement wird derzeit nur im Balanced-Modus angewendet, sodass Microsoft Edge den größtmöglichen Schutz für Benutzer bietet, die sich für Strict entschieden haben.

### <a name="the-compatexceptions-list"></a>Die CompatExceptions-Liste  

Basierend auf dem kürzlich von Microsoft erhaltenen Benutzerfeedback verwaltet Microsoft Edge eine kleine Liste von Websites \(die meisten davon befinden sich in der Kategorie Inhalt trennen\), die aufgrund der Nachverfolgungsverhütung unterbrochen wurden, obwohl die beiden oben genannten Gegenmaßnahmen vorhanden waren. Websites in dieser Liste sind von der Verfolgung von Durchsetzungsmaßnahmen ausgenommen.  Die Liste finden Sie auf dem Datenträger an den [unten beschriebenen](#determining-whetherhow-a-particular-url-is-classified) Speicherorten.  Benutzer können Einträge auf dem Computer mithilfe der **Option Blockieren** in außer Kraft `edge://settings/content/cookies` setzen.

Um zu verhindern, dass diese Liste vorwärts bewegt wird, arbeitet Microsoft derzeit an der [Storage Access-API][GitHubMsExplainersStorageAccessApi] in der Chromium Codebasis.  Die [Storage Access-API][GitHubMsExplainersStorageAccessApi] bietet Websiteentwicklern eine Möglichkeit, Speicherzugriff von Benutzern direkt an anfordern zu können, um Benutzern mehr Transparenz darüber zu bieten, wie sich ihre Datenschutzeinstellungen auf ihre Browsererfahrung ausdingen, und websiteentwicklern Steuerelemente zur schnellen und intuitiven Deblockierung zur Verfügung zu stellen.

Nachdem die [Storage-Zugriffs-API][GitHubMsExplainersStorageAccessApi] implementiert wurde, entfernt Microsoft die Liste CompatExceptions und erreicht die betroffenen Websites, um sie auf die Probleme aufmerksam zu machen und die Verwendung der [Storage-Zugriffs-API][GitHubMsExplainersStorageAccessApi] zu fordern.  

## <a name="current-tracking-prevention-behavior"></a>Aktuelles Verhalten zur Nachverfolgungsverhütung  

In der folgenden Tabelle sind die Erzwingungsaktionen und Gegenmaßnahmen aufgeführt, die auf jede Kategorie von klassifizierten Trackern in Microsoft Edge.  

*   Am oberen Rand befinden sich die Kategorien von Trackern, die in Den Schutzlistenkategorien für die Verbindungsverfolgung [definiert sind.][GitHubDisconnectTrackingProtectionCategories]  
*   Auf der linken Seite befinden sich die drei Ebenen der Nachverfolgungsverhütung in Microsoft Edge \(Basic, Balanced und Strict\).  
*   Der Buchstabe `S` gibt an, dass der Speicherzugriff blockiert ist.  
*   Der Buchstabe gibt an, dass sowohl der Speicherzugriff als auch die `B` Ressourcenauslastung \(z. B. Netzwerkanforderungen\) blockiert werden.  
*   Ein Bindestrich \( \) gibt an, dass kein Block auf Speicherzugriff oder `-` Ressourcenlasten angewendet wird.  

| | Anzeigen | Analysen | Inhalt | Cryptomining | Fingerabdruck | Soziale Netzwerke | Other | Gleiche Risikominderung für Organisationen | Risikominderung für Organisationsengagement |  
| - | - | - | - | - | - | - | - | - | - | - |  
| **Einfach** | - | - | - | B | B | - | - | Aktiviert | n.a. |  
| **Ausgeglichen** | E | - | E | B | B | E | E | Aktiviert | Aktiviert |  
| **Streng** | B | B | E | B | B | B | B | Aktiviert | Deaktiviert |  

> [!NOTE]
> Die Risikominderung für Organisationsengagement gilt nicht für die Kategorien Cryptomining oder Fingerprinting.  

> [!TIP]
> Der strenge Modus blockiert mehr Ressourcenlasten als Balanced.  Das Blockieren von mehr Ressourcenlasten kann dazu führen, dass der Strenge Modus weniger Nachverfolgungsanforderungen blockiert als Balanced, da die Tracker, die die Anforderungen stellen, nie geladen werden.  

> [!NOTE]
> Die Spalte Fingerprinting in [Current tracking prevention behavior](#current-tracking-prevention-behavior) bezieht sich neben einer anderen Liste auf Tracker, die sich in der Fingerabdruckliste befinden.  Tracker, die ausschließlich in der Fingerabdruckliste angezeigt werden, gelten als nicht schädliche Fingerabdruckerkennungen und werden nicht blockiert.

### <a name="inprivate-behavior"></a>InPrivate-Verhalten  

In Microsoft Edge 79 war das Standardverhalten die Anwendung von Strengen Modusschutz in InPrivate.  In Microsoft Edge 80 wurde dieses Verhalten durch eine Option ersetzt, mit der Benutzer entscheiden können, ob sie strikten Modusschutz anwenden oder ihre regulären Einstellungen beim Browsen von `edge://settings/privacy` InPrivate behalten möchten.  

## <a name="determining-whetherhow-a-particular-url-is-classified"></a>Bestimmen, ob/wie eine bestimmte URL klassifiziert wird  

Am einfachsten können Sie ermitteln, ob eine bestimmte URL als bekannter Tracker klassifiziert wird, wenn Sie die folgenden Schritte ausführen.  

1.  Öffnen Sie DevTools, und navigieren Sie zur Registerkarte Konsole.  
1.  Aktualisieren Sie die Webseite.  
    1.  Möglicherweise möchten Sie Cookies und **andere** Websitedaten zuerst löschen, um die Ergebnisse der Websitebindung zurückzusetzen und eine vollständig saubere Schieferseite sicherzustellen.  
1.  Suchen Sie nach Nachrichten, die `Tracking Prevention blocked access to storage for <URL>` lesen.  
    1.  Sie können die Nachrichten erweitern, um die einzelnen blockierten URLs zu sehen.  
1.  Wenn Sie bestimmen müssen, in welcher Kategorie sich eine bestimmte blockierte Website befindet, können Sie am einfachsten in der Liste "Trennen" nach [services.jssuchen.][GitHubDisconnectTrackingProtectionCategories]  Die Einträge sind alphabetisch, sodass Sie mit einem Bildlauf zum oberen Rand eines Blocks von Websiteeinträgen die spezifische Kategorie für eine bestimmte Website finden können.  

> [!TIP]
> Wenn Sie auf die Aufverfolgungsverhütungslisten zugreifen müssen, die auf dem Datenträger gespeichert sind, kann jede an einem der beiden Speicherorte gefunden werden.  
>
> **Komponentenbasierte Updates** – Die Listen, die von der Komponente "Vertrauensschutzlisten" heruntergeladen werden  
>
> Fenster: `%LOCALAPPDATA%\Microsoft\Edge <OptionalChannelName>\User Data\Trust Protection Lists`  
>
> macOS: `~/Library/Application Support/Microsoft Edge <OptionalChannelName>/Trust Protection Lists`  
>
> **Installationsverzeichnis** : Die Listen, die mit dem Installationsprogramm Microsoft Edge werden.  Wenn Sie ein anderes Installationsverzeichnis ausgewählt haben, können die genauen Pfade unterschiedlich sein.  
>
> Fenster: `%PROGRAMFILES(x86)%\Microsoft\ Edge <OptionalChannelName>\Application<Version>\Trust Protection Lists`  
>
> macOS: `/Applications/Microsoft Edge.app/Contents/Frameworks/Microsoft Edge Framework.framework/Libraries/Trust Protection Lists`  

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen  

Der folgende Abschnitt enthält Antworten auf häufig gestellte Fragen zum Feature zur Nachverfolgungsverhütung in Microsoft Edge.  

**Gibt es eine Möglichkeit, bestimmte Tracker zu Debugzwecken zu blockieren oder zu erlauben?**  

Derzeit wird Microsoft Edge nur eine Option zum Deaktivieren der Ausführung von Verfolgungsverhütungsersetzungen auf einer angegebenen Website verfügbar gemacht.  Auf diese Option wird über das Flyout für Seiteninformationen oder über die Seite `edge://settings/privacy/trackingPreventionExceptions` zugegriffen.  

Die Optionen **Block** und **Allow** auf der Seite können jedoch verwendet werden, um bestimmten Domänen den Zugriff auf den Speicher wie Cookies und andere `edge://settings/content/cookies` Browserspeichermechanismen zu ermöglichen oder zu verweigern.  Dies ist hilfreich beim Debuggen von Websiteproblemen, die durch das Nachverfolgen von Erzwingungen zur Verhinderung des Zugriffs auf Speicher für eine bestimmte Website verursacht werden.  

<!-- image links -->  

[ImageThreeSettingsTrackingPrevention]: ./media/tracking-prevention-settings.png  
[ImageBlockedTrackersPageInfoFlyout]: ./media/page-info-flyout.png  

<!-- links -->  

[MicrosoftEdgeBrowserPrivacyPromise]: https://microsoftedgewelcome.microsoft.com/privacy "Datenschutz – Microsoft Edge"  

[ChromiumDesignDocsSiteEngagement]: https://www.chromium.org/developers/design-documents/site-engagement "Site Engagement – Die Chromium Projekte"  

[DisconnectMain]: https://disconnect.me "Disconnect"  

[GitHubDisconnectMeTrackingProtection]: https://github.com/disconnectme/disconnect-tracking-protection "disconnectme/disconnect-tracking-protection | Github"  
[GitHubDisconnectTrackingProtectionCategories]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/services.json "services.js- disconnectme/disconnect-tracking-protection | Github"  
[GitHubDisconnectMeTrackingProtectionEntitiesJson]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/entities.json "entities.js- disconnectme/disconnect-tracking-protection | Github"  

[GitHubMsExplainersStorageAccessApi]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/StorageAccessAPI/explainer.md "Storage Access-API-Erklärer – MSEdgeExplainers/StorageAccessAPI | GitHub"
