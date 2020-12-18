---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Hier erfahren Sie, wie Sie Ihre Microsoft Edge-Erweiterung mit ManifoldJS, dem Node.js Open-Source-Tool, im Handumdrehen verpacken.
title: Verwenden von ManifoldJS zu Paketerweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 151a8b2ababb25e0964a6fbc2696b5fdc059d084
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234145"
---
# <span data-ttu-id="0a9bf-104">Verwenden von ManifoldJS zum Erstellen von Erweiterungs AppX-Paketen</span><span class="sxs-lookup"><span data-stu-id="0a9bf-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="0a9bf-105">ManifoldJS ist ein Open-Source-Node.js-Tool, mit dem Sie schnell und problemlos ein Paket erstellen können, das Sie dann für die Übermittlung an den Microsoft Store verwenden können.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>  

<span data-ttu-id="0a9bf-106">Wenn Sie in ihrer Erweiterung systemeigenes Messaging verwenden, sollten Sie den folgenden Artikel überspringen und zu [systemeigener Nachrichten in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) für Verpackungsanweisungen wechseln.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-106">If you use native messaging in your extension, you should skip the following article and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span>  

<span data-ttu-id="0a9bf-107">Bevor Sie beginnen, müssen Sie sich weiterhin mit den folgenden Artikeln vertraut machen.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-107">Before getting started, you will still need to read up on the following articles.</span></span>  

*   [<span data-ttu-id="0a9bf-108">Erweiterungen im Windows Dev Center</span><span class="sxs-lookup"><span data-stu-id="0a9bf-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)  
*   [<span data-ttu-id="0a9bf-109">Lokalisierung von Erweiterungspaketen</span><span class="sxs-lookup"><span data-stu-id="0a9bf-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)  

> [!NOTE]
> <span data-ttu-id="0a9bf-110">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="0a9bf-111">Nachdem Sie Ihre Erweiterung erstellt, verpackt und getestet haben, senden Sie uns bitte eine Anfrage über unser [Extension-Übermittlungsformular](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span><span class="sxs-lookup"><span data-stu-id="0a9bf-111">Once you have created, packaged and tested your extension, please submit a request on our [extension submission form](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span></span>  

## <span data-ttu-id="0a9bf-112">Installieren von Node.js und ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="0a9bf-112">Installing Node.js and ManifoldJS</span></span>  

<span data-ttu-id="0a9bf-113">Das erste, was Sie tun müssen, ist [Node.js LTS](https://nodejs.org/en/download)zu installieren.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-113">The first things you will need to do is install [Node.js LTS](https://nodejs.org/en/download).</span></span>  
<span data-ttu-id="0a9bf-114">Nachdem Sie über eine Befehlszeile (vorzugsweise PowerShell) über einen Knoten verfügen, führen Sie den folgenden Befehl aus, um ManifoldJS zu installieren.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS.</span></span>  

```shell
npm install -g manifoldjs
```  

<span data-ttu-id="0a9bf-115">Um zu überprüfen, ob Sie ManifoldJS ordnungsgemäß installiert haben, führen Sie `manifoldjs` über die Befehlszeile aus.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-115">To verify that you have correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="0a9bf-116">Wenn ManifoldJS nicht erkannt wurde, fügen Sie `%APPDATA%\npm` Ihre PATH-Variablen hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-116">If ManifoldJS was not recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>  

## <span data-ttu-id="0a9bf-117">Verpacken mit ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="0a9bf-117">Packaging with ManifoldJS</span></span>  

<span data-ttu-id="0a9bf-118">Um den Verpackungsprozess zu starten, müssen Sie eine Befehlszeile öffnen und Verzeichnisse in einen Ordner ändern, der das Ziel für Ihre verpackte Erweiterung ist.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-118">To start the packaging process, you will need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>  

<span data-ttu-id="0a9bf-119">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0a9bf-119">For example:</span></span>

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> <span data-ttu-id="0a9bf-120">Der `manifoldjs` Befehl wird im aktuellen Verzeichnis ausgegeben, und der Inhalt wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-120">The `manifoldjs` command outputs in the current directory and overwrites content.</span></span>  

<span data-ttu-id="0a9bf-121">Nachdem Sie sich nun im Zielordner befinden, führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-121">Now that you are in your destination folder, run the following command.</span></span>  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

<span data-ttu-id="0a9bf-122">Der `mainifoldjs` Befehl kann in die folgenden Abschnitte unterteilt werden.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-122">The `mainifoldjs` command can be broken down into the following parts.</span></span>  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="0a9bf-123">Ändert die Protokollebene, um `debug` einen vollständigen Ausdruck zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-123">Changes the log level to `debug` to get a full print out.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="0a9bf-124">Legt die einzige Plattform fest, auf die die Konvertierung ausgeführt werden soll `edgeextension` .</span><span class="sxs-lookup"><span data-stu-id="0a9bf-124">Sets the only platform to run the conversion on to `edgeextension`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="0a9bf-125">Weist das Programm darauf hin, dass das Format des Manifests ein `edgeextension` Format ist und nicht zu beachten ist, wenn die Validierung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-125">Tells the program that the format of the manifest is an `edgeextension` format and not to care if it fails validation.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="0a9bf-126">Der Pfad des Erweiterungs Manifests, das Sie konvertieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-126">The path to the extension manifest that you want to convert.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="0a9bf-127">Nachdem ManifoldJS ausgeführt wurde, verfügen Sie über einen Ordner mit den folgenden Inhalten.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-127">After ManifoldJS has finished running, you will have a folder with the following contents.</span></span>  

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

<span data-ttu-id="0a9bf-128">Bei der Datei generationInfo.jshandelt es sich um ein Protokoll, das durch Ausführen von ManifoldJS erstellt wird und nicht in Ihrem Erweiterungspaket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-128">The generationInfo.json file is a log produced by running ManifoldJS and will not be included in your extension package.</span></span> <span data-ttu-id="0a9bf-129">Nur der Inhalt des `manifest` Ordners wird gepackt.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-129">Only the contents of the `manifest` folder will be packaged.</span></span> <span data-ttu-id="0a9bf-130">Innerhalb des Manifest-Ordners enthält der Ordner "Objekte" die Bilder, die in der Windows-und Microsoft Store-Benutzeroberfläche verwendet werden, während der Ordner "Extension" den Inhalt ihrer Erweiterung enthält.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>  

<span data-ttu-id="0a9bf-131">Nachdem Sie nun über die richtigen Dateien verfügen, müssen Sie die generierte AppXManifest-Datei innerhalb des `manifest` Ordners bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-131">Now that you have the correct files, you will need to edit the generated AppXManifest file within the `manifest` folder.</span></span> <span data-ttu-id="0a9bf-132">Wenn die manifest.jsder Erweiterung für die Datei eine Internationalisierungs Zeichenfolge für das Feld "Name" enthält, wird der Name des obersten Layer-Ordners nach der Ausführung von ManifoldJS nicht unterstrichen und "msg" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="0a9bf-133">Beispiel: eine Datei mit dem folgenden `"name"` Feld manifest.js.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-133">For example, a manifest.json file with the following `"name"` field.</span></span>  

```shell
"name" : "__MSG_appName__"
```  

<span data-ttu-id="0a9bf-134">hat einen Manifest-Ordner, in dem sich die Datei befindet `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="0a9bf-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>  

<span data-ttu-id="0a9bf-135">In der AppXManifest-Datei müssen Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="0a9bf-135">In the AppXManifest file, you will need to:</span></span>  

 *   <span data-ttu-id="0a9bf-136">Ersetzen Sie das Feld erforderliche Identitätsfelder und PublisherDisplayName wie [hier](./creating-and-testing-extension-packages.md#app-identity-template-values)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="0a9bf-137">Beachten Sie, dass Sie, wenn Sie nur zu Testzwecken oder für die Unternehmens Verteilung zu verpacken sind, Platzhalterwerte anstelle der Registrierung für ein Windows dev Center-Konto verwenden können.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-137">Note that if you are only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>  
 *   <span data-ttu-id="0a9bf-138">Ersetzen Sie die Platzhaltersymbole im Ordner "Objekte" durch Symbole für Ihre Erweiterung mit den gleichen Größen (150x150, 50x50, 44x44) und Namen.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="0a9bf-139">Informationen dazu, wo diese Symbole verwendet werden, finden Sie im [Design](./../design.md#icons-for-packaging) Handbuch.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>  
 *   <span data-ttu-id="0a9bf-140">Wenn Ihre Erweiterung lokalisiert ist, folgen Sie dem gesamten Leitfaden zur [Lokalisierung von Microsoft-Edge-Erweiterungen](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="0a9bf-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="0a9bf-141">Wenn Sie nicht lokalisiert ist, lesen Sie nur den [Namen und die Beschreibung der Lokalisierung im Abschnitt Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="0a9bf-141">If it is not localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>  

<span data-ttu-id="0a9bf-142">Nachdem die `appxmanifest.xml` Datei aussortiert wurde, führen Sie den folgenden Befehl aus, um Ihr Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-142">Once your `appxmanifest.xml` file is sorted out, run the following command to create your package.</span></span>  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

<span data-ttu-id="0a9bf-143">Ihr Paket befindet sich nun im **Paket** Ordner im Ordner edgeextension.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="0a9bf-144">Weitere Informationen zum querladen des neuen Pakets finden Sie unter [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) -Abschnitt zum Erstellen und Testen von Erweiterungspaketen.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-144">For more information about how to sideload your new package, see [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing extension packages.</span></span>  

<span data-ttu-id="0a9bf-145">Nachdem Ihr Paket getestet wurde, können Sie eine Anfrage über unser [Extension-Übermittlungsformular](https://aka.ms/extension-request) einreichen, um für die Veröffentlichung im Microsoft Store in Frage zu kommen.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>  
