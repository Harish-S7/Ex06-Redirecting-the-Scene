# Ex06-Redirecting-the-Scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1: To open the unity engine.

Step 2: Create a new 3D project.

Step 3: Create plane and name it as ground and create cube and name it as player.

Step 4: Add WinText in Hierarchy.

Step 5: Create a C# Script and name it as playercontroller and add the script to player.

Step 6: Use the R button to change the level2.

Step 7 Print the Output and end the program.

## Program:
## DEVELOPED BY : PAVITRA .J
## REG NO : 212224110043
```
using UnityEngine;
using UnityEngine.SceneManagement;

public class Coding : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("level2");
        }

    }
    private void OnTriggerEnter(Collider other)
    {
        if (other.gameObject.tag == "Cube")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}
```

## Output:
![image](https://github.com/user-attachments/assets/b7fec9f1-1939-4f09-8445-584a02680016)
![image](https://github.com/user-attachments/assets/459b0f24-5262-4e3a-8e9b-0f31687909ec)
![image](https://github.com/user-attachments/assets/b9811b46-1237-440d-b10d-175518e46c29)


## Result:
The above C# coding is successfully redirecting the scene in the unity engine.
