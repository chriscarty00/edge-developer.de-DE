---
description: Schrittweiser Prozess zum Veröffentlichen von Edge (Chrom)-Erweiterungen für Microsoft Store.
title: Veröffentlichen einer Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 7b5be511af1e81efd5da4fc4bc0691f317437f94
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607378"
---
# Veröffentlichen einer Erweiterung  

Veröffentlichen Sie Ihre Erweiterung auf dem Microsoft Edge Addons-Katalog \ (Microsoft Edge Addons \).  Sie müssen zuerst eine Übermittlung im [Partner Center][MicrosoftPartnerCenter] erstellen und diese übermitteln.  In diesem Dokument sind alle Details aufgeführt, die Sie zum Erstellen einer Verlängerungs Übermittlung angeben müssen.  

## Vorbereitung  

*   Sie müssen über ein aktives Entwicklerkonto im [Partner Center][MicrosoftPartnerCenter] verfügen, um Ihre Erweiterung in Microsoft Edge-Add-ons einreichen zu können.  Wenn Sie noch keine haben, [Erstellen Sie ein neues Entwicklerkonto][MicrosoftPartnerCenter].  
*   Erstellen Sie eine ZIP-Datei Ihres Erweiterungspakets, und stellen Sie sicher, dass Sie diese Dateien enthält:  
    *   Die Manifestdatei, und die Datei muss den Namen und die Version der Erweiterung definieren.  
    *   Die Bilder und andere Dateien, die für Ihre Erweiterung erforderlich sind.  


Wenn Sie noch nicht mit dem Erstellen einer Erweiterung begonnen haben, können Sie das Lernprogramm " [Erste Schritte][ExtensionsGettingStarted] " zum Erstellen einer Microsoft Edge Chrom-Erweiterung finden.  

Führen Sie die folgenden Schritte aus, um eine Erweiterungs Übermittlung im [Partner Center][MicrosoftPartnerCenter]zu erstellen.  

## Schritt 1: Starten einer neuen Übermittlung  

Wechseln Sie zu Ihrem [entwicklerdashboard][MicrosoftPartnerCenter].  Klicken Sie auf der Seite Übersicht auf **neue Erweiterung erstellen**.  

## Schritt 2: Hochladen Ihrer ZIP-Erweiterungsdatei  

Auf der **Paket** Seite laden Sie die ZIP-Datei für Ihre Erweiterungs Übermittlung hoch.  Sie können nur ein Paket gleichzeitig hochladen, wenn Ihre Erweiterung nicht abgeschlossen ist, können Sie ein work-in-Progress-Paket hochladen und es jederzeit aktualisieren, bevor Sie es veröffentlichen.  Stellen Sie sicher, dass Ihr Paket die `manifest.json` Datei enthält und auf Microsoft Edge vor dem Hochladen einwandfrei funktioniert.  
Laden Sie das Paket hoch, indem Sie es in das Feld Upload ziehen, oder indem Sie **Dateien durchsuchen**auswählen.  Auf der Seite "Paket" wird die ZIP-Datei für Erweiterungen überprüft, und **der Status für den Erfolg oder Fehler des Uploads**wird angezeigt.  Wenn das Paket die Validierung übergibt; Sie wird erfolgreich hochgeladen, und es wird eine Erfolgsmeldung angezeigt.  Wenn die Validierung des Pakets fehlschlägt; das Paket wird nicht akzeptiert, und es wird eine Fehlermeldung angezeigt.  Wenn das Paketfehler enthält, beheben Sie die Probleme, und versuchen Sie, es erneut zu hochladen.  

Überprüfen Sie nach dem erfolgreichen hochladen Ihre Erweiterungs Details, und klicken Sie auf **weiter** , um fortzufahren.  

## Schritt 3: Bereitstellen von Verfügbarkeits Details  

### Definieren der Sichtbarkeit  

Wählen Sie eine **Sichtbarkeits** Option aus, um die Zielgruppe zu definieren, die ihre Erweiterung entdecken und erwerben kann.  Auf diese Weise können Sie angeben, ob Benutzer ihre Erweiterung in Microsoft Edge-Addons finden oder den Eintrag überhaupt sehen sollen.  Derzeit gibt es zwei Optionen unter Sichtbarkeit:  

*   `Public`  
    Dies ist die Standardoption.  
    Wenn Sie auswählen `Public` , ist Ihre Erweiterung verfügbar und für alle Benutzer in Microsoft Edge-Add-ons sichtbar.  Lassen Sie diese Option aktiviert, wenn Sie möchten, dass Ihre Erweiterung in Microsoft Edge-Addons aufgelistet wird, die Benutzer über suchen, durchsuchen und den direkten Link ihrer Erweiterung finden können.  

*   `Hidden`  
    Wenn Sie auswählen `Hidden` , wird Ihre Erweiterung in Microsoft Edge-Addons von Benutzern, die suchen oder durchsuchen, ausgeblendet, und Sie müssen ihre Eintrags-URL freigeben, um Ihre Erweiterung zu verteilen.  Benutzer, die über den direkten Link zum Eintrag verfügen, können Sie auf Microsoft Edge herunterladen (möglicherweise finden Sie die URL Ihres Eintrags **unter der Erweiterungs** Übersichtsseite von Extension Submission \).  

> [!NOTE]
> Wenn Sie eine Erweiterung als **öffentlich** übermitteln und Sie später in " **Privat**" ändern, haben Benutzer, die die Erweiterung installiert haben, weiterhin Zugriff und erhalten zukünftige Updates.  

### Definieren von Märkten  

Sie müssen die spezifischen Märkte definieren, in denen Sie Ihre Durchwahl anbieten, indem Sie auf der Seite " **Verfügbarkeit** " im Abschnitt **Märkte** die Option **Optionen anzeigen** auswählen.  Das Popupfenster Marktauswahl wird angezeigt, in dem Sie die Märkte auswählen sollten.  Standardmäßig werden alle Märkte ausgewählt, einschließlich aller **zukünftigen Märkte** , die später hinzugefügt werden können.  Sie können einzelne Märkte deaktivieren, um Sie auszuschließen, oder Sie können auf **Alle auswählen** klicken und dann einzelne Märkte Ihrer Wahl hinzufügen.  

> [!NOTE]
> Wenn Benutzer ihre Erweiterung bereits in einem bestimmten Markt haben und Sie diesen Markt später entfernen, können Benutzer, die bereits über die Erweiterung in diesem Markt verfügen, diese weiterhin verwenden, aber Sie erhalten keine späteren Updates, die Sie übermitteln.  

Klicken Sie auf **Speichern** , um zum Abschnitt **Eigenschaften** zu gelangen.  

## Schritt 4: Auswählen von Eigenschaften für Ihre Erweiterung  

### Erweiterungseigenschaften  

*   [Kategorie](#category)  
*   [Datenschutzrichtlinien Anforderungen](#privacy-policy-requirements)  
*   [URL zu den Datenschutzrichtlinien](#privacy-policy-url)  
*   [Website-URL](#website-url)  
*   [Support-URL/e-Mail-Adresse](#support-urlemail-address)  
*   [Durchwahl](#extension-rating)  

#### Kategorie  

Wenn Sie Ihre Erweiterung in der richtigen Kategorie auflisten, können Benutzer ihre Erweiterung problemlos finden und mehr darüber erfahren.  Wählen Sie eine Kategorie aus, die ihre Erweiterung am besten beschreibt.  

**Mögliche Werte**:  

*   `Accessibility`  
*   `Blogging`  
*   `Developer Tools`  
*   `Fun`  
*   `News & Weather`  
*   `Photos`  
*   `Productivity`  
*   `Search Tools`  
*   `Shopping`  
*   `Social & Communication`  
*   `Sports`  

#### Datenschutzrichtlinien Anforderungen  

Geben Sie an, ob Ihre Durchwahl personenbezogene Informationen zugreift, sammelt oder überträgt.  

> [!NOTE]
> Wenn für Ihre Erweiterung eine Datenschutzrichtlinie erforderlich ist und Sie diese nicht angegeben haben, kann es vorkommen, dass ihre Übermittlung eine Zertifizierung ausfällt.  

**Mögliche Werte**:  

*   `No`: Eine Datenschutzrichtlinien-URL ist optional.  
*   `Yes`: Eine Datenschutzrichtlinien-URL ist erforderlich.  

#### URL zu den Datenschutzrichtlinien  

Sie sind dafür verantwortlich, sicherzustellen, dass Ihre Erweiterung den Datenschutzbestimmungen und-Vorschriften entspricht, und für die Bereitstellung einer gültigen Datenschutzrichtlinien-URL, falls erforderlich.  Sie müssen eine URL für Datenschutzrichtlinien angeben, wenn Ihre Durchwahl auf persönliche Informationen zugreifen, diese übertragen oder von ihr erfasst wird.  
Wenn Sie feststellen möchten, ob Ihre Erweiterung eine Datenschutzrichtlinie erfordert, lesen Sie die [Microsoft Edge-Entwickler Vereinbarung][MicrosoftAppDeveloperAgreement] und das [Microsoft Edge Addons-Katalog-Entwicklerrichtlinien Dokument][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Mögliche Werte**:  

*   `{url}`  

#### Website-URL  

Diese Eigenschaft ist optional.  
Die URL der Webseite für Ihre Erweiterung.  Diese URL muss auf eine Seite auf Ihrer eigenen Website verweisen, nicht auf den Webeintrag für Ihre Erweiterung in Microsoft Edge-addons.  

**Mögliche Werte**:  

*   `{url}`  

#### Support-URL/e-Mail-Adresse  

Diese Eigenschaft ist optional.  
Die URL der Webseite, auf der Benutzer Unterstützung für Ihre Durchwahl erhalten, oder eine e-Mail-Adresse, die Sie zur Unterstützung kontaktieren können.  Sie enthalten Supportinformationen für alle Übermittlungen, damit Ihre Benutzer wissen, wie Sie Support von Ihnen erhalten.  

**Mögliche Werte**:  

*   `{email_address}`  
*   `{url}`  

#### Durchwahl  

Die Durchwahl Bewertung hilft uns, das Alter der Zielgruppe Ihrer Erweiterung festzulegen.  
Wenn Sie feststellen möchten, ob Ihre Erweiterungen über einen ausgereiften Inhalt verfügen, lesen Sie das [Dokument Microsoft Edge Addons-Katalog-Entwicklerrichtlinien][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Mögliche Werte**:  

*   Ausgereift \ (CheckBox \): Aktivieren Sie dieses Kontrollkästchen, wenn Ihre Erweiterung ausgereifte Inhalte enthält.  Wenn Sie für Ihre Erweiterung ausgereift auswählen, steht Ihr Eintrag mit einem separaten Tag zur Verfügung, um anzugeben, dass die Erweiterung ausgereifte Inhalte enthält.  

Klicken Sie auf **Speichern** , um den Abschnitt mit der Auflistung fortzusetzen.  

## Schritt 5: Hinzufügen von Eintrags Informationen für Ihre Erweiterung  

Dies sind die Informationen, die Benutzern angezeigt werden, wenn Sie Ihren Eintrag in Microsoft Edge Addons anzeigen.  Viele der Felder in einem Eintrag sind optional, aber wir empfehlen, so viele Informationen wie möglich bereitzustellen, damit Ihr Eintrag hervorgehoben wird.  Das für Ihren Eintrag in Microsoft Edge Addons erforderliche Mindestgebot ist die [Textbeschreibung](#description), das [Erweiterungs Logo](#store-logo)und die [kleine Werbe Kachel](#small-promotional-tile) in jeder Sprache, die in Ihrem Erweiterungspaket erwähnt wird.  

### Store-Eintragsfelder  

*   [Sprachen für Store-Einträge](#store-listing-languages)  
*   [Store-Anzeigename](#store-display-name)  
*   [Beschreibung](#description)  
*   [Store-Logo](#store-logo)  
*   [Kleine Werbe Kachel](#small-promotional-tile)  
*   [Medien](#media)  
*   [Kurze Beschreibung](#short-description)  
*   [Suchbegriffe](#search-terms)  

#### Sprachen für Store-Einträge  

Wenn Ihr Erweiterungspaket mehrere Sprachen unterstützt, muss Ihre Erweiterung über eine Eintragsseite für jede andere Sprache verfügen.  
Sie müssen die Eintragsdetails \ (Textbeschreibung, Bilder usw.) für jede Sprache separat ausfüllen, auch wenn Sie für jede Sprache denselben Inhalt verwenden.  Wenn Ihre Erweiterung in mehr als einer Sprache lokalisiert ist, werden diese Sprachen oben auf der Eintragsseite angezeigt.  

1.  Wählen **Sie in der Dropdownliste Sprache einen** beliebigen Sprachnamen aus.  
1.  Füllen Sie die Eintragsdetails aus.  
1.  Klicken Sie auf **Speichern**.  
1.  Wiederholen Sie diese Schritte für alle unterstützten Sprachen.  

> [!NOTE]
> Wenn Sie Sprachen für Ihren Eintrag in Microsoft Edge Addons hinzufügen oder entfernen möchten, müssen Sie die Liste der von Ihrem Erweiterungspaket unterstützten Sprachen ändern und erneut hochladen.  

**Mögliche Werte**:  

*   `English (United States)`: Dies ist der Standardwert.  Wenn Sie in Ihrem Paket keine Sprache erwähnen, wird Ihre Standardsprache auf Englisch (USA \) festgesetzt, und Sie müssen einen Eintrag in Englisch (USA) angeben.  
*   `{language}` \(`{Country}`\)  

#### Store-Anzeigename  

Der Name der Erweiterung, wie in Ihrem Erweiterungspaket Manifest erwähnt.  

> [!NOTE]
> Wenn Sie den Namen bearbeiten möchten, müssen Sie das Manifest in Ihrem Erweiterungspaket aktualisieren und erneut hochladen.  

#### Beschreibung  

Dieses Feld ist erforderlich.  
Die Beschreibung für Ihre Benutzer, wie Ihre Erweiterung funktioniert.  

**Mögliche Werte**:  

*   {plain_text}: weniger als 10.000 Zeichen.  

#### Store-Logo  

Dieses Feld ist erforderlich.  
Ein 1:1-Bild für Ihr Erweiterungs Logo.  

**Mögliche Werte**:  

*   128px x 128px, PNG \ (. png \)  
*   150px x 140px, PNG \ (. png \)  
*   300px x 300px, PNG \ (. png \): die empfohlene Größe.  

#### Kleine Werbe Kachel  

Dieses Feld ist erforderlich.  
Eine Werbe Kachel für kleine Größen.  Ihr Eintrag wird auf dieser Kachel angezeigt.  

**Mögliche Werte**:  

*   440px x 280x, PNG \ (. png \)  

#### Medien  

Dieses Feld ist optional.  
Sie sollten diese Ressourcen bereitstellen, um Ihr Produkt effektiver anzeigen zu können.  

*   Screenshots  
    Die Bilder ihrer Erweiterung, die beschreiben, was Ihre Erweiterung tut.  
    
*   Große Werbe Kacheln  
    Eine große Werbe Kachel, mit der Ihre Erweiterung in Microsoft Edge Addons deutlicher hervorgeht.  
    
*   YouTube-Video-URL  
    Eine gültige [YouTube-Video-URL für Ihre Erweiterung][MicrosoftEdgeAddonsUploadYouTubeVideo].  Ihr Video sollte eine gute Qualität und eine minimale Länge aufweisen.  Ihr YouTube-Video muss eine Zertifizierung bestehen, bevor Sie Ihre Erweiterung in Microsoft Edge-Addons veröffentlichen.  Überprüfen Sie, ob Ihr YouTube-Video dem [Microsoft Edge Addons-Katalog für Entwicklerrichtlinien][MicrosoftEdgeAddonsCatalogDeveloperPolicies]entspricht.  

**Mögliche Werte**:  

*   maximal 10 Screenshots.  
    *   640px x 480px, PNG \ (. png \): Screenshots.  
    *   1280px x 800px, PNG \ (. png \): Screenshots.  
*   1400px x 560px, PNG \ (. png \): große Werbe Kacheln.  
*   60 Sekunden oder kürzer und 2GB oder kleiner, YouTube-Video-URL.  

#### Kurze Beschreibung  

Eine kurze, einprägsame Beschreibung, die am Anfang des Eintrags für Ihr Produkt verwendet werden kann.  Wenn Sie nicht bereitgestellt werden, werden stattdessen die ersten Zeilen aus der längeren Beschreibung verwendet.  Da Ihre Beschreibung auch unter diesem Text angezeigt wird, sollten Sie eine kurze Beschreibung mit unterschiedlichem Text angeben, damit Ihr Eintrag weniger repetitiv ist.  Die kurze Beschreibung ihrer Erweiterung wird direkt aus der Manifestdatei Ihres Pakets ausgewählt.  

> [!NOTE]
> Um die Kurzbeschreibung zu bearbeiten, müssen Sie das Manifest in Ihrem Erweiterungspaket aktualisieren und es erneut hochladen.  

#### Suchbegriffe  

Suchbegriffe sind einzelne Wörter oder kurze Ausdrücke, die nicht für Benutzer angezeigt werden, aber dazu beitragen, dass Ihre Erweiterung in Microsoft Edge-Add-ons auffindbar ist, wenn Benutzer mithilfe dieser Begriffe suchen.  

**Anforderungen**:  

*   7 oder weniger Suchbegriffe  
*   30 oder weniger Zeichen pro Suchbegriff  
*   21 oder weniger Wörter für kombinierte Suchbegriffe  

Klicken Sie auf **Speichern** , um den Abschnitt zum Speichern Ihres Eintrags fortzusetzen.  Klicken Sie auf **veröffentlichen** , um Übermittlungsdetails bereitzustellen.  

## Schritt 6: Abschließen der Übermittlung und klicken auf "veröffentlichen"  

Auf der Seite "Übermittlungsoptionen" des Übermittlungsprozesses für die Erweiterung finden Sie weitere Informationen, die uns helfen, Ihr Produkt ordnungsgemäß zu testen.  Dieser Schritt ist optional, wird aber für viele Übermittlungen empfohlen.  

### Optionen zum Anhalten der Veröffentlichung  

Standardmäßig wird ihre Übermittlung veröffentlicht, sobald Sie die Zertifizierung absolviert hat.  Sie haben die Möglichkeit, die Veröffentlichung ihrer Übermittlung bis zu einem bestimmten Datum zu sperren.  Die Optionen in diesem Abschnitt werden im Anschluss beschrieben.  

*   **Veröffentlichen Ihrer Übermittlung, sobald Sie die Zertifizierung absolviert hat**  

    Dies ist die Standardauswahl.  Das bedeutet, dass ihre Übermittlung den Veröffentlichungsprozess beginnt, sobald die Zertifizierung erfolgreich ist.  

*   **Starten Sie die Veröffentlichung der Übermittlung an einem bestimmten Datum**  

    Wählen Sie **Start Veröffentlichung ihrer Übermittlung an einem bestimmten Datum** aus, um sicherzustellen, dass die Übermittlung erst an einem bestimmten Datum veröffentlicht wird.  Mit dieser Option wird ihre Übermittlung so schnell wie möglich am oder nach dem von Ihnen angegebenen Datum veröffentlicht.  Das Datum muss mindestens 24Stunden in der Zukunft liegen.  Zusammen mit dem Datum können Sie die Uhrzeit angeben, zu der die Übermittlung der Veröffentlichung beginnen soll.  

### Hinweise zur Zertifizierung  

Wenn Sie Ihre Erweiterung übermitteln, haben Sie die Möglichkeit, die Seite Hinweise für die Zertifizierung zu verwenden, um den Zertifizierungs Prüfern zusätzliche Informationen zur Verfügung zu stellen.  Mithilfe dieser Informationen können Sie sicherstellen, dass Ihre Erweiterung richtig getestet wird.  Wenn wir ihre Übermittlung nicht vollständig testen können, kann dies zu einer Zertifizierung führen.  

Stellen Sie sicher, dass Sie die folgenden \ (falls zutreffend für Ihre Erweiterung \) einbeziehen:  

*   Benutzernamen und Kennwörter für Testkonten.  
*   Schritte für den Zugriff auf ausgeblendete oder gesperrte Features  
*   Erwartete Unterschiede im Verhalten auf der Grundlage der Region oder anderer Benutzereinstellungen.  
*   Informationen dazu, was in einem App-Update geändert wurde.  
*   Alles, was Sie von den Testern für ihre Übermittlung wissen müssen.  

Klicken Sie nach Abschluss der obigen Informationen auf **veröffentlichen** , um Ihre Erweiterung in Microsoft Edge-Addons einzureichen.  

Wenn Sie mit dem Erstellen der Übermittlung für Ihre Erweiterung fertig sind und auf **veröffentlichen**klicken, tritt die Übermittlung in den Zertifizierungs Schritt ein.  Dieser Vorgang ist in der Regel innerhalb von ein paar Tagen abgeschlossen, in manchen Fällen kann es jedoch bis zu 7 Arbeitstage dauern.  Nachdem ihre Übermittlung die Zertifizierung erfolgreich durchlaufen hat, wird Ihre Erweiterung in Microsoft Edge Addons veröffentlicht, es sei denn, Sie haben die Optionen für den Veröffentlichungs Speicher ausgewählt, um anzugeben, dass Sie bis zu einem bestimmten Datum nicht freigegeben werden soll.  Sie werden benachrichtigt, wenn ihre Übermittlung veröffentlicht wird, und der Status Ihrer Erweiterung im Dashboard wird in geändert `In the Store` .  

<!-- image links -->  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Erste Schritte mit Microsoft Edge \ (Chrom \)-Erweiterungen | Microsoft docs"  

[MicrosoftEdgeAddonsUploadYouTubeVideo]: ./upload-video.md "Hochladen eines YouTube-Videos | Microsoft docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Microsoft Edge Addons-Katalog-Entwicklerrichtlinien | Microsoft docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Vereinbarung für App-Entwickler | Microsoft docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
