# Discount Code Applied

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "Discount Code Applied",
    "event_data": {
        "coupon": "<coupon>"
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
|event_data.coupon|string|Records the system the user utilized to log in.|summer\_fun, couponName1~couponName2~couponName3|||||||
|user_data.user_id|string|The ID of the currently logged-in user, provided the site supports authentication and the user is authenticated. For CRP, this should be the hashedEmail value when available; if not, use an empty string (""). If the user is not authenticated but the email field is populated, use the captured hashedEmail value. However, if the user is authenticated, use the hashedEmail associated with their logged-in account.|ba7816bf8f01cfea414140de5dae2223b00361a396177a9cb410ff61f20015ad|||||||
|user_data.user_type|string|The users current login status, LX Key = Temporary name of users who registered directly on the CRP platform authenticated user HarvardKey = Harvard alumni/staff authenticated user, Harvard Guest Account = Authenticated User, logged in, Unauthenticated User = Not logged in | LX Key(Temporary name of users who registered directly on the CRP platform) HarvardKey, Harvard Guest Account, Unauthenticated User|||||||

## Attached Notes

<p><strong>Platform: CRP</strong></p>
<p>Trigger this event when a user successfully signs into their account. This occurs after they select one of the three sign-in options: the native sign-in from the modal on the CRP, or one of the two authorized methods (HBSO or HarvardKey).</p>
<p>Include a coupon_applied custom metric and setup in the tag setup.</p>

