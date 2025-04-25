# Order Placed

CRP flow: Fire this on the order confirmation page when the user returns from the payment platform.

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "purchase",
  "detailed_event": "Order Placed",
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
        "payment_method": "<payment_method>",
        "tax": <tax>,
        "transaction_id": "<transaction_id>",
        "value": <value>
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
|ecommerce.items[n].course_name|string|Value for Course Name. ex 'Financial Analysis and Valuation for Lawyers'|Financial Analysis and Valuation for Lawyers, Data Privacy and Technology|||||||
|ecommerce.items[n].course_price|string|Value for Course Price. ex. '1600'|1600, 945, 125.00|||||||
|ecommerce.items[n].item_brand|string|Item brand|Harvard Online|||||||
|ecommerce.items[n].item_category|string|Item Category \(context-specific\)|Include course categories similar to grouping on Harvard Online, if available|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(SKU or UPC\)|Clotho_id for course|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|Same value as Course Name|||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter. This is with discounte applied|9.99|||||||
|ecommerce.items[n].discount|number|The monetary value of discount in units of the specified currency parameter.|2.00|||||||
|ecommerce.items[n].program_dates|string|Value for Program Dates. ex. May 11, 2022 – May 10, 2023|May 11, 2022 – May 10, 2023|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.payment_method|string|Captures the payment methods used for a transaction \(i.e. credit card, Visa, MasterCard, Amex, Paypal, purchase order, etc\).|Credit Card, PayPal, Mastercard, Visa, Amex, Discover|||||||
|ecommerce.tax|number|Tax cost associated with a transaction.|1.11|||||||
|ecommerce.transaction_id|string|The unique identifier of a transaction.|T\_12345, 19283j2nm9jdjs|^[a-zA-Z0-9]{6,20}$|6|20||||
|ecommerce.value|number|The monetary value of the event. quantity x sale price|7.77, 239.55, 659|||||||
|user_data.user_id|string|The ID of the currently logged-in user, provided the site supports authentication and the user is authenticated. For CRP, this should be the hashedEmail value when available; if not, use an empty string (""). If the user is not authenticated but the email field is populated, use the captured hashedEmail value. However, if the user is authenticated, use the hashedEmail associated with their logged-in account.|ba7816bf8f01cfea414140de5dae2223b00361a396177a9cb410ff61f20015ad|||||||
|user_data.user_type|string|The users current login status, LX Key = Temporary name of users who registered directly on the CRP platform authenticated user HarvardKey = Harvard alumni/staff authenticated user, Harvard Guest Account = Authenticated User, logged in, Unauthenticated User = Not logged in | LX Key(Temporary name of users who registered directly on the CRP platform) HarvardKey, Harvard Guest Account, Unauthenticated User|||||||

