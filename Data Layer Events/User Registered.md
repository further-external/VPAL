# User Registered

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "sign_up",
  "detailed_event": "User Registered",
    "event_data": {
        "method": "<method>"
    },
    "user_data": {
        "user_id": "<user_id>",
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.method|string|Records the system the user utilized to sign up.|HBSO, HarvardKey, Native|||||||
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||

## Attached Notes

<p><strong>Platform: CRP</strong></p>
<p>Trigger this event after a user creates an account using the sign-up option in the modal when they click "Sign in to Harvard Online."</p>
