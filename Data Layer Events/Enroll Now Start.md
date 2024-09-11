# Enroll Now Start

CRP status - this is a new event designed for the CRP flow. Fire this event when the user starts to fill out a field in the Enroll now page. Only fire this for the user's first engagement with the form. 

(Note: we will be pulling the course name and the program dates from the page_load_started event on the page, so we need to confirm they are implemented correctly there)


### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "enroll_now_start"
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |



