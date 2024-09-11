# Internal Campaigns Displayed

CRP Notes: Not part of CRP.

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "view_promotion",
  "detailed_event": "Internal Campaigns Displayed",
    "ecommerce": {
        "items": [
            {
                "course_certificate_price": "<course_certificate_price>",
                "course_difficulty": "<course_difficulty>",
                "course_language": "<course_language>",
                "course_length": "<course_length>",
                "course_modality": "<course_modality>",
                "course_name": "<course_name>",
                "course_pace": "<course_pace>",
                "course_platform": "<course_platform>",
                "course_price": "<course_price>",
                "course_school": "<course_school>",
                "course_transcript_language": "<course_transcript_language>",
                "item_brand": "<item_brand>",
                "item_category": "<item_category>",
                "item_category2": "<item_category2>",
                "item_id": "<item_id>",
                "item_name": "<item_name>",
                "location_id": "<location_id>",
                "program_dates": "<program_dates>",
                "quantity": <quantity>
            }
        ],
        "promotion_id": "<promotion_id>",
        "promotion_name": "<promotion_name>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.items[n].course_certificate_price|string|Value for Certificate Price - ex. 1600|1600, 950, 0, 25.00|||||||
|ecommerce.items[n].course_difficulty|string|Value for Course Difficulty E-commerce. ex 'Introductory'|introductory, intermediate|||||||
|ecommerce.items[n].course_language|string|Value for Course Language. ex 'English'|english|||||||
|ecommerce.items[n].course_length|string|Value for Course Length. ex. '8 weeks \| 2-4 hours a week'|8 weeks \| 2-4 hours a week, 4 weeks 1-2 hours a week, 5 weeks long|||||||
|ecommerce.items[n].course_modality|string|Value for Course Modality - ex. 'Online'|on\_campus, online, online\_hybrid, flex, ...|||||||
|ecommerce.items[n].course_name|string|Value for Course Name. ex 'Financial Analysis and Valuation for Lawyers'|Financial Analysis and Valuation for Lawyers, Data Privacy and Technology|||||||
|ecommerce.items[n].course_pace|string|Value for Course Pace. ex. 'Self-Paced'|self-paced, instructor|||||||
|ecommerce.items[n].course_platform|string|Value for Course Platform. ex. edX'|hbs, edx, ...|||||||
|ecommerce.items[n].course_price|string|Value for Course Price. ex. '1600'|1600, 945, 125.00|||||||
|ecommerce.items[n].course_school|string|Value for Course School. ex. 'HKUSTx, Harvard School of Engineering and Applied Sciences'|HKUSTx, HarvardX, CaltechX, Harvard School of Engineering and Applied Sciences|||||||
|ecommerce.items[n].course_transcript_language|string|Value for Course Transcript Language. ex. 'English'|english|||||||
|ecommerce.items[n].item_brand|string|Item brand|Gucci|||||||
|ecommerce.items[n].item_category|string|Item Category \(context-specific\). item\_category2 through item\_category5 can also be used if the item has many categories.|pants|||||||
|ecommerce.items[n].item_category2|string|The second category of an item.||||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(SKU or UPC\)|SKU\_12345|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|jeggings|||||||
|ecommerce.items[n].location_id|string|Captures a unique ID of a physical location such as a store, banking branch, atm, hotel, office, or other.|155, 65588, 987764448|||||||
|ecommerce.items[n].program_dates|string|Value for Program Dates. ex. May 11, 2022 – May 10, 2023|May 11, 2022 – May 10, 2023|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.promotion_id|string|Captures the ID associated with internal campaigns. Used for internal campaign impressions and clicks only.|2345, 56789, 9876|||||||
|ecommerce.promotion_name|string|Captures the name associated with internal campaigns. Used for internal campaign impressions and clicks only.|Trek bikes for kids, REI Spring Sale 2019, Viking Cruise Fall Specials|||||||

## Attached Notes

<p><strong>Platform: harvardonline, PLL (if serving a promotion)</strong></p>
<p>Capture this when a promotion is loaded on a page. If the promotion is promoting a course or courses pass the items array as well.</p>
<p>&nbsp;</p>
