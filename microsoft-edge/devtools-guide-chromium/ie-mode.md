---
description: IE-Modus und Microsoft Edge (Chrom) devtools
title: Internet Explorer-Modus und DevTools
author: robpaveza
ms.author: ropaveza
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, ie11, Internet Explorer 11, IE-Modus
ms.openlocfilehash: 18e5f029d277e446857ec48b9cf129149f219256
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568296"
---
# Internet Explorer-Modus und DevTools

In diesem Dokument wird beschrieben, wie der Internet Explorer-Modus (IE-Modus) in den Microsoft Edge (Chrom)-devtools integriert ist.

## Grundlegendes zum IE-Modus

Der IE-Modus ist ein Mechanismus, mit dem Unternehmen eine Reihe von Websites angeben können, die bis jetzt nur in Internet Explorer 11 funktionieren. Wenn diese Websites in Microsoft Edge (Chrom) angezeigt werden, wird eine vollständige Instanz von Internet Explorer 11 ausgeführt und auf der Registerkarte gerendert. Auf diese Weise können Unternehmen die Kompatibilität für IE-Dokumentmodi, ActiveX-Steuerelemente und andere Legacykomponenten verwalten, die derzeit nicht mit modernen Webbrowsern kompatibel sind.

Im IE-Modus basiert der Renderingprozess vollständig auf Internet Explorer 11. Der Microsoft Edge (Chrom)-Manager-Prozess verwaltet die Lebensdauer des Rendering-Prozesses, wird jedoch auf die Lebensdauer der Registerkarte auf einer bestimmten Website oder Anwendung beschränkt. Wenn eine Registerkarte im IE-Modus gerendert wird, wird in der Adressleiste für den angegebenen Reiter ein Badge angezeigt:

![IE-Modus-Abzeichen in der Adressleiste](./media/ie-mode-badge.png)

Der IE-Modus ist derzeit unter Windows 10, Version 1903 (Mai 2019-Update), verfügbar, wird aber demnächst für alle unterstützten Windows-Plattformen bereitgestellt.

## Starten des devtools auf einer Registerkarte im IE-Modus

Wenn Sie versuchen, den Dokumentmodus einer Website im IE-Modus anzuzeigen, können Sie in der Adressleiste auf das Badge klicken.

![Anzeigen des Dokumentmodus über den IE-Modus-Badge](./media/ie-mode-badge-doc-mode.png)

Wenn Sie sich auf einer Registerkarte im IE-Modus befinden, funktioniert der devtools nicht. `F12`Durch Drücken oder `Ctrl` + `Shift` + `I` wird nur eine leere Instanz des Microsoft Edge (Chrom)-devtools mit einer Meldung gestartet, die lautet: "Entwickler Tools sind im Internet Explorer-Modus nicht verfügbar. Um die Seite zu debuggen, öffnen Sie Sie in Internet Explorer 11. " Die **Ansicht Quelle** startet den Editor, und **Inspect-Element** wird im Kontextmenü im IE-Modus nicht angezeigt.

Dies liegt daran, dass eine Reihe von Komponenten im devtools (wie die Netzwerk-und Leistungstools) unterbrechen würden, wenn das Rendering-Modul im IE-Modus von Chrom zu Internet Explorer 11 wechselt. Wenn Sie uns Feedback geben möchten, klicken Sie auf das `:)` Symbol.

![DevTools im IE-Modus gestartet](./media/ie-mode-devtools.png)

Wenn Sie eine Internet Explorer 11-basierte Website oder Anwendung entwickeln oder verwalten, empfehlen wir, in Internet Explorer 11 zur gleichen Seite zu navigieren. Unter Windows 10 können Sie die Verknüpfung für Internet Explorer 11 im Startmenü unter Windows-Zubehör finden. Unter Windows 7 können Sie Internet Explorer 11 im Haupt Startmenü finden. Sie können dann die Internet Explorer-devtools starten, indem Sie `F12` im Kontextmenü auf **Element überprüfen** klicken. Wenn Sie mehr über die Verwendung dieser Tools erfahren möchten, klicken Sie [hier](/previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85)).

## Remote Debuggen und IE-Modus

Sie können Microsoft Edge (Chrom) mit aktiviertem Remotedebuggen starten, und zwar in der Regel wie Tools wie Visual Studio oder vs-Code in der Befehlszeile starten:

`start msedge --remote-debugging-port=9222`

Wenn Microsoft Edge (Chrom) mit diesem Befehlszeilenargument gestartet wird, ist der IE-Modus nicht verfügbar. Sie können weiterhin zu Websites oder Anwendungen navigieren, die sich ansonsten im IE-Modus befinden, aber die Inhalte werden über Chrom gerendert, nicht über Internet Explorer 11. Sie können davon ausgehen, dass die Teile dieser Seiten, die auf IE11 basieren, wie ActiveX-Steuerelemente, nicht richtig gerendert werden. Das Symbol für den IE-Modus wird nicht mehr in der Adressleiste angezeigt.

Der IE-Modus bleibt erst verfügbar, wenn Sie Microsoft Edge (Chrom) vollständig schließen.