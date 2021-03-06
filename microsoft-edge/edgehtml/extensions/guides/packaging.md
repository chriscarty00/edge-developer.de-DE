---
description: Erfahren Sie, wie Sie Ihre Erweiterung packen können.
title: Erweiterungen – Verpacken
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
keywords: edge, web development, html, css, javascript, developer
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62c7858c38cf0c06e24c25938a885b10b391fd8f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398497"
---
# <a name="packaging-microsoft-edge-extensions"></a>Packen von Microsoft Edge-Erweiterungen  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Sie haben also ihre Erweiterung abgeschlossen und sind bereit, sie zu packen. Möglicherweise fragen Sie sich, welche Schritte es als nächstes gibt, um dies potenziellen Benutzern zu ermöglichen. In diesem Leitfaden erfahren Sie, wie Sie genau dies tun.  

Der Leitfaden für die Erweiterungspackung ist umfassend, da er alles umfasst, was Sie über das Verpacken wissen möchten, auch die feinesten, nüchtriensten Details. Wenn Sie nicht alles wissen möchten, was Sie über das Packen Ihrer Erweiterung wissen müssen, haben Sie Glück. Wir haben Unterstützung für Erweiterungen zu ManifoldJS hinzugefügt, einem Open Source-Node.js-Tool, das den Großteil Ihrer Verpackungs-Wehe wegnimmt.  

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion. [Kontaktieren Sie uns mit](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) Ihren Anforderungen, Teil des Microsoft Store zu sein, und wir werden Sie für ein zukünftiges Update in Betracht ziehen.  

Verwenden Sie die unten aufgeführte Prozessgliederung, um Ihr Packabenteuer zu zuordnungen.  

## [<a name="extensions-in-the-windows-dev-center"></a>Erweiterungen im Windows Dev Center](./packaging/extensions-in-the-windows-dev-center.md)  

Unabhängig davon, welche Paketerstellungsroute Sie auswählen, manuell oder ManifoldJS, besteht der erste Schritt in der Registrierung für ein Windows Developer-Konto und dem Reservieren der Namen Ihrer Erweiterung.  

Nachdem Sie dies getan haben, können Sie entweder zu Erstellen und Testen von [Erweiterungspaketen](./packaging/creating-and-testing-extension-packages.md) wechseln, um zu erfahren, wie AppXs erstellt und manuell verpackt werden, oder sie können die einfachere Route gehen und zu [Verwenden von ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md)wechseln.  

> [!NOTE]
> Sobald Sie uns erreicht haben und ihre Erweiterung im Microsoft Store genehmigt haben, sehen Sie sich die Prüfliste für die [App-Übermittlung an.](https://docs.microsoft.com/windows/uwp/publish/app-submissions)  


## [<a name="creating-and-testing-extension-packages"></a>Erstellen und Testen von Erweiterungspaketen](./packaging/creating-and-testing-extension-packages.md)  

In diesem Abschnitt des Handbuchs wird die manuelle Erstellung von Erweiterungspaketen erläutert, sobald Sie Ihr Windows Developer-Konto eingerichtet und Ihre [Durchwahlnamen reserviert haben.](./packaging/extensions-in-the-windows-Dev-Center.md) Wenn Sie auf die feineren Details des Verpackens einer Erweiterung gespannt sind, lesen Sie dies.  

Außerdem sind Informationen zum Testen und Entpacken einer verpackten [Erweiterung enthalten.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) Diese Informationen sind auch dann relevant, wenn Sie die ManifoldJS-Verpackungsroute gegangen sind.  

## [<a name="localizing-extension-packages"></a>Lokalisierung von Erweiterungspaketen](./packaging/localizing-extension-packages.md)  

Der Paketlokalisierungsschritt liegt zwischen dem Erstellen appxmanifest.xml datei und dem Ausführen des letzten Befehls zum Packen Der Erweiterung.  
Auf diese Weise können Sie angeben, welche Sprachen Ihre Erweiterungen in Ihrem Microsoft Store-Eintrag unterstützen und welche Sprache der Name Ihrer Erweiterung in Windows angezeigt wird.  

Sie können zu Name und Beschreibung für den [Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) lokalisieren in diesem Abschnitt des Handbuchs wechseln, wenn Ihre Erweiterung nicht mehrere Sprachen unterstützt.  

## [<a name="using-manifoldjs-to-package-extensions"></a>Verwenden von ManifoldJS zu Paketerweiterungen](./packaging/using-ManifoldJS-to-package-extensions.md)  

Die Toolroute zum Packen Ihrer Erweiterung, ManifoldJS, verpackt Ihre Erweiterung mit minimalem Aufwand am Ende. Stellen Sie nach dem Ausfüllen einiger AppXManifest-Eigenschaften einige Windows-/Microsoft Store-Ressourcen zur Verfügung, und Ihre Erweiterung wird in einem handfesten Paket verpackt.  

Sobald Ihre Erweiterung gepackt [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) wurde, lesen Sie den Testabschnitt Erstellen und Testen Ihrer Microsoft Edge-Erweiterung, um zu erfahren, wie Sie sie querladen oder entpacken.  

## [<a name="running-the-windows-app-certification-kit"></a>Ausführen des Zertifizierungskits für Windows-Apps](./packaging/running-the-windows-app-certification-kit.md)  

Sobald Sie über eine verpackte Erweiterung verfügen, können Sie sie über das Zertifizierungskit für Windows-Apps ausführen. Dadurch werden eine Reihe von Tests für Ihr Erweiterungspaket ausgeführt, um sicherzustellen, dass es für den Microsoft Store bereit ist.  
