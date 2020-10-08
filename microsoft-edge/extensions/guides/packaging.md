---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Erfahren Sie, wie Sie mithilfe von systemeigenem Messaging ihre Erweiterung mit einer Begleit UWP-App kommunizieren können.
title: Erweiterungen – verpacken
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 23c97f366db527cae2672d6ad46fa666583f6398
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567392"
---
# Verpacken von Microsoft-Edge-Erweiterungen  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Sie haben also endlich ihre Erweiterung abgeschlossen und sind bereit, Sie zu verpacken. Sie Fragen sich vielleicht, was die nächsten Schritte sind, um diese in die Hände potenzieller Nutzer zu bringen. In diesem Leitfaden lernen Sie, wie Sie genau das tun.

Der Leitfaden für die Erweiterung der Verpackung ist umfassend, da er alles umfasst, was Sie über Verpackungen wissen möchten, und zwar selbst die feinkörnigen Details. Wenn Sie nicht alles wissen möchten, was Sie über das Verpacken Ihrer Erweiterung wissen sollten, haben Sie Glück. Wir haben die Unterstützung für Erweiterungen zu ManifoldJS hinzugefügt, einem Open-Source-Node.js-Tool, das die meisten ihrer Verpackungen verträgt.

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion. Wenden Sie sich mit Ihren Anforderungen an den Microsoft Store an [uns](https://aka.ms/extension-request) , und wir werden Sie für ein zukünftiges Update in Erwägung ziehen.


Verwenden Sie die nachstehende Prozess Gliederung, um Ihr Verpackungs Abenteuer zu kartieren!


## [Erweiterungen im Windows Dev Center](./packaging/extensions-in-the-windows-dev-center.md)

Unabhängig davon, welche Paket Erstellungs Route Sie manuell oder ManifoldJS auswählen, ist der erste Schritt die Registrierung für ein Windows-Entwicklerkonto und das Reservieren der Namen ihrer Erweiterung.

Nachdem Sie diese Schritte ausgeführt haben, können Sie entweder mit dem [Erstellen und Testen von Erweiterungspaketen](./packaging/creating-and-testing-extension-packages.md) fortfahren, um zu erfahren, wie AppXs erstellt werden und ihre Erweiterung manuell Verpacken, oder die einfachere Route verwenden und zu [ManifoldJS zu Paketerweiterungen](./packaging/using-ManifoldJS-to-package-extensions.md)wechseln.

> [!NOTE]
> Nachdem Sie sich bei uns angemeldet haben und ihre Erweiterung im Microsoft Store genehmigt wurde, lesen Sie die Checkliste für die [App-Übermittlung](https://docs.microsoft.com/windows/uwp/publish/app-submissions).


## [Erstellen und Testen von Erweiterungspaketen](./packaging/creating-and-testing-extension-packages.md)

Dieser Abschnitt des Leitfadens durchläuft die Erstellung manueller Erweiterungen [, nachdem Sie Ihr Windows Developer-Konto eingerichtet und ihre Erweiterungsnamen reserviert haben](./packaging/extensions-in-the-windows-Dev-Center.md). Wenn Sie neugierig auf die feineren Details des Packens einer Erweiterung sind, lesen Sie diesen Artikel.

Darüber hinaus finden Sie Informationen dazu, wie Sie [eine verpackte Erweiterung testen und entpacken](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package)können. Diese Informationen sind auch dann relevant, wenn Sie die ManifoldJS-Verpackungs Route verlassen haben.

## [Lokalisierung von Erweiterungspaketen](./packaging/localizing-extension-packages.md)
Der Paket Lokalisierungs Schritt fällt zwischen dem Erstellen Ihrer appxmanifest.xml Datei und dem Ausführen des letzten Befehls zum Verpacken der Erweiterung.
Auf diese Weise können Sie angeben, welche Sprachen Ihre Erweiterungen in Ihrem Microsoft Store-Eintrag unterstützen, und welche Sprache der Name der Erweiterung in Windows angezeigt wird.

Sie können in diesem Abschnitt des Leitfadens zu [Localize-Name und Beschreibung für den Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) springen, wenn Ihre Erweiterung nicht mehrere Sprachen unterstützt.

## [Verwenden von ManifoldJS zu Paketerweiterungen](./packaging/using-ManifoldJS-to-package-extensions.md)

Die Tool-Route zum Verpacken Ihrer Erweiterung wird ManifoldJS ihre Erweiterung im Handumdrehen mit minimalem Aufwand für ihr Ende verpacken. Stellen Sie nach dem Ausfüllen einiger AppXManifest-Eigenschaften einige Windows/Microsoft Store-Ressourcen bereit, und ihre Erweiterung wird in kürzester Zeit verpackt.

Nachdem Sie Ihre Erweiterung gepackt haben, lesen Sie den Abschnitt [Testen](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) zum Erstellen und Testen Ihrer Microsoft Edge-Erweiterung, um zu erfahren, wie Sie Sie querladen oder entpacken können.


## [Ausführen des Zertifizierungskits für Windows-Apps](./packaging/running-the-windows-app-certification-kit.md)

Sobald Sie über eine verpackte Erweiterung verfügen, können Sie diese über das Windows-App-Zertifizierungs Kit ausführen. Auf diese Weise wird eine Reihe von Tests für Ihr Erweiterungspaket ausgeführt, um sicherzustellen, dass es für den Microsoft Store bereit ist.
