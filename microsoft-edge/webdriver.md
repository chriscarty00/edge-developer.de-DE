---
ms.assetid: e56172c0-b635-4c02-8e0c-56bf8cb4c164
description: Hier erfahren Sie, wie Sie mit WebDriver beginnen, einem Draht Protokoll, mit dem Programme und Skripts das Verhalten des Webbrowsers steuern können.
title: WebDriver (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, WebDriver, Selen, testen
ms.openlocfilehash: 0a6ef78103852234a6b52dfe88e60273cc3bd3d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568732"
---
# WebDriver (EdgeHTML)
Bei der W3C- [WebDriver](https://www.w3.org/TR/webdriver/) -API handelt es sich um eine Plattform-und sprachneutrale Schnittstelle und ein Draht Protokoll, mit der Programme oder Skripts das Verhalten eines Webbrowsers steuern können.

WebDriver ermöglicht Entwicklern das Erstellen automatisierter Tests, die die Benutzerinteraktion simulieren. Dies unterscheidet sich von JavaScript-Komponententests, da WebDriver Zugriff auf Funktionen und Informationen hat, die JavaScript im Browser nicht ausführt, und es können Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer simuliert werden. WebDriver kann auch Tests über mehrere Fenster, Registerkarten und Webseiten in einer einzigen Testsitzung verwalten.

Hier erfahren Sie, wie Sie mit WebDriver für Microsoft Edge (EdgeHTML) beginnen.

Die Microsoft Edge-Implementierung (EdgeHTML) von WebDriver unterstützt sowohl die W3C- [WebDriver](https://www.w3.org/TR/webdriver/) -Spezifikation als auch das [JSON-Wire-Protokoll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol) für die Abwärtskompatibilität mit vorhandenen Tests.

## Erste Schritte mit WebDriver für Microsoft Edge (EdgeHTML)
* Installieren Sie Windows 10.
* Laden Sie den entsprechenden [Microsoft WebDriver](https://developer.microsoft.com/microsoft-edge/tools/webdriver/) -Server für Ihren Build von Windows und Microsoft Edge (EdgeHTML) herunter.
* Laden Sie die WebDriver-Sprachbindung Ihrer Wahl herunter. [Alle Selenium-Sprachbindungen unterstützen Microsoft Edge (EdgeHTML)](https://docs.seleniumhq.org/download/).

> [!NOTE]
> Hilfe, Berichts Probleme und Datei Funktionsanforderungen finden Sie unter [Microsoft Edge (EdgeHTML) Feedback &-Support](https://developer.microsoft.com/microsoft-edge/support/).


## Verwenden von WebDriver
Die ersten Schritte mit WebDriver mit Microsoft Edge (EdgeHTML) finden Sie in den folgenden Beispielen:

* [C \ # Codebeispiel](https://gist.github.com/InstyleVII/baf25274c55e891076d5#file-webdriver-cs) zum Öffnen eines Browserfensters, navigieren zu Bing.com und suchen nach "WebDriver" (GitHub GIST).

## Befehlszeilen Attribute für WebDriver Server
Liste der Befehlszeilen Kennzeichen für den WebDriver-Server.

| Name    | Beschreibung                                                                                                      | Verfügbare Version |
|:--------|:-----------------------------------------------------------------------------------------------------------------|:------------------|
| Host    | Host-IP für den WebDriver-Server (Standard: localhost)                                                     | 14393             |
| Anschluss    | Zu verwendender Port für den WebDriver-Server (Standard: 17556)                                                            | 14393             |
| package | ApplicationUserModelId (AUMID) für die Anwendung, die vom WebDriver-Server gestartet werden soll                        | 14393             |
| Ausführliche | Ausgänge empfangene Anfragen und Antworten, die vom WebDriver-Server gesendet wurden                                             | 14393             |
| lautlos  | Gibt nichts aus                                                                                                  | 15063             |
| version | Gibt die Version von "MicrosoftWebDriver. exe" aus.                                                                    | 17763             |
| W3C     | Verwenden des W3C-weblaufwerks Protokolls (Standardoption)                                                                      | 17763             |
| JWP     | Verwenden des JSON-Draht Protokolls                                                                                           | 17763             |
| Bereinigung | Bereinigen von temporären Daten und Registrierungsschlüsseln, die vom WebDriver-Server für-Paket festgelegten sind. Andere Parameter werden ignoriert | 17763             |

## W3C-WebDriver
Die Unterstützung für die [W3C-WebDriver-Spezifikation](https://www.w3.org/TR/webdriver/)pro Befehl.

### Funktionen
| Funktion                       | Schlüssel                       | Status                   | Verfügbare Version |
|:---------------------------------|:--------------------------|:-------------------------|:------------------|
| Browser Name                     | Browser Name             | Unterstützt                | 17763             |
| Browser Version                  | Browserversion          | Unterstützt                | 17763             |
| Platt Form Name                    | platformName            | Unterstützt                | 17763             |
| Akzeptieren von unsicheren TLS-Zertifikaten | "acceptInsecureCerts"     | Nicht &nbsp; unterstützt       | n.v.               |
| Seiten Lade Strategie               | "pageLoadStrategy"        | Unterstützt                | 17763             |
| Proxykonfiguration              | Proxy                   | Nicht &nbsp; unterstützt       | n.v.               |
| Fenster Bemaßung/-Positionierung  | setWindowRect           | Unterstützt                | 17763             |
| Konfiguration der Sitzungstimeouts   | Timeouts                | Unterstützt                | 17763             |
| Unbehandeltes Eingabe Aufforderungsverhalten        | "unhandledPromptBehavior" | Teilweise &nbsp; unterstützt | 17763             |
| InPrivate                        | "MS: InPrivate"            | Unterstützt                | 17763             |
| Erweiterungs Pfade                  | "MS: extensionPaths"       | Unterstützt                | 17763             |
| Startseite                       | "MS: Startpage"            | Unterstützt                | 17763             |

### Locator-Strategien
| Locator-Strategie                                                        | Status    | Verfügbare Version |
|:------------------------------------------------------------------------|:----------|:------------------|
| [CSS-Auswahlen](https://www.w3.org/TR/webdriver/#css-selectors)         | Unterstützt | 17763             |
| [Verknüpfen von Text](https://www.w3.org/TR/webdriver/#link-text)                 | Unterstützt | 17763             |
| [Text für teilweise Verknüpfung](https://www.w3.org/TR/webdriver/#partial-link-text) | Unterstützt | 17763             |
| [Tag-Name](https://www.w3.org/TR/webdriver/#tag-name)                   | Unterstützt | 17763             |
| [XPath](https://www.w3.org/TR/webdriver/#xpath)                         | Unterstützt | 17763             |

### Befehle
| HTTP Method | URI-Vorlage                                                   | Befehl                                                                                   | Status             | Verfügbare Version |
|:------------|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------|:-------------------|:----------------  |
| POST        | /session                                                       | [Neue Sitzung](https://www.w3.org/TR/webdriver/#new-session)                               | Unterstützt          | 17763             |
| DELETE      | /Session/{Session-ID}                                          | [Sitzung löschen](https://www.w3.org/TR/webdriver/#delete-session)                         | Unterstützt          | 17763             |
| GET         | /Status                                                        | [Status](https://www.w3.org/TR/webdriver/#status)                                         | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Timeouts                                 | [Timeouts abrufen](https://www.w3.org/TR/webdriver/#get-timeouts)                             | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Timeouts                                 | [Timeouts einstellen](https://www.w3.org/TR/webdriver/#set-timeouts)                             | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/URL                                      | [Navigieren Sie zu](https://www.w3.org/TR/webdriver/#navigate-to)                               | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/URL                                      | [Aktuelle URL abrufen](https://www.w3.org/TR/webdriver/#get-current-url)                       | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Back                                     | [Zurück](https://www.w3.org/TR/webdriver/#back)                                             | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Forward                                  | [Vorwärts](https://www.w3.org/TR/webdriver/#forward)                                       | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Refresh                                  | [Aktualisieren](https://www.w3.org/TR/webdriver/#refresh)                                       | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Titel                                    | [Titel abrufen](https://www.w3.org/TR/webdriver/#get-title)                                   | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Window                                   | [Fenster Handle abrufen](https://www.w3.org/TR/webdriver/#get-window-handle)                   | Unterstützt          | 17763             |
| DELETE      | /Session/{Session-ID}/Window                                   | [Fenster schließen](https://www.w3.org/TR/webdriver/#close-window)                             | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Window                                   | [Zu Fenster wechseln](https://www.w3.org/TR/webdriver/#switch-to-window)                     | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Window/Handles                           | [Abrufen von Fensterhandles](https://www.w3.org/TR/webdriver/#get-window-handles)                 | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Frame                                    | [Zu Frame wechseln](https://www.w3.org/TR/webdriver/#switch-to-frame)                       | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Frame/Parent                             | [Zum übergeordneten Frame wechseln](https://www.w3.org/TR/webdriver/#switch-to-parent-frame)         | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Window/Rect                              | [Abrufen des Fensterrechtecks](https://www.w3.org/TR/webdriver/#get-window-rect)                       | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Window/Rect                              | [Fensterrechteck einrichten](https://www.w3.org/TR/webdriver/#set-window-rect)                       | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Window/Maximize                          | [Fenster maximieren](https://www.w3.org/TR/webdriver/#maximize-window)                       | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Window/Minimize                          | [Fenster minimieren](https://www.w3.org/TR/webdriver/#minimize-window)                       | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Window/Fullscreen                        | [Vollbild-Fenster](https://www.w3.org/TR/webdriver/#fullscreen-window)                   | Nicht &nbsp; unterstützt | n.v.               |
| GET         | /Session/{Session-ID}/Element/Active                           | [Abrufen des aktiven Elements](https://www.w3.org/TR/webdriver/#get-active-element)                 | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/normales Element                                  | [Element suchen](https://www.w3.org/TR/webdriver/#find-element)                             | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Elements                                 | [Suchen von Elementen](https://www.w3.org/TR/webdriver/#find-elements)                           | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Element/{Element-ID}/normales Element             | [Element aus Element suchen](https://www.w3.org/TR/webdriver/#find-element-from-element)   | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Element/{Element-ID}/Elements            | [Suchen von Elementen aus einem Element](https://www.w3.org/TR/webdriver/#find-elements-from-element) | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Element/{Element-ID}/Selected            | [Ist-Element markiert](https://www.w3.org/TR/webdriver/#is-element-selected)               | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Element/{Element-ID}/Attribute/{Name}    | [Get-Element Attribut](https://www.w3.org/TR/webdriver/#get-element-attribute)           | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Element/{Element-ID}/Property/{Name}     | [Get-Element Eigenschaft](https://www.w3.org/TR/webdriver/#get-element-property)             | Unterstützt          | 17763             |
| GET         | /Session/{Session ID}/Element/{Element ID}/CSS/{Property Name} | [Element-CSS-Wert abrufen](https://www.w3.org/TR/webdriver/#get-element-css-value)           | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Element/{Element-ID}/Text                | [Abrufen von Element Text](https://www.w3.org/TR/webdriver/#get-element-text)                     | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Element/{Element-ID}/Name                | [Element-Tag-Name abrufen](https://www.w3.org/TR/webdriver/#get-element-tag-name)             | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Element/{Element-ID}/Rect                | [Element Rect abrufen](https://www.w3.org/TR/webdriver/#get-element-rect)                     | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Element/{Element-ID}/Enabled             | [Ist-Element aktiviert](https://www.w3.org/TR/webdriver/#is-element-enabled)                 | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Element/{Element-ID}/Klick funktioniert               | [Element klicken](https://www.w3.org/TR/webdriver/#element-click)                           | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Element/{Element-ID}/Clear               | [Element löschen](https://www.w3.org/TR/webdriver/#element-clear)                           | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Element/{Element-ID}/sendKeys            | [Schlüssel "Element senden"](https://www.w3.org/TR/webdriver/#element-send-keys)                   | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Source                                   | [Abrufen der Seitenquelle](https://www.w3.org/TR/webdriver/#get-page-source)                       | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Execute/Sync                             | [Skript ausführen](https://www.w3.org/TR/webdriver/#execute-script)                         | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Execute/Async                            | [Ausführen eines asynchronen Skripts](https://www.w3.org/TR/webdriver/#execute-async-script)             | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Cookie                                   | [Abrufen aller Cookies](https://www.w3.org/TR/webdriver/#get-all-cookies)                       | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Cookie/{Name}                            | [Erhalten des benannten Cookies](https://www.w3.org/TR/webdriver/#get-named-cookie)                     | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Cookie                                   | [Cookie hinzufügen](https://www.w3.org/TR/webdriver/#add-cookie)                                 | Unterstützt          | 17763             |
| DELETE      | /Session/{Session-ID}/Cookie/{Name}                            | [Löschen eines Cookies](https://www.w3.org/TR/webdriver/#delete-cookie)                           | Unterstützt          | 17763             |
| DELETE      | /Session/{Session-ID}/Cookie                                   | [Alle Cookies löschen](https://www.w3.org/TR/webdriver/#delete-all-cookies)                 | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Actions                                  | [Ausführen von Aktionen](https://www.w3.org/TR/webdriver/#perform-actions)                       | Unterstützt          | 17763             |
| DELETE      | /Session/{Session-ID}/Actions                                  | [Freigabe Aktionen](https://www.w3.org/TR/webdriver/#release-actions)                       | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Alert/Dismiss                            | [Benachrichtigung ablehnen](https://www.w3.org/TR/webdriver/#dismiss-alert)                           | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Alert/Accept                             | [Benachrichtigung annehmen](https://www.w3.org/TR/webdriver/#accept-alert)                             | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Alert/Text                               | [Abrufen von Warnungs Text](https://www.w3.org/TR/webdriver/#get-alert-text)                         | Unterstützt          | 17763             |
| POST        | /Session/{Session-ID}/Alert/Text                               | [Benachrichtigungs Text senden](https://www.w3.org/TR/webdriver/#send-alert-text)                       | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Screenshot                               | [Screenshot aufnehmen](https://www.w3.org/TR/webdriver/#take-screenshot)                       | Unterstützt          | 17763             |
| GET         | /Session/{Session-ID}/Screenshot/{Element-ID}                  | [Screenshot des Take-Elements](https://www.w3.org/TR/webdriver/#take-element-screenshot)       | Unterstützt          | 17763             |

## JSON-Wire-Protokoll
Die Unterstützung für das [JSON Wire-Protokoll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol)pro Befehl.

### Befehle
| HTTP Method | Pfad                                                                                                                                                         | Status             | Verfügbare Version |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------|:------------------|
| GET         | [/Status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#status)                                                                               | Unterstützt          | 10240             |
| POST        | [/session](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#session-1)                                                                           | Unterstützt          | 10240             |
| GET         | [/sessions](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessions)                                                                           | Unterstützt          | 10240             |
| GET         | [/Session/: SessionID](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Unterstützt          | 10240             |
| DELETE      | [/Session/: SessionID](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Timeouts](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeouts)                                        | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Timeouts/async_script](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsasync_script)               | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Timeouts/implicit_wait](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsimplicit_wait)             | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/window_handle](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handle)                              | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/window_handles](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handles)                            | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/URL](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/URL](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Forward](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidforward)                                          | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/zurück](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidback)                                                | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Refresh](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidrefresh)                                          | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Execute](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute)                                          | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/execute_async](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute_async)                              | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Screenshot](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidscreenshot)                                    | Unterstützt          | 10240             |
| GET         | [/Session/: SessionID/IME/available_engines](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeavailable_engines)               | Nicht &nbsp; unterstützt | n.v.               |
| GET         | [/Session/: SessionID/IME/active_engine](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactive_engine)                       | Nicht &nbsp; unterstützt | n.v.               |
| GET         | [/Session/: SessionID/IME/aktiviert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivated)                               | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/IME/Deactivate](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimedeactivate)                             | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/IME/Activate](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivate)                                 | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Frame](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframe)                                              | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Frame/übergeordnetes Element](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframeparent)                                 | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Fenster](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Unterstützt          | 10586             |
| DELETE      | [/Session/: SessionID/Fenster](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Window/: windowHandle/Größe](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Window/: windowHandle/Größe](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Window/: windowHandle/Position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Window/: windowHandle/Position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Window/: windowHandle/maximieren](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlemaximize) | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Unterstützt          | 10240             |
| DELETE      | [/Session/: SessionID/Cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Unterstützt          | 10586             |
| DELETE      | [/Session/: SessionID/Cookie/: Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookiename)                                  | Unterstützt          | 10240             |
| GET         | [/Session/: SessionID/Quelle](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsource)                                            | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID}/Titel](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtitle)                                             | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Element](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelement)                                          | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Elemente](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelements)                                        | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Element/aktiv](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementactive)                             | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Element/: ID](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementid)                                    | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Element/: ID/Element](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelement)                     | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Element/: ID/Elemente](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelements)                   | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Element/: ID/Click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclick)                         | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Element/: ID/Submit](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsubmit)                       | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Element/: ID/Text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidtext)                           | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Element/: ID/Wert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidvalue)                         | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Keys](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidkeys)                                                | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Element/: ID/Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidname)                           | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Element/: ID/Clear](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclear)                         | Unterstützt          | 10240             |
| GET         | [/Session/: SessionID/Element/: ID/ausgewählt](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidselected)                   | Unterstützt          | 10240             |
| GET         | [/Session/: SessionID/Element/: ID/aktiviert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidenabled)                     | Unterstützt          | 10240             |
| GET         | [/Session/: SessionID/Element/: ID/Attribut/: Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidattribute/:name)     | Unterstützt          | 10240             |
| GET         | [/Session/: SessionID/Element/: ID/entspricht/: anderes](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidequals/:other)         | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Element/: ID/angezeigt](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementiddisplayed)                 | Unterstützt          | 10240             |
| GET         | [/Session/: SessionID/Element/: ID/Ort](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation)                   | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Element/: ID/location_in_view](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation_in_view)   | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Element/: ID/Größe](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsize)                           | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Element/: ID/CSS/:p ropertyname](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidcss/:propertyName) | Unterstützt          | 10240             |
| GET         | [/Session/: SessionID/Ausrichtung](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Ausrichtung](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Nicht &nbsp; unterstützt | n.v.               |
| GET         | [/Session/: SessionID/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/accept_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidaccept_alert)                                | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/dismiss_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddismiss_alert)                              | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Schalt](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidmoveto)                                            | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/klicken](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidclick)                                              | Unterstützt          | 10240             |
| POST        | [/Session/: SessionID/Button down](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttondown)                                    | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/BUTTONUP](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttonup)                                        | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddoubleclick)                                  | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/tippen/klicken](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchclick)                                   | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Touch/Down](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdown)                                     | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Touch/up](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchup)                                         | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Touch/Move](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchmove)                                     | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Touch/Scroll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll)                                 | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Touch/Scroll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll-1)                               | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Touch/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdoubleclick)                       | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Touch/longclick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchlongclick)                           | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Touch/Flick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick)                                   | Nicht &nbsp; unterstützt | n.v.               |
| POST        | [/Session/: SessionID/Touch/Flick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick-1)                                 | Nicht &nbsp; unterstützt | n.v.               |
| GET         | [/Session/: SessionID/Ort](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/Ort](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Unterstützt          | 10586             |
| DELETE      | [/Session/: SessionID/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/local_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Unterstützt          | 10586             |
| DELETE      | [/Session/: SessionID/local_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/local_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagesize)                     | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Unterstützt          | 10586             |
| POST        | [/Session/: SessionID/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Unterstützt          | 10586             |
| DELETE      | [/Session/: SessionID/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/session_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Unterstützt          | 10586             |
| DELETE      | [/Session/: SessionID/session_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/session_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagesize)                 | Unterstützt          | 10586             |
| GET         | [/Session/: SessionID/Log](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlog)                                                  | Nicht &nbsp; unterstützt | n.v.               |
| GET         | [/Session/: SessionID/Log/Typen](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlogtypes)                                       | Nicht &nbsp; unterstützt | n.v.               |
| GET         | [/Session/: SessionID/application_cache/Status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidapplication_cachestatus)         | Unterstützt          | 10586             |  
