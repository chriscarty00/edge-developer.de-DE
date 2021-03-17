---
description: Erhalten Sie einen Ende-zu-Ende-Überblick über den Weg vom Beginn der Entwicklung bis hin zum Packen von Microsoft Edge-Erweiterungen.
title: Erweiterungen – Erste Schritte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, javascript, developer, extensions
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 52d0aa5c1968518194a4e3b90cb0cc876d0c7f86
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439717"
---
# <a name="getting-started-with-extensions"></a>Erste Schritte mit Erweiterungen  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Unabhängig davon, ob Sie ein neuer Entwickler sind, der sich mit Erweiterungen vertraut machen möchte oder ein erfahrener Veteran mit einer Chrome-Erweiterung, die Sie portieren möchten, enthält dieses Handbuch alle Informationen, die Sie zum Entwickeln, Testen, Packen und Veröffentlichen einer Erweiterung für Microsoft Edge benötigen. 

## <a name="developing-an-extension"></a>Entwickeln einer Erweiterung

Der erste Schritt dieser Reise ist das Erstellen einer Microsoft Edge-Erweiterung: 
- Neu bei Erweiterungen? In unserem Leitfaden [zum Erstellen](./guides/creating-an-extension.md) von Erweiterungen finden Sie Informationen zum Erstellen Ihrer ersten Browsererweiterung! 
- Sie sind bereits mit Erweiterungs-APIs vertraut? In der [DOKUMENTATION zum API-Support](./api-support.md) finden Sie die neuesten Informationen dazu, welche APIs in der Entwicklung unterstützt werden. 
- Sie haben eine Chrome-Erweiterung, die Sie zu Microsoft Edge portieren möchten? Testen Sie [das Microsoft Edge Extension Toolkit](./guides/porting-chrome-extensions.md)!

## <a name="loading-and-debugging"></a>Laden und Debuggen

Sobald Sie über eine Erweiterung verfügen, die in Microsoft Edge funktioniert, sollten Sie sie seitlich laden, um sie in Aktion zu sehen. Der erste Schritt zu diesem Schritt besteht in der Sicherstellung, dass [Erweiterungsentwicklerfeatures aktiviert sind.](./guides/adding-and-removing-extensions.md) Auf diese Weise können Sie die Ladeerweiterungsdateien in Microsoft Edge nebeneinander verwenden, sodass Sie Ihre Erweiterung während der Entwicklung testen können. Sollten Probleme auftreten, können Sie mit den F12-Entwicklertools die verschiedenen Kontexte Ihrer Erweiterung debuggen, um genau zu bestimmen, was vor sich geht. [](./guides/debugging-extensions.md) Gibt es immer noch Probleme? Unser [Problembehandlungshandbuch](./troubleshooting.md) bietet Lösungen für verschiedene gängige Gotchas. 

## <a name="reporting-bugs-and-getting-help"></a>Melden von Fehlern und Abrufen von Hilfe

Denken Sie, Sie haben einen Fehler in unserer Erweiterungsplattform gefunden? Wenn das Problem spezifisch für Microsoft Edge ist, suchen Sie in unserem [Microsoft Edge Issue Tracker](https://developer.microsoft.com/microsoft-edge/platform/issues/) nach diesem Problem, um zu sehen, ob es bereits gemeldet wurde. Wenn ja, großartig! Sie können die Schaltfläche "+ Ich zu" drücken, um den Fehler zu aktualisieren, und die Schaltfläche "Dieses Problem auf Updates überprüfen", um auf änderungen an dem Problem aufmerksam gemacht zu werden. Wenn Sie das Problem nicht finden können, in das Sie gelaufen sind, können Sie ein neues Problem öffnen und so viele Informationen wie möglich bereitstellen, damit unsere Entwickler es sich anschauen können. 

<!--Are we missing an API that your extension needs to work properly? If so, [we're always listening on UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions). Feel free to upvote your API if it already exists, or to create a new feedback item so that other developers can upvote it too! -->  

Haben Sie eine Frage, auf die Sie in der Dokumentation keine Antwort finden können? Es wird dringend empfohlen, dass Sie der [Microsoft Edge Extensions-Community](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) auf Stack Overflow beitreten und sie dort fragen!

## <a name="testing-your-extension"></a>Testen Der Erweiterung

Ab dem Windows Anniversary Update unterstützt [Microsoft WebDriver](../webdriver/index.md) das automatische Seitenladen von Erweiterungen in Microsoft #A0. Auf diese Weise können Sie einfache Tests schreiben, um sicherzustellen, dass jede Erweiterung, die eine Seite ändern soll, dies in der erwarteten Weise tut. Weitere Informationen dazu finden Sie in unserem [Testhandbuch](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver). Bleiben Sie auch auf Updates eingestellt, da wir in Zukunft weitere erweiterungsspezifische Features zu Microsoft WebDriver hinzufügen möchten.

## <a name="adding-the-final-touches"></a>Hinzufügen der letzten Berührungen

Ihre Erweiterung funktioniert also in Microsoft Edge. Wie geht es weiter? Bevor Sie mit dem Verpacken Ihrer Erweiterung fortfahren, empfehlen wir dringend, diese Anleitungen zu lesen, um sicherzustellen, dass Ihre Erweiterung unsere bewährten Richtlinien eingeht: 
- Stellen Sie sicher, [](./guides/design.md) dass ihre Erweiterungssymbole richtig dimensioniert und zugänglich sind [(d.](./guides/accessibility.md) h. sie sind sowohl in hellen als auch dunklen Designs von Microsoft Edge sowie im Modus mit hohem Kontrast sichtbar). 
- Wenn Ihre Erweiterung mehrere Sprachen unterstützen muss, stellen Sie sicher, dass Sie unseren [Internationalisierungsleitfaden durchschaut haben.](./guides/internationalization.md) 

## <a name="packaging-an-extension"></a>Packen einer Erweiterung

Jetzt ist Ihre Erweiterung endlich aufpoliert und kann verpackt werden. Unabhängig davon, ob Sie es packen möchten, um die Übermittlung an den Microsoft Store vorzubereiten oder die Verteilung innerhalb Ihrer Entwicklungs-/Testteams zu vereinfachen, stehen Ihnen zahlreiche Ressourcen zur Verfügung: 

- Unsere empfohlene Lösung für das Erstellen eines Erweiterungspakets besteht in der Befolgen der [ManifoldJS-Verpackungsanleitung,](./guides/packaging/using-manifoldjs-to-package-extensions.md) die Sie durch die Schritte der Verwendung eines Node.js-basierten Tools führt, um Ihre Erweiterung unabhängig von der Plattform, auf der Sie entwickeln, einfach zu verpacken. Wenn Sie einen genaueren und manuellen Einblick in unser Erweiterungspaketformat wünschen, lesen Sie bitte unseren Leitfaden zur Erstellung von [AppX-Paketen.](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder) 
- Wenn Ihre Erweiterung mehrere Sprachen unterstützt, müssen Sie auch unsere Anleitung zum Lokalisieren von [Erweiterungspaketen](./guides/packaging/localizing-extension-packages.md) befolgen, damit die Sprachen, die Sie in Ihrer Erweiterung haben, nach dem Verpacken ordnungsgemäß registriert sind. 

Wenn Sie ein Unternehmenskunde sind, der Ihre verpackten Erweiterungen über interne Kanäle verteilen möchte, lesen Sie bitte unseren [Leitfaden](./extensions-for-enterprise.md) für Erweiterungen für Unternehmen, um dies zu erfahren.  

## <a name="publishing-to-the-microsoft-store"></a>Veröffentlichen im Microsoft Store

Da sich unsere Erweiterungsplattform noch in den Kinderschuhen befindet, verwalten wir erweiterungsübermittlungen an den Microsoft Store zwecks Zweck, damit wir uns auf die Bereitstellung einer Qualitätserfahrung für unsere Benutzer und Entwickler konzentrieren können. Darüber hinaus möchten wir es Entwicklern so einfach wie möglich machen, ihre Erweiterungen zu veröffentlichen. Daher haben wir kürzlich ein [](https://aka.ms/extension-request) neues Übermittlungsformular für Erweiterungserweiterungen gestartet, in dem Entwickler die Berechtigung zum Übermitteln ihrer Erweiterung AppX an den Microsoft Store anfordern können.
 
Der erste Schritt des Veröffentlichungsprozesses besteht im Sicherstellen, dass Ihre Erweiterung unserer Browsererweiterungsrichtlinie sowie dem [Abschnitt Microsoft Edge-Erweiterungen der Microsoft Store-Richtlinien entspricht.](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12) ****  

<!--  The first step of the publishing process is to make sure your extension conforms to our [browser extension policy](./microsoft-browser-extension-policy.md) as well as the [Microsoft Edge extensions section of the Microsoft Store Policies](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).  -->  

Sobald Sie bestätigt haben, dass Ihre Erweiterung den Richtlinien folgt, müssen Sie sich für ein Entwicklerkonto im Partner Center registrieren und den Namen [Ihrer Erweiterung reservieren.](./guides/packaging/extensions-in-the-windows-dev-center.md) Anschließend müssen Sie eine Anforderung über unser [](https://aka.ms/extension-request) Erweiterungsübermittlungsformular übermitteln, um die Berechtigung zum Veröffentlichen im Microsoft Store an bitten zu können. Wenn Sie versuchen, Ihre Erweiterung AppX ohne vorheriges Abrufen der Berechtigung zu übermitteln, wird der folgende Fehler angezeigt:

```text
Package acceptance validation error: com.microsoft.edge.extension is a reserved extension type. Your app does not have permission to use this extension type.
```  

Nachdem Sie eine Anforderung übermittelt haben, erhalten wir eine Benachrichtigung und versuchen, so schnell wie möglich zu Ihrer Übermittlung zu kommen. Dies kann aufgrund der hohen Anzahl von Übermittlungen, die wir erhalten haben, etwas dauern, aber wir benachrichtigen Sie per E-Mail, sobald Sie genehmigt sind! Sobald Sie die E-Mail erhalten haben, können Sie Ihre Erweiterung AppX über das Partner Center an den Microsoft Store übermitteln. Bitte beachten Sie, dass Sie Ihre AppX nicht signieren müssen, bevor Sie sie übermitteln. Der Microsoft Store-Ingestion-Prozess kümmert sich darum für Sie!
 
> [!NOTE]
> Der Prozess zum Veröffentlichen einer Erweiterung im Microsoft Store (unabhängig davon, ob es sich um eine völlig neue Erweiterung oder um ein Update für eine vorhandene Erweiterung oder ein Update in einer vorhandenen Erweiterung) geht, kann bis zu 72 Stunden dauern. Um diesen Prozess zu beschleunigen, stellen Sie sicher, dass Sie diese häufigen Gotchas vor der Übermittlung überprüft haben, um zu vermeiden, dass sie später erneut übermittelt werden müssen: 
> - Ihre Screenshots sind korrekt dimensioniert und werden in Microsoft Edge ausgeführt. 
> - Ihre Erweiterungsbeschreibung verweist auf "Microsoft Edge" anstelle von "Edge" (dies ist eine gesetzliche Anforderung) 
> - Ihr 150 x 150-Symbol in Ihrem Erweiterungspaket hat keinen [transparenten](./guides/design.md#microsoft-store-icon) Hintergrund (Der Microsoft Store-Client rendert Bilder mit transparenten Hintergründen nicht ordnungsgemäß) 

Stellen Sie zusätzlich zu den obigen Informationen und ggf. sicher, dass alle Informationen zur Plattformverfügbarkeit auf Ihrer Website die Verfügbarkeit Ihrer Erweiterung auf Microsoft Edge korrekt erwähnen. Während im Microsoft Store keine Installationen von Inlineerweiterungen mit einem Klick zulässig sind, können Sie eine Tiefe Verknüpfung zu Ihrer Erweiterung im [Microsoft Store](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) erstellen, um benutzern den Erwerb zu ermöglichen. 

Mit dem Microsoft Store können Sie auch [die](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) Sichtbarkeit Ihrer Erweiterung im Microsoft Store-Katalog steuern. Einige unserer Partner haben diese Funktionalität genutzt, um Folgendes zu erreichen: 
- Veröffentlichen einer zweiten Betaversion ihrer Erweiterung, die im Microsoft Store ausgeblendet ist.
- Veröffentlichen Sie zunächst ihre Erweiterung als ausgeblendet, um die anfängliche Telemetrie zu überwachen, bevor sie schließlich ihren Status in sichtbar ändert, sobald ein bestimmtes Maß an Vertrauen erreicht ist.

## <a name="thats-it"></a>Das war's.

Wenn Sie das Ende dieses Handbuchs erreicht haben, haben Sie den Prozess der Entwicklung einer Erweiterung für Microsoft Edge abgeschlossen! Achten Sie darauf, dass Sie auf unserer [Seite mit Tipps](./tips-and-tricks.md) und Tricks Ideen finden, wie Sie Ihre Erweiterung auf den Markt bringen und mit Ihren Benutzern interagieren können.
