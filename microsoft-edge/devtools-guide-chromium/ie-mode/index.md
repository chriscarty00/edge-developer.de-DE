---
description: IE-Modus und Microsoft Edge (Chromium) DevTools
title: Internet Explorer-Modus und devTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, ie11, internet explorer 11, ie mode
ms.openlocfilehash: e65869cd88b449dcde0aec25c77df27f99b78f8d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398602"
---
# <a name="internet-explorer-mode-and-the-devtools"></a>Internet Explorer-Modus und devTools  

In diesem Artikel wird beschrieben, wie der Internet Explorer-Modus \(IE-Modus\) in microsoft Edge \(Chromium\) DevTools integriert wird.  

## <a name="understanding-ie-mode"></a>Grundlegendes zum IE-Modus  

Im IE-Modus können Unternehmen eine Liste der Websites angeben, die nur in Internet Explorer 11 funktionieren.  Wenn Sie zu diesen Websites in Microsoft Edge \(Chromium\) navigieren, wird eine Instanz von Internet Explorer 11 ausgeführt und die Website auf einer Registerkarte gerendert.  Mit der Funktionalität können Unternehmen die Kompatibilität mit Technologien verwalten, die derzeit nicht mit modernen Webbrowsern kompatibel sind.  Unterstützung für die folgenden Technologien ist im IE-Modus enthalten.  

*   IE-Dokumentmodi  
*   ActiveX-Steuerelemente  
*   andere Legacykomponenten  

Im IE-Modus basiert der Rendervorgang auf Internet Explorer 11.  Der Microsoft Edge \(Chromium\)-Prozess-Manager übernimmt die Lebensdauer des Renderingprozesses.  Sie ist auf die Lebensdauer der Registerkarte für eine bestimmte Website \(oder App\) beschränkt.  Wenn eine Registerkarte im IE-Modus gerendert wird, wird in der Adressleiste für die spezifische Registerkarte ein Signal angezeigt.  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="IE-Modus-Signal in der Adressleiste" lightbox="../media/ie-mode-badge.msft.png":::
   IE-Modus-Signal in der Adressleiste  
:::image-end:::  

Der IE-Modus ist derzeit unter Windows 10 Version 1903 \(Mai 2019 Update\) verfügbar, wird aber bald für alle unterstützten Windows-Plattformen verfügbar sein.  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a>Starten der DevTools auf einer Registerkarte im IE-Modus  

Wenn Sie versuchen, den Dokumentmodus einer Website im IE-Modus zu sehen, wählen Sie das Signal in der Adressleiste aus.  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badges" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badges  
:::image-end:::  

Wenn eine Registerkarte den IE-Modus verwendet, funktionieren die DevTools nicht, und die folgenden Bedingungen treten auf.

*   Wenn Sie auswählen oder auswählen, wird die folgende Meldung angezeigt, wenn eine leere Instanz von `F12` `Ctrl` + `Shift` + `I` Microsoft Edge \(Chromium\) DevTools gestartet wird.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Wenn Sie ein kontextbezogenes Menü \(rechtsklicken\) öffnen und Quelle **anzeigen**auswählen, wird Editor gestartet.  
*   Wenn Sie ein kontextbezogenes Menü \(mit der rechten Maustaste klicken\) öffnen, ist das **Inspect-Element** nicht sichtbar.  

Der Grund, warum eine Reihe der Tools innerhalb **** der **** DevTools \(wie die Netzwerk- und Leistungstools\) nicht funktioniert, ist der Wechsel des Renderingmoduls von Chromium zu Internet Explorer 11 im IE-Modus.  Um Feedback zu geben, navigieren Sie zu Kontakt mit dem [Microsoft Edge DevTools-Team](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools im IE-Modus gestartet" lightbox="../media/ie-mode-devtools.msft.png":::
   DevTools im IE-Modus gestartet  
:::image-end:::  

Führen Sie die folgenden Schritte aus, um Ihre Internet Explorer 11-basierte Website \(oder App\) im Internet Explorer 11- und IE-Modus zu testen.  

1.  Öffnen Sie Internet Explorer 11.  
    *   Suchen Sie unter Windows 10 nach der Verknüpfung für Internet Explorer 11.
        1.  **Startmenü**  >  **Windows-Zubehör**  >  **Internet Explorer 11**.  
    *   Suchen Sie unter Windows 7 nach Internet Explorer 11.
        1.  **Startmenü**  >  **Internet Explorer 11**.  
1.  Öffnen Sie in Internet Explorer 11 dieselbe Webseite.  
1.  Starten Sie Internet Explorer DevTools.  
    *   Wählen Sie `F12` aus.  
    *   Zeigen Sie auf eine beliebige Stelle, öffnen Sie ein kontextbezogenes Menü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Inspect-Element aus.**  Weitere Informationen zur Verwendung dieser Tools finden Sie unter [Verwenden der F12-Entwicklertools.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]  

## <a name="remote-debugging-and-ie-mode"></a>Remotedebuding und IE-Modus  

Starten Sie Microsoft Edge \(Chromium\) mit aktiviertem Remotedebu debugging über die Befehlszeilenschnittstelle.  Microsoft Visual Studio, Microsoft Visual Studio Code und andere Entwicklungstools führen in der Regel einen Befehl aus, um Microsoft Edge zu starten.  Mit dem folgenden Befehl wird Microsoft Edge gestartet, und der Remotedebugport ist auf `9222` festgelegt.  

```shell
start msedge --remote-debugging-port=9222
```  

Nachdem Sie Microsoft Edge \(Chromium\) mithilfe eines Befehlszeilenarguments gestartet haben, ist der IE-Modus nicht verfügbar.  Sie können weiterhin zu Websites \(oder Apps\) navigieren, die andernfalls im IE-Modus angezeigt werden.  Der Inhalt der Website \(oder App\) wird mit Chromium gerendert, nicht mit Internet Explorer 11.  Erwarten Sie, dass die Teile der Webseiten, die auf IE11 beruhen, z. B. ActiveX Steuerelemente, nicht ordnungsgemäß gerendert werden.  Das IE-Modus-Signal wird nicht in der Adressleiste angezeigt.  

Der IE-Modus ist erst verfügbar, wenn Sie Microsoft Edge \(Chromium\) vollständig schließen und neu starten.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Verwenden der F12-Entwicklertools | Microsoft Docs"  
