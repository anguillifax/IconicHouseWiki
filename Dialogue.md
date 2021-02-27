# Dialogue System

## Create a New Spoken Sequence
1. `Content Browser > Create > Miscellaneous > Data Asset > Spoken Sequence`
2. Set sound asset if available. Otherwise set `DurationIfNoSound`.
3. Fill out caption text.
4. Assign to `CommentInteraction` component.

## Caption Rules
* Start times must be in increasing order.
* An empty caption line hides the caption widget.
* A speaker of `None` results in the default style.
* `DurationIfNoSound` must be positive.
* The sequence stops once sound clip / duration finishes regardless of caption contents.
* The first caption does not have to start a 0s.
* A caption can have no lines.

## Create a New Caption Style
1. `Content Browser > Create > Widget`.
2. Design widget.
3. Implement `ISetCaptionText` interface.
4. Assign to caption line in `SpokenSequence`.

## Caption Widget Display Rules
* One widget at a time.
* Widgets are created and destroyed each line.
* If the widget does not implement `ISetCaptionText`, then the text on widget cannot be changed.
* The default style is `CaptionStyles/Caption_Default`.