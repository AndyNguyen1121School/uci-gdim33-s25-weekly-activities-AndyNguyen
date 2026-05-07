# GDIM 33 In-Class Activities

## W1

### Activity 1

https://docs.google.com/drawings/d/1omhXGpyFYs1cH8w1IvPOZ4nwgCNixbkcyZSOJxBWWaA/edit?usp=sharing

1. Some patterns that emerged during the creation of my mood board was that most of the games I put included melee combat in the hack-and-slash genre. All of these games are also PVE.
2. One of my groups mates expressed that they like playing difficult games and time management games. We are alike in the sense that we both desire intensity in games rather than calm, cozy games.
3. My table's TA expressed that their current favorite game was Baldur's Gate 3, which is also a game that I am currently enjoying. Our tastes are similar in the way that we both like playing non-competitive games. Although we both dabble in competitive games, we would rather spend our time playing single player games like Tomb Raider and Prince of Persia.



### Activity 2

![alt text](image.png)


### W3

### Activity 1
![alt text](image-1.png)

### Activity 2
1. Having the event name a variable reduces the chances of the programmer having an error due to typing the wrong event name in the graph. Additionally, since every other graph has access to the string, the programmer can access the variable in any graph to activate the custom event.

2. I used Debug logs to track every state change to see whether the state is being entered correctly. I labeled my debug logs to "dialogue to explore" and "explore to dialogue" to track the exact game state the player is in.

3. Set cursor lock and visible is important to my vertical slice because I am making a FPS, which requires the cursor to be hidden and locked to control the camera.

4. The game state is relevant to my vertical slice as I need something to track what happens when the game starts, continues, and ends. In the start, a countdown will begin that will activate the main game state. When the player dies or completes the level, the end game state will activate.

### W4

### Activity 1

Playable parts in my vertical slice:
- Character movement: Jumping and walking.
- Core mechanics: Propel mechanic, damage, guns, shooting
- Timer
- Enemy death
- Gun animations
- Weapon Switching

Playtesters: 
- Zom
- Zoya 
- Jacob
- Noah
- Kristin
- Julie

Players do not interact with propell mechanic often. Shotgun should have more feedback behind it's shot. Add barriers for the roof. Shots spawn behind the player.

Possible adjustments: 
- add higher platforms to incentivize players to propell more. 
- Make rifle stronger. Shotguns are too strong
- Sensitivity is too high, add a slider.


### Activity 2
1. The writer can add more dialogue to this setup because all of the dialogue is managed through scriptable objects that the writers can create without worrying about the backend. In the backend, the flow of the dialogue is control automatically without having the writers interfering with internal logic.

2. The writer can only put four dialogue nodes before the layout group overflows and makes the UI look weird.

3. The regenerate nodes button is used to create nodes to access custom classes that do not derive from monobehavior or scriptable objects within the visual graph. However, new monohavior and scriptable object scripts are scraped and automatically added to be used in the visual graph.

### W5
### Activity 1
1. Set up walking animations for enemies
    - Add idle and walking animation clips in the animator
    - Create a parameter named "IsWalking" to control transitions.
    - In the EnemyManager C# script, set "IsWalking" to true if the agent's velocity magnitude is above 0.05f and false if less
    - TEST: When the enemy walks towards the player, the "IsWalking" parameter in the animator should be set to true

2. Set up transitions between walking states 
    - Hook up Idle -> Walk and Walk <- Idle
        - Idle -> Walk: Set exit time to 0 and transition time to 0.25. In the transition, add the parameter so the animation activates when IsWalking == true.
        - Walk -> Idle: Set exit time to 0 and transition time to 0.25.  In the transition, add the parameter so the animation activates when IsWalking == false.
        - TEST: When the animator parameter "IsWalking" is true, the enemy should smoothly transition from idle -> running and vice versa.

3.  Play attack animation when in range.
    - Add the attack animation to the animator
    - Set a transition from the attack to idle. Make the exit time 0.75 and the transition duration 0.25f.
    - Make a function in EnemyManager to detect the range between the enemy and the player.
    - Make a minimumDistanceToHit variable to customize the range of the attack.
    - Make a attack cooldown to make sure the enemy does not spam the animation
    - TEST: When the player is close enough and the cooldown is over, play the attack animation using animator.CrossFade("Attack", 0.1f). Reset the cooldown afterwards

### Activity 2
1. I completed setting up the walking and idle animations and linking it up to the speed of the navmesh. Additionally, I have completed the attack logic when the distance between the enemy and the player are below the minimum distance. Now, I have to set up the actual damage logic so the player dies when they are atatcked.

### W6
### Activity 1
1. 
    - I added new enemy behavior that chases the player when they get in range. I also adjusted physics and movement logic.
    - https://andy-nguyen-uci.itch.io/propellantplaytest2
    - Playtest Goal: Do the guns feel satisfying? Is the movement responsive and tight? How do players feel about the control scheme?

    Playtesting Notes: NEED sensitivity slider. Make longer levels, gameplay is fun but players desire more. Enemies feel scary when they chase the player (intended).

### Activity 2
1. The multiply setting makes the resulting color darker and less saturated because it multiplies the two colors together. The multiplication node essentially muliplies two Vector4's whose values range from 0-1 per channel. If a color has a value less than one, then the color becomes darker and less saturated.

2. If 2 alpha values are multiplied together, the result will be more translucent unless both alpha values are 1. If a value is less than one, then the result will be more transparent.

3. The shader gets the UV values from mesh vertices. This tells you where in the texture should map onto the model. 

4. I don't understand what the different blend modes mean but I find the concept very interesting and I am excited to learn more.

