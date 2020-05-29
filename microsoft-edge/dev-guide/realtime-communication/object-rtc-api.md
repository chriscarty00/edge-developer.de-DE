---
ms.assetid: ef705c70-73f8-445b-84ed-4f83679f1980
description: Erfahren Sie, wie Sie mit der Objekt-ORTC (Real-Time Communications) Medien in Echtzeit direkt zwischen Webbrowsern, mobilen Geräten oder Servern streamen können.
title: Dev Guide-Object RTC-API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: ac033ea26fa7c1eb435b0164e5dbd2a3a5428474
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566759"
---
# <span data-ttu-id="08e3c-104">Objekt-RTC-API</span><span class="sxs-lookup"><span data-stu-id="08e3c-104">Object RTC API</span></span>

<span data-ttu-id="08e3c-105">Mit der Objekt-Echtzeitkommunikation (ORTC) können Medien (Audio und/oder Video) über systemeigene JavaScript-APIs in Echtzeit direkt zwischen Webbrowsern, mobilen Geräten und Servern gestreamt (gesendet und empfangen) werden.</span><span class="sxs-lookup"><span data-stu-id="08e3c-105">Object Real-Time Communications (ORTC) enables media (audio and/or video) to be streamed (sent and received) in real-time directly between web browsers, mobile devices, and servers via native Javascript APIs.</span></span>

> [!NOTE]
> <span data-ttu-id="08e3c-106">Microsoft Edge implementiert nun ORTC für Windows 10-Geräte.</span><span class="sxs-lookup"><span data-stu-id="08e3c-106">Microsoft Edge now implements ORTC for Windows 10 devices.</span></span> <span data-ttu-id="08e3c-107">Diese Implementierung unterscheidet sich jedoch von der neuesten Version der [ORTC-API](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span><span class="sxs-lookup"><span data-stu-id="08e3c-107">However, this implementation differs from the most recent version of the [ORTC API](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span></span> <span data-ttu-id="08e3c-108">ORTC hat sich seit der Entwicklung und Veröffentlichung von Microsoft Edge weiterentwickelt – der Browser implementiert nicht alle Objekte oder Methoden innerhalb der ORTC-API und umfasst Erweiterungen, die derzeit nicht in der Spezifikation enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="08e3c-108">ORTC has continued to evolve since the development and release of Microsoft Edge -- the browser does not implement every object or method within the ORTC API, and includes extensions not currently incorporated within the specification.</span></span> <span data-ttu-id="08e3c-109">Weiterentwicklung wird mit dem Ziel fortgesetzt, Entwicklern auf der ganzen Welt zu ermöglichen, Erfahrungen zu erstellen, die die Möglichkeit beinhalten, mit Skype-Nutzern und anderen WebRTC kompatiblen Kommunikationsdiensten zu sprechen.</span><span class="sxs-lookup"><span data-stu-id="08e3c-109">Further development will continue with the goal to enable developers around the world to build experiences that include the ability to talk to Skype users and other WebRTC compatible communication services.</span></span>



<span data-ttu-id="08e3c-110">Um eine praktische Erfahrung mit ORTC zu erhalten, probieren Sie die folgenden Demos auf Test Drive aus:</span><span class="sxs-lookup"><span data-stu-id="08e3c-110">To get a hands-on experience with ORTC, try out these demos on Test Drive:</span></span>
-  [<span data-ttu-id="08e3c-111">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="08e3c-111">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [<span data-ttu-id="08e3c-112">ORTC-Telefonanruf</span><span class="sxs-lookup"><span data-stu-id="08e3c-112">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [<span data-ttu-id="08e3c-113">ORTC-Demo</span><span class="sxs-lookup"><span data-stu-id="08e3c-113">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


<span data-ttu-id="08e3c-114">Weitere Informationen zu ORTC finden Sie unter [ORTC-API steht jetzt in Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) im Microsoft Edge dev-Blog zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="08e3c-114">For more information about ORTC, check out [ORTC API is now available in Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) on the Microsoft Edge dev blog.</span></span>


## <span data-ttu-id="08e3c-115">Übersichtsdiagramm</span><span class="sxs-lookup"><span data-stu-id="08e3c-115">Overview Diagram</span></span>


<span data-ttu-id="08e3c-116">Das folgende Diagramm enthält eine Zusammenfassung, in der die Beziehungen zwischen ORTC-Objekten beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="08e3c-116">The diagram below provides a summary describing relationships between ORTC objects.</span></span> <span data-ttu-id="08e3c-117">Horizontale oder schräge Pfeile kennzeichnen den Fluss von Medien oder Daten, während vertikale Pfeile Interaktionen mithilfe von Methoden und Ereignissen kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="08e3c-117">Horizontal or slanted arrows denote the flow of media or data, whereas vertical arrows denote interactions via methods and events.</span></span>

<span data-ttu-id="08e3c-118">ORTC verwendet "*Absender*"-, "*Empfänger*"-und "*Transport*"-Objekte, die über "*Funktionen*" verfügen, die beschreiben, was Sie tun können, sowie "*Parameter*", die definieren, wozu Sie konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="08e3c-118">ORTC uses "*sender*", "*receiver*" and "*transport*" objects, which have "*capabilities*" describing what they are capable of doing, as well as "*parameters*" which define what they are configured to do.</span></span> <span data-ttu-id="08e3c-119">"*Tracks*" erfasst und codiert Mediendatenströme von Absendern, reist über Transporte und wird dann von Empfängern dekodiert, die den Mediendatenstrom in Video-und Audiotags umwandeln.</span><span class="sxs-lookup"><span data-stu-id="08e3c-119">"*Tracks*" capture and encode media streams by senders, traveling over transports, then decoded by receivers that render the media stream tracks to video/audio tags.</span></span>

![<span data-ttu-id="08e3c-120">Microsoft Edge-ORTC-Flussdiagramm ](./../media/ortc_diagram.png) in der obigen Abbildung [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) codiert die als eingabebereit gestellte Spur, die über a oder a transportiert wird [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) .</span><span class="sxs-lookup"><span data-stu-id="08e3c-120">Microsoft Edge ORTC Flow Diagram](./../media/ortc_diagram.png) In the figure above, the [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) encodes the track provided as input, which is transported over a [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) or an [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527).</span></span> <span data-ttu-id="08e3c-121">Das Senden von DTMF-Tönen (Dual Tone Multi Frequency) wird über das [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .</span><span class="sxs-lookup"><span data-stu-id="08e3c-121">Sending of Dual Tone Multi Frequency (DTMF) tones is supported via the [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496).</span></span>

<span data-ttu-id="08e3c-122">[`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495)Und [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) verwenden Sie einen [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) , um einen Kommunikationspfad zum Erreichen des empfangenden Peers auszuwählen `RTCIceTransport` , der wiederum mit einem `RTCDtlsTransport` oder einem `RTCSrtpSdesTransport` Demultiplexen von Medien zu dem verbunden ist [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="08e3c-122">The [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) and [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) utilize an [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) to select a communication path to reach the receiving peer's `RTCIceTransport`, which is in turn associated with an `RTCDtlsTransport` or `RTCSrtpSdesTransport` which de-multiplexes media to the [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span> <span data-ttu-id="08e3c-123">Anschließend wird das `RTCRtpReceiver` Medium decodiert, wodurch eine Spur entsteht, die von einem Audio-oder Video-Tag gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="08e3c-123">The `RTCRtpReceiver` then decodes media, producing a track which is rendered by an audio or video tag.</span></span>

<span data-ttu-id="08e3c-124">Auch mehrere andere Objekte spielen eine Rolle.</span><span class="sxs-lookup"><span data-stu-id="08e3c-124">Several other objects also play a role.</span></span> <span data-ttu-id="08e3c-125">Der [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) sammelt ortsansässige Ice-Kandidaten zur Verwendung durch ein einzelnes [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) Objekt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-125">The [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) gathers local ICE candidates for use by a single [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) object.</span></span> <span data-ttu-id="08e3c-126">In den verbleibenden Abschnitten der API werden Details zu den RTP- *Funktionen* und- *Parametern*, *Betriebsstatistiken* und Kompatibilität mit der [WebRTC 1,0-API](https://go.microsoft.com/fwlink/p/?LinkID=627573)ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-126">Remaining sections of the API fill in details relating to RTP *capabilities* and *parameters*, *operational statistics* and compatibility with the [WebRTC 1.0 API](https://go.microsoft.com/fwlink/p/?LinkID=627573).</span></span>

> [!NOTE]
> <span data-ttu-id="08e3c-127">Da Microsoft Edge den Datenkanal nicht implementiert, werden die `RTCDataChannel` `RTCSctpTransport` Objekte und nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-127">Since Microsoft Edge does not implement the data channel, the `RTCDataChannel` and `RTCSctpTransport` objects are not supported.</span></span>




## <span data-ttu-id="08e3c-128">In der ersten Microsoft Edge-Implementierung unterstützte Komponenten</span><span class="sxs-lookup"><span data-stu-id="08e3c-128">Components supported in the initial Microsoft Edge implementation</span></span>


* **<span data-ttu-id="08e3c-129">ORTC-API-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="08e3c-129">ORTC API support.</span></span>** <span data-ttu-id="08e3c-130">Die Audio-und Videokommunikation ist der Hauptfokus, einschließlich der folgenden Objekte:,,,, sowie [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) die [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) Schnittstellen, die nicht direkt im Diagramm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="08e3c-130">Audio/video communications is the primary focus, including the following objects: [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107), [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112), [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495), [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516), [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508), as well as the [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces that are not shown directly in the diagram.</span></span>
* **<span data-ttu-id="08e3c-131">RTP/RTCP-Multiplexing-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="08e3c-131">RTP/RTCP multiplexing support.</span></span>** <span data-ttu-id="08e3c-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)ist für die Verwendung mit [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) .</span><span class="sxs-lookup"><span data-stu-id="08e3c-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503) is required for use with the [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495).</span></span> <span data-ttu-id="08e3c-133">A/V-Multiplexing wird ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-133">A/V multiplexing is also supported.</span></span>
* **<span data-ttu-id="08e3c-134">Betäubung/Turn/ICE-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="08e3c-134">STUN/TURN/ICE support.</span></span>** <span data-ttu-id="08e3c-135">Stun [(RFC 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), Turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) sowie Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621)werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-135">STUN [(RFC 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), TURN [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) as well as ICE [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621), are supported.</span></span> <span data-ttu-id="08e3c-136">Innerhalb des Eises wird eine reguläre Nominierung unterstützt, wobei eine aggressive Nominierung teilweise unterstützt wird (als Empfänger).</span><span class="sxs-lookup"><span data-stu-id="08e3c-136">Within ICE, regular nomination is supported, with aggressive nomination partially supported (as a receiver).</span></span> <span data-ttu-id="08e3c-137">DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) wird basierend auf DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-137">DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) is supported, based on DTLS 1.0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).</span></span>
* **<span data-ttu-id="08e3c-138">Codec-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="08e3c-138">Codec support.</span></span>** <span data-ttu-id="08e3c-139">Für [Audio-Codecs](https://msdn.microsoft.com/library/Mt599587)unterstützen wir g. 711, g. 722, Opus und Silk.</span><span class="sxs-lookup"><span data-stu-id="08e3c-139">For [audio codecs](https://msdn.microsoft.com/library/Mt599587), we support G.711, G.722, Opus and SILK.</span></span> <span data-ttu-id="08e3c-140">Darüber hinaus unterstützen wir Comfort Noise (CN) und DTMF entsprechend den RTCWEB-Audioanforderungen.</span><span class="sxs-lookup"><span data-stu-id="08e3c-140">We also support Comfort Noise (CN) and DTMF according to the RTCWEB audio requirements.</span></span> <span data-ttu-id="08e3c-141">Für Video unterstützen wir derzeit den [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) von Skype-Diensten verwendeten Codec und unterstützen erweiterte Funktionen, wie etwa die Übertragungen, skalierbare Videocodierung und die Weiterleitung von Fehlerkorrekturen.</span><span class="sxs-lookup"><span data-stu-id="08e3c-141">For video we currently support the [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) codec used by Skype services, supporting advanced features such as simulcast, scalable video coding and forward error correction.</span></span> <span data-ttu-id="08e3c-142">Wir arbeiten daran, interoperables Video mit H. 264 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="08e3c-142">We're working toward to enabling interoperable video with H.264.</span></span>

> [!NOTE]
> <span data-ttu-id="08e3c-143">Wenn Sie mit WebRTC 1,0-Implementierungen vertraut sind und an der Entwicklung der Objekt Unterstützung innerhalb von WebRTC 1,0 und ORTC interessiert sind, empfehlen wir die folgende Präsentation von Google, Microsoft und Hookflash aus der 2014 IIT RTC-Konferenz: "[ORTC-API-Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)".</span><span class="sxs-lookup"><span data-stu-id="08e3c-143">If you are familiar with WebRTC 1.0 implementations, and are interested in the evolution of object support within WebRTC 1.0 and ORTC, we recommend the following presentation by Google, Microsoft, and Hookflash from the 2014 IIT RTC Conference: "[ORTC API Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)."</span></span>




## <span data-ttu-id="08e3c-144">Code Fluss auf App-Ebene für 1:1-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="08e3c-144">App level code flow for 1:1 communications</span></span>


<span data-ttu-id="08e3c-145">In diesem Szenario fungieren zwei Windows 10-Computer als zwei Peers mit einem Webserver als Signalisierungskanal zum Austauschen von Informationen zwischen den Peers, damit eine Verbindung zwischen Ihnen hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="08e3c-145">For this scenario, two Windows 10 machines will act as two peers with a webserver as the signaling channel to exchange information between the peers so that a connection may be established between them.</span></span>

<span data-ttu-id="08e3c-146">Die folgenden Schritte sind auf Vorgänge beschränkt, die von einem Peer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08e3c-146">The steps below are scoped to operations taken by one peer.</span></span> <span data-ttu-id="08e3c-147">Beide Peers müssen ähnliche Schritte durchlaufen, um die 1:1-Kommunikation einzurichten.</span><span class="sxs-lookup"><span data-stu-id="08e3c-147">Both peers must go through similar steps in order to set up the 1:1 communications.</span></span> <span data-ttu-id="08e3c-148">Wenn Sie die folgenden Codeausschnitte besser verstehen möchten, lesen Sie die [Demo zu Microsoft Edge-Test Laufwerk](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="08e3c-148">To make better sense out of the code snippets below, refer to the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

<span data-ttu-id="08e3c-149">In diesem Beispiel wird Audio-Video-und RTP-RTCP-Multiplexing verwendet, sodass Sie nur einen einzigen Ice-und DTLS-Transport sehen, der zum Transport von RTP-und RTCP-Paketen für Audio-und Videoübertragungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08e3c-149">This example uses audio-video and RTP/RTCP multiplexing, so you will see only a single ICE and DTLS transport, used to transport RTP and RTCP packets for both audio and video.</span></span>

`Step #1.` <span data-ttu-id="08e3c-150">Erstellen Sie [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) ein Objekt (beispielsweise die [Media Capture-und Streams-API](./../multimedia/media-Capture-and-Streams.md)) mit einer Audiospur und einer Videospur.</span><span class="sxs-lookup"><span data-stu-id="08e3c-150">Create [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) object (i.e. [Media Capture and Streams API](./../multimedia/media-Capture-and-Streams.md)) with one audio track and one video track.</span></span>

```js
navigator.MediaDevices.getUserMedia ({
    "audio": true,
    "video": {
        width: 640,
        height: 360,
        facingMode: "user"
    }
}).then(
    gotStream
).catch(
    gotMediaError
);

function gotStream(stream) {
    var mediaStreamLocal = stream;
    …
}
```

`Step #2.` <span data-ttu-id="08e3c-151">Erstellen [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) Sie die, und aktivieren Sie lokal, [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) um Sie an Remote Peer zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="08e3c-151">Create the [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx), and enable local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) to be signaled to remote peer.</span></span>

```js
var iceOptions = new RTCIceGatherOptions;
iceOptions.gatherPolicy = "all";
iceOptions.iceservers = ... ;
var iceGathr = new RTCIceGatherer(iceOptions);
iceGathr.onlocalcandidate = function(evt) {
    mySignaller.signalMessage({
        "candidate": evt.candidate
    });
};
```

<span data-ttu-id="08e3c-152">Zum Schutz der Privatsphäre von Benutzern bietet Microsoft Edge eine Option, mit der ein Benutzer steuern kann, ob die Objekte lokale Host-IP-Adressen verfügbar gemacht werden können [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) .</span><span class="sxs-lookup"><span data-stu-id="08e3c-152">To help protect user privacy, Microsoft Edge introduces an option that allows a user to control whether local host IP addresses can be exposed by the [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objects.</span></span> <span data-ttu-id="08e3c-153">Eine Schnittstellenoption wird bereitgestellt, um diese Einstellung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="08e3c-153">An interface option will be provided to toggle this setting.</span></span>

<span data-ttu-id="08e3c-154">In der [Demo zu Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635)wurde ein Turn Server eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="08e3c-154">In the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635), a TURN server has been set up.</span></span> <span data-ttu-id="08e3c-155">Dieser Turn-Server hat einen sehr geringen Durchsatz und ist daher auf die Verwendung von Demo-Seiten limitiert.</span><span class="sxs-lookup"><span data-stu-id="08e3c-155">This TURN server has a very limited throughput, so is limited to only demo page use.</span></span>

`Step #3.` <span data-ttu-id="08e3c-156">Erstellen [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) Sie das für Audio und Video, und bereiten Sie die Behandlung von Remote [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) auf dem ICE-Transport vor.</span><span class="sxs-lookup"><span data-stu-id="08e3c-156">Create the [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) for audio and video, and prepare to handle remote [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) on the ICE transport.</span></span>

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

<span data-ttu-id="08e3c-157">Eine weitere Möglichkeit besteht darin, alle Remote-Ice-Kandidaten in einem Array zu sammeln `remoteCandidates` und `iceTr.setRemoteCandidates(remoteCandidates)` alle entfernten Kandidaten zusammen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="08e3c-157">Another option here is to accumulate all the remote ICE candidates into an array `remoteCandidates` and call `iceTr.setRemoteCandidates(remoteCandidates)` to add all the remote candidates together.</span></span>

`Step #4.` <span data-ttu-id="08e3c-158">Erstellen Sie den DTLS-Transport.</span><span class="sxs-lookup"><span data-stu-id="08e3c-158">Create the DTLS transport.</span></span>

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` <span data-ttu-id="08e3c-159">Erstellen Sie die Absender-und Empfängerobjekte.</span><span class="sxs-lookup"><span data-stu-id="08e3c-159">Create the sender and receiver objects.</span></span>

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

<span data-ttu-id="08e3c-160">Schritt #6.</span><span class="sxs-lookup"><span data-stu-id="08e3c-160">Step #6.</span></span> <span data-ttu-id="08e3c-161">Abrufen der Empfänger-und Absender Funktionen</span><span class="sxs-lookup"><span data-stu-id="08e3c-161">Retrieve the receiver and sender capabilities.</span></span>

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` <span data-ttu-id="08e3c-162">Ice/DTLS-Parameter und Sende-und Empfangsfunktionen können ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="08e3c-162">ICE/DTLS parameters and Send/Receive capabilities can be exchanged.</span></span>

```js
mySignaller.signalMessage({
    "ice": iceGathr.getLocalParameters(),
    "dtls": dtlsTr.getLocalParameters(),
    "recvAudioCaps": recvAudioCaps,
    "recvVideoCaps": recvVideoCaps,
    "sendAudioCaps": sendAudioCaps,
    "sendVideoCaps": sendVideoCaps
};
```

`Step #8.` <span data-ttu-id="08e3c-163">Rufen Sie Remote-params ab, starten Sie die [`ICE`](https://msdn.microsoft.com/library/Mt433112) und [`DTLS`](https://msdn.microsoft.com/library/Mt502495) Transporte, und legen Sie die Audio-und Video-Sende-und Empfangsparameter ein.</span><span class="sxs-lookup"><span data-stu-id="08e3c-163">Get remote params, start the [`ICE`](https://msdn.microsoft.com/library/Mt433112) and [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transports, and set the audio and video send and receive parameters.</span></span>

```js
mySignaller.onRemoteParams = function(params) {
    // The responder answers with its preferences, parameters and capabilities
    // Derive the send and receive parameters.
    var audioSendParams = myCapsToSendParams(sendAudioCaps, params.recvAudioCaps);
    var videoSendParams = myCapsToSendParams(sendVideoCaps, params.recvVideoCaps);
    var audioRecvParams = myCapsToRecvParams(recvAudioCaps, params.sendAudioCaps);
    var videoRecvParams = myCapsToRecvParams(recvVideoCaps, params.sendVideoCaps);
    iceTr.start(iceGathr, params.ice, RTCIceRole.controlling);
    dtlsTr.start(params.dtls);
    audioSender.send(audioSendParams);
    videoSender.send(videoSendParams);
    audioReceiver.receive(audioRecvParams);
    videoReceiver.receive(videoRecvParams);
};
```

<span data-ttu-id="08e3c-164">Nachfolgend finden Sie ein Skelett der Hilfsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="08e3c-164">Below is a skeleton of the helper functions.</span></span> <span data-ttu-id="08e3c-165">Weitere Informationen finden Sie in der [Demo zu Microsoft Edge-Test Laufwerk](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="08e3c-165">Find more details in the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

```js
RTCRtpParameters function myCapsToSendParams (RTCRtpCapabilities sendCaps, RTCRtpCapabilities remoteRecvCaps) {
    // Function returning the sender RTCRtpParameters, based on intersection of the local sender and remote receiver capabilities.
    // Steps to be followed:
    // 1. Determine the RTP features that the receiver and sender have in common.
    // 2. Determine the codecs that the sender and receiver have in common.
    // 3. Within each common codec, determine the common formats and rtcpFeedback mechanisms.
    // 4. Determine the payloadType to be used, based on the receiver preferredPayloadType.
    // 5. Set RTCRtcpParameters such as mux to their default values.  
}

RTCRtpParameters function myCapsToRecvParams(RTCRtpCapabilities recvCaps, RTCRtpCapabilities remoteSendCaps) {
    return myCapsToSendParams(remoteSendCaps, recvCaps);
}
```

`Step #9.` <span data-ttu-id="08e3c-166">Rendern und Abspielen des Remote-Mediendatenstroms über ein Video-Tag.</span><span class="sxs-lookup"><span data-stu-id="08e3c-166">Render and play the remote media stream tracks through a video tag.</span></span>

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

<span data-ttu-id="08e3c-167">Sobald Sie mit der Einrichtung von 1:1-anrufen vertraut sind, wenden Sie die gleichen Prinzipien an, um kleine Gruppenanrufe mithilfe einer Mesh-Topologie einzurichten, wobei jeder Peer eine 1:1-Verbindung mit dem restlichen Teil der Gruppe hat.</span><span class="sxs-lookup"><span data-stu-id="08e3c-167">Once familiar with setting up 1:1 calls, apply the same principles to set up small group calls using a mesh topology, where each peer will have a 1:1 connection with the rest of the group.</span></span> <span data-ttu-id="08e3c-168">Da die parallele Verzweigung auf der Microsoft Edge-Plattform nicht unterstützt wird, sollte diese über 1:1-Signalisierung gehandhabt werden, damit unabhängige [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) und [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) Objekte für jede Verbindung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08e3c-168">Since parallel forking is not supported on the Microsoft Edge platform, this should be handled via 1:1 signaling, so that independent [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) and [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) objects will be used for each connection.</span></span>

## <span data-ttu-id="08e3c-169">Details zur Implementierung in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="08e3c-169">Implementation details in Microsoft Edge</span></span>


<span data-ttu-id="08e3c-170">Die ORTC-Spezifikation war relativ stabil, da die ORTC-Community-Gruppe den "Aufruf für Implementierungen" herausgegeben hat und erhebliche Herausforderungen auf der JavaScript-API-Ebene nicht erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="08e3c-170">The ORTC spec has been relatively stable since the ORTC Community Group issued the "Call for Implementations," and significant challenges at the JavaScript API level are not expected.</span></span> <span data-ttu-id="08e3c-171">Auf dieser Grundlage wurde die Microsoft Edge-Implementierung für browserübergreifende Interoperabilitätstests auf Protokollebene veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="08e3c-171">Based on this, Microsoft Edge implementation has been released for cross-browser interoperability testing at the protocol level.</span></span>

<span data-ttu-id="08e3c-172">Einige Einschränkungen in der Microsoft Edge-Implementierung sollten beachtet werden:</span><span class="sxs-lookup"><span data-stu-id="08e3c-172">A few limitations in the Microsoft Edge implementation should be noted:</span></span>

* `RTCIceTransportController` <span data-ttu-id="08e3c-173">wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-173">is not supported.</span></span> <span data-ttu-id="08e3c-174">Die Microsoft Edge-Implementierung verarbeitet das Einfrieren/Aufheben der Fixierung von Eis pro Transport, sodass die Bestellung `IceTransports` nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="08e3c-174">Microsoft Edge implementation handles ICE freezing/unfreezing on a per-transport basis, so that ordering all the `IceTransports` is not necessary.</span></span> <span data-ttu-id="08e3c-175">Dieser Ansatz sollte mit vorhandenen Implementierungen interagieren.</span><span class="sxs-lookup"><span data-stu-id="08e3c-175">This approach should interoperate with existing implementations.</span></span>
* `RtpListener` <span data-ttu-id="08e3c-176">wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-176">is not yet supported.</span></span> <span data-ttu-id="08e3c-177">Dies bedeutet, dass SSRCs (Datenstrom-und Synchronisierungs Quellen) im Voraus im [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="08e3c-177">This means that SSRCs (stream and synchronization sources) need to be specified in advance within the [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span>
* <span data-ttu-id="08e3c-178">Forking wird in den beiden, oder nicht unterstützt `IceTransport` `IceGatherer` `DtlsTransport` .</span><span class="sxs-lookup"><span data-stu-id="08e3c-178">Forking is not yet supported in either `IceTransport`, `IceGatherer`, or `DtlsTransport`.</span></span> <span data-ttu-id="08e3c-179">Die Lösung für `DtlsTransport` Forking wird in der ORTC-Community-Gruppe noch erörtert.</span><span class="sxs-lookup"><span data-stu-id="08e3c-179">The solution to `DtlsTransport` forking is still under discussion in the ORTC Community Group.</span></span>
* <span data-ttu-id="08e3c-180">RTP/RTCP-nicht-MUX mit `DtlsTransport` wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-180">RTP/RTCP non-mux with `DtlsTransport` is not yet supported.</span></span> <span data-ttu-id="08e3c-181">Wenn `DtlsTransport` Sie Ihre Anwendung verwenden, muss RTP/RTCP-MUX unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="08e3c-181">When using `DtlsTransport` your application will need to support RTP/RTCP mux.</span></span>
* <span data-ttu-id="08e3c-182">In [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) wird Microsoft Edge die meisten Codierungs Qualitätssteuer Elemente derzeit ignoriert, erfordert jedoch das Festlegen der "Active"-und "SSRC"-Attribute.</span><span class="sxs-lookup"><span data-stu-id="08e3c-182">In [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx), Microsoft Edge currently ignores most of the encoding quality controls, but does require setting the 'active' and 'ssrc' attributes.</span></span>
* <span data-ttu-id="08e3c-183">Das `icecandidatepairchanged` Ereignis wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08e3c-183">The `icecandidatepairchanged` event is not yet supported.</span></span> <span data-ttu-id="08e3c-184">Sie können die Kandidaten paar Informationen über die [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) Methode extrahieren.</span><span class="sxs-lookup"><span data-stu-id="08e3c-184">You can extract the candidate pair information through the [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) method.</span></span>
* <span data-ttu-id="08e3c-185">Microsoft Edge unterstützt derzeit keine der `DataChannel` Funktionen, die derzeit in der ORTC-Spezifikation definiert sind.</span><span class="sxs-lookup"><span data-stu-id="08e3c-185">Microsoft Edge currently does not support any of the `DataChannel` functionality currently defined in the ORTC spec.</span></span>

#### <span data-ttu-id="08e3c-186">Wir freuen uns</span><span class="sxs-lookup"><span data-stu-id="08e3c-186">Looking forward</span></span>

<span data-ttu-id="08e3c-187">Microsoft Edge-Implementierung noch zu früh ist, erwarten, dass die Funktionsgruppe in den nächsten Monaten weiterhin wächst.</span><span class="sxs-lookup"><span data-stu-id="08e3c-187">Microsoft Edge implementation is still early, expect the feature set to continue to grow in the coming months.</span></span> <span data-ttu-id="08e3c-188">Das Ziel für die Microsoft Edge-Implementierung ist die Interoperabilität im gesamten Internet sowie die langfristige Kommunikation in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="08e3c-188">The goal for Microsoft Edge implementation is interoperability across the web today as well as with the real-time communications industry in the long term.</span></span>



## <span data-ttu-id="08e3c-189">API-Referenz</span><span class="sxs-lookup"><span data-stu-id="08e3c-189">API reference</span></span>

[<span data-ttu-id="08e3c-190">ORTC (Objekt Echtzeitkommunikation)</span><span class="sxs-lookup"><span data-stu-id="08e3c-190">ORTC (Object Real-Time Communications)</span></span>](https://msdn.microsoft.com/library/Mt433097)

## <span data-ttu-id="08e3c-191">Demos</span><span class="sxs-lookup"><span data-stu-id="08e3c-191">Demos</span></span>

[<span data-ttu-id="08e3c-192">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="08e3c-192">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[<span data-ttu-id="08e3c-193">ORTC-Telefonanruf</span><span class="sxs-lookup"><span data-stu-id="08e3c-193">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[<span data-ttu-id="08e3c-194">ORTC-Demo</span><span class="sxs-lookup"><span data-stu-id="08e3c-194">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## <span data-ttu-id="08e3c-195">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="08e3c-195">Related topics</span></span>

[<span data-ttu-id="08e3c-196">ORTC-API steht jetzt in Microsoft Edge zur Verfügung</span><span class="sxs-lookup"><span data-stu-id="08e3c-196">ORTC API is now available in Microsoft Edge</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[<span data-ttu-id="08e3c-197">SimpleWebRTC: Verwenden Sie die ORTC-API von Microsoft Edge und die WebRTC-APIs in Chrome und Firefox, um browserübergreifende Konferenzgespräche zu führen.</span><span class="sxs-lookup"><span data-stu-id="08e3c-197">SimpleWebRTC: Use Microsoft Edge's ORTC API and the WebRTC APIs in Chrome and Firefox to make cross-browser conference calls.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[<span data-ttu-id="08e3c-198">Ermöglichen Sie nahtlose Kommunikationsmöglichkeiten für das Internet mit Skype, Skype for Business und Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="08e3c-198">Enabling Seamless Communication Experiences for the Web with Skype, Skype for Business, and Microsoft Edge.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[<span data-ttu-id="08e3c-199">ORTC (Objekt-Echtzeitkommunikation) Community-Gruppe</span><span class="sxs-lookup"><span data-stu-id="08e3c-199">ORTC (OBJECT REAL-TIME COMMUNICATIONS) COMMUNITY GROUP</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## <span data-ttu-id="08e3c-200">Spezifikation</span><span class="sxs-lookup"><span data-stu-id="08e3c-200">Specification</span></span>

[<span data-ttu-id="08e3c-201">W3C Object RTC (ORTC)-API für WebRTC</span><span class="sxs-lookup"><span data-stu-id="08e3c-201">W3C Object RTC (ORTC) API for WebRTC</span></span>](http://draft.ortc.org/)  
