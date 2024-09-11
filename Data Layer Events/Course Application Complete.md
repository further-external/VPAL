# Course Application Complete

CRP Notes: Not part of CRP. Delete after all courses have migrated to CRP. Also note myhbx implemented this manually and never added this DL event.

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "course_application_complete",
  "detailed_event": "Course Application Complete",
    "event_data": {
        "course_application_step": "<course_application_step>",
        "name": "<name>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.course_application_step|string|Datasource for Application Step Name||||||||
|event_data.name|string|Captures the human-friendly name of the form.|Payment Info, Mailing Address, Payment Address, Contact Us|||||||

## Attached Notes

<p><strong>Platform: myhbx</strong></p>
<p>This event fires when the course application is successfully submitted. (step3)</p>
