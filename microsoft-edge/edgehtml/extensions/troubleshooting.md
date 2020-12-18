---
ms.assetid: 8b7f362f-da09-43db-8a42-cfa128c1808c
description: Hier erhalten Sie Antworten auf häufig gestellte Fragen, die beim Laden von ungepackten Erweiterungen auftreten können.
title: Erweiterungen – Problembehandlung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 74743923000766473a96b56a97d302b6ab79a9e3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233790"
---
# Problembehandlung  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Wenn Sie versuchen, ungepackte Erweiterungen zu laden und Probleme auftreten, können die folgenden Informationen hilfreich sein:

## 1. Ich sehe den Fehler "Diese Erweiterung konnte nicht geladen werden"

Dies bedeutet in der Regel, dass Microsoft Edge nicht auf den Erweiterungsordner zugreifen kann, den Sie zu laden versucht haben.

Nachfolgend finden Sie eine Zusammenfassung der möglichen Fehler, die möglicherweise auftreten:

Fehlermeldung | Details
:--------- | :------------
Manifest-Analysefehler: fehlende oder fehlerhafte Manifestdatei. | Entweder wurde die Datei am `"manifest.json"` angegebenen Speicherort nicht gefunden, oder die Datei hat einen Fehler. Um das Problem zu beheben, stellen Sie sicher, dass der angegebene Ordner das Manifest auf der obersten Ebene enthält, und doppelklicken Sie auf die Kommas, Anführungszeichen und Klammern.
Manifest-Analysefehler: `"content_scripts"` muss ein Array definieren. | Das Feld `"content_scripts"` sollte ein Array sein. Um das Problem zu beheben, überprüfen Sie die Syntax. Zum Beispiel: `"content_scripts": [{"matches": [...],"css": [...],"js": [...] }]`
Manifest-Analysefehler: `"content_scripts"` muss den Wert für `"matches"` Property definieren. | Die Eigenschaft `"matches"` ist erforderlich. Um das Problem zu beheben, geben Sie den Wert der Eigenschaft mit einem Array von Zeichenfolgen an. Zum Beispiel: `"content_scripts": [ {... "matches": ["http://www.bing.com"] ...} ]`
Manifest-Analysefehler: `"content_scripts"` muss auf mindestens eine CSS-oder JS-Datei verweisen. | Mindestens eine Eigenschaft `"css"` oder `"js"` erforderlich. Um das Problem zu beheben, geben Sie den Wert der Eigenschaft mit einem Array von Zeichenfolgen an. Zum Beispiel: `"content_scripts": [ { ... "js": ["myScript1.js", "myScript2.js"] ...} ]`
Manifest-Analysefehler: `"<field>"` muss den Wert für " <property> "-Eigenschaft definieren. | Die Eigenschaft `<property>` für das Feld `<field>` ist erforderlich. Um das Problem zu beheben, geben Sie einen gültigen Wert für an `<property>` .
Manifest-Analysefehler: `"content_scripts"` verweist auf einen ungültigen Wert für das Feld "run_at". | Die Eigenschaft `"run_at"` gibt einen unbekannten Wert an. Um das Problem zu beheben, geben Sie `"document_start"` eines `"document_end"` oder ein `"document_idle"` . Zum Beispiel: `"content_scripts": [ {... "run_at": "document_start" ... } ]`
Manifest-Analysefehler: Fehlendes `"<field>"` Feld. | Das Feld `<field>` ist erforderlich. Um das Problem zu beheben, definieren Sie das Feld mit einem gültigen Wert.
Manifest-Analysefehler: Ungültiges Feld `"<field1>"` gefunden in `"<field2>"` . | Das Feld <field1> für das Feld <field2> gibt einen unbekannten Wert an. Um das Problem zu beheben, geben Sie einen gültigen Wert für an <field1> .
Manifest-Analysefehler: Ungültiger Wert für " <field> "-Feld. | Das Feld <field> gibt einen unbekannten Wert an. Um das Problem zu beheben, geben Sie einen gültigen Wert an.
Fehler bei der Manifest-Analyse: die Erweiterung wird von der aktuellen Version von Microsoft Edge nicht unterstützt. | Die Eigenschaft `"minimum_edge_version"` gibt eine neuere Version von Microsoft Edge an als die, die Sie besitzen. Sie können die aktuelle Version finden, indem Sie das "..." öffnen. (Mehr) und wählen Sie dann "Einstellungen" (unter dem Abschnitt "Informationen zu dieser app"). Um das Problem zu beheben, aktualisieren Sie Ihren Browser entweder auf eine neuere Version, oder ändern Sie den Wert im Manifest. Zum Beispiel: `"minimum_edge_version": "x.xxxx.xxxx.x"`
Manifest-Analysefehler: `"background"` muss den Wert für die Eigenschaft "page" oder "Scripts" definieren. | Die Eigenschaft "Seite" oder "Skripte" ist für das Feld "Hintergrund" erforderlich. Um das Problem zu beheben, geben Sie eine Zeichenfolge für "page" oder ein Array von Zeichenfolgen für "Skripts" an. Zum Beispiel: `"background": { ... "scripts": ["background.js"] ... }`
Manifest-Analysefehler: `"background"` muss den Wert für `"persistent"` Property definieren. | Die Eigenschaft `"persistent"` ist erforderlich. Um das Problem zu beheben, geben Sie den Wert wahr oder falsch ein. Zum Beispiel: `"background": {... "persistent": true ...}`
Manifest-Analysefehler: nur ein `"browser_action"` oder `"page_action"` kann definiert werden. | Eine Erweiterung kann nicht gleichzeitig eine Seiten Aktion und eine Browser Aktion definieren. Um das Problem zu beheben, entfernen Sie entweder eine der Definitionen.
Unspezifizierter Fehler: `<error>` | Generische Catch-All-Fehlermeldung. `<error>` wird durch den angegebenen Fehler ersetzt.


## 2. die Schaltfläche "Lade Erweiterung" wird nicht angezeigt
Bis Erweiterungen über den Microsoft Store verfügbar sind, *sollte* diese Schaltfläche standardmäßig angezeigt werden. Wenn Sie das Menü "mehr" (...) öffnen, wählen Sie das Menüelement "Erweiterungen" aus, und sehen Sie die Schaltfläche nicht, gehen Sie folgendermaßen vor:

1. Geben Sie in der Adressleiste **"about: Flags"** ein, und drücken Sie die **Eingabe** Taste.
2. Stellen Sie unter der Überschrift **"Entwicklereinstellungen"** sicher, dass das Kontrollkästchen neben **"Erweiterungsentwickler Features aktivieren"** aktiviert ist.

   ![Informationen zu Flags](./media/aboutflags.PNG)  

3. Schließen Sie Microsoft Edge, und öffnen Sie es erneut, und überprüfen Sie, ob die Schaltfläche **"Erweiterung laden"** nun angezeigt wird.
