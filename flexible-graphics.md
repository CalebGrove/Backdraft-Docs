# Flexible Graphic Items

One of the only downsides to Freeway 7 is how it handles graphics on a responsive website. Basically, all graphic that need to be flexible must be imported as pass-through graphics now.

Here's why: In the past, Freeway never had to deal with having a flexible design-view. When you would add a graphic item to a page, that graphic item would have a fixed width set in pixels. That fixed width value could be overridden with a snippet of CSS (this is how Backdraft 1.5 worked with graphic items). However, now Freeway's design view can be viewed at different sizes (breakpoints). This means that everything on a page **must** be flexible or it will cause overflow problems - which can be pretty nasty. Now, remember how regular graphic items aren't flexible? Yep, that is the cause.

However, pass-through graphic items are treated in Freeway's eyes much like regular old HTML items. They are flexible.

Some of you may be asking what a pass-though graphic is - and that is a fair question. As Softpress says in their [knowledgebase article on the topic](http://www.softpress.com/kb/questions/82/Working+with+Optimized+Images+(%22Pass+Throughs%22)): *"A pass through is an exact copy of the original image you imported, no change can or will be made to the quality, size, or any aspect of pass through images."* In other words, you can't use any of Freeway's built-in image editing tools with a pass-through graphic. It needs to be cropped, sized, and optimized before you add it to your Freeway website.

However, it's not quite as painful as it sounds. There is actually a pretty decent workflow that will still allow you to use Freeway's built-in editing tools while arriving at a properly configured pass-through image.

---

## Steps

1. Ensure that you are in the default breakpoint.

2. Add your image to the page as a regular graphic item (not a pass-through) either by dropping the image onto one of the placeholders in the modules, or by inserting an inline graphic item and dropping the image into that.

3. Use Freeway's graphic editing tools until you are happy with how it looks in the default breakpoint.

4. Export the image by selecting the graphic item, and going to **File > Export** in the menubar or by using the **⌥⌘E** shortcut.

5. In the resulting dialog, make sure that it is set to export the selection and that the export format matches the format that you set up in Freeway. Save it to the **Media** folder and name it sensibly.

6. In the next dialog, just click **OK**. By default, all the settings here will match your settings for the graphic in Freeway.

7. Now, go to **File > Import** (**⌘E**). Select your freshly exported image. Check **Pass-through** and click **Open**.

8. Finally, open the inspector and set the max-width to 100%. **DONE!**
