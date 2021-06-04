---
description: Ein Verweis auf WebDriver-Funktionen und Microsoft Edge-spezifische Optionen, die von EdgeDriver (Chromium) unterstützt werden.
title: Funktionen und EdgeOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, HTML, CSS, Javascript, Entwickler, WebDriver, Selenium, Tests, Tools, Automatisierung, Test
ms.openlocfilehash: 5a48ca34e46b56fa60bcacfade2add23026be144
ms.sourcegitcommit: f95812c4e1b7277f67c6c4891be2779cc1b5bdf1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2021
ms.locfileid: "11343779"
---
# Funktionen und EdgeOptions  

Funktionen sind Optionen, die Sie zum Anpassen und Konfigurieren einer Sitzung `EdgeDriver` verwenden können.  Weitere Informationen zum Starten einer neuen `EdgeDriver` Sitzung finden Sie unter Automatisieren von Microsoft [Edge][WebdriverIndexAutomateMicrosoftEdgeChromium].  In diesem Artikel werden alle unterstützten Funktionen für [Microsoft Edge und][WebdriverIndexInstallMicrosoftEdgeChromium] Details zum Übergeben der Funktionen an Sitzungen `EdgeDriver` beschrieben.  

Funktionen werden als #A0 an eine WebDriver-Sitzung übergeben.  WebDriver-Sprachbindungen bieten in der Regel typsichere Komfortmethoden, sodass Sie die #A0 nicht selbst konfigurieren müssen.  Unterschiedliche WebDriver-Sprachbindungen verwenden unterschiedliche Mechanismen zum Konfigurieren von Funktionen.  Navigieren Sie zur Dokumentation für Ihre [bevorzugte Sprachbindung,][WebdriverIndexChooseWebdriverLanguageBinding] um mehr über das Konfigurieren von Funktionen zu erfahren.  [Selenium][SeleniumMain] konfiguriert Funktionen über die `EdgeOptions` Klasse.  

##  <a name="using-the-edgeoptions-class"></a>Verwenden der EdgeOptions-Klasse  

Erstellen Sie eine Instanz von `EdgeOptions` , die Convenience-Methoden zum Festlegen von Microsoft Edge-spezifischen Funktionen bietet.  Nachdem Sie das Objekt `EdgeOptions` konfiguriert haben, übergeben Sie `EdgeOptions` es an den `EdgeDriver` Konstruktor.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Verwenden Sie die -Methode, um Funktionen zu verwenden, die keine zugehörige Komfortmethode `AddAdditionalCapability` haben.  Sie müssen den vollständigen Namen der Funktion und einen Wert mit dem richtigen Typ übergeben.  Navigieren Sie zum EdgeOptions-Objekt, um die vollständige Liste der akzeptierten Funktionen und [Werttypen zu überprüfen.](#edgeoptions-object)  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

##  <a name="recognized-capabilities"></a>Erkannte Funktionen  

Standardfunktionen, die akzeptiert werden, finden Sie in der `EdgeDriver` [#A0][SharedCapabilitiesSeleniumDocumentation] und im [W3C WebDriver-Standard.][CapabilitiesW3cWebdriver]  In diesem Artikel werden nur funktionen aufgeführt, die für Microsoft Edge spezifisch sind.  

## <a name="edgeoptions-object"></a>EdgeOptions-Objekt  

Die meisten Microsoft Edge-spezifischen Funktionen werden über das Objekt `EdgeOptions` verfügbar gemacht.  In einigen Sprachen werden die Funktionen von der Klasse `EdgeOptions` implementiert.  In anderen Sprachen werden die Funktionen unter dem `ms:edgeOptions` Wörterbuch in `DesiredCapabilities` gespeichert.  

| Funktion | Typ | Standardwert | Details |  
|:--- |:--- |:--- |:--- |  
| args | Liste der Zeichenfolgen |  | Liste der Befehlszeilenargumente, die beim Starten von Microsoft Edge verwendet werden.  Argumente mit einem zugeordneten Wert sollten durch ein Zeichen `=` \(z. B. `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \) getrennt werden. |  
| binary | string |  | Pfad zur Microsoft Edge-Binärdatei, die \(unter macOS) verwendet werden soll, sollte der Pfad die eigentliche Binärdatei sein, nicht nur die App.  z. B. `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \). |  
| debuggerAddress | string |  | Eine Adresse eines Debuggerservers, mit dem eine Verbindung hergestellt werden soll, z. B. `hostname/ip:port` `127.0.0.1:38947` . |
| detach | boolean | `false` | Wenn , wird Microsoft Edge beendet, wenn der WebDriver-Dienst heruntergefahren wird, auch wenn das lokale WebDriver-Ende die Sitzung `false` nicht geschlossen hat.  Wenn `true` , wird Microsoft Edge nur beendet, wenn das lokale WebDriver-Ende die Sitzung schließt.  Wenn `true` , und das lokale WebDriver-Ende die Sitzung nicht schließt, wird der temporäre Benutzerdatenordner, der von der Microsoft #A0 verwendet wird, nicht `EdgeDriver` bereinigt. |  
| excludeSwitches | Liste der Zeichenfolgen |  | Liste der Microsoft #A0 zum Ausschließen, dass EdgeDriver beim Starten von Microsoft Edge standardmäßig besteht.  Vermeiden Sie `--` das Präfix für Switches. |  
| extensions | Liste der Zeichenfolgen |  | Eine Liste der Erweiterungen, die beim Start installiert werden.  Jedes Element in der Liste sollte eine base-64-codierte gepackte Erweiterung \( `.crx` \) sein. |  
| localState | dictionary |  | Ein Wörterbuch mit jedem Eintrag, der aus dem Namen der Einstellung und dem Wert besteht.  Die Einstellungen werden auf die Datei "Lokaler Status" im Benutzerdatenordner angewendet. |  
| minidumpPath | string |  | Verzeichnis zum Speichern von Microsoft Edge-Minidumps.  \(Wird nur unter Linux unterstützt.\) |  
| mobileEmulation | dictionary |  | Ein Wörterbuch mit einem Wert für `deviceName` , oder Werten für und `deviceMetrics` `userAgent` . |  
| perfLoggingPrefs | dictionary |  | Ein optionales Wörterbuch, das die Einstellungen für die Leistungsprotokollierung angibt.  Weitere Informationen finden Sie unter [perfLoggingPrefs-Objekt.](#perfloggingprefs-object) |  
| prefs | dictionary |  | Ein Wörterbuch mit jedem Eintrag, der aus dem Namen der Einstellung und dem Wert besteht.  Die Einstellungen werden nur auf das verwendete Benutzerprofil angewendet.  Navigieren Sie beispielsweise zu der `Preferences` Datei im Benutzerdatenordner von Microsoft Edge. |  
| wdpAddress | string |  | Eine Adresse eines Windows Device Portal-Servers, mit dem Sie eine Verbindung herstellen, z. B. `hostname/ip:port`  `127.0.0.1:50080` .  Weitere Informationen finden Sie unter [Remotedebubugen – Windows 10-Geräte][DevtoolsRemoteDebuggingWindows]. |  
| wdpPassword | string |  | Optionales Kennwort, das beim Herstellen einer Verbindung mit einem Windows Device Portal-Server verwendet werden soll.  Erforderlich, wenn die Authentifizierung auf dem Server aktiviert ist. |  
| wdpUsername | string |  | Optionaler Benutzername, der beim Herstellen einer Verbindung mit einem Windows Device Portal-Server verwendet werden soll.  Erforderlich, wenn die Authentifizierung auf dem Server aktiviert ist. |  
| windowsApp | string |  | Anwendungsbenutzermodell-ID eines zu startende Microsoft Edge-App-Pakets, z. B. `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` .  Verwenden Sie dies, anstatt eine Verbindung mit einem `windowsApp` `binary` Windows 10X-Gerät oder Emulator mithilfe des Windows Device Portals zu herstellen. |  
| windowTypes | Liste der Zeichenfolgen |  | Eine Liste der Fenstertypen, die in der Liste der Fensterhandles angezeigt werden.  Für den Zugriff auf Android-Webview-Elemente müssen Sie `webview` in die Liste aufgenommen werden. |  

## <a name="perfloggingprefs-object"></a>perfLoggingPrefs-Objekt  

Das `perfLoggingPrefs` Wörterbuch hat das folgende Format \(alle Schlüssel sind optional\).  

| Key | Typ | Standardwert | Details |  
|:--- |:--- |:--- |:--- |  
| bufferUsageReportingInterval | positive ganze Zahl | 1000 | Die angeforderte Anzahl von Millisekunden zwischen DevTools-Ablaufverfolgungspufferverwendungsereignissen.  Wenn beispielsweise 1000, dann einmal pro Sekunde, DevTools meldet, wie voll der Ablaufverfolgungspuffer ist.  Wenn ein Bericht angibt, dass die Pufferauslastung 100 % beträgt, wird eine Warnung ausgegeben. |  
| enableNetwork | boolean | true | So sammeln Sie \(oder nicht)-Ereignisse aus der Netzwerkdomäne. |  
| enablePage | boolean | true | So sammeln Sie \(oder nicht)-Ereignisse aus der Page-Domäne. |  
| traceCategories | string | \(empty\) | Eine durch Kommas getrennte Zeichenfolge von Microsoft Edge-Ablaufverfolgungskategorien, für die Ablaufverfolgungsereignisse erfasst werden sollen.  Eine nicht bestimmte oder leere Zeichenfolge deaktiviert die Ablaufverfolgung. |  

##  <a name="returned-capabilities"></a>Zurückgegebene Funktionen  

Die folgende Liste enthält alle Microsoft Edge-spezifischen Funktionen, die beim `EdgeDriver` Erstellen einer neuen Sitzung zurückgegeben werden.  

| Funktion | Typ | Details |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | Die Version von EdgeDriver. |  
| msedge.userDataDir | string | Der Pfad zum Benutzerdatenordner, der von der Microsoft Edge-Instanz verwendet wird. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Erste Schritte mit dem Remotedebugen von Windows 10-Geräten | Microsoft Docs"  
[WebdriverIndexChooseWebdriverLanguageBinding]: ./index.md#choose-a-webdriver-language-binding "Auswählen einer WebDriver-Sprachbindung – WebDriver (Chromium) | Microsoft Docs"
[WebdriverIndexAutomateMicrosoftEdgeChromium]: ./index.md#automate-microsoft-edge-chromium "Automatisieren von Microsoft Edge (Chromium) – WebDriver (Chromium) | Microsoft Docs"    
[WebdriverIndexInstallMicrosoftEdgeChromium]: ./index.md#install-microsoft-edge-chromium "Installieren von Microsoft Edge (Chromium) – WebDriver (Chromium) | Microsoft Docs"  

[SeleniumMain]: https://www.selenium.dev "SeleniumHQ-Browserautomatisierung"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Freigegebene Funktionen | Selenium-Dokumentation"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver#capabilities "Funktionen – WebDriver-Spezifikations-| W3C"   
