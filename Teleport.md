A sample solution to the Week 3 and 4 Teleportation Tutorial.

```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Teleporter : MonoBehaviour {

    //Externally linked target teleporter
    public Teleporter target;
    //Globally available cooldown property.
    float cooldown = 0f;

    private void OnTriggerEnter(Collider other)
    {
        //Condition checks cooldown And
        //what the entering object is
        if (other.gameObject.name == "Cube" && cooldown <= 0)
        {
            //Set the Target's Cooldown to disable it
            target.cooldown = 2f;

            //Set the destination to the position of
            //the linked teleporter
            Vector3 destination = target.gameObject.transform.position;
            //Vector3 destination = new Vector3(0, 2, 0);

            //Raise the destination's y value
            // so your object doesn't get stuck inside
            destination.y = destination.y + 2;
            //Set the entering object's position
            //to the destination
            other.gameObject.transform.position = destination;
            //Same for rotation (this is not needed)
            other.gameObject.transform.rotation = target.gameObject.transform.rotation;

        }
    }

	private void Update()
	{
    //Reset THIS teleporter's own cooldown
    //over time.
        if (cooldown > 0){
            cooldown = cooldown - Time.deltaTime;
        }
	}
}



```
