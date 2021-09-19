# Creating Dialogue

1. Go to `Content/Dialogue/`.
2. Duplicate the `__Template` asset.
3. If available, import the voiceover and place in `Content/Dialogue/Voiceover`. The file format must be `.wav`.
4. Open the dialogue asset.
5. If there is a voiceover, assign it to the `Sound` property. If there is not, set `Duration if No Sound` to how long the caption should be visible.
6. Unroll the `Lines` property.
7. Write in the transcript for the voiceover. Each subtitle will begin being shown at `BeginAt`. The text `Caption` will be shown to the player. The subtitle will stop being shown once the next line starts or the audio clip ends. You will want to match `BeginAt` with the moment a phrase begins to be said in the sound clip.

**Tip:** Open the voiceover in a sound editor (like Audacity) and scrub through it for the `BeginAt` timestamps.

I know the interface is really clunky. I'm really sorry, there's not much I can do about it! Bear with it, we can persevere!! 🙏 