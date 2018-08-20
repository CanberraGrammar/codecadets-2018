---

title: Interaction as simple AI

---


### Courseware link


## [http://unity.codecadets.com](http://unity.codecadets.com)

### The goal : Create a basic AI using scripts

* Using your previous script, control multiple objects.

* Using scripts to make objects act on their own.

* Create an object that follows the player


### Scripting multiple Objects in Tandem

> Using your movement scripts from Weeks 1-2

Create a new object in your Game world next to your controllable object from before.

Your code has no specific binding to any one object, and will respond for any number of objects attached to it.

**Copy paste your controllable object, or create a new and different object and attach your movement script to it.**  Observe its behaviour.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Army.gif" alt="" style="width: 100%;"/>


### Autonomous actions

Create a new object to serve as your Non-Player Character (NPC). Give it a collider and a new script.

<font color="red">You CAN give it Rigidbody if you want, but if your map isn't very flat this could get messy.</font><br/>


From the original movement script you might recall that an object can move on its own. You might recall using this function *without* the Input.GetAxis() function.

```cs
transform.Translate(x,y,z);
```

Start from here, using your simple movement as a basis for Time.deltaTime and speed properties if you can.


### Hunt you down

Using a public property like before, create a target GameObject.

```cs
Vector3 pos = target.transform.position - transform.position;
pos = pos.normalized;
transform.Translate(pos.x * Time.deltaTime * speed, pos.y * Time.deltaTime * speed, pos.z * Time.deltaTime * speed);
```

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Enemy.gif" alt="" style="width: 100%;"/>

### Using existing functions

However, we've implemented this ourselves using math. Unity has a simple function

```cs
transform.position = Vector3.MoveTowards(transform.position, target.transform.position, step);
```

The three parameters are:

* transform.position - as in the position of this object.

* target.transform.position - the destination which is the position of the target you passed in.

* step - which is the movement speed, so perhaps ```speed * Time.deltaTime``` or similar constant.

### Simple Hostility

We can really easily make use of this simple AI to act as the basis of a typical video game enemy.  

Using the same logic for ```OnTriggerEnter``` from the Teleporter exercise, create some code to recognise when the controllable player object enters your enemy object. Then, you can add the following line to "kill" your player.

```cs
Destroy(other);
```

OR, you can choose to self destruct the object on impact.

```cs
Destroy(gameObject);
```

Let your pursuing object run into you and see what happens next.

### Extended Compatibility

This was a relatively short lab compared to the last two; if you've finished this add Compatibility to use your teleporters to your enemy object. 


----

### Appendix:

To avoid potentialconfusion, there are two uses of gameObject and GameObject

| Type | Description|
| :---:| :---|
| gameObject | A SELF reference. When called, it refers to the object this script is attached to specifically. |
| GameObject | The DATATYPE of a unity object. Used to hold reference to other GameObjects in the world. |
