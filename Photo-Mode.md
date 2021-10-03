# Photo Mode

Photo Mode is based on teleporting the player to the right spot.

## Adding a New Memory Trigger

1. First we need to indicate to the system that the object you are looking at is a memory trigger. Add the component `PhotoModeTarget` to the actor.
1. Next we need to tell the system where to teleport the player once they click on it. You can technically use any actor to do this, but we recommend creating a new PlayerStart each time since it has the friendliest interface. Position this PlayerStart where you want the player to land after clicking the memory.
1. Finally, we need to tell the memory trigger which object to teleport the player to. Go back to the memory trigger actor. Select the `PhotoModeTarget` component and assign the field `Warp Target` to the PlayerStart you just created.

## Using the `Main` Tag

Because we are using multiple player starts, Unreal will assume we want to randomly place the player into a different place each time we start the game. To prevent this, there is a special tag called `Main`.

1. Select the PlayerStart you want the player to begin the game at every time.
1. In the details panel, search for `Actor > (Advanced Options) > Tags`.
1. Add a new tag called `Main`.

## Changing the Filters

The PhotoMode look is a combination of a postprocessing volume and UI widget. Both of these can be edited freely.

To edit the postprocessing volume, open the asset `OverworldPlayerCharacter`. Find the component `PostProcess`. This postprocessing volume is toggled on and off when moving between Photo Mode. Any visual settings in the details panel can be edited freely.

To edit the UI, open the asset `Implementation > PhotoMode > PhotoModeFrame`. This widget is nested inside the player HUD and toggled on and off when moving between Photo Mode. This widget can be edited in any way, shape, or form freely.

Editing the shader is much more complicated. It is implemented in `Implementation > PhotoMode > M_PhotoModeFilter`. Be sure to consult someone knowledgeable in Unreal shaders.