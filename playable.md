---

title: Final Week of Term 2

---


### Courseware link


## [http://unity.codecadets.com](http://unity.codecadets.com)

### The goal : Make a simple moveable object

At the end of last term some of you may have found the standard assets moveable character. We can return to this later, for now we want to implement a more basic movement system from scratch so we can appreciate how it all works.

This lab is designed to last one to two sessions depending on your speed.

### Adding Physics to an Object and your world.

We covered this last time but seeing as it's been a while, let's do it again.

Start by selecting your terrain in the Hierarchy menu. Follow to the top bar, and select

```
Component -> Physics -> Terrain Collider
```

This is likely already added by default, you should be able to see it in the inspector for your terrain.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/TerrainCollider.png" alt="Adding collision to your ground" style="width: 100%;"/>

The properties of the terrain collider will appear over in the inspector for your terrain.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/TerrainCollider_2.png" alt="It appears over here" style="width: 100%;"/>

Next, add two things to your object in the world. Select your object, and go to the physics menu again and add these two things.

* Rigidbody Physics. These will apply gravity to your object, and you can change the properties of the object's mass in the inspector on the right.

* An appropriately shaped collider. Box will work for more objects, but if you have a different shape like a ball you would want a sphere. This will stop your falling object from just phasing through the floor.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/ObjectColliders.png" alt="Add collision to your objects" style="width: 100%;"/>


If done correctly, your object should fall naturally and stop on the ground like so.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/Gravity.gif" alt="falling firetruck" style="width: 100%;"/>

### Adding a Camera to your object

When you created the new project there should've been a default camera in the world. This Camera is stationary, and would be useful in a top down game. But on a large map you could easily lose your player.

Add a Main Camera to the Heirarchy of the Object you want to move. If your main Camera isn't in the world still, ```GameObject -> Camera```.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/NewCamera.png" alt="" style="width: 40%;"/>

### Providing mobility


To do this we need to create a new script. Right click the project menu and select ```Create -> C# Script```.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/NewScript.png" alt="" style="width: 100%;"/>

Name it something like ```SimpleMove```. Then select the script in the project menu, and go over to the inspector and hit the open button.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/OpenScript.png" alt="" style="width: 100%;"/>


The script should look like this on creation.

```

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class SimpleMove.cs : MonoBehaviour {

	// Use this for initialization
	void Start () {

	}

	// Update is called once per frame
	void Update () {

	}
}
```

#### Add the script to your object(s)

Simply drag your script from the project menu onto the game object you want to move.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/ScriptAdded.png" alt="" style="width: 100%;"/>

It should add the script to the object's properties.

#### A Unity C# script

When first created, the C# script will have two main functions. ```Start()``` and ```Update()```. We are interested in the second of these two.

The ```Update()``` function is called once per frame of the game's run time, so anything you put in there will happen many times a second. To add your own code to this function, put it inside the {Braces}.



#### Aside: Relative timing

Because all your computers will run at slightly different speeds, functions call once per frame are potentially extremely inconsistent. For this, we will need the expression ```Time.deltaTime``` to let Unity calculate the average speed.


### Moving your object.

We need a function to move an object, for which we will use ```transform.Translate(x,y,z);```. Here, x, y and z are all numbers that you can set to change the speed of the object.

Add a simple expression like ```transform.Translate(1 * Time.deltaTime, 0, 0);``` to your update function, to move at 1 times your average frame speed in only the X direction. You should see your object sliding around on its own in one direction, ideally along the ground if you added gravity.

Play around with these numbers to move in different directions.


### Taking Control

#### Selecting the buttons

To take control of our simple movement, we need to tell the script to respond to our input. First of all, we want to look at what keys are bound to your controls at present.

Going to ```Edit -> Project Settings -> Input``` will let you see the list of default controls. For now we only care about movement, we have the Vertical and Horizontal Axes on this list, bound to both the Arrow Keys and WASD like most normal games.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Controls.png" alt="" style="width: 100%;"/>

#### Mapping input to movement.

We need another expression here, ```Input.GetAxis("AxisName")``` where AxisName will be one of the Axes from our control list, where we want Vertical and Horizontal.

An example of a full basic movement translation like this: ```transform.Translate(Input.GetAxis("Horizontal") * Time.deltaTime, 0, Input.GetAxis("Vertical") * Time.deltaTime);```

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Moving.gif" alt="" style="width: 100%;"/>

### Finished all this? Try and implement a basic jump using the knowledge gained here, and make Spacebar the Jump button.


-----

### Week 2 - Adding onto it.

This week we will continue to look at basic movement as a means of understanding how code interacts with our game objects.



#### Cleaning up. Adding a public property

Last time we used the expression ``` 10 * Time.deltaTime``` (or any number of your choice) in every parameter of transform.Translate. Let's clean that up a little. Near, the top of your file, under the class declaration add the following line: ``` public float speed = 10 * Time.deltaTime;```

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Cleanup.png" alt="" style="width: 100%;"/>

Now we can easily condense our movement code so it is easier to read.

```cs
transform.Translate(Input.GetAxis("Horizontal") * speed, 0, speed * Input.GetAxis("Vertical"));

//Notice how I can put speed on either
//side of our input. It doesn't matter.
```
The property will also appear in our unity editor.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Property.png" alt="" style="width: 100%;"/>

#### Another Axis: Simple Jumping

At the end of last week I asked you to try and create a jump using what you'd learnt in the previous session. The solution was adding ```Input.GetAxis("Jump") * Time.deltaTime``` to the Y-value parameter of your Movement function.


#### Using Position as a variable: Create a safety net

Right now if your object goes off the side of the map it will spiral forever into the infinite void.

First things first, you want a way to access your values. For instance, let's store our object's Y Value in a variable like so ```float ypos = transform.position.y;```.

Then, using our knowledge of if statements, we want to make a condition in our *update* method that detects if ```ypos``` has gone below the height of our terrain. In case you've forgotten, C# If statements use curly braces like so:

``` cs
if (condition) {
	//Your code
}
```

Once you've made this condition, you'll want to over wright your object's current position in order to teleport it somewhere safe.

```c
Vector3 temp = new Vector3(x, y, z);
this.transform.position = temp;
```

A Vector3 is a special Datatype to represent 3D space. Set the x,y,z set to coordinates somewhere on your map, and then try walk off the edge to see if it works.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Teleport.gif" alt="" style="width: 100%;"/>

#### Mapping Mouse to look around

We want to map a *very basic* rotation to your mouse so that you can see the X,Y,Z movement of your object is relative to your current position, and not fixed to a grid. You'll need this function: ```transform.Rotate(X,Y,Z,0);```, which behaves very similarly to the Translate function you've used that far. Map the Y variable to the input for the "Mouse X" axis similar to before, and see what happens.


#### Finished this?

The Unity Courseware videos has a section on PlayerMovement. If you've download the Zombie Toys assets, check out their script in the Project Menu under ```Assets -> Scripts -> Player -> PlayerMovement.cs```.
