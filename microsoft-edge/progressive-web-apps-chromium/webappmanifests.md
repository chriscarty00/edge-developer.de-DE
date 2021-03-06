---
title: Verwenden des Web-App-Manifests zum Integrieren Ihrer Progressive Web App in das Betriebssystem
description: Erfahren Sie, wie Sie das Web App-Manifest verwenden, um Ihre Progressive Web App in Ihr Betriebssystem zu integrieren.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 0063323b1fde94d84e70df51170726325dd0f2a9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399099"
---
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a><span data-ttu-id="26205-104">Verwenden des Web-App-Manifests zum Integrieren Ihrer Progressive Web App in das Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="26205-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="26205-105">Ein Web-App-Manifest einer Website bestimmt, wie Ihre Progressive Web App \(PWA\) aussieht und sich verhält, wenn sie auf einem Gerät installiert wird.</span><span class="sxs-lookup"><span data-stu-id="26205-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="26205-106">Auf der grundlegendsten Ebene enthält das Manifest Details zum Namen Ihrer App, Symbole zur Darstellung Ihrer App in Systemmenüs und die Designfarben, die das Betriebssystem \(OS\) in der Titelleiste verwendet.</span><span class="sxs-lookup"><span data-stu-id="26205-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="26205-107">Mit dem Manifest können Sie außerdem leistungsstarke Features entsperren, mit denen sich Ihre App wie andere systemeigene Apps auf dem System verhalten kann.</span><span class="sxs-lookup"><span data-stu-id="26205-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a><span data-ttu-id="26205-108">Verwenden von Verknüpfungen zum schnellen Zugriff auf Features</span><span class="sxs-lookup"><span data-stu-id="26205-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="26205-109">Die meisten Betriebssysteme bieten schnellen Zugriff auf wichtige App-Features mithilfe von Verknüpfungen im Kontextmenü, das mit dem Symbol der App verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="26205-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="26205-110">Um Verknüpfungen in Ihrem PWA zu verwenden, schließen Sie die `shortcuts` Eigenschaft in Ihr Web App-Manifest ein.</span><span class="sxs-lookup"><span data-stu-id="26205-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="26205-111">Der folgende Codeausschnitt zeigt, wie Sie eine Verknüpfung in Ihrem Web-App-Manifest definieren.</span><span class="sxs-lookup"><span data-stu-id="26205-111">The following code snippet displays how to define a shortcut in your web app manifest.</span></span>  

```json
"shortcuts": [
    {
        "name": "Play Later",
        "description": "View the list of podcasts you saved for later",
        "url": "/play-later",
        "icons": [
            {
                "src": "/icons/play-later.svg",
                "type": "image/svg+xml",
                "purpose": "any"
            }
        ]
    },
    {
        "name": "Subscriptions",
        "description": "View the list of podcasts available in your subscription",
        "url": "/subscriptions?sort=desc"
    }
]
```  

<span data-ttu-id="26205-112">Wenn das Hinzufügen des vorherigen Codeausschnitts zu einem vollständigen Web-App-Manifest hinzugefügt wird, werden zwei Verknüpfungen im Kontextmenü auf dem Symbol der App aktiviert.</span><span class="sxs-lookup"><span data-stu-id="26205-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="26205-113">Die erste ist benannt `Play Later` und hat ein benutzerdefiniertes Symbol.</span><span class="sxs-lookup"><span data-stu-id="26205-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="26205-114">Die zweite ist benannt `Subscriptions` und hat kein Symbol, da die Eigenschaft `icons` optional ist.</span><span class="sxs-lookup"><span data-stu-id="26205-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="26205-115">Die Eigenschaft ist auch optional und kann verwendet werden, um `description` zusätzliche Informationen für Barrierefreiheitszwecke zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="26205-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <a name="identify-your-app-as-a-share-target"></a><span data-ttu-id="26205-116">Identifizieren Ihrer App als Freigabeziel</span><span class="sxs-lookup"><span data-stu-id="26205-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="26205-117">Viele Betriebssysteme ermöglichen Benutzern die schnelle Freigabe von Links und Dateien für systemeigene Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="26205-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="26205-118">Progressive Web Apps können auch mit dem Mitglied des Web App-Manifests an `share_target` diesem Feature teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="26205-118">Progressive Web Apps can participate in this feature as well, using the `share_target` member of the Web App Manifest.</span></span>  <span data-ttu-id="26205-119">Mit `share_target` definieren Sie die Seite \(ähnlich einem Formular\) und die Parameter, die Sie davon erwarten, `"action"` dass sie übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="26205-119">Using `share_target`, you define the `"action"` page \(similar to a form\) and the parameters you expect to be passed into it.</span></span>  <span data-ttu-id="26205-120">Im folgenden Codeausschnitt wird ein Beispiel für die Verwendung von `share_target` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26205-120">The following code snippet displays an example of how to use `share_target`.</span></span>

```json
"share_target": {
    "action": "/share.html",
    "params": {
        "title": "name",
        "text": "description",
        "url": "link"
    }
}
```

<span data-ttu-id="26205-121">Beim Hinzufügen zum Web-App-Manifest wird dies `"/share.html"` als Aktionsseite für eine Freigabe etabliert.</span><span class="sxs-lookup"><span data-stu-id="26205-121">When added to the Web App Manifest, this establishes `"/share.html"` as the action page for a share.</span></span> <span data-ttu-id="26205-122">Darüber hinaus werden drei Parameter definiert, die an diese Aktionsseite übergeben würden: `"title"` `"text"` , und `"url"` .</span><span class="sxs-lookup"><span data-stu-id="26205-122">Additionally, it defines three parameters that would be passed to that action page:`"title"`, `"text"`, and `"url"`.</span></span>  <span data-ttu-id="26205-123">Diese Parameter werden in den `"name"` Eigenschaften , und des `"description"` `"link"` [ShareData-Objekts][GitHubWicgWebShareDomSharedata] gespeichert.</span><span class="sxs-lookup"><span data-stu-id="26205-123">These parameters will be stored in the `"name"`, `"description"`, and `"link"` properties of the [ShareData][GitHubWicgWebShareDomSharedata] object.</span></span>  <span data-ttu-id="26205-124">Standardmäßig empfängt die Aktionsseite die Parameter als Teil einer GET-Anforderung, Aber Sie können die Anforderung und Codierung \(als \) angeben, genau wie in einem `method` `enctype` Webformular.</span><span class="sxs-lookup"><span data-stu-id="26205-124">By default, the action page receives the parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <a name="see-also"></a><span data-ttu-id="26205-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="26205-125">See also</span></span>  

<span data-ttu-id="26205-126">Weitere Informationen zu Web-App-Manifesten finden Sie in der folgenden Liste verwandter Themen.</span><span class="sxs-lookup"><span data-stu-id="26205-126">To learn more about Web App Manifests, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="26205-127">Web App-Manifeste</span><span class="sxs-lookup"><span data-stu-id="26205-127">Web App Manifests</span></span>][MDNWebAppManifests]  
*   [<span data-ttu-id="26205-128">Web Share Target</span><span class="sxs-lookup"><span data-stu-id="26205-128">Web Share Target</span></span>][GitHubWicgWebShareTarget]
*   [<span data-ttu-id="26205-129">Web Share</span><span class="sxs-lookup"><span data-stu-id="26205-129">Web Share</span></span>][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Web-App-Manifeste | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Web Share Target API | WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "ShareData-Wörterbuch – Web Share-API-| WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "Web Share-API-| WICG"
