# Definitions

Input: A device that measures or detects movements/force from a user's body used to influence the Output

Output: A value sent from the controller to the game console

Analog Input: Any Input device that measures a smoothly-changing value roughly proportional to a physical position or applied force

Half-Range Analog Input (HRAI): any Analog Input device with a default output at the extreme end of its range

Full-Range Analog Input: any Analog Input device with a default output not at either end of its range

Nonreturning Analog Input: any Analog Input device that does not automatically return to a default output.

Digital Input: Any Input device that produces exactly two possible values according to a physical position or applied force

Analog Output: Analog stick X and Y axes, C-stick X and Y axes, L and R trigger analog values

Digital Output: A, B, X, Y, L digital, R digital, D-pad up/down/left/right, and Start

Combined Analog Digital Input (CADI): An Analog Input device which over the course of its travel activates an electrically distinct Digital Input (ex. GCC triggers)

# General

## Enforcement

TOs may inspect any controller at any time.
If a player suspects their opponent's controller is not abiding by these rules, they may request a controller inspection by TOs.
The TO is not required to abide by this request.
If TOs are unable to determine that a controller is in full compliance, that controller may be banned at the TOs' sole discretion. 
If a game or match cannot be played out in full due to a controller malfunction which cannot be fixed in a timely manner, and the player using the controller does not have a replacement controller readily available, the player may be disqualified at the sole discretion of TOs.

## Input Layout

Generally, any layout of Inputs is permitted.

Aside from CADI, Inputs must not share actuators in a way that makes it impossible to actuate one without actuating another.

Inputs must not have two separate actuators that produce the same output. For example, you may not tie a string to an analog stick in order to move it using a different finger.

# Digital Outputs

Digital Outputs consist of A, B, X, Y, L digital, R digital, the four D-pad directions, and Start.

Digital Outputs must be off in their default states regardless of what type of Input influences each one.

Each Digital Output may be influenced by no more than one Input of any type.

## Digital Input, Digital Output

Each Digital Input may only influence one Output of any type.

## Analog Input, Digital Output

The only type of Analog Input permitted to influence a Digital Output is a Half-Range Analog Input (HRAI) such as the slider in GCC triggers, analog keyboard switches, or force-sensitive buttons.

Each HRAI may only influence one Digital Output. 

The Digital Output influenced by a HRAI must switch on upon the HRAI increasing above one fixed threshold and switch off upon the HRAI decreasing below another fixed threshold.
The increasing threshold must be greater than or equal to the decreasing threshold.

If a Half-Range Analog Input used to influence a Digital Output is part of a Combined Analog Digital Input, the Digital Input part of the CADI must not influence any Outputs.

# Analog Outputs

## Analog Stick Outputs

### Both

### Control Stick

### C-Stick

## Analog Trigger Outputs

If either Analog Trigger Output is influenced by digital inputs, both Analog Trigger Outputs must be influenced solely by digital inputs.

### Analog Input, Analog Output

yoshi mode okay? limit to 49 (z-lightshield)

### Digital Input, Analog Output

limit to 49 (z-lightshield)

If a Digital Input used to influence an Analog Trigger Output is part of a Combined Analog Digital Input, the Analog Input part of the CADI must not influence any Outputs.




---

this part is old

# Digital Input, Digital Output

Each Digital Input may not influence more than one Digital Output.

If a Digital Output is influenced by one Digital Input, no other Inputs may control it.

# Digital Input, Analog Output

Digital to Analog conversion, henceforth known as DTA, is when an analog output value is influenced by one or more digital inputs.

This includes but is not limited to: 

* All-digital input controllers using nothing but buttons
* GCC triggers modified so that digital press of the trigger is mapped to a fixed analog value
* GCC C-stick digital button-based submodules

## Analog Stick

## C-Stick

## Triggers

# Analog Input, Analog Output

Each Analog Input must not influence more than one Analog Output.

## Stick Outputs

### Full-Range Dual-Axis

Any Analog Input with two orthogonal axes of sensitivity for a single control with its default output not at either end of its range is henceforth referred to as a Full-Range Dual-Axis Analog Input.

(we want to permit stick coordinate remapping, so there needs to be some cross-axis correction but only when the two input axes are on the same Input and the two output axes are on the same control stick)

Example: the control stick and C-stick on a GCC, laptop pointing sticks

### Full-Range Single-Axis

### Half-Range Single-Axis

An Analog Input with its default output at one end of its range is henceforth referred to as a Half-Range Analog Input.

Two Half-Range Analog Inputs may be combined, by taking the difference of their outputs, to influence exactly one Stick Output.

If a Stick Output is influenced by two Half-Range Analog Inputs, no other Inputs

Example: a box controller with analog buttons, a Theremin

### Multitouch

Multitouch panels are not permitted for controlling 

Example: Steam Controller

## Analog Triggers

# Analog Input, Digital Output

An Analog Input may only be used to produce a Digital Output when the Analog Input device has one threshold (hysteresis is permitted) to control one Digital Output.

Each Digital Output may not be controlled by more than one Input.

The Digital Input of a Combined Analog Digital Input must not control any output if its corresponding Analog Input is being used to control a Digital Output.

(this is to prevent a wavedash trigger that jumps on an analog threshold and then digital shields on hard press)
