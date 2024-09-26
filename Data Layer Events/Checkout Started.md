# Checkout Started

This event has been updated for the CRP - (pending testing, we could just go with the HTML attribute)


### 

## HTML Attribute

Add the following data attribute to the checkout link that takes the user to the offsite payment platform. If we rely on the data attribute we are relying on capturing the ecommerce data from the prior add_to_cart event that will be firing on the page.

data-gtm-event="begin_checkout"

![image](https://github.com/user-attachments/assets/6b1655bf-b55a-497a-8cc6-db738ea29456)


## Tag Updates Needed

We will need to update MHX custom event to also capture course name and program dates at the event level for the existing MHX courses.



