# Known Bugs

Because there is no real upgrade path for Freeway templates, I try and keep the number of releases to a minimum. If there are any minor bugs, I may wait until the next major release to fix them. For major bugs, I will release a patch update (x.x.1). However, the only way to apply the changes in the patch releases to your current document is to make the changes manually. Hence, this page where I list all known bugs and how to fix them yourself.

----

## Old Artifacts

**This was fixed in Backdraft 2.1.1**. There are some old artifacts from past versions of Backdraft that I forgot to clean out. Here's how you can fix it:

1. Remove the **Box Sizing** action from the **Flexible Video** module in the **BD: Extra Modules** master page, and anywhere else you used that module on your website.

2. Remove the **Flexible Page** action from the **BD: Extra Modules** page.

3. Profit!

## Four Column Out-Of-Order

**This was fixed in Backdraft 2.1.2**. If you are using an older version, follow these steps to apply the changes to your current document:

1. In the **BD: Framework Modules** master page, use the sidebar to select the **fourMiddleRight** element. Hit ⌘C to copy it to your clipboard.

2. Hit the ⌫ key to delete it.

3. Using the sidebar, select the **fourRight** element.

4. Hit the ← key on your keyboard once.

5. Press ⌘V to paste **fourMiddleRight** back in.

6. Do it again, but this time for the four column module on the **BD: Alt Modules** page, and anywhere you used a four column module in your website.
