---
description: Einführung in die Microsoft Edge-Entwicklungstools (Chromium)
title: Microsoft Edge (Chromium)-Entwicklungstools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 05b757b7cb399815d072b9d6038873cfd118a59d
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327491"
---
# Übersicht über Microsoft Edge (Chromium)-Entwicklertools  

Microsoft Edge hat das Open-Source-Projekt Chromium übernommen.  Der neue Microsoft Edge-Browser sorgt für eine bessere Webkompatibilität und verringert die Fragmentierung verschiedener Webplattformen.  Die Änderung sollte ihnen das Erstellen und Testen Ihrer Webseiten in Microsoft Edge erleichtern.  Mit dem neuen Microsoft Edge sollten Ihre Webseiten wie erwartet funktionieren, wenn sie in anderen Chromium-basierten Browsern geöffnet werden.  Chromium-basierte Browser umfassen Google Chrome, Chromeldi, Opera, Chrome und das neue Microsoft Edge.  

Die Nutzung des Webs hat sich in einem ständig wachsenden Array von Gerätetypen vergrößert.  Die Komplexität und der Aufwand für das Testen von Webseiten sind schnell größer geworden.  Webentwickler wie Sie müssen mit vielen verschiedenen Systemen testen.  Um sicherzustellen, dass Ihre Webseiten auf allen Gerätetypen und Browsern gut funktionieren, kann es fast unmöglich sein, insbesondere, wenn Sie in einem kleinen Unternehmen arbeiten.  Der neue Microsoft Edge basiert jetzt auf Chromium.  Das Microsoft Edge-Team hat die Matrix vereinfacht, indem die Microsoft Edge-Webplattform an anderen Chromium-basierten Browsern ausgerichtet wurde.  Das neue Microsoft Edge bietet eine erstklassige Entwicklungsumgebung.  Die Erfahrung wird innerhalb des Browsers und zusammen mit den anderen Entwicklertools, die Sie täglich verwenden, wie z. B. Visual Studio Code.  

Als Chromium-basierter Browserentwickler sollten Sie sich mit dem neuen Microsoft Edge-Browser wohl fühlen.  Die Microsoft Edge \(Chromium\) DevTools funktionieren genau wie die Entwicklertools, die Sie bereits kennen und verwenden.  Die Microsoft Edge \(Chromium\)-Entwicklertools werden häufig als Microsoft Edge \(Chromium\) DevTools oder DevTools bezeichnet.  Weitere Informationen finden Sie in den [Microsoft Edge (Chromium)-DevTools.][DevtoolsGuideChromiumWhatsNewIndex]  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (Chromium)-Entwicklungstools (DevTools)" lightbox="./media/devtools.png":::
   Microsoft Edge (Chromium)-Entwicklungstools (DevTools)  
:::image-end:::  

Wenn Sie zuvor für Microsoft Edge \(EdgeHTML\) entwickelt haben und das neue Microsoft Edge auswerten, bietet es jetzt großartige neue Tools zum einfacheren und schnelleren Erstellen und Testen Ihrer Webseiten.  

## Entwicklungstools öffnen  

Die Microsoft Edge DevTools sind eine Reihe von Tools, die direkt in den Microsoft Edge Browser integrierten sind.  Mit devTools können Sie die folgenden Aufgaben alle direkt im Browser ausführen.  

*   Überprüfen und Vornehmen von Änderungen an Ihrer HTML-Webseite  
*   Bearbeiten sie CSS, und sehen Sie sofort eine Vorschau, wie Ihre Webseite gerendert wird  
*   Überprüfen Sie alle `console.log()` Anweisungen aus Ihrem Front-End-JavaScript-Code.  
*   Debuggen Des Skripts, Festlegen von Haltepunkten und Schrittweises Durchschritten des Codes zeile für Zeile  
    
Weitere Beispiele für die Features, die DevTools bereitstellen, um das Erstellen und Testen Ihrer Webseite in Microsoft Edge zu vereinfachen und zu beschleunigen.  

So öffnen Sie die Entwicklungstools  

*   Auswählen `F12` 
*   Wählen `Ctrl` + `Shift` + `I` Sie \(Windows/Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.  
    
Wenn Sie den HTML- oder CSS-Code für ein Element auf **** Ihrer Website anzeigen möchten, klicken Sie mit der rechten Maustaste auf das Element, und wählen Sie "Überprüfen" aus, um in das **Elementtool zu** springen.  Um die DevTools im **Elementmodus**zu öffnen, wählen Sie `Ctrl` + `Shift` + `C` \(Windows/Linux\) oder `Command` + `Option` + `C` \(macOS\) aus. Im **Elementmodus "Überprüfen"** können Sie ein Element auf der Webseite auswählen und HTML und CSS im Tool **"Elemente"** anzeigen.  

Wenn Sie Protokolle aus Ihrem Front-End-JavaScript-Code überprüfen oder schnell Skripts ausführen möchten, öffnen Sie die **Konsole.**   Um das **Konsolentool** in devTools zu starten, wählen Sie `Ctrl` + `Shift` + `J` \(Windows/Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  

## Grundlegende Tools  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Microsoft Edge (Chromium)-DevTools – Grundlegende Tools" lightbox="./media/devtools-core-tools.png":::
   Microsoft Edge (Chromium)-DevTools – Grundlegende Tools  
:::image-end::: 

Die Microsoft Edge \(Chromium\) DevTools enthalten die folgenden Tools.  

*   Ein **Elementtool** zum Bearbeiten von HTML und CSS, Überprüfen von Barrierefreiheitseigenschaften, Anzeigen von Ereignislistenern und Festlegen von HALTEpunkten der DOM-Mutation  
*   Eine **Konsole zum** Überprüfen und Filtern von Protokollmeldungen, Überprüfen von JavaScript-Objekten und DOM-Knoten und Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Frames  
*   Ein **Quellentool** zum Öffnen und Bearbeiten des Codes, Festlegen von Haltepunkten, Schrittweises Durchschritten von Code und Anzeigen des Status Ihrer Webseite
*   Ein **Netzwerktool** zum Überwachen und Überprüfen von Anforderungen und Antworten aus dem Netzwerk- und Browsercache   
*   Ein **Leistungstool** zum Profilieren der für Ihre Website erforderlichen Zeit- und Systemressourcen  
*   Ein **Speichertool** zum Messen der Verwendung von Speicherressourcen und Vergleichen von Heapmomentaufnahmen bei unterschiedlichen Zuständen der Codelaufzeit  
*   Ein **Anwendungstool** zum Überprüfen, Ändern und Debuggen von Web-App-Manifesten, Service Workern und Dienstarbeitscaches.  Sie können auch Speicher, Datenbanken und Caches über das **Anwendungstool** überprüfen und verwalten.  
*   Ein **Sicherheitstool** zum Debuggen von Sicherheitsproblemen und sicherstellen, dass SIE HTTPS auf Ihrer Webseite ordnungsgemäß implementiert haben.  HTTPS bietet wichtige Sicherheit und Datenintegrität sowohl für Ihre Website als auch für Ihre Benutzer, die auf Ihrer Website personenbezogene Daten angeben.  
*   Ein **Überwachungstool** \(jetzt umbenannt in **"Unteres**\") zum Ausführen einer Überwachung Ihrer Webseite.  Die Ergebnisse der Überwachung helfen Ihnen dabei, die Qualität Ihrer Website folgendermaßen zu verbessern.  
    *   Fangen Sie häufige Fehler im Zusammenhang mit der Barrierefreie, sichere, performante und so weiter.  
    *   Alle Fehler beheben.  
    *   Eine PWA erstellen.  
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Senden Sie Ihr [Feedback und Ihre Featureanforderungen.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## Extensions  

Möglicherweise haben Sie auf DevTools mithilfe von Erweiterungen zugegriffen, wenn Sie Während der Webseitenerstellen \(oder Apps\) Probleme diagnostizieren und debuggen. Microsoft Edge Erweiterungen werden von [Microsoft Edge-Add-Ons erworben.][MicrosoftEdgeAddonsExtensions]  Durchsuchen [Sie in Microsoft Edge-Add-Ons][MicrosoftEdgeAddonsExtensions]die DevTools-Erweiterungen aus der Kategorie **"Entwicklertools",** oder suchen Sie nach einer bestimmten Erweiterung.  

Sie können auch Erweiterungen aus dem [Chrome Web Store][GoogleChromeWebstoreExtensions] hinzufügen.  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Chrome Web Store in Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Chrome Web Store in Microsoft Edge  
:::image-end:::  

At the top, choose **Allow extensions from other stores** and then choose **Allow** in the dialog that appears.  

> [!NOTE]
> Erweiterungen, die aus anderen Quellen als dem Microsoft Store installiert werden, sind nicht verifiziert, und können die Browser-Leistung beeinträchtigen.  

Choose **Add to Chrome** to add your DevTools extension to Microsoft Edge.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Hinzufügen einer Erweiterung aus dem Chrome Web Store zu Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Hinzufügen einer Erweiterung aus dem Chrome Web Store zu Microsoft Edge  
:::image-end:::  

## Tastenkombinationen  

Die folgenden Verknüpfungen steuern das Hauptfenster von DevTools, arbeiten über alle Tools hinweg oder beides.  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Einblenden/Ausblenden von DevTools \(öffnet sich zum zuletzt angezeigten Tool\) | `F12` oder `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Anzeigen der Konsole | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Anzeigen der DevTools im **Elementmodus "Untersuchen",** mit dem Sie ein Element auswählen und HTML und CSS im Tool **"Elemente"** anzeigen können | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Einstellungen anzeigen | `?` oder `Fn`+`F1` | `?` oder `Fn`+`F1` |  
| Anzeigen des nächsten Bereichs | `Ctrl`+`]` | `Command`+`]` |  
| Anzeigen des vorherigen Bereichs | `Ctrl`+`[` | `Command`+`[` |  
| Entwicklungstools in der letzten verwendeten Position andocken.  Wenn die DevTools für die gesamte Sitzung an der Standardposition bleiben, werden die DevTools mit der Verknüpfung in ein separates Fenster entfernt. | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| **Gerätemodus** einschalten | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Toggle **Inspect Element Mode** that allows you to choose an element and display the HTML and CSS in the **Elements** tool | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Anzeigen des Befehlsmenüs | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Einblenden/Ausblenden der Schublade | `Esc` | `Esc` |  
| Aktualisieren.  Aktualisiert die Webseite mithilfe des Caches.  | `F5` oder `Ctrl`+`R` | `Command`+`R` |  
| Harte Aktualisierung.  Erzwingt Microsoft Edge, Ressourcen erneut herunterzuladen und neu zu laden.  Die verwendeten Ressourcen stammen möglicherweise aus einer zwischengespeicherten Version. | `Ctrl`+`F5` oder `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Im aktuellen Bereich nach Text suchen.  Nicht unterstützt in den Überwachungs-, Anwendungs- und Sicherheitstools | `Ctrl`+`F` | `Command`+`F` |  
| Anzeigen des Suchtools in der Drawer, mit dem Sie in allen geladenen Ressourcen nach Text suchen können | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
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
