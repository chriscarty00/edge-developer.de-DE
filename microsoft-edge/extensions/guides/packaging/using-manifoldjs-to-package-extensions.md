---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Hier erfahren Sie, wie Sie Ihre Microsoft Edge-Erweiterung mit ManifoldJS, dem Open-Source-Tool "Node. js", im Handumdrehen verpacken.
title: Verwenden von ManifoldJS für Paketerweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.openlocfilehash: cca83a26c9f80eca6454e3b5b329f72a7491b6e2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567374"
---
# Verwenden von ManifoldJS zum Erstellen von Erweiterungs AppX-Paketen  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS ist ein Open-Source-Knoten. js-Tool, mit dem Sie schnell und problemlos ein Paket erstellen können, das Sie dann für die Übermittlung an den Microsoft Store verwenden können.

Wenn Sie in ihrer Erweiterung systemeigenes Messaging verwenden, sollten Sie dies überspringen und zu [systemeigener Nachrichten in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) für Verpackungsanweisungen wechseln. 

Bevor Sie beginnen, müssen Sie sich weiterhin mit den folgenden Artikeln vertraut machen:

- [Erweiterungen im Windows dev Center](./extensions-in-the-windows-dev-center.md)
- [Localize-Erweiterungspakete](./localizing-extension-packages.md)

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion. Nachdem Sie Ihre Erweiterung erstellt, verpackt und getestet haben, senden Sie uns bitte eine Anfrage über unser [Extension-Übermittlungsformular](https://aka.ms/extension-request).


## Installieren von Node. js und ManifoldJS

Als erstes müssen Sie [node. js LTS](https://nodejs.org/en/download/)installieren.
Nachdem Sie über eine Befehlszeile (vorzugsweise PowerShell) über einen Knoten verfügen, führen Sie den folgenden Befehl aus, um ManifoldJS zu installieren:

`npm install -g manifoldjs`

Um zu überprüfen, ob Sie ManifoldJS ordnungsgemäß installiert haben, führen Sie `manifoldjs` über die Befehlszeile aus. Wenn ManifoldJS nicht erkannt wurde, fügen Sie `%APPDATA%\npm` Ihre PATH-Variablen hinzu.

## Verpacken mit ManifoldJS

Um den Verpackungsprozess zu starten, müssen Sie eine Befehlszeile öffnen und Verzeichnisse in einen Ordner ändern, der das Ziel für Ihre verpackte Erweiterung ist.

Beispiel:

`cd C:\manifoldJSTest`

> [!NOTE]
> ManifoldJS wird im aktuellen Verzeichnis ausgegeben und kann Inhalt überschreiben.



Nachdem Sie sich nun im Zielordner befinden, führen Sie den folgenden Befehl aus:

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


Dieser Befehl kann in die folgenden Abschnitte unterteilt werden:
 -    **-l Debug**: ändert die Protokollebene in "Debug", um einen vollständigen Ausdruck zu erhalten.
 -    **-p edgeextension**: legt die einzige Plattform zum Ausführen der Konvertierung auf edgeextension fest.
 -    **-f edgeextension**: teilt dem Programm mit, dass das Format des Manifests ein edgeextension-Format ist und nicht zu beachten ist, wenn die Validierung fehlschlägt.
 -    **-m \ < Extension Location > \manifest.JSON**: der Pfad zu dem Erweiterungs Manifest, das Sie konvertieren möchten.


Nachdem ManifoldJS ausgeführt wurde, haben Sie einen Ordner mit folgendem Inhalt:

    My Extension
        edgeextension
            generationInfo.json
            manifest
                   appxmanifest.xml
                Assets
                    Square150x150Logo.png
                    Square44x44Logo.png
                    StoreLogo.png    
                Extension
                    manifest.json
                    popup.html
                    ...
                ...

Bei der generationInfo. JSON-Datei handelt es sich um ein vom Ausführen von ManifoldJS erstelltes Protokoll, das nicht in Ihrem Erweiterungspaket enthalten ist. Nur der Inhalt des **Manifest** -Ordners wird gepackt. Innerhalb des Manifest-Ordners enthält der Ordner "Objekte" die Bilder, die in der Windows-und Microsoft Store-Benutzeroberfläche verwendet werden, während der Ordner "Extension" den Inhalt ihrer Erweiterung enthält.


Nachdem Sie nun über die richtigen Dateien verfügen, müssen Sie die generierte AppXManifest-Datei innerhalb des **Manifest** -Ordners bearbeiten. Wenn die Manifest. JSON-Datei der Erweiterung für das Feld "Name" eine Internationalisierungs Zeichenfolge enthält, wird der Name des obersten Layer-Ordners nach der Ausführung von ManifoldJS nicht unterstrichen und "msg" enthalten.

Beispielsweise eine Manifest. JSON-Datei mit dem folgenden `"name"` Feld:

`"name" : "__MSG_appName__"`

hat einen Manifest-Ordner, in dem sich die Datei befindet `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .

In der AppXManifest-Datei müssen Sie Folgendes ausführen:
 -    Ersetzen Sie das Feld erforderliche Identitätsfelder und PublisherDisplayName wie [hier](./creating-and-testing-extension-packages.md#app-identity-template-values)beschrieben. Beachten Sie, dass Sie Platzhalterwerte anstelle der Registrierung für ein Windows dev Center-Konto verwenden können, wenn Sie nur zu Testzwecken oder für die Unternehmens Verteilung verpackt sind.
 -    Ersetzen Sie die Platzhaltersymbole im Ordner "Objekte" durch Symbole für Ihre Erweiterung mit den gleichen Größen (150x150, 50x50, 44x44) und Namen. Informationen dazu, wo diese Symbole verwendet werden, finden Sie im [Design](./../design.md#icons-for-packaging) Handbuch.
 - Wenn Ihre Erweiterung lokalisiert ist, folgen Sie dem gesamten Leitfaden zur [Lokalisierung von Microsoft-Edge-Erweiterungen](./localizing-extension-packages.md) . Wenn Sie nicht lokalisiert ist, lesen Sie [im Abschnitt Microsoft Store nur den Namen und die Beschreibung der Lokalisierung](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .

Nachdem die Datei "appxmanifest. xml" aussortiert wurde, führen Sie den folgenden Befehl aus, um Ihr Paket zu erstellen:

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

Ihr Paket befindet sich nun im **Paket** Ordner im Ordner edgeextension. Informationen zum querladen des neuen Pakets finden Sie unter Erstellen und Testen des [Test](./creating-and-testing-extension-packages.md#testing-an-appx-package) Abschnitts für Erweiterungspakete.

Nachdem Ihr Paket getestet wurde, können Sie eine Anfrage über unser [Extension-Übermittlungsformular](https://aka.ms/extension-request) einreichen, um für die Veröffentlichung im Microsoft Store in Frage zu kommen.
