---
description: Testen Der Erweiterung durch Querladen im Browser
title: Querladen der Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge Chromium, Webentwicklung, html, css, javascript, Entwickler, Erweiterungen
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104773"
---
# <span data-ttu-id="11557-104">Eine Erweiterung querladen</span><span class="sxs-lookup"><span data-stu-id="11557-104">Sideload an extension</span></span>

<span data-ttu-id="11557-105">Während der Entwicklung können Sie den browser Microsoft Edge \(Chromium\) verwenden, um die Erweiterung sicher zu ausführen und zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="11557-105">During development, you may use the Microsoft Edge \(Chromium\) browser to run and debug your extension safely.</span></span> <span data-ttu-id="11557-106">Indem Sie Ihre Erweiterung lokal in Ihrem Browser querladen, können Sie Ihre Erweiterung ausführen und testen.</span><span class="sxs-lookup"><span data-stu-id="11557-106">By sideloading your extension locally in your browser, you can run and test your extension.</span></span> <span data-ttu-id="11557-107">In diesem Artikel wird das Querladen von Erweiterungen in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="11557-107">This article explains how to sideload extensions into Microsoft Edge.</span></span>

<span data-ttu-id="11557-108">Führen Sie die folgenden Schritte aus, um die Erweiterung quer zu laden.</span><span class="sxs-lookup"><span data-stu-id="11557-108">To sideload your extension, follow these steps.</span></span>

1.  <span data-ttu-id="11557-109">Öffnen Sie die Seite, indem Sie die drei Punkte oben im Browser auswählen und dann `edge://extensions` **Erweiterungen auswählen.**</span><span class="sxs-lookup"><span data-stu-id="11557-109">Open the `edge://extensions` page by choosing the three dots at the top of your browser, and then selecting **Extensions**.</span></span>

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Öffnen der edge://extensions Seite":::
          <span data-ttu-id="11557-111">Öffnen der edge://extensions Seite</span><span class="sxs-lookup"><span data-stu-id="11557-111">Open the edge://extensions page</span></span> :::image-end:::

1.  <span data-ttu-id="11557-112">Aktivieren Sie auf der Seite Erweiterungsverwaltung unter den Entwicklermodus mit dem Umschalter unten `edge://extensions` links auf der Seite. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="11557-112">On the extension management page at `edge://extensions`, turn on **Developer mode** using the toggle at the bottom left of the page.</span></span>

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Aktivieren des Entwicklermodus":::
          <span data-ttu-id="11557-114">Aktivieren des Entwicklermodus</span><span class="sxs-lookup"><span data-stu-id="11557-114">Turn on Developer Mode</span></span> :::image-end:::

1.  <span data-ttu-id="11557-115">Wählen Sie bei der ersten Installation der Erweiterung die Option **Entpackt laden aus.**</span><span class="sxs-lookup"><span data-stu-id="11557-115">When installing your extension for the first time, choose **Load Unpacked**.</span></span>  <span data-ttu-id="11557-116">Sie werden zur Eingabe des Verzeichnisses mit ihren Erweiterungsquellendateien aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="11557-116">You'll be prompted for the directory with your extension source files.</span></span>  <span data-ttu-id="11557-117">Ihre Erweiterung wird in Ihrem Browser installiert, ähnlich wie erweiterungen, die aus dem Store installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="11557-117">Your extension is installed in your browser, similar to extensions installed from the store.</span></span>  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Seite Installierte Erweiterungen mit einer seitengeladenen Erweiterung":::
          <span data-ttu-id="11557-119">Seite "Installierte Erweiterungen" mit einer seitengeladenen Erweiterung</span><span class="sxs-lookup"><span data-stu-id="11557-119">Installed extensions page showing a sideloaded extension</span></span> :::image-end:::

<span data-ttu-id="11557-120">Während der Entwicklung müssen Sie möglicherweise auch die folgenden Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="11557-120">During development, you may also need to perform the following tasks.</span></span>
* <span data-ttu-id="11557-121">Aktualisieren Sie die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="11557-121">Update the extension.</span></span> <span data-ttu-id="11557-122">Navigieren Sie zu `edge://extensions` , und wählen Sie dann Erneut laden **aus,** um Ihre Erweiterung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="11557-122">Navigate to `edge://extensions`, and then select **Reload** to update your extension.</span></span>  
* <span data-ttu-id="11557-123">Entfernen Sie die Erweiterung aus Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="11557-123">Remove the extension from your browser.</span></span> <span data-ttu-id="11557-124">Navigieren Sie `edge://extensions` zu , und wählen Sie dann die Erweiterung `Remove` aus.</span><span class="sxs-lookup"><span data-stu-id="11557-124">Navigate to `edge://extensions`, and then select `Remove` on your extension.</span></span>