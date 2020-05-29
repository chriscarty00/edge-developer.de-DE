---
description: Microsoft Edge Addons-Katalog-Entwicklerrichtlinien.
title: Microsoft Edge Addons-Katalog-Entwicklerrichtlinien
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: be159491d892c176a8439393573dc23680fac377
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607433"
---
# Microsoft Edge Addons-Katalog-Entwicklerrichtlinien  

## Einführung und Ziel dieses Dokuments  

Vielen Dank für Ihr Interesse an der Entwicklung von Erweiterungen für den Microsoft Edge Addons-Katalog.  Die Microsoft Edge Addons-Katalog-Entwicklerrichtlinien \ (Addons-Katalog-Entwicklerrichtlinien \) gelten für Ihre Erweiterungen, einschließlich ihrer Übermittlung von Erweiterungen über das [Partner Center][MicrosoftPartnerCenter] und die Bereitstellungsolcher Erweiterungen über die Microsoft Edge-Add-ons.  

## Prinzipien  

Zunächst einige wichtige Grundregeln:  

*   Sie sollten innerhalb Ihrer Erweiterungen für Microsoft Edge einen eindeutigen und eindeutigen Wert anbieten.  Bieten Sie einen zwingenden Grund, Ihre Erweiterungen aus dem Microsoft Edge Addons-Katalog herunterzuladen \ (Microsoft Edge Addons \).  
*   Sie dürfen die gemeinsamen Benutzer nicht darüber täuschen, was Ihre Erweiterung tut, wer Sie anbietet usw.  
*   Sie dürfen nicht versuchen, Benutzer, das System oder das Ökosystem zu betrügen.  Es gibt keinen Platz in unseren Microsoft Edge-Addons für jegliche Art von Betrug. seien es Bewertungen und Überprüfung von Manipulationen, Kreditkartenbetrug oder anderen betrügerischen Aktivitäten.  

Durch die Einhaltung dieser Addons-Katalog-Entwicklerrichtlinien sollten Sie Entscheidungen treffen können, die die Attraktivität und das Publikum ihrer Erweiterung verbessern.  

Ihre Erweiterungen sind entscheidend für die Erfahrung von Hunderten von Millionen von Benutzern.  Wir freuen uns darauf, das zu erleben, was Sie schaffen, und freuen uns, Ihnen bei der Bereitstellung Ihrer Erweiterungen zur Welt zu helfen.  

## 1. Produktrichtlinien  

### 1,1 Distinct-Funktion & Wert; Genaue Darstellung  

Ihre Erweiterung und die zugehörigen Metadaten müssen die Quelle, die Funktionalität und die Features, die Sie beschreiben, genau und deutlich widerspiegeln.  

#### 1.1.1 Erweiterungen müssen einen einzigen Zweck haben  

Ihre Erweiterung muss einen einzigen Zweck mit eingeschränkter Funktionalität aufweisen.  

#### 1.1.2 Beschreibung ihrer Erweiterung  

Alle Aspekte ihrer Erweiterung sollten die Funktionen, Funktionen und wichtigen Einschränkungen ihrer Erweiterung, einschließlich erforderlicher oder unterstützter Eingabegeräte, genau beschreiben.  Der Wert Vorschlag für Ihre Erweiterung muss während der ersten Ausführung klar sein.  Ihre Erweiterung darf keinen Namen oder ein Symbol ähnlich wie bei anderen Erweiterungen verwenden und darf nicht behaupten, ein Unternehmen, eine staatliche Einrichtung oder eine andere Einrichtung zu vertreten, wenn Sie nicht berechtigt sind, diese Vertretung zu veranlassen.  

#### 1.1.3-Funktionalität  

Ihre Erweiterung muss voll funktionsfähig sein.  

#### 1.1.4 suchen und entdecken  

Suchbegriffe dürfen sieben eindeutige Begriffe nicht überschreiten und sollten für Ihre Erweiterung relevant sein.  

#### 1.1.5 angemessene Angaben liefern  

Sie müssen unterschiedliche und informative Informationen zu ihrer Erweiterung und den Funktionen im Eintrag \ (Metadaten \) für Ihre Erweiterung angeben.  Ihre Erweiterung muss eine wertvolle und hochwertige Benutzererfahrung bieten.  Ihre Erweiterung muss auch in Microsoft Edge-Addons aktiv sein.  

#### 1.1.6 Stabilität und Leistung  

Ihre Erweiterung darf sich nicht negativ auf die Leistung oder Stabilität von Microsoft Edge auswirken.  

#### 1.1.7-Verschleierung  

Erweiterungen mit verborgenem Code sind nicht zulässig.  Dazu gehören Code innerhalb des Erweiterungspakets sowie alle externen Codes oder Ressourcen, die aus dem Internet abgerufen werden.  Sie werden möglicherweise aufgefordert, Teile Ihres Codes zu umgestalten, wenn diese nicht überarbeitet werden können.  

#### 1.1.8 ändern von Browser Einstellungen  

Ihre Erweiterung darf keine Browserfunktionen oder-Einstellungen, einschließlich, aber nicht eingeschränkt auf: der Adressleisten-Suchanbieter und-Vorschläge, die Start-oder Startseite, die neue Registerkarte und das Hinzufügen oder Entfernen von Favoriten, **ohne die entsprechende Zustimmung des Benutzers**ändern oder diese ändern.  

Eine Änderung der Browsereinstellungen sollte in der Beschreibung der Erweiterung ausdrücklich dokumentiert werden.  

Ihre Erweiterung kann nur die Schlüsseleinstellungen überprüfen, um eine Microsoft-Webseite oder einen Dienst durch die eines Drittanbieters zu ersetzen, wie beispielsweise die Verwendung einer Drittanbieter-Suchmaschine oder das Festlegen der Startseite auf eine Drittanbieter-webeigenschaft, wenn Sie mit dieser Drittpartei beschäftigt oder anderweitig verbunden sind.  

### 1,2-Sicherheit  

Ihre Erweiterung darf die Benutzersicherheit oder die Sicherheit oder Funktionalität des Geräts, des Systems oder verwandter Systeme nicht gefährden oder gefährden.  

#### 1.2.1 Inhalts Sicherheitsrichtlinien  

> [!NOTE]
> Wenn Sie Änderungen an ihrer Erweiterung über die beschriebene Funktionalität hinaus vornehmen, müssen alle Änderungen am Code mit der [Sicherheitsrichtlinie für Microsoft Edge-Inhalte][MicrosoftEdgeContentSecurityPolicyRemoteScript]kompatibel sein.  Beispiel: Ihre Erweiterung sollte kein Remoteskript herunterladen und anschließend das Skript auf eine Weise ausführen, die nicht mit den beschriebenen Funktionen konsistent ist.  

#### 1.2.2 unerwünschte und bösartige Software  

Ihre Erweiterung darf keine Malware enthalten oder aktivieren, wie Sie in den Microsoft-Kriterien für [unerwünschte und bösartige Software][MicrosoftIdentifiesMalwareUnwantedApplications]definiert ist.  

#### 1.2.3 Abhängigkeit von anderer Software  

Ihre Erweiterung kann von nicht integrierter Software (wie einem anderen Produkt, Modul oder Dienst) abhängen, um die primäre Funktionalität bereitzustellen, vorausgesetzt, Sie geben die Abhängigkeit in der Beschreibung an.  

#### 1.2.4-Erweiterungen aktualisieren  

Sofern von Microsoft nicht anderweitig zugelassen, müssen Ihre Erweiterungen nur über Microsoft Edge-Add-ons aktualisiert werden.  

### 1,3-Produkt kann getestet werden  
Die Erweiterung muss getestet werden.  Wenn es nicht möglich ist, ihre Erweiterung aus irgendeinem Grund zu testen, einschließlich, aber nicht darauf, die nachstehenden Elemente zu begrenzen, kann Ihre Erweiterung diese Anforderung nicht erfüllen.  

#### 1.3.1 Benutzeranmeldeinformationen  
Wenn für Ihre Erweiterung Anmeldeinformationen erforderlich sind, geben Sie ein funktionierendes Demokonto unter Verwendung des Felds **Hinweise für Zertifizierung** ein.  

#### 1.3.2 Verfügbarkeit von Diensten  

Wenn für Ihre Erweiterung Zugriff auf einen Server erforderlich ist, muss der Server funktionsfähig sein, um sicherzustellen, dass er ordnungsgemäß funktioniert.  

### 1,4 Usability  

Ihre Erweiterung muss den Erweiterungsspeicher Standards für die Benutzerfreundlichkeit entsprechen, einschließlich, aber nicht ausschließlich, die in den folgenden Unterabschnitten aufgeführt sind.  

#### 1.4.1 plattformübergreifende Kompatibilität  

Erweiterungen sollten mit Microsoft Edge auf allen Geräten und Plattformen kompatibel sein, auf denen Sie heruntergeladen werden können.  Wenn eine Erweiterung auf einem Gerät heruntergeladen wird, mit dem Sie nicht kompatibel ist, sollte Sie diese beim Start erkennen und eine Meldung an den Benutzer anzeigen, in der die Anforderungen aufgeführt sind, die die Geräte erfüllen müssen, damit Sie mit ihrer Erweiterung kompatibel sind.  

#### 1.4.2 Benutzererfahrung  

Die Erweiterung muss sofort gestartet werden und muss für die Benutzereingabe ansprechbar sein.  Erweiterungen müssen weiterhin ausgeführt werden und reagieren weiterhin auf die Benutzereingabe.  Erweiterungen müssen ordnungsgemäß heruntergefahren und nicht unerwartet geschlossen werden.  Die Erweiterung sollte Ausnahmen behandeln und weiterhin auf Benutzereingaben reagieren, nachdem die Ausnahme behandelt wurde.  

### 1,5 personenbezogene Informationen  

Die folgenden Anforderungen gelten für Erweiterungen, die auf persönliche Informationen zugreifen.  Zu den personenbezogenen Informationen gehören alle Informationen oder Daten, die zur Identifizierung einer Person oder zur Verwendung solcher Informationen oder Daten verwendet werden können.  

#### 1.5.1 Erfassen persönlicher Informationen nur bei Bedarf  

Ihre Erweiterung kann persönliche Informationen erfassen, darauf zugreifen, Sie verwenden oder übertragen \ (einschließlich der Aktivitäten im Web-Browsing \); nur bei Bedarf von und nur zur Verwendung in einer prominent offenbarten, nutzerorientierten Funktion.  

#### 1.5.2 aufrecht erhalten einer Datenschutzrichtlinie  

Unabhängig davon, ob Ihre Durchwahl personenbezogene Informationen zugreift, sammelt oder überträgt; Wenn gesetzlich vorgeschrieben, müssen Sie Ihre Datenschutzrichtlinien bekannt machen und diese einhalten.  Ihre Datenschutzrichtlinien müssen die Nutzer über die persönlichen Informationen informieren, die von ihrer Durchwahl abgerufen, erfasst oder übertragen werden, wie diese Informationen verwendet, gespeichert und gesichert werden, und die Typen der Parteien angeben, denen Sie bekannt gegeben werden.  Ihre Datenschutzrichtlinien müssen die Steuerelemente beschreiben, die Nutzer über die Nutzung und die Weitergabe Ihrer Informationen haben, wie Sie auf Ihre Informationen zugreifen, und Sie müssen die geltenden Gesetze und Vorschriften einhalten.  Ihre Datenschutzrichtlinien müssen auf dem neuesten Stand gehalten werden, wenn Sie Ihrer Erweiterung neue Funktionen und Funktionen hinzufügen.  

Wenn Sie Microsoft Ihre Datenschutzrichtlinien zur Verfügung stellen, erklären Sie sich damit einverstanden, Microsoft die Möglichkeit zu geben, diese Datenschutzrichtlinien mit Nutzern ihrer Durchwahl zu teilen.  

#### 1.5.3 Freigeben von Daten an Dritte  

Sie können die persönlichen Informationen der Nutzer ihrer Durchwahl an einen externen Dienst oder Drittanbieter über Ihre Erweiterung oder zugehörige Metadaten nur veröffentlichen, nachdem Sie die Zustimmung dieser Nutzer erhalten haben.  Einwilligung in die Zustimmung bedeutet, dass die Benutzer Ihre ausdrückliche Genehmigung auf der Benutzeroberfläche Ihrer Durchwahl für die angeforderte Aktivität erteilen, nachdem Sie:  

*   Beschreiben Sie Ihren Benutzern, wie die Informationen abgerufen, verwendet oder freigegeben werden, und geben Sie an, welche Arten von Parteien Sie offen legen, und  
*   Stellen Sie Ihren Benutzern einen Mechanismus auf der Benutzeroberfläche der Erweiterung zur Verfügung, über den Sie die Möglichkeit haben, die Berechtigung später zu widerrufen und abzumelden.  

#### 1.5.4 Freigeben von Informationen für nicht-Benutzer  

Wenn Sie die persönlichen Informationen einer Person über Ihre Erweiterung oder die Metadaten an einen externen Dienst oder Drittanbieter veröffentlichen, die Person, deren Informationen freigegeben werden, jedoch kein Nutzer ihrer Durchwahl ist;  

1.  Sie müssen die ausdrückliche schriftliche Zustimmung zur Veröffentlichung dieser personenbezogenen Informationen erhalten.  
1.  Sie müssen der Person, deren Informationen freigegeben sind, die Zustimmung jederzeit zurückziehen.  
1.  Ihre Datenschutzrichtlinie muss klar offen legen, dass Sie personenbezogene Informationen auf diese Weise erfassen können.  
1.  Wenn dies nach geltendem Recht erforderlich ist, müssen Sie die persönlichen Informationen jeder Person auf Anfrage löschen, einschließlich Personen, deren Informationen Sie auf diese Weise sammeln.  
1.  Wenn Ihre Erweiterung Benutzern den Zugriff auf die persönlichen Informationen einer anderen Person gewährt, gilt diese Anforderung auch.  

#### 1.5.5 Informationen sicher übertragen  

Wenn Ihre Durchwahl personenbezogene Informationen sammelt, speichert oder überträgt; Dies muss mithilfe moderner kryptografischer Methoden sicher erfolgen.  

#### 1.5.6 hochsensible Informationen  

Ihre Erweiterung darf keine vertraulichen persönlichen Informationen wie Gesundheits-oder Finanzdaten erfassen, speichern oder übertragen, es sei denn, die Informationen beziehen sich auf die Funktionalität ihrer Erweiterung.  Ihre Erweiterung muss auch die ausdrückliche Zustimmung des Nutzers einholen, bevor diese Informationen gesammelt, gespeichert oder übermittelt werden.  

### 1,6-Berechtigungen  

Ihre Erweiterung darf nur die Berechtigungen anfordern, die für die Funktion erforderlich sind.  Sie müssen eine Beschreibung der Funktionsweise der Erweiterung angeben.  Ihre Erweiterung darf nur wie beschrieben ausgeführt werden.  Ihre Erweiterung fordert möglicherweise keine Berechtigung für Funktionen an, die über die Funktionen hinausgehen, die für die Ausführung und Funktion als deklariert erforderlich sind.  

### 1,7-Lokalisierung  

Sie sollten die Erweiterung für alle Sprachen lokalisieren, die von der Erweiterung unterstützt werden.  Der Text der Beschreibung ihrer Erweiterung sollte in jeder von Ihnen deklarierten Sprache lokalisiert werden.  
Wenn Ihre Erweiterung so lokalisiert ist, dass einige Features in einer lokalisierten Version nicht zur Verfügung stehen, müssen Sie die Grenzwerte für die Lokalisierung in der Erweiterungsbeschreibung klar angeben oder anzeigen. Die Erfahrung, die durch eine Erweiterung bereitgestellt wird, muss in allen unterstützten Sprachen relativ ähnlich sein.  

### 1,8 Finanztransaktionen  

Wenn Ihr Produkt in-Product-Käufe, Abonnements, virtuelle Währung, Abrechnungsfunktionen oder erfasste Finanzinformationen umfasst; Es gelten die Anforderungen in den folgenden Abschnitten.  

#### 1.8.1 kostenpflichtige Funktionen  

Ihre Erweiterung kann es Benutzern ermöglichen, digitale Inhalte oder Dienste zu nutzen, die über einen Kauf Mechanismus oder eine API eines Drittanbieters erworben wurden.  

Sie müssen eine sichere Drittanbieter-Kauf-API für den Kauf von physischen Gütern oder Dienstleistungen verwenden.  Sie müssen eine sichere Drittanbieter-Kauf-API für Zahlungen verwenden, die in Verbindung mit anderen Dienstleistungen wie realen Glücksspielen oder gemeinnützigen Beiträgen getätigt wurden.  

*   Wenn Ihre Verlängerung zur Erleichterung oder Sammlung von gemeinnützigen Beiträgen oder zur Durchführung von Werbe Verlosungen oder Wettbewerben verwendet wird, müssen Sie dies unter Beachtung des anwendbaren Rechts tun.  
*   Zudem muss deutlich gemacht werden, dass Microsoft weder als Spendensammler noch als Sponsor der Werbeaktion auftritt.  
*   In ihrer Verlängerung verkaufte Produktangebote dürfen nicht in eine rechtlich gültige Währung (wie USD, Euro usw.) oder physische waren oder Dienstleistungen umgewandelt werden.  

Die folgenden Anforderungen gelten für ihre Verwendung einer sicheren Drittanbieter-Kauf-API:  

*   Zum Zeitpunkt der Transaktion oder wenn Sie Zahlungs-oder Finanzinformationen des Nutzers einholen; Ihre Durchwahl muss den Commerce-Transaktions Anbieter identifizieren, den Benutzer authentifizieren und die Bestätigung des Benutzers für die Transaktion anfordern.  Ein Commerce-Transaktions Anbieter pflegt eine sichere Plattform für Finanz Börsen.  
*   Ihre Erweiterung bietet Benutzern möglicherweise die Möglichkeit, diese Authentifizierung zu speichern, aber die Benutzer müssen die Möglichkeit haben, bei jeder Transaktion eine Authentifizierung zu verlangen oder in-Product-Transaktionen zu deaktivieren.  
*   Wenn Ihre Durchwahl Kreditkarteninformationen sammelt oder einen externen Zahlungsprozessor verwendet, der Kreditkarteninformationen sammelt, muss die Zahlungsabwicklung den aktuellen PCI-Daten Sicherheits Standard erfüllen \ (PCI DSS).  

#### 1.8.2 Offenlegung bezahlter Funktionen  

Ihre Erweiterung und die zugehörigen Metadaten müssen Informationen zu den Arten von in-Product-Käufen und dem Preisbereich bereitstellen.  Sie dürfen die Nutzer nicht in die Irre führen und müssen sich über die Art ihrer in-Product-Werbeaktionen und-Angebote sowie über den Umfang und die Ausdrücke der Test Erfahrungen klar sein.  Wenn Ihre Erweiterung den Zugriff auf vom Benutzer erstellte Inhalte während oder nach einer Testversion einschränken soll, müssen Sie die Benutzer im Voraus benachrichtigen.  Darüber hinaus muss Ihre Erweiterung Benutzern deutlich machen, dass Sie eine Kaufoption in der Erweiterung initiieren.  

### 1,9-Benachrichtigungen  

Ihre Erweiterung muss die Systemeinstellungen für Benachrichtigungen beachten.  Das bedeutet, dass jede Präsentation von anzeigen und Benachrichtigungen für Benutzer mit den Benutzereinstellungen konsistent sein muss, unabhängig davon, ob die Benachrichtigungen vom Microsoft Push Notification Service \ (MPNS \), Windows Push Notification Service \ (WNS \) oder einem anderen Dienst bereitgestellt werden.  Wenn der Benutzer Benachrichtigungen entweder auf produktspezifischer oder auf Systemebene deaktiviert, muss Ihre Erweiterung funktionsfähig bleiben.  

Wenn Ihr Produkt MPNS oder WNS zum Übertragen von Benachrichtigungen verwendet, muss es die folgenden Voraussetzungen erfüllen:  

#### 1.9.1 Allgemeine Anleitungen  

Benachrichtigungen, die über WNS oder MPNS bereitgestellt werden, gelten als Produktinhalte und unterliegen allen Addons-Katalog-Entwicklerrichtlinien.  

#### 1.9.2 Besitz von Benachrichtigungen  

Sie dürfen die Quelle jeder Benachrichtigung, die von ihrer Erweiterung initiiert wurde, nicht verschleiern oder verschleiern.  

#### 1.9.3 keine vertraulichen oder sensiblen Informationen  

Sie dürfen in einer Benachrichtigung keine Informationen angeben, die Benutzer möglicherweise als vertraulich oder vertraulich empfinden.  

#### 1.9.4 Zweck von Benachrichtigungen  

Benachrichtigungen, die von ihrer Durchwahl gesendet werden, müssen sich auf diese Erweiterung oder auf andere Erweiterungen beziehen, die Sie im Microsoft Edge Addons-Katalog veröffentlichen, und dürfen keine Werbebotschaften jeglicher Art enthalten, die nicht mit ihren Erweiterungen in Verbindung stehen.  

### 1,10 Werbeverhalten und Inhalte  

Für alle Aktivitäten im Zusammenhang mit Werbung gelten die folgenden Anforderungen:  

#### 1.10.1 Zweck  

Der Hauptinhalt ihrer Erweiterung darf keine Werbung sein, und Werbung muss deutlich von anderen Inhalten in ihrer Erweiterung unterschieden werden.  

#### 1.10.2-Richtlinien und-Vereinbarungen  

Alle Werbungs Inhalte, die ihre Erweiterung anzeigt, müssen der [Microsoft Creative Acceptance Policy][MicrosoftAdvertisingCreativeAcceptancePolicies]unterliegen.  
Wenn Ihre Erweiterung anzeigen anzeigt, müssen alle angezeigten Inhalte den Werbeanforderungen der [App-Entwickler Vereinbarung][MicrosoftAppDeveloperAgreement] und dieser Richtlinie entsprechen.  

#### 1.10.3 Qualität der Werbung  

*   Der Hauptzweck ihrer Erweiterung darf nicht darin liegen, dass Benutzer zum Klicken auf anzeigen gelangen.  
*   Ihre Erweiterung darf nichts tun, was die Sichtbarkeit, den Wert oder die Qualität von anzeigen beeinträchtigt oder vermindert.  

#### 1.10.4-Werbeaktionen  

Wenn Sie Werbekampagnen kaufen oder erstellen, um Ihre Erweiterungen über die Anzeigenkampagnen Funktionalität im [Partner Center][MicrosoftPartnerCenter]zu promoten, müssen alle anzeigen Materialien, die Sie für Microsoft bereitstellen, einschließlich aller zugehörigen Zielseiten, den Richtlinien für die [Microsoft Creative-Spezifikationen][MicrosoftAdvertisingCreativeSpecifications] und die [Microsoft Creative-Akzeptanz Richtlinie][MicrosoftAdvertisingCreativeAcceptancePolicies]entsprechen.  

#### 1.10.5 Benachrichtigung der Nutzer über das ablehnen für Interessenbasierte Werbung  

Ihre Datenschutzbestimmungen oder Nutzungsbedingungen müssen Benutzern mitteilen, dass Sie beabsichtigen, personenbezogene Informationen an den Anzeigendienst Anbieter zu senden, und Benutzern mitzuteilen, wie Sie die Interessenbasierte Werbung ablehnen können.  

#### 1.10.6 Sonstige Richtlinien  

Wenn Ihre Durchwahl an Kinder unter 13 Jahren gerichtet ist, wie Sie im [Online-schutzgesetz für Kinder][FTCChildrensPrivacy]festgelegt sind; Sie müssen Microsoft diese Tatsache im [Partner Center][MicrosoftPartnerCenter] mitteilen und sicherstellen, dass alle in ihrer Erweiterung angezeigten Anzeigeninhalte für Kinder unter 13 Jahren geeignet sind.  

## 2 Inhaltsrichtlinien  

Die folgenden Richtlinien gelten für Inhalte und Metadaten \ (einschließlich Herausgebername, Erweiterungsname, Erweiterungssymbol, Erweiterungsbeschreibung, Screenshots für Erweiterungen, Erweiterungs Anhänger und Miniaturansichten des Trailers sowie alle anderen Erweiterungs Metadaten \), die in Microsoft Edge-Add-ons zur Verfügung gestellt werden.  Inhalt bezieht sich auf die Bilder, Sounds, Videos und Text in der Erweiterung, die Kacheln, Benachrichtigungen, Fehlermeldungen oder anzeigen, die über Ihre Erweiterung bereitgestellt werden, und alles, was von einem Server geliefert wird oder mit dem die Erweiterung verbunden ist.  Da Erweiterungen und Microsoft Edge-Add-ons weltweit verwendet werden, werden diese Anforderungen im Kontext regionaler und kultureller Normen interpretiert und angewendet.  

### 2,1-Inhaltsanforderungen für den Microsoft Edge Addon-Katalogeintrag  

Metadaten und andere Inhalte, die Sie Ihrer Erweiterung beifügen, enthalten möglicherweise keine ausgereiften Inhalte.  
Übermittlungen, die die Anforderungen des Erweiterungsspeichers nicht erfüllen, werden abgelehnt oder umgehend entfernt.  

### 2,2-Inhalte, einschließlich Namen, Logos, Original und Drittanbietern  

Der gesamte Inhalt ihrer Erweiterung und zugehöriger Metadaten muss entweder ursprünglich von Ihnen erstellt oder von einem Rechteinhaber Dritter angemessen lizenziert werden und darf nur wie vom Rechteinhaber zugelassen oder im gesetzlich zulässigen Rahmen verwendet werden.  

### 2,3 Risiko von Schaden  

#### 2.3.1 Voraussetzungen  

Ihre Erweiterung darf keine Inhalte enthalten, die die folgenden realen Aktivitäten erleichtern oder glamorizes: \ (a \) Extreme oder unentgeltliche Gewalt; \ (b \) Verletzungen der Menschenrechte; \ (c \) die Schaffung von illegalen Waffen; oder \ (d \) die Verwendung von Waffen gegen eine Person, ein Tier oder ein echtes oder persönliches Eigentum.  

#### 2.3.2 Verantwortlichkeit  

Ihre Erweiterung darf nicht sein: \ (a \) stellen Sie ein Sicherheitsrisiko dar, das nicht zu Unbehagen, Verletzungen oder sonstigem Schaden für Endnutzer oder andere Personen oder Tiere führen kann. oder \ (b \) stellen ein Risiko dar oder führen zu Schäden an einer realen oder persönlichen Eigenschaft.  Sie tragen die alleinige Verantwortung für alle Sicherheitsprüfungen bei der Erweiterung, die Zertifikat Erfassung und die Implementierung der entsprechenden Funktionsgarantien.  Sie dürfen keine Plattformsicherheit oder Komfortfunktionen deaktivieren, und Sie müssen alle anwendbaren gesetzlichen und branchenüblichen Warnungen, Hinweise und Haftungsausschlüsse in ihrer Durchwahl angeben.  

### 2,4 diffamierenden, verleumderischen, verleumderischen und bedrohlichen  

Ihre Erweiterung darf keine diffamierenden, verleumderischen, verleumderischen oder bedrohlichen Inhalte enthalten.  

### 2,5 anstößiger Inhalt  

Ihre Erweiterung und die zugehörigen Metadaten dürfen keine potenziell sensiblen oder anstößigen Inhalte enthalten.  Inhalte können aufgrund örtlicher Gesetze oder kultureller Normen in bestimmten Ländern/Regionen als sensibel oder beleidigend eingestuft werden.  Darüber hinaus dürfen Ihre Erweiterung und die zugehörigen Metadaten keine Inhalte enthalten, die sich auf Diskriminierung, Hass oder Gewalt Gründen, die auf Überlegungen hinsichtlich Rasse, Ethnizität, nationaler Herkunft, Sprache, Geschlecht, Alter, Behinderung, Religion, sexueller Orientierung, Status als Veteran oder Mitgliedschaft in einer anderen sozialen Gruppe beruhen.  

### 2,6 Alkohol, Tabak und Drogen  

Ihre Erweiterung darf keine Inhalte enthalten, die zu einer exzessiven oder unverantwortlichen Verwendung von Alkohol oder glamorizes oder Medikamenten führen.  

### 2,7 Adult-Inhalte  

Ihre Erweiterung darf keine Inhalte enthalten oder anzeigen, die eine vernünftige Person als pornographische oder sexuell explizit einschätzen würde.  

### 2,8 verbotene Inhalte, Dienste und Aktivitäten  

Ihre Durchwahl muss die folgenden Bedingungen erfüllen:  

*   Ihre Erweiterung darf keine Inhalte enthalten oder Dienste bereitstellen, die das Online-spielen erleichtern.  Online-Glücksspiel umfasst aber nicht nur Online-Casinos, Sportwetten, Lotterien oder Geschicklichkeitsspiele, die Preise von Bargeld oder anderen Werten anbieten.  
*   Ihre Erweiterung darf keinen unbefugten Zugriff auf Websiteinhalte ermöglichen, beispielsweisedurch Umgehung von bezahlschranken-oder Login-Einschränkungen.  
*   Ihre Erweiterung darf den unbefugten Zugriff, den Download oder das Streaming urheberrechtlich geschützter Inhalte oder Medien nicht bereitstellen, fördern oder aktivieren.  
*   Ihre Durchwahl darf cryptocurrency nicht abbauen.  

### 2,9 illegale Aktivitäten  

Ihre Erweiterung darf keine Inhalte oder Funktionen enthalten, die illegale Aktivitäten in der realen Welt ermutigen, erleichtern oder glamorizes.  

### 2,10 übermäßige Obszönitäten und ungeeignete Inhalte  

*   Ihre Erweiterung darf keine exzessiven oder unentgeltlichen Obszönitäten enthalten.  
*   Ihre Erweiterung darf keine Inhalte enthalten oder anzeigen, die eine vernünftige Person für obszön hält.  

### 2,11 spezifische Anforderungen für Länder/Regionen  

Inhalte, die in allen Ländern/Regionen beleidigend sind, auf die ihre Erweiterung ausgerichtet ist, sind nicht zulässig.  Inhalte können aufgrund lokaler Gesetze oder kultureller Normen in bestimmten Ländern/Regionen als beleidigend angesehen werden.  Beispiele für potenziell beleidigende Inhalte in bestimmten Ländern/Regionen:  

**China**  

*   Verbot pornographischer Inhalte  
*   Verweise auf umstrittene Gebiete oder Regionen  
*   Bereitstellung oder Zugriff auf Inhalte oder Dienste, die unter dem jeweils anwendbaren Recht rechtswidrig sind.  

### 2,12 Altersfreigaben  

#### überfälliger Inhalt  

Wenn Sie Ihre Durchwahl an das [Partner Center][MicrosoftPartnerCenter]übermitteln, müssen Sie angeben, ob Ihre Erweiterung Inhalte anzeigt, die als "ausgereift" gekennzeichnet sein sollen.  Berücksichtigen Sie bei der Bestimmung der Bewertung für Ihre Erweiterung den gesamten Inhalt Ihrer APP, einschließlich von Benutzern generierter Inhalte und anzeigen, sowie den Inhalt, den Ihre Erweiterung verknüpft.  Wenn Sie angeben, dass Ihre Durchwahl keine "ausgereiften" Inhalte enthält, sind Sie dafür verantwortlich, die Richtigkeit dieser Bewertung zu gewährleisten.  Unabhängig von der Bewertung, die Sie für Ihre Durchwahl erhalten haben, muss Sie weiterhin alle inhaltlichen Anforderungen der Microsoft Edge Addons-Entwicklerrichtlinien erfüllen.  

#### Änderung der 2.12.2-Bewertungen  

Wenn Ihre Erweiterung Inhalte enthält, die möglicherweise für eine höhere Alterseinstufung als die zugewiesene Bewertung geeignet sind (beispielsweise vom benutzergenerierten, im Einzelhandel oder in anderen webbasierten Inhalten), müssen Sie die Benutzer dazu auffordern, diese Inhalte mithilfe eines Inhaltsfilters zu empfangen oder sich mit einem bereits vorhandenen Konto anzumelden.  

### 2,13-Videos  

Wenn Sie ein Werbevideo im Eintrag einreichen, sollten alle in dieser Richtlinie erwähnten Inhaltsrichtlinien befolgt werden.  Wenn Sie einen YouTube-Link zur Verfügung stellen möchten, müssen Sie sicherstellen, dass Ankündigungen für die Videos, die Sie einbetten möchten, deaktiviert sind.  Weitere Informationen zur Aktivierung und Deaktivierung von anzeigen auf YouTube finden Sie unter [Support.Google.com/YouTube/Answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] und [Support.Google.com/YouTube/Answer/132596][GoogleYoutubeAnswer132596].  

<!-- image links -->  

<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Relaxen der Standardrichtlinien-Inhalts Sicherheitsrichtlinie \ (CSP \) | Microsoft docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Vereinbarung für App-Entwickler | Microsoft docs"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "So erkennt Microsoft Malware und potenziell unerwünschte Anwendungen | Microsoft docs"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Festlegen der standardmäßigen Anzeigenformate-YouTube-Hilfe"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anzeigen in eingebetteten Videos – YouTube-Hilfe"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Privatsphäre der Kinder-Federal Trade Commission"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Kreative Akzeptanz Richtlinien – Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Kreative Spezifikationen – Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
