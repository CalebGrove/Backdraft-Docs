# Creating Your First Backdraft Page

In this tutorial you will be walked though creating your first responsive page.

----

## Video

<div class="video-container" style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; background-color: black;" markdown="1"><iframe src="http://www.youtube.com/embed/oWpMS-e2zCM" style="position: absolute; width: 100%; height: 100%; background-color: transparent; border: 0px none transparent; padding: 0px; overflow: hidden;" seamless="seamless"></iframe></div>

## Setup

1. [Install Backdraft](installation/).
2. Launch Freeway and in the **new document** dialog, choose **Responsive** from the site panel and select **Backdraft 2.0**.
3. Choose a location for the site folder.
4. Once the document opens, create a new page in the site folder based off of the **Main Master** master page, and name it `My First Responsive Webpage`.

## Adding Modules

Now it’s time to add the modules to the page!

1. First, let’s add the header. In Freeway’s site panel, navigate to the **BD: Extra Modules** page.

2. Click on the arrow to the left of the page title to see the page contents. If you can't see the arrow, click on the gear icon at the bottom of the site panel and check "Show items".

3. Click on **sideBySideHeaderWrapper** in the site panel and hit ⌘C to copy it to your clipboard.

4. Go back to your own page, and double-click in the page canvas. You should see a blinking text cursor. Hit ⌘V to paste the module onto the page.

5. Customize the text and CSS menu, preview in a browser and try shrinking the window width to make sure that it’s responding.

6. Now we will add a hero image to showcase your product. Go to the **BD: Framework Modules** page, copy the **oneWrapper** to your clipboard.

7. Back on your page, double-click beneath the header and hit ⌘V to paste the module in. Remove the text, and replace the image with your own. **For your new image to be flexible, it needs to be imported as a pass-though.** See [this article](flexible-graphics.html) for more details.

8. Underneath the hero image, we want to have a two column layout to describe our product. Now we will go to the **BD: Framework Modules** page, copy the **twoWrapper** element, and paste it into the text flow of your new page, just like you did in step 7. Customize the content to taste.

9. Last but not least, we need a footer. Go and get the four column module from the **BD: Alt Modules** page and add it to the page just as you've been doing.

Congratulations, you have just created a responsive page! Make sure the test and verify that it is all working correctly.

## Adding Custom Elements

You've just created your responsive website, but what if you want to add images inside the columns, or have a Google Maps action element on the page?

This requires **Inline Construction**. Building inline is not as hard as some people think it is, but it is a large departure from the standard method of adding elements in Freeway. The basis of inline is adding HTML, graphic, and other elements just like you would add text. Let's just look at one example.

### Google Maps Action

The Google Maps action is very easy to make flexible, and is much like many other action items. Double-click inside one of the elements and go to **Insert > Action Item > Google Maps** in the topbar. Open up the inspector and enter ``100%`` in the width text area. Set the height to whatever you wish.
