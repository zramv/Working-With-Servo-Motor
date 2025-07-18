# Working With Servo Motor
This project demonstrates basic control of four servo motors using an Arduino.  
At startup, all servos perform a sweep motion — moving back and forth — for 2 seconds.  
After the initial movement, all servos hold a fixed position at 90 degrees.<br><br>
## Circuit
<p align="center">
<img width="686" height="370" alt="Screenshot 2025-07-18 151533" src="https://github.com/user-attachments/assets/6e3085b7-bc3f-4047-931c-f63fc7b975ca" />
<br><br>
</p>

## Test Video

https://github.com/user-attachments/assets/7c80b96b-a57c-41e3-bc10-47463b4a57b8.mp4

<br><br>
## Step-by-Step Walking Motion (with Servo Angles)
The walking motion is executed using four servo motors that control the hips and knees of a humanoid robot.
two for the hips and two for the knees (left and right). The walking behavior follows a repeated pattern of shifting weight and stepping forward, creating a looped movement.

### How It Works

1. **Idle Position**  
   All servos are set to 90°, representing a standing neutral position.

2. **Right Leg Step**  
   - Shift weight to the **left leg** by:
     - Setting **left hip** to 120° (leans body left).
     - Setting **right hip** to 60° (raises right leg).
   - Keep both knees at 90° for balance.

3. **Return to Center**  
   - Bring both hips back to 90°.
   - Set **left knee** to 120° (lowers body slightly).
   - Keep **right knee** at 90° (right leg straightened after step).

4. **Left Leg Step** (opposite of Step 2)  
   - Shift weight to the **right leg** by:
     - Setting **right hip** to 120°.
     - Setting **left hip** to 60°.
   - Knees at 90°.

5. **Return to Center Again**  
   - Both hips at 90°.
   - **Right knee** = 120°, **left knee** = 90°.

6. **Repeat steps 2–5** for continuous walking.

### Angle Reference Table

| Step                | Left Hip | Right Hip | Left Knee | Right Knee |
|---------------------|----------|-----------|-----------|------------|
| Idle                |   90°    |    90°    |   90°     |    90°     |
| Step with Right Leg |  120°    |    60°    |   90°     |    90°     |
| Center After Step   |   90°    |    90°    |  120°     |    90°     |
| Step with Left Leg  |   60°    |   120°    |   90°     |    90°     |
| Center After Step   |   90°    |    90°    |   90°     |   120°     |


