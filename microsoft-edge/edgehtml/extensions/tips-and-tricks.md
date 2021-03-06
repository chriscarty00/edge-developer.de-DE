---
description: Erfahren Sie mehr über einige praktische Tipps und Tricks zu Microsoft Edge-Erweiterungen
title: Tipps und Tricks | Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, javascript, developer, extensions
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8a5ea19152f5524d86d17d6f978c677c45f8f3a8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399351"
---
# <a name="tips-and-tricks"></a><span data-ttu-id="edf94-104">Tipps und Tricks</span><span class="sxs-lookup"><span data-stu-id="edf94-104">Tips and tricks</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="edf94-105">Unabhängig davon, ob Sie derzeit an einer Microsoft Edge-Erweiterung arbeiten oder bereits eine erweiterung veröffentlicht haben, sind die folgenden Tipps und Tricks hilfreich.</span><span class="sxs-lookup"><span data-stu-id="edf94-105">Whether you're currently working on a Microsoft Edge extension or have already published one, the following tips and tricks might come in handy.</span></span>  

## <a name="get-a-direct-link-to-your-extension-in-the-microsoft-store"></a><span data-ttu-id="edf94-106">Einen direkten Link zu Ihrer Erweiterung im Microsoft Store erhalten</span><span class="sxs-lookup"><span data-stu-id="edf94-106">Get a direct link to your extension in the Microsoft Store</span></span>  

<span data-ttu-id="edf94-107">Im Windows Dev Center-Dashboard finden Sie einen direkten Link zu Ihrer Erweiterung im Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="edf94-107">In the Windows Dev Center dashboard, you can find a direct link to your extension in the Microsoft Store.</span></span>  <span data-ttu-id="edf94-108">Dieser Link kann für Werbung und die Freigabe Ihrer Erweiterung hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="edf94-108">This link can be useful for advertising and sharing out your extension.</span></span>  

<span data-ttu-id="edf94-109">Nachdem Sie sich beim Windows Dev Center anmelden und über das Dashboard zu Ihrer Erweiterung navigieren, finden Sie auf der Seite App-Identität den Link in der **Linkzeile Store-Protokoll:**</span><span class="sxs-lookup"><span data-stu-id="edf94-109">After logging in to the Windows Dev Center and navigating to your extension through the dashboard, on the App identity page you’ll find the link in the **Store protocol link** row:</span></span>  

![Speicherprotokollverknüpfung](./media/store-link.png)  
 
## <a name="make-sure-youre-following-the-microsoft-store-policy"></a><span data-ttu-id="edf94-111">Stellen Sie sicher, dass Sie die Microsoft Store-Richtlinie folgen</span><span class="sxs-lookup"><span data-stu-id="edf94-111">Make sure you’re following the Microsoft Store Policy</span></span>  

<span data-ttu-id="edf94-112">Beachten Sie beim Erstellen Ihrer Erweiterung die Richtlinien für die Übermittlung an den Microsoft Store, die in der [Microsoft Store-Richtlinie hervorgehoben sind.](/windows/uwp/publish/store-policies)</span><span class="sxs-lookup"><span data-stu-id="edf94-112">When creating your extension, make sure you keep in mind the guidelines for submitting to the Microsoft Store highlighted in the [Microsoft Store Policy](/windows/uwp/publish/store-policies).</span></span>  
 
<span data-ttu-id="edf94-113">Microsoft Edge-Erweiterungen haben auch einen zusätzlichen Satz von Richtlinien, die hier zu [folgen sind.](/windows/uwp/publish/store-policies#pol_10_12)</span><span class="sxs-lookup"><span data-stu-id="edf94-113">Microsoft Edge extensions also have an additional set of policies to follow seen [here](/windows/uwp/publish/store-policies#pol_10_12).</span></span>  

## <a name="improve-your-extensions-discoverability-in-the-microsoft-store"></a><span data-ttu-id="edf94-114">Verbessern sie die Aufdingbarkeit Ihrer Erweiterung im Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="edf94-114">Improve your extension’s discoverability in the Microsoft Store</span></span>  

<span data-ttu-id="edf94-115">Sie können Ihrer Erweiterungsübermittlung Schlüsselwörter hinzufügen, um die Aufsuchung durch Suchen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="edf94-115">You can add keywords to your extension submission to improve its discoverability through searches.</span></span>  <span data-ttu-id="edf94-116">Beispiele: `Microsoft Edge Extensions` und `name of my extension`.</span><span class="sxs-lookup"><span data-stu-id="edf94-116">For example, `Microsoft Edge Extensions` and `name of my extension`.</span></span>  

<span data-ttu-id="edf94-117">Dies kann im Windows Dev Center unter dem Beschreibungsabschnitt Ihrer Erweiterung geschehen.</span><span class="sxs-lookup"><span data-stu-id="edf94-117">This can be done in the Windows Dev Center under the description section of your extension.</span></span>  <span data-ttu-id="edf94-118">Diese Schlüsselwörter müssen für jede Sprache hinzugefügt werden, die von Ihrer Erweiterung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="edf94-118">These keywords will need to be added for every language your extension supports.</span></span>  

![Senden einer Antwort auf eine Rezension mithilfe von Schlüsselwörtern](./media/keywords.png)  

## <a name="automate-your-submission-to-the-microsoft-store"></a><span data-ttu-id="edf94-120">Automatisieren Der Übermittlung an den Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="edf94-120">Automate your submission to the Microsoft Store</span></span>  

<span data-ttu-id="edf94-121">Sie können Ihre Übermittlungen an den Microsoft Store automatisieren und optimieren, indem Sie die neue Microsoft Store-Übermittlungs-API verwenden, mit der Sie Apps/Spiele, Add-Ons \(In-App-Käufe\) und Paketflüge über eine REST-API aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="edf94-121">You can automate and streamline your submissions to the Microsoft Store by using the new Microsoft Store Submission API, which allows you to update apps/games, add-ons \(in-app purchases\), and package flights through a REST API.</span></span>  <span data-ttu-id="edf94-122">Sehen Sie sich die [Dokumentation und Beispiele an,](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) oder verwenden Sie die Open Source [Submission API VSTS-Erweiterung,](https://github.com/Microsoft/windows-dev-center-vsts-extension) um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="edf94-122">Check out the [documentation and samples](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) or use the open source [Submission API VSTS extension](https://github.com/Microsoft/windows-dev-center-vsts-extension) to get started.</span></span>  

## <a name="use-the-windows-feedback-hub-to-gather-feedbackreviewsfeature-requests"></a><span data-ttu-id="edf94-123">Verwenden des Windows Feedback Hub zum Sammeln von Feedback/Rezensionen/Featureanforderungen</span><span class="sxs-lookup"><span data-stu-id="edf94-123">Use the Windows Feedback Hub to gather feedback/reviews/feature requests</span></span>  

<span data-ttu-id="edf94-124">Sie können Benutzer zur Windows Feedback Hub-Unterkategorie für Ihre Erweiterung durch Einbetten eines Links, der darauf verweist, an die Windows Feedback Hub-Unterkategorie weiterverstellen.</span><span class="sxs-lookup"><span data-stu-id="edf94-124">You can direct users to the Windows Feedback Hub subcategory for your extension by embedding a link that points to it.</span></span>  <span data-ttu-id="edf94-125">Dieser Link muss im folgenden Format erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="edf94-125">This link will need to be created using the following format:</span></span>  

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

<span data-ttu-id="edf94-126">Sie müssen durch den `<PFN>` Paketfamiliennamen ihrer Erweiterung ersetzen.</span><span class="sxs-lookup"><span data-stu-id="edf94-126">You will need to substitute `<PFN>` with the Package Family Name of you extension.</span></span>  <span data-ttu-id="edf94-127">Dies finden Sie im **Abschnitt App-Identität** für Ihre Erweiterung im Windows Dev Center.</span><span class="sxs-lookup"><span data-stu-id="edf94-127">This can be found under the **App identity** section for your extension in the Windows Dev Center.</span></span>  

## <a name="check-out-your-ratings-and-reviews"></a><span data-ttu-id="edf94-128">Sehen Sie sich Ihre Bewertungen und Rezensionen an</span><span class="sxs-lookup"><span data-stu-id="edf94-128">Check out your ratings and reviews</span></span>  

<span data-ttu-id="edf94-129">Melden Sie sich regelmäßig an, um Ihre Benutzerbewertungen und Bewertungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="edf94-129">Log in regularly to check your user reviews and ratings.</span></span>  <span data-ttu-id="edf94-130">Während die UWP-App nur Informationen über den aktuellen Benutzermarkt hat, zeigt die Anmeldung beim Windows Dev Center die durchschnittliche Bewertung in allen Märkten an.</span><span class="sxs-lookup"><span data-stu-id="edf94-130">While the UWP app will only have info on the current user market, logging into the Windows Dev Center will display average rating across all markets.</span></span>  

## <a name="respond-to-user-reviews"></a><span data-ttu-id="edf94-131">Antworten auf Benutzerrezensionen</span><span class="sxs-lookup"><span data-stu-id="edf94-131">Respond to user reviews</span></span>  

<span data-ttu-id="edf94-132">Sie können auf Benutzerbewertungen im Microsoft Store über das Windows Dev Center-Dashboard antworten.</span><span class="sxs-lookup"><span data-stu-id="edf94-132">You can respond to user reviews in the Microsoft Store through the Windows Dev Center's dashboard.</span></span>  <span data-ttu-id="edf94-133">Navigieren Sie zu Ihrer Erweiterung, und wählen Sie unter Analytics **Rezensionen aus.**</span><span class="sxs-lookup"><span data-stu-id="edf94-133">Navigate to your extension and under Analytics select **Reviews**.</span></span>  <span data-ttu-id="edf94-134">Unter jeder Rezension wird ein Link angezeigt, mit dem Sie direkt auf den Kunden antworten können.</span><span class="sxs-lookup"><span data-stu-id="edf94-134">A link will appear underneath each review that will allow you to respond directly to the customer.</span></span>  <span data-ttu-id="edf94-135">Dieser Kommunikationskanal ermöglicht Es Ihnen, Feedback, Lösungen oder ein Dankeschön für die Rezension zu senden!</span><span class="sxs-lookup"><span data-stu-id="edf94-135">This channel of communication enables you to offer feedback, resolutions, or send a thank you for the review!</span></span>  

![Reagieren auf die Benutzerüberprüfung](./media/reviews.png)  
