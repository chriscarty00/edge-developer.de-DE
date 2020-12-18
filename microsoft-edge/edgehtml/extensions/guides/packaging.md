---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Hier erfahren Sie, wie Sie Ihre Erweiterung verpacken.
title: Erweiterungen – verpacken
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ea4d6a4450d47d116164fd8481fdfb0f79bd30b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234168"
---
# <span data-ttu-id="10b7a-104">Verpacken von Microsoft-Edge-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="10b7a-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="10b7a-105">Sie haben also endlich ihre Erweiterung abgeschlossen und sind bereit, Sie zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="10b7a-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="10b7a-106">Sie Fragen sich vielleicht, was die nächsten Schritte sind, um diese in die Hände potenzieller Nutzer zu bringen.</span><span class="sxs-lookup"><span data-stu-id="10b7a-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="10b7a-107">In diesem Leitfaden lernen Sie, wie Sie genau das tun.</span><span class="sxs-lookup"><span data-stu-id="10b7a-107">This guide is intended to teach you how to do just that.</span></span>

<span data-ttu-id="10b7a-108">Der Leitfaden für die Erweiterung der Verpackung ist umfassend, da er alles umfasst, was Sie über Verpackungen wissen möchten, und zwar selbst die feinkörnigen Details.</span><span class="sxs-lookup"><span data-stu-id="10b7a-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="10b7a-109">Wenn Sie nicht alles wissen möchten, was Sie über das Verpacken Ihrer Erweiterung wissen sollten, haben Sie Glück.</span><span class="sxs-lookup"><span data-stu-id="10b7a-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="10b7a-110">Wir haben die Unterstützung für Erweiterungen zu ManifoldJS hinzugefügt, einem Open-Source-Node.js-Tool, das die meisten ihrer Verpackungen verträgt.</span><span class="sxs-lookup"><span data-stu-id="10b7a-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>

> [!NOTE]
> <span data-ttu-id="10b7a-111">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="10b7a-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="10b7a-112">Wenden Sie sich mit Ihren Anforderungen an den Microsoft Store an [uns](https://aka.ms/extension-request) , und wir werden Sie für ein zukünftiges Update in Erwägung ziehen.</span><span class="sxs-lookup"><span data-stu-id="10b7a-112">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>


<span data-ttu-id="10b7a-113">Verwenden Sie die nachstehende Prozess Gliederung, um Ihr Verpackungs Abenteuer zu kartieren!</span><span class="sxs-lookup"><span data-stu-id="10b7a-113">Use the process outline below to map out your packaging adventure!</span></span>


## [<span data-ttu-id="10b7a-114">Erweiterungen im Windows Dev Center</span><span class="sxs-lookup"><span data-stu-id="10b7a-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)

<span data-ttu-id="10b7a-115">Unabhängig davon, welche Paket Erstellungs Route Sie manuell oder ManifoldJS auswählen, ist der erste Schritt die Registrierung für ein Windows-Entwicklerkonto und das Reservieren der Namen ihrer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="10b7a-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>

<span data-ttu-id="10b7a-116">Nachdem Sie diese Schritte ausgeführt haben, können Sie entweder mit dem [Erstellen und Testen von Erweiterungspaketen](./packaging/creating-and-testing-extension-packages.md) fortfahren, um zu erfahren, wie AppXs erstellt werden und ihre Erweiterung manuell Verpacken, oder die einfachere Route verwenden und zu [ManifoldJS zu Paketerweiterungen](./packaging/using-ManifoldJS-to-package-extensions.md)wechseln.</span><span class="sxs-lookup"><span data-stu-id="10b7a-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="10b7a-117">Nachdem Sie sich bei uns angemeldet haben und ihre Erweiterung im Microsoft Store genehmigt wurde, lesen Sie die Checkliste für die [App-Übermittlung](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span><span class="sxs-lookup"><span data-stu-id="10b7a-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>


## [<span data-ttu-id="10b7a-118">Erstellen und Testen von Erweiterungspaketen</span><span class="sxs-lookup"><span data-stu-id="10b7a-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)

<span data-ttu-id="10b7a-119">Dieser Abschnitt des Leitfadens durchläuft die Erstellung manueller Erweiterungen [, nachdem Sie Ihr Windows Developer-Konto eingerichtet und ihre Erweiterungsnamen reserviert haben](./packaging/extensions-in-the-windows-Dev-Center.md).</span><span class="sxs-lookup"><span data-stu-id="10b7a-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="10b7a-120">Wenn Sie neugierig auf die feineren Details des Packens einer Erweiterung sind, lesen Sie diesen Artikel.</span><span class="sxs-lookup"><span data-stu-id="10b7a-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>

<span data-ttu-id="10b7a-121">Darüber hinaus finden Sie Informationen dazu, wie Sie [eine verpackte Erweiterung testen und entpacken](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package)können.</span><span class="sxs-lookup"><span data-stu-id="10b7a-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="10b7a-122">Diese Informationen sind auch dann relevant, wenn Sie die ManifoldJS-Verpackungs Route verlassen haben.</span><span class="sxs-lookup"><span data-stu-id="10b7a-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>

## [<span data-ttu-id="10b7a-123">Lokalisierung von Erweiterungspaketen</span><span class="sxs-lookup"><span data-stu-id="10b7a-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)
<span data-ttu-id="10b7a-124">Der Paket Lokalisierungs Schritt fällt zwischen dem Erstellen Ihrer appxmanifest.xml Datei und dem Ausführen des letzten Befehls zum Verpacken der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="10b7a-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>
<span data-ttu-id="10b7a-125">Auf diese Weise können Sie angeben, welche Sprachen Ihre Erweiterungen in Ihrem Microsoft Store-Eintrag unterstützen, und welche Sprache der Name der Erweiterung in Windows angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="10b7a-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>

<span data-ttu-id="10b7a-126">Sie können in diesem Abschnitt des Leitfadens zu [Localize-Name und Beschreibung für den Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) springen, wenn Ihre Erweiterung nicht mehrere Sprachen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10b7a-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>

## [<span data-ttu-id="10b7a-127">Verwenden von ManifoldJS zu Paketerweiterungen</span><span class="sxs-lookup"><span data-stu-id="10b7a-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)

<span data-ttu-id="10b7a-128">Die Tool-Route zum Verpacken Ihrer Erweiterung wird ManifoldJS ihre Erweiterung im Handumdrehen mit minimalem Aufwand für ihr Ende verpacken.</span><span class="sxs-lookup"><span data-stu-id="10b7a-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="10b7a-129">Stellen Sie nach dem Ausfüllen einiger AppXManifest-Eigenschaften einige Windows/Microsoft Store-Ressourcen bereit, und ihre Erweiterung wird in kürzester Zeit verpackt.</span><span class="sxs-lookup"><span data-stu-id="10b7a-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>

<span data-ttu-id="10b7a-130">Nachdem Sie Ihre Erweiterung gepackt haben, lesen Sie den Abschnitt [Testen](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) zum Erstellen und Testen Ihrer Microsoft Edge-Erweiterung, um zu erfahren, wie Sie Sie querladen oder entpacken können.</span><span class="sxs-lookup"><span data-stu-id="10b7a-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>


## [<span data-ttu-id="10b7a-131">Ausführen des Zertifizierungskits für Windows-Apps</span><span class="sxs-lookup"><span data-stu-id="10b7a-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)

<span data-ttu-id="10b7a-132">Sobald Sie über eine verpackte Erweiterung verfügen, können Sie diese über das Windows-App-Zertifizierungs Kit ausführen.</span><span class="sxs-lookup"><span data-stu-id="10b7a-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="10b7a-133">Auf diese Weise wird eine Reihe von Tests für Ihr Erweiterungspaket ausgeführt, um sicherzustellen, dass es für den Microsoft Store bereit ist.</span><span class="sxs-lookup"><span data-stu-id="10b7a-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>
