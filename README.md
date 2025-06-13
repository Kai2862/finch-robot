# finch-robot

### Development Checklist

| Completed | Task         | Description |
|:---------:| :-----------:|:------------|
|    ✅     | Familiarize  | Learn how to: <ul><li>Connect to the robot</li><li>Interpret what built-in sensors detect</li><li>Program basics in SNAP!</li><li>Setup local developing environment to code in Java</li></ul>|
|    ✅     | 3D Design    |             |
|    ❌     | Develop Code |             |

---

<details>
<summary><strong>Inspiration for the Project</strong></summary>

I wanted to serve people **Oreos** as a prize for participating!
</details>

---

### Design Cycle
<img src="design_cycle.png" alt="design cycle" width="300" height="300">

###### The process when designing the golf puck included:
- Getting dimentions and measurements of the robot.
- Creating a joint system that moves in one direction.
- Attatching the joint the arm system and creating a base for the puck.
- The joint that I chose needed 3 parts: 2 parts attatched by an attatchment that would be glued onto a flat piece serving as an ancor.
- laying the design flat for minimal redundency when printing

---

### Code to Highlight
```java
public static void followLine(Finch f) {
	int left = f.getLine("L");
	int right = f.getLine("R");
	
	System.out.println("left: " + left + " right: " + right);
	if (left < 90) {
		f.setMotors(0, 10);
	} else if (right > 90) {
		f.setMotors(10, 0);
	} else {
		f.setMotors(10, 10);
	}
	f.pause(.1);
}
```

---

### The upbringing of the putter
- Original ideas involved a dart game. That felt too little user interaction and too much human interaction. A golf puck was far more innovative and Mr. Hans gave me the green light.

- From this project I brainstomed ways to create the joint of this design which deemed to be a challenge. I settled with a design that only moved in one direction so it's more about the position of the robot instead of steadiness of human tampering.

- The idea itself is as generic as it gets. Subsequent to previewing inspirations a puck that moves back and forth is way more desirable than pushing a ball simply with the speed of the robot; the robot mad slow. That is where I came up with the idea with the joint that extends out of the hole in the robot that extends to the front of the robot given the joint that is mean't to serve as the putter subsequent to the robot's ultimate stop.
