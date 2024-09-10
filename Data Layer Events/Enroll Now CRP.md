# Enroll Now CRM

User clicks  CTA link to enroll on CRP flow. We are requesting the data attributes below for these links. We would be able to pick up the link_url and link_tex if it is a standard <a> tag but in the case of a button where it can't be picked up we are also requesting those value.


## HTML Data Attributes

```html
<button
  data-gtm-event="enroll_now"
  data-gtm-link_text="<link_text>"
  data-gtm-link_url="<link_url>"
>
```

## Variable Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|link_text|string|required|The full text of the link.|`enroll now`|
|link_url|string|required|The full URL of the link.|https://www.example.com/form|
