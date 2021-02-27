## Create New View Model
1. `Content Browser > Create > Blueprint > Static Mesh View Model`
1. Configure static mesh component.
1. Set radius of `ClosestView` and `FarthestView`.
1. Move `InitialViewpoint` to where the camera should start viewing the object.
1. Add `ViewerTextSurface` components to create popup text.
1. Assign model to `ExamineInteraction` component.

## Text Surface
* The forward vector is a normal out of text surface.
* Add an arrow component as a child for visualization.
* Only rotation affects whether surface is visible.
* If surface area overlaps, then closest angle to normal is shown.
* `MaxViewAngle` is +/- maximum degrees camera can be rotated away from normal.