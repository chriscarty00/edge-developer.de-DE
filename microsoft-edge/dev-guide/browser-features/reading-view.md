---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Schauen Sie sich an, wie Microsoft Edge eine Leseansicht für Webseiten bietet, um Add-Free-Lesefunktionen zu ermöglichen.
title: Dev-Leitfaden – Leseansicht
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: e84edb5cc29b644939895f2996c50f3b4ec23379
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566766"
---
# <span data-ttu-id="7b680-104">Leseansicht</span><span class="sxs-lookup"><span data-stu-id="7b680-104">Reading view</span></span>

<span data-ttu-id="7b680-105">Microsoft Edge bietet eine *Leseansicht* für eine optimierte, Buch ähnliche Leseerfahrung von Webseiten ohne Ablenkung von nicht miteinander verknüpften oder anderen sekundären Inhalten auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="7b680-105">Microsoft Edge provides a *reading view* for a more streamlined, book-like reading experience of webpages without the distraction of unrelated or other secondary content on the page.</span></span> <span data-ttu-id="7b680-106">Die Leseansicht kann über die Schaltfläche **Leseansicht** (Buchsymbol) auf der **Adressleiste** (oder mit **STRG**+  +  **UMSCHALT**  +  **R**) ein-oder ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b680-106">Reading view can be toggled on or off from the **Reading view** (book icon) button on the **address bar** (or with **Ctrl** + **Shift** + **R**).</span></span> <span data-ttu-id="7b680-107">In der Leseansicht werden die folgenden Metadaten von einer Seite extrahiert:</span><span class="sxs-lookup"><span data-stu-id="7b680-107">Reading view extracts the following metadata from a page:</span></span>

* <span data-ttu-id="7b680-108">Title</span><span class="sxs-lookup"><span data-stu-id="7b680-108">Title</span></span>
* <span data-ttu-id="7b680-109">Autor</span><span class="sxs-lookup"><span data-stu-id="7b680-109">Author</span></span>
* <span data-ttu-id="7b680-110">Date</span><span class="sxs-lookup"><span data-stu-id="7b680-110">Date</span></span>
* <span data-ttu-id="7b680-111">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="7b680-111">Publisher</span></span>
* <span data-ttu-id="7b680-112">Dominantes Bild (e)</span><span class="sxs-lookup"><span data-stu-id="7b680-112">Dominant image(s)</span></span>
* <span data-ttu-id="7b680-113">Beschriftungen der dominanten Bilder</span><span class="sxs-lookup"><span data-stu-id="7b680-113">Captions of dominant image(s)</span></span>
* <span data-ttu-id="7b680-114">Sekundäre Bilder</span><span class="sxs-lookup"><span data-stu-id="7b680-114">Secondary images</span></span>
* <span data-ttu-id="7b680-115">Haupt Textinhalt der Seite</span><span class="sxs-lookup"><span data-stu-id="7b680-115">Main text content of the page</span></span>
* <span data-ttu-id="7b680-116">Copyright</span><span class="sxs-lookup"><span data-stu-id="7b680-116">Copyright</span></span>

<span data-ttu-id="7b680-117">Benutzer können dann den Seiten Kontrast und den Schriftgrad im Microsoft Edge **Settings** -Panel anpassen.</span><span class="sxs-lookup"><span data-stu-id="7b680-117">Users can then adjust the page contrast and font size from the Microsoft Edge **Settings** panel.</span></span>

## <span data-ttu-id="7b680-118">Extraktion von Metadaten</span><span class="sxs-lookup"><span data-stu-id="7b680-118">Metadata extraction</span></span>


<span data-ttu-id="7b680-119">Hier finden Sie Details zu den Seiten Metadaten, die von der Leseansicht gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="7b680-119">Here are details of the page metadata rendered by reading view.</span></span>

### <span data-ttu-id="7b680-120">Title</span><span class="sxs-lookup"><span data-stu-id="7b680-120">Title</span></span>

<span data-ttu-id="7b680-121">So stellen Sie sicher, dass die Leseansicht den Titel Ihres Artikels rendert:</span><span class="sxs-lookup"><span data-stu-id="7b680-121">To ensure Reading view renders your article's title:</span></span>

* <span data-ttu-id="7b680-122">Einfügen eines **Titel** Elements in die Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="7b680-122">Include a **title** element in your header</span></span>
* <span data-ttu-id="7b680-123">Einfügen eines Meta-Tags</span><span class="sxs-lookup"><span data-stu-id="7b680-123">Include a meta tag with</span></span> `name="title"`
* <span data-ttu-id="7b680-124">Vergleichen Sie den Titeltext in Ihrem Artikel Text mit der Inhaltszeichenfolge Ihres Meta-Tags.</span><span class="sxs-lookup"><span data-stu-id="7b680-124">Match the title text in your article body with the content string of your meta tag.</span></span> <span data-ttu-id="7b680-125">Pipes `|` in der Inhaltszeichenfolge verhindern, dass die Leseransicht aktiv wird, versuchen Sie stattdessen, hypens zu verwenden `-` .</span><span class="sxs-lookup"><span data-stu-id="7b680-125">Pipes `|` in your content string prevent the reader view from becoming active, try using hypens `-` instead.</span></span>

### <span data-ttu-id="7b680-126">Autor</span><span class="sxs-lookup"><span data-stu-id="7b680-126">Author</span></span>

<span data-ttu-id="7b680-127">In der Leseansicht wird nach einem Element gesucht `class = "byline-name"` .</span><span class="sxs-lookup"><span data-stu-id="7b680-127">Reading View will look for an element with `class = "byline-name"`.</span></span> <span data-ttu-id="7b680-128">Bewährte Methode besteht darin, den Autorennamen hinter dem Titel und vor dem Artikel Text zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="7b680-128">Best practice is to place the author name after the title and before the article body.</span></span>

```html
<div class="byline-name">Author name</div>
```

### <span data-ttu-id="7b680-129">Date</span><span class="sxs-lookup"><span data-stu-id="7b680-129">Date</span></span>

<span data-ttu-id="7b680-130">In der Leseansicht werden der Herausgeber und die Datumsinformationen in derselben Zeile zusammen mit zusätzlicher Formatierung gerendert, um diese Informationen hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="7b680-130">Reading view will render the publisher and date information together on the same line, with additional styling to highlight this information.</span></span> <span data-ttu-id="7b680-131">Das Veröffentlichungsdatum des Artikels wird exakt so gerendert, wie es in der Zeichenfolge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7b680-131">The article's publishing date will render exactly as it appears in the string.</span></span> <span data-ttu-id="7b680-132">Die Leseansicht wird nicht in ein bestimmtes Datumsformat konvertiert.</span><span class="sxs-lookup"><span data-stu-id="7b680-132">Reading view does not convert to a specific date format.</span></span>

<span data-ttu-id="7b680-133">Wenn Sie über ein Datum in Ihrem Artikel Text verfügen und es in der Leseansicht rendern möchten, weisen Sie das Element mit dem Datum der Klasse zu `'dateline'` :</span><span class="sxs-lookup"><span data-stu-id="7b680-133">If you have a date in your article body and would like Reading view to render it, assign the element containing the date with the class `'dateline'`:</span></span>

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```

<span data-ttu-id="7b680-134">Verwenden Sie das Meta-Tag, wenn Sie nicht über ein Datum im Artikel Text verfügen, aber die Leseansicht zum Rendern des Datums verwenden möchten `name='displaydate'` :</span><span class="sxs-lookup"><span data-stu-id="7b680-134">If you don't have a date in the article body but would like Reading view to render the date, use the meta tag `name='displaydate'`:</span></span>

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```

### <span data-ttu-id="7b680-135">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="7b680-135">Publisher</span></span>

<span data-ttu-id="7b680-136">In der Leseansicht wird nach dem *Open Graph* -Protokoll gesucht `"og:site_name"` , um die Herausgeberinformationen zu rendern.</span><span class="sxs-lookup"><span data-stu-id="7b680-136">Reading view will look for the *Open Graph* protocol `"og:site_name"` to render the publisher information.</span></span> <span data-ttu-id="7b680-137">Darüber hinaus sucht Sie nach `source_organization` und `publisher` Attribute in einem beliebigen HTML-Tag als sekundärer Indikator für Herausgeberinformationen auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="7b680-137">It also looks for `source_organization` and `publisher` attributes in any html tag as a secondary indicator of publisher information on the page.</span></span> <span data-ttu-id="7b680-138">Der Text des Herausgebers wird mit der URL der Seite über den Hyperlink-Stil "Leseansicht" verknüpft.</span><span class="sxs-lookup"><span data-stu-id="7b680-138">The publisher text will be hyperlinked to the URL of page using the Reading view page hyperlink style.</span></span>

```html
<meta content="Name of organization source" property="og:site_name">
```

### <span data-ttu-id="7b680-139">Images</span><span class="sxs-lookup"><span data-stu-id="7b680-139">Images</span></span>

<span data-ttu-id="7b680-140">In der Leseansicht werden die meisten RAW-Bilder mit Breite >= 400px und Seitenverhältnis >= 1/3 und =< 3,0 erfasst.</span><span class="sxs-lookup"><span data-stu-id="7b680-140">Reading view captures most raw images with width >= 400px and aspect ratio >= 1/3 and =< 3.0.</span></span> <span data-ttu-id="7b680-141">Bilder, die diese Dimensionen nicht erfüllen, werden möglicherweise weiterhin extrahiert, wie Bilder, die kleiner als 400px sind, aber über Beschriftungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="7b680-141">Images that do not meet these dimensions may still be extracted, such as images that are smaller than 400px in width but have captions.</span></span> <span data-ttu-id="7b680-142">Das erste geeignete Bild wird zum dominanten Bild des Artikels.</span><span class="sxs-lookup"><span data-stu-id="7b680-142">The first eligible image becomes the dominant image of the article.</span></span> <span data-ttu-id="7b680-143">Das dominante Bild wird als erster Teil des Inhalts gerendert und erhält die volle Spaltenbreite.</span><span class="sxs-lookup"><span data-stu-id="7b680-143">The dominant image is rendered as the first piece of content and given full column width.</span></span> <span data-ttu-id="7b680-144">Alle folgenden Bilder werden als Inline Bilder innerhalb des Artikels gerendert.</span><span class="sxs-lookup"><span data-stu-id="7b680-144">All following images are rendered as inline images within the article.</span></span>

### <span data-ttu-id="7b680-145">Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="7b680-145">Captions</span></span>

<span data-ttu-id="7b680-146">Bewährte Methode ist das Platzieren von Bildern in [Abbildungs](https://msdn.microsoft.com/library/gg593038(v=vs.85).aspx) Tags mit nicht mehr als zwei geschachtelten [figcaption](https://msdn.microsoft.com/library/gg593037(v=vs.85).aspx) -Tags.</span><span class="sxs-lookup"><span data-stu-id="7b680-146">Best practice is to place images in [figure](https://msdn.microsoft.com/library/gg593038(v=vs.85).aspx) tags with no more than two nested [figcaption](https://msdn.microsoft.com/library/gg593037(v=vs.85).aspx) tags.</span></span>

### <span data-ttu-id="7b680-147">Textkörper</span><span class="sxs-lookup"><span data-stu-id="7b680-147">Body</span></span>

<span data-ttu-id="7b680-148">Um sicherzustellen, dass der gesamte Textkörper Ihrer Seite in der Leseansicht erfasst wird, hilft es, den größten Teil des Artikel Texts auf den gleichen Schriftgrad und die gleiche Dom-Tiefe zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="7b680-148">To ensure that all the body text of your page is captured by Reading view, it helps to keep most of the article text the same font size and DOM depth.</span></span> <span data-ttu-id="7b680-149">Der Leseansicht-Algorithmus ermöglicht eine gewisse Abweichung von dieser Regel, damit Publisher die Freiheit haben, Zeilen oder Wörter hervorheben zu können.</span><span class="sxs-lookup"><span data-stu-id="7b680-149">The reading view algorithm allows for some deviation from this rule so publishers can have the freedom to add emphasis to lines or words.</span></span>

### <span data-ttu-id="7b680-150">Copyright</span><span class="sxs-lookup"><span data-stu-id="7b680-150">Copyright</span></span>

<span data-ttu-id="7b680-151">Leseansicht extrahiert und zeigt Copyright Informationen an, die durch Metatags gekennzeichnet `name = "copyright"` sind, oder wenn keine Meta-Tag-Informationen vorhanden sind, ein Textknoten, der das Copyright (**©**)-Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="7b680-151">Reading view extracts and displays copyright information denoted by meta tags with `name = "copyright"`, or if no meta tag information exists, a text node that contains the copyright (**©**) symbol.</span></span> <span data-ttu-id="7b680-152">In der Leseansicht werden die Copyright Informationen am Ende des Haupttexts des Artikels angezeigt, wobei ein kleinerer Schriftgrad als der Hauptteil des Texts formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="7b680-152">Reading view displays copyright information at the end of the article main body, styled using a smaller font size than the main body text.</span></span>

```html
<meta name="copyright" content="Your copyright information">
```

## <span data-ttu-id="7b680-153">Deaktivieren der Leseansicht</span><span class="sxs-lookup"><span data-stu-id="7b680-153">Opting out of Reading View</span></span>


<span data-ttu-id="7b680-154">Wenn Sie der Meinung sind, dass Ihre Inhalte für die Leseansicht nicht geeignet sind, können Sie das folgende Meta-Tag verwenden, um dieses Feature zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="7b680-154">If you feel your content is not a good fit for Reading view, you can use the following meta tag to opt out of this feature:</span></span>

```html
<meta name="IE_RM_OFF" content="true">
```

<span data-ttu-id="7b680-155">Mit dieser Kategorie wird die Schaltfläche " **Leseansicht** " in der Adressleiste nicht angezeigt, wenn die Benutzer Ihre Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b680-155">With this tag, the **Reading view** button will not appear in the address bar when your users view your page.</span></span>
