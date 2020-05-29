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
# Objekt-RTC-API

Mit der Objekt-Echtzeitkommunikation (ORTC) können Medien (Audio und/oder Video) über systemeigene JavaScript-APIs in Echtzeit direkt zwischen Webbrowsern, mobilen Geräten und Servern gestreamt (gesendet und empfangen) werden.

> [!NOTE]
> Microsoft Edge implementiert nun ORTC für Windows 10-Geräte. Diese Implementierung unterscheidet sich jedoch von der neuesten Version der [ORTC-API](https://go.microsoft.com/fwlink/p/?LinkID=690096). ORTC hat sich seit der Entwicklung und Veröffentlichung von Microsoft Edge weiterentwickelt – der Browser implementiert nicht alle Objekte oder Methoden innerhalb der ORTC-API und umfasst Erweiterungen, die derzeit nicht in der Spezifikation enthalten sind. Weiterentwicklung wird mit dem Ziel fortgesetzt, Entwicklern auf der ganzen Welt zu ermöglichen, Erfahrungen zu erstellen, die die Möglichkeit beinhalten, mit Skype-Nutzern und anderen WebRTC kompatiblen Kommunikationsdiensten zu sprechen.



Um eine praktische Erfahrung mit ORTC zu erhalten, probieren Sie die folgenden Demos auf Test Drive aus:
-  [SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [ORTC-Telefonanruf](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [ORTC-Demo](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


Weitere Informationen zu ORTC finden Sie unter [ORTC-API steht jetzt in Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) im Microsoft Edge dev-Blog zur Verfügung.


## Übersichtsdiagramm


Das folgende Diagramm enthält eine Zusammenfassung, in der die Beziehungen zwischen ORTC-Objekten beschrieben sind. Horizontale oder schräge Pfeile kennzeichnen den Fluss von Medien oder Daten, während vertikale Pfeile Interaktionen mithilfe von Methoden und Ereignissen kennzeichnen.

ORTC verwendet "*Absender*"-, "*Empfänger*"-und "*Transport*"-Objekte, die über "*Funktionen*" verfügen, die beschreiben, was Sie tun können, sowie "*Parameter*", die definieren, wozu Sie konfiguriert sind. "*Tracks*" erfasst und codiert Mediendatenströme von Absendern, reist über Transporte und wird dann von Empfängern dekodiert, die den Mediendatenstrom in Video-und Audiotags umwandeln.

![Microsoft Edge-ORTC-Flussdiagramm ](./../media/ortc_diagram.png) in der obigen Abbildung [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) codiert die als eingabebereit gestellte Spur, die über a oder a transportiert wird [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) . Das Senden von DTMF-Tönen (Dual Tone Multi Frequency) wird über das [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .

[`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495)Und [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) verwenden Sie einen [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) , um einen Kommunikationspfad zum Erreichen des empfangenden Peers auszuwählen `RTCIceTransport` , der wiederum mit einem `RTCDtlsTransport` oder einem `RTCSrtpSdesTransport` Demultiplexen von Medien zu dem verbunden ist [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) . Anschließend wird das `RTCRtpReceiver` Medium decodiert, wodurch eine Spur entsteht, die von einem Audio-oder Video-Tag gerendert wird.

Auch mehrere andere Objekte spielen eine Rolle. Der [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) sammelt ortsansässige Ice-Kandidaten zur Verwendung durch ein einzelnes [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) Objekt. In den verbleibenden Abschnitten der API werden Details zu den RTP- *Funktionen* und- *Parametern*, *Betriebsstatistiken* und Kompatibilität mit der [WebRTC 1,0-API](https://go.microsoft.com/fwlink/p/?LinkID=627573)ausgefüllt.

> [!NOTE]
> Da Microsoft Edge den Datenkanal nicht implementiert, werden die `RTCDataChannel` `RTCSctpTransport` Objekte und nicht unterstützt.




## In der ersten Microsoft Edge-Implementierung unterstützte Komponenten


* **ORTC-API-Unterstützung.** Die Audio-und Videokommunikation ist der Hauptfokus, einschließlich der folgenden Objekte:,,,, sowie [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) die [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) Schnittstellen, die nicht direkt im Diagramm angezeigt werden.
* **RTP/RTCP-Multiplexing-Unterstützung.** [`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)ist für die Verwendung mit [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) . A/V-Multiplexing wird ebenfalls unterstützt.
* **Betäubung/Turn/ICE-Unterstützung.** Stun [(RFC 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), Turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) sowie Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621)werden unterstützt. Innerhalb des Eises wird eine reguläre Nominierung unterstützt, wobei eine aggressive Nominierung teilweise unterstützt wird (als Empfänger). DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) wird basierend auf DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629)unterstützt.
* **Codec-Unterstützung.** Für [Audio-Codecs](https://msdn.microsoft.com/library/Mt599587)unterstützen wir g. 711, g. 722, Opus und Silk. Darüber hinaus unterstützen wir Comfort Noise (CN) und DTMF entsprechend den RTCWEB-Audioanforderungen. Für Video unterstützen wir derzeit den [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) von Skype-Diensten verwendeten Codec und unterstützen erweiterte Funktionen, wie etwa die Übertragungen, skalierbare Videocodierung und die Weiterleitung von Fehlerkorrekturen. Wir arbeiten daran, interoperables Video mit H. 264 zu ermöglichen.

> [!NOTE]
> Wenn Sie mit WebRTC 1,0-Implementierungen vertraut sind und an der Entwicklung der Objekt Unterstützung innerhalb von WebRTC 1,0 und ORTC interessiert sind, empfehlen wir die folgende Präsentation von Google, Microsoft und Hookflash aus der 2014 IIT RTC-Konferenz: "[ORTC-API-Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)".




## Code Fluss auf App-Ebene für 1:1-Kommunikation


In diesem Szenario fungieren zwei Windows 10-Computer als zwei Peers mit einem Webserver als Signalisierungskanal zum Austauschen von Informationen zwischen den Peers, damit eine Verbindung zwischen Ihnen hergestellt werden kann.

Die folgenden Schritte sind auf Vorgänge beschränkt, die von einem Peer ausgeführt werden. Beide Peers müssen ähnliche Schritte durchlaufen, um die 1:1-Kommunikation einzurichten. Wenn Sie die folgenden Codeausschnitte besser verstehen möchten, lesen Sie die [Demo zu Microsoft Edge-Test Laufwerk](https://go.microsoft.com/fwlink/p/?LinkID=627635).

In diesem Beispiel wird Audio-Video-und RTP-RTCP-Multiplexing verwendet, sodass Sie nur einen einzigen Ice-und DTLS-Transport sehen, der zum Transport von RTP-und RTCP-Paketen für Audio-und Videoübertragungen verwendet wird.

`Step #1.` Erstellen Sie [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) ein Objekt (beispielsweise die [Media Capture-und Streams-API](./../multimedia/media-Capture-and-Streams.md)) mit einer Audiospur und einer Videospur.

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

`Step #2.` Erstellen [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) Sie die, und aktivieren Sie lokal, [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) um Sie an Remote Peer zu signalisieren.

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

Zum Schutz der Privatsphäre von Benutzern bietet Microsoft Edge eine Option, mit der ein Benutzer steuern kann, ob die Objekte lokale Host-IP-Adressen verfügbar gemacht werden können [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) . Eine Schnittstellenoption wird bereitgestellt, um diese Einstellung zu aktivieren.

In der [Demo zu Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635)wurde ein Turn Server eingerichtet. Dieser Turn-Server hat einen sehr geringen Durchsatz und ist daher auf die Verwendung von Demo-Seiten limitiert.

`Step #3.` Erstellen [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) Sie das für Audio und Video, und bereiten Sie die Behandlung von Remote [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) auf dem ICE-Transport vor.

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

Eine weitere Möglichkeit besteht darin, alle Remote-Ice-Kandidaten in einem Array zu sammeln `remoteCandidates` und `iceTr.setRemoteCandidates(remoteCandidates)` alle entfernten Kandidaten zusammen hinzuzufügen.

`Step #4.` Erstellen Sie den DTLS-Transport.

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` Erstellen Sie die Absender-und Empfängerobjekte.

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

Schritt #6. Abrufen der Empfänger-und Absender Funktionen

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` Ice/DTLS-Parameter und Sende-und Empfangsfunktionen können ausgetauscht werden.

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

`Step #8.` Rufen Sie Remote-params ab, starten Sie die [`ICE`](https://msdn.microsoft.com/library/Mt433112) und [`DTLS`](https://msdn.microsoft.com/library/Mt502495) Transporte, und legen Sie die Audio-und Video-Sende-und Empfangsparameter ein.

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

Nachfolgend finden Sie ein Skelett der Hilfsfunktionen. Weitere Informationen finden Sie in der [Demo zu Microsoft Edge-Test Laufwerk](https://go.microsoft.com/fwlink/p/?LinkID=627635).

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

`Step #9.` Rendern und Abspielen des Remote-Mediendatenstroms über ein Video-Tag.

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

Sobald Sie mit der Einrichtung von 1:1-anrufen vertraut sind, wenden Sie die gleichen Prinzipien an, um kleine Gruppenanrufe mithilfe einer Mesh-Topologie einzurichten, wobei jeder Peer eine 1:1-Verbindung mit dem restlichen Teil der Gruppe hat. Da die parallele Verzweigung auf der Microsoft Edge-Plattform nicht unterstützt wird, sollte diese über 1:1-Signalisierung gehandhabt werden, damit unabhängige [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) und [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) Objekte für jede Verbindung verwendet werden.

## Details zur Implementierung in Microsoft Edge


Die ORTC-Spezifikation war relativ stabil, da die ORTC-Community-Gruppe den "Aufruf für Implementierungen" herausgegeben hat und erhebliche Herausforderungen auf der JavaScript-API-Ebene nicht erwartet werden. Auf dieser Grundlage wurde die Microsoft Edge-Implementierung für browserübergreifende Interoperabilitätstests auf Protokollebene veröffentlicht.

Einige Einschränkungen in der Microsoft Edge-Implementierung sollten beachtet werden:

* `RTCIceTransportController` wird nicht unterstützt. Die Microsoft Edge-Implementierung verarbeitet das Einfrieren/Aufheben der Fixierung von Eis pro Transport, sodass die Bestellung `IceTransports` nicht erforderlich ist. Dieser Ansatz sollte mit vorhandenen Implementierungen interagieren.
* `RtpListener` wird noch nicht unterstützt. Dies bedeutet, dass SSRCs (Datenstrom-und Synchronisierungs Quellen) im Voraus im [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .
* Forking wird in den beiden, oder nicht unterstützt `IceTransport` `IceGatherer` `DtlsTransport` . Die Lösung für `DtlsTransport` Forking wird in der ORTC-Community-Gruppe noch erörtert.
* RTP/RTCP-nicht-MUX mit `DtlsTransport` wird noch nicht unterstützt. Wenn `DtlsTransport` Sie Ihre Anwendung verwenden, muss RTP/RTCP-MUX unterstützt werden.
* In [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) wird Microsoft Edge die meisten Codierungs Qualitätssteuer Elemente derzeit ignoriert, erfordert jedoch das Festlegen der "Active"-und "SSRC"-Attribute.
* Das `icecandidatepairchanged` Ereignis wird noch nicht unterstützt. Sie können die Kandidaten paar Informationen über die [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) Methode extrahieren.
* Microsoft Edge unterstützt derzeit keine der `DataChannel` Funktionen, die derzeit in der ORTC-Spezifikation definiert sind.

#### Wir freuen uns

Microsoft Edge-Implementierung noch zu früh ist, erwarten, dass die Funktionsgruppe in den nächsten Monaten weiterhin wächst. Das Ziel für die Microsoft Edge-Implementierung ist die Interoperabilität im gesamten Internet sowie die langfristige Kommunikation in Echtzeit.



## API-Referenz

[ORTC (Objekt Echtzeitkommunikation)](https://msdn.microsoft.com/library/Mt433097)

## Demos

[SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[ORTC-Telefonanruf](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[ORTC-Demo](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## Verwandte Themen

[ORTC-API steht jetzt in Microsoft Edge zur Verfügung](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[SimpleWebRTC: Verwenden Sie die ORTC-API von Microsoft Edge und die WebRTC-APIs in Chrome und Firefox, um browserübergreifende Konferenzgespräche zu führen.](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[Ermöglichen Sie nahtlose Kommunikationsmöglichkeiten für das Internet mit Skype, Skype for Business und Microsoft Edge.](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[ORTC (Objekt-Echtzeitkommunikation) Community-Gruppe](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## Spezifikation

[W3C Object RTC (ORTC)-API für WebRTC](http://draft.ortc.org/)  
