# Quests

The questing system is broken into two parts: quests and tasks. A *quest* is a group of things the player needs to do. A *task* is one particular thing the player needs to do. A *quest* contains 1 or more *tasks*.

## Creating a New Quest

1. Go to `Content/Quests`.
1. Duplicate the asset `__Template`.
1. Assign the quest information. `Name` is used for both the title of the quest panel and the button in the tab menu. `Description` is shown in the quest panel underneath the title.
1. Create the tasks. Each task is two parts: an id and a description. Begin by assigning a unique id to the quest. Keep track of this. Unroll the task you just created. `Description` is the text of the bullet point.
1. Now we need to add the quest to the quest book itself. Right now it is floating in space. We need to tell the quest system about it.
1. Open the asset `Content/Implementation/Quests/QuestSystem`. Go to the My Blueprint tab and find `Variables/Templates`. Under the details panel, find the `Default Value` section. Use the `+` button to add your new quest. The order the quests are listed here is the same order as they will appear in the menu.

## Revealing a Quest

Quests are initially hidden until 