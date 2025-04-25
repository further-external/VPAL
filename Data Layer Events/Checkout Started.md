# Checkout Started

This event should fire when the user successfully clicks on the 'proceed to checkout' button - the values in the ecommerce dataLayer should be the same values passed with the add_to_cart event that fires on the page



![image](https://github.com/user-attachments/assets/6b1655bf-b55a-497a-8cc6-db738ea29456)

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "begin_checkout",
    "ecommerce": {
        "coupon": "<coupon>", // REQUIRED | string - delimited (~) | ex. couponName1~couponName2~couponName3
        "currency": "<currency>",
        "items": [
            {
                "item_name": "<item_name>",
                "item_id": "<item_id>",
                "item_brand": "<item_brand>",
                "item_category": "<item_category>",
                "price": <price>,
                "discount": <discount>,
                "quantity": <quantity>,
                "course_name": "<course_name>",
                "program_dates": "<program_dates>",

            }
        ],
        "value": <value>,
        "tax": <tax>
    },
    "user_data": {
        "user_id": "<user_id>",
        "user_type": "<user_type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.coupon|string|Order-level coupon code used for a purchase.|summer\_fun, couponName1~couponName2~couponName3|||||||
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.||||||||
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.||||||||
|ecommerce.items[n].course_name|string|Value for Course Name. ex 'Financial Analysis and Valuation for Lawyers'|Financial Analysis and Valuation for Lawyers, Data Privacy and Technology|||||||
|ecommerce.items[n].course_price|string|Value for Course Price. ex. '1600'|1600, 945, 125.00|||||||
|ecommerce.items[n].item_brand|string|Item brand|Harvard Online|||||||
|ecommerce.items[n].item_category|string|Item Category \(context-specific\)|Include course categories similar to grouping on Harvard Online, if available|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(SKU or UPC\)|Clotho_id for course|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|Same value as Course Name|||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].discount|number|The monetary value of discount in units of the specified currency parameter.|2.00|||||||
|ecommerce.items[n].program_dates|string|Value for Program Dates. ex. May 11, 2022 – May 10, 2023|May 11, 2022 – May 10, 2023|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.value|number|The monetary value of the event which will be equal to course price.|7.77, 239.55, 659|||||||
|ecommerce.tax|number|Tax cost associated with a transaction.|1.11|||||||
|user_data.user_id|string|The ID of the currently logged-in user, provided the site supports authentication and the user is authenticated. For CRP, this should be the hashedEmail value when available; if not, use an empty string (""). If the user is not authenticated but the email field is populated, use the captured hashedEmail value. However, if the user is authenticated, use the hashedEmail associated with their logged-in account.|ba7816bf8f01cfea414140de5dae2223b00361a396177a9cb410ff61f20015ad|||||||
|user_data.user_type|string|The users current login status, LX Key = Temporary name of users who registered directly on the CRP platform authenticated user HarvardKey = Harvard alumni/staff authenticated user, Harvard Guest Account = Authenticated User, logged in, Unauthenticated User = Not logged in | LX Key(Temporary name of users who registered directly on the CRP platform) HarvardKey, Harvard Guest Account, Unauthenticated User|||||||





## Tag Updates Needed

N/A



