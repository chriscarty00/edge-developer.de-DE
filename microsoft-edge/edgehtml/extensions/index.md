---
description: Erfahren Sie, wie Sie Microsoft Edge-Erweiterungen entwickeln. Diese kleinen Programme können verwendet werden, um Microsoft Edge neue Funktionen hinzuzufügen oder vorhandene Funktionen zu ändern.
title: Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: extensions
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cc54e3512cf315183ce8baa59abde3db568d1828
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234138"
---
# <span data-ttu-id="72a35-105">Microsoft Edge-Erweiterungen (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="72a35-105">Microsoft Edge (EdgeHTML) extensions</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="72a35-106">Erweiterungen sind kleine Programme, die zum Hinzufügen neuer Features zu Microsoft Edge (EdgeHTML) oder zum Ändern der vorhandenen Funktionalität verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="72a35-106">Extensions are small programs that can be used to add new features to Microsoft Edge (EdgeHTML) or modify the existing functionality.</span></span> <span data-ttu-id="72a35-107">Erweiterungen dienen dazu, den Alltag des Nutzers zu verbessern, indem Sie Nischen Funktionen zur Verfügung stellen, die für Zielgruppen wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="72a35-107">Extensions are intended to improve a user’s day-to-day browsing experience by providing niche functionality that is important to targeted audiences.</span></span>

<span data-ttu-id="72a35-108">Microsoft Edge (EdgeHTML) unterstützt ein neues HTML-, JavaScript-und CSS-basiertes Erweiterungsmodell.</span><span class="sxs-lookup"><span data-stu-id="72a35-108">Microsoft Edge (EdgeHTML) supports a new HTML, JavaScript and CSS based extension model.</span></span> <span data-ttu-id="72a35-109">Dieses neue Modell ist Chrome-kompatibel, was bedeutet, dass vorhandene Chrome Extension-Entwickler Ihre Erweiterungen zu Microsoft Edge (EdgeHTML) mit minimalen Änderungen migrieren können.</span><span class="sxs-lookup"><span data-stu-id="72a35-109">This new model is Chrome-compatible which means that existing Chrome extension developers will be able to migrate their extensions to Microsoft Edge (EdgeHTML) with minimal changes.</span></span>

<span data-ttu-id="72a35-110">Eine Übersicht über die End-to-End-Reise zum Erstellen einer Microsoft Edge-Erweiterung (EdgeHTML) von der Entwicklung bis zur Veröffentlichung finden Sie im [Leitfaden "erste Schritte](./getting-started.md)".</span><span class="sxs-lookup"><span data-stu-id="72a35-110">To get an overview of the end to end journey of creating a Microsoft Edge (EdgeHTML) extension from development to publishing, check out the [Getting started guide](./getting-started.md)!</span></span>


## <span data-ttu-id="72a35-111">Beliebte Artikel</span><span class="sxs-lookup"><span data-stu-id="72a35-111">Popular articles</span></span>

<table>
  <tr>
    <td><a href = "./api-support/extension-api-roadmap.md"><span data-ttu-id="72a35-112">Wegweiser zur Erweiterungs-API</span><span class="sxs-lookup"><span data-stu-id="72a35-112">Extension API roadmap</span></span></a></td>
    <td><span data-ttu-id="72a35-113">Schauen Sie sich an, welche APIs unterstützt werden/in der Entwicklung für Windows 10 Insider Preview und öffentlich veröffentlichte Builds von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="72a35-113">Check out what APIs are supported/in development for Windows 10 Insider Preview and publicly released builds of Microsoft Edge.</span></span></td></p>
<p>  </tr>
  <tr>
    <td><a href = "./api-support/supported-apis.md"><span data-ttu-id="72a35-114">Unterstützte APIs</span><span class="sxs-lookup"><span data-stu-id="72a35-114">Supported APIs</span></span></a></td>
    <td><span data-ttu-id="72a35-115">Erhalten Sie Informationen zu unseren unterstützten APIs, einschließlich bekannter Probleme und Chrom Inkompatibilitäten.</span><span class="sxs-lookup"><span data-stu-id="72a35-115">Get info on our supported APIs including known issues and Chrome incompatibilities.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/creating-an-extension.md"><span data-ttu-id="72a35-116">Erstellen einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="72a35-116">Creating an extension</span></span></a></td>
    <td><span data-ttu-id="72a35-117">Sind Sie neu in der Welt der Erweiterungs Entwicklung?</span><span class="sxs-lookup"><span data-stu-id="72a35-117">New to the world of extension development?</span></span> <span data-ttu-id="72a35-118">Probieren Sie einige Tutorials aus, um sich zu beeilen.</span><span class="sxs-lookup"><span data-stu-id="72a35-118">Try out some tutorials to get up to speed.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/packaging.md"><span data-ttu-id="72a35-119">Verpacken</span><span class="sxs-lookup"><span data-stu-id="72a35-119">Packaging</span></span></a></td>
    <td><span data-ttu-id="72a35-120">Hier erfahren Sie, wie Sie Ihre Erweiterung verpacken, nachdem Sie die Entwicklung&#39;ve durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="72a35-120">Learn how to package up your extension after you&#39;ve finished development.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/porting-chrome-extensions.md"><span data-ttu-id="72a35-121">Portieren von Chrome-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="72a35-121">Porting Chrome extensions</span></span></a></td>
    <td><span data-ttu-id="72a35-122">Haben Sie eine Chrome-Erweiterung erstellt, die Sie&#39;d gerne auf Microsoft Edge sehen möchten?</span><span class="sxs-lookup"><span data-stu-id="72a35-122">Created a Chrome extension you&#39;d like to see on Microsoft Edge?</span></span> <span data-ttu-id="72a35-123">Hier erfahren Sie, wie Sie es mit dem Microsoft Edge Extension Toolkit portieren.</span><span class="sxs-lookup"><span data-stu-id="72a35-123">See how to port it with the Microsoft Edge Extension Toolkit.</span></span></td>

  </tr>
</table>
