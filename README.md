# Ghost in the Shell

**Ghost in the shell** is a 3D Platformer game made with **UnrealEngine 4.27.2** by **Antoine Mordant** and **Julien Bertrand**.

<img src="images/MainMenu.PNG" alt="main menu" title="Main Menu">

---

# Plot

    You wake up in a cold dark place. You have no idea how did you get here. By looking around, you seems to be in a graveyard. Suddenly, you remember :

    You were going back home but the night fell faster than you thought. You decided to cut through the forest to be quicker without listnening of all the stories you've heard about murder and disappearance in it at night.

    After a long run, you looked around. Obviously, you lost your way. You tried to retrieve it when you heard a sound behind you. Thanks to the moon light, you saw it. A monster, who should have been human once but who looked more like a living puppet of putrefied flesh stood there in front of you. You didn't had the time to move that it were already on you. The last thing you remember is being tracked by the thing before passing out.

    Yes, you remember now. You are dead. You are in Hell. It's colder that you thought it would be. However, you don't feel blocked here. You have the strange feeling that your physical body is nearby and with it, your way out of this gloomy place.

    Follow your path and find your body to get out of Hell. B ut be careful ! Hell is a dangerous place and you are not welcomed here...

---

# Player

<img src="images/Player.PNG" alt="player" title="Player">

The controls are basically the same that the original CharacterController from Unreal.

<img src="images/PlayerControls.PNG" alt="player controls" title="Player Controls">

## Controls

- `WASD` : Move
- `SPACE` : Jump
- `P` : Pause the Game
- `Mouse` : Turn the camera around the player

---

# Enemies

We used **behaviour trees** to code our enemies. Each enemy type has his own **behaviour tree, blackboard and ai controller blueprint** to program his behavior.

## Basic enemy

<img src="images/BasicEnemy.PNG" alt="BasicEnemy" title="Basic Enemy">

The first enemy you will encounter and the most commun has **1 HP**. He walks randomly until he saw you. Then he will hunt you until you are dead or he lost you. The best way to get rid of him is to **jump on his head**. That will kill him. Once he is dead, he will drop a **healing potion**.

<img src="images/BehaviourTreeNPC.PNG" alt="Behaviour Tree NPC" title="Basic Enemy's Behaviour Tree">

## Big enemy

<img src="images/BigEnemy.PNG" alt="BigEnemy" title="Big Enemy">

This is the stronger enemy you will encounter. He has **2 HP** and run away to his spawnpoint when he is hit. If you let him go, he will return **after healing himself**. He also drop a healing potion when he dies.

<img src="images/BehaviourTreeNPC2.PNG" alt="Behaviour Tree NPC2" title="Big Enemy's Behaviour Tree">

## Chasing enemy

This is the same as the first enemy but when he doesn't see the player, he just stand still.

<img src="images/BehaviourTreeNPC3.PNG" alt="Behaviour Tree NPC3" title="Chasing Enemy's Behaviour Tree">