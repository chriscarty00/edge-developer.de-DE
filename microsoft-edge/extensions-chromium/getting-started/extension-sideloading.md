---
description: Testen Sie Ihre Erweiterung, indem Sie Sie im Browser Sideloading
title: Querladen ihrer Durchwahl
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104773"
---
# <span data-ttu-id="5f3cf-104">Querladen einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="5f3cf-104">Sideload an extension</span></span>

<span data-ttu-id="5f3cf-105">Während der Entwicklung können Sie den Microsoft Edge \(Chrom \)-Browser verwenden, um Ihre Erweiterung sicher auszuführen und zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-105">During development, you may use the Microsoft Edge \(Chromium\) browser to run and debug your extension safely.</span></span> <span data-ttu-id="5f3cf-106">Indem Sie Ihre Erweiterung lokal in Ihrem Browser Sideloading, können Sie Ihre Erweiterung ausführen und testen.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-106">By sideloading your extension locally in your browser, you can run and test your extension.</span></span> <span data-ttu-id="5f3cf-107">In diesem Artikel wird erläutert, wie Sie Erweiterungen in Microsoft Edge querladen.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-107">This article explains how to sideload extensions into Microsoft Edge.</span></span>

<span data-ttu-id="5f3cf-108">Führen Sie die folgenden Schritte aus, um die Erweiterung zu querladen.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-108">To sideload your extension, follow these steps.</span></span>

1.  <span data-ttu-id="5f3cf-109">Öffnen `edge://extensions` Sie die Seite, indem Sie die drei Punkte oben im Browser auswählen und dann **Erweiterungen**auswählen.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-109">Open the `edge://extensions` page by choosing the three dots at the top of your browser, and then selecting **Extensions**.</span></span>

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Öffnen der Seite &quot;Edge://Extensions&quot;":::
          <span data-ttu-id="5f3cf-111">Öffnen der Seite "Edge://Extensions"</span><span class="sxs-lookup"><span data-stu-id="5f3cf-111">Open the edge://extensions page</span></span> :::image-end:::

1.  <span data-ttu-id="5f3cf-112">Aktivieren Sie auf der Seite Erweiterungsverwaltung unter `edge://extensions` den **Entwicklermodus** mithilfe der Umschaltfläche unten links auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-112">On the extension management page at `edge://extensions`, turn on **Developer mode** using the toggle at the bottom left of the page.</span></span>

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Öffnen der Seite &quot;Edge://Extensions&quot;":::
          <span data-ttu-id="5f3cf-114">Aktivieren des Entwicklermodus</span><span class="sxs-lookup"><span data-stu-id="5f3cf-114">Turn on Developer Mode</span></span> :::image-end:::

1.  <span data-ttu-id="5f3cf-115">Wenn Sie Ihre Erweiterung zum ersten Mal installieren, wählen Sie **Laden entpackt**aus.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-115">When installing your extension for the first time, choose **Load Unpacked**.</span></span>  <span data-ttu-id="5f3cf-116">Sie werden aufgefordert, das Verzeichnis mit den Quelldateien für die Erweiterung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-116">You'll be prompted for the directory with your extension source files.</span></span>  <span data-ttu-id="5f3cf-117">Ihre Erweiterung wird in Ihrem Browser installiert, ähnlich wie im Store installierte Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-117">Your extension is installed in your browser, similar to extensions installed from the store.</span></span>  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Öffnen der Seite &quot;Edge://Extensions&quot;":::
          <span data-ttu-id="5f3cf-119">Seite "installierte Erweiterungen" mit einer quer geladene-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="5f3cf-119">Installed extensions page showing a sideloaded extension</span></span> :::image-end:::

<span data-ttu-id="5f3cf-120">Während der Entwicklung müssen Sie möglicherweise auch die folgenden Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-120">During development, you may also need to perform the following tasks.</span></span>
* <span data-ttu-id="5f3cf-121">Aktualisieren Sie die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-121">Update the extension.</span></span> <span data-ttu-id="5f3cf-122">Navigieren `edge://extensions` Sie zu, und wählen Sie dann **Reload** aus, um Ihre Erweiterung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-122">Navigate to `edge://extensions`, and then select **Reload** to update your extension.</span></span>  
* <span data-ttu-id="5f3cf-123">Entfernen Sie die Erweiterung aus Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-123">Remove the extension from your browser.</span></span> <span data-ttu-id="5f3cf-124">Navigieren Sie zu `edge://extensions` , und wählen Sie dann `Remove` Ihre Erweiterung aus.</span><span class="sxs-lookup"><span data-stu-id="5f3cf-124">Navigate to `edge://extensions`, and then select `Remove` on your extension.</span></span>