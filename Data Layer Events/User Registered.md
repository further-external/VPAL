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
        "user_type": "<user_type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.method|string|Records the system the user utilized to sign up.|HBSO, HarvardKey, Native|||||||
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated. For CRP this will be the hashedEmail value when avaliable, if not avaliable pass an empty string value ("")|ba7816bf8f01cfea414140de5dae2223b00361a396177a9cb410ff61f20015ad|||||||
|user_data.user_type|string|The users current login status, HarvardKey People = Har alumni/staff, Harvard Guest Account = Authenticated User, logged in, Unauthenticated User = Not logged in | HarvardKey, Harvard Guest Account, Unauthenticated User|||||||

## Attached Notes

<p><strong>Platform: CRP</strong></p>
<p>Trigger this event after a user creates an account using the sign-up option in the modal when they click "Sign in to Harvard Online."</p>
