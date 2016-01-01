# Using Master Pages in Backdraft
----

There is nothing different or magical about how master pages and child pages work in Backdraft when compared to any other Freeway document, but there is a "best practice" approach that will make your life easier.

What we are going to do is add three full-width wrappers to the master page. The first will hold the header, the second will be left blank to hold each pages content, and the third will hold the footer. Let's get started!

***Note:** The master pages that are used by Backdraft to store modules (prefixed by **BD**) should not be used to create new pages. They are used just to hold the modules in a place where they will not be published with the rest of the site.*

----

## Video

<div class="video-container" markdown="1">
<iframe src="http://www.youtube.com/embed/_xRnpm9dGTw" seamless="seamless"></iframe>
</div>

## Configuring Your Master Page

1. Begin by going to the **Extra Modules** page and copying the **fullWidthWrapper** element to your clipboard.
2. Navigate to the **Main Master** page. This will be your main master page (profound, huh?).
3. Double-click inside the page, and hit **⌘V** to paste the **fullWidthWrapper** in it as an inflow item.
4. Select your new **fullWidthWrapper** and hit **⌘D** twice, so you now have three instances of it on the page.
5. Rename the first **fullWidthWrapper** to `headerWrapper`, the second to `contentWrapper`, and the third to `footerWrapper`.
5. In the **Extra Modules** page, choose your header and copy it to your clipboard.
6. Back in your master page, double-click inside **headerWrapper** to get a blinking text cursor.
7. Paste your header inside it and configure to taste.
8. By default, the **fullWidthWrapper** element has a min-height of 100px set. This keeps it from collapsing to 0px when it's empty, but after you have content in it, you should deactivate the min-height. To do this, in the first pane of the inspector, change the **Height** dropdown from **Minimum** to **Flexible**.
9. Find the module that you want to use for your footer, and paste it into **footerWrapper**. Leave the middle wrapper empty, this will hold the individual content of the non-master pages.

## Using Your Master Page

Now that we have your master page configured, let's look at how you will use it to create a "normal" page.

1. Drag the **Main Master** page from the **Master pages** folder to the **Site Folder** in Freeway's sidebar. Name your page in the resulting dialog. Now you have a normal page that is based on the master page! **Don't make any changes to the header or footer in the normal pages. To modify these, use the Master Page.**
2. Pick the first module that you want on the page directly below the header element and copy it to your clipboard.
3. Back at your normal page, double-click inside **contentWrapper** and paste your module inside it.
4. Choose the next module that you will have on the page (optional). *This is when things will get a little tricky*: you need to paste it into the **contentWrapper** element, but because you already have a module in it, there is no place to double-click!
5. Using Freeway's sidebar, select the module that you added to the page in step #4.
6. Press the → key on your keyboard *once*. This will place an inflow text cursor directly after the module. You may not be able to see it, but it's there.
7. Hit **⌘V** to paste your second module in.
8. Rinse and repeat steps 4-7 for any other module you want on the page.
9. Rinse and repeat steps 1-8 for any other pages you need.
10. Now comes the magical part - make a modification to the header or footer on the master page, and you will see that all of the pages based on that master reflect the change while still keeping their individual content!
