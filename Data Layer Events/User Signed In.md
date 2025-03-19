# User Signed In

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "login",
  "detailed_event": "User Signed In",
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
|event_data.method|string|Records the system the user utilized to log in.|HBSO, HarvardKey, Native|||||||
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||
|user_data.user_type|string|The users current login status, HarvardKey People = Har alumni/staff, Harvard Guest Account = Authenticated User, logged in, Unauthenticated User = Not logged in | HarvardKey, Harvard Guest Account, Unauthenticated User|||||||

## Attached Notes

<p><strong>Platform: CRP</strong></p>
<p>Trigger this event when a user successfully signs into their account. This occurs after they select one of the three sign-in options: the native sign-in from the modal on the CRP, or one of the two authorized methods (HBSO or HarvardKey).</p>

