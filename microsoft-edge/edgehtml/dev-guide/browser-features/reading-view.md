---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Schauen Sie sich an, wie Microsoft Edge eine Leseansicht für Webseiten bietet, um Add-Free-Lesefunktionen zu ermöglichen.
title: Leseansicht – Entwicklerhandbuch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 30c01d61ff896cca7b0af90b345a8619307f91c0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234124"
---
# <span data-ttu-id="fe34d-104">Leseansicht</span><span class="sxs-lookup"><span data-stu-id="fe34d-104">Reading view</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="fe34d-105">Microsoft Edge bietet eine Leseansicht für eine optimierte, Buch ähnliche Leseerfahrung von Webseiten ohne Ablenkung von nicht miteinander verknüpften oder anderen sekundären Inhalten auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="fe34d-105">Microsoft Edge provides a reading view for a more streamlined, book-like reading experience of webpages without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="fe34d-106">Die Leseansicht kann über die Schaltfläche " **Leseansicht** \(Buchsymbol \)" auf der Adressleiste oder mit aktiviert oder deaktiviert werden `Ctrl` + `Shift` + `R` .</span><span class="sxs-lookup"><span data-stu-id="fe34d-106">Reading view can be toggled on or off from the **Reading view** \(book icon\) button on the address bar or with `Ctrl`+`Shift`+`R`.</span></span>  <span data-ttu-id="fe34d-107">In der Leseansicht werden die folgenden Metadaten von einer Seite extrahiert:</span><span class="sxs-lookup"><span data-stu-id="fe34d-107">Reading view extracts the following metadata from a page:</span></span>  

*   <span data-ttu-id="fe34d-108">Title</span><span class="sxs-lookup"><span data-stu-id="fe34d-108">Title</span></span>
*   <span data-ttu-id="fe34d-109">Autor</span><span class="sxs-lookup"><span data-stu-id="fe34d-109">Author</span></span>
*   <span data-ttu-id="fe34d-110">Date</span><span class="sxs-lookup"><span data-stu-id="fe34d-110">Date</span></span>
*   <span data-ttu-id="fe34d-111">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="fe34d-111">Publisher</span></span>
*   <span data-ttu-id="fe34d-112">Dominantes Bild \(s \)</span><span class="sxs-lookup"><span data-stu-id="fe34d-112">Dominant image\(s\)</span></span>
*   <span data-ttu-id="fe34d-113">Beschriftungen des dominanten Bilds \(s \)</span><span class="sxs-lookup"><span data-stu-id="fe34d-113">Captions of dominant image\(s\)</span></span>
*   <span data-ttu-id="fe34d-114">Sekundäre Bilder</span><span class="sxs-lookup"><span data-stu-id="fe34d-114">Secondary images</span></span>
*   <span data-ttu-id="fe34d-115">Haupt Textinhalt der Seite</span><span class="sxs-lookup"><span data-stu-id="fe34d-115">Main text content of the page</span></span>
*   <span data-ttu-id="fe34d-116">Copyright</span><span class="sxs-lookup"><span data-stu-id="fe34d-116">Copyright</span></span>

<span data-ttu-id="fe34d-117">Benutzer können dann den Seiten Kontrast und den Schriftgrad im Microsoft Edge **Settings** -Panel anpassen.</span><span class="sxs-lookup"><span data-stu-id="fe34d-117">Users can then adjust the page contrast and font size from the Microsoft Edge **Settings** panel.</span></span>  

## <span data-ttu-id="fe34d-118">Extraktion von Metadaten</span><span class="sxs-lookup"><span data-stu-id="fe34d-118">Metadata extraction</span></span>  

<span data-ttu-id="fe34d-119">Hier finden Sie Details zu den Seiten Metadaten, die von der Leseansicht gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="fe34d-119">Here are details of the page metadata rendered by reading view.</span></span>  

### <span data-ttu-id="fe34d-120">Title</span><span class="sxs-lookup"><span data-stu-id="fe34d-120">Title</span></span>  

<span data-ttu-id="fe34d-121">So stellen Sie sicher, dass die Leseansicht den Titel Ihres Artikels rendert:</span><span class="sxs-lookup"><span data-stu-id="fe34d-121">To ensure Reading view renders your article's title:</span></span>  

*   <span data-ttu-id="fe34d-122">Einfügen eines `title` Elements in die Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="fe34d-122">Include a `title` element in your header</span></span>  
*   <span data-ttu-id="fe34d-123">Einfügen eines Meta-Tags</span><span class="sxs-lookup"><span data-stu-id="fe34d-123">Include a meta tag with</span></span> `name="title"`  
*   <span data-ttu-id="fe34d-124">Vergleichen Sie den Titeltext in Ihrem Artikel Text mit der Inhaltszeichenfolge Ihres Meta-Tags.</span><span class="sxs-lookup"><span data-stu-id="fe34d-124">Match the title text in your article body with the content string of your meta tag.</span></span>  <span data-ttu-id="fe34d-125">Pipes \( `|` \) in der Inhaltszeichenfolge verhindern, dass die Leseransicht aktiv wird, versuchen Sie stattdessen, Bindestriche zu verwenden `-` .</span><span class="sxs-lookup"><span data-stu-id="fe34d-125">Pipes \(`|`\) in your content string prevent the reader view from becoming active, try using hyphens \(`-`\) instead.</span></span>  

### <span data-ttu-id="fe34d-126">Autor</span><span class="sxs-lookup"><span data-stu-id="fe34d-126">Author</span></span>  

<span data-ttu-id="fe34d-127">In der Leseansicht wird nach einem Element gesucht `class = "byline-name"` .</span><span class="sxs-lookup"><span data-stu-id="fe34d-127">Reading View will look for an element with `class = "byline-name"`.</span></span>  <span data-ttu-id="fe34d-128">Bewährte Methode besteht darin, den Autorennamen hinter dem Titel und vor dem Artikel Text zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="fe34d-128">Best practice is to place the author name after the title and before the article body.</span></span>  

```html
<div class="byline-name">Author name</div>
```  

### <span data-ttu-id="fe34d-129">Date</span><span class="sxs-lookup"><span data-stu-id="fe34d-129">Date</span></span>  

<span data-ttu-id="fe34d-130">In der Leseansicht werden der Herausgeber und die Datumsinformationen in derselben Zeile zusammen mit zusätzlicher Formatierung gerendert, um diese Informationen hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="fe34d-130">Reading view will render the publisher and date information together on the same line, with additional styling to highlight this information.</span></span>  <span data-ttu-id="fe34d-131">Das Veröffentlichungsdatum des Artikels wird exakt so gerendert, wie es in der Zeichenfolge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fe34d-131">The article's publishing date will render exactly as it appears in the string.</span></span>  <span data-ttu-id="fe34d-132">Die Leseansicht wird nicht in ein bestimmtes Datumsformat konvertiert.</span><span class="sxs-lookup"><span data-stu-id="fe34d-132">Reading view does not convert to a specific date format.</span></span>  

<span data-ttu-id="fe34d-133">Wenn Sie über ein Datum in Ihrem Artikel Text verfügen und es in der Leseansicht rendern möchten, weisen Sie das Element mit dem Datum der Klasse zu `'dateline'` :</span><span class="sxs-lookup"><span data-stu-id="fe34d-133">If you have a date in your article body and would like Reading view to render it, assign the element containing the date with the class `'dateline'`:</span></span>  

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```  

<span data-ttu-id="fe34d-134">Verwenden Sie das Meta-Tag, wenn Sie nicht über ein Datum im Artikel Text verfügen, aber die Leseansicht zum Rendern des Datums verwenden möchten `name='displaydate'` :</span><span class="sxs-lookup"><span data-stu-id="fe34d-134">If you don't have a date in the article body but would like Reading view to render the date, use the meta tag `name='displaydate'`:</span></span>  

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```  

### <span data-ttu-id="fe34d-135">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="fe34d-135">Publisher</span></span>  

<span data-ttu-id="fe34d-136">In der Leseansicht wird nach dem Open Graph `"og:site_name"` -Protokoll gesucht, um die Herausgeberinformationen zu rendern.</span><span class="sxs-lookup"><span data-stu-id="fe34d-136">Reading view will look for the Open Graph protocol `"og:site_name"` to render the publisher information.</span></span>  <span data-ttu-id="fe34d-137">Darüber hinaus sucht Sie nach `source_organization` und `publisher` Attribute in einem beliebigen HTML-Tag als sekundärer Indikator für Herausgeberinformationen auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="fe34d-137">It also looks for `source_organization` and `publisher` attributes in any html tag as a secondary indicator of publisher information on the page.</span></span>  <span data-ttu-id="fe34d-138">Der Text des Herausgebers wird mit der URL der Seite über den Hyperlink-Stil "Leseansicht" verknüpft.</span><span class="sxs-lookup"><span data-stu-id="fe34d-138">The publisher text will be hyperlinked to the URL of page using the Reading view page hyperlink style.</span></span>  

```html
<meta content="Name of organization source" property="og:site_name">
```  

### <span data-ttu-id="fe34d-139">Images</span><span class="sxs-lookup"><span data-stu-id="fe34d-139">Images</span></span>  

<span data-ttu-id="fe34d-140">In der Leseansicht werden die meisten RAW-Bilder mit Breite >= 400px und Seitenverhältnis >= 1/3 und =< 3,0 erfasst.</span><span class="sxs-lookup"><span data-stu-id="fe34d-140">Reading view captures most raw images with width >= 400px and aspect ratio >= 1/3 and =< 3.0.</span></span>  <span data-ttu-id="fe34d-141">Bilder, die diese Dimensionen nicht erfüllen, werden möglicherweise weiterhin extrahiert, wie Bilder, die kleiner als 400px sind, aber über Beschriftungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="fe34d-141">Images that do not meet these dimensions may still be extracted, such as images that are smaller than 400px in width but have captions.</span></span>  <span data-ttu-id="fe34d-142">Das erste geeignete Bild wird zum dominanten Bild des Artikels.</span><span class="sxs-lookup"><span data-stu-id="fe34d-142">The first eligible image becomes the dominant image of the article.</span></span>  <span data-ttu-id="fe34d-143">Das dominante Bild wird als erster Teil des Inhalts gerendert und erhält die volle Spaltenbreite.</span><span class="sxs-lookup"><span data-stu-id="fe34d-143">The dominant image is rendered as the first piece of content and given full column width.</span></span>  <span data-ttu-id="fe34d-144">Alle folgenden Bilder werden als Inline Bilder innerhalb des Artikels gerendert.</span><span class="sxs-lookup"><span data-stu-id="fe34d-144">All following images are rendered as inline images within the article.</span></span>  

### <span data-ttu-id="fe34d-145">Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="fe34d-145">Captions</span></span>  

<span data-ttu-id="fe34d-146">Bewährte Methode ist das Platzieren von Bildern in [Abbildungs](https://developer.mozilla.org/docs/Web/HTML/Element/figure) Tags mit nicht mehr als zwei geschachtelten [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) -Tags.</span><span class="sxs-lookup"><span data-stu-id="fe34d-146">Best practice is to place images in [figure](https://developer.mozilla.org/docs/Web/HTML/Element/figure) tags with no more than two nested [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) tags.</span></span>  

### <span data-ttu-id="fe34d-147">Textkörper</span><span class="sxs-lookup"><span data-stu-id="fe34d-147">Body</span></span>  

<span data-ttu-id="fe34d-148">Um sicherzustellen, dass der gesamte Textkörper Ihrer Seite in der Leseansicht erfasst wird, hilft es, den größten Teil des Artikel Texts auf den gleichen Schriftgrad und die gleiche Dom-Tiefe zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="fe34d-148">To ensure that all the body text of your page is captured by Reading view, it helps to keep most of the article text the same font size and DOM depth.</span></span>  <span data-ttu-id="fe34d-149">Der Leseansicht-Algorithmus ermöglicht eine gewisse Abweichung von dieser Regel, damit Publisher die Freiheit haben, Zeilen oder Wörter hervorheben zu können.</span><span class="sxs-lookup"><span data-stu-id="fe34d-149">The reading view algorithm allows for some deviation from this rule so publishers can have the freedom to add emphasis to lines or words.</span></span>  

### <span data-ttu-id="fe34d-150">Copyright</span><span class="sxs-lookup"><span data-stu-id="fe34d-150">Copyright</span></span>  

<span data-ttu-id="fe34d-151">Leseansicht extrahiert und zeigt Copyright Informationen an, die durch Metatags gekennzeichnet `name = "copyright"` sind, oder wenn keine Meta-Tag-Informationen vorhanden sind, ein Textknoten, der das Copyright-Symbol "\( `©` \)" enthält.</span><span class="sxs-lookup"><span data-stu-id="fe34d-151">Reading view extracts and displays copyright information denoted by meta tags with `name = "copyright"`, or if no meta tag information exists, a text node that contains the copyright \(`©`\) symbol.</span></span>  <span data-ttu-id="fe34d-152">In der Leseansicht werden die Copyright Informationen am Ende des Haupttexts des Artikels angezeigt, wobei ein kleinerer Schriftgrad als der Hauptteil des Texts formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="fe34d-152">Reading view displays copyright information at the end of the article main body, styled using a smaller font size than the main body text.</span></span>  

```html
<meta name="copyright" content="Your copyright information">
```  

## <span data-ttu-id="fe34d-153">Deaktivieren der Leseansicht</span><span class="sxs-lookup"><span data-stu-id="fe34d-153">Opting out of Reading View</span></span>  

<span data-ttu-id="fe34d-154">Wenn Sie der Meinung sind, dass Ihre Inhalte für die Leseansicht nicht geeignet sind, können Sie das folgende Meta-Tag verwenden, um dieses Feature zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="fe34d-154">If you feel your content is not a good fit for Reading view, you can use the following meta tag to opt out of this feature:</span></span>  

```html
<meta name="IE_RM_OFF" content="true">
```  

<span data-ttu-id="fe34d-155">Mit dieser Kategorie wird die Schaltfläche " **Leseansicht** " in der Adressleiste nicht angezeigt, wenn die Benutzer Ihre Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="fe34d-155">With this tag, the **Reading view** button will not appear in the address bar when your users view your page.</span></span>  
