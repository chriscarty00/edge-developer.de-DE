---
description: Informieren Sie sich über Ressourcen für inklusive Design Tools und bewährte Methoden.
title: Barrierefreiheit – Entwurf
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 8468f8e1-9f4a-426c-a969-76eab9419137
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Web-Entwicklung, Aria, Developer, UIA, UI-Automatisierung
ms.openlocfilehash: 8d31f7b32cb92794ff8592c239436f3b101a3859
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230817"
---
# <span data-ttu-id="f665a-104">Entwerfen barrierefreier Websites</span><span class="sxs-lookup"><span data-stu-id="f665a-104">Designing Accessible Websites</span></span>  

<span data-ttu-id="f665a-105">Durch die Erstellung eines integrativen Designs ist Technologie für alle Menschen unabhängig von Alter, Ausbildung, geographischem Standort, Sprache oder Behinderung nutzbar.</span><span class="sxs-lookup"><span data-stu-id="f665a-105">Creating an inclusive design makes technology usable by all people no matter their age, education, geographic location, language, or disability.</span></span>  <span data-ttu-id="f665a-106">Personen, die Technologie verwenden und das Internet durchsuchen, verfügen über eine breite Palette von Fähigkeiten und Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="f665a-106">People using technology and browsing the web have a wide range of abilities and preferences.</span></span>  <span data-ttu-id="f665a-107">Beachten Sie beim Entwerfen Ihrer Website die folgenden wichtigen Barrierefreiheits Szenarien:</span><span class="sxs-lookup"><span data-stu-id="f665a-107">As you design your website, keep in mind the following key accessibility scenarios:</span></span>

*   <span data-ttu-id="f665a-108">Bildschirmsprachausgaben – blinde oder sehbehinderte Benutzer verlassen sich auf Sprachausgabe, um die Benutzeroberfläche Ihrer APP zu interpretieren und mit ihr zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="f665a-108">Screen readers—Users who are blind or visually impaired rely on screen readers to interpret and interact with the UI of your app.</span></span>  <span data-ttu-id="f665a-109">Bei der Interpretation werden die Benutzeroberflächenelement Namen, Rollen, Werte usw. gelesen, und die Interaktion mit der Benutzeroberfläche umfasst das Verschieben des Fokus von einem Element zu einem anderen und das Aufrufen von Funktionen.</span><span class="sxs-lookup"><span data-stu-id="f665a-109">Interpreting involves reading the UI element names, roles, values, and so on, and interacting with the UI involves moving the focus from one element to another and invoking functionality.</span></span>
*   <span data-ttu-id="f665a-110">Barrierefreiheit in der Tastatur – viele Benutzer von Barrierefreiheit Vertrauen auf die Tastatur, um die Benutzeroberfläche zu navigieren und zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="f665a-110">Keyboard accessibility—Many accessibility users rely on the keyboard to navigate and operate the UI by:</span></span>
    *   <span data-ttu-id="f665a-111">Bewegen des Fokus zwischen Elementen mithilfe der TAB-TASTE.</span><span class="sxs-lookup"><span data-stu-id="f665a-111">Moving focus among elements by using the Tab key.</span></span>
    *   <span data-ttu-id="f665a-112">Navigieren in Containerelementen wie Listen, Rastern und Strukturansichten mithilfe der Pfeiltasten</span><span class="sxs-lookup"><span data-stu-id="f665a-112">Navigating in container elements such as lists, grids, and tree views by using the arrow keys.</span></span>
    *   <span data-ttu-id="f665a-113">Aktivieren der Funktion \(Aufrufen von Aktionen \) mithilfe der EINGABETASTE oder LEERTASTE.</span><span class="sxs-lookup"><span data-stu-id="f665a-113">Activating functionality \(invoking actions\) by using the Enter or Space key.</span></span>
    *   <span data-ttu-id="f665a-114">Verwenden von Tastenkombinationen zum effektiven Zugreifen auf andere App-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f665a-114">Using shortcut keys to efficiently access other app functionality.</span></span>
*   <span data-ttu-id="f665a-115">Barrierefreie visuelle Ober Leistung: Benutzer, die sehbehindert sind, benötigen ein ausreichendes Textkontrast Verhältnis für Textinhalte und eine gute visuelle Darstellung mit Designs mit hohem Kontrast insgesamt.</span><span class="sxs-lookup"><span data-stu-id="f665a-115">Accessible visual experience—Users who are visually impaired need a sufficient text contrast ratio for text content, and a good visual experience with high contrast themes overall.</span></span>  <span data-ttu-id="f665a-116">Für farbenblinde Benutzer müssen Informationen auf andere Art als über Farbe vermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="f665a-116">Users who are color blind need information to be conveyed in ways other than through color.</span></span>

<span data-ttu-id="f665a-117">Viele häufige Probleme mit der Barrierefreiheit im Internet können durch eine gute Codierungspraxis gelöst werden.</span><span class="sxs-lookup"><span data-stu-id="f665a-117">Many common accessibility issues on the web can be solved through good coding practice.</span></span>  <span data-ttu-id="f665a-118">Die [2,0-Dokumentation für Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/TR/WCAG20) bietet Techniken und bewährte Methoden, mit denen Sie barrierefreiere dynamische Webanwendungen entwerfen können.</span><span class="sxs-lookup"><span data-stu-id="f665a-118">The [Web Content Accessibility Guidelines (WCAG) 2.0](https://www.w3.org/TR/WCAG20) documentation provides techniques and best practices to help you design more accessible dynamic web applications.</span></span>  <span data-ttu-id="f665a-119">Weitere Informationen zum Erstellen von barrierefreien Websites finden Sie unter [Erstellen von barrierefreien](./build/index.md) Websites.</span><span class="sxs-lookup"><span data-stu-id="f665a-119">For more information on building accessible websites, navigate to [Building Accessible Websites](./build/index.md) .</span></span>

## <span data-ttu-id="f665a-120">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f665a-120">Resources</span></span>  

#### [<span data-ttu-id="f665a-121">Entwerfen für Inklusion</span><span class="sxs-lookup"><span data-stu-id="f665a-121">Designing for Inclusion</span></span>](https://w3.org/WAI/users/Overview.html)  

<span data-ttu-id="f665a-122">Das Entwerfen für die Integration durch die W3C Web Accessibility-Initiative bietet Ressourcen, die Ihnen helfen, Benutzer mit Behinderungen besser zu verstehen, und wie Sie Ihre Website mit Ihnen entwerfen.</span><span class="sxs-lookup"><span data-stu-id="f665a-122">Designing for Inclusion by the W3C Web Accessibility Initiative provides resources to help you better understand users with disabilities and how to design your website with them in mind.</span></span>

#### [<span data-ttu-id="f665a-123">Entwerfen von barrierefreier Software</span><span class="sxs-lookup"><span data-stu-id="f665a-123">Designing inclusive software</span></span>](https://msdn.microsoft.com/windows/uwp/accessibility/designing-inclusive-software)  

<span data-ttu-id="f665a-124">Beim Entwerfen von inklusiver Software werden die Microsoft-Entwurfsgrundsätze und-Methoden für die universelle Windows-Plattform (UWP) erläutert.</span><span class="sxs-lookup"><span data-stu-id="f665a-124">Designing inclusive software discusses Microsoft design principles and practices for the Universal Windows Platform (UWP).</span></span>

#### [<span data-ttu-id="f665a-125">Verwenden von Personen mit Behinderungen im Web</span><span class="sxs-lookup"><span data-stu-id="f665a-125">How People with Disabilities Use the Web</span></span>](https://www.w3.org/WAI/intro/people-use-web/Overview.html)  

<span data-ttu-id="f665a-126">Diese Ressource des W3C führt vor, wie Personen mit Behinderungen, einschließlich Personen mit altersbedingten Beeinträchtigungen, das Web verwenden.</span><span class="sxs-lookup"><span data-stu-id="f665a-126">This resource by the W3C introduces how people with disabilities, including people with age-related impairments, use the Web.</span></span>

#### [<span data-ttu-id="f665a-127">Inklusives Design-Toolkit</span><span class="sxs-lookup"><span data-stu-id="f665a-127">Inclusive Design Toolkit</span></span>](https://www.microsoft.com/design/practice#howwemake-section)  

<span data-ttu-id="f665a-128">Microsoft hat das inklusive Design-Toolkit entwickelt, um zu zeigen, wie die menschliche Vielfalt zu besseren Design Zwängen führen kann und wie scheinbar Nische Lösungen an breitere Märkte angeschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="f665a-128">Microsoft developed the Inclusive Design Toolkit to show how human diversity can create better design constraints and how to connect seemingly niche solutions to broader markets.</span></span>
