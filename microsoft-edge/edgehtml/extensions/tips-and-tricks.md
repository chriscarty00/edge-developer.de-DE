---
description: Erfahren Sie mehr über einige praktische Tipps und Tricks zu Microsoft Edge-Erweiterungen
title: Tipps und Tricks | Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, javascript, developer, extensions
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8a5ea19152f5524d86d17d6f978c677c45f8f3a8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399351"
---
# <a name="tips-and-tricks"></a>Tipps und Tricks  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Unabhängig davon, ob Sie derzeit an einer Microsoft Edge-Erweiterung arbeiten oder bereits eine erweiterung veröffentlicht haben, sind die folgenden Tipps und Tricks hilfreich.  

## <a name="get-a-direct-link-to-your-extension-in-the-microsoft-store"></a>Einen direkten Link zu Ihrer Erweiterung im Microsoft Store erhalten  

Im Windows Dev Center-Dashboard finden Sie einen direkten Link zu Ihrer Erweiterung im Microsoft Store.  Dieser Link kann für Werbung und die Freigabe Ihrer Erweiterung hilfreich sein.  

Nachdem Sie sich beim Windows Dev Center anmelden und über das Dashboard zu Ihrer Erweiterung navigieren, finden Sie auf der Seite App-Identität den Link in der **Linkzeile Store-Protokoll:**  

![Speicherprotokollverknüpfung](./media/store-link.png)  
 
## <a name="make-sure-youre-following-the-microsoft-store-policy"></a>Stellen Sie sicher, dass Sie die Microsoft Store-Richtlinie folgen  

Beachten Sie beim Erstellen Ihrer Erweiterung die Richtlinien für die Übermittlung an den Microsoft Store, die in der [Microsoft Store-Richtlinie hervorgehoben sind.](/windows/uwp/publish/store-policies)  
 
Microsoft Edge-Erweiterungen haben auch einen zusätzlichen Satz von Richtlinien, die hier zu [folgen sind.](/windows/uwp/publish/store-policies#pol_10_12)  

## <a name="improve-your-extensions-discoverability-in-the-microsoft-store"></a>Verbessern sie die Aufdingbarkeit Ihrer Erweiterung im Microsoft Store  

Sie können Ihrer Erweiterungsübermittlung Schlüsselwörter hinzufügen, um die Aufsuchung durch Suchen zu verbessern.  Beispiele: `Microsoft Edge Extensions` und `name of my extension`.  

Dies kann im Windows Dev Center unter dem Beschreibungsabschnitt Ihrer Erweiterung geschehen.  Diese Schlüsselwörter müssen für jede Sprache hinzugefügt werden, die von Ihrer Erweiterung unterstützt wird.  

![Senden einer Antwort auf eine Rezension mithilfe von Schlüsselwörtern](./media/keywords.png)  

## <a name="automate-your-submission-to-the-microsoft-store"></a>Automatisieren Der Übermittlung an den Microsoft Store  

Sie können Ihre Übermittlungen an den Microsoft Store automatisieren und optimieren, indem Sie die neue Microsoft Store-Übermittlungs-API verwenden, mit der Sie Apps/Spiele, Add-Ons \(In-App-Käufe\) und Paketflüge über eine REST-API aktualisieren können.  Sehen Sie sich die [Dokumentation und Beispiele an,](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) oder verwenden Sie die Open Source [Submission API VSTS-Erweiterung,](https://github.com/Microsoft/windows-dev-center-vsts-extension) um zu beginnen.  

## <a name="use-the-windows-feedback-hub-to-gather-feedbackreviewsfeature-requests"></a>Verwenden des Windows Feedback Hub zum Sammeln von Feedback/Rezensionen/Featureanforderungen  

Sie können Benutzer zur Windows Feedback Hub-Unterkategorie für Ihre Erweiterung durch Einbetten eines Links, der darauf verweist, an die Windows Feedback Hub-Unterkategorie weiterverstellen.  Dieser Link muss im folgenden Format erstellt werden:  

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

Sie müssen durch den `<PFN>` Paketfamiliennamen ihrer Erweiterung ersetzen.  Dies finden Sie im **Abschnitt App-Identität** für Ihre Erweiterung im Windows Dev Center.  

## <a name="check-out-your-ratings-and-reviews"></a>Sehen Sie sich Ihre Bewertungen und Rezensionen an  

Melden Sie sich regelmäßig an, um Ihre Benutzerbewertungen und Bewertungen zu überprüfen.  Während die UWP-App nur Informationen über den aktuellen Benutzermarkt hat, zeigt die Anmeldung beim Windows Dev Center die durchschnittliche Bewertung in allen Märkten an.  

## <a name="respond-to-user-reviews"></a>Antworten auf Benutzerrezensionen  

Sie können auf Benutzerbewertungen im Microsoft Store über das Windows Dev Center-Dashboard antworten.  Navigieren Sie zu Ihrer Erweiterung, und wählen Sie unter Analytics **Rezensionen aus.**  Unter jeder Rezension wird ein Link angezeigt, mit dem Sie direkt auf den Kunden antworten können.  Dieser Kommunikationskanal ermöglicht Es Ihnen, Feedback, Lösungen oder ein Dankeschön für die Rezension zu senden!  

![Reagieren auf die Benutzerüberprüfung](./media/reviews.png)  
