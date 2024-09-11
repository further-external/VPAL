# Enroll Now Click

CRP Status = Variable update needed to fire this new event name for clicking through to CRP from harvard online. No dataLayer udpate required, this is an update for the Further team for implementation only.

User clicks  CTA link to enroll on CRP flow. A new event name called enroll_now needs to be set up with the 'Enroll or Apply' lookup variable based on the domain of the link clicked.





## Tag Set up Notes (for Further)
If the link can be picked up by GTM we will use the existing lookup table "Enroll or Apply" and add another option for the new subdomain to identify an enroll_now link. We will need to add this subdomain to the existing apply now link (perhaps renaming to apply or enroll now). If the link cannot be picked up, we will set up a new trigger and variables using these values.
