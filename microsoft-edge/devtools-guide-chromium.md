---
description: Kennenlernen der Microsoft Edge (Chrom)-Entwickler Tools
title: Microsoft Edge (Chrom)-Entwickler Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: cb51e16083e4798478817910e54c571721d094f8
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931224"
---
# Microsoft Edge (Chrom)-Entwickler Tools  

Microsoft Edge hat das Chrom-Open-Source-Projekt angenommen, um eine bessere Web-Kompatibilität und geringere Fragmentierung unterschiedlicher zugrunde liegender Webplattformen zu schaffen.  Diese Änderung sollte es für Sie einfacher machen, ihre Websites in Microsoft Edge zu erstellen und zu testen und sicherzustellen, dass Sie auch in einem anderen Chrom basierten Browser wie erwartet funktionieren (wie Google Chrome, Vivaldi, Opera oder Brave \).  

Da das Web in einem immer größer werdenden Array von Gerätetypen in der Nutzung zugenommen hat, ist die Komplexität und der Overhead beim Testen von Websites explodiert. Da Webentwickler \ (insbesondere bei kleinen Unternehmen \) auf so vielen unterschiedlichen Systemen testen müssen, ist es möglicherweise nahezu unmöglich, sicherzustellen, dass Websites auf allen Gerätetypen und allen Browsern optimal funktionieren.  Nachdem Microsoft Edge nun auf Chrom basiert, hat das Microsoft Edge-Team die Matrix vereinfacht, indem die Microsoft Edge-Webplattform mit anderen Chrom basierten Browsern ausgerichtet und eine erstklassige Entwicklertools-Umgebung bereitgestellt wird, sowohl im Browser als auch mit den anderen Entwicklertools, die Sie täglich verwenden (beispielsweise Visual Studio-Code \).  

Wenn Sie Microsoft Edge Auschecken und sich hauptsächlich in einem Chrom basierten Browser entwickeln, sollten Sie sich wie zu Hause fühlen.  Die Microsoft Edge \ (Chrom \)-Entwicklertools funktionieren auf die gleiche Weise wie die Entwicklertools, die Sie bereits kennen und verwenden.  Weitere Informationen finden Sie unter [Neuerungen in Microsoft Edge (Chrom) devtools][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./devtools-guide-chromium/media/devtools.png" alt-text="Microsoft Edge (Chrom) devtools":::
   Microsoft Edge (Chrom) devtools  
:::image-end:::  

Wenn Sie die nächste Version von Microsoft Edge Auschecken und zuvor in Microsoft Edge \ (EdgeHTML \) entwickelt haben, verfügen Sie nun über einige hervorragende neue Tools, die es einfacher und schneller machen, ihre Websites in Microsoft Edge zu erstellen und zu testen!  

## Öffnen des devtools  

Wenn Sie das devtools noch nie zuvor verwendet haben, handelt es sich bei den Microsoft Edge-Entwicklertools um eine Reihe von Tools, die direkt in den Microsoft Edge-Browser integriert sind.  Mit diesen devtools können Sie die folgenden Aktionen ausführen:  

*   Überprüfen und Ändern der HTML-Website  
*   CSS bearbeiten und sofort anzeigen, wie Ihre Website gerendert wird  
*   Anzeigen aller `console.log()` Anweisungen aus dem Front-End-JavaScript-Code  
*   Debuggen des Skripts durch Festlegen von Haltepunkten und Durchführen einer Zeile für Zeile  

alle direkt im Browser.  Dies sind nur einige Beispiele für einige der Features, die die devtools bereitstellen, damit Sie Ihre Websites in Microsoft Edge einfacher und schneller erstellen und testen können.  

So öffnen Sie das devtools  

*   drücken Sie `F12` 
*   Drücken Sie `Ctrl` + `Shift` + `I` auf Windows \ ( `Command` + `Option` + `I` unter macOS \).  

Wenn Sie den HTML-oder CSS-Code für ein Element auf Ihrer Website anzeigen möchten, klicken Sie mit der rechten Maustaste auf das Element, und wählen Sie über **prüfen** aus, um in das Panel Elemente zu wechseln.  Sie können auch `Ctrl` + `Shift` + `C` auf Windows \ ( `Command` + `Option` + `C` unter macOS \) drücken, um das devtools im Kontroll **Element Modus** zu öffnen, in dem Sie ein Element auf der Website auswählen und den HTML-und **Elements** CSS-Code im Element Panel sehen können.  

Wenn Sie die Protokolle aus Ihrem Front-End-JavaScript-Code anzeigen oder schnell ein Skript ausführen möchten, drücken Sie `Ctrl` + `Shift` + `J` auf Windows oder `Command` + `Option` + `J` auf macOS, um den Konsolenbereich im devtools zu starten.  

## Grundlegende Tools  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-core-tools.png" alt-text="Microsoft Edge (Chrom) devtools-Kern Tools":::
   Microsoft Edge (Chrom) devtools-Kern Tools  
:::image-end::: 

Zu den Microsoft Edge \ (Chromium \) devtools gehören die folgenden Panels.  

*   Einen Bereich **Elemente** zum Bearbeiten von HTML und CSS, Untersuchen von Barrierefreiheitseigenschaften, Anzeigen von Ereignis-Listenern und Festlegen von Haltepunkten für DOM-Mutationen  
*   Eine **Konsole** zum Anzeigen und Filtern von Protokollmeldungen, zum Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Rahmens  
*   Ein **Quellen** Panel zum Öffnen und Live Bearbeiten Ihres Codes, Festlegen von Haltepunkten, durchlaufen des Codes und Anzeigen des Zustands Ihrer Website in einer Zeile mit JavaScript gleichzeitig  
*   Einen Bereich **Netzwerk** zum Überwachen und Überprüfen von Anforderungen und Antworten aus dem Netzwerk- und Browsercache   
*   Einen Bereich **Leistung**, um die Zeit und Systemressourcen zu ermitteln, die für Ihre Website erforderlich sind  
*   Einen Bereich **Arbeitsspeicher** zum Messen der Nutzung von Speicherressourcen und Vergleichen von Heap-Momentaufnahmen in unterschiedlichen Zuständen der Code-Runtime  
*   Ein **Anwendungs** Panel zum Überprüfen, ändern und Debuggen von Web App-Manifesten, Servicemitarbeitern und Service Worker-Caches.  Sie können auch Speicher, Datenbanken und Caches über den **Anwendungs** Panel prüfen und verwalten.  
*   Ein **Sicherheits** Bereich, um Sicherheitsprobleme zu Debuggen und sicherzustellen, dass Sie HTTPS auf Ihrer Website richtig implementiert haben.  HTTPS bietet kritische Sicherheit und Datenintegrität sowohl für Ihre Website als auch für Ihre Benutzer, die persönliche Informationen auf Ihrer Website bereitstellen.  
*   Ein **Überwachungs** Panel \ (jetzt **Lighthouse**umbenannt), um eine Überprüfung Ihrer Website durchzuführen.  Die Ergebnisse der Prüfung helfen Ihnen, die Qualität Ihrer Website auf folgende Weise zu verbessern.  
    *   Häufig auftretende Fehler im Zusammenhang mit dem Erstellen einer barrierefreien, sicheren, leistungsfähigen Website usw.  
    *   Beheben Sie die einzelnen Fehler.  
    *   Erstellen Sie eine PWA.  

[!INCLUDE [audits-panel-note](./devtools-guide-chromium/includes/audits-panel-note.md)]  

Bitte senden Sie Ihre [Feedback-und Funktionswünsche](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## Extensions  

Sie haben möglicherweise Erweiterungen des devtools verwendet, um Ihnen beim Erstellen von Websites oder apps beim Diagnostizieren und Debuggen von Problemen zu helfen.  Sie können Erweiterungen für Microsoft Edge über die [Microsoft Edge Addons][MicrosoftEdgeAddonsExtensions] -Seite erwerben.  Auf der [Microsoft Edge-Addons][MicrosoftEdgeAddonsExtensions] -Seite können Sie devtools-Erweiterungen aus der Kategorie **Entwicklertools** durchsuchen oder nach einer bestimmten Erweiterung suchen.  

Sie können auch Erweiterungen aus dem [Chrome Web Store][GoogleChromeWebstoreExtensions]hinzufügen.  

:::image type="complex" source="./devtools-guide-chromium/media/allow-extensions-from-stores.png" alt-text="Chrome Web Store in Microsoft Edge":::
   Chrome Web Store in Microsoft Edge  
:::image-end:::  

Wählen Sie oben im Dialogfeld, das angezeigt wird, die Option **Erweiterungen von anderen speichern zulassen aus** , und wählen Sie dann **zulassen** aus.  

> [!NOTE]
> Erweiterungen, die von anderen Quellen als dem Microsoft Store installiert wurden, werden nicht überprüft und können sich auf die Browserleistung auswirken.  

Wählen Sie **zu Chrome hinzufügen** aus, um Ihre devtools-Erweiterung zu Microsoft Edge hinzuzufügen!  

:::image type="complex" source="./devtools-guide-chromium/media/install-extension-from-chrome-store.png" alt-text="Hinzufügen einer Erweiterung von Chrome Web Store zu Microsoft Edge":::
   Hinzufügen einer Erweiterung von Chrome Web Store zu Microsoft Edge  
:::image-end:::  

## Kombinationen  

Diese Tastenkombinationen steuern das Hauptfenster von devtools, arbeiten über alle Tools oder beides.  

| Aktion | Windows | macOS |  
|:--- |:--- | :--- |  
| DevTools ein-/ausblenden\(zuletzt angezeigter Bereich wird geöffnet\) | `F12` oder `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Anzeigen des Konsolen Panels | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Anzeigen der devtools im **Element Modus überprüfen** , mit dem Sie ein Element auf der Website auswählen und den HTML-und CSS-Code im **Element Panel anzeigen** können | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Einstellungen anzeigen | `?` oder `Fn`+`F1` | `?` oder `Fn`+`F1` |  
| Anzeigen des nächsten Panels | `Ctrl`+`]` | `Command`+`]` |  
| Anzeigen des vorherigen Panels | `Ctrl`+`[` | `Command`+`[` |  
| Docken Sie das devtools an der zuletzt verwendeten Position an.  Wenn der devtools für die gesamte Sitzung in der Standardposition verbleibt, wird die devtools in einem separaten Fenster von dieser Verknüpfung Abdocken. | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| **Gerätemodus** umschalten | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Umschalten des **Element Modus überprüfen** , mit dem Sie ein Element auf der Website auswählen und den HTML-und CSS-Code im **Element Panel anzeigen** können | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Anzeigen des Befehlsmenüs | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Einblenden/Ausblenden der Schublade | `Esc` | `Esc` |  
| Aktualisieren.  Dadurch wird die Seite mit dem Cache aktualisiert.  | `F5` oder `Ctrl`+`R` | `Command`+`R` |  
| Harte Aktualisierung.  Dadurch wird Microsoft Edge gezwungen, Ressourcen erneut herunterzuladen und neu zu laden.  Möglicherweise stammen die verwendeten Ressourcen aus einer zwischengespeicherten Version. | `Ctrl`+`F5` oder `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Suchen nach Text im aktuellen Bereich  Wird in den Bereichen Audits, Anwendung und Sicherheit nicht unterstützt | `Ctrl`+`F` | `Command`+`F` |  
| Anzeigen der Suchleiste in der Schublade, mit der Sie nach Text über alle geladenen Ressourcen suchen können | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Öffnen einer Datei im Quellen Panel | `Ctrl`+`O` oder `Ctrl`+`P` | `Command`+`O` oder `Command`+`P` |  
| Heranzoomen | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Verkleinern | `Ctrl`+`-` | `Command`+`-` |  
| Standardzoom Stufe wiederherstellen | `Ctrl`+`0` | `Command`+`0` |  
| Ausführen eines Snippets | `Ctrl`+`O`oder `Ctrl` + `P` geben `!` Sie gefolgt vom Namen des Skripts ein, und drücken Sie dann `Enter` | Drücken Sie `Command` + `O` oder `Command` + `P` , geben Sie `!` gefolgt vom Namen des Skripts ein, und drücken Sie dann `Enter` |  
| Anzeigen des nicht bearbeitbaren HTML-Quellcodes auf einer neuen Registerkarte | `Ctrl`+`U` | n.a. |  

> [!NOTE]
> Wenn Sie das Debugging durchgeführt und an einem Haltepunkt angehalten haben, wird die Laufzeit zuerst mit der **Aktualisierungs** Verknüpfung fortgesetzt.  

## Weitere Informationen  

*   [DevTools für Anfänger: Erste Schritte mit HTML und dem Dom][DevtoolsGuideChromiumBeginnersHtml]  
*   [Microsoft Edge (Chrom)-devtools-Protokoll][DevtoolsProtocolChromiumIndex]  

## Kontakt mit dem Microsoft Edge devtools-Team  

Bitte senden Sie Ihr Feedback, damit das Microsoft Edge-Team die Microsoft Edge-devtools für Sie weiter verbessert.  Wählen Sie einfach das **Feedback** -Symbol im devtools aus, oder drücken Sie `Alt` + `Shift` + `I` unter Windows \ ( `Option` + `Shift` + `I` unter macOS \), und geben Sie Feedback-oder Funktionsanforderungen für das devtools ein.  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Feedback zu Microsoft Edge geben":::
   Feedback zu Microsoft Edge geben  
:::image-end:::  

Wenn Sie eine Vorschau der [neuesten Features in devtools][DevtoolsGuideChromiumWhatsNewIndex]anzeigen möchten, laden Sie [Microsoft Edge Canary][MicrosoftedgeinsiderDownload]herunter, das nächtlich erstellt wird.  

<!-- image links -->  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools für Anfänger: Erste Schritte mit HTML und dem Dom | Microsoft docs"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools "Neuerungen in Microsoft Edge (Chrom) devtools | Microsoft docs"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Microsoft Edge (Chrom) devtools-Protokoll | Microsoft docs"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Microsoft Edge-Add-ons"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Erweiterungen | Chrome Web Store"  
