This script will move an object naturally side to side. It has 3 public parameters.

* degreesPerSecond : This is the speed of travel as a Float.

* amplitude : This is the distance it travels.

* frequency : This is the time it takes to turn around.

This variant works in the X axis.

```c#

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class SideToSide : MonoBehaviour
{


    public float degreesPerSecond = 15.0f;
    public float amplitude = 0.5f;
    public float frequency = 1f;

    // Position Storage Variables
    Vector3 posOffset = new Vector3();
    Vector3 Pos = new Vector3();

    // Use this for initialization
    void Start()
    {
        // Store the starting position & rotation of the object
        posOffset = transform.position;
    }

    // Update is called once per frame
    void Update()
    {
        // Spin object around Y-Axis
        //transform.Rotate(new Vector3(Time.deltaTime * degreesPerSecond, 0f, 0f), Space.World);

        // Float up/down with a Sin()
        Pos = posOffset;
        Pos.x += Mathf.Sin(Time.fixedTime * Mathf.PI * frequency) * amplitude;

        transform.position = Pos;
    }


}
```

To make it work in the Y or Z axes, change ```Pos.x += Mathf.Sin(Time.fixedTime * Mathf.PI * frequency) * amplitude;``` to Pos.y or Pos.z
