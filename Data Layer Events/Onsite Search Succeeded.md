# Onsite Search Succeeded

CRP Notes: Not part of CRP.

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "view_search_results",
  "detailed_event": "Onsite Search Succeeded",
    "event_data": {
        "number_of_items": "<number_of_items>",
        "search_term": "<search_term>",
        "type": "<type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.number_of_items|string|A count of the number of items returned in a search results list.|39, 12, 0,|||||||
|event_data.search_term|string|Captures the search text used in on-site searches.|bluth, blue, red lobster|||||||
|event_data.type|string|Captures the type of on-site search performed \(i.e., content, product, location, product location, scheduled event, room, report\)|products, properties, articles, authors, coupons, publications|||||||

## Attached Notes

<p><span style="font-weight: 400;"><strong>Platform: harvardonline, PLL</strong></span></p>
<p><span style="font-weight: 400;">This event triggers when someone successfully completes an internal search on the website even if '0' results are returned.</span></p>
<p><span style="font-weight: 400;">Example URL:</span></p>
<p><a href="https://www.harvardonline.harvard.edu/course?search_api_fulltext=harvard"><span style="font-weight: 400;">https://www.harvardonline.harvard.edu/course?search_api_fulltext=harvard</span></a><span style="font-weight: 400;">&nbsp;</span></p>
