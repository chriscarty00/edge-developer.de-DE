---
description: Verteilungsoptionen beim Freigeben einer APP mit Microsoft Edge WebView2
title: Verteilung der Microsoft Edge WebView2-Anwendung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 370b5da2d42412a08a5c7f8a7401496fa70e3065
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844404"
---
# Verteilung von Anwendungen mithilfe von WebView2  

Das WebView2-Steuerelement verwendet die Microsoft Edge \ (Chromium \)-Plattform.  Wenn Sie Ihre APP Verpacken und verteilen, stellen Sie sicher, dass eine Kopie der Plattform oder der WebView2-Laufzeit vorhanden ist, bevor die APP gestartet wird.  Auf der folgenden Seite wird beschrieben, wie Sie \ (der Entwickler \) sicherstellen können, dass die WebView2-Laufzeit installiert ist, und die beiden Verteilungs Modi für Ihre WebView2-Anwendung verwenden: [Evergreen](#evergreen-distribution-mode) und [Feste Version](#fixed-version-distribution-mode).  

## Immergrüner Verteilungsmodus  

Der immergrüne Verteilungsmodus sorgt dafür, dass Ihre APP die neuesten Funktionen und Sicherheitsupdates nutzt.  Der immergrüne Verteilungsmodus weist die folgenden Merkmale auf:  

*   Die Web-Plattform wird automatisch ohne zusätzlichen Aufwand von Ihnen aktualisiert.  
*   Alle Anwendungen, die den immergrünen Verteilungsmodus nutzen, verwenden eine freigegebene Kopie der Platt Form Binärdateien, wodurch Speicherplatz gespart wird.  

Es gibt mehrere Kanäle, WebView2 die Anwendungen als Web-Plattform verwenden können.  Standardmäßig zielt WebView2 auf den stabilsten auf dem Gerät verfügbaren Kanal, der die Mindestanforderungen für die Version des WebView2-SDK erfüllt.  Die folgenden Kanäle sind in der Reihenfolge von Most zu least stable-Kanal aufgelistet.  

1.  WebView2-Laufzeit \ (Vorschau \)  
1.  Microsoft Edge Beta Channel  
1.  Microsoft Edge Dev Channel  
1.  Microsoft Edge Canary Channel    

> [!NOTE]
> Das Evergreen-Verteilungsmodell wird für die meisten Entwickler empfohlen.  

> [!IMPORTANT]
> Microsoft Edge stable-Kanal ist kein gültiges Ziel für WebView2, und die Gründe werden später beschrieben.  

Weitere Informationen zur Versionsverwaltung finden Sie unter [Versionsverwaltung][ConceptsVersioning] und [Globals][ReferenceWin3209538WebviewIdl].  

### Grundlegendes zur WebView2-Laufzeit und zum Installationsprogramm (Preview)  

Microsoft Edge stable-Kanal ist auf allen Benutzercomputern, auf denen die Anwendung ausgeführt wird, möglicherweise nicht installiert.  Anstatt zu verlangen, dass Benutzer Microsoft Edge installieren, verwendet Ihre Anwendung möglicherweise die Evergreen-WebView2-Laufzeit und das Installationsprogramm \ (Preview \).  Die WebView2-Laufzeit ist eine angepasste Kopie der Microsoft Edge-Binärdateien, mit denen Ihre WebView2-Anwendungen ausgeführt werden.  Wenn die WebView2-Laufzeit installiert ist, können Benutzer Sie nicht als normalen Browser verwenden.  Beispielsweise gibt es keine Desktopverknüpfung, Startmenüeintrag, Benutzer können ein Browserfenster nicht unter Verwendung der Runtime-Binärdateien öffnen usw.  Alle Evergreen-WebView2-Anwendungen auf dem Gerät verwenden möglicherweise eine einzelne immergrüne WebView2-Laufzeitinstallation.  

Während der Vorschau werden die Evergreen-WebView2-Laufzeit und der Microsoft Edge dev-Kanal zur gleichen Zeit aktualisiert und verfügen über denselben Build.  Während der Vorschau plant das WebView2-Team in Zukunft, die WebView2-Laufzeit zu aktualisieren und dem gleichen Build wie dem Microsoft Edge-Beta Kanal zu entsprechen.  Wenn WebView2 in Zukunft die allgemeine Verfügbarkeit erreicht \ (GA \), plant das WebView2-Team, die WebView2-Laufzeit zu aktualisieren und dem gleichen Build wie dem Microsoft Edge stable-Kanal zu entsprechen.  Nach GA sollten Anwendungen die WebView2-Laufzeit in Production verwenden.  

> [!IMPORTANT]
> Senden Sie während der Vorschau keine WebView2-Anwendungen in der Produktion.  

Verwenden Sie den folgenden Workflow, um sicherzustellen, dass die Evergreen WebView2-Laufzeit verfügbar ist.  

1.  Laden Sie das neueste [Evergreen WebView2 Runtime-Installationsprogramm][Webview2Installer]herunter.  
1.  Fügen Sie das Installationsprogramm in ihr Anwendungs Installationsprogramm oder Updater ein.  
1.  Überprüfen Sie während der Anwendungsinstallation oder-Aktualisierung, ob die Evergreen WebView2-Laufzeit bereits auf dem Benutzer Computer installiert ist.  Wenn dies nicht der Fall ist, ruft die Anwendung das Installationsprogramm auf, um die Laufzeit zu installieren.  

Je nach Szenario müssen Sie möglicherweise den oben genannten Workflow ändern.  Beispielsweise kann ihr Anwendungs Installationsprogramm das Evergreen-WebView2-Runtime-Installationsprogramm herunterladen, anstatt es in Ihr Anwendungspaket einzubinden.  

> [!NOTE]
> Sowohl das WebView2-Runtime-als auch das WebView2-Runtime-Installationsprogramm befinden sich in Preview.  Die Vorschau hat einen beschränkten anfänglichen Umfang und ist nur als eigenständige Installation pro Computer unter Windows 10 auf x64 verfügbar.  In Zukunft ist die Unterstützung für Windows 7, x86 und ARM64 geplant.  

### Bewährte Methoden für die Verwendung von WebView2-Runtime und nicht stabilen Microsoft Edge-Kanälen  

Betrachten Sie die folgenden Empfehlungen während der Vorschau.  

*   Stellen Sie sicher, dass Sie die [Evergreen WebView2-Laufzeit und das Installationsprogramm][Webview2Installer] verwenden, um ihre Verpackungs-und Verteilungs Pipeline zu entwickeln oder zu testen.  In Zukunft sollte Ihre Produktionsanwendung das Installationsprogramm beinhalten.  
*   Für die Entwicklung ihrer Anwendung können Sie die Evergreen WebView2-Laufzeit verwenden.  Da sich die Laufzeit jedoch vom dev-Kanal zum Beta Kanal oder zum stabilen Kanal verlagert, entspricht die Buildnummer des Laufzeitmoduls möglicherweise nicht den neuesten Versionsanforderungen für das neueste Preview WebView2 SDK.  Wenn Sie das neueste SDK verwenden möchten, installieren Sie den Canary-Kanal von Microsoft Edge, um sicherzustellen, dass ein kompatibler Build auf dem Gerät verfügbar ist.  Weitere Informationen zur Versionsverwaltung finden Sie unter [Versionsverwaltung][ConceptsVersioning].  
*   Wenn Sie Ihre Webinhalte auf Kompatibilität mit Änderungen an der Plattform testen möchten, die nicht im stable-Kanal verfügbar sind, verwenden Sie den entsprechenden nicht stabilen Kanal nach Bedarf.  

## Modus für feste Versions Verteilung  

> [!NOTE]
> Das Modell für die feste Versions Verteilung steht zurzeit nicht zur Verfügung.  

Für abhängige Umgebungen gibt es Pläne zur Unterstützung einer festen Version \ (zuvor als "Bring-your-own \" bezeichnet)-Verteilungsmodus.  Mit dem Modus für die feste Versions Verteilung können Sie eine bestimmte Version der WebView2-Laufzeit auswählen und Verpacken.  Mit dem Modus für die feste Versions Verteilung können Sie steuern, welche Version der WebView2-Laufzeit von Ihrer Anwendung verwendet wird und wann Benutzer Computer aktualisiert werden.  Der Modus für die feste Versions Verteilung erhält keine automatischen Updates, und Sie sollten planen, Updates manuell anzuwenden.  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Grundlegendes zu Browserversionen und WebView2 | Microsoft docs"  
[ReferenceWin3209538WebviewIdl]: ../reference/win32/0-9-538/webview2-idl.md  "Globals | Microsoft docs"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-Installationsprogramm"  
