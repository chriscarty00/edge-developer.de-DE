---
description: Diese Seite enthält die Dokumentation zur Nachverfolgungsfunktion von Microsoft Edge (Chrom)
title: Nach Verfolgungs Verhinderung in Microsoft Edge (Chrom)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Web-Plattform, Tracking-Prävention, Tracker, Cookies, Speicher, AD-Blockierung, Tracker-Blockierung, Tracking-Schutz
ms.openlocfilehash: a767e55a44c4d416b6d40ca12eb49f2c3a722010
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231152"
---
# Nach Verfolgungs Verhinderung in Microsoft Edge (Chrom)  

Das Feature zur nach Verfolgungs Verhinderung in Microsoft Edge schützt Benutzer vor Online Nachverfolgung, indem es die Möglichkeit von Nachverfolgungen für den Zugriff auf browserbasierten Speicher sowie für das Netzwerk einschränken.  Es wurde entwickelt, um die [Datenschutz Versprechen][MicrosoftEdgeBrowserPrivacyPromise] von Microsoft Edge Browser zu wahren und gleichzeitig sicherzustellen, dass es keine Auswirkungen auf die Website Kompatibilität oder die wirtschaftliche Rentabilität des Webs gibt.  

Microsoft Edge bietet derzeit Benutzern drei Ebenen der nach Verfolgungs Prävention, die durch Navigieren zu ausgewählt werden `edge://settings/privacy` .  

![Drei Einstellungen für die nach Verfolgungs Verhinderung][ImageThreeSettingsTrackingPrevention]  

1.  **Standard** – die am wenigsten einschränkende Ebene der nach Verfolgungs Prävention, die für Benutzer entwickelt wurde, die personalisierte Ankündigungen nutzen und die nicht im Web verfolgt werden.  Standard schützt nur Benutzer vor böswilligen Tracker wie Fingerabdruck-und cryptominers.  
1.  **Ausgeglichen (Standard)** – die Standardebene der nach Verfolgungs Verhinderung, die für Benutzer entwickelt wurde, die nicht so gruselige Ankündigungen sehen möchten, die Ihnen während der Durchsuchung im Internet folgen.  "Balanced" zielt darauf ab, Nachverfolgen von Websites zu blockieren, mit denen Benutzer nie in Kontakt treten, während das Risiko von Kompatibilitätsproblemen im Internet minimiert wird.  
1.  **Strict** -die restriktivste Ebene der nach Verfolgungs Prävention, die für Benutzer konzipiert ist, die in der Lage sind, die Kompatibilität der Website für maximale Datensicherheit zu überwachen.  

Das Feature zur nach Verfolgungs Verhinderung in Microsoft Edge besteht aus drei Hauptkomponenten, die zusammenarbeiten, um zu ermitteln, ob eine bestimmte Ressource einer Website als Tracker klassifiziert und blockiert werden soll.  Die Komponenten lauten wie folgt:  

1.  **Klassifizierung** : die Art und Weise, wie Microsoft Edge feststellt, ob eine URL zu einem Tracker gehört.  
1.  **Erzwingung** – die Aktionen, mit denen Microsoft Edge-Benutzer vor URLs geschützt werden, die als Tracker klassifiziert wurden.  
1.  **Abschwächungen** – die Mechanismen, mit denen sichergestellt wird, dass benutzerdefinierte bevorzugte Websites weiterhin funktionieren, während ein starker Standardschutz geboten wird.  

Auf dieser Seite werden alle Komponenten untersucht und ausführlich erläutert.  

## Klassifizierung  

Die erste Komponente des Features zur nach Verfolgungs Verhinderung in Microsoft Edge ist die Klassifizierung.  Um Online-Tracker zu klassifizieren und Sie in Kategorien zu gruppieren, verwendet Microsoft Edge die [Disconnect][|::ref1::|Main] Open Source [Tracking Protection-Listen][GitHubDisconnectMeTrackingProtection].  Die Listen werden über die "Trust Protection lists"-Komponente bereitgestellt, die bei angezeigt werden kann `edge://components` .  Nach dem herunterladen werden die Listen auf der Festplatte gespeichert, wo Sie Sie verwenden können, um festzustellen, ob/wie eine bestimmte URL klassifiziert wird.  

Wenn Sie feststellen möchten, ob eine URL vom Klassifikationssystem in Microsoft Edge als Nachverfolgung angesehen wird, werden eine Reihe von Hostnamen überprüft, beginnend mit einer genauen Übereinstimmung, und dann wird die Überprüfung auf partielle Übereinstimmungen mit bis zu vier Beschriftungen über die Domäne der obersten Ebene hinaus fortgesetzt.  

> **Beispiel**:  
> 
> URL `https://a.subdomain.of.a.known.tracker.test/some/path`  
> 
> Getestete Host-Namen:  
> 
> *   `a.subdomain.of.a.known.tracker.test`  
> *   `of.a.known.tracker.test`  
> *   `a.known.tracker.test`  
> *   `known.tracker.test`  
> *   `tracker.test`  

Wenn einer dieser Hostnamen mit einem Hostnamen in der [Liste][GitHubDisconnectMeTrackingProtection]" [trennen][|::ref2::|Main] " übereinstimmt, wird Microsoft Edge mit der Auswertung von Erzwingungs Aktionen fortgesetzt, um zu verhindern, dass Benutzer nachverfolgt werden.  

## Erzwingung  

Um Schutz vor der Nachverfolgung von Aktionen im Web zu gewährleisten, übernimmt Microsoft Edge zwei Erzwingungs Aktionen für klassifizierte Tracker:

*   **Einschränken des Speicherzugriffs** – wenn eine bekannte nach Verfolgungs Ressource versucht, auf einen Webspeicher zuzugreifen, in dem Sie möglicherweise versucht, Daten über den Benutzer zu speichern, blockiert Microsoft Edge diesen Zugriff.  Dies umfasst das Einschränken der Möglichkeit für diesen Tracker, Cookies abzurufen oder festzulegen sowie Access-Speicher-APIs wie und zu speichern `IndexedDB` `localStorage` .  
*   **Blockieren von Ressourcen Lasten** – wenn eine bekannte nach Verfolgungs Ressource auf eine Website geladen wird, blockiert Microsoft Edge möglicherweise diese Last, bevor die Anforderung das Netzwerk erreicht, abhängig von der Kompatibilitäts Auswirkung der Last und der Einstellung für die nach Verfolgungs Vermeidung, die ein Benutzer festgelegt hat.  Blockierte Lasten können Tracking-Skripte, Pixel, Iframes und vieles mehr umfassen.  Dadurch wird verhindert, dass Daten potenziell an die Überwachungs Domäne gesendet werden, und möglicherweise sogar die Ladezeiten und die Seitenleistung als Nebeneffekt verbessern.  

Ein Benutzer kann auf der linken Seite der Adressleiste auf das Symbol "Seiten Info" klicken, um festzustellen, welche Tracker auf einer bestimmten Seite blockiert wurden: 

![Blockierte Tracker im Seiten Info-Flyout][ImageBlockedTrackersPageInfoFlyout]  

Wie die Erzwingung angewendet wird, hängt davon ab, welche Ebene der nach Verfolgungs Verhinderung der Benutzer ausgewählt hat und welche Abschwächungen möglicherweise gelten.  

## Minderungen  

Um sicherzustellen, dass die webkompatibilität so weit wie möglich erhalten bleibt, verfügt Microsoft Edge über drei Schadensbegrenzende Maßnahmen, um die Erzwingung in bestimmten Situationen zu unterstützen.  Hierbei handelt es sich um die [Minderung der org-Beziehung](#org-relationship-mitigation), die Minderung des org- [Engagements](#org-engagement-mitigation)und die [CompatExceptions-Liste](#the-compatexceptions-list).  

Vor dem Eintauchen in die Schadensbegrenzende Maßnahmen ist es sinnvoll, das Konzept einer "Organisation" oder "org" kurz zu definieren.  [Disconnect][|::ref3::|Main] verwaltet auch eine Liste mit dem Namen [entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson] , die Gruppen von URLs definiert, die der gleichen übergeordneten Organisation/Firma gehören.  Das Feature zur nach Verfolgungs Verhinderung in Microsoft Edge verwendet diese Liste sowohl in der Vermeidung von Organisations [Beziehungen](#org-relationship-mitigation) als auch in der Vermeidung von Organisations [Engagements](#org-engagement-mitigation) , um das Auftreten von Kompatibilitätsproblemen zu minimieren, die durch nach Verfolgungs Vermeidung mit Auswirkungen auf organisationsübergreifende Anforderungen verursacht werden.  

### Vermeidung von Organisationsbeziehungen  

Mehrere beliebte Websites verwalten sowohl Websites als auch Content Delivery Networks \ (CDNs \), um statische Ressourcen und Inhalte für diese Websites bereitzustellen.  Um sicherzustellen, dass diese Arten von Szenarien nicht von der nach Verfolgungs Verhinderung betroffen sind, behebt Microsoft Edge eine Website von der nach Verfolgungs Verhinderung, wenn die Website Drittanbieter Anforderungen an andere Websites annimmt, die derselben übergeordneten Organisation gehören (wie in der [Liste "trennen entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson]in der Liste \" definiert).  Dies ist am besten anhand eines Beispiels zu veranschaulichen.  

> **Beispiel:**
> 
> Eine Organisation mit dem Namen Org1 besitzt die Domänen `org1.test` und `org1-cdn.test` , wie in der [Liste entities.jstrennen][GitHubDisconnectMeTrackingProtectionEntitiesJson]definiert.  Stellen Sie sich vor, dass `org1-cdn.test` es sich um einen Tracker handelt, auf den normalerweise Tracking Prevention-Erzwingungen angewendet werden.  Wenn ein Benutzer besucht `https://org1.test` und die Website versucht, eine Ressource zu laden `https://org1-cdn.test` , übernimmt Microsoft Edge keine Erzwingungs Aktionen für Anforderungen, die an vorgenommen wurden, obwohl `org1-cdn.test` es sich nicht um eine URL des ersten Anbieters handelt.  Wenn jedoch eine andere URL, die nicht Teil der Org1-Organisation ist, versucht, die gleiche Ressource zu laden, unterliegt die Anforderung jedoch der Erzwingung, da Sie nicht Teil derselben Organisation ist.  
> 
> Auch wenn dadurch die Verfolgung von Verhinderungen für Websites, die zur gleichen Organisation gehören, entspannt wird, ist es unwahrscheinlich, dass dadurch ein hoher Datenschutzrisiko eingeführt wird, da solche Organisationen `https://org1.test` auch `https://org1-cdn.test` mithilfe interner Back-End-Daten ermitteln können, auf welche Websites/Ressourcen Sie zugegriffen haben.  

### Vermeidung von org-Engagements  

Die Minderung des org-Engagements wurde erstellt, um Kompatibilitätsrisiken zu minimieren, die durch das Nachverfolgen der Prävention eingeführt wurden, indem sichergestellt wird, dass Websites, deren Besitzer Organisationen sind, die die Benutzer ausreichend engagieren, weiterhin wie erwartet im Internet funktionieren  Es nutzt das [Website-Engagement][ChromiumDesignDocsSiteEngagement] , um die erzwungene Nutzung zu entspannen, wenn ein Benutzer eine laufende Beziehung (derzeit durch ein Website-Engagement-Score von 4,1 oder höher) mit einer bestimmten Website definiert hat.  Das ist am besten durch ein Beispiel illustriert:

> **Beispiel:**
> 
> Eine Organisation mit dem Namen Social org besitzt die Domänen `social.example` und `social-videos.example` .
> 
> Benutzer werden als eine Beziehung mit Social org angesehen, wenn Sie eine Website-Engagement-Punktzahl von 4,1 oder höher mit einem der Domänen, die im Besitz von Social org sind, eingerichtet haben.
> 
> Wenn es sich bei einer anderen Website um `https://content-embedder.example` Inhalte von Drittanbietern handelt (sagen Sie ein eingebettetes Video von `social-videos.example` \) aus einer der Domänen, die im Besitz von Social org sind, die normalerweise durch Nachverfolgung von Vorbeugungsmaßnahmen eingeschränkt werden, ist die Website von der Verfolgung von Präventionsmaßnahmen ausgenommen, solange der Standort Einsatzfaktor des Benutzers mit Domänen, die im Besitz von Social org sind,
> 
> Wenn eine Website nicht zu einer Organisation gehört, muss ein Benutzer eine Website-Engagement-Punktzahl von 4,1 oder höher einrichten, bevor alle Speicherzugriffs-/Ressourcen Auslastungs Blöcke, die durch nach Verfolgungs Verhinderung auferlegt werden, gelockert werden.

Die Minderung des org-Engagements wird derzeit nur im Modus "ausgeglichen" angewendet, damit Microsoft Edge den größtmöglichen Schutz für Benutzer bietet, die sich für Strict entschieden haben.

### Die CompatExceptions-Liste  

Basierend auf dem kürzlich von Microsoft empfangenen Feedback von Benutzern, verwaltet Microsoft Edge eine kleine Liste von Websites \ (die meisten von Ihnen sind in der Kategorie "Inhalt trennen" \), die aufgrund von nach Verfolgungs Verhinderung unterbrechen, obwohl die beiden oben genannten Abschwächungen vorhanden sind. Websites in dieser Liste sind von der Nachverfolgung von Präventions Erzwingungen ausgenommen.  Die Liste befindet sich auf der Festplatte an den unten beschriebenen [Speicherorten](#determining-whetherhow-a-particular-url-is-classified) .  Benutzer können Einträge mit der Option **blockieren** in überschreiben `edge://settings/content/cookies` .

Um zu verhindern, dass diese Liste weitergeleitet wird, arbeitet Microsoft derzeit an der [Speicherzugriffs-API][GitHubMsExplainersStorageAccessApi] in der Chrom-CodeBase.  Die [Speicherzugriffs-API][GitHubMsExplainersStorageAccessApi] bietet Websiteentwicklern eine Möglichkeit, den Speicherzugriff von Benutzern direkt anzufordern, wodurch die Benutzer mehr Transparenz darüber erhalten, wie Ihre Datenschutzeinstellungen ihre Browserumgebung beeinflussen, und es den Websiteentwicklern ermöglicht, sich schnell und intuitiv zu entsperren.

Nachdem die [Speicherzugriffs-API][GitHubMsExplainersStorageAccessApi] implementiert wurde, wird die CompatExceptions-Liste von Microsoft als veraltet markiert, und die betroffenen Websites greifen auf die betreffenden Websites zu, um Sie auf die Probleme aufmerksam zu machen, und um zu beantragen, dass Sie die [Speicherzugriffs-API][GitHubMsExplainersStorageAccessApi] verwenden, die weitergeleitet wird.  

## Verhalten zur Verhinderung der aktuellen Nachverfolgung  

In der folgenden Tabelle sind die Erzwingungs Aktionen und-Abschwächungen aufgeführt, die auf die einzelnen Kategorien von klassifizierten Tracker in Microsoft Edge angewendet werden.  

*   Im oberen Bereich sind die Kategorien der Tracker aufgeführt, die durch die [Kategorien "Nachverfolgung der Schutzliste trennen][GitHubDisconnectTrackingProtectionCategories]" definiert sind.  
*   Auf der linken Seite befinden sich die drei Ebenen der nach Verfolgungs Verhinderung in Microsoft Edge \ (Basic, Balanced und Strict \).  
*   Der Buchstabe `S` gibt an, dass der Speicherzugriff blockiert ist.  
*   Der Buchstabe `B` gibt an, dass sowohl der Speicherzugriff als auch die Ressourcenauslastung \ (wie Netzwerkanforderungen \) blockiert sind.  
*   Ein Bindestrich \ ( `-` \) gibt an, dass kein Block auf Speicherzugriff oder Ressourcen Lasten angewendet wird.  

| | Werbe | Analysen | Inhalt | Cryptomining | Fingerprinting | Soziale Netzwerke | Other | Gleiche Minderung der Organisation | Vermeidung von org-Engagements |  
| - | - | - | - | - | - | - | - | - | - | - |  
| **Einfach** | - | - | - | B | B | - | - | Aktiviert | n.a. |  
| **Ausgeglichen** | E | - | E | B | B | E | E | Aktiviert | Aktiviert |  
| **Streng** | B | B | E | B | B | B | B | Aktiviert | Deaktiviert |  

> [!NOTE]
> Die Minderung des org-Engagements gilt nicht für die Cryptomining-oder Fingerabdruck Kategorien.  

> [!TIP]
> Der Strict-Modus blockiert mehr Ressourcen Lasten als ausgeglichen.  Die Blockierung von mehr Ressourcen Lasten kann dazu führen, dass der strikte Modus angezeigt wird, um weniger nachverfolgungsanforderungen als ausgeglichen zu blockieren, da die Tracker, die die Anforderungen vornehmen, nie geladen werden.  

> [!NOTE]
> Die Spalte "Fingerabdruck" im [aktuellen Tracking-Verhinderung-Verhalten](#current-tracking-prevention-behavior) bezieht sich auf Tracker, die sich neben einer anderen Liste in der Liste der Fingerabdrücke befinden.  Tracker, die nur auf der Liste der Fingerabdrücke angezeigt werden, gelten als nicht-böswillige Fingerabdrücke und werden nicht blockiert.

### InPrivate-Verhalten  

In Microsoft Edge 79 war das Standardverhalten die Anwendung des Strict-Modus-Schutzes in InPrivate.  In Microsoft Edge 80 wurde dieses Verhalten durch einen Schalter ersetzt, in `edge://settings/privacy` dem Benutzer entscheiden können, ob Sie den strikten modusschutz anwenden oder Ihre normalen Einstellungen beim Durchsuchen von InPrivate beibehalten möchten.  

## Ermitteln, ob/wie eine bestimmte URL klassifiziert wird  

Die einfachste Methode, um festzustellen, ob eine bestimmte URL als bekannter Tracker klassifiziert wird, besteht darin, die folgenden Schritte auszuführen.  

1.  Öffnen Sie devtools, und navigieren Sie zur Registerkarte Konsole.  
1.  Laden Sie die Seite neu.  
    1.  Möglicherweise möchten Sie **Cookies und andere Website Daten** zuerst löschen, um die Ergebnisse der Website Einsätze zurückzusetzen und einen völlig sauberen Schiefer zu gewährleisten.  
1.  Suchen Sie nach Nachrichten, die gelesen werden `Tracking Prevention blocked access to storage for <URL>` .  
    1.  Sie können die Nachrichten erweitern, um die einzelnen URLs anzuzeigen, die blockiert wurden.  
1.  Wenn Sie feststellen möchten, in welcher Kategorie sich eine bestimmte blockierte Website befindet, ist es am einfachsten, wenn Sie in der [Liste services.jstrennen in auf][GitHubDisconnectTrackingProtectionCategories]suchen.  Da die Einträge alphabetisch sortiert sind, können Sie durch Scrollen an den Anfang eines Blocks von Website Einträgen die spezifische Kategorie für eine bestimmte Website finden.  

> [!TIP]
> Wenn Sie auf die auf dem Datenträger gespeicherten Tracking Prevention-Listen zugreifen müssen, befinden sich die einzelnen Speicherorte an einem von zwei Speicherorten.  
>
> **Komponentenbasierte Updates** – die Listen, die aus der Komponente "Trust Protection lists" heruntergeladen werden  
>
> Fenster: `%LOCALAPPDATA%\Microsoft\Edge <OptionalChannelName>\User Data\Trust Protection Lists`  
>
> macOS `~/Library/Application Support/Microsoft Edge <OptionalChannelName>/Trust Protection Lists`  
>
> **Installationsverzeichnis** – die Listen, die mit dem Microsoft Edge-Installationsprogramm gebündelt sind.  Wenn Sie ein anderes Installationsverzeichnis ausgewählt haben, können die genauen Pfade unterschiedlich sein.  
>
> Fenster: `%PROGRAMFILES(x86)%\Microsoft\ Edge <OptionalChannelName>\Application<Version>\Trust Protection Lists`  
>
> macOS `/Applications/Microsoft Edge.app/Contents/Frameworks/Microsoft Edge Framework.framework/Libraries/Trust Protection Lists`  

## Häufig gestellte Fragen  

Der folgende Abschnitt enthält Antworten auf häufig gestellte Fragen zum Feature zur nach Verfolgungs Prävention in Microsoft Edge.  

**Gibt es eine Möglichkeit zum Blockieren oder Zulassen bestimmter Tracker für Debugging-Zwecke?**  

Derzeit macht Microsoft Edge nur eine Option verfügbar, mit der Sie die Verfolgungs Verhinderung für die Ausführung auf einer bestimmten Website deaktivieren können.  Auf diese Option wird über das Seiten Info-Flyout oder über die `edge://settings/privacy/trackingPreventionExceptions` Seite zugegriffen.  

Allerdings können die Optionen **blockieren** und **zulassen** auf der `edge://settings/content/cookies` Seite verwendet werden, um bestimmte Domänenzugriff auf Speicher wie Cookies und andere Browser Speichermechanismen zuzulassen oder zu verweigern.  Dies ist hilfreich für das Debuggen von Websiteproblemen, die durch Nachverfolgung von Verhinderung erzwungen werden, die den Zugriff auf den Speicher für eine bestimmte Website blockieren.  

<!-- image links -->  

[ImageThreeSettingsTrackingPrevention]: ./media/tracking-prevention-settings.png  
[ImageBlockedTrackersPageInfoFlyout]: ./media/page-info-flyout.png  

<!-- links -->  

[MicrosoftEdgeBrowserPrivacyPromise]: https://microsoftedgewelcome.microsoft.com/privacy "Datenschutz – Microsoft Edge"  

[ChromiumDesignDocsSiteEngagement]: https://www.chromium.org/developers/design-documents/site-engagement "Website-Engagement – die Chrom-Projekte"  

[DisconnectMain]: https://disconnect.me "Trennen"  

[GitHubDisconnectMeTrackingProtection]: https://github.com/disconnectme/disconnect-tracking-protection "disconnectme/Disconnect-Tracking-Schutz | GitHub"  
[GitHubDisconnectTrackingProtectionCategories]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/services.json "services.json-disconnectme/Disconnect-Tracking-Protection | GitHub"  
[GitHubDisconnectMeTrackingProtectionEntitiesJson]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/entities.json "entities.json-disconnectme/Disconnect-Tracking-Protection | GitHub"  

[GitHubMsExplainersStorageAccessApi]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/StorageAccessAPI/explainer.md "Erläuterung der Speicherzugriffs-API-MSEdgeExplainers/StorageAccessAPI | GitHub"
