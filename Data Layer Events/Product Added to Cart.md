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
                "course_platform": "<Harvard Online>",

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
|ecommerce.items[n].course_platform|string|Value for Course Platform. ex. edX'|Harvard oOline|||||||
|ecommerce.items[n].course_price|string|Value for Course Price. ex. '1600'|1600, 945, 125.00|||||||
|ecommerce.items[n].item_brand|string|Item brand|Harvard Online|||||||
|ecommerce.items[n].item_category|string|Item Category \(context-specific\)|Include course categories similar to grouping on Harvard Online, if available|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(SKU or UPC\)|Clotho_id for course|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|Same value as Course Name|||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].program_dates|string|Value for Program Dates. ex. May 11, 2022 – May 10, 2023|May 11, 2022 – May 10, 2023|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||



## Tag Updates (Further)
Update add_to_cart event tag to pass course name and program dates at the event scope - these can be mapped for the page-level variables
