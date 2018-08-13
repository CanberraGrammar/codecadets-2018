Here is a copy of an example solution to the Week 1/2 Lab:

```cs

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

//Note if your file is a different name
//the class must be the same name/
public class SimpleMove : MonoBehaviour {

  //A public speed value allows for changing in Unity
  public float speedfactor;

	void Start () {}    
	}

	// Update is called once per frame
	void Update () {
        //Multiply our speed factor by Deltatime
        float speed = speedfactor * Time.deltaTime;

        //The code that moves an object
        transform.Translate(Input.GetAxis("Horizontal") * speed, Input.GetAxis("Jump") * speed, speed * Input.GetAxis("Vertical") );

        //Get the Y position of our Object
        float ypos = transform.position.y;

        //If y is less than -1
        if (ypos < -1){
            //Create a new location
            Vector3 temp = new Vector3(1, 1, 1);
            //Set our object's position to that location
            this.transform.position = temp;
        }
	}
}
```
