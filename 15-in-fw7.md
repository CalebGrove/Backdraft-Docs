# Using Backdraft 1.5 with Freeway 7
----

If you have a website that you built with Backdraft 1.5 (BD1.5), you are probably interested in how you can use some of the new responsive tools that Freeway 7 (FW7) introduced in your website. In this article, we will discuss general compatibility, then beak down the new FW7 features and just how compatible they are with your website. To get some more details of what is new in FW7, please read [Softpress' extended reference](http://download2.softpress.com/docs/Extended_Reference_For_FW7.pdf?_ga=1.14162866.485017711.1379472539).

*Keep in mind that this is a living document that has been based on limited testing with a stock copy of Backdraft and a small sample of websites. As I'm unable to test "all the things", I will need feedback from you all concerning any Backdraft functionality that might break in FW7. Thanks!*

## General Compatibility

First things first, you should be able to open any website you created in BD1.5/FW6 in FW7 and publish without any problems. Anything you could do under FW6 you can safely do in FW7 (changing content, adding/removing/customizing modules, etc).

With that said, I highly recommend that you archive a copy of the folder that contains your website and media before opening the file in FW7 so that you can revert easily at any time.

## CSS Menus Action

One of the coolest things in FW7 is the big update to the CSS Menu action. You can define a breakpoint where it will turn into a hamburger menu that slides down from the top of the page. If you want to use that instead of the Responsive CSS Menu action that came with Backdraft 1.5, follow these directions:

1. Select the **navigation** element of a **Responsive CSS Menu** module instance and open the Actions window (⌥⌘A).
2. Click on the **x** to the left of the action name at the top of this window. This will remove that action from the item.
3. Click on the **+** at the bottom of the Actions window.
4. Select the **CSS Menus** action, and click **OK**.
5. Configure the action to taste, and make sure to set up the responsive options!

## Responsive Layout

Freeway 7 also introduces a tool that allows you to define custom settings for items at breakpoints in Freeway's construction view (for more details of how this works, please read [Softpress' extended reference](http://download2.softpress.com/docs/Extended_Reference_For_FW7.pdf?_ga=1.14162866.485017711.1379472539)). Due to some fundamental changes in FW7, and how Backdraft 1.5 is constructed, if you are using a Backdraft 1.5 website in FW7, you can only use a subset of the supported settings that can be customized at breakpoints.

In a nutshell, you can adjust everything in the **appearance** pane of the inspector in breakpoints. However, you shouldn't make any adjustments in the **general** pane in any breakpoints besides **Default**, as it may cause conflicts with the hand-coded CSS that Backdraft 1.5 uses.

Also, don't adjust the page width at breakpoints, as it will break all the graphic items that aren't pass-though and wreak havoc with the layout.

If you want the breakpoints in Freeway to reflect the default Backdraft breakpoints for appearance customizations, here's a list of the breakpoints in BD:

- 928px (Netbook/iPad)
- 570px (Horizontal mobile)
- 480px (Mobile)

## Closing Notes

As I said at the beginning of this document, this is a living document that has been based on limited testing with a stock copy of Backdraft and a small sample of websites. As I'm unable to test "all the things", I will need feedback from you all concerning any Backdraft functionality that might break in FW7. If you find anything that doesn't work right, please let me know.
