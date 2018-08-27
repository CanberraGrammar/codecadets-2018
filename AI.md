A sample solution to the Week 5 AI basis tutorial.


```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Enemy : MonoBehaviour {

    public int speed;
    public GameObject player;

    void Update()
    {
        Vector3 localPosition = player.transform.position - transform.position;
        localPosition = localPosition.normalized; // The normalized direction in LOCAL space
        transform.Translate(localPosition.x * Time.deltaTime * speed, localPosition.y * Time.deltaTime * speed, localPosition.z * Time.deltaTime * speed);
        Vector3 newDir = Vector3.RotateTowards(transform.forward, localPosition, speed * Time.deltaTime, 0.0f);
        //Debug.DrawRay(transform.position, newDir, Color.red);
        transform.rotation = Quaternion.LookRotation(newDir);
    }

	private void OnTriggerEnter(Collider other)
	{
        Destroy(gameObject);
	}
}
```
