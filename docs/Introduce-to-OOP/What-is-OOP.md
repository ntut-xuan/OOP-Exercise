## What's OOP

### Introduce to OOP

OOP is a principle that have object concept.

- It's kind a blueprint. You can design a object like design a blueprint. (Design a class)
- You can create a object according to the blueprint. (Implement a object)

<img src="../assets/Blueprint-to-computer.png" alt="Computer" style="zoom: 50%;" />

### How do you design a class

In the following image, the blueprint (class) can split into two parts. One is member, and another is function.

- For a member, we have computer name, operating system, CPU model, screen size, it record the state of laptop.

- For a function, we have some function that can boot, control the brightness, or shutdown the laptop. It change the state of laptop.

<img src="../assets/Blueprint-member-and-function.png" alt="Computer" style="zoom:67%;" />

### How do you implement a object

Once we have a blueprint, we can setup some attribute and implement a laptop as a object.

<img src="../assets/Blueprint-to-laptop.png" alt="Computer" style="zoom:67%;" />

### Control the object

When we have a object (that is, laptop), we can control the laptop with function!

<img src="../assets/Laptop-control.png" alt="Computer" style="zoom:67%;" />

### How do we write the code

We can practice the idea with code. It will look like this:

<img src="../assets/Emoji-code.png" alt="Computer" style="zoom:67%;" />

Actually it will look like this:

```cpp
Computer computer = Computer("It's a cool laptop", "16'' screen", true, false, "Doors 11", "Letni i11-48763", 0.88, 0.78);

std::string name = computer.GetName(); // Return "It's a cool laptop" string

computer.setBrightness(0.66); // Set brightness from 78% into 66%

double brightness = computer.GetBrightness(); // Return 0.66 (66%)
```