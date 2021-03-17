---
description: Erfahren Sie, wie Sie die HTTP-Cookies für eine Seite mit Microsoft Edge DevTools anzeigen, bearbeiten und löschen.
title: Anzeigen, Bearbeiten und Löschen von Cookies mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c208ca628fe91ed5922bc36566be2b9bdd20ec0b
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439682"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a><span data-ttu-id="c92df-104">Anzeigen, Bearbeiten und Löschen von Cookies mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c92df-104">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c92df-105">[HTTP-Cookies][MDNHTTPCookies] werden hauptsächlich verwendet, um Benutzersitzungen zu verwalten, Benutzerpersonalisierungseinstellungen zu speichern und das Benutzerverhalten nachverfolgt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c92df-105">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="c92df-106">Cookies sind auch die Ursache für alle lästigen, die diese **Seite verwendet** Cookies Zustimmungsformulare, die im Web gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c92df-106">Cookies are also the cause of all of the annoying **this page uses cookies** consent forms that are found across the web.</span></span>  <span data-ttu-id="c92df-107">Im folgenden Handbuch erfahren Sie, wie Sie die HTTP-Cookies für eine Webseite mit Microsoft Edge DevTools anzeigen, [bearbeiten und löschen.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="c92df-107">The following guide teaches you how to view, edit, and delete the HTTP cookies for a webpage with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-the-cookies-pane"></a><span data-ttu-id="c92df-108">Öffnen des Bereichs "Cookies"</span><span class="sxs-lookup"><span data-stu-id="c92df-108">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="c92df-109">[Öffnen Sie DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="c92df-109">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="c92df-110">Wählen Sie die **Registerkarte Anwendung** aus, um den Bereich **Anwendung zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="c92df-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="c92df-111">Der **Manifestbereich** sollte geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="c92df-111">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="c92df-113">Abbildung 1: Der Manifestbereich</span><span class="sxs-lookup"><span data-stu-id="c92df-113">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="c92df-114">Wählen **Sie unter Speicher** erweitern **Cookies**einen Ursprung aus.</span><span class="sxs-lookup"><span data-stu-id="c92df-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Der Bereich Cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="c92df-116">Abbildung 2: Der Bereich "Cookies"</span><span class="sxs-lookup"><span data-stu-id="c92df-116">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <a name="fields"></a><span data-ttu-id="c92df-117">Felder</span><span class="sxs-lookup"><span data-stu-id="c92df-117">Fields</span></span>  

<span data-ttu-id="c92df-118">Die **Tabelle Cookies** enthält die folgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="c92df-118">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="c92df-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="c92df-119">**Name**.</span></span>  <span data-ttu-id="c92df-120">Der Name des Cookies.</span><span class="sxs-lookup"><span data-stu-id="c92df-120">The name of the cookie.</span></span>  
*   <span data-ttu-id="c92df-121">**Wert**.</span><span class="sxs-lookup"><span data-stu-id="c92df-121">**Value**.</span></span>  <span data-ttu-id="c92df-122">Der Wert des Cookies.</span><span class="sxs-lookup"><span data-stu-id="c92df-122">The value of the cookie.</span></span>  
*   <span data-ttu-id="c92df-123">**Domäne**.</span><span class="sxs-lookup"><span data-stu-id="c92df-123">**Domain**.</span></span>  <span data-ttu-id="c92df-124">Die Hosts, die das Cookie empfangen dürfen.</span><span class="sxs-lookup"><span data-stu-id="c92df-124">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="c92df-125">Navigieren Sie zu [Bereich der Cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="c92df-125">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="c92df-126">**Pfad**.</span><span class="sxs-lookup"><span data-stu-id="c92df-126">**Path**.</span></span>  <span data-ttu-id="c92df-127">Die URL, die in der angeforderten URL vorhanden sein muss, um den Header zu `Cookie` senden.</span><span class="sxs-lookup"><span data-stu-id="c92df-127">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="c92df-128">Navigieren Sie zu [Bereich der Cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="c92df-128">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="c92df-129">**Läuft ab / Max-Age**.</span><span class="sxs-lookup"><span data-stu-id="c92df-129">**Expires / Max-Age**.</span></span>  <span data-ttu-id="c92df-130">Das Ablaufdatum oder das maximale Alter des Cookies.</span><span class="sxs-lookup"><span data-stu-id="c92df-130">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="c92df-131">Navigieren Sie zu [Dauerhafte Cookies][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="c92df-131">Navigate to [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="c92df-132">Für [Sitzungscookies][MDNHTTPCookiesSession] ist dieser Wert immer `Session` .</span><span class="sxs-lookup"><span data-stu-id="c92df-132">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="c92df-133">**Größe**.</span><span class="sxs-lookup"><span data-stu-id="c92df-133">**Size**.</span></span>  <span data-ttu-id="c92df-134">Die Größe des Cookies in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c92df-134">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="c92df-135">**HTTP**.</span><span class="sxs-lookup"><span data-stu-id="c92df-135">**HTTP**.</span></span>  <span data-ttu-id="c92df-136">Wenn true, gibt dieses Feld an, dass das Cookie nur über HTTP verwendet werden soll, und die JavaScript-Änderung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c92df-136">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="c92df-137">Navigieren Sie zu [HttpOnly Cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="c92df-137">Navigate to [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="c92df-138">**Secure**.</span><span class="sxs-lookup"><span data-stu-id="c92df-138">**Secure**.</span></span>  <span data-ttu-id="c92df-139">Wenn true, gibt dieses Feld an, dass das Cookie nur über eine sichere HTTPS-Verbindung an den Server gesendet werden darf.</span><span class="sxs-lookup"><span data-stu-id="c92df-139">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="c92df-140">Navigieren Sie zu [Sichere Cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="c92df-140">Navigate to [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="c92df-141">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="c92df-141">**SameSite**.</span></span>  <span data-ttu-id="c92df-142">Enthält `strict` oder wenn das Cookie das experimentelle `lax` [Samesite-Attribut][MDNHTTPCookiesSamesite] verwendet.</span><span class="sxs-lookup"><span data-stu-id="c92df-142">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="c92df-143">**Priorität**.</span><span class="sxs-lookup"><span data-stu-id="c92df-143">**Priority**.</span></span>  <span data-ttu-id="c92df-144">Enthält `low` , \(default\), oder wenn das Cookie das veraltete `medium` Cookie `high` [Priority-Attribut][ChromiumIssue232693] verwendet.</span><span class="sxs-lookup"><span data-stu-id="c92df-144">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <a name="filter-cookies"></a><span data-ttu-id="c92df-145">Filtern von Cookies</span><span class="sxs-lookup"><span data-stu-id="c92df-145">Filter cookies</span></span>  

<span data-ttu-id="c92df-146">Verwenden Sie das **Textfeld Filter,** um Cookies nach **Name oder Value** zu **filtern.**</span><span class="sxs-lookup"><span data-stu-id="c92df-146">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="c92df-147">Das Filtern nach anderen Feldern wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c92df-147">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtern von Cookies, die die Text-ID nicht enthalten" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="c92df-149">Abbildung 3: Filtern von Cookies, die den Text nicht enthalten</span><span class="sxs-lookup"><span data-stu-id="c92df-149">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a><span data-ttu-id="c92df-150">Bearbeiten eines Cookies</span><span class="sxs-lookup"><span data-stu-id="c92df-150">Edit a cookie</span></span>  

<span data-ttu-id="c92df-151">Die **Felder Name**, **Value**, **Domain**, **Path**und **Expires / Max-Age** können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c92df-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="c92df-152">Doppelklicken Sie auf ein Feld, um es zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c92df-152">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Festlegen des Namens eines Cookies auf DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="c92df-154">Abbildung 4: Festlegen des Namens eines Cookies auf</span><span class="sxs-lookup"><span data-stu-id="c92df-154">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a><span data-ttu-id="c92df-155">Löschen von Cookies</span><span class="sxs-lookup"><span data-stu-id="c92df-155">Delete cookies</span></span>  

<span data-ttu-id="c92df-156">Wählen Sie ein Cookie aus, und wählen Sie **Ausgewähltes** Löschen \( Ausgewähltes Löschen \) aus, ![ um das spezifische Cookie zu ](../media/delete-icon.msft.png) löschen.</span><span class="sxs-lookup"><span data-stu-id="c92df-156">Choose a cookie and choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\) to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Löschen eines bestimmten Cookies" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="c92df-158">Abbildung 5: Löschen eines bestimmten Cookies</span><span class="sxs-lookup"><span data-stu-id="c92df-158">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="c92df-159">Wählen **Sie Alle** löschen \( Alle löschen ![ ](../media/clear-icon.msft.png) \), um alle Cookies zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c92df-159">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\) to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Löschen aller Cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="c92df-161">Abbildung 6: Löschen aller Cookies</span><span class="sxs-lookup"><span data-stu-id="c92df-161">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c92df-162">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="c92df-162">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium) Developer Tools"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Chromium Issue 232693: Implementing Priority Field for Cookies | Chromium-Bugs"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "HTTP-Cookies | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "HTTP-Cookies – permanente | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "HTTP-Cookies – SameSite-Cookies | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "HTTP-Cookies – Umfang der | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "HTTP-Cookies – Secure and HttpOnly cookies | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "HTTP-Cookies – Sitzungscookies | MDN"  

> [!NOTE]
> <span data-ttu-id="c92df-172">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c92df-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c92df-173">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="c92df-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c92df-175">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c92df-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
