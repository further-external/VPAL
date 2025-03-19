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
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated. For CRP this will be the hashedEmail value when avaliable, if not avaliable pass an empty string value ("")|ba7816bf8f01cfea414140de5dae2223b00361a396177a9cb410ff61f20015ad|||||||
|user_data.user_type|string|The users current login status, HarvardKey People = Har alumni/staff, Harvard Guest Account = Authenticated User, logged in, Unauthenticated User = Not logged in | HarvardKey, Harvard Guest Account, Unauthenticated User|||||||

## Attached Notes

<p><strong>Platform: CRP</strong></p>
<p>Trigger this event when a user successfully signs into their account. This occurs after they select one of the three sign-in options: the native sign-in from the modal on the CRP, or one of the two authorized methods (HBSO or HarvardKey).</p>
<p>Include a coupon_applied custom metric and setup in the tag setup.</p>

