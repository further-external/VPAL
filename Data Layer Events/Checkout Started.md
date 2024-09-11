# Checkout Started

This event has been updated for the CRP - (pending testing, we could just go with the HTML attribute)


### 

## HTML Attribute

Add the following data attribute to the checkout link that takes the user to the offsite payment platform.

data-gtm-event="nav_click"


## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "begin_checkout",
  "detailed_event": "Checkout Started",
    "ecommerce": {
        "coupon": "<coupon>",
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
|ecommerce.coupon|string|Order-level coupon code used for a purchase.|summer\_fun|||||||
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.||||||||
|ecommerce.items[n].course_name|string|Value for Course Name. ex 'Financial Analysis and Valuation for Lawyers'|Financial Analysis and Valuation for Lawyers, Data Privacy and Technology|||||||
|ecommerce.items[n].course_price|string|Value for Course Price. ex. '1600'|1600, 945, 125.00|||||||
|ecommerce.items[n].item_brand|string|Item brand|Harvard Online|||||||
|ecommerce.items[n].item_category|string|Item Category \(context-specific\)|Include course categories similar to grouping on Harvard Online, if available|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(SKU or UPC\)|Clotho_id for course|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|Same value as Course Name|||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].program_dates|string|Value for Program Dates. ex. May 11, 2022 – May 10, 2023|May 11, 2022 – May 10, 2023|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.value|number|The monetary value of the event which will be equal to course price.|7.77, 239.55, 659|||||||


## Tag Updates Needed

We will need to update MHX custom event to also capture course name and program dates at the event level for the existing MHX courses.



