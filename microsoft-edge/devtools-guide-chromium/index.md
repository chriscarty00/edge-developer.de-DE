---
description: Einführung in die Microsoft Edge-Entwicklungstools (Chromium)
title: Microsoft Edge (Chromium)-Entwicklungstools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: fcae8f0974244e87ba781b94221cb5d8a1bb3dce
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233604"
---
# Microsoft Edge (Chrom) – Übersicht über Entwickler Tools  

Microsoft Edge hat das Chrom-Open-Source-Projekt angenommen, um eine bessere Web-Kompatibilität und geringere Fragmentierung unterschiedlicher zugrundeliegender Webplattformen zu schaffen.  Diese Änderungen sollte es Ihnen einfacher machen, Ihre Websites in Microsoft Edge zu erstellen und zu testen, und sicherzustellen, dass sie wie erwartet funktionieren, wenn sie in einem anderen Browser auf Chromium-Basis \(wie Google Chrome, Vivaldi, Opera, oder Brave\) angezeigt werden.  

Da das Web immer stärker auf immer mehr Gerätetypen genutzt wird, sind die Komplexität und der Mehraufwand beim Testen von Websites in die Höhe geschossen. Webentwickler müssen \(besonders in kleinen Unternehmen\) so viele verschiedene Systeme testen, dass es beinahe unmöglich ist sicherzustellen, dass Websites auf allen Gerätetypen und in allen Browsern gut funktionieren.  Da nun Microsoft Edge auf Chromium basiert, hat das Microsoft Edge-Team die Matrix vereinfacht, indem die Microsoft Edge-Webplattform an andere Browsern auf Chromium-Basis angepasst wurde. Außerdem wird jetzt sowohl im Browser als auch in den weiteren Entwicklungstools, die Sie täglich benutzen \(wie Visual Studio Code\)., erstklassige Benutzerfreundlichkeit geboten.  

Wenn Sie Microsoft Edge ausprobieren und bisher hauptsächlich in einem Browser auf Chromium-Basis entwickelt haben, sollten Sie sich wie zuhause fühlen.  Die Microsoft Edge \(Chromium\)-Entwicklungstools funktionieren auf die gleiche Weise wie die Entwicklungstools, die Sie bereits kennen und verwenden.  Weitere Informationen finden Sie unter [Neuerungen in der Microsoft Edge (Chrom)-devtools][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (Chromium)-Entwicklungstools (DevTools)" lightbox="./media/devtools.png":::
   Microsoft Edge (Chromium)-Entwicklungstools (DevTools)  
:::image-end:::  

Wenn Sie den neuen Microsoft Edge Auschecken und zuvor in Microsoft Edge \ (EdgeHTML \) entwickelt haben, verfügen Sie nun über einige hervorragende neue Tools, die es einfacher und schneller machen, ihre Websites in Microsoft Edge zu erstellen und zu testen.  

## Entwicklungstools öffnen  

Falls Sie die Entwicklungstools noch nie verwendet haben: Bei den Microsoft Edge-Entwicklungstools handelt es sich um eine Reihe von Tools, die direkt in den Microsoft Edge-Browser integriert sind.  Mit dem devtools können Sie die folgenden Aktionen ausführen:  

*   Ihre HTML-Website überprüfen und ändern  
*   CSS bearbeiten und sofort in der Vorschau sehen, wie Ihre Website gerendert wird  
*   Alle `console.log()` Anweisungen aus Ihrem Front-End-Code in JavaScript anzeigen  
*   Ihr Skript debuggen, indem Haltepunkte festgelegt und diese zeilenweise durchlaufen werden  
    
Alle direkt im Browser.  Das sind nur einige Beispiele für die Features, die Ihnen in den Entwicklungstools zur Verfügung stehen, damit Sie einfacher und schneller Ihre Websites in Microsoft Edge erstellen und testen können.  

So öffnen Sie die Entwicklungstools  

*   Auswählen `F12` 
*   `Ctrl` + `Shift` + `I` Unter Windows/Linux auswählen \ ( `Command` + `Option` + `I` unter macOS \)  
    
Wenn Sie den HTML-oder CSS-Code für ein Element auf Ihrer Website anzeigen möchten, klicken Sie mit der rechten Maustaste auf das Element, und wählen Sie **Prüfen** aus, um in den Bereich „Elemente“ zu wechseln.  Sie können auch `Ctrl`+`Shift`+`C` auf Windows/Linux \(`Command`+`Option`+`C` auf macOS\) drücken, um die Entwicklungstools im **Modus „Element prüfen“** zu öffnen. So können Sie ein Element auf der Website auswählen und den HTML- und CSS-Code im Bereich **Elemente** ansehen.  

Wenn Sie die Protokolle aus Ihrem Front-End-JavaScript-Code anzeigen oder schnell ein Skript ausführen möchten, wählen Sie `Ctrl` + `Shift` + `J` unter Windows/Linux oder `Command` + `Option` + `J` unter macOS aus, um den **Konsolen** Bereich im devtools zu starten.  

## Grundlegende Tools  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Microsoft Edge (Chromium)-DevTools – Grundlegende Tools" lightbox="./media/devtools-core-tools.png":::
   Microsoft Edge (Chromium)-DevTools – Grundlegende Tools  
:::image-end::: 

Die Microsoft Edge \(Chromium\)-DevTools umfassen die folgenden Bereiche.  

*   Einen Bereich **Elemente** zum Bearbeiten von HTML und CSS, Untersuchen von Barrierefreiheitseigenschaften, Anzeigen von Ereignis-Listenern und Festlegen von Haltepunkten für DOM-Mutationen  
*   Eine **Konsole** zum Anzeigen und Filtern von Protokollmeldungen, zum Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Rahmens  
*   Einen Bereich **Quellen**, in dem Sie Ihren Code öffnen und ihn live bearbeiten, Haltepunkte festlegen, den Code Schritt für Schritt durchlaufen, und den Zustand Ihrer Website je JavaScript-Zeile anzeigen können  
*   Einen Bereich **Netzwerk** zum Überwachen und Überprüfen von Anforderungen und Antworten aus dem Netzwerk- und Browsercache   
*   Einen Bereich **Leistung**, um die Zeit und Systemressourcen zu ermitteln, die für Ihre Website erforderlich sind  
*   Einen Bereich **Arbeitsspeicher** zum Messen der Nutzung von Speicherressourcen und Vergleichen von Heap-Momentaufnahmen in unterschiedlichen Zuständen der Code-Runtime  
*   Einen Bereich **Anwendung** zum Untersuchen, Anpassen und Debuggen von Web-App-Manifesten, Service Workers, und Service Worker-Caches.  Sie können Speicher, Datenbanken und Caches auch im Bereich **Anwendung** prüfen und verwalten.  
*   Einen Bereich **Sicherheit** zum Debuggen von Sicherheitsproblemen und Sicherstellen, dass Sie HTTPS ordnungsgemäß auf Ihrer Website implementiert haben.  HTTPS bietet wichtige Sicherheit und Datenintegrität sowohl für Ihre Website als auch für Ihre Benutzer, die auf Ihrer Website personenbezogene Daten angeben.  
*   Einen Bereich **Überwachung** \(jetzt unter dem neuen Namen **Lighthouse**\), in dem Sie eine Überwachung Ihrer Website veranlassen können.  Die Ergebnisse der Überwachung helfen Ihnen dabei, die Qualität Ihrer Website folgendermaßen zu verbessern.  
    *   Erfassen häufiger Fehler in Bezug darauf, Ihre Website barrierefrei, sicher, leistungsstark, und so weiter zu gestalten.  
    *   Alle Fehler beheben.  
    *   Eine PWA erstellen.  
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Bitte senden Sie Ihre [Feedback-und Funktionswünsche](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## Erweiterungen  

Möglicherweise haben Sie Erweiterungen der Entwicklungstools verwendet, um Probleme beim Erstellen Ihrer Websites oder Apps besser erkennen und debuggen zu können.  Erweiterungen für Microsoft Edge erhalten Sie auf der Seite [Microsoft Edge Add-Ons][MicrosoftEdgeAddonsExtensions].  Auf der Seite [Microsoft Edge Add-Ons][MicrosoftEdgeAddonsExtensions] können Sie Erweiterungen für die Entwicklungstools in der Kategorie **Entwicklungstools** durchsuchen, oder nach einer bestimmten Erweiterung suchen.  

Sie können auch Erweiterungen aus dem [Chrome Web Store][GoogleChromeWebstoreExtensions] hinzufügen.  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Chrome Web Store in Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Chrome Web Store in Microsoft Edge  
:::image-end:::  

Wählen Sie oben im Dialogfeld, das angezeigt wird, die Option **Erweiterungen von anderen speichern zulassen aus** , und wählen Sie dann **zulassen** aus.  

> [!NOTE]
> Erweiterungen, die aus anderen Quellen als dem Microsoft Store installiert werden, sind nicht verifiziert, und können die Browser-Leistung beeinträchtigen.  

Wählen Sie **zu Chrome hinzufügen** aus, um Ihre devtools-Erweiterung zu Microsoft Edge hinzuzufügen.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Hinzufügen einer Erweiterung von Chrome Web Store zu Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Hinzufügen einer Erweiterung von Chrome Web Store zu Microsoft Edge  
:::image-end:::  

## Tastenkombinationen  

Diese Tastenkombinationen steuern das Hauptfenster der Entwicklungstools, funktionieren in allen Tools, oder beides.  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Entwicklungstools ein-/ausblenden\(zuletzt angezeigter Bereich wird geöffnet\) | `F12` oder `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Anzeigen des Bereichs „Konsole“ | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Anzeigen der devtools im **Element Modus überprüfen** , mit dem Sie ein Element auf der Website auswählen und den HTML-und CSS-Code im **Element Panel anzeigen** können | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Einstellungen anzeigen | `?` oder `Fn`+`F1` | `?` oder `Fn`+`F1` |  
| Anzeigen des nächsten Bereichs | `Ctrl`+`]` | `Command`+`]` |  
| Anzeigen des vorherigen Bereichs | `Ctrl`+`[` | `Command`+`[` |  
| Entwicklungstools in der letzten verwendeten Position andocken.  Wenn der devtools für die gesamte Sitzung in der Standardposition verbleibt, wird der devtools in einem separaten Fenster von der Verknüpfung Abdocken. | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| **Gerätemodus** einschalten | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Schalten Sie den **Modus „Element prüfen“** ein, in dem Sie ein Element auf der Website auswählen und das HTML und CSS im Bereich **Elemente** ansehen können | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Anzeigen des Befehlsmenüs | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Einblenden/Ausblenden der Schublade | `Esc` | `Esc` |  
| Aktualisieren.  Fefreshes Sie die Seite mit dem Cache.  | `F5` oder `Ctrl`+`R` | `Command`+`R` |  
| Harte Aktualisierung.  Zwingt Microsoft Edge, Ressourcen erneut herunterzuladen und neu zu laden.  Möglicherweise stammen die verwendeten Ressourcen aus einer zwischengespeicherten Version | `Ctrl`+`F5` oder `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Im aktuellen Bereich nach Text suchen.  Wird in den Bereichen Überwachung, Anwendung und Sicherheit nicht unterstützt | `Ctrl`+`F` | `Command`+`F` |  
| In der Schublade den Bereich Suche anzeigen, in dem Sie in allen geladenen Ressourcen nach Text suchen können | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Im Bereich Quellen eine Datei öffnen | `Ctrl`+`O` oder `Ctrl`+`P` | `Command`+`O` oder `Command`+`P` |  
| Vergrößern | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Verkleinern | `Ctrl`+`-` | `Command`+`-` |  
| Standardzoom wiederherstellen | `Ctrl`+`0` | `Command`+`0` |  
| Ausführen eines Codeausschnitts | `Ctrl`+`O` oder `Ctrl`+`P`, geben Sie `!` und den Namen des Skripts ein, drücken Sie dann `Enter` | Drücken Sie `Command`+`O` oder `Command`+`P` , geben Sie `!` und den Namen des Skrips ein, drücken Sie dann `Enter` |  
| Nicht-bearbeitbaren HTML-Quellcode in neuer Registerkarte anzeigen | `Ctrl`+`U` | n.a. |  

> [!NOTE]
> Wenn Sie das Debugging durchgeführt und an einem Haltepunkt angehalten haben, wird die Laufzeit zuerst mit der Tastenkombination **Aktualisierung** fortgesetzt.  

## Weitere Informationen  

*   [Entwicklungstools für Einsteiger: Erste Schritte mit HTML und dem DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Microsoft Edge (Chromium) DevTools Protocol][DevtoolsProtocolChromiumIndex]  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Wenn Sie eine Vorschau der [neusten Features für die Entwicklungstools anzeigen möchten][DevtoolsGuideChromiumWhatsNewIndex], laden Sie [Microsoft Edge Canary][MicrosoftedgeinsiderDownload] mit nächtlichen Builds herunter.  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "Entwicklungstools für Einsteiger: Erste Schritte mit HTML und dem DOM | Microsoft-Dokumentation"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools "Neuigkeiten in den Microsoft Edge (Chromium)- DevTools | Microsoft-Dokumentation"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Microsoft Edge (Chromium) Entwicklungstools-Protokoll | Microsoft-Dokumentation"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Microsoft Edge-Add-Ons"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Erweiterungen | Chrome Web Store"  
