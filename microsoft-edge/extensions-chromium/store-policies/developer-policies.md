---
description: Microsoft Edge Add-ons Catalog Developer Policies.
title: Microsoft Edge-Add-Ons-Katalog – Entwicklerrichtlinien
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 5c2a8dd816a28a35b6e7b725d5106814e401f6ec
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327645"
---
# Microsoft Edge-Add-Ons-Katalog – Entwicklerrichtlinien  

## Einführung und Ziel dieses Dokuments  

Vielen Dank für Ihr Interesse an der Entwicklung von Erweiterungen für den Microsoft Edge-Add-Ons-Katalog.  Die Microsoft Edge-Add-Ons-Katalog-Entwicklerrichtlinien \(Addons-Katalog-Entwicklerrichtlinien\) gelten für Ihre Erweiterungen, einschließlich der Übermittlung von Erweiterungen über [Partner Center][MicrosoftPartnerCenter] und der Bereitstellung solcher Erweiterungen über die Microsoft Edge-Add-Ons.  

## Prinzipien  

Zunächst einige wichtige Grundregeln:  

*   Sie sollten innerhalb Ihrer Erweiterungen für Microsoft Edge einen eindeutigen und eindeutigen Wert anbieten.  Geben Sie einen überzeugenden Grund an, Ihre Erweiterungen aus dem Microsoft Edge-Add-Ons-Katalog \(Microsoft Edge-Add-Ons\) herunterzuladen.  
*   Sie dürfen unsere gemeinsamen Benutzer nicht in die Irre führen, was Ihre Erweiterung macht, wer sie bietet und so weiter.  
*   Sie dürfen nicht versuchen, Benutzer, das System oder das Ökosystem zu vertäuschen.  Es gibt keinen Ort in unseren Microsoft Edge-Add-Ons für jegliche Art von Betrug. Seien es Bewertungen und Überprüfungen von Manipulationen, Kreditkartenmanipulationen oder anderen betrügerischen Aktivitäten.  
    
Die Einhaltung der Entwicklerrichtlinien des Microsoft Edge-Add-Ons-Speichers sollte Ihnen dabei helfen, Entscheidungen zu treffen, die die Ansing- und Zielgruppe Ihrer Erweiterung verbessern.  

Ihre Erweiterungen sind entscheidend für die Erfahrung von Hunderten Millionen von Benutzern.  Wir freuen uns auf das, was Sie erstellen, und freuen uns darauf, Ihnen bei der Bereitstellung Ihrer Erweiterungen auf der ganzen Welt zu helfen.  

## 1. Produktrichtlinien  

### 1.1 Distinct Function & Value; Genaue Darstellung  

Ihre Erweiterung und die zugehörigen Metadaten müssen die von Ihnen beschriebene Quelle, Funktionalität und Features genau und deutlich widerspiegeln.  

#### 1.1.1 Erweiterungen müssen einen einzigen Zweck haben  

Ihre Erweiterung muss einen einzigen Zweck mit eingeschränkter Funktionalität haben.  

#### 1.1.2 Beschreiben der Erweiterung  

Alle Aspekte ihrer Erweiterung sollten die Funktionen, Features und wichtigen Einschränkungen Ihrer Erweiterung genau beschreiben, einschließlich erforderlicher oder unterstützter Eingabegeräte.  Das Nutzenversprechen Ihrer Erweiterung muss während der ersten Ausführung klar sein.  Ihre Erweiterung darf keinen Namen oder ein Ähnliches wie andere Erweiterungen verwenden und darf nicht beanspruchen, ein Unternehmen, eine Regierungsstelle oder eine andere Entität zu repräsentieren, wenn Sie nicht berechtigt sind, diese Darstellung zu machen.  

#### 1.1.3 Funktionalität  

Ihre Erweiterung muss voll funktionsfähig sein.  

#### 1.1.4 Suche und Ermittlung  

Suchbegriffe dürfen sieben eindeutige Begriffe nicht überschreiten und sollten für Ihre Erweiterung relevant sein.  

#### 1.1.5 Bereitstellen geeigneter Details  

Sie müssen unterschiedliche und informative Details zu Ihrer Erweiterung und zur Funktionalität in der Auflistung \(Metadaten\) für Ihre Erweiterung bereitstellen.  Ihre Erweiterung muss eine wertvolle und qualitativ hochwertige Benutzererfahrung bieten.  Ihre Erweiterung muss auch in Microsoft Edge-Add-Ons aktiv sein.  

#### 1.1.6 Stabilität und Leistung  

Ihre Erweiterung darf sich nicht negativ auf die Leistung oder Stabilität von Microsoft Edge auswirken.  

#### 1.1.7 Verschleierung  

Erweiterungen mit verschleiertem Code sind nicht zulässig.  Dies umfasst Code innerhalb des Erweiterungspakets sowie alle externen Code- oder Ressourcen, die aus dem Web abgerufen werden.  Sie werden möglicherweise aufgefordert, Teile Ihres Codes umgestalten, wenn er nicht überprüft werden kann.  

#### 1.1.8 Ändern von Browsereinstellungen  

Ihre Erweiterung darf die Browserfunktionalität oder -einstellungen, einschließlich, aber nicht beschränkt auf: den Suchanbieter der Adressleiste und Vorschläge, die Startseite, die neue Registerkartenseite und das Hinzufügen oder Entfernen von Favoriten, ohne entsprechende Zustimmung des Benutzers nicht ändern oder ändern.  

Änderungen an den Browsereinstellungen sollten explizit in der Beschreibung Ihrer Erweiterung dokumentiert werden.  

Ihre Erweiterung kann nur wichtige Einstellungen überarbeiten, um eine Microsoft-Webseite oder einen Dienst durch die einer Drittanbieterwebsite zu ersetzen (z. B. die Verwendung einer Drittanbietersuchmaschine oder das Festlegen der Homepage auf eine Drittanbieterwebeigenschaft\), wenn Sie von einem solchen Drittanbieter verwendet oder anderweitig zugeordnet sind.  

### 1.2 Sicherheit  

Ihre Erweiterung darf die Benutzersicherheit oder die Sicherheit oder Funktionalität des Geräts, systems oder verwandter Systeme nicht gefährden oder gefährden.  

#### 1.2.1 Inhaltssicherheitsrichtlinien  

> [!NOTE]
> Wenn Sie über die beschriebene Funktionalität hinausgehende Änderungen an Ihrer Erweiterung vornehmen, müssen alle Änderungen am Code mit der [Microsoft Edge-Inhaltssicherheitsrichtlinie kompatibel sein.][MicrosoftEdgeContentSecurityPolicyRemoteScript]  Ihre Erweiterung sollte beispielsweise kein Remoteskript herunterladen und dieses Skript anschließend auf eine Weise ausführen, die nicht mit der beschriebenen Funktionalität konsistent ist.  

#### 1.2.2 Unerwünschte und schädliche Software  

Ihre Erweiterung darf keine Schadsoftware gemäß den Kriterien von Microsoft für unerwünschte und [bösartige Software enthalten oder aktivieren.][MicrosoftIdentifiesMalwareUnwantedApplications]  

#### 1.2.3 Abhängigkeit von anderer Software  

Ihre Erweiterung hängt möglicherweise von nicht integrierter Software \(z. B. einem anderen Produkt, Modul oder Dienst\) ab, um die primäre Funktionalität bereitzustellen, sofern Sie die Abhängigkeit in der Beschreibung offenlegen.  

#### 1.2.4 Extensions Update  

Sofern nicht anders von Microsoft zugelassen, dürfen Ihre Erweiterungen nur über Microsoft Edge-Add-Ons aktualisiert werden.  

### 1.3 Produkt ist testbar  

Ihre Erweiterung muss testbar sein.  Wenn es nicht möglich ist, Ihre Erweiterung aus irgendeinem Grund zu testen, einschließlich, aber nicht beschränkt auf die unten aufgeführten Elemente, kann ihre Erweiterung diese Anforderung nicht erfüllen.  

#### 1.3.1 Benutzeranmeldeinformationen  

Wenn Ihre Erweiterung Anmeldeinformationen erfordert, geben Sie mithilfe des Felds ein funktionierendes Demokonto `Notes for certification` an.  

#### 1.3.2 Verfügbarkeit von Diensten  

Wenn Ihre Erweiterung Zugriff auf einen Server erfordert, muss der Server funktionsfähig sein, um sicherzustellen, dass er ordnungsgemäß funktioniert.  

### 1.4 Benutzerfreundlichkeit  

Ihre Erweiterung muss die Standards des Microsoft Edge-Add-Ons-Speichers für benutzerfreundlichkeit erfüllen, einschließlich, aber nicht beschränkt auf die standards, die in den folgenden Unterabschnitten aufgeführt sind.  

#### 1.4.1 Plattformübergreifend kompatibilität  

Ihre Erweiterung sollte mit Microsoft Edge auf allen Geräten und Plattformen kompatibel sein, auf denen sie heruntergeladen werden können.  Wenn eine Erweiterung auf ein Gerät heruntergeladen wird, mit dem sie nicht kompatibel ist, sollte sie dies beim Start erkennen und dem Benutzer eine Meldung mit den Anforderungen anzeigen, die Geräte erfüllen müssen, um mit Ihrer Erweiterung kompatibel zu sein.  

#### 1.4.2 Benutzeroberfläche  

Ihre Erweiterung muss sofort gestartet werden und für Benutzereingaben reaktionsfähig bleiben.  Ihre Erweiterung muss weiterhin ausgeführt werden und für Benutzereingaben reaktionsfähig bleiben.  Ihre Erweiterung muss ohne Unerwartetes heruntergefahren werden.  Ihre Erweiterung sollte Ausnahmen behandeln und auf Benutzereingaben reagieren, nachdem die Ausnahme behandelt wurde.  

### 1.5 Persönliche Informationen  

Die folgenden Anforderungen gelten für Erweiterungen, die auf persönliche Informationen zugreifen.  Personenbezogene Informationen umfassen alle Informationen oder Daten, die eine Person identifizieren oder verwenden können, die mit diesen Informationen oder Daten verknüpft ist.  

#### 1.5.1 Persönliche Informationen nur bei Bedarf sammeln  

Ihre Erweiterung kann persönliche Informationen sammeln, darauf zugreifen, diese verwenden oder übertragen (einschließlich Webbrowsen-Aktivitäten\); nur, wenn dies nur für die Verwendung in einem öffentlich offengelegten, benutzerfreundlichen Feature erforderlich ist.  

#### 1.5.2 Beibehalten einer Datenschutzrichtlinie  

Unabhängig davon, ob Ihre Erweiterung auf personenbezogene Informationen zu, diese erfasst oder überträgt; Sie müssen Ihre Datenschutzrichtlinien deutlich beachten und einhalten, wenn dies gesetzlich vorgeschrieben ist.  Ihre Datenschutzrichtlinie muss Die Benutzer über die von Ihrer Erweiterung zugegriffenen, erfassten oder übermittelten personenbezogenen Informationen informieren, wie diese Informationen verwendet, gespeichert und geschützt werden, und die Arten von Parteien angeben, denen sie offengelegt werden.  Ihre Datenschutzrichtlinie muss die Kontrollen beschreiben, über die Benutzer über die Verwendung und Freigabe ihrer Informationen verfügen, wie sie auf ihre Informationen zugreifen, und sie muss die geltenden Gesetze und Bestimmungen einhalten.  Ihre Datenschutzrichtlinie muss auf dem neuesten Stand gehalten werden, wenn Sie Ihrer Erweiterung neue Features und Funktionen hinzufügen.  

Wenn Sie Microsoft Ihre Datenschutzrichtlinie bereitstellen, erklären Sie sich damit einverstanden, Microsoft zu erlauben, diese Datenschutzrichtlinie für Benutzer Ihrer Erweiterung zu teilen.  

#### 1.5.3 Freigeben von Daten für Dritte  

Sie können die persönlichen Informationen von Benutzern Ihrer Erweiterung über Ihre Erweiterung oder die zugehörigen Metadaten nur dann an einen außerhalb des Diensts oder an einen Drittanbieter veröffentlichen, nachdem Sie die Zustimmung von diesen Benutzern einholen.  Die Zustimmung bedeutet, dass die Benutzer ihre ausdrückliche Zustimmung in der Benutzeroberfläche Ihrer Erweiterung für die angeforderte Aktivität erteilen, nachdem Sie:  

*   Beschreiben Sie Ihren Benutzern, wie auf die Informationen zugegriffen, sie verwendet oder freigegeben wird, und geben Sie die Arten von Parteien an, denen sie offengelegt werden, und  
*   Stellen Sie Ihren Benutzern einen Mechanismus in Ihrer Benutzeroberfläche für Erweiterungen zur Verfügung, über den sie später die Berechtigung zurücksenten und abmelden können.  
    
#### 1.5.4 Freigabeinformationen von Nichtbenutzern  

Wenn Sie die persönlichen Informationen einer Person über Ihre Erweiterung oder die Metadaten für einen außen bzw. einen Drittanbieter veröffentlichen, die Person, deren Informationen freigegeben werden, jedoch kein Benutzer Ihrer Erweiterung ist;  

1.  Sie müssen eine ausdrückliche schriftliche Zustimmung einholen, um diese personenbezogenen Informationen zu veröffentlichen.  
1.  Sie müssen der Person, deren Informationen freigegeben werden, erlauben, diese Zustimmung jederzeit zurückzuziehen.  
1.  Ihre Datenschutzrichtlinie muss eindeutig offenlegen, dass Sie personenbezogene Informationen auf diese Weise sammeln können.  
1.  Wenn dies nach geltendem Recht erforderlich ist, müssen Sie die personenbezogenen Informationen aller Personen auf Anfrage löschen, einschließlich Einzelpersonen, deren Informationen Sie auf diese Weise sammeln.  
1.  Wenn Ihre Erweiterung Benutzern Zugriff auf die persönlichen Informationen einer anderen Person bietet, gilt diese Anforderung ebenfalls.  
    
#### 1.5.5 Sicheres Übertragen von Informationen  

Wenn Ihre Erweiterung persönliche Informationen sammelt, speichert oder überträgt; Dies muss mithilfe moderner Kryptografiemethoden sicher sein.  

#### 1.5.6 Hochgradig vertrauliche Informationen  

Ihre Erweiterung darf keine hochgradig vertraulichen persönlichen Informationen wie Gesundheits- oder Finanzdaten sammeln, speichern oder übertragen, es sei denn, die Informationen stehen im Zusammenhang mit der Funktionalität Ihrer Erweiterung.  Ihre Erweiterung muss auch die ausdrückliche Zustimmung des Benutzers einholen, bevor solche Informationen gesammelt, gespeichert oder übertragen werden.  

### 1.6 Berechtigungen  

Ihre Erweiterung darf nur die Berechtigungen anfordern, die für die Funktion erforderlich sind.  Sie müssen eine Beschreibung der Funktionsweise Ihrer Erweiterung bereitstellen.  Die Erweiterung darf nur wie beschrieben verwendet werden.  Ihre Erweiterung verlangt möglicherweise keine Berechtigung für Funktionen, die über die funktionen hinausgehen, die zum Ausführen und Funktionieren wie deklariert erforderlich sind.  

### 1.7 Lokalisierung  

Sie sollten die Erweiterung für alle Sprachen lokalisieren, die von der Erweiterung unterstützt werden sollen.  Der Text der Beschreibung Der Erweiterung sollte in jeder sprache lokalisiert werden, die Sie deklarieren.  
Wenn Ihre Erweiterung so lokalisiert ist, dass einige Features in einer lokalisierten Version nicht verfügbar sind, müssen Sie die Grenzen der Lokalisierung klar in Ihrer Erweiterungsbeschreibung anzeigen. Die von einer Erweiterung bereitgestellte Erfahrung muss in allen unterstützten Sprachen relativ ähnlich sein.  

### 1.8 Finanztransaktionen  

Wenn Ihr Produkt Produktkauf, Abonnements, virtuelle Währung, Abrechnungsfunktionen umfasst oder Finanzinformationen erfasst; Die Anforderungen in den folgenden Abschnitten gelten.  

#### 1.8.1 Kostenpflichtige Features  

Ihre Erweiterung kann es Benutzern ermöglichen, digitale Inhalte oder Dienste zu nutzen, die über einen Drittanbieterkaufsmechanismus oder eine API erworben wurden.  

Sie müssen eine sichere Drittanbieter-Einkaufs-API für den Kauf von physischen Waren oder Dienstleistungen verwenden.  Sie müssen eine sichere Drittanbieter-Einkaufs-API für Zahlungen verwenden, die in Verbindung mit anderen Diensten, einschließlich realer, gemeinnütziger oder gemeinnütziger Beiträge, vorgenommen werden.  

*   Wenn Ihre Erweiterung verwendet wird, um gemeinnützige Beiträge zu erleichtern oder zu sammeln oder um Werbeaustrage oder -wettbewerbe zu führen, müssen Sie dies in Übereinstimmung mit dem geltenden Recht tun.  
*   Zudem muss deutlich gemacht werden, dass Microsoft weder als Spendensammler noch als Sponsor der Werbeaktion auftritt.  
*   In Ihrer Durchwahl verkaufte In-Product-Angebote dürfen nicht in eine rechtlich gültige Währung \(z. B. USD, Euro und so weiter\) oder physische Waren oder Dienstleistungen umgewandelt werden.  
    
Die folgenden Anforderungen gelten für die Verwendung einer sicheren Drittanbieter-Einkaufs-API:  

*   Zum Zeitpunkt der Transaktion oder wenn Sie Zahlungs- oder Finanzdaten vom Benutzer erfassen; Ihre Erweiterung muss den Handelstransaktionsanbieter identifizieren, den Benutzer authentifizieren und eine Benutzerbestätigung für die Transaktion erhalten.  Ein Handelstransaktionsanbieter verwaltet eine sichere Plattform für den Austausch von Finanzdaten.  
*   Ihre Erweiterung bietet Benutzern möglicherweise die Möglichkeit, diese Authentifizierung zu speichern, aber Die Benutzer müssen in der Lage sein, entweder eine Authentifizierung für jede Transaktion zu erfordern oder Produkttransaktionen zu deaktivieren.  
*   Wenn Ihre Durchwahl Kreditkarteninformationen erfasst oder einen Drittanbieter für Zahlungsverarbeiter verwendet, der Kreditkarteninformationen erfasst, muss die Zahlungsverarbeitung den aktuellen PCI Data Security Standard \(PCI DSS\) erfüllen.  
    
#### 1.8.2 Offenlegung kostenpflichtiger Features  

Ihre Erweiterung und die zugehörigen Metadaten müssen Informationen über die angebotenen Arten von In-Product-Käufen und die Preispalette enthalten.  Sie dürfen Die Benutzer nicht in die Irre führen und sich über die Art Ihrer Produktaktionen und Angebote im Klaren sein, einschließlich des Umfangs und der Bedingungen der Testversionen.  Wenn Ihre Erweiterung den Zugriff auf vom Benutzer erstellte Inhalte während oder nach einer Testversion einschränkt, müssen Sie die Benutzer vorab benachrichtigen.  Darüber hinaus muss Ihre Durchwahl den Benutzern klar machen, dass sie eine Kaufoption in Ihrer Durchwahl initiieren.  

### 1.9 Benachrichtigungen  

Ihre Erweiterung muss die Systemeinstellungen für Benachrichtigungen achten.  Dies bedeutet, dass jede Darstellung von Anzeigen und Benachrichtigungen für Benutzer mit den Benutzereinstellungen konsistent sein muss, unabhängig davon, ob die Benachrichtigungen vom Microsoft Push Notification Service \(MPNS\), dem Windows Push Notification Service \(WNS\) oder einem anderen Dienst bereitgestellt werden.  Wenn der Benutzer Benachrichtigungen entweder produktspezifisch oder systemweit deaktiviert, muss Ihre Erweiterung funktionsfähig bleiben.  

Wenn Ihr Produkt MPNS oder WNS zum Übertragen von Benachrichtigungen verwendet, muss es die folgenden Anforderungen erfüllen:  

#### 1.9.1 Allgemeiner Leitfaden  

Benachrichtigungen, die über WNS oder MPNS bereitgestellt werden, gelten als Produktinhalte und unterliegen allen Add-Ons-Katalog-Entwicklerrichtlinien.  

#### 1.9.2 Besitz von Benachrichtigungen  

Sie dürfen die Quelle von Benachrichtigungen, die von Ihrer Erweiterung initiiert wurden, nicht verbergen oder versuchen, sie zu verbergen.  

#### 1.9.3 Keine vertraulichen oder vertraulichen Informationen  

Sie dürfen keine Informationen, die Benutzer als vertraulich oder vertraulich betrachten können, in eine Benachrichtigung mit ein- oder aussentigen.  

#### 1.9.4 Zweck von Benachrichtigungen  

Benachrichtigungen, die von Ihrer Erweiterung gesendet werden, müssen sich auf diese Erweiterung oder andere Erweiterungen beziehen, die Sie im Microsoft Edge-Add-Ons-Katalog veröffentlichen, und dürfen keine Werbenachrichten enthalten, die nicht mit Ihren Erweiterungen in Zusammenhang stehen.  

### 1.10 Verhalten und Inhalte von Werbung  

Für alle Aktivitäten im Zusammenhang mit Werbung gelten die folgenden Anforderungen:  

#### 1.10.1 Zweck  

Der Hauptinhalt Ihrer Erweiterung darf keine Werbung sein, und Werbung muss deutlich von anderen Inhalten in Ihrer Erweiterung unterschieden werden.  

#### 1.10.2 Richtlinien und Vereinbarungen  

Alle Werbeinhalte, die in Ihrer Erweiterung angezeigt werden, müssen der [Microsoft Creative Acceptance Policy (Microsoft Creative Acceptance Policy) einhalten.][MicrosoftAdvertisingCreativeAcceptancePolicies]  
Wenn Ihre Erweiterung Anzeigen anzeigt, müssen alle angezeigten Inhalte den Werbeanforderungen der Vereinbarung für [App-Entwickler][MicrosoftAppDeveloperAgreement] und dieser Richtlinie entsprechen.  

#### 1.10.3 Qualität der Werbung  

*   Der Hauptzweck Ihrer Erweiterung darf nicht sein, Benutzer zum Klicken auf Anzeigen zu besennen.  
*   Ihre Erweiterung darf nichts tun, was die Sichtbarkeit, den Wert oder die Qualität von anzeigenden Anzeigen beeinträchtigt oder beeinträchtigt.  

#### 1.10.4 Werbeaktionen  

Wenn Sie Werbeanzeigenkampagnen erwerben oder erstellen, um Ihre Erweiterungen über die Anzeigenkampagnenfunktion im [Partner Center][MicrosoftPartnerCenter]zu bewerben, müssen alle Werbematerialien, die Sie Microsoft zur Verfügung stellen, einschließlich aller zugehörigen Angebotsseiten, den Microsoft [Creative Specifications][MicrosoftAdvertisingCreativeSpecifications] Policy und [der Microsoft Creative Acceptance Policy][MicrosoftAdvertisingCreativeAcceptancePolicies]entsprechen.  

#### 1.10.5 Benachrichtigen von Benutzern über Opt-Out für Interest-Based Advertising  

Ihre Datenschutzbestimmungen oder Nutzungsbedingungen müssen Die Benutzer darüber informieren, dass Sie planen, personenbezogene Informationen an den Anzeigendienstanbieter zu senden, und den Benutzern mitteilen, wie sie die interessenbasierte Werbung abmelden können.  

#### 1.10.6 Weitere Richtlinien  

Wenn Ihre Erweiterung an Kinder unter 13 Jahren gerichtet ist, wie im [Children's Online Privacy Protection Act definiert;][FTCChildrensPrivacy] Sie müssen Microsoft im [Partner Center][MicrosoftPartnerCenter] über diese Tatsache informieren und sicherstellen, dass alle in Ihrer Erweiterung angezeigten Anzeigeninhalte für Kinder unter 13 Jahren geeignet sind.  

## 2 Inhaltsrichtlinien  

Die folgenden Richtlinien gelten für Inhalte und Metadaten \(einschließlich Herausgebername, Erweiterungsname, Erweiterungssymbol, Erweiterungsbeschreibung, Erweiterungs-Screenshots, Erweiterungstrailer und Trailerminiaturansichten sowie alle anderen Erweiterungsmetadaten\), die für die Verteilung in Microsoft Edge-Add-Ons angeboten werden.  Inhalt bedeutet die Bilder, Sounds, Videos und Text in Ihrer Erweiterung, die Kacheln, Benachrichtigungen, Fehlermeldungen oder Anzeigen, die über Ihre Erweiterung verfügbar gemacht werden, und alles, was von einem Server oder mit dem ihre Erweiterung eine Verbindung herstellt.  Da Erweiterungen und Microsoft Edge-Add-Ons weltweit verwendet werden, werden diese Anforderungen im Kontext von regionalen und kulturellen Normen interpretiert und angewendet.  

### 2.1 Inhaltsanforderungen für Microsoft Edge Addon Catalog Listing  

Metadaten und andere Inhalte, die Sie zur Erweiterung übermitteln, enthalten möglicherweise keine ausgereiften Inhalte.  
Übermittlungen, die die Anforderungen für Microsoft Edge-Add-Ons im Store nicht erfüllen, werden abgelehnt oder umgehend entfernt.  

### 2.2 Inhalte, einschließlich Namen, Logos, Original und Drittanbieter  

Alle Inhalte in Ihrer Erweiterung und die zugehörigen Metadaten müssen entweder ursprünglich von Ihnen erstellt oder von einem Drittanbieter lizenziert werden und dürfen nur verwendet werden, wenn dies vom Rechteinhaber gestattet oder anderweitig gesetzlich zulässig ist.  

### 2.3 Schadensrisiko  

#### 2.3.1 Anforderungen  

Ihre Erweiterung darf keine Inhalte enthalten, die die folgenden aktivitäten in der realen Welt erleichtern oder vereigen: \(a\) extreme oder uneigennliche Gewalt; \(b\) Verletzungen der Rechte; \(c\) die Erstellung von unzulässigen Waffen; oder \(d\) die Verwendung von Waffen gegen eine Person, einen Tier oder ein echtes oder persönliches Eigentum.  

#### 2.3.2 Verantwortung  

Ihre Erweiterung darf nicht: \(a\) ein Sicherheitsrisiko darstellen oder zu Beschwerden, Verletzungen oder sonstigen Schäden für Endbenutzer oder andere Personen oder Tier führen; oder \(b\) ein Risiko darstellen oder zu schäden an realen oder persönlichen Eigenschaften führen.  Sie sind allein für alle Tests der Erweiterungssicherheit, den Erwerb von Zertifikaten und die Implementierung geeigneter Featurevorkehrungen verantwortlich.  Sie dürfen keine Plattformsicherheits- oder Komfortfeatures deaktivieren, und Sie müssen alle anwendbaren gesetzlich erforderlichen und branchenüblichen Warnungen, Benachrichtigungen und Haftungsausschlüsse in Ihre Erweiterung mit einbeführen.  

### 2.4 Verleumdung, Verleumdung, Verleumdung und Bedrohlich  

Ihre Erweiterung darf keine Inhalte enthalten, die verleumderisch, verleumderisch, verleumderisch oder bedrohlich sind.  

### 2.5 Anstößige Inhalte  

Ihre Erweiterung und die zugehörigen Metadaten dürfen keine potenziell vertraulichen oder anstößigen Inhalte enthalten.  Inhalte können in bestimmten Ländern/Regionen aufgrund lokaler Gesetze oder kulturellen Normen als vertraulich oder anstößig betrachtet werden.  Darüber hinaus dürfen Ihre Erweiterung und die zugehörigen Metadaten keine Inhalte enthalten, die Auferlegungen, Gewalt oder Gewalt aufgrund von Überlegungen zu Race, Ethnischer Zugehörigkeit, nationaler Herkunft, Sprache, Geschlecht, Alter, Behinderung, Behinderung, sexueller Orientierung, Status als Erfahrene oder Mitgliedschaft in einer anderen sozialen Gruppe befürsprechen.  

### 2.6 Konsum, Konsum und Rauschmittel  

Ihre Erweiterung darf keine Inhalte enthalten, die die übermäßige oder unverantwortliche Verwendung von Konsum von Konsum von Produkten oder Rauschmitteln durch Über- oder Rauschmittel erleichtern oder verwertbar machen.  

### 2.7 Nicht jugendalter Inhalte  

Ihre Erweiterung darf keine Inhalte enthalten oder anzeigen, die eine angemessene Person als lästig oder sexual explizit betrachten würde.  

### 2.8 Verbotene Inhalte, Dienste und Aktivitäten  

Ihre Erweiterung muss die folgenden Bedingungen erfüllen.  

*   Ihre Erweiterung darf keine Inhalte enthalten oder Dienste bereitstellen, die das Onlineding erleichtern.  Onlinespiele umfassen, sind jedoch nicht auf Onlinesport, Sportsport, Sportspiele oder Fertigkeiten beschränkt, die Geld oder einen anderen Wert bieten.  
*   Ihre Erweiterung darf keinen nicht autorisierten Zugriff auf Websiteinhalte ermöglichen, z. B. durch Umgehen von Paywalls oder Anmeldeeinschränkungen.  
*   Ihre Erweiterung darf nicht den nicht autorisierten Zugriff, das Herunterladen oder Streaming von urheberrechtlich geschützten Inhalten oder Medien ermöglichen.  
*   Ihre Erweiterung darf keine Kryptokryptografie aus der Grube gruben.  
    
### 2.9 Unzulässige Aktivitäten  

Ihre Erweiterung darf keine Inhalte oder Funktionen enthalten, die zu unzulässigen Aktivitäten in der realen Welt ermuntern, sie vereinfachen oder vereigen.  

### 2.10 Übermäßige Anstößigkeit und unangemessene Inhalte  

*   Ihre Erweiterung darf keine exzessive oder überflüssige Ansässigkeit enthalten.  
*   Ihre Erweiterung darf keine Inhalte enthalten oder anzeigen, die eine angemessene Person als obszön betrachtet.  
    
### 2.11 Länder-/Regionenspezifische Anforderungen  

Inhalte, die in jedem Land/jeder Region, auf das/die Ihre Erweiterung ausgerichtet ist, anstößig sind, sind nicht zulässig.  Inhalte können aufgrund lokaler Gesetze oder kultureller Normen in bestimmten Ländern/Regionen als beleidigend angesehen werden.  Beispiele für potenziell beleidigende Inhalte in bestimmten Ländern/Regionen:  

**China**  

*   Verbot pornographischer Inhalte  
*   Verweise auf umstrittene Gebiete oder Regionen  
*   Bereitstellung oder Zugriff auf Inhalte oder Dienste, die unter dem jeweils anwendbaren Recht rechtswidrig sind.  
    
### 2.12 Altersfreigaben  

#### 2.12.1 Ausgereifte Inhalte  

Wenn Sie Ihre Erweiterung an [Partner Center][MicrosoftPartnerCenter]übermitteln, müssen Sie angeben, ob ihre Erweiterung Inhalte anzeigt, die als "Ausgereifte" gekennzeichnet werden sollen.  Berücksichtigen Sie beim Bestimmen der Bewertung für Ihre Erweiterung alle Inhalte in Ihrer App, einschließlich der vom Benutzer generierten Inhalte und Anzeigen, sowie die Inhalte, auf die Ihre Erweiterung verknüpft ist.  Wenn Sie angeben, dass Ihre Erweiterung keine "ausgereiften" Inhalte enthält, sind Sie für die Aufrechterhaltung der Genauigkeit dieser Bewertung verantwortlich.  Unabhängig von der Bewertung Ihrer Erweiterung muss sie dennoch alle Inhaltsanforderungen der Entwicklerrichtlinien für Microsoft Edge-Add-Ons erfüllen.  

#### 2.12.2 Bewertungsänderung  

Wenn Ihre Erweiterung Inhalte \(z. B. vom Benutzer generierte, Einzelhandels- oder andere webbasierte Inhalte\) enthält, die möglicherweise für eine höhere Altersfreigabe als die zugewiesene Bewertung geeignet sind, müssen Sie die Benutzer dazu über einen Inhaltsfilter oder die Anmeldung mit einem bereits vorhandenen Konto dazu veranmelden.  

### 2.13 Videos  

Wenn Sie ein Werbevideo in dem Eintrag übermitteln, sollte es allen in dieser Richtlinie genannten Inhaltsrichtlinien entsprechen.  Wenn Sie einen YouTube-Link bereitstellen, müssen Sie sicherstellen, dass Werbung für die bestimmten Videos deaktiviert ist, die Sie einbetten möchten.  Weitere Informationen dazu, wie Anzeigen auf YouTube aktiviert und [deaktiviert][GoogleYoutubeAnswer132596]werden, finden Sie unter [support.google.com/youtube/answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] und support.google.com/youtube/answer/132596 .  

<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Festlegen der Standardrichtlinie - Content Security Policy \(CSP\) | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Vereinbarung für App-| Microsoft Docs"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Wie Microsoft Schadsoftware und potenziell unerwünschte Anwendungen identifiziert | Microsoft Docs"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Festlegen der Standardanzeigeformate – YouTube-Hilfe"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anzeigen in eingebetteten Videos – Hilfe zu YouTube"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Datenschutz für Kinder – Federal Trade Commission"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Richtlinien für die kreative Akzeptanz – Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Kreative Spezifikationen – Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
