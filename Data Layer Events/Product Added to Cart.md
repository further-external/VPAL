# Product Added to Cart

CRP Relevance - the code below has been updated for the CRP flow.

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
                "item_name": "<item_name>",
                "item_id": "<item_id>",
                "item_brand": "<item_brand>",
                "item_category": "<item_category>",
                "price": <price>,
                "quantity": <quantity>,
                "course_name": "<course_name>",
                "program_dates": "<program_dates>",
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
|ecommerce.items[n].course_name|string|Value for Course Name. ex 'Financial Analysis and Valuation for Lawyers'|Financial Analysis and Valuation for Lawyers, Data Privacy and Technology|||||||
|ecommerce.items[n].course_platform|string|Value for Course Platform. ex. edX'|harvard online|||||||
|ecommerce.items[n].course_price|string|Value for Course Price. ex. '1600'|1600, 945, 125.00|||||||
|ecommerce.items[n].item_brand|string|Item brand|Harvard Online|||||||
|ecommerce.items[n].item_category|string|Item Category \(context-specific\). item\_category2 through item\_category5 can also be used if the item has many categories.|pants|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(SKU or UPC\)|SKU\_12345|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|Same value as Course Name|||||||
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


## Tag Updates (Further)
Update add_to_cart event tag to pass course name and program dates at the event scope - these can be mapped for the page-level variables
