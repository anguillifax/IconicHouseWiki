# Quests

The questing system is broken into two parts: quests and tasks. A *quest* is a group of things the player needs to do. A *task* is one particular thing the player needs to do. A *quest* contains 1 or more *tasks*.



## Creating a New Quest

1. Go to `Content/Quests`. All remaining steps assume you are inside this folder.
1. First, we need to create a new Quest Template asset. The easiest way to do this is to duplicate the asset `__Template`.
1. Next, we need to fill out the quest information. Open the asset. `Name` is used for both the title of the quest panel and the button in the tab menu. `Description` is shown in the quest panel underneath the title.
1. Now we will need to create the tasks. Tasks are the things the player actually does.
1. Use the `+` button to add a new entry to `Tasks`. Give this new task a unique id. This id is used internally by the system and will never be shown to the player. Keep track of this id, you will need it later.
1. Now that you have a task created, we need to fill out its display information. Unroll the task you just created. `Description` is the text shown for the task's associated bullet point.
1. Now we need to add the quest to the quest book itself. Right now it is floating in space. We need to tell the quest system about it.
1. Open the asset `__QuestOrder`. Add your quest asset to the list using the `+` button. Keep in mind that the quests will appear in the same order that they appear here.



## Revealing a Quest

To reveal a quest, call the function `Reveal Questbook Quest` from a Blueprint.

Keep in mind that all quests initially start hidden.



## Fulfilling a Task

Each quest is composed of tasks. Once all tasks are fulfilled, the quest is marked as complete. The following steps describe how to make it so that clicking on an actor fulfills a task.

1. First we will need to tell the system that you can click on this actor to trigger an action.
1. Find the actor the player should click on to fulfill the task. Look in the Components panel of the actor. Press the button Add Component and add a `QuestCompletionInteraction` component.
1. Now, we need to tell the actor which task they are going to mark complete. To do this, we will need two pieces of information, the target quest template and the task id.
1. Look in the details panel. Find the section `Default`. Assign the property `Quest` to the asset you created.
1. Now we need the id. Open the quest template asset and find the unique id for the task you want to fulfill. Copy and paste this id into the field `Task`.

The alternative is to fulfill a task directly through code. To do this, call the function `Fulfill Questbook Task` and pass in the same information as above.