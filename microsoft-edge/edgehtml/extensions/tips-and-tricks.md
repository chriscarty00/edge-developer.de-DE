---
description: Erfahren Sie mehr über einige praktische Tipps und Tricks zu Microsoft Edge-Erweiterungen.
title: Tipps und Tricks | Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd512085f13b76c5a8e474301ef296612eeb0414
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233796"
---
# Tipps und Tricks  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Ganz gleich, ob Sie derzeit an einer Microsoft Edge-Erweiterung arbeiten oder eine bereits veröffentlicht haben, können sich die folgenden Tipps und Tricks als hilfreich erweisen.

## Abrufen eines direkten Links zu ihrer Erweiterung im Microsoft Store

Im Windows dev Center-Dashboard können Sie einen direkten Link zu ihrer Erweiterung im Microsoft Store finden. Dieser Link kann für Werbung und die Freigabe ihrer Erweiterung nützlich sein.

Nachdem Sie sich beim Windows dev Center angemeldet haben und über das Dashboard zu ihrer Erweiterung navigieren, finden Sie auf der Seite App-Identität den Link in der Zeile **Store Protocol Link** :

![Link zum Store-Protokoll](./media/store-link.png)
 
## Sicherstellen, dass Sie der Microsoft Store-Richtlinie folgen

Achten Sie beim Erstellen Ihrer Erweiterung darauf, dass Sie die Richtlinien für die Übermittlung an den Microsoft Store berücksichtigen, die in der [Microsoft Store-Richtlinie](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx)hervorgehoben sind. 
 
Microsoft Edge-Erweiterungen verfügen auch über eine Reihe weiterer Richtlinien, die [hier](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12)zu sehen sind.

## Verbessern der Auffindbarkeit ihrer Erweiterung im Microsoft Store

Sie können Ihrer Erweiterungs Übermittlung Stichwörter hinzufügen, um die Auffindbarkeit durchsuchen zu verbessern. Beispiel: "Microsoft Edge Extensions" und "Name meiner Erweiterung". 

Dies kann im Windows dev Center unter dem Abschnitt Beschreibung der Erweiterung erfolgen. Diese Schlüsselwörter müssen für jede Sprache hinzugefügt werden, die von der Erweiterung unterstützt wird.

![Senden einer Antwort auf eine Rezension – Stichwörter](./media/keywords.png)

## Automatisieren der Übermittlung an den Microsoft Store

Mithilfe der neuen Microsoft Store-Übermittlungs-API, mit der Sie Apps/Spiele, Add-ons (in-App-Käufe) und Flight-Pakete über eine Ruhe-API aktualisieren können, können Sie Ihre Übermittlungen an den Microsoft Store automatisieren und optimieren. Schauen Sie sich die [Dokumentation und Beispiele](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) an, oder verwenden Sie die Open Source [Submission API VSTS-Erweiterung](https://github.com/Microsoft/windows-dev-center-vsts-extension) , um zu beginnen.

## Verwenden des Windows-Feedback-Hubs zum Sammeln von Feedback/Rezensionen/Funktionsanforderungen

Sie können Benutzer an die Windows-Feedback-Hub-Unterkategorie für Ihre Erweiterung weiterleiten, indem Sie einen Link einbetten, der darauf verweist. Dieser Link muss mit dem folgenden Format erstellt werden: 

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

Sie müssen `<PFN>` den Namen der paketfamilie der Erweiterung ersetzen. Diese finden Sie im Abschnitt **App Identity** für Ihre Erweiterung im Windows dev Center.

## Sehen Sie sich Ihre Bewertungen und Bewertungen an

Melden Sie sich regelmäßig an, um die Bewertungen und Bewertungen ihrer Nutzer zu überprüfen. Während die UWP-app nur Informationen auf dem aktuellen Nutzer Markt hat, wird bei der Anmeldung beim Windows dev Center die durchschnittliche Bewertung in allen Märkten angezeigt.

## Antworten auf Nutzer Rezensionen

Sie können im Microsoft Store über das Windows dev Center-Dashboard auf Benutzer Rezensionen Antworten. Navigieren Sie zu ihrer Erweiterung, und wählen Sie unter Analytics die Option **Bewertungen**aus. Unter jeder Bewertung wird ein Link angezeigt, mit dem Sie direkt auf den Kunden Antworten können. Dieser Kommunikationskanal bietet Ihnen Feedback, Auflösungen oder ein Dankeschön für die Rezension!

![Senden einer Antwort auf eine Überprüfung](./media/reviews.png)
