# Product Added to Cart

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "add_to_cart",
  "detailed_event": "Product Added to Cart",
    "ecommerce": {
        "currency": "<currency>",
        "items": [
            {
                "applications_close": "<applications_close>",
                "cohort": "<cohort>",
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
                "currency": "<currency>",
                "item_brand": "<item_brand>",
                "item_category": "<item_category>",
                "item_category2": "<item_category2>",
                "item_id": "<item_id>",
                "item_list_id": "<item_list_id>",
                "item_list_name": "<item_list_name>",
                "item_name": "<item_name>",
                "price": <price>,
                "program_dates": "<program_dates>",
                "quantity": <quantity>
            }
        ],
        "value": <value>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.||||||||
|ecommerce.items[n].applications_close|string|Date on which course Applications Close|Jul 10, 2023|||||||
|ecommerce.items[n].cohort|string|Cohort \(or wave\) a user selects for a course.|July 19, 2023|||||||
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
|ecommerce.items[n].currency|string|The currency, in 3-letter ISO 4217 format.|USD|||||||
|ecommerce.items[n].item_brand|string|Item brand|Gucci|||||||
|ecommerce.items[n].item_category|string|Item Category \(context-specific\). item\_category2 through item\_category5 can also be used if the item has many categories.|pants|||||||
|ecommerce.items[n].item_category2|string|The second category of an item.||||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(SKU or UPC\)|SKU\_12345|||||||
|ecommerce.items[n].item_list_id|string|The computer-readable machine name of the list the item showed up in \(if sent with a view\_item\_list event\). Use UUID provided by the component if no more specific ID is available.|12345abcde12345|||||||
|ecommerce.items[n].item_list_name|string|The human-readable name of the item list the item showed up in \(if sent with a view\_item\_list event\). If one is not available, populate with numerical index of which list this is on the page \(1-indexed\). For filter\_by\_group component, use that value.|filter\_by\_group, recommended\_products, recently\_viewed\_products|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|jeggings|||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].program_dates|string|Value for Program Dates. ex. May 11, 2022 – May 10, 2023|May 11, 2022 – May 10, 2023|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||

## Attached Notes

<p><strong>Plaform: myhbx.org</strong></p>
<p>This event should fire when a user successfully submits a course application.</p>
<p>&nbsp;</p>
<table>
<tbody>
<tr>
<td>
<p><strong>Ecom Parameter</strong></p>
</td>
<td>
<p><strong>Definition for VPAL</strong></p>
</td>
</tr>
<tr>
<td>
<p><span style="font-weight: 400;">item_list_id</span></p>
</td>
<td>
<p><strong>ID for course list (if not available, pass name),</strong><span style="font-weight: 400;"> after click must be stored for other events</span></p>
</td>
</tr>
<tr>
<td>
<p><span style="font-weight: 400;">item_list_name</span></p>
</td>
<td>
<p><strong>Name of course list </strong><span style="font-weight: 400;">(after click must be stored for other events)</span></p>
</td>
</tr>
<tr>
<td>
<p><span style="font-weight: 400;">item_brand</span></p>
</td>
<td>
<p><strong>School </strong><span style="font-weight: 400;">(ex HKUSTx, HarvardX, CaltechX, Harvard School of Engineering and Applied Sciences)</span></p>
</td>
</tr>
<tr>
<td>
<p><span style="font-weight: 400;">item_category</span></p>
</td>
<td>
<p><strong>Highest categorization for courses - Series?</strong></p>
</td>
</tr>
<tr>
<td>
<p><span style="font-weight: 400;">item_category2</span></p>
</td>
<td>
<p><strong>Capture if course offered through edX vs. VPAL platform&nbsp;</strong></p>
</td>
</tr>
<tr>
<td>
<p><span style="font-weight: 400;">item_id</span></p>
</td>
<td>
<p><strong>Course Code</strong></p>
</td>
</tr>
<tr>
<td>
<p><span style="font-weight: 400;">item_name</span></p>
</td>
<td>
<p><strong>Course Title</strong></p>
</td>
</tr>
</tbody>
</table>
