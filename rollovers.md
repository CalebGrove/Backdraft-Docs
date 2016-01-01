# Flexible-Width Rollovers
----

The difficult thing about the rollover action is that it requires all the image stages to be layers, which is the opposite of inline construction. However, with a tad of ingenuity this can be circumnavigated. For this example, let's say that we are creating rollover where each of the graphics is a 400px wide by 200px high rectangle.

----

## Steps

1. Begin by adding an inline HTML box. Name it ``rolloverWrapper``, deselect the width field in the inspector, but set the max-width to 400px. Open the extended dialog and switch to the `<div style>` tab. Add a listing with `width` as the name, and `100%` as the value.

2. Draw three rollover graphics **inside** the `rolloverWrapper` box as layer items (not inline!). Name them `click`, `hover`, and `normal`, respectively.

3. Align them on each-other and group them. Name the new group container ``rolloverGraphic``, and apply the Rollover Action to it. (For a more detailed set of instructions on this part, see the [official documentation](http://www.softpress.com/kb/questions/326/Rollover+Action)).

4. Open the extended dialog for that container, and in *both* the ``<img>`` and ``<div>`` tabs, add entries with `class` for the name and `flexImage` for the value.

5. As always, save, publish, and test!
