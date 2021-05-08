---
description: Microsoft Edge Add-Ons Store Entwicklerrichtlinien
title: Microsoft Edge Add-Ons Store Entwicklerrichtlinien
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: cc34a95e08d01ebee54581222d0eb9fefa3dc458
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343080"
---
# Microsoft Edge Add-Ons Store Entwicklerrichtlinien  

## Einführung und Ziel dieses Dokuments  

Vielen Dank für Ihr Interesse an der Entwicklung von Erweiterungen für den Microsoft Edge-Add-Ons-Store.  Die Microsoft Edge-Add-Ons-Speicherentwicklerrichtlinien \(Add-Ons store developer policies\) gelten für Ihre Erweiterungen, einschließlich der Übermittlung von Erweiterungen über [Partner Center][MicrosoftPartnerCenter] und der Bereitstellung solcher Erweiterungen über die Microsoft Edge-Add-Ons.  

## Prinzipien  

Zunächst einige wichtige Grundregeln:  

*   Sie sollten einen eindeutigen und eindeutigen Wert in Ihren Erweiterungen für Microsoft Edge anbieten.  Geben Sie einen überzeugenden Grund an, Ihre Erweiterungen aus dem Microsoft Edge-Add-Ons-Store \(Microsoft Edge-Add-Ons\) herunterzuladen.  
*   Sie dürfen unsere gemeinsamen Benutzer nicht in die Irre führen, was Ihre Erweiterung macht, wer sie bietet und so weiter.  
*   Sie dürfen nicht versuchen, Benutzer, das System oder das Ökosystem zu betrügen.  Es gibt keinen Platz in unseren Microsoft Edge-Add-Ons für jegliche Art von Betrug. Seien es Bewertungen und Überprüfung von Manipulationen, Kreditkartenbetrug oder andere betrügerische Aktivitäten.  
    
Die Einhaltung der Microsoft Edge-Add-Ons-Entwicklerrichtlinien sollte Ihnen dabei helfen, Entscheidungen zu treffen, die die Ansinnen und Zielgruppen Ihrer Erweiterung verbessern.  

Ihre Erweiterungen sind entscheidend für die Erfahrung von Hunderten von Millionen von Benutzern.  Wir freuen uns auf Ihre Erstellung und freuen uns auf Ihre Erweiterungen auf der Ganzen Welt.  

## 1. Produktrichtlinien  

### 1.1 Distinct Function & Value; Genaue Darstellung  

Ihre Erweiterung und die zugehörigen Metadaten müssen die von Ihnen beschriebene Quelle, Funktionalität und Features genau und deutlich widerspiegeln.  

#### 1.1.1 Erweiterungen müssen einen einzigen Zweck haben  

Ihre Erweiterung muss einen einzigen Zweck mit eingeschränkter Funktionalität haben.  

#### 1.1.2 Beschreiben Der Erweiterung  

Alle Aspekte Ihrer Erweiterung sollten die Funktionen, Features und wichtigen Einschränkungen Ihrer Erweiterung, einschließlich erforderlicher oder unterstützter Eingabegeräte, genau beschreiben.  Die Wertversprechung Ihrer Erweiterung muss während der ersten Ausführung klar sein.  Ihre Erweiterung verwendet möglicherweise keinen Namen oder ein Symbol, das dem anderer Erweiterungen ähnelt, und darf nicht beanspruchen, ein Unternehmen, eine Regierungsstelle oder eine andere Entität zu repräsentieren, wenn Sie nicht über die Berechtigung zum Erstellen dieser Darstellung verfügen.  

#### 1.1.3-Funktionalität  

Ihre Erweiterung muss voll funktionsfähig sein.  

#### 1.1.4 Suche und Ermittlung  

Suchbegriffe dürfen sieben eindeutige Begriffe nicht überschreiten und sollten für Ihre Erweiterung relevant sein.  

#### 1.1.5 Bereitstellen entsprechender Details  

Sie müssen unterschiedliche und informative Details zu Ihrer Erweiterung und zu den Funktionen im Eintrag \(metadaten\) für Ihre Erweiterung bereitstellen.  Ihre Erweiterung muss eine wertvolle und hochwertige Benutzererfahrung bieten.  Ihre Erweiterung muss auch in Microsoft Edge-Add-Ons aktiv sein.  

#### 1.1.6 Stabilität und Leistung  

Ihre Erweiterung darf sich nicht negativ auf die Leistung oder Stabilität von Microsoft Edge auswirken.  

#### 1.1.7 Verschleierung  

Erweiterungen mit verschleiertem Code sind nicht zulässig.  Dies umfasst Code innerhalb Ihres Erweiterungspakets sowie alle externen Code- oder Ressourcen, die aus dem Web abgerufen werden.  Möglicherweise werden Sie aufgefordert, Teile Ihres Codes umgestalten, wenn er nicht überprüft werden kann.  

#### 1.1.8 Ändern von Browsereinstellungen  

Ihre Erweiterung darf ohne entsprechende Zustimmung des Benutzers die Browserfunktionen oder -einstellungen nicht ändern oder ändern, einschließlich, aber nicht beschränkt auf: den Adressleistensuchanbieter und -vorschläge, die Startseite oder Homepage, die neue Registerkartenseite und das Hinzufügen oder Entfernen von Favoriten.  

Jede Änderung der Browsereinstellungen sollte explizit in der Beschreibung Ihrer Erweiterung dokumentiert werden.  

Ihre Erweiterung kann nur die Schlüsseleinstellungen überarbeiten, um eine Microsoft-Webseite oder einen Dienst durch die eines Drittanbieters zu ersetzen \(z. B. die Verwendung einer Drittanbietersuchmaschine erfordern oder die Homepage auf eine Drittanbieterwebeigenschaft\) festlegen, wenn Sie von einem solchen Drittanbieter beschäftigt sind oder anderweitig diesem Drittanbieter zugeordnet sind.  

### 1.2 Sicherheit  

Ihre Erweiterung darf weder die Sicherheit des Benutzers noch die Sicherheit oder Funktionalität des Geräts, Systems oder verwandter Systeme gefährden oder gefährden.  

#### 1.2.1 Inhaltssicherheitsrichtlinien  

> [!NOTE]
> Wenn Sie Änderungen an Ihrer Erweiterung vornehmen, die über die beschriebene Funktionalität hinausgehen, müssen alle Codeänderungen mit der [Microsoft Edge-Inhaltssicherheitsrichtlinie kompatibel sein.][MicrosoftEdgeContentSecurityPolicyRemoteScript]  Ihre Erweiterung sollte z. B. kein Remoteskript herunterladen und dieses Skript anschließend auf eine Weise ausführen, die nicht mit der beschriebenen Funktionalität konsistent ist.  

#### 1.2.2 Unerwünschte und schädliche Software  

Ihre Erweiterung darf keine Schadsoftware gemäß den Microsoft-Kriterien für unerwünschte und [bösartige Software enthalten oder aktivieren.][MicrosoftIdentifiesMalwareUnwantedApplications]  

#### 1.2.3 Abhängigkeit von anderer Software  

Ihre Erweiterung hängt möglicherweise von nicht integrierter Software \(z. B. einem anderen Produkt, Modul oder Dienst\) ab, um die primäre Funktionalität bereitzustellen, vorausgesetzt, Sie geben die Abhängigkeit in der Beschreibung an.  

#### 1.2.4 Extensions Update  

Sofern nicht anders von Microsoft zulässig, dürfen Ihre Erweiterungen nur über Microsoft Edge-Add-Ons aktualisiert werden.  

### 1.3 Produkt ist testbar  

Ihre Erweiterung muss testbar sein.  Wenn Es nicht möglich ist, Ihre Erweiterung aus irgendeinem Grund zu testen, einschließlich, aber nicht beschränkt auf die unten aufgeführten Elemente, kann ihre Erweiterung diese Anforderung nicht erfüllen.  

#### 1.3.1 Benutzeranmeldeinformationen  

Wenn Ihre Erweiterung Anmeldeinformationen erfordert, geben Sie ein funktionierendes Demokonto mithilfe des Felds `Notes for certification` an.  

#### 1.3.2 Verfügbarkeit von Diensten  

Wenn Ihre Erweiterung Zugriff auf einen Server erfordert, muss der Server funktionsfähig sein, um zu überprüfen, ob er ordnungsgemäß funktioniert.  

### 1.4 Verwendbarkeit  

Ihre Erweiterung muss microsoft Edge-Add-Ons-Speicherstandards für die Benutzerfreundlichkeit erfüllen, einschließlich, aber nicht beschränkt auf die in den folgenden Unterabschnitten aufgeführten.  

#### 1.4.1 Plattformübergreifend kompatibilität  

Ihre Erweiterung sollte mit Microsoft Edge auf allen Geräten und Plattformen kompatibel sein, auf denen sie heruntergeladen werden können.  Wenn eine Erweiterung auf einem Gerät heruntergeladen wird, mit dem sie nicht kompatibel ist, sollte sie diese beim Start erkennen und dem Benutzer eine Meldung mit den Anforderungen anzeigen, die Geräte erfüllen müssen, um mit Ihrer Erweiterung kompatibel zu sein.  

#### 1.4.2 Benutzeroberfläche  

Ihre Erweiterung muss sofort gestartet werden und auf Benutzereingaben reagieren.  Ihre Erweiterung muss weiterhin ausgeführt werden und auf Benutzereingaben reagieren.  Ihre Erweiterung muss anmutig heruntergefahren werden und nicht unerwartet geschlossen werden.  Ihre Erweiterung sollte Ausnahmen behandeln und auf Benutzereingaben reagieren, nachdem die Ausnahme behandelt wurde.  

### 1.5 Personenbezogene Informationen  

Die folgenden Anforderungen gelten für Erweiterungen, die auf personenbezogene Informationen zugreifen.  Personenbezogene Informationen umfassen alle Informationen oder Daten, die eine Person identifizieren oder verwenden können oder die solchen Informationen oder Daten zugeordnet sind.  

#### 1.5.1 Sammeln von personenbezogenen Informationen nur bei Bedarf  

Ihre Erweiterung kann persönliche Informationen sammeln, darauf zugreifen, diese verwenden oder übertragen \(einschließlich Webbrowsingaktivitäten\); nur, wenn dies von und nur für die Verwendung in einem öffentlich offengelegten, benutzerfreundlichen Feature erforderlich ist.  

#### 1.5.2 Beibehalten einer Datenschutzrichtlinie  

Unabhängig davon, ob Ihre Erweiterung auf personenbezogene Informationen zutritt, sammelt oder überträgt; Sie müssen Ihre Datenschutzrichtlinie bei gesetzlicher Aufforderung prominent beachten und einhalten.  Ihre Datenschutzrichtlinie muss die Benutzer über die von Ihrer Durchwahl zugegriffenen, erfassten oder übermittelten personenbezogenen Informationen informieren, wie diese Informationen verwendet, gespeichert und gesichert werden, und die Arten von Parteien angeben, denen sie offengelegt werden.  Ihre Datenschutzrichtlinie muss die Steuerelemente beschreiben, die Benutzer über die Verwendung und Freigabe ihrer Informationen verfügen, wie sie auf ihre Informationen zugreifen und die geltenden Gesetze und Vorschriften einhalten müssen.  Ihre Datenschutzrichtlinie muss auf dem neuesten Stand gehalten werden, wenn Sie ihrer Erweiterung neue Features und Funktionen hinzufügen.  

Wenn Sie Microsoft Ihre Datenschutzrichtlinie bereitstellen, stimmen Sie zu, Microsoft zu erlauben, diese Datenschutzrichtlinie für Benutzer Ihrer Erweiterung zu teilen.  

#### 1.5.3 Freigeben von Daten an Dritte  

Sie können die persönlichen Informationen von Benutzern Ihrer Erweiterung nur dann über Ihre Erweiterung oder die zugehörigen Metadaten an einen außerhalb bzw. an Einen Drittanbieter veröffentlichen, nachdem Sie die Zustimmung dieser Benutzer einholen.  Opt-In-Zustimmung bedeutet, dass die Benutzer ihre ausdrückliche Berechtigung auf der Benutzeroberfläche Ihrer Erweiterung für die angeforderte Aktivität erteilen, nachdem Sie:  

*   Beschreiben Sie Ihren Benutzern, wie auf die Informationen zugegriffen, sie verwendet oder freigegeben werden, und geben Sie die Arten von Parteien an, denen sie offengelegt werden, und  
*   Stellen Sie Ihren Benutzern einen Mechanismus in Der Benutzeroberfläche der Erweiterung bereit, über den sie die Möglichkeit haben, die Berechtigung später zurück zu setzen und sich abmelden zu können.  
    
#### 1.5.4 Freigabeinformationen von Nichtbenutzern  

Wenn Sie die persönlichen Informationen einer Person über Ihre Durchwahl oder die Metadaten an einen außerhalb bzw. Drittanbieter weitergegebenen Dienst veröffentlichen, aber die Person, deren Informationen freigegeben werden, ist kein Benutzer Ihrer Durchwahl;  

1.  Sie müssen die ausdrückliche schriftliche Zustimmung einholen, um diese personenbezogenen Informationen zu veröffentlichen.  
1.  Sie müssen der Person, deren Informationen weitergegeben werden, jederzeit erlauben, diese Zustimmung zurückzuziehen.  
1.  Ihre Datenschutzrichtlinie muss eindeutig offenlegen, dass Sie personenbezogene Informationen auf diese Weise sammeln können.  
1.  Wenn dies nach geltendem Recht erforderlich ist, müssen Sie die personenbezogenen Informationen jeder Person auf Anfrage löschen, einschließlich Personen, deren Informationen Sie auf diese Weise sammeln.  
1.  Wenn Ihre Erweiterung Benutzern Zugriff auf die persönlichen Informationen einer anderen Person bietet, gilt diese Anforderung auch.  
    
#### 1.5.5 Sicheres Übertragen von Informationen  

Wenn Ihre Erweiterung personenbezogene Informationen erfasst, speichert oder überträgt; Dies muss mithilfe moderner Kryptografiemethoden sicher sein.  

#### 1.5.6 Hochsensible Informationen  

Ihre Erweiterung darf keine hochsensiblen personenbezogenen Informationen, z. B. Gesundheits- oder Finanzdaten, sammeln, speichern oder übertragen, es sei denn, die Informationen stehen im Zusammenhang mit der Funktionalität Ihrer Erweiterung.  Ihre Erweiterung muss auch die ausdrückliche Zustimmung des Benutzers einholen, bevor diese Informationen gesammelt, gespeichert oder übertragen werden.  

### 1.6 Berechtigungen  

Ihre Erweiterung darf nur die Berechtigungen anfordern, die für die Funktionsweise erforderlich sind.  Sie müssen eine Beschreibung der Funktionsweise Ihrer Erweiterung bereitstellen.  Ihre Erweiterung darf nur wie beschrieben ausführen.  Ihre Erweiterung erfordert möglicherweise keine Berechtigung für Funktionen, die über die funktionen hinausgehen, die zum Ausführen und Funktionieren wie deklariert erforderlich sind.  

### 1.7 Lokalisierung  

Sie sollten ihre Erweiterung für alle Sprachen lokalisieren, die von Ihrer Erweiterung unterstützt werden sollen.  Der Text der Beschreibung Ihrer Erweiterung sollte in jeder sprache lokalisiert werden, die Sie deklarieren.  
Wenn Ihre Erweiterung so lokalisiert ist, dass einige Features in einer lokalisierten Version nicht verfügbar sind, müssen Sie die Grenzen der Lokalisierung deutlich in Ihrer Erweiterungsbeschreibung anzeigen. Die von einer Erweiterung bereitgestellte Erfahrung muss in allen unterstützten Sprachen relativ ähnlich sein.  

### 1.8 Finanztransaktionen  

Wenn Ihr Produkt Produktkäufe, Abonnements, virtuelle Währung, Abrechnungsfunktionen oder Finanzinformationen erfasst; Die Anforderungen in den folgenden Abschnitten gelten.  

#### 1.8.1 Kostenpflichtige Features  

Ihre Erweiterung kann Benutzern die Möglichkeit bieten, digitale Inhalte oder Dienste zu nutzen, die über einen Drittanbieterkaufsmechanismus oder eine API erworben wurden.  

Sie müssen eine sichere Drittanbieter-Einkaufs-API für den Kauf physischer Waren oder Dienstleistungen verwenden.  Sie müssen eine sichere Drittanbieter-Einkaufs-API für Zahlungen verwenden, die in Verbindung mit anderen Diensten, einschließlich realer Spiele oder gemeinnütziger Beiträge, vorgenommen werden.  

*   Wenn Ihre Erweiterung verwendet wird, um gemeinnützige Beiträge zu erleichtern oder einzusammeln oder um Werbeauslosungen oder -gewinnspiels zu führen, müssen Sie dies in Übereinstimmung mit dem geltenden Recht tun.  
*   Zudem muss deutlich gemacht werden, dass Microsoft weder als Spendensammler noch als Sponsor der Werbeaktion auftritt.  
*   Produktangebote, die in Ihrer Erweiterung verkauft werden, dürfen nicht in eine rechtlich gültige Währung \(z. B. USD, Euro und so weiter\) oder physische Waren oder Dienstleistungen konvertiert werden.  
    
Die folgenden Anforderungen gelten für die Verwendung einer sicheren Drittanbieter-Einkaufs-API:  

*   Zum Zeitpunkt der Transaktion oder zum Sammeln von Zahlungs- oder Finanzinformationen vom Benutzer; Ihre Erweiterung muss den Handelstransaktionsanbieter identifizieren, den Benutzer authentifizieren und eine Benutzerbestätigung für die Transaktion erhalten.  Ein Handelstransaktionsanbieter verwaltet eine sichere Plattform für Finanzaustausche.  
*   Ihre Erweiterung bietet Benutzern möglicherweise die Möglichkeit, diese Authentifizierung zu speichern. Benutzer müssen jedoch in der Lage sein, entweder eine Authentifizierung für jede Transaktion erforderlich zu machen oder Produkttransaktionen zu deaktivieren.  
*   Wenn Ihre Durchwahl Kreditkarteninformationen erfasst oder einen Drittanbieter zum Sammeln von Kreditkarteninformationen verwendet, muss die Zahlungsverarbeitung den aktuellen PCI Data Security Standard \(PCI DSS\) erfüllen.  
    
#### 1.8.2 Offenlegung kostenpflichtiger Features  

Ihre Erweiterung und die zugehörigen Metadaten müssen Informationen zu den angebotenen Produktkäufen und dem Preisbereich enthalten.  Sie dürfen Die Benutzer nicht irreführen und müssen sich über die Art Ihrer Produktaktionen und -angebote, einschließlich des Umfangs und der Bedingungen von Testerfahrungen, im Klaren sein.  Wenn Ihre Erweiterung den Zugriff auf vom Benutzer erstellte Inhalte während oder nach einer Testversion einschränkt, müssen Sie die Benutzer vorab benachrichtigen.  Darüber hinaus muss Ihre Erweiterung benutzern klar machen, dass sie eine Kaufoption in Ihrer Erweiterung initiieren.  

### 1.9 Benachrichtigungen  

Ihre Erweiterung muss systemeinstellungen für Benachrichtigungen respektieren.  Dies bedeutet, dass jede Präsentation von Anzeigen und Benachrichtigungen für Benutzer mit den Benutzereinstellungen konsistent sein muss, unabhängig davon, ob die Benachrichtigungen vom Microsoft Push Notification Service \(MPNS\), dem Windows Push Notification Service \(WNS\) oder einem anderen Dienst bereitgestellt werden.  Wenn der Benutzer Benachrichtigungen entweder produktspezifisch oder systemweit deaktiviert, muss Ihre Erweiterung funktionsfähig bleiben.  

Wenn Ihr Produkt MPNS oder WNS zum Übermitteln von Benachrichtigungen verwendet, muss es die folgenden Anforderungen erfüllen:  

#### 1.9.1 Allgemeine Anleitung  

Benachrichtigungen, die über WNS oder MPNS bereitgestellt werden, gelten als Produktinhalte und unterliegen allen Add-Ons-Katalogentwicklerrichtlinien.  

#### 1.9.2 Besitz von Benachrichtigungen  

Sie dürfen die Quelle von Benachrichtigungen, die von Ihrer Erweiterung initiiert wurden, nicht verdingen oder versuchen, sie zu verbergen.  

#### 1.9.3 Keine vertraulichen oder vertraulichen Informationen  

Sie dürfen in einer Benachrichtigung keine Informationen enthalten, die Benutzer vertraulich oder vertraulich behandeln können.  

#### 1.9.4 Zweck von Benachrichtigungen  

Benachrichtigungen, die von Ihrer Erweiterung gesendet werden, müssen sich auf diese Erweiterung oder andere Erweiterungen beziehen, die Sie im Microsoft Edge-Add-Ons-Speicher veröffentlichen, und dürfen keine Werbenachrichten jeglicher Art enthalten, die nicht im Zusammenhang mit Ihren Erweiterungen stehen.  

### 1.10 Verhalten und Inhalte von Werbung  

Für alle Aktivitäten im Zusammenhang mit Werbung gelten die folgenden Anforderungen:  

#### 1.10.1 Zweck  

Der Hauptinhalt Ihrer Erweiterung darf keine Werbung sein, und Werbung muss deutlich von anderen Inhalten in Ihrer Erweiterung unterschieden werden.  

#### 1.10.2 Richtlinien und Vereinbarungen  

Alle Werbeinhalte, die Ihre Erweiterung anzeigt, müssen den [Microsoft Creative Acceptance Policy einhalten.][MicrosoftAdvertisingCreativeAcceptancePolicies]  
Wenn Ihre Erweiterung Anzeigen anzeigt, müssen alle angezeigten Inhalte den Werbeanforderungen des [App-Entwicklervertrags][MicrosoftAppDeveloperAgreement] und dieser Richtlinie entsprechen.  

#### 1.10.3 Qualität der Werbung  

*   Der Hauptzweck Ihrer Erweiterung darf nicht sein, Benutzer zum Klicken auf Anzeigen zu erm nen.  
*   Ihre Erweiterung darf nichts tun, was die Sichtbarkeit, den Wert oder die Qualität von anzeigenden Anzeigen beeinträchtigt oder beeinträchtigt.  

#### 1.10.4 Werbeaktionen  

Wenn Sie Werbeanzeigenkampagnen erwerben oder erstellen, um Ihre Erweiterungen über die Anzeigenkampagnenfunktionalität im [Partner Center][MicrosoftPartnerCenter]zu bewerben, müssen alle Anzeigenmaterialien, die Sie Microsoft zur Verfügung stellen, einschließlich aller zugehörigen Angebotsseiten, die Microsoft [Creative Specifications Policy][MicrosoftAdvertisingCreativeSpecifications] und Microsoft Creative Acceptance [Policy][MicrosoftAdvertisingCreativeAcceptancePolicies]entsprechen.  

#### 1.10.5 Benachrichtigen von Benutzern Opt-Out für Interest-Based Werbung  

Ihre Datenschutzbestimmungen oder Nutzungsbedingungen müssen Den Benutzern mitteilen, dass Sie planen, personenbezogene Informationen an den Anzeigendienstanbieter zu senden, und den Benutzern mitteilen, wie sie sich von interessenbasierter Werbung abmelden können.  

#### 1.10.6 Weitere Richtlinien  

Wenn Ihre Erweiterung sich an Kinder unter 13 Jahren richtet, wie im [Children's Online Privacy Protection Act definiert;][FTCChildrensPrivacy] Sie müssen Microsoft im [Partner Center][MicrosoftPartnerCenter] darüber informieren und sicherstellen, dass alle in Ihrer Erweiterung angezeigten Anzeigeninhalte für Kinder unter 13 Jahren geeignet sind.  

## 2 Inhaltsrichtlinien  

Die folgenden Richtlinien gelten für Inhalte und Metadaten \(einschließlich Herausgebername, Erweiterungsname, Erweiterungssymbol, Erweiterungsbeschreibung, Erweiterungsfotos, Erweiterungstrailer und Trailerminiaturansichten sowie alle anderen Erweiterungsmetadaten\), die für die Verteilung in Microsoft Edge-Add-Ons angeboten werden.  Inhalt bedeutet die Bilder, Sounds, Videos und Text in Ihrer Erweiterung, die Kacheln, Benachrichtigungen, Fehlermeldungen oder Anzeigen, die über Ihre Erweiterung verfügbar gemacht werden, und alles, was von einem Server oder mit dem Ihre Erweiterung verbunden ist.  Da Erweiterungen und Microsoft Edge-Add-Ons weltweit verwendet werden, werden diese Anforderungen im Kontext von regionalen und kulturellen Normen interpretiert und angewendet.  

### 2.1 Inhaltsanforderungen für Microsoft Edge Addon Catalog Listing  

Metadaten und andere Inhalte, die Sie zur Begleitung Ihrer Erweiterung übermitteln, enthalten möglicherweise keine ausgereiften Inhalte.  
Übermittlungen, die die Anforderungen an Microsoft Edge-Add-Ons-Speicherauflistungen nicht erfüllen, werden abgelehnt oder umgehend entfernt.  

### 2.2 Inhalt einschließlich Namen, Logos, Original und Drittanbieter  

Alle Inhalte in Ihrer Erweiterung und die zugehörigen Metadaten müssen entweder vom Sie erstellt oder von einem Rechteinhaber eines Drittanbieters entsprechend lizenziert werden und dürfen nur verwendet werden, wenn dies vom Rechteinhaber zulässig oder anderweitig gesetzlich zulässig ist.  

### 2.3 Schadensrisiko  

#### 2.3.1-Anforderungen  

Ihre Erweiterung darf keine Inhalte enthalten, die die folgenden aktivitäten in der realen Welt erleichtern oder verfechten: \(a\) extreme oder unanfechtliche Gewalt; \(b\) Verstöße gegen die Menschenrechte; \(c\) die Erstellung illegaler Waffen; oder \(d\) die Verwendung von Waffen gegen eine Person, ein Tier oder ein echtes oder persönliches Eigentum.  

#### 2.3.2 Verantwortung  

Ihre Erweiterung darf nicht: \(a\) ein Sicherheitsrisiko darstellen oder zu Unannehmlichkeiten, Verletzungen oder sonstigen Schäden für Endbenutzer oder andere Personen oder Tiere führen; oder \(b\) ein Risiko oder eine Beschädigung des tatsächlichen oder persönlichen Eigentums darstellen.  Sie sind allein für alle Erweiterungssicherheitstests, den Zertifikaterwerb und die Implementierung der entsprechenden Funktionsschutzmechanismen verantwortlich.  Sie dürfen keine Sicherheits- oder Komfortfeatures der Plattform deaktivieren, und Sie müssen alle anwendbaren gesetzlich vorgeschriebenen und branchenüblichen Warnungen, Hinweise und Haftungsausschlüsse in Ihre Erweiterung einschlussen.  

### 2.4 Verleumdung, Verleumdung, Verleumdung, Verleumdung und Bedrohung  

Ihre Erweiterung darf keine Inhalte enthalten, die verleumderisch, verleumderisch, verleumderisch oder bedrohlich sind.  

### 2.5 Anstößige Inhalte  

Ihre Erweiterung und die zugehörigen Metadaten dürfen keine potenziell vertraulichen oder anstößigen Inhalte enthalten.  Inhalte können aufgrund von lokalen Gesetzen oder kulturellen Normen in bestimmten Ländern/Regionen als vertraulich oder anstößig betrachtet werden.  Darüber hinaus dürfen Ihre Erweiterung und die zugehörigen Metadaten keine Inhalte enthalten, die Sich für Diskriminierung, Hass oder Gewalt auf der Grundlage von Überlegungen zu Rasse, Ethnischer Herkunft, nationaler Herkunft, Sprache, Geschlecht, Alter, Behinderung, Religiöser, sexueller Ausrichtung, Status als Veteran oder Mitgliedschaft in einer anderen sozialen Gruppe aussprechen.  

### 2.6 Alkohol, Tabak und Drogen  

Ihre Erweiterung darf keine Inhalte enthalten, die den übermäßigen oder unverantwortlichen Konsum von Alkohol oder Tabakprodukten oder -rauschmitteln erleichtern oder verfeinern.  

### 2.7 Inhalte für Erwachsene  

Ihre Erweiterung darf keine Inhalte enthalten oder anzeigen, die eine angemessene Person als pornografische oder sexuell explizit betrachten würde.  

### 2.8 Verbotene Inhalte, Dienste und Aktivitäten  

Ihre Erweiterung muss die folgenden Bedingungen erfüllen.  

*   Ihre Erweiterung darf keine Inhalte enthalten oder Dienste bereitstellen, die Onlinespiele erleichtern.  Onlinespiel umfasst, ist aber nicht auf Onlinecasinos, Sportwetten, Lottospiele oder Geschicklichkeitsspiele beschränkt, die Geldpreise oder einen anderen Wert bieten.  
*   Ihre Erweiterung darf keinen nicht autorisierten Zugriff auf Websiteinhalte bereitstellen, z. B. durch Umgehen von Paywalls oder Anmeldeeinschränkungen.  
*   Ihre Erweiterung darf den nicht autorisierten Zugriff, das Herunterladen oder Streaming von urheberrechtlich geschützten Inhalten oder Medien nicht bereitstellen, fördern oder aktivieren.  
*   Ihre Erweiterung darf keine Kryptokryptografie minen.  
    
### 2.9 Unzulässige Aktivitäten  

Ihre Erweiterung darf keine Inhalte oder Funktionen enthalten, die unrechtmäßige Aktivitäten in der realen Welt fördern, erleichtern oder verfechten.  

### 2.10 Übermäßige Anstößigkeit und unangemessene Inhalte  

*   Ihre Erweiterung darf keine exzessive oder überflüssige Ansässigkeit enthalten.  
*   Ihre Erweiterung darf keine Inhalte enthalten oder anzeigen, die eine angemessene Person als obszön betrachtet.  
    
### 2.11 Länder-/Regionenspezifische Anforderungen  

Inhalte, die in jedem Land/jeder Region, für das Ihre Erweiterung zielgerichtet ist, anstößig sind, sind nicht zulässig.  Inhalte können aufgrund lokaler Gesetze oder kultureller Normen in bestimmten Ländern/Regionen als beleidigend angesehen werden.  Beispiele für potenziell beleidigende Inhalte in bestimmten Ländern/Regionen:  

**China**  

*   Verbot pornographischer Inhalte  
*   Verweise auf umstrittene Gebiete oder Regionen  
*   Bereitstellung oder Zugriff auf Inhalte oder Dienste, die unter dem jeweils anwendbaren Recht rechtswidrig sind.  
    
### 2.12 Altersfreigaben  

#### 2.12.1 Ausgereifte Inhalte  

Wenn Sie Ihre Erweiterung an [Partner Center][MicrosoftPartnerCenter]übermitteln, müssen Sie angeben, ob ihre Erweiterung Inhalte anzeigt, die als "Reifen" gekennzeichnet werden sollen.  Berücksichtigen Sie bei der Festlegung der Bewertung für Ihre Erweiterung alle Inhalte in Ihrer App, einschließlich vom Benutzer generierter Inhalte und Anzeigen sowie die Inhalte, auf die Ihre Erweiterung verknüpft ist.  Wenn Sie angeben, dass Ihre Erweiterung keine "ausgereiften" Inhalte enthält, sind Sie für die Beibehaltung der Genauigkeit dieser Bewertung verantwortlich.  Unabhängig von der Bewertung Ihrer Erweiterung muss sie weiterhin alle Inhaltsanforderungen von Microsoft Edge-Add-Ons-Entwicklerrichtlinien erfüllen.  

#### 2.12.2 Bewertungsänderung  

Wenn Ihre Erweiterung Inhalte \(z. B. vom Benutzer generierte, Einzelhandels- oder andere webbasierte Inhalte\) enthält, die möglicherweise für eine höhere Altersfreigabe als die zugewiesene Bewertung geeignet sind, müssen Sie von Benutzern verlangen, dass sie sich für den Erhalt solcher Inhalte entscheiden, indem Sie einen Inhaltsfilter verwenden oder sich mit einem bereits vorhandenen Konto anmelden.  

### 2.13 Videos  

Wenn Sie ein Werbevideo im Eintrag übermitteln, sollte es alle in dieser Richtlinie genannten Inhaltsrichtlinien befolgen.  Wenn Sie einen YouTube-Link bereitstellen möchten, müssen Sie sicherstellen, dass Werbung für die bestimmten Videos deaktiviert ist, die Sie einbetten möchten.  Weitere Informationen dazu, wie Anzeigen auf YouTube aktiviert und [deaktiviert][GoogleYoutubeAnswer132596]werden, finden Sie unter [support.google.com/youtube/answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] und support.google.com/youtube/answer/132596 .  

<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Lockerung der Standardrichtlinie – Inhaltssicherheitsrichtlinie \(CSP\) | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "App Developer Agreement | Microsoft Docs"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Wie Microsoft Schadsoftware und potenziell unerwünschte Anwendungen identifiziert, | Microsoft Docs"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Festlegen Ihrer Standardanzeigeformate – YouTube-Hilfe"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anzeigen in eingebetteten Videos – YouTube-Hilfe"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Datenschutz für Kinder – Federal Trade Commission"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Richtlinien für kreative Akzeptanz – Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Kreative Spezifikationen – Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
