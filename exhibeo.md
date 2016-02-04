# Using Exhibeo with Backdraft

<<<<<<< HEAD
[Download example document](https://github.com/CalebGrove/Backdraft-Docs/blob/master/downloads/exhibeo.zip?raw=true) (9.7 MB)
=======
[Download example document](https://github.com/CalebGrove/Backdraft-Docs/blob/master/downloads/exhibeo.zip) (9.7 MB)
>>>>>>> 228bcbd3f9b1c46eb70f56d2047d8cc1a3a66ae3

[Exhibeo](http://exhibeoapp.com) is a very easy to use web gallery generator created by the folks at Softpress, which makes it easy to create responsive-friendly galleries for Freeway. While most of the themes are responsive-friendly from the get-go, a few need a helping hand.

----

## Focus

1. Export the gallery from Exhibeo for Freeway.

2. Double-click inside the element that you want the gallery thumbnail to appear in.

3. In the top-bar, choose Insert > Action Item > Exhibeo Import.

4. Open the actions palette and choose the Exhibeo export file.

5. Resize the action item to barely fit the thumbnail preview.


## Bloxx

Simply follow the steps for the "Focus" theme.


## Impress

1. Begin by following steps 1-4 of the "Focus" theme.

2. Using the item handles, resize the action item to the full width of it's parent element and it's height to fit the preview.

3. Control-click on the action element, and chose "Extended". In the resulting dialog, switch to the `<div style>` tab.

4. Add this entry:

	| Name | Value |
	|------+-------|
	| `width` | `100% !important` |


## Slide, Showtime, and Thumblie

1. Follow the steps for the "Impress" theme.

2. In the extended dialog, add this as another entry:

	| Name | Value |
	|------+-------|
	| `height` | `auto !important` |

3. Save, publish, and test!
