---
description: Veröffentlichen von Microsoft Edge (Chromium)-Erweiterungen im Microsoft Edge-Add-Ons Store
title: Veröffentlichen Sie die Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: b03a74d1faef914298729020e3c9ca4d465e0443
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327677"
---
# Veröffentlichen Sie die Erweiterung  

Nachdem Sie Ihre Erweiterung entwickelt und testen, können Sie Ihre Erweiterung verteilen. Verwenden Sie den Microsoft Edge-Add-Ons-Katalog, um Ihre Erweiterung zu verteilen.  Um Ihre vorhandene Chromium-Erweiterung für Microsoft Edge-Benutzer frei zu geben, navigieren Sie [zum Port ihrer vorhandenen Chromium-Erweiterung.][PortChromiumExtension]  

Veröffentlichen Sie Ihre Erweiterung im Microsoft Edge-Add-Ons-Katalog, um die Reichweite zu erhöhen und sie Benutzern von Microsoft Edge zur Verfügung zu stellen.  In diesem Artikel wird beschrieben, wie Sie Ihre Erweiterung an den Microsoft Edge-Add-Ons-Katalog übermitteln.  

## Vorbemerkungen  

Sie sollten einen funktionierenden Prototyp Ihrer Erweiterung bereit haben.  Informationen zum Erstellen einer Erweiterung finden Sie im Lernprogramm ["Erste Schritte".][ExtensionsGettingStarted]  

Um Ihre Erweiterung im Microsoft Edge-Add-Ons-Katalog zu veröffentlichen, verwenden Sie Ihr aktives Entwicklerkonto [im Partner Center.][MicrosoftPartnerCenter]  Wenn Sie kein Entwicklerkonto haben, erstellen Sie ein neues Entwicklerkonto.  Um ein neues Entwicklerkonto zu öffnen und sich beim Microsoft Edge-Add-Ons-Programm zu registrieren, navigieren Sie zur [Entwicklerregistrierung.][DeveloperRegistration]  

Erstellen Sie eine ZIP-Datei, die Ihr Erweiterungspaket darstellt.  Das Erweiterungspaket muss die folgenden Dateien enthalten.  

*   Das Erweiterungsmanifest, in dem Details wie der Name der Erweiterung, eine kurze Beschreibung, Berechtigungen und die Standardsprache angegeben werden.  
*   Bilder und andere Dateien, die für Ihre Erweiterung erforderlich sind.  

Die folgenden Felder im Manifest werden automatisch in ihre Details zum Storeeintrag aufgenommen.  Die Felder sind auf der Seite mit den **Store-Einträgen schreibgeschützt.**  Die Seite mit den Store-Einträgen wird weiter unten in diesem Artikel beschrieben.  Stellen Sie sicher, dass die Feldwerte Ihrer bevorzugten Anzeige auf der Seite mit den Store-Details entsprechen, bevor Sie Ihr Paket in Partner Center hochladen.  Ein Beispiel für den für die Manifestdatei erforderlichen Code erhalten Sie in den Grundlagen der Manifestdatei.  

*   `Name` in der Manifestdatei, bei der es sich um den **Anzeigenamen** auf der Seite mit den Speicherdetails handelt.  
*   `Description` feld in der Manifestdatei, die die **Kurzbeschreibung auf** der Seite mit den Storedetails ist.  Geben Sie eine kurze, eingängige Beschreibung an, die am Anfang des Eintrags für Ihre Erweiterung angezeigt wird.  Wenn enthalten, wird die kurze Beschreibung, die in der Erweiterungsmanifestdatei angegeben ist, in Ihrem Storeeintrag angezeigt.  Wenn keine kurze Beschreibung in der Manifestdatei enthalten ist, werden die ersten Zeilen der Beschreibung angezeigt.  Stellen Sie eine kurze Beschreibung zur Vermeidung von Inhaltswiederholungen auf Ihrer Seite für den Store-Eintrag zur Verfügung.  

## Übermitteln Ihrer Erweiterung an den Microsoft Edge-Add-Ons-Store  

Um Ihre Erweiterung an [Partner Center zu][MicrosoftPartnerCenter]übermitteln, verwenden Sie die folgenden Schritte.  

#### Schritt 1: Starten einer neuen Übermittlung  

Navigieren Sie zum [Entwicklerdashboard,][MicrosoftPartnerCenter] und wählen Sie auf der Seite **"Übersicht"** die Option "Neue **Erweiterung erstellen"** aus.  

#### Schritt 2: Hochladen des Erweiterungspakets  

Verwenden Sie **die Seite "Pakete",** um die ZIP-Datei Ihres Erweiterungspakets hochzuladen.  Sie können immer nur ein Paket hochladen.  Sie können die Übermittlung nicht fortsetzen, wenn der Paketupload auf der Seite **"Pakete" nicht erfolgreich** war.  

Um das Paket hochzuladen, wählen Sie das Paket aus, und ziehen Sie es in das Uploadfeld. Sie können auch **"Dateien durchsuchen" auswählen.**  Nachdem das Paket hochgeladen wurde, wird das Paket überprüft.  Nachdem die Überprüfung erfolgreich war, überprüfen Sie die Erweiterungsdetails, und wählen Sie dann **"Weiter"** aus, um fortzufahren.  Wenn Überprüfungsfehler auftreten, beheben Sie die Probleme, und versuchen Sie es erneut.  

#### Schritt 3: Bereitstellen von Verfügbarkeitsdetails  

Geben Sie **auf der** Seite Verfügbarkeit die folgenden Informationen zur Verfügbarkeit Ihrer Erweiterung ein.  

##### Sichtbarkeit  

Wählen Sie eine der folgenden Sichtbarkeitsoptionen aus, um zu definieren, ob Ihre Erweiterung im Microsoft Edge-Add-Ons-Katalog sichtbar ist.  

*   `Public` \(Standard\)  
    Public ermöglicht es jedem, Ihre Erweiterung über die Suche zu entdecken, im Microsoft Edge-Add-Ons-Katalog zu browsen oder die Eintrags-URL zu Ihrer Erweiterung im Microsoft Edge-Add-Ons-Store zu verwenden.  Die Eintrags-URL ist auf Ihrem Partner Center-Dashboard auf der Seite **"Erweiterungsübersicht"** verfügbar.  
    
*   `Hidden`  
    Ausgeblendet entfernt Erweiterungen aus Suchergebnissen oder durchsucht den Microsoft Edge-Add-Ons-Katalog.  Um ausgeblendete Erweiterungen im Microsoft Edge-Add-Ons-Store zu verteilen, müssen Sie die Eintrags-URL für die Erweiterung für Ihre Kunden freigeben.  
    
> [!NOTE]
> Sie können die Sichtbarkeit Ihrer **** Erweiterung von "Öffentlich" in **"Ausgeblendet" ändern.**  Benutzer, die Ihre Erweiterung installiert haben, während die Sichtbarkeit auf öffentlich festgelegt war, behalten den Zugriff auf Ihre Erweiterung und erhalten alle Updates, die Sie über die Microsoft Edge-Add-Ons-Website zur Verfügung stellen.  

##### Märkte  

Definieren Sie die spezifischen Märkte, in denen Sie Ihre Erweiterung anbieten möchten.  Die Standardeinstellung für Märkte sind alle Märkte, die alle zukünftigen Märkte umfassen, die später hinzugefügt werden.  Um bestimmte Märkte zu wählen, wählen Sie **"Märkte ändern" aus.**  Umschalten einzelner Märkte, um die einzelnen Märkte auszuschließen, oder **wählen** Sie "Auswahl aufheben" aus, und fügen Sie dann einzelne Märkte Ihrer Wahl hinzu.  

> [!NOTE]
> Sie können die Märkte ändern, in denen Ihre Erweiterung angeboten wird.  Ein Benutzer, der Ihre Erweiterung installiert, während sie im Markt des Benutzers verfügbar ist, behält den Zugriff auf Ihre Erweiterung.  Der Benutzer hat jedoch keinen Zugriff auf zukünftige Updates, die an den Microsoft Edge-Add-Ons-Katalog übermittelt werden.  

Wählen **Sie "Speichern"** aus, um mit dem Abschnitt **"Eigenschaften" fortzufahren.**  

#### Schritt 4: Auswählen von Eigenschaften für Ihre Erweiterung  

Geben Sie **auf der Seite "Eigenschaften"** die folgenden Informationen ein, um die Eigenschaften Ihrer Erweiterung anzugeben.  Die Eigenschaften werden Benutzern im Microsoft Edge-Add-Ons-Katalog angezeigt.  

| Name der Erweiterungseigenschaft | Beschreibung |  
|:--- |:--- |  
| Kategorie \(erforderlich\) | Die Kategorie, die Ihre Erweiterung am besten beschreibt.  Wenn Sie Ihre Erweiterung in der richtigen Kategorie auflisten, können Benutzer Ihre Erweiterung leicht finden und mehr darüber erfahren.  |  
| Datenschutzrichtlinienanforderungen \(erforderlich\) | Geben Sie an, ob Ihre Erweiterung auf personenbezogene Informationen zu, diese erfasst oder überträgt.  Ihre Erweiterung besteht möglicherweise den Zertifizierungsschritt nicht, wenn Sie **"Ja"** auswählen und keine . `Privacy policy URL`  |  
| URL zu den Datenschutzrichtlinien | Eine gültige DATENSCHUTZrichtlinien-URL, um zu kommunizieren, wie Ihre Erweiterung den Datenschutzgesetzen und -bestimmungen entspricht.  Sie sind dafür verantwortlich, sicherzustellen, dass Ihre Erweiterung den Datenschutzgesetzen und -bestimmungen entspricht.  Sie sind auch für die Bereitstellung einer Datenschutzrichtlinien-URL verantwortlich, wenn von Ihrer Erweiterung auf persönliche Informationen zugegriffen, übertragen oder erfasst wird.  Um festzustellen, ob Ihre Erweiterung eine Datenschutzrichtlinie erfordert, navigieren Sie zu [Microsoft Edge Developer Agreement][MicrosoftAppDeveloperAgreement] und Microsoft Edge [Add-Ons Katalog Entwicklerrichtlinien][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  
| Website-URL | Eine Webseite, die zusätzliche Informationen zu Ihrer Erweiterung enthält.  Der muss auf eine Seite auf Ihrer eigenen Website verweisen, nicht auf den Webeintrag für Ihre Erweiterung im `Website URL` Microsoft Edge-Add-Ons-Katalog.  Dies `Website URL` hilft Benutzern, mehr über Ihre Erweiterung, deren Features und andere relevante Informationen zu erfahren.  |  
| Supportkontaktdetails | Die URL zu Ihrer Supportwebseite oder die E-Mail-Adresse, unter der Sie Ihr Supportteam kontaktieren können.  |  
| Ausgereifte Inhalte | Kontrollkästchen, um anzugeben, ob Ihre Erweiterung ausgereifte Inhalte enthält.  Die Erweiterungsbewertung hilft dabei, die geeignete Altersgruppe der Zielgruppe Ihrer Erweiterung zu ermitteln.  Um festzustellen, ob Ihre Erweiterung ausgereifte Inhalte enthält, navigieren Sie zu [Microsoft Edge-Add-Ons-Katalog-Entwicklerrichtlinien.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  |  

Wählen **Sie "Speichern"** aus, um mit dem Abschnitt **"Store-Angebote" fortzufahren.**  

> [!Important]
> Der Name Ihres Entwicklers/Ihrer Organisation, die Website-URL und die Supportkontaktdetails, die Sie während der Registrierung übermittelt haben, werden Benutzern im Microsoft Edge-Add-Ons Store angezeigt.  

#### Schritt 5: Hinzufügen von Details zum Store-Eintrag für Ihre Erweiterung  

Die im folgenden Abschnitt bereitgestellten Informationen werden Benutzern angezeigt, die Ihren Eintrag im Microsoft Edge-Add-Ons-Katalog überprüfen.  Obwohl einige Felder optional sind, sollten Sie so viele Informationen wie möglich bereitstellen.  Um Ihre Erweiterung im Store auflisten zu können, sind die folgenden Details erforderlich.  

*   **Beschreibung** für jede Sprache in Ihrem Erweiterungspaket.  
*   **Das Logo des Erweiterungsspeichers** für jede Sprache in Ihrem Erweiterungspaket.  
    
> [!NOTE]
> Die mindestens erforderlichen Details zum Storeeintrag müssen für mindestens eine der sprachen ausgefüllt werden, die im Zip-Paket für die Erweiterung erwähnt werden.  Zum Hinzufügen oder Entfernen von Sprachen in Ihrem Store-Eintrag im **** Microsoft Edge-Add-Ons-Katalog verwenden Sie die Dropdownliste "Sprache hinzufügen" auf der **Seite "Store-Einträge".**  Darüber hinaus können Sie Ihre Ressourcen aus einer Sprache über die Schaltfläche "Funktionen duplizieren" auf der Seite mit den Sprachdetails duplizieren.  

| Name der Eigenschaft "Sprachdetails" | Beschreibung |  
|:--- |:--- |  
| Anzeigename \(erforderlich\) | Die in der Manifestdatei Ihrer Erweiterung `name` angegebene Erweiterung.  Um den Anzeigenamen des Speichers nach der Übermittlung zu ändern, können Sie den Namen in der Manifestdatei aktualisieren, ein neues Erweiterungspaket erstellen und es dann erneut laden.  |  
| Beschreibung \(erforderlich\) | Der Schwerpunkt des Felds liegt auf der Erläuterung der Bedeutung Ihrer Erweiterung, der Gründe für die Installation der Erweiterung oder anderer relevanter Informationen, die `description` Benutzer kennen müssen.  Er sollte weniger als 10.000 Zeichen lang sein.  |  
| Logo des Erweiterungsspeichers \(erforderlich\) | Ein Bild, das Ihr Unternehmen oder ein Seitenverhältnis von 1 darstellt, und eine empfohlene Größe von `extension logo` 300 x 300 Pixeln.  Darüber hinaus können Sie das Objekt mithilfe der Schaltfläche "Duplizieren" aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche folgt dem Feld, nachdem Sie Ihr Logo für die Sprache hochgeladen haben.  |  
| Kleine Werbekachel \(optional\) | Das Bild wird verwendet, um Ihre Erweiterung zusammen `Small promotional tile` mit anderen Erweiterungen im Store anzeigen.  Die Größe des Bilds sollte 440 x 280 Pixel betragen.  Darüber hinaus können Sie das Objekt mithilfe der Schaltfläche "Duplizieren" aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird nach dem Feld gefunden, nachdem Sie eine Werbekachel für die Sprache hochgeladen haben.  |  
| Screenshots \(optional\) | Sie können maximal 10 Detaillierte Beschreibungen der Funktionalität `screenshots` Ihrer Erweiterung übermitteln.  Die Größe der Screenshots muss entweder 640 x 480 Pixel oder 1280 x 800 Pixel betragen.  Darüber hinaus können Sie das Objekt mithilfe der Schaltfläche "Duplizieren" aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird nach dem Feld gefunden, nachdem Sie mindestens eine für die Sprache hochgeladen haben.|  
| Große Werbekachel \(optional\) | `Large promotion tiles` werden im Store verwendet, um Erweiterungen auf der Microsoft Edge-Add-Ons-Website besser zu nutzen.  Wenn die Bilder übermittelt werden, sind sie für die Benutzer sichtbar.  Die Größe der PNG-Dateien muss 1400 x 560 Pixel betragen.  Darüber hinaus können Sie das Objekt mithilfe der Schaltfläche "Duplizieren" aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird nach dem Feld gefunden, nachdem Sie eine Werbekachel für die Sprache hochgeladen haben.  |  
| YouTube-Video-URL \(optional\) | Sie können ein Werbe-YouTube-Video Ihrer Erweiterung verwenden.  Das `YouTube video URL` Video wird auf der Seite "Store-Eintrag" Ihrer Erweiterung angezeigt.  |  
| Kurzbeschreibung \(erforderlich\) | Zum Bearbeiten des Erweiterungspakets müssen Sie das Beschreibungsfeld in der Manifestdatei des Erweiterungspakets aktualisieren und `short description` erneut laden.  |  
| Suchbegriffe \(optional\) | `Search terms` sind einzelne Wörter oder Ausdrücke, die Benutzern bei der Suche im Microsoft Edge-Add-Ons-Katalog helfen, Ihre Erweiterung zu finden.  Die Suchbegriffe werden Benutzern nicht angezeigt.  |  

##### Anforderungen an die YouTube-Video-URL  

Stellen Sie sicher, dass Ihr Video die folgenden Anforderungen erfüllt.  

*   Stellen Sie sicher, dass der Inhalt des YouTube-Videos den [Microsoft Edge-Add-Ons-Katalog-Entwicklerrichtlinien entspricht.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  
*   Deaktivieren Sie Werbung für Ihr Video.  Weitere Informationen finden Sie unter ["Festlegen Ihrer Standardanzeigeformate und][GoogleYoutubeAnswer2531367Topic7072227] [Anzeigen in eingebetteten Videos".][GoogleYoutubeAnswer132596]  
*   Aktivieren Sie die Einbettung für Ihre Videos.  Weitere Informationen finden Sie unter ["Einbetten von Videos & Wiedergabelisten".][GoogleYoutubeAnswer171780]  
    
Führen Sie die folgenden Schritte aus, um die YouTube-Video-URL Ihres Videos zu übermitteln.  

1.  Suchen Sie auf YouTube das Video, das Sie ihrer Seite mit dem Storeeintrag hinzufügen möchten.  
1.  Wählen Sie unter dem Video **"Share**  >  **Embed" aus.**  
1.  Kopieren Sie den angezeigten HTML-Code.  
1.  Fügen Sie auf der Seite mit den Details des Speichereintrags den HTML-Code in das Feld `YouTube video URL` ein.  
    
##### Suchbegriffsanforderungen  

Suchbegriffe müssen die folgenden Anforderungen erfüllen.  

*   Sie können Suchbegriffe eingeben, um maximal 21 Wörter zu verwenden.  Unabhängig davon, ob sie als einzelne Wörter, Ausdrücke oder eine Kombination aus beiden verwendet werden, sind maximal 21 Wörter zulässig.  
*   Bis zu sieben Suchbegriffe: einzelne Wörter oder Ausdrücke.  Jeder Suchbegriff hat eine Zeichenbeschränkung von 30 Zeichen.  
    
#### Schritt 6: Abschließen der Übermittlung  

Fügen Sie **auf der Seite "Ihre Erweiterung übermitteln"** Hinweise zur Zertifizierung hinzu, um die Erweiterung zu testen.  

##### Hinweise zur Zertifizierung (optional)  

Wenn Sie Ihre Erweiterung übermitteln, verwenden Sie die Seite "Hinweise für **Zertifizierung",** um den Zertifizierungstestern zusätzliche Informationen zur Verfügung zu stellen.  Die zusätzlichen Informationen stellen sicher, dass Ihre Erweiterung ordnungsgemäß getestet wird.  Wenn Ihre Erweiterung nicht vollständig getestet wurde, kann die Zertifizierung fehlschlagen.  

Stellen Sie bei Bedarf sicher, dass Sie die folgenden Informationen enthalten.  

*   Benutzernamen und Kennwörter für Testkonten.  
*   Schritte für den Zugriff auf ausgeblendete oder gesperrte Features.  
*   Erwartete Unterschiede in der Funktionalität basierend auf der Region oder anderen Benutzereinstellungen.  
*   Wenn Ihre Übermittlung eine Aktualisierung einer vorhandenen Erweiterung ist, fügen Sie Informationen zu den An der Erweiterung vorgenommenen Änderungen ein.  
*   Alle zusätzlichen Informationen, die Tester über Ihre Übermittlung verstehen müssen.  

Nachdem Sie die Informationen erhalten haben, wählen Sie **"Veröffentlichen"** aus, um Ihre Erweiterung an den Microsoft Edge-Add-Ons-Katalog zu übermitteln.  Ihre Übermittlung geht mit dem Zertifizierungsschritt fort.  Der Zertifizierungsprozess kann bis zu sieben Werktage nach der Übermittlung dauern.  

Wenn Ihre Übermittlung die Zertifizierung besteht, wird Ihre Erweiterung im Microsoft Edge-Add-Ons-Katalog veröffentlicht.  Der Status Ihrer Erweiterung im Partner Center-Dashboard ändert sich in `In the Store` .  

> [!NOTE]
> Wenn beim Übermittlungs- oder Registrierungsprozess Probleme auftreten, senden Sie ein Supportticket auf [der Erweiterungsanfrage][ExtensionsSupportForm] für neue Supportanfrage, oder senden Sie eine E-Mail an [ext_dev_support@microsoft.com][MailtoExtDevSupportMicrosoftCom].  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Erste Schritte mit Microsoft Edge-Erweiterungen (Chromium) | Microsoft Docs"  
[DeveloperRegistration]: ./create-dev-account.md "Registrieren Sie sich als Entwickler von Microsoft Edge-| Microsoft Docs"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Portierung Ihrer Chromium-Erweiterung zu Microsoft Edge | Microsoft Docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Microsoft Edge Add-Ons Catalog Developer Policies | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Vereinbarung für App-| Microsoft Docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensions New Support Request | Microsoft Support"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Festlegen der Standardanzeigeformate | Hilfe zu YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anzeigen in eingebetteten Videos | Hilfe zu YouTube"  
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Einbetten von Videos & Wiedergabelisten | Hilfe zu YouTube"  

[MailtoExtDevSupportMicrosoftCom]: mailto:ext_dev_support@microsoft.com "Senden von E-Mails ext_dev_support@microsoft.com" 
