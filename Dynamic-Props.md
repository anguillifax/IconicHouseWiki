# Dynamic Props

A dynamic prop is a prop that responds to mouse clicks and can be interacted with.

# Structure

Base components are `UseHandler`, `ListenHandler`, and `AnyInteractionHandler`. Use the callbacks for highly specialized implementations.

# Common Cases

**Comment:** Add a `SingleCommentInteraction` to the actor. Assign the dialogue asset.

**Quest Task Completion Trigger:** Add a `QuestCompletionInteraction` to the actor. Assign the quest and associated task to mark complete.