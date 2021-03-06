---
description: Veröffentlichen von Microsoft Edge (Chromium)-Erweiterungen im Microsoft Edge-Add-Ons-Speicher
title: Veröffentlichen Sie die Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 67fdbdb39f3ef0b2b6cef2831520849933ffeeec
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399127"
---
# <a name="publish-your-extension"></a>Veröffentlichen Sie die Erweiterung  

Nachdem Sie Ihre Erweiterung entwickelt und testen, können Sie Ihre Erweiterung verteilen. Verwenden Sie den Microsoft Edge-Add-Ons-Speicher, um Ihre Erweiterung zu verteilen.  Navigieren Sie zum Port ihrer vorhandenen Chromium-Erweiterung, um Ihre vorhandene Chromium-Erweiterung für Microsoft [Edge-Benutzer frei zu geben.][PortChromiumExtension]  

Veröffentlichen Sie Ihre Erweiterung im Microsoft Edge-Add-Ons-Store, um die Reichweite zu erhöhen und sie Benutzern von Microsoft Edge zur Verfügung zu stellen.  Dieser Artikel enthält den Prozess zum Übermitteln Ihrer Erweiterung an den Microsoft Edge-Add-Ons-Speicher.  

## <a name="before-you-begin"></a>Vorbemerkungen  

Sie sollten einen funktionierenden Prototyp Ihrer Erweiterung bereit haben.  Informationen zum Erstellen einer Erweiterung finden Sie im [Lernprogramm Erste Schritte][ExtensionsGettingStarted].  

Verwenden Sie Ihr aktives Entwicklerkonto im Partner Center, um Ihre Erweiterung im Microsoft Edge-Add-Ons-Store [zu veröffentlichen.][MicrosoftPartnerCenter]  Wenn Sie über kein Entwicklerkonto verfügen, erstellen Sie ein neues Entwicklerkonto.  Um ein neues Entwicklerkonto zu öffnen und sich beim Microsoft Edge-Add-Ons-Programm zu registrieren, navigieren Sie zu [Entwicklerregistrierung][DeveloperRegistration].  

Erstellen Sie eine ZIP-Datei, die Ihr Erweiterungspaket darstellt.  Das Erweiterungspaket muss die folgenden Dateien enthalten.  

*   Das Erweiterungsmanifest, in dem Details wie der Name der Erweiterung, eine kurze Beschreibung, Berechtigungen und die Standardsprache angegeben werden.  
*   Bilder und andere Dateien, die für Ihre Erweiterung erforderlich sind.  

Die folgenden Felder im Manifest werden automatisch in die Details ihres Informationsspeichereintrags aufgenommen.  Die Felder sind auf der Seite Store-Einträge **schreibgeschützt.**  Die Seite mit den Speicherauflistungen wird weiter unten in diesem Artikel beschrieben.  Stellen Sie sicher, dass die Feldwerte ihrer bevorzugten Anzeige auf der Seite mit den Storedetails entsprechen, bevor Sie Ihr Paket in das Partner Center hochladen.  Ein Beispiel für den code, der für die Manifestdatei erforderlich ist, lesen Sie die Grundlagen der Manifestdatei.  

*   `Name` feld in der Manifestdatei, bei der es sich um den **Anzeigenamen** auf der Seite "Storedetails" handelt.  
*   `Description` feld in der Manifestdatei, die die **Kurze Beschreibung auf** der Seite "Storedetails" ist.  Geben Sie eine kurze, eingängige Beschreibung an, die am oberen Rand des Eintrags für Ihre Erweiterung angezeigt werden soll.  Wenn enthalten, wird die kurze Beschreibung, die in der Erweiterungsmanifestdatei angegeben ist, in Ihrem Storeeintrag angezeigt.  Wenn keine kurze Beschreibung in der Manifestdatei enthalten ist, werden die ersten Zeilen beschreibung angezeigt.  Geben Sie eine kurze Beschreibung an, um Inhaltswiederholungen auf Ihrer Storeeintragsseite zu vermeiden.  

## <a name="submit-your-extension-to-microsoft-edge-add-ons-store"></a>Übermitteln Ihrer Erweiterung an den Microsoft Edge-Add-Ons-Store  

Um Ihre Erweiterung an [Partner Center zu übermitteln,][MicrosoftPartnerCenter]verwenden Sie die folgenden Schritte.  

#### <a name="step-1--start-a-new-submission"></a>Schritt 1: Starten einer neuen Übermittlung  

Navigieren Sie zum [Entwicklerdashboard,][MicrosoftPartnerCenter] und wählen **Sie auf** der Seite Übersicht die Option Neue Erweiterung **erstellen** aus.  

#### <a name="step-2--upload-the-extension-package"></a>Schritt 2: Hochladen des Erweiterungspakets  

Verwenden Sie die Seite Pakete, um die ZIP-Datei Ihres **Erweiterungspakets** hochzuladen.  Sie können nur ein Paket gleichzeitig hochladen.  Sie können die Übermittlung nicht fortsetzen, wenn der Paketupload auf der Seite Pakete **nicht erfolgreich** war.  

Um das Paket hochzuladen, wählen Sie das Paket aus, und ziehen Sie es in das Uploadfeld. Sie können auch Durchsuchen **Ihrer Dateien auswählen.**  Nachdem das Paket hochgeladen wurde, wird das Paket überprüft.  Nachdem die Überprüfung erfolgreich war, überprüfen Sie die Erweiterungsdetails, und wählen Sie **dann Weiter** aus, um den Schritt fortzufahren.  Wenn Überprüfungsfehler auftreten, beheben Sie die Probleme, und versuchen Sie es erneut hochzuladen.  

#### <a name="step-3--provide-availability-details"></a>Schritt 3: Bereitstellen von Verfügbarkeitsdetails  

Geben Sie **auf** der Seite Verfügbarkeit die folgenden Informationen zur Verfügbarkeit Ihrer Erweiterung ein.  

##### <a name="visibility"></a>Sichtbarkeit  

Wählen Sie eine der folgenden Sichtbarkeitsoptionen aus, um zu definieren, ob Ihre Erweiterung im Microsoft Edge-Add-Ons-Speicher auffbar ist.  

*   `Public` \(default\)  
    Public ermöglicht es jedem Benutzer, Ihre Erweiterung über die Suche zu ermitteln, im Microsoft Edge-Add-Ons-Speicher zu browsen oder die Eintrags-URL zu Ihrer Erweiterung im Microsoft Edge-Add-Ons-Speicher zu verwenden.  Die Eintrags-URL ist auf Ihrem Partner Center-Dashboard auf der Seite **Erweiterungsübersicht** verfügbar.  
    
*   `Hidden`  
    Ausgeblendet entfernt Erweiterungen aus Suchergebnissen oder browsen im Microsoft Edge-Add-Ons-Speicher.  Um ausgeblendete Erweiterungen im Microsoft Edge-Add-Ons-Speicher zu verteilen, müssen Sie die Eintrags-URL für die Erweiterung für Ihre Kunden freigeben.  
    
> [!NOTE]
> Sie können die Sichtbarkeit Ihrer Erweiterung von **Public** in **Hidden ändern.**  Benutzer, die Ihre Erweiterung installiert haben, während die Sichtbarkeit auf öffentlich festgelegt wurde, behalten den Zugriff auf Ihre Erweiterung bei und erhalten alle Updates, die Sie über die Microsoft Edge-Add-Ons-Website zur Verfügung stellen.  

##### <a name="markets"></a>Märkte  

Definieren Sie die spezifischen Märkte, in denen Sie Ihre Erweiterung anbieten möchten.  Die Standardeinstellung für Märkte sind alle Märkte, die alle zukünftigen Märkte umfassen, die später hinzugefügt werden.  Um bestimmte Märkte zu wählen, wählen Sie **Märkte ändern aus.**  Umschalten Sie einzelne Märkte, um die einzelnen Märkte auszuschließen, oder wählen Sie **Alle** deaktivieren aus, und fügen Sie dann einzelne Märkte Ihrer Wahl hinzu.  

> [!NOTE]
> Sie können die Märkte ändern, in denen Ihre Erweiterung angeboten wird.  Ein Benutzer, der Ihre Erweiterung installiert, während sie im Markt des Benutzers verfügbar ist, behält den Zugriff auf Ihre Erweiterung.  Der Benutzer hat jedoch keinen Zugriff auf zukünftige Updates, die an den Microsoft Edge-Add-Ons-Speicher übermittelt werden.  

Wählen **Sie Speichern** aus, um mit dem Abschnitt Eigenschaften **fortzufahren.**  

#### <a name="step-4-select-properties-for-your-extension"></a>Schritt 4: Auswählen von Eigenschaften für Ihre Erweiterung  

Geben Sie **auf der Seite Eigenschaften**die folgenden Informationen ein, um die Eigenschaften Ihrer Erweiterung anzugeben.  Die Eigenschaften werden Benutzern im Microsoft Edge-Add-Ons-Speicher angezeigt.  

| Name der Erweiterungseigenschaft | Beschreibung |  
|:--- |:--- |  
| Kategorie \(erforderlich\) | Die Kategorie, die Ihre Erweiterung am besten beschreibt.  Wenn Sie Ihre Erweiterung in der richtigen Kategorie auflisten, können Benutzer Ihre Erweiterung leicht finden und mehr darüber erfahren.  |  
| Datenschutzrichtlinienanforderungen \(erforderlich\) | Geben Sie an, ob Ihre Erweiterung auf personenbezogene Informationen zu zugegriffen, erfasst oder übermittelt hat.  Ihre Erweiterung kann beim Zertifizierungsschritt fehlschlagen, wenn Sie **Ja** auswählen und keinen `Privacy policy URL` bereitstellen.  |  
| URL zu den Datenschutzrichtlinien | Eine gültige Datenschutzrichtlinien-URL, um zu kommunizieren, wie Ihre Erweiterung datenschutzgesetzen und -bestimmungen folgt.  Sie sind dafür verantwortlich, sicherzustellen, dass Ihre Erweiterung den Datenschutzgesetzen und -bestimmungen entspricht.  Sie sind auch für die Bereitstellung einer Datenschutzrichtlinien-URL verantwortlich, wenn von Ihrer Durchwahl auf personenbezogene Informationen zugegriffen, übertragen oder gesammelt wird.  Navigieren Sie zu Microsoft Edge Developer [Agreement][MicrosoftAppDeveloperAgreement] und [Microsoft Edge Add-ons store developer policies,][MicrosoftEdgeAddonsCatalogDeveloperPolicies]um zu ermitteln, ob für Ihre Erweiterung eine Datenschutzrichtlinie erforderlich ist.  |  
| Website-URL | Eine Webseite, die zusätzliche Informationen zu Ihrer Erweiterung enthält.  The `Website URL` must point to a page on your own website, not the web listing for your extension in the Microsoft Edge Add-ons store.  Der `Website URL` hilft Benutzern, mehr über Ihre Erweiterung, ihre Features und alle anderen relevanten Informationen zu erfahren.  |  
| Support-Kontaktdetails | Die URL zu Ihrer Supportwebseite oder die E-Mail-Adresse, mit der Sie Ihr Supportteam kontaktieren möchten.  |  
| Ausgereifte Inhalte | Aktivieren Sie das Kontrollkästchen, um anzugeben, ob Ihre Erweiterung ausgereifte Inhalte enthält.  Die Erweiterungsbewertung hilft bei der Bestimmung der entsprechenden Altersgruppe der Zielgruppe Ihrer Erweiterung.  Um zu ermitteln, ob Ihre Erweiterung ausgereifte Inhalte enthält, navigieren Sie zu [Microsoft Edge-Add-Ons-Speicher-Entwicklerrichtlinien][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  

Wählen **Sie Speichern** aus, um mit dem Abschnitt **Store-Einträge fortzufahren.**  

> [!Important]
> Ihr Entwickler-/Organisationsname, die Website-URL und die Supportkontaktdetails, die Sie während der Registrierung übermittelt haben, werden Benutzern im Microsoft Edge-Add-Ons-Store angezeigt.  

#### <a name="step-5-add-store-listing-details-for-your-extension"></a>Schritt 5: Hinzufügen von Store-Eintragsdetails für Ihre Erweiterung  

Die im folgenden Abschnitt bereitgestellten Informationen werden Benutzern angezeigt, die Ihren Eintrag im Microsoft Edge-Add-Ons-Speicher überprüfen.  Auch wenn einige Felder optional sind, sollten Sie so viele Informationen wie möglich bereitstellen.  Um Ihre Erweiterung im Store auflisten zu können, sind die folgenden Details erforderlich.  

*   **Beschreibung** für jede Sprache in Ihrem Erweiterungspaket.  
*   **Erweiterungsspeicherlogo** für jede Sprache in Ihrem Erweiterungspaket.  
    
> [!NOTE]
> Die mindestens erforderlichen Speichereintragsdetails müssen für mindestens eine der sprachen ausgefüllt werden, die in Ihrem Erweiterungs-ZIP-Paket erwähnt sind.  Verwenden Sie zum Hinzufügen oder Entfernen von Sprachen in Ihrem Storeeintrag im Microsoft Edge-Add-Ons-Store das Dropdownliste Sprache hinzufügen auf der Seite **Store-Einträge.** ****  Darüber hinaus können Sie Ihre Ressourcen aus einer Sprache in anderen sprachen duplizieren, indem Sie die Schaltfläche doppelte Funktionalität auf der Seite mit den Sprachdetails verwenden.  

| Name der Sprachdetails-Eigenschaft | Beschreibung |  
|:--- |:--- |  
| Anzeigename \(erforderlich\) | Die in der Manifestdatei Ihrer Erweiterung angegebene `name` Erweiterung.  Um den Anzeigenamen des Speichers nach der Übermittlung zu ändern, können Sie den Namen in der Manifestdatei aktualisieren, ein neues Erweiterungspaket erstellen und dann erneut laden.  |  
| Beschreibung \(erforderlich\) | Das Feld befasst sich mit der Erläuterung der Bedeutung Ihrer Erweiterung, der Gründe für die Installation der Erweiterung oder anderer relevanter Informationen, die `description` Benutzer kennen müssen.  Er sollte weniger als 10.000 Zeichen lang sein.  |  
| Erweiterungsspeicherlogo \(erforderlich\) | Ein Bild, das Ihr Unternehmen oder ein Seitenverhältnis von 1 darstellt, und eine empfohlene Größe von `extension logo` 300 x 300 Pixel.  Darüber hinaus können Sie das Objekt mithilfe der doppelten Schaltfläche aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird im Anschluss an das Feld gefunden, nachdem Sie Ihr Logo für die Sprache hochgeladen haben.  |  
| Kleine Werbekachel \(optional\) | Das `Small promotional tile` Bild wird verwendet, um Ihre Erweiterung zusammen mit anderen Erweiterungen im Store anzeigen.  Die Größe des Bilds sollte 440 x 280 Pixel betragen.  Darüber hinaus können Sie das Objekt mithilfe der doppelten Schaltfläche aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird im Anschluss an das Feld gefunden, nachdem Sie eine Werbekachel für die Sprache hochgeladen haben.  |  
| Screenshots \(optional\) | Sie können maximal 10 übermitteln, um die `screenshots` Funktionalität Ihrer Erweiterung detailliert zu beschreiben.  Die Größe der Screenshots muss entweder 640 x 480 Pixel oder 1280 x 800 Pixel betragen.  Darüber hinaus können Sie das Objekt mithilfe der doppelten Schaltfläche aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird im Anschluss an das Feld gefunden, nachdem Sie mindestens eine für die Sprache hochgeladen haben.|  
| Große Werbekachel \(optional\) | `Large promotion tiles` werden im Store verwendet, um Erweiterungen in der Microsoft Edge-Add-Ons-Website bekannter zu machen.  Wenn die Bilder übermittelt werden, sind sie für die Benutzer sichtbar.  Die Größe der PNG-Dateien muss 1400 x 560 Pixel betragen.  Darüber hinaus können Sie das Objekt mithilfe der doppelten Schaltfläche aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird im Anschluss an das Feld gefunden, nachdem Sie eine Werbekachel für die Sprache hochgeladen haben.  |  
| YouTube-Video-URL \(optional\) | Sie können ein Werbevideo ihrer Erweiterung für YouTube verwenden.  Das `YouTube video URL` Video wird auf der Seite mit dem Storeeintrag Ihrer Erweiterung angezeigt.  |  
| Kurzbeschreibung \(erforderlich\) | Zum Bearbeiten des müssen Sie das Beschreibungsfeld in der Manifestdatei des Erweiterungspakets aktualisieren und `short description` erneut laden.  |  
| Suchbegriffe \(optional\) | `Search terms` sind einzelne Wörter oder Ausdrücke, mit denen Benutzer Ihre Erweiterung beim Durchsuchen im Microsoft Edge-Add-Ons-Speicher ermitteln können.  Die Suchbegriffe werden benutzern nicht angezeigt.  |  

##### <a name="youtube-video-url-requirements"></a>Anforderungen an die YouTube-Video-URL  

Stellen Sie sicher, dass Ihr Video die folgenden Anforderungen erfüllt.  

*   Stellen Sie sicher, dass der Inhalt des YouTube-Videos den [Microsoft Edge-Add-Ons-Store-Entwicklerrichtlinien folgt.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  
*   Deaktivieren Sie Werbung für Ihr Video.  Weitere Informationen finden Sie unter [Set your default ad formats][GoogleYoutubeAnswer2531367Topic7072227] and Ads on embedded [videos][GoogleYoutubeAnswer132596].  
*   Aktivieren Sie die Einbettung für Ihre Videos.  Weitere Informationen finden Sie unter [Einbetten von Videos & Wiedergabelisten.][GoogleYoutubeAnswer171780]  
    
Führen Sie die folgenden Schritte aus, um die YouTube-Video-URL Ihres Videos zu übermitteln.  

1.  Suchen Sie auf YouTube nach dem Video, das Sie Ihrer Storeeintragsseite hinzufügen möchten.  
1.  Wählen Sie im Video **Die**Freigabe  >  **einbetten aus.**  
1.  Kopieren Sie den angezeigten HTML-Code.  
1.  Fügen Sie auf der Seite Speichereintragsdetails den HTML-Code in das Feld `YouTube video URL` ein.  
    
##### <a name="search-terms-requirements"></a>Anforderungen an Suchbegriffe  

Suchbegriffe müssen die folgenden Anforderungen erfüllen.  

*   Sie können Suchbegriffe eingeben, um maximal 21 Wörter zu verwenden.  Unabhängig davon, ob sie als einzelne Wörter, Ausdrücke oder eine Kombination aus beiden verwendet werden, sind maximal 21 Wörter zulässig.  
*   Bis zu sieben Suchbegriffe: einzelne Wörter oder Ausdrücke.  Jeder Suchbegriff hat eine Zeichenbeschränkung von 30 Zeichen.  
    
#### <a name="step-6-complete-your-submission"></a>Schritt 6: Abschließen der Übermittlung  

Fügen Sie **auf der Seite** Ihre Erweiterung übermitteln Hinweise zur Zertifizierung hinzu, um Die Erweiterung zu testen.  

##### <a name="notes-for-certification-optional"></a>Hinweise zur Zertifizierung (optional)  

Wenn Sie Ihre Erweiterung übermitteln, verwenden Sie die Seite Notizen für **Zertifizierung,** um den Zertifizierungstestern zusätzliche Informationen zur Verfügung zu stellen.  Die zusätzlichen Informationen tragen dazu bei, sicherzustellen, dass Ihre Erweiterung ordnungsgemäß getestet wird.  Wenn Ihre Erweiterung nicht vollständig getestet wurde, kann die Zertifizierung fehlschlagen.  

Stellen Sie bei Bedarf sicher, dass Sie die folgenden Informationen enthalten.  

*   Benutzernamen und Kennwörter für Testkonten.  
*   Schritte zum Zugreifen auf ausgeblendete oder gesperrte Features.  
*   Erwartete Unterschiede bei der Funktionalität basierend auf region- oder anderen Benutzereinstellungen.  
*   Wenn Ihre Übermittlung eine Aktualisierung einer vorhandenen Erweiterung ist, fügen Sie Informationen zu den An der Erweiterung vorgenommenen Änderungen ein.  
*   Alle zusätzlichen Informationen, die Tester über Ihre Übermittlung verstehen müssen.  

Nachdem Sie die Informationen zur Verfügung stellen, wählen Sie **Veröffentlichen** aus, um Ihre Erweiterung an den Microsoft Edge-Add-Ons-Speicher zu übermitteln.  Ihre Übermittlung wird mit dem Zertifizierungsschritt fortgesetzt.  Der Zertifizierungsprozess kann bis zu sieben Werktage nach der Übermittlung dauern.  

Wenn Ihre Übermittlung die Zertifizierung besteht, wird Ihre Erweiterung im Microsoft Edge-Add-Ons-Speicher veröffentlicht.  Der Status Ihrer Erweiterung im Partner Center-Dashboard ändert sich in `In the Store` .  

> [!NOTE]
> Wenn beim Übermittlungs- oder Registrierungsprozess Probleme auftreten, senden Sie ein Supportticket unter [Extensions New Support Request,][ExtensionsSupportForm] oder senden Sie eine E-Mail an [ext_dev_support@microsoft.com][MailtoExtDevSupportMicrosoftCom].  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Erste Schritte mit Microsoft Edge-Erweiterungen (Chromium) | Microsoft Docs"  
[DeveloperRegistration]: ./create-dev-account.md "Registrieren als Microsoft Edge-Erweiterungsentwickler | Microsoft Docs"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Portierung Ihrer Chromium-Erweiterung zu Microsoft Edge | Microsoft Docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Microsoft Edge-Add-Ons speichern Entwicklerrichtlinien | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "App Developer Agreement | Microsoft Docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Erweiterungen Neue Supportanfrage | Microsoft Support"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Legen Sie Ihre Standardanzeigeformate | Hilfe zu YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anzeigen in eingebetteten Videos | Hilfe zu YouTube"  
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Einbetten von Videos & Wiedergabelisten | Hilfe zu YouTube"  

[MailtoExtDevSupportMicrosoftCom]: mailto:ext_dev_support@microsoft.com "Senden von E-Mails an ext_dev_support@microsoft.com" 
