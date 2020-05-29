---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Erfahren Sie, wie die Web-Benachrichtigungs-API verwendet werden kann, damit Websites Benutzer Benachrichtigungen außerhalb des Kontexts des Microsoft Edge-Browsers senden können.
title: Dev-Leitfaden – webbenachrichtigungs-API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/18/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: da563a333491ef699925adec6f97b3c21d3e54a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567105"
---
# <span data-ttu-id="3c354-104">Web-Benachrichtigungs-API</span><span class="sxs-lookup"><span data-stu-id="3c354-104">Web Notifications API</span></span>

<span data-ttu-id="3c354-105">Mit der Web-Benachrichtigungs-API können Websites Benutzer Benachrichtigungen außerhalb des Kontexts einer Webseite innerhalb des Microsoft Edge-Browsers senden.</span><span class="sxs-lookup"><span data-stu-id="3c354-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span> <span data-ttu-id="3c354-106">Ein Beispiel für dieses Feature in Aktion wäre eine Messaging-Anwendung wie Skype.</span><span class="sxs-lookup"><span data-stu-id="3c354-106">An example of this feature in action would be with a messaging application like Skype.</span></span> <span data-ttu-id="3c354-107">Wenn ein Benutzer eine neue Nachricht erhalten würde, wird eine Benachrichtigung auf dem Desktop angezeigt, in der Sie über die Nachricht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="3c354-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span> <span data-ttu-id="3c354-108">Web-Benachrichtigungen sind vollständig in die Benachrichtigungs Plattform und das Wartungs Center in Windows 10 integriert.</span><span class="sxs-lookup"><span data-stu-id="3c354-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span> 

## <span data-ttu-id="3c354-109">Erstellen einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="3c354-109">Creating a notification</span></span>

<span data-ttu-id="3c354-110">Die folgende CodePen erstellt eine Pseudo-Skype-Benachrichtigung, indem Sie ein [`Notification`](https://msdn.microsoft.com/library/mt710818) Objekt mit den Optionen "," und "Optionen" Erstellen [`title`](https://msdn.microsoft.com/library/mt710826) [`icon`](https://msdn.microsoft.com/library/mt710814) [`body`](https://msdn.microsoft.com/library/mt710811) :</span><span class="sxs-lookup"><span data-stu-id="3c354-110">The CodePen below creates a mock Skype notification by making a [`Notification`](https://msdn.microsoft.com/library/mt710818) object with the [`title`](https://msdn.microsoft.com/library/mt710826), [`icon`](https://msdn.microsoft.com/library/mt710814), and [`body`](https://msdn.microsoft.com/library/mt710811) options set:</span></span>


<iframe height='295' scrolling='no' title='<span data-ttu-id="3c354-111">Web-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="3c354-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="3c354-112">Lesen Sie die Stift <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> -webbenachrichtigungen </a> von Microsoft Edge docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) auf <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="3c354-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span>
</iframe>

<span data-ttu-id="3c354-113">Es wird dringend empfohlen, `icon` für jede Benachrichtigung eine Angabe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3c354-113">It is strongly recommended that an `icon` be specified for each notification.</span></span> <span data-ttu-id="3c354-114">Dies verbessert nicht nur eine Benachrichtigung aus Sicht einer Benutzeroberfläche, sondern hilft auch, Benutzer darüber zu informieren, von wo aus die Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c354-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>

<span data-ttu-id="3c354-115">Schauen Sie sich das folgende Video an, um eine exemplarische Vorgehensweise zum Erstellen einer webbenachrichtigung und zum Anzeigen des Verhaltens in Windows 10 zu sehen!</span><span class="sxs-lookup"><span data-stu-id="3c354-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### <span data-ttu-id="3c354-116">Benachrichtigungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c354-116">Notification properties</span></span>

<span data-ttu-id="3c354-117">Benachrichtigungen können mit den folgenden Optionen eingestellt werden:</span><span class="sxs-lookup"><span data-stu-id="3c354-117">Notifications can be set with the following options:</span></span>

<span data-ttu-id="3c354-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3c354-118">Property</span></span> | <span data-ttu-id="3c354-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c354-119">Description</span></span>
:-------- | :----------
[<span data-ttu-id="3c354-120">body</span><span class="sxs-lookup"><span data-stu-id="3c354-120">body</span></span>](https://msdn.microsoft.com/library/mt710811) | <span data-ttu-id="3c354-121">Der Textkörper der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="3c354-121">The body text of the notification.</span></span>
[<span data-ttu-id="3c354-122">dir</span><span class="sxs-lookup"><span data-stu-id="3c354-122">dir</span></span>](https://msdn.microsoft.com/library/mt710813) | <span data-ttu-id="3c354-123">Die Richtung des Texts der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="3c354-123">The direction of the notification's text.</span></span>
[<span data-ttu-id="3c354-124">icon</span><span class="sxs-lookup"><span data-stu-id="3c354-124">icon</span></span>](https://msdn.microsoft.com/library/mt710814) | <span data-ttu-id="3c354-125">Die URL der Benachrichtigung, die für das zugehörige Symbol verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c354-125">The notification's URL that is used for its icon.</span></span>
[<span data-ttu-id="3c354-126">lang</span><span class="sxs-lookup"><span data-stu-id="3c354-126">lang</span></span>](https://msdn.microsoft.com/library/mt710815) | <span data-ttu-id="3c354-127">Die Sprache der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="3c354-127">The language of the notification.</span></span>
[<span data-ttu-id="3c354-128">Berechtigungs</span><span class="sxs-lookup"><span data-stu-id="3c354-128">permission</span></span>](https://msdn.microsoft.com/library/mt670637) | <span data-ttu-id="3c354-129">Die aktuelle benachrichtigungsanzeige Berechtigung, die der Benutzer für den aktuellen Ursprung gewährt hat.</span><span class="sxs-lookup"><span data-stu-id="3c354-129">The current notification display permission the user has granted for the current origin.</span></span>
[<span data-ttu-id="3c354-130">tag</span><span class="sxs-lookup"><span data-stu-id="3c354-130">tag</span></span>](https://msdn.microsoft.com/library/mt710825) | <span data-ttu-id="3c354-131">Das Tag der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="3c354-131">The tag of the notification.</span></span>
[<span data-ttu-id="3c354-132">title</span><span class="sxs-lookup"><span data-stu-id="3c354-132">title</span></span>](https://msdn.microsoft.com/library/mt710826) | <span data-ttu-id="3c354-133">Der Titel der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="3c354-133">The title of the notification.</span></span>

### <span data-ttu-id="3c354-134">Benachrichtigungsereignisse</span><span class="sxs-lookup"><span data-stu-id="3c354-134">Notification events</span></span>

<span data-ttu-id="3c354-135">Die folgenden Ereignisse werden für das [`Notification`](https://msdn.microsoft.com/library/mt710818) Objekt verwendet:</span><span class="sxs-lookup"><span data-stu-id="3c354-135">The following events are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="3c354-136">Ereignis</span><span class="sxs-lookup"><span data-stu-id="3c354-136">Event</span></span> | <span data-ttu-id="3c354-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c354-137">Description</span></span>
:-------- | :----------
[<span data-ttu-id="3c354-138">OnClick</span><span class="sxs-lookup"><span data-stu-id="3c354-138">onclick</span></span>](https://msdn.microsoft.com/library/mt712180) | <span data-ttu-id="3c354-139">Wird ausgelöst, wenn der Benutzer auf eine Benachrichtigung klickt.</span><span class="sxs-lookup"><span data-stu-id="3c354-139">Fires when a notification is clicked by the user.</span></span>
[<span data-ttu-id="3c354-140">OnClose</span><span class="sxs-lookup"><span data-stu-id="3c354-140">onclose</span></span>](https://msdn.microsoft.com/library/mt712178) | <span data-ttu-id="3c354-141">Wird ausgelöst, wenn eine Benachrichtigung vom Benutzer geschlossen wird, oder ein automatisches Timeout.</span><span class="sxs-lookup"><span data-stu-id="3c354-141">Fires when a notification is closed by the user or an auto timeout.</span></span>
[<span data-ttu-id="3c354-142">OnError</span><span class="sxs-lookup"><span data-stu-id="3c354-142">onerror</span></span>](https://msdn.microsoft.com/library/mt712181) | <span data-ttu-id="3c354-143">Wird ausgelöst, wenn beim Behandeln einer Benachrichtigung ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="3c354-143">Fires when an error occurs while handling a notification.</span></span>
[<span data-ttu-id="3c354-144">onShow</span><span class="sxs-lookup"><span data-stu-id="3c354-144">onshow</span></span>](https://msdn.microsoft.com/library/mt712182) | <span data-ttu-id="3c354-145">Wird ausgelöst, wenn eine Benachrichtigung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3c354-145">Fires when a notification is displayed.</span></span>

### <span data-ttu-id="3c354-146">Benachrichtigungsmethoden</span><span class="sxs-lookup"><span data-stu-id="3c354-146">Notification methods</span></span>

<span data-ttu-id="3c354-147">Die folgenden Methoden werden für das [`Notification`](https://msdn.microsoft.com/library/mt710818) Objekt verwendet:</span><span class="sxs-lookup"><span data-stu-id="3c354-147">The following methods are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="3c354-148">Methode</span><span class="sxs-lookup"><span data-stu-id="3c354-148">Method</span></span> | <span data-ttu-id="3c354-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c354-149">Description</span></span>
:-------- | :----------
[<span data-ttu-id="3c354-150">close</span><span class="sxs-lookup"><span data-stu-id="3c354-150">close</span></span>](https://msdn.microsoft.com/library/mt670636) | <span data-ttu-id="3c354-151">Schließt eine angezeigte Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="3c354-151">Closes a displayed notification.</span></span>
[<span data-ttu-id="3c354-152">requestPermission</span><span class="sxs-lookup"><span data-stu-id="3c354-152">requestPermission</span></span>](https://msdn.microsoft.com/library/mt710824) | <span data-ttu-id="3c354-153">Fordert die Berechtigung des Benutzers an, Benachrichtigungen vom aktuellen Ursprung angezeigt werden zu lassen.</span><span class="sxs-lookup"><span data-stu-id="3c354-153">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>

## <span data-ttu-id="3c354-154">Benachrichtigungs Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="3c354-154">Notification permissions</span></span>

<span data-ttu-id="3c354-155">Microsoft Edge ermöglicht Benutzern das Verwalten von Benachrichtigungs Berechtigungen für jede bestimmte Website Domäne.</span><span class="sxs-lookup"><span data-stu-id="3c354-155">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span> <span data-ttu-id="3c354-156">Der Benutzer muss entweder "Ja" oder "Nein" auswählen, wenn er von der Domäne aufgefordert wird, Benachrichtigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3c354-156">It's up to the user to either select "Yes" or "No" when asked by the domain to let it show notifications.</span></span> <span data-ttu-id="3c354-157">Die [`requestPermission`](https://msdn.microsoft.com/library/mt710824) Methode wird verwendet, um den Berechtigungszustand entweder als, oder zu signalisieren `granted` `denied` `default` .</span><span class="sxs-lookup"><span data-stu-id="3c354-157">The [`requestPermission`](https://msdn.microsoft.com/library/mt710824) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span> <span data-ttu-id="3c354-158">Der Wert `default` "gibt an, dass der Benutzer keine Entscheidung getroffen hat, die als äquivalent zu sehen ist `denied` .</span><span class="sxs-lookup"><span data-stu-id="3c354-158">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>




## <span data-ttu-id="3c354-159">API-Referenz</span><span class="sxs-lookup"><span data-stu-id="3c354-159">API reference</span></span>

[<span data-ttu-id="3c354-160">Web-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="3c354-160">Web Notifications</span></span>](https://msdn.microsoft.com/library/mt710827)

## <span data-ttu-id="3c354-161">Spezifikation</span><span class="sxs-lookup"><span data-stu-id="3c354-161">Specification</span></span>

[<span data-ttu-id="3c354-162">Web-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="3c354-162">Web Notifications</span></span>](https://notifications.spec.whatwg.org)
