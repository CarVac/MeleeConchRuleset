# Definitions

Input: A device that measures or detects movements/force from a user's body used to influence the Output

Actuator: A part of an Input that a user interacts with in order to change the value read by that Input

Output: A value sent from the controller to the game console

Analog Output: Analog stick X and Y axes, C-stick X and Y axes, L and R analog

Digital Output: A, B, X, Y, L digital, R digital, D-pad up/down/left/right, and Start

Trigger: L or R

Analog Trigger Output: L or R Analog Outputs

Digital Trigger Output: L or R Digital Outputs

Analog Input: Any Input device that measures a smoothly-changing value roughly proportional to a physical position or applied force

Half-Range Analog Input (HRAI): any Analog Input device with a default output at the extreme end of its range

Digitized Half-Range Analog Input (DHRAI): an intermediate digital value activated when a HRAI's value exceeds a constant rising-edge threshold and deactivated when it drops below a constant falling-edge threshold

Full-Range Analog Input: any Analog Input device with a default output not at either end of its range

Nonreturning Analog Input: any Analog Input device that does not automatically return to a default output

Digital Input: Any Input device that produces exactly two possible values according to a physical position or applied force

Combined Analog Digital Input (CADI): An Analog Input device which over the course of its travel activates an electrically distinct Digital Input (ex. GCC triggers)

Emulated Combined Analog Digital Input (Emulated CADI): A HRAI acting simultaneously as a HRAI and a DHRAI so as to emulate the behavior of a CADI

Modifier Input: Any Digital Input or Digitized HRAI that, when actuated in combination with other Inputs, changes the behavior of an Analog Output or a Digital Trigger Output

Dedicated Modifier Input: Any Modifier Input that influences no Outputs when actuated alone or in concert with other Dedicated Modifiers

Influence: to be one of the inputs used by the controller to determine the state of an Output

# General

## Enforcement

TOs may inspect any controller at any time.
If a player suspects their opponent's controller is not abiding by these rules, they may request a controller inspection by TOs.
The TO is not required to abide by this request.
If TOs are unable to determine that a controller is in full compliance, that controller may be banned at the TOs' sole discretion. 
If a game or match cannot be played out in full due to a controller malfunction which cannot be fixed in a timely manner, and the player using the controller does not have a replacement controller readily available, the player may be disqualified at the sole discretion of TOs.

## Communications

All communication between the controller and console must be either via wires or a wireless protocol that prevents interference.

## Input Layout

Generally, any layout of Inputs is permitted.

Aside from Combined Analog Digital Inputs (CADI), Emulated CADI, and orthogonal axes of a control stick Analog Input, Inputs must not share Actuators in a way that makes it difficult or impossible to actuate one without actuating another.

Inputs must not have two separate Actuators that both influence the value read by that Input. For example, you may not tie a string to an analog stick in order to move it using a different finger.

## Configuration

These rules do not apply during a configuration mode which is not permitted for use during gameplay.

# Digital Outputs

Digital Outputs consist of A, B, X, Y, Z, L digital, R digital, the four D-pad directions, and Start.

If any Input influences A, X, Y, Z, D-pad directions, or Start Outputs, then it may not influence any other Output.

If any Input influences B, L Digital, or R Digital Outputs, it may only influence other outputs as a Modifier Input.

Each Digital Output may be influenced by no more than one Input of any type.
The first exception is that Z may be influenced by up to two Inputs.
The other exception to this is that L Digital and R Digital Outputs may have the Digital Outputs disabled by a Dedicated Modifier Input that modifies the Digital Input or DHRAI to output only a fixed Analog Trigger Output for the corresponding Trigger.

Digital Outputs must be off in their default states regardless of what type of Input influences each one.

Each Digital Output must not have any delayed response to any change in the state of any Input that influences it.

## Digital Input, Digital Output

WHAT ABOUT MODIFIERS

## Analog Input, Digital Output

The only type of Analog Input permitted to influence a Digital Output is a Digitized Half-Range Analog Input (DHRAI) such as the slider in GCC triggers, position-sensing analog keyboard switches, or force-sensitive buttons.

If a DHRAI is used as a Modifier for an Analog Output as well as the primary influence on a Digital Output, the DHRAI thresholds must be the same for both.

If a Half-Range Analog Input used to influence a Digital Output is part of a Combined Analog Digital Input, the Digital Input part of the CADI must not influence any Outputs.

# Analog Outputs

## Analog Stick Outputs

### Analog Precision

Any Full-Rage Analog Inputs used to influence the Analog Stick Outputs must have a resolution of at least 256 digital readout levels over the Input range.

Any Half-Range Analog Inputs used to influence the Analog Stick Outputs must have a resolution of at least 128 digital readout levels over the Input range.

### Both

#### Analog Input, Analog Stick Outputs

#### Digital Input, Analog Stick Outputs

The following Analog Stick coordinates must not be accessible using Digital Inputs:

1. Cardinal/Quadrant Boundaries: X or Y ±0.2875 and ±0.3000 must not be accessible. Explanation: these represent the two values in each axis that separate cardinals from quadrants, which enable a variety of techniques such as the steepest/shallowest angles, "middle-tilted" tilts and smash attacks, tap jump short hop with the stick outside the deadzone, and double jumping backwards with Yoshi, Jigglypuff, and Kirby without turning around.
2. Shield Drop Down: Y = -0.6625, -0.6750, and -0.6875 must not be accessible while |X| < 0.7000.
3. Directional Airdodge Angles: While either Digital L or Digital R outputs are active, all output coordinates must meet one of the following three criteria:
  * 22.96° < atan(|Y/X|) < 67.04° (within the permissible angle range) (NOTE: This was 23-67 in the SWT ruleset, but b0xx firefox angles are 22.96377... degrees; b0xx uses 30.46554... degree wavedash angles)
  * |X| < 0.2875 (within the X deadzone)
  * |Y| < 0.2875 (within the Y deadzone)
4. Ice Climbers Desyncs:
  * Analog Stick
    * X = ±0.8000: Popo Smash/Nana Tilt
    * Y = ±0.6625: Popo Smash/Nana Tilt
    * X = ±0.7000: Popo Roll
    * Y = -0.7000: Popo Spotdodge/Nana Shield Drop (TODO: is this important for the SWT ruleset given that UCF will make both shield drop?)
    * X = +0.6250: Popo Run/Nana Runbrake
    * X = +0.7500: Popo Teeter Break/Nana Teeter
    * Y = +0.5625: Popo Jump out of Dash
    * |X| <= 0.5875, Y = -0.5500: Grounded Nana Neutral-B, Popo Up/Down-B
    * X = +0.5250, Y = +0.6250: two different aerials (TODO: positive X only?)
    * X = -0.4375, Y = +0.5250: two different aerials (TODO: negative X only?)
  * C-Stick
    * X = ±0.8000: Popo Smash
    * Y = ±0.6625: Popo Smash
    * X = ±0.7000: Popo Roll
    * X = -0.7000: Popo Spotdodge
    * Y = +0.6625: Popo Jump out of Shield
    * X = +0.5250, Y = +0.6250: two different aerials (TODO: positive X only?)
    * X = -0.4375, Y = +0.5250: two different aerials (TODO: negative X only?)
5. 2-Frame Turnaround Uptilt and Downtilt: All output coordinates must meet one of the following three criteria:
  * atan(|Y/X|) <= 50° (forward tilt instead of uptilt/downtilt)
  * |Y| >= 0.6625 (produce a tap jump)
  * |X| < 0.2875 (within the X deadzone)
6. Pikachu/Pichu Double Up-B: The following four coordinates, which allow Pikachu and Pichu to move twice in the same direction during an Up-B, must not be accessible:
  * X = ±0.5000, Y = 0
  * X = 0,       Y = ±0.5000
  * X = ±0.4000, Y = ±0.3000
  * X = ±0.3000, Y = ±0.4000

### Control Stick

…it should be permissible to greatly stretch the output of input regions that originally existed fully in the melee deadzone, to handle worn firefox notches.

### C-Stick

## Analog Trigger Outputs

### General Analog Trigger Information

The Analog Trigger Outputs sent by the controller exist in a range from 0 to 255, but Melee caps the accepted value at 140.

Values 43 and greater produce an analog shield in Melee.

When Z is held, the resulting lightshield is equivalent to the lightshield from an Analog Trigger Output of 49.

### Analog Trigger General Rules

If either Analog Trigger Output is influenced by Digital Inputs, both Analog Trigger Outputs must be influenced solely by Digital Inputs, or by Digitized Half-Range Analog Inputs.

### Analog Input, Analog Trigger Output

The Analog Trigger outputs may be influenced only by Half-Range Analog Inputs.

The default Output must be 0.

Any Analog Inputs used to influence the Analog Trigger Outputs must have a resolution of at least 64 digital readout levels over the Input range.

The Analog Input controlling an Analog Trigger Output may be the analog part of a CADI or Emulated CADI but if the digital part of the CADI is used it must Influence only the same trigger's Digital Output.

yoshi mode okay? limit to 49 (z-lightshield)

The relation between the Analog Trigger Input and the Analog Trigger Output must be linear from 0 to 49.

The mapping between the value read by the Input and the Analog Trigger Output must be a static relation.

### Digital Input, Analog Trigger Output

Each Analog Trigger Output may be influenced by at most a single standalone Digital Input, or a Modifier Input combined with the Digital Input corresponding to the same trigger's Digital Output.

The Analog Trigger Output value must default to 0.

The Analog Trigger Output value when influenced by Digital Inputs must not be from 43 to 48 inclusive.

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
