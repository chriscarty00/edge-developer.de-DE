---
description: Erfahren Sie, wie Sie Microsoft Edge-Erweiterungen entwickeln. Diese kleinen Programme können verwendet werden, um Microsoft Edge neue Funktionen hinzuzufügen oder vorhandene Funktionen zu ändern.
title: Extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
ms.technology: extensions
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.openlocfilehash: 4cc47ba9d927caf7457141f5c8c7eacbb9627b07
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567370"
---
# <span data-ttu-id="77eaf-105">Microsoft Edge-Erweiterungen (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="77eaf-105">Microsoft Edge (EdgeHTML) extensions</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="77eaf-106">Erweiterungen sind kleine Programme, die zum Hinzufügen neuer Features zu Microsoft Edge (EdgeHTML) oder zum Ändern der vorhandenen Funktionalität verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="77eaf-106">Extensions are small programs that can be used to add new features to Microsoft Edge (EdgeHTML) or modify the existing functionality.</span></span> <span data-ttu-id="77eaf-107">Erweiterungen dienen dazu, den Alltag des Nutzers zu verbessern, indem Sie Nischen Funktionen zur Verfügung stellen, die für Zielgruppen wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="77eaf-107">Extensions are intended to improve a user’s day-to-day browsing experience by providing niche functionality that is important to targeted audiences.</span></span>

<span data-ttu-id="77eaf-108">Microsoft Edge (EdgeHTML) unterstützt ein neues HTML-, JavaScript-und CSS-basiertes Erweiterungsmodell.</span><span class="sxs-lookup"><span data-stu-id="77eaf-108">Microsoft Edge (EdgeHTML) supports a new HTML, JavaScript and CSS based extension model.</span></span> <span data-ttu-id="77eaf-109">Dieses neue Modell ist Chrome-kompatibel, was bedeutet, dass vorhandene Chrome Extension-Entwickler Ihre Erweiterungen zu Microsoft Edge (EdgeHTML) mit minimalen Änderungen migrieren können.</span><span class="sxs-lookup"><span data-stu-id="77eaf-109">This new model is Chrome-compatible which means that existing Chrome extension developers will be able to migrate their extensions to Microsoft Edge (EdgeHTML) with minimal changes.</span></span>

<span data-ttu-id="77eaf-110">Eine Übersicht über die End-to-End-Reise zum Erstellen einer Microsoft Edge-Erweiterung (EdgeHTML) von der Entwicklung bis zur Veröffentlichung finden Sie im [Leitfaden "erste Schritte](./getting-started.md)".</span><span class="sxs-lookup"><span data-stu-id="77eaf-110">To get an overview of the end to end journey of creating a Microsoft Edge (EdgeHTML) extension from development to publishing, check out the [Getting started guide](./getting-started.md)!</span></span>


## <span data-ttu-id="77eaf-111">Beliebte Artikel</span><span class="sxs-lookup"><span data-stu-id="77eaf-111">Popular articles</span></span>

<table>
  <tr>
    <td><a href = "./api-support/extension-api-roadmap.md"><span data-ttu-id="77eaf-112">Wegweiser zur Erweiterungs-API</span><span class="sxs-lookup"><span data-stu-id="77eaf-112">Extension API roadmap</span></span></a></td>
    <td><span data-ttu-id="77eaf-113">Schauen Sie sich an, welche APIs unterstützt werden/in der Entwicklung für Windows 10 Insider Preview und öffentlich veröffentlichte Builds von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="77eaf-113">Check out what APIs are supported/in development for Windows 10 Insider Preview and publicly released builds of Microsoft Edge.</span></span></td></p>
<p>  </tr>
  <tr>
    <td><a href = "./api-support/supported-apis.md"><span data-ttu-id="77eaf-114">Unterstützte APIs</span><span class="sxs-lookup"><span data-stu-id="77eaf-114">Supported APIs</span></span></a></td>
    <td><span data-ttu-id="77eaf-115">Erhalten Sie Informationen zu unseren unterstützten APIs, einschließlich bekannter Probleme und Chrom Inkompatibilitäten.</span><span class="sxs-lookup"><span data-stu-id="77eaf-115">Get info on our supported APIs including known issues and Chrome incompatibilities.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/creating-an-extension.md"><span data-ttu-id="77eaf-116">Erstellen einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="77eaf-116">Creating an extension</span></span></a></td>
    <td><span data-ttu-id="77eaf-117">Sind Sie neu in der Welt der Erweiterungs Entwicklung?</span><span class="sxs-lookup"><span data-stu-id="77eaf-117">New to the world of extension development?</span></span> <span data-ttu-id="77eaf-118">Probieren Sie einige Tutorials aus, um sich zu beeilen.</span><span class="sxs-lookup"><span data-stu-id="77eaf-118">Try out some tutorials to get up to speed.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/packaging.md"><span data-ttu-id="77eaf-119">Verpacken</span><span class="sxs-lookup"><span data-stu-id="77eaf-119">Packaging</span></span></a></td>
    <td><span data-ttu-id="77eaf-120">Hier erfahren Sie, wie Sie Ihre Erweiterung verpacken, nachdem Sie die Entwicklung&#39;ve durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="77eaf-120">Learn how to package up your extension after you&#39;ve finished development.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/porting-chrome-extensions.md"><span data-ttu-id="77eaf-121">Portieren von Chrome-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="77eaf-121">Porting Chrome extensions</span></span></a></td>
    <td><span data-ttu-id="77eaf-122">Haben Sie eine Chrome-Erweiterung erstellt, die Sie&#39;d gerne auf Microsoft Edge sehen möchten?</span><span class="sxs-lookup"><span data-stu-id="77eaf-122">Created a Chrome extension you&#39;d like to see on Microsoft Edge?</span></span> <span data-ttu-id="77eaf-123">Hier erfahren Sie, wie Sie es mit dem Microsoft Edge Extension Toolkit portieren.</span><span class="sxs-lookup"><span data-stu-id="77eaf-123">See how to port it with the Microsoft Edge Extension Toolkit.</span></span></td>

  </tr>
</table>
