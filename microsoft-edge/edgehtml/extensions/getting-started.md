---
description: Verschaffen Sie sich eine End-to-End-Übersicht über die Reise von der ersten Entwicklung bis zur Verpackung von Microsoft Edge-Erweiterungen.
title: Erweiterungen – erste Schritte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f06762692c451ea89b74fdf6f9959172c69a32ca
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234228"
---
# Erste Schritte mit Erweiterungen  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Ganz gleich, ob Sie ein neuer Entwickler sind und sich mit Erweiterungen oder einem erfahrenen Veteranen mit einer Chrome-Erweiterung vertraut machen möchten, die Sie portieren möchten, dieser Leitfaden enthält alle Informationen, die Sie zum entwickeln, testen, Verpacken und Veröffentlichen einer Erweiterung für Microsoft Edge benötigen. 

## Entwickeln einer Erweiterung

Der erste Schritt dieser Reise besteht darin, eine Microsoft Edge-Erweiterung zu erstellen: 
- Neu bei Extensions? Schauen Sie sich unseren [Leitfaden zum Erstellen von Erweiterungen](./guides/creating-an-extension.md) an, um zu erfahren, wie Sie Ihre erste Browser-Erweiterung erstellen können. 
- Sind Sie bereits mit Erweiterungs-APIs vertraut? Schauen Sie sich unsere [API-Support-Dokumentation](./api-support.md) an, um die neuesten Informationen darüber zu erhalten, welche APIs unterstützt werden/in der Entwicklung. 
- Haben Sie eine Chrome-Erweiterung, die Sie an Microsoft Edge portieren möchten? Testen Sie das [Microsoft Edge Extension Toolkit](./guides/porting-chrome-extensions.md)!

## Laden und Debuggen

Sobald Sie über eine Erweiterung verfügen, die in Microsoft Edge funktioniert, sollten Sie Sie auf der Seite laden, um Sie in Aktion zu sehen. Der erste Schritt besteht darin, sicherzustellen, dass die [Erweiterungsentwickler Features aktiviert](./guides/adding-and-removing-extensions.md)sind. Auf diese Weise können Sie Erweiterungsdateien in Microsoft Edge laden, damit Sie Ihre Erweiterung während der Entwicklung testen können. Wenn Sie Probleme haben, können Sie mit den F12-Entwicklertools [die verschiedenen Kontexte ihrer Erweiterung Debuggen](./guides/debugging-extensions.md) , um genau zu bestimmen, was vor sich geht. Gibt es immer noch Probleme? Unser [Leitfaden zur Problembehandlung](./troubleshooting.md) bietet Lösungen für verschiedene häufige Probleme. 

## Melden von Fehlern und Anfordern von Hilfe

Sie haben einen Fehler in unserer Erweiterungs Plattform gefunden? Wenn es sich um ein spezifisches Problem mit Microsoft Edge handelt, suchen Sie es in unserem [Microsoft Edge Issue Tracker](https://developer.microsoft.com/microsoft-edge/platform/issues/) , um festzustellen, ob es bereits gemeldet wurde. Wenn ja, großartig! Sie können die Schaltfläche "+ mich auch" drücken, um den Fehler zu überstimmen, und die Schaltfläche "dieses Problem für Updates überwachen", um auf etwaige Änderungen des Problems aufmerksam zu werden. Wenn Sie das Problem nicht finden können, in dem Sie gerade arbeiten, können Sie ein neues Problem öffnen und so viele Informationen wie möglich zur Verfügung stellen, damit sich unsere Entwickler damit vertraut machen können. 

Fehlt eine API, die ihre Erweiterung ordnungsgemäß funktionieren muss? In diesem Fall [hören wir immer auf UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions). Wenn Sie bereits vorhanden sind, können Sie Ihr API gerne upvoten oder ein neues feedbackelement erstellen, damit andere Entwickler es auch überstimmen können! 

Haben Sie eine Frage, auf die Sie in der Dokumentation keine Antwort finden können? Wir empfehlen dringend, dass Sie sich der [Microsoft Edge Extensions-Community](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) bei Stack Overflow anschließen und Sie dort Fragen.

## Testen der Erweiterung

Ab dem Windows Anniversary-Update unterstützt [Microsoft WebDriver](../webdriver/index.md) das automatisierte seitliche Laden von Erweiterungen in Microsoft Edge-Sitzungen. Auf diese Weise können Sie einfache Tests schreiben, um sicherzustellen, dass jede Erweiterung, die für die Änderung einer Seite vorgesehen ist, in der erwarteten Weise erfolgt. Weitere Informationen hierzu finden Sie in unserem [Testhandbuch](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver). Bleiben Sie auch für Updates auf dem laufenden, während wir in Zukunft weitere erweiterungsspezifische Features zu Microsoft WebDriver hinzufügen möchten.

## Hinzufügen des letzten Schliffs

Ihre Erweiterung funktioniert also in Microsoft Edge. Was passiert als nächstes? Bevor Sie mit dem Verpacken der Erweiterung fortfahren, empfehlen wir Ihnen dringend, diese Leitfäden zu lesen, um sicherzustellen, dass Ihre Erweiterung unseren Best Practice-Richtlinien folgt: 
- Stellen Sie sicher, dass die Erweiterungssymbole [richtig dimensioniert](./guides/design.md) und [barrierefrei](./guides/accessibility.md) sind (was bedeutet, dass Sie sowohl in hellen als auch in dunklen Designs von Microsoft Edge sowie im Modus für hohen Kontrast sichtbar sind). 
- Wenn Ihre Erweiterung mehrere Sprachen unterstützen muss, stellen Sie bitte sicher, dass Sie einen Blick auf unseren [Leitfaden zur Internationalisierung](./guides/internationalization.md)genommen haben. 

## Verpacken einer Erweiterung

Nun wird Ihre Erweiterung endlich aufpoliert und kann verpackt werden. Ganz gleich, ob Sie es verpacken möchten, um die Übermittlung an den Microsoft Store vorzubereiten, oder um die Verteilung innerhalb Ihrer Entwicklungs-und Test Teams zu vereinfachen, es stehen Ihnen zahlreiche Ressourcen zur Verfügung, die Ihnen helfen können: 

- Unsere empfohlene Lösung zum Erstellen eines Erweiterungspakets besteht darin, unserem [ManifoldJS-Leitfaden für Verpackungen](./guides/packaging/using-manifoldjs-to-package-extensions.md) zu folgen, der Sie durch die Schritte der Verwendung eines Node.js basierten Tools zum einfachen Verpacken Ihrer Erweiterung führt, unabhängig von der Plattform, auf der Sie sich entwickeln. Wenn Sie eine genauere Übersicht über unser Erweiterungs-Verpackungsformat wünschen, lesen Sie bitte unseren Leitfaden zur AppX- [Paketerstellung](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder). 
- Wenn Ihre Erweiterung mehrere Sprachen unterstützt, müssen Sie auch unserem Leitfaden zum [Lokalisieren von Erweiterungspaketen](./guides/packaging/localizing-extension-packages.md) folgen, damit die Sprachen, die Sie in ihrer Erweiterung haben, nach dem Verpacken richtig registriert sind. 

Wenn Sie ein Enterprise-Kunde sind und ihre verpackten Erweiterungen über interne Kanäle verteilen möchten, lesen Sie unseren [Leitfaden für Erweiterungen für Unternehmen](./extensions-for-enterprise.md) , um zu erfahren, wie dies geht.  

## Veröffentlichen im Microsoft Store

Da sich unsere Erweiterungs Plattform noch in den Kinderschuhen befindet, verwalten wir im Microsoft Store absichtlich Erweiterungsbeiträge, damit wir uns auf die Bereitstellung einer Qualitätserfahrung für unsere Benutzer und Entwickler konzentrieren können. Allerdings möchten wir Entwicklern die Veröffentlichung Ihrer Erweiterungen so einfach wie möglich machen. Aus diesem Grund haben wir vor kurzem ein neues [Formular](https://aka.ms/extension-request) für die Übermittlung von Erweiterungen gestartet, in dem Entwickler die Berechtigung zum Übermitteln Ihrer Erweiterungs-AppX an den Microsoft Store anfordern können.
 
Der erste Schritt des Veröffentlichungsprozesses besteht darin, sicherzustellen, dass Ihre Erweiterung den Richtlinien für **Browsererweiterungen** und dem [Abschnitt Microsoft-Edge-Erweiterungen in den Microsoft Store-Richtlinien](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12)entspricht.  

<!--  The first step of the publishing process is to make sure your extension conforms to our [browser extension policy](./microsoft-browser-extension-policy.md) as well as the [Microsoft Edge extensions section of the Microsoft Store Policies](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).  -->  

Nachdem Sie bestätigt haben, dass Ihre Erweiterung den Richtlinien folgt, müssen Sie sich für ein [Entwicklerkonto im Partner Center registrieren und den Namen Ihrer Durchwahl reservieren](./guides/packaging/extensions-in-the-windows-dev-center.md). Anschließend müssen Sie eine Anfrage über unser [Verlängerungsformular](https://aka.ms/extension-request) einreichen, um die Berechtigung zum Veröffentlichen im Microsoft Store zu beantragen. Wenn Sie versuchen, ihre Erweiterungs-AppX zu übermitteln, ohne zuerst die Berechtigung zu erhalten, erhalten Sie die folgende Fehlermeldung:

```text
Package acceptance validation error: com.microsoft.edge.extension is a reserved extension type. Your app does not have permission to use this extension type.
```  

Nachdem Sie eine Anfrage eingereicht haben, erhalten Sie eine Benachrichtigung und werden versuchen, so schnell wie möglich zu ihrer Übermittlung zu gelangen. Dies kann aufgrund der großen Anzahl von Übermittlungen, die wir erhalten haben, etwas dauern, aber wir werden Sie per e-Mail benachrichtigen, sobald Sie genehmigt sind! Nachdem Sie die e-Mail erhalten haben, können Sie Ihre Durchwahl AppX über das Partner Center an den Microsoft Store übermitteln. Bitte beachten Sie, dass Sie Ihr AppX nicht unterschreiben müssen, bevor Sie es einreichen. der Microsoft Store-Aufnahmeprozess übernimmt das für Sie!
 
> [!NOTE]
> Das Verfahren zum Veröffentlichen einer Erweiterung für den Microsoft Store (unabhängig davon, ob es sich um eine brandneue Erweiterung oder um eine Aktualisierung auf eine vorhandene handelt) kann bis zu 72 Stunden dauern. Um diesen Vorgang zu beschleunigen, stellen Sie bitte sicher, dass Sie diese allgemeinen Probleme vor dem einreichen überprüft haben, um zu verhindern, dass Sie später erneut übermitteln müssen: 
> - Ihre Screenshots sind ordnungsgemäß sortiert und werden von ihrer Erweiterung in Microsoft Edge ausgeführt. 
> - Ihre Erweiterungsbeschreibung verweist auf "Microsoft Edge" anstelle von "Edge" (Dies ist eine rechtliche Anforderung). 
> - Ihr 150x150-Symbol in Ihrem Erweiterungspaket hat [keinen transparenten Hintergrund](./guides/design.md#microsoft-store-icon) (der Microsoft Store-Client rendert Bilder mit transparenten Hintergründen nicht ordnungsgemäß) 

Darüber hinaus müssen Sie, falls zutreffend, sicherstellen, dass alle Informationen zur Plattformverfügbarkeit auf Ihrer Website die Verfügbarkeit ihrer Erweiterung auf Microsoft Edge richtig erwähnen. Während der Microsoft Store keine Installationen mit einem Klick auf Inline-Erweiterungen zulässt, können Sie [im Microsoft Store Deep-Link zu ihrer Erweiterung](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) erstellen, damit die Benutzer Sie einfach abrufen können. 

Im Microsoft Store können Sie auch [die Sichtbarkeit ihrer Erweiterung](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) im Microsoft Store-Katalog steuern. Einige unserer Partner haben diese Funktionalität genutzt, um Folgendes zu erreichen: 
- Veröffentlichen einer zweiten Beta Version ihrer Erweiterung als ausgeblendet im Microsoft Store.
- Anfängliche Veröffentlichung der Erweiterung als "ausgeblendet", um die ursprüngliche Telemetrie zu überwachen, bevor Sie Ihren Status auf "sichtbar" ändert, sobald eine bestimmte Vertrauensstufe erreicht ist.

## Das war's.

Wenn Sie das Ende dieses Leitfadens erreicht haben, haben Sie den Prozess der Entwicklung einer Erweiterung für Microsoft Edge abgeschlossen! Schauen Sie sich unsere [Tipps und Kniffe](./tips-and-tricks.md) an, um zu erfahren, wie Sie Ihre Erweiterung vermarkten und mit ihren Nutzern interagieren können.
