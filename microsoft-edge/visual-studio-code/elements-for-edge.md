---
description: Verwenden von Elementen für Microsoft Edge (Chrom) aus vs-Code
title: Elemente für Microsoft Edge (Chrom) aus vs-Code
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Elemente
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568674"
---
# Elemente für Microsoft Edge vs Code Extension

Indem Sie die [Elemente für Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs Code Extension hinzufügen, können Sie das Tool Elemente des Browsers in [Visual Studio-Code](https://code.visualstudio.com/)verwenden. Durch Starten oder Anfügen stellt das elementtool eine Verbindung mit einer Instanz von Microsoft Edge her, zeigt die HTML-Laufzeitstruktur an und ermöglicht Ihnen, das Layout zu ändern oder Formatierungsprobleme zu beheben.

![GIF der Elemente für Edge-vs-Code Erweiterung am Arbeitsplatz](./media/elements-for-edge.gif)

## Starten von Microsoft Edge aus der Elements-Erweiterung 

Navigieren Sie zu Elementen in der **Aktivitäts Leiste**. Neben der Schaltfläche "Elemente für Microsoft Edge: Ziele" gibt es ein Pluszeichen, mit dem der Browser für Ihre APP geöffnet wird. Wenn Sie die Option *about: blank* ausgewählt haben, müssen Sie im Browser zu Ihrer Web-App navigieren, damit Sie im vs-Code im Bedienfeld "Elemente" angezeigt wird.

## Starten von Microsoft Edge aus der Ansicht "Debuggen"

Wenn Sie mit der Debugansicht in Visual Studio-Code vertraut sind, können Sie über dieses Tool auf Elemente zugreifen. Navigieren Sie zur Ansicht Debuggen ( `Ctrl`  +  `Shift`  +  `D` unter Windows oder `Command`  +  `Shift`  +  `D` Mac). 

Wenn Sie keine Konfigurationen im vs-Code haben, drücken Sie `F5` Windows oder Mac, oder klicken Sie auf die grüne Schaltfläche " **Wiedergabe** ". Wählen Sie in der Dropdownliste "Edge" aus. Nun wird eine **JSON-Start** Datei mit der folgenden Konfiguration angezeigt:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```

Nachdem Sie nun die richtige Konfiguration geladen haben, drücken Sie entweder `F5` auf Windows oder Mac, oder klicken Sie auf die grüne **Wiedergabe** Schaltfläche. Das elementtool, mit dem Sie über den Microsoft Edge-Browser vertraut sind, wird nun im vs-Code gestartet, sodass Sie auf einen Screencast Ihres Browsers zugreifen und die Komponenten Ihrer Seite untersuchen können.

## Anfügen an Microsoft Edge
Wenn Sie einen vs-Code an eine Instanz von Microsoft Edge (Chrom) anfügen möchten, müssen Sie den Browser starten, indem Sie den folgenden Befehl in Ihrem Terminal ausführen:

`start msedge --remote-debugging-port=9222`

Nachdem die APP gestartet wurde, fügen Sie die folgende Konfiguration zu Ihrer **Start. JSON** -Datei hinzu:

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```

Wählen Sie "an Microsoft Edge anfügen aus, und öffnen Sie das elementtool" aus dem Dropdownmenü des Debuggers. Klicken Sie als nächstes entweder `F5` auf Windows oder Mac oder auf die grüne Schaltfläche " **Wiedergabe** ". Mit dem vs-Code wird das elementtool gestartet, sodass Sie auf einen Screencast Ihres Browsers zugreifen, das DOM und die Formatierung der Komponenten auf der Seite überprüfen können.

## Feedback senden
Senden Sie uns Ihr Feedback, indem Sie [ein Problem](https://github.com/microsoft/vscode-edge-devtools/issues/new) mit dem [GitHub-Repo](https://github.com/microsoft/vscode-edge-devtools)dieser Erweiterung einreichen. 

Wenn Sie uns helfen möchten, diese Erweiterung besser zu gestalten, freuen wir uns über Ihre Beiträge! Sie finden alles, was Sie für den Einstieg in [unser GitHub-Repo](https://github.com/microsoft/vscode-edge-devtools)benötigen.