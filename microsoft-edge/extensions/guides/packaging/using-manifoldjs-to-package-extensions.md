---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Hier erfahren Sie, wie Sie Ihre Microsoft Edge-Erweiterung mit ManifoldJS, dem Node.js Open-Source-Tool, im Handumdrehen verpacken.
title: Verwenden von ManifoldJS zu Paketerweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.openlocfilehash: 83aa57ae0e4ae302b1360be50e5158782b6fbb76
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986206"
---
# Verwenden von ManifoldJS zum Erstellen von Erweiterungs AppX-Paketen  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS ist ein Open-Source-Node.js-Tool, mit dem Sie schnell und problemlos ein Paket erstellen können, das Sie dann für die Übermittlung an den Microsoft Store verwenden können.  

Wenn Sie in ihrer Erweiterung systemeigenes Messaging verwenden, sollten Sie den folgenden Artikel überspringen und zu [systemeigener Nachrichten in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) für Verpackungsanweisungen wechseln.  

Bevor Sie beginnen, müssen Sie sich weiterhin mit den folgenden Artikeln vertraut machen.  

*   [Erweiterungen im Windows Dev Center](./extensions-in-the-windows-dev-center.md)  
*   [Lokalisierung von Erweiterungspaketen](./localizing-extension-packages.md)  

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.  Nachdem Sie Ihre Erweiterung erstellt, verpackt und getestet haben, senden Sie uns bitte eine Anfrage über unser [Extension-Übermittlungsformular](https://developer.microsoft.com/microsoft-edge/extensions/requests).  

## Installieren von Node.js und ManifoldJS  

Das erste, was Sie tun müssen, ist [Node.js LTS](https://nodejs.org/en/download)zu installieren.  
Nachdem Sie über eine Befehlszeile (vorzugsweise PowerShell) über einen Knoten verfügen, führen Sie den folgenden Befehl aus, um ManifoldJS zu installieren.  

```shell
npm install -g manifoldjs
```  

Um zu überprüfen, ob Sie ManifoldJS ordnungsgemäß installiert haben, führen Sie `manifoldjs` über die Befehlszeile aus. Wenn ManifoldJS nicht erkannt wurde, fügen Sie `%APPDATA%\npm` Ihre PATH-Variablen hinzu.  

## Verpacken mit ManifoldJS  

Um den Verpackungsprozess zu starten, müssen Sie eine Befehlszeile öffnen und Verzeichnisse in einen Ordner ändern, der das Ziel für Ihre verpackte Erweiterung ist.  

Zum Beispiel:

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> Der `manifoldjs` Befehl wird im aktuellen Verzeichnis ausgegeben, und der Inhalt wird überschrieben.  

Nachdem Sie sich nun im Zielordner befinden, führen Sie den folgenden Befehl aus.  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

Der `mainifoldjs` Befehl kann in die folgenden Abschnitte unterteilt werden.  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      Ändert die Protokollebene, um `debug` einen vollständigen Ausdruck zu erhalten.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      Legt die einzige Plattform fest, auf die die Konvertierung ausgeführt werden soll `edgeextension` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      Weist das Programm darauf hin, dass das Format des Manifests ein `edgeextension` Format ist und nicht zu beachten ist, wenn die Validierung fehlschlägt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      Der Pfad des Erweiterungs Manifests, das Sie konvertieren möchten.  
   :::column-end:::
:::row-end:::  

Nachdem ManifoldJS ausgeführt wurde, verfügen Sie über einen Ordner mit den folgenden Inhalten.  

```text
┌ My Extension
└┬ edgeextension
 ├- generationInfo.json
 └┬ manifest
  ├- appxmanifest.xml
  ├┬ Assets
  |├- Square150x150Logo.png
  |├- Square44x44Logo.png
  |└- StoreLogo.png    
  └┬ Extension
   ├- manifest.json
   └- popup.html
```  
<!-- 
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
-->  

Bei der Datei generationInfo.jshandelt es sich um ein Protokoll, das durch Ausführen von ManifoldJS erstellt wird und nicht in Ihrem Erweiterungspaket enthalten ist. Nur der Inhalt des `manifest` Ordners wird gepackt. Innerhalb des Manifest-Ordners enthält der Ordner "Objekte" die Bilder, die in der Windows-und Microsoft Store-Benutzeroberfläche verwendet werden, während der Ordner "Extension" den Inhalt ihrer Erweiterung enthält.  

Nachdem Sie nun über die richtigen Dateien verfügen, müssen Sie die generierte AppXManifest-Datei innerhalb des `manifest` Ordners bearbeiten. Wenn die manifest.jsder Erweiterung für die Datei eine Internationalisierungs Zeichenfolge für das Feld "Name" enthält, wird der Name des obersten Layer-Ordners nach der Ausführung von ManifoldJS nicht unterstrichen und "msg" enthalten.

Beispiel: eine Datei mit dem folgenden `"name"` Feld manifest.js.  

```shell
"name" : "__MSG_appName__"
```  

hat einen Manifest-Ordner, in dem sich die Datei befindet `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .  

In der AppXManifest-Datei müssen Sie Folgendes ausführen:  

 *   Ersetzen Sie das Feld erforderliche Identitätsfelder und PublisherDisplayName wie [hier](./creating-and-testing-extension-packages.md#app-identity-template-values)beschrieben. Beachten Sie, dass Sie, wenn Sie nur zu Testzwecken oder für die Unternehmens Verteilung zu verpacken sind, Platzhalterwerte anstelle der Registrierung für ein Windows dev Center-Konto verwenden können.  
 *   Ersetzen Sie die Platzhaltersymbole im Ordner "Objekte" durch Symbole für Ihre Erweiterung mit den gleichen Größen (150x150, 50x50, 44x44) und Namen. Informationen dazu, wo diese Symbole verwendet werden, finden Sie im [Design](./../design.md#icons-for-packaging) Handbuch.  
 *   Wenn Ihre Erweiterung lokalisiert ist, folgen Sie dem gesamten Leitfaden zur [Lokalisierung von Microsoft-Edge-Erweiterungen](./localizing-extension-packages.md) . Wenn Sie nicht lokalisiert ist, lesen Sie nur den [Namen und die Beschreibung der Lokalisierung im Abschnitt Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .  

Nachdem die `appxmanifest.xml` Datei aussortiert wurde, führen Sie den folgenden Befehl aus, um Ihr Paket zu erstellen.  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

Ihr Paket befindet sich nun im **Paket** Ordner im Ordner edgeextension. Weitere Informationen zum querladen des neuen Pakets finden Sie unter [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) -Abschnitt zum Erstellen und Testen von Erweiterungspaketen.  

Nachdem Ihr Paket getestet wurde, können Sie eine Anfrage über unser [Extension-Übermittlungsformular](https://aka.ms/extension-request) einreichen, um für die Veröffentlichung im Microsoft Store in Frage zu kommen.  
