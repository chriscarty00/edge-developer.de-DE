---
description: Erfahren Sie mehr über einige praktische Tipps und Tricks zu Microsoft Edge-Erweiterungen.
title: Tipps und Tricks | Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd512085f13b76c5a8e474301ef296612eeb0414
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233796"
---
# <span data-ttu-id="45eb0-104">Tipps und Tricks</span><span class="sxs-lookup"><span data-stu-id="45eb0-104">Tips and tricks</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="45eb0-105">Ganz gleich, ob Sie derzeit an einer Microsoft Edge-Erweiterung arbeiten oder eine bereits veröffentlicht haben, können sich die folgenden Tipps und Tricks als hilfreich erweisen.</span><span class="sxs-lookup"><span data-stu-id="45eb0-105">Whether you're currently working on a Microsoft Edge extension or have already published one, the following tips and tricks might come in handy.</span></span>

## <span data-ttu-id="45eb0-106">Abrufen eines direkten Links zu ihrer Erweiterung im Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="45eb0-106">Get a direct link to your extension in the Microsoft Store</span></span>

<span data-ttu-id="45eb0-107">Im Windows dev Center-Dashboard können Sie einen direkten Link zu ihrer Erweiterung im Microsoft Store finden.</span><span class="sxs-lookup"><span data-stu-id="45eb0-107">In the Windows Dev Center dashboard, you can find a direct link to your extension in the Microsoft Store.</span></span> <span data-ttu-id="45eb0-108">Dieser Link kann für Werbung und die Freigabe ihrer Erweiterung nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="45eb0-108">This link can be useful for advertising and sharing out your extension.</span></span>

<span data-ttu-id="45eb0-109">Nachdem Sie sich beim Windows dev Center angemeldet haben und über das Dashboard zu ihrer Erweiterung navigieren, finden Sie auf der Seite App-Identität den Link in der Zeile **Store Protocol Link** :</span><span class="sxs-lookup"><span data-stu-id="45eb0-109">After logging in to the Windows Dev Center and navigating to your extension through the dashboard, on the App identity page you’ll find the link in the **Store protocol link** row:</span></span>

![Link zum Store-Protokoll](./media/store-link.png)
 
## <span data-ttu-id="45eb0-111">Sicherstellen, dass Sie der Microsoft Store-Richtlinie folgen</span><span class="sxs-lookup"><span data-stu-id="45eb0-111">Make sure you’re following the Microsoft Store Policy</span></span>

<span data-ttu-id="45eb0-112">Achten Sie beim Erstellen Ihrer Erweiterung darauf, dass Sie die Richtlinien für die Übermittlung an den Microsoft Store berücksichtigen, die in der [Microsoft Store-Richtlinie](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx)hervorgehoben sind.</span><span class="sxs-lookup"><span data-stu-id="45eb0-112">When creating your extension, make sure you keep in mind the guidelines for submitting to the Microsoft Store highlighted in the [Microsoft Store Policy](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span></span> 
 
<span data-ttu-id="45eb0-113">Microsoft Edge-Erweiterungen verfügen auch über eine Reihe weiterer Richtlinien, die [hier](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12)zu sehen sind.</span><span class="sxs-lookup"><span data-stu-id="45eb0-113">Microsoft Edge extensions also have an additional set of policies to follow seen [here](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span></span>

## <span data-ttu-id="45eb0-114">Verbessern der Auffindbarkeit ihrer Erweiterung im Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="45eb0-114">Improve your extension’s discoverability in the Microsoft Store</span></span>

<span data-ttu-id="45eb0-115">Sie können Ihrer Erweiterungs Übermittlung Stichwörter hinzufügen, um die Auffindbarkeit durchsuchen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="45eb0-115">You can add keywords to your extension submission to improve its discoverability through searches.</span></span> <span data-ttu-id="45eb0-116">Beispiel: "Microsoft Edge Extensions" und "Name meiner Erweiterung".</span><span class="sxs-lookup"><span data-stu-id="45eb0-116">For example, "Microsoft Edge Extensions" and "name of my extension".</span></span> 

<span data-ttu-id="45eb0-117">Dies kann im Windows dev Center unter dem Abschnitt Beschreibung der Erweiterung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="45eb0-117">This can be done in the Windows Dev Center under the description section of your extension.</span></span> <span data-ttu-id="45eb0-118">Diese Schlüsselwörter müssen für jede Sprache hinzugefügt werden, die von der Erweiterung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="45eb0-118">These keywords will need to be added for every language your extension supports.</span></span>

![Senden einer Antwort auf eine Rezension – Stichwörter](./media/keywords.png)

## <span data-ttu-id="45eb0-120">Automatisieren der Übermittlung an den Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="45eb0-120">Automate your submission to the Microsoft Store</span></span>

<span data-ttu-id="45eb0-121">Mithilfe der neuen Microsoft Store-Übermittlungs-API, mit der Sie Apps/Spiele, Add-ons (in-App-Käufe) und Flight-Pakete über eine Ruhe-API aktualisieren können, können Sie Ihre Übermittlungen an den Microsoft Store automatisieren und optimieren.</span><span class="sxs-lookup"><span data-stu-id="45eb0-121">You can automate and streamline your submissions to the Microsoft Store by using the new Microsoft Store Submission API, which allows you to update apps/games, add-ons (in-app purchases), and package flights through a REST API.</span></span> <span data-ttu-id="45eb0-122">Schauen Sie sich die [Dokumentation und Beispiele](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) an, oder verwenden Sie die Open Source [Submission API VSTS-Erweiterung](https://github.com/Microsoft/windows-dev-center-vsts-extension) , um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="45eb0-122">Check out the [documentation and samples](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) or use the open source [Submission API VSTS extension](https://github.com/Microsoft/windows-dev-center-vsts-extension) to get started.</span></span>

## <span data-ttu-id="45eb0-123">Verwenden des Windows-Feedback-Hubs zum Sammeln von Feedback/Rezensionen/Funktionsanforderungen</span><span class="sxs-lookup"><span data-stu-id="45eb0-123">Use the Windows Feedback Hub to gather feedback/reviews/feature requests</span></span>

<span data-ttu-id="45eb0-124">Sie können Benutzer an die Windows-Feedback-Hub-Unterkategorie für Ihre Erweiterung weiterleiten, indem Sie einen Link einbetten, der darauf verweist.</span><span class="sxs-lookup"><span data-stu-id="45eb0-124">You can direct users to the Windows Feedback Hub subcategory for your extension by embedding a link that points to it.</span></span> <span data-ttu-id="45eb0-125">Dieser Link muss mit dem folgenden Format erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="45eb0-125">This link will need to be created using the following format:</span></span> 

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

<span data-ttu-id="45eb0-126">Sie müssen `<PFN>` den Namen der paketfamilie der Erweiterung ersetzen.</span><span class="sxs-lookup"><span data-stu-id="45eb0-126">You will need to substitute `<PFN>` with the Package Family Name of you extension.</span></span> <span data-ttu-id="45eb0-127">Diese finden Sie im Abschnitt **App Identity** für Ihre Erweiterung im Windows dev Center.</span><span class="sxs-lookup"><span data-stu-id="45eb0-127">This can be found under the **App identity** section for your extension in the Windows Dev Center.</span></span>

## <span data-ttu-id="45eb0-128">Sehen Sie sich Ihre Bewertungen und Bewertungen an</span><span class="sxs-lookup"><span data-stu-id="45eb0-128">Check out your ratings and reviews</span></span>

<span data-ttu-id="45eb0-129">Melden Sie sich regelmäßig an, um die Bewertungen und Bewertungen ihrer Nutzer zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="45eb0-129">Log in regularly to check your user reviews and ratings.</span></span> <span data-ttu-id="45eb0-130">Während die UWP-app nur Informationen auf dem aktuellen Nutzer Markt hat, wird bei der Anmeldung beim Windows dev Center die durchschnittliche Bewertung in allen Märkten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45eb0-130">While the UWP app will only have info on the current user market, logging into the Windows Dev Center will display average rating across all markets.</span></span>

## <span data-ttu-id="45eb0-131">Antworten auf Nutzer Rezensionen</span><span class="sxs-lookup"><span data-stu-id="45eb0-131">Respond to user reviews</span></span>

<span data-ttu-id="45eb0-132">Sie können im Microsoft Store über das Windows dev Center-Dashboard auf Benutzer Rezensionen Antworten.</span><span class="sxs-lookup"><span data-stu-id="45eb0-132">You can respond to user reviews in the Microsoft Store through the Windows Dev Center's dashboard.</span></span> <span data-ttu-id="45eb0-133">Navigieren Sie zu ihrer Erweiterung, und wählen Sie unter Analytics die Option **Bewertungen**aus.</span><span class="sxs-lookup"><span data-stu-id="45eb0-133">Navigate to your extension and under Analytics select **Reviews**.</span></span> <span data-ttu-id="45eb0-134">Unter jeder Bewertung wird ein Link angezeigt, mit dem Sie direkt auf den Kunden Antworten können.</span><span class="sxs-lookup"><span data-stu-id="45eb0-134">A link will appear underneath each review that will allow you to respond directly to the customer.</span></span> <span data-ttu-id="45eb0-135">Dieser Kommunikationskanal bietet Ihnen Feedback, Auflösungen oder ein Dankeschön für die Rezension!</span><span class="sxs-lookup"><span data-stu-id="45eb0-135">This channel of communication enables you to offer feedback, resolutions, or send a thank you for the review!</span></span>

![Senden einer Antwort auf eine Überprüfung](./media/reviews.png)
