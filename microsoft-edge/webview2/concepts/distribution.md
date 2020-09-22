---
description: Verteilungsoptionen beim Freigeben einer APP mit Microsoft Edge WebView2
title: Verteilung von Microsoft Edge WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 7db610ff1133b1b5b380372422f1f2f10981e583
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "11052186"
---
# Verteilung von Anwendungen mithilfe von WebView2  

Stellen Sie beim Verteilen Ihrer WebView2-Anwendung sicher, dass die Backing-Webplattform-die [WebView2-Runtime](#understanding-the-webview2-runtime) vorhanden ist, bevor die APP gestartet wird.  In diesem Artikel wird beschrieben, wie Entwickler die WebView2-Laufzeit installieren können, und wie Sie die beiden Verteilungs Modi für Ihre WebView2-Anwendung verwenden:  [Evergreen](#evergreen-distribution-mode) und [Feste Version](#fixed-version-distribution-mode).  

## Immergrüner Verteilungsmodus  

> [!NOTE]
> Der immergrüne Verteilungsmodus wird für die meisten Entwickler empfohlen.  

Der immergrüne Verteilungsmodus sorgt dafür, dass Ihre APP die neuesten Funktionen und Sicherheitsupdates nutzt.  Sie weist die folgenden Merkmale auf:  

*   Die zugrunde liegende Web-Plattform \ (WebView2 Runtime \) wird automatisch ohne zusätzlichen Aufwand von Entwicklern aktualisiert.  
*   Alle Anwendungen, die den immergrünen Verteilungsmodus verwenden, verwenden eine freigegebene Kopie der immergrünen WebView2-Laufzeit, wodurch Speicherplatz gespart wird.  

### Grundlegendes zur WebView2-Laufzeit  

Die WebView2-Laufzeit ist eine erneut verteilbare Laufzeit und dient als unterstützte Webplattform für WebView2-Anwendungen.  Dieses Konzept ähnelt der VC + + oder .NET Runtime für C++-/.net-apps.  Unter der Haube werden die Common Language Runtime Microsoft Edge \ (Chromium \)-Binärdateien geändert, die fein abgestimmt und für Anwendungen getestet wurden.  Die Common Language Runtime wird bei der Installation nicht als Benutzersicht barer Browser angezeigt, beispielsweise haben Benutzer keinen Browser-Desktop-Verknüpfung oder Menüeintrag im Startmenü.  

Für die Entwicklung und das Testen können Entwickler die Laufzeit oder einen beliebigen, nicht stabilen Microsoft Edge \ (Chromium \)-Browser Kanal für die Sicherungs-Webplattform verwenden.  In Produktionsumgebungen müssen Entwickler sicherstellen, dass die Laufzeit auf Benutzergeräten vorhanden ist, bevor die Anwendung gestartet wird.  Der Microsoft Edge stable-Kanal steht für die WebView2-Verwendung nicht zur Verfügung, um zu verhindern, dass apps eine Abhängigkeit vom Browser in der Produktion übernehmen.  

Entwickler dürfen keine Abhängigkeit vom Browser übernehmen, weil:  

*   Microsoft Edge \ (Chrom \) ist auf allen Benutzergeräten nicht garantiert vorhanden.  Geräte, die nicht mit Windows Update verbunden sind oder nicht direkt von Microsoft verwaltet werden \ (ein großer Teil des Enterprise/edu-Marktes), haben möglicherweise nicht den Browser.  Das zulassen, dass Entwickler die WebView2-Laufzeit verteilen können, vermeidet eine Abhängigkeit vom Browser als Voraussetzung für apps.
*   In Browsern und apps gibt es unterschiedliche Anwendungsfälle, und daher kann es vorkommen, dass eine Abhängigkeit von einem Browser unbeabsichtigte Nebeneffekte für Ihre apps hat.  So können IT-Administratoren beispielsweise den Browser für die interne Website Kompatibilität steuern.  Mit der WebView2-Laufzeit können apps immergrün bleiben, während Browser Updates aktiv verwaltet werden.  
*   Im Gegensatz zum Browser wird die Common Language Runtime für Anwendungsszenarien entwickelt und getestet und kann in einigen Fällen Fehlerkorrekturen beinhalten, die im Browser noch nicht verfügbar sind.  

Die Evergreen WebView2-Laufzeit ist für den Versand von Posteingang in zukünftigen Versionen von Windows vorgesehen.  Bevor die Laufzeit universeller verfügbar wird, wird Entwicklern empfohlen, die Laufzeit zusammen mit der Produktionsanwendung bereitzustellen.  

### Bereitstellen der immergrünen WebView2-Laufzeit  

Für alle Evergreen-apps auf dem Gerät ist nur eine Installation der Evergreen WebView2-Laufzeit erforderlich.  Auf der [Download Seite der WebView2-Runtime][Webview2Installer] stehen eine Reihe von Tools zur Verfügung, mit denen Entwickler die Evergreen-Laufzeit bereitstellen können, beispielsweise:  

*   WebView2-Runtime-Bootstrapper \ (in Kürze freigegeben werden \) ist ein kleines \ (ca. 2 MB \)-Installationsprogramm.  Dieses Installationsprogramm lädt die Evergreen-Laufzeit von Microsoft-Servern herunter und installiert Sie, die der Gerätearchitektur des Benutzers entspricht.  
*   Link zum Herunterladen des Bootstrappers \ (in Kürze verfügbar) ist ein Link für Entwickler, um den Bootstrapper programmgesteuert herunterzuladen.
*   Das Standalone-Installationsprogramm von WebView2 Runtime ist ein vollständiges Installationsprogramm, das die immergrüne WebView2-Runtime in Offlineumgebungen installieren kann.  

Derzeit unterstützen sowohl der Bootstrapper als auch das Standalone-Installationsprogramm nur die Installation pro Computer, für die eine Anhebung erforderlich ist.  Wenn Sie ohne Elevation ausführen, wird eine Aufforderung zur Windows-Benutzerkontensteuerung angezeigt, um Benutzer zu bitten, Berechtigungen zu erhöhen.  

Wir empfehlen die folgenden Workflows, um sicherzustellen, dass die Laufzeit bereits installiert ist, bevor die Anwendung gestartet wird.  Sie können Ihren Workflow je nach Szenario anpassen.  Wir werden auch in Zukunft Beispielcode bereitstellen.  

#### Nur Online Bereitstellung  

Führen Sie die folgenden Schritte aus, wenn Sie über ein Szenario für die Onlinebereitstellung verfügen, in dem Endbenutzer davon ausgegangen werden, dass Sie über einen Internetzugriff verfügen:  

*   Überprüfen Sie während der Anwendungseinrichtung, ob die Laufzeit bereits installiert ist, indem Sie eine der folgenden Aktionen ausführen:  
    *   Überprüfen, ob `pv (REG_SZ)` unter der Registrierungsschlüssel vorhanden ist `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}` , oder  
    *   Rufen Sie die WebView2-API- [GetAvailableCoreWebView2BrowserVersionString](../reference/win32/0-9-622/webview2-idl.md#getavailablecorewebview2browserversionstring) auf, und überprüfen Sie, ob VERSIONINFO NULL ist.  
*   Wenn die Common Language Runtime nicht installiert ist, verwenden Sie den Link zum programmgesteuerten Download des Bootstrappers.  
*   Rufen Sie den Bootstrapper über einen erhöhten Prozess oder eine Eingabeaufforderung mit `MicrosoftEdgeWebview2Setup.exe /silent /install` für die unbeaufsichtigte Installation auf.  

Dieser Workflow stellt sicher, dass Sie die Laufzeit nur dann installieren, wenn Sie benötigt wird, dass Sie keine Installationsprogramme Verpacken oder die Architektur von Benutzergeräten nicht ermitteln müssen, und die Laufzeit im Hintergrund installieren können.  Sie können den Bootstrapper auch mit Ihrer Anwendung Verpacken, anstatt ihn bei Bedarf programmgesteuert herunterzuladen.  

#### Offline Bereitstellung  

Wenn Sie über ein Offline Bereitstellungsszenario verfügen, in dem die APP-Bereitstellung vollständig Offline funktionieren muss, führen Sie die folgenden Schritte aus:  

*   Laden Sie das [Standalone-Installationsprogramm][Webview2Installer]herunter.  
*   Fügen Sie das Installationsprogramm in ihr Anwendungs Installationsprogramm oder Updater ein.  
*   Überprüfen Sie während der Anwendungseinrichtung, ob die Laufzeit bereits installiert ist, indem Sie eine der folgenden Aktionen ausführen:  
    *   Überprüfen, ob `pv (REG_SZ)` unter der Registrierungsschlüssel vorhanden ist `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}` , oder  
    *   Rufen Sie die WebView2-API- [GetAvailableCoreWebView2BrowserVersionString](../reference/win32/0-9-622/webview2-idl.md#getavailablecorewebview2browserversionstring) auf, und überprüfen Sie, ob VERSIONINFO NULL ist.  
*   Wenn die Common Language Runtime nicht installiert ist, rufen Sie das eigenständige Installationsprogramm von einem erhöhten Prozess oder einer Eingabeaufforderung mit `MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install` für die unbeaufsichtigte Installation auf.  

## Modus für feste Versions Verteilung  

> [!NOTE]
> Der Verteilungsmodus für feste Versionen steht noch nicht zur Verfügung.  

Für abhängige Umgebungen sind Pläne zur Unterstützung einer festen Version vorgesehen, die zuvor den Distributions Modus "Bring-eigene" genannt hat.  Der Modus für die feste Versions Verteilung ermöglicht Entwicklern das auswählen und Verpacken einer bestimmten Version der WebView2-Laufzeit.  Mit dem Modus für die feste Versions Verteilung können Sie steuern, welche Version der WebView2-Laufzeit von Ihrer Anwendung verwendet wird und wann Benutzer Computer aktualisiert werden.  Der Modus für die feste Versions Verteilung erhält keine automatischen Updates, und Entwickler sollten selbst Updates anwenden.  


<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Grundlegendes zu Browserversionen und WebView2 | Microsoft docs"  
[ReferenceWin3209622WebviewIdl]: ../reference/win32/0-9-622/webview2-idl.md  "Globals | Microsoft docs"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-Installationsprogramm"  
