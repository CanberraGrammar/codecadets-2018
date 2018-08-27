Sample solutions to the Projectile Attack labs.

> Attack.cs

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

> Projectile.cs

```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Projectile : MonoBehaviour {

    public GameObject SPFX;

    void OnTriggerEnter(Collider other){
        if ((other.gameObject.name == "Cube") || (other.gameObject.name == "Terrain"))
        {
         //Do nothing
        }
        else {
            print(other);
            Destroy(gameObject);
            Instantiate(SPFX, transform.position, transform.rotation);
            Destroy(other);
        }
    }
}
```

> Damage.cs

<font color="red">Not implemented yet</font>
