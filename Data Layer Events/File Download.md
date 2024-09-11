# File Download

CRP Notes: Not part of CRP.

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "file_download",
  "detailed_event": "File Download",
    "event_data": {
        "file_extension": "<file_extension>",
        "file_name": "<file_name>",
        "file_target_url": "<file_target_url>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.file_extension|string|Captures the type of file that was downloaded \(i.e. PDF, EPUB, DMG\).|pdf, doc, csv, dmp, zip|||||||
|event_data.file_name|string|Captures the file name associated with file downloads.|Year End 2012.pdf, Operating Instructions.doc`|||||||
|event_data.file_target_url|string|Captures the download file url.|https:\/\/www.example.com\/docs\/file.pdf|||||||

## Attached Notes

<p><span style="font-weight: 400;"><strong>Platform: harvardonline, PLL</strong></span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">Trigger this event when a user clicks to download a file.</span></p>
<p><span style="font-weight: 400;">Example page:</span></p>
<p><a href="https://www.harvardonline.harvard.edu/course/data-science-principles"><span style="font-weight: 400;">https://www.harvardonline.harvard.edu/course/data-science-principles</span></a><span style="font-weight: 400;">&nbsp; -&gt; </span><span style="font-weight: 400;">[Course Calendar]</span></p>
