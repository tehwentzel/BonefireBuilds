# Assignment 7

## Writeup

### Design Rational

...

### AI Constructs

-   Zombie (FSM): The zombie construct is an enemy construct that uses a finite state machine to transition between 3 states: idle, patrolling and chasing
    

-   Patrolling: The default state, the zombie walks between set patrol points defined in the prefab script, using pathfinding. After a set amount of time, the zombie will be bored and go into the idle state.
    
-   Idle: The zombie will stay still and dance for a while, before resuming walking
    
-   Chase: If the player walks into the zombie’s field of view, it will act “startled” and chase the player using pathfinding. If the zombie hits the player, or the player gets a certain distance away, the zombie will idle for a second, look over their shoulder, and return to patrolling. If the zombie hits the player, the player is teleported to their last respawn position
    

-   Bird Flock: A flock of birds that flies around in the background of the scene for ambiance. The birds use AI-base flocking behavior to imitate a real swarm.
    

### Mechanism

-   The zombie: The zombie animation will “walk” when moving. Upon seeing a character, the zombie will stop and play a “startled” animation. Upon endearing the Idle state, the zombie will dance, and when the zombie loses sight of the player and exits the “chase” state, the zombie will stop and briefly look over its shoulder. Upon reaching one patrol point and moving to the next, the zombie will play a short turn animation (which needs work).
    
-   The player: currently there is one player character model working. The character includes an idle state, a “running” animation when moving, and a “button press” animation that plays when the player hit’s the “Interact” button (space bar).
    
-   Timmy: There is a model of Timmy on the map (who will eventually be the model for player 2), who will have an idle animation. If the player goes up to timmy and presses space (interact), Timmy will start boxing.
    

### Sounds

-   Sound when the jump pads activate
    
-   Sound when the player collides with a hazard (the tree)
    
-   Sound when the player interacts with the fire and teleports to the other fire.
    

### Physics

-   Jump pad launches player in the air
    
-   Grabbing and dropping mechanics with the capsules objects
    
-   Particle system for simulating a fire
    
-   Mechanics for teleporting between fires into an “upside-down” area where gravity is inverted