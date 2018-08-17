---

title: Scripts to create and destroy objects

---


### Courseware link


## [http://unity.codecadets.com](http://unity.codecadets.com)

### The goal : Create a simple projectile attack system



## Create a new Object to be your projectile

I personally recommend a sphere. Scale it to an appropriate size.

> GameObject -> 3D Object -> Sphere

For the purposes of this tutorial, we will be making a physical missile object, similar to a torpedo or bullet. However, I will leave some instructions on how to instead make it use the particle system, and act more like, say, a fireball, at the bottom of the lab.


* Make the object a pre-fab, this makes it easier to instantiate.


* Create new Script on your controllable, called it Attack or something along those lines.

```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Attack : MonoBehaviour {

    public GameObject projectile;
    public float speed;

	private void Update()
	{
        if (Input.GetKeyDown(KeyCode.G))
        {
            print("FIRE!");
            GameObject missile = Instantiate(projectile, gameObject.transform.position, Quaternion.identity) as GameObject;
            Rigidbody rb = missile.GetComponent<Rigidbody>();
            rb.velocity = transform.forward * speed;
        }
	}
}

```

* Add new script to projectile prefab. Call it Projectile.

* Add an OnTriggerEnter method. Destroy self and instantiate explosion



----

## The Unity Particle system

* Turn off Mesh Render

* Right Click the object and add a Particle system

* Customise.
