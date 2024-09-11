# Article Load

CRP status: N/A for CRP flow


### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "article_load",
  "detailed_event": "Article Load",
    "event_data": {
        "article_length": <article_length>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.article_length|number|Value for for Article Length. \(character\/word count\)|4321, 265, ...|||||||

## Attached Notes

<p><strong>Platform: harvardonline</strong></p>
<p>Trigger this event with each article/blog page load. This event should trigger before Page Load Completed.</p>
<p>Example Page:<br /><a href="https://www.harvardonline.harvard.edu/blog/business-health-care-united-states" target="_blank" rel="noopener noreferrer">https://www.harvardonline.harvard.edu/blog/business-health-care-united-states</a></p>
