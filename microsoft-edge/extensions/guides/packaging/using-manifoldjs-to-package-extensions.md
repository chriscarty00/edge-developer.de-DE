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
# <span data-ttu-id="cfec0-104">Verwenden von ManifoldJS zum Erstellen von Erweiterungs AppX-Paketen</span><span class="sxs-lookup"><span data-stu-id="cfec0-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="cfec0-105">ManifoldJS ist ein Open-Source-Knoten. js-Tool, mit dem Sie schnell und problemlos ein Paket erstellen können, das Sie dann für die Übermittlung an den Microsoft Store verwenden können.</span><span class="sxs-lookup"><span data-stu-id="cfec0-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>

<span data-ttu-id="cfec0-106">Wenn Sie in ihrer Erweiterung systemeigenes Messaging verwenden, sollten Sie dies überspringen und zu [systemeigener Nachrichten in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) für Verpackungsanweisungen wechseln.</span><span class="sxs-lookup"><span data-stu-id="cfec0-106">If you use native messaging in your extension, you should skip this and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span> 

<span data-ttu-id="cfec0-107">Bevor Sie beginnen, müssen Sie sich weiterhin mit den folgenden Artikeln vertraut machen:</span><span class="sxs-lookup"><span data-stu-id="cfec0-107">Before getting started, you will still need to read up on the following articles:</span></span>

- [<span data-ttu-id="cfec0-108">Erweiterungen im Windows dev Center</span><span class="sxs-lookup"><span data-stu-id="cfec0-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)
- [<span data-ttu-id="cfec0-109">Localize-Erweiterungspakete</span><span class="sxs-lookup"><span data-stu-id="cfec0-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)

> [!NOTE]
> <span data-ttu-id="cfec0-110">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="cfec0-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="cfec0-111">Nachdem Sie Ihre Erweiterung erstellt, verpackt und getestet haben, senden Sie uns bitte eine Anfrage über unser [Extension-Übermittlungsformular](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="cfec0-111">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>


## <span data-ttu-id="cfec0-112">Installieren von Node. js und ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="cfec0-112">Installing Node.js and ManifoldJS</span></span>

<span data-ttu-id="cfec0-113">Als erstes müssen Sie [node. js LTS](https://nodejs.org/en/download/)installieren.</span><span class="sxs-lookup"><span data-stu-id="cfec0-113">The first things you'll need to do is install [Node.js LTS](https://nodejs.org/en/download/).</span></span>
<span data-ttu-id="cfec0-114">Nachdem Sie über eine Befehlszeile (vorzugsweise PowerShell) über einen Knoten verfügen, führen Sie den folgenden Befehl aus, um ManifoldJS zu installieren:</span><span class="sxs-lookup"><span data-stu-id="cfec0-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS:</span></span>

`npm install -g manifoldjs`

<span data-ttu-id="cfec0-115">Um zu überprüfen, ob Sie ManifoldJS ordnungsgemäß installiert haben, führen Sie `manifoldjs` über die Befehlszeile aus.</span><span class="sxs-lookup"><span data-stu-id="cfec0-115">To verify that you've correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="cfec0-116">Wenn ManifoldJS nicht erkannt wurde, fügen Sie `%APPDATA%\npm` Ihre PATH-Variablen hinzu.</span><span class="sxs-lookup"><span data-stu-id="cfec0-116">If ManifoldJS wasn't recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>

## <span data-ttu-id="cfec0-117">Verpacken mit ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="cfec0-117">Packaging with ManifoldJS</span></span>

<span data-ttu-id="cfec0-118">Um den Verpackungsprozess zu starten, müssen Sie eine Befehlszeile öffnen und Verzeichnisse in einen Ordner ändern, der das Ziel für Ihre verpackte Erweiterung ist.</span><span class="sxs-lookup"><span data-stu-id="cfec0-118">To start the packaging process, you'll need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>

<span data-ttu-id="cfec0-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cfec0-119">For example:</span></span>

`cd C:\manifoldJSTest`

> [!NOTE]
> <span data-ttu-id="cfec0-120">ManifoldJS wird im aktuellen Verzeichnis ausgegeben und kann Inhalt überschreiben.</span><span class="sxs-lookup"><span data-stu-id="cfec0-120">ManifoldJS will output in the current directory and can overwrite content.</span></span>



<span data-ttu-id="cfec0-121">Nachdem Sie sich nun im Zielordner befinden, führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="cfec0-121">Now that you're in your destination folder, run the following command:</span></span>

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


<span data-ttu-id="cfec0-122">Dieser Befehl kann in die folgenden Abschnitte unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="cfec0-122">This command can be broken down into the following parts:</span></span>
 -    <span data-ttu-id="cfec0-123">**-l Debug**: ändert die Protokollebene in "Debug", um einen vollständigen Ausdruck zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cfec0-123">**-l debug**: Changes the log level to "debug" to get a full print out.</span></span>
 -    <span data-ttu-id="cfec0-124">**-p edgeextension**: legt die einzige Plattform zum Ausführen der Konvertierung auf edgeextension fest.</span><span class="sxs-lookup"><span data-stu-id="cfec0-124">**-p edgeextension**: Sets the only platform to run the conversion on to edgeextension.</span></span>
 -    <span data-ttu-id="cfec0-125">**-f edgeextension**: teilt dem Programm mit, dass das Format des Manifests ein edgeextension-Format ist und nicht zu beachten ist, wenn die Validierung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="cfec0-125">**-f edgeextension**: Tells the program that the format of the manifest is an edgeextension format and not to care if it fails validation.</span></span>
 -    <span data-ttu-id="cfec0-126">**-m \ < Extension Location > \manifest.JSON**: der Pfad zu dem Erweiterungs Manifest, das Sie konvertieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cfec0-126">**-m \<EXTENSION LOCATION>\manifest.json**: The path to the extension manifest that you want to convert.</span></span>


<span data-ttu-id="cfec0-127">Nachdem ManifoldJS ausgeführt wurde, haben Sie einen Ordner mit folgendem Inhalt:</span><span class="sxs-lookup"><span data-stu-id="cfec0-127">After ManifoldJS has finished running, you'll have a folder with the following contents:</span></span>

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

<span data-ttu-id="cfec0-128">Bei der generationInfo. JSON-Datei handelt es sich um ein vom Ausführen von ManifoldJS erstelltes Protokoll, das nicht in Ihrem Erweiterungspaket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cfec0-128">The generationInfo.json file is a log produced by running ManifoldJS and won't be included in your extension package.</span></span> <span data-ttu-id="cfec0-129">Nur der Inhalt des **Manifest** -Ordners wird gepackt.</span><span class="sxs-lookup"><span data-stu-id="cfec0-129">Only the contents of the **manifest** folder will be packaged.</span></span> <span data-ttu-id="cfec0-130">Innerhalb des Manifest-Ordners enthält der Ordner "Objekte" die Bilder, die in der Windows-und Microsoft Store-Benutzeroberfläche verwendet werden, während der Ordner "Extension" den Inhalt ihrer Erweiterung enthält.</span><span class="sxs-lookup"><span data-stu-id="cfec0-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>


<span data-ttu-id="cfec0-131">Nachdem Sie nun über die richtigen Dateien verfügen, müssen Sie die generierte AppXManifest-Datei innerhalb des **Manifest** -Ordners bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="cfec0-131">Now that you have the correct files, you'll need to edit the generated AppXManifest file within the **manifest** folder.</span></span> <span data-ttu-id="cfec0-132">Wenn die Manifest. JSON-Datei der Erweiterung für das Feld "Name" eine Internationalisierungs Zeichenfolge enthält, wird der Name des obersten Layer-Ordners nach der Ausführung von ManifoldJS nicht unterstrichen und "msg" enthalten.</span><span class="sxs-lookup"><span data-stu-id="cfec0-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="cfec0-133">Beispielsweise eine Manifest. JSON-Datei mit dem folgenden `"name"` Feld:</span><span class="sxs-lookup"><span data-stu-id="cfec0-133">For example, a manifest.json file with the following `"name"` field:</span></span>

`"name" : "__MSG_appName__"`

<span data-ttu-id="cfec0-134">hat einen Manifest-Ordner, in dem sich die Datei befindet `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="cfec0-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>

<span data-ttu-id="cfec0-135">In der AppXManifest-Datei müssen Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="cfec0-135">In the AppXManifest file, you'll need to:</span></span>
 -    <span data-ttu-id="cfec0-136">Ersetzen Sie das Feld erforderliche Identitätsfelder und PublisherDisplayName wie [hier](./creating-and-testing-extension-packages.md#app-identity-template-values)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cfec0-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="cfec0-137">Beachten Sie, dass Sie Platzhalterwerte anstelle der Registrierung für ein Windows dev Center-Konto verwenden können, wenn Sie nur zu Testzwecken oder für die Unternehmens Verteilung verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="cfec0-137">Note that if you're only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>
 -    <span data-ttu-id="cfec0-138">Ersetzen Sie die Platzhaltersymbole im Ordner "Objekte" durch Symbole für Ihre Erweiterung mit den gleichen Größen (150x150, 50x50, 44x44) und Namen.</span><span class="sxs-lookup"><span data-stu-id="cfec0-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="cfec0-139">Informationen dazu, wo diese Symbole verwendet werden, finden Sie im [Design](./../design.md#icons-for-packaging) Handbuch.</span><span class="sxs-lookup"><span data-stu-id="cfec0-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>
 - <span data-ttu-id="cfec0-140">Wenn Ihre Erweiterung lokalisiert ist, folgen Sie dem gesamten Leitfaden zur [Lokalisierung von Microsoft-Edge-Erweiterungen](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="cfec0-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="cfec0-141">Wenn Sie nicht lokalisiert ist, lesen Sie [im Abschnitt Microsoft Store nur den Namen und die Beschreibung der Lokalisierung](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="cfec0-141">If it isn't localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>

<span data-ttu-id="cfec0-142">Nachdem die Datei "appxmanifest. xml" aussortiert wurde, führen Sie den folgenden Befehl aus, um Ihr Paket zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="cfec0-142">Once your appxmanifest.xml file is sorted out, run the following command to create your package:</span></span>

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

<span data-ttu-id="cfec0-143">Ihr Paket befindet sich nun im **Paket** Ordner im Ordner edgeextension.</span><span class="sxs-lookup"><span data-stu-id="cfec0-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="cfec0-144">Informationen zum querladen des neuen Pakets finden Sie unter Erstellen und Testen des [Test](./creating-and-testing-extension-packages.md#testing-an-appx-package) Abschnitts für Erweiterungspakete.</span><span class="sxs-lookup"><span data-stu-id="cfec0-144">See Creating and testing extension packages' [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section for info on how to sideload your new package.</span></span>

<span data-ttu-id="cfec0-145">Nachdem Ihr Paket getestet wurde, können Sie eine Anfrage über unser [Extension-Übermittlungsformular](https://aka.ms/extension-request) einreichen, um für die Veröffentlichung im Microsoft Store in Frage zu kommen.</span><span class="sxs-lookup"><span data-stu-id="cfec0-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>
