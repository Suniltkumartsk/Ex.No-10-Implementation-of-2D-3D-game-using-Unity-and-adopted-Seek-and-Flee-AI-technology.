# Ex.No: 10  Implementation of 2D/3D game using Unity and adopted Seek and Flee AI technology.
### DATE: 28-05-26                                                                     
### REGISTER NUMBER : 212223240164
### AIM: 
To develop a game Seek and flee with cop & robber in Unity 
### Algorithm:
```
1. Create a new Unity 3D project.
2. Add two game objects:
   - Cop
   - Robber
3. Assign movement scripts to both objects.
4. Implement Seek behavior for the Cop.
5. The Cop continuously moves toward the Robber.
6. Implement Flee behavior for the Robber.
7. The Robber continuously moves away from the Cop.
8. Update positions every frame using Vector calculations.
9. Run the scene to simulate chasing and escaping behavior.
```  
### Program:
```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class seekScript : MonoBehaviour
{
    // Start is called before the first frame update
    public Transform target;  // The object to seek
    public float speed = 5f;  // Movement speed
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        if (target == null) return;  // Exit if no target is assigned

        // Calculate the desired direction
        Vector3 direction = (target.position - transform.position).normalized;

        // Move the object towards the target
        transform.position += direction * speed * Time.deltaTime;
    }
}
```
```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class fleeScript : MonoBehaviour
{
    // Start is called before the first frame update
    public Transform target;  // The object to seek
    public float speed = 5f;  // Movement speed
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        if (target == null) return;  // Exit if no target is assigned

        // Calculate the desired direction
        Vector3 direction = (transform.position-target.position).normalized;

        // Move the object towards the target
        transform.position += direction * speed * Time.deltaTime;
    }
}
```
### Output:
### Before:
<img width="1918" height="1077" alt="image" src="https://github.com/user-attachments/assets/e1820abb-1a8c-4578-a07a-ac45bea6f2f7" />

### After:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/05f5e8ab-f029-4ae2-b29f-aeb3dcac2960" />


### Result:
Thus the game was developed using Unity and adopted Seek and Flee AI technology.
