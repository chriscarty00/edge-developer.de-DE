---
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
description: Erfahren Sie, wie Sie barrierefreie Websites in Microsoft Edge erstellen, entwerfen und testen können.
title: Bedienungshilfen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Web-Entwicklung, Aria, Developer, UIA, UI-Automatisierung
ms.openlocfilehash: 6ad95e9c250aa6a4a61ca09470cea86efd715427
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583105"
---
# <span data-ttu-id="7084d-104">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="7084d-104">Accessibility</span></span>  

> <span data-ttu-id="7084d-105">"\ [T \] die Auswirkungen einer Behinderung werden im Internet grundlegend geändert, weil das Internet Hindernisse für Kommunikation und Interaktion entfernt, die viele Menschen in der physischen Welt sehen."</span><span class="sxs-lookup"><span data-stu-id="7084d-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="7084d-106">(Barrierefreiheit | W3C</span><span class="sxs-lookup"><span data-stu-id="7084d-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="7084d-107">Die [Weltgesundheitsorganisation][WHODisabilities] definiert Behinderung als "ein Missverhältnis zwischen den Funktionen des Körpers einer Person und den Eigenschaften der Umgebung, in der Sie leben".</span><span class="sxs-lookup"><span data-stu-id="7084d-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="7084d-108">Behinderungen reichern von situationsbedingten Behinderungen wie eingeschränkter Mobilität, während Sie ein Baby oder ein helles Sonnenlicht auf einem Telefon halten, bis zu anderen körperlichen, auditiven, visuellen oder altersbedingten Beeinträchtigungen.</span><span class="sxs-lookup"><span data-stu-id="7084d-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="7084d-109">Das Entwerfen von Websites und anderen Technologien für die Integration sorgt für ein angenehmes Erlebnis jeder Person.</span><span class="sxs-lookup"><span data-stu-id="7084d-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="7084d-110">Inklusive Design und Barrierefreiheit im Web ermöglicht und unterstützt jeden, das Internet zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="7084d-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="7084d-111">Im folgenden finden Sie einige bewährte Methoden, Codebeispiele und weitere Ressourcen, mit denen Sie mehr über das [entwerfen][AccessibilityDesign], [Erstellen][AccessibilityBuild]und [Testen][AccessibilityTest] von barrierefreien Websites in Microsoft Edge erfahren.</span><span class="sxs-lookup"><span data-stu-id="7084d-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="7084d-112">Barrierefreiheit in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7084d-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="7084d-113">In Microsoft Edge haben wir eine moderne [UI-Automatisierung-API][WindowsWin32AutoEntryui] (UIA-API \) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7084d-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="7084d-114">Die Änderung an UIA war eine wichtige Investition in die Barrierefreiheit des Browsers und bildet die Grundlage für ein umfassenderes Weberlebnis für Benutzer, die von Hilfstechnologien in Windows 10 abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="7084d-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="7084d-115">Benutzer profitieren auch vom immergrünen Charakter der Chrom Maschine.</span><span class="sxs-lookup"><span data-stu-id="7084d-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="7084d-116">Das Barrierefreiheits System in Microsoft Edge unterstützt inhärent moderne Web-Standards wie Aria, HTML5 und CSS3.</span><span class="sxs-lookup"><span data-stu-id="7084d-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="7084d-117">Das folgende Diagramm der vereinfachten Browser Pipeline folgt dem Inhalt einer Webseite in einer barrierefreien Präsentationsschicht.</span><span class="sxs-lookup"><span data-stu-id="7084d-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Inhalte, die in das Modul Modell umgewandelt werden, werden in visuelle und Barrierefreiheits Ansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden.":::
   <span data-ttu-id="7084d-119">Abbildung1.</span><span class="sxs-lookup"><span data-stu-id="7084d-119">Figure 1.</span></span>  <span data-ttu-id="7084d-120">Inhalte, die in das Modul Modell umgewandelt werden, werden in visuelle und Barrierefreiheits Ansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7084d-120">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>
:::image-end:::

<!--![Figure 1.  Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation][ImageAccessibilityArchitecture]  -->  

<span data-ttu-id="7084d-121">Das Microsoft Edge-Team arbeitet kontinuierlich mit dem W3C und anderen Browser Anbietern zusammen, um sicherzustellen, dass die Features der neuen Webplattform genügend integrierte Barrierefreiheit aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7084d-121">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="7084d-122">Informationen zu den neuen HTML5-Features, die von Microsoft Edge zugänglich unterstützt werden, finden Sie unter [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="7084d-122">For information on which new HTML5 features are accessibly supported by Microsoft Edge, visit [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="7084d-123">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7084d-123">Resources</span></span>  

#### <span data-ttu-id="7084d-124">Microsoft Windows-Benutzeroberflächen Automatisierungs Blog</span><span class="sxs-lookup"><span data-stu-id="7084d-124">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="7084d-125">Der [Microsoft Windows-Benutzeroberflächen Automatisierungs Blog][ArchiveBlogsWinuiautomation] behandelt Themen im Zusammenhang mit der Windows-Automatisierungs-API.</span><span class="sxs-lookup"><span data-stu-id="7084d-125">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="7084d-126">Web Accessibility Initiative (WAI)</span><span class="sxs-lookup"><span data-stu-id="7084d-126">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="7084d-127">Die [Web Accessibility Initiative (WAI)][W3CWaiHome] , die BT im W3C zur Verfügung stellt, ist eine Bemühung, die Barrierefreiheit im Internet zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7084d-127">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="7084d-128">Die Website bietet eine Reihe von Ressourcen für den Einstieg [in die Barrierefreiheit im Web][W3CWaiGettingstartedOverview], das [Entwerfen für Inklusion][W3CWaiFundamentals], [Tutorials und Präsentationen][W3CWaiTeachAdvocate]und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="7084d-128">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  


<!-- image links -->  

<!--[ImageAccessibilityArchitecture]: ./media/accessibilityarchitecture.png "Figure 1: Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation"  -->  

<!-- links -->  

[AccessibilityBuild]: ./accessibility/build.md "Erstellen von barrierefreien Websites"  
[AccessibilityDesign]: ./accessibility/design.md "Entwerfen barrierefreier Websites"  
[AccessibilityTest]: ./accessibility/test.md "Barrierefreiheits Tests"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Benutzeroberflächenautomatisierungs"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Microsoft Windows-Benutzeroberflächen Automatisierungs Blog"  

[HTML5Accessibility]: https://html5accessibility.com "Barrierefreiheit in HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Barrierefreiheit | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Einführung in Barrierefreiheit im Web | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Erste Schritte: Erstellen einer Website für Barrierefreiheit | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Übersicht über unterrichten und Fürsprecher | Web Accessibility Initiative (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Behinderungen | Wer"  

