---
ms.assetid: 1319a070-c6e3-4592-9f4b-40ce1575851f
description: Hier erfahren Sie, wie Sie Ihre Chrome-Erweiterung mithilfe des Microsoft Edge Extension Toolkit zu Microsoft Edge portieren.
title: Portieren von Chrome-Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.openlocfilehash: 38bf1324c2e7e6f7754912177ce0e53d6c15a276
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567371"
---
# Portieren einer Erweiterung von Chrome zu Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Das Portieren einer Erweiterung von Chrome zu Microsoft Edge wird mithilfe des [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb)vereinfacht. Dieses Entwicklertool wandelt eine ungepackte Chrome-Erweiterung in eine ungepackte Microsoft-Edge-Erweiterung um, indem Sie APIs überbrückt und Fehler in Ihrer Datei aufweist `manifest.json` .


### API-Bridges
Um eine nahtlose Portierung von Chrome-APIs auf unterstützte Microsoft Edge-APIs zu ermöglichen, werden dem Ordner Ihrer Erweiterung zwei Skripts hinzugefügt. Diese Skripts überbrücken APIs (bei Bedarf polyfiling), was bedeutet, dass Sie sich keine Gedanken über das Ändern von Chrome-spezifischem Code in Ihrem Hintergrundskript oder in Inhalts Skripts machen müssen.

Nach der Konvertierung werden die Dateien in der Manifestdatei ihrer Erweiterung mit dem folgenden Schlüssel angezeigt `"-ms-preload"` :

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## Verwenden des Microsoft Edge Extension Toolkit

Die folgenden Anweisungen erläutern, wie Sie Ihre Chrome-Erweiterung in Windows 10 Anniversary Update Edition auf Microsoft Edge konvertieren:

1. Installieren Sie das [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).
2. Erstellen Sie eine Kopie des Ordners ihrer Chrome-Erweiterung, um eine sichere Aufbewahrung zu gewährleisten. Durch den Konvertierungsprozess wird der Code überschrieben. 
3. Führen Sie das Microsoft Edge Extension Toolkit aus, und laden Sie die Kopie der Erweiterung.  
 ![Schaltfläche ' Erweiterung laden '](./../media/save-folder.png)
4. Korrigieren Sie alle Fehler, die im Text-Editor des Tools gemeldet werden. Wählen Sie "erneut überprüfen" aus, um nach dem korrigieren auf Fehler zu überprüfen.  
 ![Erweiterungen-Toolkitfehler finden](./../media/extension-toolkit.png)
5. Wählen Sie "Dateien speichern".

Sie können jetzt das Toolkit verlassen und ihre Erweiterung in Microsoft Edge laden! 

Sie können mit dem [EdgeHTML Issue Tracker](http://issues.microsoftedge.com)nach bekannten Platt Form Problemen suchen. Wenn Sie der Meinung sind, dass Sie etwas neues gefunden haben, [Öffnen Sie ein Problem](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!
