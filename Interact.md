---

title: Script Interaction

---


### Courseware link


## [http://unity.codecadets.com](http://unity.codecadets.com)

### The goal : Create teleporters using scripts

* We want to observe how multiple scripts can interact with each other.

* How they can pass information and make each other perform actions.


### Set up

* Create an object to act as your teleporter, perhaps a large cube or cylinder. For my demonstration, I used two cylinders flattened using scaling.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/cylinders.png" alt="" style="width: 100%;"/>

* Create a new script for your object called ```Teleporter.cs``` or similar


* As well as the Start() and Update() methods you're now familiar with, you want to introduce a new special case for collider interactions.

```cs
public void OnTriggerEnter(Collider other){
    //"other" is the reference name
    // for the object that entered the teleporter  
}
```

This function will be called only when the collider of another object moves into our teleporter's collider.

But to stop it from teleporting everything (including our world), before we do anything else we should first place a condition on what will happen.


```cs
if (other.gameObject.name == "YOUR_OBJECT"){
  //YOUR_OBJECT is the name of your controllable
  //object from last session.
  //As an example
  //other.gameObject.name == "Cube"
}
```
This will contain all our teleportation code, and ensure it only runs on our playable object, and not the world around it.


### One Way motion

Now we want to move the object that touches the teleporter. Above we called it ```other```, and we will use that name continuing on as well.

Create a new variable to be the coordinates of the target destination. Give any coordinates you want as the x,y,z, here I have used 2 for all of them.

```cs
Vector3 destination = new Vector3(2, 2, 2);
```

Now, we want to move our interacting object, called ```other``` to this location. To do this, we need to set ```other```'s position property to our new ```destination```;

```cs
other.gameObject.transform.position = destination;
```

Now save and run your game, you should find that you can interact with your teleporter, and your player will warp to the point in space you specified.

### Two Way motion

Now we want to add to it so we can send an object from one teleporter to another.

Similar to speed last week, add a public property to your script of type "Transform".

```cs
public Transform target;
```
This will add the property to our unity editor like so:

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/teleProp.png" alt="" style="width: 40%;"/>

Copy and paste your original teleporter so that you have two in the world now. Now, select your first teleporter and **drag** the second telepoter from the heirarchy menu into the target property.


<img src="https://canberragrammar.github.io/codecadets-2018/Resources/DragProp.png" alt="" style="width: 40%;"/>


Do the same for Teleporter 2, add Teleporter 1 as its target.

### Stopping the chaos

If you've got this far, you should have a pair of teleport pads that warp an object back and forth. However, you're likely stuck inside them, switching quickly from one to the other.

Now we need to turn off the teleporters for a couple of seconds after we've travelled through in order to prevent this.


<font color="red">TO DO: Cooldown timer</font>

### In working order

You should now have two working teleporters that connect to one and other. But we've built it with a custom Destination property, so this code could be used for as many teleporters as you want.

If you need something else to do, try make the following using this script.

* A 2 pairs of two way Teleporters that operate separately.

* A loop of 3 or more teleporters that take you around the world.

* A set of teleporters that all go one way to a single central teleporter.
