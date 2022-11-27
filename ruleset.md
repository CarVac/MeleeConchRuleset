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

Nonreturning Analog Input: any Analog Input device that does not automatically return to a default output (ex. physical volume slider)

Two-Axis Analog Input: any Analog Input device which consists of two independently-controllable Full-Range Analog Inputs that share an Actuator (ex. analog stick)

Digital Input: Any Input device that produces exactly two possible values according to a physical position or applied force (ex. button)

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

These rules do not apply during any configuration mode that uses the controller outputs to display settings.

Any such configuration modes are not permitted for use during gameplay.

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

Modifiers may only influence Digital Outputs on triggers in the case that the modifier disables the Digital Input or DHRAI to output only a fixed Analog Trigger Output for the corresponding Trigger.

## Analog Input, Digital Output

The only type of Analog Input permitted to influence a Digital Output is a Digitized Half-Range Analog Input (DHRAI) such as the slider in GCC triggers, position-sensing analog keyboard switches, or force-sensitive buttons.

If a DHRAI is used as a Modifier for an Analog Output as well as the primary influence on a Digital Output, the DHRAI thresholds must be the same for both.

If a Half-Range Analog Input used to influence a Digital Output is part of a Combined Analog Digital Input, the Digital Input part of the CADI must not influence any Outputs.

# Analog Outputs

## Analog Stick Outputs

Each Analog Stick Output may be influenced only by one of the following choices:

1. One Two-Axis Analog Input
2. Two Full-Range Analog Inputs, one for each Analog Stick Output axis.
3. Four Half-Range Analog Inputs, with two influencing each direction.
4. Four Digital Inputs or DHRAI, optionally with additional Modifiers.

Pairs of Half-Range Analog Inputs (HRAI), each used to influence one Analog Stick Output axis, must use average SOCD with one HRAI mapped to the range from (<=-1 to 0) and one ranging from (0 to >=1).

Analog Inputs may not be used together with Digital Inputs for any given Analog Stick, even for different axes, but one Analog Stick may be fully analog while the other is fully digital.

### Analog Input Precision and Linearization

Any Full-Rage Analog Inputs used to influence the Analog Stick Outputs must have a resolution of at least 256 digital readout levels over the Input range.

Any Half-Range Analog Inputs used to influence the Analog Stick Outputs must have a resolution of at least 128 digital readout levels over the Input range.

If and only if the relation between the motion of an Analog Input's Actuator and the value it measures is nonlinear, the value must be linearized before being presented to the console as an Analog Output.
This linearization must be a static mapping.
For example, a stick with its position read by a Hall Effect sensor must have linearization performed, while a linear potentiometer must *not* have linearization performed.

As an exception to the linearization rule, OEM first-party or second-party controllers that have developed nonlinearity in potentiometers are not required to have their output linearized (due to the inability to do so).

### Analog Input, Analog Stick Outputs

Remapping Distance Restriction: Aside from duplicating global coordinate shifts equivalent to initializing an OEM controller with an off-center stick, no input coordinate, after linearization, may be mapped to an output coordinate more than 18 Melee coordinate units away in a tangential direction, or more than 2 Melee coordinate units away in a radial direction, after applying normalization to fit within the 80-unit radius circle.
Any such coordinate remapping must be static.
This restriction exists to prevent modifications of the coordinate grid that make the game easier to play, while allowing adjustments to notches so that they may perform their intended function even when they are physically worn down.

Coordinate Snapping/Accessibility Restriction: The region of linearized Input coordinates corresponding to a given Output coordinate must not have its bounding box dimensions differ from the dimensions of the output coordinate by more than 30%, whether stretched or compressed.
This restriction exists to prevent coordinate remapping that makes it easy to pinpoint specific values or that prevents you from ever outputting certain coordinates.

EXCEPTION: Output coordinates that are within 3 units of or entirely contained in the Melee Deadzone may have linearized Input coordinates that are more than 30% smaller bounding box and/or 50% smaller in area than the corresponding Output coordinates.
This exception does not allow a violation of radial remapping distance restrions.
This exception is to allow "rescuing" of heavily worn notches that were originally intended to keep the stick out of the the deadzone.
This is not intended to allow, for example, an across-the-board remapping of deadzone values near Y = +0.2875 to be mapped to Y = +0.2875 to make uptilts easier.

EXCEPTION: Input coordinates outside the Melee unit circle and within the Melee deadzone may have their smaller coordinate axis mapped to 0 even if that violates distance restrictions or if this results in inaccessible output coordinates.
This exception is to allow third-party controllers to make 1.0 magnitude cardinals more accessible with analog sticks.

EXCEPTION: Linearized Input coordinates with |X| <= 5 and |Y| <= 5 may be mapped to the origin.
This exception allows controllers to make the origin initialization more consistent.

Digital Input Filtering: All digital filtering, or processing, of Analog Inputs for a given Analog Stick must completely ignore all other Inputs on the controller.
If the filter output does not correspond directly to the filter input, the output shall be either stationary, moving towards, or accelerating towards the input to the filter.

Filters must be composed of weighted sums of the following values:

* current and one-iteration previous input position in the same axis as the output being processed
* current and one-iteration previous input velocity in the same axis as the output being processed
* current and one-iteration previous intermediate filter values in the same axis as the output being processed
* one-iteration previous filtered output in the axis being processed.

The weights of these terms may be either constant or non-constant.
Non-constant weights may vary according to axisymmetric and otherwise monotonic functions of:

* current input position in the axis being processed
* current input velocity in the axis being processed
* current input acceleration in the axis being processed
* current difference between input position and previous output position
* current input radius away from the origin (the only permitted cross-axis interaction)

A simple windowed median filter is also permitted, despite not meeting the above requirements.

Permitted filters include but are not limited to:
1. Hysteresis
2. Median
3. PhobGCC Smart Snapback Filter
4. PhobGCC Waveshaping
5. Simple low-pass filtering
6. "energy-state tracking low-pass filter" (may need more rule tweaking once we know more about how it's implemented)

Illegal filters include but are not limited to:
1. Timer-based pode emulation
2. Timer-based dashback out of crouch enhancement
3. Timer-based empty pivot enhancement
4. Angle- and timer-based ledgedash enhancement

Filters may be linearly chained so that the output of one is used as the input to the next.

### Digital Input, Analog Stick Outputs

The following Analog Stick coordinates must not be accessible using Digital Inputs for either the Control Stick or the C-Stick

1. Cardinal/Quadrant Boundaries: X or Y ±0.2875 and ±0.3000 must not be accessible. These are on the quadrant boundaries and enable the steepest/shallowest angles, "mid-angle" tilts and smashes, tap jump short hop with the stick outside of the deadzone, and double-jumping backwards with Yoshi/Jigglypuff/Kirby without turning around.

#### Digital Input, Control Stick Output

The following Control Stick coordinates must not be accessible using Digital Inputs:

1. Shield Drop Down: Y = -0.6625, -0.6750, and -0.6875 must not be accessible while |X| < 0.7000.
2. Directional Airdodge Angles: While either Digital L or Digital R outputs are active, all output coordinates must meet one of the following three criteria:
  * 22.96° < atan(|Y/X|) < 67.04° (within the permissible angle range) (NOTE: This was 23-67 in the SWT ruleset, but b0xx firefox angles are 22.96377... degrees; b0xx uses 30.46554... degree wavedash angles)
  * |X| < 0.2875 (within the X deadzone)
  * |Y| < 0.2875 (within the Y deadzone)
3. Ice Climbers Desyncs:
  * X = ±0.8000: Popo Smash/Nana Tilt
  * Y = ±0.6625: Popo Smash/Nana Tilt
  * X = ±0.7000: Popo Roll EXCEPT FOR Y = ±0.7000
  * Y = -0.7000: Popo Spotdodge/Nana Shield Drop EXCEPT FOR X = ±0.7000
  * X = +0.6250: Popo Run/Nana Runbrake
  * X = +0.7500: Popo Teeter Break/Nana Teeter
  * Y = +0.5625: Popo Jump out of Dash
  * |X| <= 0.5875, Y = -0.5500: Grounded Nana Neutral-B, Popo Up/Down-B
  * X = +0.5250, Y = +0.6250: two different aerials
  * X = -0.4375, Y = +0.5250: two different aerials
  * X = ±0.7000, Y = ±0.7125: stronger-than-analog-stick-accessible diagonal DI
  * X = ±0.7125, Y = ±0.7000: stronger-than-analog-stick-accessible diagonal DI
  * X = ±0.6875, Y = ±0.7250: stronger-than-analog-stick-accessible diagonal DI
  * X = ±0.7250, Y = ±0.6875: stronger-than-analog-stick-accessible diagonal DI
  * X = ±0.6750, Y = ±0.7375: stronger-than-analog-stick-accessible diagonal DI
  * X = ±0.7375, Y = ±0.6750: stronger-than-analog-stick-accessible diagonal DI
4. 2-Frame Turnaround Uptilt and Downtilt: All output coordinates must meet one of the following three criteria:
  * atan(|Y/X|) <= 50° (forward tilt instead of uptilt/downtilt)
  * |Y| >= 0.6625 (produce a tap jump)
  * |X| < 0.2875 (within the X deadzone)
5. Pikachu/Pichu Double Up-B: The following four coordinates, which allow Pikachu and Pichu to move twice in the same direction during an Up-B, must not be accessible:
  * X = ±0.5000, Y = 0
  * X = 0,       Y = ±0.5000
  * X = ±0.4000, Y = ±0.3000
  * X = ±0.3000, Y = ±0.4000

#### Digital Input, C-Stick Output

The following C-Stick coordinates must not be accessible using Digital Inputs:

1. Ice Climbers Desyncs:
  * X = ±0.8000: Popo Smash
  * Y = ±0.6625: Popo Smash
  * X = ±0.7000: Popo Roll EXCEPT FOR Y = ±0.7000
  * X = -0.7000: Popo Spotdodge EXCEPT FOR X = ±0.7000 
  * Y = +0.6625: Popo Jump out of Shield
  * X = +0.5250, Y = +0.6250: two different aerials
  * X = -0.4375, Y = +0.5250: two different aerials
  * X = ±0.7000, Y = ±0.7125: stronger-than-analog-stick-accessible diagonal ASDI
  * X = ±0.7125, Y = ±0.7000: stronger-than-analog-stick-accessible diagonal ASDI
  * X = ±0.6875, Y = ±0.7250: stronger-than-analog-stick-accessible diagonal ASDI
  * X = ±0.7250, Y = ±0.6875: stronger-than-analog-stick-accessible diagonal ASDI
  * X = ±0.6750, Y = ±0.7375: stronger-than-analog-stick-accessible diagonal ASDI
  * X = ±0.7375, Y = ±0.6750: stronger-than-analog-stick-accessible diagonal ASDI

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


