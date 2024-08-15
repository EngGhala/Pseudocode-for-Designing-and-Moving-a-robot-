# Pseudocode-for-Designing-and-Moving-a-robot-
The robot has 4 servo motors, can move forward and stop when facing obstacles.

Pseudocode:
1. Design of the Legs
    * Leg Structure:
        * Each leg has two joints: a hip joint (controlled by hipServo) and a knee joint (controlled by kneeServo).
        * The legs are designed with a foot that helps stabilize the robot during movement.
    * Range of Motion:
        * The hip joint allows the leg to move forward and backward.
        * The knee joint allows the leg to bend and straighten, enabling the robot to lift and lower the leg.
    * Servo Mounting:
        * Servos are mounted in such a way that they can efficiently control the movement of the hip and knee joints.
    * Balance and Stability:
        * The design ensures that the robot maintains balance when one leg is lifted, with a stable center of gravity.
2. Initialize Components
    * Set up four servos: hipServo1, kneeServo1, hipServo2, kneeServo2.
    * Set up a distance sensor to detect obstacles.
3. Setup Function
    * Attach hipServo1 to hipServo1Pin.
    * Attach kneeServo1 to kneeServo1Pin.
    * Attach hipServo2 to hipServo2Pin.
    * Attach kneeServo2 to kneeServo2Pin.
    * Initialize the distance sensor.
    * Set initial positions of all servos to a neutral (middle) position (90 degrees).
4. Loop Function (Repeat Continuously)
    * Check for Obstacle
        * Use the distance sensor to check if an obstacle is within a certain distance in front of the robot.
        * If an obstacle is detected:
            * Stop all movement to prevent collision.
            * Wait until the obstacle is cleared.
        * If no obstacle is detected:
            * Proceed to the movement steps below.
    * Movement Steps:
        * Step 1: Lift Leg 1:
            * Bend kneeServo1 to lift Leg 1, ensuring the foot clears the ground.
            * Maintain balance by ensuring the robot's center of gravity stays within its base.
            * Wait for 500 milliseconds.
        * Step 2: Move Leg 1 Forward:
            * Rotate hipServo1 to move Leg 1 forward, simulating a walking motion.
            * Wait for 500 milliseconds.
        * Step 3: Place Leg 1 Down:
            * Straighten kneeServo1 to place Leg 1 down, ensuring the foot lands flat on the ground.
            * Wait for 500 milliseconds.
        * Step 4: Lift Leg 2:
            * Bend kneeServo2 to lift Leg 2, ensuring it lifts similarly to Leg 1.
            * Wait for 500 milliseconds.
        * Step 5: Move Leg 2 Forward:
            * Rotate hipServo2 to move Leg 2 forward.
            * Wait for 500 milliseconds.
        * Step 6: Place Leg 2 Down:
            * Straighten kneeServo2 to place Leg 2 down.
            * Wait for 500 milliseconds.
    * Reset Position:
        * Return hipServo1 and hipServo2 to the neutral (starting) position.
        * Ensure the robot is balanced and stable before proceeding.
        * Wait for 1 second before repeating the steps.

Additional Notes:
* Leg Design Considerations:
    * Foot Shape and Size: Designed to provide enough surface area to keep the robot stable during movement.
    * Joint Flexibility: The hip and knee joints are designed with enough range of motion to allow the robot to walk smoothly while maintaining balance.
    * Weight Distribution: The servos and legs are designed to distribute the robot’s weight evenly, minimizing the risk of tipping over.
* Obstacle Detection and Movement:
    * The robot stops when an obstacle is detected and resumes walking once the path is clear, all while maintaining stability thanks to the well-designed legs.
