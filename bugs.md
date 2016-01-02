# Fixes for Known Bugs

Because of how Freeway treats templates, publishing updates for Backdraft is difficult and time-consuming for both me and you - making fewer larger updates more preferable than a lot of small updates. This page will cover known bugs in the current version of Backdraft (1.5) and their fixes. All the bugs listed here will be fixed in the next release.

* [Responsive CSS Menu not Toggling](#responsive-menu-toggle)
* [Right Column Pulling Away](#box-sizing)
* [Send Form Action Bug](#send-form)
* [Four Column Max-Width Bug](#four-max-width)

----

<div class="h2-segment" id="responsive-menu-toggle" markdown="1">

## Responsive CSS Menu not Toggling

### The Problem

At mobile device sizes, tapping the hamburger button is not causing the menu to appear.

### The Fix

1. Drag the Backdraft pages up into the master area of the Freeway sidebar.
2. Delete the `Backdraft Modules` folder.
3. Publish and test!

</div>
<div class="h2-segment" id="box-sizing" markdown="1">

## Right Column Pulling Away

### The Problem

The furthest right column of many modules is pulling away from the other columns when the site is previewed in a browser.

### The Fix

1. Install the latest version of the [Responsive CSS Menu action](http://actionsforge.com/actions/view/314-responsive-css-menu) from ActionsForge.
2. Test!

</div>
<div class="h2-segment" id="send-form" markdown="1">

## Send Form Action Bug

### The Problem

In Freeway Pro 6.1.2 using the Send Form action on an inline element may result in a large number of duplicated `FW_send_form.php` files being published and uploaded. While this won't hurt your site, it can get annoying.

### The Fix

1. In Freeway's sidebar, select **contactWrapper / contactInnerWrapper / twoLeft**.
2. Open the actions palette (⌥⌘A)
3. Remove the **Send Form** action.
4. In Freeway's sidebar, select the current page.
5. If you closed it, reopen the actions palette (⌥⌘A).
6. Click on the **+** button, and choose **Send Form** from the list of actions.
7. Configure to taste.
8. Repeat steps 1-7 for the contact form on the **Extra Modules** Backdraft page.

If you have multiple forms on one page, using the Send Form action in this manner may break them. If this is the case, there are no options except to revert back to using the action on inline elements and learn to ignore the extra PHP files.

</div>
<div class="h2-segment" id="four-max-width" markdown="1">

## Max-Width on Four Column Module

### The Problem

No matter how many times you forcefully deposit your face on your computer screen, the Four Column module won't respect the max-width you set.

### The Fix

Right-click on the `fourWrapper` element, chose **Extended**, pop over to the **<div style>** tab, and delete the `max-width: 1200px` entry.

</div>
