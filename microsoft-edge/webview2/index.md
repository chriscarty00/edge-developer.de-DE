---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Microsoft Edge-WebView2-Steuerelement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML, Windows Forms, WinForms, WPF, .net
ms.openlocfilehash: 1b140d9f644c7a864cac4966bb4cfdd400feeb0d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697742"
---
# Einführung in Microsoft Edge WebView2 (Preview)  

Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webtechnologien (HTML, CSS und JavaScript \) in ihre systemeigenen Anwendungen einbetten.  Das WebView2-Steuerelement verwendet [Microsoft Edge (Chrom)](https://www.microsoftedgeinsider.com) als Rendering-Modul, um die Webinhalte in systemeigenen Anwendungen anzuzeigen.  Mit WebView2 können Sie Webcode in verschiedenen Teilen der systemeigenen Anwendung einbetten oder die gesamte systemeigene Anwendung in einem einzigen WebView-Webpart erstellen.  Informationen zum Erstellen einer WebView2-Anwendung finden Sie unter [Erste Schritte](./index.md#getting-started).  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Was ist WebView":::
   Was ist WebView  
:::image-end:::  

> [!NOTE]
> Die WebView2 Preview ist für frühzeitiges Prototyping vorgesehen, um Feedback zu sammeln, um die API zu gestalten.  Das Microsoft Edge-WebView-Team rät davon ab, die Vorschau in ihren Produktions-apps zu verwenden, da möglicherweise [wichtige Änderungen](./releasenotes.md)auftreten.  

## Ansatz der Hybrid Anwendung  

Entwickler müssen häufig zwischen dem Erstellen einer Webanwendung oder einer systemeigenen Anwendung auswählen.  Die Entscheidung hängt vom Kompromiss zwischen Reichweite und macht ab.  Web-Anwendungen ermöglichen eine breite Reichweite.  Als Web-Entwickler können Sie die meisten, wenn nicht alle Ihren Code, auf allen verschiedenen Plattformen wieder verwenden.  Systemeigene Anwendungen nutzen jedoch die Funktionen der gesamten systemeigenen Plattform.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native":::
   Web Native  
:::image-end:::  

Hybrid Anwendungen ermöglichen Entwicklern, das Beste aus beiden Welten zu genießen.  Entwickler von Hybrid Anwendungen profitieren von der Allgegenwart und Stärke der Web-Plattform sowie von der Leistungsfähigkeit und den vollständigen Funktionen der systemeigenen Plattform.  

## WebView2-Vorteile   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="WebView-Gründe":::
   WebView-Gründe  
:::image-end:::  

:::row:::
   :::column span="1":::
      **Web-Ökosystem \ & skillset**  
      Verwenden Sie die gesamte Web-Plattform, Bibliotheken, Tools und Talente, die im Web-Ökosystem vorhanden sind.  
   :::column-end:::
   :::column span="1":::
      **Schnelle Innovation**  
      Web-Entwicklung ermöglicht schnellere Bereitstellung und Iteration.  
   :::column-end:::
   :::column span="1":::
      **Windows 7, 8, 10 Support**  
      Unterstützung für eine konsistente Benutzeroberfläche in Windows 7, 8 und 10.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Systemeigene Funktionen**  
      Greifen Sie auf den vollständigen Satz nativer APIs zu.  
   :::column-end:::
   :::column span="1":::
      **Code Freigabe**  
      Durch Hinzufügen von Webcode zu ihrer CodeBase können Sie die Wiederverwendung auf mehreren Plattformen erhöhen.  
   :::column-end:::
   :::column span="1":::
      **Microsoft-Support**  
      Microsoft bietet Support und fügt neue Funktionsanforderungen hinzu, wenn WebView2 als "ga" veröffentlicht wird.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Immergrüne Verteilung**  
      Verlassen Sie sich auf eine aktuelle Version von Chromium mit regulären Plattformupdates und Sicherheitspatches.  
   :::column-end:::
   :::column span="1":::
      **Behoben** \ (in Kürze verfügbar)  
      Wählen Sie aus, um die Chrom Bits in Ihrer Anwendung zu verpacken.  
   :::column-end:::
   :::column span="1":::
      **Inkrementelle Einführung**  
      Fügen Sie Ihrer Anwendung Stück für Stück Webkomponenten hinzu.  
   :::column-end:::
:::row-end:::

## Erste Schritte  

Wenn Sie Ihre Anwendung mithilfe des WebView2-Steuerelements erstellen und testen möchten, müssen Sie sowohl [Microsoft Edge (Chrom)](https://www.microsoftedgeinsider.com/download) als auch das [WebView2-SDK](https://aka.ms/webviewnuget) installiert haben.  Wählen Sie eine der folgenden Optionen aus, um loszulegen.  

*   [Erste Schritte mit Win32 C/C++](./gettingstarted/win32.md)  
*   [Erste Schritte mit WPF](./gettingstarted/wpf.md)  
*   [Erste Schritte mit WinForms](./gettingstarted/winforms.md)  

Das [WebView2-Beispiel](https://github.com/MicrosoftEdge/WebView2Samples) -Repository enthält Beispiele, die alle WebView2-SDKs-Features und API-Verwendungsmuster veranschaulichen. Wenn dem WebView2-SDK weitere Features hinzugefügt werden, werden die Beispielanwendungen aktualisiert.   

## Unterstützte Plattformen  

Eine Entwicklervorschau steht in den folgenden Programmierumgebungen zur Verfügung.  

*   Win32 C/C++  
*   .NET Framework 4.6.2 oder höher  
*   .Net Core 3,0 oder höher  
*   [WinUI 3,0](/uwp/toolkits/winui3/)  

Sie können WebView2-Anwendungen unter den folgenden Windows-Versionen ausführen.  

*   Windows 10  
*   Windows8.1  
*   Windows 8  
*   Windows 7  
*   Windows Server 2016  
*   Windows Server 2012  
*   Windows Server-2012R2  
*   Windows Server 2008 R2  

## Nächste Schritte  

Ausführlichere Informationen zum Erstellen und Bereitstellen von WebView2-Anwendungen finden Sie in den konzeptionellen Dokumentationen und Anleitungen.  

#### Konzepte  

*   [WebView2 SDK und Microsoft Edge-Versionsverwaltung](./concepts/versioning.md)
*   [Verteilen von WebView2-Anwendungen](./concepts/distribution.md)  
 
#### Anleitungen  

*   [Debuggen von WebView2 mit devtools und Visual Studio-Skriptdebugging](./howto/debug.md)  
*   [Automatisieren und Debuggen von WebView2 mit Microsoft EdgeDriver](./howto/webdriver.md)  

<!--todo: add how-tos when available  -->  

## Kontakt mit dem WebView2-Team  

Helfen Sie beim Aufbau einer reicheren WebView2-Erfahrung, indem Sie Ihr Feedback freigeben.  Besuchen Sie das WebView [Feedback Repo](https://aka.ms/webviewfeedback) , um Funktionsanforderungen oder Fehlerberichte zu übermitteln.  Es ist auch ein guter Ort, um nach bekannten Problemen zu suchen.  

> [!NOTE]
> Während der Entwicklervorschau sammelt das Microsoft Edge-WebView-Team auch Daten, die zum Erstellen einer besseren WebView beitragen.  Benutzer können WebView-Datensammlung deaktivieren, indem Sie `edge://settings/privacy` im Microsoft Edge-Browser navigieren und die Browserdaten Sammlung deaktivieren.  
