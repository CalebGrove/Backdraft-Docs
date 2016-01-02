# Using v1.5 Modules in v1.1 Sites

Because Freeway templates are essentially a FW file with some special attributes, it's impossible to upgrade a website from an older version of Backdraft to a newer version. A site is tied to the version of Backdraft that it was initially built with. However, it is entirely possible to get the new modules introduced in 1.5 to work in a website built using 1.1.

Note: These directions will also allow you to use the new [utility classes](hiding-elements.html) and prevent Mobile Safari from zooming in on rotate.
{:.aside}

----

## Steps

1. Download, install, and create a new document using Backdraft 1.5.
2. Open your site built with v1.1 in Freeway.
3. Copy the **Responsive Header**, **Five Column**, and/or the **Six Column** modules from the 1.5 document and paste them as inline elements into your 1.1 website. You can now close out of the Backdraft 1.5 document.
4. Back in your 1.1 document, apply the [Auto Clearfix action](http://actionsforge.com/actions/view/299-auto-clearfix) to any page that the new modules will be on.

	It's actually a good idea to apply the action to all of the pages, as it can fix/prevent a lot of weird layout issues.
	{:.aside}

5. Go to **Page / HTML Markup… / Before &lt;/head&gt;**.
6. Scroll down the the very bottom, then **under** the `</style>` tag, paste this in:

		<style type="text/css">
		/* CSS for using the Responsive Header, Five Column, and Six Column modules from Backdraft 1.5 in Backdraft 1.1 */
		/* Don't forget to apply the Auto ClearFix action to the page! */

		/* Keep Mobile Safari from zooming in on rotate */
		body { -webkit-text-size-adjust: 100%; }

		/* Tweaking column widths so they have a 20px left margin start */
		#PageDiv .fiveTwo, #PageDiv .fiveTwo.f-ms,
		#PageDiv .fiveThree, #PageDiv .fiveThree.f-ms,
		#PageDiv .fiveFour, #PageDiv .fiveFour.f-ms,
		#PageDiv .fiveFive, #PageDiv .fiveFive.f-ms,
		#PageDiv .sixTwo, #PageDiv .sixTwo.f-ms,
		#PageDiv .sixThree, #PageDiv .sixThree.f-ms,
		#PageDiv .sixFour, #PageDiv .sixFour.f-ms,
		#PageDiv .sixFive, #PageDiv .sixFive.f-ms,
		#PageDiv .sixSix, #PageDiv .sixSix.f-ms {
			margin-left: 1.7%;
		}

		/*----------------------------------------*/
		/* 928px breakpoint (Netbook/iPad) */
		@media screen and (max-width:928px) {

			/* 5 column TRANSFORM to 2 column top, 1 column bottom */
			#PageDiv .fiveOne, #PageDiv .fiveOne.f-ms,
			#PageDiv .fiveTwo, #PageDiv .fiveTwo.f-ms {
				width: 49.1%;
			}
			#PageDiv .fiveThree, #PageDiv .fiveThree.f-ms,
			#PageDiv .fiveFour, #PageDiv .fiveFour.f-ms,
			#PageDiv .fiveFive, #PageDiv .fiveFive.f-ms {
				width: 32.2%;
				margin-top: 20px;
			}
			#PageDiv .fiveThree, #PageDiv .fiveThree.f-ms {
				clear: both;
				margin-left: 0;
			}
			#PageDiv .five .flexImage {
				display: block;
				margin-left: auto;
				margin-right: auto;
			}

			/* 6 column TRANSFORM to 3x2 */
			#PageDiv .six, #PageDiv .six.f-ms {
				width: 32.2%;
				margin-left: 1.7%;
			}
			#PageDiv .sixOne, #PageDiv .sixOne.f-ms,
			#PageDiv .sixSix, #PageDiv .sixSix.f-ms {
				margin-left: 0;
			}

			#PageDiv .sixThree, #PageDiv .sixThree.f-ms  {
				float: right;
				margin-left: 0;
			}

			#PageDiv .sixFour, #PageDiv .sixFour.f-ms  {
				margin-left: 0;
				clear: both;
			}

			#PageDiv .sixFour, #PageDiv .sixFour.f-ms,
			#PageDiv .sixFive, #PageDiv .sixFive.f-ms,
			#PageDiv .sixSix, #PageDiv .sixSix.f-ms  {
				margin-top: 20px;
			}

			#PageDiv .six .flexImage {
				display: block;
				margin-left: auto;
				margin-right: auto;
			}
		}

		/*----------------------------------------*/
		/* 570px breakpoint (mobile) */
		@media screen and (max-width:570px) {

			/* 6 Column TRANSFORM to 2X3 */
			#PageDiv .six, #PageDiv .six.f-ms {
				width: 48.2%;
				margin-left: 0;
			}
			#PageDiv .sixOne, #PageDiv .sixOne.f-ms,
			#PageDiv .sixThree, #PageDiv .sixThree.f-ms,
			#PageDiv .sixFive, #PageDiv .five.f-ms {
				float: left;
				clear: both;
			}
			#PageDiv .sixTwo, #PageDiv .sixTwo.f-ms,
			#PageDiv .sixFour, #PageDiv .sixFour.f-ms,
			#PageDiv .sixSix, #PageDiv .sixSix.f-ms {
				float: right;
				clear: none;
			}
			#PageDiv .sixThree, #PageDiv .sixThree.f-ms {
				margin-top: 20px;
			}

			/* Responsive Header */
			#PageDiv .responsiveHeader, #PageDiv .responsiveHeader.f-ms {
				padding: 14px;
			}
		}

		/*----------------------------------------*/
		/* 480px breakpoint (smaller mobile) */
		@media screen and (max-width:480px) {

			/* 5 column TRANSFORM to 1x5 */
			#PageDiv .five, #PageDiv .five.f-ms {
				width: 100%;
				margin-left: 0;
				margin-top: 20px;
			}
			#PageDiv .fiveOne, #PageDiv .fiveOne.f-ms {
				margin-top: 0;
			}

			/* Tweak PageName to override 1.1 defaults */
			.responsiveHeader .pageName {
				text-align: center !important;
				margin-bottom: 0 !important;
			}

			/* Do not hide the navigation in Responsive Header */
			.responsiveHeader .navigation {
				display: block !important;
			}
		}

		/*----------------------------------------*/
		/* Utility classes */

		@media screen and (min-width:929px){
			.desktopHide { display: none !important; }
		}

		@media screen and (min-width:481px) and (max-width:928px){
			.tabletHide { display: none !important; }
		}

		@media screen and (max-width:480px) {
			.mobileHide { display: none !important; }
		}
		</style>

7. Save, publish, and test!
