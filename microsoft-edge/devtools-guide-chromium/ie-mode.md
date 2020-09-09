---
description: IE-Modus und Microsoft Edge (Chrom) devtools
title: Internet Explorer-Modus und DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, ie11, Internet Explorer 11, IE-Modus
ms.openlocfilehash: b059cae3ff48a45fe92cbf69e37ad692e329b200
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003967"
---
# Internet Explorer-Modus und DevTools  

In diesem Artikel wird beschrieben, wie der Internet Explorer-Modus \ (IE-Modus \) in den Microsoft Edge \ (Chromium \) devtools integriert ist.  

## Grundlegendes zum IE-Modus  

Mit dem IE-Modus können Unternehmen eine Liste der Websites angeben, die nur in Internet Explorer 11 funktionieren.  Wenn Sie zu diesen Websites in Microsoft Edge (Chrom \) navigieren, wird eine Instanz von Internet Explorer 11 ausgeführt, und die Website wird auf einer Registerkarte gerendert.  Mit dieser Funktion können Unternehmen die Kompatibilität mit Technologien verwalten, die derzeit nicht mit modernen Webbrowsern kompatibel sind.  Unterstützung für die folgenden Technologien ist im IE-Modus enthalten.  

*   IE-Dokumentmodi  
*   ActiveX-Steuerelemente  
*   andere Legacykomponenten  

Im IE-Modus basiert der Renderingprozess auf Internet Explorer 11.  Der Microsoft Edge-Prozess-Manager (Chrom) verarbeitet die Lebensdauer des Rendering-Prozesses.  Sie ist auf die Lebensdauer der Registerkarte für eine bestimmte Website beschränkt \ (oder App \).  Wenn eine Registerkarte im IE-Modus gerendert wird, wird in der Adressleiste für die jeweilige Registerkarte ein Badge angezeigt.  

:::image type="complex" source="./media/ie-mode-badge.msft.png" alt-text="IE-Modus-Abzeichen in der Adressleiste" lightbox="./media/ie-mode-badge.msft.png":::
   IE-Modus-Abzeichen in der Adressleiste  
:::image-end:::  

Der IE-Modus ist derzeit unter Windows 10, Version 1903, verfügbar (Mai 2019-Update \), wird aber in Kürze für alle unterstützten Windows-Plattformen bereitgestellt.  

## Starten des devtools auf einer Registerkarte im IE-Modus  

Wenn Sie versuchen, den Dokumentmodus einer Website im IE-Modus anzuzeigen, wählen Sie das Abzeichen in der Adressleiste aus.  

:::image type="complex" source="./media/ie-mode-badge-doc-mode.msft.png" alt-text="Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badges" lightbox="./media/ie-mode-badge-doc-mode.msft.png":::
   Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badges  
:::image-end:::  

Wenn eine Registerkarte den IE-Modus verwendet, funktionieren die devtools nicht, und die folgenden Bedingungen treten auf.

*   Wenn Sie auswählen `F12` oder auswählen `Ctrl` + `Shift` + `I` , wird eine leere Instanz des Microsoft Edge \ (Chrom \) devtools gestartet, und die folgende Meldung wird angezeigt.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Wenn Sie ein Kontextmenü öffnen (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Quelle anzeigen**aus, wird der Editor gestartet.  
*   Wenn Sie ein Kontextmenü öffnen \ (mit der rechten Maustaste auf \), wird das **Inspect-Element** nicht angezeigt.  

Der Grund dafür, dass eine Reihe von Tools innerhalb des devtools \ (wie **Netzwerk** -und **Leistungs** Tools \) nicht funktioniert, ist die Rendering-Engine, die im IE-Modus von Chrom zu Internet Explorer 11 wechselt.  Wenn Sie Feedback bereitstellen möchten, navigieren Sie zum [Kontakt mit dem Microsoft Edge devtools-Team](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

:::image type="complex" source="./media/ie-mode-devtools.msft.png" alt-text="DevTools im IE-Modus gestartet" lightbox="./media/ie-mode-devtools.msft.png":::
   DevTools im IE-Modus gestartet  
:::image-end:::  

Führen Sie die folgenden Schritte aus, um Ihre Internet Explorer 11-basierte Website \ (oder App \) in Internet Explorer 11 und dem IE-Modus zu testen.  

1.  Öffnen Sie Internet Explorer 11.  
    *   Suchen Sie unter Windows 10 die Verknüpfung für Internet Explorer 11.
        1.  **Startmenü**  >  **Windows-Zubehör**  >  **Internet Explorer 11**.  
    *   Suchen Sie unter Windows 7 nach Internet Explorer 11.
        1.  **Startmenü**  >  **Internet Explorer 11**.  
1.  Öffnen Sie in Internet Explorer 11 dieselbe Webseite.  
1.  Starten Sie die Internet Explorer-devtools.  
    *   Wählen Sie aus `F12` .  
    *   Zeigen Sie auf eine beliebige Stelle, öffnen Sie ein Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Element prüfen**aus.  Weitere Informationen zur Verwendung dieser Tools finden Sie unter [Verwenden der F12-Entwicklertools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].  

## Remote Debuggen und IE-Modus  

Starten Sie Microsoft Edge \ (Chromium \) mit aktiviertem Remotedebuggen über die Befehlszeilenschnittstelle.  Visual Studio, Visual Studio-Code und andere Entwicklungstools führen in der Regel einen Befehl aus, um Microsoft Edge zu starten.  Mit dem folgenden Befehl wird Microsoft Edge gestartet, wobei der Remote Debugging-Port auf eingestellt ist `9222` .  

```shell
start msedge --remote-debugging-port=9222
```  

Nachdem Sie Microsoft Edge \ (Chrom \) mithilfe eines Befehlszeilenarguments gestartet haben, ist der IE-Modus nicht verfügbar.  Sie können weiterhin zu Websites \ (oder apps \) navigieren, die andernfalls im IE-Modus angezeigt werden. Der Inhalt der Website \ (oder App \) wird mit Chrom und nicht mit Internet Explorer 11 gerendert.  Es wird davon ausgegangen, dass die Teile der Seiten, die auf IE11 basieren, wie ActiveX-Steuerelemente, nicht richtig gerendert werden.  Das IE-Modus-Abzeichen wird in der Adressleiste nicht angezeigt.  

Der IE-Modus bleibt erst verfügbar, wenn Sie Microsoft Edge (Chrom) vollständig schließen und neu starten.  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Verwenden der F12-Entwicklertools | Microsoft docs"  