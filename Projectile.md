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

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Particles.png" alt="" style="width: 90%;"/>

* Customise this Particle System in the inspector window as you see fit.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/PSystem.png" alt="" style="width: 90%;"/>

* Go to your projectile object, and **untick the box that says MeshRender**. This will remove the physical form of the object, but leaving its collider and the particle systems you've placed in it.

Your object should now roughly look like a Fireball or similar energy project, leaving a trail of particles in flight.


### Create copies

* Make the object a pre-fab. (This makes it easier to instantiate.) To do this, just drag your completed object into the Assets folder at the bottom.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Prefab.png" alt="" style="width: 90%;"/>

### Spawning in

* Create new Script on your player object, call it ```Attack```. This code could go in our SimpleMove file, however this would make it harder to read and understand; seeing as a Unity object supports multiple scripts, we will benefit from this decision.

* Similar to previous sections, we want some public variables we can access from our editor. One for a reference to our projectile object, and another as a speed constant. Put these at the top under the class.

```cs
public GameObject projectile;
public float speed;
//This should be familiar territory now
```

* Then, within our update method, we first want a condition to recognise a button press. Unlike the movement Axes, in this case we just want to recognise a specific key being pressed once.

```cs
if (Input.GetKeyDown(KeyCode.G)) {
//I have chosen G, but you can use any key you wish.
}
```
* This code will recognise a Key Down event on the chosen key. That means it will recognise input the second the key is pressed. There is an alternative in ```GetKeyUp``` that will respond to the **release** of the key instead.

* Now we need to **Instantiate** our object. This means to create an **Instance** of it within the game.

```cs
GameObject missile = Instantiate(projectile, gameObject.transform.position, Quaternion.identity) as GameObject;
```

* This line is relatively long, but essentially you just give it position data and then create a new GameObject called ```missile```.


```cs
Rigidbody rb = missile.GetComponent<Rigidbody>();
rb.velocity = transform.forward * speed;
```
### Flying true

### Destruction

* Add new script to projectile prefab. Call it ```Projectile```.

* Add an OnTriggerEnter method like we've used before.

* In the class add a public variable to reference an Explosion data type.

```cs
public GameObject SPFX;
```

* Then, from the Unity editor drag the Explosion asset into this property.


### FIRE!

* If all things went as planned, you should be able to launch the projectile system forward like so.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/FIRE.gif" alt="" style="width: 90%;"/>

----

### Extension Activity.

Create a new script to be "Damage", that handles a response to being hit by a projectile, and has a Health value so that objects can take multiple hits.
