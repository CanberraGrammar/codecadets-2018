---

title: Scripts to create and destroy objects

---


### Courseware link


## [http://unity.codecadets.com](http://unity.codecadets.com)

### The goal : Create a simple projectile attack system


This is a long one and may take two sessions, so don't feel a need to rush through it.

## Create a new Object to be your projectile

I personally recommend a simple sphere. Scale it to an appropriate size.

> GameObject -> 3D Object -> Sphere

For the purposes of this tutorial, we will be making a physics-less missile object, similar to a fireball or spell. However, if you use Rigidbody and leave the physical model in, it can just as easily be a physical missile or bullet.


### Particles and Effects

First, we're going to want to import a new assets pack if you don't have it already.

* Right click the Project window down the bottom,

> RightClick -> Import Package -> ParticleSystems

* Then, once that is imported, Right Click your object in the heirarchy window, and create a new Particle System on it.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Particles.png" alt="" style="width: 50%;"/>

* Customise this Particle System in the inspector window as you see fit.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/PSystem.png" alt="" style="width: 35%;"/>

* Go to your projectile object, and **untick the box that says MeshRender**. This will remove the physical form of the object, but leaving its collider and the particle systems you've placed in it.

Your object should now roughly look like a Fireball or similar energy project, leaving a trail of particles in flight.


### Create copies

* Make the object a pre-fab. (This makes it easier to instantiate.) To do this, just drag your completed object into the Assets folder at the bottom.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Prefab.png" alt="" style="width: 80%;"/>

### Spawning in


* Create new Script on your player object, call it ```Attack```. This code could go in our SimpleMove file, however this would make it harder to read and understand; seeing as a Unity object supports multiple scripts, we will benefit from this decision.

> FOR THESE SECTIONS YOU ARE WORKING IN Attack.cs

* Similar to previous sections, we want some public variables we can access from our editor. One for a reference to our projectile object, and another as a speed constant. Put these at the top under the class.

```cs
public GameObject projectile;
public float speed;
//This should be somewhat familiar territory now
```

* Then, within our update method, we first want a condition to recognise a button press. Unlike the movement Axes, in this case we just want to recognise a specific key being pressed once.

```cs
if (Input.GetKeyDown(KeyCode.G)) {
//I have chosen G, but you can use any key you wish.
}
```
* This code will recognise a Key Down event on the chosen key. That means it will recognise input the second the key is pressed. There is an alternative in ```GetKeyUp``` that will respond to the **release** of the key instead.

* Put a simple message like ```print("Key Pressed");``` in the if statement and run it to confirm it responds to input.

* Now we need to **Instantiate** our object. This means to create an **Instance** of it within the game.

```cs
GameObject missile = Instantiate(projectile, gameObject.transform.position, Quaternion.identity) as GameObject;
```

* This line is relatively long, but essentially you just give it position data and then create a new GameObject called ```missile```. For now, it should do nothing other than create a ```missile (clone)``` in the Heirarchy when run.



### Flying true

Once we've spawned an object in, we want to give it Velocity so that it flies off on its own. Instead of using a simple coordinate Translation however, we're going to use Rigidbody physics to apply a speed property.

* If it doesn't already, make sure your projectile Pre-fab has a Rigidbody component. Make sure ```Uses Gravity``` is unticked for now, but you can enable if really you want to.

```cs
Rigidbody rb = missile.GetComponent<Rigidbody>();
rb.velocity = transform.forward * speed;
```

* This will access the instantiated missle's physics properties, and apply a forward speed to it, multiplied by the speed factor you pass in from the editor. Make sure this is not 0.

### Destruction

* Add new script to projectile prefab in your assets folder. Call it ```Projectile```.

> FOR THESE SECTIONS YOU ARE WORKING IN Projectile.cs

* Add an ```OnTriggerEnter``` method like we've used in previous sessions. Check your teleporter code if you don't remember what this looks like. Make sure the Missile Prefab has ```Is Trigger``` ticked in the inspector menu for its collider.

* In the class add a public variable to reference our explosion effect within the code.

```cs
public GameObject SPFX;
```

* Then, from the Unity editor drag the Explosion asset into this property. If you can't find it, use the Search bar in the project menu.

* Then within our OnTriggerEnter method, we want to self-destruct the missile and instantiate our explosion effect.

```cs
Destroy(gameObject);
Instantiate(SPFX, transform.position, transform.rotation);
```

### Bug Fixing

Run your game and try to fire your new projectile system. If you've followed this code exactly, one somewhat entertaining problem should immediately present itself.

The missile is going to explode **inside your player** object, because it spawns inside its collider and then trigged ```OnTriggerEnter```. This sends the object flying from the force of the explosion.

* To fix this all we need to do is add a condition to ignore our player object in the ```OnTriggerEnter``` method.

```cs
if (other.gameObject.name == "Cube"){
    //IGNORE
}
else {
    //PUT YOUR DESTRUCTION CODE IN HERE
}
```


### FIRE!

* If all things went as planned, you should be able to launch the projectile system forward like so.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/FIRE.gif" alt="" style="width: 90%;"/>

* For this demonstration I left the MeshRender on so the object is clearly visible.

* You may find the missile is capable of destroying your terrain, leading to your object falling through the floor. See if you can fix this using conditions like before.

----

### Extension Activity.

Create a new script to be "Damage", that handles a response to being hit by a projectile, and has a Health value so that objects can take multiple hits.
