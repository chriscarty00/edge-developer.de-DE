---
title: MSApp-API-Referenz
description: Stellt Hilfsfunktionen bereit, mit deren Hilfe Sie BLOB-und MSStream-Objekte erstellen können. MSApp-Objekte und-Member werden für Windows-apps mit JavaScript unterstützt.
author: mattwojo
ms.author: mattwoj
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, Dateiupload, Blog, MSStream, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 0ed8cefa918bd44f3b2c4e8312d2c1d3b4ace8fc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568720"
---
# <span data-ttu-id="d631c-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="d631c-105">MSApp</span></span>

<span data-ttu-id="d631c-106">Das MSApp-Objekt und seine Member werden nur für Windows-Apps unterstützt, die JavaScript verwenden (einschließlich PWAs Zugriff auf Windows-API-Features).</span><span class="sxs-lookup"><span data-stu-id="d631c-106">The MSApp object and its members are supported only for Windows apps using JavaScript (including PWAs accessing Windows API features).</span></span> <span data-ttu-id="d631c-107">Das MSApp-Objekt ist nur im lokalen Kontext eines HTML-Dokuments in einer Windows-app vorhanden, die über das URI-Schema "MS-AppX" geladen wird. Andernfalls ist das Objekt nicht vorhanden (und daher sind keine seiner Methoden und Eigenschaften verfügbar).</span><span class="sxs-lookup"><span data-stu-id="d631c-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>

<span data-ttu-id="d631c-108">Sie stellt Hilfsfunktionen bereit, mit deren Hilfe Sie [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) -und [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) -Objekte erstellen können.</span><span class="sxs-lookup"><span data-stu-id="d631c-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**<span data-ttu-id="d631c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="d631c-109">Methods</span></span>**](#msapp-methods) | <span data-ttu-id="d631c-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getviewl](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="d631c-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span> |

| | |
| :--- | :--- |
| [**<span data-ttu-id="d631c-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d631c-111">Constants</span></span>**](#msapp-constants) | <span data-ttu-id="d631c-112">[aktuell](#current), [groß](#high), [inaktiv](#idle), [Normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="d631c-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>|

| | |
| :--- | :--- |
| [<span data-ttu-id="d631c-113">**MSAppAsyncOperation** -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d631c-113">**MSAppAsyncOperation** interface</span></span>](#msappasyncoperation) | [<span data-ttu-id="d631c-114">start</span><span class="sxs-lookup"><span data-stu-id="d631c-114">start</span></span>](#start) |

## <span data-ttu-id="d631c-115">MSApp-Methoden</span><span class="sxs-lookup"><span data-stu-id="d631c-115">MSApp Methods</span></span>

### <span data-ttu-id="d631c-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="d631c-116">clearTemporaryWebDataAsync</span></span> 
<span data-ttu-id="d631c-117">Löscht Cache-und indexedDB-Daten für die APP oder [WebView](../../webview.md).</span><span class="sxs-lookup"><span data-stu-id="d631c-117">Clears cache and indexedDB data for the app or [WebView](../../webview.md).</span></span>

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### <span data-ttu-id="d631c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-118">Parameters</span></span>
<span data-ttu-id="d631c-119">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d631c-119">This method has no parameters.</span></span>

#### <span data-ttu-id="d631c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-120">Return value</span></span>
<span data-ttu-id="d631c-121">Geben[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="d631c-121">Type: [`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span></span>

<span data-ttu-id="d631c-122">Stellt eine asynchrone Aktion dar.</span><span class="sxs-lookup"><span data-stu-id="d631c-122">Represents an asynchronous action.</span></span>

### <span data-ttu-id="d631c-123">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="d631c-123">createBlobFromRandomAccessStream</span></span>
<span data-ttu-id="d631c-124">Erstellt ein [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) aus einem [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) Objekt.</span><span class="sxs-lookup"><span data-stu-id="d631c-124">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span> <span data-ttu-id="d631c-125">Diese Methode sollte beim Umgang mit `IRandomAccessStream` Objekten in Apps verwendet werden, um ein W3C-basiertes Objekt aus dem Datenstrom zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d631c-125">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span> <span data-ttu-id="d631c-126">Nachdem das BLOB erstellt wurde, kann es mit [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL-APIs](https://developer.mozilla.org/docs/Web/API/URL)und [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d631c-126">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span> 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### <span data-ttu-id="d631c-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-127">Parameters</span></span>

`type` <span data-ttu-id="d631c-128">in</span><span class="sxs-lookup"><span data-stu-id="d631c-128">[in]</span></span>

|<span data-ttu-id="d631c-129">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-129">Type</span></span> | <span data-ttu-id="d631c-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-130">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d631c-131">String</span></span> | <span data-ttu-id="d631c-132">Inhaltstyp der Daten.</span><span class="sxs-lookup"><span data-stu-id="d631c-132">Content type of the data.</span></span> <span data-ttu-id="d631c-133">Diese Zeichenfolge sollte das Format aufweisen, das in dem in Abschnitt 3,7 von RFC 2616 definierten Media-Type-Token angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d631c-133">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>

`stream` <span data-ttu-id="d631c-134">in</span><span class="sxs-lookup"><span data-stu-id="d631c-134">[in]</span></span>

|<span data-ttu-id="d631c-135">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-135">Type</span></span> | <span data-ttu-id="d631c-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-136">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-137">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-137">Any</span></span> | <span data-ttu-id="d631c-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) , der im BLOB gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d631c-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>

#### <span data-ttu-id="d631c-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-139">Return value</span></span>
|<span data-ttu-id="d631c-140">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-140">Type</span></span> | <span data-ttu-id="d631c-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-141">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-142">BLOB</span><span class="sxs-lookup"><span data-stu-id="d631c-142">Blob</span></span> | <span data-ttu-id="d631c-143">Neues BLOB-Objekt, das den Datenstrom enthält.</span><span class="sxs-lookup"><span data-stu-id="d631c-143">New blob object that contains the stream.</span></span>

#### <span data-ttu-id="d631c-144">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="d631c-144">Exceptions</span></span>
|<span data-ttu-id="d631c-145">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="d631c-145">Exception</span></span> | <span data-ttu-id="d631c-146">Bedingung</span><span class="sxs-lookup"><span data-stu-id="d631c-146">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-147">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="d631c-147">TypeMismatchError</span></span> | <span data-ttu-id="d631c-148">Der Knotentyp ist mit dem erwarteten Parametertyp nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d631c-148">The node type is incompatible with the expected parameter type.</span></span> <span data-ttu-id="d631c-149">Bei älteren Versionen als Internet Explorer 10 wird TYPE_MISMATCH_ERR zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d631c-149">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

#### <span data-ttu-id="d631c-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-150">Remarks</span></span>
<span data-ttu-id="d631c-151">Erstellt ein BLOB aus Windows-Runtime-Typen über den MSApp-Namespace für das Window-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d631c-151">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span> <span data-ttu-id="d631c-152">Diese Methode erstellt ein BLOB, das im Wesentlichen ein Licht Wrapper über dem Objekt ist, das [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) ihm bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d631c-152">This method will create a blob that is essentially a light wrapper over the [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span> <span data-ttu-id="d631c-153">Das BLOB besitzt die Lebensdauer dieses Streams, und der Datenstrom wird geschlossen, wenn das BLOB zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="d631c-153">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span> 

#### <span data-ttu-id="d631c-154">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d631c-154">Example</span></span>

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### <span data-ttu-id="d631c-155">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="d631c-155">createDataPackage</span></span>
<span data-ttu-id="d631c-156">Wandelt den angegebenen Bereich des Benutzers oder der Anwendung in ein HTML-Fragment um, das freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d631c-156">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### <span data-ttu-id="d631c-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-157">Parameters</span></span>
`object` <span data-ttu-id="d631c-158">in</span><span class="sxs-lookup"><span data-stu-id="d631c-158">[in]</span></span>

|<span data-ttu-id="d631c-159">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-159">Type</span></span> | <span data-ttu-id="d631c-160">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-160">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-161">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-161">Any</span></span> | <span data-ttu-id="d631c-162">Dieser Bereich kann entweder aus einem Selection-Objekt, beispielsweise: `window.selection.getRangeAt(0)` oder manuell, erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d631c-162">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>

#### <span data-ttu-id="d631c-163">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-163">Return value</span></span>
|<span data-ttu-id="d631c-164">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-164">Type</span></span> | <span data-ttu-id="d631c-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-165">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-166">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-166">Any</span></span> | <span data-ttu-id="d631c-167">Enthält das HTML-Markup für den angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="d631c-167">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="d631c-168">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-168">Remarks</span></span>
<span data-ttu-id="d631c-169">Diese Methode unterstützt nur den [DOM-Bereich (Document Object Model)](https://developer.mozilla.org/docs/Web/API/Range), nicht [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="d631c-169">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span> <span data-ttu-id="d631c-170">Das zurückgegebene Datenpaket für den angegebenen Bereich enthält HTML-Markup im Zwischenablageformat.</span><span class="sxs-lookup"><span data-stu-id="d631c-170">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>

<span data-ttu-id="d631c-171">Es gibt keine verfügbaren Eigenschaften für das zurückgegebene Datenpaket.</span><span class="sxs-lookup"><span data-stu-id="d631c-171">There are no available properties for the returned data package.</span></span>

### <span data-ttu-id="d631c-172">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="d631c-172">createDataPackageFromSelection</span></span> 
<span data-ttu-id="d631c-173">Wandelt die Auswahl des Benutzers oder der Anwendung in ein HTML-Fragment um, das freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d631c-173">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### <span data-ttu-id="d631c-174">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-174">Parameters</span></span>
<span data-ttu-id="d631c-175">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d631c-175">This method has no parameters.</span></span>

#### <span data-ttu-id="d631c-176">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-176">Return value</span></span>
|<span data-ttu-id="d631c-177">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-177">Type</span></span> | <span data-ttu-id="d631c-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-178">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-179">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-179">Any</span></span> | <span data-ttu-id="d631c-180">Enthält das HTML-Markup für den angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="d631c-180">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="d631c-181">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-181">Remarks</span></span>
<span data-ttu-id="d631c-182">Das zurückgegebene Datenpaket für die Auswahl enthält HTML-Markup im Zwischenablageformat.</span><span class="sxs-lookup"><span data-stu-id="d631c-182">The returned data package for the selection contains HTML markup in clipboard format.</span></span> <span data-ttu-id="d631c-183">Wenn keine Benutzerauswahl an einer beliebigen Stelle auf der Benutzeroberfläche der Anwendung vorhanden ist, wird `createDataPackageFromSelection` NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d631c-183">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns null.</span></span>

<span data-ttu-id="d631c-184">Es gibt keine verfügbaren Eigenschaften für das zurückgegebene Datenpaket.</span><span class="sxs-lookup"><span data-stu-id="d631c-184">There are no available properties for the returned data package.</span></span>
 
### <span data-ttu-id="d631c-185">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="d631c-185">createFileFromStorageFile</span></span> 
<span data-ttu-id="d631c-186">Konvertiert eine [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) in ein Standard [`File`](https://developer.mozilla.org/docs/Web/API/File) -W3C-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d631c-186">Converts a [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) to a standard W3C [`File`](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### <span data-ttu-id="d631c-187">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-187">Parameters</span></span>
`storageFile` <span data-ttu-id="d631c-188">in</span><span class="sxs-lookup"><span data-stu-id="d631c-188">[in]</span></span>

|<span data-ttu-id="d631c-189">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-189">Type</span></span> | <span data-ttu-id="d631c-190">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-190">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-191">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-191">Any</span></span> | <span data-ttu-id="d631c-192">Enthält die Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="d631c-192">Contains the storage file.</span></span>

#### <span data-ttu-id="d631c-193">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="d631c-193">Exceptions</span></span>
|<span data-ttu-id="d631c-194">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="d631c-194">Exception</span></span> | <span data-ttu-id="d631c-195">Bedingung</span><span class="sxs-lookup"><span data-stu-id="d631c-195">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-196">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="d631c-196">TypeMismatchError</span></span> | <span data-ttu-id="d631c-197">Der angegebene W3C-Dateiverweis ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d631c-197">The specified W3C file reference is invalid.</span></span> <span data-ttu-id="d631c-198">Bei älteren Versionen als Internet Explorer 10 wird TYPE_MISMATCH_ERR zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d631c-198">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

### <span data-ttu-id="d631c-199">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="d631c-199">createStreamFromInputStream</span></span>  

<span data-ttu-id="d631c-200">Erstellt eine [`MSStream`](https://msdn.microsoft.com/library/hh772328) von einer [`InputStream`](https://msdn.microsoft.com/library/hh772327) .</span><span class="sxs-lookup"><span data-stu-id="d631c-200">Creates an [`MSStream`](https://msdn.microsoft.com/library/hh772328) from an [`InputStream`](https://msdn.microsoft.com/library/hh772327).</span></span>  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### <span data-ttu-id="d631c-201">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-201">Parameters</span></span>
`type` <span data-ttu-id="d631c-202">in</span><span class="sxs-lookup"><span data-stu-id="d631c-202">[in]</span></span>

|<span data-ttu-id="d631c-203">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-203">Type</span></span> | <span data-ttu-id="d631c-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-204">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-205">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-205">DOMString</span></span> | <span data-ttu-id="d631c-206">Inhaltstyp der Daten.</span><span class="sxs-lookup"><span data-stu-id="d631c-206">Content type of the data.</span></span> <span data-ttu-id="d631c-207">Diese Zeichenfolge sollte das Format aufweisen, das in dem in Abschnitt 3,7 von RFC 2616 definierten Media-Type-Token angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d631c-207">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span> <span data-ttu-id="d631c-208">([Siehe MIME-Typen,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. Text/Plain, Text/HTML, Bild/JPEG, Bild/PNG, Audio/MPEG, Audio/OGG, Audio/\*, Video/MP4 usw.).</span><span class="sxs-lookup"><span data-stu-id="d631c-208">([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) ie. text/plain, text/html, image/jpeg, image/png, audio/mpeg, audio/ogg, audio/\*, video/mp4, etc.).</span></span> 

`inputStream` <span data-ttu-id="d631c-209">in</span><span class="sxs-lookup"><span data-stu-id="d631c-209">[in]</span></span>

|<span data-ttu-id="d631c-210">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-210">Type</span></span> | <span data-ttu-id="d631c-211">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-211">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-212">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-212">Any</span></span> | <span data-ttu-id="d631c-213">Die [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) in der gespeichert werden soll `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="d631c-213">The [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>

#### <span data-ttu-id="d631c-214">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-214">Remarks</span></span>
<span data-ttu-id="d631c-215">Diese Methode verwendet einen Inhaltstyp und den `IInputStream` Verweis.</span><span class="sxs-lookup"><span data-stu-id="d631c-215">This method takes a content-type, and the `IInputStream` reference.</span></span> <span data-ttu-id="d631c-216">Die Methode überprüft dann, ob es sich bei dem übergebenen Datenstrom Verweis um eine Instanz von Type handelt `IInputStream` , und wenn dies nicht der Fall ist, wird ausgelöst `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="d631c-216">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span> <span data-ttu-id="d631c-217">Wenn kein Fehler auftritt, wird `createStreamFromInputStream` ein `MSStream` (aus seinen Eingaben) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d631c-217">If no error occurs, `createStreamFromInputStream` creates an `MSStream` (from its inputs).</span></span>

#### <span data-ttu-id="d631c-218">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d631c-218">Example</span></span>
<span data-ttu-id="d631c-219">Eine `IInputStream` kann verwendet werden, um eine zu erstellen `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="d631c-219">An `IInputStream` can be used to create an `MSStream`.</span></span> <span data-ttu-id="d631c-220">Da `MSStreams` es sich um eigenständige Objekte mit einmaliger Verwendung handelt, werden alle von Ihnen erstellten URLs `URL.createObjectURL` beim erstmaligen lösen durch das Image-Element aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="d631c-220">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span> <span data-ttu-id="d631c-221">Darüber hinaus schlägt die Anforderung einer zweiten URL für dieses Objekt, nachdem der Datenstrom verwendet wurde, fehl.</span><span class="sxs-lookup"><span data-stu-id="d631c-221">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### <span data-ttu-id="d631c-222">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="d631c-222">execAsyncAtPriority</span></span> 
<span data-ttu-id="d631c-223">Plant einen Rückruf, der zu einem späteren Zeitpunkt entsprechend der angegebenen Priorität ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d631c-223">Schedules a callback to be executed at a later time according to the given priority.</span></span> 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### <span data-ttu-id="d631c-224">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-224">Parameters</span></span>
`asynchronousCallback` <span data-ttu-id="d631c-225">in</span><span class="sxs-lookup"><span data-stu-id="d631c-225">[in]</span></span>

|<span data-ttu-id="d631c-226">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-226">Type</span></span> | <span data-ttu-id="d631c-227">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-227">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-228">Funktion</span><span class="sxs-lookup"><span data-stu-id="d631c-228">Function</span></span> | <span data-ttu-id="d631c-229">Die Rückruffunktion, die asynchron ausgeführt werden soll, wird mit der angegebenen Prioritäts Priorität verteilt.</span><span class="sxs-lookup"><span data-stu-id="d631c-229">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>

`priority` <span data-ttu-id="d631c-230">in</span><span class="sxs-lookup"><span data-stu-id="d631c-230">[in]</span></span>

|<span data-ttu-id="d631c-231">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-231">Type</span></span> | <span data-ttu-id="d631c-232">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-232">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-233">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-233">DOMString</span></span> | <span data-ttu-id="d631c-234">Der kontextbezogene Prioritätswert, in dem der asynchronousCallback-Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d631c-234">The contextual priority value at which the asynchronousCallback callback is run.</span></span> <span data-ttu-id="d631c-235">Siehe [MSApp-Konstanten](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="d631c-235">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="d631c-236">in</span><span class="sxs-lookup"><span data-stu-id="d631c-236">[in]</span></span>

|<span data-ttu-id="d631c-237">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-237">Type</span></span> | <span data-ttu-id="d631c-238">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-238">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-239">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-239">Any</span></span> | <span data-ttu-id="d631c-240">Eine optionale Reihe von Argumenten, die an die synchronousCallback-Rückruffunktion übergeben werden (als Parameter 1 und ein).</span><span class="sxs-lookup"><span data-stu-id="d631c-240">An optional series of arguments that are passed to the synchronousCallback callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="d631c-241">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-241">Return value</span></span>
<span data-ttu-id="d631c-242">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d631c-242">This method does not return a value.</span></span>

#### <span data-ttu-id="d631c-243">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-243">Remarks</span></span>
<span data-ttu-id="d631c-244">Die bereitgestellte `asynchronousCallback` Rückruffunktion wird später asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d631c-244">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span> `asynchronousCallback` <span data-ttu-id="d631c-245">wird entsprechend der angegebenen Priorität versandt.</span><span class="sxs-lookup"><span data-stu-id="d631c-245">will be dispatched according to the provided priority.</span></span> <span data-ttu-id="d631c-246">Die normale Priorität entspricht der vorhandenen [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) Methode.</span><span class="sxs-lookup"><span data-stu-id="d631c-246">Normal priority is equivalent to the existing [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span> <span data-ttu-id="d631c-247">Wenn der Rückruf ausgeführt wird, wird die aktuelle kontextbezogene Priorität für die Dauer der Ausführung des Rückrufs auf den angegebenen Prioritäts Parameterwert gesetzt.</span><span class="sxs-lookup"><span data-stu-id="d631c-247">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>

<span data-ttu-id="d631c-248">Der `asynchronousCallback` Rückrufparameter kann eine beliebige Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="d631c-248">The `asynchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="d631c-249">Wenn Argumente nach dem Parameter bereitgestellt werden `priority` , werden Sie alle an die Rückruffunktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="d631c-249">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>

<span data-ttu-id="d631c-250">Im Gegensatz dazu `execAtPriority` wird jedes von der Rückruffunktion zurückgegebene Objekt `asynchronousCallback` ignoriert (und nicht über) zurückgegeben `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="d631c-250">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored (and not returned via `execAsyncAtPriority`).</span></span>

### <span data-ttu-id="d631c-251">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="d631c-251">execAtPriority</span></span> 
<span data-ttu-id="d631c-252">Führt die angegebene Rückruffunktion unter der angegebenen Kontext Priorität aus.</span><span class="sxs-lookup"><span data-stu-id="d631c-252">Runs the specified callback function at the given contextual priority.</span></span>

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### <span data-ttu-id="d631c-253">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-253">Parameters</span></span>
`synchronousCallback` <span data-ttu-id="d631c-254">in</span><span class="sxs-lookup"><span data-stu-id="d631c-254">[in]</span></span>

|<span data-ttu-id="d631c-255">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-255">Type</span></span> | <span data-ttu-id="d631c-256">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-256">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-257">Funktion</span><span class="sxs-lookup"><span data-stu-id="d631c-257">Function</span></span> | <span data-ttu-id="d631c-258">Die Rückruffunktion, die mit der angegebenen Prioritäts Kontext Priorität synchron ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d631c-258">The callback function to run synchronously at the given priority contextual priority.</span></span>

`priority` <span data-ttu-id="d631c-259">in</span><span class="sxs-lookup"><span data-stu-id="d631c-259">[in]</span></span>

|<span data-ttu-id="d631c-260">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-260">Type</span></span> | <span data-ttu-id="d631c-261">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-261">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-262">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-262">DOMString</span></span> | <span data-ttu-id="d631c-263">Der angegebene Prioritätswert, auf den der aktuelle kontextabhängige Prioritätswert festgelegt wird, wenn die `synchronousCallback` Rückruffunktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d631c-263">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span> <span data-ttu-id="d631c-264">Siehe [MSApp-Konstanten](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="d631c-264">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="d631c-265">in</span><span class="sxs-lookup"><span data-stu-id="d631c-265">[in]</span></span>

|<span data-ttu-id="d631c-266">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-266">Type</span></span> | <span data-ttu-id="d631c-267">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-267">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-268">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-268">Any</span></span> | <span data-ttu-id="d631c-269">Eine optionale Reihe von Argumenten, die an die `synchronousCallback` Rückruffunktion übergeben werden (als Parameter 1 und ein).</span><span class="sxs-lookup"><span data-stu-id="d631c-269">An optional series of arguments that are passed to the `synchronousCallback` callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="d631c-270">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-270">Return value</span></span>
|<span data-ttu-id="d631c-271">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-271">Type</span></span> | <span data-ttu-id="d631c-272">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-272">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-273">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-273">Any</span></span> | <span data-ttu-id="d631c-274">Gibt den Rückgabewert des `synchronousCallback` Rückrufs (falls zutreffend) zurück.</span><span class="sxs-lookup"><span data-stu-id="d631c-274">Returns the return value of the `synchronousCallback` callback (as applicable).</span></span>

#### <span data-ttu-id="d631c-275">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-275">Remarks</span></span>
<span data-ttu-id="d631c-276">Die bereitgestellte `synchronousCallback` Rückrufmethode wird synchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d631c-276">The provided `synchronousCallback` callback method is execute synchronously.</span></span> <span data-ttu-id="d631c-277">Die aktuelle kontextbezogene Priorität wird für die Dauer der bereitgestellten Rückruffunktion in den angegebenen Prioritätswert (angegeben durch das Prioritäts Argument) geändert.</span><span class="sxs-lookup"><span data-stu-id="d631c-277">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span> <span data-ttu-id="d631c-278">Sobald die Rückruffunktion die Ausführung beendet hat, wird die Priorität vor dem Aufruf an den vorherigen Wert zurückgegeben `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="d631c-278">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span> <span data-ttu-id="d631c-279">Der Rückgabewert von `execAtPriority` ist der Rückgabewert der Rückrufmethode (wie angegeben).</span><span class="sxs-lookup"><span data-stu-id="d631c-279">The return value from `execAtPriority` is the return value of the callback method (as provided).</span></span>
 
<span data-ttu-id="d631c-280">Der `synchronousCallback` Rückrufparameter kann eine beliebige Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="d631c-280">The `synchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="d631c-281">Wenn nach dem Priority-Parameter Argumente bereitgestellt werden, werden Sie an die bereitgestellte Rückrufmethode übergeben.</span><span class="sxs-lookup"><span data-stu-id="d631c-281">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span> <span data-ttu-id="d631c-282">Wenn der Rückrufparameter einen Wert zurückgibt, wird dieser Wert ebenfalls zum Rückgabewert `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="d631c-282">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>

#### <span data-ttu-id="d631c-283">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d631c-283">Example</span></span>

```javascript
var user = Windows.System.UserProfile.UserInformation;

MSApp.execAtPriority(function () { // This callback executes synchronously.
  user.getFirstNameAsync().then(function () { // Dispatches at high priority.
    return user.getLastNameAsync();
  }).done(function () { // Dispatches at high priority.
    // USEFUL CODE HERE
  });
}, MSApp.HIGH); // The second argument of the execAtPriority method.
```

### <span data-ttu-id="d631c-284">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="d631c-284">getCurrentPriority</span></span> 
<span data-ttu-id="d631c-285">Gibt die aktuelle kontextbezogene Priorität zurück.</span><span class="sxs-lookup"><span data-stu-id="d631c-285">Returns the current contextual priority.</span></span>

```javascript
var retval = MSApp.getCurrentPriority();
```

#### <span data-ttu-id="d631c-286">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-286">Parameters</span></span>
<span data-ttu-id="d631c-287">Keine</span><span class="sxs-lookup"><span data-stu-id="d631c-287">None.</span></span> 

#### <span data-ttu-id="d631c-288">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-288">Return value</span></span>
|<span data-ttu-id="d631c-289">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-289">Type</span></span> | <span data-ttu-id="d631c-290">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-290">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-291">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-291">DOMString</span></span> | <span data-ttu-id="d631c-292">Der Rückgabewert ist eine der Zeichenfolgen `MSApp.HIGH` , `MSApp.NORMAL` oder `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="d631c-292">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>

#### <span data-ttu-id="d631c-293">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-293">Remarks</span></span>
<span data-ttu-id="d631c-294">Diese Methode gibt die aktuelle kontextbezogene Priorität zurück (siehe [`MSApp Constants`](#msapp-constants) ), die über und geändert werden kann `execAtPriority` `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="d631c-294">This method returns the current contextual priority (see [`MSApp Constants`](#msapp-constants)), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>

#### <span data-ttu-id="d631c-295">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d631c-295">Example</span></span>

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### <span data-ttu-id="d631c-296">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="d631c-296">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="d631c-297">Synchrone API, die als veraltet markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d631c-297">Synchronous API that has been deprecated.</span></span> <span data-ttu-id="d631c-298">Informationen zu Windows 10 finden Sie unter `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="d631c-298">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span> <span data-ttu-id="d631c-299">Informationen zu Windows 8-und 8,1-apps finden Sie im MSDN-Eintrag für [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="d631c-299">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="d631c-300">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="d631c-300">getHtmlPrintDocumentSourceAsync</span></span>
<span data-ttu-id="d631c-301">Gibt den Quellinhalt zurück, der gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d631c-301">Returns the source content that is to be printed.</span></span>

#### <span data-ttu-id="d631c-302">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-302">Parameters</span></span>
`htmlDoc` <span data-ttu-id="d631c-303">in</span><span class="sxs-lookup"><span data-stu-id="d631c-303">[in]</span></span>

|<span data-ttu-id="d631c-304">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-304">Type</span></span> | <span data-ttu-id="d631c-305">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-305">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-306">Dokument</span><span class="sxs-lookup"><span data-stu-id="d631c-306">Document</span></span> | <span data-ttu-id="d631c-307">Das HTML-Dokument, das gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d631c-307">The HTML document to be printed.</span></span> <span data-ttu-id="d631c-308">Dies kann das Stammdokument, das Dokument in einem IFRAME, ein Dokument Fragment oder ein SVG-Dokument sein.</span><span class="sxs-lookup"><span data-stu-id="d631c-308">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span> <span data-ttu-id="d631c-309">Beachten Sie, dass htmlDoc ein Dokument und kein Element sein muss.</span><span class="sxs-lookup"><span data-stu-id="d631c-309">Be aware that htmlDoc must be a document, not an element.</span></span>

#### <span data-ttu-id="d631c-310">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d631c-310">Example 1</span></span>

```javascript
var printTask = event.request.createPrintTask(title, function (args) {
                var deferral = args.getDeferral();
                var getPrintDocumentSourceAsync;
                if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                    getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
                } else {
                    getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
                }
                getPrintDocumentSourceAsync.then(function (source) {
                    args.setSource(source);
                    deferral.complete();
                }, function (error) {
                    console.error(error);
                    deferral.complete();
                });
            });
```

#### <span data-ttu-id="d631c-311">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d631c-311">Example 2</span></span>

```javascript
    function registerForPrintContract() {
            var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
            printManager.onprinttaskrequested = onPrintTaskRequested;
            console.log("Print Contract registered. Use the Print button to print.", "sample", "status");
    }
    
    // Variable to hold the document source to print
    var gHtmlPrintDocumentSource = null;
    
    // Print event handler for printing via the PrintManager API.
    function onPrintTaskRequested(printEvent) {
        var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
            args.setSource(gHtmlPrintDocumentSource);
    
            // Register the handler for print task completion event
            printTask.oncompleted = onPrintTaskCompleted;
        });
    }
    
    // Print Task event handler is invoked when the print job is completed.
    function onPrintTaskCompleted(printTaskCompletionEvent) {
        // Notify the user about the failure
        if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
            console.log("Failed to print.", "sample", "error");
        }
    }
    
    // Executed just before printing.
    var beforePrint = function () {
        // Replace with code to be executed just before printing the current document:
    };
    
    // Executed immediately after printing.
    var afterPrint = function () {
        // Replace with code to be executed immediately after printing the current document:
    };
    
    function printButtonHandler() {
        // Optionally, functions to be executed immediately before and after printing can be configured as following:
        window.document.body.onbeforeprint = beforePrint;
        window.document.body.onafterprint = afterPrint;
    
        // Get document source to print
        MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
            gHtmlPrintDocumentSource = htmlPrintDocumentSource;
    
            // If the print contract is registered, the print experience is invoked.
            Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
        });
    }
```

### <span data-ttu-id="d631c-312">GetView-Nr.</span><span class="sxs-lookup"><span data-stu-id="d631c-312">getViewId</span></span> 
<span data-ttu-id="d631c-313">Unterstützung für mehrere Fenster.</span><span class="sxs-lookup"><span data-stu-id="d631c-313">Support for multiple windows.</span></span> 

> [!NOTE] 
> <span data-ttu-id="d631c-314">In Win 8.1 JavaScript UWP-apps wurden mehrere Fenster unterstützt, die MSApp-DOM-APIs verwenden, die jetzt depricated sind.</span><span class="sxs-lookup"><span data-stu-id="d631c-314">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span> <span data-ttu-id="d631c-315">Verwenden Sie für Windows 10 `window.open` `window` und das neue `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="d631c-315">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>

| <span data-ttu-id="d631c-316">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-316">Description</span></span> |<span data-ttu-id="d631c-317">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d631c-317">Windows 10</span></span> | <span data-ttu-id="d631c-318">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="d631c-318">Windows 8.1</span></span> |  
|:---- |:---- |:--- |  
| <span data-ttu-id="d631c-319">Neues Fenster erstellen</span><span class="sxs-lookup"><span data-stu-id="d631c-319">Create new window</span></span> | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|<span data-ttu-id="d631c-320">Neues Fensterobjekt</span><span class="sxs-lookup"><span data-stu-id="d631c-320">New window object</span></span> | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### <span data-ttu-id="d631c-321">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-321">Parameters</span></span>
`window`

|<span data-ttu-id="d631c-322">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-322">Type</span></span> | <span data-ttu-id="d631c-323">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-323">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-324">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-324">DOMString</span></span> | <span data-ttu-id="d631c-325">Ein Objekt, das ein Fenster darstellt, das ein DOM-Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="d631c-325">An object representing a window containing a DOM document.</span></span> | 

#### <span data-ttu-id="d631c-326">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-326">Return value</span></span>

`viewId`

|<span data-ttu-id="d631c-327">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-327">Type</span></span> | <span data-ttu-id="d631c-328">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-328">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-329">Zahl</span><span class="sxs-lookup"><span data-stu-id="d631c-329">Number</span></span> | <span data-ttu-id="d631c-330">Kann mit den verschiedenen APIs verwendet werden [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .</span><span class="sxs-lookup"><span data-stu-id="d631c-330">Can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

#### <span data-ttu-id="d631c-331">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-331">Remarks</span></span>
<span data-ttu-id="d631c-332">Verwenden Sie [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) und [`window`](https://developer.mozilla.org/docs/Web/API/Window) zum Erstellen neuer Fenster, und fügen Sie dann die API hinzu, um mit WinRT-APIs zu interagieren `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="d631c-332">Use [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) and [`window`](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span> <span data-ttu-id="d631c-333">Sie akzeptiert ein `window` Objekt als Parameter und gibt eine `viewId` Zahl zurück, die mit den verschiedenen APIs verwendet werden kann [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .</span><span class="sxs-lookup"><span data-stu-id="d631c-333">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

##### <span data-ttu-id="d631c-334">Verzögern der Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="d631c-334">Delaying Visibility</span></span> 
<span data-ttu-id="d631c-335">Ansichten in WinRT werden normalerweise ausgeblendet, und der endentwickler verwendet so etwas wie `TryShowAsStandaloneAsync` , um die Ansicht anzuzeigen, sobald Sie vollständig vorbereitet ist.</span><span class="sxs-lookup"><span data-stu-id="d631c-335">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span> <span data-ttu-id="d631c-336">In der Web-Welt wird `window.open` sofort ein Fenster angezeigt, und der Endbenutzer kann beobachten, wie Inhalte geladen und gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="d631c-336">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span> <span data-ttu-id="d631c-337">Damit Ihre neuen Windows-Ansichten in WinRT und nicht sofort angezeigt werden, haben wir eine Option hinzugefügt `window.open` .</span><span class="sxs-lookup"><span data-stu-id="d631c-337">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span> <span data-ttu-id="d631c-338">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d631c-338">For example:</span></span>
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### <span data-ttu-id="d631c-339">Unterschiede im primären Fenster</span><span class="sxs-lookup"><span data-stu-id="d631c-339">Primary Window Differences</span></span>
<span data-ttu-id="d631c-340">Das primäre Fenster, das zunächst vom Betriebssystem geöffnet wird, fungiert anders als das von ihm geöffnete sekundäre Fenster:</span><span class="sxs-lookup"><span data-stu-id="d631c-340">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span> 

|<span data-ttu-id="d631c-341">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-341">Description</span></span> | <span data-ttu-id="d631c-342">Primär</span><span class="sxs-lookup"><span data-stu-id="d631c-342">Primary</span></span> | <span data-ttu-id="d631c-343">Sekundärer</span><span class="sxs-lookup"><span data-stu-id="d631c-343">Secondary</span></span> |
|:---- |:--- |:--- |
|<span data-ttu-id="d631c-344">Window. Open</span><span class="sxs-lookup"><span data-stu-id="d631c-344">window.open</span></span> | <span data-ttu-id="d631c-345">Zugelassen</span><span class="sxs-lookup"><span data-stu-id="d631c-345">Allowed</span></span> | <span data-ttu-id="d631c-346">Disallowed</span><span class="sxs-lookup"><span data-stu-id="d631c-346">Disallowed</span></span> |
|<span data-ttu-id="d631c-347">Fenster. Schließen</span><span class="sxs-lookup"><span data-stu-id="d631c-347">window.close</span></span> | <span data-ttu-id="d631c-348">APP schließen</span><span class="sxs-lookup"><span data-stu-id="d631c-348">Close app</span></span> | <span data-ttu-id="d631c-349">Fenster schließen</span><span class="sxs-lookup"><span data-stu-id="d631c-349">Close window</span></span> |
| <span data-ttu-id="d631c-350">Navigations Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d631c-350">Navigation restrictions</span></span> | <span data-ttu-id="d631c-351">Nur ACUR</span><span class="sxs-lookup"><span data-stu-id="d631c-351">ACUR only</span></span> | <span data-ttu-id="d631c-352">Keine Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d631c-352">No restrictions</span></span> |

<span data-ttu-id="d631c-353">Die Einschränkung, dass sekundäre Fenster nicht geöffnet werden können, kann sich in Zukunft je nach [Feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer)ändern.</span><span class="sxs-lookup"><span data-stu-id="d631c-353">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>

##### <span data-ttu-id="d631c-354">Kommunikationseinschränkungen für denselben Ursprung</span><span class="sxs-lookup"><span data-stu-id="d631c-354">Same Origin Communication Restrictions</span></span> 
<span data-ttu-id="d631c-355">Es gibt ein schwieriges technisches Problem, das die korrekte Unterstützung für synchrone, identische Ursprungs-, Fenster-und Skriptaufrufe verhindert.</span><span class="sxs-lookup"><span data-stu-id="d631c-355">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span> <span data-ttu-id="d631c-356">Wenn Sie ein Fenster öffnen, das denselben Ursprung hat, kann das Skript in einem Fensterfunktionen direkt im anderen Fenster aufrufen, und einige dieser Aufrufe können nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d631c-356">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span> `postMessage` <span data-ttu-id="d631c-357">Anrufe funktionieren prima und sind die empfohlene Vorgehensweise, wenn es möglich ist.</span><span class="sxs-lookup"><span data-stu-id="d631c-357">calls work just fine and is the recommended way to do things if possible.</span></span> <span data-ttu-id="d631c-358">Arbeiten zur Verbesserung dieses Problems sind in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="d631c-358">Work to improve this issue is in progress.</span></span>


### <span data-ttu-id="d631c-359">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="d631c-359">isTaskScheduledAtPriorityOrHigher</span></span> 
<span data-ttu-id="d631c-360">Gibt einen booleschen Wert zurück, der angibt, ob die Arbeit auf der angegebenen Prioritätsstufe oder höher aussteht.</span><span class="sxs-lookup"><span data-stu-id="d631c-360">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### <span data-ttu-id="d631c-361">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-361">Parameters</span></span>
`priority` <span data-ttu-id="d631c-362">in</span><span class="sxs-lookup"><span data-stu-id="d631c-362">[in]</span></span>

|<span data-ttu-id="d631c-363">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-363">Type</span></span> | <span data-ttu-id="d631c-364">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-364">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-365">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-365">DOMString</span></span> | <span data-ttu-id="d631c-366">Ein Prioritätswert (siehe [MSApp-Konstanten](#msapp-constants)), der die Prioritätsstufe und höher angibt, um nach ausstehender in der Warteschlange befindlicher Arbeit zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="d631c-366">A priority value (see [MSApp Constants](#msapp-constants)) specifying the priority level and above to query for any outstanding queued work.</span></span>

#### <span data-ttu-id="d631c-367">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-367">Return value</span></span>
|<span data-ttu-id="d631c-368">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-368">Type</span></span> | <span data-ttu-id="d631c-369">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-369">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-370">Boolesch</span><span class="sxs-lookup"><span data-stu-id="d631c-370">Boolean</span></span> | <span data-ttu-id="d631c-371">Gibt zurück `true` , wenn Warteschlangen Arbeit auf der angegebenen Prioritätsstufe oder höher vorhanden ist, `false` andernfalls.</span><span class="sxs-lookup"><span data-stu-id="d631c-371">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>

#### <span data-ttu-id="d631c-372">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-372">Remarks</span></span>
<span data-ttu-id="d631c-373">Die `isTaskScheduledAtPriorityOrHigher` Methode bietet eine Möglichkeit für JavaScript-Code, um festzustellen, ob die Arbeit auf den verschiedenen Prioritätsebenen (oder höher) aussteht, mit der Absicht, dass sich der aufrufende JavaScript-Code dann entscheiden kann, die Arbeit mit höherer Priorität zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="d631c-373">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels (or above) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>

#### <span data-ttu-id="d631c-374">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d631c-374">Example</span></span>

```javascript
function performIdleWork(array_in) {
  var idx = 0;

  function performIdleWorkHelper() {
    for (; idx < array_in.length; ++idx) {

      // USEFUL CODE HERE 

      if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
        MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
        break;
      } // if
    } // for
  } // performIdleWorkHelper

  performIdleWorkHelper();
} // performIdleWork
```

### <span data-ttu-id="d631c-375">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="d631c-375">pageHandlesAllApplicationActivations</span></span>
<span data-ttu-id="d631c-376">Wird verwendet, um eine Aktualisierung des Start Pfads (Page Reload) vor jedem Activate-Ereignis (also klicken auf eine Benachrichtigung oder eine angeheftete Kachel) zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d631c-376">Used to avoid a refresh of the start path (page reload) before every activate event (ie. clicking a notification or a pinned tile).</span></span> 

#### <span data-ttu-id="d631c-377">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-377">Parameters</span></span>

|<span data-ttu-id="d631c-378">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-378">Type</span></span> | <span data-ttu-id="d631c-379">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-379">Description</span></span> |
|:---- |:--- |
<span data-ttu-id="d631c-380">Boolesch</span><span class="sxs-lookup"><span data-stu-id="d631c-380">Boolean</span></span> | <span data-ttu-id="d631c-381">Verwenden Sie `MSApp.pageHandlesAllApplicationActivations(true)` diese Option, um die Aktualisierung des startpfads (Seite neu laden) immer zu überspringen und stattdessen direkt zum Auslösen des Activated-Ereignisses zu springen `WebUIApplication` .</span><span class="sxs-lookup"><span data-stu-id="d631c-381">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span> <span data-ttu-id="d631c-382">Erfordert, dass alle Seiten Aktivierungsereignisse separat behandeln.</span><span class="sxs-lookup"><span data-stu-id="d631c-382">Requires that all pages handle activation events separately.</span></span> <span data-ttu-id="d631c-383">Wenn Sie diese Methode definieren `true` , wird durch Klicken auf ein Activated-Ereignis (wie ein Benachrichtigung gesendet) das erneute Laden nicht ausgelöst, was ein wesentlicher Faktor für einzelne Seiten-Apps ist, die das erneute Laden von Seiten vermeiden möchten.</span><span class="sxs-lookup"><span data-stu-id="d631c-383">By defining this method as `true`, clicking an activated event (like a notificaiton) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>

#### <span data-ttu-id="d631c-384">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d631c-384">Example</span></span> 

```javascript
// Without this, the app will first refresh to the start path before every activate event
window.MSApp.pageHandlesAllApplicationActivations(true); 

// This must not be deffered so that it can receive the initial `activated` event in time
window.Windows.UI.WebUI.WebUIApplication.addEventListener(
    `activated`,
    e =>
        microsoftInterface.handleActivatedEvent(e);
    }),
    false
);
```

### <span data-ttu-id="d631c-385">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="d631c-385">suppressSubdownloadCredentialPrompts</span></span> 
<span data-ttu-id="d631c-386">Steuert, ob eine APP während des Downloads von Ressourcen mögliche Authentifizierungs Aufforderungen unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="d631c-386">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### <span data-ttu-id="d631c-387">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-387">Parameters</span></span>
`suppress` <span data-ttu-id="d631c-388">in</span><span class="sxs-lookup"><span data-stu-id="d631c-388">[in]</span></span>

|<span data-ttu-id="d631c-389">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-389">Type</span></span> | <span data-ttu-id="d631c-390">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-390">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-391">Boolesch</span><span class="sxs-lookup"><span data-stu-id="d631c-391">Boolean</span></span> | <span data-ttu-id="d631c-392">Der Wert true unterdrückt potenzielle Authentifizierungs Aufforderungen.</span><span class="sxs-lookup"><span data-stu-id="d631c-392">A value of true suppresses potential authentication prompts.</span></span> <span data-ttu-id="d631c-393">Der Wert false unterdrückt keine potenziellen Authentifizierungs Aufforderungen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d631c-393">A value of false does not suppress any potential authentication prompts from the user.</span></span>

#### <span data-ttu-id="d631c-394">Returan-Wert</span><span class="sxs-lookup"><span data-stu-id="d631c-394">Returan value</span></span>
<span data-ttu-id="d631c-395">Keine</span><span class="sxs-lookup"><span data-stu-id="d631c-395">None.</span></span>

#### <span data-ttu-id="d631c-396">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-396">Remarks</span></span>
<span data-ttu-id="d631c-397">Die `suppressSubdownloadCredentialPrompts` Methode steuert, ob eine APP potenzielle Authentifizierungs Aufforderungen während des Downloads von Ressourcen unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="d631c-397">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span> <span data-ttu-id="d631c-398">Das Standardverhalten besteht darin, Anmeldeinformationen nicht zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="d631c-398">The default behavior is to not suppress credential prompts.</span></span>

`suppressSubdownloadCredentialPrompts` <span data-ttu-id="d631c-399">ist für die Verwendung durch Apps vorgesehen, die eine übermäßige Anzahl von Ressourcen laden können, die eine Authentifizierung erfordern, beispielsweise eine Mail-app (die einen Newsletter mit einer Reihe von Bildern enthalten kann, bei denen für jedes Bild eine Authentifizierung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="d631c-399">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app (which could contain a newsletter containing a number of images where each image requires authentication).</span></span>

<span data-ttu-id="d631c-400">Wenn Sie Anmeldeinformationen unterdrücken, werden Dialogfelder für die Authentifizierung bei Servern beim Zugriff auf Ressourcen, die eine Authentifizierung erfordern, nicht angezeigt, und die Ressource wird nicht heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="d631c-400">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span> <span data-ttu-id="d631c-401">Beachten Sie, dass dies `suppressSubdownloadCredentialPrompts` keine Auswirkungen auf andere mögliche Eingabeaufforderungen wie Proxyauthentifizierung oder Client Zertifizierungs Anforderungs Dialogfelder hat und sich auch nicht auf XMLHttpRequest auswirkt.</span><span class="sxs-lookup"><span data-stu-id="d631c-401">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>

<span data-ttu-id="d631c-402">Beachten Sie, dass `suppressSubdownloadCredentialPrompts` alle Inhalte in der Anwendung, einschließlich der Inhalte, die im Element gehostet werden, beeinträchtigt werden `webview` .</span><span class="sxs-lookup"><span data-stu-id="d631c-402">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>
 
<span data-ttu-id="d631c-403">**Wichtig:**  Entscheidungen für Anmeldeinformationen werden zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="d631c-403">**Important:**  Credential prompt decisions are cached.</span></span> <span data-ttu-id="d631c-404">Daher wird die Unterdrückung von Anmeldeinformationen für Anmeldeinformationen sofort wirksam, sodass die Eingabeaufforderung für Anmeldeinformationen nach dem unterdrücken möglicherweise ein erneutes Laden des Dokuments benötigt, damit es wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="d631c-404">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>

#### <span data-ttu-id="d631c-405">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d631c-405">Example</span></span>

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### <span data-ttu-id="d631c-406">terminateApp</span><span class="sxs-lookup"><span data-stu-id="d631c-406">terminateApp</span></span>
<span data-ttu-id="d631c-407">Beendet die aktuelle Anwendung und generiert einen Fehlerbericht.</span><span class="sxs-lookup"><span data-stu-id="d631c-407">Terminates the current application and generates a failure report.</span></span> 

```javascript
MSApp.terminateApp(error); 
```

#### <span data-ttu-id="d631c-408">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-408">Parameters</span></span>
`error` <span data-ttu-id="d631c-409">in</span><span class="sxs-lookup"><span data-stu-id="d631c-409">[in]</span></span>

<span data-ttu-id="d631c-410">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-410">Type</span></span> | <span data-ttu-id="d631c-411">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-411">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-412">Fehler</span><span class="sxs-lookup"><span data-stu-id="d631c-412">Error</span></span> | <span data-ttu-id="d631c-413">Ein `Error` Objekt, das Sie verwenden können, um den Fehler zu beschreiben, der die Kündigung ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="d631c-413">An `Error` object that you can use to describe the error that triggered the termination.</span></span> <span data-ttu-id="d631c-414">Das `Error` Objekt muss die Eigenschaften Number, Description und Stack enthalten; es wird kein Fehlerbericht generiert, wenn das Objekt diese Eigenschaften nicht enthält.</span><span class="sxs-lookup"><span data-stu-id="d631c-414">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>

#### <span data-ttu-id="d631c-415">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-415">Return value</span></span>
<span data-ttu-id="d631c-416">Keine</span><span class="sxs-lookup"><span data-stu-id="d631c-416">None.</span></span>

#### <span data-ttu-id="d631c-417">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d631c-417">Remarks</span></span>
<span data-ttu-id="d631c-418">Wenn das gemeldete Problem zu `terminateApp` einem der 5 häufigsten Probleme Ihrer APP wird, wird es auf der Qualitätsseite der App angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d631c-418">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>

#### <span data-ttu-id="d631c-419">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d631c-419">Example</span></span>
<span data-ttu-id="d631c-420">In diesem Beispiel `terminateApp` wird aufgerufen, wenn eine Ausnahme auftritt.</span><span class="sxs-lookup"><span data-stu-id="d631c-420">This example calls `terminateApp` when an exception is encountered.</span></span> <span data-ttu-id="d631c-421">Sie verwendet das `Error` Objekt, das beim Abfangen einer Ausnahme bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d631c-421">It uses the `Error` object provided when you catch an exception.</span></span> 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### <span data-ttu-id="d631c-422">MSApp-Konstanten</span><span class="sxs-lookup"><span data-stu-id="d631c-422">MSApp Constants</span></span>
<span data-ttu-id="d631c-423">Zulässige Prioritätswerte, die mit `execAsyncAtPriority` , `execAtPriority` , und verknüpft sind `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="d631c-423">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>

#### <span data-ttu-id="d631c-424">Aktuell</span><span class="sxs-lookup"><span data-stu-id="d631c-424">Current</span></span>
`current`

|<span data-ttu-id="d631c-425">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-425">Type</span></span> | <span data-ttu-id="d631c-426">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-426">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-427">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-427">DOMString</span></span> | <span data-ttu-id="d631c-428">Wenn die `current` Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs die aktuelle kontextbezogene Priorität.</span><span class="sxs-lookup"><span data-stu-id="d631c-428">When `current` is used with the appropriate method (See also section), the method will use the current contextual priority when executing the requested operation.</span></span>

#### <span data-ttu-id="d631c-429">Hoch </span><span class="sxs-lookup"><span data-stu-id="d631c-429">High</span></span>
`high`

|<span data-ttu-id="d631c-430">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-430">Type</span></span> | <span data-ttu-id="d631c-431">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-431">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-432">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-432">DOMString</span></span> | <span data-ttu-id="d631c-433">Wenn die `high` Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs eine höhere Priorität als normal, und die Operation wird vor jeder vorhandenen normalen Priorität ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d631c-433">When `high` is used with the appropriate method (See also section), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>

#### <span data-ttu-id="d631c-434">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="d631c-434">Idle</span></span>
`idle`

|<span data-ttu-id="d631c-435">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-435">Type</span></span> | <span data-ttu-id="d631c-436">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-436">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-437">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-437">DOMString</span></span> | <span data-ttu-id="d631c-438">Wenn `ideal` mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs eine niedrigere Priorität als normal, und die Operation wird nach jeder vorhandenen normalen Priorität ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d631c-438">When `ideal` is used with the appropriate method (See also section), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>

#### <span data-ttu-id="d631c-439">Normal</span><span class="sxs-lookup"><span data-stu-id="d631c-439">Normal</span></span>
`normal`

|<span data-ttu-id="d631c-440">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-440">Type</span></span> | <span data-ttu-id="d631c-441">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-441">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-442">Dom</span><span class="sxs-lookup"><span data-stu-id="d631c-442">DOMString</span></span> | <span data-ttu-id="d631c-443">Wenn die `normal` Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs die normale vorhandene Priorität.</span><span class="sxs-lookup"><span data-stu-id="d631c-443">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>

#### <span data-ttu-id="d631c-444">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d631c-444">Example</span></span>

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### <span data-ttu-id="d631c-445">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d631c-445">Requirements</span></span>
|<span data-ttu-id="d631c-446">IDL</span><span class="sxs-lookup"><span data-stu-id="d631c-446">IDL</span></span> | <span data-ttu-id="d631c-447">MSHTML. idl</span><span class="sxs-lookup"><span data-stu-id="d631c-447">Mshtml.idl</span></span> |
|:---- |:--- |

## <span data-ttu-id="d631c-448">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="d631c-448">MSAppAsyncOperation</span></span>

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### <span data-ttu-id="d631c-449">start</span><span class="sxs-lookup"><span data-stu-id="d631c-449">start</span></span>
<span data-ttu-id="d631c-450">Startet das `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="d631c-450">Starts the `MSAppAsyncOperation`.</span></span>

```javascript
var retval = MSAppAsyncOperation.start();
```

#### <span data-ttu-id="d631c-451">Parameter</span><span class="sxs-lookup"><span data-stu-id="d631c-451">Parameters</span></span>
<span data-ttu-id="d631c-452">Keine</span><span class="sxs-lookup"><span data-stu-id="d631c-452">None.</span></span>

#### <span data-ttu-id="d631c-453">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d631c-453">Return value</span></span>
<span data-ttu-id="d631c-454">Keine</span><span class="sxs-lookup"><span data-stu-id="d631c-454">None.</span></span>

#### <span data-ttu-id="d631c-455">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d631c-455">Properties</span></span>
`error` <span data-ttu-id="d631c-456">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d631c-456">property</span></span>

|<span data-ttu-id="d631c-457">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-457">Type</span></span> | <span data-ttu-id="d631c-458">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-458">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-459">DOMError</span><span class="sxs-lookup"><span data-stu-id="d631c-459">DOMError</span></span> | <span data-ttu-id="d631c-460">Stellt einen Fehler in dar `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="d631c-460">Represents an error in `MSAppAsyncOperation`.</span></span>

```javascript
p = object.error
```

`oncomplete` <span data-ttu-id="d631c-461">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d631c-461">property</span></span>

|<span data-ttu-id="d631c-462">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-462">Type</span></span> | <span data-ttu-id="d631c-463">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-463">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-464">EventHandler</span><span class="sxs-lookup"><span data-stu-id="d631c-464">EventHandler</span></span> | <span data-ttu-id="d631c-465">Eigenschaft zum Festlegen eines Ereignishandlers nach Abschluss von `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="d631c-465">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.oncomplete
```

`onerror` <span data-ttu-id="d631c-466">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d631c-466">property</span></span>

|<span data-ttu-id="d631c-467">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-467">Type</span></span> | <span data-ttu-id="d631c-468">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-468">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-469">EventHandler</span><span class="sxs-lookup"><span data-stu-id="d631c-469">EventHandler</span></span> | <span data-ttu-id="d631c-470">Eigenschaft zum Festlegen eines Ereignishandlers bei einem Fehler `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="d631c-470">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>

```javascript
p = object.onerror
```

`readyState` <span data-ttu-id="d631c-471">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d631c-471">property</span></span>

|<span data-ttu-id="d631c-472">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-472">Type</span></span> | <span data-ttu-id="d631c-473">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-473">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-474">Zahl</span><span class="sxs-lookup"><span data-stu-id="d631c-474">Number</span></span> | <span data-ttu-id="d631c-475">Stellt den Zustand des asynchronen Vorgangs in der Windows-App mit JavaScript dar.</span><span class="sxs-lookup"><span data-stu-id="d631c-475">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span> <span data-ttu-id="d631c-476">Zu den Werten zählen: gestartet [0], abgeschlossen [1], Fehler [2].</span><span class="sxs-lookup"><span data-stu-id="d631c-476">Values include: Started[0], Completed[1], Error[2].</span></span>

```javascript
p = object.readyState
```

`result` <span data-ttu-id="d631c-477">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d631c-477">property</span></span>

|<span data-ttu-id="d631c-478">Typ</span><span class="sxs-lookup"><span data-stu-id="d631c-478">Type</span></span> | <span data-ttu-id="d631c-479">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d631c-479">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="d631c-480">Any</span><span class="sxs-lookup"><span data-stu-id="d631c-480">Any</span></span> |<span data-ttu-id="d631c-481">Stellt das Ergebnis von dar `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="d631c-481">Represents the result of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.result
```
