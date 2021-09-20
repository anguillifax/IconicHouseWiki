# Dialogue

Dialogue is voiceover clips.



## Creating Dialogue

1. Go to `Content/Dialogue/`. All the following steps assume you are in this folder.
1. First, we need to import the voiceover audio clip. Import this into Unreal and place it in the `/Voiceover` folder. Keep in mind that Unreal only accepts `.wav` format.
1. Now, we need to describe what subtitles are being shown and when. To do this, we need to create a `Dialogue Sequence` data asset. The easiest way to do this is to duplicate the `__Template` asset.
1. Next, we need to fill out the voiceover information. Open the asset. Begin by assigning the voiceover clip to the `Sound` property. Ignore the `Duration if No Sound` property, it is only used if there is no sound clip.
1. Finally, we need to add the subtitles. Unroll the `Lines` property. Each entry here is one line that will be shown to the player one after another. Each line will be closed once the next line starts or the audio clip ends.
1. First, we need to write down what is being said. Put this in the `Caption` field.
1. Now, we need to tell the system when to show this line. Each line will begin to be shown once the playback reaches a certain time. This time is specified by `BeginAt` in seconds. You will want to match `BeginAt` with the moment a phrase begins to be said in the sound clip. For best results, use a sound editor to quickly scrub through the waveform.



## Playing Dialogue

1. First find the actor you want to play the dialogue on.
1. Add a `SingleCommentInteraction` component.
1. Click on the newly added component. Assign the voiceover asset to `Default/Dialogue` in the details panel.