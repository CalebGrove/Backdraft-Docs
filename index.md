# What's New in Backdraft 2.1

Backdraft 2.1 is an incremental improvement on 2.0. It fixes a few bugs, and reflects what we've learned about working with Freeway 7 over the past year. Although there are no big new features, you should noticed a considerably refined experience when working with 2.1.

1. Improved

	* All padding is defined as percentages. As a result, the buggy Box Sizing action is no longer needed, and the boxes should have much more consistent sizing. This change should make Backdraft much easier to work with.
	* Heading text styles are now responsive. As such, Backdraft now requires Freeway 7.1+.
	* Better semantics. The website title in the header modules are no longer `<h1>`s.
	* Instead of using "width: 100%", we are now using "width: undefined".
	* Scroll wheel capture has been disabled for the embedded Google Maps in the Contact Form module. Oftentimes, the map would keep mobile users from scrolling down the page because the map would capture the scrolling.
	* Logos in the headers are now pass-through graphics and flexible.
	* The [Responsive Video action](http://actionsforge.com/actions/responsive-video) has been updated to v1.2.

2. Fixed

	* Submenus are now styled.

Go forth and make the web responsive!

**Caleb Grove**  
Dude at [OnRamp Web Design](http://onrampwebdesign.com)  
Creator of [Backdraft](http://getbackdraft.com)
