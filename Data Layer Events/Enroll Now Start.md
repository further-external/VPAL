# Enroll Now Start

CRP status - this is a new event designed for the CRP flow. Fire this event when the user starts to fill out a field in the Enroll now page. Only fire this for the user's first engagement with the form. 

(Note: we will be pulling the course name and the program dates from the page_load_started event on the page, so we need to confirm they are implemented correctly there)


### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "enroll_now_start",
   "user_data": {
        "user_id": "<user_id>",
         "user_type": "<user_type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated. For CRP this will be the hashedEmail value when avaliable, if not avaliable pass an empty string value ("")|ba7816bf8f01cfea414140de5dae2223b00361a396177a9cb410ff61f20015ad|||||||
|user_data.user_type|string|The users current login status, HarvardKey People = Har alumni/staff, Harvard Guest Account = Authenticated User, logged in, Unauthenticated User = Not logged in | HarvardKey, Harvard Guest Account, Unauthenticated User|||||||


