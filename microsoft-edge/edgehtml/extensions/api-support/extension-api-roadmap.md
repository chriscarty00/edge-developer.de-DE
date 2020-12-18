---
description: Hier finden Sie Informationen zu den aktuellen Fortschritten beim Abschließen der Microsoft Edge-Erweiterungs-API.
title: Roadmap für Erweiterungen-API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, API, Erweiterungen, JavaScript, Entwickler
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3552fede729a37ff83ac4b19cfadf89d6917a75
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234272"
---
# Roadmap für Microsoft Edge Extension API  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Neben Web-APIs ermöglicht die Erweiterungs-API Erweiterungen, eine tiefere Integration mit dem Browserhost zu erreichen. Diese API bietet Entwicklern Zugriff auf die Browser Features von Microsoft Edge, wie etwa Tab-und Fenster Manipulation. In der folgenden Tabelle wird erläutert, welche APIs unterstützt werden/in der Entwicklung für Windows 10 öffentlich veröffentlichte Builds von Microsoft Edge.


|     Klasse     |                                                              Beschreibung                                                              |                Status – Buildnummer                 |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
|   Lesezeichen   |                                          Dient zum Erstellen, organisieren und Bearbeiten von Textmarken.                                          | Unterstützt – Microsoft Edge (40)/Windows 10 (15063) |
| BrowserAction |                                 Ermöglicht Erweiterungen das Hinzufügen einer beständigen Schaltfläche in Microsoft Edge.                                  | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
| Befehle      |                                                      Definiert Tastenkombinationen.                                                      | Unter Berücksichtigung
| contextMenus  |                           Fügt ein Kontextmenüelement für eine bestimmte URL in einem bestimmten Kontext einer Webseite hinzu.                            | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|    Cookies    |                                 Dient zum Abfragen und Ändern von Cookies sowie zur Benachrichtigung, wenn Sie geändert werden.                                 | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|   Downloads   |                           Wird zum programmgesteuerten initiieren, überwachen, manipulieren und suchen nach Downloads verwendet.                           |                 Unter Berücksichtigung                  |
|   Erweiterung   |                                      Enthält Dienstprogramme, die von jeder Erweiterungsseite verwendet werden können.                                       | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|    Verlauf    |                                         Interagiert mit dem Browser-Eintrag der besuchten Seiten.                                         |                 Unter Berücksichtigung                  |
|     i18n      |                                         Implementiert die Internationalisierung über eine Erweiterung hinweg.                                          | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|   Identität    |                                       Dient zum Abrufen eines OAuth2-Autorisierungscodes oder Zugriffstokens.                                       |                 Unter Berücksichtigung                  |
|     im Leerlauf      |                                       Wird verwendet, um zu ermitteln, wann der Leerlaufzustand des Computers geändert wird.                                        | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|  Management   |                                              Ruft Informationen zu installierten Add-ons ab.                                                |                 Unter Berücksichtigung                  |
| Benachrichtigungen |                      Ermöglicht das Erstellen von Benachrichtigungen mithilfe von Vorlagen, die in der Systemleiste des Benutzers angezeigt werden sollen.                      | Unterstützt – Microsoft Edge (42)/Windows 10 (17134) |
|  PageAction   |                                      Ermöglicht Erweiterungen das Hinzufügen einer Schaltfläche in der Adressleiste.                                       | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|  Berechtigungen  |                   Ermöglicht Benutzern, die optionalen Berechtigungen auszuwählen, auf die Sie einer Erweiterung Zugriff gewähren möchten.                   |                 Unter Berücksichtigung                  |
|    Runtime    | Ruft die Hintergrundseite ab, gibt Details zu dem Manifest zurück und überwacht und reagiert auf Ereignisse im Erweiterungs Lebenszyklus. | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|    Speicher    |                                      Wird von der Erweiterung zum Lesen/Schreiben von Daten und zum Synchronisieren von Daten verwendet.                                       | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|     Registerkarten      |                Interagiert mit dem Tab-System von Microsoft Edge, indem Tabstopps im Browser erstellt, geändert und neu angeordnet werden.                | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
| Webnavigation |                           Wird verwendet, um Benachrichtigungen über den Status von Navigationsanforderungen in Flight zu erhalten.                            | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|  WebRequest   |        Ermöglicht die Verwendung der WebRequest-API zum beobachten und Analysieren von Datenverkehr sowie zum Abfangen, blockieren oder Ändern von Anforderungen in Flight.        | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
|    windows    |                              Interagiert mit dem Browser durch erstellen, ändern und Neuanordnen von Fenstern.                              | Unterstützt – Microsoft Edge (38)/Windows 10 (14393) |
