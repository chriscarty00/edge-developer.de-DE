---
description: Erfahren Sie, wie Sie barrierefreie Websites in Microsoft Edge erstellen, entwerfen und testen können.
title: Bedienungshilfen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Web-Entwicklung, Aria, Developer, UIA, UI-Automatisierung
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233726"
---
# <span data-ttu-id="5071b-104">Barrierefreiheit im Überblick</span><span class="sxs-lookup"><span data-stu-id="5071b-104">Accessibility overview</span></span>  

> <span data-ttu-id="5071b-105">"\ [T \] die Auswirkungen einer Behinderung werden im Internet grundlegend geändert, weil das Internet Hindernisse für Kommunikation und Interaktion entfernt, die viele Menschen in der physischen Welt sehen."</span><span class="sxs-lookup"><span data-stu-id="5071b-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="5071b-106">(Barrierefreiheit | W3C</span><span class="sxs-lookup"><span data-stu-id="5071b-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="5071b-107">Die [Weltgesundheitsorganisation][WHODisabilities] definiert Behinderung als "ein Missverhältnis zwischen den Funktionen des Körpers einer Person und den Eigenschaften der Umgebung, in der Sie leben".</span><span class="sxs-lookup"><span data-stu-id="5071b-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="5071b-108">Behinderungen reichern von situationsbedingten Behinderungen wie eingeschränkter Mobilität, während Sie ein Baby oder ein helles Sonnenlicht auf einem Telefon halten, bis zu anderen körperlichen, auditiven, visuellen oder altersbedingten Beeinträchtigungen.</span><span class="sxs-lookup"><span data-stu-id="5071b-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="5071b-109">Das Entwerfen von Websites und anderen Technologien für die Integration sorgt für ein angenehmes Erlebnis jeder Person.</span><span class="sxs-lookup"><span data-stu-id="5071b-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="5071b-110">Inklusive Design und Barrierefreiheit im Web ermöglicht und unterstützt jeden, das Internet zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="5071b-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="5071b-111">Im folgenden finden Sie einige bewährte Methoden, Codebeispiele und weitere Ressourcen, mit denen Sie mehr über das [entwerfen][AccessibilityDesign], [Erstellen][AccessibilityBuild]und [Testen][AccessibilityTest] von barrierefreien Websites in Microsoft Edge erfahren.</span><span class="sxs-lookup"><span data-stu-id="5071b-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="5071b-112">Barrierefreiheit in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5071b-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="5071b-113">In Microsoft Edge haben wir eine moderne [UI-Automatisierung-API][WindowsWin32AutoEntryui] (UIA-API \) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5071b-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="5071b-114">Die Änderung an UIA war eine wichtige Investition in die Barrierefreiheit des Browsers und bildet die Grundlage für ein umfassenderes Weberlebnis für Benutzer, die von Hilfstechnologien in Windows 10 abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5071b-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="5071b-115">Benutzer profitieren auch vom immergrünen Charakter der Chrom Maschine.</span><span class="sxs-lookup"><span data-stu-id="5071b-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="5071b-116">Das Barrierefreiheits System in Microsoft Edge unterstützt inhärent moderne Web-Standards wie Aria, HTML5 und CSS3.</span><span class="sxs-lookup"><span data-stu-id="5071b-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="5071b-117">Das folgende Diagramm der vereinfachten Browser Pipeline folgt dem Inhalt einer Webseite in einer barrierefreien Präsentationsschicht.</span><span class="sxs-lookup"><span data-stu-id="5071b-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Inhalte, die in das Modul Modell umgewandelt werden, werden in visuelle und Barrierefreiheits Ansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden.":::
   <span data-ttu-id="5071b-119">Inhalte, die in das Modul Modell umgewandelt werden, werden in visuelle und Barrierefreiheits Ansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5071b-119">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>  
:::image-end:::  

<span data-ttu-id="5071b-120">Das Microsoft Edge-Team arbeitet kontinuierlich mit dem W3C und anderen Browser Anbietern zusammen, um sicherzustellen, dass die Features der neuen Webplattform genügend integrierte Barrierefreiheit aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5071b-120">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="5071b-121">Informationen zu den neuen HTML5-Features, die von Microsoft Edge unterstützt zugänglich, finden Sie unter [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="5071b-121">For information on which new HTML5 features are accessibly supported by Microsoft Edge, navigate to [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="5071b-122">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5071b-122">Resources</span></span>  

#### <span data-ttu-id="5071b-123">Microsoft Windows-Benutzeroberflächen Automatisierungs Blog</span><span class="sxs-lookup"><span data-stu-id="5071b-123">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="5071b-124">Der [Microsoft Windows-Benutzeroberflächen Automatisierungs Blog][ArchiveBlogsWinuiautomation] behandelt Themen im Zusammenhang mit der Windows-Automatisierungs-API.</span><span class="sxs-lookup"><span data-stu-id="5071b-124">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="5071b-125">Web Accessibility Initiative (WAI)</span><span class="sxs-lookup"><span data-stu-id="5071b-125">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="5071b-126">Die [Web Accessibility Initiative (WAI)][W3CWaiHome] , die BT im W3C zur Verfügung stellt, ist eine Bemühung, die Barrierefreiheit im Internet zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="5071b-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="5071b-127">Die Website bietet eine Reihe von Ressourcen für den Einstieg [in die Barrierefreiheit im Web][W3CWaiGettingstartedOverview], das [Entwerfen für Inklusion][W3CWaiFundamentals], [Tutorials und Präsentationen][W3CWaiTeachAdvocate]und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="5071b-127">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Erstellen von barrierefreien Websites | Microsoft doc"  
[AccessibilityDesign]: ./design.md "Entwerfen barrierefreier Websites | Microsoft doc"  
[AccessibilityTest]: ./test.md "Barrierefreiheits Tests | Microsoft docs"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "UI-Automatisierung | Microsoft doc"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog für Microsoft Windows-Benutzeroberflächenautomatisierung | Microsoft doc"  

[HTML5Accessibility]: https://html5accessibility.com "Barrierefreiheit in HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Barrierefreiheit | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Einführung in Barrierefreiheit im Web | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Erste Schritte: Erstellen einer Website für Barrierefreiheit | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Übersicht über unterrichten und Fürsprecher | Web Accessibility Initiative (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Behinderungen | Wer"  

