---
description: Eine Referenz für WebDriver-Funktionen und Microsoft Edge-spezifische Optionen, die von EdgeDriver (Chrom) unterstützt werden.
title: Funktionen und edgeoptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, WebDriver, Selen, testen, Tools, Automatisierung, Test
ms.openlocfilehash: 1f6dca1b7ce3eb4fab3aaaab6450eee7cbf3eae5
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192249"
---
# Funktionen und edgeoptions  

Funktionen sind Optionen, die Sie zum Anpassen und Konfigurieren einer Sitzung verwenden können `EdgeDriver` .  Navigieren Sie zum Starten einer `EdgeDriver` Sitzung zu [Driving Microsoft Edge][DrivingEdgeWebDriverIndex].  In diesem Artikel werden alle unterstützten Funktionen für [Microsoft Edge][DownloadEdgeWebDriverIndex] und weitere Details zur Übergabe der Funktionen an eine `EdgeDriver` Sitzung dokumentiert.  

WebDriver-Sprachbindungen bieten Möglichkeiten zum Übergeben von Funktionen an `EdgeDriver` .  Der genaue Mechanismus hängt von der von [Ihnen ausgewählten Sprachen Bindung][ChooseLanguageBindingWebDriverIndex]ab.  In [Selen][SeleniumMain]werden Funktionen über die Klasse bereitgestellt `EdgeOptions` .  

## Verwenden der edgeoptions-Klasse  

Erstellen Sie eine Instanz von `EdgeOptions` , die über bequeme Methoden zum Festlegen von Microsoft Edge-spezifischen Funktionen verfügt.  Nachdem Sie das Objekt konfiguriert haben `EdgeOptions` , übergeben Sie `EdgeOptions` den `EdgeDriver` Konstruktor.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Verwenden Sie die Methode für Funktionen, die noch keine geeignete Methode aufweisen `AddAdditionalCapability` .  Sie müssen den Namen der Funktion und den Typ des von ihr akzeptierten Werts kennen.  Navigieren Sie zu [edgeoptions-Objekt](#edgeoptions-object), um die vollständige Liste zu überprüfen.  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## Erkannte Funktionen  

Für Standardfunktionen, die `EdgeDriver` akzeptiert werden, navigieren Sie zu [Selenium-Dokumentation][SharedCapabilitiesSeleniumDocumentation] und dem W3C- [WebDriver-Standard][CapabilitiesW3cWebdriver].  In diesem Artikel werden nur die für Microsoft Edge spezifischen Funktionen aufgeführt.  

## Edgeoptions-Objekt  

Die meisten Microsoft Edge-spezifischen Funktionen werden über das `EdgeOptions` Objekt verfügbar gemacht.  In einigen Sprachen werden die Funktionen von der Klasse implementiert `EdgeOptions` .  In anderen Sprachen werden die Funktionen unter dem `ms:edgeOptions` Wörterbuch in gespeichert `DesiredCapabilities` .  

| Funktion | Typ | Standardwert | Details |  
|:--- |:--- |:--- |:--- |  
| args | Liste der Zeichenfolgen |  | Liste der Befehlszeilenargumente, die beim Starten von Microsoft Edge zu verwenden sind.  Argumente mit einem zugeordneten Wert sollten durch ein `=` Zeichen (z. b `['start-maximized', 'user-data-dir=/tmp/temp_profile']` . \) getrennt werden.  |  
| Binär | string |  | Pfad zur Microsoft Edge-Binärdatei zur Verwendung von \ (unter macOS sollte der Pfad die eigentliche Binärdatei sein, nicht nur die app.  Beispiel: `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \).  |  
| Erweiterungen | Liste der Zeichenfolgen |  | Eine Liste der Erweiterungen, die beim Start installiert werden sollen.  Bei jedem Element in der Liste sollte es sich um eine Base64-codierte, komprimierte 64-Datei ( `.crx` \) handeln.  |  
| localState | dictionary |  | Ein Wörterbuch mit jedem Eintrag, bestehend aus dem Namen der Einstellung und seinem Wert.  Die Einstellungen werden auf die lokale Statusdatei im Ordner Benutzerdaten angewendet.  |  
| Einstellungen | dictionary |  | Ein Wörterbuch mit jedem Eintrag, bestehend aus dem Namen der Einstellung und seinem Wert.  Die Einstellungen werden nur auf das Benutzerprofil angewendet, das verwendet wird.  Beispiele: Navigieren Sie zu der `Preferences` Datei im Benutzerdatenverzeichnis von Microsoft Edge.  |  
| Trennen | boolesch | Falsch | Ist der Wert false, wird Microsoft Edge beendet `EdgeDriver` , wenn beendet wird, ob die Sitzung beendet wird oder nicht.  Ist "true", wird Microsoft Edge nur beendet, wenn die Sitzung beendet wird \ (oder geschlossen \).  **Hinweis**: Wenn "true" und die Sitzung nicht beendet wird, wird `EdgeDriver` das von der Microsoft Edge-Instanz verwendete temporäre Benutzerdatenverzeichnis nicht bereinigt.  |  
| debuggerAddress | string |  | Die Adresse eines Debugger-Servers, mit dem eine Verbindung hergestellt werden soll, beispielsweise in Form von <Hostname/IP: Port>  `127.0.0.1:38947` .  |
| excludeSwitches | Liste der Zeichenfolgen |  | Liste der Befehlszeilenoptionen von Microsoft Edge, um zu verhindern, dass EdgeDriver standardmäßig beim Starten von Microsoft Edge übergeben wird.  Keine Präfix Schalter mit `--` .  |  
| minidumpPath | string |  | Verzeichnis zum Speichern von Microsoft Edge-Mini Absichten.  \ (Wird nur unter Linux unterstützt. \) |  
| mobileEmulation | dictionary |  | Ein Wörterbuch mit einem Wert für `deviceName` oder Werte für `deviceMetrics` und `userAgent` .  |  
| perfLoggingPrefs | dictionary |  | Ein optionales Wörterbuch, das die Einstellungen für die Leistungsprotokollierung angibt.  Wenn Sie weitere Informationen wünschen, navigieren Sie zu [perfLoggingPrefs-Objekt](#perfloggingprefs-object).  |  
| windowTypes | Liste der Zeichenfolgen |  | Eine Liste der Fenstertypen, die in der Liste der Fensterhandles angezeigt werden.  Wenn Sie Zugriff auf Android-WebView-Elemente haben, fügen Sie Sie `webview` in die Liste ein.  |  
| wdpAddress | string |  | Eine Adresse eines Windows-Geräte Portal Servers, mit dem Sie eine Verbindung herstellen, beispielsweise in Form von `hostname/ip:port`  `127.0.0.1:50080` .  Wenn Sie weitere Informationen wünschen, navigieren Sie zu [Remote Debuggen – Windows 10-Geräte][DevtoolsRemoteDebuggingWindows].  |  
| wdpUsername | string |  | Optionaler Benutzername, der beim Herstellen einer Verbindung mit einem Windows-Geräte Portal Server verwendet wird.  Erforderlich, wenn auf dem Server die Authentifizierung aktiviert ist.  |  
| wdpPassword | string |  | Optionales Kennwort, das beim Herstellen einer Verbindung mit einem Windows-Geräte Portal Server verwendet werden soll.  Erforderlich, wenn auf dem Server die Authentifizierung aktiviert ist.  |  
| Anw. | string |  | Anwendungsbenutzer Modell-ID eines Microsoft Edge-App-Pakets zum Starten, beispielsweise `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` .  Verwenden Sie `windowsApp` anstelle der `binary` Verbindung zu einem Windows 10X-Gerät oder-Emulator mithilfe des Windows Device Portals.  |  

## perfLoggingPrefs-Objekt  

Das `perfLoggingPrefs` Wörterbuch weist das folgende Format auf \ (alle Schlüssel sind optional \).  

| Key | Typ | Standardwert | Details |  
|:--- |:--- |:--- |:--- |  
| enableNetwork | boolean | true | So sammeln Sie Ereignisse aus der Netzwerkdomäne.  |  
| enablePage | boolean | true | So sammeln Sie Ereignisse aus der Seiten Domäne.  |  
| traceCategories | string | \ (leer \) | Eine durch Kommas getrennte Zeichenfolge von Microsoft-Edge-Ablaufverfolgungskategorien, für die Ablaufverfolgungsereignisse erfasst werden sollen.  Eine nicht angegebene oder leere Zeichenfolge deaktiviert die Ablaufverfolgung.  |  
| bufferUsageReportingInterval | positive Ganzzahl | 1000 | Die angeforderte Anzahl von Millisekunden zwischen devtools-Ablaufverfolgungspuffer-nutzungsereignissen.  Wenn beispielsweise 1000, dann einmal pro Sekunde, devtools meldet, wie voll der Ablaufverfolgungspuffer ist.  Wenn ein Bericht angibt, dass die Puffernutzung 100% beträgt, wird eine Warnung ausgegeben.  |  

## Zurückgegebene Funktionen  

Die folgende Liste enthält alle Microsoft Edge-spezifischen Funktionen, die `EdgeDriver` beim Erstellen einer neuen Sitzung zurückgegeben werden.  

| Funktion | Typ | Details |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | Die Version von EdgeDriver. |  
| msedge.userDataDir | string | Der Pfad zum Benutzerdatenverzeichnis, das von der Microsoft Edge-Instanz verwendet wird. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Erste Schritte mit dem Remote Debuggen von Windows 10-Geräten | Microsoft docs"  
[DrivingEdgeWebDriverIndex]: ./index.md#driving-microsoft-edge-chromium "Driving Microsoft Edge (Chrom) | Microsoft docs"    
[DownloadEdgeWebDriverIndex]: ./index.md#install-microsoft-edge-chromium "Installieren von Microsoft Edge (Chrom) | Microsoft docs"  
[ChooseLanguageBindingWebDriverIndex]: ./index.md#choose-a-webdriver-language-binding "Auswählen einer WebDriver-Sprachbindung | Microsoft docs"

[SeleniumMain]: https://www.selenium.dev "SeleniumHQ-Browser Automatisierung"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Freigegebene Funktionen | Selen-Dokumentation"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver/#capabilities "Funktionen-WebDriver-Spezifikation | W3C"   
