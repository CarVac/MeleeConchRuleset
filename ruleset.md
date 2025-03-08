# Definitions

Input: A device that measures or detects movements/force from a user's body used to influence the Output

Actuator: The part of an Input that a user can interact with in order to change the value read by that Input

Output: A value sent from the controller to the game console

Analog Output: Analog stick X and Y axes, C-stick X and Y axes, L and R analog

Digital Output: A, B, X, Y, L digital, R digital, D-pad up/down/left/right, and Start

Trigger: L or R

Analog Trigger Output: L or R Analog Outputs

Digital Trigger Output: L or R Digital Outputs

Analog Input: Any Input device that measures a smoothly-changing value roughly proportional to a physical position or applied force

Half-Range Analog Input (HRAI): any Analog Input device with a default output at one end of its range (ex. XBox controller trigger)

Digitized Half-Range Analog Input (DHRAI): an intermediate digital value activated when a HRAI's value exceeds a constant rising-edge threshold and deactivated when it drops below a constant falling-edge threshold

Full-Range Analog Input: any Analog Input device with a default output at the center of its range

Nonreturning Analog Input: any Analog Input device that does not automatically return to a default output when the Actuator is released (ex. physical volume slider)

Two-Axis Analog Input: any Analog Input device which consists of two independently-controllable Full-Range Analog Inputs that share an Actuator (ex. analog stick)

Digital Input: Any Input device that produces exactly two possible values according to a physical position or applied force (ex. button)

Combined Analog Digital Input (CADI): A Half-Range Analog Input device which over the course of its travel activates an electrically distinct Digital Input (ex. GCC trigger)

Emulated Combined Analog Digital Input (Emulated CADI): A HRAI acting simultaneously as a HRAI and a DHRAI so as to emulate the behavior of a CADI

Modifier Input: Any Digital Input or Digitized HRAI that, when actuated in combination with other Inputs, changes the behavior of an Analog Output or a Digital Trigger Output

Dedicated Modifier Input: Any Modifier Input that influences no Outputs when actuated alone or in concert with other Dedicated Modifiers

Influence: to be one of the Inputs used by the controller to determine the state of an Output

# General

## Enforcement

Tournament Organizers may inspect any controller at any time.
If a player suspects their opponent's controller is not abiding by these rules, they may request a controller inspection by TOs.
The TO is not required to abide by this request.
If TOs are unable to determine that a controller is in full compliance, that controller may be banned at the TOs' sole discretion.
If a game or match cannot be played out in full due to a controller malfunction which cannot be fixed in a timely manner, and the player using the controller does not have a replacement controller readily available, the player may be disqualified at the sole discretion of TOs.

All controllers or components for controllers that are not either Nintendo-made or officially licensed Gamecube Controllers must have non-obfuscated source code for all core functionality pertaining to inputs and outputs made available for inspection on request by any party, even if with a proprietary license that does not permit redistribution or modification. (Creative Commons BY-SA-NC-ND recommended)
Non-core controller features that makers wish to remain closed-source must be cleanly isolated from the rest of the code so as to make it impossible to interfere with the core controller function.
(This means that anyone gets to see the code and check for compliance)

If requested by a TO or an opponent, players utilizing a reprogrammable controller must declare the firmware they are using. (This can be used later when inspecting controller inputs from replays)

At a TO's discretion, exceptions may be made to accommodate players with limited dexterity.

## Communications

All communication between the controller and console must be either via wires or a wireless protocol that prevents interference.

It must not be possible to simultaneously connect two controllers to one wireless receiver, or one controller to two wireless receivers. (The Wavebird is not permitted.)

## Input Layout

Generally, any placement of Inputs on the controller is permitted. (Rectangles exist, therefore full button swapping must be legal)

However, the controls may be manipulated by no more than 2 limbs. (No bite buttons, no footpedals, except with TO approval)

Additionally, unless they occupy the same location as the C-Stick below the buttons on the top face akin to a standard Gamecube Controller reachable only by the thumbs, the C-Stick buttons must be arranged around the A button, with C-Up being within 30 degrees of the "up" direction (defined as the direction away from the player's torso along the centerline of the controller), C-Down being within 65 degrees of the "down" direction, and C-Left and C-Right being at least 30 degrees away from the up or down directions. (C-Pad is okay, B0XX is okay, some placement flexibility but limited independence of cstick down input)

Aside from Combined Analog Digital Inputs (CADI), Emulated CADI, and orthogonal axes of a control stick Analog Input, Inputs must not share Actuators in a way that makes it difficult or impossible to actuate one without actuating another. (no physical macros)

Inputs must not have two separate Actuators that both influence the value read by that Input. (no physical duplication of a single electrical button)
Each Actuator must consist of exactly one rigid body, with no surface deflecting by more than 5mm under 100 gram force. (no ASDI-down c-stick string)

## Configuration

These rules do not apply during any configuration mode that uses the controller outputs to display settings.

Any such configuration modes are not permitted for use during gameplay.

# Digital Outputs

Digital Outputs consist of A, B, X, Y, Z, L digital, R digital, the four D-pad directions, and Start.

If any Input influences A, X, Y, Z, D-pad directions, or Start Outputs, then it may not influence any other Output. (limiting rectangle modifiers)

If any Input influences the B Output, it may only influence other outputs as a Non-Dedicated Modifier Input. (limiting rectangle modifiers)

If any Input influences L Digital or R Digital Outputs, it may either simultaneously actuate the corresponding Analog Trigger Output to a fixed value, or it may influence other outputs only as a Modifier Input. (limiting rectangle modifiers)

Each Digital Output may be influenced by no more than one Input of any type. (The Hori GCC is not permitted unless one Z button is disabled. This prevents things like the Optimal Potempkin Controller where duplicate buttons were lined up for frequently used input sequences)
The only exception to this is that L Digital and R Digital Outputs may have the Digital Outputs disabled by a Dedicated Modifier Input that modifies the Digital Input or DHRAI to output only a fixed Analog Trigger Output for the corresponding Trigger. (This allows for R1 B0XX lightshield.)

Digital Outputs must be off in their default states regardless of what type of Input influences each one. (No buttons that must be pressed to turn off an input)

Each Digital Output must not have any delayed response to any change in the state of any Input that influences it. (This rule prohibits macros.)

EXCEPTION: Lockouts and other transfer functions related to Digital Input, Analog Output controls (rectangle nerfs)

EXCEPTION: Start and D-pad inputs may have >1s delayed responses imposed by various means to reduce the likelihood of misinputs.

EXCEPTION: A macro or button combination that simultaneously presses all of Digital L, Digital R, A, and Start is permitted.

## Analog Input, Digital Output

The only type of Analog Input permitted to influence a Digital Output is a Digitized Half-Range Analog Input (DHRAI) such as the slider in GCC triggers, position-sensing analog keyboard switches, or force-sensitive buttons.

If a DHRAI is used as a Modifier Input for an Analog Output as well as the primary influence on a Digital Output, the DHRAI thresholds must be the same for both. (Any digital interpretation of a DHRAI must act identically to a pure Digital Input; there must be no way to have two different thresholds for two digital behaviors.)

If a Half-Range Analog Input used to influence a Digital Output is part of a Combined Analog Digital Input, the Digital Input part of the CADI must not influence any Outputs. (You can't use an analog threshold for a digital output, then use the physical digital part of that input to control something else)

# Analog Outputs

## Analog Stick Outputs

Each Analog Stick Output may be influenced only by one of the following choices:

1. One Two-Axis Analog Input
2. Two Full-Range Analog Inputs, one for each Analog Stick Output axis.
3. Four Half-Range Analog Inputs, with two influencing each direction.
4. Four Digital Inputs or DHRAI, optionally with additional Modifier Inputs.

Pairs of Half-Range Analog Inputs (HRAI), each used to influence one Analog Stick Output axis, must use average SOCD with one HRAI mapped to the range from (<=-1 to 0) and one ranging from (0 to >=1).

Analog Inputs may not be used together with Digital Inputs for any given Analog Stick, even for different axes, but one Analog Stick may be fully analog while the other is fully digital. (No mixing of analog and digital to try to get the best of both worlds)

### Analog Input Precision and Linearization

Any Full-Range Analog Inputs used to influence the Analog Stick Outputs must have a resolution of at least 256 digital readout levels over the Input range. (to prevent skipped values)

Any Half-Range Analog Inputs used to influence the Analog Stick Outputs must have a resolution of at least 128 digital readout levels over the Input range. (to prevent skipped values)

If and only if the relation between the motion of an Analog Input's Actuator and the value it measures is nonlinear, the value must be linearized before being presented to the console as an Analog Stick Output.
This linearization must be a static mapping.
(For example, a stick with its position read by a Hall Effect sensor must have linearization performed, while a linear potentiometer must *not* have (non-)linearization performed.)

As an exception to the linearization rule, OEM first-party or second-party controllers with linear potentiometers that have developed nonlinearity in potentiometers are not required to have their output linearized (due to the inability to do so).

#### Digitized Analog Inputs, C-Stick Outputs

As an exception to the precision and linearization restrictions, two-axis Full-Range Analog Inputs may have the input space segmented into 9 zones (deadzone, 4 cardinals, 4 diagonals) which each output one pinpointed coordinate.
The ranges do not need to correspond to the Melee deadzone sizes.
The ranges must be arranged in the same sequence: the region outputting diagonal up/right must be adjacent to up and right cardinals.
The output coordinates must not change under any circumstances during a match.

The same coordinate restrictions apply as for Digital Input, C-Stick Output.

### Analog Input, Analog Stick Outputs

Scaling Restriction: If the input/output mapping of a two-axis analog input can be calibrated by the user, the resulting calibration must be able to access at least 90 controller units away from the origin but no more than 110 units.

Remapping Restriction: Coordinates may only be remapped by changing their angle from the origin, never their distance.

* Any such angle remapping must be static. (This isn't allowed to change based on any circumstances, whether that be stick inputs or button inputs)
* Angle remappings be piecewise linear and continuous around the circle. (no gaps or overlap)
* The piecewise linear angle remappings must be defined by no more than 16 segments around the circle, each bounded by the 4 cardinals, 4 diagonals, and 8 modder-added notch angles (one between each cardinal and diagonal).
* The angle between a diagonal's output angle and each adjacent cardinal must be stretched by no more than 30% or compressed by no more than 23.1% relative to before remapping.
* The angle between each modder-added notch angle and each adjacent cardinal or diagonal must be stretched by no more than 100% or compressed by no more than 50% relative to before remapping.
* (This restriction exists to prevent modifications of the coordinate grid that make the game easier to play, while allowing adjustments to notches so that they may perform their intended function even when they are physically worn down.)

Exception: Input angle sectors that would be entirely within the Melee deadzone on the rim of the Melee unit circle are permitted to be stretched so that they can reach an angle equivalent to the coordinate 0.3250, 0.9375.
(This exception is to allow "rescuing" of heavily worn notches that were originally intended to keep the stick out of the the deadzone.)
(This is not intended to allow, for example, a remapping of deadzone values not at the rim to be mapped to Y = +0.2875 to make uptilts easier.)

Exception: Input coordinates outside the Melee unit circle and within 6 units of the cardinal may have their smaller coordinate axis mapped to 0 even if that violates other remapping restrictions or if this results in inaccessible output coordinates.
(This exception is to allow third-party controllers to make 1.0 magnitude cardinals more accessible with analog sticks even with older UCF versions)

Exception: Input coordinates outside the Melee unit circle and within the Melee deadzone may have their smaller coordinate axis mapped away from 0 to ±7 even if that violates distance restrictions or if this results in inaccessible output coordinates.
(This exception is to allow third-party controllers to avoid 1.0 magnitude cardinals even on newer UCF versions)

Exception: Linearized Input coordinates with |X| <= 5 and |Y| <= 5 may be mapped to the origin.
(This exception allows controllers to make origin initialization on Dolphin more consistent without affecting gameplay at all.)

Digital Input Filtering:
The Analog Stick Output may be digitally filtered, or processed, to change its response. (For example, to reduce snapback, or make certain techniques easier. We do not limit what can be made easier, but we will limit how it's done.)
All digital filtering of Analog Inputs for a given Analog Stick must completely ignore all other Inputs on the controller. (No using buttons or the other stick to change stick behavior)
If the filter output does not correspond directly to the filter input, the output shall be either stationary, moving towards, or accelerating towards the input to the filter. (No "running ahead" of the stick in anticipation of future motion)

Filters must be composed of weighted sums of the following values: (a limit on how filters may be implemented to prevent overly-smart "macros")

* current and one-iteration previous input position in the same axis as the output being processed
* current and one-iteration previous input velocity in the same axis as the output being processed
* current and one-iteration previous intermediate filter values in the same axis as the output being processed
* one-iteration previous filtered output in the axis being processed.

The weights of these terms may be either constant or non-constant.
Non-constant weights may vary according to axisymmetric and otherwise monotonically changing functions of:

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
6. "energy-state tracking low-pass filter" (Rienne's Goomwave firmware, **may need more rule tweaking or explicit permission once we know more about how it's implemented**)

The following techniques are explicitly prohibited:
1. Timers
2. Cross-axis interactions aside from radius measurements used as weights
3. Non symmetric thresholds or weights
4. Weights that both increase and decrease between center and rim

Prohibited filters include but are not limited to:
1. Timer-based pode emulation
2. Timer-based dashback out of crouch enhancement
3. Timer-based empty pivot enhancement
4. Angle- and timer-based ledgedash enhancement

Filters may be linearly chained so that the output of one is used as the input to the next. (you can use several filters in a row, but they must not go their separate ways and rejoin so as to get information from deep in the past)

### Digital Input, Analog Stick Outputs

#### Simultaneous Opposing Cardinal Direction resolution (SOCD)

When simultaneous opposing cardinal Digital Inputs are pressed, the output must be resolved according to Neutral SOCD: when opposing cardinals are pressed, the output must be 0 in that axis.

#### Coordinate Set Changing

When controlled by digital inputs, the target coordinates may not be changed during a match.

#### Digital Input, Control Stick Output

##### Coordinate Fuzzing ("RNG")

Each time the targeted coordinate changes, for each axis there must be a 50% chance that the actual destination coordinate is left unchanged from the targeted coordinate, a 25% chance that it is increased by one, and a 25% chance that it is decreased by one.

Exception: fuzzing is not required in an axis if that axis of the coordinate is 0.

The random number generation for each axis must be independent.

##### Linear Interpolation ("Travel Time")

Each time the targeted coordinate changes, the output must be linearly interpolated over time from the currently interpolated output position to the target coordinate.

The duration of the interpolation is determined by the radius of the targeted coordinate (pre-RNG) according to the following:

* X^2 + Y^2 <= 6184: 12ms (non-rim coordinates)
* 6185 <= X^2 + Y^2 <= 6857: 6ms (rim coordinates)
* 6858 <= X^2 + Y^2 <= 8978: 7ms (legal outside-of-melee-circle diagonal coordinates)
* 8979 <= X^2 + Y^2: 8ms (legal outside-of-melee-circle cardinal coordinates)

##### Coordinate Restrictions

With the following exceptions, all Control Stick coordinates targeted (pre-RNG) must lie inside the Melee unit circle (raw coordinate X^2 + Y^2 <= 6400).

Exceptions (in integer controller coordinates about the origin):

* |X| = 112, Y = 0 (1.0 X cardinal, no Y RNG)
* X = 0, |Y| = 112 (1.0 Y cardinal, no X RNG)
* |X| = 67, |Y| = 67 (perfect diagonal)
* |X| = 61, Y = -56 (guaranteed vanilla shield drop and crouch-jab option select)
* |X| = 56, Y = -61 (guaranteed jab while crouching with RNG, UCF shield drop)

The following Control Stick coordinates must not be targeted using Digital Inputs (prior to RNG fuzzing):

1. Cardinal/Quadrant Boundaries: X and Y ±0.2875 and ±0.3000 must not be accessible. These are on the quadrant boundaries and enable the steepest/shallowest angles, "mid-angle" tilts and smashes, tap jump short hop with the stick outside of the deadzone, double-jumping backwards with Yoshi/Jigglypuff/Kirby without turning around, and Nana Short Hop/Popo Full Hop.
2. Shield Drop Straight Down: Y = -0.6625, -0.6750, and -0.6875 must not be targeted while |X| < 0.7000 unless accessed via a combination of modifiers that includes a C-stick button. (the c-stick will buffer roll/spotdodge/jump instead of shield dropping)
3. Firefox Angles: All target coordinates must meet one of the following three criteria:
  * 20° < atan(|Y/X|) < 70°
  * |X| <= 0.2750 (within the X deadzone)
  * |Y| <= 0.2750 (within the Y deadzone)
4. Ice Climbers Desyncs: inputting any of these coordinates will cause each Ice Climber to perform different actions. Most of them are conditionally allowed given input coordinate fuzzing.
  * ~~X = ±0.8000: Popo Smash/Nana Tilt~~
  * ~~Y = ±0.6625: Popo Smash/Nana Tilt~~
  * ~~X = ±0.7000: Popo Roll, EXCEPT this is legal when Y = ±0.7000 since this is on the rim~~
  * ~~Y = -0.7000: Popo Spotdodge/Nana Shield Drop EXCEPT FOR X = ±0.7000~~
  * ~~X = +0.6250: Popo Run/Nana Runbrake~~
  * ~~X = +0.7500: Popo Teeter Break/Nana Teeter~~
  * ~~Y = +0.5625: Popo Jump out of Dash~~
  * ~~Y = +0.3000: Popo Full Hop/Nana Short Hop~~
  * |X| <= 0.5875, Y = -0.5500: Grounded Nana Solo Neutral-B, with a 1-unit keepout zone in all directions
  * X = +0.5250, Y = +0.6250: two different aerials, with a 1-unit keepout zone in all directions
  * X = -0.4375, Y = +0.5250: two different aerials, with a 1-unit keepout zone in all directions
5. 1-Frame Turnaround Uptilt and Downtilt
  * |X| >= 0.2875 AND -0.6875 <= Y <= 0.6500 AND atan(|Y/X|) > 50°
6. Aerial Up-B Without Midair Jump
  * Y >= 0.5500, Y <= 0.6500 (no keep-out zone)
7. Peach Parasol Dash 2f window: the following coordinates must be inaccessible
  * 56.95° <= atan(Y/|X|) <= 60.10° while Y >= 0.2875 (no 1-unit keep-out zone)
8. Stronger diagonal DI than accessible on stick:
  * |X|+|Y| = 1.4125
9. Pikachu/Pichu Double Up-B: The following four coordinates, which allow Pikachu and Pichu to move twice in the same direction during an Up-B, must not be accessible: (using any of these coordinates makes the second step go in the same direction as the first)
  * ~~X = ±0.5000, Y < ±0.2875~~ Note: may be banned in an update if found to be abusable at 50% chance
  * ~~X < ±0.2875, Y = ±0.5000~~ Note: may be banned in an update if found to be abusable at 50% chance
  * ~~X = ±0.4000, Y = ±0.3000~~
  * ~~X = ±0.3000, Y = ±0.4000~~

Conditionally Inaccessible Coordinates:

1. If one of the following coordinates occurs within at least 2 frames after the last input where Y < 0, the following coordinates must be promoted to a tap jump coordinate (X <= 0.7375, Y >= 0.6625, or equivalent beyond-80-radius coordinate) for at least 2 frames. This exists to prevent instant uptilt while crouching.
  * 0.2875 <= |Y| <= 0.6500
2. For at least 8 frames after the last input that has >=50% probability of succeeding at an empty pivot (crossing from one dash coordinate |X| >= 0.8 to the other within at least 15 frames, then remaining in the new dash coordinate between 0.5 and 1.5 frames inclusive), any coordinates meeting either of the following criteria must be replaced as specified:
  * 0.2875 <= Y <= 0.6500: Set Y to a tap jump coordinate (X <= 0.7375, Y >= 0.6625, or equivalent beyond-rim coordinate) as long as this slight up input is maintained.
  * -0.6500 <= Y <= -0.2875: Replace the angle with a coordinate of an equivalent angle (less than 0.5 degree difference) at a radius of at least 80.
3. Airdodge Angles: While L or R digital are pressed, all target coordinates must additionally meet one of the following three criteria. If L or R is used as a non-dedicated modifier, and if L or R is changed mid-interpolation, then the current interpolation in progress may proceed as if the target destination has always been the new destination, in order to prevent inherently inconsistent wavedash angles. If L and R are used as non-dedicated modifiers, then they must target the same coordinates.
  * 27° < atan(|Y/X|) < 73°
  * |X| <= 0.2750 (within the X deadzone)
  * |Y| <= 0.2750 (within the Y deadzone)
4. Instant Turnaround Neutral B: While B is pressed, the following target coordinates are prohibited. If these coordinates are accessible, B must be used as a non-dedicated modifier to increase the stick magnitude in the X direction so that the target coordinate no longer falls into this region.
  * 0.2875 <= |X| <= 0.5875
  * |Y| <= 0.5375

##### Smash Directional Influence Restrictions

Smash Directional Influence, or SDI, is performed by rapidly moving the control stick between zones on the stickmap, with up to one input per frame.

The zones are as follows:

* |X| > 0.7000, |Y| < 0.2875: X cardinal SDI zone
* |X| < 0.2875, |Y| > 0.7000: Y cardinal SDI zone
* |X| >= 0.2875, |Y| >= 0.2875, X^2 + Y^2 >= 3136: Diagonal SDI zone (radius > 0.7000, not in either stick deadzone)
* All other stick coordinates fall into the neutral SDI zone.

During hitlag, when the stick travels quickly from the center deadzone to any of the other zones, one SDI is performed proportional to the magnitude of the stick.
Additionally, when the stick travels from a cardinal or a diagonal zone to another diagonal zone, SDI is performed.

The first limitation on SDI is neutral SOCD, which prevents trivial three-consecutive input SDI by inputting a cardinal, a diagonal, and utilizing 2nd Input Priority SOCD to jump to the opposite diagonal without releasing any buttons.

There are, however, several additional explicit SDI restrictions.

1. If the target coordinate alternates between the neutral SDI zone and any of the other zones faster than once every 5.5 frames, SDI must be restricted to one movement.
2. If the target coordinate alternates between a cardinal SDI zone and either adjacent diagonal SDI zone faster than once every 5.5 frames, SDI must be restricted to one movement.
3. If the target coordinate alternates between two diagonal SDI zones adjacent to the same cardinal faster than once every 5.5 frames, SDI must be restricted to one movement.

A sequence of one cardinal SDI followed immediately by one diagonal SDI is not feasible to restrict without severely hampering playability, so digital inputs remain capable of two-consecutive input SDI.

##### Modifiers

Compared to the unmodified 8 primary directions, Modifiers may not move a coordinate in or out of any of the deadzones.

For any given set of Modifiers (dedicated and non-dedicated), it must not be possible to have coordinates where:

* When down is held, Y <= -0.6250, and down+side enters dash (one-button DBOOC)

Controllers may have up to 6 non-interacting Dedicated Modifiers, 3 pairwise-interacting Dedicated Modifiers, or 2 non-interacting Dedicated Modifiers plus 4 Non-Dedicated Modifiers that are used as C-Stick digital inputs.

If more modifiers are pressed than are allowed to be active, firmware may either ignore all modifiers or omit excess modifiers. This may be used as a shortcut to cause C buttons to produce D-Pad output.

B may be used as a non-dedicated modifier to increase radius so long as the angle does not change by more than 0.5 degrees.

#### Digital Input, C-Stick Output

C-Stick outputs are not subject to Coordinate Fuzzing or Linear Interpolation.

##### Coordinate Restrictions

The following C-Stick coordinates must not be accessible using Digital Inputs:

1. Cardinal/Quadrant Boundaries: X and Y ±0.2875 and ±0.3000 must not be accessible. These are on the quadrant boundaries and enable the steepest/shallowest angles, smashes.
1. Ice Climbers Desyncs:
  * X = ±0.8000: Popo Smash
  * Y = ±0.6625: Popo Smash
  * X = ±0.7000: Popo Roll EXCEPT FOR Y = ±0.7000
  * X = -0.7000: Popo Spotdodge EXCEPT FOR X = ±0.7000
  * Y = +0.6625: Popo Jump out of Shield
  * X = +0.5250, Y = +0.6250: two different aerials
  * X = -0.4375, Y = +0.5250: two different aerials
2. Stronger diagonal ASDI than is accessible on the analog stick rim:
  * |X|+|Y| = 1.4125

##### Modifiers

When the C-Stick outputs are influenced by digital inputs, up to two modified coordinate sets are permitted, controlled by either two dedicated modifier buttons or one dedicated and two non-dedicated modifier buttons.
The only permitted change to the coordinates from modifiers is that the left and right cardinals may cross the deadzone boundary in order to produce angled f-smashes without requiring frame-perfect simultaneous button presses.
No other coordinates, including the diagonals, may change.

## Analog Trigger Outputs

### General Analog Trigger Information

The Analog Trigger Outputs sent by the controller exist in a range from 0 to 255, but Melee caps the accepted value at 140.

Values 43 and greater produce an analog shield in Melee.

When Z is held, the resulting lightshield is equivalent to the lightshield from an Analog Trigger Output of 49.

### Analog Input, Analog Trigger Output

The Analog Trigger outputs may not be influenced by Full-Range Analog Inputs. (No defaulting to a middle value)

The default Output must be 0. (No defaulting to the max range)

Any Analog Inputs used to influence the Analog Trigger Outputs must have a resolution of at least 64 digital readout levels over the full Input motion range. (limit how coarse the resolution can be to limit the number of pinpoints available)

The Analog Input controlling an Analog Trigger Output may be the analog part of a CADI or Emulated CADI but if the digital part of the CADI is used it must Influence only the same trigger's Digital Output. (no having analog shield and a non-shield function on the same trigger)

If and only if the relation between the motion of an Analog Input's Actuator and the value it measures is nonlinear, the value must be linearized before being presented to the console as an Analog Trigger Output. (handle hall effect triggers)
This linearization must be a static mapping. (you can't switch behaviors)

Nonlinearization of this is permitted with the following restrictions:

The mapping between the linearized Analog Trigger Input and the Analog Trigger Output must be linear from 43 to 49 with a Y-intercept of 0. (this ensures that you can't easily pinpoint better-than-Z-lightshield)

The mapping between the linearized Analog Trigger Input and the Analog Trigger Output must be monotonically non-decreasing. (no on-off-on-off analog output for easy L-cancels)

Any nonlinear relation between the linearized Analog Trigger Input and the Analog Trigger Output must be a static mapping. (you can't switch behaviors)

Digital Input Filtering:
The Analog Trigger Output may be digitally filtered, or processed, to change its response.
All digital filtering of Analog Inputs for a given Analog Trigger must completely ignore all other Inputs on the controller.
If the filter output does not correspond directly to the filter input, the output shall be either stationary, moving towards, or accelerating towards the input to the filter. (similar restrictions to the stick filters)

Filters must be composed of weighted sums of the following values:

* current and one-iteration previous input position
* current and one-iteration previous input velocity
* current and one-iteration previous intermediate filter values
* one-iteration previous filtered output

The weights of these terms may be either constant or non-constant.
Non-constant weights may vary according monotonically changing functions of:

* current input position
* current input velocity
* current input acceleration
* current difference between input position and previous output position

A simple windowed median filter is also permitted, despite not meeting the above requirements.


### Digital Input, Analog Trigger Output

Each Analog Trigger Output may be influenced by at most a single standalone Digital Input, or a Modifier Input combined with the Digital Input corresponding to the same trigger's Digital Output.

The Analog Trigger Output value must default to 0.

The Analog Trigger Output value when influenced by Digital Inputs must not be from 43 to 48 inclusive. (prohibit better-than-Z lightshield)

If a Digital Input used to influence an Analog Trigger Output is part of a Combined Analog Digital Input, the Analog Input part of the CADI must not influence any Outputs. (once you use the digital part for a shield, the analog part can't be used for anything else, including the same shield)
