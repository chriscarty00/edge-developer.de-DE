---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Erfahren Sie, wie die Web-Benachrichtigungs-API verwendet werden kann, damit Websites Benutzer Benachrichtigungen außerhalb des Kontexts des Microsoft Edge-Browsers senden können.
title: Web-Benachrichtigungs-API – dev-Leitfaden
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 24b8a7b25fb3e0f0221f6d81b105d5d0374ea423
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941798"
---
# <span data-ttu-id="a8270-104">Webbenachrichtigungs-API</span><span class="sxs-lookup"><span data-stu-id="a8270-104">Web Notifications API</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="a8270-105">Mit der Web-Benachrichtigungs-API können Websites Benutzer Benachrichtigungen außerhalb des Kontexts einer Webseite innerhalb des Microsoft Edge-Browsers senden.</span><span class="sxs-lookup"><span data-stu-id="a8270-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span>  <span data-ttu-id="a8270-106">Ein Beispiel für dieses Feature in Aktion wäre eine Messaging-Anwendung wie Skype.</span><span class="sxs-lookup"><span data-stu-id="a8270-106">An example of this feature in action would be with a messaging application like Skype.</span></span>  <span data-ttu-id="a8270-107">Wenn ein Benutzer eine neue Nachricht erhalten würde, wird eine Benachrichtigung auf dem Desktop angezeigt, in der Sie über die Nachricht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="a8270-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span>  <span data-ttu-id="a8270-108">Web-Benachrichtigungen sind vollständig in die Benachrichtigungs Plattform und das Wartungs Center in Windows 10 integriert.</span><span class="sxs-lookup"><span data-stu-id="a8270-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span>  

## <span data-ttu-id="a8270-109">Erstellen einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a8270-109">Creating a notification</span></span>  

<span data-ttu-id="a8270-110">In der folgenden CodePen wird eine Pseudo-Skype-Benachrichtigung erstellt, indem ein [Benachrichtigungs](https://msdn.microsoft.com/library/mt710818) Objekt mit den Optionen [Titel](https://msdn.microsoft.com/library/mt710826), [Symbol](https://msdn.microsoft.com/library/mt710814)und [Textkörper](https://msdn.microsoft.com/library/mt710811) eingerichtet wird:</span><span class="sxs-lookup"><span data-stu-id="a8270-110">The CodePen below creates a mock Skype notification by making a [Notification](https://msdn.microsoft.com/library/mt710818) object with the [title](https://msdn.microsoft.com/library/mt710826), [icon](https://msdn.microsoft.com/library/mt710814), and [body](https://msdn.microsoft.com/library/mt710811) options set:</span></span>  

<iframe height='295' scrolling='no' title='<span data-ttu-id="a8270-111">Web-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a8270-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="a8270-112">Lesen Sie die Stift <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> -webbenachrichtigungen </a> von Microsoft Edge docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) auf <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="a8270-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

<span data-ttu-id="a8270-113">Es wird dringend empfohlen, für jede Benachrichtigung ein **Symbol** anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a8270-113">It is strongly recommended that an **icon** be specified for each notification.</span></span>  <span data-ttu-id="a8270-114">Dies verbessert nicht nur eine Benachrichtigung aus Sicht einer Benutzeroberfläche, sondern hilft auch, Benutzer darüber zu informieren, von wo aus die Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8270-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>  

<span data-ttu-id="a8270-115">Schauen Sie sich das folgende Video an, um eine exemplarische Vorgehensweise zum Erstellen einer webbenachrichtigung und zum Anzeigen des Verhaltens in Windows 10 zu sehen!</span><span class="sxs-lookup"><span data-stu-id="a8270-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### <span data-ttu-id="a8270-116">Benachrichtigungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8270-116">Notification properties</span></span>  

<span data-ttu-id="a8270-117">Benachrichtigungen können mit den folgenden Eigenschaften eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="a8270-117">Notifications can be set with the following properties:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-118">body</span><span class="sxs-lookup"><span data-stu-id="a8270-118">body</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-119">Der Textkörper der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a8270-119">The body text of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-120">dir</span><span class="sxs-lookup"><span data-stu-id="a8270-120">dir</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-121">Die Richtung des Texts der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a8270-121">The direction of the notification's text.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-122">icon</span><span class="sxs-lookup"><span data-stu-id="a8270-122">icon</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-123">Die URL der Benachrichtigung, die für das zugehörige Symbol verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8270-123">The notification's URL that is used for its icon.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-124">lang</span><span class="sxs-lookup"><span data-stu-id="a8270-124">lang</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-125">Die Sprache der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a8270-125">The language of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-126">Berechtigungs</span><span class="sxs-lookup"><span data-stu-id="a8270-126">permission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-127">Die aktuelle benachrichtigungsanzeige Berechtigung, die der Benutzer für den aktuellen Ursprung gewährt hat.</span><span class="sxs-lookup"><span data-stu-id="a8270-127">The current notification display permission the user has granted for the current origin.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-128">tag</span><span class="sxs-lookup"><span data-stu-id="a8270-128">tag</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-129">Das Tag der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a8270-129">The tag of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-130">title</span><span class="sxs-lookup"><span data-stu-id="a8270-130">title</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-131">Der Titel der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a8270-131">The title of the notification.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="a8270-132">Benachrichtigungsereignisse</span><span class="sxs-lookup"><span data-stu-id="a8270-132">Notification events</span></span>  

<span data-ttu-id="a8270-133">Die folgenden Ereignisse werden mit dem [Benachrichtigungs](https://developer.mozilla.org/docs/Web/API/Notification) Objekt verwendet:</span><span class="sxs-lookup"><span data-stu-id="a8270-133">The following events are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-134">OnClick</span><span class="sxs-lookup"><span data-stu-id="a8270-134">onclick</span></span>](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-135">Wird ausgelöst, wenn der Benutzer auf eine Benachrichtigung klickt.</span><span class="sxs-lookup"><span data-stu-id="a8270-135">Fires when a notification is clicked by the user.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-136">OnClose</span><span class="sxs-lookup"><span data-stu-id="a8270-136">onclose</span></span>](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-137">Wird ausgelöst, wenn eine Benachrichtigung vom Benutzer geschlossen wird, oder ein automatisches Timeout.</span><span class="sxs-lookup"><span data-stu-id="a8270-137">Fires when a notification is closed by the user or an auto timeout.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-138">OnError</span><span class="sxs-lookup"><span data-stu-id="a8270-138">onerror</span></span>](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-139">Wird ausgelöst, wenn beim Behandeln einer Benachrichtigung ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="a8270-139">Fires when an error occurs while handling a notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-140">onShow</span><span class="sxs-lookup"><span data-stu-id="a8270-140">onshow</span></span>](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-141">Wird ausgelöst, wenn eine Benachrichtigung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a8270-141">Fires when a notification is displayed.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="a8270-142">Benachrichtigungsmethoden</span><span class="sxs-lookup"><span data-stu-id="a8270-142">Notification methods</span></span>  

<span data-ttu-id="a8270-143">Die folgenden Methoden werden mit dem [Benachrichtigungs](https://developer.mozilla.org/docs/Web/API/Notification) Objekt verwendet:</span><span class="sxs-lookup"><span data-stu-id="a8270-143">The following methods are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-144">close</span><span class="sxs-lookup"><span data-stu-id="a8270-144">close</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-145">Schließt eine angezeigte Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a8270-145">Closes a displayed notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="a8270-146">requestPermission</span><span class="sxs-lookup"><span data-stu-id="a8270-146">requestPermission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8270-147">Fordert die Berechtigung des Benutzers an, Benachrichtigungen vom aktuellen Ursprung angezeigt werden zu lassen.</span><span class="sxs-lookup"><span data-stu-id="a8270-147">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="a8270-148">Benachrichtigungs Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a8270-148">Notification permissions</span></span>  

<span data-ttu-id="a8270-149">Microsoft Edge ermöglicht Benutzern das Verwalten von Benachrichtigungs Berechtigungen für jede bestimmte Website Domäne.</span><span class="sxs-lookup"><span data-stu-id="a8270-149">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span>  <span data-ttu-id="a8270-150">Der Benutzer muss entweder " **Ja** " oder " **Nein** " auswählen, wenn er von der Domäne gefragt wird, ob Benachrichtigungen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8270-150">It's up to the user to either select **Yes** or **No** when asked by the domain to let it show notifications.</span></span>  <span data-ttu-id="a8270-151">Die [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) -Methode wird verwendet, um den Berechtigungszustand als entweder `granted` , oder zu signalisieren `denied` `default` .</span><span class="sxs-lookup"><span data-stu-id="a8270-151">The [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span>  <span data-ttu-id="a8270-152">Der Wert `default` "gibt an, dass der Benutzer keine Entscheidung getroffen hat, die als äquivalent zu sehen ist `denied` .</span><span class="sxs-lookup"><span data-stu-id="a8270-152">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>  

## <span data-ttu-id="a8270-153">API-Referenz</span><span class="sxs-lookup"><span data-stu-id="a8270-153">API reference</span></span>  

[<span data-ttu-id="a8270-154">Web-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a8270-154">Web Notifications</span></span>](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## <span data-ttu-id="a8270-155">Spezifikation</span><span class="sxs-lookup"><span data-stu-id="a8270-155">Specification</span></span>  

[<span data-ttu-id="a8270-156">Web-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a8270-156">Web Notifications</span></span>](https://notifications.spec.whatwg.org)  
