# Photo Mode

Photo Mode is based on teleporting the player to the right spot.

## Adding a New Memory Trigger

1. First we need to indicate to the system that the object you are looking at is a memory trigger. Add the component `PhotoModeTarget` to the actor.
1. Next we need to tell the system where to teleport the player once they click on it. You can technically use any actor to do this, but we recommend a PlayerStart since it has the friendliest interface. Position this PlayerStart where you want the player to land after clicking the memory.
1. Finally, we need to tell the memory trigger which object to teleport the player to. Do this by selecting the `PhotoModeTarget` component and assigning the field `Warp Target` to the actor you just created.

## Using the `Main` Tag

Because we are using multiple actors, Unreal will assume we want to randomly place the actor every time we start the game. To prevent this, there is a special tag called `Main`. Assign this tag to the player start that you want the player to begin the game at every time.