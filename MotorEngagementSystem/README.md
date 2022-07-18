Designed a mechanism for a nuclear reactor. Designed the motor engagement system that pushes the control rods in / out of the nuclear reactor based on safety systems.

An input pin called "DIRECTION" will be 1 if the control rods are directed to be inserted and 0 if the control rods are directed to be removed. Furthermore, an input pin called "GO" will be the command for your circuit to drive the motors. This pin is a momentary 1, meaning that if the controller wants your circuit to move the rods, the GO pin will go from 0 to 1 then back to 0.

Created a circuit, including an FSM, that takes the direction input and turns on the appropriate motor to guide the control rods either into or out of the nuclear reactor. There are two other input pins, one called TOP and one called BOTTOM. These are microswitches that allow your circuit to detect if the control rods are fully inserted (BOTTOM=1) or fully retracted (TOP=1). If the control rods are in transit, both TOP and BOTTOM will be 0.

Made sure to drive the motor (MOTOR_DOWN or MOTOR_UP) exclusively in the up or down position. It's important to never have MOTOR_DOWN and MOTOR_UP = 1 at the same time.

Finally, an input pin called ESTOP (emergency stop) can be pressed to reset MOTOR_DOWN and MOTOR_UP back to 0. ESTOP is much like the GO pin in that it is momentarily actuated. The ESTOP pin must take priority over the GO pin. So, if both are actuated simultaneously, GO must be ignored.
