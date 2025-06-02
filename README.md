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
## DEVELOPED BY : Harish S
## REG NO : 212224230086
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
![image](https://github.com/user-attachments/assets/72ba02ae-4e90-4c6f-bf2d-ebe219dd9ed7)
![image](https://github.com/user-attachments/assets/ca7deb7c-cf41-4e20-b6ac-956383140f2b)
![image](https://github.com/user-attachments/assets/e0a70008-3b7d-47d7-a78e-31edb919d5a9)




## Result:
The above C# coding is successfully redirecting the scene in the unity engine.
