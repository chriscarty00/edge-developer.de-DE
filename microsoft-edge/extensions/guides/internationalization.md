---
description: Stellen Sie Ihre Erweiterung für verschiedene Sprachen barrierefrei zur Verfügung, und testen Sie Ihre Sprachzeichenfolgen mit dem Internationalisierungs Leit Faden.
title: Erweiterungen – Internationalisierung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: d1f553d0e3e39192e68665fe6720daa811777c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567400"
---
# <span data-ttu-id="756db-104">Internationalisierung</span><span class="sxs-lookup"><span data-stu-id="756db-104">Internationalization</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="756db-105">Damit Ihre Erweiterung für eine Vielzahl unterschiedlicher Personen zugänglich ist, ist es wichtig, sich mit anderen Ländern zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="756db-105">In order to make your extension accessible to a variety of different people, it is important to develop with other countries in mind.</span></span> <span data-ttu-id="756db-106">Mit Microsoft Edge Extensions können Sie Ihren Erweiterungen unterschiedliche Sprachzeichenfolgen hinzufügen, damit Ihre Sprache problemlos geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="756db-106">Microsoft Edge extensions allows you to add different language strings to your extensions so that their language can easily be changed.</span></span>

<span data-ttu-id="756db-107">Weitere Informationen zum Internationalisierung ihrer Erweiterung finden Sie im [Leitfaden zur Internationalisierung](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)von MDN.</span><span class="sxs-lookup"><span data-stu-id="756db-107">For more information on internationalizing your extension, check out MDN's [Internationalization guide](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization).</span></span>


## <span data-ttu-id="756db-108">Testen von Sprachen</span><span class="sxs-lookup"><span data-stu-id="756db-108">Testing languages</span></span>

<span data-ttu-id="756db-109">Um Ihre Sprachzeichenfolgen zu testen, müssen Sie zuerst die Windows-Anzeigesprache auf die Sprache einstellen, auf die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="756db-109">To test your language strings, you first need to set the Windows display language to the language that you want to test for.</span></span>

<span data-ttu-id="756db-110">Führen Sie die folgenden Schritte aus, um die Windows-Anzeigesprache zu ändern:</span><span class="sxs-lookup"><span data-stu-id="756db-110">Follow the steps below to change the Windows display language:</span></span>

1. <span data-ttu-id="756db-111">Öffnen Sie die App Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="756db-111">Open the Settings app.</span></span>

   ![Einstellungsanwendung](./../media/loc-settings.png)
2. <span data-ttu-id="756db-113">Wählen Sie "Uhrzeit & Sprache" aus.</span><span class="sxs-lookup"><span data-stu-id="756db-113">Select "Time & language".</span></span>
3. <span data-ttu-id="756db-114">Wählen Sie "Region & Sprache" aus.</span><span class="sxs-lookup"><span data-stu-id="756db-114">Select "Region & language".</span></span>
4. <span data-ttu-id="756db-115">Wählen Sie "+ Sprache hinzufügen" aus, um die Sprache der Liste der möglichen Sprachen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="756db-115">Select "+ Add a language" to add the language to the list of possible languages.</span></span>
5. <span data-ttu-id="756db-116">Wählen Sie die gewünschte Sprache in der Liste "Sprachen" aus, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="756db-116">Choose the language from the "Languages" list that you want to test.</span></span>
6. <span data-ttu-id="756db-117">Wählen Sie die Schaltfläche "als Standard festlegen" aus (möglicherweise müssen Sie Ihren PC neu starten).</span><span class="sxs-lookup"><span data-stu-id="756db-117">Select the "Set as default" button (you may need to restart your PC).</span></span>
7. <span data-ttu-id="756db-118">Öffnen Sie Microsoft Edge, und überprüfen Sie, ob die für das Gebietsschema definierten Zeichenfolgen wie erwartet angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="756db-118">Open Microsoft Edge and verify that the strings defined for the locale appear as expected.</span></span>

<span data-ttu-id="756db-119">Mithilfe der [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) -Eigenschaft können Sie überprüfen, ob die Sprache, die Microsoft Edge für die Windows-Anzeigesprache festgelegt hat, richtig ist.</span><span class="sxs-lookup"><span data-stu-id="756db-119">By using the [NavigatorLanguage.language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) property, you can verify that the language Microsoft Edge has determined to be the Windows display language is correct.</span></span>

<span data-ttu-id="756db-120">Klicken Sie auf die Schaltfläche im CodePen unten, um die Anzeigesprache Ihres Browsers anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="756db-120">Click the button in the CodePen below to see the display language of your browser.</span></span>

<iframe height='300' scrolling='no' title='<span data-ttu-id="756db-121">Gebietsschema abrufen</span><span class="sxs-lookup"><span data-stu-id="756db-121">Get locale</span></span>' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="756db-122">Weitere Informationen finden Sie unter <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> </a> MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='http://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="756db-122">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'>Get locale</a>by MSEdgeDev (<a href='http://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span>
</iframe>
