# Quests

The questing system is broken into two parts: quests and tasks. A *quest* is a group of things the player needs to do. A *task* is one particular thing the player needs to do. A *quest* contains 1 or more *tasks*.

## Creating a New Quest

1. Go to `Content/Quests`.
1. Duplicate the asset `__Template`.
1. Assign the quest information. `Name` is used for both the title of the quest panel and the button in the tab menu. `Description` is shown in the quest panel underneath the title.
1. Create the tasks. Each task is two parts: an id and a description. Begin by assigning a unique id to the quest. This will be used internally by the system and will never be shown to the player. Keep track of this id. Unroll the task you just created. `Description` is the text of the bullet point.
1. Now we need to add the quest to the quest book itself. Right now it is floating in space. We need to tell the quest system about it.
1. Open the asset `Content/Implementation/Quests/QuestSystem`. Go to the My Blueprint tab and find `Variables/Templates`. Click on it. In the details panel, find the `Default Value` section. Use the `+` button to add your new quest. The order the quests are listed here is the same order as they will appear in the menu.

## Revealing a Quest

Keep in mind that all quests initially start hidden.

These are the general instructions of how to use the system. Ask someone knowledgeable about Unreal on what this looks like in blueprints.

1. Look in the Components panel of the actor. Press the button Add Component and add a `RevealQuestUtil` component.
1. Look in the details panel for the section `Default/Quest`. Assign the quest you want to show to the component.
1. Call the function `RevealQuest` on the component you just added.

## Fulfilling a Task

Each quest is composed of tasks. Once all tasks are fulfilled, the quest is marked as complete. This section explains how to fulfill a task.

1. Find the actor the player should click on to fulfill the task.
1. Look in the Components panel of the actor. Press the button Add Component and add a `QuestCompletionInteraction` component.
1. Look in the details panel. Find the section `Default`. You will need two pieces of information, the quest the task is part of and the task itself.
1. Assign the property `Quest` to the asset you created.
1. Find the unique id of the task you want to fulfill. You may have to open the quest asset itself and search for it. Type this into the field `Task`.