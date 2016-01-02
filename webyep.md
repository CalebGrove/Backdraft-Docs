# Using the WebYep Actions With Backdraft

For the most part, the Webyep action should work without a hitch within Backdraft's environment. However, there are a few things to keep in mind, as outlined below.

----

## Tips

* As with anything else in Backdraft, the Webyep actions MUST be inline elements. To do this, double-click to enter the text-flow of an element, then use the "insert" menu to choose the action that you want to use.

* In Backdraft, there is a custom CSS class applied to the images through the extended dialog that makes them flexible width. If you want any WebYep images to be flexible-width, you will need to add it to the actions extended interface. Open the actions palette, click on the **extended** button, and paste this in: `class="flexImage"`

* WebYep galleries are not flexible-width, and so must not be used with Backdraft. I've cooked up a custom module for this (essentially a looping row of Webyep images), so if you need a WebYep gallery-like feature, please email me with a copy of your receipt for the WebYep actions, and I'll send it to you with directions for implementation. Send the email to <caleb@onrampwebdesign.com>.
