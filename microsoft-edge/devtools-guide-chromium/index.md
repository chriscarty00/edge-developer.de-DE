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
ms.openlocfilehash: fa407393f8ecb79a3382294742bf9061787ec04a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397703"
---
# <a name="microsoft-edge-chromium-developer-tools-overview"></a>Übersicht über Microsoft Edge (Chromium)-Entwicklertools  

Microsoft Edge hat das Open-Source-Projekt Chromium übernommen.  Der neue Microsoft Edge-Browser sorgt für eine bessere Webkompatibilität und reduziert die Fragmentierung verschiedener Webplattformen.  Die Änderung sollte es Ihnen erleichtern, Ihre Webseiten in Microsoft Edge zu erstellen und zu testen.  Das neue Microsoft Edge sollte Ihre Webseiten beim Öffnen in anderen Chromium-basierten Browsern dabei unterstützen, wie erwartet zu funktionieren.  Chrombasierte Browser umfassen Google Chrome, Vivaldi, Opera, Brave und das neue Microsoft Edge.  

Das Web ist in einem immer größer werdenden Array von Gerätetypen in der Nutzung gewachsen.  Die Komplexität und der Aufwand für das Testen von Webseiten sind rapide gestiegen.  Webentwickler wie Sie müssen mit vielen verschiedenen Systemen testen.  Um sicherzustellen, dass Ihre Webseiten auf allen Gerätetypen und Browsern gut funktionieren, ist dies möglicherweise nahezu unmöglich, insbesondere wenn Sie in einem kleinen Unternehmen arbeiten.  Das neue Microsoft Edge basiert jetzt auf Chromium.  Das Microsoft Edge-Team hat die Matrix vereinfacht, indem die Microsoft Edge-Webplattform an anderen Chromium-basierten Browsern ausgerichtet wurde.  Das neue Microsoft Edge bietet eine erstklassige Entwicklungsumgebung.  Die Erfahrung erfolgt im Browser und zusammen mit den anderen Entwicklertools, die Sie täglich verwenden, z. B. Visual Studio Code.  

Als Chromium-basierter Browserentwickler sollten Sie sich mit dem neuen Microsoft Edge-Browser wohl fühlen.  Die Microsoft Edge \(Chromium\) DevTools funktionieren genauso wie die Entwicklertools, die Sie bereits kennen und verwenden.  Die Microsoft Edge \(Chromium\) Developer Tools werden häufig als Microsoft Edge \(Chromium\) DevTools oder DevTools bezeichnet.  Weitere Informationen finden Sie unter [What's new in the Microsoft Edge (Chromium) DevTools][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (Chromium)-Entwicklungstools (DevTools)" lightbox="./media/devtools.png":::
   Microsoft Edge (Chromium)-Entwicklungstools (DevTools)  
:::image-end:::  

Wenn Sie zuvor für Microsoft Edge \(EdgeHTML\) entwickelt haben und das neue Microsoft Edge auswerten, bietet es ihnen jetzt großartige neue Tools, um Ihre Webseiten einfacher und schneller zu erstellen und zu testen.  

## <a name="open-the-devtools"></a>Entwicklungstools öffnen  

Die Microsoft Edge DevTools sind eine Reihe von Tools, die direkt in den Microsoft Edge-Browser integrierten.  Mit devTools können Sie die folgenden Aufgaben direkt im Browser ausführen.  

*   Überprüfen und Vornehmen von Änderungen an Ihrer HTML-Webseite  
*   Bearbeiten von CSS und sofortiges Anzeigen der Vorschau, wie Ihre Webseite gerendert wird  
*   Überprüfen Aller Anweisungen `console.log()` aus Ihrem Front-End-JavaScript-Code  
*   Debuggen Des Skripts, Festlegen von Haltepunkten und Schrittweises Durchbrechen der Codezeile nach Zeile  
    
Weitere Beispiele für die Features, die DevTools bereitstellen, um das Erstellen und Testen Ihrer Webseite in Microsoft Edge zu vereinfachen und zu beschleunigen.  

So öffnen Sie die Entwicklungstools  

*   Auswählen `F12` 
*   Wählen `Ctrl` + `Shift` + `I` Sie \(Windows/Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.  
    
Wenn Sie html oder CSS für ein Element auf Ihrer Website anzeigen möchten, klicken Sie mit der rechten Maustaste auf das Element, und wählen Sie **Überprüfen** aus, um in das **Elementtool zu** springen.  Wählen Sie **** `Ctrl` + `Shift` + `C` \(Windows/Linux\) oder `Command` + `Option` + `C` \(macOS\) aus, um die DevTools im Inspect-Elementmodus zu öffnen. Im **Inspect-Elementmodus** können Sie ein Element auf der Webseite auswählen und html und CSS im **Elementtool** anzeigen.  

Wenn Sie Protokolle aus Ihrem Front-End-JavaScript-Code überprüfen oder schnell skripts ausführen möchten, öffnen Sie die **Konsole**.   Um das **Konsolentool** in devTools zu starten, wählen `Ctrl` + `Shift` + `J` Sie \(Windows/Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  

## <a name="core-tools"></a>Grundlegende Tools  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Microsoft Edge (Chromium)-DevTools – Grundlegende Tools" lightbox="./media/devtools-core-tools.png":::
   Microsoft Edge (Chromium)-DevTools – Grundlegende Tools  
:::image-end::: 

Die Microsoft Edge \(Chromium\) DevTools enthalten die folgenden Tools.  

*   Ein **Elements-Tool** zum Bearbeiten von HTML und CSS, Überprüfen von Barrierefreiheitseigenschaften, Anzeigen von Ereignislistenern und Festlegen von DOM-Mutations-Haltepunkten  
*   Eine **Konsole zum** Überprüfen und Filtern von Protokollmeldungen, Überprüfen von JavaScript-Objekten und DOM-Knoten und Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Frames  
*   Ein **Quellentool** zum Öffnen und Bearbeiten Des Codes, Festlegen von Haltepunkten, Schrittweises Durchbrechen von Code und Anzeigen des Status Ihrer Webseite
*   Ein **Netzwerktool** zum Überwachen und Überprüfen von Anforderungen und Antworten aus dem Netzwerk- und Browsercache   
*   Ein **Performance-Tool** zum Profilieren der Zeit- und Systemressourcen, die für Ihre Website erforderlich sind  
*   Ein **Speichertool** zum Messen der Verwendung von Arbeitsspeicherressourcen und Vergleichen von Heapmomentaufnahmen in unterschiedlichen Zuständen der Codelaufzeit  
*   Ein **Anwendungstool** zum Überprüfen, Ändern und Debuggen von Web-App-Manifesten, Servicemitarbeitern und Dienstarbeitercaches.  Sie können auch Speicher, Datenbanken und Caches aus dem Anwendungstool überprüfen **und** verwalten.  
*   Ein **Sicherheitstool** zum Debuggen von Sicherheitsproblemen und sicherstellen, dass Sie HTTPS auf Ihrer Webseite ordnungsgemäß implementiert haben.  HTTPS bietet wichtige Sicherheit und Datenintegrität sowohl für Ihre Website als auch für Ihre Benutzer, die auf Ihrer Website personenbezogene Daten angeben.  
*   Ein **Überwachungstool** \(jetzt **umbenannt in "Leuchtturm**\") zum Ausführen einer Überwachung Ihrer Webseite.  Die Ergebnisse der Überwachung helfen Ihnen dabei, die Qualität Ihrer Website folgendermaßen zu verbessern.  
    *   Fangen Sie häufige Fehler im Zusammenhang mit dem Zugriff auf Ihre Webseite, Sicherheit, Leistung und so weiter ab.  
    *   Alle Fehler beheben.  
    *   Eine PWA erstellen.  
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Senden Sie Ihr [Feedback und Featureanforderungen.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## <a name="extensions"></a>Erweiterungen  

Möglicherweise haben Sie auf DevTools mithilfe von Erweiterungen zugegriffen, wenn Sie Beim Erstellen Ihrer Webseiten \(oder Apps\) Probleme diagnostizieren und debuggen. Microsoft Edge-Erweiterungen werden von [Microsoft Edge-Add-Ons erworben.][MicrosoftEdgeAddonsExtensions]  Durchsuchen [Sie in Microsoft Edge-Add-Ons DevTools-Erweiterungen][MicrosoftEdgeAddonsExtensions]aus der Kategorie **Entwicklertools,** oder suchen Sie nach einer bestimmten Erweiterung.  

Sie können auch Erweiterungen aus dem [Chrome Web Store][GoogleChromeWebstoreExtensions] hinzufügen.  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Chrome Web Store in Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Chrome Web Store in Microsoft Edge  
:::image-end:::  

Wählen Sie oben Erweiterungen **aus** anderen Speichern zulassen aus, und klicken Sie dann **im** angezeigten Dialogfeld auf Zulassen.  

> [!NOTE]
> Erweiterungen, die aus anderen Quellen als dem Microsoft Store installiert werden, sind nicht verifiziert, und können die Browser-Leistung beeinträchtigen.  

Wählen **Sie Zu Chrome hinzufügen aus,** um Ihre DevTools-Erweiterung zu Microsoft Edge hinzuzufügen.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Hinzufügen einer Erweiterung aus dem Chrome Web Store zu Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Hinzufügen einer Erweiterung aus dem Chrome Web Store zu Microsoft Edge  
:::image-end:::  

## <a name="shortcuts"></a>Tastenkombinationen  

Die folgenden Tastenkombinationen steuern das Hauptfenster devTools, arbeiten über alle Tools hinweg oder beides.  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Ein-/Ausblenden von DevTools \(öffnet zum zuletzt angezeigten Tool\) | `F12` oder `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Anzeigen der Konsole | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Anzeigen der DevTools im **Inspect-Elementmodus,** mit dem Sie ein Element auswählen und html und CSS im **Elementtool anzeigen** können | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Einstellungen anzeigen | `?` oder `Fn`+`F1` | `?` oder `Fn`+`F1` |  
| Anzeigen des nächsten Bereichs | `Ctrl`+`]` | `Command`+`]` |  
| Anzeigen des vorherigen Bereichs | `Ctrl`+`[` | `Command`+`[` |  
| Entwicklungstools in der letzten verwendeten Position andocken.  Wenn die DevTools für die gesamte Sitzung an der Standardposition bleiben, werden die DevTools mit der Verknüpfung in ein separates Fenster entfernt. | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| **Gerätemodus** einschalten | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| **Umschalten des Inspect-Elementmodus,** mit dem Sie ein Element auswählen und html und CSS im **Elementtool anzeigen** können | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Anzeigen des Befehlsmenüs | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Einblenden/Ausblenden der Schublade | `Esc` | `Esc` |  
| Aktualisieren.  Aktualisiert die Webseite mithilfe des Caches.  | `F5` oder `Ctrl`+`R` | `Command`+`R` |  
| Harte Aktualisierung.  Erzwingt Microsoft Edge, Ressourcen erneut herunterzuladen und neu zu laden.  Die verwendeten Ressourcen stammen möglicherweise aus einer zwischengespeicherten Version. | `Ctrl`+`F5` oder `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Im aktuellen Bereich nach Text suchen.  Nicht unterstützt in den Überwachungs-, Anwendungs- und Sicherheitstools | `Ctrl`+`F` | `Command`+`F` |  
| Anzeigen des Suchtools in der Schublade, mit dem Sie nach Text in allen geladenen Ressourcen suchen können | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Im Bereich Quellen eine Datei öffnen | `Ctrl`+`O` oder `Ctrl`+`P` | `Command`+`O` oder `Command`+`P` |  
| Vergrößern | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Verkleinern | `Ctrl`+`-` | `Command`+`-` |  
| Standardzoom wiederherstellen | `Ctrl`+`0` | `Command`+`0` |  
| Ausführen eines Codeausschnitts | `Ctrl`+`O`oder `Ctrl` + `P` , geben `!` Sie gefolgt vom Namen des Skripts ein, und wählen Sie dann `Enter` | Wählen `Command` + `O` Sie `Command` + `P` oder , geben Sie `!` gefolgt vom Namen des Skripts ein, und wählen Sie dann aus. `Enter` |  
| Nicht-bearbeitbaren HTML-Quellcode in neuer Registerkarte anzeigen | `Ctrl`+`U` | n.a. |  

> [!NOTE]
> Wenn Sie das Debugging durchgeführt und an einem Haltepunkt angehalten haben, wird die Laufzeit zuerst mit der Tastenkombination **Aktualisierung** fortgesetzt.  

## <a name="see-also"></a>Weitere Informationen  

*   [Entwicklungstools für Einsteiger: Erste Schritte mit HTML und dem DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Microsoft Edge (Chromium) DevTools Protocol][DevtoolsProtocolChromiumIndex]  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Wenn Sie eine Vorschau der [neusten Features für die Entwicklungstools anzeigen möchten][DevtoolsGuideChromiumWhatsNewIndex], laden Sie [Microsoft Edge Canary][MicrosoftedgeinsiderDownload] mit nächtlichen Builds herunter.  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "Entwicklungstools für Einsteiger: Erste Schritte mit HTML und dem DOM | Microsoft-Dokumentation"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools "Neuigkeiten in den Microsoft Edge (Chromium)- DevTools | Microsoft-Dokumentation"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Microsoft Edge (Chromium) Entwicklungstools-Protokoll | Microsoft-Dokumentation"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Microsoft Edge-Add-Ons"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Erweiterungen | Chrome Web Store"  
