---
title: Verwenden des Web App-Manifests, um Ihre Progressive Web-App in das Betriebs System zu integrieren
description: Erfahren Sie, wie Sie das Web App-Manifest verwenden, um Ihre Progressive Web-App in Ihr Betriebs System zu integrieren.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f493ae0c3cef3a1950b2207d66fef65055b2d959
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659293"
---
# <span data-ttu-id="66be4-104">Verwenden des Web App-Manifests, um Ihre Progressive Web-App in das Betriebs System zu integrieren</span><span class="sxs-lookup"><span data-stu-id="66be4-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="66be4-105">Ein Web-App-Manifest einer Website steuert, wie Ihre Progressive Web-App \ (PWA \) aussieht und sich verhält, wenn Sie auf einem Gerät installiert ist.</span><span class="sxs-lookup"><span data-stu-id="66be4-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="66be4-106">Auf der grundlegendsten Ebene enthält das Manifest Details zum Namen Ihrer APP, zu Symbolen für die Darstellung Ihrer APP in Systemmenüs sowie zu den Designfarben, die das Betriebssystem \ (OS \) in der Titelleiste verwendet.</span><span class="sxs-lookup"><span data-stu-id="66be4-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="66be4-107">Darüber hinaus können Sie mit dem Manifest leistungsstarke Features entsperren, mit denen sich Ihre APP wie andere systemeigene apps Verhalten kann.</span><span class="sxs-lookup"><span data-stu-id="66be4-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <span data-ttu-id="66be4-108">Verwenden von Tastenkombinationen, um schnellen Zugriff auf Funktionen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="66be4-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="66be4-109">Die meisten Betriebssysteme bieten schnellen Zugriff auf wichtige App-Features mithilfe von Tastenkombinationen im Kontextmenü, das mit dem Symbol der App verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="66be4-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="66be4-110">Wenn Sie Tastenkombinationen in PWA verwenden möchten, schließen `shortcuts` Sie die Eigenschaft in das Web App-Manifest ein.</span><span class="sxs-lookup"><span data-stu-id="66be4-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="66be4-111">Der folgende Codeausschnitt zeigt, wie Sie eine Verknüpfung in Ihrem Web App-Manifest definieren.</span><span class="sxs-lookup"><span data-stu-id="66be4-111">The following code snippet shows how to define a shortcut in your web app manifest.</span></span>  

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

<span data-ttu-id="66be4-112">Wenn Sie ein vollständiges Web App-Manifest hinzugefügt haben, werden im Kontextmenü auf dem Symbol der APP zwei Tastenkombinationen für das Hinzufügen des vorherigen Codeausschnitts aktiviert.</span><span class="sxs-lookup"><span data-stu-id="66be4-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="66be4-113">Der erste Name ist `Play Later` ein benutzerdefiniertes Symbol.</span><span class="sxs-lookup"><span data-stu-id="66be4-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="66be4-114">Die zweite ist benannt `Subscriptions` und weist kein Symbol auf, da die `icons` Eigenschaft optional ist.</span><span class="sxs-lookup"><span data-stu-id="66be4-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="66be4-115">Die `description` Eigenschaft ist ebenfalls optional und kann zum Bereitstellen zusätzlicher Informationen für Barrierefreiheits Zwecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66be4-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <span data-ttu-id="66be4-116">Identifizieren ihrer App als freigabeziel</span><span class="sxs-lookup"><span data-stu-id="66be4-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="66be4-117">Viele Betriebssysteme ermöglichen es Benutzern, schnell Links und Dateien mit systemeigenen Anwendungen zu teilen.</span><span class="sxs-lookup"><span data-stu-id="66be4-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="66be4-118">Progressive Web-Apps können auch über das `share_target` Mitglied des Web App-Manifests an dieser Funktion teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="66be4-118">Progressive Web Apps can participate in this feature as well, via the `share_target` member of the Web App Manifest.</span></span> <span data-ttu-id="66be4-119">Wenn Sie share_target verwenden, definieren Sie die Seite "Aktion" (ähnlich wie in einem Formular) und die Parameter, die Sie erwarten, an Sie weitergegeben zu werden.</span><span class="sxs-lookup"><span data-stu-id="66be4-119">Using share_target, you define the "action" page (similar to a form) and the parameters you expect to be passed into it.</span></span> <span data-ttu-id="66be4-120">Der folgende Codeausschnitt zeigt ein Beispiel für die Verwendung von `share_target` .</span><span class="sxs-lookup"><span data-stu-id="66be4-120">The following code snippet shows an example of how to use `share_target`.</span></span>

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

<span data-ttu-id="66be4-121">Wenn Sie dem Web App-Manifest hinzugefügt wird, wird "/Share.html" als Aktionsseite für eine Freigabe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="66be4-121">When added to the Web App Manifest, this establishes "/share.html" as the action page for a share.</span></span> <span data-ttu-id="66be4-122">Darüber hinaus werden drei Parameter definiert, die an die Aktionsseite übergeben werden: "Title", "Text" und "URL".</span><span class="sxs-lookup"><span data-stu-id="66be4-122">Additionally, it defines three parameters that would be passed to that action page: "title", "text", and "url".</span></span> <span data-ttu-id="66be4-123">Diese Parameter werden in den Eigenschaften "Name", "Description" und "Link" des [ShareData](https://wicg.github.io/web-share#dom-sharedata) -Objekts gespeichert.</span><span class="sxs-lookup"><span data-stu-id="66be4-123">These parameters will be stored in the [ShareData](https://wicg.github.io/web-share#dom-sharedata) object’s "name", "description", and "link" properties.</span></span> <span data-ttu-id="66be4-124">Standardmäßig empfängt die Aktionsseite diese Parameter als Teil einer GET-Anforderung, doch Sie können die Anforderung `method` und Codierung \ (as `enctype` \) wie in einem Webformular angeben.</span><span class="sxs-lookup"><span data-stu-id="66be4-124">By default, the action page receives these parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <span data-ttu-id="66be4-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="66be4-125">See also</span></span>  

<span data-ttu-id="66be4-126">Weitere Informationen zu Web App-Manifesten finden Sie in der folgenden Liste verwandter Themen.</span><span class="sxs-lookup"><span data-stu-id="66be4-126">To learn more about Web App Manifests, see the following list of related topics.</span></span>  

* [<span data-ttu-id="66be4-127">Web App-Manifeste</span><span class="sxs-lookup"><span data-stu-id="66be4-127">Web App Manifests</span></span>][MDNWebAppManifests]  
* [<span data-ttu-id="66be4-128">Webfreigabe Ziel</span><span class="sxs-lookup"><span data-stu-id="66be4-128">Web Share Target</span></span>][WICGShareTarget]
* [<span data-ttu-id="66be4-129">Webfreigabe</span><span class="sxs-lookup"><span data-stu-id="66be4-129">Web Share</span></span>][WICGShare]

<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifeste | MDN"  
[WICGShareTarget]: https://wicg.github.io/web-share-target/ "Ziel-API für Webfreigaben | WICG"
[WICGShare]: https://w3c.github.io/web-share/ "Webfreigabe-API | WICG"
