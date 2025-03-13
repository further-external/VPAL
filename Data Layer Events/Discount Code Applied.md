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
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.coupon|string|Records the system the user utilized to log in.|HBSO, HarvardKey, Native|||||||

## Attached Notes

<p><strong>Platform: CRP</strong></p>
<p>Trigger this event when a user successfully signs into their account. This occurs after they select one of the three sign-in options: the native sign-in from the modal on the CRP, or one of the two authorized methods (HBSO or HarvardKey).</p>
<p>Include a coupon_applied custom metric and setup in the tag setup.</p>

