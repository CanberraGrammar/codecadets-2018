---

title: Term 4

---

### Putting things together

In the past term we learnt various ways to utilise code to influence objects in a Game World.

<font color="red">You may continue using your existing game, or start a new one. <br/>

Additionally, if you are working on something of your own design, you may continue with that in its place</font>



If you choose to start a new project, you can copy your scripts over to the new one.

### A simple platformer game

##### Physics and Movement

We've in the past used combinations of **Rigidbody, Colliders and Translation scripts** to implement movement systems that move as though they existed in the real World

Using either:

* Your own Movement Scripts

* <font color="red">Recommended: </font>The Standard Assets First Person Controller

Introduce movement to some controllable object, and some form of following Camera. For further detail on custom simple movement, refer back to [Simple Movement from Last Term](SimpleMove.md).


##### Platforms

Create a normal cube element and mould it into the desired shape for a platform using the Scale elements. Make sure both the platforms and your object have colliders.


##### Moving Platforms

Of course, a collection of motionless platforms wouldn't present much of a challenge on their own, so let's up the difficult a little.

We want to make platforms that move around, namely back and forth, or side to side.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Jumping.gif" alt="" style="width: 100%;"/>



For a challenge, you can implement this yourself using your own methods, or [provided here is a simple script that will move a platform side to side in the X direction, smoothly.](SideToSide.md)




##### Materials

Using the Unity Materials feature, make some platforms slippery or bouncy. Something abnormal to increase the difficulty. Select these properties from the Collider menu in the Inspector for a platform.


<img src="https://canberragrammar.github.io/codecadets-2018/Resources/PhysMat.png" alt="" style="width: 100%;"/>

Create a new textures to distinguish your various platforms. I've made moving platforms purple, and hazards red, but you can choose whatever you like.

Right click in your assets folder and create a new Material like so.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Material.png" alt="" style="width: 80%;"/>

To apply it to an object, simply drag and drop the finished material onto the object in the world.

##### Hazardous Obstacles

Using our [Teleporter Code](teleport.md) from last term, we can create moving obstacles that return us to the Start of the course whenever we hit them. Restarting and 'death' in a video game are often one and the same afterall.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Hazard.gif" alt="" style="width: 100%;"/>

To do this, create a new object in the game. As this is a hazard we don't want to touch, let's colour it with a red texture as well.

We're going to place this object between two of our platforms, and then give it the following:

* The Teleport script, which we will then **link** to an object at the start of our platforming Challenge.

* The Side to side movement script from before.

This will create a moving object that goes back and forth to obstruct the target jump; the player must demonstrate timing skills to get past.

# Challenge

##### Checkpoint System

If our course gets too long and we reset back to the start when we fall, some players might get frustrated.

So we want to add a toggleable network of Checkpoints so that they can return to places they've reached.

This will utilise the teleporter script for two way teleporters, and a new one that can be used to unhide objects within the world.

To toggle whether something is hidden, you can use ```renderer.enabled = !renderer.enabled;```. This will convert a hidden object into a visible one, and a visible object into a hidden one.
