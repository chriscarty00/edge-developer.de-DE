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
# <a name="packaging-microsoft-edge-extensions"></a><span data-ttu-id="eb7ce-104">Packen von Microsoft Edge-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="eb7ce-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="eb7ce-105">Sie haben also ihre Erweiterung abgeschlossen und sind bereit, sie zu packen.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="eb7ce-106">Möglicherweise fragen Sie sich, welche Schritte es als nächstes gibt, um dies potenziellen Benutzern zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="eb7ce-107">In diesem Leitfaden erfahren Sie, wie Sie genau dies tun.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-107">This guide is intended to teach you how to do just that.</span></span>  

<span data-ttu-id="eb7ce-108">Der Leitfaden für die Erweiterungspackung ist umfassend, da er alles umfasst, was Sie über das Verpacken wissen möchten, auch die feinesten, nüchtriensten Details.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="eb7ce-109">Wenn Sie nicht alles wissen möchten, was Sie über das Packen Ihrer Erweiterung wissen müssen, haben Sie Glück.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="eb7ce-110">Wir haben Unterstützung für Erweiterungen zu ManifoldJS hinzugefügt, einem Open Source-Node.js-Tool, das den Großteil Ihrer Verpackungs-Wehe wegnimmt.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>  

> [!NOTE]
> <span data-ttu-id="eb7ce-111">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="eb7ce-112">[Kontaktieren Sie uns mit](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) Ihren Anforderungen, Teil des Microsoft Store zu sein, und wir werden Sie für ein zukünftiges Update in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-112">[Reach out to us](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>  

<span data-ttu-id="eb7ce-113">Verwenden Sie die unten aufgeführte Prozessgliederung, um Ihr Packabenteuer zu zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-113">Use the process outline below to map out your packaging adventure!</span></span>  

## [<a name="extensions-in-the-windows-dev-center"></a><span data-ttu-id="eb7ce-114">Erweiterungen im Windows Dev Center</span><span class="sxs-lookup"><span data-stu-id="eb7ce-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)  

<span data-ttu-id="eb7ce-115">Unabhängig davon, welche Paketerstellungsroute Sie auswählen, manuell oder ManifoldJS, besteht der erste Schritt in der Registrierung für ein Windows Developer-Konto und dem Reservieren der Namen Ihrer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>  

<span data-ttu-id="eb7ce-116">Nachdem Sie dies getan haben, können Sie entweder zu Erstellen und Testen von [Erweiterungspaketen](./packaging/creating-and-testing-extension-packages.md) wechseln, um zu erfahren, wie AppXs erstellt und manuell verpackt werden, oder sie können die einfachere Route gehen und zu [Verwenden von ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md)wechseln.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="eb7ce-117">Sobald Sie uns erreicht haben und ihre Erweiterung im Microsoft Store genehmigt haben, sehen Sie sich die Prüfliste für die [App-Übermittlung an.](https://docs.microsoft.com/windows/uwp/publish/app-submissions)</span><span class="sxs-lookup"><span data-stu-id="eb7ce-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>  


## [<a name="creating-and-testing-extension-packages"></a><span data-ttu-id="eb7ce-118">Erstellen und Testen von Erweiterungspaketen</span><span class="sxs-lookup"><span data-stu-id="eb7ce-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)  

<span data-ttu-id="eb7ce-119">In diesem Abschnitt des Handbuchs wird die manuelle Erstellung von Erweiterungspaketen erläutert, sobald Sie Ihr Windows Developer-Konto eingerichtet und Ihre [Durchwahlnamen reserviert haben.](./packaging/extensions-in-the-windows-Dev-Center.md)</span><span class="sxs-lookup"><span data-stu-id="eb7ce-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="eb7ce-120">Wenn Sie auf die feineren Details des Verpackens einer Erweiterung gespannt sind, lesen Sie dies.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>  

<span data-ttu-id="eb7ce-121">Außerdem sind Informationen zum Testen und Entpacken einer verpackten [Erweiterung enthalten.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package)</span><span class="sxs-lookup"><span data-stu-id="eb7ce-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="eb7ce-122">Diese Informationen sind auch dann relevant, wenn Sie die ManifoldJS-Verpackungsroute gegangen sind.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>  

## [<a name="localizing-extension-packages"></a><span data-ttu-id="eb7ce-123">Lokalisierung von Erweiterungspaketen</span><span class="sxs-lookup"><span data-stu-id="eb7ce-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)  

<span data-ttu-id="eb7ce-124">Der Paketlokalisierungsschritt liegt zwischen dem Erstellen appxmanifest.xml datei und dem Ausführen des letzten Befehls zum Packen Der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>  
<span data-ttu-id="eb7ce-125">Auf diese Weise können Sie angeben, welche Sprachen Ihre Erweiterungen in Ihrem Microsoft Store-Eintrag unterstützen und welche Sprache der Name Ihrer Erweiterung in Windows angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>  

<span data-ttu-id="eb7ce-126">Sie können zu Name und Beschreibung für den [Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) lokalisieren in diesem Abschnitt des Handbuchs wechseln, wenn Ihre Erweiterung nicht mehrere Sprachen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>  

## [<a name="using-manifoldjs-to-package-extensions"></a><span data-ttu-id="eb7ce-127">Verwenden von ManifoldJS zu Paketerweiterungen</span><span class="sxs-lookup"><span data-stu-id="eb7ce-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)  

<span data-ttu-id="eb7ce-128">Die Toolroute zum Packen Ihrer Erweiterung, ManifoldJS, verpackt Ihre Erweiterung mit minimalem Aufwand am Ende.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="eb7ce-129">Stellen Sie nach dem Ausfüllen einiger AppXManifest-Eigenschaften einige Windows-/Microsoft Store-Ressourcen zur Verfügung, und Ihre Erweiterung wird in einem handfesten Paket verpackt.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>  

<span data-ttu-id="eb7ce-130">Sobald Ihre Erweiterung gepackt [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) wurde, lesen Sie den Testabschnitt Erstellen und Testen Ihrer Microsoft Edge-Erweiterung, um zu erfahren, wie Sie sie querladen oder entpacken.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>  

## [<a name="running-the-windows-app-certification-kit"></a><span data-ttu-id="eb7ce-131">Ausführen des Zertifizierungskits für Windows-Apps</span><span class="sxs-lookup"><span data-stu-id="eb7ce-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)  

<span data-ttu-id="eb7ce-132">Sobald Sie über eine verpackte Erweiterung verfügen, können Sie sie über das Zertifizierungskit für Windows-Apps ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="eb7ce-133">Dadurch werden eine Reihe von Tests für Ihr Erweiterungspaket ausgeführt, um sicherzustellen, dass es für den Microsoft Store bereit ist.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>  
