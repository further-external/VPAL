# Page Load Started

CRP updates - include the following page_data variables:

        "course_name": "<course_name>",
        "course_program_dates": "<course_program_dates>",
        "page_location": "<page_location>",
        "page_title": "<page_title>",
        "site_section": "<site_section>", // expected value 'CRP'
        "site_section2": "<site_section2>", // expected value 'CRP'
        "type": "<type>" // expected value 'CRP'

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ page_data: null });  // Clear the previous page_data object.
dataLayer.push({
  "event": "page_load_started",
  "detailed_event": "Page Load Started",
    "page_data": {
        "course_name": "<course_name>",
        "course_program_dates": "<course_program_dates>",
        "page_location": "<page_location>",
        "page_title": "<page_title>",
        "site_section": "<site_section>", // expected value 'CRP'
        "site_section2": "<site_section2>", // expected value 'CRP'
        "type": "<type>" // expected value 'CRP'
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
|page_data.applications_close|string|Value for date when the Applications Close for a course.|Jul 10, 2023|||||||
|page_data.article_author|string|Value for Article Author. ex. 'Liz Mineo'|Liz Mineo, John Smith,  Aswita Tan-McGrory, Harvard Online|||||||
|page_data.article_name|string|Value for Article Name. ex 'Introductory Courses for Anything You Want to Learn in 2023'|Introductory Courses for Anything You Want to Learn in 2023|||||||
|page_data.article_photo_content|boolean|Value for Article Photo Content; does the article contain an images?|yes, no|||||||
|page_data.article_video_content|boolean|Value for Article Video Content. Does the article contain any video content? ex. 'yes'|yes, no|||||||
|page_data.breadcrumb|string|A delimited list of hierarchical sections that describe the current page's location within the navigation of the site.|Home&gt;Women&gt;Tops&gt;Sweaters, Mens - Tops - Sweaters - Supmina, Wool, Rayon, Checkout &gt; Order Thank You|||||||
|page_data.country|string|The country associated with the current page.|US, CA, FR, UK|||||||
|page_data.course_certificate_price|string|Value for Certificate Price - ex. 1600|1600, 950, 0, 25.00|||||||
|page_data.course_difficulty|string|Value for Course Difficulty. ex. 'Introductory'|introductory, intermediate|||||||
|page_data.course_language|string|Value for Course Language. ex. 'English'|english|||||||
|page_data.course_length|string|Value for Course Length. ex. '8 weeks \| 2-4 hours a week'|8 weeks \| 2-4 hours a week, 4 weeks 1-2 hours a week, 5 weeks long|||||||
|page_data.course_modality|string|Value for Course Modality - ex. 'Online'|on\_campus, online, online\_hybrid, flex, ...|||||||
|page_data.course_name|string|Value for Course Name. ex 'Financial Analysis and Valuation for Lawyers'|Financial Analysis and Valuation for Lawyers, Data Privacy and Technology|||||||
|page_data.course_pace|string|Value for Course Pace. ex. 'Self-Paced'|self-paced, instructor|||||||
|page_data.course_platform|string|Value for Course Platform. ex. edX'|hbs, edx, ...|||||||
|page_data.course_price|string|Value for Course Price. ex. '1600'|1600, 945, 125.00|||||||
|page_data.course_program_dates|string|Value for Course Program Dates. ex. May 11, 2022 – May 10, 2023|May 11, 2022 – May 10, 2023|||||||
|page_data.course_promo_name|string|Value for Course Promotion Name. ex. 'Related Products'|Related Products|||||||
|page_data.course_school|string|Value for Course School. ex. 'HKUSTx, Harvard School of Engineering and Applied Sciences'|HKUSTx, HarvardX, CaltechX, Harvard School of Engineering and Applied Sciences|||||||
|page_data.course_transcript_language|string|Value for Course Transcript Language. ex. 'English'|english|||||||
|page_data.language|string|The language of the current page, usually pulled from the &lt;html&gt; tag lang attribute.|en-us, en-gb, ch-cn, fr-ca, fr-fr|||||||
|page_data.page_location|string|The URL of the page currently being viewed. This value will include the full, unaltered URL of the page\/screen the user is currently viewing, including query parameters, fragments, etc., for example https:\/\/www.example.com\/home?user=true&audience=test\#aboutus.|https:\/\/www.example.com\/home?user=true&audience=test\#aboutus|||||||
|page_data.page_title|string|The title of the page currently being viewed, generally available in &lt;title&gt;.|Data Science Principles \| Harvard Online Course, 18th-Century Opera: Handel & Mozart|||||||
|page_data.pages_viewed_num_visit|string|Running total of how many pages or screens a visitor had viewed at the time they took a website or mobile app action. Count re-starts with each visit.||||||||
|page_data.site_section|string|The section of the site that the current page resides in. site\_section2 through site\_section5can also be used if the site has many sections.|series, blog, news, make-a-course|||||||
|page_data.site_section2|string|Captures the sub-section of the site where the page being viewed is located|series &gt; harvard-on-digital, series &gt; leadership, course &gt; data-privacy-technology, course &gt; digital-health|||||||
|page_data.type|string|The type of page currently viewed.|home, pdp, article|||||||
|user_data.user_id|string|The ID of the currently logged-in user, provided the site supports authentication and the user is authenticated. For CRP, this should be the hashedEmail value when available; if not, use an empty string (""). If the user is not authenticated but the email field is populated, use the captured hashedEmail value. However, if the user is authenticated, use the hashedEmail associated with their logged-in account.|ba7816bf8f01cfea414140de5dae2223b00361a396177a9cb410ff61f20015ad|||||||
|user_data.user_type|string|The users current login status, LX Key = Temporary name of users who registered directly on the CRP platform authenticated user HarvardKey = Harvard alumni/staff authenticated user, Harvard Guest Account = Authenticated User, logged in, Unauthenticated User = Not logged in | LX Key(Temporary name of users who registered directly on the CRP platform) HarvardKey, Harvard Guest Account, Unauthenticated User|||||||


## Attached Notes

<p dir="auto"><span style="font-weight: 400;"><strong>Platform: ALL</strong></span></p>
<p dir="auto">Fire whenever a user loads in a new page, whether that is done synchronously or asynchronously.</p>
<p dir="auto">This event should be the first pushed into the data layer on each page. Given many 3rd party scripts push events to the data layer, this event push should be placed in the page&nbsp;<code>&lt;head&gt;</code>&nbsp;and should be the first&nbsp;<code>&lt;script&gt;</code>&nbsp;tag on the page to ensure it is the first event.</p>
<p dir="auto">There is no longer a concept of virtual page view, so this event should be fired whenever a virtual page view would have been fired in the past, such as when a new screen is loaded asyncronously within an angular, react, or vue app/embed.</p>
