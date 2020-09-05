---
description: Veröffentlichen von Microsoft Edge (Chrom)-Erweiterungen im Microsoft Edge-Add-ons-Store.
title: Veröffentlichen Sie die Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/04/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 47e6a96ec2fcd3d2ad8fb3edad702abfc91ab57d
ms.sourcegitcommit: 7e3644e6b1d568ab795168e421c013814efa0073
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/04/2020
ms.locfileid: "10996215"
---
# Veröffentlichen Sie die Erweiterung  

Nachdem Sie Ihre Erweiterung entwickelt und getestet haben, sind Sie möglicherweise bereit, ihre Erweiterung mithilfe des Microsoft Edge-Add-ons-Katalogs zu verteilen.  Wenn Sie über eine vorhandene Chromium-Erweiterung verfügen, die Sie für Microsoft Edge-Benutzer verfügbar machen möchten, können Sie [Ihre vorhandene Chrom-Erweiterung][PortChromiumExtension] auch an Microsoft Edge portieren.  

Durch das Veröffentlichen Ihrer Erweiterung im Microsoft Edge-Add-ons-Katalog wird die Reichweite ihrer Erweiterung erhöht und für Endbenutzer verfügbar.  Dieses Thema enthält eine exemplarische Vorgehensweise zum Übermitteln Ihrer Erweiterung an den Microsoft Edge-Add-ons-Katalog.  

## Vorbemerkungen  

An diesem Punkt sollten Sie einen funktionierenden Prototyp ihrer Erweiterung bereit haben.  Informationen zum Erstellen einer Erweiterung finden Sie im [Lernprogramm "erste Schritte][ExtensionsGettingStarted]".  

Wenn Sie Ihre Erweiterung auf der Microsoft Edge-Add-ons-Website veröffentlichen möchten, müssen Sie über ein aktives Entwicklerkonto im [Partner Center][MicrosoftPartnerCenter]verfügen.  Wenn Sie ein neues Entwicklerkonto öffnen und sich beim Microsoft Edge-Add-ons-Programm registrieren möchten, führen Sie den im [Entwickler Registrierungs][DeveloperRegistration] Handbuch erwähnten Vorgang aus.  

Erstellen Sie eine ZIP-Datei, die das Erweiterungspaket darstellt.  Ihr Erweiterungspaket muss die folgenden Dateien beinhalten.  

*   Das Erweiterungs Manifest, das Details wie den Namen der Erweiterung, Kurzbeschreibung, Berechtigungen und Standardsprache angibt.  
*   Bilder und andere Dateien, die für Ihre Erweiterung erforderlich sind.  

Die folgenden Felder im Manifest werden automatisch in die Details Ihres Store-Eintrags aufgenommen und können nicht über die Seite Store-Einträge geändert werden, die weiter unten in diesem Thema beschrieben wird.  Stellen Sie sicher, dass die Felder ausgefüllt sind, damit Sie Ihrer bevorzugten Anzeige auf der Seite Store Details entsprechen, bevor Sie Ihr Paket zum Partner Center hochladen.  Ein Beispiel für den Code, der für die Manifestdatei erforderlich ist, finden Sie Untergrund lagen der Manifestdatei.  

*   `Name` Feld in der Manifestdatei, bei dem es sich um den **Anzeigenamen** auf der Seite Store Details handelt.  
*   `Description` Feld in der Manifestdatei, das die **kurze Beschreibung** auf der Seite Store-Details ist.  Geben Sie eine kurze, einprägsame Beschreibung ein, die am oberen Rand des Eintrags für Ihre Erweiterung angezeigt werden soll.  Wenn enthalten, wird die in der Erweiterungs Manifestdatei angegebene kurze Beschreibung in Ihrem Store-Eintrag angezeigt.  Wenn in der Manifestdatei keine kurze Beschreibung enthalten ist, werden die ersten Zeilen der Beschreibung angezeigt.  Sie sollten eine kurze Beschreibung zur Vermeidung von inhaltlichen Wiederholungen auf Ihrer Store-Eintragsseite angeben.  

## Übermitteln der Erweiterung an den Microsoft Edge-Add-ons-Store  

Führen Sie die folgenden Schritte aus, um Ihre Durchwahl an das [Partner Center][MicrosoftPartnerCenter]zu übermitteln.  

#### Schritt 1: Starten einer neuen Übermittlung  

Wechseln Sie zum [entwicklerdashboard][MicrosoftPartnerCenter] , und wählen Sie auf der Übersichts **Seite** **neue Erweiterung erstellen** aus.  

#### Schritt 2: Hochladen des Erweiterungspakets  

Verwenden Sie die Seite " **Pakete** ", um die ZIP-Datei Ihres Erweiterungspakets hochzuladen.  Sie können nur jeweils ein Paket hochladen.  Sie können die Übermittlung nicht fortsetzen, wenn der Paket Upload auf der Seite " **Pakete** " nicht erfolgreich ist.  

Laden Sie das Paket hoch, indem Sie entweder das Paket in das Feld Upload ziehen, oder indem Sie **Dateien durchsuchen**auswählen.  Nachdem das Paket hochgeladen wurde, wird Ihr Paket überprüft.  Nachdem die Validierung erfolgreich war, überprüfen Sie die Erweiterungs Details, und wählen Sie dann **weiter** aus, um fortzufahren.  Wenn es Validierungsfehler gibt, beheben Sie die Probleme, und versuchen Sie erneut, das Hochladen.  

#### Schritt 3: Bereitstellen von Verfügbarkeits Details  

Geben Sie auf der Seite **Verfügbarkeit** die folgenden Informationen zur Verfügbarkeit ihrer Erweiterung ein.  

##### Sichtbarkeit  

Wählen Sie eine der folgenden Sichtbarkeitsoptionen aus, um zu definieren, ob Ihre Erweiterung im Microsoft Edge-Add-ons-Katalog auffindbar ist.  

*   `Public` \ (Standard \)  
    Mit Public können Erweiterungen für alle Personen über die Suchfunktion, Durchsuchen im Microsoft Edge-Add-ons-Katalog oder mithilfe der Eintrags-URL für Ihre Erweiterung im Microsoft Edge-Add-on-Store erkannt werden.  Die Eintrags-URL ist auf der Seite mit der Erweiterungs **Übersicht** im Partner Center-Dashboard verfügbar.  

*   `Hidden`  
    Ausgeblendet entfernt Erweiterungen aus Suchergebnissen oder Durchsuchen im Microsoft Edge-Add-ons-Katalog.  Wenn Sie versteckte Erweiterungen im Microsoft Edge-Add-ons-Store verteilen möchten, müssen Sie die Eintrags-URL für die Erweiterung für Ihre Kunden freigeben.  

> [!NOTE]
> Sie können die Sichtbarkeit ihrer Erweiterung von **Public** in **Hidden**ändern.  Benutzer, die ihre Erweiterung installiert haben, während die Sichtbarkeit auf öffentlich festgesetzt wurde, behalten den Zugriff auf Ihre Erweiterung und erhalten alle Updates, die Sie über die Microsoft Edge-Add-ons-Website zur Verfügung stellen.  

##### Märkte  

Definieren Sie die spezifischen Märkte, in denen Sie Ihre Erweiterung anbieten möchten.  Standardmäßig wurden alle Märkte ausgewählt, einschließlich aller zukünftigen Märkte, die später hinzugefügt werden.  Sie können aber auch bestimmte Märkte auswählen, indem Sie **Märkte ändern**auswählen.  Deaktivieren Sie einzelne Märkte, um Sie auszuschließen, oder wählen Sie **Alle auswählen** aus, und fügen Sie dann einzelne Märkte Ihrer Wahl hinzu.  

> [!NOTE]
> Sie können die Märkte ändern, auf denen Ihre Durchwahl angeboten wird.  Benutzer, die ihre Erweiterung installiert haben, während Sie auf Ihrem Markt verfügbar waren, behalten den Zugriff auf Ihre Durchwahl.  Ihre Benutzer haben jedoch keinen Zugriff mehr auf zukünftige Updates, die an den Microsoft Edge-Add-ons-Katalog übermittelt wurden.  

Wählen Sie **Speichern** aus, um mit dem Abschnitt **Eigenschaften** fortzufahren.  

#### Schritt 4: Auswählen von Eigenschaften für Ihre Erweiterung  

Geben Sie auf der **Seite Eigenschaften**die folgenden Informationen ein, um die Eigenschaften ihrer Erweiterung anzugeben.  Die Eigenschaften werden Benutzern im Microsoft Edge-Add-ons-Katalog angezeigt.  

| Name der Erweiterungseigenschaft | Beschreibung |  
|:--- |:--- |  
| Kategorie \ (erforderlich \) | Die Kategorie, die ihre Erweiterung am besten beschreibt.  Wenn Sie Ihre Erweiterung in der richtigen Kategorie auflisten, können Benutzer ihre Erweiterung problemlos finden und mehr darüber erfahren.  |  
| Datenschutzrichtlinien Anforderungen \ (erforderlich \) | Geben Sie an, ob Ihre Durchwahl personenbezogene Informationen zugreift, sammelt oder überträgt.  Ihre Erweiterung kann den Zertifizierungs Schritt nicht ausführen, wenn Sie " **Ja** " auswählen und keine angeben `Privacy policy URL` .  |  
| URL zu den Datenschutzrichtlinien | Eine gültige Datenschutzrichtlinien-URL, um zu kommunizieren, wie Ihre Erweiterung den Datenschutzbestimmungen entspricht.  Sie sind dafür verantwortlich, sicherzustellen, dass Ihre Erweiterung den Datenschutzbestimmungen und-Vorschriften entspricht, und bei Bedarf eine gültige URL für die Datenschutzrichtlinie zur Verfügung stellen.  Geben Sie eine Datenschutzrichtlinien-URL an, wenn über Ihre Erweiterung auf persönliche Informationen zugegriffen, diese übertragen oder erfasst wird.  Wenn Sie feststellen möchten, ob für Ihre Erweiterung eine Datenschutzrichtlinie erforderlich ist, wechseln Sie zu [Microsoft Edge Developer Agreement][MicrosoftAppDeveloperAgreement] und [Microsoft Edge Add-ons Catalog-Entwicklerrichtlinien][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  
| Website-URL | Eine Webseite, die zusätzliche Informationen zu ihrer Erweiterung enthält.  Der `Website URL` Verweis muss auf eine Seite auf Ihrer eigenen Website verweisen, nicht auf den Webeintrag für Ihre Erweiterung im Microsoft Edge-Add-ons-Katalog.  Das `Website URL` hilft Benutzern, mehr über Ihre Erweiterung, ihre Features und alle anderen relevanten Informationen zu erfahren.  |  
| Support-Kontaktdetails | Die URL Ihrer Support-Webseite oder die e-Mail-Adresse, an die Sie Ihr Support-Team wenden können.  |  
| Ausgereifte Inhalte | Kontrollkästchen, um anzugeben, ob Ihre Erweiterung ausgereifte Inhalte enthält.  Mit der Erweiterungs Bewertung können Sie die geeignete Altersgruppe der Zielgruppe Ihrer Durchwahl ermitteln.  Wenn Sie feststellen möchten, ob Ihre Erweiterung über ausgereifte Inhalte verfügt, wechseln Sie zu [Microsoft Edge Add-ons Catalog-Entwicklerrichtlinien][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  

Wählen Sie **Speichern** aus, um zum Abschnitt **Store-Einträge** weiter zu gehen.  

#### Schritt 5: Hinzufügen von Details zu Store-Einträgen für Ihre Erweiterung  

Die Informationen, die im folgenden Abschnitt bereitgestellt werden, werden Benutzern angezeigt, die Ihren Eintrag im Microsoft Edge-Add-ons-Katalog besuchen.  Obwohl einige Felder optional sind, sollten Sie so viele Informationen wie möglich angeben.  Die Mindestanforderungen für die Erweiterung für den Eintrag im Store für jede Sprache, die in Ihrem Erweiterungspaket angegeben ist, sind **Description** und das **Logo des Erweiterungsspeichers**.  

> [!NOTE]
> Die erforderlichen Mindestinformationen für den Store-Eintrag müssen für jede Sprache ausgefüllt werden, die in Ihrem ZIP-Erweiterungspaket angegeben ist.  Wenn Sie Sprachen in Ihrem Store-Eintrag im Microsoft Edge-Add-ons-Katalog hinzufügen oder entfernen möchten, müssen Sie die Liste der von der Erweiterung unterstützten Sprachen im Erweiterungspaket ändern, ein neues Erweiterungspaket erstellen und es erneut hochladen.  

| Eigenschaftsname des Store-Eintrags | Beschreibung |  
|:--- |:--- |  
| Store Listing Languages \ (erforderlich \) | Wählen Sie im Dropdownmenü **Sprachen** eine Sprache aus, und geben Sie die Details für den Store-Eintrag für diese Sprache ein.  Erweiterungen, die mehrere Sprachen unterstützen, müssen eine Store-Eintragsseite für jede unterstützte Sprache bereitstellen.  |  
| Anzeigename \ (erforderlich \) | Der Name der Erweiterung, die in der Manifestdatei der Erweiterung angegeben ist.  Wenn Sie den Store-Anzeigenamen nach der Übermittlung ändern möchten, können Sie den Namen in der Manifestdatei aktualisieren, ein neues Erweiterungspaket erstellen und es dann erneut hochladen.  |  
| Beschreibung \ (erforderlich \) | Das Feld "Beschreibung" konzentriert sich darauf, zu erläutern, was Ihre Erweiterung tut, warum Benutzer Sie installieren sollten, oder andere relevante Informationen, die Benutzer wissen müssen.  Es sollte kleiner als 10.000 Zeichen sein.  |  
| Erweiterungsspeicher-Logo \ (erforderlich \) | Ein Bild, das Ihr Firmen-oder Erweiterungs Logo mit einem Seitenverhältnis von 1 und einer empfohlenen Größe von 300 x 300 Pixel darstellt.  |  
| Kleine Werbe Kachel \ (optional \) | Das `Small promotional tile` Bild wird verwendet, um Ihre Erweiterung neben anderen Erweiterungen im Store anzuzeigen.  Die Größe des Bilds sollte 440 x 280 Pixel aufweisen.  |  
| Screenshots \ (optional \) | Sie können maximal 10 Screenshots einreichen, in denen die Funktionalität ihrer Erweiterung ausführlich beschrieben wird.  Die Größe der Screenshots muss entweder 640 x 480 Pixel oder 1280 x 800 Pixel sein.  |  
| Große Werbe Kachel \ (optional \) | Große Absatz Förderungs Kacheln werden im Store verwendet, um Erweiterungen in der Microsoft Edge-Add-ons-Website hervorgehobener zu machen.  Die Bilder sind für die Benutzer sichtbar, wenn Sie übermittelt wurden.  Die Größe der PNG-Dateien muss 1400 x 560 Pixel sein.  |  
| YouTube-Video-URL \ (optional \) | Sie können ein YouTube-Promo-Video Ihrer Durchwahl hinzufügen.  Das `YouTube video URL` Video wird auf der Store-Eintragsseite ihrer Durchwahl angezeigt.  |  
| Kurzbeschreibung \ (erforderlich \) | Um die Kurzbeschreibung zu bearbeiten, müssen Sie das Feld Beschreibung in der Manifestdatei Ihres Erweiterungspakets aktualisieren und erneut hochladen.  |  
| Suchbegriffe \ (optional \) | Suchbegriffe sind einzelne Wörter oder Ausdrücke, die Benutzern bei der Suche im Microsoft Edge-Add-ons-Katalog helfen, ihre Erweiterung zu entdecken.  Die Suchbegriffe werden Benutzern nicht angezeigt.  |  

##### YouTube-Video-URL-Anforderungen  

Stellen Sie sicher, dass Ihr Video die folgenden Anforderungen erfüllt.  

*   Überprüfen Sie, ob der Inhalt des YouTube-Videos dem [Microsoft Edge Addons Catalog Developer Policys][MicrosoftEdgeAddonsCatalogDeveloperPolicies] Topic entspricht.  
*   Deaktivieren Sie Werbung für Ihr Video.  Weitere Informationen finden [Sie unter Festlegen der standardmäßigen Anzeigenformate][GoogleYoutubeAnswer2531367Topic7072227] und [anzeigen für eingebettete Videos][GoogleYoutubeAnswer132596].  
*   Aktivieren Sie die Einbettung für Ihre Videos.  Weitere Informationen finden Sie unter [Einbetten von Videos & Wiedergabelisten][GoogleYoutubeAnswer171780].  

Führen Sie die folgenden Schritte aus, um die YouTube-Video-URL Ihres Videos einzureichen.  

1.  Suchen Sie auf YouTube das Video, das Sie zu Ihrer Shop-Eintragsseite hinzufügen möchten.  
1.  Wählen Sie unter dem Video **Share**die Option  >  **Einbettung**freigeben aus.  
1.  Kopieren Sie den angezeigten HTML-Code.  
1.  Fügen Sie auf der Seite Store Listing Details den HTML-Code in das `YouTube video URL` Feld ein.  

##### Anforderungen für Suchbegriffe  

Suchbegriffe müssen die folgenden Voraussetzungen erfüllen.  

*   Sie können Suchbegriffe eingeben, um maximal 21 Wörter zu verwenden.  Unabhängig davon, ob Sie als einzelne Wörter, Phrasen oder eine Kombination aus beidem verwendet werden, dürfen maximal 21 Wörter verwendet werden.  
*   Bis zu maximal sieben Suchbegriffe: einzelne Wörter oder Ausdrücke.  Jeder Suchbegriff hat eine Zeichen Grenze von 30 Zeichen.  

#### Schritt 6: Abschließen der Übermittlung  

Fügen Sie auf der Seite **Submit your extension** die Hinweise für die Zertifizierung hinzu, damit Sie Ihre Erweiterung testen können.  

##### Hinweise zur Zertifizierung (optional)  

Verwenden Sie beim übermitteln der Erweiterung die Seite **Hinweise für die Zertifizierung** , um den Zertifizierungs Prüfern zusätzliche Informationen zur Verfügung zu stellen.  Mit den zusätzlichen Informationen können Sie sicherstellen, dass Ihre Erweiterung richtig getestet wird.  Wenn Ihre Erweiterung nicht vollständig getestet wurde, kann Sie möglicherweise nicht zertifiziert werden.  

Stellen Sie sicher, dass Sie die folgenden Informationen bei Bedarf angeben.  

*   Benutzernamen und Kennwörter für Testkonten.  
*   Schritte für den Zugriff auf ausgeblendete oder gesperrte Features  
*   Erwartete Unterschiede bei der Funktionalität basierend auf Regions-oder anderen Benutzereinstellungen.  
*   Wenn es sich bei der Übermittlung um eine Aktualisierung einer vorhandenen Erweiterung handelt, fügen Sie Informationen zu den an der Erweiterung vorgenommenen Änderungen hinzu.  
*   Alle weiteren Informationen, die Tester über ihre Übermittlung wissen müssen.  

Nachdem Sie die Informationen bereitgestellt haben, wählen Sie **veröffentlichen** aus, um Ihre Erweiterung an den Microsoft Edge-Add-ons-Katalog zu übermitteln.  Ihre Übermittlung geht zum Zertifizierungs Schritt über.  Der Zertifizierungsprozess kann bis zu sieben arbeitstagenach ihrer Übermittlung dauern.  

Wenn Ihre Übermittlung die Zertifizierung übergibt, wird Ihre Erweiterung im Microsoft Edge-Add-ons-Katalog veröffentlicht.  Der Status Ihrer Erweiterung im Partner Center-Dashboard wird in geändert `In the Store` .  

> [!NOTE]
> Wenn Sie Probleme bei der Übermittlung oder Registrierung haben, geben Sie [hier][ExtensionsSupportForm] ein Support-Ticket ein oder senden Sie eine e-Mail an [ext_dev_support@Microsoft.com](mailto:ext_dev_support@microsoft.com).  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Erste Schritte mit Microsoft Edge-Erweiterungen (Chromium) | Microsoft Docs"  
[DeveloperRegistration]: ./create-dev-account.md "Registrieren als Microsoft Edge Extensions Developer | Microsoft docs"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Portieren Sie Ihre Chrom-Erweiterung zu Microsoft Edge | Microsoft docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Microsoft Edge Addons-Katalog-Entwicklerrichtlinien | Microsoft docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Vereinbarung für App-Entwickler | Microsoft docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Erweiterungen neue Support Anfrage | Microsoft-Support"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Festlegen der standardmäßigen Anzeigenformate-YouTube-Hilfe"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anzeigen in eingebetteten Videos – YouTube-Hilfe"
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Einbetten von Videos & Wiedergabelisten – YouTube-Hilfe"  
