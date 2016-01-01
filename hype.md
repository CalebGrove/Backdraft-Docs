# Using Hype With Backdraft
----

<!--[Download example document](http://getbackdraft.com/docs/downloads/hype.zip) (2.6 MB)-->

[Hype](http://tumult.com/hype/) is a great WYSIWYG editor for creating some really awesome JavaScript and HTML5 based animations. This tutorial will instruct you how to get your Hype canvas to be flexible-width using Backdraft.

<aside markdown="1">
Notes:

* This relies on jQuery to work, so don't use this on the same page as a "scripty" action.
* You can only have one Hype element on your page.
* Hype creates monolithic amounts of slow-loading code - use sparingly.

</aside>

---

## Steps

1. When you create your Hype animation, the Hype document width should reflect the width of the element in Backdraft that it is going to be placed in. The formula for this is `width of the element in Freeway` - `left padding` - `right padding`. If it is going into the one-column module with default padding, that is `1200px - 14px - 14px = 1172px`, so the Hype document should be 1172px wide. The height can be whatever you want, but do jot it down as you will need it later.

2. Export the Hype animation to the **Site Folder** for your Freeway website. This way the preview within Freeway will be accurate.

3. Insert an HTML (not markup) item inline where you want the Hype animation to appear. Deactivate the width and min-height. Set it's overflow to **hidden**.

4. Right-click on the HTML item you just created. Choose **Extended** and add this entry in the `<div style>` tab:

	|  Name   |  Value  |
	|   - -   |   - -   |
	| `height` | `0` |
	| `padding-bottom` | `60%` |

	**Important:** You will need to change the `padding-bottom` value to match the height/width ratio of your Hype document. Enter the width and height of the Hype document into the calculator below to get the value that you need to use.

	<aside>
	<form name="Calculator">
	<div>
		<label>Width: <input type="text" id="width" placeholder="1200" onkeyup="validateThis(document.getElementById('width'))"></input>px</label>
	</div>
	<div>
		<label>Height: <input type="text" id="height" placeholder="600" onkeyup="validateThis(document.getElementById('height'))"></input>px</label>
	</div>
	<div>
		<input type="button" value="Calculate" onclick="pxToPercent()"></input>
	</div>
		<span id="result"></span>
	</form>
	<script>
		function pxToPercent() {
			var pxWidth = document.getElementById("width").value;
			var pxHeight = document.getElementById("height").value;
			var percent = pxHeight / pxWidth * 100;
			var solution = Math.ceil(percent * 10000) / 10000;
			document.getElementById("result").innerHTML = "<code>padding-bottom: " + solution + "%</code>";
		};

		function validateThis(toValidate){
			if (/^[0-9]*$/.test(toValidate.value) === true){
				toValidate.className = "valid";
			} else {
				toValidate.className = "invalid";
			}
		}
	</script>
	</aside>

5. Just inside the HTML item, insert an inline [Crowbar action](http://actionsforge.com/actions/view/13-crowbar-inline), with the height set to flexible. In the actions palette, click on the **code** button, and paste the following in the resulting box:

		<!-- Begin Hype -->
		<div id="containingElement">
			<div id="scalecontainer">
				<!-- Replace the lines below with the code from your Hype export -->
				<div id="hype_hype_container" style="position:relative;overflow:hidden;width:1172px;height:500px;">
					<script type="text/javascript" charset="utf-8" src="hype.hyperesources/hype_hype_generated_script.js?80825"></script>
				</div>
				<!-- Replace the lines above with the code from your Hype export -->
			</div>
		</div>
		<!-- End Hype -->

6. Open the `project-name.html` file that Hype exported, copy the code wrapped in the comments `<!-- copy these lines to your document -->` and `<!-- end copy -->`, and use it to replace the code in-between the replacement comments of the code in step 4.

7. Still in your Freeway document, go to `Page > HTML Markup…` in the menubar. Choose `Before </head>` in the drop-down menu, and paste the following code *below* any other code there:

		<!-- Begin Hype Head -->
		<style>
			#scalecontainer {
				-moz-transform-origin: left top;
				-webkit-transform-origin: left top;
				-ms-transform-origin: left top;
				-o-transform-origin: left top;
				transform-origin: left top;
				width: 1172px !important; /* <- This should match the Hype document width */
				margin: 0 auto;
			}
			#containingElement {
				width: 100%;
				height: 600px; /* <- This should match the Hype document height */
				position: relative;
			}
		</style>
		<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
		<script type="text/javascript" language="javascript">
			var alsoenlarge = true;
			$(function(){
				if(isScalePossible()){
					$('#scalecontainer').css({position: 'absolute', margin: 0});
					scaleSite();
					scaleSite();
					$(window).resize(scaleSite);
				}
			});
			function scaleSite(){
				containerw = $("#containingElement").width();
				containerh = $("#containingElement").height();
				sitew = $('#scalecontainer').width();
				siteh = $('#scalecontainer').height();
				f = containerw/sitew;
				f = containerh/siteh<f?containerh/siteh:f;
				if(!alsoenlarge && f>1) f = 1;
				$('#scalecontainer').css({
				  "-moz-transform"    : "scale("+f+")",
				  "-webkit-transform" : "scale("+f+")",
				  "-ms-transform"     : "scale("+f+")",
				  "-o-transform"      : "scale("+f+")",
				  "transform"         : "scale("+f+")",
				  "left"              : ((containerw-(sitew*f))/2)+"px",
				  "top"               : "0px"
				});
			}
			function isScalePossible(){
				can = 'MozTransform' in document.body.style;
				if(!can) can = 'webkitTransform' in document.body.style;
				if(!can) can = 'msTransform' in document.body.style;
				if(!can) can = 'OTransform' in document.body.style;
				if(!can) can = 'transform' in document.body.style;
				if(!can) can = 'Transform' in document.body.style;
				return can;
			}
		</script>
		<!-- End Hype Head -->

8. Find these lines of CSS in the code block above, and set them to match the dimensions of your Hype document:

		width: 1172px !important; /* <- This should match the Hype document width */
		...
		height: 600px; /* <- This should match the Hype document height */

10. Finally, when you upload the website to your server, you will need to manually upload the `projectname.resources` folder to the root level of your server using a FTP client.
