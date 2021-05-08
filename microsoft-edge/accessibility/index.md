---
description: Informationen zum Erstellen, Entwerfen und Testen barrierefreier Websites innerhalb Microsoft Edge.
title: Barrierefreiheit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Webentwicklung, ARIA, Entwickler, UIA, Benutzeroberflächenautomatisierung
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233726"
---
# <span data-ttu-id="d8853-104">Barrierefreiheit – Übersicht</span><span class="sxs-lookup"><span data-stu-id="d8853-104">Accessibility overview</span></span>  

> <span data-ttu-id="d8853-105">"\[T\]er Auswirkungen von Behinderungen werden im Web grundlegend geändert, da das Web Hindernisse für Kommunikation und Interaktion beseitigt, mit der viele Menschen in der physischen Welt zu sehen sind."</span><span class="sxs-lookup"><span data-stu-id="d8853-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="d8853-106">(Barrierefreiheit | W3C)</span><span class="sxs-lookup"><span data-stu-id="d8853-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="d8853-107">Die [Who Health Organization][WHODisabilities] definiert Behinderung als "einen Konflikt in der Interaktion zwischen den Features des Körpers einer Person und den Features der Umgebung, in der sie leben".</span><span class="sxs-lookup"><span data-stu-id="d8853-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="d8853-108">Behinderungen reichen von situationenbezogenen Behinderungen, z. B. eingeschränkter Mobilität beim Halten eines Babys oder hellem Sonnenlicht auf einem Telefon, bis zu anderen physischen, auditorischen, visuellen oder altersbezogenen Beeinträchtigungen.</span><span class="sxs-lookup"><span data-stu-id="d8853-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="d8853-109">Das Entwerfen von Websites und anderen Technologien für die Inklusion sorgt für eine für jede Person angenehme Erfahrung.</span><span class="sxs-lookup"><span data-stu-id="d8853-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="d8853-110">Inklusives Design und Barrierefreiheit im Web ermöglichen und unterstützen alle, das Web zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="d8853-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="d8853-111">Hier finden Sie einige bewährte Methoden, Codebeispiele und weitere Ressourcen, [][AccessibilityTest] um mehr über [das Entwerfen,][AccessibilityDesign]Erstellen [und][AccessibilityBuild]Testen barrierefreier Websites in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d8853-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="d8853-112">Barrierefreiheit in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d8853-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="d8853-113">In Microsoft Edge haben wir die moderne [Benutzeroberflächenautomatisierungs-API][WindowsWin32AutoEntryui] \(UIA-API\) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d8853-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="d8853-114">Die Umstellung auf UIA war eine wichtige Investition in die Barrierefreiheit von Browsern und legt die Grundlage für eine inklusivere Weberfahrung für Benutzer, die auf Hilfstechnologie in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d8853-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="d8853-115">Benutzer profitieren auch vom immergrünen Charakter des Chromium Engine.</span><span class="sxs-lookup"><span data-stu-id="d8853-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="d8853-116">Das Barrierefreiheitssystem in Microsoft Edge unterstützt grundsätzlich moderne Webstandards wie ARIA, HTML5 und CSS3.</span><span class="sxs-lookup"><span data-stu-id="d8853-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="d8853-117">Das folgende Diagramm der vereinfachten Browserpipeline folgt Webseiteninhalten in einer barrierefreien Präsentationsebene.</span><span class="sxs-lookup"><span data-stu-id="d8853-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="In das Modulmodell transformierte Inhalte werden in visuelle Ansichten und Barrierefreiheitsansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden":::
   <span data-ttu-id="d8853-119">In das Modulmodell transformierte Inhalte werden in visuelle Ansichten und Barrierefreiheitsansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden</span><span class="sxs-lookup"><span data-stu-id="d8853-119">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>  
:::image-end:::  

<span data-ttu-id="d8853-120">Das Microsoft Edge arbeitet kontinuierlich mit dem W3C und anderen Browseranbietern zusammen, um sicherzustellen, dass neue Webplattformfeatures über ausreichende integrierte Barrierefreiheit verfügen.</span><span class="sxs-lookup"><span data-stu-id="d8853-120">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="d8853-121">Informationen dazu, welche neuen HTML5-Features von der Microsoft Edge unterstützt werden, finden Sie unter [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="d8853-121">For information on which new HTML5 features are accessibly supported by Microsoft Edge, navigate to [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="d8853-122">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d8853-122">Resources</span></span>  

#### <span data-ttu-id="d8853-123">Microsoft Windows Ui Automation Blog</span><span class="sxs-lookup"><span data-stu-id="d8853-123">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="d8853-124">Der [Microsoft Windows-Benutzeroberflächenautomatisierungsblog][ArchiveBlogsWinuiautomation] behandelt Themen im Zusammenhang mit Windows Automatisierungs-API.</span><span class="sxs-lookup"><span data-stu-id="d8853-124">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="d8853-125">Web Accessibility Initiative (WAI)</span><span class="sxs-lookup"><span data-stu-id="d8853-125">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="d8853-126">Die [Web Accessibility Initiative (WAI),][W3CWaiHome] die bt das W3C bereitgestellt hat, ist ein Versuch, die Barrierefreiheit des Webs zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d8853-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="d8853-127">Die Website bietet eine Vielzahl von Ressourcen für erste Schritte mit [Webbarrierefreiheit,][W3CWaiGettingstartedOverview] [Entwerfen für][W3CWaiFundamentals]Inklusion, Lernprogramme und Präsentationen und [vieles][W3CWaiTeachAdvocate]mehr.</span><span class="sxs-lookup"><span data-stu-id="d8853-127">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Erstellen von Barrierefreien Websites | Microsoft Doc"  
[AccessibilityDesign]: ./design.md "Entwerfen von barrierefreien Websites | Microsoft Doc"  
[AccessibilityTest]: ./test.md "Barrierefreiheitstests | Microsoft Docs"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Benutzeroberflächenautomatisierung | Microsoft Doc"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Microsoft Windows Ui Automation Blog | Microsoft Doc"  

[HTML5Accessibility]: https://html5accessibility.com "HTML5-Barrierefreiheit"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Barrierefreiheit | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Einführung in web accessibility | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Erste Schritte: So können Sie auf eine Website | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Teach and Advocate Overview | Web Accessibility Initiative (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Behinderungen | WHO"  

